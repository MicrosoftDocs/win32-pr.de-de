---
title: MCIWNDM_VALIDATEMEDIA Meldung (VFW. h)
description: Die mciwndm \_ validatemedia-Nachricht aktualisiert die Start-und Endpositionen des Inhalts, die aktuelle Position im Inhalt und die TrackBar gemäß dem aktuellen Zeitformat.
ms.assetid: 98ac6227-fc90-4276-8e26-2bd005e35dc6
keywords:
- MCIWNDM_VALIDATEMEDIA-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_VALIDATEMEDIA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43cb6e6a4a7c320d4eb6472c3c72da2843d0814c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517411"
---
# <a name="mciwndm_validatemedia-message"></a><span data-ttu-id="412a4-104">Mciwndm \_ validatemedia-Meldung</span><span class="sxs-lookup"><span data-stu-id="412a4-104">MCIWNDM\_VALIDATEMEDIA message</span></span>

<span data-ttu-id="412a4-105">Die **mciwndm \_ validatemedia** -Nachricht aktualisiert die Start-und Endpositionen des Inhalts, die aktuelle Position im Inhalt und die TrackBar gemäß dem aktuellen Zeitformat.</span><span class="sxs-lookup"><span data-stu-id="412a4-105">The **MCIWNDM\_VALIDATEMEDIA** message updates the starting and ending locations of the content, the current position in the content, and the trackbar according to the current time format.</span></span> <span data-ttu-id="412a4-106">Sie können diese Nachricht explizit oder mithilfe des [**mciwndvalidatemedia**](/windows/desktop/api/Vfw/nf-vfw-mciwndvalidatemedia) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="412a4-106">You can send this message explicitly or by using the [**MCIWndValidateMedia**](/windows/desktop/api/Vfw/nf-vfw-mciwndvalidatemedia) macro.</span></span>


```C++
MCIWNDM_VALIDATEMEDIA 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="412a4-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="412a4-107">Return Value</span></span>

<span data-ttu-id="412a4-108">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="412a4-108">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="412a4-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="412a4-109">Remarks</span></span>

<span data-ttu-id="412a4-110">In der Regel sollten Sie dieses Makro nicht verwenden. Wenn Ihre Anwendung jedoch das Zeitformat eines Geräts ohne Verwendung von mciwnd ändert, die Start-und Endpositionen des Inhalts sowie die TrackBar verwenden weiterhin das alte Format.</span><span class="sxs-lookup"><span data-stu-id="412a4-110">Typically, you should not need to use this macro; however, if your application changes the time format of a device without using MCIWnd; the starting and ending locations of the content, as well as the trackbar, continue to use the old format.</span></span> <span data-ttu-id="412a4-111">Mit diesem Makro können Sie diese Werte aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="412a4-111">You can use this macro to update these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="412a4-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="412a4-112">Requirements</span></span>



| <span data-ttu-id="412a4-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="412a4-113">Requirement</span></span> | <span data-ttu-id="412a4-114">Wert</span><span class="sxs-lookup"><span data-stu-id="412a4-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="412a4-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="412a4-115">Minimum supported client</span></span><br/> | <span data-ttu-id="412a4-116">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="412a4-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="412a4-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="412a4-117">Minimum supported server</span></span><br/> | <span data-ttu-id="412a4-118">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="412a4-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="412a4-119">Header</span><span class="sxs-lookup"><span data-stu-id="412a4-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="412a4-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="412a4-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="412a4-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="412a4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="412a4-122">**Mciwndvalidatemedia**</span><span class="sxs-lookup"><span data-stu-id="412a4-122">**MCIWndValidateMedia**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndvalidatemedia)
</dt> </dl>

 

 





