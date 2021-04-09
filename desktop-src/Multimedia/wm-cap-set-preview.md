---
title: WM_CAP_SET_PREVIEW Meldung (VFW. h)
description: Die WM- \_ Obergrenze für die \_ Festlegung von \_ Voreinstellungen aktiviert oder deaktiviert den Vorschaumodus.
ms.assetid: ef6218d6-4fff-469f-b2e0-d7990998a3e5
keywords:
- WM_CAP_SET_PREVIEW-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_SET_PREVIEW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4a7e490809efa2e2d9f1ad27bca697c6333e682
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106113"
---
# <a name="wm_cap_set_preview-message"></a><span data-ttu-id="b2e38-104">WM- \_ Obergrenze für \_ festgelegte \_ Vorschau</span><span class="sxs-lookup"><span data-stu-id="b2e38-104">WM\_CAP\_SET\_PREVIEW message</span></span>

<span data-ttu-id="b2e38-105">Die **WM- \_ Obergrenze für die \_ Festlegung von \_ Voreinstellungen** aktiviert oder deaktiviert den Vorschaumodus.</span><span class="sxs-lookup"><span data-stu-id="b2e38-105">The **WM\_CAP\_SET\_PREVIEW** message enables or disables preview mode.</span></span> <span data-ttu-id="b2e38-106">Im Vorschaumodus werden Frames von der Aufzeichnungs Hardware in den Systemspeicher übertragen und dann im Erfassungsfenster mithilfe von GDI-Funktionen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b2e38-106">In preview mode, frames are transferred from the capture hardware to system memory and then displayed in the capture window using GDI functions.</span></span> <span data-ttu-id="b2e38-107">Sie können diese Nachricht explizit oder mithilfe des [**cappreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="b2e38-107">You can send this message explicitly or by using the [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) macro.</span></span>


```C++
WM_CAP_SET_PREVIEW 
wParam = (WPARAM) (BOOL) (f); 
lParam = 0L; 
```



## <a name="parameters"></a><span data-ttu-id="b2e38-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2e38-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2e38-109"><span id="f"></span><span id="F"></span>*c*</span><span class="sxs-lookup"><span data-stu-id="b2e38-109"><span id="f"></span><span id="F"></span>*f*</span></span>
</dt> <dd>

<span data-ttu-id="b2e38-110">Vorschauflag.</span><span class="sxs-lookup"><span data-stu-id="b2e38-110">Preview flag.</span></span> <span data-ttu-id="b2e38-111">Geben Sie **true** für diesen Parameter an, um den Vorschaumodus zu aktivieren oder **false** , um ihn zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="b2e38-111">Specify **TRUE** for this parameter to enable preview mode or **FALSE** to disable it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2e38-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b2e38-112">Return Value</span></span>

<span data-ttu-id="b2e38-113">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="b2e38-113">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2e38-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b2e38-114">Remarks</span></span>

<span data-ttu-id="b2e38-115">Im Vorschaumodus werden beträchtliche CPU-Ressourcen verwendet.</span><span class="sxs-lookup"><span data-stu-id="b2e38-115">The preview mode uses substantial CPU resources.</span></span> <span data-ttu-id="b2e38-116">Anwendungen können die Vorschau deaktivieren oder die Vorschau Rate verringern, wenn eine andere Anwendung den Fokus hat.</span><span class="sxs-lookup"><span data-stu-id="b2e38-116">Applications can disable preview or lower the preview rate when another application has the focus.</span></span> <span data-ttu-id="b2e38-117">Der **flivewindow** -Member der [**capstatus**](/windows/win32/api/vfw/ns-vfw-capstatus) -Struktur zeigt an, ob der Vorschaumodus aktuell aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b2e38-117">The **fLiveWindow** member of the [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) structure indicates if preview mode is currently enabled.</span></span>

<span data-ttu-id="b2e38-118">Durch Aktivieren des Vorschaumodus wird der Überlagerungs Modus automatisch deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="b2e38-118">Enabling preview mode automatically disables overlay mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2e38-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b2e38-119">Requirements</span></span>



| <span data-ttu-id="b2e38-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b2e38-120">Requirement</span></span> | <span data-ttu-id="b2e38-121">Wert</span><span class="sxs-lookup"><span data-stu-id="b2e38-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b2e38-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b2e38-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b2e38-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b2e38-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b2e38-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b2e38-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b2e38-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b2e38-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b2e38-126">Header</span><span class="sxs-lookup"><span data-stu-id="b2e38-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2e38-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2e38-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2e38-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b2e38-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2e38-129">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="b2e38-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="b2e38-130">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="b2e38-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





