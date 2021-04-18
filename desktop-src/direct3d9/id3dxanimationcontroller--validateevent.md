---
description: Überprüft, ob ein angegebenes Ereignis Handle gültig ist und das Animations Ereignis noch nicht abgeschlossen wurde.
ms.assetid: 242ad1e2-4b04-4ce1-9cdf-f66da9f83f06
title: 'ID3DXAnimationController:: ValidateEvent-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.ValidateEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e1a632fa867269f04e8f5f66e6bc352ef1701cd9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354411"
---
# <a name="id3dxanimationcontrollervalidateevent-method"></a><span data-ttu-id="74026-103">ID3DXAnimationController:: ValidateEvent-Methode</span><span class="sxs-lookup"><span data-stu-id="74026-103">ID3DXAnimationController::ValidateEvent method</span></span>

<span data-ttu-id="74026-104">Überprüft, ob ein angegebenes Ereignis Handle gültig ist und das Animations Ereignis noch nicht abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="74026-104">Checks whether a specified event handle is valid and the animation event has not yet completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="74026-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="74026-105">Syntax</span></span>


```C++
HRESULT ValidateEvent(
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="74026-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="74026-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74026-107">*hevent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74026-107">*hEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74026-108">Typ: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="74026-108">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="74026-109">Ereignis Handle für ein Animations Ereignis.</span><span class="sxs-lookup"><span data-stu-id="74026-109">Event handle to an animation event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74026-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="74026-110">Return value</span></span>

<span data-ttu-id="74026-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="74026-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="74026-112">Gibt S \_ OK zurück, wenn das Ereignis Handle gültig ist und das Ereignis noch nicht abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="74026-112">Returns S\_OK if the event handle is valid and the event has not yet completed.</span></span>

<span data-ttu-id="74026-113">Gibt "E Fail" zurück, \_ Wenn das Ereignis Handle ungültig ist und/oder das Ereignis abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="74026-113">Returns E\_FAIL if the event handle is invalid and/or the event has completed.</span></span>

## <a name="remarks"></a><span data-ttu-id="74026-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="74026-114">Remarks</span></span>

<span data-ttu-id="74026-115">Die-Methode gibt an, dass ein Ereignis Handle gültig ist, auch wenn das Ereignis ausgeführt wird, aber noch nicht abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="74026-115">The method will indicate that an event handle is valid even if the event is running but has not yet completed.</span></span>

## <a name="requirements"></a><span data-ttu-id="74026-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="74026-116">Requirements</span></span>



| <span data-ttu-id="74026-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="74026-117">Requirement</span></span> | <span data-ttu-id="74026-118">Wert</span><span class="sxs-lookup"><span data-stu-id="74026-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="74026-119">Header</span><span class="sxs-lookup"><span data-stu-id="74026-119">Header</span></span><br/>  | <dl> <span data-ttu-id="74026-120"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="74026-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="74026-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="74026-121">Library</span></span><br/> | <dl> <span data-ttu-id="74026-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="74026-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="74026-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74026-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74026-124">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="74026-124">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




