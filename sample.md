# Language samples
dart programing ကိုစတင်လေ့လာ လိုသူတွေအတွက် example တွေနဲ့ တကွလေ့လာနိုင်ပါတယ်။

## Hello World

app တိုင်းမှာ `main()` function ရှိရပါတယ်။ console မှာ စာသားတစ်ခုကို display လုပ်ပြဖို့ top-level `print()` function ကို သုံးရပါတယ်။

```dart
void main(){
    print('Hello, World!');
}
```

## Variables

type-safe Dart code မှာတောင် variable အများစုကို တိကျတဲ့ types တွေ ထည့်သွင်းရေးသားစရာ မလိုပါဘူး။

```dart
var name = 'Voyager I';
var year = 1997;
var antennaDiameter = 3.7;
var flybyObjects = ['Jupiter', 'Saturn', 'Uranus', 'Neptune'];
var image = {
    'tags': ['saturn'],
    'url': '//path/to/saturn.jpg'
};
```

## Control flow statements

dart မှာ ပုံမှန် control flow statement တွေကို သုံးလို့ရပါတယ်။

```dart
if(year>= 2001){
    print('21st century');
}else{
    print('20th century');
}

for(var object in flybyObjects){
    print(object);
}

for(int month = 1; month <= 12; month++){
    print(month);
}

while(year < 2016){
    year += 1;
}
```

## Functions

အကြံပြုချင်တာကတော့ function တိုင်းမှာ type တွေသတ်မှတ်ပေးဖို့နဲ့ value ကို return ပြန်ဖို့ဖြစ်ပါတယ်။

```dart
int fibonacci(int n){
    if(n == 0 || n == 1) return n;
    return fibonacci(n - 1) + fibonacci(n - 2);
}

var fibonacci(20);
```

အတိုကောက် `=>` (arrow) syntax ကတော့ statement တစ်ခုသာပါတဲ့ function တွေမှာ သုံးနိုင်ပါတယ်။

```dart
flybyObjects.where((name) => name.contains('turn')).forEach(print);
```
`where()` ရဲ့ argument က anonymous function တစ်ခုဖြစ်ပါတယ်။ ဒါကြောင့် dart မှာ function တွေက object ဖြစ်တယ်လို့ ဆိုတာပါ။ top-level `print()` function ကိုလည်း `forEach()` function ရဲ့ argument တစ်ခုအနေ သုံးထားတာ တွေ့မြင်နိုင်ပါတယ်။

## Comments
dart comments တွေ အမြဲတမ်း `//` နဲ့စပါတယ်။
```dart
// This is a normal, one-line comment.

/// Thie is a documentation comment, used to document libraries,
/// classes, and their members. Tools like IDEs and dartdoc treat
/// doc comment specially.

/* Commments like these are also supported. */
```

## Imports
အခြားသော libraries တွေထဲမှာ သတ်မှတ်ထားတဲ့ APIs တွေကို access လုပ်ဖို့ `import` ကို အသုံးပြုရပါတယ်။

```dart
// Importing core libraries
import 'dart:math';

// Importing libraries from external packages
import 'package:test/test.dart';

// Importing files
import 'path/to/my_other_file.dart';
```

## Classes
ဒါက properties (၃)ခု၊ constructor (၂)ခု၊ နဲ့ method (၁)ခု ပါဝင်တဲ့ class တစ်ခုရဲ့ example ဖြစ်ပါတယ်။ properties တွေထဲကမှ property တစ်ခုကို တိုက်ရိုက်သတ်မှတ်ပေးလို့ မရပါဘူး၊ သူ့ကိုသတ်မှတ်ပေးဖို့ အတွက် (variable တစ်ခုအစား) getter method တစ်ခုကို သုံးရပါတယ်။

```dart
class Spacecraft{
    String name;
    DateTime? launchDate;

    int? get launchYear => launchDate?.year; // read-only non-final property

    // Constructor, with syntactic sugar for assignment to members.
    Spacecraft(this.name, this.launchDate){
        // Initialization code goes here.
    }

    // Named constructor that forwards to the default one.
    Spacecraft.unlaunched(String name) : this(name, null);

    // Method
    void describe(){
        print('Spacecraft: $name');
        var launchDate = this.launchDate;
        if(launchDate != null){
            int years = DateTime.now().difference(launchDate).inDays ~/ 365;
            print('Launched: $launchYear ($years years ago)');
        }else{
            print('Unlaunched');
        }
    }
}
```

`Spacecraft` ကို အောက်ပါအတိုင်း ခေါ်ယူအသုံးပြုရမှာဖြစ်ပါတယ် 
```dart
var voyager = Spacecraft('Voyager I', DateTime(1977, 9, 5));
voyager.describe();

var voyager3 = Spacecraft.unlaunch('Voyager III');
voyager3.describe();
```

## Inheritance
Dart မှာ inheritance လုပ်ပုံတစ်ခုရှိပါတယ်
```dart
class Orbiter extends Spacecraft{
    double altitude;

    Orbiter(String name, DateTime launchDate, this.altitude) 
        : super(name, launchDate);
}
```

