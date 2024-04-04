# Markdown Parser

This console application takes as input the path to a Markdown text file and generates a fragment in HTML or ANSI formats. The 
application outputs the generated markup either to the standard output (stdout) or, with the `--out /path/to/outputFile`
argument, to the output file. By using the `--format==value` flag, you can specify the output format. ANSI format is used for standard output (stdout) by default, whereas HTML is used for output to a file. If the markup in the input file is incorrect, the program prints the error to the standard error line
(stderr) and exits with a non-zero exit code.

## Usage

1. Compile Java files
```
javac -d target src/main/java/org/example/*.java
```

2. Run the application
```
java -cp target org.example.Main <file path>
```

> **NOTE:** set the --out flag to write the converted fragment to the specified file

```
java -cp target org.example.Main <file path> --out <output file path>
```

>**NOTE:** set the --format flag to specify the output format

```
java -cp target org.example.Main <file path> [--out <output file path>] --format <ansi/html>
```

## Example

Markdown
```
Я із **надій** будую човен,
І вже немовби наяву
З `тобою, ніжний, срібномовен`,
По морю радості пливу.

І гомонять навколо `хвилі`,
З _бортів човна змивають мох_,
І ми з тобою вже не в силі
**Буть нещасливими удвох**.

\```
І ти **ясна**, і я `прозорий`,
_І душі наші мов пісні_,
І світ **_великий, неозорий_**
Належить нам – тобі й мені.
\```

О **мо_ре** радості безкрає,
Чи я тебе `перепливу`?
Якби того, що в _мріях маю_,
**Хоч краплю мати наяву**.
```
HTML
```
<p>Я із <b>надій</b> будую човен,</p>
<p>І вже немовби наяву</p>
<p>З <tt>тобою, ніжний, срібномовен</tt>,</p>
<p>По морю радості пливу.</p>
<p>І гомонять навколо <tt>хвилі</tt>,</p>
<p>З <i>бортів човна змивають мох</i>,</p>
<p>І ми з тобою вже не в силі</p>
<p><b>Буть нещасливими удвох</b>.</p>
<p><pre>
І ти **ясна**, і я `прозорий`,
_І душі наші мов пісні_,
І світ **_великий, неозорий_**
Належить нам – тобі й мені.
</pre></p>
<p>О <b>мо_ре</b> радості безкрає,</p>
<p>Чи я тебе <tt>перепливу</tt>?</p>
<p>Якби того, що в <i>мріях маю</i>,</p>
<p><b>Хоч краплю мати наяву</b>.</p>
```
