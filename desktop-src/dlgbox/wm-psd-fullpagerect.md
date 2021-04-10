---
title: WM_PSD_FULLPAGERECT Meldung (kommdlg. h)
description: Benachrichtigt eine pagepainthook-Hook-Prozedur über die Koordinaten des Sample Page-Rechtecks im Dialogfeld Seite einrichten. Das Dialogfeld sendet diese Meldung, wenn der Inhalt der Beispielseite gezeichnet wird.
ms.assetid: 88ca1d60-3335-480a-b874-c6f248a3c23a
keywords:
- Dialog Felder WM_PSD_FULLPAGERECT Meldung
topic_type:
- apiref
api_name:
- WM_PSD_FULLPAGERECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b5265144822ba1f46c470b71169e0b27f2e1c75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956843"
---
# <a name="wm_psd_fullpagerect-message"></a><span data-ttu-id="ebe3c-105">WM- \_ PSD- \_ fullpagerernachricht</span><span class="sxs-lookup"><span data-stu-id="ebe3c-105">WM\_PSD\_FULLPAGERECT message</span></span>

<span data-ttu-id="ebe3c-106">Benachrichtigt eine [*pagepainthook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) -Hook-Prozedur über die Koordinaten des Sample Page-Rechtecks im Dialogfeld **Seite einrichten** .</span><span class="sxs-lookup"><span data-stu-id="ebe3c-106">Notifies a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure of the coordinates of the sample page rectangle in the **Page Setup** dialog box.</span></span> <span data-ttu-id="ebe3c-107">Das Dialogfeld sendet diese Meldung, wenn der Inhalt der Beispielseite gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="ebe3c-107">The dialog box sends this message when it is about to draw the contents of the sample page.</span></span>


```C++
#define WM_USER                  0x0400
#define WM_PSD_FULLPAGERECT     (WM_USER+1)
```



## <a name="parameters"></a><span data-ttu-id="ebe3c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ebe3c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebe3c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ebe3c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ebe3c-110">Ein Handle für den Gerätekontext der Beispielseite.</span><span class="sxs-lookup"><span data-stu-id="ebe3c-110">A handle to the device context for the sample page.</span></span>

</dd> <dt>

<span data-ttu-id="ebe3c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ebe3c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ebe3c-112">Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die die Koordinaten der Beispielseite in Pixel enthält.</span><span class="sxs-lookup"><span data-stu-id="ebe3c-112">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the coordinates, in pixels, of the sample page.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebe3c-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ebe3c-113">Return value</span></span>

<span data-ttu-id="ebe3c-114">Wenn die Hook-Prozedur **true** zurückgibt, sendet das Dialogfeld keine weiteren Nachrichten und wird erst dann auf der Beispielseite gezeichnet, wenn das System die Beispielseite das nächste Mal neu zeichnen muss.</span><span class="sxs-lookup"><span data-stu-id="ebe3c-114">If the hook procedure returns **TRUE**, the dialog box sends no more messages and does not draw in the sample page until the next time the system needs to redraw the sample page.</span></span>

<span data-ttu-id="ebe3c-115">Wenn die Hook-Prozedur **false** zurückgibt, sendet das Dialogfeld die übrigen Nachrichten der Zeichnungs Sequenz.</span><span class="sxs-lookup"><span data-stu-id="ebe3c-115">If the hook procedure returns **FALSE**, the dialog box sends the remaining messages of the drawing sequence.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebe3c-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ebe3c-116">Remarks</span></span>

<span data-ttu-id="ebe3c-117">Das Dialogfeld **Seite einrichten** enthält ein Bild einer Beispielseite, das zeigt, wie sich die Auswahl des Benutzers auf die Darstellung der gedruckten Ausgabe auswirkt.</span><span class="sxs-lookup"><span data-stu-id="ebe3c-117">The **Page Setup** dialog box includes an image of a sample page that shows how the user's selections affect the appearance of the printed output.</span></span> <span data-ttu-id="ebe3c-118">Wenn Sie die [**pagesetupdlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) -Funktion aufrufen, können Sie eine [*pagepainthook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) -Hook-Prozedur bereitstellen, um die Darstellung der Beispielseite anzupassen.</span><span class="sxs-lookup"><span data-stu-id="ebe3c-118">When you call the [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) function, you can provide a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure to customize the appearance of the sample page.</span></span> <span data-ttu-id="ebe3c-119">Wenn im Dialogfeld der Inhalt der Beispielseite gezeichnet wird, sendet das Dialogfeld eine Sequenz von Meldungen an die Hook-Prozedur.</span><span class="sxs-lookup"><span data-stu-id="ebe3c-119">Whenever the dialog box is about to draw the contents of the sample page, the dialog box sends a sequence of messages to the hook procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebe3c-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ebe3c-120">Requirements</span></span>



| <span data-ttu-id="ebe3c-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ebe3c-121">Requirement</span></span> | <span data-ttu-id="ebe3c-122">Wert</span><span class="sxs-lookup"><span data-stu-id="ebe3c-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebe3c-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ebe3c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ebe3c-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ebe3c-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ebe3c-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ebe3c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ebe3c-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ebe3c-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ebe3c-127">Header</span><span class="sxs-lookup"><span data-stu-id="ebe3c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebe3c-128"><dt>Kommdlg. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ebe3c-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebe3c-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ebe3c-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="ebe3c-130">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="ebe3c-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ebe3c-131">*Pagepainthook*</span><span class="sxs-lookup"><span data-stu-id="ebe3c-131">*PagePaintHook*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

<span data-ttu-id="ebe3c-132">[**Pagesetupdlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ebe3c-132">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ebe3c-133">**WM- \_ PSD \_ pagesetupdlg**</span><span class="sxs-lookup"><span data-stu-id="ebe3c-133">**WM\_PSD\_PAGESETUPDLG**</span></span>](wm-psd-pagesetupdlg.md)
</dt> <dt>

<span data-ttu-id="ebe3c-134">**Licher**</span><span class="sxs-lookup"><span data-stu-id="ebe3c-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ebe3c-135">Allgemeine Dialog Feld Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ebe3c-135">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

