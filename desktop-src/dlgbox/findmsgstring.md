---
title: Findmsgstring-Nachricht (kommdlg. h)
description: Im Dialogfeld Suchen oder ersetzen wird die registrierte Nachricht findmsgstring an die Fenster Prozedur des Besitzer Fensters gesendet, wenn der Benutzer auf die Schaltfläche weiter suchen, ersetzen oder alle ersetzen klickt oder das Dialogfeld schließt.
ms.assetid: ed0b256a-96df-4588-b8f3-f7d1f89ffe74
keywords:
- Dialog Felder für die findmsgstring-Meldung
topic_type:
- apiref
api_name:
- FINDMSGSTRING
- FINDMSGSTRINGA
- FINDMSGSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0d3a73d8734d79d5ed0862f66bf9ba5c030e46
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518875"
---
# <a name="findmsgstring-message"></a><span data-ttu-id="0c897-104">Findmsgstring-Meldung</span><span class="sxs-lookup"><span data-stu-id="0c897-104">FINDMSGSTRING message</span></span>

<span data-ttu-id="0c897-105">Im Dialogfeld **Suchen** oder **ersetzen** wird die registrierte Nachricht **findmsgstring** an die Fenster Prozedur des Besitzer Fensters gesendet, wenn der Benutzer auf die Schaltfläche **weiter suchen**, **ersetzen** oder **Alle ersetzen** klickt oder das Dialogfeld schließt.</span><span class="sxs-lookup"><span data-stu-id="0c897-105">A **Find** or **Replace** dialog box sends the **FINDMSGSTRING** registered message to the window procedure of its owner window when the user clicks the **Find Next**, **Replace**, or **Replace All** button, or closes the dialog box.</span></span>


```C++
#define FINDMSGSTRING TEXT("commdlg_FindReplace")
```



## <a name="parameters"></a><span data-ttu-id="0c897-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c897-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c897-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0c897-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0c897-108">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0c897-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0c897-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0c897-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0c897-110">Ein Zeiger auf eine [**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="0c897-110">A pointer to a [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) structure.</span></span> <span data-ttu-id="0c897-111">Die Elemente dieser Struktur enthalten die aktuelle Benutzereingabe, einschließlich der zu suchenden Zeichenfolge, der Ersetzungs Zeichenfolge (sofern vorhanden) und der Such-und Ersetzungs Optionen.</span><span class="sxs-lookup"><span data-stu-id="0c897-111">The members of this structure contain the latest user input, including the string to search for, the replacement string (if any) and the search-and-replacement options.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c897-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0c897-112">Return value</span></span>

<span data-ttu-id="0c897-113">Diese Nachricht weist keinen Rückgabewert auf.</span><span class="sxs-lookup"><span data-stu-id="0c897-113">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c897-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0c897-114">Remarks</span></span>

<span data-ttu-id="0c897-115">Sie müssen die **findmsgstring** -Konstante in einem Aufrufen der [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) -Funktion angeben, um den Bezeichner für die vom Dialogfeld gesendete Nachricht abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0c897-115">You must specify the **FINDMSGSTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier for the message sent by the dialog box.</span></span>

<span data-ttu-id="0c897-116">Wenn Sie das Dialogfeld erstellen, verwenden Sie das **hwndOwner** -Element der [**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) -Struktur, um das Fenster zum Empfangen von **findmsgstring** -Nachrichten zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="0c897-116">When you create the dialog box, use the **hwndOwner** member of the [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) structure to identify the window to receive **FINDMSGSTRING** messages.</span></span>

<span data-ttu-id="0c897-117">Der **Flags** -Member der [**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) -Struktur enthält eines der folgenden Flags, um das Ereignis anzugeben, das die Meldung verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="0c897-117">The **Flags** member of the [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) structure includes one of the following flags to indicate the event that caused the message.</span></span>



