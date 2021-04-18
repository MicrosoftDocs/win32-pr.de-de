---
description: Gibt ein Ereignis Handle für das Ereignis zurück, das momentan auf dem angegebenen Animations Titel ausgeführt wird.
ms.assetid: 2e3d4b85-42f0-463f-9eca-d9b1fa8932f6
title: 'ID3DXAnimationController:: getcurrenttrackevent-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetCurrentTrackEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b00b90f6fbb3f4bb6170c8987f3634fec4bd0bf5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365327"
---
# <a name="id3dxanimationcontrollergetcurrenttrackevent-method"></a><span data-ttu-id="ad1ac-103">ID3DXAnimationController:: getcurrenttrackevent-Methode</span><span class="sxs-lookup"><span data-stu-id="ad1ac-103">ID3DXAnimationController::GetCurrentTrackEvent method</span></span>

<span data-ttu-id="ad1ac-104">Gibt ein Ereignis Handle für das Ereignis zurück, das momentan auf dem angegebenen Animations Titel ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ad1ac-104">Returns an event handle to the event currently running on the specified animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad1ac-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad1ac-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE GetCurrentTrackEvent(
  [in] UINT           Track,
  [in] D3DXEVENT_TYPE EventType
);
```



## <a name="parameters"></a><span data-ttu-id="ad1ac-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad1ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad1ac-107">Nach *verfolgen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ad1ac-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad1ac-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ad1ac-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ad1ac-109">Bezeichner nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="ad1ac-109">Track identifier.</span></span>

</dd> <dt>

<span data-ttu-id="ad1ac-110">*EventType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ad1ac-110">*EventType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad1ac-111">Type: **[ **D3DXEVENT- \_ Typ**](./d3dxevent-type.md)**</span><span class="sxs-lookup"><span data-stu-id="ad1ac-111">Type: **[**D3DXEVENT\_TYPE**](./d3dxevent-type.md)**</span></span>

<span data-ttu-id="ad1ac-112">Typ des abzufragende Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="ad1ac-112">Type of event to query.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad1ac-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ad1ac-113">Return value</span></span>

<span data-ttu-id="ad1ac-114">Typ: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="ad1ac-114">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="ad1ac-115">Ereignis Handle für das Ereignis, das zurzeit auf der angegebenen Spur ausgeführt wird. **Null** wird zurückgegeben, wenn kein Ereignis auf der angegebenen Spur ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ad1ac-115">Event handle to the event currently running on the specified track. **NULL** is returned if no event is running on the specified track.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad1ac-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ad1ac-116">Requirements</span></span>



| <span data-ttu-id="ad1ac-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ad1ac-117">Requirement</span></span> | <span data-ttu-id="ad1ac-118">Wert</span><span class="sxs-lookup"><span data-stu-id="ad1ac-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad1ac-119">Header</span><span class="sxs-lookup"><span data-stu-id="ad1ac-119">Header</span></span><br/>  | <dl> <span data-ttu-id="ad1ac-120"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad1ac-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="ad1ac-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ad1ac-121">Library</span></span><br/> | <dl> <span data-ttu-id="ad1ac-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ad1ac-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ad1ac-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad1ac-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad1ac-124">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="ad1ac-124">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
