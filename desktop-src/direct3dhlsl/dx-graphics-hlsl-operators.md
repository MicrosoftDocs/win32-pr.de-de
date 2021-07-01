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
# <a name="operators"></a><span data-ttu-id="4e81b-103">Operatoren</span><span class="sxs-lookup"><span data-stu-id="4e81b-103">Operators</span></span>

<span data-ttu-id="4e81b-104">Ausdrücke sind Sequenzen von [Variablen und](dx-graphics-hlsl-variable-syntax.md) Literalen, die durch Operatoren [interpunktioniert werden.](dx-graphics-hlsl-statement-blocks.md)</span><span class="sxs-lookup"><span data-stu-id="4e81b-104">Expressions are sequences of [variables](dx-graphics-hlsl-variable-syntax.md) and literals punctuated by [operators](dx-graphics-hlsl-statement-blocks.md).</span></span> <span data-ttu-id="4e81b-105">Operatoren bestimmen, wie die Variablen und Literale kombiniert, verglichen, ausgewählt und so weiter.</span><span class="sxs-lookup"><span data-stu-id="4e81b-105">Operators determine how the variables and literals are combined, compared, selected, and so on.</span></span> <span data-ttu-id="4e81b-106">Zu den Operatoren gehören:</span><span class="sxs-lookup"><span data-stu-id="4e81b-106">The operators include:</span></span>



