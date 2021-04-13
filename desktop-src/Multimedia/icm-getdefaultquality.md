---
title: ICM_GETDEFAULTQUALITY Meldung (VFW. h)
description: Die ICM \_ getdefaultquality-Meldung fragt einen Video Komprimierungs Treiber ab, um die Standardeinstellung für die Qualität bereitzustellen. Sie können diese Nachricht explizit oder mithilfe des icgetdefaultquality-Makros senden.
ms.assetid: bba7f451-52c2-4684-a7c9-e4b05cb946c5
keywords:
- ICM_GETDEFAULTQUALITY-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_GETDEFAULTQUALITY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4350539851ca720e3538d297f955a56fedfc4a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475699"
---
# <a name="icm_getdefaultquality-message"></a><span data-ttu-id="8b5d4-105">ICM \_ getdefaultquality-Meldung</span><span class="sxs-lookup"><span data-stu-id="8b5d4-105">ICM\_GETDEFAULTQUALITY message</span></span>

<span data-ttu-id="8b5d4-106">Die **ICM \_ getdefaultquality** -Meldung fragt einen Video Komprimierungs Treiber ab, um die Standardeinstellung für die Qualität bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="8b5d4-106">The **ICM\_GETDEFAULTQUALITY** message queries a video compression driver to provide its default quality setting.</span></span> <span data-ttu-id="8b5d4-107">Sie können diese Nachricht explizit oder mithilfe des [**icgetdefaultquality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="8b5d4-107">You can send this message explicitly or by using the [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) macro.</span></span>


```C++
ICM_GETDEFAULTQUALITY 
wParam = (DWORD_PTR) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="8b5d4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b5d4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b5d4-109"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwicvalue*</span><span class="sxs-lookup"><span data-stu-id="8b5d4-109"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*</span></span>
</dt> <dd>

<span data-ttu-id="8b5d4-110">Adresse, die den Standardwert für die Qualität enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="8b5d4-110">Address to contain the default quality value.</span></span> <span data-ttu-id="8b5d4-111">Qualitätswerte liegen im Bereich von 0 bis 10.000.</span><span class="sxs-lookup"><span data-stu-id="8b5d4-111">Quality values range from 0 to 10,000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b5d4-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8b5d4-112">Return Value</span></span>

<span data-ttu-id="8b5d4-113">Gibt ICERR \_ OK zurück, wenn der Treiber diese Nachricht unterstützt oder wenn ICERR \_ andernfalls nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="8b5d4-113">Returns ICERR\_OK if the driver supports this message or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b5d4-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b5d4-114">Requirements</span></span>



| <span data-ttu-id="8b5d4-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b5d4-115">Requirement</span></span> | <span data-ttu-id="8b5d4-116">Wert</span><span class="sxs-lookup"><span data-stu-id="8b5d4-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8b5d4-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8b5d4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8b5d4-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b5d4-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="8b5d4-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8b5d4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8b5d4-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b5d4-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8b5d4-121">Header</span><span class="sxs-lookup"><span data-stu-id="8b5d4-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b5d4-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b5d4-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b5d4-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b5d4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b5d4-124">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="8b5d4-124">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="8b5d4-125">Video Komprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="8b5d4-125">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





