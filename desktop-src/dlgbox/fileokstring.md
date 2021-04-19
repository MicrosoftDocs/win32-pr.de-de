---
title: FILEOKSTRING-Nachricht (Commdlg.h)
description: Ein Dialogfeld Öffnen oder Speichern unter sendet die registrierte FILEOKSTRING-Nachricht an die Hookprozedur OFNHookProc, wenn der Benutzer einen Dateinamen angibt und auf die Schaltfläche OK klickt.
ms.assetid: 32bf3cc7-76a2-4b78-81d7-682b088c4e14
keywords:
- Dialogfelder für FILEOKSTRING-Meldung
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
ms.openlocfilehash: a6fddbb3460f15e1efb946b9bd17f1c85fd031a8
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590787"
---
# <a name="fileokstring-message"></a><span data-ttu-id="bb965-104">FILEOKSTRING-Nachricht</span><span class="sxs-lookup"><span data-stu-id="bb965-104">FILEOKSTRING message</span></span>

<span data-ttu-id="bb965-105">\[Ab Windows Vista wurden die Dialogfelder **Öffnen** und **Speichern unter** allgemein durch das [Dialogfeld "Allgemeines Element"](/windows/win32/shell/common-file-dialog)ersetzt.</span><span class="sxs-lookup"><span data-stu-id="bb965-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="bb965-106">Es wird empfohlen, die DIALOGFELD-API für allgemeine Elemente anstelle dieser Dialogfelder aus der Common Dialog Box Library zu verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="bb965-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="bb965-107">Ein Dialogfeld **Öffnen** oder **Speichern unter** sendet die registrierte **FILEOKSTRING-Nachricht** an Die Hookprozedur [*OFNHookProc,*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)wenn der Benutzer einen Dateinamen angibt und auf die Schaltfläche **OK** klickt.</span><span class="sxs-lookup"><span data-stu-id="bb965-107">An **Open** or **Save As** dialog box sends the **FILEOKSTRING** registered message to your hook procedure, [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc), when the user specifies a file name and clicks the **OK** button.</span></span> <span data-ttu-id="bb965-108">Die Hookprozedur kann den Dateinamen akzeptieren und zulassen, dass das Dialogfeld geschlossen wird, oder den Dateinamen ablehnen und erzwingen, dass das Dialogfeld geöffnet bleibt.</span><span class="sxs-lookup"><span data-stu-id="bb965-108">The hook procedure can accept the file name and allow the dialog box to close, or reject the file name and force the dialog box to remain open.</span></span>


```C++
#define FILEOKSTRING TEXT("commdlg_FileNameOK")
```



## <a name="parameters"></a><span data-ttu-id="bb965-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb965-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb965-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bb965-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb965-111">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="bb965-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bb965-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bb965-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb965-113">Ein Zeiger auf eine [**OPENFILENAME-Struktur.**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)</span><span class="sxs-lookup"><span data-stu-id="bb965-113">A pointer to an [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure.</span></span> <span data-ttu-id="bb965-114">Der **lpstrFile-Member** dieser Struktur enthält das Laufwerk, den Pfad und den Dateinamen, die vom Benutzer angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="bb965-114">The **lpstrFile** member of this structure contains the drive, path, and file name specified by the user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb965-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bb965-115">Return value</span></span>

<span data-ttu-id="bb965-116">Wenn die Hookprozedur 0 (null) zurückgibt, akzeptiert das Dialogfeld **Öffnen** oder **Speichern unter** den angegebenen Dateinamen und wird geschlossen.</span><span class="sxs-lookup"><span data-stu-id="bb965-116">If the hook procedure returns zero, the **Open** or **Save As** dialog box accepts the specified file name and closes.</span></span>

<span data-ttu-id="bb965-117">Wenn die Hookprozedur einen Wert ungleich 0 (null) zurückgibt, lehnt das Dialogfeld **Öffnen** oder **Speichern unter** den angegebenen Dateinamen ab und bleibt geöffnet.</span><span class="sxs-lookup"><span data-stu-id="bb965-117">If the hook procedure returns a nonzero value, the **Open** or **Save As** dialog box rejects the specified file name and remains open.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb965-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bb965-118">Remarks</span></span>

<span data-ttu-id="bb965-119">Die Hookprozedur muss die **FILEOKSTRING-Konstante** in einem Aufruf der [**RegisterWindowMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) angeben, um den Bezeichner für die vom Dialogfeld gesendete Nachricht abzurufen.</span><span class="sxs-lookup"><span data-stu-id="bb965-119">The hook procedure must specify the **FILEOKSTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier for the message sent by the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb965-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bb965-120">Requirements</span></span>



| <span data-ttu-id="bb965-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bb965-121">Requirement</span></span> | <span data-ttu-id="bb965-122">Wert</span><span class="sxs-lookup"><span data-stu-id="bb965-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb965-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bb965-123">Minimum supported client</span></span><br/> | <span data-ttu-id="bb965-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bb965-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="bb965-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bb965-125">Minimum supported server</span></span><br/> | <span data-ttu-id="bb965-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bb965-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bb965-127">Header</span><span class="sxs-lookup"><span data-stu-id="bb965-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb965-128"><dt>Commdlg.h (windows.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="bb965-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="bb965-129">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="bb965-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="bb965-130">**FILEOKSTRINGW** (Unicode) und **FILEOKSTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="bb965-130">**FILEOKSTRINGW** (Unicode) and **FILEOKSTRINGA** (ANSI)</span></span><br/>                                      |



## <a name="see-also"></a><span data-ttu-id="bb965-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="bb965-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="bb965-132">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="bb965-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bb965-133">**CDN \_ FILEOK**</span><span class="sxs-lookup"><span data-stu-id="bb965-133">**CDN\_FILEOK**</span></span>](cdn-fileok.md)
</dt> <dt>

[<span data-ttu-id="bb965-134">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="bb965-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[<span data-ttu-id="bb965-135">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="bb965-135">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="bb965-136">**Konzeptionellen**</span><span class="sxs-lookup"><span data-stu-id="bb965-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="bb965-137">Allgemeine Dialogfeldbibliothek</span><span class="sxs-lookup"><span data-stu-id="bb965-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

