---
title: WM_CAP_SET_OVERLAY Meldung (VFW. h)
description: Die WM-Obergrenze für die über \_ \_ \_ Lagerung aktiviert oder deaktiviert den Überlagerungs Modus. Im Überlagerungs Modus wird Video mithilfe der Hardware Überlagerung angezeigt. Sie können diese Nachricht explizit oder mithilfe des capoverlay-Makros senden.
ms.assetid: b74c0619-2b70-46e0-9acd-43d658529233
keywords:
- WM_CAP_SET_OVERLAY-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_SET_OVERLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f197ae3a7df9ad1520b84cf27fd15a1c76524ab1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346127"
---
# <a name="wm_cap_set_overlay-message"></a><span data-ttu-id="e1180-106">Über \_ \_ \_ Lagerungs Nachricht für WM-Cap</span><span class="sxs-lookup"><span data-stu-id="e1180-106">WM\_CAP\_SET\_OVERLAY message</span></span>

<span data-ttu-id="e1180-107">Die **WM-Obergrenze für die über \_ \_ \_ Lagerung** aktiviert oder deaktiviert den Überlagerungs Modus.</span><span class="sxs-lookup"><span data-stu-id="e1180-107">The **WM\_CAP\_SET\_OVERLAY** message enables or disables overlay mode.</span></span> <span data-ttu-id="e1180-108">Im Überlagerungs Modus wird Video mithilfe der Hardware Überlagerung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e1180-108">In overlay mode, video is displayed using hardware overlay.</span></span> <span data-ttu-id="e1180-109">Sie können diese Nachricht explizit oder mithilfe des [**capoverlay**](/windows/desktop/api/Vfw/nf-vfw-capoverlay) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="e1180-109">You can send this message explicitly or by using the [**capOverlay**](/windows/desktop/api/Vfw/nf-vfw-capoverlay) macro.</span></span>


```C++
WM_CAP_SET_OVERLAY 
wParam = (WPARAM) (BOOL) (f); 
lParam = 0L; 
```



## <a name="parameters"></a><span data-ttu-id="e1180-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1180-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1180-111"><span id="f"></span><span id="F"></span>*c*</span><span class="sxs-lookup"><span data-stu-id="e1180-111"><span id="f"></span><span id="F"></span>*f*</span></span>
</dt> <dd>

<span data-ttu-id="e1180-112">Overlay-Flag.</span><span class="sxs-lookup"><span data-stu-id="e1180-112">Overlay flag.</span></span> <span data-ttu-id="e1180-113">Geben Sie **true** für diesen Parameter an, um ihn zu aktivieren, oder **false** , um ihn zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="e1180-113">Specify **TRUE** for this parameter to enable overlay mode or **FALSE** to disable it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1180-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e1180-114">Return Value</span></span>

<span data-ttu-id="e1180-115">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="e1180-115">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1180-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e1180-116">Remarks</span></span>

<span data-ttu-id="e1180-117">Die Verwendung einer Überlagerung erfordert keine CPU-Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="e1180-117">Using an overlay does not require CPU resources.</span></span>

<span data-ttu-id="e1180-118">Der **fhasoverlay** -Member der [**capdrivercaps**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) -Struktur gibt an, ob das Gerät überlagern kann.</span><span class="sxs-lookup"><span data-stu-id="e1180-118">The **fHasOverlay** member of the [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) structure indicates whether the device is capable of overlay.</span></span> <span data-ttu-id="e1180-119">Der **foverlaywindow** -Member der [**capstatus**](/windows/win32/api/vfw/ns-vfw-capstatus) -Struktur gibt an, ob der Überlagerungs Modus aktuell aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e1180-119">The **fOverlayWindow** member of the [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) structure indicates whether overlay mode is currently enabled.</span></span>

<span data-ttu-id="e1180-120">Durch Aktivieren des Überlagerungs Modus wird der Vorschaumodus automatisch deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="e1180-120">Enabling overlay mode automatically disables preview mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1180-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e1180-121">Requirements</span></span>



| <span data-ttu-id="e1180-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e1180-122">Requirement</span></span> | <span data-ttu-id="e1180-123">Wert</span><span class="sxs-lookup"><span data-stu-id="e1180-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e1180-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e1180-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e1180-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e1180-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e1180-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e1180-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e1180-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e1180-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e1180-128">Header</span><span class="sxs-lookup"><span data-stu-id="e1180-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1180-129"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1180-129"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1180-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e1180-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1180-131">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="e1180-131">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="e1180-132">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="e1180-132">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





