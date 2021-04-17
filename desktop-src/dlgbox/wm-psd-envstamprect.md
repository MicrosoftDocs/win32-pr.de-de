---
title: WM_PSD_ENVSTAMPRECT Meldung (kommdlg. h)
description: Benachrichtigt die Hook-Prozedur über das Dialogfeld "Seite einrichten" (pagepainthook), dass das Dialogfeld im Begriff ist, das Umschlag Stempel Rechteck der Beispielseite zu zeichnen.
ms.assetid: f193baa0-a084-416e-90c9-9c838758a3d3
keywords:
- Dialog Felder WM_PSD_ENVSTAMPRECT Meldung
topic_type:
- apiref
api_name:
- WM_PSD_ENVSTAMPRECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf13485ab75f51298ef273c7e02ea0253e4244d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477970"
---
# <a name="wm_psd_envstamprect-message"></a><span data-ttu-id="0339a-104">WM- \_ PSD- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="0339a-104">WM\_PSD\_ENVSTAMPRECT message</span></span>

<span data-ttu-id="0339a-105">Benachrichtigt die Hook-Prozedur über das Dialogfeld " **Seite einrichten** " ( [*pagepainthook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)), dass das Dialogfeld im Begriff ist, das Umschlag Stempel Rechteck der Beispielseite zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="0339a-105">Notifies the hook procedure of a **Page Setup** dialog box, [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), that the dialog box is about to draw the envelope-stamp rectangle of the sample page.</span></span>


```C++
#define WM_USER                  0x0400
#define WM_PSD_ENVSTAMPRECT     (WM_USER+5)
```



## <a name="parameters"></a><span data-ttu-id="0339a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0339a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0339a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0339a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0339a-108">Ein Handle für den Gerätekontext der Beispielseite.</span><span class="sxs-lookup"><span data-stu-id="0339a-108">A handle to the device context for the sample page.</span></span>

</dd> <dt>

<span data-ttu-id="0339a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0339a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0339a-110">Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die die Koordinaten des Umschlag Stempel Rechtecks in Pixel enthält.</span><span class="sxs-lookup"><span data-stu-id="0339a-110">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the coordinates, in pixels, of the envelope-stamp rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0339a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0339a-111">Return value</span></span>

<span data-ttu-id="0339a-112">Wenn die Hook-Prozedur **true** zurückgibt, wird der Teil des Umschlag Stempels der Beispielseite nicht im Dialogfeld gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="0339a-112">If the hook procedure returns **TRUE**, the dialog box does not draw the envelope-stamp portion of the sample page.</span></span>

<span data-ttu-id="0339a-113">Wenn die Hook-Prozedur **false** zurückgibt, wird das Dialogfeld den Umschlag Stempel Bereich der Beispielseite gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="0339a-113">If the hook procedure returns **FALSE**, the dialog box draws the envelope-stamp portion of the sample page.</span></span>

## <a name="remarks"></a><span data-ttu-id="0339a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0339a-114">Remarks</span></span>

<span data-ttu-id="0339a-115">Das Dialogfeld **Seite einrichten** enthält ein Bild einer Beispielseite, das zeigt, wie sich die Auswahl des Benutzers auf die Darstellung der gedruckten Ausgabe auswirkt.</span><span class="sxs-lookup"><span data-stu-id="0339a-115">The **Page Setup** dialog box includes an image of a sample page that shows how the user's selections affect the appearance of the printed output.</span></span> <span data-ttu-id="0339a-116">Wenn Sie die [**pagesetupdlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) -Funktion aufrufen, können Sie eine [*pagepainthook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) -Hook-Prozedur bereitstellen, um die Darstellung der Beispielseite anzupassen.</span><span class="sxs-lookup"><span data-stu-id="0339a-116">When you call the [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) function, you can provide a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure to customize the appearance of the sample page.</span></span> <span data-ttu-id="0339a-117">Wenn im Dialogfeld der Inhalt der Beispielseite gezeichnet wird, sendet das Dialogfeld eine Sequenz von Meldungen an die Hook-Prozedur.</span><span class="sxs-lookup"><span data-stu-id="0339a-117">Whenever the dialog box is about to draw the contents of the sample page, the dialog box sends a sequence of messages to the hook procedure.</span></span>

<span data-ttu-id="0339a-118">Eine Hook-Prozedur empfängt diese Nachricht nur, wenn es sich bei dem ausgewählten Papiertyp um einen Umschlag handelt.</span><span class="sxs-lookup"><span data-stu-id="0339a-118">A hook procedure receives this message only if the selected paper type is an envelope.</span></span>

## <a name="requirements"></a><span data-ttu-id="0339a-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0339a-119">Requirements</span></span>



| <span data-ttu-id="0339a-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0339a-120">Requirement</span></span> | <span data-ttu-id="0339a-121">Wert</span><span class="sxs-lookup"><span data-stu-id="0339a-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0339a-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0339a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0339a-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0339a-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0339a-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0339a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0339a-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0339a-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0339a-126">Header</span><span class="sxs-lookup"><span data-stu-id="0339a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0339a-127"><dt>Kommdlg. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0339a-127"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0339a-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0339a-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="0339a-129">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="0339a-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0339a-130">*Pagepainthook*</span><span class="sxs-lookup"><span data-stu-id="0339a-130">*PagePaintHook*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

<span data-ttu-id="0339a-131">[**Pagesetupdlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0339a-131">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0339a-132">**WM- \_ PSD \_ pagesetupdlg**</span><span class="sxs-lookup"><span data-stu-id="0339a-132">**WM\_PSD\_PAGESETUPDLG**</span></span>](wm-psd-pagesetupdlg.md)
</dt> <dt>

<span data-ttu-id="0339a-133">**Licher**</span><span class="sxs-lookup"><span data-stu-id="0339a-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0339a-134">Allgemeine Dialog Feld Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0339a-134">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

