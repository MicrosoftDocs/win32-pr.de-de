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
# <a name="per-component-math-operations"></a><span data-ttu-id="1b686-103">Per-Component Mathematische Operationen</span><span class="sxs-lookup"><span data-stu-id="1b686-103">Per-Component Math Operations</span></span>

<span data-ttu-id="1b686-104">Mit HLSL können Sie Shader auf Algorithmusebene programmieren.</span><span class="sxs-lookup"><span data-stu-id="1b686-104">With HLSL, you can program shaders at an algorithm level.</span></span> <span data-ttu-id="1b686-105">Um die Sprache zu verstehen, müssen Sie wissen, wie Sie Variablen und Funktionen deklarieren, systeminterne Funktionen verwenden, benutzerdefinierte Datentypen definieren und Semantik verwenden, um Shaderargumente mit anderen Shadern und mit der Pipeline zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="1b686-105">To understand the language, you will need to know how to declare variables and functions, use intrinsic functions, define custom data types and use semantics to connect shader arguments to other shaders and to the pipeline.</span></span>

<span data-ttu-id="1b686-106">Nachdem Sie erfahren haben, wie Sie Shader in HLSL erstellen, müssen Sie sich mit API-Aufrufen informieren, damit Sie einen Shader für bestimmte Hardware kompilieren, Shaderkonstatoren initialisieren und bei Bedarf einen anderen Pipelinezustand initialisieren können.</span><span class="sxs-lookup"><span data-stu-id="1b686-106">Once you learn how to author shaders in HLSL, you will need to learn about API calls so that you can: compile a shader for particular hardware, initialize shader constants, and initialize other pipeline state if necessary.</span></span>

