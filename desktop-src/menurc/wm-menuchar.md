---
title: WM_MENUCHAR Meldung (Winuser. h)
description: Wird gesendet, wenn ein Menü aktiv ist und der Benutzer eine Taste drückt, die keiner mnetmonischen oder Zugriffstaste entspricht. Diese Meldung wird an das Fenster gesendet, das das Menü besitzt.
ms.assetid: de6c91bb-80fd-44b2-8d96-d016477a6547
keywords:
- WM_MENUCHAR von Meldungs Menüs und anderen Ressourcen
topic_type:
- apiref
api_name:
- WM_MENUCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a278e4a1b4333631741a6a542318a8a55e40b512
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743832"
---
# <a name="wm_menuchar-message"></a><span data-ttu-id="f5581-105">WM- \_ menuchar-Meldung</span><span class="sxs-lookup"><span data-stu-id="f5581-105">WM\_MENUCHAR message</span></span>

<span data-ttu-id="f5581-106">Wird gesendet, wenn ein Menü aktiv ist und der Benutzer eine Taste drückt, die keiner mnetmonischen oder Zugriffstaste entspricht.</span><span class="sxs-lookup"><span data-stu-id="f5581-106">Sent when a menu is active and the user presses a key that does not correspond to any mnemonic or accelerator key.</span></span> <span data-ttu-id="f5581-107">Diese Meldung wird an das Fenster gesendet, das das Menü besitzt.</span><span class="sxs-lookup"><span data-stu-id="f5581-107">This message is sent to the window that owns the menu.</span></span>


```C++
#define WM_MENUCHAR                     0x0120
```



## <a name="parameters"></a><span data-ttu-id="f5581-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5581-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5581-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f5581-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f5581-110">Das nieder wertige Wort gibt den Zeichencode an, der dem vom Benutzer gedrückten Schlüssel entspricht.</span><span class="sxs-lookup"><span data-stu-id="f5581-110">The low-order word specifies the character code that corresponds to the key the user pressed.</span></span>

<span data-ttu-id="f5581-111">Das höchst wertige Wort gibt den aktiven Menütyp an.</span><span class="sxs-lookup"><span data-stu-id="f5581-111">The high-order word specifies the active menu type.</span></span> <span data-ttu-id="f5581-112">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="f5581-112">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="f5581-113">Wert</span><span class="sxs-lookup"><span data-stu-id="f5581-113">Value</span></span>                                                                                                                                                                                                                 | <span data-ttu-id="f5581-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f5581-114">Meaning</span></span>                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <span data-ttu-id="f5581-115"><dt>**MF \_ Popup**</dt> <dt>0x00000010l</dt></span><span class="sxs-lookup"><span data-stu-id="f5581-115"><dt>**MF\_POPUP**</dt> <dt>0x00000010L</dt></span></span> </dl>       | <span data-ttu-id="f5581-116">Ein Dropdown Menü, ein Untermenü oder ein Kontextmenü.</span><span class="sxs-lookup"><span data-stu-id="f5581-116">A drop-down menu, submenu, or shortcut menu.</span></span><br/> |
| <span id="MF_SYSMENU"></span><span id="mf_sysmenu"></span><dl> <span data-ttu-id="f5581-117"><dt>**MF \_ Sysmenu**</dt> <dt>0x00002000l</dt></span><span class="sxs-lookup"><span data-stu-id="f5581-117"><dt>**MF\_SYSMENU**</dt> <dt>0x00002000L</dt></span></span> </dl> | <span data-ttu-id="f5581-118">Das Fenstermenü.</span><span class="sxs-lookup"><span data-stu-id="f5581-118">The window menu.</span></span><br/>                             |



 

</dd> <dt>

<span data-ttu-id="f5581-119">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f5581-119">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f5581-120">Ein Handle für das aktive Menü.</span><span class="sxs-lookup"><span data-stu-id="f5581-120">A handle to the active menu.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5581-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f5581-121">Return value</span></span>

<span data-ttu-id="f5581-122">Eine Anwendung, die diese Nachricht verarbeitet, sollte einen der folgenden Werte im höherwertigen Wort des Rückgabewerts zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="f5581-122">An application that processes this message should return one of the following values in the high-order word of the return value.</span></span>



