---
title: CDN_SHAREVIOLATION Benachrichtigungscode (Commdlg.h)
description: Wird über das Dialogfeld Öffnen oder Speichern unter im Explorer-Stil gesendet, wenn der Benutzer auf die Schaltfläche OK klickt und für die ausgewählte Datei ein Verstoß gegen die Netzwerkfreigabe auftritt.
ms.assetid: a62ca550-0997-4379-aaaf-a5bc9414bd69
keywords:
- CDN_SHAREVIOLATION Benachrichtigungscode (Dialogfelder)
topic_type:
- apiref
api_name:
- CDN_SHAREVIOLATION
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77cd862fa1c3598a4e81a776004f26ef02290477
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548855"
---
# <a name="cdn_shareviolation-notification-code"></a><span data-ttu-id="0f802-104">CDN \_ SHAREVIOLATION-Benachrichtigungscode</span><span class="sxs-lookup"><span data-stu-id="0f802-104">CDN\_SHAREVIOLATION notification code</span></span>

<span data-ttu-id="0f802-105">\[Ab Windows Vista wurden  **die** allgemeinen Dialogfelder Öffnen und Speichern unter durch den Allgemeinen [Elementdialog ersetzt.](../shell/common-file-dialog.md)</span><span class="sxs-lookup"><span data-stu-id="0f802-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="0f802-106">Es wird empfohlen, anstelle dieser Dialogfelder aus der Common Dialog Box Library die API für den Allgemeinen Elementdialog zu verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="0f802-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="0f802-107">Wird über das  Dialogfeld  Öffnen oder Speichern unter im Explorer-Stil gesendet, wenn der Benutzer auf die Schaltfläche **OK** klickt und für die ausgewählte Datei ein Verstoß gegen die Netzwerkfreigabe auftritt.</span><span class="sxs-lookup"><span data-stu-id="0f802-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the user clicks the **OK** button and a network sharing violation occurs for the selected file.</span></span>

<span data-ttu-id="0f802-108">Ihre [*OFNHookProc-Hookprozedur*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) empfängt diese Nachricht in Form einer [**WM \_ NOTIFY-Nachricht.**](../controls/wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="0f802-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_SHAREVIOLATION      (CDN_FIRST - 0x0003)
```



## <a name="parameters"></a><span data-ttu-id="0f802-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f802-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f802-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0f802-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0f802-111">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0f802-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0f802-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0f802-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0f802-113">Ein Zeiger auf eine [**OFNOTIFY-Struktur.**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)</span><span class="sxs-lookup"><span data-stu-id="0f802-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="0f802-114">Der **pszFile-Member** dieser -Struktur ist ein Zeiger auf den Namen der Datei, die den Freigabeverstoß hatte.</span><span class="sxs-lookup"><span data-stu-id="0f802-114">The **pszFile** member of this structure is a pointer to the name of the file that had the sharing violation.</span></span> <span data-ttu-id="0f802-115">Die **OFNOTIFY-Struktur** enthält eine [**NMHDR-Struktur,**](/windows/win32/api/richedit/ns-richedit-nmhdr) deren **Code** member die **CDN \_ SHAREVIOLATION-Benachrichtigungsmeldung** angibt.</span><span class="sxs-lookup"><span data-stu-id="0f802-115">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_SHAREVIOLATION** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f802-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0f802-116">Return value</span></span>

<span data-ttu-id="0f802-117">Der Rückgabewert gibt an, wie das Dialogfeld den Freigabeverstoß behandeln soll.</span><span class="sxs-lookup"><span data-stu-id="0f802-117">The return value indicates how the dialog box should handle the sharing violation.</span></span>

<span data-ttu-id="0f802-118">Wenn die Hookprozedur 0 (null) zurückgibt, wird im Dialogfeld die Standardwarnmeldung für einen Freigabeverstoß angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0f802-118">If the hook procedure returns zero, the dialog box displays the standard warning message for a sharing violation.</span></span>

<span data-ttu-id="0f802-119">Um die Anzeige der Standardwarnmeldung zu verhindern, geben Sie einen Wert ungleich 0 (null) aus der Hookprozedur zurück, und rufen Sie die [**SetWindowLong-Funktion**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) auf, um einen der folgenden **\_ MSGRESULT-DWL-Werte** zu setzen.</span><span class="sxs-lookup"><span data-stu-id="0f802-119">To prevent the display of the standard warning message, return a nonzero value from the hook procedure and call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function to set one of the following **DWL\_MSGRESULT** values.</span></span>



| <span data-ttu-id="0f802-120">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="0f802-120">Return code/value</span></span>                                                                                                                                           | <span data-ttu-id="0f802-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0f802-121">Description</span></span>                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0f802-122"><dt>**OFN \_ SHAREFALLTHROUGH**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="0f802-122"><dt>**OFN\_SHAREFALLTHROUGH**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="0f802-123">Bewirkt, dass das Dialogfeld den Dateinamen zurück gibt, ohne den Benutzer vor dem Freigabeverstoß zu warnen.</span><span class="sxs-lookup"><span data-stu-id="0f802-123">Causes the dialog box to return the file name without warning the user about the sharing violation.</span></span><br/>  |
| <dl> <span data-ttu-id="0f802-124"><dt>**OFN \_ SHARENOWARN**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="0f802-124"><dt>**OFN\_SHARENOWARN**</dt> <dt>1</dt></span></span> </dl>      | <span data-ttu-id="0f802-125">Bewirkt, dass das Dialogfeld den Dateinamen zurückweisen kann, ohne den Benutzer vor dem Freigabeverstoß zu warnen.</span><span class="sxs-lookup"><span data-stu-id="0f802-125">Causes the dialog box to reject the file name without warning the user about the sharing violation.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="0f802-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0f802-126">Remarks</span></span>

<span data-ttu-id="0f802-127">Das System sendet diese Benachrichtigung nur, wenn das Dialogfeld mit dem **\_ OFN-EXPLORER-Wert** erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="0f802-127">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

<span data-ttu-id="0f802-128">Das System sendet diese Benachrichtigung nur, wenn der **OFN \_ SHAREAWARE-Wert** beim Erstellen des Dialogfelds nicht angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="0f802-128">The system sends this notification only if the **OFN\_SHAREAWARE** value was not specified when the dialog box was created.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f802-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0f802-129">Requirements</span></span>



| <span data-ttu-id="0f802-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0f802-130">Requirement</span></span> | <span data-ttu-id="0f802-131">Wert</span><span class="sxs-lookup"><span data-stu-id="0f802-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f802-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0f802-132">Minimum supported client</span></span><br/> | <span data-ttu-id="0f802-133">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0f802-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0f802-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0f802-134">Minimum supported server</span></span><br/> | <span data-ttu-id="0f802-135">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0f802-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0f802-136">Header</span><span class="sxs-lookup"><span data-stu-id="0f802-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f802-137"><dt>Commdlg.h (windows.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="0f802-137"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f802-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f802-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="0f802-139">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="0f802-139">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0f802-140">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="0f802-140">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="0f802-141">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="0f802-141">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="0f802-142">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="0f802-142">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="0f802-143">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="0f802-143">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="0f802-144">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="0f802-144">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[<span data-ttu-id="0f802-145">**SetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="0f802-145">**SetWindowLong**</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

<span data-ttu-id="0f802-146">**Konzeptionellen**</span><span class="sxs-lookup"><span data-stu-id="0f802-146">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0f802-147">Allgemeine Dialogfeldbibliothek</span><span class="sxs-lookup"><span data-stu-id="0f802-147">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

