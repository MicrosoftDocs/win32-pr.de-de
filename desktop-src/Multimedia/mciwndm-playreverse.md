---
title: MCIWNDM_PLAYREVERSE Meldung (VFW. h)
description: Die mciwndm \_ -playreverse-Nachricht gibt den aktuellen Inhalt in umgekehrter Richtung an, beginnend an der aktuellen Position und endet am Anfang des Inhalts, oder bis ein anderer Befehl die Wiedergabe beendet.
ms.assetid: 93a22454-eca6-453f-abbe-6cf20198dbad
keywords:
- MCIWNDM_PLAYREVERSE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_PLAYREVERSE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84b0a2e230e3c57e8314e455be5dfbc5cea2c013
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102839"
---
# <a name="mciwndm_playreverse-message"></a><span data-ttu-id="57652-104">Mciwndm- \_ playreverse-Nachricht</span><span class="sxs-lookup"><span data-stu-id="57652-104">MCIWNDM\_PLAYREVERSE message</span></span>

<span data-ttu-id="57652-105">Die **mciwndm- \_ playreverse** -Nachricht gibt den aktuellen Inhalt in umgekehrter Richtung an, beginnend an der aktuellen Position und endet am Anfang des Inhalts, oder bis ein anderer Befehl die Wiedergabe beendet.</span><span class="sxs-lookup"><span data-stu-id="57652-105">The **MCIWNDM\_PLAYREVERSE** message plays the current content in the reverse direction, beginning at the current position and ending at the beginning of the content or until another command stops playback.</span></span> <span data-ttu-id="57652-106">Sie können diese Nachricht explizit oder mithilfe des [**mciwndplayreverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="57652-106">You can send this message explicitly or by using the [**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse) macro.</span></span>


```C++
MCIWNDM_PLAYREVERSE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="57652-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="57652-107">Return Value</span></span>

<span data-ttu-id="57652-108">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="57652-108">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="57652-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="57652-109">Requirements</span></span>



| <span data-ttu-id="57652-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="57652-110">Requirement</span></span> | <span data-ttu-id="57652-111">Wert</span><span class="sxs-lookup"><span data-stu-id="57652-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="57652-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="57652-112">Minimum supported client</span></span><br/> | <span data-ttu-id="57652-113">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="57652-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="57652-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="57652-114">Minimum supported server</span></span><br/> | <span data-ttu-id="57652-115">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="57652-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="57652-116">Header</span><span class="sxs-lookup"><span data-stu-id="57652-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="57652-117"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="57652-117"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57652-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="57652-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57652-119">**Mciwndplayreverse**</span><span class="sxs-lookup"><span data-stu-id="57652-119">**MCIWndPlayReverse**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse)
</dt> </dl>

 

 





