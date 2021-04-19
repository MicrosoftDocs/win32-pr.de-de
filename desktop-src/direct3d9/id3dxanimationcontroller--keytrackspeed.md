---
description: Legt einen Ereignis Schlüssel fest, der die Geschwindigkeit eines Animations Titels ändert.
ms.assetid: 217d3a2d-0fb7-4995-86ec-7a4e8420e338
title: 'ID3DXAnimationController:: keytrackspeed-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackSpeed
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 09705dd03e7767e94b1508cf4951186a509a3c5b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355238"
---
# <a name="id3dxanimationcontrollerkeytrackspeed-method"></a><span data-ttu-id="b6b59-103">ID3DXAnimationController:: keytrackspeed-Methode</span><span class="sxs-lookup"><span data-stu-id="b6b59-103">ID3DXAnimationController::KeyTrackSpeed method</span></span>

<span data-ttu-id="b6b59-104">Legt einen Ereignis Schlüssel fest, der die Geschwindigkeit eines Animations Titels ändert.</span><span class="sxs-lookup"><span data-stu-id="b6b59-104">Sets an event key that changes the rate of play of an animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6b59-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6b59-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE KeyTrackSpeed(
  [in] UINT                Track,
  [in] FLOAT               NewSpeed,
  [in] DOUBLE              StartTime,
  [in] DOUBLE              Duration,
  [in] D3DXTRANSITION_TYPE Transition
);
```



## <a name="parameters"></a><span data-ttu-id="b6b59-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6b59-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6b59-107">Nach *verfolgen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6b59-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6b59-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b6b59-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b6b59-109">Der Bezeichner des zu ändernden Titels.</span><span class="sxs-lookup"><span data-stu-id="b6b59-109">Identifier of the track to modify.</span></span>

</dd> <dt>

<span data-ttu-id="b6b59-110">*Neugeschwindigkeit* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6b59-110">*NewSpeed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6b59-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b6b59-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b6b59-112">Neue Geschwindigkeit des Animations Titels.</span><span class="sxs-lookup"><span data-stu-id="b6b59-112">New speed of the animation track.</span></span>

</dd> <dt>

<span data-ttu-id="b6b59-113">*StartTime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6b59-113">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6b59-114">Typ: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b6b59-114">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b6b59-115">Globaler Zeit Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="b6b59-115">Global time key.</span></span> <span data-ttu-id="b6b59-116">Gibt die globale Zeit an, zu der die Änderung stattfindet.</span><span class="sxs-lookup"><span data-stu-id="b6b59-116">Specifies the global time when the change will take place.</span></span>

</dd> <dt>

<span data-ttu-id="b6b59-117">*Dauer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6b59-117">*Duration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6b59-118">Typ: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b6b59-118">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b6b59-119">Übergangszeit, die angibt, wie lange der reibungslose Übergang dauert.</span><span class="sxs-lookup"><span data-stu-id="b6b59-119">Transition time, which specifies how long the smooth transition will take to complete.</span></span>

</dd> <dt>

<span data-ttu-id="b6b59-120">*Übergang* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6b59-120">*Transition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6b59-121">Type: **[ **D3DXTRANSITION- \_ Typ**](./d3dxtransition-type.md)**</span><span class="sxs-lookup"><span data-stu-id="b6b59-121">Type: **[**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md)**</span></span>

<span data-ttu-id="b6b59-122">Gibt den für den Übergang zwischen Geschwindigkeiten verwendeten transitionstyp an.</span><span class="sxs-lookup"><span data-stu-id="b6b59-122">Specifies the transition type used for transitioning between speeds.</span></span> <span data-ttu-id="b6b59-123">Siehe [**D3DXTRANSITION \_ Type**](./d3dxtransition-type.md).</span><span class="sxs-lookup"><span data-stu-id="b6b59-123">See [**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6b59-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b6b59-124">Return value</span></span>

<span data-ttu-id="b6b59-125">Typ: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="b6b59-125">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="b6b59-126">Ereignis Handle für das Priority Blend-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="b6b59-126">Event handle to the priority blend event.</span></span> <span data-ttu-id="b6b59-127">**Null** wird zurückgegeben, wenn mindestens ein Eingabeparameter ungültig ist oder kein freies Ereignis verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="b6b59-127">**NULL** is returned if one or more of the input parameters is invalid, or no free event is available.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6b59-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b6b59-128">Requirements</span></span>



| <span data-ttu-id="b6b59-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b6b59-129">Requirement</span></span> | <span data-ttu-id="b6b59-130">Wert</span><span class="sxs-lookup"><span data-stu-id="b6b59-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6b59-131">Header</span><span class="sxs-lookup"><span data-stu-id="b6b59-131">Header</span></span><br/>  | <dl> <span data-ttu-id="b6b59-132"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6b59-132"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="b6b59-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b6b59-133">Library</span></span><br/> | <dl> <span data-ttu-id="b6b59-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b6b59-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b6b59-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6b59-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6b59-136">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="b6b59-136">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
