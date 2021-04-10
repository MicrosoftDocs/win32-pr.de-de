---
title: WM_CAP_DLG_VIDEOCOMPRESSION Meldung (VFW. h)
description: Die Meldung "WM \_ Cap \_ DLG \_ videocompression" zeigt ein Dialogfeld an, in dem der Benutzer einen während des Erfassungs Vorgangs zu verwendenden Kompressor auswählen kann.
ms.assetid: 526e4b5d-49a4-4bb5-92d6-cdd567636354
keywords:
- WM_CAP_DLG_VIDEOCOMPRESSION-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEOCOMPRESSION
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d851f73df7adbc205585eb7c69ad9d4d969aba66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040577"
---
# <a name="wm_cap_dlg_videocompression-message"></a><span data-ttu-id="fc59e-104">WM- \_ Cap- \_ DLG- \_ Video Komprimierungs Meldung</span><span class="sxs-lookup"><span data-stu-id="fc59e-104">WM\_CAP\_DLG\_VIDEOCOMPRESSION message</span></span>

<span data-ttu-id="fc59e-105">Die Meldung " **WM \_ Cap \_ DLG \_ videocompression** " zeigt ein Dialogfeld an, in dem der Benutzer einen während des Erfassungs Vorgangs zu verwendenden Kompressor auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="fc59e-105">The **WM\_CAP\_DLG\_VIDEOCOMPRESSION** message displays a dialog box in which the user can select a compressor to use during the capture process.</span></span> <span data-ttu-id="fc59e-106">Die Liste der verfügbaren Kompressoren kann sich von dem im Dialogfeld Videoformat des Erfassungs Treibers ausgewählten Videoformat unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="fc59e-106">The list of available compressors can vary with the video format selected in the capture driver's Video Format dialog box.</span></span> <span data-ttu-id="fc59e-107">Sie können diese Nachricht explizit oder mithilfe des [**capdlgvideocompression**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideocompression) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="fc59e-107">You can send this message explicitly or by using the [**capDlgVideoCompression**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideocompression) macro.</span></span>


```C++
WM_CAP_DLG_VIDEOCOMPRESSION 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="fc59e-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fc59e-108">Return Value</span></span>

<span data-ttu-id="fc59e-109">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="fc59e-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc59e-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fc59e-110">Remarks</span></span>

<span data-ttu-id="fc59e-111">Verwenden Sie diese Nachricht mit Erfassungs Treibern, die Frames nur im BI RGB-Format bereitstellen \_ .</span><span class="sxs-lookup"><span data-stu-id="fc59e-111">Use this message with capture drivers that provide frames only in the BI\_RGB format.</span></span> <span data-ttu-id="fc59e-112">Diese Meldung ist am nützlichsten beim Schritt Aufzeichnungs Vorgang, um die Erfassung und Komprimierung in einem einzelnen Vorgang zu kombinieren.</span><span class="sxs-lookup"><span data-stu-id="fc59e-112">This message is most useful in the step capture operation to combine capture and compression in a single operation.</span></span> <span data-ttu-id="fc59e-113">Das Komprimieren von Frames mit einem Software-Kompressor als Teil eines echt Zeit Erfassungs Vorgangs ist wahrscheinlich zu viel zeitaufwändig.</span><span class="sxs-lookup"><span data-stu-id="fc59e-113">Compressing frames with a software compressor as part of a real-time capture operation is most likely too time-consuming to perform.</span></span>

<span data-ttu-id="fc59e-114">Die Komprimierung hat keine Auswirkungen auf die in die Zwischenablage kopierten Frames.</span><span class="sxs-lookup"><span data-stu-id="fc59e-114">Compression does not affect the frames copied to the clipboard.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc59e-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fc59e-115">Requirements</span></span>



| <span data-ttu-id="fc59e-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fc59e-116">Requirement</span></span> | <span data-ttu-id="fc59e-117">Wert</span><span class="sxs-lookup"><span data-stu-id="fc59e-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="fc59e-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fc59e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fc59e-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fc59e-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="fc59e-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fc59e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fc59e-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fc59e-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="fc59e-122">Header</span><span class="sxs-lookup"><span data-stu-id="fc59e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc59e-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc59e-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc59e-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fc59e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc59e-125">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="fc59e-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="fc59e-126">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="fc59e-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





