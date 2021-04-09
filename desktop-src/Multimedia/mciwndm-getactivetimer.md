---
title: MCIWNDM_GETACTIVETIMER Meldung (VFW. h)
description: Die mciwndm \_ getactivetimer-Nachricht Ruft den Aktualisierungs Zeitraum ab, der verwendet wird, wenn das mciwnd-Fenster das aktive Fenster ist. Sie können diese Nachricht explizit oder mithilfe des Makros mciwndgetactivetimer senden.
ms.assetid: f9e6f9ed-75fd-4e45-ad92-79a82d8d572c
keywords:
- MCIWNDM_GETACTIVETIMER-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_GETACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cb86fc2940c8bd5d82c004754b81e5389ada892
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106532"
---
# <a name="mciwndm_getactivetimer-message"></a><span data-ttu-id="4baaa-105">Mciwndm \_ getactivetimer-Nachricht</span><span class="sxs-lookup"><span data-stu-id="4baaa-105">MCIWNDM\_GETACTIVETIMER message</span></span>

<span data-ttu-id="4baaa-106">Die **mciwndm \_ getactivetimer** -Nachricht Ruft den Aktualisierungs Zeitraum ab, der verwendet wird, wenn das mciwnd-Fenster das aktive Fenster ist.</span><span class="sxs-lookup"><span data-stu-id="4baaa-106">The **MCIWNDM\_GETACTIVETIMER** message retrieves the update period used when the MCIWnd window is the active window.</span></span> <span data-ttu-id="4baaa-107">Sie können diese Nachricht explizit oder mithilfe des Makros [**mciwndgetactivetimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer) senden.</span><span class="sxs-lookup"><span data-stu-id="4baaa-107">You can send this message explicitly or by using the [**MCIWndGetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer) macro.</span></span>


```C++
MCIWNDM_GETACTIVETIMER 
wParam = 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="4baaa-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4baaa-108">Return Value</span></span>

<span data-ttu-id="4baaa-109">Gibt den Update Zeitraum in Millisekunden zurück.</span><span class="sxs-lookup"><span data-stu-id="4baaa-109">Returns the update period in milliseconds.</span></span> <span data-ttu-id="4baaa-110">Der Standardwert ist 500 Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="4baaa-110">The default is 500 milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="4baaa-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4baaa-111">Requirements</span></span>



| <span data-ttu-id="4baaa-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4baaa-112">Requirement</span></span> | <span data-ttu-id="4baaa-113">Wert</span><span class="sxs-lookup"><span data-stu-id="4baaa-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4baaa-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4baaa-114">Minimum supported client</span></span><br/> | <span data-ttu-id="4baaa-115">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4baaa-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="4baaa-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4baaa-116">Minimum supported server</span></span><br/> | <span data-ttu-id="4baaa-117">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4baaa-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="4baaa-118">Header</span><span class="sxs-lookup"><span data-stu-id="4baaa-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="4baaa-119"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="4baaa-119"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4baaa-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4baaa-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4baaa-121">**Mciwndgetactivetimer**</span><span class="sxs-lookup"><span data-stu-id="4baaa-121">**MCIWndGetActiveTimer**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer)
</dt> </dl>

 

 