| <span data-ttu-id="0c897-118">Flag</span><span class="sxs-lookup"><span data-stu-id="0c897-118">Flag</span></span>                            | <span data-ttu-id="0c897-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0c897-119">Meaning</span></span>                                                                                                                                                                                                     |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c897-120">**Fr \_ Dialogterm** (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="0c897-120">**FR\_DIALOGTERM** (0x00000040)</span></span> | <span data-ttu-id="0c897-121">Das Dialogfeld wird geschlossen.</span><span class="sxs-lookup"><span data-stu-id="0c897-121">The dialog box is closing.</span></span> <span data-ttu-id="0c897-122">Nachdem das Besitzer Fenster diese Nachricht verarbeitet hat, ist ein Handle für das Dialogfeld nicht mehr gültig.</span><span class="sxs-lookup"><span data-stu-id="0c897-122">After the owner window processes this message, a handle to the dialog box is no longer valid.</span></span>                                                                                    |
| <span data-ttu-id="0c897-123">**Fr \_ FindNext** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="0c897-123">**FR\_FINDNEXT** (0x00000008)</span></span>   | <span data-ttu-id="0c897-124">Der Benutzer hat auf die Schaltfläche " **weiter suchen** " im Dialogfeld " **Suchen** oder **ersetzen** " geklickt.</span><span class="sxs-lookup"><span data-stu-id="0c897-124">The user clicked the **Find Next** button in a **Find** or **Replace** dialog box.</span></span> <span data-ttu-id="0c897-125">Der **lpstraufindwhat** -Member gibt die zu suchende Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="0c897-125">The **lpstrFindWhat** member specifies the string to search for.</span></span>                                                         |
| <span data-ttu-id="0c897-126">**Fr \_ Ersetzen** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="0c897-126">**FR\_REPLACE** (0x00000010)</span></span>    | <span data-ttu-id="0c897-127">Der Benutzer hat im Dialogfeld " **ersetzen** " auf die Schaltfläche " **ersetzen** " geklickt.</span><span class="sxs-lookup"><span data-stu-id="0c897-127">The user clicked the **Replace** button in a **Replace** dialog box.</span></span> <span data-ttu-id="0c897-128">Der **lpstraufindwhat** -Member gibt die zu ersetzende Zeichenfolge an, und der **lpstraureplacewith** -Member gibt die Ersatz Zeichenfolge an</span><span class="sxs-lookup"><span data-stu-id="0c897-128">The **lpstrFindWhat** member specifies the string to replace and the **lpstrReplaceWith** member specifies the replacement string.</span></span>     |
| <span data-ttu-id="0c897-129">**Fr \_ ReplaceAll** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="0c897-129">**FR\_REPLACEALL** (0x00000020)</span></span> | <span data-ttu-id="0c897-130">Der Benutzer hat auf die Schaltfläche **Alle ersetzen** im Dialogfeld **ersetzen** geklickt.</span><span class="sxs-lookup"><span data-stu-id="0c897-130">The user clicked the **Replace All** button in a **Replace** dialog box.</span></span> <span data-ttu-id="0c897-131">Der **lpstraufindwhat** -Member gibt die zu ersetzende Zeichenfolge an, und der **lpstraureplacewith** -Member gibt die Ersatz Zeichenfolge an</span><span class="sxs-lookup"><span data-stu-id="0c897-131">The **lpstrFindWhat** member specifies the string to replace and the **lpstrReplaceWith** member specifies the replacement string.</span></span> |



 

<span data-ttu-id="0c897-132">Für eine " **weiter** suchen"-oder " **Alle ersetzen** "-Meldung kann das **Flags** -Element eines oder mehrere der folgenden Flags enthalten, um die Suchoptionen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="0c897-132">For a **Find Next** or **Replace All** message, the **Flags** member can include one or more of the following flags to indicate the search options.</span></span>



