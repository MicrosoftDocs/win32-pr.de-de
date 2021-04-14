---
title: WM_PSD_MINMARGINRECT Meldung (kommdlg. h)
description: Benachrichtigt eine pagepainthook-Hook-Prozedur über die Koordinaten des Rand Rechtecks auf der Beispielseite. Diese Meldung wird im Dialogfeld Seite einrichten gesendet, wenn der Inhalt der Beispielseite gezeichnet wird.
ms.assetid: 14977b52-7a6f-4c55-956a-716398a71613
keywords:
- Dialog Felder WM_PSD_MINMARGINRECT Meldung
topic_type:
- apiref
api_name:
- WM_PSD_MINMARGINRECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22ec7271026ba7557fcbe3fe17cd890d62eadbca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518338"
---
# <a name="wm_psd_minmarginrect-message"></a><span data-ttu-id="a50da-105">WM- \_ PSD- \_ minmarginrect-Meldung</span><span class="sxs-lookup"><span data-stu-id="a50da-105">WM\_PSD\_MINMARGINRECT message</span></span>

<span data-ttu-id="a50da-106">Benachrichtigt eine [*pagepainthook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) -Hook-Prozedur über die Koordinaten des Rand Rechtecks auf der Beispielseite.</span><span class="sxs-lookup"><span data-stu-id="a50da-106">Notifies a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure of the coordinates of the margin rectangle in the sample page.</span></span> <span data-ttu-id="a50da-107">Diese Meldung wird im Dialogfeld **Seite einrichten** gesendet, wenn der Inhalt der Beispielseite gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="a50da-107">A **Page Setup** dialog box sends this message when it is about to draw the contents of the sample page.</span></span>


```C++
#define WM_USER                  0x0400
#define WM_PSD_MINMARGINRECT    (WM_USER+2)
```



## <a name="parameters"></a><span data-ttu-id="a50da-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a50da-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a50da-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a50da-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a50da-110">Ein Handle für den Gerätekontext der Beispielseite.</span><span class="sxs-lookup"><span data-stu-id="a50da-110">A handle to the device context for the sample page.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a50da-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a50da-112">Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die die Koordinaten des minimalen Rand Rechtecks in Pixel enthält.</span><span class="sxs-lookup"><span data-stu-id="a50da-112">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the coordinates, in pixels, of the minimum margin rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a50da-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a50da-113">Return value</span></span>

<span data-ttu-id="a50da-114">Wenn die Hook-Prozedur **true** zurückgibt, sendet das Dialogfeld keine weiteren Nachrichten und wird erst dann auf der Beispielseite gezeichnet, wenn das System die Beispielseite das nächste Mal neu zeichnen muss.</span><span class="sxs-lookup"><span data-stu-id="a50da-114">If the hook procedure returns **TRUE**, the dialog box sends no more messages and does not draw in the sample page until the next time the system needs to redraw the sample page.</span></span>

<span data-ttu-id="a50da-115">Wenn die Hook-Prozedur **false** zurückgibt, sendet das Dialogfeld die übrigen Nachrichten der Zeichnungs Sequenz.</span><span class="sxs-lookup"><span data-stu-id="a50da-115">If the hook procedure returns **FALSE**, the dialog box sends the remaining messages of the drawing sequence.</span></span>

## <a name="remarks"></a><span data-ttu-id="a50da-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a50da-116">Remarks</span></span>

<span data-ttu-id="a50da-117">Das Dialogfeld **Seite einrichten** enthält ein Bild einer Beispielseite, das zeigt, wie sich die Auswahl des Benutzers auf die Darstellung der gedruckten Ausgabe auswirkt.</span><span class="sxs-lookup"><span data-stu-id="a50da-117">The **Page Setup** dialog box includes an image of a sample page that shows how the user's selections affect the appearance of the printed output.</span></span> <span data-ttu-id="a50da-118">Wenn Sie die [**pagesetupdlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) -Funktion aufrufen, können Sie eine [*pagepainthook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) -Hook-Prozedur bereitstellen, um die Darstellung der Beispielseite anzupassen.</span><span class="sxs-lookup"><span data-stu-id="a50da-118">When you call the [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) function, you can provide a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure to customize the appearance of the sample page.</span></span> <span data-ttu-id="a50da-119">Wenn im Dialogfeld der Inhalt der Beispielseite gezeichnet wird, sendet das Dialogfeld eine Sequenz von Meldungen an die Hook-Prozedur.</span><span class="sxs-lookup"><span data-stu-id="a50da-119">Whenever the dialog box is about to draw the contents of the sample page, the dialog box sends a sequence of messages to the hook procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="a50da-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a50da-120">Requirements</span></span>



| <span data-ttu-id="a50da-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a50da-121">Requirement</span></span> | <span data-ttu-id="a50da-122">Wert</span><span class="sxs-lookup"><span data-stu-id="a50da-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a50da-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a50da-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a50da-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a50da-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a50da-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a50da-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a50da-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a50da-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a50da-127">Header</span><span class="sxs-lookup"><span data-stu-id="a50da-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a50da-128"><dt>Kommdlg. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a50da-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a50da-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a50da-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="a50da-130">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="a50da-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a50da-131">*Pagepainthook*</span><span class="sxs-lookup"><span data-stu-id="a50da-131">*PagePaintHook*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

<span data-ttu-id="a50da-132">[**Pagesetupdlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a50da-132">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="a50da-133">**WM- \_ PSD \_ pagesetupdlg**</span><span class="sxs-lookup"><span data-stu-id="a50da-133">**WM\_PSD\_PAGESETUPDLG**</span></span>](wm-psd-pagesetupdlg.md)
</dt> <dt>

<span data-ttu-id="a50da-134">**Licher**</span><span class="sxs-lookup"><span data-stu-id="a50da-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a50da-135">Allgemeine Dialog Feld Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a50da-135">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

