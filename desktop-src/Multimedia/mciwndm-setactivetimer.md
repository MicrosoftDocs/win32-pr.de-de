---
title: MCIWNDM_SETACTIVETIMER Meldung (VFW. h)
description: Die mciwndm \_ setactivetimer-Nachricht legt den Update Zeitraum fest, der von mciwnd zum Aktualisieren der TrackBar im mciwnd-Fenster, Aktualisieren der Positionsinformationen, die in der Fenstertitelleiste angezeigt werden, und Senden von Benachrichtigungs Meldungen an das übergeordnete Fenster, wenn das mciwnd-Fenster aktiv ist. Sie können diese Nachricht explizit oder mit dem mciwndabtactivetimer-Makro senden.
ms.assetid: a30c0091-d9bb-44a3-a7b0-d1be30adcd9c
keywords:
- MCIWNDM_SETACTIVETIMER-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_SETACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1924a991f0627009a8e622c8f8be086b2e045635
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104714"
---
# <a name="mciwndm_setactivetimer-message"></a><span data-ttu-id="66ffa-105">Mciwndm- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="66ffa-105">MCIWNDM\_SETACTIVETIMER message</span></span>

<span data-ttu-id="66ffa-106">Die **mciwndm \_ setactivetimer** -Nachricht legt den Update Zeitraum fest, der von mciwnd zum Aktualisieren der TrackBar im mciwnd-Fenster, Aktualisieren der Positionsinformationen, die in der Fenstertitelleiste angezeigt werden, und Senden von Benachrichtigungs Meldungen an das übergeordnete Fenster, wenn das mciwnd-Fenster aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="66ffa-106">The **MCIWNDM\_SETACTIVETIMER** message sets the update period used by MCIWnd to update the trackbar in the MCIWnd window, update position information displayed in the window title bar, and send notification messages to the parent window when the MCIWnd window is active.</span></span> <span data-ttu-id="66ffa-107">Sie können diese Nachricht explizit oder mit dem [**mciwndabtactivetimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer) -Makro senden.</span><span class="sxs-lookup"><span data-stu-id="66ffa-107">You can send this message explicitly or by using the [**MCIWndSetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer) macro.</span></span>


```C++
MCIWNDM_SETACTIVETIMER 
wParam = (WPARAM) (UINT) active; 
lParam = 0L; 
```



## <a name="parameters"></a><span data-ttu-id="66ffa-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="66ffa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66ffa-109"><span id="active"></span><span id="ACTIVE"></span>*enden*</span><span class="sxs-lookup"><span data-stu-id="66ffa-109"><span id="active"></span><span id="ACTIVE"></span>*active*</span></span>
</dt> <dd>

<span data-ttu-id="66ffa-110">Aktualisierungs Zeitraum in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="66ffa-110">Update period, in milliseconds.</span></span> <span data-ttu-id="66ffa-111">Der Standardwert ist 500 Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="66ffa-111">The default is 500 milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66ffa-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="66ffa-112">Return Value</span></span>

<span data-ttu-id="66ffa-113">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="66ffa-113">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="66ffa-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="66ffa-114">Requirements</span></span>



| <span data-ttu-id="66ffa-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="66ffa-115">Requirement</span></span> | <span data-ttu-id="66ffa-116">Wert</span><span class="sxs-lookup"><span data-stu-id="66ffa-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="66ffa-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="66ffa-117">Minimum supported client</span></span><br/> | <span data-ttu-id="66ffa-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="66ffa-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="66ffa-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="66ffa-119">Minimum supported server</span></span><br/> | <span data-ttu-id="66ffa-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="66ffa-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="66ffa-121">Header</span><span class="sxs-lookup"><span data-stu-id="66ffa-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="66ffa-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="66ffa-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66ffa-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66ffa-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66ffa-124">**Mciwndabtactivetimer**</span><span class="sxs-lookup"><span data-stu-id="66ffa-124">**MCIWndSetActiveTimer**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer)
</dt> </dl>

 

 





