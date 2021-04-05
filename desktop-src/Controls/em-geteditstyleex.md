---
title: EM_GETEDITSTYLEEX Meldung (RichEdit. h)
description: Ruft die aktuellen Flags für erweiterte Bearbeitungs Stile ab.
ms.assetid: 3E81F7BB-404D-4465-982A-3CF6FD9359DA
keywords:
- Windows-Steuerelemente für EM_GETEDITSTYLEEX Meldung
topic_type:
- apiref
api_name:
- EM_GETEDITSTYLEEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb4077abaedd0c5ec720603d6b23e77950fd5307
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858950"
---
# <a name="em_geteditstyleex-message"></a><span data-ttu-id="af77b-104">EM \_ geteditstyleex-Meldung</span><span class="sxs-lookup"><span data-stu-id="af77b-104">EM\_GETEDITSTYLEEX message</span></span>

<span data-ttu-id="af77b-105">Ruft die aktuellen Flags für erweiterte Bearbeitungs Stile ab.</span><span class="sxs-lookup"><span data-stu-id="af77b-105">Retrieves the current extended edit style flags.</span></span>


```C++
#define EM_GETEDITSTYLEEX       (WM_USER + 276)
```



## <a name="parameters"></a><span data-ttu-id="af77b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="af77b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af77b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="af77b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="af77b-108">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="af77b-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="af77b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="af77b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="af77b-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="af77b-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af77b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="af77b-111">Return value</span></span>

<span data-ttu-id="af77b-112">Gibt die erweiterten Flags für den Bearbeitungs Stil zurück, die einen oder mehrere der folgenden Werte enthalten können.</span><span class="sxs-lookup"><span data-stu-id="af77b-112">Returns the extended edit style flags, which can include one or more of the following values.</span></span>