| <span data-ttu-id="f5581-123">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="f5581-123">Return code/value</span></span>                                                                                                                                  | <span data-ttu-id="f5581-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f5581-124">Description</span></span>                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f5581-125"><dt>**MNC \_ Schließen**</dt> Sie <dt>1</dt> .</span><span class="sxs-lookup"><span data-stu-id="f5581-125"><dt>**MNC\_CLOSE**</dt> <dt>1</dt></span></span> </dl>   | <span data-ttu-id="f5581-126">Informiert das System, dass es das aktive Menü schließen soll.</span><span class="sxs-lookup"><span data-stu-id="f5581-126">Informs the system that it should close the active menu.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="f5581-127"><dt>**MNC \_**</dt> <dt>2</dt> ausführen</span><span class="sxs-lookup"><span data-stu-id="f5581-127"><dt>**MNC\_EXECUTE**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="f5581-128">Informiert das System, dass es das im nieder wertigen Wort des Rückgabewerts angegebene Element auswählen soll.</span><span class="sxs-lookup"><span data-stu-id="f5581-128">Informs the system that it should choose the item specified in the low-order word of the return value.</span></span> <span data-ttu-id="f5581-129">Das Besitzer Fenster empfängt eine [**WM- \_ Befehls**](wm-command.md) Meldung.</span><span class="sxs-lookup"><span data-stu-id="f5581-129">The owner window receives a [**WM\_COMMAND**](wm-command.md) message.</span></span><br/> |
| <dl> <span data-ttu-id="f5581-130"><dt>**MNC \_**</dt> <dt>0</dt> ignorieren</span><span class="sxs-lookup"><span data-stu-id="f5581-130"><dt>**MNC\_IGNORE**</dt> <dt>0</dt></span></span> </dl>  | <span data-ttu-id="f5581-131">Informiert das System darüber, dass das vom Benutzer gedrückte Zeichen verworfen und auf dem System Sprecher ein kurzes Signal erstellt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="f5581-131">Informs the system that it should discard the character the user pressed and create a short beep on the system speaker.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="f5581-132"><dt>**MNC \_**</dt> <dt>3</dt> auswählen</span><span class="sxs-lookup"><span data-stu-id="f5581-132"><dt>**MNC\_SELECT**</dt> <dt>3</dt></span></span> </dl>  | <span data-ttu-id="f5581-133">Informiert das System, dass es das im nieder wertigen Wort des Rückgabewerts angegebene Element auswählen soll.</span><span class="sxs-lookup"><span data-stu-id="f5581-133">Informs the system that it should select the item specified in the low-order word of the return value.</span></span> <br/>                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="f5581-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f5581-134">Remarks</span></span>

<span data-ttu-id="f5581-135">Das nieder wertige Wort wird ignoriert, wenn das höchst wertige Wort 0 oder 1 enthält.</span><span class="sxs-lookup"><span data-stu-id="f5581-135">The low-order word is ignored if the high-order word contains 0 or 1.</span></span>

<span data-ttu-id="f5581-136">Eine Anwendung sollte diese Nachricht verarbeiten, wenn eine Zugriffstaste verwendet wird, um ein Menü Element auszuwählen, das eine Bitmap anzeigt.</span><span class="sxs-lookup"><span data-stu-id="f5581-136">An application should process this message when an accelerator is used to select a menu item that displays a bitmap.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5581-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f5581-137">Requirements</span></span>



| <span data-ttu-id="f5581-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f5581-138">Requirement</span></span> | <span data-ttu-id="f5581-139">Wert</span><span class="sxs-lookup"><span data-stu-id="f5581-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5581-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f5581-140">Minimum supported client</span></span><br/> | <span data-ttu-id="f5581-141">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f5581-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f5581-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f5581-142">Minimum supported server</span></span><br/> | <span data-ttu-id="f5581-143">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f5581-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f5581-144">Header</span><span class="sxs-lookup"><span data-stu-id="f5581-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5581-145"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="f5581-145"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5581-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5581-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="f5581-147">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="f5581-147">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="f5581-148">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f5581-148">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="f5581-149">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f5581-149">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="f5581-150">**Licher**</span><span class="sxs-lookup"><span data-stu-id="f5581-150">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f5581-151">Tastaturkürzel</span><span class="sxs-lookup"><span data-stu-id="f5581-151">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 

