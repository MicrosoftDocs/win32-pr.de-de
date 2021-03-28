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
# <a name="per-component-math-operations"></a><span data-ttu-id="e6b1f-103">Per-Component mathematische Vorgänge</span><span class="sxs-lookup"><span data-stu-id="e6b1f-103">Per-Component Math Operations</span></span>

<span data-ttu-id="e6b1f-104">Mit HLSL können Sie Shader auf Algorithmusebene programmieren.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-104">With HLSL, you can program shaders at an algorithm level.</span></span> <span data-ttu-id="e6b1f-105">Um die Sprache zu verstehen, müssen Sie wissen, wie Sie Variablen und Funktionen deklarieren, systeminterne Funktionen verwenden, benutzerdefinierte Datentypen definieren und die Semantik verwenden, um shaderargumente mit anderen Shader und der Pipeline zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-105">To understand the language, you will need to know how to declare variables and functions, use intrinsic functions, define custom data types and use semantics to connect shader arguments to other shaders and to the pipeline.</span></span>

<span data-ttu-id="e6b1f-106">Nachdem Sie erfahren haben, wie Shader in HLSL erstellt werden, müssen Sie sich mit API-aufrufen vertraut machen, damit Sie: einen Shader für bestimmte Hardware kompilieren, shaderkonstanten initialisieren und ggf. anderen Pipeline Status initialisieren können.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-106">Once you learn how to author shaders in HLSL, you will need to learn about API calls so that you can: compile a shader for particular hardware, initialize shader constants, and initialize other pipeline state if necessary.</span></span>

