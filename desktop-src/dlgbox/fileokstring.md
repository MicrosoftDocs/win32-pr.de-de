---
title: Fileokstring-Nachricht (kommdlg. h)
description: Ein Dialogfeld zum Öffnen oder speichern unter sendet die registrierte fileokstring-Nachricht an Ihre Hook-Prozedur, ofnhost-proc, wenn der Benutzer einen Dateinamen angibt, und klickt auf die Schaltfläche OK.
ms.assetid: 32bf3cc7-76a2-4b78-81d7-682b088c4e14
keywords:
- Fileokstring-Meldungs Dialogfelder
topic_type:
- apiref
api_name:
- FILEOKSTRING
- FILEOKSTRINGA
- FILEOKSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61208ddebc63f1186c2947416e451231f0bea24e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478981"
---
# <a name="fileokstring-message"></a><span data-ttu-id="e34dd-104">Fileokstring-Nachricht</span><span class="sxs-lookup"><span data-stu-id="e34dd-104">FILEOKSTRING message</span></span>

<span data-ttu-id="e34dd-105">\[Ab Windows Vista wurden die Dialogfelder " **Öffnen** " und " **Speichern** unter" im allgemeinen [Element](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85))ersetzt.</span><span class="sxs-lookup"><span data-stu-id="e34dd-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="e34dd-106">Es wird empfohlen, dass Sie die allgemeine Element Dialogfeld-API anstelle dieser Dialogfelder aus der allgemeinen Dialogfeld Bibliothek verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="e34dd-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="e34dd-107">Ein Dialogfeld zum **Öffnen** oder **Speichern** unter sendet die registrierte **fileokstring** -Nachricht an Ihre Hook-Prozedur, [*ofnhost-proc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc), wenn der Benutzer einen Dateinamen angibt, und klickt auf die Schaltfläche **OK** .</span><span class="sxs-lookup"><span data-stu-id="e34dd-107">An **Open** or **Save As** dialog box sends the **FILEOKSTRING** registered message to your hook procedure, [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc), when the user specifies a file name and clicks the **OK** button.</span></span> <span data-ttu-id="e34dd-108">Die Hook-Prozedur kann den Dateinamen akzeptieren und das Dialogfeld schließen oder den Dateinamen ablehnen und erzwingen, dass das Dialogfeld geöffnet bleibt.</span><span class="sxs-lookup"><span data-stu-id="e34dd-108">The hook procedure can accept the file name and allow the dialog box to close, or reject the file name and force the dialog box to remain open.</span></span>


```C++
#define FILEOKSTRING TEXT("commdlg_FileNameOK")
```



## <a name="parameters"></a><span data-ttu-id="e34dd-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e34dd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e34dd-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e34dd-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e34dd-111">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="e34dd-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e34dd-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e34dd-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e34dd-113">Ein Zeiger auf eine [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="e34dd-113">A pointer to an [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure.</span></span> <span data-ttu-id="e34dd-114">Der **lpstraufile** -Member dieser Struktur enthält das Laufwerk, den Pfad und den Dateinamen, die vom Benutzer angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e34dd-114">The **lpstrFile** member of this structure contains the drive, path, and file name specified by the user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e34dd-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e34dd-115">Return value</span></span>

<span data-ttu-id="e34dd-116">Wenn die Hook-Prozedur NULL zurückgibt, akzeptiert das Dialogfeld **Öffnen** oder **Speichern** unter den angegebenen Dateinamen und wird geschlossen.</span><span class="sxs-lookup"><span data-stu-id="e34dd-116">If the hook procedure returns zero, the **Open** or **Save As** dialog box accepts the specified file name and closes.</span></span>

<span data-ttu-id="e34dd-117">Wenn die Hook-Prozedur einen Wert ungleich 0 (null) zurückgibt, lehnt das Dialogfeld **Öffnen** oder speichern unter den angegebenen Dateinamen **ab** und bleibt geöffnet.</span><span class="sxs-lookup"><span data-stu-id="e34dd-117">If the hook procedure returns a nonzero value, the **Open** or **Save As** dialog box rejects the specified file name and remains open.</span></span>

## <a name="remarks"></a><span data-ttu-id="e34dd-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e34dd-118">Remarks</span></span>

<span data-ttu-id="e34dd-119">Die Hook-Prozedur muss die **fileokstring** -Konstante in einem Aufrufen der [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) -Funktion angeben, um den Bezeichner für die vom Dialogfeld gesendete Nachricht abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e34dd-119">The hook procedure must specify the **FILEOKSTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier for the message sent by the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="e34dd-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e34dd-120">Requirements</span></span>



| <span data-ttu-id="e34dd-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e34dd-121">Requirement</span></span> | <span data-ttu-id="e34dd-122">Wert</span><span class="sxs-lookup"><span data-stu-id="e34dd-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e34dd-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e34dd-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e34dd-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e34dd-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e34dd-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e34dd-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e34dd-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e34dd-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e34dd-127">Header</span><span class="sxs-lookup"><span data-stu-id="e34dd-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e34dd-128"><dt>Kommdlg. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e34dd-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e34dd-129">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="e34dd-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e34dd-130">**Fileokstringw** (Unicode) und **fileokstraninga** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e34dd-130">**FILEOKSTRINGW** (Unicode) and **FILEOKSTRINGA** (ANSI)</span></span><br/>                                      |



## <a name="see-also"></a><span data-ttu-id="e34dd-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e34dd-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="e34dd-132">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="e34dd-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e34dd-133">**CDN- \_ Datei OK**</span><span class="sxs-lookup"><span data-stu-id="e34dd-133">**CDN\_FILEOK**</span></span>](cdn-fileok.md)
</dt> <dt>

[<span data-ttu-id="e34dd-134">**OpenFileName**</span><span class="sxs-lookup"><span data-stu-id="e34dd-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[<span data-ttu-id="e34dd-135">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="e34dd-135">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="e34dd-136">**Licher**</span><span class="sxs-lookup"><span data-stu-id="e34dd-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e34dd-137">Allgemeine Dialog Feld Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e34dd-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

