---
title: Per-Component mathematische Vorgänge
description: Mit HLSL können Sie Shader auf Algorithmusebene programmieren.
ms.assetid: a919df50-2d13-489d-9011-1137c997e121
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5ff30cd19b7821c9a059251e105f6acfa9cf961e
ms.sourcegitcommit: fa5c081bf792b119a7bb92182cde1f85ca75967b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/17/2021
ms.locfileid: "104982820"
---
# <a name="per-component-math-operations"></a>Per-Component mathematische Vorgänge

Mit HLSL können Sie Shader auf Algorithmusebene programmieren. Um die Sprache zu verstehen, müssen Sie wissen, wie Sie Variablen und Funktionen deklarieren, systeminterne Funktionen verwenden, benutzerdefinierte Datentypen definieren und die Semantik verwenden, um shaderargumente mit anderen Shader und der Pipeline zu verbinden.

Nachdem Sie erfahren haben, wie Shader in HLSL erstellt werden, müssen Sie sich mit API-aufrufen vertraut machen, damit Sie: einen Shader für bestimmte Hardware kompilieren, shaderkonstanten initialisieren und ggf. anderen Pipeline Status initialisieren können.

-   [Der Vektortyp.](#the-vector-type)
-   [Der Matrix-Typ](#the-matrix-type)
    -   [Matrix Reihenfolge](#matrix-ordering)
-   [Beispiele](#examples)
-   [Zugehörige Themen](#related-topics)

## <a name="the-vector-type"></a>Der Vektortyp.

Ein Vektor ist eine Datenstruktur, die zwischen einer und vier Komponenten enthält.


```
bool    bVector;   // scalar containing 1 Boolean
bool1   bVector;   // vector containing 1 Boolean
int1    iVector;   // vector containing 1 int
float3  fVector;   // vector containing 3 floats
double4 dVector;   // vector containing 4 doubles
```



Die ganze Zahl, die unmittelbar auf den-Datentyp folgt, ist die Anzahl der Komponenten auf dem Vektor.

Initialisierer können auch in die Deklarationen eingeschlossen werden.


```
bool    bVector = false;
int1    iVector = 1;
float3  fVector = { 0.2f, 0.3f, 0.4f };
double4 dVector = { 0.2, 0.3, 0.4, 0.5 };
```



Alternativ kann der Vector Type verwendet werden, um dieselben Deklarationen zu erstellen:


```
vector <bool,   1> bVector = false;
vector <int,    1> iVector = 1;
vector <float,  3> fVector = { 0.2f, 0.3f, 0.4f };
vector <double, 4> dVector = { 0.2, 0.3, 0.4, 0.5 };
```



Der Vektortyp verwendet spitzen Klammern, um den Typ und die Anzahl der Komponenten anzugeben.

Vektoren enthalten bis zu vier Komponenten, auf die jeweils mit einem von zwei Benennungs Sätzen zugegriffen werden kann:

-   Der Positions Satz: x, y, z, w
-   Der Farbsatz: r, g, b, a

In diesen Anweisungen wird der Wert in der dritten Komponente zurückgegeben.


```
// Given
float4 pos = float4(0,0,2,1);

pos.z    // value is 2
pos.b    // value is 2
```



Benennungs Sätze können eine oder mehrere Komponenten verwenden, aber Sie können nicht gemischt werden.


```
// Given
float4 pos = float4(0,0,2,1);
float2 temp;

temp = pos.xy  // valid
temp = pos.rg  // valid

temp = pos.xg  // NOT VALID because the position and color sets were used.
```



Das Angeben einer oder mehrerer Vektor Komponenten beim Lesen von Komponenten wird als "swizzling" bezeichnet. Beispiel:


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



Zuweisungen können nicht mehrmals in dieselbe Komponente geschrieben werden. Die linke Seite dieser Anweisung ist daher ungültig:


```
f_4D.xx = pos.xy;   // cannot write to the same destination components 
```



Außerdem kann der Komponenten Namespaces nicht gemischt werden. Dies ist ein ungültiger Komponenten Schreibvorgang:


```
f_4D.xg = pos.rgrg;    // invalid write: cannot mix component name spaces 
```



Der Zugriff auf einen Vektor als Skalar erfolgt auf die erste Komponente des Vektors. Die folgenden zwei Anweisungen sind gleichwertig.


```
f_4D.a = pos * 5.0f;
f_4D.a = pos.r * 5.0f;
```



## <a name="the-matrix-type"></a>Der Matrix-Typ

Eine Matrix ist eine Datenstruktur, die Zeilen und Spalten mit Daten enthält. Bei den Daten kann es sich um einen beliebigen skalaren Datentypen handeln, aber jedes Element einer Matrix ist derselbe Datentyp. Die Anzahl der Zeilen und Spalten wird mit der zeilenweise Zeichenfolge angegeben, die an den Datentyp angehängt wird.


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

Eine Matrix kann beim Deklarieren initialisiert werden:


```
float2x2 fMatrix = { 0.0f, 0.1, // row 1
                     2.1f, 2.2f // row 2
                   };   
```



Oder der Matrix-Typ kann verwendet werden, um dieselben Deklarationen zu erstellen:


```
matrix <float, 2, 2> fMatrix = { 0.0f, 0.1, // row 1
                                 2.1f, 2.2f // row 2
                               };
```



Der Matrixtyp verwendet die spitzen Klammern, um den Typ, die Anzahl der Zeilen und die Anzahl der Spalten anzugeben. In diesem Beispiel wird eine Gleit Komma Matrix mit zwei Zeilen und zwei Spalten erstellt. Alle skalaren Datentypen können verwendet werden.

Diese Deklaration definiert eine Matrix von float-Werten (32-Bit-Gleit Komma Zahlen) mit zwei Zeilen und drei Spalten:


```
matrix <float, 2, 3> fFloatMatrix;
```



Eine Matrix enthält Werte, die in Zeilen und Spalten organisiert sind, auf die mit dem Structure-Operator "." gefolgt von einem von zwei Benennungs Sätzen zugegriffen werden kann:

-   Die null basierte Zeilen Spaltenposition:
    -   \_M00, \_ M01, \_ M02, \_ M03
    -   \_M10, \_ M11, \_ M12, \_ M13
    -   \_M20, \_ M21, \_ M22, \_ M23
    -   \_M30, \_ M31, \_ M32, \_ M33
-   Die einbasierte Zeilen Spaltenposition:
    -   \_11, \_ 12, \_ 13, \_ 14
    -   \_21, \_ 22, \_ 23, \_ 24
    -   \_31, \_ 32, \_ 33, \_ 34
    -   \_41, \_ 42, \_ 43, \_ 44

Jeder Benennungs Satz beginnt mit einem Unterstrich, gefolgt von der Zeilennummer und der Spaltennummer. Die null basierte Konvention enthält auch den Buchstaben "m" vor der Zeilen-und Spaltennummer. Im folgenden finden Sie ein Beispiel, das die beiden Benennungs Sätze verwendet, um auf eine Matrix zuzugreifen:


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



Ebenso wie Vektoren können Benennungs Sätze eine oder mehrere Komponenten aus einer der beiden Benennungs Sätze verwenden.


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



Auf eine Matrix kann auch mit der Array Zugriffs Notation zugegriffen werden, bei der es sich um einen NULL basierten Satz von Indizes handelt. Jeder Index befindet sich in eckigen Klammern. Der Zugriff auf eine 4X4-Matrix erfolgt mit den folgenden Indizes:

-   \[0 \] \[ 0 \] , \[ 0 \] \[ 1 \] , \[ 0 \] \[ 2 \] , \[ 0 \] \[ 3\]
-   \[1 \] \[ 0 \] , \[ 1 \] \[ 1 \] , \[ 1 \] \[ 2 \] , \[ 1 \] \[ 3\]
-   \[2 \] \[ 0,0 \] \[ \] \[ 1, 2 \] 2 \[ \] \[ \] , \[ 2 \] \[ 3\]
-   \[3 \] \[ 0,0 \] \[ \] \[ 1, 3 \] \[ \] \[ 2, 3 \] \[ \] \[ 3\]

Im folgenden finden Sie ein Beispiel für den Zugriff auf eine Matrix:


```
float2x2 fMatrix = { 1.0f, 1.1f, // row 1
                     2.0f, 2.1f  // row 2
                   };
float temp;

temp = fMatrix[0][0] // single component read
temp = fMatrix[0][1] // single component read
```



Beachten Sie, dass der Structure-Operator "." nicht verwendet wird, um auf ein Array zuzugreifen. Die Array Zugriffs Notation kann nicht zum Lesen von mehr als einer Komponente verwendet werden.


```
float2 temp;
temp = fMatrix[0][0]_[0][1] // invalid, cannot read two components
```



Allerdings kann der Array Zugriff einen Vektor mit mehreren Komponenten lesen.


```
float2 temp;
float2x2 fMatrix;
temp = fMatrix[0] // read the first row
```



Wie bei Vektoren wird das Lesen von mehr als einer Matrix Komponente als "swizzling" bezeichnet. Es können mehrere Komponenten zugewiesen werden, sofern nur ein Namespace verwendet wird. Dies sind alle gültigen Zuweisungen:


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



Zuweisungen können nicht mehrmals in dieselbe Komponente geschrieben werden. Die linke Seite dieser Anweisung ist daher ungültig:


```
// cannot write to the same component more than once
tempMatrix._m00_m00 = worldMatrix._m00_m11;
```



Außerdem kann der Komponenten Namespaces nicht gemischt werden. Dies ist ein ungültiger Komponenten Schreibvorgang:


```
// Invalid use of same component on left side
tempMatrix._11_m23 = worldMatrix._11_22; 
```



### <a name="matrix-ordering"></a>Matrix Reihenfolge

Die Matrix Verpackungs Reihenfolge für einheitliche Parameter ist standardmäßig auf Column-Major festgelegt. Dies bedeutet, dass jede Spalte der Matrix in einem einzelnen Konstanten Register gespeichert wird. Auf der anderen Seite verpackt eine Zeilen hauptmatrix jede Zeile der Matrix in einem einzelnen Konstanten Register. Die Matrix Verpackung kann mit der **\# pragmapack- \_ Matrix** Direktive oder mit dem Haupt Schlüsselwort der **Zeile \_** oder der **Spalte " \_ Major** " geändert werden.

Die Daten in einer Matrix werden vor dem Ausführen eines Shaders in Shader-Konstante Register geladen. Es gibt zwei Möglichkeiten, wie die Matrix Daten gelesen werden: in Zeilen Hauptreihen Folge oder in Spalten Hauptreihen Folge. Die Spalten-Haupt Reihenfolge bedeutet, dass jede Matrix Spalte in einem einzelnen Konstanten Register gespeichert wird, und die Reihenfolge von Zeilen ist, dass jede Zeile der Matrix in einem einzigen konstanten Register gespeichert wird. Dies ist ein wichtiger Aspekt, wie viele Konstante Register für eine Matrix verwendet werden.

Eine Zeilen hauptmatrix wird wie folgt angeordnet:



|     |     |     |     |
|-----|-----|-----|-----|
| 11  | 12  | 13  | 14  |
| 21  | 22  | 23  | 24  |
| 31  | 32  | 33  | 34  |
| 41  | 42  | 43  | 44  |



 

Eine Spalten hauptmatrix wird wie folgt angeordnet:



|     |     |     |     |
|-----|-----|-----|-----|
| 11  | 21  | 31  | 41  |
| 12  | 22  | 32  | 42  |
| 13  | 23  | 33  | 43  |
| 14  | 24  | 34  | 44  |



 

Zeilen-Haupt-und Spalten hauptmatrizen Reihenfolge bestimmt die Reihenfolge, in der die Matrixkomponenten aus shadereingaben gelesen werden. Nachdem die Daten in Konstante Register geschrieben wurden, wirkt sich die Reihenfolge der Matrizen nicht darauf aus, wie die Daten im Shader-Code verwendet oder aufgerufen werden. Außerdem werden in einem shadertext deklarierte Matrizen nicht in Konstante Register gepackt. Die Reihenfolge der Zeilen-Haupt-und Spalten hauptverpackung hat keinen Einfluss auf die Komprimierungs Reihenfolge von Konstruktoren (die immer auf die Reihenfolge der Zeilen Hauptreihen folgen).

Die Reihenfolge der Daten in einer Matrix kann zur Kompilierzeit deklariert werden, oder der Compiler sortiert die Daten zur Laufzeit, um die effizienteste Verwendung zu erreichen.

## <a name="examples"></a>Beispiele

HLSL verwendet zwei spezielle Typen, einen Vektortyp und einen Matrixtyp, um die Programmierung von 2D-und 3D-Grafiken zu vereinfachen. Jeder dieser Typen enthält mehr als eine Komponente. ein Vektor enthält bis zu vier Komponenten, und eine Matrix enthält bis zu 16 Komponenten. Wenn Vektoren und Matrizen in standardmäßigen HLSL-Gleichungen verwendet werden, ist die durchgeführte Mathematik so konzipiert, dass Sie pro Komponente funktioniert. Beispielsweise implementiert HLSL diese Multiplikation:


```
float4 v = a*b;
```



als eine Multiplikation mit vier Komponenten. Das Ergebnis sind vier skalare:


```
float4 v = a*b;

v.x = a.x*b.x;
v.y = a.y*b.y;
v.z = a.z*b.z;
v.w = a.w*b.w;
```



Dies sind vier Multiplikationen, bei denen jedes Ergebnis in einer separaten Komponente von v gespeichert wird. Dies wird als vier-Komponenten-Multiplikation bezeichnet. HLSL verwendet die Komponente math, wodurch das Schreiben von Shader sehr effizient wird.

Dies unterscheidet sich sehr von einem multiplizieren, das in der Regel als ein Punktprodukt implementiert wird, das einen einzelnen Skalarwert generiert:


```
v = a.x*b.x + a.y*b.y + a.z*b.z + a.w*b.w;
```



Eine Matrix verwendet in HLSL auch Vorgänge pro Komponente:


```
float3x3 mat1,mat2;
...
float3x3 mat3 = mat1*mat2;
```



Das Ergebnis ist eine Multiplikation der beiden Matrizen pro Komponente (im Gegensatz zu einer standardmäßigen 3X3-Matrix Multiplikation). Eine Matrix Multiplikation pro Komponente ergibt diesen ersten Begriff:


```
mat3.m00 = mat1.m00 * mat2._m00;
```



Dies unterscheidet sich von einer 3X3-Matrix Multiplikation, die diesen ersten Begriff ergibt:


```
// First component of a four-component matrix multiply
mat.m00 = mat1._m00 * mat2._m00 + 
          mat1._m01 * mat2._m10 + 
          mat1._m02 * mat2._m20 + 
          mat1._m03 * mat2._m30;
```



Überladene Versionen der intrinsischen Funktion zum Multiplizieren von Funktionen, bei denen ein-Operand ein Vektor und der andere Operand eine Matrix ist. Beispielsweise: Vektor \* Vektor, Vektor \* Matrix, Matrix \* Vektor und Matrix \* Matrix. Beispiel:


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



In diesem Beispiel wird der POS-Vektor mithilfe der Umwandlung (float1x4) in einen Spalten Vektor umgewandelt. Das Ändern eines Vektors durch umwandeln oder Austauschen der Reihenfolge der zu multiplizierenden Argumente entspricht der Umsetzung der Matrix.

Die automatische Umwandlung von Umwandlungen bewirkt, dass die intrinsischen Funktionen multiplizieren und Punkt dieselben Ergebnisse wie hier verwendet zurückgeben:


```
{
  float4 val;
  return mul(val,val);
}
```



Das Ergebnis der Multiplikation ist ein 1 x 4 \* 4 x 1 = 1x1-Vektor. Dies entspricht einem Punktprodukt:


```
{
  float4 val;
  return dot(val,val);
}
```



, der einen einzelnen Skalarwert zurückgibt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Datentypen (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 




