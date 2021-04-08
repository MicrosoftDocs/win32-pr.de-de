---
title: WM_CAP_DLG_VIDEOFORMAT Meldung (VFW. h)
description: Die Meldung "WM \_ Cap \_ DLG \_ Videoformat" zeigt ein Dialogfeld an, in dem der Benutzer das Videoformat auswählen kann.
ms.assetid: 3b44507e-3806-467f-877a-e9992d1337cb
keywords:
- WM_CAP_DLG_VIDEOFORMAT-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d244c4c141845d4ede66804918514e091872e89
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949753"
---
# <a name="wm_cap_dlg_videoformat-message"></a><span data-ttu-id="416f0-104">WM \_ Cap \_ DLG- \_ Videoformat Meldung</span><span class="sxs-lookup"><span data-stu-id="416f0-104">WM\_CAP\_DLG\_VIDEOFORMAT message</span></span>

<span data-ttu-id="416f0-105">Die Meldung " **WM \_ Cap \_ DLG \_ Videoformat** " zeigt ein Dialogfeld an, in dem der Benutzer das Videoformat auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="416f0-105">The **WM\_CAP\_DLG\_VIDEOFORMAT** message displays a dialog box in which the user can select the video format.</span></span> <span data-ttu-id="416f0-106">Das Dialogfeld Video Format kann verwendet werden, um Bild Dimensionen, Bittiefe und Hardware Komprimierungs Optionen auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="416f0-106">The Video Format dialog box might be used to select image dimensions, bit depth, and hardware compression options.</span></span> <span data-ttu-id="416f0-107">Sie können diese Nachricht explizit oder mithilfe des [**capdlgvideoformat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="416f0-107">You can send this message explicitly or by using the [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) macro.</span></span>


```C++
WM_CAP_DLG_VIDEOFORMAT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="416f0-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="416f0-108">Return Value</span></span>

<span data-ttu-id="416f0-109">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="416f0-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="416f0-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="416f0-110">Remarks</span></span>

<span data-ttu-id="416f0-111">Nachdem diese Nachricht zurückgegeben wurde, müssen Anwendungen möglicherweise die [**capstatus**](/windows/win32/api/vfw/ns-vfw-capstatus) -Struktur aktualisieren, da der Benutzer möglicherweise die Bild Dimensionen geändert hat.</span><span class="sxs-lookup"><span data-stu-id="416f0-111">After this message returns, applications might need to update the [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) structure because the user might have changed the image dimensions.</span></span>

<span data-ttu-id="416f0-112">Das Dialogfeld Video Format ist für jeden Aufzeichnungs Treiber eindeutig.</span><span class="sxs-lookup"><span data-stu-id="416f0-112">The Video Format dialog box is unique for each capture driver.</span></span> <span data-ttu-id="416f0-113">Einige Aufzeichnungs Treiber unterstützen möglicherweise kein Video Format-Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="416f0-113">Some capture drivers might not support a Video Format dialog box.</span></span> <span data-ttu-id="416f0-114">Anwendungen können ermitteln, ob der Erfassungs Treiber diese Nachricht unterstützt, indem Sie den Member **fhasdlgvideoformat** von [**capdrivercaps**](/windows/win32/api/vfw/ns-vfw-capdrivercaps)überprüfen.</span><span class="sxs-lookup"><span data-stu-id="416f0-114">Applications can determine if the capture driver supports this message by checking the **fHasDlgVideoFormat** member of [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps).</span></span>

## <a name="requirements"></a><span data-ttu-id="416f0-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="416f0-115">Requirements</span></span>



| <span data-ttu-id="416f0-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="416f0-116">Requirement</span></span> | <span data-ttu-id="416f0-117">Wert</span><span class="sxs-lookup"><span data-stu-id="416f0-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="416f0-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="416f0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="416f0-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="416f0-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="416f0-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="416f0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="416f0-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="416f0-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="416f0-122">Header</span><span class="sxs-lookup"><span data-stu-id="416f0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="416f0-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="416f0-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="416f0-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="416f0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="416f0-125">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="416f0-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="416f0-126">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="416f0-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





