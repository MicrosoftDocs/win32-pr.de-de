---
title: ICM_GETDEFAULTKEYFRAMERATE Meldung (VFW. h)
description: Die ICM \_ getdefaultkeyframerate-Nachricht fragt einen Video Komprimierungs Treiber nach dem standardmäßigen (oder bevorzugten) Schlüssel Frame Abstand ab. Sie können diese Nachricht explizit oder mithilfe des icgetdefaulteyframerate-Makros senden.
ms.assetid: 2ebe37cc-3ec2-4b52-bd8f-71c44b704647
keywords:
- ICM_GETDEFAULTKEYFRAMERATE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_GETDEFAULTKEYFRAMERATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64f2796ca1c2de10222330217a0e1deb7883baa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391968"
---
# <a name="icm_getdefaultkeyframerate-message"></a><span data-ttu-id="4fc80-105">ICM \_ getdefaultkeyframerate-Meldung</span><span class="sxs-lookup"><span data-stu-id="4fc80-105">ICM\_GETDEFAULTKEYFRAMERATE message</span></span>

<span data-ttu-id="4fc80-106">Die **ICM \_ getdefaultkeyframerate** -Nachricht fragt einen Video Komprimierungs Treiber nach dem standardmäßigen (oder bevorzugten) Schlüssel Frame Abstand ab.</span><span class="sxs-lookup"><span data-stu-id="4fc80-106">The **ICM\_GETDEFAULTKEYFRAMERATE** message queries a video compression driver for its default (or preferred) key-frame spacing.</span></span> <span data-ttu-id="4fc80-107">Sie können diese Nachricht explizit oder mithilfe des [**icgetdefaulteyframerate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="4fc80-107">You can send this message explicitly or by using the [**ICGetDefaulteyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) macro.</span></span>


```C++
ICM_GETDEFAULTKEYFRAMERATE 
wParam = (DWORD_PTR) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="4fc80-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4fc80-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fc80-109"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwicvalue*</span><span class="sxs-lookup"><span data-stu-id="4fc80-109"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*</span></span>
</dt> <dd>

<span data-ttu-id="4fc80-110">Adresse, die den bevorzugten Schlüssel Frame Abstand enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="4fc80-110">Address to contain the preferred key-frame spacing.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fc80-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4fc80-111">Return Value</span></span>

<span data-ttu-id="4fc80-112">Gibt ICERR \_ OK zurück, wenn der Treiber diese Nachricht unterstützt oder wenn ICERR \_ andernfalls nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="4fc80-112">Returns ICERR\_OK if the driver supports this message or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fc80-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4fc80-113">Requirements</span></span>



| <span data-ttu-id="4fc80-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4fc80-114">Requirement</span></span> | <span data-ttu-id="4fc80-115">Wert</span><span class="sxs-lookup"><span data-stu-id="4fc80-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4fc80-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4fc80-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4fc80-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4fc80-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="4fc80-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4fc80-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4fc80-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4fc80-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="4fc80-120">Header</span><span class="sxs-lookup"><span data-stu-id="4fc80-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4fc80-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="4fc80-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fc80-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4fc80-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fc80-123">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="4fc80-123">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="4fc80-124">Video Komprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="4fc80-124">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





