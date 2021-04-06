---
title: MCIWNDM_CAN_EJECT Meldung (VFW. h)
description: Die mciwndm \_ - \_ Nachricht kann ermitteln, ob ein MCI-Gerät seine Medien auswerfen kann. Sie können diese Nachricht explizit oder mithilfe des mciwndcaneject-Makros senden.
ms.assetid: e9bd33c4-0ad8-4c0a-8b75-52011b58904d
keywords:
- MCIWNDM_CAN_EJECT-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_EJECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00ba54c9263e23fdd9830be892e4559ae3755c07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743688"
---
# <a name="mciwndm_can_eject-message"></a><span data-ttu-id="96e24-105">Mciwndm \_ kann \_ Nachricht Auswerfen</span><span class="sxs-lookup"><span data-stu-id="96e24-105">MCIWNDM\_CAN\_EJECT message</span></span>

<span data-ttu-id="96e24-106">Die **mciwndm-Nachricht \_ kann \_** ermitteln, ob ein MCI-Gerät seine Medien auswerfen kann.</span><span class="sxs-lookup"><span data-stu-id="96e24-106">The **MCIWNDM\_CAN\_EJECT** message determines if an MCI device can eject its media.</span></span> <span data-ttu-id="96e24-107">Sie können diese Nachricht explizit oder mithilfe des [**mciwndcaneject**](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="96e24-107">You can send this message explicitly or by using the [**MCIWndCanEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject) macro.</span></span>


```C++
MCIWNDM_CAN_EJECT 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="96e24-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="96e24-108">Return Value</span></span>

<span data-ttu-id="96e24-109">Gibt " **true** " zurück, wenn das Gerät seine Medien auswerfen kann, andernfalls " **false** ".</span><span class="sxs-lookup"><span data-stu-id="96e24-109">Returns **TRUE** if the device can eject its media or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="96e24-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="96e24-110">Requirements</span></span>



| <span data-ttu-id="96e24-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="96e24-111">Requirement</span></span> | <span data-ttu-id="96e24-112">Wert</span><span class="sxs-lookup"><span data-stu-id="96e24-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="96e24-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="96e24-113">Minimum supported client</span></span><br/> | <span data-ttu-id="96e24-114">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="96e24-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="96e24-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="96e24-115">Minimum supported server</span></span><br/> | <span data-ttu-id="96e24-116">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="96e24-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="96e24-117">Header</span><span class="sxs-lookup"><span data-stu-id="96e24-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="96e24-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="96e24-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96e24-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="96e24-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96e24-120">**Mciwndcaneject**</span><span class="sxs-lookup"><span data-stu-id="96e24-120">**MCIWndCanEject**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject)
</dt> </dl>

 

 





