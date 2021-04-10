---
title: MCIWNDM_SETOWNER Meldung (VFW. h)
description: Die mciwndm \_ SetOwner-Nachricht legt das Fenster fest, um dem mciwnd-Fenster zugeordnete Benachrichtigungs Meldungen zu empfangen. Sie können diese Nachricht explizit oder mit dem mciwndltowner-Makro senden.
ms.assetid: c2d0f9d5-bf60-4036-a613-65ba1ed83110
keywords:
- MCIWNDM_SETOWNER-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_SETOWNER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3989632e83a65cda5e805bd91da3f502ca387d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104720"
---
# <a name="mciwndm_setowner-message"></a><span data-ttu-id="b8504-105">Mciwndm- \_ Abmeldung</span><span class="sxs-lookup"><span data-stu-id="b8504-105">MCIWNDM\_SETOWNER message</span></span>

<span data-ttu-id="b8504-106">Die **mciwndm \_ SetOwner** -Nachricht legt das Fenster fest, um dem mciwnd-Fenster zugeordnete Benachrichtigungs Meldungen zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="b8504-106">The **MCIWNDM\_SETOWNER** message sets the window to receive notification messages associated with the MCIWnd window.</span></span> <span data-ttu-id="b8504-107">Sie können diese Nachricht explizit oder mit dem [**mciwndltowner**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner) -Makro senden.</span><span class="sxs-lookup"><span data-stu-id="b8504-107">You can send this message explicitly or by using the [**MCIWndSetOwner**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner) macro.</span></span>


```C++
MCIWNDM_SETOWNER 
wParam = (WPARAM) hwndP; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="b8504-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b8504-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8504-109"><span id="hwndP"></span><span id="hwndp"></span><span id="HWNDP"></span>*hwndp*</span><span class="sxs-lookup"><span data-stu-id="b8504-109"><span id="hwndP"></span><span id="hwndp"></span><span id="HWNDP"></span>*hwndP*</span></span>
</dt> <dd>

<span data-ttu-id="b8504-110">Handle für das Fenster, um die Benachrichtigungs Meldungen zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="b8504-110">Handle to the window to receive the notification messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8504-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b8504-111">Return Value</span></span>

<span data-ttu-id="b8504-112">Gibt 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="b8504-112">Returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8504-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b8504-113">Requirements</span></span>



| <span data-ttu-id="b8504-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b8504-114">Requirement</span></span> | <span data-ttu-id="b8504-115">Wert</span><span class="sxs-lookup"><span data-stu-id="b8504-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b8504-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b8504-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b8504-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b8504-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b8504-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b8504-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b8504-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b8504-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b8504-120">Header</span><span class="sxs-lookup"><span data-stu-id="b8504-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8504-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8504-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8504-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8504-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8504-123">**Mciwndseetowner**</span><span class="sxs-lookup"><span data-stu-id="b8504-123">**MCIWndSetOwner**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner)
</dt> </dl>

 

 





