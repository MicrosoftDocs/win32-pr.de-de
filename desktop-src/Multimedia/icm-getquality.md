---
title: ICM_GETQUALITY Meldung (VFW. h)
description: Die ICM \_ getquality-Nachricht fragt einen Video Komprimierungs Treiber ab, um die aktuelle Qualitätseinstellung zurückzugeben.
ms.assetid: 8da99a26-7b2a-4118-89e1-7485915cbdc9
keywords:
- ICM_GETQUALITY-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_GETQUALITY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c4fa2a26e1fe5fa111585ce0a59422a2fe9b072
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957237"
---
# <a name="icm_getquality-message"></a><span data-ttu-id="d5c41-104">ICM \_ getquality-Meldung</span><span class="sxs-lookup"><span data-stu-id="d5c41-104">ICM\_GETQUALITY message</span></span>

<span data-ttu-id="d5c41-105">Die **ICM \_ getquality** -Nachricht fragt einen Video Komprimierungs Treiber ab, um die aktuelle Qualitätseinstellung zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="d5c41-105">The **ICM\_GETQUALITY** message queries a video compression driver to return its current quality setting.</span></span>


```C++
ICM_GETQUALITY 
wParam = (DWORD) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="d5c41-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d5c41-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5c41-107"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwicvalue*</span><span class="sxs-lookup"><span data-stu-id="d5c41-107"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*</span></span>
</dt> <dd>

<span data-ttu-id="d5c41-108">Adresse, die den aktuellen Qualitäts Wert enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="d5c41-108">Address to contain the current quality value.</span></span> <span data-ttu-id="d5c41-109">Qualitätswerte liegen im Bereich von 0 bis 10.000.</span><span class="sxs-lookup"><span data-stu-id="d5c41-109">Quality values range from 0 to 10,000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5c41-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d5c41-110">Return Value</span></span>

<span data-ttu-id="d5c41-111">Gibt ICERR \_ OK zurück, wenn der Treiber diese Nachricht unterstützt oder wenn ICERR \_ andernfalls nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="d5c41-111">Returns ICERR\_OK if the driver supports this message or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5c41-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d5c41-112">Requirements</span></span>



| <span data-ttu-id="d5c41-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d5c41-113">Requirement</span></span> | <span data-ttu-id="d5c41-114">Wert</span><span class="sxs-lookup"><span data-stu-id="d5c41-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d5c41-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d5c41-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d5c41-116">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d5c41-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d5c41-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d5c41-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d5c41-118">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d5c41-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d5c41-119">Header</span><span class="sxs-lookup"><span data-stu-id="d5c41-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5c41-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5c41-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5c41-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d5c41-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5c41-122">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="d5c41-122">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="d5c41-123">Video Komprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="d5c41-123">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





