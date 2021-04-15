---
title: MCIWNDM_CAN_SAVE Meldung (VFW. h)
description: Die mciwndm \_ kann die \_ Nachricht speichern, um zu ermitteln, ob ein MCI-Gerät Daten speichern kann. Sie können diese Nachricht explizit oder mithilfe des mciwndcansave-Makros senden.
ms.assetid: b4e27190-b095-494b-9ed3-10653bea187b
keywords:
- MCIWNDM_CAN_SAVE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_SAVE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11b60b8a5d93ac80befc8beeb6665399efe44f1e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475681"
---
# <a name="mciwndm_can_save-message"></a><span data-ttu-id="037e9-105">Mciwndm \_ kann \_ Nachricht speichern.</span><span class="sxs-lookup"><span data-stu-id="037e9-105">MCIWNDM\_CAN\_SAVE message</span></span>

<span data-ttu-id="037e9-106">Die **mciwndm \_ kann \_** die Nachricht speichern, um zu ermitteln, ob ein MCI-Gerät Daten speichern kann.</span><span class="sxs-lookup"><span data-stu-id="037e9-106">The **MCIWNDM\_CAN\_SAVE** message determines if an MCI device can save data.</span></span> <span data-ttu-id="037e9-107">Sie können diese Nachricht explizit oder mithilfe des [**mciwndcansave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="037e9-107">You can send this message explicitly or by using the [**MCIWndCanSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave) macro.</span></span>


```C++
MCIWNDM_CAN_SAVE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="037e9-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="037e9-108">Return Value</span></span>

<span data-ttu-id="037e9-109">Gibt **true** zurück, wenn das Gerät das Speichern oder **false** unterstützt.</span><span class="sxs-lookup"><span data-stu-id="037e9-109">Returns **TRUE** if the device supports saving or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="037e9-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="037e9-110">Requirements</span></span>



| <span data-ttu-id="037e9-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="037e9-111">Requirement</span></span> | <span data-ttu-id="037e9-112">Wert</span><span class="sxs-lookup"><span data-stu-id="037e9-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="037e9-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="037e9-113">Minimum supported client</span></span><br/> | <span data-ttu-id="037e9-114">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="037e9-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="037e9-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="037e9-115">Minimum supported server</span></span><br/> | <span data-ttu-id="037e9-116">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="037e9-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="037e9-117">Header</span><span class="sxs-lookup"><span data-stu-id="037e9-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="037e9-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="037e9-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="037e9-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="037e9-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="037e9-120">**Mciwndcansave**</span><span class="sxs-lookup"><span data-stu-id="037e9-120">**MCIWndCanSave**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave)
</dt> </dl>

 

 





