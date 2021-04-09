---
title: WM_PSD_YAFULLPAGERECT Meldung (kommdlg. h)
description: Benachrichtigt die Hook-Prozedur über das Dialogfeld "Seite einrichten" (pagepainthook), dass das Dialogfeld im Begriff ist, den Rückgabe Adressbereich einer Umschlag Beispielseite zu zeichnen.
ms.assetid: 1f6aea69-a1bd-41ea-b508-44b4f5c38757
keywords:
- Dialog Felder WM_PSD_YAFULLPAGERECT Meldung
topic_type:
- apiref
api_name:
- WM_PSD_YAFULLPAGERECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb325a8d408724cd865f5f9b70cfe7369fe6ffe6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040961"
---
# <a name="wm_psd_yafullpagerect-message"></a><span data-ttu-id="86eac-104">WM- \_ PSD \_ yafullpagerierernachricht</span><span class="sxs-lookup"><span data-stu-id="86eac-104">WM\_PSD\_YAFULLPAGERECT message</span></span>

<span data-ttu-id="86eac-105">Benachrichtigt die Hook-Prozedur über das Dialogfeld " **Seite einrichten** " ( [*pagepainthook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)), dass das Dialogfeld im Begriff ist, den Rückgabe Adressbereich einer Umschlag Beispielseite zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="86eac-105">Notifies the hook procedure of a **Page Setup** dialog box, [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), that the dialog box is about to draw the return address portion of an envelope sample page.</span></span>


```C++
#define WM_USER                  0x0400
#define WM_PSD_YAFULLPAGERECT   (WM_USER+6)
```



## <a name="parameters"></a><span data-ttu-id="86eac-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="86eac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86eac-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="86eac-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="86eac-108">Ein Handle für den Gerätekontext der Beispielseite.</span><span class="sxs-lookup"><span data-stu-id="86eac-108">A handle to the device context for the sample page.</span></span>

</dd> <dt>

<span data-ttu-id="86eac-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="86eac-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="86eac-110">Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die die Koordinaten der Beispielseite in Pixel enthält.</span><span class="sxs-lookup"><span data-stu-id="86eac-110">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the coordinates, in pixels, of the sample page.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86eac-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="86eac-111">Return value</span></span>

<span data-ttu-id="86eac-112">Wenn die Hook-Prozedur **true** zurückgibt, wird das Dialogfeld den Rückgabe Adressteil einer Umschlag Beispielseite nicht gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="86eac-112">If the hook procedure returns **TRUE**, the dialog box does not draw the return address portion of an envelope sample page.</span></span>

<span data-ttu-id="86eac-113">Wenn die Hook-Prozedur **false** zurückgibt, wird das Dialogfeld den Rückgabe Adressteil einer Umschlag Beispielseite gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="86eac-113">If the hook procedure returns **FALSE**, the dialog box draws the return address portion of an envelope sample page.</span></span>

<span data-ttu-id="86eac-114">Wenn der Papiertyp kein Umschlag ist, hat der Rückgabewert keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="86eac-114">If the paper type is not an envelope, the return value has no effect.</span></span>

## <a name="remarks"></a><span data-ttu-id="86eac-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="86eac-115">Remarks</span></span>

<span data-ttu-id="86eac-116">Das Dialogfeld **Seite einrichten** enthält ein Bild einer Beispielseite, das zeigt, wie sich die Auswahl des Benutzers auf die Darstellung der gedruckten Ausgabe auswirkt.</span><span class="sxs-lookup"><span data-stu-id="86eac-116">The **Page Setup** dialog box includes an image of a sample page that shows how the user's selections affect the appearance of the printed output.</span></span> <span data-ttu-id="86eac-117">Wenn Sie die [**pagesetupdlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) -Funktion aufrufen, können Sie eine [*pagepainthook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) -Hook-Prozedur bereitstellen, um die Darstellung der Beispielseite anzupassen.</span><span class="sxs-lookup"><span data-stu-id="86eac-117">When you call the [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) function, you can provide a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure to customize the appearance of the sample page.</span></span> <span data-ttu-id="86eac-118">Wenn im Dialogfeld der Inhalt der Beispielseite gezeichnet wird, sendet das Dialogfeld eine Sequenz von Meldungen an die Hook-Prozedur.</span><span class="sxs-lookup"><span data-stu-id="86eac-118">Whenever the dialog box is about to draw the contents of the sample page, the dialog box sends a sequence of messages to the hook procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="86eac-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="86eac-119">Requirements</span></span>



| <span data-ttu-id="86eac-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="86eac-120">Requirement</span></span> | <span data-ttu-id="86eac-121">Wert</span><span class="sxs-lookup"><span data-stu-id="86eac-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86eac-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="86eac-122">Minimum supported client</span></span><br/> | <span data-ttu-id="86eac-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="86eac-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="86eac-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="86eac-124">Minimum supported server</span></span><br/> | <span data-ttu-id="86eac-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="86eac-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="86eac-126">Header</span><span class="sxs-lookup"><span data-stu-id="86eac-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="86eac-127"><dt>Kommdlg. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="86eac-127"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86eac-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="86eac-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="86eac-129">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="86eac-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="86eac-130">*Pagepainthook*</span><span class="sxs-lookup"><span data-stu-id="86eac-130">*PagePaintHook*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

<span data-ttu-id="86eac-131">[**Pagesetupdlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="86eac-131">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="86eac-132">**WM- \_ PSD \_ pagesetupdlg**</span><span class="sxs-lookup"><span data-stu-id="86eac-132">**WM\_PSD\_PAGESETUPDLG**</span></span>](wm-psd-pagesetupdlg.md)
</dt> <dt>

<span data-ttu-id="86eac-133">**Licher**</span><span class="sxs-lookup"><span data-stu-id="86eac-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="86eac-134">Allgemeine Dialog Feld Bibliothek</span><span class="sxs-lookup"><span data-stu-id="86eac-134">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

