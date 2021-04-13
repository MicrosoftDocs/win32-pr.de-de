---
description: Beschreibt Farbwerte.
ms.assetid: 6af8c2ec-bc79-4dc6-b56d-7a7676a50b39
title: D3DCOLORVALUE-Struktur (D3D9Types. h)
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
ms.openlocfilehash: 1fe2f187921749207bbbf51d7fcfd75357a70858
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354407"
---
# <a name="d3dcolorvalue-structure-d3d9typesh"></a><span data-ttu-id="5b081-103">D3DCOLORVALUE-Struktur (D3D9Types. h)</span><span class="sxs-lookup"><span data-stu-id="5b081-103">D3DCOLORVALUE structure (D3D9Types.h)</span></span>

<span data-ttu-id="5b081-104">Beschreibt Farbwerte.</span><span class="sxs-lookup"><span data-stu-id="5b081-104">Describes color values.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b081-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b081-105">Syntax</span></span>


```C++
typedef struct _D3DCOLORVALUE {
  float r;
  float g;
  float b;
  float a;
} D3DCOLORVALUE;
```



## <a name="members"></a><span data-ttu-id="5b081-106">Member</span><span class="sxs-lookup"><span data-stu-id="5b081-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5b081-107">**r**</span><span class="sxs-lookup"><span data-stu-id="5b081-107">**r**</span></span>
</dt> <dd>

<span data-ttu-id="5b081-108">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="5b081-108">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="5b081-109">Ein Gleit Komma Wert, der die rote Komponente einer Farbe angibt.</span><span class="sxs-lookup"><span data-stu-id="5b081-109">Floating-point value that specifies the red component of a color.</span></span> <span data-ttu-id="5b081-110">Dieser Wert liegt im Allgemeinen im Bereich von 0,0 bis 1,0.</span><span class="sxs-lookup"><span data-stu-id="5b081-110">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="5b081-111">Der Wert 0,0 gibt das vollständige Fehlen der roten Komponente an, während der Wert 1,0 angibt, dass Rot vollständig vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="5b081-111">A value of 0.0 indicates the complete absence of the red component, while a value of 1.0 indicates that red is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="5b081-112">**g**</span><span class="sxs-lookup"><span data-stu-id="5b081-112">**g**</span></span>
</dt> <dd>

<span data-ttu-id="5b081-113">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="5b081-113">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="5b081-114">Ein Gleit Komma Wert, der die grüne Komponente einer Farbe angibt.</span><span class="sxs-lookup"><span data-stu-id="5b081-114">Floating-point value that specifies the green component of a color.</span></span> <span data-ttu-id="5b081-115">Dieser Wert liegt im Allgemeinen im Bereich von 0,0 bis 1,0.</span><span class="sxs-lookup"><span data-stu-id="5b081-115">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="5b081-116">Der Wert 0,0 gibt das vollständige Fehlen der grünen Komponente an, während der Wert 1,0 angibt, dass grün vollständig vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="5b081-116">A value of 0.0 indicates the complete absence of the green component, while a value of 1.0 indicates that green is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="5b081-117">**b**</span><span class="sxs-lookup"><span data-stu-id="5b081-117">**b**</span></span>
</dt> <dd>

<span data-ttu-id="5b081-118">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="5b081-118">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="5b081-119">Ein Gleit Komma Wert, der die blaue Komponente einer Farbe angibt.</span><span class="sxs-lookup"><span data-stu-id="5b081-119">Floating-point value that specifies the blue component of a color.</span></span> <span data-ttu-id="5b081-120">Dieser Wert liegt im Allgemeinen im Bereich von 0,0 bis 1,0.</span><span class="sxs-lookup"><span data-stu-id="5b081-120">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="5b081-121">Der Wert 0,0 gibt das vollständige Fehlen der blauen Komponente an, während der Wert 1,0 angibt, dass Blue vollständig vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="5b081-121">A value of 0.0 indicates the complete absence of the blue component, while a value of 1.0 indicates that blue is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="5b081-122">**ein**</span><span class="sxs-lookup"><span data-stu-id="5b081-122">**a**</span></span>
</dt> <dd>

<span data-ttu-id="5b081-123">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="5b081-123">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="5b081-124">Ein Gleit Komma Wert, der die Alpha Komponente einer Farbe angibt.</span><span class="sxs-lookup"><span data-stu-id="5b081-124">Floating-point value that specifies the alpha component of a color.</span></span> <span data-ttu-id="5b081-125">Dieser Wert liegt im Allgemeinen im Bereich von 0,0 bis 1,0.</span><span class="sxs-lookup"><span data-stu-id="5b081-125">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="5b081-126">Der Wert 0,0 gibt vollständig transparent an, während der Wert 1,0 vollständig deckend angibt.</span><span class="sxs-lookup"><span data-stu-id="5b081-126">A value of 0.0 indicates fully transparent, while a value of 1.0 indicates fully opaque.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5b081-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5b081-127">Remarks</span></span>

<span data-ttu-id="5b081-128">Sie können die Member dieser Struktur auf Werte außerhalb des Bereichs von 0 bis 1 festlegen, um ungewöhnliche Effekte zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="5b081-128">You can set the members of this structure to values outside the range of 0 through 1 to implement some unusual effects.</span></span> <span data-ttu-id="5b081-129">Werte, die größer als 1 sind, führen zu starken Lichtern, die tendenziell eine Szene auslagern.</span><span class="sxs-lookup"><span data-stu-id="5b081-129">Values greater than 1 produce strong lights that tend to wash out a scene.</span></span> <span data-ttu-id="5b081-130">Durch negative Werte werden dunkle Lichter erzeugt, die das Licht aus einer Szene entfernen.</span><span class="sxs-lookup"><span data-stu-id="5b081-130">Negative values produce dark lights that actually remove light from a scene.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b081-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5b081-131">Requirements</span></span>



| <span data-ttu-id="5b081-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5b081-132">Requirement</span></span> | <span data-ttu-id="5b081-133">Wert</span><span class="sxs-lookup"><span data-stu-id="5b081-133">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b081-134">Header</span><span class="sxs-lookup"><span data-stu-id="5b081-134">Header</span></span><br/> | <dl> <span data-ttu-id="5b081-135"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b081-135"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b081-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b081-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b081-137">Direct3D-Strukturen</span><span class="sxs-lookup"><span data-stu-id="5b081-137">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 




