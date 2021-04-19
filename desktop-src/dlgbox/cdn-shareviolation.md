---
title: CDN_SHAREVIOLATION Benachrichtigungs Code (kommdlg. h)
description: Wird von einem Explorer-Dialogfeld "Öffnen" oder "Speichern unter" gesendet, wenn der Benutzer auf die Schaltfläche "OK" klickt und eine Netzwerkfreigabe Verletzung für die ausgewählte Datei auftritt.
ms.assetid: a62ca550-0997-4379-aaaf-a5bc9414bd69
keywords:
- Dialog Felder für CDN_SHAREVIOLATION Benachrichtigungs Code
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
ms.openlocfilehash: acfa3a91e9c84f15984285f99d071fcde24a4d66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339967"
---
# <a name="cdn_shareviolation-notification-code"></a><span data-ttu-id="7456c-104">CDN- \_ shareverletzungs-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="7456c-104">CDN\_SHAREVIOLATION notification code</span></span>

<span data-ttu-id="7456c-105">\[Ab Windows Vista wurden die Dialogfelder " **Öffnen** " und " **Speichern** unter" im allgemeinen [Element](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85))ersetzt.</span><span class="sxs-lookup"><span data-stu-id="7456c-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="7456c-106">Es wird empfohlen, dass Sie die allgemeine Element Dialogfeld-API anstelle dieser Dialogfelder aus der allgemeinen Dialogfeld Bibliothek verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="7456c-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="7456c-107">Wird von einem Explorer-Dialogfeld " **Öffnen** " oder " **Speichern** unter" gesendet, wenn der Benutzer auf die Schaltfläche " **OK** " klickt und eine Netzwerkfreigabe Verletzung für die ausgewählte Datei auftritt.</span><span class="sxs-lookup"><span data-stu-id="7456c-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the user clicks the **OK** button and a network sharing violation occurs for the selected file.</span></span>

<span data-ttu-id="7456c-108">Die [*ofnhuokproc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) -Hook-Prozedur empfängt diese Nachricht in Form einer [**WM- \_ Benachrichtigungs**](../controls/wm-notify.md) Meldung.</span><span class="sxs-lookup"><span data-stu-id="7456c-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_SHAREVIOLATION      (CDN_FIRST - 0x0003)
```



## <a name="parameters"></a><span data-ttu-id="7456c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7456c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7456c-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7456c-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7456c-111">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="7456c-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7456c-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7456c-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7456c-113">Ein Zeiger auf eine [**ofnotify**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="7456c-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="7456c-114">Der **pszFile** -Member dieser Struktur ist ein Zeiger auf den Namen der Datei mit der Freigabe Verletzung.</span><span class="sxs-lookup"><span data-stu-id="7456c-114">The **pszFile** member of this structure is a pointer to the name of the file that had the sharing violation.</span></span> <span data-ttu-id="7456c-115">Die **ofnotify** -Struktur enthält eine [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) -Struktur, deren **Codemember** die **CDN \_ shareverletzungs** -Benachrichtigungs Meldung angibt.</span><span class="sxs-lookup"><span data-stu-id="7456c-115">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_SHAREVIOLATION** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7456c-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7456c-116">Return value</span></span>

<span data-ttu-id="7456c-117">Der Rückgabewert gibt an, wie das Dialogfeld die Freigabe Verletzung behandeln soll.</span><span class="sxs-lookup"><span data-stu-id="7456c-117">The return value indicates how the dialog box should handle the sharing violation.</span></span>

<span data-ttu-id="7456c-118">Wenn die Hook-Prozedur NULL zurückgibt, wird im Dialogfeld die Standard Warnmeldung für eine Freigabe Verletzung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7456c-118">If the hook procedure returns zero, the dialog box displays the standard warning message for a sharing violation.</span></span>

<span data-ttu-id="7456c-119">Wenn Sie die Anzeige der Standard Warnmeldung verhindern möchten, geben Sie einen Wert ungleich 0 (null) von der Hookprozedur zurück, und geben Sie die Funktion [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) an, um einen der folgenden **DWL- \_ msgresult** -Werte festzulegen.</span><span class="sxs-lookup"><span data-stu-id="7456c-119">To prevent the display of the standard warning message, return a nonzero value from the hook procedure and call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function to set one of the following **DWL\_MSGRESULT** values.</span></span>



| <span data-ttu-id="7456c-120">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="7456c-120">Return code/value</span></span>                                                                                                                                           | <span data-ttu-id="7456c-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7456c-121">Description</span></span>                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7456c-122"><dt>**Ofn \_ Sharefallthrough**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="7456c-122"><dt>**OFN\_SHAREFALLTHROUGH**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="7456c-123">Bewirkt, dass im Dialogfeld der Dateiname zurückgegeben wird, ohne dass der Benutzer die Freigabe Verletzung warnt.</span><span class="sxs-lookup"><span data-stu-id="7456c-123">Causes the dialog box to return the file name without warning the user about the sharing violation.</span></span><br/>  |
| <dl> <span data-ttu-id="7456c-124"><dt>**Ofn \_ Sharenowarn**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="7456c-124"><dt>**OFN\_SHARENOWARN**</dt> <dt>1</dt></span></span> </dl>      | <span data-ttu-id="7456c-125">Bewirkt, dass im Dialogfeld der Dateiname abgelehnt wird, ohne dass der Benutzer über die Freigabe Verletzung gewarnt werden muss.</span><span class="sxs-lookup"><span data-stu-id="7456c-125">Causes the dialog box to reject the file name without warning the user about the sharing violation.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="7456c-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7456c-126">Remarks</span></span>

<span data-ttu-id="7456c-127">Das System sendet diese Benachrichtigung nur, wenn das Dialogfeld mit dem Wert des **ofn- \_ Explorers** erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="7456c-127">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

<span data-ttu-id="7456c-128">Das System sendet diese Benachrichtigung nur dann, wenn beim Erstellen des Dialog Felds kein Wert für " **\_ shareaware** " angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="7456c-128">The system sends this notification only if the **OFN\_SHAREAWARE** value was not specified when the dialog box was created.</span></span>

## <a name="requirements"></a><span data-ttu-id="7456c-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7456c-129">Requirements</span></span>



| <span data-ttu-id="7456c-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7456c-130">Requirement</span></span> | <span data-ttu-id="7456c-131">Wert</span><span class="sxs-lookup"><span data-stu-id="7456c-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7456c-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7456c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="7456c-133">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7456c-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7456c-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7456c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="7456c-135">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7456c-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7456c-136">Header</span><span class="sxs-lookup"><span data-stu-id="7456c-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="7456c-137"><dt>Kommdlg. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7456c-137"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7456c-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7456c-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="7456c-139">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="7456c-139">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7456c-140">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="7456c-140">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="7456c-141">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="7456c-141">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="7456c-142">*Ofnhuokproc*</span><span class="sxs-lookup"><span data-stu-id="7456c-142">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="7456c-143">**Ofnotify**</span><span class="sxs-lookup"><span data-stu-id="7456c-143">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="7456c-144">**OpenFileName**</span><span class="sxs-lookup"><span data-stu-id="7456c-144">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[<span data-ttu-id="7456c-145">**SetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="7456c-145">**SetWindowLong**</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

<span data-ttu-id="7456c-146">**Licher**</span><span class="sxs-lookup"><span data-stu-id="7456c-146">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7456c-147">Allgemeine Dialog Feld Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7456c-147">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

