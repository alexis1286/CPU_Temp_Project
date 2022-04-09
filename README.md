# Requirements

  * Python 3.9

# Sample Execution & Output

If run without command line arguments, using

```
python main.py

```
the following usage message will be displayed.

```
    file_name = sys.argv[1]
    IndexError: list index out of range
```

If run using

```
python main.py sensors-2018.12.26.txt

```

```
file inputted will contain input similar to:

+61.0Â°C +63.0Â°C +50.0Â°C +58.0Â°C
+80.0Â°C +81.0Â°C +68.0Â°C +77.0Â°C
+62.0Â°C +63.0Â°C +52.0Â°C +60.0Â°C
+83.0Â°C +82.0Â°C +70.0Â°C +79.0Â°C
+68.0Â°C +69.0Â°C +58.0Â°C +65.0Â°C
+82.0Â°C +81.0Â°C +67.0Â°C +77.0Â°C
+76.0Â°C +78.0Â°C +63.0Â°C +73.0Â°C
+83.0Â°C +84.0Â°C +71.0Â°C +79.0Â°C
+74.0Â°C +77.0Â°C +65.0Â°C +73.0Â°C
+83.0Â°C +81.0Â°C +71.0Â°C +79.0Â°C
+77.0Â°C +79.0Â°C +67.0Â°C +74.0Â°C
+65.0Â°C +68.0Â°C +55.0Â°C +64.0Â°C
+78.0Â°C +83.0Â°C +64.0Â°C +78.0Â°C
+66.0Â°C +67.0Â°C +53.0Â°C +62.0Â°C
+65.0Â°C +67.0Â°C +55.0Â°C +63.0Â°C
+85.0Â°C +83.0Â°C +71.0Â°C +75.0Â°C
+85.0Â°C +83.0Â°C +71.0Â°C +81.0Â°C
+66.0Â°C +67.0Â°C +55.0Â°C +64.0Â°C
.
.
.
.
Etc

```

output will be *simliar* to

```
4 text files for each core will be created in the program file named:
sensors-2018.12.26-core-1.txt
sensors-2018.12.26-core-2.txt
sensors-2018.12.26-core-3.txt
sensors-2018.12.26-core-4.txt
```
Example of output in file:
0<= x < 30; y_0 = 61.0 + 0.6333333333333333x; interpolation 
30<= x < 60; y_1 = 98.0 + -0.6x; interpolation 
60<= x < 90; y_2 = 20.0 + 0.7x; interpolation 
90<= x < 120; y_3 = 128.0 + -0.5x; interpolation 
.
.
. (30 second increments to 35580)
.
.
35490<= x < 35520; y_1183 = -8208.0 + 0.23333333333333334x; interpolation 
35520<= x < 35550; y_1184 = 22576.0 + -0.6333333333333333x; interpolation 
35550<= x < 35580; y_1185 = -20084.0 + 0.5666666666666667x; interpolation 
35580<= x < 35610; y_1186 = -3480.0 + 0.1x; interpolation 
0 <= x < 35610;   y = 77.14593793273355 -0.00011882251628365715x; least-squares

```

will be generated.

---

```
An optional input without CPU labels can also be inputted. For example:

```

python main.py sensors-2018.12.26-no-labels.txt

```
file inputted will contain input similar to:

61.0 63.0 50.0 58.0
80.0 81.0 68.0 77.0
62.0 63.0 52.0 60.0
83.0 82.0 70.0 79.0
68.0 69.0 58.0 65.0
82.0 81.0 67.0 77.0
76.0 78.0 63.0 73.0
83.0 84.0 71.0 79.0
74.0 77.0 65.0 73.0
83.0 81.0 71.0 79.0
.
.
.
etc


```
output will be *simliar* to

```
4 text files for each core will be created in the program file named:
sensors-2018.12.26-no-labels-core-1.txt
sensors-2018.12.26-no-labels-core-2.txt
sensors-2018.12.26-no-labels-core-3.txt
sensors-2018.12.26-no-labels-core-4.txt
```
```
Example of output in file:
0<= x < 30; y_0 = 61.0 + 0.6333333333333333x; interpolation 
30<= x < 60; y_1 = 98.0 + -0.6x; interpolation 
60<= x < 90; y_2 = 20.0 + 0.7x; interpolation 
90<= x < 120; y_3 = 128.0 + -0.5x; interpolation 
.
.
. (30 second increments to 35580)
.
.
35490<= x < 35520; y_1183 = -8208.0 + 0.23333333333333334x; interpolation 
35520<= x < 35550; y_1184 = 22576.0 + -0.6333333333333333x; interpolation 
35550<= x < 35580; y_1185 = -20084.0 + 0.5666666666666667x; interpolation 
35580<= x < 35610; y_1186 = -3480.0 + 0.1x; interpolation 
0 <= x < 35610;   y = 77.14593793273355 -0.00011882251628365715x; least-squares

```

will be generated.

---
