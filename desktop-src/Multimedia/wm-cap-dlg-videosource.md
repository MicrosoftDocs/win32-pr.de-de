---
title: WM_CAP_DLG_VIDEOSOURCE Meldung (VFW. h)
description: Die Meldung "WM \_ Cap \_ DLG \_ videosource" zeigt ein Dialogfeld an, in dem der Benutzer die Videoquelle steuern kann.
ms.assetid: 8dc2f271-1f48-4e63-badf-9f3322063018
keywords:
- WM_CAP_DLG_VIDEOSOURCE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEOSOURCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38e8ae7e3d619964a547fbe0db4517fd1e7d277f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476221"
---
# <a name="wm_cap_dlg_videosource-message"></a><span data-ttu-id="cc13e-104">WM- \_ Cap- \_ DLG- \_ videosource-Nachricht</span><span class="sxs-lookup"><span data-stu-id="cc13e-104">WM\_CAP\_DLG\_VIDEOSOURCE message</span></span>

<span data-ttu-id="cc13e-105">Die Meldung " **WM \_ Cap \_ DLG \_ videosource** " zeigt ein Dialogfeld an, in dem der Benutzer die Videoquelle steuern kann.</span><span class="sxs-lookup"><span data-stu-id="cc13e-105">The **WM\_CAP\_DLG\_VIDEOSOURCE** message displays a dialog box in which the user can control the video source.</span></span> <span data-ttu-id="cc13e-106">Das Dialogfeld Video Quelle enthält möglicherweise Steuerelemente, die Eingabe Quellen auswählen. Ändern Sie den Farbton, den Kontrast und die Helligkeit des Bilds. und ändern Sie die Videoqualität, bevor Sie die Bilder im Frame Puffer digitalisieren.</span><span class="sxs-lookup"><span data-stu-id="cc13e-106">The Video Source dialog box might contain controls that select input sources; alter the hue, contrast, brightness of the image; and modify the video quality before digitizing the images into the frame buffer.</span></span> <span data-ttu-id="cc13e-107">Sie können diese Nachricht explizit oder mithilfe des [**capdlgvideosource**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideosource) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="cc13e-107">You can send this message explicitly or by using the [**capDlgVideoSource**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideosource) macro.</span></span>


```C++
WM_CAP_DLG_VIDEOSOURCE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="cc13e-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cc13e-108">Return Value</span></span>

<span data-ttu-id="cc13e-109">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="cc13e-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc13e-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cc13e-110">Remarks</span></span>

<span data-ttu-id="cc13e-111">Das Dialogfeld Video Quelle ist für jeden Aufzeichnungs Treiber eindeutig.</span><span class="sxs-lookup"><span data-stu-id="cc13e-111">The Video Source dialog box is unique for each capture driver.</span></span> <span data-ttu-id="cc13e-112">Einige Aufzeichnungs Treiber unterstützen möglicherweise kein Dialogfeld "Video Quelle".</span><span class="sxs-lookup"><span data-stu-id="cc13e-112">Some capture drivers might not support a Video Source dialog box.</span></span> <span data-ttu-id="cc13e-113">Anwendungen können bestimmen, ob der Erfassungs Treiber diese Nachricht unterstützt, indem Sie den **fhasdlgvideosource** -Member der [**capdrivercaps**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) -Struktur überprüfen.</span><span class="sxs-lookup"><span data-stu-id="cc13e-113">Applications can determine if the capture driver supports this message by checking the **fHasDlgVideoSource** member of the [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc13e-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cc13e-114">Requirements</span></span>



| <span data-ttu-id="cc13e-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc13e-115">Requirement</span></span> | <span data-ttu-id="cc13e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="cc13e-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="cc13e-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cc13e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cc13e-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cc13e-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="cc13e-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cc13e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cc13e-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cc13e-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="cc13e-121">Header</span><span class="sxs-lookup"><span data-stu-id="cc13e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc13e-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc13e-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc13e-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cc13e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc13e-124">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="cc13e-124">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="cc13e-125">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="cc13e-125">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





