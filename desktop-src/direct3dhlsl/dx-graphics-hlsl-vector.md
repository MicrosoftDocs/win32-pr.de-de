---
title: Vector Type (HLSL)
description: Ein Vektor enthält zwischen einer und vier skalare Komponenten. jede Komponente eines Vektors muss denselben Typ aufweisen.
ms.assetid: 16e66f3c-c513-4d03-8adf-463dc8d83e12
keywords:
- Vector Type HLSL
topic_type:
- apiref
api_name:
- Vector Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76d07da5d22dfb44215f70a7620d6519b5c8a802
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "104995262"
---
# <a name="vector-type"></a><span data-ttu-id="37c3d-104">Vektortyp</span><span class="sxs-lookup"><span data-stu-id="37c3d-104">Vector Type</span></span>

<span data-ttu-id="37c3d-105">Ein Vektor enthält zwischen einer und vier skalare Komponenten. jede Komponente eines Vektors muss denselben Typ aufweisen.</span><span class="sxs-lookup"><span data-stu-id="37c3d-105">A vector contains between one and four scalar components; every component of a vector must be of the same type.</span></span>



|                     |
|---------------------|
| <span data-ttu-id="37c3d-106">**Name der Typnummer**</span><span class="sxs-lookup"><span data-stu-id="37c3d-106">**TypeNumber Name**</span></span> |



 


```
TypeComponents Name
```



## <a name="components"></a><span data-ttu-id="37c3d-107">Komponenten</span><span class="sxs-lookup"><span data-stu-id="37c3d-107">Components</span></span>



| <span data-ttu-id="37c3d-108">Element</span><span class="sxs-lookup"><span data-stu-id="37c3d-108">Item</span></span>                                                                                                                             | <span data-ttu-id="37c3d-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="37c3d-109">Description</span></span>                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37c3d-110"><span id="TypeComponents"></span><span id="typecomponents"></span><span id="TYPECOMPONENTS"></span>**Typecomponents**</span><span class="sxs-lookup"><span data-stu-id="37c3d-110"><span id="TypeComponents"></span><span id="typecomponents"></span><span id="TYPECOMPONENTS"></span>**TypeComponents**</span></span><br/> | <span data-ttu-id="37c3d-111">Ein einzelner Name, der zwei Teile enthält.</span><span class="sxs-lookup"><span data-stu-id="37c3d-111">A single name that contains two parts.</span></span> <span data-ttu-id="37c3d-112">Der erste Teil ist einer der [skalaren](dx-graphics-hlsl-data-types.md) Typen.</span><span class="sxs-lookup"><span data-stu-id="37c3d-112">The first part is one of the [scalar](dx-graphics-hlsl-data-types.md) types.</span></span> <span data-ttu-id="37c3d-113">Der zweite Teil ist die Anzahl der Komponenten, die zwischen 1 und 4 einschließlich liegen muss.</span><span class="sxs-lookup"><span data-stu-id="37c3d-113">The second part is the number of components, which must be between 1 and 4 inclusive.</span></span><br/> |
| <span data-ttu-id="37c3d-114"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Benennen**</span><span class="sxs-lookup"><span data-stu-id="37c3d-114"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>                                         | <span data-ttu-id="37c3d-115">Eine ASCII-Zeichenfolge, die den Variablennamen eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="37c3d-115">An ASCII string that uniquely identifies the variable name.</span></span><br/>                                                                                                                                                |



 

## <a name="examples"></a><span data-ttu-id="37c3d-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="37c3d-116">Examples</span></span>

<span data-ttu-id="37c3d-117">Hier einige Beispiele:</span><span class="sxs-lookup"><span data-stu-id="37c3d-117">Here are some examples:</span></span>


```
bool    bVector;   // scalar containing 1 Boolean
int1    iVector = 1;
float3  fVector = { 0.2f, 0.3f, 0.4f };
```



<span data-ttu-id="37c3d-118">Ein Vektor kann auch mit der folgenden Syntax deklariert werden:</span><span class="sxs-lookup"><span data-stu-id="37c3d-118">A vector can be declared using this syntax also:</span></span>


```
vector <Type, Number> VariableName
```



<span data-ttu-id="37c3d-119">Hier einige Beispiele:</span><span class="sxs-lookup"><span data-stu-id="37c3d-119">Here are some examples:</span></span>


```
vector <int,    1> iVector = 1;
vector <double, 4> dVector = { 0.2, 0.3, 0.4, 0.5 };
```

## <a name="see-also"></a><span data-ttu-id="37c3d-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="37c3d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37c3d-121">Datentypen (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="37c3d-121">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