| <span data-ttu-id="0c897-133">Flag</span><span class="sxs-lookup"><span data-stu-id="0c897-133">Flag</span></span>                           | <span data-ttu-id="0c897-134">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0c897-134">Meaning</span></span>                                                                                                                                                                                                                                                                                         |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c897-135">**Fr \_ Down** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="0c897-135">**FR\_DOWN** (0x00000001)</span></span>      | <span data-ttu-id="0c897-136">Wenn festgelegt, wird die **nach-unten** -Taste der Optionsfeld Richtung ausgewählt und zeigt an, dass der Benutzer vom aktuellen Speicherort bis zum Ende des Dokuments suchen möchte.</span><span class="sxs-lookup"><span data-stu-id="0c897-136">If set, the **Down** button of the direction radio buttons is selected indicating that user wants to search from the current location to the end of the document.</span></span> <span data-ttu-id="0c897-137">Wenn die Option " **\_ nach unten** " nicht festgelegt ist, wird die Schaltfläche "nach **oben** " ausgewählt, sodass der Benutzer am Anfang des Dokuments suchen möchte.</span><span class="sxs-lookup"><span data-stu-id="0c897-137">If **FR\_DOWN** is not set, the **Up** button is selected so the user wants to search to the beginning of the document.</span></span>       |
| <span data-ttu-id="0c897-138">**Fr \_ MatchCase** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="0c897-138">**FR\_MATCHCASE** (0x00000004)</span></span> | <span data-ttu-id="0c897-139">Wenn diese Option festgelegt ist, wird das Kontrollkästchen **Groß-/Kleinschreibung** aktivieren ausgewählt</span><span class="sxs-lookup"><span data-stu-id="0c897-139">If set, the **Match Case** check box is selected indicating that the user wants the search to be case-sensitive.</span></span> <span data-ttu-id="0c897-140">Wenn **fr \_ MatchCase** nicht festgelegt ist, wird das Kontrollkästchen deaktiviert, sodass bei der Suche die Groß-/Kleinschreibung nicht beachtet wird.</span><span class="sxs-lookup"><span data-stu-id="0c897-140">If **FR\_MATCHCASE** is not set, the check box is unselected so the search should be case-insensitive.</span></span>                                                                         |
| <span data-ttu-id="0c897-141">**Fr \_ Wholeword** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="0c897-141">**FR\_WHOLEWORD** (0x00000002)</span></span> | <span data-ttu-id="0c897-142">Wenn diese Option festgelegt ist, wird das Kontrollkästchen **Nur ganzes Wort** suchen aktiviert, das anzeigt, dass der Benutzer nur nach ganzen Wörtern suchen möchte, die der Such Zeichenfolge entsprechen.</span><span class="sxs-lookup"><span data-stu-id="0c897-142">If set, the **Match Whole Word Only** check box is selected indicating that the user wants to search only for whole words that match the search string.</span></span> <span data-ttu-id="0c897-143">Wenn **fr \_ wholeword** nicht festgelegt ist, ist das Kontrollkästchen deaktiviert, sodass Sie auch nach Wortfragmenten suchen müssen, die der Such Zeichenfolge entsprechen.</span><span class="sxs-lookup"><span data-stu-id="0c897-143">If **FR\_WHOLEWORD** is not set, the check box is unselected so you should also search for word fragments that match the search string.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="0c897-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0c897-144">Requirements</span></span>



| <span data-ttu-id="0c897-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0c897-145">Requirement</span></span> | <span data-ttu-id="0c897-146">Wert</span><span class="sxs-lookup"><span data-stu-id="0c897-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c897-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0c897-147">Minimum supported client</span></span><br/> | <span data-ttu-id="0c897-148">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0c897-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0c897-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0c897-149">Minimum supported server</span></span><br/> | <span data-ttu-id="0c897-150">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0c897-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0c897-151">Header</span><span class="sxs-lookup"><span data-stu-id="0c897-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c897-152"><dt>Kommdlg. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0c897-152"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="0c897-153">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="0c897-153">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0c897-154">**Findmsgstringw** (Unicode) und **findmsgstrauinga** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="0c897-154">**FINDMSGSTRINGW** (Unicode) and **FINDMSGSTRINGA** (ANSI)</span></span><br/>                                    |



## <a name="see-also"></a><span data-ttu-id="0c897-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0c897-155">See also</span></span>

<dl> <dt>

<span data-ttu-id="0c897-156">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="0c897-156">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0c897-157">**FindReplace**</span><span class="sxs-lookup"><span data-stu-id="0c897-157">**FINDREPLACE**</span></span>](/windows/win32/api/commdlg/ns-commdlg-findreplacea)
</dt> <dt>

[<span data-ttu-id="0c897-158">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="0c897-158">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="0c897-159">**Licher**</span><span class="sxs-lookup"><span data-stu-id="0c897-159">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0c897-160">Allgemeine Dialog Feld Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0c897-160">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

