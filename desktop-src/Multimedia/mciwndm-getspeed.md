---
title: MCIWNDM_GETSPEED Meldung (VFW. h)
description: Die mciwndm \_ getspeed-Meldung Ruft die Wiedergabegeschwindigkeit eines MCI-Geräts ab. Sie können diese Nachricht explizit oder mithilfe des mciwndgetspeed-Makros senden.
ms.assetid: d10a8f88-e85e-449b-8655-bb0832031d59
keywords:
- MCIWNDM_GETSPEED-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_GETSPEED
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c84a8ebb3e97d4543f68f3a237add8eed7706ae2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478927"
---
# <a name="mciwndm_getspeed-message"></a><span data-ttu-id="7814d-105">Mciwndm \_ getspeed-Meldung</span><span class="sxs-lookup"><span data-stu-id="7814d-105">MCIWNDM\_GETSPEED message</span></span>

<span data-ttu-id="7814d-106">Die **mciwndm \_ getspeed** -Meldung Ruft die Wiedergabegeschwindigkeit eines MCI-Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="7814d-106">The **MCIWNDM\_GETSPEED** message retrieves the playback speed of an MCI device.</span></span> <span data-ttu-id="7814d-107">Sie können diese Nachricht explizit oder mithilfe des [**mciwndgetspeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="7814d-107">You can send this message explicitly or by using the [**MCIWndGetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed) macro.</span></span>


```C++
MCIWNDM_GETSPEED 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="7814d-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7814d-108">Return Value</span></span>

<span data-ttu-id="7814d-109">Gibt die Wiedergabegeschwindigkeit zurück, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="7814d-109">Returns the playback speed if successful.</span></span> <span data-ttu-id="7814d-110">Der Wert für die normale Geschwindigkeit ist 1000.</span><span class="sxs-lookup"><span data-stu-id="7814d-110">The value for normal speed is 1000.</span></span> <span data-ttu-id="7814d-111">Größere Werte weisen auf schnellere Geschwindigkeiten hin, kleinere Werte auf langsamere Geschwindigkeiten.</span><span class="sxs-lookup"><span data-stu-id="7814d-111">Larger values indicate faster speeds, smaller values indicate slower speeds.</span></span>

## <a name="requirements"></a><span data-ttu-id="7814d-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7814d-112">Requirements</span></span>



| <span data-ttu-id="7814d-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7814d-113">Requirement</span></span> | <span data-ttu-id="7814d-114">Wert</span><span class="sxs-lookup"><span data-stu-id="7814d-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7814d-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7814d-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7814d-116">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7814d-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7814d-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7814d-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7814d-118">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7814d-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7814d-119">Header</span><span class="sxs-lookup"><span data-stu-id="7814d-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="7814d-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="7814d-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7814d-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7814d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7814d-122">**Mciwndgetspeed**</span><span class="sxs-lookup"><span data-stu-id="7814d-122">**MCIWndGetSpeed**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed)
</dt> </dl>

 

 





