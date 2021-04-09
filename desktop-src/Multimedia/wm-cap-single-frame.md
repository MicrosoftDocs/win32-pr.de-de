---
title: WM_CAP_SINGLE_FRAME Meldung (VFW. h)
description: Die "WM \_ Cap \_ Single Frame"- \_ Nachricht fügt einen einzelnen Frame an eine Erfassungs Datei an, die mithilfe der Open-Message-Nachricht für das WM-Cap geöffnet wurde \_ \_ \_ \_ . Sie können diese Nachricht explizit oder mithilfe des capcapturesingleframe-Makros senden.
ms.assetid: 95466961-0719-4ff7-afc8-f7bf0e0974ac
keywords:
- WM_CAP_SINGLE_FRAME-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_SINGLE_FRAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a919036ee38fdcf00f55c3d4044cd3f45bd13c82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106100"
---
# <a name="wm_cap_single_frame-message"></a><span data-ttu-id="72a79-105">WM- \_ Cap- \_ Einzel \_ Rahmen Nachricht</span><span class="sxs-lookup"><span data-stu-id="72a79-105">WM\_CAP\_SINGLE\_FRAME message</span></span>

<span data-ttu-id="72a79-106">Die " **WM \_ Cap \_ Single \_ Frame** "-Nachricht fügt einen einzelnen Frame an eine Erfassungs Datei an, die mithilfe der [**\_ \_ \_ \_ Open**](wm-cap-single-frame-open.md) -Message-Nachricht für das WM-Cap geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="72a79-106">The **WM\_CAP\_SINGLE\_FRAME** message appends a single frame to a capture file that was opened using the [**WM\_CAP\_SINGLE\_FRAME\_OPEN**](wm-cap-single-frame-open.md) message.</span></span> <span data-ttu-id="72a79-107">Sie können diese Nachricht explizit oder mithilfe des [**capcapturesingleframe**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframe) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="72a79-107">You can send this message explicitly or by using the [**capCaptureSingleFrame**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframe) macro.</span></span>


```C++
WM_CAP_SINGLE_FRAME 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="72a79-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="72a79-108">Return Value</span></span>

<span data-ttu-id="72a79-109">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="72a79-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="72a79-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="72a79-110">Requirements</span></span>



| <span data-ttu-id="72a79-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="72a79-111">Requirement</span></span> | <span data-ttu-id="72a79-112">Wert</span><span class="sxs-lookup"><span data-stu-id="72a79-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="72a79-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="72a79-113">Minimum supported client</span></span><br/> | <span data-ttu-id="72a79-114">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="72a79-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="72a79-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="72a79-115">Minimum supported server</span></span><br/> | <span data-ttu-id="72a79-116">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="72a79-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="72a79-117">Header</span><span class="sxs-lookup"><span data-stu-id="72a79-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="72a79-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="72a79-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72a79-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="72a79-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72a79-120">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="72a79-120">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="72a79-121">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="72a79-121">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





