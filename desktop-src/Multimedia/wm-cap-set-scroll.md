---
title: WM_CAP_SET_SCROLL Meldung (VFW. h)
description: Die "WM Cap"- \_ \_ \_ scrollnachricht definiert den Teil des Video Frames, der im Erfassungsfenster angezeigt werden soll.
ms.assetid: 545605e4-6b1f-403a-a3ab-0fd6750ae776
keywords:
- WM_CAP_SET_SCROLL-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_SET_SCROLL
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 812b76bdcad166b9f766957032f232293d4083c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479053"
---
# <a name="wm_cap_set_scroll-message"></a><span data-ttu-id="3dcce-104">Bild \_ Lauf \_ \_ Meldung zur WM-Abdeckung</span><span class="sxs-lookup"><span data-stu-id="3dcce-104">WM\_CAP\_SET\_SCROLL message</span></span>

<span data-ttu-id="3dcce-105">Die " **WM Cap"- \_ \_ \_ scrollnachricht** definiert den Teil des Video Frames, der im Erfassungsfenster angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3dcce-105">The **WM\_CAP\_SET\_SCROLL** message defines the portion of the video frame to display in the capture window.</span></span> <span data-ttu-id="3dcce-106">Mit dieser Meldung wird die linke obere Ecke des Client Bereichs des Aufzeichnungs Fensters auf die Koordinaten eines angegebenen Pixels im Videorahmen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3dcce-106">This message sets the upper left corner of the client area of the capture window to the coordinates of a specified pixel within the video frame.</span></span> <span data-ttu-id="3dcce-107">Sie können diese Nachricht explizit oder mithilfe des [**capsetscrollpos**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="3dcce-107">You can send this message explicitly or by using the [**capSetScrollPos**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos) macro.</span></span>


```C++
WM_CAP_SET_SCROLL 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPPOINT) (lpP); 
```



## <a name="parameters"></a><span data-ttu-id="3dcce-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3dcce-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3dcce-109"><span id="lpP"></span><span id="lpp"></span><span id="LPP"></span>*LPP*</span><span class="sxs-lookup"><span data-stu-id="3dcce-109"><span id="lpP"></span><span id="lpp"></span><span id="LPP"></span>*lpP*</span></span>
</dt> <dd>

<span data-ttu-id="3dcce-110">Adresse, die die gewünschte Scrollposition enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="3dcce-110">Address to contain the desired scroll position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3dcce-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3dcce-111">Return Value</span></span>

<span data-ttu-id="3dcce-112">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="3dcce-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3dcce-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3dcce-113">Remarks</span></span>

<span data-ttu-id="3dcce-114">Die Bild Lauf Position wirkt sich auf das Bild im Vorschau-und Überlagerungs Modus aus.</span><span class="sxs-lookup"><span data-stu-id="3dcce-114">The scroll position affects the image in both preview and overlay modes.</span></span>

## <a name="requirements"></a><span data-ttu-id="3dcce-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3dcce-115">Requirements</span></span>



| <span data-ttu-id="3dcce-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3dcce-116">Requirement</span></span> | <span data-ttu-id="3dcce-117">Wert</span><span class="sxs-lookup"><span data-stu-id="3dcce-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3dcce-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3dcce-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3dcce-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3dcce-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3dcce-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3dcce-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3dcce-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3dcce-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3dcce-122">Header</span><span class="sxs-lookup"><span data-stu-id="3dcce-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3dcce-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="3dcce-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3dcce-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3dcce-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dcce-125">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="3dcce-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="3dcce-126">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="3dcce-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





