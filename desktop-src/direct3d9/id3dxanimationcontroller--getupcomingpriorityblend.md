---
description: Gibt ein Ereignis Handle an das nächste in der nächsten Priorität angegebene Blend-Ereignis zurück, das nach einem angegebenen Ereignis geplant ist.
ms.assetid: 64fa6fca-dc4a-4534-ab8e-b11b3c7ed23c
title: 'ID3DXAnimationController:: getupcomingpriorityblend-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetUpcomingPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 72f9b8854041094d43d9e8250ab61b5f59a67848
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394054"
---
# <a name="id3dxanimationcontrollergetupcomingpriorityblend-method"></a><span data-ttu-id="61682-103">ID3DXAnimationController:: getupcomingpriorityblend-Methode</span><span class="sxs-lookup"><span data-stu-id="61682-103">ID3DXAnimationController::GetUpcomingPriorityBlend method</span></span>

<span data-ttu-id="61682-104">Gibt ein Ereignis Handle an das nächste in der nächsten Priorität angegebene Blend-Ereignis zurück, das nach einem angegebenen Ereignis geplant ist.</span><span class="sxs-lookup"><span data-stu-id="61682-104">Returns an event handle to the next priority blend event scheduled to occur after a specified event.</span></span>

## <a name="syntax"></a><span data-ttu-id="61682-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="61682-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE GetUpcomingPriorityBlend(
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="61682-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="61682-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61682-107">*hevent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="61682-107">*hEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61682-108">Typ: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="61682-108">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="61682-109">Ereignis Handle für ein angegebenes Ereignis, nach dem nach einem folgenden Ereignis für die Prioritäts Mischung gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="61682-109">Event handle to a specified event after which to search for a following priority blend event.</span></span> <span data-ttu-id="61682-110">Wenn der Wert auf **null** festgelegt ist, gibt die Methode das nächste Ereignis für die nächste geplante Priorität zurück.</span><span class="sxs-lookup"><span data-stu-id="61682-110">If set to **NULL**, then the method will return the next scheduled priority blend event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61682-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="61682-111">Return value</span></span>

<span data-ttu-id="61682-112">Typ: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="61682-112">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="61682-113">Ereignis Handle zum nächsten geplanten Prioritäts-Blend-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="61682-113">Event handle to the next scheduled priority blend event.</span></span> <span data-ttu-id="61682-114">**Null** wird zurückgegeben, wenn kein neues Prioritäts-Blend-Ereignis geplant ist.</span><span class="sxs-lookup"><span data-stu-id="61682-114">**NULL** is returned if no new priority blend event is scheduled.</span></span>

## <a name="remarks"></a><span data-ttu-id="61682-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="61682-115">Remarks</span></span>

<span data-ttu-id="61682-116">Diese Methode kann iterativ verwendet werden, um ein gewünschtes Prioritäts-Blend-Ereignis durch wiederholtes übergeben von **null** für hevent zu suchen.</span><span class="sxs-lookup"><span data-stu-id="61682-116">This method can be used iteratively to locate a desired priority blend event by repeatedly passing in **NULL** for hEvent.</span></span>

> [!Note]  
> <span data-ttu-id="61682-117">Iterieren Sie nicht weiter, nachdem die Methode **null** zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="61682-117">Do not iterate further after the method has returned **NULL**.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="61682-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="61682-118">Requirements</span></span>



| <span data-ttu-id="61682-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="61682-119">Requirement</span></span> | <span data-ttu-id="61682-120">Wert</span><span class="sxs-lookup"><span data-stu-id="61682-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="61682-121">Header</span><span class="sxs-lookup"><span data-stu-id="61682-121">Header</span></span><br/>  | <dl> <span data-ttu-id="61682-122"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="61682-122"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="61682-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="61682-123">Library</span></span><br/> | <dl> <span data-ttu-id="61682-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="61682-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="61682-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61682-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61682-126">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="61682-126">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




