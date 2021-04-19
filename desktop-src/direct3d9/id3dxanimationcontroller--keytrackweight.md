---
description: Legt einen Ereignis Schlüssel fest, mit dem die Gewichtung eines Animations Titels geändert wird. Die Gewichtung wird als Multiplikator verwendet, wenn mehrere Titel zusammen kombiniert werden.
ms.assetid: fb2859de-9e77-49dd-be48-a50e22e2fc3a
title: 'ID3DXAnimationController:: keytrackweight-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackWeight
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 74f5e38392f6b4ac192f02b9d85421c8357a16ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363169"
---
# <a name="id3dxanimationcontrollerkeytrackweight-method"></a><span data-ttu-id="9aa80-103">ID3DXAnimationController:: keytrackweight-Methode</span><span class="sxs-lookup"><span data-stu-id="9aa80-103">ID3DXAnimationController::KeyTrackWeight method</span></span>

<span data-ttu-id="9aa80-104">Legt einen Ereignis Schlüssel fest, mit dem die Gewichtung eines Animations Titels geändert wird. Die Gewichtung wird als Multiplikator verwendet, wenn mehrere Titel zusammen kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="9aa80-104">Sets an event key that changes the weight of an animation track. The weight is used as a multiplier when combining multiple tracks together.</span></span>

## <a name="syntax"></a><span data-ttu-id="9aa80-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9aa80-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE KeyTrackWeight(
  [in] UINT                Track,
  [in] FLOAT               NewWeight,
  [in] DOUBLE              StartTime,
  [in] DOUBLE              Duration,
  [in] D3DXTRANSITION_TYPE Transition
);
```



## <a name="parameters"></a><span data-ttu-id="9aa80-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9aa80-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9aa80-107">Nach *verfolgen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9aa80-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aa80-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9aa80-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9aa80-109">Der Bezeichner des zu ändernden Titels.</span><span class="sxs-lookup"><span data-stu-id="9aa80-109">Identifier of the track to modify.</span></span>

</dd> <dt>

<span data-ttu-id="9aa80-110">*Newweight* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9aa80-110">*NewWeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aa80-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9aa80-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9aa80-112">Neue Gewichtung des Titels.</span><span class="sxs-lookup"><span data-stu-id="9aa80-112">New weight of the track.</span></span>

</dd> <dt>

<span data-ttu-id="9aa80-113">*StartTime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9aa80-113">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aa80-114">Typ: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9aa80-114">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9aa80-115">Globaler Zeit Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="9aa80-115">Global time key.</span></span> <span data-ttu-id="9aa80-116">Gibt die globale Zeit an, zu der die Änderung stattfindet.</span><span class="sxs-lookup"><span data-stu-id="9aa80-116">Specifies the global time when the change will take place.</span></span>

</dd> <dt>

<span data-ttu-id="9aa80-117">*Dauer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9aa80-117">*Duration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aa80-118">Typ: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9aa80-118">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9aa80-119">Übergangszeit, die angibt, wie lange der reibungslose Übergang dauert.</span><span class="sxs-lookup"><span data-stu-id="9aa80-119">Transition time, which specifies how long the smooth transition will take to complete.</span></span>

</dd> <dt>

<span data-ttu-id="9aa80-120">*Übergang* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9aa80-120">*Transition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aa80-121">Type: **[ **D3DXTRANSITION- \_ Typ**](./d3dxtransition-type.md)**</span><span class="sxs-lookup"><span data-stu-id="9aa80-121">Type: **[**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md)**</span></span>

<span data-ttu-id="9aa80-122">Gibt den für den Übergang zwischen Gewichtungen verwendeten transitionstyp an.</span><span class="sxs-lookup"><span data-stu-id="9aa80-122">Specifies the transition type used for transitioning between weights.</span></span> <span data-ttu-id="9aa80-123">Siehe [**D3DXTRANSITION \_ Type**](./d3dxtransition-type.md).</span><span class="sxs-lookup"><span data-stu-id="9aa80-123">See [**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9aa80-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9aa80-124">Return value</span></span>

<span data-ttu-id="9aa80-125">Typ: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="9aa80-125">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="9aa80-126">Ereignis Handle für das Priority Blend-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="9aa80-126">Event handle to the priority blend event.</span></span> <span data-ttu-id="9aa80-127">**Null** wird zurückgegeben, wenn mindestens ein Eingabeparameter ungültig ist oder kein freies Ereignis verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="9aa80-127">**NULL** is returned if one or more of the input parameters is invalid, or no free event is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="9aa80-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9aa80-128">Remarks</span></span>

<span data-ttu-id="9aa80-129">Die Gewichtung wird wie ein Multiplikator verwendet, um zu bestimmen, wie viel von dieser Spur mit anderen Spuren verknüpft werden muss.</span><span class="sxs-lookup"><span data-stu-id="9aa80-129">The weight is used like a multiplier to determine how much of this track to blend together with other tracks.</span></span>

## <a name="requirements"></a><span data-ttu-id="9aa80-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9aa80-130">Requirements</span></span>



| <span data-ttu-id="9aa80-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9aa80-131">Requirement</span></span> | <span data-ttu-id="9aa80-132">Wert</span><span class="sxs-lookup"><span data-stu-id="9aa80-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9aa80-133">Header</span><span class="sxs-lookup"><span data-stu-id="9aa80-133">Header</span></span><br/>  | <dl> <span data-ttu-id="9aa80-134"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="9aa80-134"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="9aa80-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9aa80-135">Library</span></span><br/> | <dl> <span data-ttu-id="9aa80-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9aa80-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9aa80-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9aa80-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9aa80-138">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="9aa80-138">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
