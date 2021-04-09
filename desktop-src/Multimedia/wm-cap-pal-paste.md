---
title: WM_CAP_PAL_PASTE Meldung (VFW. h)
description: Die WM \_ \_ -Cap \_ -PAL-Einfüge Nachricht kopiert die Palette aus der Zwischenablage und übergibt sie an einen Aufzeichnungs Treiber. Sie können diese Nachricht explizit oder mithilfe des cappalettepaste-Makros senden.
ms.assetid: d49c7fd9-be40-4a07-8339-b85f7c4c331e
keywords:
- WM_CAP_PAL_PASTE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_PAL_PASTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3daf88c69edbb8bad6257456b95a86c8a68df328
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949677"
---
# <a name="wm_cap_pal_paste-message"></a><span data-ttu-id="e5eff-105">WM- \_ Obergrenze für \_ PAL- \_ Einfügen</span><span class="sxs-lookup"><span data-stu-id="e5eff-105">WM\_CAP\_PAL\_PASTE message</span></span>

<span data-ttu-id="e5eff-106">Die **WM- \_ Cap-PAL- \_ \_ Einfüge** Nachricht kopiert die Palette aus der Zwischenablage und übergibt sie an einen Aufzeichnungs Treiber.</span><span class="sxs-lookup"><span data-stu-id="e5eff-106">The **WM\_CAP\_PAL\_PASTE** message copies the palette from the clipboard and passes it to a capture driver.</span></span> <span data-ttu-id="e5eff-107">Sie können diese Nachricht explizit oder mithilfe des [**cappalettepaste**](/windows/desktop/api/Vfw/nf-vfw-cappalettepaste) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="e5eff-107">You can send this message explicitly or by using the [**capPalettePaste**](/windows/desktop/api/Vfw/nf-vfw-cappalettepaste) macro.</span></span>


```C++
WM_CAP_PAL_PASTE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="e5eff-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e5eff-108">Return Value</span></span>

<span data-ttu-id="e5eff-109">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="e5eff-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="e5eff-110">Wenn ein Fehler auftritt und eine Fehler Rückruffunktion mithilfe der WM- [**\_ Cap- \_ \_ Rückruf \_ Fehlermeldung**](wm-cap-set-callback-error.md) festgelegt wird, wird die Fehler Rückruffunktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="e5eff-110">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5eff-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e5eff-111">Remarks</span></span>

<span data-ttu-id="e5eff-112">Ein Aufzeichnungs Treiber verwendet eine Palette, wenn dies für das angegebene digitalisierte Videoformat erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="e5eff-112">A capture driver uses a palette when required by the specified digitized video format.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5eff-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e5eff-113">Requirements</span></span>



| <span data-ttu-id="e5eff-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e5eff-114">Requirement</span></span> | <span data-ttu-id="e5eff-115">Wert</span><span class="sxs-lookup"><span data-stu-id="e5eff-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e5eff-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e5eff-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e5eff-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e5eff-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e5eff-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e5eff-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e5eff-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e5eff-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e5eff-120">Header</span><span class="sxs-lookup"><span data-stu-id="e5eff-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5eff-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5eff-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5eff-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e5eff-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5eff-123">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="e5eff-123">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="e5eff-124">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="e5eff-124">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





