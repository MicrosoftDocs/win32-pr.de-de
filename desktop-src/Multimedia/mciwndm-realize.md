---
title: MCIWNDM_REALIZE Meldung (VFW. h)
description: Die mciwndm- \_ Meldung "erkennen" erkennt die Palette, die zurzeit vom MCI-Gerät in einem mciwnd-Fenster verwendet wird. Dieses Makro wird mit der Meldung "mciwndm-Erkenntnis" definiert \_ . Sie können diese Nachricht explizit oder mithilfe des mciwndrealize-Makros senden.
ms.assetid: fe8803b5-3500-44b4-97f7-784bedf0b362
keywords:
- MCIWNDM_REALIZE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_REALIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ef3a803791a4f8dfe94d128d42ea06a7b28e739
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949483"
---
# <a name="mciwndm_realize-message"></a><span data-ttu-id="4be8c-106">Mciwndm-Fehler \_ Meldung</span><span class="sxs-lookup"><span data-stu-id="4be8c-106">MCIWNDM\_REALIZE message</span></span>

<span data-ttu-id="4be8c-107">Die **mciwndm \_** -Meldung "erkennen" erkennt die Palette, die zurzeit vom MCI-Gerät in einem mciwnd-Fenster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4be8c-107">The **MCIWNDM\_REALIZE** message realizes the palette currently used by the MCI device in an MCIWnd window.</span></span> <span data-ttu-id="4be8c-108">Dieses Makro wird mit der Meldung " **mciwndm- \_ Erkenntnis** " definiert.</span><span class="sxs-lookup"><span data-stu-id="4be8c-108">This macro is defined with the **MCIWNDM\_REALIZE** message.</span></span> <span data-ttu-id="4be8c-109">Sie können diese Nachricht explizit oder mithilfe des [**mciwndrealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="4be8c-109">You can send this message explicitly or by using the [**MCIWndRealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize) macro.</span></span>


```C++
MCIWNDM_REALIZE 
wParam = (WPARAM) (BOOL) fBkgnd; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="4be8c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4be8c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4be8c-111"><span id="fBkgnd"></span><span id="fbkgnd"></span><span id="FBKGND"></span>*"f"*</span><span class="sxs-lookup"><span data-stu-id="4be8c-111"><span id="fBkgnd"></span><span id="fbkgnd"></span><span id="FBKGND"></span>*fBkgnd*</span></span>
</dt> <dd>

<span data-ttu-id="4be8c-112">Hintergrundflag.</span><span class="sxs-lookup"><span data-stu-id="4be8c-112">Background flag.</span></span> <span data-ttu-id="4be8c-113">Geben Sie **true** für diesen Parameter an, wenn das Fenster eine Hintergrund Anwendung ist.</span><span class="sxs-lookup"><span data-stu-id="4be8c-113">Specify **TRUE** for this parameter if the window is a background application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4be8c-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4be8c-114">Return Value</span></span>

<span data-ttu-id="4be8c-115">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="4be8c-115">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4be8c-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4be8c-116">Remarks</span></span>

<span data-ttu-id="4be8c-117">**Mciwndm \_ "Erkennen** " verwendet die Palette des MCI-Geräts und ruft die [**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="4be8c-117">**MCIWNDM\_REALIZE** uses the palette of the MCI device and calls the [**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) function.</span></span> <span data-ttu-id="4be8c-118">Wenn die Anwendung die Nachrichten " [**WM \_ palettechanged**](/windows/desktop/gdi/wm-palettechanged) " und " [**WM \_ querynewpalette**](/windows/desktop/gdi/wm-querynewpalette) " explizit verarbeitet, sollten Sie diese Meldung in der Anwendung verwenden, anstatt **RealizePalette** zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="4be8c-118">If your application explicitly handles the [**WM\_PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) and [**WM\_QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) messages, you should use this message in your application instead of using **RealizePalette**.</span></span> <span data-ttu-id="4be8c-119">Wenn der Text eines dieser Nachrichten Handler nur **RealizePalette** enthält, leiten Sie die Nachricht an das mciwnd-Fenster weiter, wodurch die Palette automatisch erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="4be8c-119">If the body of one of these message handlers contains only **RealizePalette**, forward the message to the MCIWnd window, which will automatically realize the palette.</span></span>

## <a name="requirements"></a><span data-ttu-id="4be8c-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4be8c-120">Requirements</span></span>



| <span data-ttu-id="4be8c-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4be8c-121">Requirement</span></span> | <span data-ttu-id="4be8c-122">Wert</span><span class="sxs-lookup"><span data-stu-id="4be8c-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4be8c-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4be8c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4be8c-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4be8c-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="4be8c-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4be8c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4be8c-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4be8c-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="4be8c-127">Header</span><span class="sxs-lookup"><span data-stu-id="4be8c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="4be8c-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="4be8c-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4be8c-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4be8c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4be8c-130">**Mciwndrealize**</span><span class="sxs-lookup"><span data-stu-id="4be8c-130">**MCIWndRealize**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize)
</dt> <dt>

[<span data-ttu-id="4be8c-131">**RealizePalette**</span><span class="sxs-lookup"><span data-stu-id="4be8c-131">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="4be8c-132">**WM \_ palettechanged**</span><span class="sxs-lookup"><span data-stu-id="4be8c-132">**WM\_PALETTECHANGED**</span></span>](/windows/desktop/gdi/wm-palettechanged)
</dt> <dt>

[<span data-ttu-id="4be8c-133">**WM \_ querynewpalette**</span><span class="sxs-lookup"><span data-stu-id="4be8c-133">**WM\_QUERYNEWPALETTE**</span></span>](/windows/desktop/gdi/wm-querynewpalette)
</dt> </dl>

 

