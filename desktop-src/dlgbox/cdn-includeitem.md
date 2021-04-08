---
title: CDN_INCLUDEITEM Benachrichtigungs Code (kommdlg. h)
description: Wird von einem Dialogfeld "Öffnen" oder "Speichern unter" gesendet, um zu bestimmen, ob das Dialogfeld ein Element in der Elementliste eines shellordners anzeigen soll.
ms.assetid: 0972a78d-e058-4bac-85bd-fbd4c3885552
keywords:
- Dialog Felder für CDN_INCLUDEITEM Benachrichtigungs Code
topic_type:
- apiref
api_name:
- CDN_INCLUDEITEM
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67cbe830c644657425eb087dd64884da17a9a0c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742848"
---
# <a name="cdn_includeitem-notification-code"></a><span data-ttu-id="8e684-104">CDN \_ includeitem-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="8e684-104">CDN\_INCLUDEITEM notification code</span></span>

<span data-ttu-id="8e684-105">\[Ab Windows Vista wurden die Dialogfelder " **Öffnen** " und " **Speichern** unter" im allgemeinen [Element](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85))ersetzt.</span><span class="sxs-lookup"><span data-stu-id="8e684-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="8e684-106">Es wird empfohlen, dass Sie die allgemeine Element Dialogfeld-API anstelle dieser Dialogfelder aus der allgemeinen Dialogfeld Bibliothek verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="8e684-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="8e684-107">Wird von einem Dialogfeld " **Öffnen** " oder " **Speichern** unter" gesendet, um zu bestimmen, ob das Dialogfeld ein Element in der Elementliste eines shellordners anzeigen soll.</span><span class="sxs-lookup"><span data-stu-id="8e684-107">Sent by an **Open** or **Save As** dialog box to determine whether the dialog box should display an item in a shell folder's item list.</span></span> <span data-ttu-id="8e684-108">Wenn der Benutzer einen Ordner öffnet, sendet das Dialogfeld für jedes Element im Ordner eine **CDN- \_ includeitem** -Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="8e684-108">When the user opens a folder, the dialog box sends a **CDN\_INCLUDEITEM** notification for each item in the folder.</span></span> <span data-ttu-id="8e684-109">Das Dialogfeld sendet diese Benachrichtigung nur dann, wenn das **ofn \_ enableinclubezeichtifisflag** beim Erstellen des Dialog Felds festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="8e684-109">The dialog box sends this notification only if the **OFN\_ENABLEINCLUDENOTIFY** flag was set when the dialog box was created.</span></span>

<span data-ttu-id="8e684-110">Die [*ofnhuokproc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) -Hook-Prozedur empfängt diese Nachricht in Form einer [**WM- \_ Benachrichtigungs**](../controls/wm-notify.md) Meldung.</span><span class="sxs-lookup"><span data-stu-id="8e684-110">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_INCLUDEITEM         (CDN_FIRST - 0x0007)
```



## <a name="parameters"></a><span data-ttu-id="8e684-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e684-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e684-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8e684-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8e684-113">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="8e684-113">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8e684-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8e684-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8e684-115">Ein Zeiger auf eine [**ofnotifyex**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="8e684-115">A pointer to an [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) structure.</span></span>

<span data-ttu-id="8e684-116">Die [**ofnotifyex**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) -Struktur enthält eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, deren **Codemember** die **CDN \_ includeitem** -Benachrichtigungs Meldung angibt.</span><span class="sxs-lookup"><span data-stu-id="8e684-116">The [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_INCLUDEITEM** notification message.</span></span>

<span data-ttu-id="8e684-117">Der **PSF** -Member der [**ofnotifyex**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) -Struktur ist ein Zeiger auf eine Schnittstelle für den Ordner, dessen Elemente aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="8e684-117">The **psf** member of the [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) structure is a pointer to an interface for the folder whose items are being enumerated.</span></span> <span data-ttu-id="8e684-118">Der **PIDL** -Member ist ein Zeiger auf eine Element Bezeichner-Liste, die das Element relativ zum Ordner identifiziert.</span><span class="sxs-lookup"><span data-stu-id="8e684-118">The **pidl** member is a pointer to an item identifier list that identifies the item relative to the folder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e684-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8e684-119">Return value</span></span>

<span data-ttu-id="8e684-120">Wenn die [*ofnhuokproc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) -Hook-Prozedur NULL zurückgibt, schließt das Dialogfeld das Element aus der Liste der Elemente aus.</span><span class="sxs-lookup"><span data-stu-id="8e684-120">If the [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure returns zero, the dialog box excludes the item from the list of items.</span></span>

<span data-ttu-id="8e684-121">Um das Element einzuschließen, geben Sie einen Wert ungleich 0 (null) von der Hook-Prozedur zurück.</span><span class="sxs-lookup"><span data-stu-id="8e684-121">To include the item, return a nonzero value from the hook procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e684-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8e684-122">Remarks</span></span>

<span data-ttu-id="8e684-123">Das Dialogfeld enthält immer Elemente, die sowohl das **sfgao- \_ Dateisystem** als auch das **sfgao \_ filesysancestor** -Attribut aufweisen, unabhängig von dem Wert, der von **CDN \_ includeitem** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8e684-123">The dialog box always includes items that have both the **SFGAO\_FILESYSTEM** and **SFGAO\_FILESYSANCESTOR** attributes, regardless of the value returned by **CDN\_INCLUDEITEM**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e684-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8e684-124">Requirements</span></span>



| <span data-ttu-id="8e684-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8e684-125">Requirement</span></span> | <span data-ttu-id="8e684-126">Wert</span><span class="sxs-lookup"><span data-stu-id="8e684-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e684-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8e684-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8e684-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8e684-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="8e684-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8e684-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8e684-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8e684-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8e684-131">Header</span><span class="sxs-lookup"><span data-stu-id="8e684-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e684-132"><dt>Kommdlg. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8e684-132"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e684-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8e684-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="8e684-134">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="8e684-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8e684-135">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="8e684-135">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="8e684-136">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="8e684-136">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="8e684-137">*Ofnhuokproc*</span><span class="sxs-lookup"><span data-stu-id="8e684-137">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="8e684-138">**Ofnotifyex**</span><span class="sxs-lookup"><span data-stu-id="8e684-138">**OFNOTIFYEX**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa)
</dt> <dt>

<span data-ttu-id="8e684-139">**Licher**</span><span class="sxs-lookup"><span data-stu-id="8e684-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8e684-140">Allgemeine Dialog Feld Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8e684-140">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

