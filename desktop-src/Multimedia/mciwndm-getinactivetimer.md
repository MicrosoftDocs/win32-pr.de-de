---
title: MCIWNDM_GETINACTIVETIMER Meldung (VFW. h)
description: Die mciwndm \_ getinactivetimer-Nachricht Ruft den Aktualisierungs Zeitraum ab, der verwendet wird, wenn das mciwnd-Fenster das inaktive Fenster ist. Sie können diese Nachricht explizit oder mithilfe des Makros mciwndgetinactivetimer senden.
ms.assetid: 84e00d2f-2cf8-4b6b-a8cb-7eb320754783
keywords:
- MCIWNDM_GETINACTIVETIMER-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_GETINACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a270aeffdee59b7749aa87a0e711204960d74d7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339123"
---
# <a name="mciwndm_getinactivetimer-message"></a><span data-ttu-id="fbf59-105">Mciwndm \_ getinactivetimer-Nachricht</span><span class="sxs-lookup"><span data-stu-id="fbf59-105">MCIWNDM\_GETINACTIVETIMER message</span></span>

<span data-ttu-id="fbf59-106">Die **mciwndm \_ getinactivetimer** -Nachricht Ruft den Aktualisierungs Zeitraum ab, der verwendet wird, wenn das mciwnd-Fenster das inaktive Fenster ist.</span><span class="sxs-lookup"><span data-stu-id="fbf59-106">The **MCIWNDM\_GETINACTIVETIMER** message retrieves the update period used when the MCIWnd window is the inactive window.</span></span> <span data-ttu-id="fbf59-107">Sie können diese Nachricht explizit oder mithilfe des Makros [**mciwndgetinactivetimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer) senden.</span><span class="sxs-lookup"><span data-stu-id="fbf59-107">You can send this message explicitly or by using the [**MCIWndGetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer) macro.</span></span>


```C++
MCIWNDM_GETINACTIVETIMER 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="fbf59-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fbf59-108">Return Value</span></span>

<span data-ttu-id="fbf59-109">Gibt den Aktualisierungs Zeitraum in Millisekunden zurück.</span><span class="sxs-lookup"><span data-stu-id="fbf59-109">Returns the update period, in milliseconds.</span></span> <span data-ttu-id="fbf59-110">Der Standardwert beträgt 2.000 Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="fbf59-110">The default value is 2000 milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbf59-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fbf59-111">Requirements</span></span>



| <span data-ttu-id="fbf59-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fbf59-112">Requirement</span></span> | <span data-ttu-id="fbf59-113">Wert</span><span class="sxs-lookup"><span data-stu-id="fbf59-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="fbf59-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fbf59-114">Minimum supported client</span></span><br/> | <span data-ttu-id="fbf59-115">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fbf59-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="fbf59-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fbf59-116">Minimum supported server</span></span><br/> | <span data-ttu-id="fbf59-117">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fbf59-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="fbf59-118">Header</span><span class="sxs-lookup"><span data-stu-id="fbf59-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbf59-119"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbf59-119"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbf59-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fbf59-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbf59-121">**Mciwndgetinactivetimer**</span><span class="sxs-lookup"><span data-stu-id="fbf59-121">**MCIWndGetInactiveTimer**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer)
</dt> </dl>

 

 





