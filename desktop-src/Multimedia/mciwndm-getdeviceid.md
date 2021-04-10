---
title: MCIWNDM_GETDEVICEID Meldung (VFW. h)
description: Die mciwndm \_ getdeviceid-Meldung Ruft den Bezeichner des derzeit geöffneten MCI-Geräts ab, das mit der mciSendCommand-Funktion verwendet werden soll. Sie können diese Nachricht explizit oder mit dem mciwndgetdeviceid-Makro senden.
ms.assetid: 188f15fa-579a-438e-a812-9a2b684127c0
keywords:
- MCIWNDM_GETDEVICEID-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_GETDEVICEID
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f2271b18dcf8f295594031ab2c7c80dd8dec06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040217"
---
# <a name="mciwndm_getdeviceid-message"></a><span data-ttu-id="e6e42-105">Mciwndm \_ getdeviceid-Meldung</span><span class="sxs-lookup"><span data-stu-id="e6e42-105">MCIWNDM\_GETDEVICEID message</span></span>

<span data-ttu-id="e6e42-106">Die **mciwndm \_ getdeviceid** -Meldung Ruft den Bezeichner des derzeit geöffneten MCI-Geräts ab, das mit der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e6e42-106">The **MCIWNDM\_GETDEVICEID** message retrieves the identifier of the currently open MCI device to use with the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span> <span data-ttu-id="e6e42-107">Sie können diese Nachricht explizit oder mit dem [**mciwndgetdeviceid**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid) -Makro senden.</span><span class="sxs-lookup"><span data-stu-id="e6e42-107">You can send this message explicitly or by using the [**MCIWndGetDeviceID**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid) macro.</span></span>


```C++
MCIWNDM_GETDEVICEID 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="e6e42-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e6e42-108">Return Value</span></span>

<span data-ttu-id="e6e42-109">Gibt den Geräte Bezeichner zurück.</span><span class="sxs-lookup"><span data-stu-id="e6e42-109">Returns the device identifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6e42-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e6e42-110">Requirements</span></span>



| <span data-ttu-id="e6e42-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e6e42-111">Requirement</span></span> | <span data-ttu-id="e6e42-112">Wert</span><span class="sxs-lookup"><span data-stu-id="e6e42-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e6e42-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e6e42-113">Minimum supported client</span></span><br/> | <span data-ttu-id="e6e42-114">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e6e42-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e6e42-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e6e42-115">Minimum supported server</span></span><br/> | <span data-ttu-id="e6e42-116">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e6e42-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e6e42-117">Header</span><span class="sxs-lookup"><span data-stu-id="e6e42-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6e42-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6e42-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6e42-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6e42-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="e6e42-120">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e6e42-120">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e6e42-121">**Mciwndgetde viceid**</span><span class="sxs-lookup"><span data-stu-id="e6e42-121">**MCIWndGetDeviceID**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid)
</dt> </dl>

 

