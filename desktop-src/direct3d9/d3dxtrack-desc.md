---
description: Beschreibt einen Animations Titel und gibt das Mischungs Gewicht, die Geschwindigkeit und die Position für den Track zu einem bestimmten Zeitpunkt an.
ms.assetid: f1469b6f-861f-4b7d-a187-933092a5d257
title: D3DXTRACK_DESC-Struktur (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTRACK_DESC
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 12f1604cf954bcdd6a2a898fec5410804112e498
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365309"
---
# <a name="d3dxtrack_desc-structure"></a><span data-ttu-id="46135-103">D3DXTRACK- \_ Struktur</span><span class="sxs-lookup"><span data-stu-id="46135-103">D3DXTRACK\_DESC structure</span></span>

<span data-ttu-id="46135-104">Beschreibt einen Animations Titel und gibt das Mischungs Gewicht, die Geschwindigkeit und die Position für den Track zu einem bestimmten Zeitpunkt an.</span><span class="sxs-lookup"><span data-stu-id="46135-104">Describes an animation track and specifies blending weight, speed, and position for the track at a given time.</span></span>

## <a name="syntax"></a><span data-ttu-id="46135-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="46135-105">Syntax</span></span>


```C++
typedef struct D3DXTRACK_DESC {
  D3DXPRIORITY_TYPE Priority;
  FLOAT             Weight;
  FLOAT             Speed;
  DOUBLE            Position;
  BOOL              Enable;
} D3DXTRACK_DESC, *LPD3DXTRACK_DESC;
```



## <a name="members"></a><span data-ttu-id="46135-106">Member</span><span class="sxs-lookup"><span data-stu-id="46135-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="46135-107">**Priority**</span><span class="sxs-lookup"><span data-stu-id="46135-107">**Priority**</span></span>
</dt> <dd>

<span data-ttu-id="46135-108">Type: **[ **D3DXPRIORITY- \_ Typ**](./d3dxpriority-type.md)**</span><span class="sxs-lookup"><span data-stu-id="46135-108">Type: **[**D3DXPRIORITY\_TYPE**](./d3dxpriority-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="46135-109">Der Prioritäts Typen, wie in [**D3DXPRIORITY \_ Type**](./d3dxpriority-type.md)definiert.</span><span class="sxs-lookup"><span data-stu-id="46135-109">Priority type, as defined in [**D3DXPRIORITY\_TYPE**](./d3dxpriority-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="46135-110">**Weight**</span><span class="sxs-lookup"><span data-stu-id="46135-110">**Weight**</span></span>
</dt> <dd>

<span data-ttu-id="46135-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46135-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="46135-112">Gewichtungswert.</span><span class="sxs-lookup"><span data-stu-id="46135-112">Weight value.</span></span> <span data-ttu-id="46135-113">Die Gewichtung bestimmt den Anteil dieses Titels zum Mischen mit anderen Spuren.</span><span class="sxs-lookup"><span data-stu-id="46135-113">The weight determines the proportion of this track to blend with other tracks.</span></span>

</dd> <dt>

<span data-ttu-id="46135-114">**Geschwindigkeit**</span><span class="sxs-lookup"><span data-stu-id="46135-114">**Speed**</span></span>
</dt> <dd>

<span data-ttu-id="46135-115">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46135-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="46135-116">Geschwindigkeitswert.</span><span class="sxs-lookup"><span data-stu-id="46135-116">Speed value.</span></span> <span data-ttu-id="46135-117">Dies wird ähnlich wie bei einem Multiplikator verwendet, um den Zeitraum des Titels zu skalieren.</span><span class="sxs-lookup"><span data-stu-id="46135-117">This is used similarly to a multiplier to scale the period of the track.</span></span>

</dd> <dt>

<span data-ttu-id="46135-118">**Position**</span><span class="sxs-lookup"><span data-stu-id="46135-118">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="46135-119">Typ: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46135-119">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="46135-120">Uhrzeit Position des Titels im lokalen Zeitrahmen des aktuellen Animations Satzes.</span><span class="sxs-lookup"><span data-stu-id="46135-120">Time position of the track, in the local timeframe of its current animation set.</span></span>

</dd> <dt>

<span data-ttu-id="46135-121">**Aktivieren**</span><span class="sxs-lookup"><span data-stu-id="46135-121">**Enable**</span></span>
</dt> <dd>

<span data-ttu-id="46135-122">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46135-122">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="46135-123">Nachverfolgen von aktivieren/deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="46135-123">Track enable/disable.</span></span> <span data-ttu-id="46135-124">Legen Sie zum Aktivieren von auf **true** fest.</span><span class="sxs-lookup"><span data-stu-id="46135-124">To enable, set to **TRUE**.</span></span> <span data-ttu-id="46135-125">Legen Sie zum Deaktivieren von auf **false** fest.</span><span class="sxs-lookup"><span data-stu-id="46135-125">To disable, set to **FALSE**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="46135-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="46135-126">Remarks</span></span>

<span data-ttu-id="46135-127">Spuren mit der gleichen Priorität werden kombiniert, und die beiden resultierenden Werte werden dann mithilfe des Prioritäts-Blend-Faktors gemischt.</span><span class="sxs-lookup"><span data-stu-id="46135-127">Tracks with the same priority are blended together, and the two resulting values are then blended using the priority blend factor.</span></span> <span data-ttu-id="46135-128">Einem Track muss ein Animations Satz (separat gespeichert) zugeordnet sein.</span><span class="sxs-lookup"><span data-stu-id="46135-128">A track must have an animation set (stored separately) associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="46135-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46135-129">Requirements</span></span>



| <span data-ttu-id="46135-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="46135-130">Requirement</span></span> | <span data-ttu-id="46135-131">Wert</span><span class="sxs-lookup"><span data-stu-id="46135-131">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="46135-132">Header</span><span class="sxs-lookup"><span data-stu-id="46135-132">Header</span></span><br/> | <dl> <span data-ttu-id="46135-133"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="46135-133"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46135-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46135-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46135-135">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="46135-135">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