-   [<span data-ttu-id="1b686-107">Der Vektortyp</span><span class="sxs-lookup"><span data-stu-id="1b686-107">The Vector Type</span></span>](#the-vector-type)
-   [<span data-ttu-id="1b686-108">Der Matrixtyp</span><span class="sxs-lookup"><span data-stu-id="1b686-108">The Matrix Type</span></span>](#the-matrix-type)
    -   [<span data-ttu-id="1b686-109">Matrix reihenfolge</span><span class="sxs-lookup"><span data-stu-id="1b686-109">Matrix Ordering</span></span>](#matrix-ordering)
-   [<span data-ttu-id="1b686-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1b686-110">Examples</span></span>](#examples)
-   [<span data-ttu-id="1b686-111">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="1b686-111">Related topics</span></span>](#related-topics)

## <a name="the-vector-type"></a><span data-ttu-id="1b686-112">Der Vektortyp</span><span class="sxs-lookup"><span data-stu-id="1b686-112">The Vector Type</span></span>

<span data-ttu-id="1b686-113">Ein Vektor ist eine Datenstruktur, die zwischen einer und vier Komponenten enthält.</span><span class="sxs-lookup"><span data-stu-id="1b686-113">A vector is a data structure that contains between one and four components.</span></span>


```
bool    bVector;   // scalar containing 1 Boolean
bool1   bVector;   // vector containing 1 Boolean
int1    iVector;   // vector containing 1 int
float3  fVector;   // vector containing 3 floats
double4 dVector;   // vector containing 4 doubles
```



<span data-ttu-id="1b686-114">Die ganze Zahl, die unmittelbar auf den Datentyp folgt, ist die Anzahl der Komponenten im Vektor.</span><span class="sxs-lookup"><span data-stu-id="1b686-114">The integer immediately following the data type is the number of components on the vector.</span></span>

<span data-ttu-id="1b686-115">Initialisierer können auch in die Deklarationen eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="1b686-115">Initializers can also be included in the declarations.</span></span>


```
bool    bVector = false;
int1    iVector = 1;
float3  fVector = { 0.2f, 0.3f, 0.4f };
double4 dVector = { 0.2, 0.3, 0.4, 0.5 };
```



<span data-ttu-id="1b686-116">Alternativ kann der Vektortyp verwendet werden, um die gleichen Deklarationen zu machen:</span><span class="sxs-lookup"><span data-stu-id="1b686-116">Alternatively, the vector type can be used to make the same declarations:</span></span>


```
vector <bool,   1> bVector = false;
vector <int,    1> iVector = 1;
vector <float,  3> fVector = { 0.2f, 0.3f, 0.4f };
vector <double, 4> dVector = { 0.2, 0.3, 0.4, 0.5 };
```



<span data-ttu-id="1b686-117">Der Vektortyp verwendet eckige Klammern, um den Typ und die Anzahl der Komponenten anzugeben.</span><span class="sxs-lookup"><span data-stu-id="1b686-117">The vector type uses angle brackets to specify the type and number of components.</span></span>

<span data-ttu-id="1b686-118">Vektoren enthalten bis zu vier Komponenten, auf die jeweils mit einem von zwei Benennungssätzen zugegriffen werden kann:</span><span class="sxs-lookup"><span data-stu-id="1b686-118">Vectors contain up to four components, each of which can be accessed using one of two naming sets:</span></span>

-   <span data-ttu-id="1b686-119">Der Positionssatz: x,y,z,w</span><span class="sxs-lookup"><span data-stu-id="1b686-119">The position set: x,y,z,w</span></span>
-   <span data-ttu-id="1b686-120">Der Farbsatz: r,g,b,a</span><span class="sxs-lookup"><span data-stu-id="1b686-120">The color set: r,g,b,a</span></span>

<span data-ttu-id="1b686-121">Beide Anweisungen geben den Wert in der dritten Komponente zurück.</span><span class="sxs-lookup"><span data-stu-id="1b686-121">These statements both return the value in the third component.</span></span>


```
// Given
float4 pos = float4(0,0,2,1);

pos.z    // value is 2
pos.b    // value is 2
```



<span data-ttu-id="1b686-122">Benennungssätze können eine oder mehrere Komponenten verwenden, sie können jedoch nicht gemischt werden.</span><span class="sxs-lookup"><span data-stu-id="1b686-122">Naming sets can use one or more components, but they cannot be mixed.</span></span>


```
// Given
float4 pos = float4(0,0,2,1);
float2 temp;

temp = pos.xy  // valid
temp = pos.rg  // valid

temp = pos.xg  // NOT VALID because the position and color sets were used.
```



<span data-ttu-id="1b686-123">Das Angeben einer oder mehrere Vektorkomponenten beim Lesen von Komponenten wird als Swizzling bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="1b686-123">Specifying one or more vector components when reading components is called swizzling.</span></span> <span data-ttu-id="1b686-124">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="1b686-124">For example:</span></span>


```
float4 pos = float4(0,0,2,1);
float2 f_2D;
f_2D = pos.xy;   // read two components 
f_2D = pos.xz;   // read components in any order       
f_2D = pos.zx;

f_2D = pos.xx;   // components can be read more than once
f_2D = pos.yy;
```



<span data-ttu-id="1b686-125">Die Maskierung steuert, wie viele Komponenten geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="1b686-125">Masking controls how many components are written.</span></span>


```
float4 pos = float4(0,0,2,1);
float4 f_4D;
f_4D    = pos;     // write four components          

f_4D.xz = pos.xz;  // write two components        
f_4D.zx = pos.xz;  // change the write order

f_4D.xzyw = pos.w; // write one component to more than one component
f_4D.wzyx = pos;
```



<span data-ttu-id="1b686-126">Zuweisungen können nicht mehr als einmal in dieselbe Komponente geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="1b686-126">Assignments cannot be written to the same component more than once.</span></span> <span data-ttu-id="1b686-127">Daher ist die linke Seite dieser Anweisung ungültig:</span><span class="sxs-lookup"><span data-stu-id="1b686-127">So the left side of this statement is invalid:</span></span>


```
f_4D.xx = pos.xy;   // cannot write to the same destination components 
```



<span data-ttu-id="1b686-128">Außerdem können die Komponentennamensräume nicht gemischt werden.</span><span class="sxs-lookup"><span data-stu-id="1b686-128">Also, the component name spaces cannot be mixed.</span></span> <span data-ttu-id="1b686-129">Dies ist ein ungültiger Komponenten-Schreibzugriff:</span><span class="sxs-lookup"><span data-stu-id="1b686-129">This is an invalid component write:</span></span>


```
f_4D.xg = pos.rgrg;    // invalid write: cannot mix component name spaces 
```



<span data-ttu-id="1b686-130">Der Zugriff auf einen Vektor als Skalarzugriff auf die erste Komponente des Vektors.</span><span class="sxs-lookup"><span data-stu-id="1b686-130">Accessing a vector as a scalar will access the first component of the vector.</span></span> <span data-ttu-id="1b686-131">Die folgenden beiden Anweisungen sind gleichwertig.</span><span class="sxs-lookup"><span data-stu-id="1b686-131">The following two statements are equivalent.</span></span>


```
f_4D.a = pos * 5.0f;
f_4D.a = pos.r * 5.0f;
```



## <a name="the-matrix-type"></a><span data-ttu-id="1b686-132">Der Matrixtyp</span><span class="sxs-lookup"><span data-stu-id="1b686-132">The Matrix Type</span></span>

<span data-ttu-id="1b686-133">Eine Matrix ist eine Datenstruktur, die Datenzeilen und -spalten enthält.</span><span class="sxs-lookup"><span data-stu-id="1b686-133">A matrix is a data structure that contains rows and columns of data.</span></span> <span data-ttu-id="1b686-134">Die Daten können alle skalaren Datentypen sein, aber jedes Element einer Matrix ist derselbe Datentyp.</span><span class="sxs-lookup"><span data-stu-id="1b686-134">The data can be any of the scalar data types, however, every element of a matrix is the same data type.</span></span> <span data-ttu-id="1b686-135">Die Anzahl der Zeilen und Spalten wird mit der Zeilen-für-Spalte-Zeichenfolge angegeben, die an den Datentyp angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="1b686-135">The number of rows and columns is specified with the row-by-column string that is appended to the data type.</span></span>


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



<span data-ttu-id="1b686-136">Die maximale Anzahl von Zeilen oder Spalten ist 4. die Mindestanzahl ist 1.</span><span class="sxs-lookup"><span data-stu-id="1b686-136">The maximum number of rows or columns is 4; the minimum number is 1.</span></span>

<span data-ttu-id="1b686-137">Eine Matrix kann initialisiert werden, wenn sie deklariert wird:</span><span class="sxs-lookup"><span data-stu-id="1b686-137">A matrix can be initialized when it is declared:</span></span>


```
float2x2 fMatrix = { 0.0f, 0.1, // row 1
                     2.1f, 2.2f // row 2
                   };   
```



<span data-ttu-id="1b686-138">Oder der Matrixtyp kann verwendet werden, um die gleichen Deklarationen zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="1b686-138">Or, the matrix type can be used to make the same declarations:</span></span>


```
matrix <float, 2, 2> fMatrix = { 0.0f, 0.1, // row 1
                                 2.1f, 2.2f // row 2
                               };
```



<span data-ttu-id="1b686-139">Der Matrixtyp verwendet die eckigen Klammern, um den Typ, die Anzahl der Zeilen und die Anzahl der Spalten anzugeben.</span><span class="sxs-lookup"><span data-stu-id="1b686-139">The matrix type uses the angle brackets to specify the type, the number of rows, and the number of columns.</span></span> <span data-ttu-id="1b686-140">In diesem Beispiel wird eine Gleitkommamatrix mit zwei Zeilen und zwei Spalten erstellt.</span><span class="sxs-lookup"><span data-stu-id="1b686-140">This example creates a floating-point matrix, with two rows and two columns.</span></span> <span data-ttu-id="1b686-141">Jeder der skalaren Datentypen kann verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1b686-141">Any of the scalar data types can be used.</span></span>

<span data-ttu-id="1b686-142">Diese Deklaration definiert eine Matrix von Gleitkommawerten (32-Bit-Gleitkommazahlen) mit zwei Zeilen und drei Spalten:</span><span class="sxs-lookup"><span data-stu-id="1b686-142">This declaration defines a matrix of float values (32-bit floating-point numbers) with two rows and three columns:</span></span>


```
matrix <float, 2, 3> fFloatMatrix;
```



<span data-ttu-id="1b686-143">Eine Matrix enthält In Zeilen und Spalten angeordnete Werte, auf die mithilfe des Strukturoperator "." gefolgt von einem von zwei Benennungssätzen zugegriffen werden kann:</span><span class="sxs-lookup"><span data-stu-id="1b686-143">A matrix contains values organized in rows and columns, which can be accessed using the structure operator "." followed by one of two naming sets:</span></span>

-   <span data-ttu-id="1b686-144">Die nullbasierte Zeilenspaltenposition:</span><span class="sxs-lookup"><span data-stu-id="1b686-144">The zero-based row-column position:</span></span>
    -   <span data-ttu-id="1b686-145">\_m00, \_ m01, \_ m02, \_ m03</span><span class="sxs-lookup"><span data-stu-id="1b686-145">\_m00, \_m01, \_m02, \_m03</span></span>
    -   <span data-ttu-id="1b686-146">\_m10, \_ m11, \_ m12, \_ m13</span><span class="sxs-lookup"><span data-stu-id="1b686-146">\_m10, \_m11, \_m12, \_m13</span></span>
    -   <span data-ttu-id="1b686-147">\_m20, \_ m21, \_ m22, \_ m23</span><span class="sxs-lookup"><span data-stu-id="1b686-147">\_m20, \_m21, \_m22, \_m23</span></span>
    -   <span data-ttu-id="1b686-148">\_m30, \_ m31, \_ m32, \_ m33</span><span class="sxs-lookup"><span data-stu-id="1b686-148">\_m30, \_m31, \_m32, \_m33</span></span>
-   <span data-ttu-id="1b686-149">Die 1-basierte Zeilenspaltenposition:</span><span class="sxs-lookup"><span data-stu-id="1b686-149">The one-based row-column position:</span></span>
    -   <span data-ttu-id="1b686-150">\_11, \_ 12, \_ 13, \_ 14</span><span class="sxs-lookup"><span data-stu-id="1b686-150">\_11, \_12, \_13, \_14</span></span>
    -   <span data-ttu-id="1b686-151">\_21, \_ 22, \_ 23, \_ 24</span><span class="sxs-lookup"><span data-stu-id="1b686-151">\_21, \_22, \_23, \_24</span></span>
    -   <span data-ttu-id="1b686-152">\_31, \_ 32, \_ 33, \_ 34</span><span class="sxs-lookup"><span data-stu-id="1b686-152">\_31, \_32, \_33, \_34</span></span>
    -   <span data-ttu-id="1b686-153">\_41, \_ 42, \_ 43, \_ 44</span><span class="sxs-lookup"><span data-stu-id="1b686-153">\_41, \_42, \_43, \_44</span></span>

<span data-ttu-id="1b686-154">Jeder Benennungssatz beginnt mit einem Unterstrich, gefolgt von der Zeilennummer und der Spaltennummer.</span><span class="sxs-lookup"><span data-stu-id="1b686-154">Each naming set starts with an underscore followed by the row number and the column number.</span></span> <span data-ttu-id="1b686-155">Die nullbasierte Konvention enthält auch den Buchstaben "m" vor der Zeile und Spaltennummer.</span><span class="sxs-lookup"><span data-stu-id="1b686-155">The zero-based convention also includes the letter "m" before the row and column number.</span></span> <span data-ttu-id="1b686-156">Hier ist ein Beispiel, in dem die beiden Benennungssätze für den Zugriff auf eine Matrix verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="1b686-156">Here's an example that uses the two naming sets to access a matrix:</span></span>


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



<span data-ttu-id="1b686-157">Genau wie Vektoren können Benennungssätze eine oder mehrere Komponenten aus beiden Benennungssätzen verwenden.</span><span class="sxs-lookup"><span data-stu-id="1b686-157">Just like vectors, naming sets can use one or more components from either naming set.</span></span>


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



<span data-ttu-id="1b686-158">Auf eine Matrix kann auch mithilfe der Arrayzugriffs-Notation zugegriffen werden, bei der es sich um einen nullbasierten Satz von Indizes handelt.</span><span class="sxs-lookup"><span data-stu-id="1b686-158">A matrix can also be accessed using array access notation, which is a zero-based set of indices.</span></span> <span data-ttu-id="1b686-159">Jeder Index befindet sich in eckigen Klammern.</span><span class="sxs-lookup"><span data-stu-id="1b686-159">Each index is inside of square brackets.</span></span> <span data-ttu-id="1b686-160">Auf eine 4x4-Matrix wird mit den folgenden Indizes zugegriffen:</span><span class="sxs-lookup"><span data-stu-id="1b686-160">A 4x4 matrix is accessed with the following indices:</span></span>

-   <span data-ttu-id="1b686-161">\[0 \] \[ 0 \] , \[ 0 \] \[ 1 \] , \[ 0 \] \[ 2 \] , \[ 0 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="1b686-161">\[0\]\[0\], \[0\]\[1\], \[0\]\[2\], \[0\]\[3\]</span></span>
-   <span data-ttu-id="1b686-162">\[1 \] \[ \] 0, \[ 1 \] \[ \] 1, \[ 1 \] \[ \] 2, \[ 1 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="1b686-162">\[1\]\[0\], \[1\]\[1\], \[1\]\[2\], \[1\]\[3\]</span></span>
-   <span data-ttu-id="1b686-163">\[2 \] \[ \] 0, \[ 2 \] \[ \] 1, \[ 2 \] \[ \] 2, \[ 2 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="1b686-163">\[2\]\[0\], \[2\]\[1\], \[2\]\[2\], \[2\]\[3\]</span></span>
-   <span data-ttu-id="1b686-164">\[3 \] \[ \] 0, \[ 3 \] \[ \] 1, \[ 3 \] \[ \] 2, \[ 3 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="1b686-164">\[3\]\[0\], \[3\]\[1\], \[3\]\[2\], \[3\]\[3\]</span></span>

<span data-ttu-id="1b686-165">Hier ist ein Beispiel für den Zugriff auf eine Matrix:</span><span class="sxs-lookup"><span data-stu-id="1b686-165">Here is an example of accessing a matrix:</span></span>


```
float2x2 fMatrix = { 1.0f, 1.1f, // row 1
                     2.0f, 2.1f  // row 2
                   };
float temp;

temp = fMatrix[0][0] // single component read
temp = fMatrix[0][1] // single component read
```



<span data-ttu-id="1b686-166">Beachten Sie, dass der Strukturoperator "." nicht für den Zugriff auf ein Array verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1b686-166">Notice that the structure operator "." is not used to access an array.</span></span> <span data-ttu-id="1b686-167">Die Arrayzugriffs-Notation kann nicht swizzling verwenden, um mehr als eine Komponente zu lesen.</span><span class="sxs-lookup"><span data-stu-id="1b686-167">Array access notation cannot use swizzling to read more than one component.</span></span>


```
float2 temp;
temp = fMatrix[0][0]_[0][1] // invalid, cannot read two components
```



<span data-ttu-id="1b686-168">Der Arrayzugriff kann jedoch einen Vektor mit mehreren Komponenten lesen.</span><span class="sxs-lookup"><span data-stu-id="1b686-168">However, array accessing can read a multi-component vector.</span></span>


```
float2 temp;
float2x2 fMatrix;
temp = fMatrix[0] // read the first row
```



<span data-ttu-id="1b686-169">Wie bei Vektoren wird das Lesen von mehr als einer Matrixkomponente als Swizzling bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="1b686-169">As with vectors, reading more than one matrix component is called swizzling.</span></span> <span data-ttu-id="1b686-170">Es können mehrere Komponenten zugewiesen werden, vorausgesetzt, es wird nur ein Namensraum verwendet.</span><span class="sxs-lookup"><span data-stu-id="1b686-170">More than one component can be assigned, assuming only one name space is used.</span></span> <span data-ttu-id="1b686-171">Dies sind alle gültige Zuweisungen:</span><span class="sxs-lookup"><span data-stu-id="1b686-171">These are all valid assignments:</span></span>


```
// Given these variables
float4x4 worldMatrix = float4( {0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} );
float4x4 tempMatrix;

tempMatrix._m00_m11 = worldMatrix._m00_m11; // multiple components
tempMatrix._m00_m11 = worldMatrix.m13_m23;

tempMatrix._11_22_33 = worldMatrix._11_22_33; // any order on swizzles
tempMatrix._11_22_33 = worldMatrix._24_23_22;
```



<span data-ttu-id="1b686-172">Die Maskierung steuert, wie viele Komponenten geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="1b686-172">Masking controls how many components are written.</span></span>


```
// Given
float4x4 worldMatrix = float4( {0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} );
float4x4 tempMatrix;

tempMatrix._m00_m11 = worldMatrix._m00_m11; // write two components
tempMatrix._m23_m00 = worldMatrix._m00_m11;
```



<span data-ttu-id="1b686-173">Zuweisungen können nicht mehr als einmal in dieselbe Komponente geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="1b686-173">Assignments cannot be written to the same component more than once.</span></span> <span data-ttu-id="1b686-174">Daher ist die linke Seite dieser Anweisung ungültig:</span><span class="sxs-lookup"><span data-stu-id="1b686-174">So the left side of this statement is invalid:</span></span>


```
// cannot write to the same component more than once
tempMatrix._m00_m00 = worldMatrix._m00_m11;
```



<span data-ttu-id="1b686-175">Außerdem können die Komponentennamensräume nicht gemischt werden.</span><span class="sxs-lookup"><span data-stu-id="1b686-175">Also, the component name spaces cannot be mixed.</span></span> <span data-ttu-id="1b686-176">Dies ist ein ungültiger Komponenten-Schreibzugriff:</span><span class="sxs-lookup"><span data-stu-id="1b686-176">This is an invalid component write:</span></span>


```
// Invalid use of same component on left side
tempMatrix._11_m23 = worldMatrix._11_22; 
```



### <a name="matrix-ordering"></a><span data-ttu-id="1b686-177">Matrix reihenfolge</span><span class="sxs-lookup"><span data-stu-id="1b686-177">Matrix Ordering</span></span>

<span data-ttu-id="1b686-178">Die Matrixpackungsauftrag für einheitliche Parameter ist standardmäßig auf Spaltenmatrizen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1b686-178">Matrix packing order for uniform parameters is set to column-major by default.</span></span> <span data-ttu-id="1b686-179">Dies bedeutet, dass jede Spalte der Matrix in einem einzelnen Konstantenregister gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="1b686-179">This means each column of the matrix is stored in a single constant register.</span></span> <span data-ttu-id="1b686-180">Andererseits packt eine Zeilen-Hauptmatrix jede Zeile der Matrix in einem einzelnen Konstantenregister.</span><span class="sxs-lookup"><span data-stu-id="1b686-180">On the other hand, a row-major matrix packs each row of the matrix in a single constant register.</span></span> <span data-ttu-id="1b686-181">Die Matrixpackung kann mit der **\# pragmapack-Matrix-Direktive \_** oder mit der **\_ Zeilen-Hauptzeile** oder dem **Schlüsselwort column major \_ geändert** werden.</span><span class="sxs-lookup"><span data-stu-id="1b686-181">Matrix packing can be changed with the **\#pragmapack\_matrix** directive, or with the **row\_major** or the **column\_major** keyword.</span></span>

<span data-ttu-id="1b686-182">Die Daten in einer Matrix werden in Shader-Konstantenregister geladen, bevor ein Shader ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1b686-182">The data in a matrix is loaded into shader constant registers before a shader runs.</span></span> <span data-ttu-id="1b686-183">Es gibt zwei Möglichkeiten, wie die Matrixdaten gelesen werden: in Zeilen-Hauptreihen- oder Spalten-Hauptreihen reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="1b686-183">There are two choices for how the matrix data is read: in row-major order or in column-major order.</span></span> <span data-ttu-id="1b686-184">Die Spaltenordnung bedeutet, dass jede Matrixspalte in einem einzelnen konstanten Register gespeichert wird, und zeilenbasierte Reihenfolge bedeutet, dass jede Zeile der Matrix in einem einzelnen konstanten Register gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="1b686-184">Column-major order means that each matrix column will be stored in a single constant register, and row-major order means that each row of the matrix will be stored in a single constant register.</span></span> <span data-ttu-id="1b686-185">Dies ist ein wichtiger Aspekt bei der Verwendung von konstanten Registern für eine Matrix.</span><span class="sxs-lookup"><span data-stu-id="1b686-185">This is an important consideration for how many constant registers are used for a matrix.</span></span>

<span data-ttu-id="1b686-186">Eine Zeilenmatrizenmatrix ist wie folgt angelegt:</span><span class="sxs-lookup"><span data-stu-id="1b686-186">A row-major matrix is laid out like the following:</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="1b686-187">11</span><span class="sxs-lookup"><span data-stu-id="1b686-187">11</span></span><br/>
        <span data-ttu-id="1b686-188">21</span><span class="sxs-lookup"><span data-stu-id="1b686-188">21</span></span><br/>
        <span data-ttu-id="1b686-189">31</span><span class="sxs-lookup"><span data-stu-id="1b686-189">31</span></span><br/>
        <span data-ttu-id="1b686-190">41</span><span class="sxs-lookup"><span data-stu-id="1b686-190">41</span></span><br/>
    :::column-end:::
    :::column:::
        <span data-ttu-id="1b686-191">12</span><span class="sxs-lookup"><span data-stu-id="1b686-191">12</span></span><br/>
        <span data-ttu-id="1b686-192">22</span><span class="sxs-lookup"><span data-stu-id="1b686-192">22</span></span><br/>
        <span data-ttu-id="1b686-193">32</span><span class="sxs-lookup"><span data-stu-id="1b686-193">32</span></span><br/>
        <span data-ttu-id="1b686-194">42</span><span class="sxs-lookup"><span data-stu-id="1b686-194">42</span></span><br/>
    :::column-end:::
    :::column:::
        <span data-ttu-id="1b686-195">13</span><span class="sxs-lookup"><span data-stu-id="1b686-195">13</span></span><br/>
        <span data-ttu-id="1b686-196">23</span><span class="sxs-lookup"><span data-stu-id="1b686-196">23</span></span><br/>
        <span data-ttu-id="1b686-197">33</span><span class="sxs-lookup"><span data-stu-id="1b686-197">33</span></span><br/>
        <span data-ttu-id="1b686-198">43</span><span class="sxs-lookup"><span data-stu-id="1b686-198">43</span></span><br/>
    :::column-end:::
    :::column:::
        <span data-ttu-id="1b686-199">14</span><span class="sxs-lookup"><span data-stu-id="1b686-199">14</span></span><br/>
        <span data-ttu-id="1b686-200">24</span><span class="sxs-lookup"><span data-stu-id="1b686-200">24</span></span><br/>
        <span data-ttu-id="1b686-201">34</span><span class="sxs-lookup"><span data-stu-id="1b686-201">34</span></span><br/>
        <span data-ttu-id="1b686-202">44</span><span class="sxs-lookup"><span data-stu-id="1b686-202">44</span></span><br/>
    :::column-end:::
:::row-end:::




 

<span data-ttu-id="1b686-203">Eine Spaltenmatrizenmatrix ist wie folgt angelegt:</span><span class="sxs-lookup"><span data-stu-id="1b686-203">A column-major matrix is laid out like the following:</span></span>


:::row:::
    :::column:::
        <span data-ttu-id="1b686-204">11</span><span class="sxs-lookup"><span data-stu-id="1b686-204">11</span></span><br/>
        <span data-ttu-id="1b686-205">12</span><span class="sxs-lookup"><span data-stu-id="1b686-205">12</span></span><br/>
        <span data-ttu-id="1b686-206">13</span><span class="sxs-lookup"><span data-stu-id="1b686-206">13</span></span><br/>
        <span data-ttu-id="1b686-207">14</span><span class="sxs-lookup"><span data-stu-id="1b686-207">14</span></span><br/>
    :::column-end:::
    :::column:::
        <span data-ttu-id="1b686-208">21</span><span class="sxs-lookup"><span data-stu-id="1b686-208">21</span></span><br/>
        <span data-ttu-id="1b686-209">22</span><span class="sxs-lookup"><span data-stu-id="1b686-209">22</span></span><br/>
        <span data-ttu-id="1b686-210">23</span><span class="sxs-lookup"><span data-stu-id="1b686-210">23</span></span><br/>
        <span data-ttu-id="1b686-211">24</span><span class="sxs-lookup"><span data-stu-id="1b686-211">24</span></span><br/>
    :::column-end:::
    :::column:::
        <span data-ttu-id="1b686-212">31</span><span class="sxs-lookup"><span data-stu-id="1b686-212">31</span></span><br/>
        <span data-ttu-id="1b686-213">32</span><span class="sxs-lookup"><span data-stu-id="1b686-213">32</span></span><br/>
        <span data-ttu-id="1b686-214">33</span><span class="sxs-lookup"><span data-stu-id="1b686-214">33</span></span><br/>
        <span data-ttu-id="1b686-215">34</span><span class="sxs-lookup"><span data-stu-id="1b686-215">34</span></span><br/>
    :::column-end:::
    :::column:::
        <span data-ttu-id="1b686-216">14</span><span class="sxs-lookup"><span data-stu-id="1b686-216">14</span></span><br/>
        <span data-ttu-id="1b686-217">24</span><span class="sxs-lookup"><span data-stu-id="1b686-217">24</span></span><br/>
        <span data-ttu-id="1b686-218">34</span><span class="sxs-lookup"><span data-stu-id="1b686-218">34</span></span><br/>
        <span data-ttu-id="1b686-219">44</span><span class="sxs-lookup"><span data-stu-id="1b686-219">44</span></span><br/>
    :::column-end:::
:::row-end:::




 

<span data-ttu-id="1b686-220">Die Reihenfolge der Zeilen- und Spaltenmatrizen bestimmt die Reihenfolge, in der die Matrixkomponenten aus Shadereingaben gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="1b686-220">Row-major and column-major matrix ordering determine the order the matrix components are read from shader inputs.</span></span> <span data-ttu-id="1b686-221">Sobald die Daten in konstante Register geschrieben wurden, hat die Matrix reihenfolge keine Auswirkungen darauf, wie die Daten innerhalb des Shadercodes verwendet oder darauf zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="1b686-221">Once the data is written into constant registers, matrix order has no effect on how the data is used or accessed from within shader code.</span></span> <span data-ttu-id="1b686-222">Außerdem werden Matrizen, die in einem Shader-Text deklariert sind, nicht in konstanten Registern gepackt.</span><span class="sxs-lookup"><span data-stu-id="1b686-222">Also, matrices declared in a shader body do not get packed into constant registers.</span></span> <span data-ttu-id="1b686-223">Die Zeilen- und Spalten-Hauptpackungsreihen reihenfolge hat keinen Einfluss auf die Füllreihen reihenfolge von Konstruktoren (die immer der Zeilenordnung folgt).</span><span class="sxs-lookup"><span data-stu-id="1b686-223">Row-major and column-major packing order has no influence on the packing order of constructors (which always follows row-major ordering).</span></span>

<span data-ttu-id="1b686-224">Die Reihenfolge der Daten in einer Matrix kann zur Kompilierzeit deklariert werden, oder der Compiler ordnet die Daten zur Laufzeit für die effizienteste Verwendung an.</span><span class="sxs-lookup"><span data-stu-id="1b686-224">The order of the data in a matrix can be declared at compile time or the compiler will order the data at runtime for the most efficient use.</span></span>

## <a name="examples"></a><span data-ttu-id="1b686-225">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1b686-225">Examples</span></span>

<span data-ttu-id="1b686-226">HLSL verwendet zwei spezielle Typen, einen Vektortyp und einen Matrixtyp, um die Programmierung von 2D- und 3D-Grafiken zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="1b686-226">HLSL uses two special types, a vector type and a matrix type to make programming 2D and 3D graphics easier.</span></span> <span data-ttu-id="1b686-227">Jeder dieser Typen enthält mehr als eine Komponente. ein Vektor enthält bis zu vier Komponenten, und eine Matrix enthält bis zu 16 Komponenten.</span><span class="sxs-lookup"><span data-stu-id="1b686-227">Each of these types contain more than one component; a vector contains up to four components, and a matrix contains up to 16 components.</span></span> <span data-ttu-id="1b686-228">Wenn Vektoren und Matrizen in HLSL-Standardgleichungen verwendet werden, ist die durchgeführte Mathematik so konzipiert, dass sie pro Komponente funktioniert.</span><span class="sxs-lookup"><span data-stu-id="1b686-228">When vectors and matrices are used in standard HLSL equations, the math performed is designed to work per-component.</span></span> <span data-ttu-id="1b686-229">HLSL implementiert beispielsweise diese Multiplikation:</span><span class="sxs-lookup"><span data-stu-id="1b686-229">For instance, HLSL implements this multiply:</span></span>


```
float4 v = a*b;
```



<span data-ttu-id="1b686-230">als Multiplikation mit vier Komponenten.</span><span class="sxs-lookup"><span data-stu-id="1b686-230">as a four-component multiply.</span></span> <span data-ttu-id="1b686-231">Das Ergebnis sind vier Skalar:</span><span class="sxs-lookup"><span data-stu-id="1b686-231">The result is four scalars:</span></span>


```
float4 v = a*b;

v.x = a.x*b.x;
v.y = a.y*b.y;
v.z = a.z*b.z;
v.w = a.w*b.w;
```



<span data-ttu-id="1b686-232">Dies sind vier Multiplikationen, bei denen jedes Ergebnis in einer separaten Komponente von v gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="1b686-232">This is four multiplications where each result is stored in a separate component of v.</span></span> <span data-ttu-id="1b686-233">Dies wird als Multiplikation mit vier Komponenten bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="1b686-233">This is called a four-component multiply.</span></span> <span data-ttu-id="1b686-234">HLSL verwendet Dies macht das Schreiben von Shadern sehr effizient.</span><span class="sxs-lookup"><span data-stu-id="1b686-234">HLSL uses component math which makes writing shaders very efficient.</span></span>

<span data-ttu-id="1b686-235">Dies ist sehr anders als eine Multiplikation, die in der Regel als Punktprodukt implementiert wird, das einen einzelnen Skalar generiert:</span><span class="sxs-lookup"><span data-stu-id="1b686-235">This is very different from a multiply which is typically implemented as a dot product which generates a single scalar:</span></span>


```
v = a.x*b.x + a.y*b.y + a.z*b.z + a.w*b.w;
```



<span data-ttu-id="1b686-236">Eine Matrix verwendet auch Vorgänge pro Komponente in HLSL:</span><span class="sxs-lookup"><span data-stu-id="1b686-236">A matrix also uses per-component operations in HLSL:</span></span>


```
float3x3 mat1,mat2;
...
float3x3 mat3 = mat1*mat2;
```



<span data-ttu-id="1b686-237">Das Ergebnis ist eine Multiplikation der beiden Matrizen pro Komponente (im Gegensatz zu einer standardmäßigen 3x3-Matrixmultiplikation).</span><span class="sxs-lookup"><span data-stu-id="1b686-237">The result is a per-component multiply of the two matrices (as opposed to a standard 3x3 matrix multiply).</span></span> <span data-ttu-id="1b686-238">Eine Multiplikation pro Komponentenmatrix ergibt diesen ersten Begriff:</span><span class="sxs-lookup"><span data-stu-id="1b686-238">A per component matrix multiply yields this first term:</span></span>


```
mat3.m00 = mat1.m00 * mat2._m00;
```



<span data-ttu-id="1b686-239">Dies ist anders als bei einer 3x3-Matrixmultiplikation, die diesen ersten Begriff ergeben würde:</span><span class="sxs-lookup"><span data-stu-id="1b686-239">This is different from a 3x3 matrix multiply which would yield this first term:</span></span>


```
// First component of a four-component matrix multiply
mat.m00 = mat1._m00 * mat2._m00 + 
          mat1._m01 * mat2._m10 + 
          mat1._m02 * mat2._m20 + 
          mat1._m03 * mat2._m30;
```



<span data-ttu-id="1b686-240">Überladene Versionen der multiplizierten systeminternen Funktion behandeln Fälle, in denen ein Operand ein Vektor und der andere Operand eine Matrix ist.</span><span class="sxs-lookup"><span data-stu-id="1b686-240">Overloaded versions of the multiply intrinsic function handle cases where one operand is a vector and the other operand is a matrix.</span></span> <span data-ttu-id="1b686-241">Beispiel: \* Vektorvektor, \* Vektormatrix, \* Matrixvektor und \* Matrixmatrix.</span><span class="sxs-lookup"><span data-stu-id="1b686-241">Such as: vector \* vector, vector \* matrix, matrix \* vector, and matrix \* matrix.</span></span> <span data-ttu-id="1b686-242">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="1b686-242">For instance:</span></span>


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



<span data-ttu-id="1b686-243">erzeugt das gleiche Ergebnis wie:</span><span class="sxs-lookup"><span data-stu-id="1b686-243">produces the same result as:</span></span>


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



<span data-ttu-id="1b686-244">In diesem Beispiel wird der Pos-Vektor mithilfe der (float1x4)-Cast in einen Spaltenvektor umformatiert.</span><span class="sxs-lookup"><span data-stu-id="1b686-244">This example casts the pos vector to a column vector using the (float1x4) cast.</span></span> <span data-ttu-id="1b686-245">Das Ändern eines Vektors durch Umwandlung oder das Austauschen der Reihenfolge der argumente, die zum Multiplizieren angegeben werden, entspricht dem Transpos der Matrix.</span><span class="sxs-lookup"><span data-stu-id="1b686-245">Changing a vector by casting, or swapping the order of the arguments supplied to multiply is equivalent to transposing the matrix.</span></span>

<span data-ttu-id="1b686-246">Die automatische Umwandlungskonvertierung bewirkt, dass die systeminternen Funktionen multiply und dot die gleichen Ergebnisse zurückgeben wie hier verwendet:</span><span class="sxs-lookup"><span data-stu-id="1b686-246">Automatic cast conversion causes the multiply and dot intrinsic functions to return the same results as used here:</span></span>


```
{
  float4 val;
  return mul(val,val);
}
```



<span data-ttu-id="1b686-247">Dieses Ergebnis der Multiplikation ist ein 1x4 \* 4x1 = 1x1-Vektor.</span><span class="sxs-lookup"><span data-stu-id="1b686-247">This result of the multiply is a 1x4 \* 4x1 = 1x1 vector.</span></span> <span data-ttu-id="1b686-248">Dies entspricht einem Punktprodukt:</span><span class="sxs-lookup"><span data-stu-id="1b686-248">This is equivalent to a dot product:</span></span>


```
{
  float4 val;
  return dot(val,val);
}
```



<span data-ttu-id="1b686-249">, die einen einzelnen Skalarwert zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="1b686-249">which returns a single scalar value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1b686-250">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1b686-250">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b686-251">Datentypen (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1b686-251">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 




