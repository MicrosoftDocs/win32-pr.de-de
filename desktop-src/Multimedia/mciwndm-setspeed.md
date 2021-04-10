---
title: MCIWNDM_SETSPEED Meldung (VFW. h)
description: Die mciwndm- \_ setSpeed-Nachricht legt die Wiedergabegeschwindigkeit eines MCI-Geräts fest. Sie können diese Nachricht explizit oder mithilfe des mciwndsetspeed-Makros senden.
ms.assetid: 7658dd25-dc68-4bd1-b995-df06b509be16
keywords:
- MCIWNDM_SETSPEED-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_SETSPEED
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 282bb3a2e135b674605be55aaccaa455d30edbcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956773"
---
# <a name="mciwndm_setspeed-message"></a><span data-ttu-id="6b5da-105">Mciwndm- \_ setSpeed-Meldung</span><span class="sxs-lookup"><span data-stu-id="6b5da-105">MCIWNDM\_SETSPEED message</span></span>

<span data-ttu-id="6b5da-106">Die **mciwndm- \_ setSpeed** -Nachricht legt die Wiedergabegeschwindigkeit eines MCI-Geräts fest.</span><span class="sxs-lookup"><span data-stu-id="6b5da-106">The **MCIWNDM\_SETSPEED** message sets the playback speed of an MCI device.</span></span> <span data-ttu-id="6b5da-107">Sie können diese Nachricht explizit oder mithilfe des [**mciwndsetspeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="6b5da-107">You can send this message explicitly or by using the [**MCIWndSetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed) macro.</span></span>


```C++
MCIWNDM_SETSPEED 
wParam = 0; 
lParam = (LPARAM) (UINT) iSpeed; 
```



## <a name="parameters"></a><span data-ttu-id="6b5da-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b5da-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b5da-109"><span id="iSpeed"></span><span id="ispeed"></span><span id="ISPEED"></span>*iSpeed*</span><span class="sxs-lookup"><span data-stu-id="6b5da-109"><span id="iSpeed"></span><span id="ispeed"></span><span id="ISPEED"></span>*iSpeed*</span></span>
</dt> <dd>

<span data-ttu-id="6b5da-110">Wiedergabegeschwindigkeit.</span><span class="sxs-lookup"><span data-stu-id="6b5da-110">Playback speed.</span></span> <span data-ttu-id="6b5da-111">Geben Sie 1000 für normale Geschwindigkeit, größere Werte für schnellere Geschwindigkeiten und kleinere Werte für langsamere Geschwindigkeiten an.</span><span class="sxs-lookup"><span data-stu-id="6b5da-111">Specify 1000 for normal speed, larger values for faster speeds, and smaller values for slower speeds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b5da-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6b5da-112">Return Value</span></span>

<span data-ttu-id="6b5da-113">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="6b5da-113">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b5da-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b5da-114">Requirements</span></span>



| <span data-ttu-id="6b5da-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b5da-115">Requirement</span></span> | <span data-ttu-id="6b5da-116">Wert</span><span class="sxs-lookup"><span data-stu-id="6b5da-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6b5da-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6b5da-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6b5da-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b5da-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6b5da-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6b5da-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6b5da-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b5da-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6b5da-121">Header</span><span class="sxs-lookup"><span data-stu-id="6b5da-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b5da-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b5da-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b5da-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b5da-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b5da-124">**Mciwndsetspeed**</span><span class="sxs-lookup"><span data-stu-id="6b5da-124">**MCIWndSetSpeed**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed)
</dt> </dl>

 

 





