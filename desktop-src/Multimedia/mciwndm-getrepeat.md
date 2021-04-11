---
title: MCIWNDM_GETREPEAT Meldung (VFW. h)
description: Die mciwndm \_ getretorf-Nachricht bestimmt, ob die fortlaufende Wiedergabe aktiviert wurde. Sie können diese Nachricht explizit oder mithilfe des mciwndgetrepeat-Makros senden.
ms.assetid: 6d644117-e705-421f-b45f-9f0e833e6bc8
keywords:
- MCIWNDM_GETREPEAT-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_GETREPEAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef47dc4f639c7aa34f7a00341e6ad2e19be909d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103050"
---
# <a name="mciwndm_getrepeat-message"></a><span data-ttu-id="389f1-105">Mciwndm \_ getretorf-Nachricht</span><span class="sxs-lookup"><span data-stu-id="389f1-105">MCIWNDM\_GETREPEAT message</span></span>

<span data-ttu-id="389f1-106">Die **mciwndm \_ getretorf** -Nachricht bestimmt, ob die fortlaufende Wiedergabe aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="389f1-106">The **MCIWNDM\_GETREPEAT** message determines if continuous playback has been activated.</span></span> <span data-ttu-id="389f1-107">Sie können diese Nachricht explizit oder mithilfe des [**mciwndgetrepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="389f1-107">You can send this message explicitly or by using the [**MCIWndGetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat) macro.</span></span>


```C++
MCIWNDM_GETREPEAT 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="389f1-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="389f1-108">Return Value</span></span>

<span data-ttu-id="389f1-109">Gibt **true** zurück, wenn die fortlaufende Wiedergabe aktiviert ist, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="389f1-109">Returns **TRUE** if continuous playback is activated or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="389f1-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="389f1-110">Requirements</span></span>



| <span data-ttu-id="389f1-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="389f1-111">Requirement</span></span> | <span data-ttu-id="389f1-112">Wert</span><span class="sxs-lookup"><span data-stu-id="389f1-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="389f1-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="389f1-113">Minimum supported client</span></span><br/> | <span data-ttu-id="389f1-114">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="389f1-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="389f1-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="389f1-115">Minimum supported server</span></span><br/> | <span data-ttu-id="389f1-116">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="389f1-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="389f1-117">Header</span><span class="sxs-lookup"><span data-stu-id="389f1-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="389f1-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="389f1-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="389f1-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="389f1-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="389f1-120">**Mciwndgetrepeat**</span><span class="sxs-lookup"><span data-stu-id="389f1-120">**MCIWndGetRepeat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat)
</dt> </dl>

 

 





