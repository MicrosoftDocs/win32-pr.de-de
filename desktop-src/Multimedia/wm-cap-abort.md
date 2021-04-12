---
title: WM_CAP_ABORT Meldung (VFW. h)
description: Die WM \_ - \_ Abbruchs Nachricht beendet den Aufzeichnungs Vorgang.
ms.assetid: a0479d73-8422-4833-9e8a-c262ec386f58
keywords:
- WM_CAP_ABORT-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_ABORT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2843e3c4d59b62f2b58be20cef63ed0dc2e79d4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517723"
---
# <a name="wm_cap_abort-message"></a><span data-ttu-id="3a1b9-104">\_ \_ Abbruch Meldung für WM-Cap</span><span class="sxs-lookup"><span data-stu-id="3a1b9-104">WM\_CAP\_ABORT message</span></span>

<span data-ttu-id="3a1b9-105">Die **WM \_ - \_ Abbruchs** Nachricht beendet den Aufzeichnungs Vorgang.</span><span class="sxs-lookup"><span data-stu-id="3a1b9-105">The **WM\_CAP\_ABORT** message stops the capture operation.</span></span> <span data-ttu-id="3a1b9-106">Bei der Schritt Erfassung werden die Abbild Daten, die bis zum Zeitpunkt der WM- **\_ \_ Abbruchs** Nachricht erfasst werden, in der Erfassungs Datei aufbewahrt, die Audiodaten werden jedoch nicht erfasst.</span><span class="sxs-lookup"><span data-stu-id="3a1b9-106">In the case of step capture, the image data collected up to the point of the **WM\_CAP\_ABORT** message will be retained in the capture file, but audio will not be captured.</span></span> <span data-ttu-id="3a1b9-107">Sie können diese Nachricht explizit oder mithilfe des [**capcaptureabort**](/windows/desktop/api/Vfw/nf-vfw-capcaptureabort) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="3a1b9-107">You can send this message explicitly or by using the [**capCaptureAbort**](/windows/desktop/api/Vfw/nf-vfw-capcaptureabort) macro.</span></span>


```C++
WM_CAP_ABORT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="3a1b9-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3a1b9-108">Return Value</span></span>

<span data-ttu-id="3a1b9-109">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="3a1b9-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a1b9-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3a1b9-110">Remarks</span></span>

<span data-ttu-id="3a1b9-111">Der Aufzeichnungs Vorgang muss durchführen, um diese Meldung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="3a1b9-111">The capture operation must yield to use this message.</span></span>

<span data-ttu-id="3a1b9-112">Verwenden Sie die Stop-Nachricht der [**WM- \_ Obergrenze \_**](wm-cap-stop.md) , um die Schritt Erfassung an der aktuellen Position anzuhalten und dann Audiodaten aufzuzeichnen.</span><span class="sxs-lookup"><span data-stu-id="3a1b9-112">Use the [**WM\_CAP\_STOP**](wm-cap-stop.md) message to halt step capture at the current position, and then capture audio.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a1b9-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3a1b9-113">Requirements</span></span>



| <span data-ttu-id="3a1b9-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3a1b9-114">Requirement</span></span> | <span data-ttu-id="3a1b9-115">Wert</span><span class="sxs-lookup"><span data-stu-id="3a1b9-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3a1b9-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3a1b9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3a1b9-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3a1b9-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3a1b9-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3a1b9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3a1b9-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3a1b9-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3a1b9-120">Header</span><span class="sxs-lookup"><span data-stu-id="3a1b9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a1b9-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a1b9-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a1b9-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3a1b9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a1b9-123">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="3a1b9-123">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="3a1b9-124">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="3a1b9-124">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





