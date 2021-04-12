---
description: Legt einen Ereignis Schlüssel fest, mit dem die Ortszeit eines Animations Titels geändert wird.
ms.assetid: b527e960-8ab9-42a0-bb4d-bea5aaf83424
title: 'ID3DXAnimationController:: keytrackposition-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackPosition
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d027069efa9fb49cad3d2344da593eae4c3c844c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355507"
---
# <a name="id3dxanimationcontrollerkeytrackposition-method"></a><span data-ttu-id="0a94e-103">ID3DXAnimationController:: keytrackposition-Methode</span><span class="sxs-lookup"><span data-stu-id="0a94e-103">ID3DXAnimationController::KeyTrackPosition method</span></span>

<span data-ttu-id="0a94e-104">Legt einen Ereignis Schlüssel fest, mit dem die Ortszeit eines Animations Titels geändert wird.</span><span class="sxs-lookup"><span data-stu-id="0a94e-104">Sets an event key that changes the local time of an animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a94e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a94e-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE KeyTrackPosition(
  [in] UINT   Track,
  [in] DOUBLE NewPosition,
  [in] DOUBLE StartTime
);
```



## <a name="parameters"></a><span data-ttu-id="0a94e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a94e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a94e-107">Nach *verfolgen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0a94e-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a94e-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0a94e-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0a94e-109">Der Bezeichner des zu ändernden Titels.</span><span class="sxs-lookup"><span data-stu-id="0a94e-109">Identifier of the track to modify.</span></span>

</dd> <dt>

<span data-ttu-id="0a94e-110">*Neuposition* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0a94e-110">*NewPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a94e-111">Typ: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0a94e-111">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0a94e-112">Neue lokale Zeit des Animations Titels.</span><span class="sxs-lookup"><span data-stu-id="0a94e-112">New local time of the animation track.</span></span>

</dd> <dt>

<span data-ttu-id="0a94e-113">*StartTime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0a94e-113">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a94e-114">Typ: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0a94e-114">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0a94e-115">Globaler Zeit Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="0a94e-115">Global time key.</span></span> <span data-ttu-id="0a94e-116">Gibt die globale Zeit an, zu der die Änderung stattfindet.</span><span class="sxs-lookup"><span data-stu-id="0a94e-116">Specifies the global time when the change will take place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a94e-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0a94e-117">Return value</span></span>

<span data-ttu-id="0a94e-118">Typ: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="0a94e-118">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="0a94e-119">Ereignis Handle für das Priority Blend-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="0a94e-119">Event handle to the priority blend event.</span></span> <span data-ttu-id="0a94e-120">**Null** wird zurückgegeben, wenn Track ungültig ist, oder, wenn kein freies Ereignis verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="0a94e-120">**NULL** is returned if Track is invalid, or if no free event is available.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a94e-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0a94e-121">Requirements</span></span>



| <span data-ttu-id="0a94e-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0a94e-122">Requirement</span></span> | <span data-ttu-id="0a94e-123">Wert</span><span class="sxs-lookup"><span data-stu-id="0a94e-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a94e-124">Header</span><span class="sxs-lookup"><span data-stu-id="0a94e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="0a94e-125"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a94e-125"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="0a94e-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0a94e-126">Library</span></span><br/> | <dl> <span data-ttu-id="0a94e-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0a94e-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0a94e-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0a94e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a94e-129">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="0a94e-129">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
