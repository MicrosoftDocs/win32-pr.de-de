---
title: WM_CAP_SET_SCALE Meldung (VFW. h)
description: Mit der \_ Einstellung für die WM-Cap- \_ \_ Skalierung wird die Skalierung der Preview-Videobilder aktiviert oder deaktiviert.
ms.assetid: f15f1d18-2c5a-40c1-baa1-0d18549bee23
keywords:
- WM_CAP_SET_SCALE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_SET_SCALE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd3bfc5dc463d84c935f994519060c33f89b8c0a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106112"
---
# <a name="wm_cap_set_scale-message"></a><span data-ttu-id="5ff72-104">Formel zum Festlegen der WM-Abdeckung \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="5ff72-104">WM\_CAP\_SET\_SCALE message</span></span>

<span data-ttu-id="5ff72-105">Mit der Einstellung für die **WM-Cap- \_ \_ \_ Skalierung** wird die Skalierung der Preview-Videobilder aktiviert oder deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="5ff72-105">The **WM\_CAP\_SET\_SCALE** message enables or disables scaling of the preview video images.</span></span> <span data-ttu-id="5ff72-106">Wenn die Skalierung aktiviert ist, wird der erfasste Videoframe auf die Abmessungen des Aufzeichnungs Fensters gestreckt.</span><span class="sxs-lookup"><span data-stu-id="5ff72-106">If scaling is enabled, the captured video frame is stretched to the dimensions of the capture window.</span></span> <span data-ttu-id="5ff72-107">Sie können diese Nachricht explizit oder mithilfe des [**cappreviewscale**](/windows/desktop/api/Vfw/nf-vfw-cappreviewscale) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="5ff72-107">You can send this message explicitly or by using the [**capPreviewScale**](/windows/desktop/api/Vfw/nf-vfw-cappreviewscale) macro.</span></span>


```C++
WM_CAP_SET_SCALE 
wParam = (WPARAM) (BOOL)f; 
lParam = 0L; 
```



## <a name="parameters"></a><span data-ttu-id="5ff72-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ff72-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ff72-109"><span id="f"></span><span id="F"></span>*c*</span><span class="sxs-lookup"><span data-stu-id="5ff72-109"><span id="f"></span><span id="F"></span>*f*</span></span>
</dt> <dd>

<span data-ttu-id="5ff72-110">Flag für die Vorschau Skalierung.</span><span class="sxs-lookup"><span data-stu-id="5ff72-110">Preview scaling flag.</span></span> <span data-ttu-id="5ff72-111">Geben Sie **true** für diesen Parameter an, um die Vorschau Rahmen auf die Größe des Erfassungs Fensters zu erweitern, oder auf **false** , um Sie in ihrer natürlichen Größe anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5ff72-111">Specify **TRUE** for this parameter to stretch preview frames to the size of the capture window or **FALSE** to display them at their natural size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ff72-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5ff72-112">Return Value</span></span>

<span data-ttu-id="5ff72-113">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="5ff72-113">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ff72-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5ff72-114">Remarks</span></span>

<span data-ttu-id="5ff72-115">Durch das Skalieren von Vorschaubildern wird die sofortige Darstellung der aufgezeichneten Frames im Aufzeichnungs Fenster gesteuert.</span><span class="sxs-lookup"><span data-stu-id="5ff72-115">Scaling preview images controls the immediate presentation of captured frames within the capture window.</span></span> <span data-ttu-id="5ff72-116">Dies hat keine Auswirkung auf die Größe der in der Datei gespeicherten Frames.</span><span class="sxs-lookup"><span data-stu-id="5ff72-116">It has no effect on the size of the frames saved to file.</span></span>

<span data-ttu-id="5ff72-117">Die Skalierung hat keine Auswirkungen, wenn Sie das Overlay zum Anzeigen von Videos im Frame Puffer verwenden.</span><span class="sxs-lookup"><span data-stu-id="5ff72-117">Scaling has no effect when using overlay to display video in the frame buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ff72-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ff72-118">Requirements</span></span>



| <span data-ttu-id="5ff72-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5ff72-119">Requirement</span></span> | <span data-ttu-id="5ff72-120">Wert</span><span class="sxs-lookup"><span data-stu-id="5ff72-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5ff72-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5ff72-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5ff72-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5ff72-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="5ff72-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5ff72-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5ff72-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5ff72-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5ff72-125">Header</span><span class="sxs-lookup"><span data-stu-id="5ff72-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ff72-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ff72-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ff72-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ff72-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ff72-128">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="5ff72-128">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="5ff72-129">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="5ff72-129">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





