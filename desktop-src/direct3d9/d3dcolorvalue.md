---
description: 'D3DCOLORVALUE-Struktur (D3D9Types.h): Beschreibt Farbwerte.'
ms.assetid: 6af8c2ec-bc79-4dc6-b56d-7a7676a50b39
title: D3DCOLORVALUE-Struktur (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLORVALUE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: c9b55fbf718382e9dca7e3999cce0cabe895a261
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116058"
---
# <a name="d3dcolorvalue-structure-d3d9typesh"></a><span data-ttu-id="c160c-103">D3DCOLORVALUE-Struktur (D3D9Types.h)</span><span class="sxs-lookup"><span data-stu-id="c160c-103">D3DCOLORVALUE structure (D3D9Types.h)</span></span>

<span data-ttu-id="c160c-104">Beschreibt Farbwerte.</span><span class="sxs-lookup"><span data-stu-id="c160c-104">Describes color values.</span></span>

## <a name="syntax"></a><span data-ttu-id="c160c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c160c-105">Syntax</span></span>


```C++
typedef struct _D3DCOLORVALUE {
  float r;
  float g;
  float b;
  float a;
} D3DCOLORVALUE;
```



## <a name="members"></a><span data-ttu-id="c160c-106">Member</span><span class="sxs-lookup"><span data-stu-id="c160c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c160c-107">**r**</span><span class="sxs-lookup"><span data-stu-id="c160c-107">**r**</span></span>
</dt> <dd>

<span data-ttu-id="c160c-108">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="c160c-108">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="c160c-109">Gleitkommawert, der die rote Komponente einer Farbe angibt.</span><span class="sxs-lookup"><span data-stu-id="c160c-109">Floating-point value that specifies the red component of a color.</span></span> <span data-ttu-id="c160c-110">Dieser Wert liegt im Allgemeinen im Bereich von 0,0 bis 1,0.</span><span class="sxs-lookup"><span data-stu-id="c160c-110">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="c160c-111">Der Wert 0,0 gibt das vollständige Fehlen der roten Komponente an, während der Wert 1,0 angibt, dass Rot vollständig vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c160c-111">A value of 0.0 indicates the complete absence of the red component, while a value of 1.0 indicates that red is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="c160c-112">**g**</span><span class="sxs-lookup"><span data-stu-id="c160c-112">**g**</span></span>
</dt> <dd>

<span data-ttu-id="c160c-113">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="c160c-113">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="c160c-114">Gleitkommawert, der die grüne Komponente einer Farbe angibt.</span><span class="sxs-lookup"><span data-stu-id="c160c-114">Floating-point value that specifies the green component of a color.</span></span> <span data-ttu-id="c160c-115">Dieser Wert liegt im Allgemeinen im Bereich von 0,0 bis 1,0.</span><span class="sxs-lookup"><span data-stu-id="c160c-115">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="c160c-116">Der Wert 0,0 gibt das vollständige Fehlen der grünen Komponente an, während der Wert 1,0 angibt, dass grün vollständig vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c160c-116">A value of 0.0 indicates the complete absence of the green component, while a value of 1.0 indicates that green is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="c160c-117">**b**</span><span class="sxs-lookup"><span data-stu-id="c160c-117">**b**</span></span>
</dt> <dd>

<span data-ttu-id="c160c-118">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="c160c-118">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="c160c-119">Gleitkommawert, der die blaue Komponente einer Farbe angibt.</span><span class="sxs-lookup"><span data-stu-id="c160c-119">Floating-point value that specifies the blue component of a color.</span></span> <span data-ttu-id="c160c-120">Dieser Wert liegt im Allgemeinen im Bereich von 0,0 bis 1,0.</span><span class="sxs-lookup"><span data-stu-id="c160c-120">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="c160c-121">Der Wert 0,0 gibt das vollständige Fehlen der blauen Komponente an, während der Wert 1,0 angibt, dass blau vollständig vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c160c-121">A value of 0.0 indicates the complete absence of the blue component, while a value of 1.0 indicates that blue is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="c160c-122">**Eine**</span><span class="sxs-lookup"><span data-stu-id="c160c-122">**a**</span></span>
</dt> <dd>

<span data-ttu-id="c160c-123">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="c160c-123">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="c160c-124">Gleitkommawert, der die Alphakomponente einer Farbe angibt.</span><span class="sxs-lookup"><span data-stu-id="c160c-124">Floating-point value that specifies the alpha component of a color.</span></span> <span data-ttu-id="c160c-125">Dieser Wert liegt im Allgemeinen im Bereich von 0,0 bis 1,0.</span><span class="sxs-lookup"><span data-stu-id="c160c-125">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="c160c-126">Der Wert 0,0 gibt vollständig transparent an, während der Wert 1,0 für vollständig deckend steht.</span><span class="sxs-lookup"><span data-stu-id="c160c-126">A value of 0.0 indicates fully transparent, while a value of 1.0 indicates fully opaque.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c160c-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c160c-127">Remarks</span></span>

<span data-ttu-id="c160c-128">Sie können die Member dieser Struktur auf Werte außerhalb des Bereichs von 0 bis 1 festlegen, um einige ungewöhnliche Effekte zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="c160c-128">You can set the members of this structure to values outside the range of 0 through 1 to implement some unusual effects.</span></span> <span data-ttu-id="c160c-129">Werte größer als 1 erzeugen starke Lichtlichter, die dazu tendieren, eine Szene zu verwaschen.</span><span class="sxs-lookup"><span data-stu-id="c160c-129">Values greater than 1 produce strong lights that tend to wash out a scene.</span></span> <span data-ttu-id="c160c-130">Negative Werte erzeugen dunkle Lichtlichter, die tatsächlich Licht aus einer Szene entfernen.</span><span class="sxs-lookup"><span data-stu-id="c160c-130">Negative values produce dark lights that actually remove light from a scene.</span></span>

## <a name="requirements"></a><span data-ttu-id="c160c-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c160c-131">Requirements</span></span>



| <span data-ttu-id="c160c-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c160c-132">Requirement</span></span> | <span data-ttu-id="c160c-133">Wert</span><span class="sxs-lookup"><span data-stu-id="c160c-133">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c160c-134">Header</span><span class="sxs-lookup"><span data-stu-id="c160c-134">Header</span></span><br/> | <dl> <span data-ttu-id="c160c-135"><dt>D3D9Types.h</dt></span><span class="sxs-lookup"><span data-stu-id="c160c-135"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c160c-136">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c160c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c160c-137">Direct3D-Strukturen</span><span class="sxs-lookup"><span data-stu-id="c160c-137">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 