## Mixins
class hierarchies အများအပြားကို code မှာပြန်သုံးတဲ့ နည်းလမ်း တစ်ခုကတော့ mixins ကိုတွေ အသုံးပြုတဲ့ နည်းဖြစ်ပါတယ်။ mixin တစ်ခုကို အောက်ပါအတိုင်း ကြေငြာနိုင်ပါတယ်။

```dart
mixin Piloted {
    int astronauts = 1;

    void describeCrew(){
        print('Number of astronauts: $astronauts');
    }
}
```

mixin ရဲ့ capabilaties တွေကို class တစ်ခုသို့ ပေါင်းထည့်ဖို့အတွက် class ကို mixin နဲ့ extend လုပ်ပေးလိုက်ယုံသာဖြစ်ပါတယ်။

```dart
class PilotedCraft extends Spacecraft with Piloted {
    // ...
}
```
ခုဆိုရင် `PilotedCraft` မှာ `astronauts` fleld ရှိသွားပြီးဖြစ်ပါတယ်၊ `describeCrew()` method လည်းထိုအတိုင်းပင် ဖြစ်သွားပါတယ်။


## Interfaces and abstract classes
Dart မှာ `interface` ဆိုတဲ့ keyword မရှိပါဘူး။ classes အားလုံးကို interface အဖြစ်သတ်မှတ်ပြီးသားဖြစ်ပါတယ်။ ဒါကြောင့်မို့လို့ မည်သည့် class ကိုမဆို implement လုပ်လို့ရပါတယ်။

```dart
class MockSpaceship implements Spacecraft{
    // ...
}
```
concrete class တစ်ခုဖြင့် extended (or implemented) လုပ်ဖို့အတွက် abstract class တစ်ခုကို ဖန်တီးနိုင်ပါတယ်။ abstract classes တွေမှာ (body မှာ ဘာမှမပါတဲ့) abstract methods တွေထည့်နိုင်ပါတယ်။

```dart
abstract class Describable{
    void describe();

    void describeWithEmphasis(){
        print('=========');
        describe();
        print('=========');
    }
}
```
`Describsble` ကို extending လုပ်တဲ့ မည်သည့် class မဆို `describeWithEmphasis()` method ရှိသွားမှာဖြစ်ပါတယ်။ ထို method က `describe()` ရဲ့ extender ရဲ့ implementation ကို call လုပ်ပါတယ်။

## Async
callback hell ကို avoid လုပ်ပါတယ် ပြီးတော့ `async` နဲ့ `await` ကိုသုံးပြီးတော့ code တွေကို ပိုပြီး readable ဖြစ်အောင်လုပ်နိုင်ပါတယ်။

```dart
const oneSecond = Duration(seconds: 1);
// ...
Future<void> printWithDelay(String message) async {
    await Future.delayed(oneSecond);
    print(message);
}
```
အထက်မှာဖော်ပြထားတဲ့ method နဲ့ အတူတူပဲဖြစ်ပါတယ် 
```dart
Future<void> printWithDelay(String message){
    return Future.delayed(oneSecond).then((_){
        print(message);
    });
}
```

နောက် example မှာ asynchronous code ကို `async` နဲ့ `await` တို့ရဲ့ အကူအညီနဲ့ ဖတ်ရလွယ်အောင် ဆောင်ရွက်ထားပုံကို ဖော်ပြထားပါတယ်။

```dart
Future<void> createDescriptions(Iterable<String> objects) async {
    for(var object in objects){
        try{
            var file = File('$object.txt');
            if(await file.exists()){
                var modified = await file.lastModified();
                print('File for $object already exists. It was modified on $modified.');
                continue;
            }
            await file.create();
            await file.weiteAsString('Start describing $object in this file.');
        } on IOException catch(e){
            print('Cannot create description for $object: $e');
        }
    }
}
```
`async*` ကိုသုံးပြီးတော့လည်း streams တွေတည်ဆောက်ရာမှာ readable ကောင်းအောင်လုပ်နိုင်ပါတယ်။
```dart
Stream<String> report(Spacecraft craft, Iterable<String> objects) async*{
    for(var object in objects){
        await Future.delayed(oneSecond);
        yield '${craft.name} files by $object';
    }
}
```
## Exceptions
execption တစ်ခုကို eaise လုပ်ဖို့အတွက် `throw` ကိုသုံးရပါတယ် 
```dart
if(astronauts == 0){
    throw StateError('No astronauts.');
}
```

exception တစ်ခုကို catch လုပ်ဖို့ အတွက် `try` statement ကို `on` ဖြင့်သော်လည်းကောင်း၊ `catch` ဖြင့်သော်လည်းကောင်း၊ နှစ်ခုလုံးဖြင့် သော်လည်းကောင်း တွဲပြီးသုံးနိုင်ပါတယ်။
```dart
try{
    for(var object in flybyObjects){
        var description = await File('$object.txt').readAsString();
        print(description);
    }
} on IOException catch (e) {
    print('Could not describe object: $e');
} finally  {
    flybyObjects.clear();
}
```
အထက်ပါ code က asynchronous ဖြစ်ပါတယ်။ `try` က synchronous code နဲ့ `async` function ထဲမှာရှိတဲ့ code နှစ်ခုလုံးအတွက် အလုပ်လုပ်ပါတယ်။