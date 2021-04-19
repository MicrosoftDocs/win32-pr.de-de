---
title: MCIWNDM_CAN_PLAY Meldung (VFW. h)
description: Die mciwndm \_ kann \_ Nachricht wiedergeben bestimmt, ob ein MCI-Gerät eine Datendatei oder einen Inhalt einer anderen Art wiedergeben kann. Sie können diese Nachricht explizit oder mithilfe des mciwndcanplay-Makros senden.
ms.assetid: dbb742b0-b8ab-4b80-96da-c4823a4747c9
keywords:
- MCIWNDM_CAN_PLAY-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_PLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 043a0fc15260f7448df8d009a6b468616244269d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346763"
---
# <a name="mciwndm_can_play-message"></a><span data-ttu-id="5f1f9-105">Mciwndm \_ kann \_ Nachricht wiedergeben</span><span class="sxs-lookup"><span data-stu-id="5f1f9-105">MCIWNDM\_CAN\_PLAY message</span></span>

<span data-ttu-id="5f1f9-106">Die **mciwndm \_ kann \_** Nachricht wiedergeben bestimmt, ob ein MCI-Gerät eine Datendatei oder einen Inhalt einer anderen Art wiedergeben kann.</span><span class="sxs-lookup"><span data-stu-id="5f1f9-106">The **MCIWNDM\_CAN\_PLAY** message determines if an MCI device can play a data file or content of some other kind.</span></span> <span data-ttu-id="5f1f9-107">Sie können diese Nachricht explizit oder mithilfe des [**mciwndcanplay**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="5f1f9-107">You can send this message explicitly or by using the [**MCIWndCanPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay) macro.</span></span>


```C++
MCIWNDM_CAN_PLAY 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="5f1f9-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5f1f9-108">Return Value</span></span>

<span data-ttu-id="5f1f9-109">Gibt **true** zurück, wenn das Gerät die Wiedergabe der Daten unterstützt, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="5f1f9-109">Returns **TRUE** if the device supports playing the data or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f1f9-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5f1f9-110">Requirements</span></span>



| <span data-ttu-id="5f1f9-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5f1f9-111">Requirement</span></span> | <span data-ttu-id="5f1f9-112">Wert</span><span class="sxs-lookup"><span data-stu-id="5f1f9-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5f1f9-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5f1f9-113">Minimum supported client</span></span><br/> | <span data-ttu-id="5f1f9-114">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5f1f9-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="5f1f9-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5f1f9-115">Minimum supported server</span></span><br/> | <span data-ttu-id="5f1f9-116">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5f1f9-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5f1f9-117">Header</span><span class="sxs-lookup"><span data-stu-id="5f1f9-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f1f9-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f1f9-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f1f9-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f1f9-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f1f9-120">**Mciwndcanplay**</span><span class="sxs-lookup"><span data-stu-id="5f1f9-120">**MCIWndCanPlay**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay)
</dt> </dl>

 

 





