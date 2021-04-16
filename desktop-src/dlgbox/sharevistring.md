---
title: Sharevistring-Nachricht (kommdlg. h)
description: Ein Dialogfeld zum Öffnen oder speichern unter sendet die registrierte sharevistring-Nachricht an die Hook-Prozedur ofnhuokproc, wenn eine Freigabe Verletzung für die ausgewählte Datei auftritt, wenn der Benutzer auf die Schaltfläche OK klickt.
ms.assetid: 53884497-4872-4aa8-b56e-2bb98df58fed
keywords:
- Share Message String-Meldungs Dialogfelder
topic_type:
- apiref
api_name:
- SHAREVISTRING
- SHAREVISTRINGA
- SHAREVISTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c23c17280ad1156e35f7e0f503816c07645cf4f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477979"
---
# <a name="sharevistring-message"></a><span data-ttu-id="6bdc5-104">Sharevistring-Meldung</span><span class="sxs-lookup"><span data-stu-id="6bdc5-104">SHAREVISTRING message</span></span>

<span data-ttu-id="6bdc5-105">\[Ab Windows Vista wurden die Dialogfelder " **Öffnen** " und " **Speichern** unter" im allgemeinen [Element](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85))ersetzt.</span><span class="sxs-lookup"><span data-stu-id="6bdc5-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="6bdc5-106">Es wird empfohlen, dass Sie die allgemeine Element Dialogfeld-API anstelle dieser Dialogfelder aus der allgemeinen Dialogfeld Bibliothek verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="6bdc5-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="6bdc5-107">Ein Dialogfeld zum **Öffnen** oder **Speichern** unter sendet die registrierte **sharevistring** -Nachricht an die Hook-Prozedur [*ofnhuokproc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc), wenn eine Freigabe Verletzung für die ausgewählte Datei auftritt, wenn der Benutzer auf die Schaltfläche **OK** klickt.</span><span class="sxs-lookup"><span data-stu-id="6bdc5-107">An **Open** or **Save As** dialog box sends the **SHAREVISTRING** registered message to your hook procedure, [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc), if a sharing violation occurs for the selected file when the user clicks the **OK** button.</span></span>


```C++
#define SHAREVISTRING TEXT("commdlg_ShareViolation")
```



## <a name="parameters"></a><span data-ttu-id="6bdc5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6bdc5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bdc5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6bdc5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6bdc5-110">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="6bdc5-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6bdc5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6bdc5-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6bdc5-112">Ein Zeiger auf eine [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="6bdc5-112">A pointer to a [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure.</span></span> <span data-ttu-id="6bdc5-113">Der **lpstraufile** -Member dieser Struktur enthält den Dateinamen, der die Freigabe Verletzung verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="6bdc5-113">The **lpstrFile** member of this structure contains the file name that caused the sharing violation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bdc5-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6bdc5-114">Return value</span></span>

<span data-ttu-id="6bdc5-115">Die Hook-Prozedur muss einen der folgenden Werte zurückgeben, um anzugeben, wie das Dialogfeld die Freigabe Verletzung behandeln soll.</span><span class="sxs-lookup"><span data-stu-id="6bdc5-115">The hook procedure must return one of the following values to indicate how the dialog box should handle the sharing violation.</span></span>



