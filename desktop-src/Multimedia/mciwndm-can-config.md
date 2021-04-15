---
title: MCIWNDM_CAN_CONFIG Meldung (VFW. h)
description: Die Meldung mciwndm \_ CAN \_ config bestimmt, ob ein MCI-Gerät ein Konfigurations Dialogfeld anzeigen kann. Sie können diese Nachricht explizit oder mithilfe des mciwndcanconfig-Makros senden.
ms.assetid: f1eb22a8-d0fc-4d2c-a414-392e560cfbed
keywords:
- MCIWNDM_CAN_CONFIG-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_CONFIG
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 816a8c1dfaec6fc7d7854f8873ce05e74e4de6bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479137"
---
# <a name="mciwndm_can_config-message"></a><span data-ttu-id="93546-105">Mciwndm \_ kann \_ Nachricht konfigurieren</span><span class="sxs-lookup"><span data-stu-id="93546-105">MCIWNDM\_CAN\_CONFIG message</span></span>

<span data-ttu-id="93546-106">Die Meldung **mciwndm \_ CAN \_ config** bestimmt, ob ein MCI-Gerät ein Konfigurations Dialogfeld anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="93546-106">The **MCIWNDM\_CAN\_CONFIG** message determines if an MCI device can display a configuration dialog box.</span></span> <span data-ttu-id="93546-107">Sie können diese Nachricht explizit oder mithilfe des [**mciwndcanconfig**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="93546-107">You can send this message explicitly or by using the [**MCIWndCanConfig**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig) macro.</span></span>


```C++
MCIWNDM_CAN_CONFIG 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="93546-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="93546-108">Return Value</span></span>

<span data-ttu-id="93546-109">Gibt **true** zurück, wenn das Gerät eine Konfiguration unterstützt, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="93546-109">Returns **TRUE** if the device supports configuration or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="93546-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="93546-110">Requirements</span></span>



| <span data-ttu-id="93546-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="93546-111">Requirement</span></span> | <span data-ttu-id="93546-112">Wert</span><span class="sxs-lookup"><span data-stu-id="93546-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="93546-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="93546-113">Minimum supported client</span></span><br/> | <span data-ttu-id="93546-114">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="93546-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="93546-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="93546-115">Minimum supported server</span></span><br/> | <span data-ttu-id="93546-116">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="93546-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="93546-117">Header</span><span class="sxs-lookup"><span data-stu-id="93546-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="93546-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="93546-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93546-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93546-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93546-120">**Mciwndcanconfig**</span><span class="sxs-lookup"><span data-stu-id="93546-120">**MCIWndCanConfig**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig)
</dt> </dl>

 

 





