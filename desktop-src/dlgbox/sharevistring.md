---
title: SHAREVISTRING-Nachricht (Commdlg.h)
description: Ein Dialogfeld Öffnen oder Speichern unter sendet die registrierte SHAREVISTRING-Nachricht an Ihre Hookprozedur OFNHookProc, wenn ein Freigabeverstoß für die ausgewählte Datei auftritt, wenn der Benutzer auf die Schaltfläche OK klickt.
ms.assetid: 53884497-4872-4aa8-b56e-2bb98df58fed
keywords:
- DIALOGFELDER FÜR SHAREVISTRING-Nachrichten
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
ms.openlocfilehash: 79535b66cff62ad0f9d3fd298fdd76bfc9123a3d
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590667"
---
# <a name="sharevistring-message"></a><span data-ttu-id="b34d9-104">SHAREVISTRING-Nachricht</span><span class="sxs-lookup"><span data-stu-id="b34d9-104">SHAREVISTRING message</span></span>

<span data-ttu-id="b34d9-105">\[Ab Windows Vista wurden  **die** allgemeinen Dialogfelder Öffnen und Speichern unter durch den Allgemeinen [Elementdialog ersetzt.](/windows/win32/shell/common-file-dialog)</span><span class="sxs-lookup"><span data-stu-id="b34d9-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="b34d9-106">Es wird empfohlen, anstelle dieser Dialogfelder aus der Common Dialog Box Library die API für den Allgemeinen Elementdialog zu verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="b34d9-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="b34d9-107">Ein **Dialogfeld** Öffnen oder Speichern unter sendet die registrierte **SHAREVISTRING-Nachricht** an Ihre Hookprozedur [*OFNHookProc,*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)wenn ein Freigabeverstoß für die ausgewählte Datei auftritt, wenn der Benutzer auf die Schaltfläche **OK** klickt. </span><span class="sxs-lookup"><span data-stu-id="b34d9-107">An **Open** or **Save As** dialog box sends the **SHAREVISTRING** registered message to your hook procedure, [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc), if a sharing violation occurs for the selected file when the user clicks the **OK** button.</span></span>


```C++
#define SHAREVISTRING TEXT("commdlg_ShareViolation")
```



## <a name="parameters"></a><span data-ttu-id="b34d9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b34d9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b34d9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b34d9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b34d9-110">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b34d9-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b34d9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b34d9-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b34d9-112">Ein Zeiger auf eine [**OPENFILENAME-Struktur.**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)</span><span class="sxs-lookup"><span data-stu-id="b34d9-112">A pointer to a [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure.</span></span> <span data-ttu-id="b34d9-113">Das **lpstrFile-Member** dieser Struktur enthält den Dateinamen, der den Freigabeverstoß verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="b34d9-113">The **lpstrFile** member of this structure contains the file name that caused the sharing violation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b34d9-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b34d9-114">Return value</span></span>

<span data-ttu-id="b34d9-115">Die Hookprozedur muss einen der folgenden Werte zurückgeben, um anzugeben, wie das Dialogfeld den Freigabeverstoß behandeln soll.</span><span class="sxs-lookup"><span data-stu-id="b34d9-115">The hook procedure must return one of the following values to indicate how the dialog box should handle the sharing violation.</span></span>



| <span data-ttu-id="b34d9-116">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="b34d9-116">Return code/value</span></span>                                                                                                                                           | <span data-ttu-id="b34d9-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b34d9-117">Description</span></span>                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b34d9-118"><dt>**OFN \_ SHAREFALLTHROUGH**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b34d9-118"><dt>**OFN\_SHAREFALLTHROUGH**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="b34d9-119">Akzeptieren des Dateinamens</span><span class="sxs-lookup"><span data-stu-id="b34d9-119">Accept the file name</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="b34d9-120"><dt>**OFN \_ SHARENOWARN**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b34d9-120"><dt>**OFN\_SHARENOWARN**</dt> <dt>1</dt></span></span> </dl>      | <span data-ttu-id="b34d9-121">Lehnen Sie den Dateinamen ab, aber warnen Sie den Benutzer nicht.</span><span class="sxs-lookup"><span data-stu-id="b34d9-121">Reject the file name but do not warn the user.</span></span> <span data-ttu-id="b34d9-122">Die Anwendung ist dafür verantwortlich, eine Warnmeldung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b34d9-122">The application is responsible for displaying a warning message.</span></span><br/> |
| <dl> <span data-ttu-id="b34d9-123"><dt>**OFN \_ SHAREWARN**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b34d9-123"><dt>**OFN\_SHAREWARN**</dt> <dt>0</dt></span></span> </dl>        | <span data-ttu-id="b34d9-124">Lehnen Sie den Dateinamen ab, und zeigt eine Warnmeldung an (das gleiche Ergebnis wie bei einer Hookprozedur).</span><span class="sxs-lookup"><span data-stu-id="b34d9-124">Reject the file name and displays a warning message (the same result as if there were no hook procedure).</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="b34d9-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b34d9-125">Remarks</span></span>

<span data-ttu-id="b34d9-126">Die Hookprozedur muss die **SHAREVISTRING-Konstante** in einem Aufruf der [**RegisterWindowMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) angeben, um den Bezeichner für die vom Dialogfeld gesendete Nachricht zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b34d9-126">The hook procedure must specify the **SHAREVISTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier for the message sent by the dialog box.</span></span>

<span data-ttu-id="b34d9-127">Das Dialogfeld sendet die registrierte **SHAREVISTRING-Nachricht** nur, wenn Sie beim Erstellen des Dialogfelds das **OFN \_ SHAREAWARE-Flag** nicht im **Flags-Member** der [**OPENFILENAME-Struktur**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="b34d9-127">The dialog box sends the **SHAREVISTRING** registered message only if you did not specify the **OFN\_SHAREAWARE** flag in the **Flags** member of the [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure when you created the dialog.</span></span>

<span data-ttu-id="b34d9-128">Wenn die Hookprozedur einen nicht definierten Wert zurückgibt, antwortet das Dialogfeld so, als ob **OFN \_ SHAREWARN** zurückgegeben würde.</span><span class="sxs-lookup"><span data-stu-id="b34d9-128">If the hook procedure returns an undefined value, the dialog box responds as if **OFN\_SHAREWARN** was returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="b34d9-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b34d9-129">Requirements</span></span>



| <span data-ttu-id="b34d9-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b34d9-130">Requirement</span></span> | <span data-ttu-id="b34d9-131">Wert</span><span class="sxs-lookup"><span data-stu-id="b34d9-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b34d9-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b34d9-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b34d9-133">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b34d9-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b34d9-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b34d9-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b34d9-135">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b34d9-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b34d9-136">Header</span><span class="sxs-lookup"><span data-stu-id="b34d9-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="b34d9-137"><dt>Commdlg.h (windows.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="b34d9-137"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="b34d9-138">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="b34d9-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b34d9-139">**SHAREVISTRINGW** (Unicode) und **SHAREVISTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b34d9-139">**SHAREVISTRINGW** (Unicode) and **SHAREVISTRINGA** (ANSI)</span></span><br/>                                    |



## <a name="see-also"></a><span data-ttu-id="b34d9-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b34d9-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="b34d9-141">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="b34d9-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b34d9-142">**CDN \_ SHAREVIOLATION**</span><span class="sxs-lookup"><span data-stu-id="b34d9-142">**CDN\_SHAREVIOLATION**</span></span>](cdn-shareviolation.md)
</dt> <dt>

[<span data-ttu-id="b34d9-143">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="b34d9-143">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[<span data-ttu-id="b34d9-144">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="b34d9-144">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="b34d9-145">**Konzeptionellen**</span><span class="sxs-lookup"><span data-stu-id="b34d9-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b34d9-146">Allgemeine Dialogfeldbibliothek</span><span class="sxs-lookup"><span data-stu-id="b34d9-146">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