| <span data-ttu-id="4e81b-107">Operatorname</span><span class="sxs-lookup"><span data-stu-id="4e81b-107">Operator name</span></span>                                                                                | <span data-ttu-id="4e81b-108">Operatoren</span><span class="sxs-lookup"><span data-stu-id="4e81b-108">Operators</span></span>                                                                   |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="4e81b-109">Additive und multiplikative Operatoren</span><span class="sxs-lookup"><span data-stu-id="4e81b-109">Additive and Multiplicative Operators</span></span>](#additive-and-multiplicative-operators) | <span data-ttu-id="4e81b-110">+, -, \*, /, %</span><span class="sxs-lookup"><span data-stu-id="4e81b-110">+, -, \*, /, %</span></span>                                                     |
| [<span data-ttu-id="4e81b-111">Arrayoperator</span><span class="sxs-lookup"><span data-stu-id="4e81b-111">Array Operator</span></span>](#array-operator)                                               | <span data-ttu-id="4e81b-112">\[i\]</span><span class="sxs-lookup"><span data-stu-id="4e81b-112">\[i\]</span></span>                                                              |
| [<span data-ttu-id="4e81b-113">Zuweisungsoperatoren</span><span class="sxs-lookup"><span data-stu-id="4e81b-113">Assignment Operators</span></span>](#assignment-operators)                                   | <span data-ttu-id="4e81b-114">=, +=, -=, \*=, /=, %=</span><span class="sxs-lookup"><span data-stu-id="4e81b-114">=, +=, -=, \*=, /=, %=</span></span>                                             |
| [<span data-ttu-id="4e81b-115">Binäre Casts</span><span class="sxs-lookup"><span data-stu-id="4e81b-115">Binary Casts</span></span>](#binary-casts)                                                   | <span data-ttu-id="4e81b-116">C-Regeln für float und int, C-Regeln oder systeminterne HLSL-Regeln für bool</span><span class="sxs-lookup"><span data-stu-id="4e81b-116">C rules for float and int, C rules or HLSL intrinsics for bool</span></span>     |
| [<span data-ttu-id="4e81b-117">Bitwise Operators (Bitweise Operatoren)</span><span class="sxs-lookup"><span data-stu-id="4e81b-117">Bitwise Operators</span></span>](#bitwise-operators)                                         | <span data-ttu-id="4e81b-118">~, <<, >>, &, \| , ^, <<=, >>=, &=, \| =, ^=</span><span class="sxs-lookup"><span data-stu-id="4e81b-118">~, <<, >>, &, \|, ^, <<=, >>=, &=, \|=, ^=</span></span> |
| [<span data-ttu-id="4e81b-119">Boolesche mathematische Operatoren</span><span class="sxs-lookup"><span data-stu-id="4e81b-119">Boolean Math Operators</span></span>](#boolean-math-operators)                               | <span data-ttu-id="4e81b-120">& &, , \| \| ?:</span><span class="sxs-lookup"><span data-stu-id="4e81b-120">& &, \|\|, ?:</span></span>                                                      |
| [<span data-ttu-id="4e81b-121">Cast-Operator</span><span class="sxs-lookup"><span data-stu-id="4e81b-121">Cast Operator</span></span>](#cast-operator)                                                 | <span data-ttu-id="4e81b-122">(Typ)</span><span class="sxs-lookup"><span data-stu-id="4e81b-122">(type)</span></span>                                                             |
| [<span data-ttu-id="4e81b-123">Kommaoperator</span><span class="sxs-lookup"><span data-stu-id="4e81b-123">Comma Operator</span></span>](#comma-operator)                                               | <span data-ttu-id="4e81b-124">,</span><span class="sxs-lookup"><span data-stu-id="4e81b-124">,</span></span>                                                                  |
| [<span data-ttu-id="4e81b-125">Comparison Operators (Vergleichsoperatoren)</span><span class="sxs-lookup"><span data-stu-id="4e81b-125">Comparison Operators</span></span>](#comparison-operators)                                   | <span data-ttu-id="4e81b-126"><, >, ==, !=, <=, >=</span><span class="sxs-lookup"><span data-stu-id="4e81b-126"><, >, ==, !=, <=, >=</span></span>                                   |
| [<span data-ttu-id="4e81b-127">Präfix- oder Postfixoperatoren</span><span class="sxs-lookup"><span data-stu-id="4e81b-127">Prefix or Postfix Operators</span></span>](#prefix-or-postfix-operators)                     | <span data-ttu-id="4e81b-128">++, --</span><span class="sxs-lookup"><span data-stu-id="4e81b-128">++, --</span></span>                                                             |
| [<span data-ttu-id="4e81b-129">Structure-Operator</span><span class="sxs-lookup"><span data-stu-id="4e81b-129">Structure Operator</span></span>](#structure-operator)                                       | <span data-ttu-id="4e81b-130">.</span><span class="sxs-lookup"><span data-stu-id="4e81b-130">.</span></span>                                                                  |
| [<span data-ttu-id="4e81b-131">Unary Operators (Unäre Operatoren)</span><span class="sxs-lookup"><span data-stu-id="4e81b-131">Unary Operators</span></span>](#unary-operators)                                             | <span data-ttu-id="4e81b-132">!, -, +</span><span class="sxs-lookup"><span data-stu-id="4e81b-132">!, -, +</span></span>                                                            |



 

<span data-ttu-id="4e81b-133">Viele der Operatoren sind komponentenspezifische Operatoren, was bedeutet, dass der Vorgang unabhängig für jede Komponente jeder Variablen ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4e81b-133">Many of the operators are per-component, which means that the operation is performed independently for each component of each variable.</span></span> <span data-ttu-id="4e81b-134">Beispielsweise wird für eine einzelne Komponentenvariable ein Vorgang ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4e81b-134">For example, a single component variable has one operation performed.</span></span> <span data-ttu-id="4e81b-135">Andererseits werden für eine Variable mit vier Komponenten vier Vorgänge ausgeführt, eine für jede Komponente.</span><span class="sxs-lookup"><span data-stu-id="4e81b-135">On the other hand, a four-component variable has four operations performed, one for each component.</span></span>

<span data-ttu-id="4e81b-136">Alle Operatoren, die etwas mit dem Wert tun, z. B. + und \* , funktionieren pro Komponente.</span><span class="sxs-lookup"><span data-stu-id="4e81b-136">All of the operators that do something to the value, such as + and \*, work per component.</span></span>

<span data-ttu-id="4e81b-137">Die Vergleichsoperatoren erfordern, dass eine einzelne [](dx-graphics-hlsl-any.md) Komponente funktioniert, es sei denn, Sie verwenden die [**alle**](dx-graphics-hlsl-all.md) oder eine systeminterne Funktion mit einer Variablen mit mehreren Komponenten.</span><span class="sxs-lookup"><span data-stu-id="4e81b-137">The comparison operators require a single component to work unless you use the [**all**](dx-graphics-hlsl-all.md) or [**any**](dx-graphics-hlsl-any.md) intrinsic function with a multiple-component variable.</span></span> <span data-ttu-id="4e81b-138">Der folgende Vorgang schlägt fehl, da die if-Anweisung einen einzelnen Bool erfordert, aber einen bool4 empfängt:</span><span class="sxs-lookup"><span data-stu-id="4e81b-138">The following operation fails because the if statement requires a single bool but receives a bool4:</span></span>


```
if (A4 < B4)
```



<span data-ttu-id="4e81b-139">Die folgenden Vorgänge sind erfolgreich:</span><span class="sxs-lookup"><span data-stu-id="4e81b-139">The following operations succeed:</span></span>


```
if ( any(A4 < B4) )
if ( all(A4 < B4) )
```



<span data-ttu-id="4e81b-140">Die binären Cast-Operatoren [**asfloat**](dx-graphics-hlsl-asfloat.md), [**asint**](dx-graphics-hlsl-asint.md)und so weiter für die Arbeit pro Komponente, mit Ausnahme von [**asdouble,**](asdouble.md) deren spezielle Regeln dokumentiert sind.</span><span class="sxs-lookup"><span data-stu-id="4e81b-140">The binary cast operators [**asfloat**](dx-graphics-hlsl-asfloat.md), [**asint**](dx-graphics-hlsl-asint.md), and so on work per component except for [**asdouble**](asdouble.md) whose special rules are documented.</span></span>

<span data-ttu-id="4e81b-141">Auswahloperatoren wie Perioden-, Komma- und Arrayklammern funktionieren nicht pro Komponente.</span><span class="sxs-lookup"><span data-stu-id="4e81b-141">Selection operators like period, comma, and array brackets do not work per component.</span></span>

<span data-ttu-id="4e81b-142">Cast-Operatoren ändern die Anzahl der Komponenten.</span><span class="sxs-lookup"><span data-stu-id="4e81b-142">Cast operators change the number of components.</span></span> <span data-ttu-id="4e81b-143">Die folgenden Cast-Vorgänge zeigen ihre Äquivalenz:</span><span class="sxs-lookup"><span data-stu-id="4e81b-143">The following cast operations show their equivalence:</span></span>


```
(float) i4 ->   float(i4.x)
(float4)i ->   float4(i, i, i, i)
```



## <a name="additive-and-multiplicative-operators"></a><span data-ttu-id="4e81b-144">Additive und multiplikative Operatoren</span><span class="sxs-lookup"><span data-stu-id="4e81b-144">Additive and Multiplicative Operators</span></span>

<span data-ttu-id="4e81b-145">Die additiven und multiplikativen Operatoren sind: +, -, \* , /, %</span><span class="sxs-lookup"><span data-stu-id="4e81b-145">The additive and multiplicative operators are: +, -, \*, /, %</span></span>


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



<span data-ttu-id="4e81b-146">Der Modulusoperator gibt den Rest einer Division zurück.</span><span class="sxs-lookup"><span data-stu-id="4e81b-146">The modulus operator returns the remainder of a division.</span></span> <span data-ttu-id="4e81b-147">Dies führt zu unterschiedlichen Ergebnissen, wenn ganze Zahlen und Gleitkommazahlen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4e81b-147">This produces different results when using integers and floating-point numbers.</span></span> <span data-ttu-id="4e81b-148">Ganzzahlige Reste, die Bruchzahlen sind, werden abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="4e81b-148">Integer remainders that are fractional will be truncated.</span></span>


```
int i1 = 1;
int i2 = 2;
i3 = i1 % i2;      // i3 = remainder of 1/2, which is 1
i3 = i2 % i1;      // i3 = remainder of 2/1, which is 0
i3 = 5 % 2;        // i3 = remainder of 5/2, which is 1
i3 = 9 % 2;        // i3 = remainder of 9/2, which is 1
```



<span data-ttu-id="4e81b-149">Der Modulusoperator schneide einen Bruchteil des Rests ab, wenn ganze Zahlen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4e81b-149">The modulus operator truncates a fractional remainder when using integers.</span></span>


```
f3 = f1 % f2;      // f3 = remainder of 1.0/2.0, which is 0.5
f3 = f2 % f1;      // f3 = remainder of 2.0/1.0, which is 0.0
```



<span data-ttu-id="4e81b-150">Der %-Operator wird nur in Fällen definiert, in denen beide Seiten positiv oder beide Seiten negativ sind.</span><span class="sxs-lookup"><span data-stu-id="4e81b-150">The % operator is defined only in cases where either both sides are positive or both sides are negative.</span></span> <span data-ttu-id="4e81b-151">Im Gegensatz zu C funktioniert es auch mit Gleitkommadatentypen sowie ganzen Zahlen.</span><span class="sxs-lookup"><span data-stu-id="4e81b-151">Unlike C, it also operates on floating-point data types, as well as integers.</span></span>

## <a name="array-operator"></a><span data-ttu-id="4e81b-152">Arrayoperator</span><span class="sxs-lookup"><span data-stu-id="4e81b-152">Array Operator</span></span>

<span data-ttu-id="4e81b-153">Der Array-Memberauswahloperator " \[ i " wählt eine oder mehrere Komponenten in einem Array \] aus.</span><span class="sxs-lookup"><span data-stu-id="4e81b-153">The array member selection operator "\[i\]" selects one or more components in an array.</span></span> <span data-ttu-id="4e81b-154">Es handelt sich um eine Gruppe von eckigen Klammern, die einen nullbasierten Index enthalten.</span><span class="sxs-lookup"><span data-stu-id="4e81b-154">It is a set of square brackets that contain a zero-based index.</span></span>


```
int arrayOfInts[4] = { 0,1,2,3 };
arrayOfInts[0] = 2;
arrayOfInts[1] = arrayOfInts[0];
```



<span data-ttu-id="4e81b-155">Der Arrayoperator kann auch für den Zugriff auf einen Vektor verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4e81b-155">The array operator can also be used to access a vector.</span></span>


```
float4 4D_Vector = { 0.0f, 1.0f, 2.0f, 3.0f  };         
float 1DFloat = 4D_Vector[1];          // 1.0f
```



<span data-ttu-id="4e81b-156">Durch Hinzufügen eines zusätzlichen Indexes kann der Arrayoperator auch auf eine Matrix zugreifen.</span><span class="sxs-lookup"><span data-stu-id="4e81b-156">By adding an additional index, the array operator can also access a matrix.</span></span>


```
float4x4 mat4x4 = {{0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} };
mat4x4[0][1] = 1.1f;
float 1DFloat = mat4x4[0][1];      // 0.0f
```



<span data-ttu-id="4e81b-157">Der erste Index ist der nullbasierte Zeilenindex.</span><span class="sxs-lookup"><span data-stu-id="4e81b-157">The first index is the zero-based row index.</span></span> <span data-ttu-id="4e81b-158">Der zweite Index ist der nullbasierte Spaltenindex.</span><span class="sxs-lookup"><span data-stu-id="4e81b-158">The second index is the zero-based column index.</span></span>

## <a name="assignment-operators"></a><span data-ttu-id="4e81b-159">Zuweisungsoperatoren</span><span class="sxs-lookup"><span data-stu-id="4e81b-159">Assignment Operators</span></span>

<span data-ttu-id="4e81b-160">Die Zuweisungsoperatoren sind: =, +=, -=, \* =, /=</span><span class="sxs-lookup"><span data-stu-id="4e81b-160">The assignment operators are: =, +=, -=, \*=, /=</span></span>

<span data-ttu-id="4e81b-161">Variablen können Literalwerte zugewiesen werden:</span><span class="sxs-lookup"><span data-stu-id="4e81b-161">Variables can be assigned literal values:</span></span>


```
int i = 1;            
float f2 = 3.1f; 
bool b = false;
string str = "string";
```



<span data-ttu-id="4e81b-162">Variablen können auch das Ergebnis einer mathematischen Operation zugewiesen werden:</span><span class="sxs-lookup"><span data-stu-id="4e81b-162">Variables can also be assigned the result of a mathematical operation:</span></span>


```
int i1 = 1;
i1 += 2;           // i1 = 1 + 2 = 3
```



<span data-ttu-id="4e81b-163">Eine Variable kann auf beiden Seiten des Gleichheitszeichens verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="4e81b-163">A variable can be used on either side of the equals sign:</span></span>


```
float f3 = 0.5f;
f3 *= f3;          // f3 = 0.5 * 0.5 = 0.25
```



<span data-ttu-id="4e81b-164">Die Division für Gleitkommavariablen ist wie erwartet, da dezimale Reste kein Problem darstellen.</span><span class="sxs-lookup"><span data-stu-id="4e81b-164">Division for floating-point variables is as expected because decimal remainders are not a problem.</span></span>


```
float f1 = 1.0;
f1 /= 3.0f;        // f1 = 1.0/3.0 = 0.333
```



<span data-ttu-id="4e81b-165">Seien Sie vorsichtig, wenn Sie ganze Zahlen verwenden, die geteilt werden können, insbesondere, wenn das Ergebnis durch Abschneiden beeinträchtigt wird.</span><span class="sxs-lookup"><span data-stu-id="4e81b-165">Be careful if you are using integers that may get divided, especially when truncation affects the result.</span></span> <span data-ttu-id="4e81b-166">Dieses Beispiel ist mit dem vorherigen Beispiel identisch, mit Ausnahme des -Datentyps.</span><span class="sxs-lookup"><span data-stu-id="4e81b-166">This example is identical to the previous example, except for the data type.</span></span> <span data-ttu-id="4e81b-167">Die Kürzung führt zu einem sehr anderen Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="4e81b-167">The truncation causes a very different result.</span></span>


```
int i1 = 1;
i1 /= 3;           // i1 = 1/3 = 0.333, which gets truncated to 0
```



## <a name="binary-casts"></a><span data-ttu-id="4e81b-168">Binäre Casts</span><span class="sxs-lookup"><span data-stu-id="4e81b-168">Binary Casts</span></span>

<span data-ttu-id="4e81b-169">Der Umwandlungsvorgang zwischen int und float konvertiert den numerischen Wert gemäß C-Regeln zum Abschneiden eines int-Typs in die entsprechenden Darstellungen.</span><span class="sxs-lookup"><span data-stu-id="4e81b-169">Casting operation between int and float will convert the numeric value into the appropriate representations following C rules for truncating an int type.</span></span> <span data-ttu-id="4e81b-170">Die Umwandlung eines Werts von einem float-Wert in einen int-Wert und zurück in einen float-Wert führt zu einer verlustberatenden Konvertierung basierend auf der Genauigkeit des Ziels.</span><span class="sxs-lookup"><span data-stu-id="4e81b-170">Casting a value from a float to an int and back to a float will result in a lossy conversion based on the precision of the target.</span></span>

<span data-ttu-id="4e81b-171">Binäre Casts können auch mit systeminternen Funktionen [**(DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)ausgeführt werden, die die Bitdarstellung einer Zahl in den Zieldatentyp neu interpretiert.</span><span class="sxs-lookup"><span data-stu-id="4e81b-171">Binary casts may also be performed using [**Intrinsic Functions (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md), which reinterpret the bit representation of a number into the target data type.</span></span>


```
asfloat() // Cast to float
asint()   // Cast to int 
asuint()  // Cast to uint
```



## <a name="bitwise-operators"></a><span data-ttu-id="4e81b-172">Bitweise Operatoren</span><span class="sxs-lookup"><span data-stu-id="4e81b-172">Bitwise Operators</span></span>

<span data-ttu-id="4e81b-173">HLSL unterstützt die folgenden bitweise Operatoren, die im Hinblick auf andere Operatoren der gleichen Rangfolge wie C folgen.</span><span class="sxs-lookup"><span data-stu-id="4e81b-173">HLSL supports the following bitwise operators, which follow the same precedence as C with regard to other operators.</span></span> <span data-ttu-id="4e81b-174">In der folgenden Tabelle werden die Operatoren beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4e81b-174">The following table describes the operators.</span></span>

> [!Note]  
> <span data-ttu-id="4e81b-175">Bitweise Operatoren erfordern Shader model 4 0 with Direct3D 10 and higher hardware [(Shadermodell 4 \_ 0](dx-graphics-hlsl-sm4.md) mit Direct3D 10 und höher).</span><span class="sxs-lookup"><span data-stu-id="4e81b-175">Bitwise operators require [Shader Model 4\_0](dx-graphics-hlsl-sm4.md) with Direct3D 10 and higher hardware.</span></span>

 



| <span data-ttu-id="4e81b-176">Operator</span><span class="sxs-lookup"><span data-stu-id="4e81b-176">Operator</span></span>          |  <span data-ttu-id="4e81b-177">Funktion</span><span class="sxs-lookup"><span data-stu-id="4e81b-177">Function</span></span>                 |
|-----------|-------------------|
| ~         | <span data-ttu-id="4e81b-178">Logical Not</span><span class="sxs-lookup"><span data-stu-id="4e81b-178">Logical Not</span></span>       |
| <<  | <span data-ttu-id="4e81b-179">Linksverschiebung</span><span class="sxs-lookup"><span data-stu-id="4e81b-179">Left Shift</span></span>        |
| >>  | <span data-ttu-id="4e81b-180">Rechtsverschiebung</span><span class="sxs-lookup"><span data-stu-id="4e81b-180">Right Shift</span></span>       |
| &         | <span data-ttu-id="4e81b-181">Logisches UND</span><span class="sxs-lookup"><span data-stu-id="4e81b-181">Logical And</span></span>       |
| \|        | <span data-ttu-id="4e81b-182">Logisches ODER.</span><span class="sxs-lookup"><span data-stu-id="4e81b-182">Logical Or</span></span>        |
| ^         | <span data-ttu-id="4e81b-183">Logisches Xor</span><span class="sxs-lookup"><span data-stu-id="4e81b-183">Logical Xor</span></span>       |
| <<= | <span data-ttu-id="4e81b-184">Left Shift Equal</span><span class="sxs-lookup"><span data-stu-id="4e81b-184">Left Shift Equal</span></span>  |
| >>= | <span data-ttu-id="4e81b-185">Rechtsverschiebung gleich</span><span class="sxs-lookup"><span data-stu-id="4e81b-185">Right Shift Equal</span></span> |
| &=        | <span data-ttu-id="4e81b-186">Und gleich</span><span class="sxs-lookup"><span data-stu-id="4e81b-186">And Equal</span></span>         |
| \|=       | <span data-ttu-id="4e81b-187">Oder gleich</span><span class="sxs-lookup"><span data-stu-id="4e81b-187">Or Equal</span></span>          |
| ^=        | <span data-ttu-id="4e81b-188">Xor Equal</span><span class="sxs-lookup"><span data-stu-id="4e81b-188">Xor Equal</span></span>         |



 

<span data-ttu-id="4e81b-189">Bitweise Operatoren werden so definiert, dass sie nur für int- und uint-Datentypen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4e81b-189">Bitwise operators are defined to operate only on int and uint data types.</span></span> <span data-ttu-id="4e81b-190">Der Versuch, bitweise Operatoren für float- oder struct-Datentypen zu verwenden, führt zu einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="4e81b-190">Attempting to use bitwise operators on float, or struct data types will result in an error.</span></span>

## <a name="boolean-math-operators"></a><span data-ttu-id="4e81b-191">Boolesche mathematische Operatoren</span><span class="sxs-lookup"><span data-stu-id="4e81b-191">Boolean Math Operators</span></span>

<span data-ttu-id="4e81b-192">Die booleschen mathematischen Operatoren sind: &&, \| \| , ?:</span><span class="sxs-lookup"><span data-stu-id="4e81b-192">The Boolean math operators are: &&, \|\|, ?:</span></span>


```
bool b1 = true;
bool b2 = false;
bool b3 = b1 && b2 // b3 = true AND false = false
b3 = b1 || b2                // b3 = true OR false = true
```



<span data-ttu-id="4e81b-193">Im Gegensatz zur Kurzschlussauswertung von &&, und ?: in C werden \| HLSL-Ausdrücke eine Auswertung nie kurzschalten, da es sich um \| Vektoroperationen handelt.</span><span class="sxs-lookup"><span data-stu-id="4e81b-193">Unlike short-circuit evaluation of &&, \|\|, and ?: in C, HLSL expressions never short-circuit an evaluation because they are vector operations.</span></span> <span data-ttu-id="4e81b-194">Alle Seiten des Ausdrucks werden immer ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="4e81b-194">All sides of the expression are always evaluated.</span></span>

<span data-ttu-id="4e81b-195">Boolesche Operatoren funktionieren pro Komponente.</span><span class="sxs-lookup"><span data-stu-id="4e81b-195">Boolean operators function on a per-component basis.</span></span> <span data-ttu-id="4e81b-196">Wenn Sie also zwei Vektoren vergleichen, ist das Ergebnis ein Vektor, der das boolesche Ergebnis des Vergleichs für jede Komponente enthält.</span><span class="sxs-lookup"><span data-stu-id="4e81b-196">This means that if you compare two vectors, the result is a vector containing the Boolean result of the comparison for each component.</span></span>

<span data-ttu-id="4e81b-197">Bei Ausdrücken, die boolesche Operatoren verwenden, werden die Größe und der Komponententyp jeder Variablen vor dem Auftreten des Vorgangs auf denselben Wert auf denselben Wert 2016 hinaus 2016 2016 und 2016 auf den gleichen Wert 12.0(n) des Typs der einzelnen Variablen um 10000000000000</span><span class="sxs-lookup"><span data-stu-id="4e81b-197">For expressions that use Boolean operators, the size and component type of each variable are promoted to be the same before the operation occurs.</span></span> <span data-ttu-id="4e81b-198">Der promoted-Typ bestimmt die Auflösung, bei der der Vorgang stattfindet, sowie den Ergebnistyp des Ausdrucks.</span><span class="sxs-lookup"><span data-stu-id="4e81b-198">The promoted type determines the resolution at which the operation takes place, as well as the result type of the expression.</span></span> <span data-ttu-id="4e81b-199">Beispielsweise würde ein int3 + float-Ausdruck zur Auswertung auf float3 + float3 und das Ergebnis vom Typ float3 werden.</span><span class="sxs-lookup"><span data-stu-id="4e81b-199">For example an int3 + float expression would be promoted to float3 + float3 for evaluation, and its result would be of type float3.</span></span>

## <a name="cast-operator"></a><span data-ttu-id="4e81b-200">Umwandlungsoperator</span><span class="sxs-lookup"><span data-stu-id="4e81b-200">Cast Operator</span></span>

<span data-ttu-id="4e81b-201">Ein Ausdruck, dem ein Typname in Klammern voran steht, ist eine explizite Typ cast.</span><span class="sxs-lookup"><span data-stu-id="4e81b-201">An expression preceded by a type name in parenthesis is an explicit type cast.</span></span> <span data-ttu-id="4e81b-202">Eine Typ cast konvertiert den ursprünglichen Ausdruck in den Datentyp der Umwandlung.</span><span class="sxs-lookup"><span data-stu-id="4e81b-202">A type cast converts the original expression to the data type of the cast.</span></span> <span data-ttu-id="4e81b-203">Im Allgemeinen können die einfachen Datentypen in komplexere Datentypen umgewandelt werden (mit einer Heraufstufungscast), aber nur einige komplexe Datentypen können in einfache Datentypen umgewandelt werden (mit einer Herabstufungscast).</span><span class="sxs-lookup"><span data-stu-id="4e81b-203">In general, the simple data types can be cast to the more complex data types (with a promotion cast), but only some complex data types can be cast into simple data types (with a demotion cast).</span></span>

<span data-ttu-id="4e81b-204">Nur die typisierte Umwandlung auf der rechten Seite ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="4e81b-204">Only right hand side type casting is legal.</span></span> <span data-ttu-id="4e81b-205">Beispielsweise sind Ausdrücke wie `(int)myFloat = myInt;` ungültig.</span><span class="sxs-lookup"><span data-stu-id="4e81b-205">For example, expressions such as `(int)myFloat = myInt;` are illegal.</span></span> <span data-ttu-id="4e81b-206">Verwenden Sie stattdessen `myFloat = (float)myInt;`.</span><span class="sxs-lookup"><span data-stu-id="4e81b-206">Use `myFloat = (float)myInt;` instead.</span></span>

<span data-ttu-id="4e81b-207">Der Compiler führt auch eine implizite Typcasting durch.</span><span class="sxs-lookup"><span data-stu-id="4e81b-207">The compiler also performs implicit type cast.</span></span> <span data-ttu-id="4e81b-208">Beispielsweise sind die folgenden beiden Ausdrücke gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="4e81b-208">For example, the following two expressions are equivalent:</span></span>


```
int2 b = int2(1,2) + 2;
int2 b = int2(1,2) + int2(2,2);
```



## <a name="comma-operator"></a><span data-ttu-id="4e81b-209">Kommaoperator</span><span class="sxs-lookup"><span data-stu-id="4e81b-209">Comma Operator</span></span>

<span data-ttu-id="4e81b-210">Der Kommaoperator (,) trennt einen oder mehrere Ausdrücke, die in der Reihenfolge ausgewertet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4e81b-210">The comma operator (,) separates one or more expressions that are to be evaluated in order.</span></span> <span data-ttu-id="4e81b-211">Der Wert des letzten Ausdrucks in der Sequenz wird als Wert der Sequenz verwendet.</span><span class="sxs-lookup"><span data-stu-id="4e81b-211">The value of the last expression in the sequence is used as the value of the sequence.</span></span>

<span data-ttu-id="4e81b-212">Hier sehen Sie einen Fall, auf den Sie achten müssen.</span><span class="sxs-lookup"><span data-stu-id="4e81b-212">Here is one case worth calling attention to.</span></span> <span data-ttu-id="4e81b-213">Wenn der Konstruktortyp versehentlich von der rechten Seite des Gleichheitszeichens weggelassen wird, enthält die rechte Seite jetzt vier Ausdrücke, die durch drei Kommas getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="4e81b-213">If the constructor type is accidentally left off the right side of the equals sign, the right side now contains four expressions, separated by three commas.</span></span>


```
// Instead of using a constructor
float4 x = float4(0,0,0,1); 

// The type on the right side is accidentally left off
float4 x = (0,0,0,1); 
```



<span data-ttu-id="4e81b-214">Der Kommaoperator wertet einen Ausdruck von links nach rechts aus.</span><span class="sxs-lookup"><span data-stu-id="4e81b-214">The comma operator evaluates an expression from left to right.</span></span> <span data-ttu-id="4e81b-215">Dadurch wird die rechte Seite auf Folgendes reduziert:</span><span class="sxs-lookup"><span data-stu-id="4e81b-215">This reduces the right hand side to:</span></span>


```
float4 x = 1; 
```



<span data-ttu-id="4e81b-216">HLSL verwendet in diesem Fall eine skalare Heraufstufung, sodass das Ergebnis so lautet, als ob dies wie folgt geschrieben worden wäre:</span><span class="sxs-lookup"><span data-stu-id="4e81b-216">HLSL uses scalar promotion in this case, so the result is as if this were written as follows:</span></span>


```
float4 x = float4(1,1,1,1);
```



<span data-ttu-id="4e81b-217">In diesem Fall ist das Verlassen des float4-Typs von der rechten Seite wahrscheinlich ein Fehler, den der Compiler nicht erkennen kann, da dies eine gültige Anweisung ist.</span><span class="sxs-lookup"><span data-stu-id="4e81b-217">In this instance, leaving off the float4 type from the right side is probably a mistake that the compiler is unable to detect because this is a valid statement.</span></span>

## <a name="comparison-operators"></a><span data-ttu-id="4e81b-218">Vergleichsoperatoren</span><span class="sxs-lookup"><span data-stu-id="4e81b-218">Comparison Operators</span></span>

<span data-ttu-id="4e81b-219">Die Vergleichsoperatoren sind: <, >, ==, !=, <=, >=.</span><span class="sxs-lookup"><span data-stu-id="4e81b-219">The comparison operators are: <, >, ==, !=, <=, >=.</span></span>

<span data-ttu-id="4e81b-220">Vergleichen Sie Werte, die größer (oder kleiner als) eines beliebigen Skalarwerts sind:</span><span class="sxs-lookup"><span data-stu-id="4e81b-220">Compare values that are greater than (or less than) any scalar value:</span></span>


```
if( dot(lightDirection, normalVector) > 0 )
   // Do something; the face is lit
```




```
if( dot(lightDirection, normalVector) < 0 )
   // Do nothing; the face is backwards
```



<span data-ttu-id="4e81b-221">Oder vergleichen Sie Werte, die einem beliebigen Skalarwert entsprechen (oder nicht gleich sind):</span><span class="sxs-lookup"><span data-stu-id="4e81b-221">Or, compare values equal to (or not equal to) any scalar value:</span></span>


```
if(color.a == 0)
   // Skip processing because the face is invisible

if(color.a != 0)
   // Blend two colors together using the alpha value
```



<span data-ttu-id="4e81b-222">Sie können auch sowohl - als auch -Vergleichswerte kombinieren, die größer oder gleich (oder kleiner als oder gleich) eines beliebigen Skalarwerts sind:</span><span class="sxs-lookup"><span data-stu-id="4e81b-222">Or combine both and compare values that are greater than or equal to (or less than or equal to) any scalar value:</span></span>


```
if( position.z >= oldPosition.z )
   // Skip the new face because it is behind the existing face
```




```
if( currentValue <= someInitialCondition )
   // Reset the current value to its initial condition
```



<span data-ttu-id="4e81b-223">Jeder dieser Vergleiche kann mit einem beliebigen skalaren Datentyp durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="4e81b-223">Each of these comparisons can be done with any scalar data type.</span></span>

<span data-ttu-id="4e81b-224">Um Vergleichsoperatoren mit Vektor- und Matrixtypen zu verwenden, verwenden Sie die [**all-**](dx-graphics-hlsl-all.md) oder [**eine beliebige**](dx-graphics-hlsl-any.md) systeminterne Funktion.</span><span class="sxs-lookup"><span data-stu-id="4e81b-224">To use comparison operators with vector and matrix types, use the [**all**](dx-graphics-hlsl-all.md) or [**any**](dx-graphics-hlsl-any.md) intrinsic function.</span></span>

<span data-ttu-id="4e81b-225">Dieser Vorgang schlägt fehl, da die if-Anweisung eine einzelne bool erfordert, aber bool4 empfängt:</span><span class="sxs-lookup"><span data-stu-id="4e81b-225">This operation fails because the if statement requires a single bool but receives a bool4:</span></span>


```
if (A4 < B4)
```



<span data-ttu-id="4e81b-226">Diese Vorgänge sind erfolgreich:</span><span class="sxs-lookup"><span data-stu-id="4e81b-226">These operations succeed:</span></span>


```
if ( any(A4 < B4) )
if ( all(A4 < B4) )
```



## <a name="prefix-or-postfix-operators"></a><span data-ttu-id="4e81b-227">Präfix- oder Postfixoperatoren</span><span class="sxs-lookup"><span data-stu-id="4e81b-227">Prefix or Postfix Operators</span></span>

<span data-ttu-id="4e81b-228">Die Präfix- und Postfixoperatoren sind: ++, --.</span><span class="sxs-lookup"><span data-stu-id="4e81b-228">The prefix and postfix operators are: ++, --.</span></span> <span data-ttu-id="4e81b-229">Präfixoperatoren ändern den Inhalt der Variablen, bevor der Ausdruck ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="4e81b-229">Prefix operators change the contents of the variable before the expression is evaluated.</span></span> <span data-ttu-id="4e81b-230">Postfixoperatoren ändern den Inhalt der Variablen, nachdem der Ausdruck ausgewertet wurde.</span><span class="sxs-lookup"><span data-stu-id="4e81b-230">Postfix operators change the contents of the variable after the expression is evaluated.</span></span>

<span data-ttu-id="4e81b-231">In diesem Fall verwendet eine Schleife den Inhalt von i, um die Schleifenanzahl nachzuverfolgen.</span><span class="sxs-lookup"><span data-stu-id="4e81b-231">In this case, a loop uses the contents of i to keep track of the loop count.</span></span>


```
float4 arrayOfFloats[4] = { 1.0f, 2.0f, 3.0f, 4.4f };

for (int i = 0; i<4; )
{
    arrayOfFloats[i++] *= 2; 
}
```



<span data-ttu-id="4e81b-232">Da der Postfixinkrementoperator (++) verwendet wird, wird arrayOfFloats \[ i \] mit 2 multipliziert, bevor i erhöht wird.</span><span class="sxs-lookup"><span data-stu-id="4e81b-232">Because the postfix increment operator (++) is used, arrayOfFloats\[i\] is multiplied by 2 before i is incremented.</span></span> <span data-ttu-id="4e81b-233">Dies kann leicht neu angeordnet werden, um den Präfixinkrementoperator zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="4e81b-233">This could be slightly rearranged to use the prefix increment operator.</span></span> <span data-ttu-id="4e81b-234">Dies ist schwieriger zu lesen, obwohl beide Beispiele gleichwertig sind.</span><span class="sxs-lookup"><span data-stu-id="4e81b-234">This one is harder to read, although both examples are equivalent.</span></span>


```
float4 arrayOfFloats[4] = { 1.0f, 2.0f, 3.0f, 4.4f };

for (int i = 0; i<4; )
{
    arrayOfFloats[++i - 1] *= 2; 
}
```



<span data-ttu-id="4e81b-235">Da der Präfixoperator (++) verwendet wird, wird arrayOfFloats \[ i+1 - 1 \] mit 2 multipliziert, nachdem i erhöht wurde.</span><span class="sxs-lookup"><span data-stu-id="4e81b-235">Because the prefix operator (++) is used, arrayOfFloats\[i+1 - 1\] is multiplied by 2 after i is incremented.</span></span>

<span data-ttu-id="4e81b-236">Der Präfixdekrementoperator und der Postfixdekrementoperator (--) werden in derselben Sequenz wie der Inkrementoperator angewendet.</span><span class="sxs-lookup"><span data-stu-id="4e81b-236">The prefix decrement and postfix decrement operator (--) are applied in the same sequence as the increment operator.</span></span> <span data-ttu-id="4e81b-237">Der Unterschied besteht darin, dass die Dekrementierung 1 subtrahiert, anstatt 1 hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="4e81b-237">The difference is that decrement subtracts 1 instead of adding 1.</span></span>

## <a name="structure-operator"></a><span data-ttu-id="4e81b-238">Structure-Operator</span><span class="sxs-lookup"><span data-stu-id="4e81b-238">Structure Operator</span></span>

<span data-ttu-id="4e81b-239">Der Strukturmemberauswahloperator (.) ist ein Punkt.</span><span class="sxs-lookup"><span data-stu-id="4e81b-239">The structure member selection operator (.) is a period.</span></span> <span data-ttu-id="4e81b-240">Mit dieser Struktur:</span><span class="sxs-lookup"><span data-stu-id="4e81b-240">Given this structure:</span></span>


```
struct position
{
float4 x;
float4 y;
float4 z;
};
```



<span data-ttu-id="4e81b-241">Sie kann wie folgt gelesen werden:</span><span class="sxs-lookup"><span data-stu-id="4e81b-241">It can be read like this:</span></span>


```
struct position pos = { 1,2,3 };

float 1D_Float = pos.x
1D_Float = pos.y
```



<span data-ttu-id="4e81b-242">Jeder Member kann mit dem Strukturoperator gelesen oder geschrieben werden:</span><span class="sxs-lookup"><span data-stu-id="4e81b-242">Each member can be read or written with the structure operator:</span></span>


```
struct position pos = { 1,2,3 };
pos.x = 2.0f;
pos.z = 1.0f;       // z = 1.0f
pos.z = pos.x      // z = 2.0f
```



## <a name="unary-operators"></a><span data-ttu-id="4e81b-243">Unäre Operatoren</span><span class="sxs-lookup"><span data-stu-id="4e81b-243">Unary Operators</span></span>

<span data-ttu-id="4e81b-244">Die unären Operatoren sind: !, -, +</span><span class="sxs-lookup"><span data-stu-id="4e81b-244">The unary operators are: !, -, +</span></span>

<span data-ttu-id="4e81b-245">Unäre Operatoren arbeiten mit einem einzelnen Operanden.</span><span class="sxs-lookup"><span data-stu-id="4e81b-245">Unary operators operate on a single operand.</span></span>


```
bool b = false;
bool b2 = !b;      // b2 = true
int i = 2;
int i2 = -i;       // i2 = -2
int j = +i2;       // j = +2
```



## <a name="operator-precedence"></a><span data-ttu-id="4e81b-246">Operatorrangfolge</span><span class="sxs-lookup"><span data-stu-id="4e81b-246">Operator Precedence</span></span>

<span data-ttu-id="4e81b-247">Wenn ein Ausdruck mehrere Operatoren enthält, bestimmt die Operatorrangfolge die Reihenfolge der Auswertung.</span><span class="sxs-lookup"><span data-stu-id="4e81b-247">When an expression contains more than one operator, operator precedence determines the order of evaluation.</span></span> <span data-ttu-id="4e81b-248">Die Operatorrangfolge für HLSL folgt der gleichen Rangfolge wie C.</span><span class="sxs-lookup"><span data-stu-id="4e81b-248">Operator precedence for HLSL follows the same precedence as C.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e81b-249">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4e81b-249">Remarks</span></span>

<span data-ttu-id="4e81b-250">Geschweifte Klammern {,} () starten und beenden einen Anweisungsblock.</span><span class="sxs-lookup"><span data-stu-id="4e81b-250">Curly braces ({,}) start and end a statement block.</span></span> <span data-ttu-id="4e81b-251">Wenn ein Anweisungsblock eine einzelne Anweisung verwendet, sind die geschweiften Klammern optional.</span><span class="sxs-lookup"><span data-stu-id="4e81b-251">When a statement block uses a single statement, the curly braces are optional.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4e81b-252">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4e81b-252">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e81b-253">Anweisungen (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4e81b-253">Statements (DirectX HLSL)</span></span>](dx-graphics-hlsl-statements.md)
</dt> </dl>

 

 




