---
title: Verwenden der Zwischenablage
description: 'Dieser Abschnitt enthält Codebeispiele für die folgenden Aufgaben:'
ms.assetid: 377fb2cc-5b46-481a-8222-9291e504ae2c
keywords:
- Zwischenablage, Daten werden abgeschnitten
- Zwischenablage, Kopieren von Daten
- Zwischenablage, Einfügen von Daten
- Zwischenablage, auswählen von Daten
- Zwischenablage, Menübefehle bearbeiten
- Zwischenablage, Viewer
- Zwischenablage, Viewer-Fenster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d7c7e7d6db6f25bc1016eefbcc5afc9f5e0db44
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315459"
---
# <a name="using-the-clipboard"></a><span data-ttu-id="9182a-110">Verwenden der Zwischenablage</span><span class="sxs-lookup"><span data-stu-id="9182a-110">Using the Clipboard</span></span>

<span data-ttu-id="9182a-111">Dieser Abschnitt enthält Codebeispiele für die folgenden Aufgaben:</span><span class="sxs-lookup"><span data-stu-id="9182a-111">This section has code samples for the following tasks:</span></span>

-   [<span data-ttu-id="9182a-112">Implementieren der Befehle zum Ausschneiden, kopieren und Einfügen</span><span class="sxs-lookup"><span data-stu-id="9182a-112">Implementing the Cut, Copy, and Paste Commands</span></span>](#implementing-the-cut-copy-and-paste-commands)
    -   [<span data-ttu-id="9182a-113">Auswählen von Daten</span><span class="sxs-lookup"><span data-stu-id="9182a-113">Selecting Data</span></span>](#selecting-data)
    -   [<span data-ttu-id="9182a-114">Erstellen eines Bearbeitungs Menüs</span><span class="sxs-lookup"><span data-stu-id="9182a-114">Creating an Edit Menu</span></span>](#creating-an-edit-menu)
    -   [<span data-ttu-id="9182a-115">Verarbeiten der "WM \_ initmenupopup"-Meldung</span><span class="sxs-lookup"><span data-stu-id="9182a-115">Processing the WM\_INITMENUPOPUP Message</span></span>](#processing-the-wm_initmenupopup-message)
    -   [<span data-ttu-id="9182a-116">Verarbeiten der WM- \_ Befehls Meldung</span><span class="sxs-lookup"><span data-stu-id="9182a-116">Processing the WM\_COMMAND Message</span></span>](#processing-the-wm_command-message)
    -   [<span data-ttu-id="9182a-117">Kopieren von Informationen in die Zwischenablage</span><span class="sxs-lookup"><span data-stu-id="9182a-117">Copying Information to the Clipboard</span></span>](#copying-information-to-the-clipboard)
    -   [<span data-ttu-id="9182a-118">Einfügen von Informationen aus der Zwischenablage</span><span class="sxs-lookup"><span data-stu-id="9182a-118">Pasting Information from the Clipboard</span></span>](#pasting-information-from-the-clipboard)
    -   [<span data-ttu-id="9182a-119">Registrieren eines Zwischenablage Formats</span><span class="sxs-lookup"><span data-stu-id="9182a-119">Registering a Clipboard Format</span></span>](#registering-a-clipboard-format)
    -   [<span data-ttu-id="9182a-120">Verarbeiten der \_ Nachrichten "WM Renderformat" und "WM \_ renderallformats"</span><span class="sxs-lookup"><span data-stu-id="9182a-120">Processing the WM\_RENDERFORMAT and WM\_RENDERALLFORMATS Messages</span></span>](#processing-the-wm_renderformat-and-wm_renderallformats-messages)
    -   [<span data-ttu-id="9182a-121">Verarbeiten der WM \_ destroyclipboard-Nachricht</span><span class="sxs-lookup"><span data-stu-id="9182a-121">Processing the WM\_DESTROYCLIPBOARD Message</span></span>](#processing-the-wm_destroyclipboard-message)
    -   [<span data-ttu-id="9182a-122">Verwenden des Owner-Display-Zwischenablage Formats</span><span class="sxs-lookup"><span data-stu-id="9182a-122">Using the Owner-Display Clipboard Format</span></span>](#using-the-owner-display-clipboard-format)
-   [<span data-ttu-id="9182a-123">Überwachen der Zwischenablage</span><span class="sxs-lookup"><span data-stu-id="9182a-123">Monitoring Clipboard Contents</span></span>](#monitoring-clipboard-contents)
-   [<span data-ttu-id="9182a-124">Abfragen der Zwischenablage-Sequenznummer</span><span class="sxs-lookup"><span data-stu-id="9182a-124">Querying the Clipboard Sequence Number</span></span>](#querying-the-clipboard-sequence-number)
-   [<span data-ttu-id="9182a-125">Erstellen eines-Zwischenablage-formatlistener</span><span class="sxs-lookup"><span data-stu-id="9182a-125">Creating a Clipboard Format Listener</span></span>](#creating-a-clipboard-format-listener)
-   [<span data-ttu-id="9182a-126">Erstellen eines Zwischenablage-Viewer-Fensters</span><span class="sxs-lookup"><span data-stu-id="9182a-126">Creating a Clipboard Viewer Window</span></span>](#creating-a-clipboard-viewer-window)
-   [<span data-ttu-id="9182a-127">Hinzufügen eines Fensters zur Zwischenablage-Viewer-Kette</span><span class="sxs-lookup"><span data-stu-id="9182a-127">Adding a Window to the Clipboard Viewer Chain</span></span>](#adding-a-window-to-the-clipboard-viewer-chain)
    -   [<span data-ttu-id="9182a-128">Verarbeiten der WM- \_ CHANGECBCHAIN-Nachricht</span><span class="sxs-lookup"><span data-stu-id="9182a-128">Processing the WM\_CHANGECBCHAIN Message</span></span>](#processing-the-wm_changecbchain-message)
    -   [<span data-ttu-id="9182a-129">Entfernen eines Fensters aus der Zwischenablage-Viewer-Kette</span><span class="sxs-lookup"><span data-stu-id="9182a-129">Removing a Window from the Clipboard Viewer Chain</span></span>](#removing-a-window-from-the-clipboard-viewer-chain)
    -   [<span data-ttu-id="9182a-130">Die WM- \_ drawclipboard-Nachricht wird verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="9182a-130">Processing the WM\_DRAWCLIPBOARD Message</span></span>](#processing-the-wm_drawclipboard-message)
    -   [<span data-ttu-id="9182a-131">Beispiel für einen Zwischenablage-Viewer</span><span class="sxs-lookup"><span data-stu-id="9182a-131">Example of a Clipboard Viewer</span></span>](#example-of-a-clipboard-viewer)

## <a name="implementing-the-cut-copy-and-paste-commands"></a><span data-ttu-id="9182a-132">Implementieren der Befehle zum Ausschneiden, kopieren und Einfügen</span><span class="sxs-lookup"><span data-stu-id="9182a-132">Implementing the Cut, Copy, and Paste Commands</span></span>

<span data-ttu-id="9182a-133">In diesem Abschnitt wird beschrieben, wie Standard Befehle zum **Ausschneiden**, **Kopieren** und **Einfügen** in einer Anwendung implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="9182a-133">This section describes how standard **Cut**, **Copy**, and **Paste** commands are implemented in an application.</span></span> <span data-ttu-id="9182a-134">Das Beispiel in diesem Abschnitt verwendet diese Methoden, um Daten in der Zwischenablage mithilfe eines registrierten Zwischenablage Formats, des CF-Besitzer **\_ Anzeige** Formats und des **CF- \_ Text** Formats zu platzieren.</span><span class="sxs-lookup"><span data-stu-id="9182a-134">The example in this section uses these methods to place data on the clipboard using a registered clipboard format, the **CF\_OWNERDISPLAY** format, and the **CF\_TEXT** format.</span></span> <span data-ttu-id="9182a-135">Das registrierte Format wird verwendet, um rechteckige oder elliptische Textfenster darzustellen, die als Bezeichnungen bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="9182a-135">The registered format is used to represent rectangular or elliptical text windows, called labels.</span></span>

### <a name="selecting-data"></a><span data-ttu-id="9182a-136">Auswählen von Daten</span><span class="sxs-lookup"><span data-stu-id="9182a-136">Selecting Data</span></span>

<span data-ttu-id="9182a-137">Bevor Informationen in die Zwischenablage kopiert werden können, muss der Benutzer bestimmte Informationen auswählen, die kopiert oder ausgeschnitten werden.</span><span class="sxs-lookup"><span data-stu-id="9182a-137">Before information can be copied to the clipboard, the user must select specific information to be copied or cut.</span></span> <span data-ttu-id="9182a-138">Eine Anwendung sollte dem Benutzer die Möglichkeit bieten, Informationen innerhalb eines Dokuments auszuwählen, und eine Art visuelles Feedback, um die ausgewählten Daten anzugeben.</span><span class="sxs-lookup"><span data-stu-id="9182a-138">An application should provide a means for the user to select information within a document and some kind of visual feedback to indicate selected data.</span></span>

### <a name="creating-an-edit-menu"></a><span data-ttu-id="9182a-139">Erstellen eines Bearbeitungs Menüs</span><span class="sxs-lookup"><span data-stu-id="9182a-139">Creating an Edit Menu</span></span>

<span data-ttu-id="9182a-140">Eine Anwendung sollte eine Zugriffstasten Tabelle mit den Standard-Tastatur Acceleratoren für die Befehle Menü **Bearbeiten** laden.</span><span class="sxs-lookup"><span data-stu-id="9182a-140">An application should load an accelerator table containing the standard keyboard accelerators for the **Edit** menu commands.</span></span> <span data-ttu-id="9182a-141">Die [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) -Funktion muss der Nachrichten Schleife der Anwendung hinzugefügt werden, damit die Accelerators wirksam werden.</span><span class="sxs-lookup"><span data-stu-id="9182a-141">The [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) function must be added to the application's message loop for the accelerators to take effect.</span></span> <span data-ttu-id="9182a-142">Weitere Informationen zu Tastatur Accelerators finden Sie unter [Tastaturbeschleuniger](/windows/desktop/menurc/keyboard-accelerators).</span><span class="sxs-lookup"><span data-stu-id="9182a-142">For more information about keyboard accelerators, see [Keyboard Accelerators](/windows/desktop/menurc/keyboard-accelerators).</span></span>

### <a name="processing-the-wm_initmenupopup-message"></a><span data-ttu-id="9182a-143">Verarbeiten der "WM \_ initmenupopup"-Meldung</span><span class="sxs-lookup"><span data-stu-id="9182a-143">Processing the WM\_INITMENUPOPUP Message</span></span>

<span data-ttu-id="9182a-144">Nicht alle Zwischenablage Befehle stehen dem Benutzer zu einem bestimmten Zeitpunkt zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="9182a-144">Not all clipboard commands are available to the user at any given time.</span></span> <span data-ttu-id="9182a-145">Eine Anwendung sollte die " [**WM \_ initmenupopup**](/windows/desktop/menurc/wm-initmenupopup) "-Meldung verarbeiten, um die Menü Elemente für verfügbare Befehle zu aktivieren und nicht verfügbare Befehle zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="9182a-145">An application should process the [**WM\_INITMENUPOPUP**](/windows/desktop/menurc/wm-initmenupopup) message to enable the menu items for available commands and disable unavailable commands.</span></span>

<span data-ttu-id="9182a-146">Im folgenden finden Sie den Fall " [**WM \_ initmenupopup**](/windows/desktop/menurc/wm-initmenupopup) " für eine Anwendung namens "Label".</span><span class="sxs-lookup"><span data-stu-id="9182a-146">Following is the [**WM\_INITMENUPOPUP**](/windows/desktop/menurc/wm-initmenupopup) case for an application named Label.</span></span>


```
case WM_INITMENUPOPUP:
    InitMenu((HMENU) wParam);
    break;
```



<span data-ttu-id="9182a-147">Die InitMenu-Funktion ist wie folgt definiert.</span><span class="sxs-lookup"><span data-stu-id="9182a-147">The InitMenu function is defined as follows.</span></span>


```
void WINAPI InitMenu(HMENU hmenu) 
{ 
    int  cMenuItems = GetMenuItemCount(hmenu); 
    int  nPos; 
    UINT id; 
    UINT fuFlags; 
    PLABELBOX pbox = (hwndSelected == NULL) ? NULL : 
        (PLABELBOX) GetWindowLong(hwndSelected, 0); 
 
    for (nPos = 0; nPos < cMenuItems; nPos++) 
    { 
        id = GetMenuItemID(hmenu, nPos); 
 
        switch (id) 
        { 
            case IDM_CUT: 
            case IDM_COPY: 
            case IDM_DELETE: 
                if (pbox == NULL || !pbox->fSelected) 
                    fuFlags = MF_BYCOMMAND | MF_GRAYED; 
                else if (pbox->fEdit) 
                    fuFlags = (id != IDM_DELETE && pbox->ichSel 
                            == pbox->ichCaret) ? 
                        MF_BYCOMMAND | MF_GRAYED : 
                        MF_BYCOMMAND | MF_ENABLED; 
                else 
                    fuFlags = MF_BYCOMMAND | MF_ENABLED; 
 
                EnableMenuItem(hmenu, id, fuFlags); 
                break; 
 
            case IDM_PASTE: 
                if (pbox != NULL && pbox->fEdit) 
                    EnableMenuItem(hmenu, id, 
                        IsClipboardFormatAvailable(CF_TEXT) ? 
                            MF_BYCOMMAND | MF_ENABLED : 
                            MF_BYCOMMAND | MF_GRAYED 
                    ); 
                else 
                    EnableMenuItem(hmenu, id, 
                        IsClipboardFormatAvailable( 
                                uLabelFormat) ? 
                            MF_BYCOMMAND | MF_ENABLED : 
                            MF_BYCOMMAND | MF_GRAYED 
                    ); 
 
        } 
    } 
}
```



### <a name="processing-the-wm_command-message"></a><span data-ttu-id="9182a-148">Verarbeiten der WM- \_ Befehls Meldung</span><span class="sxs-lookup"><span data-stu-id="9182a-148">Processing the WM\_COMMAND Message</span></span>

<span data-ttu-id="9182a-149">Um Menübefehle zu verarbeiten, fügen Sie den [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Fall zur Hauptfenster Prozedur Ihrer Anwendung hinzu.</span><span class="sxs-lookup"><span data-stu-id="9182a-149">To process menu commands, add the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) case to your application's main window procedure.</span></span> <span data-ttu-id="9182a-150">Im folgenden finden Sie den **WM- \_ Befehls** Fall für die Fenster Prozedur der Bezeichnung Anwendung.</span><span class="sxs-lookup"><span data-stu-id="9182a-150">Following is the **WM\_COMMAND** case for the Label application's window procedure.</span></span>


```
case WM_COMMAND: 
    switch (LOWORD(wParam)) 
    { 
        case IDM_CUT: 
            if (EditCopy()) 
                EditDelete(); 
            break; 
 
        case IDM_COPY: 
            EditCopy(); 
            break; 
 
        case IDM_PASTE: 
            EditPaste(); 
            break; 
 
        case IDM_DELETE: 
            EditDelete(); 
            break; 
 
        case IDM_EXIT: 
            DestroyWindow(hwnd); 
    } 
    break; 
```



<span data-ttu-id="9182a-151">Um die Befehle zum **Kopieren** und **Ausschneiden** auszuführen, ruft die Fenster Prozedur die Anwendungs definierte EditCopy-Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="9182a-151">To carry out the **Copy** and **Cut** commands, the window procedure calls the application-defined EditCopy function.</span></span> <span data-ttu-id="9182a-152">Weitere Informationen finden Sie unter [Kopieren von Informationen in die Zwischenablage](#copying-information-to-the-clipboard).</span><span class="sxs-lookup"><span data-stu-id="9182a-152">For more information, see [Copying Information to the Clipboard](#copying-information-to-the-clipboard).</span></span> <span data-ttu-id="9182a-153">Um den Befehl **Einfügen** auszuführen, ruft die Fenster Prozedur die Anwendungs definierte EditPaste-Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="9182a-153">To carry out the **Paste** command, the window procedure calls the application-defined EditPaste function.</span></span> <span data-ttu-id="9182a-154">Weitere Informationen zur EditPaste-Funktion finden Sie unter [Einfügen von Informationen aus der Zwischenablage](#pasting-information-from-the-clipboard).</span><span class="sxs-lookup"><span data-stu-id="9182a-154">For more information about the EditPaste function, see [Pasting Information from the Clipboard](#pasting-information-from-the-clipboard).</span></span>

### <a name="copying-information-to-the-clipboard"></a><span data-ttu-id="9182a-155">Kopieren von Informationen in die Zwischenablage</span><span class="sxs-lookup"><span data-stu-id="9182a-155">Copying Information to the Clipboard</span></span>

<span data-ttu-id="9182a-156">In der Label-Anwendung kopiert die von der Anwendung definierte EditCopy-Funktion die aktuelle Auswahl in die Zwischenablage.</span><span class="sxs-lookup"><span data-stu-id="9182a-156">In the Label application, the application-defined EditCopy function copies the current selection to the clipboard.</span></span> <span data-ttu-id="9182a-157">Diese Funktion führt Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="9182a-157">This function does the following:</span></span>

1.  <span data-ttu-id="9182a-158">Öffnet die Zwischenablage durch Aufrufen der [**OpenClipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="9182a-158">Opens the clipboard by calling the [**OpenClipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard) function.</span></span>
2.  <span data-ttu-id="9182a-159">Leert die Zwischenablage durch Aufrufen der [**EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="9182a-159">Empties the clipboard by calling the [**EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard) function.</span></span>
3.  <span data-ttu-id="9182a-160">Ruft die [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) -Funktion einmal für jedes Zwischenablage Format auf, das die Anwendung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="9182a-160">Calls the [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) function once for each clipboard format the application provides.</span></span>
4.  <span data-ttu-id="9182a-161">Schließt die Zwischenablage, indem die [**CloseClipboard**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard) -Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="9182a-161">Closes the clipboard by calling the [**CloseClipboard**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard) function.</span></span>

<span data-ttu-id="9182a-162">Abhängig von der aktuellen Auswahl kopiert die EditCopy-Funktion entweder einen Textbereich oder kopiert eine Anwendungs definierte Struktur, die eine ganze Bezeichnung darstellt.</span><span class="sxs-lookup"><span data-stu-id="9182a-162">Depending on the current selection, the EditCopy function either copies a range of text or copies an application-defined structure representing an entire label.</span></span> <span data-ttu-id="9182a-163">Die Struktur namens "LabelBox" ist wie folgt definiert.</span><span class="sxs-lookup"><span data-stu-id="9182a-163">The structure, called LABELBOX, is defined as follows.</span></span>


```
#define BOX_ELLIPSE  0 
#define BOX_RECT     1 
 
#define CCH_MAXLABEL 80 
#define CX_MARGIN    12 
 
typedef struct tagLABELBOX {  // box 
    RECT rcText;    // coordinates of rectangle containing text 
    BOOL fSelected; // TRUE if the label is selected 
    BOOL fEdit;     // TRUE if text is selected 
    int nType;      // rectangular or elliptical 
    int ichCaret;   // caret position 
    int ichSel;     // with ichCaret, delimits selection 
    int nXCaret;    // window position corresponding to ichCaret 
    int nXSel;      // window position corresponding to ichSel 
    int cchLabel;   // length of text in atchLabel 
    TCHAR atchLabel[CCH_MAXLABEL]; 
} LABELBOX, *PLABELBOX;
```



<span data-ttu-id="9182a-164">Im folgenden finden Sie die Funktion "EditCopy".</span><span class="sxs-lookup"><span data-stu-id="9182a-164">Following is the EditCopy function.</span></span>


```
BOOL WINAPI EditCopy(VOID) 
{ 
    PLABELBOX pbox; 
    LPTSTR  lptstrCopy; 
    HGLOBAL hglbCopy; 
    int ich1, ich2, cch; 
 
    if (hwndSelected == NULL) 
        return FALSE; 
 
    // Open the clipboard, and empty it. 
 
    if (!OpenClipboard(hwndMain)) 
        return FALSE; 
    EmptyClipboard(); 
 
    // Get a pointer to the structure for the selected label. 
 
    pbox = (PLABELBOX) GetWindowLong(hwndSelected, 0); 
 
    // If text is selected, copy it using the CF_TEXT format. 
 
    if (pbox->fEdit) 
    { 
        if (pbox->ichSel == pbox->ichCaret)     // zero length
        {   
            CloseClipboard();                   // selection 
            return FALSE; 
        } 
 
        if (pbox->ichSel < pbox->ichCaret) 
        { 
            ich1 = pbox->ichSel; 
            ich2 = pbox->ichCaret; 
        } 
        else 
        { 
            ich1 = pbox->ichCaret; 
            ich2 = pbox->ichSel; 
        } 
        cch = ich2 - ich1; 
 
        // Allocate a global memory object for the text. 
 
        hglbCopy = GlobalAlloc(GMEM_MOVEABLE, 
            (cch + 1) * sizeof(TCHAR)); 
        if (hglbCopy == NULL) 
        { 
            CloseClipboard(); 
            return FALSE; 
        } 
 
        // Lock the handle and copy the text to the buffer. 
 
        lptstrCopy = GlobalLock(hglbCopy); 
        memcpy(lptstrCopy, &pbox->atchLabel[ich1], 
            cch * sizeof(TCHAR)); 
        lptstrCopy[cch] = (TCHAR) 0;    // null character 
        GlobalUnlock(hglbCopy); 
 
        // Place the handle on the clipboard. 
 
        SetClipboardData(CF_TEXT, hglbCopy); 
    } 
 
    // If no text is selected, the label as a whole is copied. 
 
    else 
    { 
        // Save a copy of the selected label as a local memory 
        // object. This copy is used to render data on request. 
        // It is freed in response to the WM_DESTROYCLIPBOARD 
        // message. 
 
        pboxLocalClip = (PLABELBOX) LocalAlloc( 
            LMEM_FIXED, 
            sizeof(LABELBOX) 
        ); 
        if (pboxLocalClip == NULL) 
        { 
            CloseClipboard(); 
            return FALSE; 
        } 
        memcpy(pboxLocalClip, pbox, sizeof(LABELBOX)); 
        pboxLocalClip->fSelected = FALSE; 
        pboxLocalClip->fEdit = FALSE; 
 
        // Place a registered clipboard format, the owner-display 
        // format, and the CF_TEXT format on the clipboard using 
        // delayed rendering. 
 
        SetClipboardData(uLabelFormat, NULL); 
        SetClipboardData(CF_OWNERDISPLAY, NULL); 
        SetClipboardData(CF_TEXT, NULL); 
    } 
 
    // Close the clipboard. 
 
    CloseClipboard(); 
 
    return TRUE; 
}
```



### <a name="pasting-information-from-the-clipboard"></a><span data-ttu-id="9182a-165">Einfügen von Informationen aus der Zwischenablage</span><span class="sxs-lookup"><span data-stu-id="9182a-165">Pasting Information from the Clipboard</span></span>

<span data-ttu-id="9182a-166">In der Label-Anwendung fügt die von der Anwendung definierte EditPaste-Funktion den Inhalt der Zwischenablage ein.</span><span class="sxs-lookup"><span data-stu-id="9182a-166">In the Label application, the application-defined EditPaste function pastes the content of the clipboard.</span></span> <span data-ttu-id="9182a-167">Diese Funktion führt Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="9182a-167">This function does the following:</span></span>

1.  <span data-ttu-id="9182a-168">Öffnet die Zwischenablage durch Aufrufen der [**OpenClipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="9182a-168">Opens the clipboard by calling the [**OpenClipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard) function.</span></span>
2.  <span data-ttu-id="9182a-169">Bestimmt, welche der verfügbaren Zwischenablage Formate abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9182a-169">Determines which of the available clipboard formats to retrieve.</span></span>
3.  <span data-ttu-id="9182a-170">Ruft das Handle für die Daten im ausgewählten Format ab, indem die [**GetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata) -Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="9182a-170">Retrieves the handle to the data in the selected format by calling the [**GetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata) function.</span></span>
4.  <span data-ttu-id="9182a-171">Fügt eine Kopie der Daten in das Dokument ein.</span><span class="sxs-lookup"><span data-stu-id="9182a-171">Inserts a copy of the data into the document.</span></span>

    <span data-ttu-id="9182a-172">Das von [**GetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata) zurückgegebene Handle befindet sich immer noch im Besitz der Zwischenablage, sodass eine Anwendung Sie nicht freigeben oder gesperrt bleiben darf.</span><span class="sxs-lookup"><span data-stu-id="9182a-172">The handle returned by [**GetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata) is still owned by the clipboard, so an application must not free it or leave it locked.</span></span>

5.  <span data-ttu-id="9182a-173">Schließt die Zwischenablage, indem die [**CloseClipboard**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard) -Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="9182a-173">Closes the clipboard by calling the [**CloseClipboard**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard) function.</span></span>

<span data-ttu-id="9182a-174">Wenn eine Bezeichnung ausgewählt ist und eine Einfügemarke enthält, fügt die EditPaste-Funktion den Text aus der Zwischenablage an der Einfügemarke ein.</span><span class="sxs-lookup"><span data-stu-id="9182a-174">If a label is selected and contains an insertion point, the EditPaste function inserts the text from the clipboard at the insertion point.</span></span> <span data-ttu-id="9182a-175">Wenn keine Auswahl vorhanden ist oder eine Bezeichnung ausgewählt ist, erstellt die Funktion eine neue Bezeichnung und verwendet dabei die von der Anwendung definierte LabelBox-Struktur in der Zwischenablage.</span><span class="sxs-lookup"><span data-stu-id="9182a-175">If there is no selection or if a label is selected, the function creates a new label, using the application-defined LABELBOX structure on the clipboard.</span></span> <span data-ttu-id="9182a-176">Die LabelBox-Struktur wird mithilfe eines registrierten Zwischenablage Formats in der Zwischenablage platziert.</span><span class="sxs-lookup"><span data-stu-id="9182a-176">The LABELBOX structure is placed on the clipboard by using a registered clipboard format.</span></span>

<span data-ttu-id="9182a-177">Die Struktur namens "LabelBox" ist wie folgt definiert.</span><span class="sxs-lookup"><span data-stu-id="9182a-177">The structure, called LABELBOX, is defined as follows.</span></span>


```
#define BOX_ELLIPSE  0 
#define BOX_RECT     1 
 
#define CCH_MAXLABEL 80 
#define CX_MARGIN    12 
 
typedef struct tagLABELBOX {  // box 
    RECT rcText;    // coordinates of rectangle containing text 
    BOOL fSelected; // TRUE if the label is selected 
    BOOL fEdit;     // TRUE if text is selected 
    int nType;      // rectangular or elliptical 
    int ichCaret;   // caret position 
    int ichSel;     // with ichCaret, delimits selection 
    int nXCaret;    // window position corresponding to ichCaret 
    int nXSel;      // window position corresponding to ichSel 
    int cchLabel;   // length of text in atchLabel 
    TCHAR atchLabel[CCH_MAXLABEL]; 
} LABELBOX, *PLABELBOX;
```



<span data-ttu-id="9182a-178">Im folgenden finden Sie die EditPaste-Funktion.</span><span class="sxs-lookup"><span data-stu-id="9182a-178">Following is the EditPaste function.</span></span>


```
VOID WINAPI EditPaste(VOID) 
{ 
    PLABELBOX pbox; 
    HGLOBAL   hglb; 
    LPTSTR    lptstr; 
    PLABELBOX pboxCopy; 
    int cx, cy; 
    HWND hwnd; 
 
    pbox = hwndSelected == NULL ? NULL : 
        (PLABELBOX) GetWindowLong(hwndSelected, 0); 
 
    // If the application is in edit mode, 
    // get the clipboard text. 
 
    if (pbox != NULL && pbox->fEdit) 
    { 
        if (!IsClipboardFormatAvailable(CF_TEXT)) 
            return; 
        if (!OpenClipboard(hwndMain)) 
            return; 
 
        hglb = GetClipboardData(CF_TEXT); 
        if (hglb != NULL) 
        { 
            lptstr = GlobalLock(hglb); 
            if (lptstr != NULL) 
            { 
                // Call the application-defined ReplaceSelection 
                // function to insert the text and repaint the 
                // window. 
 
                ReplaceSelection(hwndSelected, pbox, lptstr); 
                GlobalUnlock(hglb); 
            } 
        } 
        CloseClipboard(); 
 
        return; 
    } 
 
    // If the application is not in edit mode, 
    // create a label window. 
 
    if (!IsClipboardFormatAvailable(uLabelFormat)) 
        return; 
    if (!OpenClipboard(hwndMain)) 
        return; 
 
    hglb = GetClipboardData(uLabelFormat); 
    if (hglb != NULL) 
    { 
        pboxCopy = GlobalLock(hglb); 
        if (pboxCopy != NULL) 
        { 
            cx = pboxCopy->rcText.right + CX_MARGIN; 
            cy = pboxCopy->rcText.top * 2 + cyText; 
 
            hwnd = CreateWindowEx( 
                WS_EX_NOPARENTNOTIFY | WS_EX_TRANSPARENT, 
                atchClassChild, NULL, WS_CHILD, 0, 0, cx, cy, 
                hwndMain, NULL, hinst, NULL 
            ); 
            if (hwnd != NULL) 
            { 
                pbox = (PLABELBOX) GetWindowLong(hwnd, 0); 
                memcpy(pbox, pboxCopy, sizeof(LABELBOX)); 
                ShowWindow(hwnd, SW_SHOWNORMAL); 
                SetFocus(hwnd); 
            } 
            GlobalUnlock(hglb); 
        } 
    } 
    CloseClipboard(); 
}
```



### <a name="registering-a-clipboard-format"></a><span data-ttu-id="9182a-179">Registrieren eines Zwischenablage Formats</span><span class="sxs-lookup"><span data-stu-id="9182a-179">Registering a Clipboard Format</span></span>

<span data-ttu-id="9182a-180">Fügen Sie zum Registrieren eines Zwischenablage Formats wie folgt einen aufzurufenden Befehl der [**RegisterClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) -Funktion zur instanzinitialisierungs Funktion Ihrer Anwendung hinzu.</span><span class="sxs-lookup"><span data-stu-id="9182a-180">To register a clipboard format, add a call to the [**RegisterClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) function to your application's instance initialization function, as follows.</span></span>


```
// Register a clipboard format. 
 
// We assume that atchTemp can contain the format name and
// a null-terminator, otherwise it is truncated.
//
LoadString(hinstCurrent, IDS_FORMATNAME, atchTemp, 
    sizeof(atchTemp)/sizeof(TCHAR)); 
uLabelFormat = RegisterClipboardFormat(atchTemp); 
if (uLabelFormat == 0) 
    return FALSE;
```



### <a name="processing-the-wm_renderformat-and-wm_renderallformats-messages"></a><span data-ttu-id="9182a-181">Verarbeiten der \_ Nachrichten "WM Renderformat" und "WM \_ renderallformats"</span><span class="sxs-lookup"><span data-stu-id="9182a-181">Processing the WM\_RENDERFORMAT and WM\_RENDERALLFORMATS Messages</span></span>

<span data-ttu-id="9182a-182">Wenn ein Fenster ein **null** -Handle an die [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) -Funktion übergibt, muss es die [**WM- \_ Renderformat**](wm-renderformat.md) -und [**WM- \_ renderallformats**](wm-renderallformats.md) -Nachrichten verarbeiten, um Daten auf Anforderung zu Rendering.</span><span class="sxs-lookup"><span data-stu-id="9182a-182">If a window passes a **NULL** handle to the [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) function, it must process the [**WM\_RENDERFORMAT**](wm-renderformat.md) and [**WM\_RENDERALLFORMATS**](wm-renderallformats.md) messages to render data upon request.</span></span>

<span data-ttu-id="9182a-183">Wenn ein Fenster das Rendern eines bestimmten Formats verzögert und dann eine andere Anwendung Daten in diesem Format anfordert, wird eine [**WM- \_ Renderformat**](wm-renderformat.md) -Meldung an das Fenster gesendet.</span><span class="sxs-lookup"><span data-stu-id="9182a-183">If a window delays rendering a specific format and then another application requests data in that format, then a [**WM\_RENDERFORMAT**](wm-renderformat.md) message is sent to the window.</span></span> <span data-ttu-id="9182a-184">Wenn ein Fenster außerdem das Rendern von einem oder mehreren Formaten verzögert und einige dieser Formate nicht gerendert bleiben, wenn das Fenster zerstört wird, wird eine WM- [**\_ renderallformats**](wm-renderallformats.md) -Nachricht vor deren Zerstörung an das Fenster gesendet.</span><span class="sxs-lookup"><span data-stu-id="9182a-184">In addition, if a window delays rendering one or more formats, and if some of those formats remain unrendered when the window is about to be destroyed, then a [**WM\_RENDERALLFORMATS**](wm-renderallformats.md) message is sent to the window before its destruction.</span></span>

<span data-ttu-id="9182a-185">Um ein Zwischenablage Format zu Renderen, sollte die Fenster Prozedur mithilfe der [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) -Funktion ein Daten handle ungleich **null** in der Zwischenablage platzieren.</span><span class="sxs-lookup"><span data-stu-id="9182a-185">To render a clipboard format, the window procedure should place a non-**NULL** data handle on the clipboard using the [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) function.</span></span> <span data-ttu-id="9182a-186">Wenn die Fenster Prozedur ein Format in Reaktion auf die WM- [**\_ Renderformat**](wm-renderformat.md) -Nachricht rendert, darf die Zwischenablage vor dem Aufrufen von **SetClipboardData** nicht geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="9182a-186">If the window procedure is rendering a format in response to the [**WM\_RENDERFORMAT**](wm-renderformat.md) message, it must not open the clipboard before calling **SetClipboardData**.</span></span> <span data-ttu-id="9182a-187">Wenn jedoch ein oder mehrere Formate als Antwort auf die [**WM- \_ renderallformats**](wm-renderallformats.md) -Nachricht gerendert werden, muss die Zwischenablage geöffnet werden, und es muss überprüft werden, ob das Fenster vor dem Aufrufen von **SetClipboardData** noch die Zwischenablage besitzt, und die Zwischenablage muss vor der Rückgabe geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="9182a-187">But if it is rendering one or more formats in response to the [**WM\_RENDERALLFORMATS**](wm-renderallformats.md) message, it must open the clipboard and check that the window still owns the clipboard before calling **SetClipboardData**, and it must close the clipboard before returning.</span></span>

<span data-ttu-id="9182a-188">Die Label-Anwendung verarbeitet die [**WM- \_ Renderformat**](wm-renderformat.md) -und [**WM- \_ renderallformats**](wm-renderallformats.md) -Meldungen wie folgt.</span><span class="sxs-lookup"><span data-stu-id="9182a-188">The Label application processes the [**WM\_RENDERFORMAT**](wm-renderformat.md) and [**WM\_RENDERALLFORMATS**](wm-renderallformats.md) messages as follows.</span></span>


```
case WM_RENDERFORMAT: 
    RenderFormat((UINT) wParam); 
    break; 
 
case WM_RENDERALLFORMATS:
    if (OpenClipboard(hwnd))
    {
        if (GetClipboardOwner() == hwnd)
        {
            RenderFormat(uLabelFormat);
            RenderFormat(CF_TEXT);
        }
        CloseClipboard();
    }
    break;
```



<span data-ttu-id="9182a-189">In beiden Fällen ruft die Fenster Prozedur die von der Anwendung definierte Renderformat-Funktion auf, die wie folgt definiert ist.</span><span class="sxs-lookup"><span data-stu-id="9182a-189">In both cases, the window procedure calls the application-defined RenderFormat function, defined as follows.</span></span>

<span data-ttu-id="9182a-190">Die Struktur namens "LabelBox" ist wie folgt definiert.</span><span class="sxs-lookup"><span data-stu-id="9182a-190">The structure, called LABELBOX, is defined as follows.</span></span>


```
#define BOX_ELLIPSE  0 
#define BOX_RECT     1 
 
#define CCH_MAXLABEL 80 
#define CX_MARGIN    12 
 
typedef struct tagLABELBOX {  // box 
    RECT rcText;    // coordinates of rectangle containing text 
    BOOL fSelected; // TRUE if the label is selected 
    BOOL fEdit;     // TRUE if text is selected 
    int nType;      // rectangular or elliptical 
    int ichCaret;   // caret position 
    int ichSel;     // with ichCaret, delimits selection 
    int nXCaret;    // window position corresponding to ichCaret 
    int nXSel;      // window position corresponding to ichSel 
    int cchLabel;   // length of text in atchLabel 
    TCHAR atchLabel[CCH_MAXLABEL]; 
} LABELBOX, *PLABELBOX;
```




```
void WINAPI RenderFormat(UINT uFormat) 
{ 
    HGLOBAL hglb; 
    PLABELBOX pbox; 
    LPTSTR  lptstr; 
    int cch; 
 
    if (pboxLocalClip == NULL) 
        return; 
 
    if (uFormat == CF_TEXT) 
    { 
        // Allocate a buffer for the text. 
 
        cch = pboxLocalClip->cchLabel; 
        hglb = GlobalAlloc(GMEM_MOVEABLE, 
            (cch + 1) * sizeof(TCHAR)); 
        if (hglb == NULL) 
            return; 
 
        // Copy the text from pboxLocalClip. 
 
        lptstr = GlobalLock(hglb); 
        memcpy(lptstr, pboxLocalClip->atchLabel, 
            cch * sizeof(TCHAR)); 
        lptstr[cch] = (TCHAR) 0; 
        GlobalUnlock(hglb); 
 
        // Place the handle on the clipboard. 
 
        SetClipboardData(CF_TEXT, hglb); 
    } 
    else if (uFormat == uLabelFormat) 
    { 
        hglb = GlobalAlloc(GMEM_MOVEABLE, sizeof(LABELBOX)); 
        if (hglb == NULL) 
            return; 
        pbox = GlobalLock(hglb); 
        memcpy(pbox, pboxLocalClip, sizeof(LABELBOX)); 
        GlobalUnlock(hglb); 
 
        SetClipboardData(uLabelFormat, hglb); 
    } 
}
```



### <a name="processing-the-wm_destroyclipboard-message"></a><span data-ttu-id="9182a-191">Verarbeiten der WM \_ destroyclipboard-Nachricht</span><span class="sxs-lookup"><span data-stu-id="9182a-191">Processing the WM\_DESTROYCLIPBOARD Message</span></span>

<span data-ttu-id="9182a-192">Die [**WM \_ destroyclipboard**](wm-destroyclipboard.md) -Nachricht kann von einem Fenster verarbeitet werden, um Ressourcen freizugeben, die für die Unterstützung des verzögerten Renderings reserviert wurden.</span><span class="sxs-lookup"><span data-stu-id="9182a-192">A window can process the [**WM\_DESTROYCLIPBOARD**](wm-destroyclipboard.md) message in order to free any resources that it set aside to support delayed rendering.</span></span> <span data-ttu-id="9182a-193">Beispielsweise weist die Bezeichnung Anwendung beim Kopieren einer Bezeichnung in die Zwischenablage ein lokales Speicher Objekt zu.</span><span class="sxs-lookup"><span data-stu-id="9182a-193">For example the Label application, when copying a label to the clipboard, allocates a local memory object.</span></span> <span data-ttu-id="9182a-194">Anschließend wird dieses Objekt in Reaktion auf die **WM \_ destroyclipboard** -Nachricht wie folgt freigegeben.</span><span class="sxs-lookup"><span data-stu-id="9182a-194">It then frees this object in response to the **WM\_DESTROYCLIPBOARD** message, as follows.</span></span>


```
case WM_DESTROYCLIPBOARD: 
    if (pboxLocalClip != NULL) 
    { 
        LocalFree(pboxLocalClip); 
        pboxLocalClip = NULL; 
    } 
    break;
```



### <a name="using-the-owner-display-clipboard-format"></a><span data-ttu-id="9182a-195">Verwenden des Owner-Display-Zwischenablage Formats</span><span class="sxs-lookup"><span data-stu-id="9182a-195">Using the Owner-Display Clipboard Format</span></span>

<span data-ttu-id="9182a-196">Wenn ein Fenster Informationen in der Zwischenablage mithilfe des CF-in-Zwischenablage Formats **\_ anzeigt** , muss es folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="9182a-196">If a window places information on the clipboard by using the **CF\_OWNERDISPLAY** clipboard format, it must do the following:</span></span>

-   <span data-ttu-id="9182a-197">Verarbeiten Sie die [**WM- \_ paintclipboard**](wm-paintclipboard.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="9182a-197">Process the [**WM\_PAINTCLIPBOARD**](wm-paintclipboard.md) message.</span></span> <span data-ttu-id="9182a-198">Diese Nachricht wird an den Besitzer der Zwischenablage gesendet, wenn ein Teil des Zwischenablage-Viewer-Fensters neu gezeichnet werden muss.</span><span class="sxs-lookup"><span data-stu-id="9182a-198">This message is sent to the clipboard owner when a portion of the clipboard viewer window must be repainted.</span></span>

-   <span data-ttu-id="9182a-199">Verarbeiten Sie die [**WM- \_ sizeclipboard**](wm-sizeclipboard.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="9182a-199">Process the [**WM\_SIZECLIPBOARD**](wm-sizeclipboard.md) message.</span></span> <span data-ttu-id="9182a-200">Diese Nachricht wird an den Besitzer der Zwischenablage gesendet, wenn die Größe des Fensters der Zwischenablage Anzeige geändert wurde oder sich der Inhalt geändert hat.</span><span class="sxs-lookup"><span data-stu-id="9182a-200">This message is sent to the clipboard owner when the clipboard viewer window has been resized or its content has changed.</span></span>

    <span data-ttu-id="9182a-201">In der Regel antwortet ein Fenster auf diese Meldung, indem die scrollpositionen und-Bereiche für das Fenster der Zwischenablage Anzeige festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="9182a-201">Typically, a window responds to this message by setting the scroll positions and ranges for the clipboard viewer window.</span></span> <span data-ttu-id="9182a-202">Als Antwort auf diese Nachricht aktualisiert die Bezeichnungs Anwendung auch eine [**Größen**](/previous-versions//dd145106(v=vs.85)) Struktur für das Fenster der Zwischenablage Anzeige.</span><span class="sxs-lookup"><span data-stu-id="9182a-202">In response to this message, the Label application also updates a [**SIZE**](/previous-versions//dd145106(v=vs.85)) structure for the clipboard viewer window.</span></span>

-   <span data-ttu-id="9182a-203">Verarbeiten Sie die Nachrichten " [**WM \_ hscrollclipboard**](wm-hscrollclipboard.md) " und " [**WM \_ vscrollclipboard**](wm-vscrollclipboard.md) ".</span><span class="sxs-lookup"><span data-stu-id="9182a-203">Process the [**WM\_HSCROLLCLIPBOARD**](wm-hscrollclipboard.md) and [**WM\_VSCROLLCLIPBOARD**](wm-vscrollclipboard.md) messages.</span></span> <span data-ttu-id="9182a-204">Diese Nachrichten werden an den Besitzer der Zwischenablage gesendet, wenn ein ScrollBar-Ereignis im Fenster der Zwischenablage Anzeige auftritt.</span><span class="sxs-lookup"><span data-stu-id="9182a-204">These messages are sent to the clipboard owner when a scroll bar event occurs in the clipboard viewer window.</span></span>

-   <span data-ttu-id="9182a-205">Verarbeiten Sie die [**WM- \_ askcbformatname**](wm-askcbformatname.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="9182a-205">Process the [**WM\_ASKCBFORMATNAME**](wm-askcbformatname.md) message.</span></span> <span data-ttu-id="9182a-206">Das Fenster der Zwischenablage Anzeige sendet diese Nachricht an eine Anwendung, um den Namen des Besitzer Anzeige Formats abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9182a-206">The clipboard viewer window sends this message to an application to retrieve the name of the owner-display format.</span></span>

<span data-ttu-id="9182a-207">Die Fenster Prozedur für die Bezeichnungs Anwendung verarbeitet diese Nachrichten wie folgt.</span><span class="sxs-lookup"><span data-stu-id="9182a-207">The window procedure for the Label application processes these messages, as follows.</span></span>


```
LRESULT CALLBACK MainWindowProc(hwnd, msg, wParam, lParam) 
HWND hwnd; 
UINT msg; 
WPARAM wParam; 
LPARAM lParam; 
{ 
    static RECT rcViewer; 
 
    RECT rc; 
    LPRECT lprc; 
    LPPAINTSTRUCT lpps; 
 
    switch (msg) 
    { 
        //
        // Handle other messages.
        //
        case WM_PAINTCLIPBOARD: 
            // Determine the dimensions of the label. 
 
            SetRect(&rc, 0, 0, 
                pboxLocalClip->rcText.right + CX_MARGIN, 
                pboxLocalClip->rcText.top * 2 + cyText 
            ); 
 
            // Center the image in the clipboard viewer window. 
 
            if (rc.right < rcViewer.right) 
            { 
                rc.left = (rcViewer.right - rc.right) / 2; 
                rc.right += rc.left; 
            } 
            if (rc.bottom < rcViewer.bottom) 
            { 
                rc.top = (rcViewer.bottom - rc.bottom) / 2; 
                rc.bottom += rc.top; 
            } 
 
            // Paint the image, using the specified PAINTSTRUCT 
            // structure, by calling the application-defined 
            // PaintLabel function. 
 
            lpps = (LPPAINTSTRUCT) GlobalLock((HGLOBAL) lParam); 
            PaintLabel(lpps, pboxLocalClip, &rc); 
            GlobalUnlock((HGLOBAL) lParam); 
            break; 
 
        case WM_SIZECLIPBOARD: 
            // Save the dimensions of the window in a static 
            // RECT structure. 
 
            lprc = (LPRECT) GlobalLock((HGLOBAL) lParam); 
            memcpy(&rcViewer, lprc, sizeof(RECT)); 
            GlobalUnlock((HGLOBAL) lParam); 
 
            // Set the scroll ranges to zero (thus eliminating 
            // the need to process the WM_HSCROLLCLIPBOARD and 
            // WM_VSCROLLCLIPBOARD messages). 
 
            SetScrollRange((HWND) wParam, SB_HORZ, 0, 0, TRUE); 
            SetScrollRange((HWND) wParam, SB_VERT, 0, 0, TRUE); 
 
            break; 
 
        case WM_ASKCBFORMATNAME: 
            LoadString(hinst, IDS_OWNERDISPLAY, 
                (LPSTR) lParam, wParam); 
            break; 
 
        default: 
            return DefWindowProc(hwnd, msg, wParam, lParam); 
    } 
    return 0; 
}
```



## <a name="monitoring-clipboard-contents"></a><span data-ttu-id="9182a-208">Überwachen der Zwischenablage</span><span class="sxs-lookup"><span data-stu-id="9182a-208">Monitoring Clipboard Contents</span></span>

<span data-ttu-id="9182a-209">Es gibt drei Möglichkeiten, Änderungen in der Zwischenablage zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="9182a-209">There are three ways of monitoring changes to the clipboard.</span></span> <span data-ttu-id="9182a-210">Die älteste Methode ist die Erstellung eines Zwischenablage-Viewer-Fensters.</span><span class="sxs-lookup"><span data-stu-id="9182a-210">The oldest method is to create a clipboard viewer window.</span></span> <span data-ttu-id="9182a-211">Windows 2000 hat die Möglichkeit hinzugefügt, die Sequenznummer der Zwischenablage abzufragen, und Windows Vista hat Unterstützung für die slistenslistener</span><span class="sxs-lookup"><span data-stu-id="9182a-211">Windows 2000 added the ability to query the clipboard sequence number, and Windows Vista added support for clipboard format listeners.</span></span> <span data-ttu-id="9182a-212">Zwischenablage-Viewer-Fenster werden aus Gründen der Abwärtskompatibilität mit früheren Versionen von Windows unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9182a-212">Clipboard viewer windows are supported for backward compatibility with earlier versions of Windows.</span></span> <span data-ttu-id="9182a-213">In neuen Programmen sollten slistenslistener oder die Sequenznummer der Zwischenablage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9182a-213">New programs should use clipboard format listeners or the clipboard sequence number.</span></span>

## <a name="querying-the-clipboard-sequence-number"></a><span data-ttu-id="9182a-214">Abfragen der Zwischenablage-Sequenznummer</span><span class="sxs-lookup"><span data-stu-id="9182a-214">Querying the Clipboard Sequence Number</span></span>

<span data-ttu-id="9182a-215">Bei jeder Änderung des Inhalts der Zwischenablage wird ein 32-Bit-Wert, der als Zwischenablage-Sequenznummer bezeichnet wird, inkrementiert.</span><span class="sxs-lookup"><span data-stu-id="9182a-215">Each time the contents of the clipboard change, a 32-bit value known as the clipboard sequence number is incremented.</span></span> <span data-ttu-id="9182a-216">Ein Programm kann die aktuelle Zwischenablage Sequenznummer abrufen, indem die [**getclipboardsequencenenumber**](/windows/desktop/api/Winuser/nf-winuser-getclipboardsequencenumber) -Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="9182a-216">A program can retrieve the current clipboard sequence number by calling the [**GetClipboardSequenceNumber**](/windows/desktop/api/Winuser/nf-winuser-getclipboardsequencenumber) function.</span></span> <span data-ttu-id="9182a-217">Durch Vergleichen des Werts, der mit einem Wert zurückgegeben wird, der von einem vorherigen Befehl an **getclipboardsequencenumber** zurückgegeben wurde, kann ein Programm bestimmen, ob der Inhalt der Zwischenablage geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="9182a-217">By comparing the value returned against a value returned by a previous call to **GetClipboardSequenceNumber**, a program can determine whether the clipboard contents have changed.</span></span> <span data-ttu-id="9182a-218">Diese Methode eignet sich besser für Programme, die Ergebnisse basierend auf dem aktuellen Zwischenablage Inhalt zwischenspeichern und wissen müssen, ob die Berechnungen noch gültig sind, bevor die Ergebnisse aus diesem Cache verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9182a-218">This method is more suitable to programs which cache results based on the current clipboard contents and need to know whether the calculations are still valid before using the results from that cache.</span></span> <span data-ttu-id="9182a-219">Beachten Sie, dass dies keine Benachrichtigungs Methode ist und nicht in einer Abruf Schleife verwendet werden sollte.</span><span class="sxs-lookup"><span data-stu-id="9182a-219">Note that this is a not a notification method and should not be used in a polling loop.</span></span> <span data-ttu-id="9182a-220">Wenn Sie benachrichtigt werden möchten, wenn sich der Inhalt der Zwischenablage ändert, verwenden Sie einen Zwischenablage-formatlistener oder einen</span><span class="sxs-lookup"><span data-stu-id="9182a-220">To be notified when clipboard contents change, use a clipboard format listener or a clipboard viewer.</span></span>

## <a name="creating-a-clipboard-format-listener"></a><span data-ttu-id="9182a-221">Erstellen eines-Zwischenablage-formatlistener</span><span class="sxs-lookup"><span data-stu-id="9182a-221">Creating a Clipboard Format Listener</span></span>

<span data-ttu-id="9182a-222">Ein Zwischenablage-formatlistener ist ein Fenster, das registriert wurde, um benachrichtigt zu werden, wenn sich der Inhalt der Zwischenablage geändert hat.</span><span class="sxs-lookup"><span data-stu-id="9182a-222">A clipboard format listener is a window which has registered to be notified when the contents of the clipboard has changed.</span></span> <span data-ttu-id="9182a-223">Diese Methode wird bei der Erstellung eines Zwischenablage-Viewer-Fensters empfohlen, da es einfacher ist, Probleme zu implementieren und zu vermeiden, wenn Programme die Zwischenablage-Viewer-Kette nicht ordnungsgemäß beibehalten können oder wenn ein Fenster in der Zwischenablage-Viewer-Kette nicht mehr auf</span><span class="sxs-lookup"><span data-stu-id="9182a-223">This method is recommended over creating a clipboard viewer window because it is simpler to implement and avoids problems if programs fail to maintain the clipboard viewer chain properly or if a window in the clipboard viewer chain stops responding to messages.</span></span>

<span data-ttu-id="9182a-224">Ein Fenster wird als Listener im Zwischenablage Format durch Aufrufen der [**addclipboardformatlistener**](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener) -Funktion registriert.</span><span class="sxs-lookup"><span data-stu-id="9182a-224">A window registers as a clipboard format listener by calling the [**AddClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener) function.</span></span> <span data-ttu-id="9182a-225">Wenn sich der Inhalt der Zwischenablage ändert, wird dem Fenster eine [**WM- \_ clipboardupdate**](wm-clipboardupdate.md) -Nachricht gesendet.</span><span class="sxs-lookup"><span data-stu-id="9182a-225">When the contents of the clipboard change, the window is posted a [**WM\_CLIPBOARDUPDATE**](wm-clipboardupdate.md) message.</span></span> <span data-ttu-id="9182a-226">Die Registrierung bleibt gültig, bis die Registrierung des Fensters durch Aufrufen der [**removeclipboardformatlistener**](/windows/desktop/api/Winuser/nf-winuser-removeclipboardformatlistener) -Funktion aufgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="9182a-226">The registration remains valid until the window unregister itself by calling the [**RemoveClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-removeclipboardformatlistener) function.</span></span>

## <a name="creating-a-clipboard-viewer-window"></a><span data-ttu-id="9182a-227">Erstellen eines Zwischenablage-Viewer-Fensters</span><span class="sxs-lookup"><span data-stu-id="9182a-227">Creating a Clipboard Viewer Window</span></span>

<span data-ttu-id="9182a-228">Ein Fenster der Zwischenablage Anzeige zeigt den aktuellen Inhalt der Zwischenablage an und empfängt Nachrichten, wenn der Inhalt der Zwischenablage geändert wird.</span><span class="sxs-lookup"><span data-stu-id="9182a-228">A clipboard viewer window displays the current content of the clipboard, and receives messages when the clipboard content changes.</span></span> <span data-ttu-id="9182a-229">Um ein Fenster für die Zwischenablage Anzeige zu erstellen, muss Ihre Anwendung folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="9182a-229">To create a clipboard viewer window, your application must do the following:</span></span>

-   <span data-ttu-id="9182a-230">Fügen Sie das Fenster der Zwischenablage-Viewer-Kette hinzu.</span><span class="sxs-lookup"><span data-stu-id="9182a-230">Add the window to the clipboard viewer chain.</span></span>
-   <span data-ttu-id="9182a-231">Verarbeiten Sie die Meldung " [**WM \_ CHANGECBCHAIN**](wm-changecbchain.md) ".</span><span class="sxs-lookup"><span data-stu-id="9182a-231">Process the [**WM\_CHANGECBCHAIN**](wm-changecbchain.md) message.</span></span>
-   <span data-ttu-id="9182a-232">Die [**WM- \_ drawclipboard**](wm-drawclipboard.md) -Nachricht verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="9182a-232">Process the [**WM\_DRAWCLIPBOARD**](wm-drawclipboard.md) message.</span></span>
-   <span data-ttu-id="9182a-233">Entfernen Sie das Fenster aus der Zwischenablage-Viewer-Kette, bevor es zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="9182a-233">Remove the window from the clipboard viewer chain before it is destroyed.</span></span>

## <a name="adding-a-window-to-the-clipboard-viewer-chain"></a><span data-ttu-id="9182a-234">Hinzufügen eines Fensters zur Zwischenablage-Viewer-Kette</span><span class="sxs-lookup"><span data-stu-id="9182a-234">Adding a Window to the Clipboard Viewer Chain</span></span>

<span data-ttu-id="9182a-235">Durch Aufrufen der [**setclipboardviewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) -Funktion wird ein Fenster zur Kette der Zwischenablage-Viewer hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9182a-235">A window adds itself to the clipboard viewer chain by calling the [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) function.</span></span> <span data-ttu-id="9182a-236">Der Rückgabewert ist das Handle für das nächste Fenster in der Kette.</span><span class="sxs-lookup"><span data-stu-id="9182a-236">The return value is the handle to the next window in the chain.</span></span> <span data-ttu-id="9182a-237">Ein Fenster muss diesen Wert nachverfolgen können, z. –. durch Speichern in einer statischen Variablen namens *hwndnextviewer*.</span><span class="sxs-lookup"><span data-stu-id="9182a-237">A window must keep track of this value — for example, by saving it in a static variable named *hwndNextViewer*.</span></span>

<span data-ttu-id="9182a-238">Im folgenden Beispiel wird der Kette der Zwischenablage-Viewer als Reaktion auf die [**WM \_ Create**](/windows/desktop/winmsg/wm-create) -Meldung ein Fenster hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9182a-238">The following example adds a window to the clipboard viewer chain in response to the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message.</span></span>


```
case WM_CREATE: 
 
    // Add the window to the clipboard viewer chain. 
 
    hwndNextViewer = SetClipboardViewer(hwnd); 
    break;
```



<span data-ttu-id="9182a-239">Code Ausschnitte werden für die folgenden Aufgaben angezeigt:</span><span class="sxs-lookup"><span data-stu-id="9182a-239">Code snippets are shown for the following tasks:</span></span>

-   [<span data-ttu-id="9182a-240">Verarbeiten der WM- \_ CHANGECBCHAIN-Nachricht</span><span class="sxs-lookup"><span data-stu-id="9182a-240">Processing the WM\_CHANGECBCHAIN Message</span></span>](/windows)
-   [<span data-ttu-id="9182a-241">Entfernen eines Fensters aus der Zwischenablage-Viewer-Kette</span><span class="sxs-lookup"><span data-stu-id="9182a-241">Removing a Window from the Clipboard Viewer Chain</span></span>](#removing-a-window-from-the-clipboard-viewer-chain)
-   [<span data-ttu-id="9182a-242">Die WM- \_ drawclipboard-Nachricht wird verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="9182a-242">Processing the WM\_DRAWCLIPBOARD Message</span></span>](/windows)
-   [<span data-ttu-id="9182a-243">Beispiel für einen Zwischenablage-Viewer</span><span class="sxs-lookup"><span data-stu-id="9182a-243">Example of a Clipboard Viewer</span></span>](#example-of-a-clipboard-viewer)

### <a name="processing-the-wm_changecbchain-message"></a><span data-ttu-id="9182a-244">Verarbeiten der WM- \_ CHANGECBCHAIN-Nachricht</span><span class="sxs-lookup"><span data-stu-id="9182a-244">Processing the WM\_CHANGECBCHAIN Message</span></span>

<span data-ttu-id="9182a-245">Ein Fenster der Zwischenablage Anzeige empfängt die [**WM- \_ CHANGECBCHAIN**](wm-changecbchain.md) -Nachricht, wenn sich ein anderes Fenster selbst aus der Zwischenablage-Viewer-Kette entfernt.</span><span class="sxs-lookup"><span data-stu-id="9182a-245">A clipboard viewer window receives the [**WM\_CHANGECBCHAIN**](wm-changecbchain.md) message when another window is removing itself from the clipboard viewer chain.</span></span> <span data-ttu-id="9182a-246">Wenn das zu entfernende Fenster das nächste Fenster in der Kette ist, muss das Fenster, in dem die Meldung empfangen wird, die Verknüpfung des nächsten Fensters von der Kette aufheben.</span><span class="sxs-lookup"><span data-stu-id="9182a-246">If the window being removed is the next window in the chain, the window receiving the message must unlink the next window from the chain.</span></span> <span data-ttu-id="9182a-247">Andernfalls sollte diese Nachricht an das nächste Fenster in der Kette weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="9182a-247">Otherwise, this message should be passed to the next window in the chain.</span></span>

<span data-ttu-id="9182a-248">Das folgende Beispiel zeigt die Verarbeitung der [**WM- \_ CHANGECBCHAIN**](wm-changecbchain.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="9182a-248">The following example shows the processing of the [**WM\_CHANGECBCHAIN**](wm-changecbchain.md) message.</span></span>


```
case WM_CHANGECBCHAIN: 
 
    // If the next window is closing, repair the chain. 
 
    if ((HWND) wParam == hwndNextViewer) 
        hwndNextViewer = (HWND) lParam; 
 
    // Otherwise, pass the message to the next link. 
 
    else if (hwndNextViewer != NULL) 
        SendMessage(hwndNextViewer, uMsg, wParam, lParam); 
 
    break;
```



### <a name="removing-a-window-from-the-clipboard-viewer-chain"></a><span data-ttu-id="9182a-249">Entfernen eines Fensters aus der Zwischenablage-Viewer-Kette</span><span class="sxs-lookup"><span data-stu-id="9182a-249">Removing a Window from the Clipboard Viewer Chain</span></span>

<span data-ttu-id="9182a-250">Um sich selbst aus der Zwischenablage-Viewer-Kette zu entfernen, Ruft ein Fenster die [**changeclipboardchain**](/windows/desktop/api/Winuser/nf-winuser-changeclipboardchain) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="9182a-250">To remove itself from the clipboard viewer chain, a window calls the [**ChangeClipboardChain**](/windows/desktop/api/Winuser/nf-winuser-changeclipboardchain) function.</span></span> <span data-ttu-id="9182a-251">Im folgenden Beispiel wird ein Fenster aus der Kette der Zwischenablage-Viewer als Antwort auf die WM-Lösch Nachricht entfernt. [**\_**](/windows/desktop/winmsg/wm-destroy)</span><span class="sxs-lookup"><span data-stu-id="9182a-251">The following example removes a window from the clipboard viewer chain in response to the [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message.</span></span>


```
case WM_DESTROY: 
    ChangeClipboardChain(hwnd, hwndNextViewer); 
    PostQuitMessage(0); 
    break;
```



### <a name="processing-the-wm_drawclipboard-message"></a><span data-ttu-id="9182a-252">Die WM- \_ drawclipboard-Nachricht wird verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="9182a-252">Processing the WM\_DRAWCLIPBOARD Message</span></span>

<span data-ttu-id="9182a-253">Die " [**WM \_ drawclipboard**](wm-drawclipboard.md) "-Meldung benachrichtigt das Fenster der Zwischenablage-Viewer, dass sich der Inhalt der Zwischenablage geändert hat.</span><span class="sxs-lookup"><span data-stu-id="9182a-253">The [**WM\_DRAWCLIPBOARD**](wm-drawclipboard.md) message notifies a clipboard viewer window that the content of the clipboard has changed.</span></span> <span data-ttu-id="9182a-254">Bei der Verarbeitung der **WM- \_ drawclipboard** -Nachricht sollte ein Fenster folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="9182a-254">A window should do the following when processing the **WM\_DRAWCLIPBOARD** message:</span></span>

1.  <span data-ttu-id="9182a-255">Bestimmen Sie, welches der verfügbaren Zwischenablage Formate angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9182a-255">Determine which of the available clipboard formats to display.</span></span>
2.  <span data-ttu-id="9182a-256">Rufen Sie die Zwischenablage Daten ab, und zeigen Sie Sie im Fenster an.</span><span class="sxs-lookup"><span data-stu-id="9182a-256">Retrieve the clipboard data and display it in the window.</span></span> <span data-ttu-id="9182a-257">Oder wenn das Zwischenablage Format **CF \_**-Besitzer Anzeige ist, senden Sie eine " [**WM \_ paintclipboard**](wm-paintclipboard.md) "-Meldung an den Besitzer der Zwischenablage.</span><span class="sxs-lookup"><span data-stu-id="9182a-257">Or if the clipboard format is **CF\_OWNERDISPLAY**, send a [**WM\_PAINTCLIPBOARD**](wm-paintclipboard.md) message to the clipboard owner.</span></span>
3.  <span data-ttu-id="9182a-258">Sendet die Nachricht an das nächste Fenster in der Kette der Zwischenablage-Viewer.</span><span class="sxs-lookup"><span data-stu-id="9182a-258">Send the message to the next window in the clipboard viewer chain.</span></span>

<span data-ttu-id="9182a-259">Ein Beispiel für die Verarbeitung der " [**WM \_ drawclipboard**](wm-drawclipboard.md) "-Nachricht finden Sie in der Beispiel Auflistung im [Beispiel eines Zwischenablage-Viewers](#example-of-a-clipboard-viewer).</span><span class="sxs-lookup"><span data-stu-id="9182a-259">For an example of processing the [**WM\_DRAWCLIPBOARD**](wm-drawclipboard.md) message, see the example listing in [Example of a Clipboard Viewer](#example-of-a-clipboard-viewer).</span></span>

### <a name="example-of-a-clipboard-viewer"></a><span data-ttu-id="9182a-260">Beispiel für einen Zwischenablage-Viewer</span><span class="sxs-lookup"><span data-stu-id="9182a-260">Example of a Clipboard Viewer</span></span>

<span data-ttu-id="9182a-261">Das folgende Beispiel zeigt eine einfache Anwendung der Zwischenablage Anzeige.</span><span class="sxs-lookup"><span data-stu-id="9182a-261">The following example shows a simple clipboard viewer application.</span></span>


```
HINSTANCE hinst; 
UINT uFormat = (UINT)(-1); 
BOOL fAuto = TRUE; 
 
LRESULT APIENTRY MainWndProc(hwnd, uMsg, wParam, lParam) 
HWND hwnd; 
UINT uMsg; 
WPARAM wParam; 
LPARAM lParam; 
{ 
    static HWND hwndNextViewer; 
 
    HDC hdc; 
    HDC hdcMem; 
    PAINTSTRUCT ps; 
    LPPAINTSTRUCT lpps; 
    RECT rc; 
    LPRECT lprc; 
    HGLOBAL hglb; 
    LPSTR lpstr; 
    HBITMAP hbm; 
    HENHMETAFILE hemf; 
    HWND hwndOwner; 
 
    switch (uMsg) 
    { 
        case WM_PAINT: 
            hdc = BeginPaint(hwnd, &ps); 
 
            // Branch depending on the clipboard format. 
 
            switch (uFormat) 
            { 
                case CF_OWNERDISPLAY: 
                    hwndOwner = GetClipboardOwner(); 
                    hglb = GlobalAlloc(GMEM_MOVEABLE, 
                        sizeof(PAINTSTRUCT)); 
                    lpps = GlobalLock(hglb);
                    memcpy(lpps, &ps, sizeof(PAINTSTRUCT)); 
                    GlobalUnlock(hglb); 
 
                    SendMessage(hwndOwner, WM_PAINTCLIPBOARD, 
                        (WPARAM) hwnd, (LPARAM) hglb); 
 
                    GlobalFree(hglb); 
                    break; 
 
                case CF_BITMAP: 
                    hdcMem = CreateCompatibleDC(hdc); 
                    if (hdcMem != NULL) 
                    { 
                        if (OpenClipboard(hwnd)) 
                        { 
                            hbm = (HBITMAP) 
                                GetClipboardData(uFormat); 
                            SelectObject(hdcMem, hbm); 
                            GetClientRect(hwnd, &rc); 
 
                            BitBlt(hdc, 0, 0, rc.right, rc.bottom, 
                                hdcMem, 0, 0, SRCCOPY); 
                            CloseClipboard(); 
                        } 
                        DeleteDC(hdcMem); 
                    } 
                    break; 
 
                case CF_TEXT: 
                    if (OpenClipboard(hwnd)) 
                    { 
                        hglb = GetClipboardData(uFormat); 
                        lpstr = GlobalLock(hglb); 
 
                        GetClientRect(hwnd, &rc); 
                        DrawText(hdc, lpstr, -1, &rc, DT_LEFT); 
 
                        GlobalUnlock(hglb); 
                        CloseClipboard(); 
                    } 
                    break; 
 
                case CF_ENHMETAFILE: 
                    if (OpenClipboard(hwnd)) 
                    { 
                        hemf = GetClipboardData(uFormat); 
                        GetClientRect(hwnd, &rc); 
                        PlayEnhMetaFile(hdc, hemf, &rc); 
                        CloseClipboard(); 
                    } 
                    break; 
 
                case 0: 
                    GetClientRect(hwnd, &rc); 
                    DrawText(hdc, "The clipboard is empty.", -1, 
                        &rc, DT_CENTER | DT_SINGLELINE | 
                        DT_VCENTER); 
                    break; 
 
                default: 
                    GetClientRect(hwnd, &rc); 
                    DrawText(hdc, "Unable to display format.", -1, 
                        &rc, DT_CENTER | DT_SINGLELINE | 
                        DT_VCENTER); 
            } 
            EndPaint(hwnd, &ps); 
            break; 
 
        case WM_SIZE: 
            if (uFormat == CF_OWNERDISPLAY) 
            { 
                hwndOwner = GetClipboardOwner(); 
                hglb = GlobalAlloc(GMEM_MOVEABLE, sizeof(RECT)); 
                lprc = GlobalLock(hglb); 
                GetClientRect(hwnd, lprc); 
                GlobalUnlock(hglb); 
 
                SendMessage(hwndOwner, WM_SIZECLIPBOARD, 
                    (WPARAM) hwnd, (LPARAM) hglb); 
 
                GlobalFree(hglb); 
            } 
            break; 
 
        case WM_CREATE: 
 
            // Add the window to the clipboard viewer chain. 
 
            hwndNextViewer = SetClipboardViewer(hwnd); 
            break; 
 
        case WM_CHANGECBCHAIN: 
 
            // If the next window is closing, repair the chain. 
 
            if ((HWND) wParam == hwndNextViewer) 
                hwndNextViewer = (HWND) lParam; 
 
            // Otherwise, pass the message to the next link. 
 
            else if (hwndNextViewer != NULL) 
                SendMessage(hwndNextViewer, uMsg, wParam, lParam); 
 
            break; 
 
        case WM_DESTROY: 
            ChangeClipboardChain(hwnd, hwndNextViewer); 
            PostQuitMessage(0); 
            break; 
 
        case WM_DRAWCLIPBOARD:  // clipboard contents changed. 
 
            // Update the window by using Auto clipboard format. 
 
            SetAutoView(hwnd); 
 
            // Pass the message to the next window in clipboard 
            // viewer chain. 
 
            SendMessage(hwndNextViewer, uMsg, wParam, lParam); 
            break; 
 
        case WM_INITMENUPOPUP: 
            if (!HIWORD(lParam)) 
                InitMenu(hwnd, (HMENU) wParam); 
            break; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDM_EXIT: 
                    DestroyWindow(hwnd); 
                    break; 
 
                case IDM_AUTO: 
                    SetAutoView(hwnd); 
                    break; 
 
                default: 
                    fAuto = FALSE; 
                    uFormat = LOWORD(wParam); 
                    InvalidateRect(hwnd, NULL, TRUE); 
            } 
            break; 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return (LRESULT) NULL; 
} 
 
void WINAPI SetAutoView(HWND hwnd) 
{ 
    static UINT auPriorityList[] = { 
        CF_OWNERDISPLAY, 
        CF_TEXT, 
        CF_ENHMETAFILE, 
        CF_BITMAP 
    }; 
 
    uFormat = GetPriorityClipboardFormat(auPriorityList, 4); 
    fAuto = TRUE; 
 
    InvalidateRect(hwnd, NULL, TRUE); 
    UpdateWindow(hwnd); 
} 
 
void WINAPI InitMenu(HWND hwnd, HMENU hmenu) 
{ 
    UINT uFormat; 
    char szFormatName[80]; 
    LPCSTR lpFormatName; 
    UINT fuFlags; 
    UINT idMenuItem; 
 
    // If a menu is not the display menu, no initialization is necessary. 
 
    if (GetMenuItemID(hmenu, 0) != IDM_AUTO) 
        return; 
 
    // Delete all menu items except the first. 
 
    while (GetMenuItemCount(hmenu) > 1) 
        DeleteMenu(hmenu, 1, MF_BYPOSITION); 
 
    // Check or uncheck the Auto menu item. 
 
    fuFlags = fAuto ? MF_BYCOMMAND | MF_CHECKED : 
        MF_BYCOMMAND | MF_UNCHECKED; 
    CheckMenuItem(hmenu, IDM_AUTO, fuFlags); 
 
    // If there are no clipboard formats, return. 
 
    if (CountClipboardFormats() == 0) 
        return; 
 
    // Open the clipboard. 
 
    if (!OpenClipboard(hwnd)) 
        return; 
 
    // Add a separator and then a menu item for each format. 
 
    AppendMenu(hmenu, MF_SEPARATOR, 0, NULL); 
    uFormat = EnumClipboardFormats(0); 
 
    while (uFormat) 
    { 
        // Call an application-defined function to get the name 
        // of the clipboard format. 
 
        lpFormatName = GetPredefinedClipboardFormatName(uFormat); 
 
        // For registered formats, get the registered name. 
 
        if (lpFormatName == NULL) 
        {

        // Note that, if the format name is larger than the
        // buffer, it is truncated. 
            if (GetClipboardFormatName(uFormat, szFormatName, 
                    sizeof(szFormatName))) 
                lpFormatName = szFormatName; 
            else 
                lpFormatName = "(unknown)"; 
        } 
 
        // Add a menu item for the format. For displayable 
        // formats, use the format ID for the menu ID. 
 
        if (IsDisplayableFormat(uFormat)) 
        { 
            fuFlags = MF_STRING; 
            idMenuItem = uFormat; 
        } 
        else 
        { 
            fuFlags = MF_STRING | MF_GRAYED; 
            idMenuItem = 0; 
        } 
        AppendMenu(hmenu, fuFlags, idMenuItem, lpFormatName); 
 
        uFormat = EnumClipboardFormats(uFormat); 
    } 
    CloseClipboard(); 
 
} 
 
BOOL WINAPI IsDisplayableFormat(UINT uFormat) 
{ 
    switch (uFormat) 
    { 
        case CF_OWNERDISPLAY: 
        case CF_TEXT: 
        case CF_ENHMETAFILE: 
        case CF_BITMAP: 
            return TRUE; 
    } 
    return FALSE; 
} 
```



 

 