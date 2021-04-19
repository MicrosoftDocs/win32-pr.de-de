---
description: Status Codes, die von DXGI-Funktionen zurückgegeben werden können.
ms.assetid: dd7480b4-8218-4716-ab9f-74a9955b8aa7
title: DXGI_STATUS (dxgi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39c402880ccdcbda009402d56127e70a61543d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363128"
---
# <a name="dxgi_status"></a><span data-ttu-id="be13b-103">DXGI- \_ Status</span><span class="sxs-lookup"><span data-stu-id="be13b-103">DXGI\_STATUS</span></span>

<span data-ttu-id="be13b-104">Status Codes, die von DXGI-Funktionen zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="be13b-104">Status codes that can be returned by DXGI functions.</span></span>



| <span data-ttu-id="be13b-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="be13b-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                      | <span data-ttu-id="be13b-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="be13b-106">Description</span></span>                                                                                                                                                                                                                                                                                              |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_STATUS_OCCLUDED"></span><span id="dxgi_status_occluded"></span><dl> <span data-ttu-id="be13b-107"><dt>**DXGI \_ Der \_ Status**</dt> lautet " <dt>0x087a0001</dt> ".</span><span class="sxs-lookup"><span data-stu-id="be13b-107"><dt>**DXGI\_STATUS\_OCCLUDED**</dt> <dt>0x087A0001</dt></span></span> </dl>                                                 | <span data-ttu-id="be13b-108">Der Fensterinhalt ist nicht sichtbar.</span><span class="sxs-lookup"><span data-stu-id="be13b-108">The window content is not visible.</span></span> <span data-ttu-id="be13b-109">Beim Empfang dieses Status kann eine Anwendung das Rendering beenden und den vorhandenen DXGI- \_ \_ Test verwenden, um zu bestimmen, wann das Rendering fortgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="be13b-109">When receiving this status, an application can stop rendering and use DXGI\_PRESENT\_TEST to determine when to resume rendering.</span></span> <span data-ttu-id="be13b-110">Der DXGI-Status wird nicht angezeigt, \_ \_ Wenn Sie eine Swapkette für das Kippen von Modellen verwenden.</span><span class="sxs-lookup"><span data-stu-id="be13b-110">You will not receive DXGI\_STATUS\_OCCLUDED if you're using a flip model swap chain.</span></span><br/>                                                                                                                           |
| <span id="DXGI_STATUS_MODE_CHANGED"></span><span id="dxgi_status_mode_changed"></span><dl> <span data-ttu-id="be13b-111"><dt>**DXGI \_ Status \_ Modus \_ geändert**</dt> <dt>0x087a0007</dt></span><span class="sxs-lookup"><span data-stu-id="be13b-111"><dt>**DXGI\_STATUS\_MODE\_CHANGED**</dt> <dt>0x087A0007</dt></span></span> </dl>                                    | <span data-ttu-id="be13b-112">Der Desktop Anzeigemodus wurde geändert, möglicherweise ist die Farbkonvertierung/-Streckung vorhanden.</span><span class="sxs-lookup"><span data-stu-id="be13b-112">The desktop display mode has been changed, there might be color conversion/stretching.</span></span> <span data-ttu-id="be13b-113">Die Anwendung sollte [**idxgiswapchain:: resizebuffers**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) aufrufen, damit Sie dem neuen Anzeigemodus entspricht.</span><span class="sxs-lookup"><span data-stu-id="be13b-113">The application should call [**IDXGISwapChain::ResizeBuffers**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) to match the new display mode.</span></span><br/>                                                                       |
| <span id="DXGI_STATUS_MODE_CHANGE_IN_PROGRESS"></span><span id="dxgi_status_mode_change_in_progress"></span><dl> <span data-ttu-id="be13b-114"><dt>**DXGI \_ Status \_ Modus \_ - \_ Änderung \_ in**</dt> Bearbeitung <dt>0x087a0008</dt></span><span class="sxs-lookup"><span data-stu-id="be13b-114"><dt>**DXGI\_STATUS\_MODE\_CHANGE\_IN\_PROGRESS**</dt> <dt>0x087A0008</dt></span></span> </dl> | <span data-ttu-id="be13b-115">[**Idxgiswapchain:: resizetarget**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizetarget) und [**idxgiswapchain:: setfullscreenstate**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate) gibt \_ eine Änderung im DXGI-Status Modus zurück, \_ \_ \_ \_ Wenn ein Übergang im Vollbild-/Windos-Modus stattfindet, wenn eine der beiden APIs aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="be13b-115">[**IDXGISwapChain::ResizeTarget**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizetarget) and [**IDXGISwapChain::SetFullscreenState**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate) will return DXGI\_STATUS\_MODE\_CHANGE\_IN\_PROGRESS if a fullscreen/windowed mode transition is occurring when either API is called.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="be13b-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="be13b-116">Remarks</span></span>

<span data-ttu-id="be13b-117">Der **HRESULT** -Wert für jeden **DXGI- \_ Status** Wert wird von diesem Makro bestimmt, das in "dxgitype. h" definiert ist:</span><span class="sxs-lookup"><span data-stu-id="be13b-117">The **HRESULT** value for each **DXGI\_STATUS** value is determined from this macro that is defined in DXGItype.h:</span></span>


```
#define _FACDXGI    0x87a
#define MAKE_DXGI_STATUS(code)  MAKE_HRESULT(0, _FACDXGI, code)
```



<span data-ttu-id="be13b-118">Der **DXGI- \_ Status " \_ okded** " wird beispielsweise als " **0x087a0001**" definiert:</span><span class="sxs-lookup"><span data-stu-id="be13b-118">For example, **DXGI\_STATUS\_OCCLUDED** is defined as **0x087A0001**:</span></span>


```
#define DXGI_STATUS_OCCLUDED                    MAKE_DXGI_STATUS(1)
```



## <a name="requirements"></a><span data-ttu-id="be13b-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="be13b-119">Requirements</span></span>



| <span data-ttu-id="be13b-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="be13b-120">Requirement</span></span> | <span data-ttu-id="be13b-121">Wert</span><span class="sxs-lookup"><span data-stu-id="be13b-121">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="be13b-122">Header</span><span class="sxs-lookup"><span data-stu-id="be13b-122">Header</span></span><br/> | <dl> <span data-ttu-id="be13b-123"><dt>DXGI. h</dt></span><span class="sxs-lookup"><span data-stu-id="be13b-123"><dt>DXGI.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be13b-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be13b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be13b-125">DXGI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="be13b-125">DXGI Constants</span></span>](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




