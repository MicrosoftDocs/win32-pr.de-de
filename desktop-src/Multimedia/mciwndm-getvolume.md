---
title: MCIWNDM_GETVOLUME Meldung (VFW. h)
description: Die mciwndm \_ getvolume-Nachricht Ruft die aktuelle volumeeinstellung eines MCI-Geräts ab. Sie können diese Nachricht explizit oder mithilfe des Makros mciwndgetvolume senden.
ms.assetid: 3f1de023-4da8-4899-accc-409701d6e921
keywords:
- MCIWNDM_GETVOLUME-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_GETVOLUME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4aa11fb13a56dda7cb83e3d6c98b4b66083e91b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392180"
---
# <a name="mciwndm_getvolume-message"></a><span data-ttu-id="15d4a-105">Mciwndm \_ getvolume-Meldung</span><span class="sxs-lookup"><span data-stu-id="15d4a-105">MCIWNDM\_GETVOLUME message</span></span>

<span data-ttu-id="15d4a-106">Die **mciwndm \_ getvolume** -Nachricht Ruft die aktuelle volumeeinstellung eines MCI-Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="15d4a-106">The **MCIWNDM\_GETVOLUME** message retrieves the current volume setting of an MCI device.</span></span> <span data-ttu-id="15d4a-107">Sie können diese Nachricht explizit oder mithilfe des Makros [**mciwndgetvolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume) senden.</span><span class="sxs-lookup"><span data-stu-id="15d4a-107">You can send this message explicitly or by using the [**MCIWndGetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume) macro.</span></span>


```C++
MCIWNDM_GETVOLUME 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="15d4a-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="15d4a-108">Return Value</span></span>

<span data-ttu-id="15d4a-109">Gibt die aktuelle volumeeinstellung zurück.</span><span class="sxs-lookup"><span data-stu-id="15d4a-109">Returns the current volume setting.</span></span> <span data-ttu-id="15d4a-110">Der Standardwert lautet „1000“.</span><span class="sxs-lookup"><span data-stu-id="15d4a-110">The default value is 1000.</span></span> <span data-ttu-id="15d4a-111">Höhere Werte geben höhere Volumes an, niedrigere Werte weisen auf ruhigere Volumes hin.</span><span class="sxs-lookup"><span data-stu-id="15d4a-111">Higher values indicate louder volumes, lower values indicate quieter volumes.</span></span>

## <a name="requirements"></a><span data-ttu-id="15d4a-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="15d4a-112">Requirements</span></span>



| <span data-ttu-id="15d4a-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="15d4a-113">Requirement</span></span> | <span data-ttu-id="15d4a-114">Wert</span><span class="sxs-lookup"><span data-stu-id="15d4a-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="15d4a-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="15d4a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="15d4a-116">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="15d4a-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="15d4a-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="15d4a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="15d4a-118">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="15d4a-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="15d4a-119">Header</span><span class="sxs-lookup"><span data-stu-id="15d4a-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="15d4a-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="15d4a-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15d4a-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15d4a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15d4a-122">**Mciwndgetvolume**</span><span class="sxs-lookup"><span data-stu-id="15d4a-122">**MCIWndGetVolume**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume)
</dt> </dl>

 

 





