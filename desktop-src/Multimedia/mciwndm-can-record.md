---
title: MCIWNDM_CAN_RECORD Meldung (VFW. h)
description: Die mciwndm \_ kann die \_ Meldung aufzeichnen, ob ein MCI-Gerät eine Aufzeichnung unterstützt. Sie können diese Nachricht explizit oder mithilfe des mciwndcanrecord-Makros senden.
ms.assetid: b5a789fa-6a88-487d-a374-8f4798ee5a62
keywords:
- MCIWNDM_CAN_RECORD-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_RECORD
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2acbc9efa3ca973c12112a599d1202ad936107a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478720"
---
# <a name="mciwndm_can_record-message"></a><span data-ttu-id="b87f1-105">Mciwndm \_ kann \_ Nachricht aufzeichnen</span><span class="sxs-lookup"><span data-stu-id="b87f1-105">MCIWNDM\_CAN\_RECORD message</span></span>

<span data-ttu-id="b87f1-106">Die **mciwndm \_ kann \_** die Meldung aufzeichnen, ob ein MCI-Gerät eine Aufzeichnung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b87f1-106">The **MCIWNDM\_CAN\_RECORD** message determines if an MCI device supports recording.</span></span> <span data-ttu-id="b87f1-107">Sie können diese Nachricht explizit oder mithilfe des [**mciwndcanrecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="b87f1-107">You can send this message explicitly or by using the [**MCIWndCanRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord) macro.</span></span>


```C++
MCIWNDM_CAN_RECORD 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="b87f1-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b87f1-108">Return Value</span></span>

<span data-ttu-id="b87f1-109">Gibt **true** zurück, wenn das Gerät eine Aufzeichnung unterstützt oder andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="b87f1-109">Returns **TRUE** if the device supports recording or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="b87f1-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b87f1-110">Requirements</span></span>



| <span data-ttu-id="b87f1-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b87f1-111">Requirement</span></span> | <span data-ttu-id="b87f1-112">Wert</span><span class="sxs-lookup"><span data-stu-id="b87f1-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b87f1-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b87f1-113">Minimum supported client</span></span><br/> | <span data-ttu-id="b87f1-114">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b87f1-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b87f1-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b87f1-115">Minimum supported server</span></span><br/> | <span data-ttu-id="b87f1-116">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b87f1-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b87f1-117">Header</span><span class="sxs-lookup"><span data-stu-id="b87f1-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="b87f1-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="b87f1-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b87f1-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b87f1-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b87f1-120">**Mciwndcanrecord**</span><span class="sxs-lookup"><span data-stu-id="b87f1-120">**MCIWndCanRecord**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord)
</dt> </dl>

 

 





