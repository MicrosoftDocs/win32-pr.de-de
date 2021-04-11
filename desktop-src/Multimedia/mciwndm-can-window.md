---
title: MCIWNDM_CAN_WINDOW Meldung (VFW. h)
description: Die Meldung "mciwndm \_ kann \_ ein Fenster" bestimmt, ob ein MCI-Gerät Fenster orientierte MCI-Befehle unterstützt. Sie können diese Nachricht explizit oder mithilfe des mciwndcanwindow-Makros senden.
ms.assetid: bf89c096-1272-441e-9334-2b4215dbc979
keywords:
- MCIWNDM_CAN_WINDOW-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_WINDOW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d638b61093483b6e834b57af1d5c892d77d0f1d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949756"
---
# <a name="mciwndm_can_window-message"></a><span data-ttu-id="39018-105">Mciwndm \_ kann \_ Nachricht Fenster</span><span class="sxs-lookup"><span data-stu-id="39018-105">MCIWNDM\_CAN\_WINDOW message</span></span>

<span data-ttu-id="39018-106">Die Meldung " **mciwndm \_ kann ein \_ Fenster** " bestimmt, ob ein MCI-Gerät Fenster orientierte MCI-Befehle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="39018-106">The **MCIWNDM\_CAN\_WINDOW** message determines if an MCI device supports window-oriented MCI commands.</span></span> <span data-ttu-id="39018-107">Sie können diese Nachricht explizit oder mithilfe des [**mciwndcanwindow**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="39018-107">You can send this message explicitly or by using the [**MCIWndCanWindow**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow) macro.</span></span>


```C++
MCIWNDM_CAN_WINDOW 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="39018-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="39018-108">Return Value</span></span>

<span data-ttu-id="39018-109">Gibt " **true** " zurück, wenn das Gerät Fenster orientierte MCI-Befehle unterstützt, andernfalls " **false** ".</span><span class="sxs-lookup"><span data-stu-id="39018-109">Returns **TRUE** if the device supports window-oriented MCI commands or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="39018-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39018-110">Requirements</span></span>



| <span data-ttu-id="39018-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="39018-111">Requirement</span></span> | <span data-ttu-id="39018-112">Wert</span><span class="sxs-lookup"><span data-stu-id="39018-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="39018-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="39018-113">Minimum supported client</span></span><br/> | <span data-ttu-id="39018-114">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39018-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="39018-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="39018-115">Minimum supported server</span></span><br/> | <span data-ttu-id="39018-116">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39018-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="39018-117">Header</span><span class="sxs-lookup"><span data-stu-id="39018-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="39018-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="39018-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39018-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39018-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39018-120">**Mciwndcanwindow**</span><span class="sxs-lookup"><span data-stu-id="39018-120">**MCIWndCanWindow**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow)
</dt> </dl>

 

 





