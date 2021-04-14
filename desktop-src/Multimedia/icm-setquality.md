---
title: ICM_SETQUALITY Meldung (VFW. h)
description: Die ICM \_ setquality-Meldung enthält einen Video Komprimierungs Treiber mit einer Qualitätsstufe, die während der Komprimierung verwendet werden soll.
ms.assetid: 487ff1de-7178-440a-b38d-0b82a30d7297
keywords:
- ICM_SETQUALITY-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_SETQUALITY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a1523996ad336e64d4b34143cc26cd8d0937d5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392232"
---
# <a name="icm_setquality-message"></a><span data-ttu-id="d576f-104">ICM- \_ setquality-Meldung</span><span class="sxs-lookup"><span data-stu-id="d576f-104">ICM\_SETQUALITY message</span></span>

<span data-ttu-id="d576f-105">Die **ICM \_ setquality** -Meldung enthält einen Video Komprimierungs Treiber mit einer Qualitätsstufe, die während der Komprimierung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d576f-105">The **ICM\_SETQUALITY** message provides a video compression driver with a quality level to use during compression.</span></span>


```C++
ICM_SETQUALITY 
wParam = (DWORD) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="d576f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d576f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d576f-107"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwicvalue*</span><span class="sxs-lookup"><span data-stu-id="d576f-107"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*</span></span>
</dt> <dd>

<span data-ttu-id="d576f-108">Neuer Qualitäts Wert.</span><span class="sxs-lookup"><span data-stu-id="d576f-108">New quality value.</span></span> <span data-ttu-id="d576f-109">Qualitätswerte liegen im Bereich von 0 bis 10.000.</span><span class="sxs-lookup"><span data-stu-id="d576f-109">Quality values range from 0 to 10,000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d576f-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d576f-110">Return Value</span></span>

<span data-ttu-id="d576f-111">Gibt ICERR \_ OK zurück, wenn der Treiber diese Nachricht unterstützt oder wenn ICERR \_ andernfalls nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="d576f-111">Returns ICERR\_OK if the driver supports this message or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d576f-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d576f-112">Requirements</span></span>



| <span data-ttu-id="d576f-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d576f-113">Requirement</span></span> | <span data-ttu-id="d576f-114">Wert</span><span class="sxs-lookup"><span data-stu-id="d576f-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d576f-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d576f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d576f-116">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d576f-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d576f-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d576f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d576f-118">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d576f-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d576f-119">Header</span><span class="sxs-lookup"><span data-stu-id="d576f-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="d576f-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="d576f-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d576f-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d576f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d576f-122">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="d576f-122">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="d576f-123">Video Komprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="d576f-123">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





