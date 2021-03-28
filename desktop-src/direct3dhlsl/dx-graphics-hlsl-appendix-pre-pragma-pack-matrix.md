---
title: pack_matrix pragma-Direktive
description: Pragma-Direktive, die die Verpackungs Ausrichtung für Matrizen angibt.
ms.assetid: e77dc007-d915-4d78-9fff-d44d4999e4da
keywords:
- pack_matrix pragma-Direktive HLSL
topic_type:
- apiref
api_name:
- pack_matrix pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4bb5474702a1caba3f772002c34677601715caff
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104037987"
---
# <a name="pack_matrix-pragma-directive"></a><span data-ttu-id="1fe39-104">packmatrix- \_ pragma-Direktive</span><span class="sxs-lookup"><span data-stu-id="1fe39-104">pack\_matrix pragma Directive</span></span>

<span data-ttu-id="1fe39-105">Pragma-Direktive, die die Verpackungs Ausrichtung für Matrizen angibt.</span><span class="sxs-lookup"><span data-stu-id="1fe39-105">Pragma directive that specifies packing alignment for matrices.</span></span>



| <span data-ttu-id="1fe39-106">\#Pragma Pack- \_ Matrix ( *Ausrichtung* )</span><span class="sxs-lookup"><span data-stu-id="1fe39-106">\#pragma pack\_matrix( *alignment* )</span></span> |
|--------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="1fe39-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="1fe39-107">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1fe39-108">Element</span><span class="sxs-lookup"><span data-stu-id="1fe39-108">Item</span></span></th>
<th><span data-ttu-id="1fe39-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1fe39-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1fe39-110"><span id="alignment"></span><span id="ALIGNMENT"></span><em>Richt</em></span><span class="sxs-lookup"><span data-stu-id="1fe39-110"><span id="alignment"></span><span id="ALIGNMENT"></span><em>alignment</em></span></span><br/></td>
<td><span data-ttu-id="1fe39-111">Ausrichtung, die für Matrizen festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="1fe39-111">Alignment to set for matrices.</span></span> <span data-ttu-id="1fe39-112">Dieser Parameter kann einen der in der folgenden Tabelle aufgeführten Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="1fe39-112">This parameter can take one of the values listed in the following table.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1fe39-113">Wert</span><span class="sxs-lookup"><span data-stu-id="1fe39-113">Value</span></span></th>
<th><span data-ttu-id="1fe39-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1fe39-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1fe39-115">column_major</span><span class="sxs-lookup"><span data-stu-id="1fe39-115">column_major</span></span></td>
<td><span data-ttu-id="1fe39-116">Standard.</span><span class="sxs-lookup"><span data-stu-id="1fe39-116">Default.</span></span> <span data-ttu-id="1fe39-117">Legt die Ausrichtung der Matrix Verpackung auf den Spalten Hauptwert fest.</span><span class="sxs-lookup"><span data-stu-id="1fe39-117">Sets the matrix packing alignment to column major.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fe39-118">row_major</span><span class="sxs-lookup"><span data-stu-id="1fe39-118">row_major</span></span></td>
<td><span data-ttu-id="1fe39-119">Legt die Ausrichtung der Matrix Verpackung auf den Hauptabschnitt der Zeile fest.</span><span class="sxs-lookup"><span data-stu-id="1fe39-119">Sets the matrix packing alignment to row major.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="examples"></a><span data-ttu-id="1fe39-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1fe39-120">Examples</span></span>

<span data-ttu-id="1fe39-121">Im folgenden Beispiel wird die Ausrichtung der Matrix Verpackung auf Zeilen Hauptwert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1fe39-121">The following example sets the matrix packing alignment to row major.</span></span>


```
#pragma pack_matrix( row_major )
```



## <a name="see-also"></a><span data-ttu-id="1fe39-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1fe39-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fe39-123">Präprozessordirektiven (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1fe39-123">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="1fe39-124">\#pragma-Direktive (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1fe39-124">\#pragma Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





