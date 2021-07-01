---
title: Per-Component Mathematische Operationen
description: Mit HLSL können Sie Shader auf Algorithmusebene programmieren.
ms.assetid: a919df50-2d13-489d-9011-1137c997e121
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2c8c9eeea1072c53915588ac0099998e76c0452a
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119595"
---
# <a name="per-component-math-operations"></a>Per-Component Mathematische Operationen

Mit HLSL können Sie Shader auf Algorithmusebene programmieren. Um die Sprache zu verstehen, müssen Sie wissen, wie Sie Variablen und Funktionen deklarieren, systeminterne Funktionen verwenden, benutzerdefinierte Datentypen definieren und Semantik verwenden, um Shaderargumente mit anderen Shadern und mit der Pipeline zu verbinden.

Nachdem Sie erfahren haben, wie Sie Shader in HLSL erstellen, müssen Sie sich mit API-Aufrufen informieren, damit Sie einen Shader für bestimmte Hardware kompilieren, Shaderkonstatoren initialisieren und bei Bedarf einen anderen Pipelinezustand initialisieren können.

-   [Der Vektortyp](#the-vector-type)
-   [Der Matrixtyp](#the-matrix-type)
    -   [Matrix reihenfolge](#matrix-ordering)
-   [Beispiele](#examples)
-   [Verwandte Themen](#related-topics)

## <a name="the-vector-type"></a>Der Vektortyp

Ein Vektor ist eine Datenstruktur, die zwischen einer und vier Komponenten enthält.


```
bool    bVector;   // scalar containing 1 Boolean
bool1   bVector;   // vector containing 1 Boolean
int1    iVector;   // vector containing 1 int
float3  fVector;   // vector containing 3 floats
double4 dVector;   // vector containing 4 doubles
```



Die ganze Zahl, die unmittelbar auf den Datentyp folgt, ist die Anzahl der Komponenten im Vektor.

Initialisierer können auch in die Deklarationen eingeschlossen werden.


```
bool    bVector = false;
int1    iVector = 1;
float3  fVector = { 0.2f, 0.3f, 0.4f };
double4 dVector = { 0.2, 0.3, 0.4, 0.5 };
```



Alternativ kann der Vektortyp verwendet werden, um die gleichen Deklarationen zu machen:


```
vector <bool,   1> bVector = false;
vector <int,    1> iVector = 1;
vector <float,  3> fVector = { 0.2f, 0.3f, 0.4f };
vector <double, 4> dVector = { 0.2, 0.3, 0.4, 0.5 };
```



Der Vektortyp verwendet eckige Klammern, um den Typ und die Anzahl der Komponenten anzugeben.

Vektoren enthalten bis zu vier Komponenten, auf die jeweils mit einem von zwei Benennungssätzen zugegriffen werden kann:

-   Der Positionssatz: x,y,z,w
-   Der Farbsatz: r,g,b,a

Beide Anweisungen geben den Wert in der dritten Komponente zurück.


```
// Given
float4 pos = float4(0,0,2,1);

pos.z    // value is 2
pos.b    // value is 2
```



Benennungssätze können eine oder mehrere Komponenten verwenden, sie können jedoch nicht gemischt werden.


```
// Given
float4 pos = float4(0,0,2,1);
float2 temp;

temp = pos.xy  // valid
temp = pos.rg  // valid

temp = pos.xg  // NOT VALID because the position and color sets were used.
```



Das Angeben einer oder mehrere Vektorkomponenten beim Lesen von Komponenten wird als Swizzling bezeichnet. Beispiel:


```
float4 pos = float4(0,0,2,1);
float2 f_2D;
f_2D = pos.xy;   // read two components 
f_2D = pos.xz;   // read components in any order       
f_2D = pos.zx;

f_2D = pos.xx;   // components can be read more than once
f_2D = pos.yy;
```



Die Maskierung steuert, wie viele Komponenten geschrieben werden.


```
float4 pos = float4(0,0,2,1);
float4 f_4D;
f_4D    = pos;     // write four components          

f_4D.xz = pos.xz;  // write two components        
f_4D.zx = pos.xz;  // change the write order

f_4D.xzyw = pos.w; // write one component to more than one component
f_4D.wzyx = pos;
```



Zuweisungen können nicht mehr als einmal in dieselbe Komponente geschrieben werden. Daher ist die linke Seite dieser Anweisung ungültig:


```
f_4D.xx = pos.xy;   // cannot write to the same destination components 
```



Außerdem können die Komponentennamensräume nicht gemischt werden. Dies ist ein ungültiger Komponenten-Schreibzugriff:


```
f_4D.xg = pos.rgrg;    // invalid write: cannot mix component name spaces 
```



Der Zugriff auf einen Vektor als Skalarzugriff auf die erste Komponente des Vektors. Die folgenden beiden Anweisungen sind gleichwertig.


```
f_4D.a = pos * 5.0f;
f_4D.a = pos.r * 5.0f;
```



## <a name="the-matrix-type"></a>Der Matrixtyp

Eine Matrix ist eine Datenstruktur, die Datenzeilen und -spalten enthält. Die Daten können alle skalaren Datentypen sein, aber jedes Element einer Matrix ist derselbe Datentyp. Die Anzahl der Zeilen und Spalten wird mit der Zeilen-für-Spalte-Zeichenfolge angegeben, die an den Datentyp angefügt wird.


```
int1x1    iMatrix;   // integer matrix with 1 row,  1 column
int2x1    iMatrix;   // integer matrix with 2 rows, 1 column
...
int4x1    iMatrix;   // integer matrix with 4 rows, 1 column
...
int1x4    iMatrix;   // integer matrix with 1 row, 4 columns
double1x1 dMatrix;   // double matrix with 1 row,  1 column
double2x2 dMatrix;   // double matrix with 2 rows, 2 columns
double3x3 dMatrix;   // double matrix with 3 rows, 3 columns
double4x4 dMatrix;   // double matrix with 4 rows, 4 columns
```



Die maximale Anzahl von Zeilen oder Spalten ist 4. die Mindestanzahl ist 1.

Eine Matrix kann initialisiert werden, wenn sie deklariert wird:


```
float2x2 fMatrix = { 0.0f, 0.1, // row 1
                     2.1f, 2.2f // row 2
                   };   
```



Oder der Matrixtyp kann verwendet werden, um die gleichen Deklarationen zu erstellen:


```
matrix <float, 2, 2> fMatrix = { 0.0f, 0.1, // row 1
                                 2.1f, 2.2f // row 2
                               };
```



Der Matrixtyp verwendet die eckigen Klammern, um den Typ, die Anzahl der Zeilen und die Anzahl der Spalten anzugeben. In diesem Beispiel wird eine Gleitkommamatrix mit zwei Zeilen und zwei Spalten erstellt. Jeder der skalaren Datentypen kann verwendet werden.

Diese Deklaration definiert eine Matrix von Gleitkommawerten (32-Bit-Gleitkommazahlen) mit zwei Zeilen und drei Spalten:


```
matrix <float, 2, 3> fFloatMatrix;
```



Eine Matrix enthält In Zeilen und Spalten angeordnete Werte, auf die mithilfe des Strukturoperator "." gefolgt von einem von zwei Benennungssätzen zugegriffen werden kann:

-   Die nullbasierte Zeilenspaltenposition:
    -   \_m00, \_ m01, \_ m02, \_ m03
    -   \_m10, \_ m11, \_ m12, \_ m13
    -   \_m20, \_ m21, \_ m22, \_ m23
    -   \_m30, \_ m31, \_ m32, \_ m33
-   Die 1-basierte Zeilenspaltenposition:
    -   \_11, \_ 12, \_ 13, \_ 14
    -   \_21, \_ 22, \_ 23, \_ 24
    -   \_31, \_ 32, \_ 33, \_ 34
    -   \_41, \_ 42, \_ 43, \_ 44

Jeder Benennungssatz beginnt mit einem Unterstrich, gefolgt von der Zeilennummer und der Spaltennummer. Die nullbasierte Konvention enthält auch den Buchstaben "m" vor der Zeile und Spaltennummer. Hier ist ein Beispiel, in dem die beiden Benennungssätze für den Zugriff auf eine Matrix verwendet werden:


```
// given
float2x2 fMatrix = { 1.0f, 1.1f, // row 1
                     2.0f, 2.1f  // row 2
                   }; 

float f_1D;
f_1D = matrix._m00; // read the value in row 1, column 1: 1.0
f_1D = matrix._m11; // read the value in row 2, column 2: 2.1

f_1D = matrix._11;  // read the value in row 1, column 1: 1.0
f_1D = matrix._22;  // read the value in row 2, column 2: 2.1
```



Genau wie Vektoren können Benennungssätze eine oder mehrere Komponenten aus beiden Benennungssätzen verwenden.


```
// Given
float2x2 fMatrix = { 1.0f, 1.1f, // row 1
                     2.0f, 2.1f  // row 2
                   };
float2 temp;

temp = fMatrix._m00_m11 // valid
temp = fMatrix._m11_m00 // valid
temp = fMatrix._11_22   // valid
temp = fMatrix._22_11   // valid
```



Auf eine Matrix kann auch mithilfe der Arrayzugriffs-Notation zugegriffen werden, bei der es sich um einen nullbasierten Satz von Indizes handelt. Jeder Index befindet sich in eckigen Klammern. Auf eine 4x4-Matrix wird mit den folgenden Indizes zugegriffen:

-   \[0 \] \[ 0 \] , \[ 0 \] \[ 1 \] , \[ 0 \] \[ 2 \] , \[ 0 \] \[ 3\]
-   \[1 \] \[ \] 0, \[ 1 \] \[ \] 1, \[ 1 \] \[ \] 2, \[ 1 \] \[ 3\]
-   \[2 \] \[ \] 0, \[ 2 \] \[ \] 1, \[ 2 \] \[ \] 2, \[ 2 \] \[ 3\]
-   \[3 \] \[ \] 0, \[ 3 \] \[ \] 1, \[ 3 \] \[ \] 2, \[ 3 \] \[ 3\]

Hier ist ein Beispiel für den Zugriff auf eine Matrix:


```
float2x2 fMatrix = { 1.0f, 1.1f, // row 1
                     2.0f, 2.1f  // row 2
                   };
float temp;

temp = fMatrix[0][0] // single component read
temp = fMatrix[0][1] // single component read
```



Beachten Sie, dass der Strukturoperator "." nicht für den Zugriff auf ein Array verwendet wird. Die Arrayzugriffs-Notation kann nicht swizzling verwenden, um mehr als eine Komponente zu lesen.


```
float2 temp;
temp = fMatrix[0][0]_[0][1] // invalid, cannot read two components
```



Der Arrayzugriff kann jedoch einen Vektor mit mehreren Komponenten lesen.


```
float2 temp;
float2x2 fMatrix;
temp = fMatrix[0] // read the first row
```



Wie bei Vektoren wird das Lesen von mehr als einer Matrixkomponente als Swizzling bezeichnet. Es können mehrere Komponenten zugewiesen werden, vorausgesetzt, es wird nur ein Namensraum verwendet. Dies sind alle gültige Zuweisungen:


```
// Given these variables
float4x4 worldMatrix = float4( {0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} );
float4x4 tempMatrix;

tempMatrix._m00_m11 = worldMatrix._m00_m11; // multiple components
tempMatrix._m00_m11 = worldMatrix.m13_m23;

tempMatrix._11_22_33 = worldMatrix._11_22_33; // any order on swizzles
tempMatrix._11_22_33 = worldMatrix._24_23_22;
```



Die Maskierung steuert, wie viele Komponenten geschrieben werden.


```
// Given
float4x4 worldMatrix = float4( {0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} );
float4x4 tempMatrix;

tempMatrix._m00_m11 = worldMatrix._m00_m11; // write two components
tempMatrix._m23_m00 = worldMatrix._m00_m11;
```



Zuweisungen können nicht mehr als einmal in dieselbe Komponente geschrieben werden. Daher ist die linke Seite dieser Anweisung ungültig:


```
// cannot write to the same component more than once
tempMatrix._m00_m00 = worldMatrix._m00_m11;
```



Außerdem können die Komponentennamensräume nicht gemischt werden. Dies ist ein ungültiger Komponenten-Schreibzugriff:


```
// Invalid use of same component on left side
tempMatrix._11_m23 = worldMatrix._11_22; 
```



### <a name="matrix-ordering"></a>Matrix reihenfolge

Die Matrixpackungsauftrag für einheitliche Parameter ist standardmäßig auf Spaltenmatrizen festgelegt. Dies bedeutet, dass jede Spalte der Matrix in einem einzelnen Konstantenregister gespeichert wird. Andererseits packt eine Zeilen-Hauptmatrix jede Zeile der Matrix in einem einzelnen Konstantenregister. Die Matrixpackung kann mit der **\# pragmapack-Matrix-Direktive \_** oder mit der **\_ Zeilen-Hauptzeile** oder dem **Schlüsselwort column major \_ geändert** werden.

Die Daten in einer Matrix werden in Shader-Konstantenregister geladen, bevor ein Shader ausgeführt wird. Es gibt zwei Möglichkeiten, wie die Matrixdaten gelesen werden: in Zeilen-Hauptreihen- oder Spalten-Hauptreihen reihenfolge. Die Spaltenordnung bedeutet, dass jede Matrixspalte in einem einzelnen konstanten Register gespeichert wird, und zeilenbasierte Reihenfolge bedeutet, dass jede Zeile der Matrix in einem einzelnen konstanten Register gespeichert wird. Dies ist ein wichtiger Aspekt bei der Verwendung von konstanten Registern für eine Matrix.

Eine Zeilenmatrizenmatrix ist wie folgt angelegt:

:::row:::
    :::column:::
        11<br/>
        21<br/>
        31<br/>
        41<br/>
    :::column-end:::
    :::column:::
        12<br/>
        22<br/>
        32<br/>
        42<br/>
    :::column-end:::
    :::column:::
        13<br/>
        23<br/>
        33<br/>
        43<br/>
    :::column-end:::
    :::column:::
        14<br/>
        24<br/>
        34<br/>
        44<br/>
    :::column-end:::
:::row-end:::




 

Eine Spaltenmatrizenmatrix ist wie folgt angelegt:


:::row:::
    :::column:::
        11<br/>
        12<br/>
        13<br/>
        14<br/>
    :::column-end:::
    :::column:::
        21<br/>
        22<br/>
        23<br/>
        24<br/>
    :::column-end:::
    :::column:::
        31<br/>
        32<br/>
        33<br/>
        34<br/>
    :::column-end:::
    :::column:::
        14<br/>
        24<br/>
        34<br/>
        44<br/>
    :::column-end:::
:::row-end:::




 

Die Reihenfolge der Zeilen- und Spaltenmatrizen bestimmt die Reihenfolge, in der die Matrixkomponenten aus Shadereingaben gelesen werden. Sobald die Daten in konstante Register geschrieben wurden, hat die Matrix reihenfolge keine Auswirkungen darauf, wie die Daten innerhalb des Shadercodes verwendet oder darauf zugegriffen wird. Außerdem werden Matrizen, die in einem Shader-Text deklariert sind, nicht in konstanten Registern gepackt. Die Zeilen- und Spalten-Hauptpackungsreihen reihenfolge hat keinen Einfluss auf die Füllreihen reihenfolge von Konstruktoren (die immer der Zeilenordnung folgt).

Die Reihenfolge der Daten in einer Matrix kann zur Kompilierzeit deklariert werden, oder der Compiler ordnet die Daten zur Laufzeit für die effizienteste Verwendung an.

## <a name="examples"></a>Beispiele

HLSL verwendet zwei spezielle Typen, einen Vektortyp und einen Matrixtyp, um die Programmierung von 2D- und 3D-Grafiken zu vereinfachen. Jeder dieser Typen enthält mehr als eine Komponente. ein Vektor enthält bis zu vier Komponenten, und eine Matrix enthält bis zu 16 Komponenten. Wenn Vektoren und Matrizen in HLSL-Standardgleichungen verwendet werden, ist die durchgeführte Mathematik so konzipiert, dass sie pro Komponente funktioniert. HLSL implementiert beispielsweise diese Multiplikation:


```
float4 v = a*b;
```



als Multiplikation mit vier Komponenten. Das Ergebnis sind vier Skalar:


```
float4 v = a*b;

v.x = a.x*b.x;
v.y = a.y*b.y;
v.z = a.z*b.z;
v.w = a.w*b.w;
```



Dies sind vier Multiplikationen, bei denen jedes Ergebnis in einer separaten Komponente von v gespeichert wird. Dies wird als Multiplikation mit vier Komponenten bezeichnet. HLSL verwendet Dies macht das Schreiben von Shadern sehr effizient.

Dies ist sehr anders als eine Multiplikation, die in der Regel als Punktprodukt implementiert wird, das einen einzelnen Skalar generiert:


```
v = a.x*b.x + a.y*b.y + a.z*b.z + a.w*b.w;
```



Eine Matrix verwendet auch Vorgänge pro Komponente in HLSL:


```
float3x3 mat1,mat2;
...
float3x3 mat3 = mat1*mat2;
```



Das Ergebnis ist eine Multiplikation der beiden Matrizen pro Komponente (im Gegensatz zu einer standardmäßigen 3x3-Matrixmultiplikation). Eine Multiplikation pro Komponentenmatrix ergibt diesen ersten Begriff:


```
mat3.m00 = mat1.m00 * mat2._m00;
```



Dies ist anders als bei einer 3x3-Matrixmultiplikation, die diesen ersten Begriff ergeben würde:


```
// First component of a four-component matrix multiply
mat.m00 = mat1._m00 * mat2._m00 + 
          mat1._m01 * mat2._m10 + 
          mat1._m02 * mat2._m20 + 
          mat1._m03 * mat2._m30;
```



Überladene Versionen der multiplizierten systeminternen Funktion behandeln Fälle, in denen ein Operand ein Vektor und der andere Operand eine Matrix ist. Beispiel: \* Vektorvektor, \* Vektormatrix, \* Matrixvektor und \* Matrixmatrix. Beispiel:


```
float4x3 World;

float4 main(float4 pos : SV_POSITION) : SV_POSITION
{
    float4 val;
    val.xyz = mul(pos,World);
    val.w = 0;

    return val;
}   
```



erzeugt das gleiche Ergebnis wie:


```
float4x3 World;

float4 main(float4 pos : SV_POSITION) : SV_POSITION
{
    float4 val;
    val.xyz = (float3) mul((float1x4)pos,World);
    val.w = 0;

    return val;
}   
```



In diesem Beispiel wird der Pos-Vektor mithilfe der (float1x4)-Cast in einen Spaltenvektor umformatiert. Das Ändern eines Vektors durch Umwandlung oder das Austauschen der Reihenfolge der argumente, die zum Multiplizieren angegeben werden, entspricht dem Transpos der Matrix.

Die automatische Umwandlungskonvertierung bewirkt, dass die systeminternen Funktionen multiply und dot die gleichen Ergebnisse zurückgeben wie hier verwendet:


```
{
  float4 val;
  return mul(val,val);
}
```



Dieses Ergebnis der Multiplikation ist ein 1x4 \* 4x1 = 1x1-Vektor. Dies entspricht einem Punktprodukt:


```
{
  float4 val;
  return dot(val,val);
}
```



, die einen einzelnen Skalarwert zurückgibt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Datentypen (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 




