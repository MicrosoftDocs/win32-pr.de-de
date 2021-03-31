---
title: Operatoren
description: Ausdrücke sind Sequenzen von Variablen und Literalen, die von Operatoren interpunliert werden.
ms.assetid: c31aa0b8-1284-48aa-b000-d72433f0f5cc
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 69fc29f366fa781483edb5fd4653674b387fd156
ms.sourcegitcommit: 37fb32f6150b6ca1db6c52d68a553ec2c8c0879a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2020
ms.locfileid: "104472341"
---
# <a name="operators"></a>Operatoren

Ausdrücke sind Sequenzen von [Variablen](dx-graphics-hlsl-variable-syntax.md) und Literalen, die von [Operatoren](dx-graphics-hlsl-statement-blocks.md)interpunliert werden. Operatoren bestimmen, wie die Variablen und Literale kombiniert, verglichen, ausgewählt usw. kombiniert werden. Zu den Operatoren gehören:



|                                                                                 |                                                                    |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------|
| Name des Operators                                                                   | Operatoren                                                          |
| [Additive und Multiplikative Operatoren](#additive-and-multiplicative-operators) | +, -, \*, /, %                                                     |
| [Array-Operator](#array-operator)                                               | \[i\]                                                              |
| [Zuweisungsoperatoren](#assignment-operators)                                   | =, +=, -=, \*=, /=, %=                                             |
| [Binäre Umwandlungen](#binary-casts)                                                   | C-Regeln für float-und int-, c-oder HLSL-Funktionen für bool     |
| [Bitwise Operators (Bitweise Operatoren)](#bitwise-operators)                                         | ~,  <<,  >>, &, \| , ^,  <<=,  >>=, &=, \| =, ^ = |
| [Boolesche mathematische Operatoren](#boolean-math-operators)                               | & &, \| \| ,?:                                                      |
| [Cast-Operator](#cast-operator)                                                 | Sorte                                                             |
| [Komma-Operator](#comma-operator)                                               | ,                                                                  |
| [Comparison Operators (Vergleichsoperatoren)](#comparison-operators)                                   | <, >, = =,! =, <=, >=                                   |
| [Präfix-oder Postfix Operatoren](#prefix-or-postfix-operators)                     | ++, --                                                             |
| [Structure-Operator](#structure-operator)                                       | .                                                                  |
| [Unary Operators (Unäre Operatoren)](#unary-operators)                                             | !, -, +                                                            |



 

Viele Operatoren sind pro Komponente, was bedeutet, dass der Vorgang unabhängig für jede Komponente der einzelnen Variablen ausgeführt wird. Beispielsweise wird für eine einzelne Komponenten Variable ein Vorgang ausgeführt. Andererseits werden für eine Variable mit vier Komponenten vier Vorgänge ausgeführt, eine für jede Komponente.

Alle Operatoren, die einen Wert für den Wert ausführen (z. b. + und) \* , funktionieren pro Komponente.

Die Vergleichs Operatoren erfordern, dass eine einzelne Komponente funktioniert, es sei denn, Sie verwenden die [**all**](dx-graphics-hlsl-all.md) -oder [**eine**](dx-graphics-hlsl-any.md) intrinsische Funktion mit einer Variablen mit mehreren Komponenten. Der folgende Vorgang schlägt fehl, da die if-Anweisung einen einzelnen booleschen Werten erfordert, aber eine bool4 empfängt:


```
if (A4 < B4)
```



Die folgenden Vorgänge sind erfolgreich:


```
if ( any(A4 < B4) )
if ( all(A4 < B4) )
```



Die binären Umwandlungs Operatoren [**asfloat**](dx-graphics-hlsl-asfloat.md), [**asint**](dx-graphics-hlsl-asint.md)usw. arbeiten pro Komponente, mit Ausnahme von [**AsDouble**](asdouble.md) , deren spezielle Regeln dokumentiert werden.

Auswahl Operatoren wie Zeitraum, Komma und Array eckige Klammern funktionieren nicht pro Komponente.

Umwandlungs Operatoren ändern die Anzahl der Komponenten. Die folgenden Umwandlungs Vorgänge zeigen ihre Äquivalenz:


```
(float) i4 ->   float(i4.x)
(float4)i ->   float4(i, i, i, i)
```



## <a name="additive-and-multiplicative-operators"></a>Additive und Multiplikative Operatoren

Die Additiven und Multiplikations Operatoren lauten: +,-, \* ,/,%


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



Der Modulo-Operator gibt den Rest einer Division zurück. Dies führt zu unterschiedlichen Ergebnissen, wenn ganze Zahlen und Gleit Komma Zahlen verwendet werden. Ganzzahlige Reste, die Bruchzahlen sind, werden abgeschnitten.


```
int i1 = 1;
int i2 = 2;
i3 = i1 % i2;      // i3 = remainder of 1/2, which is 1
i3 = i2 % i1;      // i3 = remainder of 2/1, which is 0
i3 = 5 % 2;        // i3 = remainder of 5/2, which is 1
i3 = 9 % 2;        // i3 = remainder of 9/2, which is 1
```



Der Modulo-Operator verkürzt bei der Verwendung von Ganzzahlen einen Bruchteil der Sekundenbruchteile.


```
f3 = f1 % f2;      // f3 = remainder of 1.0/2.0, which is 0.5
f3 = f2 % f1;      // f3 = remainder of 2.0/1.0, which is 0.0
```



Der%-Operator wird nur in Fällen definiert, in denen entweder beide Seiten positiv sind oder beide Seiten negativ sind. Im Gegensatz zu C funktioniert es auch für Gleit Komma Datentypen sowie für ganze Zahlen.

## <a name="array-operator"></a>Array-Operator

Der Array Elementauswahl-Operator " \[ i \] " wählt eine oder mehrere Komponenten in einem Array aus. Dabei handelt es sich um einen Satz von eckigen Klammern, die einen NULL basierten Index enthalten.


```
int arrayOfInts[4] = { 0,1,2,3 };
arrayOfInts[0] = 2;
arrayOfInts[1] = arrayOfInts[0];
```



Der Array-Operator kann auch für den Zugriff auf einen Vektor verwendet werden.


```
float4 4D_Vector = { 0.0f, 1.0f, 2.0f, 3.0f  };         
float 1DFloat = 4D_Vector[1];          // 1.0f
```



Wenn Sie einen zusätzlichen Index hinzufügen, kann der Array Operator auch auf eine Matrix zugreifen.


```
float4x4 mat4x4 = {{0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} };
mat4x4[0][1] = 1.1f;
float 1DFloat = mat4x4[0][1];      // 0.0f
```



Der erste Index ist der null basierte Zeilen Index. Der zweite Index ist der null basierte Spalten Index.

## <a name="assignment-operators"></a>Zuweisungsoperatoren

Die Zuweisungs Operatoren lauten: =, + =,-=, \* =,/=

Variablen können Literalwerte zugewiesen werden:


```
int i = 1;            
float f2 = 3.1f; 
bool b = false;
string str = "string";
```



Variablen kann auch das Ergebnis einer mathematischen Operation zugewiesen werden:


```
int i1 = 1;
i1 += 2;           // i1 = 1 + 2 = 3
```



Eine Variable kann auf beiden Seiten des Gleichheitszeichens verwendet werden:


```
float f3 = 0.5f;
f3 *= f3;          // f3 = 0.5 * 0.5 = 0.25
```



Die Division für Gleit Komma Variablen ist erwartungsgemäß, da dezimale Reste kein Problem darstellen.


```
float f1 = 1.0;
f1 /= 3.0f;        // f1 = 1.0/3.0 = 0.333
```



Seien Sie vorsichtig, wenn Sie ganze Zahlen verwenden, die geteilt werden können, insbesondere, wenn das Ergebnis durch Abschneiden beeinträchtigt wird. Dieses Beispiel ist mit dem vorherigen Beispiel identisch, mit Ausnahme des-Datentyps. Das Abschneiden führt zu einem sehr unterschiedlichen Ergebnis.


```
int i1 = 1;
i1 /= 3;           // i1 = 1/3 = 0.333, which gets truncated to 0
```



## <a name="binary-casts"></a>Binäre Umwandlungen

Beim Umwandlungs Vorgang zwischen int und float wird der numerische Wert in die entsprechenden Darstellungen der C-Regeln zum Abschneiden eines int-Typs konvertiert. Das Umwandeln eines Werts aus einem Gleit Komma Wert in ein int-und zurück in einen float-Wert führt zu einer verlustfreien Konvertierung basierend auf der Genauigkeit des Ziels.

Binäre Umwandlungen können auch mit [**intrinsischen Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)ausgeführt werden, die die Bit-Darstellung einer Zahl in den Ziel Datentyp uminterpretieren.


```
asfloat() // Cast to float
asint()   // Cast to int 
asuint()  // Cast to uint
```



## <a name="bitwise-operators"></a>Bitweise Operatoren

HLSL unterstützt die folgenden bitweisen Operatoren, die in Bezug auf andere Operatoren die gleiche Rangfolge wie C verwenden. In der folgenden Tabelle werden die Operatoren beschrieben.

> [!Note]  
> Bitweise Operatoren erfordern das [Shadermodell 4 \_ 0](dx-graphics-hlsl-sm4.md) mit Direct3D 10-Hardware und höher.

 



|           |                   |
|-----------|-------------------|
| Operator  | Funktion          |
| ~         | Logisches NOT       |
| <<  | Nach links verschieben        |
| >>  | Rechte Verschiebung       |
| &         | Logisches UND       |
| \|        | Logisches ODER.        |
| ^         | Logisches XOR       |
| <<= | Left Shift gleich  |
| >>= | Rechtsverschiebung gleich |
| &=        | Und gleich         |
| \|=       | Oder gleich          |
| ^=        | XOR-gleich         |



 

Bitweise Operatoren sind so definiert, dass Sie nur für die Datentypen int und uint verwendet werden. Der Versuch, bitweise Operatoren für float-oder struct-Datentypen zu verwenden, führt zu einem Fehler.

## <a name="boolean-math-operators"></a>Boolesche mathematische Operatoren

Die booleschen mathematischen Operatoren sind:  &&, \| \| ,?:


```
bool b1 = true;
bool b2 = false;
bool b3 = b1 && b2 // b3 = true AND false = false
b3 = b1 || b2                // b3 = true OR false = true
```



Anders als bei der Kurzschluss Auswertung von &&, \| \| , und?: in C wird eine Auswertung nie durch HLSL-Ausdrücke kurz geleitet, da es sich um Vektor Vorgänge handelt. Alle Seiten des Ausdrucks werden immer ausgewertet.

Boolesche Operatoren sind pro Komponente funktionsfähig. Dies bedeutet, dass beim Vergleichen von zwei Vektoren das Ergebnis ein Vektor mit dem booleschen Ergebnis des Vergleichs für jede Komponente ist.

Bei Ausdrücken, die boolesche Operatoren verwenden, werden die Größe und der Komponententyp der einzelnen Variablen vor dem Auftreten des Vorgangs so herauf gestuft, dass Sie identisch sind. Der herauf gestufte Typ bestimmt die Auflösung, bei der der Vorgang stattfindet, sowie den Ergebnistyp des Ausdrucks. Beispielsweise würde ein int3 + float-Ausdruck zur Auswertung auf float3 + float3 herauf gestuft werden, und sein Ergebnis wäre der Typ float3.

## <a name="cast-operator"></a>Umwandlungsoperator

Ein Ausdruck, dem ein Typname in Klammern vorangestellt ist, ist eine explizite Typumwandlung. Eine Typumwandlung konvertiert den ursprünglichen Ausdruck in den Datentyp der Umwandlung. Im Allgemeinen können die einfachen Datentypen in komplexere Datentypen umgewandelt werden (mit einer herauf Stufungs Umwandlung), aber nur einige komplexe Datentypen können in einfache Datentypen umgewandelt werden (mit einer Herabstufung).

Nur die Typumwandlung auf der rechten Seite ist zulässig. Ausdrücke wie sind z. b `(int)myFloat = myInt;` . unzulässig. Verwenden Sie stattdessen `myFloat = (float)myInt;`.

Der Compiler führt außerdem eine implizite Typumwandlung aus. Die folgenden beiden Ausdrücke sind z. b. äquivalent:


```
int2 b = int2(1,2) + 2;
int2 b = int2(1,2) + int2(2,2);
```



## <a name="comma-operator"></a>Komma-Operator

Der Komma Operator (,) trennt mindestens einen Ausdruck, der in der Reihenfolge ausgewertet werden soll. Der Wert des letzten Ausdrucks in der Sequenz wird als Wert der Sequenz verwendet.

Im folgenden finden Sie einen Fall, auf den Sie achten sollten. Wenn der Konstruktortyp versehentlich von der rechten Seite des Gleichheitszeichens übrig bleibt, enthält die Rechte Seite nun vier Ausdrücke, die durch drei Kommas getrennt sind.


```
// Instead of using a constructor
float4 x = float4(0,0,0,1); 

// The type on the right side is accidentally left off
float4 x = (0,0,0,1); 
```



Der Komma-Operator wertet einen Ausdruck von links nach rechts aus. Dadurch wird die Rechte Seite auf reduziert:


```
float4 x = 1; 
```



HLSL verwendet in diesem Fall eine skalare herauf Stufung, sodass das Ergebnis so lautet, als wäre es wie folgt geschrieben:


```
float4 x = float4(1,1,1,1);
```



In diesem Fall ist es wahrscheinlich ein Fehler, dass der Compiler nicht erkennen kann, da es sich um eine gültige Anweisung handelt.

## <a name="comparison-operators"></a>Vergleichsoperatoren

Die Vergleichs Operatoren lauten wie folgt: <, >, = =,! =, <=, >=.

Vergleichen Sie Werte, die größer als (oder kleiner als) skalare Werte sind:


```
if( dot(lightDirection, normalVector) > 0 )
   // Do something; the face is lit
```




```
if( dot(lightDirection, normalVector) < 0 )
   // Do nothing; the face is backwards
```



Oder vergleichen Sie Werte, die mit einem beliebigen skalaren Wert identisch sind (oder nicht gleich):


```
if(color.a == 0)
   // Skip processing because the face is invisible

if(color.a != 0)
   // Blend two colors together using the alpha value
```



Oder kombinieren Sie Werte und vergleichen Sie Werte, die größer oder gleich (oder kleiner als oder gleich) einem beliebigen skalaren Wert sind:


```
if( position.z >= oldPosition.z )
   // Skip the new face because it is behind the existing face
```




```
if( currentValue <= someInitialCondition )
   // Reset the current value to its initial condition
```



Jeder dieser Vergleiche kann mit einem beliebigen skalaren Datentyp durchgeführt werden.

Verwenden Sie die [**all**](dx-graphics-hlsl-all.md) -oder [**any**](dx-graphics-hlsl-any.md) intrinsische Funktion, um Vergleichs Operatoren mit Vektor-und Matrix Typen zu verwenden.

Dieser Vorgang schlägt fehl, da die if-Anweisung einen einzelnen booleschen Werten erfordert, aber eine bool4 empfängt:


```
if (A4 < B4)
```



Diese Vorgänge sind erfolgreich:


```
if ( any(A4 < B4) )
if ( all(A4 < B4) )
```



## <a name="prefix-or-postfix-operators"></a>Präfix-oder Postfix Operatoren

Die Präfix-und Postfix Operatoren lauten wie folgt: + +,--. Präfix Operatoren ändern den Inhalt der Variablen, bevor der Ausdruck ausgewertet wird. Postfix-Operatoren ändern den Inhalt der Variablen, nachdem der Ausdruck ausgewertet wurde.

In diesem Fall verwendet eine-Schleife den Inhalt von i, um die Schleifen Anzahl nachzuverfolgen.


```
float4 arrayOfFloats[4] = { 1.0f, 2.0f, 3.0f, 4.4f };

for (int i = 0; i<4; )
{
    arrayOfFloats[i++] *= 2; 
}
```



Da der postfix-Inkrementoperator (+ +) verwendet wird, wird arrayoffloats \[ i \] mit 2 multipliziert, bevor ich inkrementiert wird. Dies könnte leicht neu angeordnet werden, um den Präfix-Inkrementoperator zu verwenden. Diese ist schwieriger zu lesen, obwohl beide Beispiele gleichwertig sind.


```
float4 arrayOfFloats[4] = { 1.0f, 2.0f, 3.0f, 4.4f };

for (int i = 0; i<4; )
{
    arrayOfFloats[++i - 1] *= 2; 
}
```



Da der prefix-Operator (+ +) verwendet wird, wird arrayoffloats \[ i + 1-1 \] mit 2 multipliziert, nachdem ich inkrementiert wurde.

Der Präfix Dekrement und postfix-Dekrementoperator (--) werden in derselben Reihenfolge wie der Inkrementoperator angewendet. Der Unterschied besteht darin, dass Dekrement 1 subtrahiert, anstatt 1 hinzuzufügen.

## <a name="structure-operator"></a>Structure-Operator

Der Strukturmember Selection-Operator (.) ist ein-Zeitraum. Bei dieser Struktur:


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



Jeder Member kann mit dem Struktur Operator gelesen oder geschrieben werden:


```
struct position pos = { 1,2,3 };
pos.x = 2.0f;
pos.z = 1.0f;       // z = 1.0f
pos.z = pos.x      // z = 2.0f
```



## <a name="unary-operators"></a>Unäre Operatoren

Die unären Operatoren lauten:!,-, +

Unäre Operatoren arbeiten für einen einzelnen Operanden.


```
bool b = false;
bool b2 = !b;      // b2 = true
int i = 2;
int i2 = -i;       // i2 = -2
int j = +i2;       // j = +2
```



## <a name="operator-precedence"></a>Operatorrangfolge

Wenn ein Ausdruck mehr als einen Operator enthält, bestimmt die Operator Rangfolge die Reihenfolge der Auswertung. Die Operator Rangfolge für HLSL folgt der gleichen Rangfolge wie C.

## <a name="remarks"></a>Bemerkungen

Geschweifte Klammern ( {,} ) starten und Beenden einen Anweisungsblock. Wenn ein Anweisungsblock eine einzelne Anweisung verwendet, sind die geschweiften Klammern optional.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anweisungen (DirectX HLSL)](dx-graphics-hlsl-statements.md)
</dt> </dl>

 

 




