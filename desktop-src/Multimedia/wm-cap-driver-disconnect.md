---
title: WM_CAP_DRIVER_DISCONNECT Meldung (VFW. h)
description: Die "WM Cap Driver Disconnect"-Nachricht trennt die Verbindung \_ \_ \_ eines Aufzeichnungs Treibers von einem Aufzeichnungs Fenster. Sie können diese Nachricht explizit oder mithilfe des "capdriverdisconnect"-Makros senden.
ms.assetid: a420f24a-aa7d-4788-9120-2c11e5e2c14c
keywords:
- WM_CAP_DRIVER_DISCONNECT-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_DISCONNECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acad628cc61bbb50c56f68fda91ac87be4feb728
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949752"
---
# <a name="wm_cap_driver_disconnect-message"></a><span data-ttu-id="9691d-105">WM- \_ Cap- \_ Treiber Disconnect- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="9691d-105">WM\_CAP\_DRIVER\_DISCONNECT message</span></span>

<span data-ttu-id="9691d-106">Die " **WM \_ Cap \_ Driver \_ Disconnect** "-Nachricht trennt die Verbindung eines Aufzeichnungs Treibers von einem Aufzeichnungs Fenster.</span><span class="sxs-lookup"><span data-stu-id="9691d-106">The **WM\_CAP\_DRIVER\_DISCONNECT** message disconnects a capture driver from a capture window.</span></span> <span data-ttu-id="9691d-107">Sie können diese Nachricht explizit oder mithilfe des " [**capdriverdisconnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect) "-Makros senden.</span><span class="sxs-lookup"><span data-stu-id="9691d-107">You can send this message explicitly or by using the [**capDriverDisconnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect) macro.</span></span>


```C++
WM_CAP_DRIVER_DISCONNECT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="9691d-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9691d-108">Return Value</span></span>

<span data-ttu-id="9691d-109">Gibt **true** zurück, wenn erfolgreich oder **false** , wenn das Aufzeichnungs Fenster nicht mit einem Aufzeichnungs Treiber verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="9691d-109">Returns **TRUE** if successful or **FALSE** if the capture window is not connected to a capture driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="9691d-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9691d-110">Requirements</span></span>



| <span data-ttu-id="9691d-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9691d-111">Requirement</span></span> | <span data-ttu-id="9691d-112">Wert</span><span class="sxs-lookup"><span data-stu-id="9691d-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9691d-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9691d-113">Minimum supported client</span></span><br/> | <span data-ttu-id="9691d-114">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9691d-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="9691d-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9691d-115">Minimum supported server</span></span><br/> | <span data-ttu-id="9691d-116">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9691d-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9691d-117">Header</span><span class="sxs-lookup"><span data-stu-id="9691d-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="9691d-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="9691d-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9691d-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9691d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9691d-120">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="9691d-120">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="9691d-121">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="9691d-121">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





