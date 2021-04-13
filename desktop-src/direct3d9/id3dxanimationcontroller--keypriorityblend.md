---
description: Legt Mischungs Ereignis Schlüssel für den angegebenen Animations Titel fest.
ms.assetid: 2023d566-1de5-465a-ad6f-04a78ac01c33
title: 'ID3DXAnimationController:: keypriorityblend-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 31778da9b26ddd79b5f05c69c822ed62a5b5281e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354257"
---
# <a name="id3dxanimationcontrollerkeypriorityblend-method"></a><span data-ttu-id="318b2-103">ID3DXAnimationController:: keypriorityblend-Methode</span><span class="sxs-lookup"><span data-stu-id="318b2-103">ID3DXAnimationController::KeyPriorityBlend method</span></span>

<span data-ttu-id="318b2-104">Legt Mischungs Ereignis Schlüssel für den angegebenen Animations Titel fest.</span><span class="sxs-lookup"><span data-stu-id="318b2-104">Sets blending event keys for the specified animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="318b2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="318b2-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE KeyPriorityBlend(
  [in] FLOAT               NewBlendWeight,
  [in] DOUBLE              StartTime,
  [in] DOUBLE              Duration,
  [in] D3DXTRANSITION_TYPE Transition
);
```



## <a name="parameters"></a><span data-ttu-id="318b2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="318b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="318b2-107">*Newblendweight* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="318b2-107">*NewBlendWeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="318b2-108">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="318b2-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="318b2-109">Die Zahl zwischen 0 und 1, die zum Kombinieren von Spuren verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="318b2-109">Number between 0 and 1 that is used to blend tracks together.</span></span>

</dd> <dt>

<span data-ttu-id="318b2-110">*StartTime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="318b2-110">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="318b2-111">Typ: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="318b2-111">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="318b2-112">Die globale Zeit zum Starten von Blend.</span><span class="sxs-lookup"><span data-stu-id="318b2-112">Global time to start the blend.</span></span>

</dd> <dt>

<span data-ttu-id="318b2-113">*Dauer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="318b2-113">*Duration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="318b2-114">Typ: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="318b2-114">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="318b2-115">Die globale Zeitspanne der Mischung.</span><span class="sxs-lookup"><span data-stu-id="318b2-115">Global time duration of the blend.</span></span>

</dd> <dt>

<span data-ttu-id="318b2-116">*Übergang* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="318b2-116">*Transition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="318b2-117">Type: **[ **D3DXTRANSITION- \_ Typ**](./d3dxtransition-type.md)**</span><span class="sxs-lookup"><span data-stu-id="318b2-117">Type: **[**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md)**</span></span>

<span data-ttu-id="318b2-118">Gibt den für die Dauer der Blend verwendeten umgangstyp an.</span><span class="sxs-lookup"><span data-stu-id="318b2-118">Specifies the transition type used for the duration of the blend.</span></span> <span data-ttu-id="318b2-119">Siehe [**D3DXTRANSITION \_ Type**](./d3dxtransition-type.md).</span><span class="sxs-lookup"><span data-stu-id="318b2-119">See [**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="318b2-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="318b2-120">Return value</span></span>

<span data-ttu-id="318b2-121">Typ: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="318b2-121">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="318b2-122">Ereignis Handle für das Priority Blend-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="318b2-122">Event handle to the priority blend event.</span></span> <span data-ttu-id="318b2-123">**Null** wird zurückgegeben, wenn mindestens ein Eingabeparameter ungültig ist oder kein freies Ereignis verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="318b2-123">**NULL** is returned if one or more of the input parameters is invalid, or no free event is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="318b2-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="318b2-124">Remarks</span></span>

<span data-ttu-id="318b2-125">Der Animations Controller wird in drei Phasen gemischt: Titel mit niedriger Priorität werden zuerst gemischt, Titel mit hoher Priorität werden als zweites gemischt angezeigt, und dann werden die Ergebnisse beider Komponenten gemischt.</span><span class="sxs-lookup"><span data-stu-id="318b2-125">The animation controller blends in three phases: low priority tracks are blended first, high priority tracks are blended second, and then the results of both are blended.</span></span>

## <a name="requirements"></a><span data-ttu-id="318b2-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="318b2-126">Requirements</span></span>



| <span data-ttu-id="318b2-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="318b2-127">Requirement</span></span> | <span data-ttu-id="318b2-128">Wert</span><span class="sxs-lookup"><span data-stu-id="318b2-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="318b2-129">Header</span><span class="sxs-lookup"><span data-stu-id="318b2-129">Header</span></span><br/>  | <dl> <span data-ttu-id="318b2-130"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="318b2-130"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="318b2-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="318b2-131">Library</span></span><br/> | <dl> <span data-ttu-id="318b2-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="318b2-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="318b2-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="318b2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="318b2-134">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="318b2-134">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> <dt>

[<span data-ttu-id="318b2-135">**Setpriorityblend**</span><span class="sxs-lookup"><span data-stu-id="318b2-135">**SetPriorityBlend**</span></span>](id3dxanimationcontroller--setpriorityblend.md)
</dt> </dl>

 

 
