# Dart programming လမ်းညွှန်

dart မှာပါဝင်တဲ့ အဓိက feature တွေကို ဘယ်လိုသုံးမလဲဆိုတာကို ဖော်ပြပေးသွားမှာဖြစ်ပါတယ်။ variables တွေ၊ classes တွေရဲ့ operators တွေ နဲ့ libraries တွေရဲ့ feature တွေကို အဓိကထား ဖော်ပြပေးသွားမှာ ဖြစ်ပါတယ်။ ဒီစာကိုနားလည်နိုင်ဖို့ အတွက်သင်က အခြားသော programming launguage တစ်ခု နဲ့ program တွေရေးသားနိုင်သူဖြစ်ရပါမယ်။ ခုမှစပြီးလေ့လာမည့်သူ အတွက်ကတော့ language samples ကို စတင်လေ့လာသင့်ပါတယ်။

dart ရဲ့ core library ကိုလေ့လာလိုလျှင် library tour ကိုလေ့လာပါ။ ပိုပြီးအသေးစိတ် လေ့လာချင်တယ်ဆိုရင်တော့ Dart language specification ကို လေ့လာနိုင်ပါတယ်။

> **Note:** Dart language ကို DartPad မှာ တိုက်ရိုက် run ပြီး စမ်းကြည့်နိုင်ပါတယ်။

## A basic Dart program

အောက်ပါ code တွေက dart မှာရှိတဲ့ အခြေခံ feature တွေကိုသုံးပြီး ရေးသားထားတာ ဖြစ်ပါတယ်။

```dart
// Define a function.
void printInteger(int aNumber){
    print('The number is $aNumber');
}

// This is where the app starts executing.
void main(){
    var number = 42; // Declare and initialize a variable.
    printInteger(number); // Call a function.
}
```

ဒါကတော့ program မှာသုံးထားတဲ့ အရာတွေဖြစ်ပါတယ်

**_`// This is a comment.`_**

Single-line comment တစ်ကြောင်းဖြစ်ပါတယ်။ Dart မှာ multi-line နဲ့ document comments ဆိုပြီး နှစ်မျိုးရှိပါသေးတယ်။

**`void`**

special type တစ်ခုဖြစ်ပြီး ဘယ်တော့မှ အသုံးမပြုတဲ့ value တစ်ခုကို indicate လုပ်ဖို့ဖြစ်ပါတယ်။ `printInteger()` နဲ့ `main()` တို့လို return value တစ်ခုပြန်ပေးစရာ မလိုတဲ့ function တွေမှာ `void` ကိုသုံးပါတယ်။

**`int`**

အခြား type တစ်ခုဖြစ်ပါတယ်။ integer တစ်ခုကို indicate လုပ်ဖို့ပါ။ အခြားသော built-in types တွေရှိပါသေးတယ် ၎င်းတို့မှာ `String`, `List` နဲ့ `bool` တို့ဖြစ်ပါတယ်။

**`42`**

number literal တစ်ခုဖြစ်ပါတယ်။ Number literals တွေက compile-time constant အမျိုးအစားတွေဖြစ်ပါတယ်။

**`print()`**

output ကို display လုပ်ဖို့ဖြစ်ပါတယ်။

**`'...'` (or `"..."`)**

String literal တစ်ခုဖြစ်ပါတယ်။

**`$variableName` (or `${expression}`)**

String interpolation: string literial တစ်ခုအတွင်းမှာ variable တစ်ခု ဒါမှမဟုတ် string ရဲ့ expression တစ်ခု ထည့်သွင်းနိုင်ပါတယ်။

**`main()`**

special တစ်ခုဖြစ်ပါတယ်၊ _မရှိမဖြစ်ဖြစ်ပါတယ်_၊ top-level function တစ်ဖြစ်ပြီး app exection ကိုထိုနေရာမှ စတင်မှာဖြစ်ပါတယ်။

**`var`**

variable တစ်ခုကို type သတ်မှတ်စရာမလိုပဲ ကြေငြာဖို့ နည်းလမ်းဖြစ်ပါတယ်။ ထိုကဲ့သို့သော variable (`int`) တွေရဲ့ type ကို သူတို့ရဲ့ initial value (`42`) ကို ကြည့်ပြီး ဆုံးဖြတ်တာ ဖြစ်ပါတယ်။

## Important concepts

Dart programing ကိုလေ့လာတဲ့အခါမှာ။ စွဲစွဲမြဲမြဲ မှတ်သားထားရမည့် အချက်တွေရှိပါတယ်

- variable တစ်ခုအတွင်း ထည့်လို့ရတဲ့ အရာမှန်သမျှက _object_ ဖြစ်ပါတယ်။ ပြီးတော့ object တိုင်းက _class_ တစ်ခုရဲ့ instance ဖြစ်ပါတယ်။ number, function နဲ့ `null` တို့တောင် object တွေဖြစ်ပါတယ်။ ရှိသမျှ object တိုင်းက Object class ကို inhert လုပ်ထားတာဖြစ်ပါတယ်။

> **Version note:** Null saftey ကို Dart 2.12 မှာ မိတ်ဆက်ခဲ့ပါတယ်။ null safty ကိုသုံးဖို့အတွက် အနည်းဆုံး language verson 2.12 လောက်လိုပါတယ်။

- မည်သိုပင်ဆိုစေ Dart က strongly typed ဖြစ်ပြီး type annotations တွေကတော့ optional ဖြစ်ပါတယ်။ ဘာဖြစ်လို့လဲဆိုတော့ Dart က types တွေကို infer လုပ်နိုင်သောကြောင့်ဖြစ်ပါတယ်။ အထက်မှာဖော်ပြခဲ့တဲ့ code မှာဆိုရင် `number` ကို `int` type အဖြစ် ကောချက်ချပါတယ်။

- null safety ကို ဖွင့်ထားတဲ့ အခါမှာ variable တွေမှာ `null` ထည့်လို့မရပါဘူး၊ ထည့်ချင်တယ်ဆိုရင်တော့ `null` ဖြစ်လို့ရကြောင်း ပြောပေးရမှာဖြစ်ပါတယ်။ variable ကို nullable လုပ်ဖို့အတွက် data type ရဲ့အဆုံးမှာ question mark (`?`) ထည့်ပေးနိုင်ပါတယ်။ ဥပမာ၊ `int?` type ရဲ့ variable က interger တစ်ခု ဖြစ်နိုင်သလို `null` လည်းဖြစ်နိုင်ပါတယ်။ expression တစ်ခုက ဘယ်တော့မှ `null` အဖြင့် တွက်ထုတ်မပေးနိုင်ကြောင်းကို သင်သိသော်လည်း Dart ကတော့ လက်မခံပါဘူး၊ ဒီလိုဆိုရင် `!` ကို ထည်ပြီးတော့ `null` မဖြစ်နိုင်ကြောင်း assert လုပ်နိုင်ပါတယ် (အကယ်၍များ `null` ဖြစ်ရင်တော့ exception တစ်ခုကို throw သွားပါလိမ့်မယ်)။ An example: `int x = nullableButNotNullInt!`

- မည်သည့် type မဆို လက်ခံကြောင်း ကြေငြာလိုလျှင်တော့ `Object?`(null safty ဖွင့်ပေးဖို့လို), `Object` ဒါမှမဟုတ် runtime မရောက်မှီ type ကို defer လုပ်လိုလျှင်တော့ `dynamic` ဆိုတဲ့ special type ကိုသုံးပေးရပါမယ်။

- Dart မှာ generic types တွေ support လုပ်ပေးပါတယ်။ ဥပမာ - `List<int>` (integer တွေရဲ့ list) or `List<Object>` (type တစ်ခုခုရဲ့ object တွေရဲ့ list)

- Dart မှာ (`main()` လိုမျိုး) top-level function တွေ support လုပ်ပေးပါတယ်။ function တွေက class သို့မဟုတ် object တို့ကို (_static_ နဲ့ _instance methods_ တွေနဲ့ အပြန်အလှန်) tied လုပ်နိုင်ပါတယ်။ function တွေထဲမှာ (_nested_ or _local_) function တွေလည်း တည်ဆောက်နိုင်ပါသေးတယ်။

- ထိုနည်းတူ Dart မှာ top-level _variables_ တွေ support လုပ်ပေးပါတယ်။ variable တွေက class သို့မဟုတ် object တို့ကို (_static_ နဲ့ _instance variable_ တွေနဲ့) tied လုပ်နိုင်ပါတယ်။ Instance variable တွေကို တစ်ခါတရံမှာ _fields_ သို့မဟုတ် _properties_ တွေလို ခေါ်ကြပါတယ်။

- Java နဲ့ မတူတာက Dart မှာ `public`, `protected` နဲ့ `private` တို့လို keywords တွေမရှိပါဘူး။ identifier တစ်ခုမှာ underscore (\_) နဲ့ စပြီးရေးထားရင် ထို identifier က သူ့ library အတွက် private ဖြစ်ပါတယ်။

- _Identifiers_ တွေကို later သို့မဟုတ် underscore (\_) တစ်ခုနဲ့ စတင်ရေးသားနိုင်ပါတယ်။

- Dart မှာ _expressions_ (runtime values ရှိ) တွေကော _statements_(မရှိ) တွေကောရှိပါတယ်။ ဥပမာ conditional expression ဖြစ်တဲ့ `condition ? expr1 : expr2` မှာဆိုရင် `expr1` သို့မဟုတ် `expr2` တို့ရဲ့ value ရှိရပါတယ်။ **if-else** statement နှင့်ယှဉ်လိုက်တဲ့ အခါမှာ သူတို့မှာ value မရှိတော့ပါဘူး။ statement တစ်ခုမှာ တစ်ခုနဲ့ တစ်ခုထက်ပိုတဲ့ expressions တွေပါတတ်ပါတယ်၊ သို့သော် expression မှာကြတော့ statement တစ်ခုကို တိုက်ရိုက် ထည့်လို့ မရနိုင်ပါဘူး။

- dart tools တွေမှာ _warnings_ နဲ့ _errors_ ဆိုတဲ့ problems တွေကို report ပြန်ပေးပါတယ်။ Warnings တွေက code ကအလုပ်မလုပ်ကြောင်း ညွှန်ပြပေးပါတယ် သို့သော် program ကို executing လုပ်ရာမှာ အတားအစီးတော့ မရှိနိုင်ပါဘူး။ errors တွေမှာတော့ compile-time မှာ ဖြစ်နိုင်သလို run-time မှာလည်းဖြစ်နိုင်ပါတယ်။ complie-time error မှာတော့ code အားလုံးကို execute လုပ်လို့မရတော့ပါဘူး။ run-time error result ကတော့ code execute လုပ်စဉ်မှာ exception တစ်ခုအဖြစ်နဲ့ ဖော်ပြပါတယ်။

## Keywords

အောက်ပါ စာလုံးများမှာ Dart language မှာ အထူးသုံးတဲ့ စာလုံးတွေပဲဖြစ်ပါတယ်။

|                        |                         |                        |                      |
| :--------------------- | :---------------------- | :--------------------- | :------------------- |
| abstract <sup>2</sup>  | else                    | import <sup>2</sup>    | show <sup>1</sup>    |
| as <sup>2</sup>        | enum                    | in                     | static <sup>2</sup>  |
| assert                 | export <sup>2</sup>     | interface <sup>2</sup> | super                |
| async <sup>1</sup>     | extends                 | is                     | switch               |
| await <sup>3</sup>     | extension <sup>2</sup>  | late <sup>2</sup>      | sync <sup>1</sup>    |
| break                  | external <sup>2</sup>   | library <sup>2</sup>   | this                 |
| case                   | factory <sup>2</sup>    | mixin <sup>2</sup>     | throw                |
| catch                  | false                   | new                    | true                 |
| class                  | final                   | null                   | try                  |
| const                  | finally                 | on <sup>1</sup>        | typedef <sup>2</sup> |
| continue               | for                     | operator <sup>2</sup>  | var                  |
| covariant <sup>2</sup> | Function <sup>2</sup>   | part <sup>2</sup>      | void                 |
| default                | get <sup>2</sup>        | required <sup>2</sup>  | while                |
| deferred <sup>2</sup>  | hide <sup>1</sup>       | rethrow                | with                 |
| do                     | if                      | return                 | yield <sup>3</sup>   |
| dynamic <sup>2</sup>   | implements <sup>2</sup> | set <sup>2</sup>       |                      |

ထိုစားလုံးတွေကို identifier အနေနဲ့ အသုံးပြုလို့မရပါဘူး။ မည်သို့ဆိုစေ လိုအပ်လာပြီဆိုရင်တော့ superscripts တွေနဲ့ မှတ်ထားတဲ့ keywords တွေကိုတော့ identifier အနေနဲ့ အသုံးပြုနိုင်ပါတယ်။

- superscript **1** ပေးထားတဲ့ စာလုံးတွေက **contextual keywords** တွေဖြစ်ကြပါတယ်၊ သတ်မှတ်ထားတဲ့ အချို့နေရာတွေမှာသာ အဓိပ္ပာယ်ရှိတာပါ။ identifier အဖြစ်သုံးမယ်ဆိုရင် မှားတော့မမှားပါဘူး။

- superscript **2** ပေးထားတဲ့ စာလုံးတွေက **built-in identifiers** တွေဖြစ်ပါတယ်။ JavaScript code ကနေ Dart ကို porting လုပ်တဲ့ task ကို ရိုးရှင်းအောင် လုပ်ဖို့ဖြစ်ပါတယ်။ နေရာတော်တော်များများမှာ ထို keyword တွေကို identifier အဖြစ် သုံးမယ်ဆို valid ဖြစ်ပါတယ်။ သို့သော် class name သို့မဟုတ် type name သို့မဟုတ် import prefixes တွေအနေနဲ့တော့ အသုံးပြုလို့မရနိုင်ပါဘူး။

- superscript **3** ပေးထားတဲ့ စာလုံးတွေက asynchrony support နဲပတ်သက်ပြီး သီးသန့်ထားတဲ့ စကားလုံးတွေဖြစ်ပါတယ်။ `await` တို့ `yield` တို့ကို `async`, `async*`, နဲ့ `sync*` တို့နဲ့ function body မှာ marked လုပ်ထားတဲ့ ကြိုက်တဲ့ function မှာ identifier အဖြင့်သုံးနိုင်ပါတယ်။

အခြားစာလုံးတွေကတော့ သီးသန့်ထားတဲ့ စာလုံးတွေဖြစ်လို့ identifier အဖြစ်နဲ့ သုံးလို့မရပါဘူး။

## Variables

ဒါကတော့ variable တစ်ခုတည်ဆောက်ပုံနဲ့ သူ့ကို initializing လုပ်ပုံဖြစ်ပါတယ်

```dart
var name = 'Bob';
```

Variables တွေက references တွေကို store လုပ်ပါတယ်။ `name` လို့ခေါ်တဲ့ variable က `String` Object တစ်ခုကို ကိုစားပြုထားပြီး "Bob" ဆိုတဲ့ value ရှိပါတယ်။

`name` variable ရဲ့ type ကို `String` လို့ ကောက်ချက်ချထားပါတယ်။ သို့သော် သင်ကိုယ်တိုင် တိကျတဲ့ type ကို သတ်မှတ်ပေးနိုင်ပါတယ်။ တကယ်လို့ object တစ်ခုကို single type လို့ ကန့်သပ်ချက်မထားတော့ဘူးဆိုရင် `Object` type (သို့မဟုတ် `dynamic` \*လိုမှသာ) နဲ့ သတ်မှတ်နိုင်ပါတယ်။

```dart
Object name = 'Bob';
```

နောက်ထပ် ရွေးစရာကတော့ type ကို အတိအကျ သတ်မှတ်ပေးတာဖြစ်ပါတယ်

```dart
String name = 'Bob';
```

### Default value

Uninitialized variables တွေက nullable type တွေဖြစ်သွားပြီးတော့ သူတို့မှာ `null` ဆိုတဲ့တန်ဖိုး ကို initial အနေနဲ့ ရှိကုန်ပါတယ်။ (null safty ကိုဖွင့်မထားဘူးဆိုရင် variable အားလုံးက nullable type ဖြစ်မှာပါ။) Numeric type ဖြစ်တဲ့ variable တွေတောင် အစပိုင်းမှာ null ဖြစ်ကြပါတယ်၊ ဘာဖြစ်လို့လဲဆိုတော့ Dart မှာရှိတဲ့ အရာအားလုံးက objects တွေဖြစ်သောကြောင့် ဖြစ်သည်။

```dart
int? lineCount;
assert(lineCount == null);
```

> **Note:** Production code မှာ `assert()` call ကို ignore လုပ်ပါတယ်။ development လုပ်စဉ်မှာ၊ တနည်း `assert(condition)` မှာ _condition_ က false ဖြစ်တဲ့ အခါမှာ exception တစ်ခုကို throw လုပ်ပါတယ်။

null safty ကိုဖွင့်ထားတယ်ဆိုရင် non-nullable variable ကို မသုံးခင် initialize value တစ်ခု ထည့်ကို ထည့်ပေးရမှာ ဖြစ်ပါတယ်။

```dart
int lineCount = 0;
```

local variable တစ်ခုကို ကြေငြာခဲ့တဲ့နေရာမှာ initialize မလုပ်ခဲ့ဘူးဆိုရင်၊ သူကိုမသုံးခင်မှာတော့ value တစ်ခုကို assign လုပ်ပေးဖို့လိုပါတယ်။ ဥပမာ - အောက်က code က valid ဖြစ်ပါတယ်၊ ဘာဖြစ်လို့လဲဆိုတော့ Dart က `print()` မလုပ်ခင်လေးမှာ `lineCount` က none-null ဖြစ်သွားတာကို detect လုပ်မိသွားလို့ဖြစ်ပါတယ်။

```dart
int lineCount;

if(weLikeToCount){
    lineCount = countLine();
}else{
    lineCount = 0;
}

print(lineCount);
```

### Late Variables

Dart 1.12 မှာ `late` modifier ထည့်ပေးပါတယ်။ ၎င်းကို အကြောင်းနှစ်မျိုးကြောင့်သုံးပါတယ် -

- non-nullable variable ရာမှာ declaration လုပ်ပြီးရင် initialized လုပ်ဖို့။
- variable တစ်ခုကို Lazily initializing လုပ်ဖို့

non-nullable variable ကို non-null value တစ်ခုနဲ့ မသုံးခင်မှာ set လုပ်ခဲ့လားဆိုတာကို မကြာခနဆိုသလို Dart ရဲ့ control flow analysis က detect လုပ်တယ်၊ တစ်ခါတစ်လေကျတော့လဲ fails ဖြစ်တာပေါ့။ ထိုကဲ့သို့သော ဘုံပြဿနာ နှစ်ခုစလုံးက top-level variables နဲ့ instance variables မှာတွေဖြစ်တတ်ကြတယ် - Dart က မကြာခန သူတို့မှာဘာတွေ set လုပ်ထားလဲဆိုတာကို ဆုံးဖြတ်မပေးနိုင်ဘူး၊ ဆက်လည်း ကြိုးစားမကြည့်တော့ဘူး။

variable ကိုမသုံးခင်မှာ set လုပ်ခဲ့လား ဆိုတာ မင်းဘက်က သေချာအောင်လုပ်ခဲ့ပေနဲ့ dart ကတော့ ယုံမှာမဟုတ်ဘူး။ ဒီလိုပြဿနာမျိုးကိုဖြေရှင်းဖို့အတွက် variable ကို နောက်မှ set လုပ်မှာဖြစ်ကြောင်း `late` လုပ်ထားဖို့လိုတယ်။

```dart
late String description;

void main(){
    description = 'Fejioada!';
    print(description);
}
```

> **Warning** `late` variable ကို initialize လုပ်ဖို့ မေ့သွားခဲ့ရင် variable ကိုသုံးတဲ့ အခါမှာ runtime error တက်ပေးမှာဖြစ်ပါတယ်။

variable တစ်ခုကို `lake` လုပ်ထားတဲ့ အပြင် သင်က declaration လုပ်စဉ်မှာပဲ initialize လုပ်ထားတယ်ဆိုရင်၊ ထို variable သုံးတဲ့အခါမှ initializer ကို စပြီး run မှာဖြစ်ပါတယ်။ ထို lazy initialization ကို ပြဿနာနှစ်ခုကို ကိုင်တွယ်ဖို့ သုံပါတယ် -

- variable လိုတော့မလိုဘူး၊ initializing လုပ်ဖို့က အဓိက လိုတာမျိုး။
- instance variable တစ်ခုကို သင်က initializing လုပ်နေတယ် ပြီးတော့ သူ့ရဲ့ initializer က `this` ကို access လုပ်ဖို့လိုတဲ့ အခါမျိုး။

အောက်ပါ example မှာ `temperature` variable ကို ဘယ်တုန်းကမှ မသုံးပါဘူး။ ထိုကြောင့်မို့လို့ လေးလံတဲ့ `_readThermometer()` function ကို မခေါ်ပါဘူး။ သုံးမှ run မယ်ဆိုတဲ့ သဘောပါ။

```dart
// This is the program's only call to _readThermometer().
late temperature = _readThermometer(); // Lazily initialized.
```

### Final and const

variable တစ်ခုကို ဘယ်တော့မှ တန်းဖိုး မပြောင်းတော့ ဘူးလို့ ရည်ရွယ်ထားရင် `var` သို့မဟုတ် အခြား type တွေအစား `final` ဒါမှမဟုတ် `const` ကို သုံးပေးရပါတယ်။ final variable ကို တစ်ကြိမ်ပဲ set လုပ်လို့ရပါတယ်။ const variable ကတော့ complie-time constant တစ်ခုဖြစ်ပါတယ်. (const variable တွေဟာ အကြွင်းမဲ့ final ဖြစ်ပါတယ်၊) final top-level (သို့) class variable ကို ပထမဆုံးကြိမ် အသုံးပြုစဉ်မှာ initialized လုပ်ပါတယ်။

> **Note:** Instance Variables တွေက `final` နဲ့မှရမှာပါ `const` သုံးလို့မရပါဘူး။

ဒါကတော့ `final` variable တစ်ခုကို ဖန်တီးပုံဖြစ်ပါတယ်။

```dart
final name = 'Bob'; // Without a type annotation
final String nickname = `Bobby`;
```

`final` variable တစ်ခုရဲ value ကို ပြောင်းလို့မရပါဘူး

<p style="color:red; font-size:0.9em; margin-bottom: -23px; margin-left: 10px;">❌&nbsp;&nbsp;&nbsp;static analysis: error/warning</p>

```dart

name = 'Alice'; // Error: a final variable can only be set once.
```

variables တွေအတွက် **compile-time-constants** တွေကိုလိုချင်တဲ့ အခါမှာ `const` ကိုသုံးရပါတယ်။ const variable က class level မှာဆိုရင် `static const` နဲ့မှတ်ရပါတယ်။ variable ကြေငြာတဲ့နေရာမှာ value ကို compile-time constant တွေသတ်မှတ်ပေးနိုင်ပါတယ်။ ဘယ်လိုတွေလဲဆိုတော့ number သို့မဟုတ် string literal, constant variable, သို့မဟုတ် constant numbers တွေနေရာမှာ arithmetic operation တို့လိုတွေ သတ်မှတ်ပေးလို့ရပါတယ်။

```dart
const bar = 100000; // Unit of pressure (dynes/cm2)
const double atm = 1.01325 * bar; // Standard atmosphere
```

`const` keyword က constant variable တွေကြေငြာဖို့ လုံးဝမဟုတ်ပါဘူး။ constant _values_ တွေကြေငြာဖို့လည်းသုံးနိုင်ပါတယ်၊ costant values တွေ ဖန်တီးတဲ့ constructor တွေကြေငြာဖို့လည်းဖြစ်ပါတယ်။ variable တိုင်းမှာ constant value တစ်ခုရှိနိုင်ပါတယ်။

```dart
var foo = const [];
final bar = const [];
const baz = []; // Equivalent to `const []`
```

`baz` လိုမျိုး `const` declaration တစ်ခုရဲ့ initializing expression မှာ `const` ကို omit လုပ်နိုင်ပါတယ်။ const redundantly ကိုမသုံးရပါဘူး။

`const` ကိုသုံးထားပေနဲ့ non-final, non-const variable တွေရဲ့ တန်ဖိုးကို ပြောင်းလည်းသတ်မှတ်လို့ ရပါတယ်။

```dart
foo = [1, 2, 3];
```

`const` variable တစ်ခုရဲ့တန်ဖိုးကို ပြောင်းလဲသတ်မှတ်လို့မရပါဘူး။

<p style="color:red; font-size:0.9em; margin-bottom: -23px; margin-left: 10px;">❌&nbsp;&nbsp;&nbsp;static analysis: error/warning</p>

```dart

baz = [42]; // Error: Constant variable cant't be assigned a value.
```

