---
title: MCIWNDM_SETVOLUME Meldung (VFW. h)
description: Die mciwndm- \_ Nachricht SetVolume legt die Volumeebene eines MCI-Geräts fest. Sie können diese Nachricht explizit oder mithilfe des Makros mciwndsetvolume senden.
ms.assetid: 04151588-b761-447a-9a57-808c034c3059
keywords:
- MCIWNDM_SETVOLUME-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_SETVOLUME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2215f8df3ea6f7b36b224318ebac68175ff9c265
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740232"
---
# <a name="mciwndm_setvolume-message"></a><span data-ttu-id="d58ba-105">Mciwndm- \_ SetVolume-Meldung</span><span class="sxs-lookup"><span data-stu-id="d58ba-105">MCIWNDM\_SETVOLUME message</span></span>

<span data-ttu-id="d58ba-106">Die **mciwndm-Nachricht \_ SetVolume** legt die Volumeebene eines MCI-Geräts fest.</span><span class="sxs-lookup"><span data-stu-id="d58ba-106">The **MCIWNDM\_SETVOLUME** message sets the volume level of an MCI device.</span></span> <span data-ttu-id="d58ba-107">Sie können diese Nachricht explizit oder mithilfe des Makros [**mciwndsetvolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume) senden.</span><span class="sxs-lookup"><span data-stu-id="d58ba-107">You can send this message explicitly or by using the [**MCIWndSetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume) macro.</span></span>


```C++
MCIWNDM_SETVOLUME 
wParam = 0; 
lParam = (LPARAM) (UINT) iVol; 
```



## <a name="parameters"></a><span data-ttu-id="d58ba-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d58ba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d58ba-109"><span id="iVol"></span><span id="ivol"></span><span id="IVOL"></span>*ivol*</span><span class="sxs-lookup"><span data-stu-id="d58ba-109"><span id="iVol"></span><span id="ivol"></span><span id="IVOL"></span>*iVol*</span></span>
</dt> <dd>

<span data-ttu-id="d58ba-110">Neue Volumeebene.</span><span class="sxs-lookup"><span data-stu-id="d58ba-110">New volume level.</span></span> <span data-ttu-id="d58ba-111">Geben Sie 1000 für die normale Volumeebene an.</span><span class="sxs-lookup"><span data-stu-id="d58ba-111">Specify 1000 for normal volume level.</span></span> <span data-ttu-id="d58ba-112">Geben Sie einen höheren Wert für ein höheres Volume oder einen niedrigeren Wert für ein ruhigeres Volume an.</span><span class="sxs-lookup"><span data-stu-id="d58ba-112">Specify a higher value for a louder volume or a lower value for a quieter volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d58ba-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d58ba-113">Return Value</span></span>

<span data-ttu-id="d58ba-114">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="d58ba-114">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d58ba-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d58ba-115">Requirements</span></span>



| <span data-ttu-id="d58ba-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d58ba-116">Requirement</span></span> | <span data-ttu-id="d58ba-117">Wert</span><span class="sxs-lookup"><span data-stu-id="d58ba-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d58ba-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d58ba-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d58ba-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d58ba-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d58ba-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d58ba-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d58ba-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d58ba-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d58ba-122">Header</span><span class="sxs-lookup"><span data-stu-id="d58ba-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d58ba-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="d58ba-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d58ba-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d58ba-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d58ba-125">**Mciwndsetvolume**</span><span class="sxs-lookup"><span data-stu-id="d58ba-125">**MCIWndSetVolume**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume)
</dt> </dl>

 

 





