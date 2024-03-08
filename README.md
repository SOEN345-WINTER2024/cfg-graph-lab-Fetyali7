# Student name and ID:
## Ali Fetanat, ID: 40158208

### Step 1:
![CFG diagram lab drawio](https://github.com/SOEN345-WINTER2024/cfg-graph-lab-Fetyali7/assets/70493307/0d57af7b-3213-4f3f-a519-64547174957c)

### Step 2:
Test Requirements (TRs)
* 		Numeric Input Validation (TR1): Verifying the correct capture and display of numeric inputs from 0 through 9.
* 		Arithmetic Operations Verification (TR2): Ensuring the calculator accurately sets up for addition, subtraction, multiplication, and division upon the respective button presses.
* 		Clear Functionality Assurance (TR3): Confirming the calculator resets all internal states and displays as intended when the clear button is activated.
* 		Calculation Execution Accuracy (TR4): Testing the calculator's ability to perform and display the result of calculations correctly after pressing the equals button.
Detailed Test Paths
Numeric Input Validation (TR1)
* Path 1: Activate R.id.key_0_btn and verify display shows "0".
* Path 2-10: Similarly, for R.id.key_1_btn through R.id.key_9_btn, ensure each numeric button correctly updates the display with its respective value.
Arithmetic Operations Verification (TR2)
* Path 11: Press R.id.key_1_btn followed by R.id.key_add_btn and check if the addition operation is queued.
* Path 12: Press R.id.key_1_btn followed by R.id.key_sub_btn and check if the subtraction operation is queued.
* Path 13: Press R.id.key_1_btn followed by R.id.key_div_btn and check if the division operation is queued.
* Path 14: Press R.id.key_1_btn followed by R.id.key_mult_btn and verify the multiplication operation is queued.
Clear Functionality Assurance (TR3)
* Path 15: After engaging any operation or numeric input, trigger R.id.key_clear_btn and confirm that all internal states (including number, num1, num2, and symbol) are reset, and the display is cleared.
Calculation Execution Accuracy (TR4)
* Path 16 (Addition): Input 1, select addition, input another 1, press equals, and assert the displayed result is "2".
* Path 17 (Subtraction): Input 2, choose subtraction, input 1, press equals, and validate the result as "1".
* Path 18 (Division): Enter 6, opt for division, input 2, press equals, and ensure the outcome is "3".
* Path 19 (Multiplication): Key in 3, select multiplication, input another 3, hit equals, and confirm the result displayed is "9".

### Step 3: 
Test Requirements for Edge Coverage (TRs)
* 		[Sequential Numeric Inputs (TR1)]
* 		[Transition Between Arithmetic Operations (TR2)]
* 		[Operation After Calculation (TR3)]
* 		[Clear Functionality Post-Operation and Post-Calculation (TR4)]
Detailed Test Paths for Edge Coverage
[Sequential Numeric Inputs (TR1)]
* [Path 1]: [1] ➔ [2] ➔ Verify "12".
[Transition Between Arithmetic Operations (TR2)]
* [Path 2]: [3] ➔ [+] ➔ [-] ➔ [1] ➔ Verify last operation executed.
* [Path 3]: [Operation] ➔ [Operation] ➔ Verify last operation ready.
[Operation After Calculation (TR3)]
* [Path 4]: [5] ➔ [+] ➔ [3] ➔ [=] ➔ [1] ➔ [+] ➔ [1] ➔ Verify new calculation.
* [Path 5]: [2] ➔ [*] ➔ [2] ➔ [=] ➔ [6] ➔ [/] ➔ [3] ➔ Verify new calculation.
[Clear Functionality Post-Operation and Post-Calculation (TR4)]
* [Path 6]: [Operation] ➔ [C] ➔ Verify reset.
* [Path 7]: [Calculation] ➔ [C] ➔ Verify reset.

### Step 4:
Test Requirements for Edge-Pair Coverage (TRs)
* 		[Sequential Numeric Inputs (TR1)]
* 		[Transition Between Arithmetic Operations (TR2)]
* 		[Operation After Calculation (TR3)]
* 		[Clear Functionality Post-Operation and Post-Calculation (TR4)]
Detailed Test Paths for Edge-Pair Coverage
[Sequential Numeric Inputs (TR1)]
* [Path 1]: [1] ➔ [2] ➔ [3] ➔ Verify "123".
[Transition Between Arithmetic Operations (TR2)]
* [Path 2]: [3] ➔ [+] ➔ [-] ➔ [*] ➔ [1] ➔ Verify last operation executed.
* [Path 3]: [4] ➔ [/] ➔ [+] ➔ [-] ➔ Verify last operation ready.
[Operation After Calculation (TR3)]
* [Path 4]: [5] ➔ [+] ➔ [3] ➔ [=] ➔ [2] ➔ [-] ➔ [1] ➔ [=] ➔ Verify new calculation continues correctly.
* [Path 5]: [2] ➔ [*] ➔ [2] ➔ [=] ➔ [6] ➔ [/] ➔ [3] ➔ [=] ➔ Verify correct calculation result.
[Clear Functionality Post-Operation and Post-Calculation (TR4)]
* [Path 6]: [3] ➔ [+] ➔ [C] ➔ [4] ➔ [-] ➔ Verify reset and correct operation.
* [Path 7]: [2] ➔ [*] ➔ [2] ➔ [=] ➔ [C] ➔ [5] ➔ [/] ➔ [1] ➔ Verify reset and correct operation.

### Step 5:
![EFG diagram lab drawio](https://github.com/SOEN345-WINTER2024/cfg-graph-lab-Fetyali7/assets/70493307/aeef2e51-56ca-4923-baf7-02595cb29de3)

### Step 6:
node coverage:
key_0_btn to key_9_btn: Each button press for digits 0 through 9, appending the respective digit to the number variable.
key_add_btn: Initiates addition operation.
key_sub_btn: Initiates subtraction operation.
key_div_btn: Initiates division operation.
key_mult_btn: Initiates multiplication operation.
key_clear_btn: Clears all inputs and outputs.
key_equals_btn: Computes and displays the result of the operation.

Edge coverage:
key_0_btn to key_add_btn: Entering "0" then pressing "+".
key_add_btn to key_1_btn: Pressing "+" then entering "1".
And so forth for transitions between digit entry, operations, and clear.

Edge-Pair Coverage:
[Path 1]: [1] ➔ [2] ➔ [3] ➔ Verify "123".
[Transition Between Arithmetic Operations (TR2)]
* [Path 2]: [3] ➔ [+] ➔ [-] ➔ [*] ➔ [1] ➔ Verify last operation executed.
* [Path 3]: [4] ➔ [/] ➔ [+] ➔ [-] ➔ Verify last operation ready.




# Soot Tutorial
[![Build Status](https://travis-ci.com/noidsirius/SootTutorial.svg?branch=master)](https://travis-ci.com/noidsirius/SootTutorial)
[![Gitpod ready-to-code](https://img.shields.io/badge/Gitpod-ready--to--code-blue?logo=gitpod)](https://gitpod.io/#https://github.com/noidsirius/SootTutorial)
[![Docker Pull](https://img.shields.io/docker/pulls/noidsirius/soot_tutorial)](https://hub.docker.com/r/noidsirius/soot_tutorial)


This repository contains (will contain) several simple examples of static program analysis in Java using [Soot](https://github.com/Sable/soot).

## Who this tutorial is for?
Anybody who knows Java programming and wants to do some static analysis in practice but does not know anything about Soot and static analysis in theory.

If you have some prior knowledge about static program analysis I suggest you learn Soot from [here](https://github.com/Sable/soot/wiki/Tutorials).

### [Why another tutorial for Soot?](docs/Other/Motivation.md)

## Setup
In short, use Java 8 and run `./gradlew build`. For more information and Docker setup, follow this [link](docs/Setup/). 

## Chapters
### 1: Get your hands dirty

In this chapter, you will visit a very simple code example to be familiar with Soot essential data structures and **Jimple**, Soot's principle intermediate representation.

* `./gradlew run --args="HelloSoot"`: The Jimple representation of the [printFizzBuzz](demo/HelloSoot/FizzBuzz.java) method alongside the branch statement.
* `./gradlew run --args="HelloSoot draw"`: The visualization of the [printFizzBuzz](demo/HelloSoot/FizzBuzz.java) control-flow graph.



|Title |Tutorial | Soot Code        | Example Input  |
| :---: |:-------------: |:-------------:| :-----:|
|Hello Soot |[Doc](docs/1/)      | [HelloSoot.java](src/main/java/dev/navids/soottutorial/hellosoot/HelloSoot.java) | [FizzBuzz.java](demo/HelloSoot/FizzBuzz.java) |

<img src="docs/1/images/cfg.png" alt="Control Flow Graph" width="400"/>

### 2: Know the basic APIs

In this chapter, you get familiar with some basic but useful methods in Soot to help read, analyze, and even update java code.

* `./gradlew run --args="BasicAPI"`: Analyze the class [Circle](demo/BasicAPI/Circle.java).
* `./gradlew run --args="BasicAPI draw"`: Analyze the class [Circle](demo/BasicAPI/Circle.java) and draws the call graph.

|Title |Tutorial | Soot Code        | Example Input  |
| :---: |:-------------: |:-------------:| :-----:|
|Basic API |[Doc](https://medium.com/@noidsirius/know-the-basic-tools-in-soot-18f394318a9c)| [BasicAPI.java](src/main/java/dev/navids/soottutorial/basicapi/BasicAPI.java) | [Circle](demo/BasicAPI/Circle.java) |


<img src="docs/2/images/callgraph.png" alt="Call Graph" width="400"/>

### 3: Android Instrumentation

In this chapter, you learn how to insert code into Android apps (without having their source code) using Soot. To run the code, you need Android SDK (check this [link](docs/Setup/)).

* `./gradlew run --args="AndroidLogger"`: Insert logging method calls at the beginning of APK methods of [Numix Calculator](demo/Android/calc.apk).
* `./gradlew run --args="AndroidClassInjector"`: Create a new class from scratch and inject it to the  [Numix Calculator](demo/Android/calc.apk).

The instrumented APK is located in `demo/Android/Instrumented`. You need to sign it in order to install on an Android device:
```sh
cd ./demo/Android
# on Windows, replace 'sign.sh' by 'sign.ps1'
./sign.sh Instrumented/calc.apk key "android"
adb install -r -t Instrumented/calc.apk
```
To see the logs, run `adb logcat | grep -e "<SOOT_TUTORIAL>"`

|Title |Tutorial | Soot Code        | Example APK|
| :---: |:-------------: |:-------------:| :-----:|
|Log method calls in an APK| [Doc](https://medium.com/@noidsirius/instrumenting-android-apps-with-soot-dd6f146ff4d2)| [AndroidLogger.java](src/main/java/dev/navids/soottutorial/android/AndroidLogger.java) | [Numix Calculator](demo/Android/calc.apk) (from [F-Droid](https://f-droid.org/en/packages/com.numix.calculator/))|
|Create and inject a class into an APK| [Doc](https://medium.com/@noidsirius/instrumenting-android-apps-with-soot-dd6f146ff4d2) | [AndroidClassInjector.java](src/main/java/dev/navids/soottutorial/android/AndroidClassInjector.java) | [Numix Calculator](demo/Android/calc.apk) (from [F-Droid](https://f-droid.org/en/packages/com.numix.calculator/))|

<img src="docs/3/images/packs.png" alt="Soot Packs + Dexpler" width="400"/>

### 4: Call graphs and PointsTo Analysis in Android

This chapter gives you a brief overview o call graphs and PointsTo analysis in Android and you learn how to create calls graphs using FlowDroid. The source code of the example code is [here](demo/Android/STDemoApp). To run the code, you need Android SDK (check this [link](docs/Setup/)).

* `./gradlew run --args="AndroidCallGraph <CG_Algorithm> (draw)"`: Create the call graph of [SootTutorial Demo App](demo/Android/st_demo.apk) using `<CG_Algorithm>` algorithm and print information such as reachable methods or the number of edges.
    * `<CG_Algorithm>` can be `SPARK` or `CHA`
    * `draw` argument is optional, if provided a visualization of call graph will shown.
    * For example, `./gradlew run --args="AndroidCallGraph SPARK draw"` visualizes the call graph generated by SPARK algorithm.
* `./gradlew run --args="AndroidPTA"`: Perform PointsTo and Alias Analysis on [SootTutorial Demo App](demo/Android/st_demo.apk) using FlowDroid.

|Title |Tutorial | Soot Code        | Example APK|
| :---: |:-------------: |:-------------:| :-----:|
|Call graphs in Android| [Doc](https://medium.com/geekculture/generating-call-graphs-in-android-using-flowdroid-pointsto-analysis-7b2e296e6697)| [AndroidCallgraph.java](src/main/java/dev/navids/soottutorial/android/AndroidCallgraph.java) | [SootTutorial Demo App](demo/Android/st_demo.apk) ([source code](demo/Android/STDemoApp))|
|PointsTo Analysis in Android| [Doc](https://medium.com/geekculture/generating-call-graphs-in-android-using-flowdroid-pointsto-analysis-7b2e296e6697)| [AndroidPointsToAnalysis.java](src/main/java/dev/navids/soottutorial/android/AndroidPointsToAnalysis.java) | [SootTutorial Demo App](demo/Android/st_demo.apk) ([source code](demo/Android/STDemoApp))|

<img src="docs/4/images/Spark_CG.png" alt="The call graph of SootTutorial Demo app" width="400"/>



### 5: Some *Real* Static Analysis (:construction: WIP)

* `./gradlew run --args="UsageFinder 'void println(java.lang.String)' 'java.io.PrintStream"`: Find usages of the method with the given subsignature in all methods of [UsageExample.java](demo/IntraAnalysis/UsageExample.java).
* `./gradlew run --args="UsageFinder 'void println(java.lang.String)' 'java.io.PrintStream"`: Find usages of the method with the given subsignature of the given class signature in all methods of [UsageExample.java](demo/IntraAnalysis/UsageExample.java).


|Title |Tutorial | Soot Code        | Example Input  |
| :---: |:-------------: |:-------------:| :-----:|
|Find usages of a method| | [UsageFinder.java](src/main/java/dev/navids/soottutorial/intraanalysis/usagefinder/UsageFinder.java) | [UsageExample.java](demo/IntraAnalysis/usagefinder/UsageExample.java) |
|Null Pointer Analysis ||[NullPointerAnalysis](src/main/java/dev/navids/soottutorial/intraanalysis/npanalysis/) | [NullPointerExample.java](demo/IntraAnalysis/NullPointerExample.java) |

### 6: Interprocedural analysis (:construction: WIP)
|Title |Tutorial | Soot Code        | Example Input  |
| :---: |:-------------: |:-------------:| :-----:|
| | | | |
