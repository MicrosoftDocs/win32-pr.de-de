---
title: Operatoren
description: Ausdrücke sind Sequenzen von Variablen und Literalen, die durch Operatoren interpunktioniert werden.
ms.assetid: c31aa0b8-1284-48aa-b000-d72433f0f5cc
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d7a44fe02983038658247fedaec7122f09306548
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119605"
---
# <a name="operators"></a>Operatoren

Ausdrücke sind Sequenzen von [Variablen und](dx-graphics-hlsl-variable-syntax.md) Literalen, die durch Operatoren [interpunktioniert werden.](dx-graphics-hlsl-statement-blocks.md) Operatoren bestimmen, wie die Variablen und Literale kombiniert, verglichen, ausgewählt und so weiter. Zu den Operatoren gehören:



| Operatorname                                                                                | Operatoren                                                                   |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Additive und multiplikative Operatoren](#additive-and-multiplicative-operators) | +, -, \*, /, %                                                     |
| [Arrayoperator](#array-operator)                                               | \[i\]                                                              |
| [Zuweisungsoperatoren](#assignment-operators)                                   | =, +=, -=, \*=, /=, %=                                             |
| [Binäre Casts](#binary-casts)                                                   | C-Regeln für float und int, C-Regeln oder systeminterne HLSL-Regeln für bool     |
| [Bitwise Operators (Bitweise Operatoren)](#bitwise-operators)                                         | ~, <<, >>, &, \| , ^, <<=, >>=, &=, \| =, ^= |
| [Boolesche mathematische Operatoren](#boolean-math-operators)                               | & &, , \| \| ?:                                                      |
| [Cast-Operator](#cast-operator)                                                 | (Typ)                                                             |
| [Kommaoperator](#comma-operator)                                               | ,                                                                  |
| [Comparison Operators (Vergleichsoperatoren)](#comparison-operators)                                   | <, >, ==, !=, <=, >=                                   |
| [Präfix- oder Postfixoperatoren](#prefix-or-postfix-operators)                     | ++, --                                                             |
| [Structure-Operator](#structure-operator)                                       | .                                                                  |
| [Unary Operators (Unäre Operatoren)](#unary-operators)                                             | !, -, +                                                            |



 

Viele der Operatoren sind komponentenspezifische Operatoren, was bedeutet, dass der Vorgang unabhängig für jede Komponente jeder Variablen ausgeführt wird. Beispielsweise wird für eine einzelne Komponentenvariable ein Vorgang ausgeführt. Andererseits werden für eine Variable mit vier Komponenten vier Vorgänge ausgeführt, eine für jede Komponente.

Alle Operatoren, die etwas mit dem Wert tun, z. B. + und \* , funktionieren pro Komponente.

Die Vergleichsoperatoren erfordern, dass eine einzelne [](dx-graphics-hlsl-any.md) Komponente funktioniert, es sei denn, Sie verwenden die [**alle**](dx-graphics-hlsl-all.md) oder eine systeminterne Funktion mit einer Variablen mit mehreren Komponenten. Der folgende Vorgang schlägt fehl, da die if-Anweisung einen einzelnen Bool erfordert, aber einen bool4 empfängt:


```
if (A4 < B4)
```



Die folgenden Vorgänge sind erfolgreich:


```
if ( any(A4 < B4) )
if ( all(A4 < B4) )
```



Die binären Cast-Operatoren [**asfloat**](dx-graphics-hlsl-asfloat.md), [**asint**](dx-graphics-hlsl-asint.md)und so weiter für die Arbeit pro Komponente, mit Ausnahme von [**asdouble,**](asdouble.md) deren spezielle Regeln dokumentiert sind.

Auswahloperatoren wie Perioden-, Komma- und Arrayklammern funktionieren nicht pro Komponente.

Cast-Operatoren ändern die Anzahl der Komponenten. Die folgenden Cast-Vorgänge zeigen ihre Äquivalenz:


```
(float) i4 ->   float(i4.x)
(float4)i ->   float4(i, i, i, i)
```



## <a name="additive-and-multiplicative-operators"></a>Additive und multiplikative Operatoren

Die additiven und multiplikativen Operatoren sind: +, -, \* , /, %


```
int i1 = 1;
int i2 = 2;
int i3 = i1 + i2;  // i3 = 3
i3 = i1 * i2;        // i3 = 1 * 2 = 2
```




```
i3 = i1/i2;       // i3 = 1/3 = 0.333. Truncated to 0 because i3 is an integer.
i3 = i2/i1;       // i3 = 2/1 = 2
```




```
float f1 = 1.0;
float f2 = 2.0f;
float f3 = f1 - f2; // f3 = 1.0 - 2.0 = -1.0
f3 = f1 * f2;         // f3 = 1.0 * 2.0 = 2.0
```




```
f3 = f1/f2;        // f3 = 1.0/2.0 = 0.5
f3 = f2/f1;        // f3 = 2.0/1.0 = 2.0
```



Der Modulusoperator gibt den Rest einer Division zurück. Dies führt zu unterschiedlichen Ergebnissen, wenn ganze Zahlen und Gleitkommazahlen verwendet werden. Ganzzahlige Reste, die Bruchzahlen sind, werden abgeschnitten.


```
int i1 = 1;
int i2 = 2;
i3 = i1 % i2;      // i3 = remainder of 1/2, which is 1
i3 = i2 % i1;      // i3 = remainder of 2/1, which is 0
i3 = 5 % 2;        // i3 = remainder of 5/2, which is 1
i3 = 9 % 2;        // i3 = remainder of 9/2, which is 1
```



Der Modulusoperator schneide einen Bruchteil des Rests ab, wenn ganze Zahlen verwendet werden.


```
f3 = f1 % f2;      // f3 = remainder of 1.0/2.0, which is 0.5
f3 = f2 % f1;      // f3 = remainder of 2.0/1.0, which is 0.0
```



Der %-Operator wird nur in Fällen definiert, in denen beide Seiten positiv oder beide Seiten negativ sind. Im Gegensatz zu C funktioniert es auch mit Gleitkommadatentypen sowie ganzen Zahlen.

## <a name="array-operator"></a>Arrayoperator

Der Array-Memberauswahloperator " \[ i " wählt eine oder mehrere Komponenten in einem Array \] aus. Es handelt sich um eine Gruppe von eckigen Klammern, die einen nullbasierten Index enthalten.


```
int arrayOfInts[4] = { 0,1,2,3 };
arrayOfInts[0] = 2;
arrayOfInts[1] = arrayOfInts[0];
```



Der Arrayoperator kann auch für den Zugriff auf einen Vektor verwendet werden.


```
float4 4D_Vector = { 0.0f, 1.0f, 2.0f, 3.0f  };         
float 1DFloat = 4D_Vector[1];          // 1.0f
```



Durch Hinzufügen eines zusätzlichen Indexes kann der Arrayoperator auch auf eine Matrix zugreifen.


```
float4x4 mat4x4 = {{0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} };
mat4x4[0][1] = 1.1f;
float 1DFloat = mat4x4[0][1];      // 0.0f
```



Der erste Index ist der nullbasierte Zeilenindex. Der zweite Index ist der nullbasierte Spaltenindex.

## <a name="assignment-operators"></a>Zuweisungsoperatoren

Die Zuweisungsoperatoren sind: =, +=, -=, \* =, /=

Variablen können Literalwerte zugewiesen werden:


```
int i = 1;            
float f2 = 3.1f; 
bool b = false;
string str = "string";
```



Variablen können auch das Ergebnis einer mathematischen Operation zugewiesen werden:


```
int i1 = 1;
i1 += 2;           // i1 = 1 + 2 = 3
```



Eine Variable kann auf beiden Seiten des Gleichheitszeichens verwendet werden:


```
float f3 = 0.5f;
f3 *= f3;          // f3 = 0.5 * 0.5 = 0.25
```



Die Division für Gleitkommavariablen ist wie erwartet, da dezimale Reste kein Problem darstellen.


```
float f1 = 1.0;
f1 /= 3.0f;        // f1 = 1.0/3.0 = 0.333
```



Seien Sie vorsichtig, wenn Sie ganze Zahlen verwenden, die geteilt werden können, insbesondere, wenn das Ergebnis durch Abschneiden beeinträchtigt wird. Dieses Beispiel ist mit dem vorherigen Beispiel identisch, mit Ausnahme des -Datentyps. Die Kürzung führt zu einem sehr anderen Ergebnis.


```
int i1 = 1;
i1 /= 3;           // i1 = 1/3 = 0.333, which gets truncated to 0
```



## <a name="binary-casts"></a>Binäre Casts

Der Umwandlungsvorgang zwischen int und float konvertiert den numerischen Wert gemäß C-Regeln zum Abschneiden eines int-Typs in die entsprechenden Darstellungen. Die Umwandlung eines Werts von einem float-Wert in einen int-Wert und zurück in einen float-Wert führt zu einer verlustberatenden Konvertierung basierend auf der Genauigkeit des Ziels.

Binäre Casts können auch mit systeminternen Funktionen [**(DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)ausgeführt werden, die die Bitdarstellung einer Zahl in den Zieldatentyp neu interpretiert.


```
asfloat() // Cast to float
asint()   // Cast to int 
asuint()  // Cast to uint
```



## <a name="bitwise-operators"></a>Bitweise Operatoren

HLSL unterstützt die folgenden bitweise Operatoren, die im Hinblick auf andere Operatoren der gleichen Rangfolge wie C folgen. In der folgenden Tabelle werden die Operatoren beschrieben.

> [!Note]  
> Bitweise Operatoren erfordern Shader model 4 0 with Direct3D 10 and higher hardware [(Shadermodell 4 \_ 0](dx-graphics-hlsl-sm4.md) mit Direct3D 10 und höher).

 



| Operator          |  Funktion                 |
|-----------|-------------------|
| ~         | Logical Not       |
| <<  | Linksverschiebung        |
| >>  | Rechtsverschiebung       |
| &         | Logisches UND       |
| \|        | Logisches ODER.        |
| ^         | Logisches Xor       |
| <<= | Left Shift Equal  |
| >>= | Rechtsverschiebung gleich |
| &=        | Und gleich         |
| \|=       | Oder gleich          |
| ^=        | Xor Equal         |



 

Bitweise Operatoren werden so definiert, dass sie nur für int- und uint-Datentypen verwendet werden. Der Versuch, bitweise Operatoren für float- oder struct-Datentypen zu verwenden, führt zu einem Fehler.

## <a name="boolean-math-operators"></a>Boolesche mathematische Operatoren

Die booleschen mathematischen Operatoren sind: &&, \| \| , ?:


```
bool b1 = true;
bool b2 = false;
bool b3 = b1 && b2 // b3 = true AND false = false
b3 = b1 || b2                // b3 = true OR false = true
```



Im Gegensatz zur Kurzschlussauswertung von &&, und ?: in C werden \| HLSL-Ausdrücke eine Auswertung nie kurzschalten, da es sich um \| Vektoroperationen handelt. Alle Seiten des Ausdrucks werden immer ausgewertet.

Boolesche Operatoren funktionieren pro Komponente. Wenn Sie also zwei Vektoren vergleichen, ist das Ergebnis ein Vektor, der das boolesche Ergebnis des Vergleichs für jede Komponente enthält.

Bei Ausdrücken, die boolesche Operatoren verwenden, werden die Größe und der Komponententyp jeder Variablen vor dem Auftreten des Vorgangs auf denselben Wert auf denselben Wert 2016 hinaus 2016 2016 und 2016 auf den gleichen Wert 12.0(n) des Typs der einzelnen Variablen um 10000000000000 Der promoted-Typ bestimmt die Auflösung, bei der der Vorgang stattfindet, sowie den Ergebnistyp des Ausdrucks. Beispielsweise würde ein int3 + float-Ausdruck zur Auswertung auf float3 + float3 und das Ergebnis vom Typ float3 werden.

## <a name="cast-operator"></a>Umwandlungsoperator

Ein Ausdruck, dem ein Typname in Klammern voran steht, ist eine explizite Typ cast. Eine Typ cast konvertiert den ursprünglichen Ausdruck in den Datentyp der Umwandlung. Im Allgemeinen können die einfachen Datentypen in komplexere Datentypen umgewandelt werden (mit einer Heraufstufungscast), aber nur einige komplexe Datentypen können in einfache Datentypen umgewandelt werden (mit einer Herabstufungscast).

Nur die typisierte Umwandlung auf der rechten Seite ist zulässig. Beispielsweise sind Ausdrücke wie `(int)myFloat = myInt;` ungültig. Verwenden Sie stattdessen `myFloat = (float)myInt;`.

Der Compiler führt auch eine implizite Typcasting durch. Beispielsweise sind die folgenden beiden Ausdrücke gleichwertig:


```
int2 b = int2(1,2) + 2;
int2 b = int2(1,2) + int2(2,2);
```



## <a name="comma-operator"></a>Kommaoperator

Der Kommaoperator (,) trennt einen oder mehrere Ausdrücke, die in der Reihenfolge ausgewertet werden sollen. Der Wert des letzten Ausdrucks in der Sequenz wird als Wert der Sequenz verwendet.

Hier sehen Sie einen Fall, auf den Sie achten müssen. Wenn der Konstruktortyp versehentlich von der rechten Seite des Gleichheitszeichens weggelassen wird, enthält die rechte Seite jetzt vier Ausdrücke, die durch drei Kommas getrennt sind.


```
// Instead of using a constructor
float4 x = float4(0,0,0,1); 

// The type on the right side is accidentally left off
float4 x = (0,0,0,1); 
```



Der Kommaoperator wertet einen Ausdruck von links nach rechts aus. Dadurch wird die rechte Seite auf Folgendes reduziert:


```
float4 x = 1; 
```



HLSL verwendet in diesem Fall eine skalare Heraufstufung, sodass das Ergebnis so lautet, als ob dies wie folgt geschrieben worden wäre:


```
float4 x = float4(1,1,1,1);
```



In diesem Fall ist das Verlassen des float4-Typs von der rechten Seite wahrscheinlich ein Fehler, den der Compiler nicht erkennen kann, da dies eine gültige Anweisung ist.

## <a name="comparison-operators"></a>Vergleichsoperatoren

Die Vergleichsoperatoren sind: <, >, ==, !=, <=, >=.

Vergleichen Sie Werte, die größer (oder kleiner als) eines beliebigen Skalarwerts sind:


```
if( dot(lightDirection, normalVector) > 0 )
   // Do something; the face is lit
```




```
if( dot(lightDirection, normalVector) < 0 )
   // Do nothing; the face is backwards
```



Oder vergleichen Sie Werte, die einem beliebigen Skalarwert entsprechen (oder nicht gleich sind):


```
if(color.a == 0)
   // Skip processing because the face is invisible

if(color.a != 0)
   // Blend two colors together using the alpha value
```



Sie können auch sowohl - als auch -Vergleichswerte kombinieren, die größer oder gleich (oder kleiner als oder gleich) eines beliebigen Skalarwerts sind:


```
if( position.z >= oldPosition.z )
   // Skip the new face because it is behind the existing face
```




```
if( currentValue <= someInitialCondition )
   // Reset the current value to its initial condition
```



Jeder dieser Vergleiche kann mit einem beliebigen skalaren Datentyp durchgeführt werden.

Um Vergleichsoperatoren mit Vektor- und Matrixtypen zu verwenden, verwenden Sie die [**all-**](dx-graphics-hlsl-all.md) oder [**eine beliebige**](dx-graphics-hlsl-any.md) systeminterne Funktion.

Dieser Vorgang schlägt fehl, da die if-Anweisung eine einzelne bool erfordert, aber bool4 empfängt:


```
if (A4 < B4)
```



Diese Vorgänge sind erfolgreich:


```
if ( any(A4 < B4) )
if ( all(A4 < B4) )
```



## <a name="prefix-or-postfix-operators"></a>Präfix- oder Postfixoperatoren

Die Präfix- und Postfixoperatoren sind: ++, --. Präfixoperatoren ändern den Inhalt der Variablen, bevor der Ausdruck ausgewertet wird. Postfixoperatoren ändern den Inhalt der Variablen, nachdem der Ausdruck ausgewertet wurde.

In diesem Fall verwendet eine Schleife den Inhalt von i, um die Schleifenanzahl nachzuverfolgen.


```
float4 arrayOfFloats[4] = { 1.0f, 2.0f, 3.0f, 4.4f };

for (int i = 0; i<4; )
{
    arrayOfFloats[i++] *= 2; 
}
```



Da der Postfixinkrementoperator (++) verwendet wird, wird arrayOfFloats \[ i \] mit 2 multipliziert, bevor i erhöht wird. Dies kann leicht neu angeordnet werden, um den Präfixinkrementoperator zu verwenden. Dies ist schwieriger zu lesen, obwohl beide Beispiele gleichwertig sind.


```
float4 arrayOfFloats[4] = { 1.0f, 2.0f, 3.0f, 4.4f };

for (int i = 0; i<4; )
{
    arrayOfFloats[++i - 1] *= 2; 
}
```



Da der Präfixoperator (++) verwendet wird, wird arrayOfFloats \[ i+1 - 1 \] mit 2 multipliziert, nachdem i erhöht wurde.

Der Präfixdekrementoperator und der Postfixdekrementoperator (--) werden in derselben Sequenz wie der Inkrementoperator angewendet. Der Unterschied besteht darin, dass die Dekrementierung 1 subtrahiert, anstatt 1 hinzuzufügen.

## <a name="structure-operator"></a>Structure-Operator

Der Strukturmemberauswahloperator (.) ist ein Punkt. Mit dieser Struktur:


```
struct position
{
float4 x;
float4 y;
float4 z;
};
```



Sie kann wie folgt gelesen werden:


```
struct position pos = { 1,2,3 };

float 1D_Float = pos.x
1D_Float = pos.y
```



Jeder Member kann mit dem Strukturoperator gelesen oder geschrieben werden:


```
struct position pos = { 1,2,3 };
pos.x = 2.0f;
pos.z = 1.0f;       // z = 1.0f
pos.z = pos.x      // z = 2.0f
```



## <a name="unary-operators"></a>Unäre Operatoren

Die unären Operatoren sind: !, -, +

Unäre Operatoren arbeiten mit einem einzelnen Operanden.


```
bool b = false;
bool b2 = !b;      // b2 = true
int i = 2;
int i2 = -i;       // i2 = -2
int j = +i2;       // j = +2
```



## <a name="operator-precedence"></a>Operatorrangfolge

Wenn ein Ausdruck mehrere Operatoren enthält, bestimmt die Operatorrangfolge die Reihenfolge der Auswertung. Die Operatorrangfolge für HLSL folgt der gleichen Rangfolge wie C.

## <a name="remarks"></a>Bemerkungen

Geschweifte Klammern {,} () starten und beenden einen Anweisungsblock. Wenn ein Anweisungsblock eine einzelne Anweisung verwendet, sind die geschweiften Klammern optional.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anweisungen (DirectX HLSL)](dx-graphics-hlsl-statements.md)
</dt> </dl>

 

 