| <span data-ttu-id="af77b-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="af77b-113">Return code</span></span>                                                                                                | <span data-ttu-id="af77b-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="af77b-114">Description</span></span>                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="af77b-115"><dt>**SES \_ Ex- \_ handlerfriendlyurl**</dt></span><span class="sxs-lookup"><span data-stu-id="af77b-115"><dt>**SES\_EX\_HANDLEFRIENDLYURL**</dt></span></span> </dl>  | <span data-ttu-id="af77b-116">Anzeigen von anzeigen Amen mit derselben Textfarbe und Unterstreichung von automatischen Verknüpfungen, vorausgesetzt, dass die temporäre Formatierung nicht verwendet wurde oder die automatische Text Farbe verwendet (Standard: 0).</span><span class="sxs-lookup"><span data-stu-id="af77b-116">Display friendly name links with the same text color and underlining as automatic links, provided that temporary formatting isn t used or uses text autocolor (default: 0).</span></span><br/>                                                                       |
| <dl> <span data-ttu-id="af77b-117"><dt>**SES \_ Ex \_ multiberühren**</dt></span><span class="sxs-lookup"><span data-stu-id="af77b-117"><dt>**SES\_EX\_MULTITOUCH**</dt></span></span> </dl>         | <span data-ttu-id="af77b-118">Aktivieren Sie die Berührungs Unterstützung in Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="af77b-118">Enable touch support in Rich Edit.</span></span> <span data-ttu-id="af77b-119">Dies schließt Auswahl, Caretzeichen und Kontextmenü Aufrufe ein.</span><span class="sxs-lookup"><span data-stu-id="af77b-119">This includes selection, caret placement, and context-menu invocation.</span></span> <span data-ttu-id="af77b-120">Wenn dieses Flag nicht festgelegt ist, wird die Fingereingabe durch Maus Befehle emuliert, die keine Besonderheiten im Touchscreen berücksichtigen (Standard: 0).</span><span class="sxs-lookup"><span data-stu-id="af77b-120">When this flag is not set, touch is emulated by mouse commands, which do not take touch-mode specifics into account (default: 0).</span></span> <br/>      |
| <dl> <span data-ttu-id="af77b-121"><dt>**SES \_ Ex \_ noacetateselection**</dt></span><span class="sxs-lookup"><span data-stu-id="af77b-121"><dt>**SES\_EX\_NOACETATESELECTION**</dt></span></span> </dl> | <span data-ttu-id="af77b-122">Anzeigen von ausgewähltem Text mit klassischem Windows-Auswahl Text und Hintergrundfarben anstelle der Farbe für den Hintergrund (Standardwert: 0).</span><span class="sxs-lookup"><span data-stu-id="af77b-122">Display selected text using classic Windows selection text and background colors instead of background acetate color (default: 0).</span></span> <br/>                                                                                                               |
| <dl> <span data-ttu-id="af77b-123"><dt>**SES \_ Ex \_ nomath**</dt></span><span class="sxs-lookup"><span data-stu-id="af77b-123"><dt>**SES\_EX\_NOMATH**</dt></span></span> </dl>             | <span data-ttu-id="af77b-124">Einfügen von mathematischen Zonen deaktivieren (Standardwert: 1).</span><span class="sxs-lookup"><span data-stu-id="af77b-124">Disable insertion of math zones (default: 1).</span></span> <span data-ttu-id="af77b-125">Um die mathematische Bearbeitung und Anzeige zu aktivieren, senden Sie die Nachricht [**EM \_ seteditstyleex**](em-seteditstyleex.md) mit *wParam* auf 0 und *LPARAM* auf **SES \_ Ex \_ nomath**.</span><span class="sxs-lookup"><span data-stu-id="af77b-125">To enable math editing and display, send the [**EM\_SETEDITSTYLEEX**](em-seteditstyleex.md) message with *wParam* set to 0, and *lParam* set to **SES\_EX\_NOMATH**.</span></span> <br/>                              |
| <dl> <span data-ttu-id="af77b-126"><dt>**wichtige SES-Werte \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="af77b-126"><dt>**SES\_EX\_NOTABLE**</dt></span></span> </dl>            | <span data-ttu-id="af77b-127">Deaktivieren Sie das Einfügen von Tabellen.</span><span class="sxs-lookup"><span data-stu-id="af77b-127">Disable insertion of tables.</span></span> <span data-ttu-id="af77b-128">Die [**\_ geinsertfähige Nachricht "em insertting**](em-inserttable.md) " gibt " **E \_ Fail** " und RTF-Tabellen übersprungen (Standard: 0).</span><span class="sxs-lookup"><span data-stu-id="af77b-128">The [**EM\_INSERTTABLE**](em-inserttable.md) message returns **E\_FAIL** and RTF tables are skipped (default: 0).</span></span> <br/>                                                                                                  |
| <dl> <span data-ttu-id="af77b-129"><dt>**SES-Zeichen (USA) \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="af77b-129"><dt>**SES\_EX\_USESINGLELINE**</dt></span></span> </dl>      | <span data-ttu-id="af77b-130">Aktivieren Sie ein mehrzeilige Steuerelement, das wie ein einzeilige Steuerelement ausgeführt werden kann, mit der Möglichkeit, vertikal scrollen, wenn die einzeilige Höhe größer als die Fensterhöhe ist (Standard: 0).</span><span class="sxs-lookup"><span data-stu-id="af77b-130">Enable a multiline control to act like a single-line control with the ability to scroll vertically when the single-line height is greater than the window height (default: 0).</span></span> <br/>                                                                   |
| <dl> <span data-ttu-id="af77b-131"><dt>**SES \_ hidetempformat**</dt></span><span class="sxs-lookup"><span data-stu-id="af77b-131"><dt>**SES\_HIDETEMPFORMAT**</dt></span></span> </dl>         | <span data-ttu-id="af77b-132">Blenden Sie die temporäre Formatierung aus, die erstellt wird, wenn " [**itextfont. Reset**](/windows/desktop/api/Tom/nf-tom-itextfont-reset) " mit **tomapplytmp** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="af77b-132">Hide temporary formatting that is created when [**ITextFont.Reset**](/windows/desktop/api/Tom/nf-tom-itextfont-reset) is called with **tomApplyTmp**.</span></span> <span data-ttu-id="af77b-133">Beispielsweise wird eine solche Formatierung von Rechtschreibprüfungen verwendet, um einen Wellen Strich unter Umständen falsch geschriebene Wörter anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="af77b-133">For example, such formatting is used by spell checkers to display a squiggly underline under possibly misspelled words.</span></span><br/> |
| <dl> <span data-ttu-id="af77b-134"><dt>**SES \_ von \_ usemoust wParam**</dt></span><span class="sxs-lookup"><span data-stu-id="af77b-134"><dt>**SES\_EX\_USEMOUSEWPARAM**</dt></span></span> </dl>     | <span data-ttu-id="af77b-135">Verwenden Sie *wParam* , wenn Sie die [**WM- \_ mouanmove**](/windows/desktop/inputdev/wm-mousemove) -Nachricht verarbeiten und [**GetAsyncKeyState**](/windows/desktop/api/winuser/nf-winuser-getasynckeystate)nicht aufrufen.</span><span class="sxs-lookup"><span data-stu-id="af77b-135">Use *wParam* when handling the [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message and do not call [**GetAsyncKeyState**](/windows/desktop/api/winuser/nf-winuser-getasynckeystate).</span></span><br/>                                                                                              |



 

## <a name="requirements"></a><span data-ttu-id="af77b-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="af77b-136">Requirements</span></span>



| <span data-ttu-id="af77b-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="af77b-137">Requirement</span></span> | <span data-ttu-id="af77b-138">Wert</span><span class="sxs-lookup"><span data-stu-id="af77b-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="af77b-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="af77b-139">Minimum supported client</span></span><br/> | <span data-ttu-id="af77b-140">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="af77b-140">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="af77b-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="af77b-141">Minimum supported server</span></span><br/> | <span data-ttu-id="af77b-142">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="af77b-142">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="af77b-143">Header</span><span class="sxs-lookup"><span data-stu-id="af77b-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="af77b-144"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="af77b-144"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af77b-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="af77b-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af77b-146">**EM- \_ Test-ditstyleex**</span><span class="sxs-lookup"><span data-stu-id="af77b-146">**EM\_SETEDITSTYLEEX**</span></span>](em-seteditstyleex.md)
</dt> </dl>

 

