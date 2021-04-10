---
description: Gibt ein Ereignis Handle für das nächste Ereignis zurück, das geplant ist, nachdem ein bestimmtes Ereignis auf einem Animations Titel auftritt.
ms.assetid: 616b2de1-6107-4d18-ad2e-de2ef4560aee
title: 'ID3DXAnimationController:: getupcomingtrackevent-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetUpcomingTrackEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f863ce918f25c6b0975010f71a63f067c01f7345
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961558"
---
# <a name="id3dxanimationcontrollergetupcomingtrackevent-method"></a><span data-ttu-id="11eee-103">ID3DXAnimationController:: getupcomingtrackevent-Methode</span><span class="sxs-lookup"><span data-stu-id="11eee-103">ID3DXAnimationController::GetUpcomingTrackEvent method</span></span>

<span data-ttu-id="11eee-104">Gibt ein Ereignis Handle für das nächste Ereignis zurück, das geplant ist, nachdem ein bestimmtes Ereignis auf einem Animations Titel auftritt.</span><span class="sxs-lookup"><span data-stu-id="11eee-104">Returns an event handle to the next event scheduled to occur after a specified event on an animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="11eee-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="11eee-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE GetUpcomingTrackEvent(
  [in] UINT            Track,
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="11eee-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="11eee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11eee-107">Nach *verfolgen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11eee-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11eee-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="11eee-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="11eee-109">Bezeichner nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="11eee-109">Track identifier.</span></span>

</dd> <dt>

<span data-ttu-id="11eee-110">*hevent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11eee-110">*hEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11eee-111">Typ: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="11eee-111">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="11eee-112">Ereignis Handle für ein angegebenes Ereignis, nach dem nach einem folgenden Ereignis gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="11eee-112">Event handle to a specified event after which to search for a following event.</span></span> <span data-ttu-id="11eee-113">Wenn der Wert auf **null** festgelegt wird, gibt die Methode das nächste geplante Ereignis zurück.</span><span class="sxs-lookup"><span data-stu-id="11eee-113">If set to **NULL**, then the method will return the next scheduled event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11eee-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="11eee-114">Return value</span></span>

<span data-ttu-id="11eee-115">Typ: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="11eee-115">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="11eee-116">Ereignis Handle für das nächste Ereignis, das für die Ausführung auf dem angegebenen Track geplant ist. **Null** wird zurückgegeben, wenn kein neues Ereignis geplant ist.</span><span class="sxs-lookup"><span data-stu-id="11eee-116">Event handle to the next event scheduled to run on the specified track. **NULL** is returned if no new event is scheduled.</span></span>

## <a name="remarks"></a><span data-ttu-id="11eee-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="11eee-117">Remarks</span></span>

<span data-ttu-id="11eee-118">Diese Methode kann iterativ verwendet werden, um ein gewünschtes Ereignis durch wiederholtes übergeben von **null** für hevent zu suchen.</span><span class="sxs-lookup"><span data-stu-id="11eee-118">This method can be used iteratively to locate a desired event by repeatedly passing in **NULL** for hEvent.</span></span>

> [!Note]  
> <span data-ttu-id="11eee-119">Iterieren Sie nicht weiter, nachdem die Methode **null** zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="11eee-119">Do not iterate further after the method has returned **NULL**.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="11eee-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11eee-120">Requirements</span></span>



| <span data-ttu-id="11eee-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11eee-121">Requirement</span></span> | <span data-ttu-id="11eee-122">Wert</span><span class="sxs-lookup"><span data-stu-id="11eee-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="11eee-123">Header</span><span class="sxs-lookup"><span data-stu-id="11eee-123">Header</span></span><br/>  | <dl> <span data-ttu-id="11eee-124"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="11eee-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="11eee-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="11eee-125">Library</span></span><br/> | <dl> <span data-ttu-id="11eee-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="11eee-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="11eee-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11eee-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11eee-128">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="11eee-128">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
