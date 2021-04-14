---
title: WM_PSD_PAGESETUPDLG Meldung (kommdlg. h)
description: Benachrichtigt eine pagepainthook-Hook-Prozedur, dass im Dialogfeld Seite einrichten der Inhalt der Beispielseite gezeichnet wird. Die Hook-Prozedur kann diese Nachricht verwenden, um Initialisierungs Aufgaben auszuführen, die sich auf das Zeichnen des Inhalts der Beispielseite beziehen.
ms.assetid: 0d95240b-7d77-4819-8e5c-cc25cd1b30f2
keywords:
- Dialog Felder WM_PSD_PAGESETUPDLG Meldung
topic_type:
- apiref
api_name:
- WM_PSD_PAGESETUPDLG
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9706eff6d015dc31332d9f757c954081f0134b2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392188"
---
# <a name="wm_psd_pagesetupdlg-message"></a><span data-ttu-id="cc646-105">WM- \_ PSD- \_ pagesetupdlg-Nachricht</span><span class="sxs-lookup"><span data-stu-id="cc646-105">WM\_PSD\_PAGESETUPDLG message</span></span>

<span data-ttu-id="cc646-106">Benachrichtigt eine [**pagepainthook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) -Hook-Prozedur, dass im Dialogfeld **Seite einrichten** der Inhalt der Beispielseite gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="cc646-106">Notifies a [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure that the **Page Setup** dialog box is about to draw the contents of the sample page.</span></span> <span data-ttu-id="cc646-107">Die Hook-Prozedur kann diese Nachricht verwenden, um Initialisierungs Aufgaben auszuführen, die sich auf das Zeichnen des Inhalts der Beispielseite beziehen.</span><span class="sxs-lookup"><span data-stu-id="cc646-107">The hook procedure can use this message to carry out initialization tasks related to drawing the contents of the sample page.</span></span>


```C++
#define WM_USER                  0x0400
#define WM_PSD_PAGESETUPDLG     (WM_USER  )
```



## <a name="parameters"></a><span data-ttu-id="cc646-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc646-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc646-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cc646-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cc646-110">Das nieder wertige Wort gibt einen Wert an, der das Papierformat angibt.</span><span class="sxs-lookup"><span data-stu-id="cc646-110">The low-order word specifies a value that indicates the paper size.</span></span> <span data-ttu-id="cc646-111">Bei diesem Wert kann es sich um einen der **DMPAPER \_** -Werte handeln, die in der Beschreibung der Struktur aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="cc646-111">This value can be one of the **DMPAPER\_** values listed in the description of the structure.</span></span> <span data-ttu-id="cc646-112">Das höchst wertige Wort gibt die Ausrichtung des Papiers oder des Umschlags an und gibt an, ob der Drucker eine Punktmatrix oder ein HPPCL-Gerät (Hewlett Packard Printer Control Language) ist.</span><span class="sxs-lookup"><span data-stu-id="cc646-112">The high-order word specifies the orientation of the paper or envelope, and whether the printer is a dot matrix or HPPCL (Hewlett Packard Printer Control Language) device.</span></span> <span data-ttu-id="cc646-113">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="cc646-113">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="cc646-114">Wert</span><span class="sxs-lookup"><span data-stu-id="cc646-114">Value</span></span>                                                                             | <span data-ttu-id="cc646-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cc646-115">Meaning</span></span>                                            |
|-----------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="cc646-116"><dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="cc646-116"><dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="cc646-117">Papier im Querformat (Punktmatrix)</span><span class="sxs-lookup"><span data-stu-id="cc646-117">Paper in landscape mode (dot matrix)</span></span><br/>    |
| <dl> <span data-ttu-id="cc646-118"><dt>0x0003</dt></span><span class="sxs-lookup"><span data-stu-id="cc646-118"><dt>0x0003</dt></span></span> </dl> | <span data-ttu-id="cc646-119">Papier im Querformat (HPPCL)</span><span class="sxs-lookup"><span data-stu-id="cc646-119">Paper in landscape mode (HPPCL)</span></span><br/>         |
| <dl> <span data-ttu-id="cc646-120"><dt>0x0005</dt></span><span class="sxs-lookup"><span data-stu-id="cc646-120"><dt>0x0005</dt></span></span> </dl> | <span data-ttu-id="cc646-121">Papier im Hochformat (Punktmatrix)</span><span class="sxs-lookup"><span data-stu-id="cc646-121">Paper in portrait mode (dot matrix)</span></span><br/>     |
| <dl> <span data-ttu-id="cc646-122"><dt>0x0007</dt></span><span class="sxs-lookup"><span data-stu-id="cc646-122"><dt>0x0007</dt></span></span> </dl> | <span data-ttu-id="cc646-123">Papier im Hochformat (HPPCL)</span><span class="sxs-lookup"><span data-stu-id="cc646-123">Paper in portrait mode (HPPCL)</span></span><br/>          |
| <dl> <span data-ttu-id="cc646-124"><dt>0x000b</dt></span><span class="sxs-lookup"><span data-stu-id="cc646-124"><dt>0x000b</dt></span></span> </dl> | <span data-ttu-id="cc646-125">Umschlag im Querformat (HPPCL)</span><span class="sxs-lookup"><span data-stu-id="cc646-125">Envelope in landscape mode (HPPCL)</span></span><br/>      |
| <dl> <span data-ttu-id="cc646-126"><dt>0x000d</dt></span><span class="sxs-lookup"><span data-stu-id="cc646-126"><dt>0x000d</dt></span></span> </dl> | <span data-ttu-id="cc646-127">Umschlag im Hochformat (Punktmatrix)</span><span class="sxs-lookup"><span data-stu-id="cc646-127">Envelope in portrait mode (dot matrix)</span></span><br/>  |
| <dl> <span data-ttu-id="cc646-128"><dt>0x0019</dt></span><span class="sxs-lookup"><span data-stu-id="cc646-128"><dt>0x0019</dt></span></span> </dl> | <span data-ttu-id="cc646-129">Umschlag im Querformat (Punktmatrix)</span><span class="sxs-lookup"><span data-stu-id="cc646-129">Envelope in landscape mode (dot matrix)</span></span><br/> |
| <dl> <span data-ttu-id="cc646-130"><dt>0x001F</dt></span><span class="sxs-lookup"><span data-stu-id="cc646-130"><dt>0x001f</dt></span></span> </dl> | <span data-ttu-id="cc646-131">Umschlag im Hochformat (HPPCL)</span><span class="sxs-lookup"><span data-stu-id="cc646-131">Envelope in portrait mode (HPPCL)</span></span><br/>       |



 

</dd> <dt>

<span data-ttu-id="cc646-132">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cc646-132">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cc646-133">Ein Zeiger auf eine [**pagesetupdlg**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) -Struktur, die Informationen enthält, die zum Initialisieren des Dialog Felds **Seite einrichten** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cc646-133">A pointer to a [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) structure that contains information used to initialize the **Page Setup** dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc646-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cc646-134">Return value</span></span>

<span data-ttu-id="cc646-135">Wenn die Hook-Prozedur **true** zurückgibt, sendet das Dialogfeld keine weiteren Nachrichten und wird erst dann auf der Beispielseite gezeichnet, wenn das System die Beispielseite das nächste Mal neu zeichnen muss.</span><span class="sxs-lookup"><span data-stu-id="cc646-135">If the hook procedure returns **TRUE**, the dialog box sends no more messages and does not draw in the sample page until the next time the system needs to redraw the sample page.</span></span>

<span data-ttu-id="cc646-136">Wenn die Hook-Prozedur **false** zurückgibt, sendet das Dialogfeld die übrigen Nachrichten der Zeichnungs Sequenz.</span><span class="sxs-lookup"><span data-stu-id="cc646-136">If the hook procedure returns **FALSE**, the dialog box sends the remaining messages of the drawing sequence.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc646-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cc646-137">Remarks</span></span>

<span data-ttu-id="cc646-138">Das Dialogfeld **Seite einrichten** enthält ein Bild einer Beispielseite, das zeigt, wie sich die Auswahl des Benutzers auf die Darstellung der gedruckten Ausgabe auswirkt.</span><span class="sxs-lookup"><span data-stu-id="cc646-138">The **Page Setup** dialog box includes an image of a sample page that shows how the user's selections affect the appearance of the printed output.</span></span> <span data-ttu-id="cc646-139">Wenn Sie die [**pagesetupdlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) -Funktion aufrufen, können Sie eine [*pagepainthook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) -Hook-Prozedur bereitstellen, um die Darstellung der Beispielseite anzupassen.</span><span class="sxs-lookup"><span data-stu-id="cc646-139">When you call the [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) function, you can provide a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure to customize the appearance of the sample page.</span></span> <span data-ttu-id="cc646-140">Wenn im Dialogfeld der Inhalt der Beispielseite gezeichnet wird, sendet das Dialogfeld eine Sequenz von Meldungen an die Hook-Prozedur.</span><span class="sxs-lookup"><span data-stu-id="cc646-140">Whenever the dialog box is about to draw the contents of the sample page, the dialog box sends a sequence of messages to the hook procedure.</span></span>

<span data-ttu-id="cc646-141">Die ersten drei Nachrichten einer Zeichnungs Sequenz (**WM \_ PSD \_ pagesetupdlg**, [**WM \_ PSD \_ fullpagentror**](wm-psd-fullpagerect.md) [**WM \_ PSD \_ minmarginrect**](wm-psd-minmarginrect.md)) stellen Informationen bereit, die die Hook-Prozedur zum Zeichnen des Inhalts der Beispielseite verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="cc646-141">The first three messages of a drawing sequence (**WM\_PSD\_PAGESETUPDLG**, [**WM\_PSD\_FULLPAGERECT**](wm-psd-fullpagerect.md), or [**WM\_PSD\_MINMARGINRECT**](wm-psd-minmarginrect.md)) provide information that the hook procedure can use to draw the contents of the sample page.</span></span> <span data-ttu-id="cc646-142">Die übrigen Nachrichten [**(WM \_ PSD \_ marginrect**](wm-psd-marginrect.md), [**WM \_ PSD \_ greektextrect**](wm-psd-greektextrect.md), [**WM \_ PSD \_ envstamprect**](wm-psd-envstamprect.md), [**WM \_ PSD \_ yafullpagtory**](wm-psd-yafullpagerect.md)) benachrichtigen die Hook-Prozedur, dass im Dialogfeld ein bestimmter Teil der Beispielseite gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="cc646-142">The remaining messages ([**WM\_PSD\_MARGINRECT**](wm-psd-marginrect.md), [**WM\_PSD\_GREEKTEXTRECT**](wm-psd-greektextrect.md), [**WM\_PSD\_ENVSTAMPRECT**](wm-psd-envstamprect.md), [**WM\_PSD\_YAFULLPAGERECT**](wm-psd-yafullpagerect.md)) notify the hook procedure that the dialog box is about to draw a specific portion of the sample page.</span></span> <span data-ttu-id="cc646-143">Dadurch kann die Hook-Prozedur Teile der Beispielseite selektiv zeichnen.</span><span class="sxs-lookup"><span data-stu-id="cc646-143">This allows the hook procedure to selectively draw portions of the sample page.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc646-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cc646-144">Requirements</span></span>



| <span data-ttu-id="cc646-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc646-145">Requirement</span></span> | <span data-ttu-id="cc646-146">Wert</span><span class="sxs-lookup"><span data-stu-id="cc646-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc646-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cc646-147">Minimum supported client</span></span><br/> | <span data-ttu-id="cc646-148">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cc646-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="cc646-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cc646-149">Minimum supported server</span></span><br/> | <span data-ttu-id="cc646-150">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cc646-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cc646-151">Header</span><span class="sxs-lookup"><span data-stu-id="cc646-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc646-152"><dt>Kommdlg. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cc646-152"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc646-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cc646-153">See also</span></span>

<dl> <dt>

<span data-ttu-id="cc646-154">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="cc646-154">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cc646-155">*Pagepainthook*</span><span class="sxs-lookup"><span data-stu-id="cc646-155">*PagePaintHook*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

<span data-ttu-id="cc646-156">[**Pagesetupdlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cc646-156">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="cc646-157">**Pagesetupdlg**</span><span class="sxs-lookup"><span data-stu-id="cc646-157">**PAGESETUPDLG**</span></span>](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)
</dt> <dt>

[<span data-ttu-id="cc646-158">**WM- \_ PSD- \_ präct**</span><span class="sxs-lookup"><span data-stu-id="cc646-158">**WM\_PSD\_ENVSTAMPRECT**</span></span>](wm-psd-envstamprect.md)
</dt> <dt>

[<span data-ttu-id="cc646-159">**WM- \_ PSD \_ fullpagerup**</span><span class="sxs-lookup"><span data-stu-id="cc646-159">**WM\_PSD\_FULLPAGERECT**</span></span>](wm-psd-fullpagerect.md)
</dt> <dt>

[<span data-ttu-id="cc646-160">**WM- \_ PSD \_ greektextrect**</span><span class="sxs-lookup"><span data-stu-id="cc646-160">**WM\_PSD\_GREEKTEXTRECT**</span></span>](wm-psd-greektextrect.md)
</dt> <dt>

[<span data-ttu-id="cc646-161">**WM \_ PSD \_ marginrect**</span><span class="sxs-lookup"><span data-stu-id="cc646-161">**WM\_PSD\_MARGINRECT**</span></span>](wm-psd-marginrect.md)
</dt> <dt>

[<span data-ttu-id="cc646-162">**WM- \_ PSD \_ minmarginrect**</span><span class="sxs-lookup"><span data-stu-id="cc646-162">**WM\_PSD\_MINMARGINRECT**</span></span>](wm-psd-minmarginrect.md)
</dt> <dt>

[<span data-ttu-id="cc646-163">**WM- \_ PSD \_ yafullpagtory**</span><span class="sxs-lookup"><span data-stu-id="cc646-163">**WM\_PSD\_YAFULLPAGERECT**</span></span>](wm-psd-yafullpagerect.md)
</dt> <dt>

<span data-ttu-id="cc646-164">**Licher**</span><span class="sxs-lookup"><span data-stu-id="cc646-164">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="cc646-165">Allgemeine Dialog Feld Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cc646-165">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