| <span data-ttu-id="6bdc5-116">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="6bdc5-116">Return code/value</span></span>                                                                                                                                           | <span data-ttu-id="6bdc5-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6bdc5-117">Description</span></span>                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6bdc5-118"><dt>**Ofn \_ Sharefallthrough**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="6bdc5-118"><dt>**OFN\_SHAREFALLTHROUGH**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="6bdc5-119">Dateiname akzeptieren</span><span class="sxs-lookup"><span data-stu-id="6bdc5-119">Accept the file name</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="6bdc5-120"><dt>**Ofn \_ Sharenowarn**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="6bdc5-120"><dt>**OFN\_SHARENOWARN**</dt> <dt>1</dt></span></span> </dl>      | <span data-ttu-id="6bdc5-121">Ablehnen Sie den Dateinamen, aber warnen Sie den Benutzer nicht.</span><span class="sxs-lookup"><span data-stu-id="6bdc5-121">Reject the file name but do not warn the user.</span></span> <span data-ttu-id="6bdc5-122">Die Anwendung ist dafür verantwortlich, eine Warnmeldung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6bdc5-122">The application is responsible for displaying a warning message.</span></span><br/> |
| <dl> <span data-ttu-id="6bdc5-123"><dt>**Ofn \_ Sharewarn**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6bdc5-123"><dt>**OFN\_SHAREWARN**</dt> <dt>0</dt></span></span> </dl>        | <span data-ttu-id="6bdc5-124">Ablehnen Sie den Dateinamen, und zeigt eine Warnmeldung an (das gleiche Ergebnis wie bei keiner Hook-Prozedur).</span><span class="sxs-lookup"><span data-stu-id="6bdc5-124">Reject the file name and displays a warning message (the same result as if there were no hook procedure).</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="6bdc5-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6bdc5-125">Remarks</span></span>

<span data-ttu-id="6bdc5-126">Die Hook-Prozedur muss die **sharevistring** -Konstante in einem Aufrufen der [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) -Funktion angeben, um den Bezeichner für die vom Dialogfeld gesendete Nachricht abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6bdc5-126">The hook procedure must specify the **SHAREVISTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier for the message sent by the dialog box.</span></span>

<span data-ttu-id="6bdc5-127">Das Dialogfeld sendet die registrierte **sharevistring** -Nachricht nur dann, wenn Sie beim Erstellen des Dialog Felds nicht das **ofn \_ shareaware** -Flag im **Flags** -Member der [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) -Struktur angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="6bdc5-127">The dialog box sends the **SHAREVISTRING** registered message only if you did not specify the **OFN\_SHAREAWARE** flag in the **Flags** member of the [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure when you created the dialog.</span></span>

<span data-ttu-id="6bdc5-128">Wenn die Hook-Prozedur einen nicht definierten Wert zurückgibt, antwortet das Dialogfeld so, als ob **ofn \_ sharewarn** zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="6bdc5-128">If the hook procedure returns an undefined value, the dialog box responds as if **OFN\_SHAREWARN** was returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bdc5-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6bdc5-129">Requirements</span></span>



| <span data-ttu-id="6bdc5-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6bdc5-130">Requirement</span></span> | <span data-ttu-id="6bdc5-131">Wert</span><span class="sxs-lookup"><span data-stu-id="6bdc5-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bdc5-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6bdc5-132">Minimum supported client</span></span><br/> | <span data-ttu-id="6bdc5-133">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6bdc5-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6bdc5-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6bdc5-134">Minimum supported server</span></span><br/> | <span data-ttu-id="6bdc5-135">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6bdc5-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6bdc5-136">Header</span><span class="sxs-lookup"><span data-stu-id="6bdc5-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="6bdc5-137"><dt>Kommdlg. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6bdc5-137"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="6bdc5-138">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="6bdc5-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6bdc5-139">**Sharevistringw** (Unicode) und **shareviampinga** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="6bdc5-139">**SHAREVISTRINGW** (Unicode) and **SHAREVISTRINGA** (ANSI)</span></span><br/>                                    |



## <a name="see-also"></a><span data-ttu-id="6bdc5-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6bdc5-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="6bdc5-141">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="6bdc5-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6bdc5-142">**CDN- \_ share-Verletzung**</span><span class="sxs-lookup"><span data-stu-id="6bdc5-142">**CDN\_SHAREVIOLATION**</span></span>](cdn-shareviolation.md)
</dt> <dt>

[<span data-ttu-id="6bdc5-143">**OpenFileName**</span><span class="sxs-lookup"><span data-stu-id="6bdc5-143">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[<span data-ttu-id="6bdc5-144">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="6bdc5-144">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="6bdc5-145">**Licher**</span><span class="sxs-lookup"><span data-stu-id="6bdc5-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6bdc5-146">Allgemeine Dialog Feld Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6bdc5-146">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

