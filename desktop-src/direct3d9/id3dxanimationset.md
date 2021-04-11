---
description: Diese Schnittstelle kapselt die Mindestfunktionalität, die von einem Animations Controller festgelegt wurde.
ms.assetid: vs|directx_sdk|~\id3dxanimationset.htm
title: ID3DXAnimationSet-Schnittstelle (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b5aa27494931e8b6c528627fa8e96278a6d86b05
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219697"
---
# <a name="id3dxanimationset-interface"></a><span data-ttu-id="67e65-103">ID3DXAnimationSet-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="67e65-103">ID3DXAnimationSet interface</span></span>

<span data-ttu-id="67e65-104">Diese Schnittstelle kapselt die Mindestfunktionalität, die von einem Animations Controller festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="67e65-104">This interface encapsulates the minimum functionality required of an animation set by an animation controller.</span></span> <span data-ttu-id="67e65-105">Fortgeschrittene Benutzer möchten diese Schnittstelle möglicherweise selbst implementieren, um Ihren speziellen Anforderungen gerecht zu werden. für die meisten Benutzer sollten jedoch die abgeleiteten [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) -und [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) -Schnittstellen ausreichen.</span><span class="sxs-lookup"><span data-stu-id="67e65-105">Advanced users might want to implement this interface themselves to suit their specialized needs; for most users, however, the derived [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) and [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) interfaces should suffice.</span></span>

## <a name="members"></a><span data-ttu-id="67e65-106">Member</span><span class="sxs-lookup"><span data-stu-id="67e65-106">Members</span></span>

<span data-ttu-id="67e65-107">Die **ID3DXAnimationSet** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="67e65-107">The **ID3DXAnimationSet** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="67e65-108">**ID3DXAnimationSet** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="67e65-108">**ID3DXAnimationSet** also has these types of members:</span></span>

-   [<span data-ttu-id="67e65-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="67e65-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="67e65-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="67e65-110">Methods</span></span>

<span data-ttu-id="67e65-111">Die **ID3DXAnimationSet** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="67e65-111">The **ID3DXAnimationSet** interface has these methods.</span></span>



| <span data-ttu-id="67e65-112">Methode</span><span class="sxs-lookup"><span data-stu-id="67e65-112">Method</span></span>                                                                        | <span data-ttu-id="67e65-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="67e65-113">Description</span></span>                                                                       |
|:------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="67e65-114">**Getanimationindexbyname**</span><span class="sxs-lookup"><span data-stu-id="67e65-114">**GetAnimationIndexByName**</span></span>](id3dxanimationset--getanimationindexbyname.md) | <span data-ttu-id="67e65-115">Ruft den Index einer Animation ab, wenn der Name angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="67e65-115">Gets the index of an animation, given its name.</span></span><br/>                        |
| [<span data-ttu-id="67e65-116">**Getanimationnamebyindex**</span><span class="sxs-lookup"><span data-stu-id="67e65-116">**GetAnimationNameByIndex**</span></span>](id3dxanimationset--getanimationnamebyindex.md) | <span data-ttu-id="67e65-117">Ruft den Namen einer Animation ab, wenn der Index angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="67e65-117">Gets the name of an animation, given its index.</span></span><br/>                        |
| [<span data-ttu-id="67e65-118">**GetCallback**</span><span class="sxs-lookup"><span data-stu-id="67e65-118">**GetCallback**</span></span>](id3dxanimationset--getcallback.md)                         | <span data-ttu-id="67e65-119">Ruft Informationen zu einem bestimmten Rückruf im Animations Satz ab.</span><span class="sxs-lookup"><span data-stu-id="67e65-119">Gets information about a specific callback in the animation set.</span></span><br/>       |
| [<span data-ttu-id="67e65-120">**GetName**</span><span class="sxs-lookup"><span data-stu-id="67e65-120">**GetName**</span></span>](id3dxanimationset--getname.md)                                 | <span data-ttu-id="67e65-121">Ruft den Namen des Animations Satzes ab.</span><span class="sxs-lookup"><span data-stu-id="67e65-121">Gets the animation set name.</span></span><br/>                                           |
| [<span data-ttu-id="67e65-122">**Getnumanimations**</span><span class="sxs-lookup"><span data-stu-id="67e65-122">**GetNumAnimations**</span></span>](id3dxanimationset--getnumanimations.md)               | <span data-ttu-id="67e65-123">Ruft die Anzahl der Animationen im Animations Satz ab.</span><span class="sxs-lookup"><span data-stu-id="67e65-123">Gets the number of animations in the animation set.</span></span><br/>                    |
| [<span data-ttu-id="67e65-124">**GetPeriod**</span><span class="sxs-lookup"><span data-stu-id="67e65-124">**GetPeriod**</span></span>](id3dxanimationset--getperiod.md)                             | <span data-ttu-id="67e65-125">Ruft den Zeitraum des Animations Satzes ab.</span><span class="sxs-lookup"><span data-stu-id="67e65-125">Gets the period of the animation set.</span></span><br/>                                  |
| [<span data-ttu-id="67e65-126">**GetPeriodicPosition**</span><span class="sxs-lookup"><span data-stu-id="67e65-126">**GetPeriodicPosition**</span></span>](id3dxanimationset--getperiodicposition.md)         | <span data-ttu-id="67e65-127">Gibt die Uhrzeit Position im lokalen Zeitrahmen eines Animations Satzes zurück.</span><span class="sxs-lookup"><span data-stu-id="67e65-127">Returns time position in the local timeframe of an animation set.</span></span><br/>      |
| [<span data-ttu-id="67e65-128">**Gewahrheits RT**</span><span class="sxs-lookup"><span data-stu-id="67e65-128">**GetSRT**</span></span>](id3dxanimationset--getsrt.md)                                   | <span data-ttu-id="67e65-129">Ruft die Skalierungs-, Drehungs-und Übersetzungs Werte des Animations Satzes ab.</span><span class="sxs-lookup"><span data-stu-id="67e65-129">Gets the scale, rotation, and translation values of the animation set.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="67e65-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="67e65-130">Remarks</span></span>

<span data-ttu-id="67e65-131">Ein Animations Satz besteht aus Animationen für viele Knoten für dieselbe Animation.</span><span class="sxs-lookup"><span data-stu-id="67e65-131">An animation set consists of animations for many nodes for the same animation.</span></span>

<span data-ttu-id="67e65-132">Der LPD3DXANIMATIONSET-Typ wird als Zeiger auf diese Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="67e65-132">The LPD3DXANIMATIONSET type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXAnimationSet ID3DXAnimationSet;
typedef interface ID3DXAnimationSet *LPD3DXANIMATIONSET;
```



## <a name="requirements"></a><span data-ttu-id="67e65-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="67e65-133">Requirements</span></span>



| <span data-ttu-id="67e65-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="67e65-134">Requirement</span></span> | <span data-ttu-id="67e65-135">Wert</span><span class="sxs-lookup"><span data-stu-id="67e65-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="67e65-136">Header</span><span class="sxs-lookup"><span data-stu-id="67e65-136">Header</span></span><br/>  | <dl> <span data-ttu-id="67e65-137"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="67e65-137"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="67e65-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="67e65-138">Library</span></span><br/> | <dl> <span data-ttu-id="67e65-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="67e65-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="67e65-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="67e65-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67e65-141">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="67e65-141">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
