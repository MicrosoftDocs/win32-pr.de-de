---
title: CDN_INCLUDEITEM Benachrichtigungscode (Commdlg.h)
description: Wird über das Dialogfeld Öffnen oder Speichern unter gesendet, um zu bestimmen, ob im Dialogfeld ein Element in der Elementliste eines Shellordners angezeigt werden soll.
ms.assetid: 0972a78d-e058-4bac-85bd-fbd4c3885552
keywords:
- CDN_INCLUDEITEM Benachrichtigungscode (Dialogfelder)
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
ms.openlocfilehash: 2a91c61e4a7c2786e67ed28e2c62e5963762659c
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590777"
---
# <a name="cdn_includeitem-notification-code"></a><span data-ttu-id="e3e5d-104">CDN \_ INCLUDEITEM-Benachrichtigungscode</span><span class="sxs-lookup"><span data-stu-id="e3e5d-104">CDN\_INCLUDEITEM notification code</span></span>

<span data-ttu-id="e3e5d-105">\[Ab Windows Vista wurden  **die** allgemeinen Dialogfelder Öffnen und Speichern unter durch den Allgemeinen [Elementdialog ersetzt.](/windows/win32/shell/common-file-dialog)</span><span class="sxs-lookup"><span data-stu-id="e3e5d-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="e3e5d-106">Es wird empfohlen, anstelle dieser Dialogfelder aus der Common Dialog Box Library die API für den Allgemeinen Elementdialog zu verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="e3e5d-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="e3e5d-107">Wird über das **Dialogfeld Öffnen** oder Speichern **unter** gesendet, um zu bestimmen, ob im Dialogfeld ein Element in der Elementliste eines Shellordners angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e3e5d-107">Sent by an **Open** or **Save As** dialog box to determine whether the dialog box should display an item in a shell folder's item list.</span></span> <span data-ttu-id="e3e5d-108">Wenn der Benutzer einen Ordner öffnet, sendet das Dialogfeld eine **CDN \_ INCLUDEITEM-Benachrichtigung** für jedes Element im Ordner.</span><span class="sxs-lookup"><span data-stu-id="e3e5d-108">When the user opens a folder, the dialog box sends a **CDN\_INCLUDEITEM** notification for each item in the folder.</span></span> <span data-ttu-id="e3e5d-109">Das Dialogfeld sendet diese Benachrichtigung nur, wenn das **OFN \_ ENABLEINCLUDENOTIFY-Flag** beim Erstellen des Dialogfelds festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="e3e5d-109">The dialog box sends this notification only if the **OFN\_ENABLEINCLUDENOTIFY** flag was set when the dialog box was created.</span></span>

<span data-ttu-id="e3e5d-110">Ihre [*OFNHookProc-Hookprozedur*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) empfängt diese Nachricht in Form einer [**WM \_ NOTIFY-Nachricht.**](../controls/wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="e3e5d-110">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_INCLUDEITEM         (CDN_FIRST - 0x0007)
```



## <a name="parameters"></a><span data-ttu-id="e3e5d-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3e5d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3e5d-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e3e5d-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e3e5d-113">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="e3e5d-113">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e3e5d-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e3e5d-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e3e5d-115">Ein Zeiger auf eine [**OFNOTIFYEX-Struktur.**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa)</span><span class="sxs-lookup"><span data-stu-id="e3e5d-115">A pointer to an [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) structure.</span></span>

<span data-ttu-id="e3e5d-116">Die [**OFNOTIFYEX-Struktur**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) enthält eine [**NMHDR-Struktur,**](/windows/desktop/api/richedit/ns-richedit-nmhdr) deren **Code** member die **CDN \_ INCLUDEITEM-Benachrichtigungsmeldung** angibt.</span><span class="sxs-lookup"><span data-stu-id="e3e5d-116">The [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_INCLUDEITEM** notification message.</span></span>

<span data-ttu-id="e3e5d-117">Der **psf-Member** der [**OFNOTIFYEX-Struktur**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) ist ein Zeiger auf eine Schnittstelle für den Ordner, dessen Elemente aufzählt werden.</span><span class="sxs-lookup"><span data-stu-id="e3e5d-117">The **psf** member of the [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) structure is a pointer to an interface for the folder whose items are being enumerated.</span></span> <span data-ttu-id="e3e5d-118">Das **pidl-Element** ist ein Zeiger auf eine Elementbezeichnerliste, die das Element relativ zum Ordner identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e3e5d-118">The **pidl** member is a pointer to an item identifier list that identifies the item relative to the folder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3e5d-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e3e5d-119">Return value</span></span>

<span data-ttu-id="e3e5d-120">Wenn die [*HOOKprozedur OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) null zurückgibt, schließt das Dialogfeld das Element aus der Liste der Elemente aus.</span><span class="sxs-lookup"><span data-stu-id="e3e5d-120">If the [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure returns zero, the dialog box excludes the item from the list of items.</span></span>

<span data-ttu-id="e3e5d-121">Um das Element ein include zu erhalten, geben Sie einen Wert ungleich 0 (null) aus der Hookprozedur zurück.</span><span class="sxs-lookup"><span data-stu-id="e3e5d-121">To include the item, return a nonzero value from the hook procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3e5d-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e3e5d-122">Remarks</span></span>

<span data-ttu-id="e3e5d-123">Das Dialogfeld enthält immer Elemente mit den Attributen **SFGAO \_ FILESYSTEM** und **SFGAO \_ FILESYSANCESTOR,** unabhängig vom wert, der von **CDN \_ INCLUDEITEM zurückgegeben wird.**</span><span class="sxs-lookup"><span data-stu-id="e3e5d-123">The dialog box always includes items that have both the **SFGAO\_FILESYSTEM** and **SFGAO\_FILESYSANCESTOR** attributes, regardless of the value returned by **CDN\_INCLUDEITEM**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3e5d-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e3e5d-124">Requirements</span></span>



| <span data-ttu-id="e3e5d-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e3e5d-125">Requirement</span></span> | <span data-ttu-id="e3e5d-126">Wert</span><span class="sxs-lookup"><span data-stu-id="e3e5d-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3e5d-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e3e5d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e3e5d-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e3e5d-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e3e5d-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e3e5d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e3e5d-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e3e5d-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e3e5d-131">Header</span><span class="sxs-lookup"><span data-stu-id="e3e5d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3e5d-132"><dt>Commdlg.h (einschließlich Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="e3e5d-132"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3e5d-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e3e5d-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="e3e5d-134">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="e3e5d-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e3e5d-135">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="e3e5d-135">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="e3e5d-136">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="e3e5d-136">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="e3e5d-137">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="e3e5d-137">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="e3e5d-138">**OFNOTIFYEX**</span><span class="sxs-lookup"><span data-stu-id="e3e5d-138">**OFNOTIFYEX**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa)
</dt> <dt>

<span data-ttu-id="e3e5d-139">**Konzeptionellen**</span><span class="sxs-lookup"><span data-stu-id="e3e5d-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e3e5d-140">Allgemeine Dialogfeldbibliothek</span><span class="sxs-lookup"><span data-stu-id="e3e5d-140">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

