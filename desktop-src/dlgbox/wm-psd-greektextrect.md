---
title: WM_PSD_GREEKTEXTRECT Meldung (kommdlg. h)
description: Benachrichtigt die Hook-Prozedur über das Dialogfeld "Seite einrichten" (pagepainthook), dass das Dialogfeld im Begriff ist, griechischen Text innerhalb des Rand Rechtecks der Beispielseite zu zeichnen.
ms.assetid: ad0a200d-5626-4768-b3bd-73d4e3f0d548
keywords:
- Dialog Felder WM_PSD_GREEKTEXTRECT Meldung
topic_type:
- apiref
api_name:
- WM_PSD_GREEKTEXTRECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd0853720bea8cadc8df40d8fa649f644fd00694
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040811"
---
# <a name="wm_psd_greektextrect-message"></a><span data-ttu-id="afc0c-104">WM- \_ PSD- \_ Meldung "greektextrect"</span><span class="sxs-lookup"><span data-stu-id="afc0c-104">WM\_PSD\_GREEKTEXTRECT message</span></span>

<span data-ttu-id="afc0c-105">Benachrichtigt die Hook-Prozedur über das Dialogfeld " **Seite einrichten** " ( [*pagepainthook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)), dass das Dialogfeld im Begriff ist, griechischen Text innerhalb des Rand Rechtecks der Beispielseite zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="afc0c-105">Notifies the hook procedure of a **Page Setup** dialog box, [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), that the dialog box is about to draw Greek text inside the margin rectangle of the sample page.</span></span>


```C++
#define WM_USER                  0x0400
#define WM_PSD_GREEKTEXTRECT    (WM_USER+4)
```



## <a name="parameters"></a><span data-ttu-id="afc0c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="afc0c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afc0c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="afc0c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="afc0c-108">Ein Handle für den Gerätekontext der Beispielseite.</span><span class="sxs-lookup"><span data-stu-id="afc0c-108">A handle to the device context for the sample page.</span></span>

</dd> <dt>

<span data-ttu-id="afc0c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="afc0c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="afc0c-110">Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die die Koordinaten des griechischen Text Rechtecks in Pixel enthält.</span><span class="sxs-lookup"><span data-stu-id="afc0c-110">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the coordinates, in pixels, of the Greek text rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afc0c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="afc0c-111">Return value</span></span>

<span data-ttu-id="afc0c-112">Wenn die Hook-Prozedur **true** zurückgibt, wird der griechische Textteil der Beispielseite nicht im Dialogfeld gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="afc0c-112">If the hook procedure returns **TRUE**, the dialog box does not draw the Greek text portion of the sample page.</span></span>

<span data-ttu-id="afc0c-113">Wenn die Hook-Prozedur **false** zurückgibt, zeichnet das Dialogfeld den griechischen Textteil der Beispielseite.</span><span class="sxs-lookup"><span data-stu-id="afc0c-113">If the hook procedure returns **FALSE**, the dialog box draws the Greek text portion of the sample page.</span></span>

## <a name="remarks"></a><span data-ttu-id="afc0c-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="afc0c-114">Remarks</span></span>

<span data-ttu-id="afc0c-115">Das Dialogfeld **Seite einrichten** enthält ein Bild einer Beispielseite, das zeigt, wie sich die Auswahl des Benutzers auf die Darstellung der gedruckten Ausgabe auswirkt.</span><span class="sxs-lookup"><span data-stu-id="afc0c-115">The **Page Setup** dialog box includes an image of a sample page that shows how the user's selections affect the appearance of the printed output.</span></span> <span data-ttu-id="afc0c-116">Wenn Sie die [**pagesetupdlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) -Funktion aufrufen, können Sie eine [*pagepainthook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) -Hook-Prozedur bereitstellen, um die Darstellung der Beispielseite anzupassen.</span><span class="sxs-lookup"><span data-stu-id="afc0c-116">When you call the [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) function, you can provide a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure to customize the appearance of the sample page.</span></span> <span data-ttu-id="afc0c-117">Wenn im Dialogfeld der Inhalt der Beispielseite gezeichnet wird, sendet das Dialogfeld eine Sequenz von Meldungen an die Hook-Prozedur.</span><span class="sxs-lookup"><span data-stu-id="afc0c-117">Whenever the dialog box is about to draw the contents of the sample page, the dialog box sends a sequence of messages to the hook procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="afc0c-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="afc0c-118">Requirements</span></span>



| <span data-ttu-id="afc0c-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="afc0c-119">Requirement</span></span> | <span data-ttu-id="afc0c-120">Wert</span><span class="sxs-lookup"><span data-stu-id="afc0c-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afc0c-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="afc0c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="afc0c-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="afc0c-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="afc0c-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="afc0c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="afc0c-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="afc0c-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="afc0c-125">Header</span><span class="sxs-lookup"><span data-stu-id="afc0c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="afc0c-126"><dt>Kommdlg. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="afc0c-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afc0c-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="afc0c-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="afc0c-128">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="afc0c-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="afc0c-129">*Pagepainthook*</span><span class="sxs-lookup"><span data-stu-id="afc0c-129">*PagePaintHook*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

<span data-ttu-id="afc0c-130">[**Pagesetupdlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="afc0c-130">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="afc0c-131">**WM- \_ PSD \_ pagesetupdlg**</span><span class="sxs-lookup"><span data-stu-id="afc0c-131">**WM\_PSD\_PAGESETUPDLG**</span></span>](wm-psd-pagesetupdlg.md)
</dt> <dt>

<span data-ttu-id="afc0c-132">**Licher**</span><span class="sxs-lookup"><span data-stu-id="afc0c-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="afc0c-133">Allgemeine Dialog Feld Bibliothek</span><span class="sxs-lookup"><span data-stu-id="afc0c-133">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

