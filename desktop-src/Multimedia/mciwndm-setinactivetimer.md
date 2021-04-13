---
title: MCIWNDM_SETINACTIVETIMER Meldung (VFW. h)
description: Die mciwndm \_ setinactivetimer-Nachricht legt den von mciwnd verwendeten Aktualisierungs Zeitraum fest, um die TrackBar im mciwnd-Fenster zu aktualisieren, Positionsinformationen zu aktualisieren, die in der Fenstertitelleiste angezeigt werden, und Benachrichtigungs Meldungen an das übergeordnete Fenster zu senden, wenn das mciwnd-Fenster inaktiv ist. Sie können diese Nachricht explizit oder mithilfe des Makros "mciwndsegtinactivetimer" senden.
ms.assetid: 8900c372-0493-4a63-a027-ef6ecf8f8254
keywords:
- MCIWNDM_SETINACTIVETIMER-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_SETINACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4504d84b254dfb67616568f5f97bba8e3bc2e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518251"
---
# <a name="mciwndm_setinactivetimer-message"></a><span data-ttu-id="29058-105">Mciwndm \* \_ tinactivetimer-Nachricht</span><span class="sxs-lookup"><span data-stu-id="29058-105">MCIWNDM\_SETINACTIVETIMER message</span></span>

<span data-ttu-id="29058-106">Die **mciwndm \_ setinactivetimer** -Nachricht legt den von mciwnd verwendeten Aktualisierungs Zeitraum fest, um die TrackBar im mciwnd-Fenster zu aktualisieren, Positionsinformationen zu aktualisieren, die in der Fenstertitelleiste angezeigt werden, und Benachrichtigungs Meldungen an das übergeordnete Fenster zu senden, wenn das mciwnd-Fenster inaktiv ist.</span><span class="sxs-lookup"><span data-stu-id="29058-106">The **MCIWNDM\_SETINACTIVETIMER** message sets the update period used by MCIWnd to update the trackbar in the MCIWnd window, update position information displayed in the window title bar, and send notification messages to the parent window when the MCIWnd window is inactive.</span></span> <span data-ttu-id="29058-107">Sie können diese Nachricht explizit oder mithilfe des Makros " [**mciwndsegtinactivetimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer) " senden.</span><span class="sxs-lookup"><span data-stu-id="29058-107">You can send this message explicitly or by using the [**MCIWndSetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer) macro.</span></span>


```C++
MCIWNDM_SETINACTIVETIMER 
wParam = (WPARAM) (UINT) inactive; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="29058-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="29058-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29058-109"><span id="inactive"></span><span id="INACTIVE"></span>*VSTE*</span><span class="sxs-lookup"><span data-stu-id="29058-109"><span id="inactive"></span><span id="INACTIVE"></span>*inactive*</span></span>
</dt> <dd>

<span data-ttu-id="29058-110">Aktualisierungs Zeitraum in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="29058-110">Update period, in milliseconds.</span></span> <span data-ttu-id="29058-111">Der Standardwert ist 2000 Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="29058-111">The default is 2000 milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29058-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="29058-112">Return Value</span></span>

<span data-ttu-id="29058-113">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="29058-113">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="29058-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="29058-114">Requirements</span></span>



| <span data-ttu-id="29058-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="29058-115">Requirement</span></span> | <span data-ttu-id="29058-116">Wert</span><span class="sxs-lookup"><span data-stu-id="29058-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="29058-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="29058-117">Minimum supported client</span></span><br/> | <span data-ttu-id="29058-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="29058-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="29058-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="29058-119">Minimum supported server</span></span><br/> | <span data-ttu-id="29058-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="29058-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="29058-121">Header</span><span class="sxs-lookup"><span data-stu-id="29058-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="29058-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="29058-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29058-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="29058-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29058-124">**Mciwndstitinactivetimer**</span><span class="sxs-lookup"><span data-stu-id="29058-124">**MCIWndSetInactiveTimer**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer)
</dt> </dl>

 

 





