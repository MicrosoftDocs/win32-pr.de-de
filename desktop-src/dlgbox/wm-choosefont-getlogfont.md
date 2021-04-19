---
title: WM_CHOOSEFONT_GETLOGFONT Meldung (kommdlg. h)
description: Eine Anwendung sendet die WM \_ choosefont \_ getlogfont-Nachricht an ein Schriftart Dialogfeld, um Informationen über die aktuelle Schriftart Auswahl des Benutzers abzurufen.
ms.assetid: afbf953a-13dd-409b-a988-f1426c8bbd31
keywords:
- Dialog Felder WM_CHOOSEFONT_GETLOGFONT Meldung
topic_type:
- apiref
api_name:
- WM_CHOOSEFONT_GETLOGFONT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 696246d26c2b87e9b299844a9dc7e78d39ac632f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339998"
---
# <a name="wm_choosefont_getlogfont-message"></a><span data-ttu-id="9b7f0-104">WM- \_ Auswahl Schriftart \_ getlogfont</span><span class="sxs-lookup"><span data-stu-id="9b7f0-104">WM\_CHOOSEFONT\_GETLOGFONT message</span></span>

<span data-ttu-id="9b7f0-105">Eine Anwendung sendet die **WM \_ choosefont \_ getlogfont** -Nachricht an ein **Schriftart** Dialogfeld, um Informationen über die aktuelle Schriftart Auswahl des Benutzers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9b7f0-105">An application sends the **WM\_CHOOSEFONT\_GETLOGFONT** message to a **Font** dialog box to retrieve information about the user's current font selections.</span></span>


```C++
#define WM_USER                        0x0400
#define WM_CHOOSEFONT_GETLOGFONT      (WM_USER + 1)
```



## <a name="parameters"></a><span data-ttu-id="9b7f0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b7f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b7f0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9b7f0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9b7f0-108">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="9b7f0-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9b7f0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9b7f0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9b7f0-110">Ein Zeiger auf eine [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur, die Informationen über die aktuelle Schriftart Auswahl des Benutzers empfängt.</span><span class="sxs-lookup"><span data-stu-id="9b7f0-110">A pointer to a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure that receives information about the user's current font selections.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b7f0-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9b7f0-111">Return value</span></span>

<span data-ttu-id="9b7f0-112">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9b7f0-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b7f0-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9b7f0-113">Remarks</span></span>

<span data-ttu-id="9b7f0-114">Die [**Auswahl Schriftart**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) erstellt ein Dialogfeld für die **Schriftart** .</span><span class="sxs-lookup"><span data-stu-id="9b7f0-114">The [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) function creates a **Font** dialog box.</span></span> <span data-ttu-id="9b7f0-115">Wenn der Benutzer das Dialogfeld **Schriftart** schließt, gibt die **Auswahl Schriftart** Informationen über die Schriftart Auswahl des Benutzers in der [**Auswahl Schriftart**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) zurück.</span><span class="sxs-lookup"><span data-stu-id="9b7f0-115">When the user closes the **Font** dialog box, the **ChooseFont** function returns information about the user's font selections in the [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure.</span></span> <span data-ttu-id="9b7f0-116">Der **lplogfont** -Member der **chooonfont** -Struktur ist ein Zeiger auf eine [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="9b7f0-116">The **lpLogFont** member of the **CHOOSEFONT** structure is a pointer to a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span>

<span data-ttu-id="9b7f0-117">Verwenden Sie die " **WM \_ choocfont \_ getlogfont** "-Meldung, um Informationen über die aktuelle Schriftart Auswahl des Benutzers zu erhalten, während das Dialogfeld **Schriftart** geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="9b7f0-117">Use the **WM\_CHOOSEFONT\_GETLOGFONT** message to get information about the user's current font selections while the **Font** dialog box is open.</span></span> <span data-ttu-id="9b7f0-118">Wenn Sie z. b. die Schaltfläche **anwenden** im Dialogfeld **Schriftart** aktivieren, senden Sie die Nachricht, um die Schriftart Informationen zu erhalten, die auf die aktuelle Textauswahl angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9b7f0-118">For example, if you enable the **Apply** button in the **Font** dialog box, send the message to get the font information to apply to the current text selection.</span></span>

<span data-ttu-id="9b7f0-119">In der Regel aktivieren Sie eine [*cfhuokproc*](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) -Hook-Prozedur, um die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldungen für die Schaltfläche **anwenden** zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="9b7f0-119">Typically, you enable a [*CFHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) hook procedure to process [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) messages for the **Apply** button.</span></span> <span data-ttu-id="9b7f0-120">Wenn **der Benutzer auf die Schalt** Fläche übernehmen klickt, sendet die Hook-Prozedur die Meldung **WM \_ choocfont \_ getlogfont** an das Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="9b7f0-120">When the user clicks the **Apply** button, the hook procedure sends the **WM\_CHOOSEFONT\_GETLOGFONT** message to the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b7f0-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9b7f0-121">Requirements</span></span>



| <span data-ttu-id="9b7f0-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9b7f0-122">Requirement</span></span> | <span data-ttu-id="9b7f0-123">Wert</span><span class="sxs-lookup"><span data-stu-id="9b7f0-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b7f0-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9b7f0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9b7f0-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9b7f0-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9b7f0-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9b7f0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9b7f0-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9b7f0-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9b7f0-128">Header</span><span class="sxs-lookup"><span data-stu-id="9b7f0-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b7f0-129"><dt>Kommdlg. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9b7f0-129"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b7f0-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9b7f0-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="9b7f0-131">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="9b7f0-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9b7f0-132">**Cfhuokproc**</span><span class="sxs-lookup"><span data-stu-id="9b7f0-132">**CFHookProc**</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)
</dt> <dt>

[<span data-ttu-id="9b7f0-133">**Auswahl Schriftart**</span><span class="sxs-lookup"><span data-stu-id="9b7f0-133">**ChooseFont**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[<span data-ttu-id="9b7f0-134">**Auswahl Schriftart**</span><span class="sxs-lookup"><span data-stu-id="9b7f0-134">**CHOOSEFONT**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[<span data-ttu-id="9b7f0-135">**WM- \_ Befehl**</span><span class="sxs-lookup"><span data-stu-id="9b7f0-135">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> <dt>

<span data-ttu-id="9b7f0-136">**Licher**</span><span class="sxs-lookup"><span data-stu-id="9b7f0-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9b7f0-137">Allgemeine Dialog Feld Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9b7f0-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> <dt>

<span data-ttu-id="9b7f0-138">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="9b7f0-138">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="9b7f0-139">**"LogFont"**</span><span class="sxs-lookup"><span data-stu-id="9b7f0-139">**LOGFONT**</span></span>](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 