-   [<span data-ttu-id="e6b1f-107">Der Vektortyp.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-107">The Vector Type</span></span>](#the-vector-type)
-   [<span data-ttu-id="e6b1f-108">Der Matrix-Typ</span><span class="sxs-lookup"><span data-stu-id="e6b1f-108">The Matrix Type</span></span>](#the-matrix-type)
    -   [<span data-ttu-id="e6b1f-109">Matrix Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="e6b1f-109">Matrix Ordering</span></span>](#matrix-ordering)
-   [<span data-ttu-id="e6b1f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e6b1f-110">Examples</span></span>](#examples)
-   [<span data-ttu-id="e6b1f-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e6b1f-111">Related topics</span></span>](#related-topics)

## <a name="the-vector-type"></a><span data-ttu-id="e6b1f-112">Der Vektortyp.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-112">The Vector Type</span></span>

<span data-ttu-id="e6b1f-113">Ein Vektor ist eine Datenstruktur, die zwischen einer und vier Komponenten enthält.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-113">A vector is a data structure that contains between one and four components.</span></span>


```
bool    bVector;   // scalar containing 1 Boolean
bool1   bVector;   // vector containing 1 Boolean
int1    iVector;   // vector containing 1 int
float3  fVector;   // vector containing 3 floats
double4 dVector;   // vector containing 4 doubles
```



<span data-ttu-id="e6b1f-114">Die ganze Zahl, die unmittelbar auf den-Datentyp folgt, ist die Anzahl der Komponenten auf dem Vektor.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-114">The integer immediately following the data type is the number of components on the vector.</span></span>

<span data-ttu-id="e6b1f-115">Initialisierer können auch in die Deklarationen eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-115">Initializers can also be included in the declarations.</span></span>


```
bool    bVector = false;
int1    iVector = 1;
float3  fVector = { 0.2f, 0.3f, 0.4f };
double4 dVector = { 0.2, 0.3, 0.4, 0.5 };
```



<span data-ttu-id="e6b1f-116">Alternativ kann der Vector Type verwendet werden, um dieselben Deklarationen zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="e6b1f-116">Alternatively, the vector type can be used to make the same declarations:</span></span>


```
vector <bool,   1> bVector = false;
vector <int,    1> iVector = 1;
vector <float,  3> fVector = { 0.2f, 0.3f, 0.4f };
vector <double, 4> dVector = { 0.2, 0.3, 0.4, 0.5 };
```



<span data-ttu-id="e6b1f-117">Der Vektortyp verwendet spitzen Klammern, um den Typ und die Anzahl der Komponenten anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-117">The vector type uses angle brackets to specify the type and number of components.</span></span>

<span data-ttu-id="e6b1f-118">Vektoren enthalten bis zu vier Komponenten, auf die jeweils mit einem von zwei Benennungs Sätzen zugegriffen werden kann:</span><span class="sxs-lookup"><span data-stu-id="e6b1f-118">Vectors contain up to four components, each of which can be accessed using one of two naming sets:</span></span>

-   <span data-ttu-id="e6b1f-119">Der Positions Satz: x, y, z, w</span><span class="sxs-lookup"><span data-stu-id="e6b1f-119">The position set: x,y,z,w</span></span>
-   <span data-ttu-id="e6b1f-120">Der Farbsatz: r, g, b, a</span><span class="sxs-lookup"><span data-stu-id="e6b1f-120">The color set: r,g,b,a</span></span>

<span data-ttu-id="e6b1f-121">In diesen Anweisungen wird der Wert in der dritten Komponente zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-121">These statements both return the value in the third component.</span></span>


```
// Given
float4 pos = float4(0,0,2,1);

pos.z    // value is 2
pos.b    // value is 2
```



<span data-ttu-id="e6b1f-122">Benennungs Sätze können eine oder mehrere Komponenten verwenden, aber Sie können nicht gemischt werden.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-122">Naming sets can use one or more components, but they cannot be mixed.</span></span>


```
// Given
float4 pos = float4(0,0,2,1);
float2 temp;

temp = pos.xy  // valid
temp = pos.rg  // valid

temp = pos.xg  // NOT VALID because the position and color sets were used.
```



<span data-ttu-id="e6b1f-123">Das Angeben einer oder mehrerer Vektor Komponenten beim Lesen von Komponenten wird als "swizzling" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-123">Specifying one or more vector components when reading components is called swizzling.</span></span> <span data-ttu-id="e6b1f-124">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="e6b1f-124">For example:</span></span>


```
float4 pos = float4(0,0,2,1);
float2 f_2D;
f_2D = pos.xy;   // read two components 
f_2D = pos.xz;   // read components in any order       
f_2D = pos.zx;

f_2D = pos.xx;   // components can be read more than once
f_2D = pos.yy;
```



<span data-ttu-id="e6b1f-125">Die Maskierung steuert, wie viele Komponenten geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-125">Masking controls how many components are written.</span></span>


```
float4 pos = float4(0,0,2,1);
float4 f_4D;
f_4D    = pos;     // write four components          

f_4D.xz = pos.xz;  // write two components        
f_4D.zx = pos.xz;  // change the write order

f_4D.xzyw = pos.w; // write one component to more than one component
f_4D.wzyx = pos;
```



<span data-ttu-id="e6b1f-126">Zuweisungen können nicht mehrmals in dieselbe Komponente geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-126">Assignments cannot be written to the same component more than once.</span></span> <span data-ttu-id="e6b1f-127">Die linke Seite dieser Anweisung ist daher ungültig:</span><span class="sxs-lookup"><span data-stu-id="e6b1f-127">So the left side of this statement is invalid:</span></span>


```
f_4D.xx = pos.xy;   // cannot write to the same destination components 
```



<span data-ttu-id="e6b1f-128">Außerdem kann der Komponenten Namespaces nicht gemischt werden.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-128">Also, the component name spaces cannot be mixed.</span></span> <span data-ttu-id="e6b1f-129">Dies ist ein ungültiger Komponenten Schreibvorgang:</span><span class="sxs-lookup"><span data-stu-id="e6b1f-129">This is an invalid component write:</span></span>


```
f_4D.xg = pos.rgrg;    // invalid write: cannot mix component name spaces 
```



<span data-ttu-id="e6b1f-130">Der Zugriff auf einen Vektor als Skalar erfolgt auf die erste Komponente des Vektors.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-130">Accessing a vector as a scalar will access the first component of the vector.</span></span> <span data-ttu-id="e6b1f-131">Die folgenden zwei Anweisungen sind gleichwertig.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-131">The following two statements are equivalent.</span></span>


```
f_4D.a = pos * 5.0f;
f_4D.a = pos.r * 5.0f;
```



## <a name="the-matrix-type"></a><span data-ttu-id="e6b1f-132">Der Matrix-Typ</span><span class="sxs-lookup"><span data-stu-id="e6b1f-132">The Matrix Type</span></span>

<span data-ttu-id="e6b1f-133">Eine Matrix ist eine Datenstruktur, die Zeilen und Spalten mit Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-133">A matrix is a data structure that contains rows and columns of data.</span></span> <span data-ttu-id="e6b1f-134">Bei den Daten kann es sich um einen beliebigen skalaren Datentypen handeln, aber jedes Element einer Matrix ist derselbe Datentyp.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-134">The data can be any of the scalar data types, however, every element of a matrix is the same data type.</span></span> <span data-ttu-id="e6b1f-135">Die Anzahl der Zeilen und Spalten wird mit der zeilenweise Zeichenfolge angegeben, die an den Datentyp angehängt wird.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-135">The number of rows and columns is specified with the row-by-column string that is appended to the data type.</span></span>


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



<span data-ttu-id="e6b1f-136">Die maximale Anzahl von Zeilen oder Spalten ist 4. die Mindestanzahl ist 1.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-136">The maximum number of rows or columns is 4; the minimum number is 1.</span></span>

<span data-ttu-id="e6b1f-137">Eine Matrix kann beim Deklarieren initialisiert werden:</span><span class="sxs-lookup"><span data-stu-id="e6b1f-137">A matrix can be initialized when it is declared:</span></span>


```
float2x2 fMatrix = { 0.0f, 0.1, // row 1
                     2.1f, 2.2f // row 2
                   };   
```



<span data-ttu-id="e6b1f-138">Oder der Matrix-Typ kann verwendet werden, um dieselben Deklarationen zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="e6b1f-138">Or, the matrix type can be used to make the same declarations:</span></span>


```
matrix <float, 2, 2> fMatrix = { 0.0f, 0.1, // row 1
                                 2.1f, 2.2f // row 2
                               };
```



<span data-ttu-id="e6b1f-139">Der Matrixtyp verwendet die spitzen Klammern, um den Typ, die Anzahl der Zeilen und die Anzahl der Spalten anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-139">The matrix type uses the angle brackets to specify the type, the number of rows, and the number of columns.</span></span> <span data-ttu-id="e6b1f-140">In diesem Beispiel wird eine Gleit Komma Matrix mit zwei Zeilen und zwei Spalten erstellt.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-140">This example creates a floating-point matrix, with two rows and two columns.</span></span> <span data-ttu-id="e6b1f-141">Alle skalaren Datentypen können verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-141">Any of the scalar data types can be used.</span></span>

<span data-ttu-id="e6b1f-142">Diese Deklaration definiert eine Matrix von float-Werten (32-Bit-Gleit Komma Zahlen) mit zwei Zeilen und drei Spalten:</span><span class="sxs-lookup"><span data-stu-id="e6b1f-142">This declaration defines a matrix of float values (32-bit floating-point numbers) with two rows and three columns:</span></span>


```
matrix <float, 2, 3> fFloatMatrix;
```



<span data-ttu-id="e6b1f-143">Eine Matrix enthält Werte, die in Zeilen und Spalten organisiert sind, auf die mit dem Structure-Operator "." gefolgt von einem von zwei Benennungs Sätzen zugegriffen werden kann:</span><span class="sxs-lookup"><span data-stu-id="e6b1f-143">A matrix contains values organized in rows and columns, which can be accessed using the structure operator "." followed by one of two naming sets:</span></span>

-   <span data-ttu-id="e6b1f-144">Die null basierte Zeilen Spaltenposition:</span><span class="sxs-lookup"><span data-stu-id="e6b1f-144">The zero-based row-column position:</span></span>
    -   <span data-ttu-id="e6b1f-145">\_M00, \_ M01, \_ M02, \_ M03</span><span class="sxs-lookup"><span data-stu-id="e6b1f-145">\_m00, \_m01, \_m02, \_m03</span></span>
    -   <span data-ttu-id="e6b1f-146">\_M10, \_ M11, \_ M12, \_ M13</span><span class="sxs-lookup"><span data-stu-id="e6b1f-146">\_m10, \_m11, \_m12, \_m13</span></span>
    -   <span data-ttu-id="e6b1f-147">\_M20, \_ M21, \_ M22, \_ M23</span><span class="sxs-lookup"><span data-stu-id="e6b1f-147">\_m20, \_m21, \_m22, \_m23</span></span>
    -   <span data-ttu-id="e6b1f-148">\_M30, \_ M31, \_ M32, \_ M33</span><span class="sxs-lookup"><span data-stu-id="e6b1f-148">\_m30, \_m31, \_m32, \_m33</span></span>
-   <span data-ttu-id="e6b1f-149">Die einbasierte Zeilen Spaltenposition:</span><span class="sxs-lookup"><span data-stu-id="e6b1f-149">The one-based row-column position:</span></span>
    -   <span data-ttu-id="e6b1f-150">\_11, \_ 12, \_ 13, \_ 14</span><span class="sxs-lookup"><span data-stu-id="e6b1f-150">\_11, \_12, \_13, \_14</span></span>
    -   <span data-ttu-id="e6b1f-151">\_21, \_ 22, \_ 23, \_ 24</span><span class="sxs-lookup"><span data-stu-id="e6b1f-151">\_21, \_22, \_23, \_24</span></span>
    -   <span data-ttu-id="e6b1f-152">\_31, \_ 32, \_ 33, \_ 34</span><span class="sxs-lookup"><span data-stu-id="e6b1f-152">\_31, \_32, \_33, \_34</span></span>
    -   <span data-ttu-id="e6b1f-153">\_41, \_ 42, \_ 43, \_ 44</span><span class="sxs-lookup"><span data-stu-id="e6b1f-153">\_41, \_42, \_43, \_44</span></span>

<span data-ttu-id="e6b1f-154">Jeder Benennungs Satz beginnt mit einem Unterstrich, gefolgt von der Zeilennummer und der Spaltennummer.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-154">Each naming set starts with an underscore followed by the row number and the column number.</span></span> <span data-ttu-id="e6b1f-155">Die null basierte Konvention enthält auch den Buchstaben "m" vor der Zeilen-und Spaltennummer.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-155">The zero-based convention also includes the letter "m" before the row and column number.</span></span> <span data-ttu-id="e6b1f-156">Im folgenden finden Sie ein Beispiel, das die beiden Benennungs Sätze verwendet, um auf eine Matrix zuzugreifen:</span><span class="sxs-lookup"><span data-stu-id="e6b1f-156">Here's an example that uses the two naming sets to access a matrix:</span></span>


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



<span data-ttu-id="e6b1f-157">Ebenso wie Vektoren können Benennungs Sätze eine oder mehrere Komponenten aus einer der beiden Benennungs Sätze verwenden.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-157">Just like vectors, naming sets can use one or more components from either naming set.</span></span>


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



<span data-ttu-id="e6b1f-158">Auf eine Matrix kann auch mit der Array Zugriffs Notation zugegriffen werden, bei der es sich um einen NULL basierten Satz von Indizes handelt.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-158">A matrix can also be accessed using array access notation, which is a zero-based set of indices.</span></span> <span data-ttu-id="e6b1f-159">Jeder Index befindet sich in eckigen Klammern.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-159">Each index is inside of square brackets.</span></span> <span data-ttu-id="e6b1f-160">Der Zugriff auf eine 4X4-Matrix erfolgt mit den folgenden Indizes:</span><span class="sxs-lookup"><span data-stu-id="e6b1f-160">A 4x4 matrix is accessed with the following indices:</span></span>

-   <span data-ttu-id="e6b1f-161">\[0 \] \[ 0 \] , \[ 0 \] \[ 1 \] , \[ 0 \] \[ 2 \] , \[ 0 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="e6b1f-161">\[0\]\[0\], \[0\]\[1\], \[0\]\[2\], \[0\]\[3\]</span></span>
-   <span data-ttu-id="e6b1f-162">\[1 \] \[ 0 \] , \[ 1 \] \[ 1 \] , \[ 1 \] \[ 2 \] , \[ 1 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="e6b1f-162">\[1\]\[0\], \[1\]\[1\], \[1\]\[2\], \[1\]\[3\]</span></span>
-   <span data-ttu-id="e6b1f-163">\[2 \] \[ 0,0 \] \[ \] \[ 1, 2 \] 2 \[ \] \[ \] , \[ 2 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="e6b1f-163">\[2\]\[0\], \[2\]\[1\], \[2\]\[2\], \[2\]\[3\]</span></span>
-   <span data-ttu-id="e6b1f-164">\[3 \] \[ 0,0 \] \[ \] \[ 1, 3 \] \[ \] \[ 2, 3 \] \[ \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="e6b1f-164">\[3\]\[0\], \[3\]\[1\], \[3\]\[2\], \[3\]\[3\]</span></span>

<span data-ttu-id="e6b1f-165">Im folgenden finden Sie ein Beispiel für den Zugriff auf eine Matrix:</span><span class="sxs-lookup"><span data-stu-id="e6b1f-165">Here is an example of accessing a matrix:</span></span>


```
float2x2 fMatrix = { 1.0f, 1.1f, // row 1
                     2.0f, 2.1f  // row 2
                   };
float temp;

temp = fMatrix[0][0] // single component read
temp = fMatrix[0][1] // single component read
```



<span data-ttu-id="e6b1f-166">Beachten Sie, dass der Structure-Operator "." nicht verwendet wird, um auf ein Array zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-166">Notice that the structure operator "." is not used to access an array.</span></span> <span data-ttu-id="e6b1f-167">Die Array Zugriffs Notation kann nicht zum Lesen von mehr als einer Komponente verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-167">Array access notation cannot use swizzling to read more than one component.</span></span>


```
float2 temp;
temp = fMatrix[0][0]_[0][1] // invalid, cannot read two components
```



<span data-ttu-id="e6b1f-168">Allerdings kann der Array Zugriff einen Vektor mit mehreren Komponenten lesen.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-168">However, array accessing can read a multi-component vector.</span></span>


```
float2 temp;
float2x2 fMatrix;
temp = fMatrix[0] // read the first row
```



<span data-ttu-id="e6b1f-169">Wie bei Vektoren wird das Lesen von mehr als einer Matrix Komponente als "swizzling" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-169">As with vectors, reading more than one matrix component is called swizzling.</span></span> <span data-ttu-id="e6b1f-170">Es können mehrere Komponenten zugewiesen werden, sofern nur ein Namespace verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-170">More than one component can be assigned, assuming only one name space is used.</span></span> <span data-ttu-id="e6b1f-171">Dies sind alle gültigen Zuweisungen:</span><span class="sxs-lookup"><span data-stu-id="e6b1f-171">These are all valid assignments:</span></span>


```
// Given these variables
float4x4 worldMatrix = float4( {0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} );
float4x4 tempMatrix;

tempMatrix._m00_m11 = worldMatrix._m00_m11; // multiple components
tempMatrix._m00_m11 = worldMatrix.m13_m23;

tempMatrix._11_22_33 = worldMatrix._11_22_33; // any order on swizzles
tempMatrix._11_22_33 = worldMatrix._24_23_22;
```



<span data-ttu-id="e6b1f-172">Die Maskierung steuert, wie viele Komponenten geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-172">Masking controls how many components are written.</span></span>


```
// Given
float4x4 worldMatrix = float4( {0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} );
float4x4 tempMatrix;

tempMatrix._m00_m11 = worldMatrix._m00_m11; // write two components
tempMatrix._m23_m00 = worldMatrix._m00_m11;
```



<span data-ttu-id="e6b1f-173">Zuweisungen können nicht mehrmals in dieselbe Komponente geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-173">Assignments cannot be written to the same component more than once.</span></span> <span data-ttu-id="e6b1f-174">Die linke Seite dieser Anweisung ist daher ungültig:</span><span class="sxs-lookup"><span data-stu-id="e6b1f-174">So the left side of this statement is invalid:</span></span>


```
// cannot write to the same component more than once
tempMatrix._m00_m00 = worldMatrix._m00_m11;
```



<span data-ttu-id="e6b1f-175">Außerdem kann der Komponenten Namespaces nicht gemischt werden.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-175">Also, the component name spaces cannot be mixed.</span></span> <span data-ttu-id="e6b1f-176">Dies ist ein ungültiger Komponenten Schreibvorgang:</span><span class="sxs-lookup"><span data-stu-id="e6b1f-176">This is an invalid component write:</span></span>


```
// Invalid use of same component on left side
tempMatrix._11_m23 = worldMatrix._11_22; 
```



### <a name="matrix-ordering"></a><span data-ttu-id="e6b1f-177">Matrix Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="e6b1f-177">Matrix Ordering</span></span>

<span data-ttu-id="e6b1f-178">Die Matrix Verpackungs Reihenfolge für einheitliche Parameter ist standardmäßig auf Column-Major festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-178">Matrix packing order for uniform parameters is set to column-major by default.</span></span> <span data-ttu-id="e6b1f-179">Dies bedeutet, dass jede Spalte der Matrix in einem einzelnen Konstanten Register gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-179">This means each column of the matrix is stored in a single constant register.</span></span> <span data-ttu-id="e6b1f-180">Auf der anderen Seite verpackt eine Zeilen hauptmatrix jede Zeile der Matrix in einem einzelnen Konstanten Register.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-180">On the other hand, a row-major matrix packs each row of the matrix in a single constant register.</span></span> <span data-ttu-id="e6b1f-181">Die Matrix Verpackung kann mit der **\# pragmapack- \_ Matrix** Direktive oder mit dem Haupt Schlüsselwort der **Zeile \_** oder der **Spalte " \_ Major** " geändert werden.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-181">Matrix packing can be changed with the **\#pragmapack\_matrix** directive, or with the **row\_major** or the **column\_major** keyword.</span></span>

<span data-ttu-id="e6b1f-182">Die Daten in einer Matrix werden vor dem Ausführen eines Shaders in Shader-Konstante Register geladen.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-182">The data in a matrix is loaded into shader constant registers before a shader runs.</span></span> <span data-ttu-id="e6b1f-183">Es gibt zwei Möglichkeiten, wie die Matrix Daten gelesen werden: in Zeilen Hauptreihen Folge oder in Spalten Hauptreihen Folge.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-183">There are two choices for how the matrix data is read: in row-major order or in column-major order.</span></span> <span data-ttu-id="e6b1f-184">Die Spalten-Haupt Reihenfolge bedeutet, dass jede Matrix Spalte in einem einzelnen Konstanten Register gespeichert wird, und die Reihenfolge von Zeilen ist, dass jede Zeile der Matrix in einem einzigen konstanten Register gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-184">Column-major order means that each matrix column will be stored in a single constant register, and row-major order means that each row of the matrix will be stored in a single constant register.</span></span> <span data-ttu-id="e6b1f-185">Dies ist ein wichtiger Aspekt, wie viele Konstante Register für eine Matrix verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-185">This is an important consideration for how many constant registers are used for a matrix.</span></span>

<span data-ttu-id="e6b1f-186">Eine Zeilen hauptmatrix wird wie folgt angeordnet:</span><span class="sxs-lookup"><span data-stu-id="e6b1f-186">A row-major matrix is laid out like the following:</span></span>



|     |     |     |     |
|-----|-----|-----|-----|
| <span data-ttu-id="e6b1f-187">11</span><span class="sxs-lookup"><span data-stu-id="e6b1f-187">11</span></span>  | <span data-ttu-id="e6b1f-188">12</span><span class="sxs-lookup"><span data-stu-id="e6b1f-188">12</span></span>  | <span data-ttu-id="e6b1f-189">13</span><span class="sxs-lookup"><span data-stu-id="e6b1f-189">13</span></span>  | <span data-ttu-id="e6b1f-190">14</span><span class="sxs-lookup"><span data-stu-id="e6b1f-190">14</span></span>  |
| <span data-ttu-id="e6b1f-191">21</span><span class="sxs-lookup"><span data-stu-id="e6b1f-191">21</span></span>  | <span data-ttu-id="e6b1f-192">22</span><span class="sxs-lookup"><span data-stu-id="e6b1f-192">22</span></span>  | <span data-ttu-id="e6b1f-193">23</span><span class="sxs-lookup"><span data-stu-id="e6b1f-193">23</span></span>  | <span data-ttu-id="e6b1f-194">24</span><span class="sxs-lookup"><span data-stu-id="e6b1f-194">24</span></span>  |
| <span data-ttu-id="e6b1f-195">31</span><span class="sxs-lookup"><span data-stu-id="e6b1f-195">31</span></span>  | <span data-ttu-id="e6b1f-196">32</span><span class="sxs-lookup"><span data-stu-id="e6b1f-196">32</span></span>  | <span data-ttu-id="e6b1f-197">33</span><span class="sxs-lookup"><span data-stu-id="e6b1f-197">33</span></span>  | <span data-ttu-id="e6b1f-198">34</span><span class="sxs-lookup"><span data-stu-id="e6b1f-198">34</span></span>  |
| <span data-ttu-id="e6b1f-199">41</span><span class="sxs-lookup"><span data-stu-id="e6b1f-199">41</span></span>  | <span data-ttu-id="e6b1f-200">42</span><span class="sxs-lookup"><span data-stu-id="e6b1f-200">42</span></span>  | <span data-ttu-id="e6b1f-201">43</span><span class="sxs-lookup"><span data-stu-id="e6b1f-201">43</span></span>  | <span data-ttu-id="e6b1f-202">44</span><span class="sxs-lookup"><span data-stu-id="e6b1f-202">44</span></span>  |



 

<span data-ttu-id="e6b1f-203">Eine Spalten hauptmatrix wird wie folgt angeordnet:</span><span class="sxs-lookup"><span data-stu-id="e6b1f-203">A column-major matrix is laid out like the following:</span></span>



|     |     |     |     |
|-----|-----|-----|-----|
| <span data-ttu-id="e6b1f-204">11</span><span class="sxs-lookup"><span data-stu-id="e6b1f-204">11</span></span>  | <span data-ttu-id="e6b1f-205">21</span><span class="sxs-lookup"><span data-stu-id="e6b1f-205">21</span></span>  | <span data-ttu-id="e6b1f-206">31</span><span class="sxs-lookup"><span data-stu-id="e6b1f-206">31</span></span>  | <span data-ttu-id="e6b1f-207">41</span><span class="sxs-lookup"><span data-stu-id="e6b1f-207">41</span></span>  |
| <span data-ttu-id="e6b1f-208">12</span><span class="sxs-lookup"><span data-stu-id="e6b1f-208">12</span></span>  | <span data-ttu-id="e6b1f-209">22</span><span class="sxs-lookup"><span data-stu-id="e6b1f-209">22</span></span>  | <span data-ttu-id="e6b1f-210">32</span><span class="sxs-lookup"><span data-stu-id="e6b1f-210">32</span></span>  | <span data-ttu-id="e6b1f-211">42</span><span class="sxs-lookup"><span data-stu-id="e6b1f-211">42</span></span>  |
| <span data-ttu-id="e6b1f-212">13</span><span class="sxs-lookup"><span data-stu-id="e6b1f-212">13</span></span>  | <span data-ttu-id="e6b1f-213">23</span><span class="sxs-lookup"><span data-stu-id="e6b1f-213">23</span></span>  | <span data-ttu-id="e6b1f-214">33</span><span class="sxs-lookup"><span data-stu-id="e6b1f-214">33</span></span>  | <span data-ttu-id="e6b1f-215">43</span><span class="sxs-lookup"><span data-stu-id="e6b1f-215">43</span></span>  |
| <span data-ttu-id="e6b1f-216">14</span><span class="sxs-lookup"><span data-stu-id="e6b1f-216">14</span></span>  | <span data-ttu-id="e6b1f-217">24</span><span class="sxs-lookup"><span data-stu-id="e6b1f-217">24</span></span>  | <span data-ttu-id="e6b1f-218">34</span><span class="sxs-lookup"><span data-stu-id="e6b1f-218">34</span></span>  | <span data-ttu-id="e6b1f-219">44</span><span class="sxs-lookup"><span data-stu-id="e6b1f-219">44</span></span>  |



 

<span data-ttu-id="e6b1f-220">Zeilen-Haupt-und Spalten hauptmatrizen Reihenfolge bestimmt die Reihenfolge, in der die Matrixkomponenten aus shadereingaben gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-220">Row-major and column-major matrix ordering determine the order the matrix components are read from shader inputs.</span></span> <span data-ttu-id="e6b1f-221">Nachdem die Daten in Konstante Register geschrieben wurden, wirkt sich die Reihenfolge der Matrizen nicht darauf aus, wie die Daten im Shader-Code verwendet oder aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-221">Once the data is written into constant registers, matrix order has no effect on how the data is used or accessed from within shader code.</span></span> <span data-ttu-id="e6b1f-222">Außerdem werden in einem shadertext deklarierte Matrizen nicht in Konstante Register gepackt.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-222">Also, matrices declared in a shader body do not get packed into constant registers.</span></span> <span data-ttu-id="e6b1f-223">Die Reihenfolge der Zeilen-Haupt-und Spalten hauptverpackung hat keinen Einfluss auf die Komprimierungs Reihenfolge von Konstruktoren (die immer auf die Reihenfolge der Zeilen Hauptreihen folgen).</span><span class="sxs-lookup"><span data-stu-id="e6b1f-223">Row-major and column-major packing order has no influence on the packing order of constructors (which always follows row-major ordering).</span></span>

<span data-ttu-id="e6b1f-224">Die Reihenfolge der Daten in einer Matrix kann zur Kompilierzeit deklariert werden, oder der Compiler sortiert die Daten zur Laufzeit, um die effizienteste Verwendung zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-224">The order of the data in a matrix can be declared at compile time or the compiler will order the data at runtime for the most efficient use.</span></span>

## <a name="examples"></a><span data-ttu-id="e6b1f-225">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e6b1f-225">Examples</span></span>

<span data-ttu-id="e6b1f-226">HLSL verwendet zwei spezielle Typen, einen Vektortyp und einen Matrixtyp, um die Programmierung von 2D-und 3D-Grafiken zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-226">HLSL uses two special types, a vector type and a matrix type to make programming 2D and 3D graphics easier.</span></span> <span data-ttu-id="e6b1f-227">Jeder dieser Typen enthält mehr als eine Komponente. ein Vektor enthält bis zu vier Komponenten, und eine Matrix enthält bis zu 16 Komponenten.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-227">Each of these types contain more than one component; a vector contains up to four components, and a matrix contains up to 16 components.</span></span> <span data-ttu-id="e6b1f-228">Wenn Vektoren und Matrizen in standardmäßigen HLSL-Gleichungen verwendet werden, ist die durchgeführte Mathematik so konzipiert, dass Sie pro Komponente funktioniert.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-228">When vectors and matrices are used in standard HLSL equations, the math performed is designed to work per-component.</span></span> <span data-ttu-id="e6b1f-229">Beispielsweise implementiert HLSL diese Multiplikation:</span><span class="sxs-lookup"><span data-stu-id="e6b1f-229">For instance, HLSL implements this multiply:</span></span>


```
float4 v = a*b;
```



<span data-ttu-id="e6b1f-230">als eine Multiplikation mit vier Komponenten.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-230">as a four-component multiply.</span></span> <span data-ttu-id="e6b1f-231">Das Ergebnis sind vier skalare:</span><span class="sxs-lookup"><span data-stu-id="e6b1f-231">The result is four scalars:</span></span>


```
float4 v = a*b;

v.x = a.x*b.x;
v.y = a.y*b.y;
v.z = a.z*b.z;
v.w = a.w*b.w;
```



<span data-ttu-id="e6b1f-232">Dies sind vier Multiplikationen, bei denen jedes Ergebnis in einer separaten Komponente von v gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-232">This is four multiplications where each result is stored in a separate component of v.</span></span> <span data-ttu-id="e6b1f-233">Dies wird als vier-Komponenten-Multiplikation bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-233">This is called a four-component multiply.</span></span> <span data-ttu-id="e6b1f-234">HLSL verwendet die Komponente math, wodurch das Schreiben von Shader sehr effizient wird.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-234">HLSL uses component math which makes writing shaders very efficient.</span></span>

<span data-ttu-id="e6b1f-235">Dies unterscheidet sich sehr von einem multiplizieren, das in der Regel als ein Punktprodukt implementiert wird, das einen einzelnen Skalarwert generiert:</span><span class="sxs-lookup"><span data-stu-id="e6b1f-235">This is very different from a multiply which is typically implemented as a dot product which generates a single scalar:</span></span>


```
v = a.x*b.x + a.y*b.y + a.z*b.z + a.w*b.w;
```



<span data-ttu-id="e6b1f-236">Eine Matrix verwendet in HLSL auch Vorgänge pro Komponente:</span><span class="sxs-lookup"><span data-stu-id="e6b1f-236">A matrix also uses per-component operations in HLSL:</span></span>


```
float3x3 mat1,mat2;
...
float3x3 mat3 = mat1*mat2;
```



<span data-ttu-id="e6b1f-237">Das Ergebnis ist eine Multiplikation der beiden Matrizen pro Komponente (im Gegensatz zu einer standardmäßigen 3X3-Matrix Multiplikation).</span><span class="sxs-lookup"><span data-stu-id="e6b1f-237">The result is a per-component multiply of the two matrices (as opposed to a standard 3x3 matrix multiply).</span></span> <span data-ttu-id="e6b1f-238">Eine Matrix Multiplikation pro Komponente ergibt diesen ersten Begriff:</span><span class="sxs-lookup"><span data-stu-id="e6b1f-238">A per component matrix multiply yields this first term:</span></span>


```
mat3.m00 = mat1.m00 * mat2._m00;
```



<span data-ttu-id="e6b1f-239">Dies unterscheidet sich von einer 3X3-Matrix Multiplikation, die diesen ersten Begriff ergibt:</span><span class="sxs-lookup"><span data-stu-id="e6b1f-239">This is different from a 3x3 matrix multiply which would yield this first term:</span></span>


```
// First component of a four-component matrix multiply
mat.m00 = mat1._m00 * mat2._m00 + 
          mat1._m01 * mat2._m10 + 
          mat1._m02 * mat2._m20 + 
          mat1._m03 * mat2._m30;
```



<span data-ttu-id="e6b1f-240">Überladene Versionen der intrinsischen Funktion zum Multiplizieren von Funktionen, bei denen ein-Operand ein Vektor und der andere Operand eine Matrix ist.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-240">Overloaded versions of the multiply intrinsic function handle cases where one operand is a vector and the other operand is a matrix.</span></span> <span data-ttu-id="e6b1f-241">Beispielsweise: Vektor \* Vektor, Vektor \* Matrix, Matrix \* Vektor und Matrix \* Matrix.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-241">Such as: vector \* vector, vector \* matrix, matrix \* vector, and matrix \* matrix.</span></span> <span data-ttu-id="e6b1f-242">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="e6b1f-242">For instance:</span></span>


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



<span data-ttu-id="e6b1f-243">erzeugt das gleiche Ergebnis wie:</span><span class="sxs-lookup"><span data-stu-id="e6b1f-243">produces the same result as:</span></span>


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



<span data-ttu-id="e6b1f-244">In diesem Beispiel wird der POS-Vektor mithilfe der Umwandlung (float1x4) in einen Spalten Vektor umgewandelt.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-244">This example casts the pos vector to a column vector using the (float1x4) cast.</span></span> <span data-ttu-id="e6b1f-245">Das Ändern eines Vektors durch umwandeln oder Austauschen der Reihenfolge der zu multiplizierenden Argumente entspricht der Umsetzung der Matrix.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-245">Changing a vector by casting, or swapping the order of the arguments supplied to multiply is equivalent to transposing the matrix.</span></span>

<span data-ttu-id="e6b1f-246">Die automatische Umwandlung von Umwandlungen bewirkt, dass die intrinsischen Funktionen multiplizieren und Punkt dieselben Ergebnisse wie hier verwendet zurückgeben:</span><span class="sxs-lookup"><span data-stu-id="e6b1f-246">Automatic cast conversion causes the multiply and dot intrinsic functions to return the same results as used here:</span></span>


```
{
  float4 val;
  return mul(val,val);
}
```



<span data-ttu-id="e6b1f-247">Das Ergebnis der Multiplikation ist ein 1 x 4 \* 4 x 1 = 1x1-Vektor.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-247">This result of the multiply is a 1x4 \* 4x1 = 1x1 vector.</span></span> <span data-ttu-id="e6b1f-248">Dies entspricht einem Punktprodukt:</span><span class="sxs-lookup"><span data-stu-id="e6b1f-248">This is equivalent to a dot product:</span></span>


```
{
  float4 val;
  return dot(val,val);
}
```



<span data-ttu-id="e6b1f-249">, der einen einzelnen Skalarwert zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="e6b1f-249">which returns a single scalar value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6b1f-250">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e6b1f-250">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6b1f-251">Datentypen (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e6b1f-251">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 




