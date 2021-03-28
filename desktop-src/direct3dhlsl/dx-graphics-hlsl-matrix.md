---
title: Matrixtyp
description: Eine Matrix ist ein spezieller Datentyp, der zwischen einer und sechzehn Komponenten enthält. Jede Komponente einer Matrix muss denselben Typ aufweisen.
ms.assetid: 728eb472-103d-4c7f-b6f6-e515fc024801
keywords:
- Matrixtyp "HLSL"
topic_type:
- apiref
api_name:
- Matrix Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c580706a2ddae3e4a94c138a1ca0f6932457732a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104037772"
---
# <a name="matrix-type"></a><span data-ttu-id="b8dfe-105">Matrixtyp</span><span class="sxs-lookup"><span data-stu-id="b8dfe-105">Matrix Type</span></span>

<span data-ttu-id="b8dfe-106">Eine Matrix ist ein spezieller Datentyp, der zwischen einer und sechzehn Komponenten enthält.</span><span class="sxs-lookup"><span data-stu-id="b8dfe-106">A matrix is a special data type that contains between one and sixteen components.</span></span> <span data-ttu-id="b8dfe-107">Jede Komponente einer Matrix muss denselben Typ aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b8dfe-107">Every component of a matrix must be of the same type.</span></span>



|                         |
|-------------------------|
| <span data-ttu-id="b8dfe-108">**Typecomponents-Name**</span><span class="sxs-lookup"><span data-stu-id="b8dfe-108">**TypeComponents Name**</span></span> |



 

## <a name="components"></a><span data-ttu-id="b8dfe-109">Komponenten</span><span class="sxs-lookup"><span data-stu-id="b8dfe-109">Components</span></span>



| <span data-ttu-id="b8dfe-110">Element</span><span class="sxs-lookup"><span data-stu-id="b8dfe-110">Item</span></span>                                                                                                                             | <span data-ttu-id="b8dfe-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b8dfe-111">Description</span></span>                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8dfe-112"><span id="TypeComponents"></span><span id="typecomponents"></span><span id="TYPECOMPONENTS"></span>**Typecomponents**</span><span class="sxs-lookup"><span data-stu-id="b8dfe-112"><span id="TypeComponents"></span><span id="typecomponents"></span><span id="TYPECOMPONENTS"></span>**TypeComponents**</span></span><br/> | <span data-ttu-id="b8dfe-113">Ein einzelner Name, der drei Teile enthält.</span><span class="sxs-lookup"><span data-stu-id="b8dfe-113">A single name that contains three parts.</span></span> <span data-ttu-id="b8dfe-114">Der erste Teil ist einer der [skalaren](dx-graphics-hlsl-data-types.md) Typen.</span><span class="sxs-lookup"><span data-stu-id="b8dfe-114">The first part is one of the [scalar](dx-graphics-hlsl-data-types.md) types.</span></span> <span data-ttu-id="b8dfe-115">Der zweite Teil ist die Anzahl der Zeilen.</span><span class="sxs-lookup"><span data-stu-id="b8dfe-115">The second part is the number of rows.</span></span> <span data-ttu-id="b8dfe-116">Der dritte Teil ist die Anzahl der Spalten.</span><span class="sxs-lookup"><span data-stu-id="b8dfe-116">The third part is the number of columns.</span></span> <span data-ttu-id="b8dfe-117">Die Anzahl der Zeilen und Spalten ist eine positive ganze Zahl zwischen 1 und 4 einschließlich.</span><span class="sxs-lookup"><span data-stu-id="b8dfe-117">The number of rows and columns is a positive integer between 1 and 4 inclusive.</span></span><br/> |
| <span data-ttu-id="b8dfe-118"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Benennen**</span><span class="sxs-lookup"><span data-stu-id="b8dfe-118"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>                                         | <span data-ttu-id="b8dfe-119">Eine ASCII-Zeichenfolge, die den Variablennamen eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="b8dfe-119">An ASCII string that uniquely identifies the variable name.</span></span><br/>                                                                                                                                                                                                                            |



 

## <a name="examples"></a><span data-ttu-id="b8dfe-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b8dfe-120">Examples</span></span>

<span data-ttu-id="b8dfe-121">Hier einige Beispiele:</span><span class="sxs-lookup"><span data-stu-id="b8dfe-121">Here are some examples:</span></span>


```
int1x1    iMatrix;   // integer matrix with 1 row,  1 column
int4x1    iMatrix;   // integer matrix with 4 rows, 1 column
int1x4    iMatrix;   // integer matrix with 1 row, 4 columns
double3x3 dMatrix;   // double matrix with 3 rows, 3 columns

float2x2 fMatrix = { 0.0f, 0.1, // row 1
                     2.1f, 2.2f // row 2
                   };   
```



<span data-ttu-id="b8dfe-122">Eine Matrix kann auch mit der folgenden Syntax deklariert werden:</span><span class="sxs-lookup"><span data-stu-id="b8dfe-122">A matrix can be declared using this syntax also:</span></span>


```
matrix <Type, Number> VariableName
```



<span data-ttu-id="b8dfe-123">Der Matrixtyp verwendet die spitzen Klammern, um den Typ, die Anzahl der Zeilen und die Anzahl der Spalten anzugeben.</span><span class="sxs-lookup"><span data-stu-id="b8dfe-123">The matrix type uses the angle brackets to specify the type, the number of rows, and the number of columns.</span></span> <span data-ttu-id="b8dfe-124">In diesem Beispiel wird eine Gleit Komma Matrix mit zwei Zeilen und zwei Spalten erstellt.</span><span class="sxs-lookup"><span data-stu-id="b8dfe-124">This example creates a floating-point matrix, with two rows and two columns.</span></span> <span data-ttu-id="b8dfe-125">Alle skalaren Datentypen können verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b8dfe-125">Any of the scalar data types can be used.</span></span>

<span data-ttu-id="b8dfe-126">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="b8dfe-126">Here is an example:</span></span>


```
matrix <float, 2, 2> fMatrix = { 0.0f, 0.1, // row 1
                                 2.1f, 2.2f // row 2
                               };
```



## <a name="see-also"></a><span data-ttu-id="b8dfe-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b8dfe-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8dfe-128">Datentypen (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b8dfe-128">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





