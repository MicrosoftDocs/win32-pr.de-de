---
title: CDN_TYPECHANGE Benachrichtigungscode (Commdlg.h)
description: Wird über das Dialogfeld Öffnen oder Speichern unter im Explorer-Stil gesendet, wenn der Benutzer im Kombinationsfeld Dateitypen einen neuen Dateityp auswählt.
ms.assetid: fb8324db-e435-4ef2-aac5-506a6b7adb2c
keywords:
- CDN_TYPECHANGE Benachrichtigungscode (Dialogfelder)
topic_type:
- apiref
api_name:
- CDN_TYPECHANGE
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3922dd71b70ace579fa4b5f2318776779afdfa4e
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548865"
---
# <a name="cdn_typechange-notification-code"></a><span data-ttu-id="e4bf0-104">CDN \_ TYPECHANGE-Benachrichtigungscode</span><span class="sxs-lookup"><span data-stu-id="e4bf0-104">CDN\_TYPECHANGE notification code</span></span>

<span data-ttu-id="e4bf0-105">\[Ab Windows Vista wurden  **die** allgemeinen Dialogfelder Öffnen und Speichern unter durch den Allgemeinen [Elementdialog ersetzt.](../shell/common-file-dialog.md)</span><span class="sxs-lookup"><span data-stu-id="e4bf0-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="e4bf0-106">Es wird empfohlen, anstelle dieser Dialogfelder aus der Common Dialog Box Library die API für den Allgemeinen Elementdialog zu verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="e4bf0-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="e4bf0-107">Wird über das  Dialogfeld  Öffnen oder Speichern unter im Explorer-Stil gesendet, wenn der Benutzer im Kombinationsfeld Dateitypen einen neuen Dateityp auswählt.</span><span class="sxs-lookup"><span data-stu-id="e4bf0-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the user selects a new file type from the file types combo box.</span></span>

<span data-ttu-id="e4bf0-108">Ihre [*OFNHookProc-Hookprozedur*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) empfängt diese Nachricht in Form einer [**WM \_ NOTIFY-Nachricht.**](../controls/wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="e4bf0-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_TYPECHANGE          (CDN_FIRST - 0x0006)
```



## <a name="parameters"></a><span data-ttu-id="e4bf0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e4bf0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4bf0-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e4bf0-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e4bf0-111">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="e4bf0-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e4bf0-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e4bf0-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e4bf0-113">Ein Zeiger auf eine [**OFNOTIFY-Struktur.**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)</span><span class="sxs-lookup"><span data-stu-id="e4bf0-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span>

<span data-ttu-id="e4bf0-114">Die [**OFNOTIFY-Struktur**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) enthält eine [**NMHDR-Struktur,**](/windows/win32/api/richedit/ns-richedit-nmhdr) deren **Code** member die **CDN \_ TYPECHANGE-Benachrichtigungsmeldung** angibt.</span><span class="sxs-lookup"><span data-stu-id="e4bf0-114">The [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_TYPECHANGE** notification message.</span></span>

<span data-ttu-id="e4bf0-115">Die [**OFNOTIFY-Struktur**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) enthält auch einen Zeiger auf eine [**OPENFILENAME-Struktur,**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) deren **nFilterIndex-Member den einbasierten** Index des neu ausgewählten Dateitypfilters angibt.</span><span class="sxs-lookup"><span data-stu-id="e4bf0-115">The [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure also contains a pointer to an [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure whose **nFilterIndex** member indicates the one-based index of the newly selected file type filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4bf0-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e4bf0-116">Return value</span></span>

<span data-ttu-id="e4bf0-117">Diese Meldung hat keinen Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="e4bf0-117">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4bf0-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e4bf0-118">Remarks</span></span>

<span data-ttu-id="e4bf0-119">Das System sendet diese Benachrichtigung nur, wenn das Dialogfeld mithilfe des **\_ OFN-EXPLORER-Werts erstellt** wurde.</span><span class="sxs-lookup"><span data-stu-id="e4bf0-119">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4bf0-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e4bf0-120">Requirements</span></span>



| <span data-ttu-id="e4bf0-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e4bf0-121">Requirement</span></span> | <span data-ttu-id="e4bf0-122">Wert</span><span class="sxs-lookup"><span data-stu-id="e4bf0-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4bf0-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e4bf0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e4bf0-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e4bf0-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e4bf0-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e4bf0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e4bf0-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e4bf0-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e4bf0-127">Header</span><span class="sxs-lookup"><span data-stu-id="e4bf0-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4bf0-128"><dt>Commdlg.h (einschließlich Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="e4bf0-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4bf0-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e4bf0-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="e4bf0-130">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="e4bf0-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e4bf0-131">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="e4bf0-131">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="e4bf0-132">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="e4bf0-132">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="e4bf0-133">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="e4bf0-133">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="e4bf0-134">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="e4bf0-134">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="e4bf0-135">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="e4bf0-135">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="e4bf0-136">**Konzeptionellen**</span><span class="sxs-lookup"><span data-stu-id="e4bf0-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e4bf0-137">Allgemeine Dialogfeldbibliothek</span><span class="sxs-lookup"><span data-stu-id="e4bf0-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