**type checks and casts** (`is` and `as`), **collection if**, and **spread operators** (`...` and `...?`) တွေကို သုံးထားတဲ့ constants တွေကိုလည်း define လုပ်နိုင်ပါတယ်။

```dart
const Object i = 3; // Where i is a const Object with an int value...
const list = [i as int]; // Use a typecast.
const map = {if (i is int) i : 'int'}; // Use is and collection if.
const set = {if (list is List<int>) ...list}; // ...and a spread.
```

> **Note:** `final` object ကို modified လုပ်လို့မရပေနဲ့ သူ့ရဲ့ fields တွေကိုတော့ ပြောင်းလို့ရပါတယ်။ `const` နဲ့ ယှဉ်လျှင် သူ့ fields တွေကို ပြောင်းလဲသတ်မှတ်လို့ မရတာ ကွာတာပါ။ သူတို့တွေက immutable ဖြစ်ပါတယ်။

## Built-in types

Dart language မှာ အောက်ပါတို့ကို အထူး support လုပ်ပါတယ်။

- Numbers (`int`,`double`)
- Strings (`String`)
- Booleans (`bool`)
- Lists (`List`, also known as _arrays_)
- Sets (`Set`)
- Maps (`Map`)
- Runes (`Runes`; often replaced by the `characters` API)
- Symbols (`Symbols`)
- The value `null` (`Null`)

literals တွေကိုသုံးပြီး ဖန်တီးထားတဲ့ objects တွေကို သူတို့ရဲ့ abality တွေကို support လုပ်ပေးပါတယ်။ ဥပမာ `'this is a string'` က string literal တစ်ခုဖြစ်ပြီးတော့၊ `true` ကတော့ boolean literal တစ်ခုဖြစ်ပါတယ်။

ဘာဖြစ်လို့လဲဆိုတော့ Dart မှာရှိတဲ့ variable အားလုံးတို့က object တစ်ခုကို refers လုပ်ပြီးတော့ - _class_ တစ်ခုရဲ့ instance ဖြစ်သောကြောင့်ဖြစ်ပါတယ်။ _constructors_ တွေသုံးပြီးတော့ variables တွေကို initialize လုပ်လို့ရပါသေးတယ်။ အချို့သော built-in type တွေမှာ သူတို့ကိုယ်ပိုင် constructors တွေရှိပါတယ်။ ဥပမာ `Map()` constructor ကိုသုံးပြီးတော့ map တစ်ခုကိုဖန်တီးနိုင်ပါတယ်။

Dart မှာရှိတဲ့ အချို့သော type တွေမှာ လည်းပဲ special role တွေရှိပါတယ်၊

- **`Object`:** `Null` ကလွဲလို့ Dart မှာရှိသမျှ class အားလုံးရဲ့ superclass ဖြစ်ပါတယ်။

- **`Future` and `Stream`:** asynchrony support အတွက်သုံးပါတယ်။

- **`Iterable`:** _for-in loop_ နဲ့ synchronous generator functions တွေမှာ သုံးပါတယ်။

- **`Never`:** expression တစ်ခုက evealuating လုပ်ရာမှာ ဘယ်တော့မှ ပြီးမသွားနိုင်ဘူးဆိုတာကို indicate လုပ်ဖို့ဖြစ်ပါတယ်။ functions တွေအတွက် သုံးတာဖြစ်ပြီး ၎င်းက exception တစ်ခုကို အမြဲ throw လုပ်ပါတယ်။

- **`dynamic`:** static chacking ကို disable လုပ်ချင်ကြောင်း indicate လုပ်ဖို့ဖြစ်ပါတယ်။ သူအစား `Object` သို့မဟုတ် `Object?` ကို အမြဲသုံးသင့်ပါတယ်။

- **`void`:** value တစ်ကို ဘယ်တော့မှ မသုံးကြောင်း indicate လုပ်ဖို့ဖြစ်ပါတယ်။ တစ်ခါတစ်လေမှာ return type သဖွယ်သုံးပါတယ်။

`Object`,`Object?`,`Null` နဲ့ `Never` classes တွေမှာ class အဆင့်ဆင့်အလိုက် special roles တွေရှိပါတယ်။ null safty အကြောင်းရှင်းထားတဲ့ top-and-bottom section မှာ ဖော်ပြပေးထားပါတယ်။

### Numbers

Dart မှာ number နှစ်မျိုးရှိပါတယ်။

**`int`**

integer values တွေက platform ပေါ်မူတည်ပြီး 64bits ထက်ပိုမကြီးပါဘူး။ Native paltforms တွေ values တွေက -2<sup>63</sup> ကနေ 2<sup>63</sup> - 1 အထိရှိနိုင်ပါတယ်။ Web မှာတော့ integer values တွေက JavaScript numbers (64-bit floating-point values with no fractional part) တွေအဖြစ်နဲ့ represent လုပ်ပါတယ်။ -2<sup>53</sup> ကနေ 2<sup>53</sup> - 1 အထိရှိနိုင်ပါတယ်။

**`double`**

64-bit (double-precision) floating-point numbers တွေကို IEEE 754 standard နဲ့ specified လုပ်ပါတယ်။

`int` ကော `double` ကောက `num` ရဲ့ subtypes တွေဖြစ်ကြပါတယ်။ num type မှာဆိုရင် အခြေခံ operators တွေဖြစ်တဲ့ +, - , \* , / တွေနဲ့ `abs()`, `ceil()` နဲ့ `floor()` တို့လို့ methods တွေလည်း ရှိပါတယ်။ (`>>` ဒီလိုမျိုး bitwise operators တွေကြတော့ `int` class ထဲမှာ သတ်မှတ်ထားတာပါ။) num ဖြစ်ပြီး subtypes တွေက ဘာတွေမှန်းမသိတဲ့ အခါမှာ `darth:math` library မှာ ရှာကြည့်သင့်ပါတယ်။

integer ဆိုတာ decimal point မပါတဲ့ number ဖြစ်ပါတယ်။ ဒါကတော့ integer literals တွေကို defining လုပ်ပုံ example အချို့ဖြစ်ပါတယ်။

```dart
var x = 1;
var hex = 0xDEADBEEF;
var exponent = 8e5;
```

number မှာ decimal တစ်ခုပါပြီဆိုရင် အဲတာက double ဖြစ်ပါတယ်။ ဒါကတော့ double literals တွေသတ်မှတ်ပေးပုံ example အချို့ဖြစ်ပါတယ်။

```dart
var y = 1.1;
var exponents = 1.42e5;
```

num တစ်ခုအဖြစ်လဲ variable ကိုကြေငြာနိုင်ပါတယ် ,variable က integer လဲဖြစ်နိုင်တယ် double ဖြစ်နိုင်တယ် ဆိုရင် အောက်ကအတိုင်းလုပ်ပါ။

```dart
num x = 1; // x can have both int and double values
x += 2.5;
```

လိုအပ်တဲ့အခါမှာ integer literals တွေကို double အဖြစ် automatic ကြေငြာပေးနိုင်ပါတယ်။

```dart
double z = 1; // Equivalent to double z = 1.0.
```

ဒါကတော့ string ကို number အဖြစ်ပြောင်းတာဖြစ်ပြီး၊ အပြန်အလှန် number ကနေ string အဖြစ်ပြောင်းတာဖြစ်ပါတယ်။

```dart
// String -> int
var one = int.parse('1');
assert(one == 1);

// String -> double
var onePointOne = double.parse('1.1');
assert(onePointOne == 1.1);

// int -> String
String oneAsString = 1.toString();
assert(oneAsString == '1');

// double -> String
String piAsString = 3.14159.toStringAsFixed(2);
assert(piAsString == '3.14');
```

int type မှာ traditional bitwise shift (<<, >>), AND (&), and OR (|) operators တွေ သတ်မှတ်ပေးလို့ရပါတယ်။ ဥပမာ -

```dart
assert((3 << 1) == 6); // 0011 << 1 == 0110
assert((3 >> 1) == 1); // 0011 >> 1 == 0001
assert((3 | 4) == 7); // 0011 | 0101 == 0111
```

literal numbers တွေက compile-time constants တွေဖြစ်ကြပါတယ်။ arithmetic expressions တော်တော်များများကလည်း compile-time constants တွေဖြစ်ကြပါတယ်။ သူတို့ရဲ့ operands တွေကလည်း compile-time constant တွေဖြစ်ကြပြီး numbers တွေကို တွက်ထုတ်ကြပါတယ်။

```dart
const msPerSecond = 1000;
const secondsUntilRetry = 5;
const msUntilRetry = secondsUntilsRetry - msPerSecond;
```

### Strings

Dart string (`String` Object) က UTF-16 code units ရဲ့ sequence တစ်ခုဖြစ်ပါတယ်။ string တစ်ခုကို ဖန်တီးဖို့အတွက် single သို့မဟုတ် double quotes တွေကို သုံးရပါတယ်။

```dart
var s1 = 'Single quotes work will for string literals.';
var s2 = "Double quotes work just as well.";
var s3 = 'It\'s easy to escapse the string delimiter.';
var s4 = "It's even easier to use the other delimiter.";
```

`${expression}` ကိုသုံးပြီးတော့ expression တစ်ခုရဲ့ value ကို string အတွင်းမှာ ထည့်သွင်းနိုင်ပါတယ်။ တကယ်လို့ expression က identifier တစ်ခုဖြစ်ခဲ့လျှင် {} မထည့်လည်းရပါတယ်။ object တစ်ခုကနေ လိုက်လျောညီထွေတဲ့ string တစ်ခုကို ရလိုလျှင်တော့ object ရဲ့ `toString()` method ကို call လုပ်ပါ။

```dart
var s = 'string interpolation';
assert('Dart has $s, which is very handy.' ==
    'Dart has string interpolation, ' +
    'which is very handy.');
assert('That deserves all caps. ' +
    '${s.toUpperCase()} is very handy!' ==
    'That deserves all caps. ' +
    'STRING INTERPOLATION is very handy!');
```

> **Note:** `==` operator က object နှစ်ခုက equivalent ဖြစ်ကြောင်း tests လုပ်ဖို့ဖြစ်ပါတယ်။ code units တွေရဲ့ တူညီတဲ့ sequence တွေပါဝင်ရင် ထို string နှစ်ခုက equivalent ဖြစ်ပါတယ်။

string နှစ်ခုကို `+` operator သို့မဟုတ် adjacent string literals တွေသုံးပြီးတော့ ပေါင်းစပ်နိုင်ပါတယ်။

```dart
var s1 = 'String '
    'concentration'
    " works even over line breaks";

assert(s1 = 'String concatenation works even over '
    'line breaks.');

var s2 = 'The + operator ' + 'works, as well.';
assert(s2 == 'The + operator works, as well.');
```

multi-line string တွေကို quote သုံးခုနဲ့ ဖန်တီးနိုင်းပါတယ်။ single သို့မဟုတ် double quotation marks တစ်ခုခုနဲ့ သုံးနိုင်ပါတယ်။

```dart
var s1 = '''
You can create
multi-line strings like this one.
''';

var s2 = """This is also a
multi-line string.""";
```

"raw" string တစ်ခုကို `r` နဲ့ prefixing လုပ်ပြီးတော့ဖန်တီးနိုင်ပါတယ်၊

```dart
var s = r'In a raw string, not even \n gets special treatment.';
```

နောက်ပိုင်းမှာ unicode characters တွေကို string တစ်ခုအတွင်းမှာ ဘယ်လိုသုံးမလဲဆိုတာကိုဖော်ပြပေးထားပါတယ်။

literal strings တွေမှာ (null or a numeric, string, or boolean value တွေရအောင် တွက်ထုတ်ပေးရမည့်) interpolated expression တစ်ခုခုပါဝင်နေရင် ထိို literal strings တွေက compile-time constants တွေဖြစ်ကြပါတယ်။ const literal မှာ const တွေပဲထပ်ပါဝင်ခွင့်ရှိတယ်။ ပြောင်းလဲတတ်တဲ့ တန်ဖိုးတွေ ပါလို့မရဘူးဆိုတဲ့ သဘောပါ)။

```dart
// These work in a const string.
const aConstNum = 0;
const aConstBool = true;
const aConstString = 'a constant string';

// These do NOT work in a const string.
var aNum = 0;
var aBool = true;
var aString = 'a string';
const aConstList = [1, 2, 3];

const validConstString = '$aConstNum $aConstBool $aConstString';
//const invalidConstString = '$aNum $aBool $aString $aConstList';

```

String and regular expressions မှာ strings တွေအကြောင်းထပ်ရှင်းပြထားပါသေးတယ်။

### Booleans

Dart မှာ boolean values တွေကို `bool` type name နဲ့ represent လုပ်ပါတယ်။ type bool မှာ object နှစ်မျိုးသာပါဝင်ပါတယ်။ boolean literals တွေကတော့ `true` နဲ့ `false` တို့ဖြစ်ကြပါတယ်။ ထိုနှစ်ခုလုံးက compile-time constant တွေဖြစ်ကြပါတယ်။

Dart ရဲ့ type safty အရ code ကို `if (nonbooleanValue)` or `assert (nonbooleanValue)` တွေလို ရေးသားလို့မရပါဘူး။ ၎င်းအစား values တွေကို check ဖို့အတွက် အောက်ပါအတိုင်းရေးနိုင်ပါတယ်။

```dart
// Check for an empty string.
var fullName = '';
assert(fullName.isEmpty);

// Check for zero
var hitPoints = 0;
assert(hitPoints <= 0);

// Check for null.
var unicorn;
assert(unicorn == null);

// Check for NaN.
var iMentToDoThis = 0/0;
assert(iMentToDoThis == NaN);
```

### Lists

programming languages တော်တော်များများမှာ အသုံးများတဲ့ collection တွေက _array_ သို့မဟုတ် ordered group of objects ဖြစ်ပါတယ်။ Dart မှာရှိတဲ့ arrays တွေကတော့ `List` objects တွေဖြစ်ပါတယ်။ အများစုကတော့ _lists_ လို့ခေါ်ကြပါတယ်။

Dart ရဲ့ list literals တွေက JavaScript array literals တွေနဲ့ တူပါတယ်။ ဒါကတော့ simple Dart list တစ်ခုဖြစ်ပါတယ်။

```dart
var list = [1, 2, 3];
```

> **Note:** ထို `list` က `List<int>` type ကနေ ဆင်းသက်လာတာဖြစ်ပါတယ်။ ထို list ထဲကို non-integer object တစ်ခုထည့်ဖို့ကြိုးစားရင် analyzer ဒါမှမဟုတ် runtime က error တစ်ခုကို ပြပါလိမ့်မယ်။ ထိုအကြောင်းကို [type inference](https://dart.dev/guides/language/type-system#type-inference) မှာဖတ်နိုင်ပါတယ်။

Dart collection literal တစ်ခုရဲ့ နောက်ဆုံး item ရဲ့ နောက်မှာ comma တစ်ခုထည့်ပေးလို့ရပါတယ်။ ထို _trailing comma_ က collection အပေါ်မှာ အကျိုးသက်ရောက်မှုမရှိပါဘူး၊ သိုသော်လည်း copy-paste လုပ်တဲ့ အခါမှာ errors တွေမဖြစ်ဖို့ကြိုတားစီးနိုင်ပါတယ်။

```dart
var list = [
    'Car',
    'Boat',
    'Plane',
];
```

Lists တွေက zero-based indexig ကို သုံးပါတယ်။ 0 က first value ရဲ့ index ဖြစ်ပါတယ် ပြီးတော့ `list.length - 1` ကတော့ နောက်ဆုံး value ရဲ့ index ဖြစ်ပါတယ်။ list တစ်ခုရဲ့ length ကို ယူနိုင်ပါတယ် ပြီးတော့ JavaScript မှာလိုပဲ list values တွေကို refer လုပ်နိုင်ပါတယ် -

```dart
var list = [1, 2, 3];
assert(list.length == 3);
assert(list[1] == 2);

list[1] = 1;
assert(list[1] == 1);
```

compile-time const ဖြစ်တဲ့ list တစ်ခုကိုဖန်တီးချင်တယ်ဆိုရင် list literal ရဲ့ ရှေ့မှာ `const` ထည့်ပေးလိုက်ရင်ရပါပြီ။

```dart
var constantList = const [1, 2, 3];
// constantList[1] = 1; // This line will cause an error.
```

Dart 2.3 မှာ **spread operator**(`...`) နဲ့ **null-aware spread operator**(`...?`) ကို စတင်မိတ်ဆက်ခဲ့ပါတယ်။ collection တစ်ခုထဲကို multiple values တွေ လွယ်ကူကျစ်လစ်စွာ နဲ့ ထည့်လို့ရတဲ့ နည်းလမ်းဖြစ်ပါတယ်။

ဥပမာ speread operator (`...`) ကိုသုံးပြီးတော့ list တစ်ထဲကို အခြား list မှာရှိတဲ့ value တွေပေါင်းထည့်လို့ရပါတယ်။

```dart
var list = [1, 2, 3];
var list2 = [0, ...list];
assert(list2.length == 4);
```

တကယ်လို့ spread operator ရဲ့ ညာဘက်မှာရှိတဲ့ expression က null ဖြစ်လို့မရဘူးဆိုရင် ထို expression ကို null-aware operator (`...?`) သုံးပြီးတော့ avoid လုပ်လိုက်လို့ရပါတယ်။

```dart
var list;
var list2 = [0, ...?list];
assert(list2.leangth == 1);
```

spread operator သုံးပုံအပြည့်အစုံကို [spread operator proposal](https://github.com/dart-lang/language/blob/master/accepted/2.3/spread-collections/feature-specification.md) မှာလေ့လာနိုင်ပါတယ်။

Dart မှာ **collection if** နဲ့ **collection for** ဆိုတာရှိပါသေးတယ်။ collections တွေတည်ဆောက်တဲ့နေရာမှာ conditionals (`if`) နဲ့ repetition (`for`) တို့ကို ထည့်သွင်းအသုံးပြုနိုင်ပါတယ်။

ဒါကတော့ **collection if** ကိုသုံးပြီးထားတဲ့ list ဖြစ်ပါတယ်။ သူအထဲမှာ items (၃) ခု ဒါမှမဟုတ် (၄) ခုရှိနေပါတယ်။

```dart
var nav = [
    'Home',
    'Furniture',
    'Plants',
    if(promoActive) 'Outlet'
];
```

ဒါကတော့ **collection for** ကိုသုံးပြီးတော့ list တစ်ခုကို အခြား list တစ်ခုထဲသို့ မထည့်ခင် items တွေကို manipulate လုပ်ထားတာဖြစ်ပါတယ်။

```dart
var listOfInts = [1, 2, 3];
var listOfString = [
    '#0',
    for(var i in listOfInts) '#$i'
];
assert(listOfStrings[1] == '#1');
```

collection `if` နဲ့ `for` အသုံးပြုပုံ အသေးစိတ်ကို [control flow collections proposal](https://github.com/dart-lang/language/blob/master/accepted/2.3/control-flow-collections/feature-specification.md) မှာ example နဲ့ အသေးစိတ်ကိုလေ့လာနိုင်ပါတယ်။

List type မှာ lists တွေကို manipulating လုပ်ဖို့ ကိုင်တွယ်နိုင်တဲ့ methods တွေအများအပြားရှိပါတယ်။ lists တွေအကြောင်းကို [Generics](https://dart.dev/guides/language/language-tour#generics) နဲ့ [Collections](https://dart.dev/guides/libraries/library-tour#collections) မှာ အသေးစိတ်လေ့လာနိုင်ပါတယ်။

### Sets

Dart မှာရှိတဲ့ set တစ်ခုက uniquee items တွေကို အစီအစဉ်သတ်မှတ်ထားခြင်းမရှိပဲ စီထားတဲ့ collection တစ်ခုဖြစ်ပါတယ်။ Dart မှာ set literals တွေနဲ့ `Set` type ကို sets တွေအတွက် support လုပ်ပေးပါတယ်။

ဒါကတော့ simple Dart set တစ်ခုကို set literal တစ်ခုသုံပြီးဖန်တီးထားတာ ဖြစ်ပါတယ်။

```dart
var halogens = {'flourine', 'chlorine', 'bromine', 'iodine', 'astatine'};
```

> **Note:** `halogens` မှာ `Set<String>` type သက်ရောက်သွားပါတယ်။ ထို set ထဲကို မှားနေတဲ့ value တစ်ခုခု ထည့်ကြည့်လိုက်ရင် analyser သို့မဟုတ် runtime ကနေပြီတော့ error တစ်ခု ပြပေးပါလိမ့်မယ်။ အချက်အလက်အသေးစိတ်ကို [type inference]("https://dart.dev/guides/language/type-system#type-inference") မှာဖတ်နိုင်ပါတယ်။

Empty set တစ်ခုကို ဖန်တီးဖို့အတွက် `{}` ကို type argument တစ်ခုအနေနဲ့ သုံးပေးရပါတယ်။ ဒါမှမဟုတ် `{}` ကို `Set` type ဖြစ်တဲ့ variable မှာ assign လုပ်ပေးရပါတယ်။

```dart
var names = <String>{};
// Set<String> names = {}; // This works, too.
// var names = {}; // Creates a map, not a set.
```

> **Set or map?** map literals တွေအတွက် syntax က set literals တွေရဲ့ syntax နဲ့ အလားတူဖြစ်ပါတယ်။ ဘာဖြစ်လို့ဆိုတော့ map literals အရင်ပေါ်ပေါက်လာတာဖြစ်ပြီး `{}` က `Map` type ရဲ့ default ဖြစ်ပါတယ်။ type annotation ကို `{}` ရေးတာ သို့မဟုတ် variable ကို assign လုပ်တာ ကိုမေ့သွားရင်၊ `Map<dynamic, dynamic>` type ရဲ့ object နဲ့ ဖန်တီးနိုင်ပါတယ်။

```dart
var elements = <String>{};
elements.add('flourine');
elements.addAll(halogens);
```

`.length` ကိုသုံးပြီးတော့ set ထဲမှာရှိတဲ့ items တွေရဲ့ အရေအတွက်ကို ရယူနိုင်ပါတယ်။

```dart
var elements = <String>{};
elements.add('flourine');
elements.addAll(halogens);
assert(elements.length == 5);
```

set တစ်ခုကို compile-time constant တစ်ခုအနေနဲ့ ဖန်တီးဖို့အတွက် set literal ရဲ့ရှေ့မှာ `const` ကိုထည့်သွင်းပေးရပါတယ်။

```dart
final constantSet = const {
    'flourine',}
    'chlorine',
    'bromine',
    'iodine',
    'astatines',
}
```

Sets တွေမှာ spread operators (`...` and `...?`) တွေ support လုပ်တဲ့အပြင် collection `if` နဲ့ `for` ကိုလည်း support ပေးပါတယ်။ list နဲ့ လုပ်ပုံ အတူတူပါပဲ။ အသေးစိတ်အတွက် [list spread operator](https://dart.dev/guides/language/language-tour#spread-operator) နဲ့ [list collection operator](https://dart.dev/guides/language/language-tour#collection-operators) မှာလေ့လာနိုင်ပါတယ်။

Sets တွေအကြောင်းကိုတော့ [Generics](https://dart.dev/guides/language/language-tour#generics) နဲ့ [Sets](https://dart.dev/guides/libraries/library-tour#sets) မှာအသေးစိတ်လေ့လာနိုင်ပါတယ်။

### Maps

ယေဘုံယအားဖြင့် map ဆိုတာ key နဲ့ value အတွဲတွေကို စုထားတဲ့ object တစ်ခုဖြစ်ပါတယ်။ key ကော value ကောက မည်သည့် type မဆိုဖြစ်နိုင်ပါတယ်။ _ key_ တစ်ခုခြင်းစီက တစ်ကြိမ်ပဲ (unique) ဖြစ်ရမှာဖြစ်ပြီးတော့၊ _value_ မှာတော့ တစ်ခုတည်းကို အကြိမ်ကြိမ့်ထည့်လို့ရပါတယ်။ Dart မှာ maps တွေအတွက် map literals နဲ့ `Map` type ကို provide လုပ်ဖို့ support ပေးပါတယ်။

ဒါကတော့ simple Dart maps ရဲ့ example နှစ်ခုဖြစ်ပြီး map literals ကိုသုံးထားပါတယ်။

```dart
var gifts = {
    // Key: Value
    'first': 'partridge',
    'second': 'turtledoves',
    'fifth': 'golden rings'
};

var nobleGases = {
    2: 'helium',
    10: 'neon',
    18: 'argon',
};
```

> **Note:** Dart က `gifts` ကို `Map<String, String>` type လို့ယူဆလိုက်ပါတယ် ပြီးတော့ `nobleGases` ကို `Map<int, String>` type လို့ ယူဆပါတယ်။ တစ်ကယ်လိုများ type အမှားဖြစ်တဲ့ value တစ်ခုကို ထည့်ဖို့ကြိုးစားရင် analyser သို့မဟုတ် runtime ကနေ error တစ်ခုထုတ်ပေးပါလိမ့်မယ်။ အသေးစိတ်ကို [type inference](https://dart.dev/guides/language/type-system#type-inference) မှာဖတ်နိုင်ပါတယ်။

Map constructor ကိုသုံးပြီး ခုန object နဲ့ ဆင်တူတဲ့ object ကိုဖန်တီးနိုင်ပါတယ်။

```dart
var gifts = Map<String, String>();
gifts['first']= 'partrifge';
gifts['second']= 'turtledoves';
gifts['fifth']= 'golden rings';

var nobleGases = Map<int, String>();
nobleGases[2]= 'helium';
nobleGases[10]= 'neon';
nobleGases[18]= 'argon';
```

> **Note:** သင်က Java တို့ C# တို့အရင်က သုံးခဲ့ဘူးမယ်ဆိုရင် `Map()` ကို `new Map()` လို့ရေးခဲ့ရဘူးမယ်လို့ထင်ပါတယ်။ Dart မှာတော့ `new` keyword က optional ပါ။ အသေးစိတ်ကို [Using constructors](https://dart.dev/guides/language/language-tour#using-constructors) မှာလေ့လာနိုင်ပါတယ်။

key-value pair အသစ်တစ်ခုကို ရှိပြီးသား map တစ်ခုသို့ထည့်မယ်ဆိုရင် JavaScript မှာလိုပဲလုပ်နိုင်ပါတယ်။

```dart
var gifts = {'first':'partridge'};
gifts['fourth'] = 'calling birds'; // Add a key-value pair
```

map တစ်ခုထဲကနေပြီးတော့ value တစ်ခုကိုပြန်ယူမယ်ဆိုရင် JavaScript နည်းအတိုင်းပဲ ဆောင်ရွက်နိုင်ပါတယ်။

```dart
var gifts = {'first':'partridge'};
assert(gifts['first'] == 'partridge');
```

key တစ်ခုက map ထဲမှာရှိလားမရှိဘူးလာကို စစ်နိုင်ပါတယ်။ မရှိရင် `null` ကို return ပြန်ပါလိမ့်မယ်။

```dart
var gifts = {'first':'partridge'};
assert(gifts['first'] == null);
```

`.length` ကိုသုံးပြီးတော့ map ထဲမှာ key-value pairs တွေရဲ့ အရေအတွက်ကိုရယူနိင်ပါတယ်။

```dart
var gifts = {'first':'partridge'};
gifts['fourth'] = 'calling birds';
assert(gifts.length == 2);
```

map တစ်ခုကို compile-time constant အဖြစ်ဖန်တီးချင်တယ်ဆိုရင် map literal ရဲ့ရှေ့မှာ `const` ကိုထည့်ပေးလိုက်ရင်ရပါပြီ။

```dart
final constantMap = const {
    2: 'helium',
    10: 'neon',
    18: 'argon',
};

// constantMap[2] = 'Helium'; // This line will cause an error.
```

Maps တွေမှာ spread operators (`...` and `...?`) တွေနဲ့ collection `if` နဲ့ `for` ကို support လုပ်ပါတယ်။ list မှာအလုပ်လုပ်သလိုပါပဲ။ အသေးစိတ်နဲ့ ဥပမာတွေကို [spread operator proposel](https://github.com/dart-lang/language/blob/master/accepted/2.3/spread-collections/feature-specification.md) နဲ့ [control flow collections proposal](https://github.com/dart-lang/language/blob/master/accepted/2.3/control-flow-collections/feature-specification.md) မှာဝင်ရောက်ဖတ်နိုင်ပါတယ်။

maps တွေအကြောင်းပိုလေ့လာလိုလျှင်တော့ [generic](https://dart.dev/guides/language/language-tour#generics) section နှင့် library tour ရဲ့ coverage of the [Maps API](https://dart.dev/guides/libraries/library-tour#maps) မှာဖတ်ရှုနိုင်ပါတယ်။

### Runes and grapheme clusters

Dart မှာ [runes](https://api.dart.dev/stable/dart-core/Runes-class.html) တွေက string တစ်ခုရဲ့ Unicode code points တွေကို expose လုပ်ပါတယ်။ [characters package](https://pub.dev/packages/characters) ကိုသုံးပြီးတော့ ကြည့်နိုင်တဲ့အပြင် user-perceived characters တွေကို manipulate လုပ်နိုင်ပါတယ်။ ထို package ကို [Unicode grapheme clusters](https://unicode.org/reports/tr29/#Grapheme_Cluster_Boundaries) လို့လဲလူသိများကြပါတယ်။

ကမ္ဘာသုံး writing systems တွေမှာအသုံးပြုထားတဲ့ letter, digit, နဲ့ symbol တစ်လုံးချင်းစီတိုင်းကို unique ဖြစ်တဲ့ numeric value တစ်ခုစီနဲ့ Unicode ကသတ်မှတ်ပေးထားပါတယ်။ Dart string တစ်ခုက UTF-16 code unit တစ်ခုရဲ့ sequence ဖြစ်ပါတယ်။ unicode code points တွေကို string တစ်ခုထဲမှာ သုံးဖို့ special syntax လိုပါတယ်။ ပုံမှန်မဟုတ်တဲ့ unicode code point တစ်ခုကို `\uXXXX` နဲ့ဖော်ပြရပါတယ်၊ ဒီနေရာမှာ XXXX က 4 digit haxadecimal value တစ်ခုဖြစ်ပါတယ်။ ဥပမာ heart character (♥) က `\u2665` ဖြစ်ပါတယ်။ 4 hex digit ထက်များရင် (သို့မဟုတ်) နည်းရင် value ကို curly brackets တွေကြားမှာရေးသားပေးရပါတယ်။ ဥပမာ laughing emoji (😆) က `\u{1f606}` ဖြစ်ပါတယ်။

သီးသန့်ဖြစ်တဲ့ Unicode characters တွေကို read or write လုပ်လိုလျှင် `characters` ကိုသုံးပြီးတော့ String ထဲမှာ charccters package နဲ့ သတ်မှတ်ပေးရပါတယ်။ returned လုပ်တဲ့ `Characters` object က grapheme clusters တွေရဲ့ sequence တစ်ခုကဲ့သို့ string ဖြစ်ပါတယ်။ ဒါကတော့ characters API တစ်ခုအသုံးပြုထားတဲ့ example ဖြစ်ပါတယ်။

```dart
import 'package:characters/characters.dart';
...
var hi = 'Hi 🇩🇰';
print(hi);
print('The end of the string: ${hi.substring(hi.length - 1)}');
print('The last character: ${hi.characters.last}\n');
```

output က သင့်ရဲ့ environment အပေါ်မှုတည်ပါတယ်။ ဒီလိုမျိုးရပါမယ်။

<div style="padding:20px; background-color:black;">
<span style="color: gray;">$</span>&nbsp;<span style="color: green;">dart bin/main.dart</span><p>Hi 🇩🇰<br />The end of the string: ???<br />The last character: 🇩🇰</p>
</div>

strings တွေကို manipulate လုပ်ရာမှာသုံးတဲ့ charactres package အသုံးပြုပုံကို [example](https://pub.dev/packages/characters/example) နှင့် characters package အတွက် [API refrence](https://pub.dev/documentation/characters) မှာလေ့လာနိုင်ပါတယ်။

### Symbols

Dart program တစ်ခုမှ operator တစ်ခု သို့မဟုတ် ကြောငြာထာတဲ့ identifier တစ်ခုကို **Symbol** object က represents လုပ်ပါတယ်။ symbols တွေကိုဘယ်တော့မှ သုံးစရာမလိုပါဘူး၊ သို့ပေမဲ့ identifier တွေကို name နဲ့ refer လုပ်တဲ့ APIs တွေအတွက် တန်ဖိုးမဖြတ်နိုင်ပါဘူး။ ဘာဖြစ်လို့လဲဆိုတော့ minification လုပ်တဲ့နေရာမှာ identifier name တွေပဲပြောင်းပြီးတော့ identifier symbol တွေက ပြောင်းလဲသွားခြင်းမရှိသောကြောင့်ဖြစ်ပါတယ်။

identifier တစ်ခုအတွက် symbol ကိုလိုချင်တဲ့အခါမှာ symbol literal ကိုသုံးရပါတယ်။ သူက identifier ရဲ့ ရှေ့မှာ `#` တစ်ခုထည့်ပေးလိုက်ယုံပဲဖြစ်ပါတယ်။

```dart
#radix
#bar
```

Symbol literals တွေက compile-time constants တွေဖြစ်ကြပါတယ်။

## Functions

Dart က object-oriented language တစ်ခုဖြစ်ပါတယ်၊ function တွေတောင် objects တွေဖြစ်ပြီး `Function` type တောင်ရှိပါတယ်။ ဆိုလိုတာက function တွေကို variable တွေထဲသို့ assign လုပ်နိုင်ပြီး အခြား function ထဲကို arguement တွေအနေနဲ့ passed လုပ်နိုင်ပါတယ်။ function တစ်ခုဖြစ်ရင် Dart class တစ်ခုရဲ့ instance တစ်ခုကို call နိုင်ပါသေးတယ်။ အသေးစိတ်ကို [Callable classes](https://dart.dev/guides/language/language-tour#callable-classes) မှာလေ့လာနိုင်ပါတယ်။

ဒါကတော့ function တစ်ခုကို implementing လုပ်တဲ့ example ဖြစ်ပါတယ်။

```dart
bool isNoble(int atomicNumber){
    return _nobleGases[atomicNumber] != null;
}
```

Effective Dart က [type annotations for public APIs](https://dart.dev/guides/language/effective-dart/design#do-type-annotate-fields-and-top-level-variables-if-the-type-isnt-obvious) ဖြင့် မသုံးသင့်ကြောင်း အကြံပြုထားသော်လည်းပဲ၊ function မှာရှိတဲ့ types တွေကို ဖြုတ်ထားရင်တောင် ထို function က အလုပ်လုပ်တုန်းဖြစ်ပါတယ်။

```dart
isNoble(int atomicNumber){
    return _nobleGases[atomicNumber] != null;
}
```

expression တစ်ကြောင်းသာပါတဲ့ function တွေကို shorthand syntax သုံးပြီးရေးလို့ရပါတယ်။

```dart
bool isNoble(int atomicNumber) => _nobleGases[atomicNumber] != null;
```

`=> expr` syntax က `{ return expr; }` အတွက် အတိုကောက်ရေးနည်း ဖြစ်ပါတယ်။ `=>` notation က တစ်ခါတရံမှာ _arrow_ syntax ကဲသို့ referred လုပ်ပါတယ်။

> **Note:** expression တစ်ခုသာဖြစ်ရပါမယ်၊ statement တစ်ခုဖြစ်လို့မရပါဘူး၊ arrow(=>) နဲ့ semicolon(;) ကြားမှာရေးရပါမယ်။ ဥပမာ - **if statement** ကိုထားလို့မရပါဘူး၊ သို့ပေမဲ့ **conditional expression** ကိုတော့ သုံးလို့ရပါတယ်။

### Parameters

function တစ်ခုမှာ _required positional_ parameters တွေကြိုက်သလောက်ထည့်နိုင်ပါတယ်။ _named parameters_ တွေဖြစ်နိုင်သလို _optional positional_ parameters တွေလည်း ဖြစ်နိုင်ပါတယ်။(သို့ပေနဲ့ နှစ်မျိုးလုံး တစ်ပြိုင်နက်တော့ မဖြစ်နိုင်ပါဘူး)။

> **Note:** အချို့ APIs တွေ၊ အထူးသဖြင့် Flutter widget constructorမှာ၊ named parameters တစ်ခုကိုသာသုံးပါတယ်။ mandatory ဖြစ်တဲ့ parameters တွေတောင်မှပဲ ထိုနည်းကိုသုံးပါတယ်။ အသေးစိတ်ကို နောက် section မှာလေ့လာပါ။

function တစ်ခုကို arguments တွေ pass လုပ်တဲ့အခါ သို့မဟုတ် function parameters တွေသတ်မှတ်တဲ့အခါ **trailing commas** တွေကိုသုံးလို့ရပါတယ်။

#### Named parameters

Named parameters တွေကို အထူးလိုအပ်မှာသာ သုံးလေ့ရှိပါတယ်။

function တစ်ခုကို ခေါ်တဲ့အခါမှာ `paramName:value` ကိုသုံးပြီးတော့ named parameters တွေကိုသတ်မှတ်နိုင်ပါတယ်။ ဥပမာ -

```dart
enableFlags(bold: true, hidden: false);
```

function ကို သတ်မှတ်တဲ့ အခါမှာကြတော့ `{param1, param2, ...}` ကိုသုံးပြီးတော့ named parameters တွေကိုသတ်မှတ်ရပါတယ် -

```dart
/// Sets the [bold] and [hidden] flags ...
void enableFlags({bool? bold, bool? hidden}){...}
```

> **Tip:** parameter တစ်ခုက optional ဖြစ်နေတယ် ဒါပေနဲ့သူက `null` ဖြစ်လို့တော့ မရဘူးဆိုရင်တော့ **default value** တစ်ခုသတ်မှတ်ပေးဖို့လိုပါလိမ့်မယ်။

named parameters တွေက optional parameter အမျိုးအစားဖြစ်သော်ငြားလည်း `required` ကိုသုံးပြီး ထို parameter ကို user က value တစ်ခုနဲ့ မဖြစ်မနေ ဖြည့်စွတ်ပေးရန်လိုကြောင်း သတိပေးနိုင်ပါတယ်။ ဥပမာ

```dart
const Scrollbar({Key? key, required Widget child})
```

အကယ်၍ တစ်စုံတစ်ယောက်က `Scrollbar` တစ်ခုကို ဖန်တီးတဲ့နေရာမှာ `child` argument ကို သတ်မှတ်မပေးဘဲ ထားပါက analyzer က issue တစ်ခုကို report လုပ်မှဖြစ်ပါတယ်။

#### Optional positional parameters

function parameters တွေကို `[]` ကြားမှာ ထည့်လိုက်ရင် ထို parameters တွေက optional positional parameters တွေဖြစ်ကုန်ပါတယ်။

```dart
String say(String from, String msg, [String? device]){
    var result = '$from says $msg';
    if(device != null){
        result = '$result with a $device';
    }
    return result;
}
```

ဒါကတော့ optional parameter ကိုမထည့်တော့ပဲ function တစ်ခုကို ခေါ်ပုံဖြစ်ပါတယ်။

```dart
assert(say('Bob', 'Howdy') == 'Bob says Howdy');
```

ဒါကတော့ တတိယမြောက် parameter ကိုထည့်ပြီးတော့ function ကို ခေါ်ထားပုံဖြစ်ပါတယ်။

```dart
assert(say('Bob', 'Howdy', 'smoke signal') == 'Bob says Howdy with a smoke signal');
```

#### Default parameter values

named နဲ့ positional parameters အတွက် default value ကိုသတ်မှတ်ပေးလိုလျှင် `=` ကိုသုံးပြီးသတ်မှတ်ပေးရပါတယ်။ default value က compile-time constant တွေ ဖြစ်ကို ဖြစ်ရပါမယ်။ default value သတ်မှတ်မထားဘူးဆိုရင်၊ ၎င်းအစား `null` ကိုသုံးသွားမှာဖြစ်ပါတယ်။

ဒါကတော့ named parameters တွေမှာ default values တွေသတ်မှတ်ထားပုံဖြစ်ပါတယ်။

```dart
/// Sets the [bold] and [hidden] flags ...
void enableFlags({bool bold = false, bool hidden = false}){...};

// bold will be true; hidden will be false.
enableFlage(bold: true);
```

> **Deprecation note:** အရင်တုန်းက old code မှာ named parameters တွေရဲ့ dafault values ကိုသတ်မှတ်ရင် `=` အစား colon (`:`) တစ်ခုကိုသုံးရပါတယ်။ `:` က named parameter တွေအတွက်သာ ဖြစ်တယ်ဆိုတဲ့ အကြောင်းပြချက်နဲ့ ဖြစ်ပါတယ်။ ထိုသို့ အသုံပြုခြင်းကို ကန့်သပ်လိုက်ပြီဖြစ်ပြီး `=` ကိုသာသုံးဖို့ အကြံပြုပါရစေ။ [use = to specify default values](https://dart.dev/guides/language/effective-dart/usage#do-use--to-separate-a-named-parameter-from-its-default-value)

နောက် example ကတော့ positional parameters တွေမှာ default value သတ်မှတ်ပုံဖြစ်ပါတယ်။

```dart
String say(String from, String msg, [String device = 'carrier pigeon']){
    var result = '$from says $msg with a $device';
    return result;
}

assert(say('Bob', 'Howdy') ==
'Bob says Howdy with a carrier pigeon');
```

lists နဲ့ maps တွေကိုလည်း default values တွေအဖြစ်နဲ့ pass လုပ်လို့ရပါတယ်။ အောက်ပါ example ကတော့ `doStuff()` ဆိုတဲ့ function တစ်ခုကို သတ်မှတ်ထာဖြစ်ပြီး ထို function ရဲ့ `lists` parameter နဲ့ `gifts` parameter တွေကို default list နဲ့ default map တွေသတ်မှတ်ပေးပုံဖြစ်ပါတယ်။

```dart
void doStuff(
    {
        List<int> list = const [1, 2, 3],
        Map<String, String> gifts = const {
            'first':'paper',
            'second':'cotton',
            'third':'leather',
        }
    }
){
    print('list: $list');
    print('gifts: $gifts');
}
```

### The main() function

App တိုင်းမှာ top-level `main()` function တစ်ခုတော့ ပါကိုပါရမှာဖြစ်ပါတယ်။ ထို `main()`function က app ရဲ့ entrypoint တစ်ခုဖြစ်ပါတယ်။ `main()`function က `void` ကို return အဖြစ်ပြန်ပြီးတော့ arguments တွေအနေနဲ့ optional `List<String>` parameter တစ်ခုပါပါတယ်။

ဒါက simple `main()` function တစ်ခုဖြစ်ပါတယ်

```dart
void main(){
    print('Hello, World!');
}
```

ဒါက arguements တွေလက်ခံပေးတဲ့ command-line app တစ်ခုအတွက် `main()` function ဖြစ်ပါတယ်။

```dart
// Run the app like this: dart args.dart 1 test
void main(List<String> arguments){
    print (arguments);

    assert(arguments.length == 2);
    assert(int.parse(arguments[0]) == 1);
    assert(arguments[1] == test);
}
```

[args library](https://pub.dev/packages/args) ကိုသုံးပြီးတော့ command-line arguments တွေကို define လုပ်ခြင်းနဲ့ parse လုပ်ခြင်းတို့ကိုဆောင်ရွက်နိုင်ပါတယ်။

### Functions as first-class objects

function တစ်ခုကို parameter အဖြစ်နဲ့ အခြား function တစ်ခုကို pass လုပ်နိုင်ပါတယ်။ ဥပမာ -

```dart
void printElement(int element){
    print(element);
}

var list = [1, 2, 3];

// Pass printElement as a parameter
list.forEach(printElement);
```

function တစ်ခုကို variable တစ်ခုအတွင်းသို့ assign လုပ်လို့ရပါတယ်။

```dart
var loudify = (msg) => '!!! ${msg.toUpperCase()} !!!';
assert(loudify('hello') == '!!! HELLO !!!');
```

ဒီ example မှာ anonymous function တစ်ခုကို သုံးထားတာဖြစ်ပါတယ်။ ထိုအကြောင်းကို နောက်ထပ် section မှာလေ့လာနိုင်ပါတယ်။

### Anonymous functions

`main()` သို့မဟုတ် `printElement()` တို့လို့ function အများစုက named functions တွေဖြစ်ကြပါတယ်။ နာမည်တပ်စရာမလိုတဲ့ nameless functions တွေကိုလည်းဖန်တီးနိုင်ပါသေးတယ်။ ထို function တွေကို _anonymous function_, တစ်ခါတလေ _lambda_ သို့မဟုတ် _closuer_ လို့ အမျိုးမျိုးခေါ်ကြပါတယ်။ anonymous function တစ်ခုကို variable တစ်ခုအတွင်းသို့ assign လုပ်ပေးလို့ရပါတယ်။ ဘာအတွက်သုံးလဲဆိုတော့ collection တစ်ခုထဲကနေ ၎င်းကို add လုပ်တာတို့ remove လုပ်တာတေ ဆောင်ရွက်နိုင်စေဖို့ဖြစ်ပါတယ်။

function ရဲ့ body သာပါဝင်တဲ့ code block ဖြစ်ပါတယ်။

```dart
([[Type] param1[1, ...]]){
    codeBlock;
};
```

အောက်ပါ example မှာတော့ anonymous function တစ်ခုကို သတ်မှတ်ထားတာဖြစ်ပြီး ၎င်းမှာ `item` ဆိုတဲ့ untyped parameter တစ်ခု ပါဝင်ပါတယ်။ ထို function ကို list ထဲမှာရှိတဲ့ item တစ်ခုခြင်းစီတိုင်းက invoke လုပ်သွားမှာဖြစ်ပြီး သတ်မှတ်ထားတဲ့ index မှာရောက်နေတဲ့ value ဖြစ်တဲ့ string ကို print လုပ်သွားမှာဖြစ်ပါတယ်။

```dart
const list = ['apples', 'bananas', 'oranges'];
list.forEach((item){
    print('${list.indexOf(item)}: $item');
});
```

ဒီ code ကို **Run** ကြည့်ပါ။

```dart
void main() {
  const list = ['apples', 'bananas', 'oranges'];
  list.forEach((item) {
    print('${list.indexOf(item)}: $item');
  });
}

```

တကယ်လို့ function မှာ exprection ကတစ်ကြောင်းတည်းဖြစ်နေရင် သို့မဟုတ် return statement တစ်ခုသာပါရင် arrow notation ကိုသုံးပြီးတော့ အတိုကောက်နည်းနဲ့ရေးနိုင်ပါတယ်။ ဒီ code ကို run ကြည့်ပါ ခုန code နဲ့ အလုပ်လုပ်ပုံက အတူတူပဲဖြစ်ပါတယ်။

```dart
list.forEach((item) => print('${list.indexOf(item)}: $item'));
```

### Lexical scope

dart က lexical scoped language တစ်ခုဖြစ်ပါတယ်။ ဆိုလိုတာက variables တွေရဲ့ scope ကို statically အရ ဆုံးဖြတ်တယ်။ code တွေရဲ့ layout အရ symply လုပ်တယ်ဆိုတဲ့ သဘောပါ။ variable တစ်ခုက scope ထဲမှာဆိုရင် curly braces တွေရဲ့ outwards အတိုင်း ပိုင်ဆိုင်ပါတယ်။

ဒါကတော့ nested functions တွေနဲ့ scope level တစ်ခုချင်းစီတိုင်းမှာ variable တစ်ခုစီရှိပါတယ်။

```dart
bool topLevel = true;

void main(){
    var insideMain = true;

    void myFunction(){
        var insideFunction = true;

        void nestedFunction(){
            var insideNestedFunction = true;

            assert(topLevel);
            assert(insideMain);
            assert(insideFunction);
            assert(insideNestedFunction);
        }
    }
}
```

`nestedFunction()` က level တိုင်းမှာရှိတဲ့ variables ကို ရယူအသုံးပြုနိုင်ပါတယ်။ အထက် level မှာရှိတဲ့ function တွေလည်းထိုနည်းအတိုင်းပါပဲ။

### Lexical closures

_closure_ ဆိုတာ function object တစ်ခုဖြစ်ပါတယ်၊ ၎င်းက သူရဲ့ lexical scope ထဲမှာ variables တွေကို access လုပ်ပါတယ်။ သူ့ original scope ရဲ့ outside ကို function က သုံးနေတဲ့အချိန်မှာတောင် access လုပ်ပါတယ်။

scopes တွေရဲ့ပတ်လည်မှာ သတ်မှတ်ထားတဲ့ variables တွေကို functions တွေက close လုပ်နိုင်ပါတယ်။ အောက်ပါ example မှာရှိတဲ့ `makeAdder()` က variable ဖြစ်တဲ့ `addBy` ကို capture လုပ်ပါတယ်။ ဘယ်နေရာမဆို returned function က၊ `addBy` ကိုမှတ်ထားပါတယ်။

ဆိုလိုတာက function တစ်ခုကို return ပြန်တဲ့ function က return အဖြစ်ပြန်ပေး တဲ့ function အတွက် variable တွေကို မှတ်ထားပေးတယ် ဆိုတဲ့သဘောပါ။

```dart
/// Returns a function that adds [addBy] to the
/// functions's argument.

Function makeAdder(int addBy){
    return (int i) = addBy + 1;
}

void main(){
    // Create a function that adds 2.
    var add2 = makeAdder(2);

    // Create a function that adds 4.
    var add4 = makeAdder(4);

    assert(add2(3) == 5);
    assert(add4(3) == 7);
}
```

### Testing functions for equality

ဒါကတော့ top-level functions, static methods, and instance methods for equality တို့ကို စမ်းကြည့်တဲ့ example ဖြစ်ပါတယ်။

```dart
void foo() {} // A top-level function

class A {
    static void bar() {} // A static method
    void baz() {} // An instance method
}

void main() {
    Function x;

    // Comparing top-level functions.
    x = foo;
    assert(foo == x);

    // Comparing static methods.
    x = A.bar;
    assert(A.bar == x);

    // Comparing instance methods.
    var v = A(); // Instance #1 of A
    var w = A(); // Instance #2 of A
    var y = w;
    x = w.baz;

    // These closures refer to the same instance (#2),
    // so they'er equal.
    assert(y.baz == x);

    // These closures refer to different instance,
    // so they'er unequal.
    assert(v.baz != w.baz);
}
```

### Return values

function အားလုံးက value တစ်ခုကို return ပြန်ပါတယ်။ return value ကိုသတ်မှတ်ပေးမထားရင် `return null;` ဆိုတဲ့ statement ကို function body မှာ အကြွင်းမဲ့သုံးပေးသွားမှာဖြစ်ပါတယ်။

```dart
foo() {}

assert(foo() == null);
```

## Operators

Dart မှာ support လုပ်တဲ့ operators အားလုံးကို အောက်ပါဇယားမှာ ပြထားပါတယ်။ ထိုအထဲမှ တော်များများ operators တွေကို clsss members တွေအဖြစ် implement လုပ်လို့ရပါတယ်။

| Description              | Operator                                               |
| :----------------------- | :----------------------------------------------------- |
| unary postfix            | `expr++` `expr--` `()` `[]` `.` `?.`                   |
| unary prefix             | `-expr` `!expr` `~expr` `++expr` `--expr` `await expr` |
| multiplicative           | `*` `/` `%` `~/`                                       |
| additive                 | `+` `-`                                                |
| shift                    | `<<` `>>` `>>>`                                        |
| bitwise AND              | `&`                                                    |
| bitwise XOR              | `^`                                                    |
| bitwise OR               | `\|`                                                   |
| relational and type test | `>=` `>` `<=` `<` `as` `is` `is!`                      |
| equlity                  | `==` `!=`                                              |
| logical AND              | `&&`                                                   |
| logical OR               | `\|\| `                                                |
| if null                  | `??`                                                   |
| conditional              | `expr1 ? expr2 : expr3`                                |
| cascade                  | `..` `?..`                                             |
| assigment                | ` =` `*=` `/=` `+=` `-=` `&=` `^=` etc.                |

> **Warning:** Operator precedence က Dart parser တစ်ခုရဲ့ behavior ရဲ့ approximation တစ်ခုဖြစ်ပါတယ်။ အတိအကျ အဖြေကတော့ [Dart language specification](https://dart.dev/guides/language/spec) ထဲမှာ grammar ကို consult လုပ်ထားခြင်းဖြစ်ပါတယ်။

expression တွေတည်ဆောက်တဲ့အခါမှာ operators တွေကိုအသုံပြုရမှာဖြစ်ပါတယ်။ ဒါကတော့ operator expressions တွေရဲ့ example အချို့ဖြစ်ပါတယ်။

```dart
a++
a + b
a = b
a == b
c ? a : b
a is T
```

[operator table](https://dart.dev/guides/language/language-tour#operators) မှာ operator တစ်ခုခြင်းစီက သူ့ကို follow လုပ်တဲ့ rows တွေထဲမှာရှိတဲ့ operators တွေထက် precedence မြင့်ပါတယ် (အတန်းလိုက်ထဲမှာ နောက်ကကောင်ထက် ရှေ့ကကောင်ကပိုမြင့်တယ်၊ အထက်အောက်မှာဆို အောက်တန်းထက် အထက်တန်းကပိုမြင့်တယ်)။ ဥပမာ - multiplicative operator `%` က equality operator `==` ထက် precedence မြင်ပါတယ် (`%` ကိုအရင်ရှင်းပြီးမှ `==` ကိုရှင်းမှာဖြစ်တယ်)၊ ထို `==` က logical AND operator `&&` ထက် precedence ပိုမြင့်ပါတယ်။ precedence အဓိပ္ပာယ်က အောက်ပါ code လိုင်းနှစ်ခုက code execute လုပ်ပုံခြင်းအတူတူပါပဲ။ (ကွင်းတွေခပ်မထားလည်း precedence မြင့်တာကို အရင်ဖြေရှင်းမှာလို့ လိုဆိုတာပါ)။

```dart
// Parentheses improve readability.
if((n % i == 0) && (d % i == 0)) ...

// Harder to read, but equavalence
if(n % i == 0 && d % i == 0) ...
```

> **Warning:** operators တွေက operands (၂) ကိုသုံးပါတယ်။ ဘယ်ဘက်က operand က ဘယ် method ကိုသုံးထားလဲဆိုတာကို ဆုံးဖြတ်ပါတယ်။ ဥပမာ - `Vector` object နဲ့ `Point` object နှစ်ခုရှိတယ်ဆိုရင်၊ ထို့နောက် `aVector + aPoint` က `Vector` addition (`+`) ကိုသုံးသွားပါတယ်။

### Arithmetic operators

Dart မှာ table တွင်ပြထားသလို ပုံမှန် arithmetic operators တွေကို support လုပ်ပါတယ်။

| Operator | Meaning                                                                    |
| :------- | :------------------------------------------------------------------------- |
| `+`      | Add                                                                        |
| `-`      | Subtract                                                                   |
| `-expr`  | Unary minuts, also known as negation (reverse the sign of the expresssion) |
| `*`      | Multiply                                                                   |
| `/`      | Divide                                                                     |
| `~/`     | Divide, returning an integer result                                        |
| `%`      | Get the remainder of an integer division (modulo)                          |

Example:

```dart
assert(2 + 3 == 5);
assert(2 - 3 == -1);
assert(2 * 3 == 6);
assert(5 / 2 == 2.5); // Result is a double
assert(5 ~/ 2 == 2); // Result is an int
assert(5 % 2 == 1); // Remainder

assert('5/2 = ${5 ~/ 2} r ${5 % 2}' == '5/2 = 2 r 1');
```

Dart မှာ prefix (increment/decrement) နဲ့ postfix (increment/decrement) operators တွေကို support လုပ်ပါသေးတယ်။

| Operator | Meaning                                         |
| :------- | :---------------------------------------------- |
| `++var`  | `var = var + 1` (expression value is `var + 1`) |
| `var++`  | `var = var + 1` (expression value is `var`)     |
| `--var`  | `var = var - 1` (expression value is `var - 1`) |
| `var--`  | `var = var - 1` (expression value is `var`)     |

Example

```dart
int a;
int b;

a = 0;
b = ++a; // Increment a before b gets its value.
assert(a == b); // 1 == 1

a = 0;
b = a++; //  Increment a AFTER b gets its value.
assert(a != b); // 1 != 0

a = 0;
b = --a; // Decreament a before b gets its value.
assert(a == b); // -1 == -1

a = 0;
b = a--; // Decreament a AFTER b gets its value.
assert(a != b); // -1 != 0
```

### Equality and relational operators

အောက်ပါ table မှာ equality နဲ့ relational operators တွေနဲ့ သူတို့ရဲ့ အဓိပ္ပါယ်တွေကို ဖော်ပြထားပါတယ်။

| Operator | Meaning                     |
| :------- | :-------------------------- |
| `==`     | Equal; see discussion below |
| `!=`     | Not equal                   |
| `>`      | Greater than                |
| `<`      | Less than                   |
| `>=`     | Greater than or equal to    |
| `<=`     | Less than or equal to       |

`==` operator ကိုသုံးတဲ့အခါမှာ၊ object နှစ်ခု x နဲ့ y ဆိုရင် ၎င်းနှစ်ခုက တူညီတဲ့အရာတွေကို ကိုယ်စားပြုပါတယ်။ (ဖြစ်တောင့်ဖြစ်ခဲပါ၊ သိထားသင့်တာရှိပါတယ်၊ object နှစ်ခုလုံက အတိအကျ တူညီနေရင် `identical()` ကို အစားထိုးသုံးနိုင်ပါတယ်။) ဒါကတော့ `==` operator ဘယ်လို အလုပ်လုပ်လဲဆိုတာပါ -

1. _x_ သို့မဟုတ် _y_ က null ဖြစ်ရင်၊ နှစ်ခုလုံး null ဖြစ်ရင် true ကို return ပြန်ပါတယ်၊ တစ်ခုက null ဖြစ်နေရင် false ပါ။
2. method invocation `x.==y.` ရဲ့ result ကို return ပါတယ်။ (မှန်ပါတယ်၊ `==` လို operators တွေက methods တွေဖြစ်ကြပြီး ၎င်းတို့က first operand ပေါ်မှာ invoke လုပ်ပါတယ်။ အသေးစိတ်အချက်အလက်ကို [Operators](https://dart.dev/guides/language/language-tour#_operators) မှာလေ့လာပါ။

ဒါက equality နဲ့ relational operators တွေ တစ်ခုခြင်း အသုံးပြုပုံ example တစ်ခုဖြစ်ပါတယ်

```dart
assert(2 == 2);
assert(2 != 3);
assert(3 > 2);
assert(2 < 3);
assert(3 >= 3);
assert(2 <= 3);
```

### Type test operators

`as`, `is`, နဲ့ `is!` operators တွေက runtime မှာ type chacking ကိုကိုင်တွယ်တဲ့ operators တွေဖြစ်ပါတယ်။

| Operator | Meaning                                                                                                                        |
| :------- | :----------------------------------------------------------------------------------------------------------------------------- |
| `as`     | Typecast (also used to specify [library prefixes](https://dart.dev/guides/language/language-tour#specifying-a-library-prefix)) |
| `is`     | True if the object has the specified type                                                                                      |
| `is!`    | True if the object doesn't have the specified type                                                                             |

`obj` က `T` ဖြင့်သတ်မှတ်ထားတဲ့ interface ကို implement လုပ်ထားရင် `obj is T` ရဲ့ result က true ဖြစ်ပါတယ်။ ဥပမာ `obj is Object?` က အမြဲတမ်း true ဖြစ်ပါတယ်။

object တစ်ခုကို particular type တစ်ခုအဖြစ်သို့ `as` operator သုံးပြီး cast လုပ်နိုင်ပါတယ်၊ ထို object က သူ့ရဲ့ type ဖြစ်ဖို့သေချာရင်ပေါ့။ ဥပမာ

> Java မှာဆို `(TextView)findViewById(R.id.textView);` က `(TextView)` cast လုပ်တာပါ။

```dart
(employee as Person).firstName = 'Bob';
```

object က type `T` ဖြစ်တာ မသေချာလောက်ဘူးဆိုရင်တော့ `is T` ကိုသုံးပြီးတော့ object ကိုမသုံးခင် check လုပ်နိုင်ပါတယ်။

```dart
if(employee is Person){
    // Type check
    employee.firstName = 'Bob';
}
```

> **Note:** တစ်ကယ်လို့ `employee` က null ဖြစ်မယ် ဒါမှာမဟုတ် `Person` တစ်ခုမဟုတ်ဘူးဆိုရင် code က equivalent မဖြစ်နိုင်ပါဘူး။ အဲလိုဖြစ်တဲ့အခါမှာ exception တစ်ခုကို throw နိုင်သလို ဘာမှမလုပ်ပဲလဲထားနိုင်ပါတယ်။

### Assignment operators

`=` operator နဲ့ values တွေကို assign လုပ်နိုင်တာ သိခဲ့ပြီးဖြစ်ပါတယ်။ assigned-to variable က null ဖြစ်နေမှာသာ assign လုပ်ပေးဖို့ `??=` operator ကိုသုံးနိုင်ပါတယ်။

```dart
// Assign value to a
a = value;

// Assign value to b if b is null; otherwise, b stays the same
b ??= value;
```

`+=` လို compound assignment operators တွေက operation တစ်ခုကို assignment တစ်ခုနဲ့ ပေါင်းစပ်ပေးပါတယ်။

|      |      |       |       |       |       |
| :--- | :--- | :---- | :---- | :---- | :---- |
| `=`  | `-=` | `/=`  | `%=`  | `>>=` | `^=`  |
| `+=` | `*=` | `~/=` | `<<=` | `&=`  | `\|=` |

ဒါကတော့ compound assignment operators တွေဘယ်လိုအလုပ်လုပ်လဲဆိုတာပါ။

|                           | Compound assignment | Equivalent expression |
| :------------------------ | :------------------ | :-------------------- |
| **For an operator _op_:** | a _op_= b           | a = a _op_ b          |
| **Example:**              | `a += b`            | `a = a + b`           |

အောက်ပါ example မှာတော့ assignment နဲ့ compound assignment operators သုံးထားပုံဖြစ်ပါတယ်။

```dart
var a = 2; // Assign using =
a *= 3; // Assign and multiply: a = a * 3;
assert(a == 6);
```

### Logical operators

logical operators တွေသုံးပြီးတော့ boolean expressions တွေကို invert သို့မဟုတ် combine လုပ်နိုင်ပါတယ်။

| Operator | Meaning                                                                   |
| :------- | :------------------------------------------------------------------------ |
| `!expr`  | inverts the following expressions (changes false tp true, and vice virsa) |
| `\|\|`   | logical OR                                                                |
| `&&`     | logical AND                                                               |

ဒါကတော့ logical operators တွေကိုအသုံးပြုပုံ example ဖြစ်ပါတယ်

```dart
if(!done && (col == 0 || col == 3)){
   // ...Do something...
}
```

### Bitwise and shift operators

Dart မှာ numbers တွေရဲ့ indivirtual bits တွေကို manipulate လုပ်လို့ရပါတယ်။ အမြဲတမ်းတော့ bitwise နဲ့ shift operators တွေကို integers တွေနဲ့ တွဲသုံးလေ့ရှိပါတယ်။

| Operator | Meaning                                               |
| :------- | :---------------------------------------------------- |
| `&`      | AND                                                   |
| `\|`     | OR                                                    |
| `^`      | XOR                                                   |
| `~expr`  | Unary bitwise complement (0s become 1s; 1s become 0s) |
| `<<`     | Shift left                                            |
| `>>`     | Shift right                                           |

ဒါကတော့ bitwise နဲ့ shift operators တွေကို အသုံးပြုပုံ example တစ်ခုဖြစ်ပါတယ်။

```dart
final value = 0x22;
final bitmask = 0x0f;

assert((value & bitmask ) == ); // AND
assert((value & ~bitmask) == ); // AND NOT
assert((value | bitmask) == ); // OR
assert((value ^ bitmask) == ); // XOR
assert((value << 4) == ); // Shift left
assert((value >> 4) == ); // Shift right
```

### Conditional expressions

Dart မှာ`if-else` statements တွေအလုပ်လုပ်သလိုပုံစံနဲ့ expressions တွေကို လိုတိုရှင်း evaluate လုပ်ပေးနိုင်တဲ့ operator နှစ်ခုရှိပါတယ်။

**_condition ? expr1 : expr2_**
_condition_ က true ဖြစ်တဲ့အခါ _expr1_ ကို evaluate (return it value) လုပ်မှာဖြစ်ပါတယ်။ ထိုနည်းတူ false ဖြစ်ရင်တော့ _expr2_ ရဲ့ value ကို return ပြန်ပေးမှာဖြစ်ပါတယ်။

**_expr1 ?? expr2_**
_expr1_ က non-null ဖြစ်ရင် သူ့ value ပဲပြန်ပေးမှာဖြစ်ပြီး null ဖြစ်ရင်တော့ _expr2_ ကို evaluate လုပ်ပြီးတန်ဖိုးကို return ပြန်ပေးမှာဖြစ်ပါတယ်။

boolean expression တစ်ခုပေါ်မှုတည်ပြီးတော့ value တစ်ခုကို assign လုပ်ဖိုလိုလာပြီဆိုရင် `?` နဲ့ `:` ကိုသုံးဖို့ သတိရလိုက်ပါ။

```dart
var visibility = isPublic ? 'public' : 'private';

```

boolean expression က null ကို test လုပ်ဖိုဆိုရင် `??` ကိုသုံးဖို့သတိရလိုက်ပါ။

```dart
String playerName(String? name) => name ?? 'Guest';
```

အထက်ပါ example ကို အခြားနည်းနဲ့ ရေးကြည့်မယ်ဆိုရင်ရပါတယ်၊ code တော့ရှည်ပါတယ် -

```dart
// Slightly longer version uses ?: operator
String playerName(String? name) => name != null ? name : 'Guest';

// Very long version uses if-else statement.
String playerName(String? name){
    if(name != null){
        return name;
    }else{
        return 'Guest';
    }
}
```

### Cascade notation

Cascades (`..`, `?..`) တွေက same object ပေါ်မှာရှိတဲ့ operations တွေရဲ့ sequence တစ်ခုကို ဖန်တီးဖို့ဖြစ်ပါတယ်။ function calls တွေကိုထပ်ပေါင်းထည့်ဖို့ ထို same object ပေါ်မှာ field တွေကို access လုပ်နိုင်ပါတယ်။ ၎င်က မကြာခနဆိုသလို ဖန်တီးထားတဲ့ temporary variable တစ်ခုရဲ့ stap ကို saves ထားပါတယ် ပြီးတော့ fluid code တွေ ပိုရေးနိုင်အောင်လည်းဆောင်ရွက်ပေးနိုင်ပါတယ်။

အောက်ပါ code ကိုကြည့်ပါ

```dart
var paint = Paint()
    ..color = Colors.black
    ..strokeCap = StrokeCap.round
    ..strokeWidth = 5.0;
```

constructor `Paint()` က `Paint` object ကို return ပြန်ပါတယ်။ cascade notation ရဲ့နောက်မှာရှိတဲ့ code က ထို object ပေါ်မှာ operate လုပ်ပါတယ်၊ returned လုပ်နိုင်တဲ့ value မှန်သမျှကို ignore လုပ်ပါတယ်။

ယခင် example က ဒီ code နဲ့ အတူတူပါပဲ

```dart
var paint = Paint();
paint.color = Colors.black;
paint.strokeCap = StrokeCap.round;
paint.strokeWidth = 5.0;
```

null ဖြစ်နိုင်တဲ့ object မှာ cascade operates လုပ်မယ်ဆိုရင် _null-shorting_ cascade (`?..`) တစ်ခုကို first operation အတွက်သုံးနိုင်ပါတယ်။ `?..` guarantees နဲ့ စတဲ့နေရာစပြီးတော့  
ထို null object ဖြစ်သွားရင် cascade operations တစ်ခုမှ အထမမြောက်တော့ပါဘူး။

```dart
querySelector('#confirm') // Get an object.
    ?..text = 'Confirm' // Use its members.
    ..classes.add('important')
    ..onCLick.listen((e) => window.alert('Confirmed!'));
```

> **Version note:** `?..` syntax က language version အနည်းဆုံး 2.12 ရှိမှရမှဖြစ်ပါတယ်။

ယခင် code နဲ့ ဒီ code နဲ့ အတူတူပါပဲ

```dart
var button = querySelector('#confirm');
button?.text = 'Confirm';
button?.classes.add('important');
button?.onClick.listen((e) => window.alert('Confirmed!'));
```

nest cascades တွေလည်းလုပ်နိုင်ပါသေးတယ်။ ဥပမာ

```dart
final addressBook = (AddressBookBuilder()
        ..name = 'jenny'
        ..email = 'jenny@example.com'
        ..phone = (PhoneNumberBuilder()
                ..number = '415-555-0100'
                ..label = 'home')
                .build())
        .build();
```

actual object တစ်ခုကို return လုပ်တဲ့ function တစ်ခုပေါ်မှာ cascade ကို construct လုပ်ရာမှာ သတိထားသင့်တာ ရှိပါတယ်။ ဥပမာ - အောက်ပါ code က fail ဖြစ်ပါတယ်။

```dart
var sb = StringBuffer();
sb.write('foo')
..write('bar'); // Error: method 'write' isn't defined for 'void'.
```

`sb.write()` call က void ကို return လုပ်ပါတယ် ပြီးတော့ cascade တစ်ခုကို void ပေါ်မှာ construct လုပ်လို့မရပါဘူး။

> **Note:** cascades အတွက် "double dot" notation က operator တစ်ခုမဟုတ်ပါဘူး။ Dart syntax ရဲ့ အစိတ်အပိုင်းတစ်ခုသာဖြစ်ပါတယ်။

### Other operators

တစ်ခြားကျန်ရှိနေတဲ့ operators တွေကို example နှင့်တကွ တွေ့မြင်ရပါမယ်။

| Operator | Name                      | Meaning                                                                                                                                                                                                                                 |
| :------- | :------------------------ | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `()`     | Function application      | function call တစ်ခုကို ကိုယ်စားပြုပါတယ်                                                                                                                                                                                                 |
| `[]`     | List access               | list ထဲမှာ သတ်မှတ်ထားတဲ့ index မှာ ရှိတဲ့ value ကို refer လုပ်ဖို့ဖြစ်ပါတယ်                                                                                                                                                             |
| `.`      | Member access             | expression တစ်ခုရဲ့ property တစ်ခုကို refers လုပ်ပါတယ်။ ဥပမာ `foo.bar` က expression `foo` မှ `bar` property ကို selects လုပ်ပါတယ်                                                                                                       |
| `?.`     | Conditional member access | `.` နဲ့တူပါတယ်။ သို့သော်လည်း leftmost operand က null ဖြစ်လို့ရပါတယ်။ ဥပမာ `foo?.bar` က expression `foo` မှ `bar` property ကို select လုပ်ပါတယ်၊ မဟုတ်လျှင် `foo` က null ဖြစ်ပါတယ်။ (ဒီလိုဖြစ်တဲ့အခါမှာ `foo?.bar` က null ဖြစ်သွားပါတယ်) |

`.`, `?.`, နဲ့ `..` operators တွေရဲ့ အချက်အလက်ကို [Classes](https://dart.dev/guides/language/language-tour#classes) မှာကြည့်နိုင်ပါတယ်။

## Control flow statements

အောက်ပါတိုက Dart code ရဲ့ flow ကို control လုပ်ဖို့ဖြစ်ပါတယ်

- `if` and `else`
- `for` loops
- `while` and `do-while` loops
- `break` and `continue`
- `switch` and `case`
- `assert`

`try-catch` နဲ့ `throw` သုံးပြီး control flow ကိုလည်း affect လုပ်နိုင်ပါသေးတယ်။ ၎င်းကို [Expressions](https://dart.dev/guides/language/language-tour#exceptions) မှာရှင်းပြထားပါတယ်။

### If and else

Dart မှာ `if` statement နဲ့ optional ဖြစ်တဲ့ `else` statement ကို support လုပ်ပါတယ်။ နောက်လာမည့် example မှာ ပြထားပါတယ်။ [conditional expressions](https://dart.dev/guides/language/language-tour#conditional-expressions) ကိုလည်း ကြည့်သင့်ပါတယ်။

```dart
if (idRaining()) {
    you.bringRainCoat();
} else if (isSnowing()) {
    you.wearJacket();
} else {
    car.putTopDown();
}
```

JavaScript နဲ့မတူတာက၊ conditions တွေက boolean values တွေဖြစ်ကိုဖြစ်ရပါမယ်၊ ကျန်တာဖြစ်လို့မရပါဘူး။ နောက်ထပ်အချက်အလက်များအတွက် [Booleans](https://dart.dev/guides/language/language-tour#booleans) ကိုကြည့်ပါ၊

### For loops

standard `for` loop နဲ့ iterate (အကြိမ်ကြိမ်) လုပ်နိုင်ပါတယ်။ ဥပမာ

```dart
var message = StringBuffer('Dart is fun');
for (var i = 0; i < 5; i++){
    message.write('!');
}
```

Dart ရဲ့ `for` loops အတွင်းမှာ index ရဲ့ _value_ ကို capture လုပ်ပါတယ်။ JavaScript မှာ တွေ့တတ်တဲ့ common pitfall ကို avoiding လုပ်ပါတယ်။ ဥပမာ

Dart

```dart
var callbacks = [];
for(var i = 0; i < 2; i++) {
    callbacks.add(() => print(i));
}
callbacks.forEach((c) => c());
```

JavaScript

```js
var callbacks = [];
for (var i = 0; i < 2; i++) {
  callbacks.push(() => print(i));
}
callbacks.forEach((c) => c());

function print(a) {
  return console.log(a);
}
```

dart မှာ output က 0 ရယ် 1 ရယ်ဖြစ်ပါတယ်။ JavaScript မှာဆိုရင် ဒီပုံစံက 2 နှစ်လုံးကို print ထုတ်ပေးမှာဖြစ်ပါတယ်။

iterating လုပ်နေတဲ့ object က Iterable (List သို့မဟုတ် Set လိုမျိုး) ဖြစ်နေရင် ပြီးတော့ လက်ရှိ iteration counter ကိုသိစရာမလိုတော့ရင် `for-in` ကိုသုံးနိုင်ပါတယ်။ သူက [iteration](https://dart.dev/guides/libraries/library-tour#iteration) lib မှဖြစ်ပါတယ်။

```dart
for(var candidate in candidates) {
    candidate.interview();
}
```

Iterable classes တွေမှာ `forEach()` method တစ်ခုရှိပါသေးတယ်၊ သူက another option ပါ။

```dart
var collection = [1, 2, 3];
collection.forEach(print); // 1 2 3
```

### While and do-while

`while` loop တစ်ခုက loop မစခင်မှာ condition ကို evaluates လုပ်ပါတယ်။

```dart
while(!isDone()){
    doSomething();
}
```

`do-while` loop တစ်ခု က iteration တစ်ပတ်ကို အရင် လုပ်ပြီးမှ condition ကို စပြီး evaluate လုပ်ပါတယ်။

```dart
do{
    printLine();
} while (!atEndOfPage());
```

### Break and continue

`break` ကို looping ကို stop လုပ်ဖို့သုံပါတယ်။

```dart
while(true){
    if(shutDownRequested()) break;
    processIncomingRequests();
}
```

`continue` ကို နောက် loop iteration တစ်ခုကို ခုန်ကူးဖို့သုံးပါတယ်။

```dart
for (int i = 0; i < candidates.length; i++) {
    var candidate = candidates[i];
    if (candidate.yearsExperience < 5) {
        continue;
    }
    candidate.interview();
}
```

ထို example ကို list သို့မဟုတ် set တစ်ခုကဲ့သို့ [Iterable](https://api.dart.dev/stable/dart-core/Iterable-class.html) တစ်ခုကိုသုံးပြီး လုံးဝ မတူတဲ့ နည်းနဲ့ ရေးနိုင်ပါသေးတယ်။

```dart
candidates
    .where((c) => c.yearsExperiences >= 5)
    .forEach((c) => c.interview());

```

### Switch and case

Dart မှာရှိတဲ့ switch statements တွေက integer, string, သို့မဟုတ် compile-time constants တွေကို `==` သုံပြီး compare လုပ်တာဖြစ်ပါတယ်။ compared objects တွေက same class ရဲ့ instances တွေဖြစ်ရပါမယ် (သူ့ရဲ့ subtype တောင်ဖြစ်လို့မရပါ)၊ ပြီးတော့ class က `==` ကို override လုပ်လို့မဖြစ်ပါဘူး။ [Enumerated types](https://dart.dev/guides/language/language-tour#enumerated-types) တွေကလည်း `switch` statements တွေနဲ့ တွဲပြီးအလုပ်လုပ်ပါတယ်။

non-empty `case` clause တိုင်းကို `break` statement တစ်ခုနဲ့ အဆုံးသပ်ပါတယ် (rule အရပါ။)။ အခြားသော မှန်ကန်တဲ့ အဆုံးသတ်ပုံနည်းလမ်းတွေရှိပါသေးတယ် ၎င်းတို့က `continue`, `throw`, သို့မဟုတ် `return` statement တွေနဲ့ none-empty `case` တွေကို အဆုံးသပ်ပေးတာဖြစ်ပါတယ်။

`case`clause တွေတစ်ခုနဲ့မှ match မဖြစ်တဲ့အခါမှာ `default` clause တစ်ခုကိုသုံးပြီးတော့ code ကို execute လုပ်နိုင်ပါတယ်။

```dart
var command = 'OPEN';
switch (command) {
    case 'CLOSED':
        executeClosed();
        break;
    case 'PENDING':
        executePending();
        break;
    case 'APPROVED':
        executeApproved();
        break;
    case 'DENIED':
        executeDenied();
        break;
    case 'OPEN':
        executeOpen();
        break;
    default:
        executeUnknown();
}
```

အောက်ပါ example ကတော့ `case` clause မှာ `break` statement ထည့်ဖိို့မေ့သွားရင် error တစ်ခု တက်မှာဖြစ်ကြောင်းပြထားတာပါ။

```dart
var command = 'OPEN';
switch (command) {
    case 'OPEN':
        executeOpen();
        // ERROR: Missing break
    case 'CLOSED':
        executeClosed();
        break;s
}
```

Dart က empty `case` clauses တွေကို support မပေးဘူးဆိုသော်လည်း from of fall-through တစ်ခုကို ခွင့်ပြုထားပါတယ်။

```dart
var command = 'CLOSED';
switch (command) {
    case 'CLOSED': // Empty case falls through.
    case 'NOW_CLOSED':
      // Runs for both CLOSED and NOW_CLOSE.
      executeNowClosed();
      break;
}
```

fall-through လုပ်ဖို့တကယ်လိုပြီဆိုရင် `continue` statement တစ်ခုနဲ့ label တစ်ခုကို သုံးနိုင်ပါတယ်။

```dart
var command = 'CLOSED';
switch (command) {
    case 'CLOSED':
        executeClosed();
        continue nowClosed;
        // Continues executing at the nowClosed label.

    nowClosed:
    case 'NOW_CLOSED':
        // Runs for both CLOSED and NOW_CLOSED.
        executeNowClosed();
        break;
}
```

`case` တစ်ခုကို local variable တစ်ခုပေးထားနိုင်ပါတယ်။ ထို local variable က ထို clause ရဲ့ scope ထဲမှာပဲ visible ဖြစ်ပါတယ်။

### Assert

development လုပ်စဉ်မှာ၊ assert statement တစ်ခုကို သုံးရပါတယ် - `assert(condition, optionalMessage);` - boolean condition တစ်ခု false ဖြစ်တဲ့အခါမှာ normal execution တစ်ခုကို ရပ်ပစ်လိုက်ဖို့ဖြစ်ပါတယ်။ ဒီ tour ထဲမှာ assert နဲ့ပတ်သက်တဲ့ example တွေအများကြီးရှိ့ပါတယ်။ ဒါကတော့ အပိုထပ်ဆောင်း example အချို့ဖြစ်ပါတယ်။

```dart
// Make sure the variable has a non-null value.
assert(text != null);

// Make sure the value is less then 100
assert(num < 100);

// Make sure this is an https URL.
assert(urlString.startsWith('https'));
```

assertion တစ်ခုထဲကို message တစ်ခု attach လုပ်ဖို့အတွက် ထို message string ကို `assert` (optionally with a trailing comma) ရဲ့ second arguement အနေနဲ့ထည့်သွင်းနိုင်ပါတယ်။

```dart
assert(urlString.startsWith('https'), 'URL ($urlString) should start with "https".');
```

`assert` မှာရှိတဲ့ first arguement က boolean value တစ်ခုကို resolve လုပ်ပေးတဲ့ expression တစ်ခုခုဖြစ်ရပါမယ်။ expression value က true ဖြစ်ရင် assertion က successed ဖြစ်ပြီး execution ကိုဆက်လက်လုပ်ဆောင်ပါမယ်။ တစ်ကယ်လို့ false ဖြစ်ရင် assertion က fail ဖြစ်မှပါ ပြီးတော့ exception (an [AssertionErroe](https://api.dart.dev/stable/dart-core/AssertionError-class.html)) တစ်ခုကို thrown သွားပါလိမ့်မယ်။

ဘယ်အချိန်မှာ assertion က အတိအကျအလုပ်လုပ်လဲ? ဒီမေးခွန်းက သင်အသုံးပြုတဲ့ tools တွေ framework အပေါ်မူတည်ပါတယ်။

- Flutter က [debug mode](https://flutter.dev/docs/testing/debugging#debug-mode-assertions) မှာ assertions ကို enables လုပ်ပါတယ်။

- development-only ဖြစ်တဲ့ [daetdevc]() လို tools မျိုူမှာ ပုံမှန်အားဖြင့် assertions ကို default အနေနဲ့ enabled လုပ်ထားပါတယ်။

- အချို့ tools တွေ [dart run](https://dart.dev/tools/dart-run) နဲ့ [dart2js](https://dart.dev/tools/dart2js) တို့လိုမှာ assertion ကို command-line flag `--enable-asserts` နဲ့ တွဲပြီး run မှာ support ရတာပါ။

production code မှာ assertoions တွေကို ignore လုပ်ပါတယ်။ ပြီးတော့ `assert` မှာထည့်ထားတဲ့ arguements တွေကို evaluated မလုပ်ပါဘူး။

## Exceptions

dart code တွေက exceptions တွေကို throw နဲ့ catch လုပ်နိုင်ပါတယ်။ exceptions တွေဆိုတာ တစ်စုံတစ်ခုက မမျော်လင့်ပဲဖြစ်သွားတတ်တဲ့ errors တွေကိုညွှန်ပြခြင်းဖြစ်ပါတယ်။ exception မဖြစ်ဖူးဆိုရင်၊ exception ကို raised လုပ်တဲ့ [isolate](https://dart.dev/guides/language/language-tour#isolates) က suspended ဖြစ်သွားပါတယ်၊ ပြီးတော့ isolate နဲ့ program က ထုံးစံအတိုင်း terminated ဖြစ်သွားပါတယ်။

Java နဲ့မတူတဲ့အချက်က၊ Dart ရဲ့ exceptions တွေအားလုံးက unchecked expressions တွေဖြစ်တာပဲ။ methods တွေက ဘယ် exception ကို throw လုပ်ရမယ်ဆိုပြီးတော့ declear လုပ်ထားခြင်းမရှိဘူး။ ပြီးတော့ မည်သည့် exception ကိုမှ catch လုပ်စရာမလိုဘူး။

Dart မှာ [Exception](https://api.dart.dev/stable/dart-core/Exception-class.html) နဲ့ [Error](https://api.dart.dev/stable/dart-core/Error-class.html) ဆိုပြီး type နှစ်မျိုးရှိတယ်။ နှစ်ခုလုံးက numerous predefined subtypes တွေ။ သင်ကိုယ်တိုင် ကိုယ်ပိုင် exceptions တွေ define လုပ်လို့ရယ်။ ဘယ်လိုပဲဖြစ်ဖြစ် Dart programs တွေက non-null object--not just Exception နဲ့ Error objects-- တို့ကို exception တစ်ခုကဲ့သို့ throw လုပ်နိုင်တယ်။

### Throw

ဒါကတော့ throwing လုပ်ခြင်းဖြစ်ပါတယ်။ သို့မဟုတ် exception တစ်ခုကို _raising_ လုပ်ခြင်းပေါ့

```dart
throw FormatException('Expected at least 1 section');
```

arbitrary objects တွေကိုလည်း throw လုပ်နိုင်ပါသေးတယ်။

```dart
throw 'Out of Llamas!';
```

> **Note:** Production-quality code တွေက [Error](https://api.dart.dev/stable/dart-core/Error-class.html) နဲ့ [Exception](https://api.dart.dev/stable/dart-core/Exception-class.html) ကို implements လုပ်တဲ့ types တွေကို အမြဲလိုလို throw လုပ်လေ့ရှိပါတယ်။

ဘာဖြစ်လို့လဲဆိုတော့ exception တစ်ခုကို throwing လုပ်တာက expression တစ်ခုဖြစ်နေလို့ဖြစ်ပါတယ်။ exceptions တွေကို => statements တွေနဲ့လည်း throw နိုင်ပါတယ်။ နှစ်ခုလုံးကို ဘယ်နေရာမှာမဆို့ expressions တွေကို ခွင့်ပြုပါတယ်။

```dart
void distanceTo(Point other) => throw UnimplementedError();
```

### Catch

Catching လုပ်ခြင်း၊ သို့မဟုတ် capturing လုပ်ခြင်း က propagating မှ exception ကို stops လုပ်တဲ့ exception ဖြစ်ပါတယ် (unless you rethrow the exception)။ exception တစ်ခုကို catching လုပ်ခြင်းက ၎င်းကို ကိုင်တွယ်ဖို့ အခွင့်အရေးတစ်ခု ရစေပါတယ်။

```dart
try {
    breedMoreLlamas();
} on OutOfLlamasException {
    buyMoreLlamas();
}
```

code တွေကို handle လုပ်ရာမှာ exception ရဲ့ type တစ်မျိုးထက်ပိုပြီးတော့ throw လုပ်လို့ရပါတယ်။ ပထမဆုံး catch clause က thrown လုပ်တဲ့ objects ရဲ့ type နဲ့ matches ဖြစ်လို့ဖြစ်ရင် exception ကို handles လုပ်ပါတယ်။ catch clause က type တစ်ခုကို specify မလုပ်ဘူးဆိုရင် ထို caluse က thrown object ရဲ့ type တစ်ခုခု နဲ့ handle လုပ်နိုင်ပါတယ်။

```dart
try {
    breedMoreLlamas();
} on OutOfLlamasException {
    // A specific exception
    buyMoreLlamas();
} on Exception catch (e) {
    // Anything else that is an exception
    print('Unknown exception: $e');
} catch (e) {
    // No specified type, handles all
    print('Something really unknown: $e');
}
```

`on` သို့မဟုတ် `catch` သို့မဟုတ် နှစ်ခုလုံးကို အသုံးပြုနိုင်ကြောင်း ရှေ့က code က ဖော်ပြထားတာဖြစ်ပါတယ်။ exceprion type ကို specify လုပ်လိုတဲ့အခါမှာ `on` ကိုသုံးပါတယ်။ `catch` ကိုတော့ exception handler က exception object ကို လိုအပ်တဲ့အခါမှာ သုံးပါတယ်။

`catch()` ထဲကို parameters တစ်ခု သိုမဟုတ် နှစ်ခု သတ်မှတ်ပေးနိုင်ပါတယ်။ ပထမ တစ်ခုက thrown လုပ်ပြီးသွားတဲ့ exception ဖြစ်ပါတယ်။ ဒုတိယဟာကတော့ stack trace (a [StackTrace](https://api.dart.dev/stable/dart-core/StackTrace-class.html) object) ဖြစ်ပါတယ်။

```dart
try {
    // ...
} on Exception catch (e) {
    print('Exception details:\n $e');
} catch (e, s) {
    print('Exception details:\n $e');
    print('Stack trace:\n $s');
}
```

exception တစ်ခုရဲ့ တစ်စိတ်တစ်ပိုင်းကို handle လုပ်ဖို့ သူ့ကို propagate လုပ်ဖို့ခွင့်ပြုထားစဉ်အတောအတွင်း `rethrow` keyword ကိုသုံးရပါတယ်။

"ဆိုလိုတာက၊ အောက်က ဥပမာမှာဆိုရင် `misbehave()` ဆိုတဲ့ method ရဲ့ အတွင်းမှာ၊ သူကိုယ်တိုင်တောင် error တက်လို try/catch လို့ throw ထားရပါတယ်။ main() method က သူ့ကိုပြန်ခေါ်သုံးရင် main() method မှာပါ error တက်အောင် `rethrow` ထပ်ပြီး throw လုပ်စေတာဖြစ်ပါတယ်"

```dart
void misbehave() {
    try {
        dynamic foo = true;
        print(foo++); // Runtime error
    } catch (e) {
        print('misbehave() partially handled ${e.runtimeType}.');
        rethrow; // Allow callers to see the exception.
    }
}

void main() {
    try {
        misbehave();
    } catch (e) {
        print('main() finished handling ${e.runtimeType}.');
    }
}
```

### Finally

အချို့ code တွေ runs လား ဒါမှမဟုတ် exception တစ်ခုကို thrown တာမဟုတ်ဘူးလား စတာတွေကို သေချာအောင်လုပ်ဖို့ `finally` clause တစ်ခုကို သုံးပါတယ်။ တကယ် `catch` clause တစ်ခုနဲ့မှ exception နဲ့ matches မဖြစ်တဲ့အခါ၊ exception က `finally` clause ကို runs ပြီးတဲ့နောက် propagated ဖြစ်သွားပါတယ်။

```dart
try {
    breedMoreLlamas();
} finally {
    // Always clean up, even if an exception is thrown.
    cleanLlamasStalls();
}
```

`catch` clauses တစ်ခုခု matching ဖြစ်ပြီးတဲ့နောက်မှာ `finally` clause ကို runs ပါတယ်။

```dart
try {
    breedMoreLlamas();
} catch () {
    print('Error: $e'); // Handle the exception first.
} finally {
    cleanLlamaStalls(); // Then clean up.
}
```

## Classes

Dart က classes တွေရယ် mixin-based inheritance တွေပါဝင်တဲ့ object-oriented language တစ်ခုဖြစ်ပါတယ်။ object တိုင်းက class တစ်ခုရဲ့ instance တစ်ခုဖြစ်ပါတယ်၊ `Null` မှလွဲလို့ classes တွေအားလုံးက [Object](https://api.dart.dev/stable/dart-core/Object-class.html) ကနေဆင်းသက်လာတာဖြစ်ပါတယ်။ _Mixin-based inheritance_ ဆိုတာက ([top class](https://dart.dev/null-safety/understanding-null-safety#top-and-bottom), `Object?` တို့မှလွဲလို) ကျန် classes အားလုံးမှာ superclass တစ်ခုအတိအကျရှိပါတယ်၊ class body တစ်ခုကို multiple class hierarchies ထဲမှာ ပြန်လည်အသုံးပြုနိုင်ပါတယ်။ [Extension methods](https://dart.dev/guides/language/language-tour#extension-methodss) တွေက class သို့မဟုတ် ဖန်တီးထားတဲ့ subclass တစ်ခုကို ပြောင်းလဲစရာမလိုပဲ class တစ်ခုသို့ လက်တွေကျစွာထည့်နိုင်တဲ့ နည်းတစ်ခုဖြစ်ပါတယ်။

### Using class members

Objects တွေမှာ _members_ တွေရှိပါတယ်၊ members တွေက functions တွေနဲ့ data (_methods_ and _instance variables_, respectively) တွေပါဝင်ကြပါတယ်။ method တစ်ခုကို call တဲ့အခါမှာ၊ object တစ်ခုပေါ်မှာ ၎င်းကို _invoke_ လုပ်ရပါတယ်။ ထို method မှာ object ရဲ့ function နဲ့ data ကို access ရသွားပါတယ်။

dot(.) တစ်ခုကိုသုံးပြီးတော့ instance variable သို့မဟုတ် method တစ်ခုကို refer လုပ်နိုင်ပါတယ်။

```dart
var p = Point(2, 2);

// Get the value of y.
assert(p.y == 2);

// Invoke distanceTo() on p.
double distance = p.distanceTo(Point(4, 4));
```

leftmost operand က null ဖြစ်တဲ့အခါမှာ `.` အစား `?.` ကို သုံးပြီတော့ exception တစ်ခုကို avoid လုပ်နိုင်ပါတယ်။

```dart
// If p is non-null, set a variable equal to its y value.
var a = p?.y;
```

### Using constructors

_constructor_ တစ်ခုကိုသုံးပြီးတော့ object တစ်ခုကို create လုပ်နိုင်ပါတယ်။ Constructors တွေရဲ့ names တွေက `ClassName` သို့မဟုတ် `ClassName.identifier` ဖြစ်နိုင်ပါတယ်။ ဥပမာ အောက်ပါ code က `Point` objects တွေကို `Point()` နဲ့ `Point.fromJson()` constructors တွေသုံးပြီး ဖန်တီးထားတာဖြစ်ပါတယ်။

```dart
var p1 = Point(2, 2);
var p2 = Point.fromJson({'x': 1, 'y': 2});

```

အောက်ပါ code မှာလည်းတူညီတဲ့ သက်ရောက်မှုတွေရှိပါတယ်၊ သိုသော်လည်း `new` optional keyword ကို constructor name ရဲ့ရှေ့မှာ သုံးထားပါတယ်။

```dart
var p1 = new Point(2, 2);
var p2 = new Point.fromJson({'x': 1, 'y': 2});
```

> **Version note:** `new` keyword က Dart 2 မှာ optional ဖြစ်သွားပါတယ်။

အချို့သော classes တွေက [constant constructors](https://dart.dev/guides/language/language-tour#constant-constructors) တွေကို provide လုပ်ပါတယ်။ compile-time constant တစ်ခုကိုဖန်တီးဖို့အတွက် constant constructor တစ်ခုကိုသုံးရပါတယ်၊ `const` keyword က constructor name ရှေ့မှာ ထည့်ပေးရတာပါ။

```dart
var p = const ImmutablePoint(2, 2);
```

identical compile-time constants နှစ်ခုကို Constructing လုပ်ရာမှာ result က single, , canonical instance တစ်ခုဖြစ်သွားပါတယ်။

```dart
var a = const ImmutablePoint(1, 1);
var b = const ImmutablePoint(1, 1);

assert(identical(a, b)); // They are the same instance!
```

_constant context_ တစ်ခုအတွင်းမှာ constructor သို့မဟုတ် literal တစ်ခုရဲ့ရှေ့မှာ `const` ကို ချန်ခဲ့နိုင်ပါတယ်။ ဥပမာ ဒီ code ဆိုရင် const map တစ်ခုကို ဖန်တီးထားတာဖြစ်ပါတယ်။

```dart
// Lots of const keywords here
const pointAndLine = const {
    'point': const [const ImmutablePoint(0, 0)],
    'line': const [const ImmutablePoint(1, 10), const ImmutablePoint(-2, 11)],
};
```

`const` keyword ကိုပထမဆုံးသုံလိုက်တာနဲ့ အားလုံကို အားလုံးကို ချန်ထားခဲ့နိုင်ပါတယ်

```dart
// Only one const, which establishes the constant context.
const pointAndLine = {
    'point': [ImmutablePoint(0, 0)],
    'line': [ImmutablePoint(1, 10), ImmutablePoint(-2, 11)],
};
```

constant constructor တစ်ခုက constant context တစ်ခုရဲ့ အပြင်ဘက်ရောက်နေတဲ့အခါနဲ့ `const` မပါပဲ invoked လုပ်ရင်၊ သူက **non-constant object** တစ်ခုကို ဖန်တီးပါတယ်။

```dart
var a = const ImmutablePoint(1, 1); // Creates a constant
var b = ImmutablePoint(1, 1); // Does NOT create a constant

assert(!identical(a, b)); // NOT the same instance!
```

> **Version note:** constant context တစ်ခုထဲက `const` keyword က Dart 2 မှာ optional ဖြစ်သွားပါတယ်။

### Getting an object's type

runtime မှာ object တစ်ခုရဲ့ type ကိုရဖို့အတွက် `Object` property `runtimeType` ကိုသုံးနိုင်ပါတယ်။ သူက [Type](https://api.dart.dev/stable/dart-core/Type-class.html) object တစ်ခုကို return ပြန်ပေးမှာဖြစ်ပါတယ်။

```dart
print('The type of a is ${a.runtimeType}');
```

classes တွေကို ဘယ်လိုသုံးတယ်ဆိုတာ တွေ့ပြီးဖြစ်ပါတယ်။ ဒီ section ရဲ့ အဆုံးမှာ classes တွေကို ဘယ်လို _implement_ လုပ်လဲဆိုတာကိုဖော်ပြပေးထားပါတယ်။

### Instance variables

ဒါကတော့ instance variables တွေကြေငြာပုံဖြစ်ပါတယ်

```dart
class Point {
    double? x; // Declare instance variable x, initially null.
    double? y; // Declare y, initially null.
    double? z = 0; // Declare z, initially 0.
}
```

initialized မလုပ်ရသေးတဲ့ instance variables တိုင်းမှာ value `null` ရှိပါတယ်။

instance variables တွေအားလုံးက _getter_ method တစ်ကို generate လုပ်ပါတယ်။ non-final instance variables တွေနဲ့ `late` `final` instance variables တွေက initializers တွေမရှိလည်းပဲ _setter_ method တစ်ခုကို generate လုပ်ပါတယ်။ အသေးစိတ်ကို [Getters and setters](https://dart.dev/guides/language/language-tour#getters-and-setters) မှာကြည့်နိုင်ပါတယ်။

non-`late` instance variable တစ်ခု ကြေငြာထားတဲ့နေရာမှာ initialize လုပ်ရင်၊ instance က created လုပ်ပြီးမှာ value ကို set လုပ်မှာဖြစ်ပါတယ်။ ၎င်းက constructor မတိုင်မှီနဲ့ သူရဲ့ initializer list က execute မလုပ်ခင်ဖြစ်ပါတယ်။

```dart
class Point(){
    double? x; // Declare instance variable x, initially null.
    double? y; // Declare y, initially null.
}

void main(){
    var point = Point();
    point.x = 4; // Use the setter method for x.
    assert(point.x == 4); // Use the getter method for x.
    assert(point.y == null); // Values default to null.
}
```

Instance variables တွေက `final` ဖြစ်နိင်ပါတယ်၊ ထို case မှာ သူတို့ကို လုံးဝတူညီတဲတစ်ခုခုကို set လုပ်ပေးရပါမယ်။ `final`, non-`late` instance variables တွေကို declaration လုပ်စဉ်မှာ Initialize လုပ်ရင် constructor parameter တစ်ခုကို အသုံပြုခြင်း သို့မဟုတ် constructor တစ်ခုရဲ့ [initializer list](https://dart.dev/guides/language/language-tour#initializer-list) တစ်ခုကို အသုံးပြုခြင်း ဖြင့်ဆောင်ရွက်ရပါတယ်။

```dart
class ProfileMark {
    final String name;
    final DateTime start = DateTime.now();

    ProfileMark(this.name);
    ProfileMark.unnamed() : name = '';
}
```

`final` instance variable တစ်ခုရဲ့ value ကို assign လုပ်လိုလျှင် constructor body စတဲ့နေရာမှာ `late` `final` ကိုသုံးပေးရပါတယ်။ သတိတော့ထားရပါမယ်။ [be careful](https://dart.dev/guides/language/effective-dart/design#avoid-public-late-final-fields-without-initializers)

### Constructors

function တစ်ခုကို သူ့ရဲ့ class နံမည်နဲ့ ဖန်တီးပြီး constructor တစ်ခုကို declare လုပ်ရပါတယ်။ (plus, optionally, an additional identifier as described in [Named constructors](https://dart.dev/guides/language/language-tour#named-constructors)).
ဘုံအသုံးပြုလေ့ရှိတဲ့ constructor ရဲ့ form ကတော့ generative constructor၊ class တစ်ခုရဲ့ new instance တစ်ခုကို ဖန်တီးတဲ့ပုံဖြစ်ပါတယ်။

```dart
class Point {
    double x = 0;
    double y = 0;

    Point(double x, double y) {
        // There's a better way to do this, stay tuned.
        this.x = x;
        this.y = y;
    }
}
```

`this` keyword က current instance ကို refers လုပ်ပါတယ်။

> **Note:** name conflict တစ်ခုဖြစ်တဲ့အခါမှသာ `this` ကိုသုံးပါတယ်။ တနည်းဆိုရလျှင် Dart style က `this` ကို omits လုပ်ထားပါတယ်။

instance variable တစ်ခုထဲကို constructor argument တစ်ခု assigning လုပ်တဲ့ pattern က အရမ်း common ဖြစ်လွန်းအားကြီးပါတယ်။ Dart မှာ ၎င်းကိုလွယ်သွားအောင်လုပ်ဖို့ syntactic sugar ဆိုတာရှိပါတယ်။

```dart
class Point {
    double x = 0;
    double y = 0;

    // Syntactic sugar for setting x and y
    // before the constructor body runs.
    Point(this.x, this.y);
}
```

### Defult constructors

constructor မကြေငြာပဲထားရင် default constructor တစ်ခုနဲ့ ထောက်ပံ့ပေးသွားမှာဖြစ်ပါတယ်။ default constructor မှာ arguments တွေမရှိပါဘူး ပြီးတော့ superclass ထဲ no-argument constructor ကို invokes လုပ်ပါတယ်။

### Constructors aren't inherited

subclasses တွေက သူတို့ရဲ့ superclass တွေမှ constructors တွေကို inherit လုပ်ထားတာမဟုတ်ပါဘူး။ constructors တစ်ခုမှ declare လုပ်ထားခြင်းမရှိတဲ့ subclass တစ်ခုမှာ default (no argument, no name) constructor တစ်ခုသညလျှင်ရှိပါတယ်။

### Named constructors

named constructor တစ်ခုကို class တစ်ခုအတွက် multiple constructors တွေ implement လုပ်ဖို့သုံးပါတယ်။ သို့မဟုတ် extra clarity ကို provide လုပ်ဖို့သုံးပါတယ်။

```dart
const double xOrigin = 0;
const double yOrigin = 0;

class Point {
    double x = 0;
    double y = 0;

    Point(this.x, this.y);

    // Named constructor
    Point.origin()
        : x = xOrigin,
          y = yOrigin;
}
```

constructors တွေက inherited မဟုတ်ကြောင်း သတိပြုပါ။ ဆိုလိုတာက ထို superclass ရဲ့ named constructor က subclass တစ်ခုနဲ့ inherited လုပ်ထားတာမဟုတ်တဲ့ အတွက်ဖြစ်ပါတယ်။ တကယ်လို့များ named constructor တစ်ခုနဲ့တွဲပြီး subclass တစ်ခုကို ဖန်တီးလိုတယ်ဆိုရင် superclass ထဲမှာ သတ်မှတ်ပေးရမှာဖြစ်ပါတယ်။ ထို constructor ကို subclass ထဲမှာ မဖြစ်မနေ implement လုပ်ပေးရမှာပါ။

### Invoking a non-default superclass constructor

default အနေနဲ့ subclass ထဲမှာရှိတဲ့ constructor တစ်ခုကို superclass’s unnamed, no-argument constructor လို့ခေါ်ပါတယ်။ superclass ရဲ့ constructor က constructor body အစမှာ called လုပ်ပါတယ်။ [initializer list](https://dart.dev/guides/language/language-tour#initializer-list) တစ်ခုကိုလည်း အသုံပြုထားတယ်ဆိုရင် superclass ကို called မလုပ်ခင်မှာ သူ့ကို executes လုပ်ပါတယ်။ အကျဉ်းချုပ်ပြောရလျှင် execution ရဲ order ကအောက်ပါအတိုင်းဖြစ်ပါတယ် -

1. initializer list
2. superclass's no-arg constructor
3. main class's no-arg constructor

တကယ်လို့ superclass မှာ unnamed, no-argument constructor မပါခဲ့လို့ရှိရင် superclass ထဲမှာရှိတဲ့ constructors တွေထဲက တစ်ခုကို manual နဲ့ call လုပ်ရမှာဖြစ်ပါတယ်။ superclass constructor ကို specify ပြီးတဲ့နောက်မှာ colon (`:`) တစ်ခုထည့်ပေးရပါတယ်။ constructor body (if any) ရဲ့ရှေ့ပေါ့။

အောက်ပါ example မှာ Employee class အတွက် constructor က သူ့ရဲ့ superclass, Person အတွက် named constructor ကို calls လုပ်ပါတယ်။

```dart
class Person {
    String? firstName;

    Person.fromJson(Map data) {
        print('in Person');
    }
}

class Employee extands Person {
    // Person does not have a default constructor;
    // you must call super.fromJson(data).
    Employee.fromJson(Map data) : super.fromJson(data){
        print('in Employee');
    }
}

void main() {
    var employee = Employee.fromJson({});
    print(employee);
    // Prints:
    // in Person
    // in Employee
    // Instance of 'Employee'
}
```

ဘာဖြစ်လို့ဆိုတော့ superclass constructor ကိုပေးတဲ့ arguements တွေက constructor ကို invoke မလုပ်ခင်မှာ evlauate လုပ်တဲ့အတွက်ကြောင့်ဖြစ်ပါတယ်။ aeguement တွေက function call တစ်ခုကို expression တစ်ခုဖြစ်သောကြောင့်ဖြစ်ပါတယ်။

```dart
class Employee extands Person {
    Employee() : super.fromJson(fetchDefaultData());
    // ...
}
```

> **Warning:** superclass constructor ကိုပို့တဲ့ arguements တွေက `this` ကိုလက်မခံပါဘူး။ ဥပမာ - arguements တွေက static methods တွေကို call လုပ်နိုင်ပြီး instance methods တွေကို တော call မလုပ်နိုင်ပါဘူး။

### Initializer list

superclass constructor ကို invoke လုပ်နိုင်တဲ့အပြင် constructor body ကို run မလုပ်ခင်မှာ instance variables တွေကို initialize လုပ်နိုင်ပါသေးတယ်။ initializers တွေကို commas တွေနဲ့ ခြားရေးပေးရပါတယ်။

```dart
// Initializer list sets instance variables before
// the xonstructor body runs.
Point.fromJson(Map<String, double> json)
    : x = json['x']!,
      y = json['y']!{
          print('In Point.fromJson(): ($x, $y)');
      }
```

final fields တွေကို setting up လုပ်တဲ့အချိန်မှာ initializer lists တွေကို handy လုပ်ပါတယ်။ အောက်ပါ initializes တွေရဲ့ example မှာ initializer list တစ်ခုအတွင်းမှာ final fields သုံးခုရှိပါတယ်၊

```dart
import 'dart:math';

class Point {
    final double x;
    final double y;
    final double distanceFromOrigin;

    Point(double x, double y)
        : x = x,
          y = y,
          distanceFromOrigin = sqrt(x * x + y * y);
}

void main() {
    var p = Point(2, 3);
    print(p.distanceFromOrigin);
}
```

### Redirecting constructors

တစ်ခါတစ်လေမှာ constructor တစ်ခုရဲ့ တစ်ခုတည်းသောရည်ရွယ်ချက်က ရှိနေတဲ့ class ထဲက အခြား constructor ကို redirect လုပ်ဖို့ဖြစ်ပါတယ်။ redirecting constructor တစ်ခုရဲ့ body က empty ပါ။ ၎င်းရဲ့နောက်မှာ colon (:) တစ်ထည့်ပြီး constructor call နဲ့တွဲထားပါတယ်။

```dart
class Point {
    double x, y;

    // The main constructor for this class.
    Point(this.x, this.y);

    // Delegates to the main constructor.
    Point.alongXAxis(double x) : this(x, 0);
}
```

### Constant constructors

class က ဘယ်တော့မှာပြောင်းလဲသွားခြင်းမရှိတဲ့ objects တွေကို ထုတ်ပေးတာမျိုးဆိုရင် ထို objects တွေကို compile-time constants တွေအဖြစ်လုပ်လို့ရပါတယ်။ ၎င်းကိုပြုလုပ်ဖို့ဆိုရင် `const` constructor တစ်ခုကို သတ်မှတ်ပေးရပါမယ် နောက်ပြီးတော့ instant variables တွေအားလုံးက `final` ဖြစ်တာ သေချာဖို့လို့ပါတယ်။

```dart
class ImmutablePoint {
    static const ImmutablePoint origin = ImmutalePoint(0, 0);

    final double x, y;

    const ImmutablePoint(this.x, this.y);
}
```

Constant constructors တွေ constants တွေကို အမြဲတော့ create မလုပ်ပါဘူး။ အသေးစိတ်ကို [using constructors](https://dart.dev/guides/language/language-tour#using-constructors) section မှာလေ့လာနိုင်ပါတယ်။

### Factory constructors

class ရဲ့ new instance တစ်ခုကို အမြဲတမ်း create လုပ်ပေးခြင်းမရှိတဲ့ constructor တစ်ခုကို implementing လုပ်နေတဲ့ အခါမှာ `factory` keyword ကိုအသုံးပြုရပါတယ်။ ဥပမာ factory constructor တစ်ခုက cache တစ်ခုကနေ instant တစ်ခုကို return လုပ်ကောင်းလုပ်နိုင်တယ် ဒါမှမဟုတ် subtype တစ်ခုရဲ့ instance တစ်ခုကို return လည်းလုပ်နိုင်တယ။ fastory constructors တွေကို အခြားအသုံးပြုရတဲ့ အကြောင်းက initializer list ထဲမှာ handled မလုပ်နိုင်တဲ့ logic ကိုသုံးထားတဲ့ final variable တစ်ခုကို initializing လုပ်ဖို့ဖြစ်ပါတယ်။

အောက်ပါ example မှာ `Logger` factory constructor က cache တစ်ခုက objects တွေကို returns ပြန်ပေးပါတယ်။ ပြီးတော့ `Logger.fromJson` factory constructor က JSON object တစ်ခုမှ final variable တစ်ခုကို initializes လုပ်တာဖြစ်ပါတယ်။

```dart
class Logger {
    final String name;
    bool mute = false;

    // _cache is library-private, thanks to
    // the _ in front of its name.
    static final Map<String, Logger> _cache =
        <String, Logger>{};

    factory Logger(String name) {
        return _cache.putIfAbsent(
        name, () => Logger._internal(name));
    }

    factory Logger.fromJson(Map<String, Object> json) {
        return Logger(json['name'].toString());
    }

    Logger._internal(this.name);

    void log(String  msg) {
        if (!mute) print(msg);
    }
}
```

> **Note:** Factory constructors တွေက `this` ကိုလက်မခံပါဘူး။

factory constructor တစ်ခုကို invoke လုပ်ရတာက အခြားသော constuctor တွေနဲ့အတူတူပါပဲ။

```dart
var logger = Logger('UI');
logger.log('Button clicked');

var logMap = {'name': 'UI'};
var loggerJson = Logger.fromJson(logMap);
```

## Methods

object တစ်ခုအတွက် behavior ကို provide လုပ်ပေးတဲ့ functions တွေက methods တွေဖြစ်ပါတယ်။

### Instance methods

objects တွေပေါ်မှာရှိတဲ့ instance methods တွေက instance variables တွေနဲ့ `this` ကို access လုပ်နိုင်ကြပါတယ်။ အောက်ပါ simple မှ `distanceTo()` methid က instance method တစ်ခုရဲ့ ဥပမာဖြစ်ပါတယ်။

```dart
import 'dart:math';

class Point {
    double x = 0;
    double y = 0;

    Point(this.x, this.y);

    double distanceTo(Point other){
        var dx = x - other.x;
        var dy = y - other.y;
        return sqrt(dx * dx + dy * dy);
    }
}
```

### Operators

Operators တွေက special names တွေတပ်ထားတဲ့ instance methods တွေဖြစ်ကြပါတယ်။ Dart မှာ အောက်ပါ နာမည်တွေရှိတဲ့ operators တွေကို သင်ကိုယ်တိုင် သတ်မှတ်ပေးနိုင်ဖို့ ခွင့်ပြုုထားပါတယ်။

|      |      |      |       |
| :--- | :--- | :--- | :---- |
| `<`  | `+`  | `\|` | `[]`  |
| `>`  | `/`  | `^`  | `[]=` |
| `<=` | `~/` | `&`  | `~`   |
| `>=` | `*`  | `<<` | `==`  |
| `-`  | `%`  | `>>` |       |

> **Note:** တစ်ချို့ [operators](https://dart.dev/guides/language/language-tour#operators) တွေကို သတိပြုမိလိမ့်မယ်ထင်ပါတယ်။ `!=` လိုတွေက စာရင်းထဲမှာ မပါပါဘူး။ ဘာဖြစ်လို့လဲဆိုတော့ သူတို့က syntaciic sugar ဖြစ်နေလို့ပါ။ ဥပမာ expression `e1 != e2` က `!(e1 == e2)` အတွက် syntactic sugar ဖြစ်ပါတယ်။

operator declaration တစ်ခုကို identified လုပ်ဖို့ built-in identifier `operator` ကိုသုံးရပါတယ်။ အောက်ပါ example က vector addition (`+`) နဲ့ subtraction (`-`) ကို defines လုပ်တာဖြစ်ပါတယ်။

```dart
class Vector {
    final int x, y;

    Vector(this.x, this.y);

    Vector operator +(Vactor v) => Vector(x + v.x, y + v.y);
    Vector operator -(Vactor v) => Vector(x - v.x, y - v.y);

    // Operator == and hashCode not shown
    // ...
}

void main() {
    final v = Vector(2, 3);
    final w = Vector(2, 2);

    assert(v + w == Vector(4, 5));
    assert(v - w == Vector(0, 1));
}
```

### Getters and setter

Getters နဲ့ Setters တိုက special methods တွေဖြစ်ပါတယ်။ သူတိို့က object တစ်ခုရဲ့ properties တွေကို read နဲ့ write access လုပ်ဖို့ provide ပေးထားတဲ့ အရာတွေဖြစ်ပါတယ်။ ၎င်းကို recall လုပ်တဲ့အခါမှာ instance variable တစ်ခုခြင်မှာ getter တစ်ခုရှိသွားပါတယ်၊ appropriate ဖြစ်လျှင် setter တစ်ခု plus လုပ်ပါတယ်။ additional properties တွေကို getters နဲ့ setters တွေ implementing လုပ်ခြင်းဖြင့် ဖန်တီးနိုင်ပါတယ်။ ထိုသို့ဖန်တီးဖို့ `get` နဲ့ `set` keywords တွေကိုသုံးရပါတယ်။

```dart
class Rectangle {
    double left, top, width, height;

    Rectangle(this.left, this.top, this.width, this.height);

    // Define two calculated properties: right and bottom.
    double get right => left + width;
    set right(double value) => left = value - width;
    double get bottom => top + height;
    set bottom(double value) => top = value - height;
}

void main() {
    var rect = Rectangle(3, 4, 20, 15);
    assert(rect.left == 3);
    rect.right = 12;
    assert(rect.left == -8);
}
```

getters နဲ့ setters တွေနဲ့ ဆိုရင် instant variables တွေနဲ့ စလို့ရပါတယ်၊ နောက်ပိုင်း သူတို့ကို methods တွေနဲ့ wrapping လုပ်ပြီးရပါမယ်။ client code တစ်ခုမှ changing လုပ်စရာမလိုပါဘူး။

> **Note:** increment (++) လို operators တွေက getter ကို အတိအလင်း defined လုပ်လား မလုပ်ဘူးလားဆိုတဲ့ မျော်လင့်ထားတဲ့နည်းအတိုင်း အလုပ်လုပ်ပါတယ်။ မလိုလားအပ်တဲ့ side effects တစ်ခုခုကို ပယ်ဖို့အတွက် getter exactly once ဆိုတဲ့ operator ကိုသုံးပြီး သူ့ value ကို temporary variable တစ်ခုထဲမှာသိမ်းထားနိုင်ပါတယ်။

### Abstract methods

instance, getter, နဲ့ setter methods တွေကို abstract အဖြစ်လုပ်ခြင်း interface တစ်ခု သတ်မှတ်ခြင်းလုပ်လို့ရပါတယ်၊ သို့သော် ၎င်းရဲ့ implementation ကို အခြားသော classes တွေက leaving လုပ်ပါတယ်။ abstract methods တွေက [abstract classes](https://dart.dev/guides/language/language-tour#abstract-classes) တွေအတွင်းမှာသာတည်ရှိနိုင်ပါတယ်။

method abstract တစ်ခုကို ပြုလုပ်ဖို့အတွက် method body နေရာမှာ semicolon (;) တစ်ခု အစားထိုး အသုံးပြုရပါတယ်။

```dart
abstract class Doer {
    // Define instance variables and methods...

    void doSomething(); // Define and abstract method.
}

class EffectiveDoer extends Doer {
    void doSomething() {
        // Provide an implementation, so the method is not a abstract here...
    }
}
```

### Abstract classes

_abstract class_ တစ်ခုကို သတ်မှတ်ဖို့အတွက် `abstract` modifier ကိုသုံရပါတယ်။ abstract class ဆိုတာက insrantiated လုပ်လို့မရတဲ့ class တစ်ခုဖြစ်ပါတယ်။ တချို့သော implementation တွေနဲ့ မကြခနဆိုသလို့ abstract classes တွေက interfaces တွေ သတ်မှတ်ဖို့ အသုံးဝင်ပါတယ်။ abstract class ကို instantiable အဖြစ်သို့ appear လုပ်ချင်လျှင် [factory constructor](https://dart.dev/guides/language/language-tour#factory-constructors) တစ်ခုကို သတ်မှတ်ပေးရပါတယ်။

abstract classes တွေမှာ မကြာခနဆိုသလို [abstract methods](https://dart.dev/guides/language/language-tour#abstract-methods) တွေရှိတတ်ပါတယ်။ အောက်ပါ example ကတော့ abstract method တစ်ခုပါတဲ့ abstract class တစ်ခုကို declaring လုပ်ပုံဖြစ်ပါတယ်။

```dart
// This class is declared abstract and thus
// can't be instantiated.
abstract class AbstractContainer {
    // Define constructors, fields, methods...

    void updateChildren(); // Abstract method.
}
```

### Implicit interfaces

class တိုင်းက class နဲ့ ၎င်းက implements လုပ်ထားတဲ့ interface တစ်ခုခု ရဲ့ instance members တွေအားလုံးပါဝင်တဲ့ interface တစ်ခုကို အကြွင်းမဲ့ defines လုပ်ပေးပါတယ်။

B ဆိုတဲ့ class ရဲ့ implementation ကို inheriting မလုပ်ပဲ B class ရဲ့ API ကို supports လုပ်တဲ့ A ဆိုတဲ့ class တစ်ခုကို ဖန်တီးချင်တယ်ဆိုရင်၊ A က B interface ကို implement လုပ်သင့်ပါတယ်။

class တစ်ခုက interface တစ်ခုနဲ့ တစ်ခုအထက် implements လုပ်လို့ရပါတယ်၊ ထိုသို့ပြုလုပ်ဖို့အတွက် `implements` clause တစ်ခုထဲမှာ ၎င်းတို့ကိုကြေငြာရပါတယ်။ ထိုနောက် interfaces တွေနဲ့ လိုအပ်တဲ့ APIs တွေကို ထောက်ပံ့ပေးရပါတယ်။ ဥပမာ-

```dart
// A person. The implicit interface contains greet().
class Person {
    // In the interface, but visible only in library.
    final String _name;

    // Not in the interface, since this is a constructor.
    Person(this._name);

    // In the interfaace.
    String greet(String who) => 'Hello, $who. I am $_name.';
}

// An implementation of the Person interface.
class Impostor implements Person {
    String get _name => '';

    String greet(String who) => 'Hi $who. Do you know who I am?';
}

String greetBob(Person person) => person.greet('Bob');

void main() {
    print(greetBob(Person('Kathy')));
    print(greetBob(Impostor()));
}
```

ဒါကတော့ multiple interfaces တွေကို class တစ်ခုက implements လုပ်တာကိ သတ်မှတ်ပေးပုံဖြစ်ပါတယ်။

```dart
class Point implements Comparable, Location {...}
```

### Extending a class

subclass တစ်ခုကိုဖန်တီးဖို့အတွက် `extends` ကိုသုံးရပါတယ်။ `super` ကတော့ superclass တစ်ခုကို refer လုပ်ဖို့ဖြစ်ပါတယ်။

```dart
class Television {
    void turnOn() {
        _illuminateDisplay();
        _activateIrSensor();
    }
    // ...
}

class SmartTelevision extends Television {
    void turnOn() {
        super.turnOn();
        _bootNetworkInterface();
        _initializeMemory();
        _upgradeApps();
    }
    // ...
}
```

### Overriding members

Subclass တွေက instance methods (including [operators](https://dart.dev/guides/language/language-tour#_operators)), getters, နဲ့ setters တွေကို override လုပ်နိုင်ပါတယ်။ `@override` annotation ကိုသုံးပြီးတော့ member တစ်ခုကို overriding လုပ်ထားကြောင်း အများသိအောင် indicate လုပ်နိုင်ပါတယ်။

```dart
class SmartTelevision extends Television {
    @override
    void turnOn() {...}
    // ...
}
```

code ထဲမှာရှိတဲ့ method parameter တစ်ခု ရဲ့ type သို့မဟုတ် instance variable ရဲ့ type ကို ကျဉ်းသွားအောင်လုပ်တာက [type safe](https://dart.dev/guides/language/type-system) ဖြစ်ပါတယ်။ [`covariant` keyword](https://dart.dev/guides/language/sound-problems#the-covariant-keyword) ကိုသုံးနိုင်ပါတယ်။

> **Warning:** `==` ကို override လုပ်တဲ့အခါမှာ Object ရဲ့ `hashCode` getter ကိုပါ override လုပ်သင့်ပါတယ်။ ဥပမာအနေနဲ့ `==` နဲ့ `hashCode` ကို overriding လုပ်တာကို [Implementing map keys](https://dart.dev/guides/libraries/library-tour#implementing-map-keys) မှာကြည့်နိုင်ပါတယ်။

### noSuchMethod()

detect လုပ်ဖို့ဖြစ်ဖြစ် react လုပ်ဖို့ဖြစ်ဖြစ် code က non-existent method တစ်ခု သို့မဟုတ် instance variable ကိုသုံးဖို့ကြိုးစားရင်၊ `noSuchMethod()` ကို override လုပ်နိုင်ပါတယ်။

```dart
class A {
    // Unless you overrode noSuchMethod, using a
    // non-existent member results in a NoSuchMethodError.
    @override
    void noSuchMethod(Invocation invocation) {
        print('You tried to use a non-existent member: '
        '${invocation.memberName}');
    }
}
```

အောက်ပါတို့မှ တစ်ခုခုနဲ့ကိုက်ညီနေရင် unimplemented method တစ်ခုကို invoke လုပ်လို့ရမှာမဟုတ်ပါဘူး။

- receiver မှာ static type `dynamic` ရှိနေတဲ့အခါ။
- receivar မှာ static type တစ်ခုရှိမယ် ထို type က unimplemented method (abstract ကတော့ OK ပါတယ်) ကို defines လုပ်မယ်။ ပြီးတော့ receiver ရဲ့ dynamic type မှာ class `Object` ထဲက တစ်ခုနဲ့ different ဖြစ်တဲ့ `noSuchMethod()` ရဲ့ implementation တစ်ခုရှိတဲ့အခါ။

အသေးစိတ်ကို [noSuchMethod forwarding specification](https://github.com/dart-lang/sdk/blob/master/docs/language/informal/nosuchmethod-forwarding.md) မှာ အလွတ်သဘောအနေနဲ့ကြည့်နိုင်ပါတယ်။

### Extension methods

Extension methods တွေက ရှိပြီးသား libraries တွေထဲကို functionality တွေပေါင်းထည့်ဖို့ နည်းလမ်းဖြစ်ပါတယ်။ သင်မသိလိုက်ပဲနဲ့တောင် extension method ကိုသုံးနိုင်သည်။ ဥပမာ IDE တစ်ခုမှာရှိတဲ့ code completion ကိုသုံးတဲ့အခါ regular methods များနဲ့အတူ extension methods တွေကို suggests ပြုလုပ်သွားပါတယ်။

ဒါကတော့ extension method တစ်ခုကို အသုံးပြုတဲ့ example ဖြစ်ပါတယ်။ `String` မှာဆိုရင် `parseInt()` က `string_apis.dart` ထဲမှာရှိတဲ့ extension method တစ်ခုဖြစ်ပါတယ်။

```dart
import 'string_apis.dart';
...
print('42'.padLeft(5)); // Use a String method.
print('42'.parseInt()); // Use an extension method.
```

extension methods တွေကို အသုံးပြုပုံနဲ့ implementing လုပ်ပုံကို [ extension methods page](https://dart.dev/guides/language/extension-methods) မှာကြည့်နိုင်ပါတယ်။

### Enumerated types

Enumerated types တွေကို _enumerations_ or _enums_ လို့မကြာခန ခေါ်ကြပါတယ်။ ၎င်းတို့ဟာ special kind of class တွေဖြစ်ပြီး constant values တွေရဲ့ fixed number တစ်ခုကို represent လုပ်ဖို့သုံးပါတယ်။

#### Using enums

enumerated type တစ်ခုကို declare လုပ်ဖို့ `enum` keyword ကိုသုံးရပါတယ်

```dart
enum Color {red, green, blue};
```

enumerated type တစ်ခုကို declaring လုပ်စဉ်မှာ [trailing commas](https://dart.dev/guides/language/language-tour#trailing-comma) ကိုသုံးနိုင်ပါတယ်။

enum တစ်ခုအတွင်မှာရှိတဲ့ value တိုင်းမှာ `index` getter တစ်ခုစီရှိပါတယ်။ enum declaration ထဲမှာရှိတဲ့ value ရဲ့ zero-based position ကို returns ပြန်ပါတယ်။ ဥပမာ first value မှာ index 0 ရှိပြီး second value မှာ index 1 ရှိပါတယ်။

```dart
assert(Color.red.index == 0);
assert(Color.green.index == 1);
assert(Color.blue.index == 2);
```

enum ထဲမှာရှိတဲ့ values တွေရဲ့ list ကိုလိုချင်ရင် enum ရဲ့ `values` constant ကိုသုံးရပါတယ်။

```dart
List<Color> colors = Color.values;
assert(colors[2] == Color.blue);
```

enums တွေကို [switch statements](https://dart.dev/guides/language/language-tour#switch-and-case) တွေမှာသုံးနိုင်ပါတယ်။ enum ရဲ့ values တွေအားလုံးကို handle မလုပ်ရင် warning တစ်ခုရလိမ့်မှာဖြစ်ပါတယ်။

```dart
var aColor = Color.blue;

switch (aColor) {
    case Color.red:
        print('Red as roses!');
        break;
    case Color.green:
        print('Green as grass!');
        break;
    default: // Without this, you see a WARNING.
        print(aColor); // 'Color.blue'
}
```

Enumerated types တွေမှာ အောက်ပါ limits တွေရှိပါတယ်။

- enum တစ်ခုကို subclass, mix in, or implement လုပ်လို့မရပါ။
- enum တစ်ခုကို explicitly instantiate လုပ်လို့မရပါ။
  အသေးစိတ်ကို [Dart language specification](https://dart.dev/guides/language/spec) မှာကြည့်နိုင်ပါတယ်။

### Adding features to a class: mixins

multiple class hierarchies ထဲက class တစ်ခုရဲ့ code ကို reusing လုပ်တဲ့ way တစ်ခုကတော့ Mixins တွေကိုသုံးခြင်းဖြစ်ပါတယ်။

```dart
class Musician extends Performer with Musical {
    // ...
}

class Maestro extands Person
        with Musical, Aggressive, Demented {
    Maestro(String maestroName) {
        name = maestroName;
        canConduct = true;
    }
}
```

mixin တစ်ခုကို _implement_ လုပ်ဖို့ Object ကို extends လုပ်တဲ့ class တစ်ခုကိုဖန်တီးပါ၊ ပြီးတော့ constructors တစ်ခုမှ declares မလုပ်ပါနဲ့။ mixin တစ်ခုကို regular class တစ်ခုလို အသုံးပြုနိုင်ဖို့ `class` အစား `mixin` keyword ကိုသုံးပေးရပါတယ်။ ဥပမာ -

```dart
mixin Musical {
    bool canPlayPiano = false;
    bool canCompose = false;
    bool canConduct = false;

    void entertainMe() {
        if (canPlayPiano) {
            print('Playing piano');
        } else if (canConduct) {
            print('Waving hands');
        } else {
            print('Humming to self');
        }
    }
}
```

တစ်ခါတရံမှာ mixin တစ်ခုသုံးနိုင်တဲ့ types တွေကို လိုအပ်လျှင် restrict လုပ်ပစ်နိုင်ပါတယ်။ ဥပမာ၊ mixin အဖြစ် သတ်မှတ်ထားခြင်းမရှိတဲ့ method တစ်ခုကို invoke လုပ်မိခြင်း အပေါ်မူတည်ပါတယ်။ အောက်ပါ example မှာတော့ mixin တစ်ခုရဲ့ use ကို `on` keyword သုံးပြီးတော့ လိုအပ်တဲ့ superclass တွေကို specify လုပ်ခြင်းဖြင့် restrict လုပ်နိုင်ကြောင်းပြထားတာဖြစ်ပါတယ်။

```dart
class Musician {
    // ...
}
mixin MusicalPerformer on Musician {
    // ...
}
class SingerDancer extends Musician with MusicalPerformer {
    // ...
}
```

ရှေ့က code မှာဆိုရင် `Musician` class ကို extend or implement လုပ်ထားတဲ့ classes တွေက mixin `MusicalPerformer` ကိုသုံးနိုင်သွားပါတယ်။ ဘာဖြစ်လို့လဲဆိုတော့ `SingerDancer` က `Musician` extends လုပ်ထားပြီးတော့၊ `SingerDancer` ကို `MusicalPerformer` ထဲမှာ mix လုပ်လို့ရသွားလို့ဖြစ်ပါတယ်။

### Class variables and methods

class-wide variables နဲ့ methods တွေကို implements လုပ်ဖို့ `static` keyword ကိုသုံးရပါတယ်။

```dart
class Queue {
    static const initialCapacity = 16;
    // ...
}

void main() {
    assert(Queue.initialCapacity == 16);
}
```

Static variables တွေကို မသုံမခြင်း initialized မလုပ်ပါဘူး။

> **Note:** ဒီ page က constant names တွေအတွက် lowerCamelCase ဆိုတဲ့ [style guide recommendation](https://dart.dev/guides/language/effective-dart/style#identifiers) ကိုလိုက်နာထားပါတယ်။

### Static methods

Static methods (class methods) တွေက instance တစ်ခုပေါ်မှာ operate မလုပ်ပါဘူး။ ထို့ကြောင့် `this` ကိုသုံးလို့မရပါဘူး။ static variables တွေကိုတော့ access လုပ်ပါတယ်။ အောက်ပါ example မှာတော့ class တစ်ခုပေါ်က static methods တွေကို တိုက်ရိုက် invoke လုပ်တာကို ဖော်ပြထားတာဖြစ်ပါတယ်။

```dart
import 'dart:math';

class Point {
    double x, y;
    Point(this.x, this.y);

    static double distanceBetween(Point a, Point b){
        var dx = a.x - b.x;
        var dy = a.y - b.y;
        return sqrt(dx * dx + dy * dy);
    }

    void main() {
        var a = Point(2, 2);
        var b = Point(4, 4);
        var distance = Point.distanceBetween(a, b);
        assert(2.8 < distance && distance < 2.9);
        print(distance);
    }
}
```

> **Note:** static methods တွေအစား top-level functions တွေအသုံးပြုတာမှာ common or widely အတွက် utilities နဲ့ functionality တွေသုံးပါတယ်။

static methods တွေကို compile-time constants တွေကဲ့သို့သုံးနိုင်ပါတယ်။ ဥပမာ static method တစ်ခုကို constant constructor တစ်ခုသို့ parameter တစ်ခုအနေနဲ့ pass လုပ်နိုင်ပါတယ်။

## Generics

basic array type [List](https://api.dart.dev/stable/dart-core/List-class.html) ကို API documentation ထဲမှာ လေ့လာပြီးပြီဆိုရင် သူ့ရဲ့ type က အမှန်တကယ်ဆိုရင် `List<E>` ဖြစ်နေတာ တွေမြင်ရပါမယ်။ <...> notation marks List က _generic_ (or _parameterized_) type -- a type that has formal type parameters တစ်ခုကဲ့သို့ဆောင်ရွက်ပါတယ်။ [convention](https://dart.dev/guides/language/effective-dart/design#do-follow-existing-mnemonic-conventions-when-naming-type-parameters) အရ၊ type variables အများစုမှာ E, T, S, K, နဲ့ V တို့လို single-letter names တွေရှိကြပါတယ်။

### Why use generics?

type safety အတွက် generics တွေမကြာခန လိုတတ်ပါတယ်၊ သင့် code မှာထည့်သွင်းအသုံးပြုခြင်းအားဖြင့် ရနိုင်တဲ့ အကျိုးအမြတ်တွေရှိပါသေးတယ် -

- generic types ကို မှန်ကန်စွာသတ်မှတ်ခြင်းသည် ပိုမိုကောင်းမွန်သော code ကို ရရှိစေသည်။
- code duplication ကိုလျော့ချဖို့ generics ကိုသုံးနိုင်ပါတယ်။

list တစ်ခုမှာ Strings များသာပါဝင်ရမယ်လို့ intend လုပ်ထားခဲ့ရင် ၎င်းကို `List<String>` (“list of string” လို့ဖတ်ပါ) တစ်ခုအနေနဲ့ declare လုပ်နိုင်ပါတယ်။ ဒီနည်းလမ်းနဲ့ သင့်ရဲ့ fellow programmers တွေနဲ့ tools တွေက list မှာ non-string တစ်ခုကို assigning လုပ်ထားတာက mistake တစ်ခု ဖြစ်ကြောင်း detect လုပ်နိုင်ပါတယ်။ ဒါကတော့ example ဖြစ်ပါတယ် -

<p style="color:red; font-size:0.9em; margin-bottom: -23px; margin-left: 10px;">❌&nbsp;&nbsp;&nbsp;static analysis: error/warning</p>

```dart

var names = <String>[];
names.addAll(['Seth', 'Kathy', 'Lars']);
names.add(42); // Error
```

generics တွေကို အသုံးပြုရတဲ့နောက်ထပ်အကြောင်းရင်းကတော့ code duplication လျော့ချဖို့ဖြစ်ပါတယ်။

static analysis ရဲ့ advantage ယူနေစဉ်မှာ Generics တွေက single interface တစ်ခုကို share လုပ်ခြင်းနဲ့ များပြားလှတဲ့ types တွေအကြားမှာ implementation လုပ်ခြင်းကို ခွင့်ပြုထားပါတယ်။ ဥပမာ Object တစ်ခုကို caching လုပ်ဖို့ interface တစ်ခုကို create လုပ်ပါဆိုလျှင် -

```dart
abstract class ObjectCache {
    Object getByKey(String key);
    void setByKey(String key, Object value);
}
```

ဒီ interface ရဲ့ string-specific version တစ်ခုကို အလိုရှိတယ်ဆိုရင်၊ နောက်ထပ် interface တစ်ခုကို ထပ်ပြီးဖန်တီးရပါမယ်။

```dart
abstract class StringCache{
    String getByKey(String key);
    void setByKey(String key, Object value);
}
```

နောက်ပိုင်းမှာ ထို interface ရဲ့ number-specific version တစ်ခုထပ်လိုပြီ ဆိုရင်...

Generic types တွေက ထို interfaces တွေအကုန်လုံးကိုလိုက်ပြီး ဖန်တီးရမည့် ပြဿနာတွေကို မဖြစ်အောင် ဟန်တားနိုင်ပါတယ်။ ထို့သို့ interfaces တွေအများကြီးဖန်တီးနေရမည်အစား type parameter ကိုအသုံးပြုတဲ့ interface တစ်ခုကိုဖန်တီးပေးလိုက်ရင်ရပါပြီး။

```dart
abstract class Cache<T> {
    T getByKey(String key);
    void setByKey(String key, T value);
}
```

ဒီ code မှာ T ဆိုတာက stand-in type ဖြစ်ပါတယ်၊ ၎င်းသည် developer ကိုနောက်ပိုင်းမှ define လုပ်မည့် type တစ်ခုဟု ယူဆနိုင်သော placeholder တစ်ခုဖြစ်သည်။

### Using collection literals

List, set, နဲ့ map literals တွေက parameterized ဖြစ်နိုင်ပါတယ်။ Parameterized literals အရင်ကမြင်ဘူးခဲ့တဲ့ literals တွေနဲ့ တူပါတယ်။ ဘာကွာသွားလဲဆိုတော့ opening bracket ရဲ့ရှေ့မှာ `<type>` (for lists and sets) or `<keyType, valueType>` (for maps) တွေထည့်ပေးရတာ ကွာသွားပါတယ်။ ဒါကတော့ typed literals တွေကိုအသုံးပြုတဲ့ example တစ်ခုဖြစ်ပါတယ်။

```dart
var names = <String>['Seth', 'Kathy', 'Lars'];
var uniqueNames = <String>{'Seth', 'Kathy', 'Lars'};
var pages = <String, String>{
    'index.html': 'Homepage',
    'robots.txt': 'Hints for web robots',
    'human.txt': 'We are people, not machines'
}
```

### Using parameterized types with constructors

constructor တစ်ခုကိုသုံးတဲ့အချိန်မှာ တစ်ခုသို့မဟုတ်တစ်ခုထက်ပိုသော types တွေကိုဖန်တီးဖို့ အတွက် types တွေကို angle brackets (`<...>`) ထဲထည့်ပြီး class name ရဲ့ ရှေ့မှာထားပေးရမှာဖြစ်ပါတယ်။ ဥပမာ

```dart
var nameSet = Set<String>.from(names);
```

အောက်ပါ code ကတော့ keys တွေမှာ integer နဲ့ values တွေမှာ type View ရှိတဲ့ map တစ်ခုကိုဖန်တီးတာဖြစ်ပါတယ်။

```dart
var views = Map<int, View>();
```

### Generic collections and the types they contain

Dart generic types တွေက _reified_၊ အဓိပ္ပာယ်က သူတို့ရဲ့ type information ကို runtime တစ်လျှောက် carry လုပ်တာဖြစ်ပါတယ်။ ဥပမာ - collection တစ်ခုရဲ့ type ကို test လုပ်နိုင်ပါတယ်။

```dart
var names = <String>[];
names.addAll(['Seth', 'Kathy', 'Lars']);
print(name is List<String>); // true
```

> **Note:** Java နဲ့မတူတာက၊ Java မှာရှိတဲ့ generics က _erasure_ ကိုသုံးပါတယ်၊ ဆိုလိုတာက ထို generic type parameters တွေ runtime မှာ removed လုပ်ပါတယ်။ Java မှာ object တစ်ခုက List လား ဆိုတာ Test လုပ်နိုင်ပါတယ်။ သိုသော် အဲတာက `List<String>` ဖြစ်လားဆိုတာကိုတော့ test လုပ်လို့မရပါဘူး။

### Restricting the parameterized type

generic type တစ်ခုကို implementing လုပ်တဲ့အခါမှာ သူရဲ့ parameters တွေရဲ့ types ကို limit လုပ်လိုလျှင် `extends` ကိုသုံးရမှာဖြစ်ပါတယ်.

```dart
class Foo<T extends SomeBaseClass> {
    // Implementations goes here ...
    String toString() => "Instance of 'Foo<$T>'";
}

class Extender extends SomeBaseClass {...}
```

SomeBaseClass (သို့) ၎င်း၏ subclasses တစ်ခုခုကို generic argument အဖြစ်အသုံးပြုရန် OK သည်။

```dart
var someBaseClassFoo = Foo<SomeBaseClass>();
var extenderFoo = Foo<Extender>();
```

generic argument ကို မသတ်မှတ်ရန်လည်း OK သည်။

```dart
var foo = Foo();
print(foo); // Instance of 'Foo<SomeBaseClass>'
```

non-SomeBaseClass type ကို specifying လုပ်ခြင်းသည် error တစ်ခုဖြစ်ပေါ်စေသည်။

<p style="color:red; font-size:0.9em; margin-bottom: -23px; margin-left: 10px;">❌&nbsp;&nbsp;&nbsp;static analysis: error/warning</p>

```dart

var foo = Foo<Object>();
```

### Using generic methods

အစပိုင်း၌ Dart ၏ generic support သည် classes သာဖြစ်သည်။ generic methods လို့ခေါ်တဲ့ syntax အသစ်တစ်ခုသည် method နှင့် functions အပေါ်တွင် type argument များကိုခွင့်ပြုသည်။

```dart
T first<T>(List<T> ts) {
    // Do some initial work or error checking, then...
    T tmp = ts[0];
    // Do some additonal checking or processing...
    return tmp;
}
```

ဤနေရာတွင် `first(<T>)` ရှိ generic type parameter သည် သင့်အားနေရာများစွာတွင် type argument T ကို သုံးရန်ခွင့်ပြုသည်။

- function ရဲ့ return type (`T`) မှာ
- argument (`List<T>`) ရဲ့ type မှာ
- local variable (`T tmp`) ရဲ့ type မှာ

## Libraries and visibility

`import` နှင့်` library` directives တွေက modular နှင့် shareable code base ကိုဖန်တီးရန်ကူညီနိုင်သည်။ Libraries များသည် APIs များကို provide ပေးရုံသာမက privacy ၏ unit တစ်ခုဖြစ်သည်။ underscore (`_`) တစ်ခု နှင့်စတင်သော identifiers များသည် library အတွင်းမှာသာ visible ဖြစ်နိုင်သည်။ '_Dart app တိုင်းသည် library တစ်ခု ဖြစ်သည်။_ library direcivetive ကိုမသုံးရင်တောင် ဖြစ်နိုင်သည်။

libraries များကို package များဖြင့်ဖြန့်ဝေနိုင်သည်။

> Dart မှာ `public` သို့မဟုတ် `private` တို့ကဲ့သို့သော access-modifier-keywords အစား underscores များကို ဘာ့ကြောင့် အသုံးပြုသည်ကို သင်သိလိုလျှင်၊ [SDK issue 33383](https://github.com/dart-lang/sdk/issues/33383) ကိုကြည့်ပါ။

### Using libraries

library တစ်ခုမှ namespace ကိုအခြား library ၏ `scope` တွင် မည်သို့အသုံးပြုသည်ကို သတ်မှတ်ရန် `import` ကိုသုံးပါ။ ဥပမာ, Dart web app များသည်ယေဘုယျအားဖြင့် dart:html library ကိုသုံးသည်။ ၎င်းကို အောက်ပါအတိုင်း import လုပ်နိုင်ပါတယ်။

```dart
import 'dart:html';
```

import လုပ်ဖို့ လိုအပ်တဲ့ argument က libaray ကိုသတ်မှတ်ပေးတဲ့ URI တစ်ခုဖြစ်ပါတယ်။ built-in libraries အတွက် URL မှာ special `dart:` scheme ကို ထည့်ပေးရပါတယ်။ အခြားသော libraries တွေအတွက် file system path တစ်ခု သို့မဟုတ် `package:` scheme ကိုထည့်ပေးရပါတယ်။
package: scheme သည် pub tool လို package manager မှ provided လုပ်သော libraries များကို specifies ပေးပါတယ်။ ဥပမာ

```dart
import 'package:test/test.dart';
```

> **Note:** URI ရဲ့ အရှည်က Uniform Resource Identifier။ URLs(Uniform resource locators) တွေက URI ရဲ့ common kind တစ်ခုဖြစ်ပါတယ်။

### Specifying a library prefix

identifiers တွေ conflicting ဖြစ်နေတဲ့ libraries နှစ်ခုကို import လုပ်တဲ့အခါမှာ librarie တစ်ခုတည်းကိုဖြစ်စေ နှစ်ခုစလုံးကိုဖြစ်စေ prefix တစ်ခုကို specify လုပ်ပေးနိုင်ပါတယ်၊ ဥပမာ- library1 နဲ့ library2 နှစ်ခုလုံမှာ Element ဆိုတဲ့ class ပါနေတယ်ဆိုရင် သင့် code ကို အောက်ပါအတိုင်ရေးနိုင်ပါတယ်။

```dart
import 'package:lib1/lib1.dart';
import 'package:lib2/lib2.dart' as lib2;

// Uses Element from lib1.
Element element1 = Element();

// Uses Element from lib2.
lib2.Element element2 = lib2.Element();
```

### Importing only part of a library

library တစ်ခုရဲ့ အစိတ်အပိုင်းတစ်ခုကိုသာသုံးချင်တယ်ဆိုရင် library ကို selectively import လုပ်နိုင်ပါတယ်။ ဥပမာ -

```dart
// Import only foo.
import 'package:lib1/lib1.dart' show foo;

// Import all names EXCEPT foo.
import 'package:lib2/lib2.dart' hide foo;
```

### Lazily loading a library

_Deferred loading_ (_lazy loading_ လို့လဲခေါ်ပါသေးတယ်)၊ သူက web app တစ်ခုက library ကိုလိုအပ်ချက်ပေါ်မှုတည်ပြီး load လုပ်ဖို့ခွင့်ပြုထားပါတယ်။ library ကို တကယ်လိုအပ်ပြီ၊ လိုအပ်တဲ့အချိန်မှသာ ထပြီး import လုပ်ပါတယ်။

deferred loading ကိုဘယ်အချိန်မှာအသုံးပြုရမလဲဆိုတဲ့အချက်တွေပါ

- web app တစ်ခုရဲ့ initial startup time ကိုလျော့ချလိုတဲ့အခါမျိုး
- A/B testing ပြုလုပ်ရန်၊ algorithm တစ်ခုရဲ့ alternative implementations တွေကိုစမ်းကြည့်လိုတဲ့အခါမျိုး
- optional screens နဲ့ dialogs တွေကဲ့သို့သော ရံဖန်ရံခါမျှသာ သုံးတဲ့ လုပ်ဆောင်ချက်တွေကို load လုပ်တဲ့အခါမျိုးမှာ

> **dart2js မှာသာ deferred loading ကို supports လုပ်ပါတယ်** Flutter, Dart VM, နဲ့ dartdevc တို့မှာ deferred loading ကို support မလုပ်ပါ။ အသေးစိတ်အချက်အလက်ကို [issue #33118](https://github.com/dart-lang/sdk/issues/33118) နဲ့ [issue #27776](https://github.com/dart-lang/sdk/issues/27776) မှာလေ့လာပါ။

library တစ်ခုကို lazily load လုပ်ဖို့ အရင်ဆုံး import မှာ `deferred as` ကိုသုံးပေးရပါတယ်

```dart
import 'package:greetings/hello.dart' deferred as hello;
```

library လိုအပ်တဲ့အခါမှာ library ရဲ့ identifier ကိုသုံးပြီး `loadLibrary()` ကို invoke လုပ်ပါ။

```dart
Future<void> greet() async {
    await hello.loadLibrary();
    hello.printGreeting();
}
```

အထက်ပါ code မှာ `await` keyword က library ကို loaded ဖြစ်ပြီးသည့်တိုင်အောင် execution ကို pauses လုပ်ဖို့ဖြစ်ပါတယ်။ `async` နဲ့ `await` အကြောင်းကို [asynchrony support](https://dart.dev/guides/language/language-tour#asynchrony-support) မှာကြည့်ပါ။

`loadLibrary()` ကိုအကြိမ်ကြိမ် invoke လုပ်နိုင်ပါတယ်၊ library မှာ ပြဿနာမဖြစ်ပါ၊ library က တစ်ကြိမ်ထဲသာ loaded လုပ်မှာဖြစ်ပါတယ်။

deferred loading ကို သုံးတဲ့နေရာမှာ အောက်ပါတို့ကိုနားလည်ထားဖို့လိုပါတယ်။

- deferred library ရဲ့ constants တွေက importing file ထဲမှာရှိတဲ့ constants တွေမဟုတ်ပါဘူး။
- importing file ထဲမှာရှိတဲ့ deferred library တစ်ခုမှ types တွေကို သုံးလို့မရနိုင်ပါဘူး။ ၎င်းအစား deferred library နဲ့ importing file တို့မှ imported လုပ်တဲ့ library တစ်ခုသို့ interface types တွေကို moving လုပ်ခြင်းအားထည့်သွင်းစဉ်းစားပါ။
- Dart သည် `deferred as namespace` ကို သုံး၍ သင် defined ထားသော namespace ထဲသို့ `loadLibrary()` ကို လုံးလုံးလျားလျားထည့်သွင်းသည်။ `loadLibrary()` function သည် `Future` တစ်ခုကိုပြန်ပေးသည်။

### Implementing libraries

library package တစ်ခုကိုဘယ်လို့ implement လုပ်လဲ ဆိုတာကို [Create Library Packages](https://dart.dev/guides/libraries/create-library-packages) မှာလေ့လာပါ။ ၎င်းမှာပါဝင်တာတွေကတော့

- library source code တွေကိုဘယ်လို organize လုပ်လဲ
- `export` directive ကိုဘယ်လိုသုံးလဲ
- ဘယ်အချိန်မှာ `part` directive ကိုသုံးရလဲ
- ဘယ်အချိန်မှာ `library` directive ကိုသုံးရလဲ
- multiple platforms တွေကို supports လုပ်တဲ့ library တစ်ခုကို implement လုပ်ဖို့ conditional imports နဲ့ exports ကိုဘယ်လိုသုံးရလဲ။

## Asynchrony support

Dart libraries တွေမှာ `Future` or `Stream` objects တွေကို return ပြန်ပေးတဲ့ functions တွေနဲ့ပြည့်နက်နေပါတယ်။ ထို functions တွေက _asynchronous_ တွေဖြစ်ပါတယ်။ သူတို့တွေက (I/O ကဲ့သို့) possibly time-consuming operation တစ်ခုကို setting up လုပ်ပြီးတဲ့နောက်မှ return ပြန်ပေးပါတယ်။ ထို operation ကိုပြီးအောင် စောင့်မနေတော့ပါဘူး။

`async` နှင့် `await` keywords တို့သည် asynchronous programming ကိုပံ့ပိုးပေးသဖြင့် synchronous code နှင့်ဆင်တူသော asynchronous code ကိုရေးသားခွင့်ပြုသည်။

### Handling Futures

ပြည့်စုံတဲ့ Future တစ်ခုရဲ့ result ကိုလိုချင်တဲ့အခါမှာ ရွေးစရာ နှစ်ခုရှိပါတယ်

- `async` နဲ့ `await` ကိုသုံးတဲ့နည်း
- Future API ကိုသုံးတဲ့နည်း၊ ၎င်းကို [labrary tuor](https://dart.dev/guides/libraries/library-tour#future) မှာဖော်ပြထားပါတယ်။

`async` နှင့် `await` ကိုသုံးသော code သည် asynchronous ဖြစ်သော်လည်း synchronous code နှင့်တူသည်။ ဥပမာ၊ ဒါက asynchronous function တစ်ခုရဲ့ result ကိုစောင့်ဆိုင်းရန် `await` ကိုသုံးသော code အချို့ဖြစ်သည်-

```dart
await lookUpVersion();
```

`await` ကိုသုံးဖို့ code က `async` function တစ်ခုထဲမှာရှိရမှာဖြစ်ပါတယ်။ `async` လို့ သတ်မှတ်ပေးထားတဲ့ function ဖြစ်ပါတယ် -

```dart
Future<void> checkVersion() async {
    var version = await lookUpVersion();
    // Do something with version
}
```

> **Note:** `async` function တစ်ခုသည် time-consuming operations များကို လုပ်ဆောင်နိုင်သော်လည်း ထို operations များကိုမစောင့်ပါ။ ၎င်းအစား `async` function က ၎င်းရဲ့ပထမဆုံး `await` expression နှင့် encounters မလုပ်မခြင်းသာ executes လုပ်သည် ([details](https://github.com/dart-lang/sdk/blob/master/docs/newsletter/20170915.md#synchronous-async-start))။ ထို့နောက်၎င်းသည် `Future` object တစ်ခုကို return ပြန်ပေးသည်။ `await` expression ပြီးစီးမှသာ execution ပြန်လည်စတင်ပါ။

`await` ကိုသုံးတဲ့ code ထဲမှာ errors တွေကို handle လုပ်ဖို့နဲ့ cleanup ဖြစ်စေဖို့ `try`,`catch`, နဲဲ့ `finally` တို့ကိုသုံးရပါတယ်။

```dart
try {
    version = await lookUpVersion();
} catch (e) {
    // React to inability to look up the version
}
```

`async` function ထဲမှာ `await` ကို အကြိမ်ကြိမ်သုံးနိုင်ပါတယ်။ ဥပမာ အောက်ပါ code မှာ functions တွေရဲ့ results တွေအတွက် (၃)ကြိမ်တောင် waits လုပ်ပါတယ်။

```dart
var entrypoint = await findEntryPoint();
var exitCode = await runExecutable(entrypoint, args);
await flushThenExit(exitCode);
```

`await` _`expression`_ မှာ၊ _`expression`_ ရဲ့ value က အမြဲတမ်း Future တစ်ခုဖြစ်ပါတယ်။ မဟုတ်ရင်တော့ value က Future တစ်ခုထဲမှာ အလိုအလျှောက် wrapped လုပ်သွားပါတယ်။ ထို `Future` object က Object တစ်ခုကို return ပြန်ပေးရန် promise တစ်ခုကို indicate လုပ်ပါတယ်။ `await` _`expression`_ ရဲ့ value က return object ဖြစ်တယ်။ `await` _`expression`_ က ထို object ကိုမရမချင်း execution ကို pause လုပ်ထားပါတယ်။

**`await` ကိုသုံနေစဉ်မှာ compile-time error တစ်ခုဖြစ်ခဲ့ပါက၊ `await` က `async` function ထဲမှာတကယ်ကောရှိလားဆိုတာ စမ်းစစ်သင့်ပါတယ်။** ဥပမာ `main()` function ထဲမှာ `await` ကိုသုံးဖို့ `main()` ရဲ့ body ကို `async` ဖြစ်အောင်လုပ်ရမှာဖြစ်ပါတယ်။

```dart
Future<void> main() async {
    checkVersion();
    print('In main: version is ${await lookUpVersion()}');
}
```

### Declaring async functions

`async` function သည် body အား `async` modifier ဖြင့် marked လုပ်ထားသော function တစ်ခုဖြစ်သည်။ function တစ်ခုကို `async` keyword ထည့်ပြီး ထို function ကို Future တစ်ခု return ပြန်ပေးအောင်လုပ်ရပါမယ်။ ဥပမာ အောက်ပါ synchronous function ကိုကြည့်ပါ ၎င်းက String တစ်ခုကို return ပြန်ပေးပါတယ်။

```dart
String lookUpVersion() => '1.0.0';
```

၎င်းကို `async` function အဖြစ်သို့ ပြောင်းလိုက်လျှင် -- ဥပမာ၊ အကြောင်းမှာ future implementation က time consuming လုပ်ပါတယ်။ -- returned value က Future ဖြစ်ပါတယ်။

```dart
Future<String> lookUpVersion() async => `1.0.0`;
```

function ရဲ့ body က Future API ကို သုံးဖို့မလိုတာကို သတိပြုပါ။ လိုအပ်ရင် Dart က Future object ကို create လုပ်ပါတယ်၊ သင့် function က အသုံးဝင်တဲ့ value တစ်ခုကို return မလုပ်ဖူးဆိုရင် သူ့ရဲ့ return type ကို `Future<void>` type လုပ်ပေးပါတယ်။

futures, `async`, နဲ့ `await` တို့အသုံးပြုပုံကို အပြန်အလှန် မိိတ်ဆက်ထားပုံကို [asynchronous programming codelab](https://dart.dev/codelabs/async-await) မှာကြည့်ပါ။ (Flutter သမားအတွက် အရေးကြီးပါတယ်)။

### Handling Streams

Stream တစ်ခုကနေ values တွေကိုရယူလိုတဲ့အခါမှာ ရွေးစရာနှစ်ခုရှိပါတယ် -

- `async` နဲ့ asynchronous for loop (`await for`) ကိုသုံးတဲ့နည်း
- Stream API ကိုသုံးတဲ့နည်း၊ [library tuor](https://dart.dev/guides/libraries/library-tour#stream) မှာဖော်ပြထားပါတယ်။

> **Note:** `await for` ကိုမသုံးခင်မှာ code ကို clearer ဖြစ်အောင်သေချာလုပ်ပါ ပြီတော့ stream ရဲ့ results အားလုံကို တစ်ကယ်ပဲ စောင့်ချင်တာလား သေချာလုပ်ပါ။ ဥပမာ - UI event listeners တွေလိုမျိုးမှာ `await for` ကို **လုံးဝ** မသုံးသင့်ပါဘူး၊ ဘာဖြစ်လို့လဲဆိုတော့ UI frameworks တွေက events တွေရဲ့ endless streams တွေကို send လုပ်နေသောကြောင့်ဖြစ်ပါတယ်။

asynchronous for loop တစ်ခုကို အောက်ပါနမူနာအတိုင်း ရေးရပါတယ်။

```dart
await for (varOrType identifier in expression) {
    // Executes each time the stream emits a value.
}
```

_expression_ ရဲ့ value က Stream type ဖြစ်ရပါမယ်။ Execution proceeds တွေကအောက်ပါအတိုင်းဖြစ်ပါတယ် -

1. value တစ်ခုကို stream က emits မလုပ်မခြင်းစောင့်ပါတယ်
2. for loop ရဲ့ body ကို execute လုပ်ပါတယ်၊ ပြီးတော့ ထို emitted value ကို variable နဲ့ set လုပ်ပါတယ်။
3. stream က closed မဖြစ်မခြင်း 1 နဲ့ 2 ကိုအကြိမ်ကြိမ် repeat လုပ်ပါတယ်။

stream တစ်ခုကို stop listing လုပ်ဖို့အတွက် `break` သို့မဟုတ် `return` statment ကိုသုံးနိုင်ပါတယ်။ ၎င်က for loop ကိုရပ်လိုက်ပြီးတော့ stream ကနေ unsubscribes လုပ်ပါတယ်။

**asynchronous for loop တစ်ခုကို implementing လုပ်နေစဉ်မှာ compile-time error တစ်ခုဖြစ်ခဲ့ပါက၊ `await for` က `async` function ထဲမှာတကယ်ကောရှိလားဆိုတာ စမ်းစစ်သင့်ပါတယ်။** ဥပမာ main() function ထဲမှာ asynchronous for loop တစ်ခု ကိုသုံးဖို့ main() ရဲ့ body ကို async ဖြစ်အောင်လုပ်ရမှာဖြစ်ပါတယ်။

```dart
Future<void> main() async {
    // ...
    await for (var request in requestServer) {
        handleRepeat(request);
    }
    // ,,,
}
```

asynchronous programming အကြောင်းကို အသေးစိတ်ကို library tour ရဲ့ [dart:async](https://dart.dev/guides/libraries/library-tour#dartasync---asynchronous-programming) section မှာ ကြည့်နိုင်ပါတယ်။

## Generators

sequence of values တစ်ခုကို lazily produce လုပ်ချင်တဲ့အခါမှာ _generator function_ တစ််ခုကိုသုံးဖို့ သတိရပါ။ Dart မှာ generator function နှစ်မျိူးကို built-in အနေနဲ့ support ပေးထားပါတယ်။

- **Synchronous** generator: Returns an [Iterable](https://api.dart.dev/stable/dart-core/Iterable-class.html) object.
- **Asynchronous** generator: Returns a [Stream](https://api.dart.dev/stable/dart-async/Stream-class.html) object.

**synchronous** generator function တစ်ခုကို implement လုပ်ဖို့ function body ကို `sync*` လို့ mark လုပ်ပါ။ values တွေကို deliver လုပ်ဖို့ `yield` statements ကိုသုံးပေးရပါတယ်။

```dart
Iterable<int> naturalsTo(int n) sync* {
    int k = 0;
    while (k < n) yield k++;
}
```

**asynchronous** generator function တစ်ခုကို implement လုပ်ဖို့ function body ကို `async*` လို့ mark လုပ်ပါ။ values တွေကို deliver လုပ်ဖို့ `yield` statements ကိုသုံးပေးရပါတယ်။

```dart
Stream<int> asynchronousNaturalsTo(int n) async* {
    int k = 0;
    while(k < n) yield k++;
}
```

generator က recursive ဖြစ်နေတဲ့အခါမှာ `yield*`သုံးပြီး သူ့ရဲ့ performance ကို improve ဖြစ်အောင် လုပ်လို့ရပါတယ်။

```dart
Iterable<int> naturalsDownFrom(int n) sync* {
    if(n > 0) {
        yield n;
        yield* naturalsDownFrom(n - 1);
    }
}
```

## Callable classes

Dart class ရဲ့ instance တစ်ခုကို function တစ်ခုလို call လုပ်နိုင်ဖို့ `call()` method ကို implement လုပ်ပါ။

အောက်ပါ example မှာ `WannableFunction` class က call() function တစ်ခုကို defines လုပ်ထားပြီးတော့ strings သုံးခုယူကာ တစ်ခုနဲ့တစ်ခုကို space တစ်ခုစီနဲ့ခြားထားပေးပါတယ်။ နောက်ပြီတော့ exclamation တစ်ခုကိုလည်း appeding လုပ်ထားပါသေးတယ်။

```dart
class WannableFunction {
    Stirng call(String a, String b, String c) => '$a $b $c!';
}

var wf = WannableFunction();
var out = wf('Hi', 'there', 'gang');

void main() => print(out);
```

## Isolatea

mobile platforms တွေအပါအဝင် ကွန်ပျူတာအများစုမှာ multi-core CPUs တွေရှိပါတယ်။ ထို cores တွေရဲ့အားလုံးရဲ့ အားသာချက်ကို ယူဖို့အတွက် developers တွေက တပြိုင်တည်း running လုပ်နေတဲ့ shared-memory threads တွေကိုသုံးကြပါတယ်။ သိုသော် shared-state concurrency က error များလေ့ရှိတဲ့အပြင် code တွေကို လည်းရှုတ်ထွေးသွားစေနိုင်ပါတယ်။

ထို threads တွေအစား၊ Dart code အားလုံးက _isolates_ တွေအတွင်းမှာ runs နိုင်ကြပါတယ်။ isolate ရဲ့ state ကိုအခြားမည်သည့် isolate မှ accessible မလုပ်နိုင်ကြောင်းသေချာစေရန်၊ isolate တစ်ခုခြင်းစီမှာ သူတို့ကိုယ်ပိုင် memory heap ရှိကြပါတယ်။

နောက်ထပ်အချက်အလက်များကို အောက်တွင်ကြည့်ပါ။

- [Dart asynchronous programming: Isolates and event loops](https://medium.com/dartlang/dart-asynchronous-programming-isolates-and-event-loops-bffc3e296a6a)

- [dart:isolate API reference,](https://api.dart.dev/stable/dart-isolate) including [Isolate.spawn()](https://api.dart.dev/stable/dart-isolate/Isolate/spawn.html) and [TransferableTypedData](https://api.dart.dev/stable/dart-isolate/TransferableTypedData-class.html)

- [Background parsing](https://flutter.dev/docs/cookbook/networking/background-parsing) cookbook on the Flutter site
- [Isolate sample app](https://github.com/flutter/samples/tree/master/isolate_example)

## Typedefs

type alias တစ်ခု -- _typedef_ လိုခေါ်ဆိုလေ့ရှိကြပါတယ် ဘဖြစ်လို့လဲဆိုတော့ သူကို `typedef` keyword နဲ့ declared လုပ်ရသောကြောင့်ဖြစ်ပါတယ် -- ၎င်းက type တစ်ခုကို refer လုပ်ဖို့ တိကျတဲနည်းလမ်းတစ်ခုဖြစ်ပါတယ်။ ဒါကတော့ `IntList` ဆိုတဲ့ type alias တစ်ခုကို declare လုပြီးနောက် အသုံးပြုပုံကိုဖော်ပြပေးထားတာဖြစ်ပါတယ်။

```dart
typedef IntList = List<int>;
IntList il = [1, 2, 3];
```

type alias တစ်ခုမှာ type parameters တွေထည့်ပေးနိုင်ပါတယ်။

```dart
typedef ListMapper<X> = Map<X, List<X>>;
Map<Stirng, List<String>> m1 = {}; // Verbose.
ListMapper<String> m2 = {}; // Some thing but shorter and clearer.
```

> **Version note:** 2.13 မတိုင်ခင်မှာ typedefs တွေကို function types တွေအတွက် restricted လုပ်ခံထားရပါတယ်။ typedefs အသစ်ကိုသုံနိုင်ဖို့အတွက် language version အနည်းဆုံး 2.13 ရှိရပါမယ်။

functions အတွက် typedefs အစား [inline function types](https://dart.dev/guides/language/effective-dart/design#prefer-inline-function-types-over-typedefs) တွေကိုသုံးဖို့အကြံပြုလိုပါတယ်။ သို့သော်လည်း function typedefs တွေက အသုံးဝင်နေဆဲဖြစ်ပါတယ်။

```dart
typedef Compare<T> = int Function(T a, T b);

int sort(int a, int b) => a - b;

void main() {
    assert(sort is Compare<int>); // True!
}
```

## Metadata

သင့် code တွေအကြောင်းကို အပိုထပ်ဆောင်းအချက်အလက်တွေ ပေးဖို့အတွက် metadata ကိုသုံးရပါတယ်။ metadata annotation တစ်ခုက `@` character နဲ့စရေးပေးရပါတယ်။ သူရဲ့နောက်မှာ (deprecated လို )compile-time constant တစ်ခု သို့ reference ဖြစ်စေ၊ သိုမဟုတ် constant constructor တစ်ခုသို့ call တစ်ခု ဖြစ်စေ followed လုပ်ပါတယ်။

Dart core တွေအားလုံးမှာ ရနိုင်တဲ့ annotations သုံးခုရှိပါတယ်၊ `@Deprecated`, `@deprecated`, နဲ့ `@override` တို့ဖြစ်ပါတယ်။ `@override` အသုံးပြုပုံကို [Extending a class](https://dart.dev/guides/language/language-tour#extending-a-class) မှာကြည့်နိုင်ပါတယ်။ ဒါကတော့ `@Deprecated` annotation ကိုအသုံးပြုတဲ့ example တစ်ခုဖြစ်ပါတယ်။

```dart
class Television {
    /// Use [turnOn] to turn the power on instead.
    @Dwprecated('Use turnOn instead')
    void activate() {
        turnOn();
    }

    /// Turns the TV's power on.
    void turnOn() {...}
}
```

ကိုပိုင် metadata annotations တွေကိုလည်းသတ်မှတ်ပေးနိုင်ပါတယ်။ ဒါကတော့ `@Todo` annotation ကို definding လုပ်တာဖြစ်ပြီး ၎င်းမှာ arguements နှစ်ခုပါပါတယ်။

```dart
library todo;

class Todo {
    final String who;
    final Stirng what;

    const Todo(this.who, this.what);
}
```

ဒါကတော့ `@Todo` annotation ကိုအသုံးပြုပုံဖြစ်ပါတယ်။

```dart
import 'todo.dart';

@Todo('seth', 'make this do something')
void doSomething() {
    print('do something');
}
```

Metadata က class, typedef, type parameter, constructor, factory, function, field, parameter, or variable declaration နှင့် import or export directive တို့ရဲ့ရှေ့မှာ ပေါ်တတ်ပါတယ်။ reflection ကိုသုံပြီး runtime မှာ metadata ကို retrieve လုပ်နိုင်ပါတယ်။

## Comments

Dart မှာ single-line comments, multi-line comments, နဲ့ documentation comments တို့ကို support လုပ်ပါတယ်။

### Single-line comments

single-line comment ကို `//` နဲ့စတင်ရပါတယ်။ `//` နဲ့ line ရဲ့အဆုံကြားမှာရှိတဲ့ မည်သည့်အရာကိုမဆို Dart compiler က ignore လုပ်ပါတယ်။

```dart
void main() {
    // TODO: refactor into an AbstractLlamaGreetingFactory?
    print('Welcome to my Llama farm!');
}
```

### Multi-line comments

multi-line comment တစ်ခုက `/*` တစ်ခုနဲ့ စပြီးတော့ `*/` နဲ့အဆုံးသပ်ပါတယ်။ `/*` နဲ့ `*/` ကြားမှာရှိတဲ့ အရာအားလုံးကို Dart comiler က ignored လုပ်ပေးပါတယ် (comment က documentation comment မဟုတ်လျှင်၊ နောက် section ကိုကြည့်ပါ)၊ Muti-line comments တွေက nest လုပ်နိုင်ပါတယ်။

```dart
void main(){
    /*
    * This is a lot of work. Consider raising chickens.

    Llama larry = Llama()'
    larry.feed();
    larry.exercise();
    larry.cleam();
    */
}
```

### Documentation comments

Documentation comments တွေက multi-line သို့မဟုတ် single-line comments တွေဖြစ်ကြပါတယ် သူတို့ကို `///` `/**` နဲ့ စပြီးရေးရပါတယ်။ consecutive lines မှာ `///` ကိုသုံခြင်းက multi-line doc comment တစ်ခုရဲ့ အကျိုးသက်ရောက်ပုံနဲ့အတူတူပါပဲ။

documentation comment တစ်ခုရဲ့အတွင်းမှာ analyzer က brackets အတွင်းမရှိသည့် text အားလုံကို ignored လုပ်ပါတယ်။ brackets ကိုသုံးပြီး classes, methods, fields, top-level variables, functions, နဲ့ parameters တွေကို refer လုပ်နိုင်ပါတယ်။ brackets တွေအတွင်းမှာရှိတဲ့ names တွေက documented program element ရဲ့ lexical scope ထဲမှာ resolved လုပ်ပါတယ်။

ဒါကတော့ documentation comments တစ်ခုရဲ့ example ဖြစ်ပြီးတော့ classes တွေနှင့် arguments တွေကို references လုပ်ထားပါတယ်။

```dart
/// A domesticated South American camelid (Lama glama).
///
/// Andean cultures have used llamas as meat and pack
/// animals since pre-Hispanic times.
///
/// Just like any other animal, llamas need to eat,
/// so don't forget to [feed] them some [Food].
class Llama {
    String? name;

    /// Feeds your llama [food].
    ///
    /// The typical llama eats one bale of hay per week.
    void feed(Food food) {
        // ...
    }

    /// Exercises your llama with an [activity] for
    /// [timeLimit] minutes.
    void exercise(Activity activity, int timeLimit) {
        // ...
    }
}
```

class ရဲ့ generated documentation ထဲမှာ၊ `[feed]` က link တစ်ခုဖြစ်သွားပြီးတော့ `feed` method အတွက် docs ချိတ်ပေးပါတယ်။ `[Food]` က `Food` class အတွက် docs ကို link လုပ်ပေးတဲ့ link တစ်ခုဖြစ်သွားပါတယ်။

Dart code ကို parse လုပ်ဖို့နဲ့ HTML documentaton ကို generate လုပ်ပေးဖို့အတွက် Dart ရဲ့ [documentation generation tool, dartdoc](https://dart.dev/tools/dartdoc) ကိုသုံးပါ။ generated documentation ဥပမာ ကို [ Dart API documentation](https://api.dart.dev/stable) မှာကြည့်ပါ။ comments တွေကိုဘယ်လိုတည်ဆောင်ရမယ်ဆိုတဲ့ အကြံပြုချက်တွေကို [Guidelines for Dart Doc Comments](https://dart.dev/guides/language/effective-dart/documentation) မှာကြည့်ပါ၊

## Summary

ဤစာမျက်နှာတွင် Dart language တွင်အသုံးများသော features များကို အကျဉ်းချုပ်ဖော်ပြထားသည်။ နောက်ထပ်လုပ်ဆောင်ချက်များကို အကောင်အထည်ဖော်နေပါသည်၊ သို့သော် ၎င်းတို့သည် ရှိပြီးသားကုဒ်ကို မချိုးဖောက်ဟု ကျွန်ုပ်တို့မျှော်လင့်သည်။

ပိုမိုသောအချက်အလက်များအတွက် [Dart language specification](https://dart.dev/guides/language/spec) နဲ့ [Effective Dart](https://dart.dev/guides/language/effective-dart)တွင်ကြည့်ပါ။

To learn more about Dart’s core libraries, see [A Tour of the Dart Libraries](https://dart.dev/guides/libraries/library-tour).
