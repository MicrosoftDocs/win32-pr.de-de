---
title: Verwenden von Dialog Feldern
description: Mithilfe von Dialogfeldern können Sie Informationen anzeigen und Eingabeaufforderung für den Benutzer eingeben.
ms.assetid: 8a5b6bdd-4429-4f48-b846-6bd617a87abf
keywords:
- Windows-Benutzeroberfläche, Fenster
- Windows-Benutzeroberfläche, Dialogfelder
- Fenster, Dialogfelder
- Dialogfelder, Info
- Dialogfelder, anzeigen
- Modale Dialogfelder
- Nicht modale Dialogfelder
- Dialogfelder, Modal
- Dialogfelder, ohne Modell
- Dialogfelder, initialisieren
- Dialogfeld Vorlagen
- Dialogfelder, Vorlagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21da47d7d59f4cadc21314566bce41a9ef3456a7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039419"
---
# <a name="using-dialog-boxes"></a><span data-ttu-id="b846b-115">Verwenden von Dialog Feldern</span><span class="sxs-lookup"><span data-stu-id="b846b-115">Using Dialog Boxes</span></span>

<span data-ttu-id="b846b-116">Mithilfe von Dialogfeldern können Sie Informationen anzeigen und Eingabeaufforderung für den Benutzer eingeben.</span><span class="sxs-lookup"><span data-stu-id="b846b-116">You use dialog boxes to display information and prompt for input from the user.</span></span> <span data-ttu-id="b846b-117">Die Anwendung lädt und initialisiert das Dialogfeld, verarbeitet Benutzereingaben und zerstört das Dialogfeld, wenn der Benutzer die Aufgabe beendet.</span><span class="sxs-lookup"><span data-stu-id="b846b-117">Your application loads and initializes the dialog box, processes user input, and destroys the dialog box when the user finishes the task.</span></span> <span data-ttu-id="b846b-118">Der Prozess für die Behandlung von Dialogfeldern variiert abhängig davon, ob das Dialogfeld modal oder nicht modelliert ist.</span><span class="sxs-lookup"><span data-stu-id="b846b-118">The process for handling dialog boxes varies, depending on whether the dialog box is modal or modeless.</span></span> <span data-ttu-id="b846b-119">Ein modales Dialogfeld erfordert, dass der Benutzer das Dialogfeld schließt, bevor ein anderes Fenster in der Anwendung aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="b846b-119">A modal dialog box requires the user to close the dialog box before activating another window in the application.</span></span> <span data-ttu-id="b846b-120">Der Benutzer kann jedoch Fenster in verschiedenen Anwendungen aktivieren.</span><span class="sxs-lookup"><span data-stu-id="b846b-120">However, the user can activate windows in different applications.</span></span> <span data-ttu-id="b846b-121">Ein nicht modalem Dialogfeld erfordert keine sofortige Antwort vom Benutzer.</span><span class="sxs-lookup"><span data-stu-id="b846b-121">A modeless dialog box does not require an immediate response from the user.</span></span> <span data-ttu-id="b846b-122">Es ähnelt einem Hauptfenster, das-Steuerelemente enthält.</span><span class="sxs-lookup"><span data-stu-id="b846b-122">It is similar to a main window containing controls.</span></span>

<span data-ttu-id="b846b-123">In den folgenden Abschnitten wird erläutert, wie beide Arten von Dialogfeldern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b846b-123">The following sections discuss how to use both types of dialog boxes.</span></span>

-   [<span data-ttu-id="b846b-124">Anzeigen eines Meldungs Felds</span><span class="sxs-lookup"><span data-stu-id="b846b-124">Displaying a Message Box</span></span>](#displaying-a-message-box)
-   [<span data-ttu-id="b846b-125">Erstellen eines modalen Dialog Felds</span><span class="sxs-lookup"><span data-stu-id="b846b-125">Creating a Modal Dialog Box</span></span>](#creating-a-modal-dialog-box)
-   [<span data-ttu-id="b846b-126">Erstellen eines nicht modalem Dialog Felds</span><span class="sxs-lookup"><span data-stu-id="b846b-126">Creating a Modeless Dialog Box</span></span>](#creating-a-modeless-dialog-box)
-   [<span data-ttu-id="b846b-127">Initialisieren eines Dialog Felds</span><span class="sxs-lookup"><span data-stu-id="b846b-127">Initializing a Dialog Box</span></span>](#initializing-a-dialog-box)
-   [<span data-ttu-id="b846b-128">Erstellen einer Vorlage im Speicher</span><span class="sxs-lookup"><span data-stu-id="b846b-128">Creating a Template in Memory</span></span>](#creating-a-template-in-memory)

## <a name="displaying-a-message-box"></a><span data-ttu-id="b846b-129">Anzeigen eines Meldungs Felds</span><span class="sxs-lookup"><span data-stu-id="b846b-129">Displaying a Message Box</span></span>

<span data-ttu-id="b846b-130">Die einfachste Form eines modalen Dialog Felds ist das Meldungs Feld.</span><span class="sxs-lookup"><span data-stu-id="b846b-130">The simplest form of modal dialog box is the message box.</span></span> <span data-ttu-id="b846b-131">Die meisten Anwendungen verwenden Meldungs Felder, um den Fehler des Benutzers zu warnen und Anweisungen einzugeben, wie nach einem Fehler fortgefahren werden kann.</span><span class="sxs-lookup"><span data-stu-id="b846b-131">Most applications use message boxes to warn the user of errors and to prompt for directions on how to proceed after an error has occurred.</span></span> <span data-ttu-id="b846b-132">Sie erstellen ein Meldungs Feld mit der [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) -Funktion oder der [**messageboxex**](/windows/desktop/api/Winuser/nf-winuser-messageboxexa) -Funktion, indem Sie die Meldung sowie die Anzahl und den Typ der anzuzeigenden Schaltflächen angeben.</span><span class="sxs-lookup"><span data-stu-id="b846b-132">You create a message box by using the [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) or [**MessageBoxEx**](/windows/desktop/api/Winuser/nf-winuser-messageboxexa) function, specifying the message and the number and type of buttons to display.</span></span> <span data-ttu-id="b846b-133">Das System erstellt ein modales Dialogfeld, das eine eigene Dialogfeld Vorlage und eine eigene Prozedur bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="b846b-133">The system creates a modal dialog box, providing its own dialog box template and procedure.</span></span> <span data-ttu-id="b846b-134">Nachdem der Benutzer das Meldungs Feld geschlossen hat, gibt **MessageBox** oder **messageboxex** einen Wert zurück, der die Schaltfläche identifiziert, die der Benutzer zum Schließen des Meldungs Felds ausgewählt hat.</span><span class="sxs-lookup"><span data-stu-id="b846b-134">After the user closes the message box, **MessageBox** or **MessageBoxEx** returns a value identifying the button chosen by the user to close the message box.</span></span>

<span data-ttu-id="b846b-135">Im folgenden Beispiel zeigt die Anwendung ein Meldungs Feld an, das den Benutzer zur Eingabe einer Aktion auffordert, nachdem ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="b846b-135">In the following example, the application displays a message box that prompts the user for an action after an error condition has occurred.</span></span> <span data-ttu-id="b846b-136">Im Meldungs Feld wird die Meldung angezeigt, in der der Fehlerzustand und die Lösung beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="b846b-136">The message box displays the message that describes the error condition and how to resolve it.</span></span> <span data-ttu-id="b846b-137">Das Format **MB \_ YesNo** weist [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) an, zwei Schaltflächen bereitzustellen, mit denen der Benutzer auswählen kann, wie der Vorgang fortgesetzt werden soll:</span><span class="sxs-lookup"><span data-stu-id="b846b-137">The **MB\_YESNO** style directs [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) to provide two buttons with which the user can choose how to proceed:</span></span>


```
int DisplayConfirmSaveAsMessageBox()
{
    int msgboxID = MessageBox(
        NULL,
        L"temp.txt already exists.\nDo you want to replace it?",
        L"Confirm Save As",
        MB_ICONEXCLAMATION | MB_YESNO
    );

    if (msgboxID == IDYES)
    {
        // TODO: add code
    }

    return msgboxID;    
}
```



<span data-ttu-id="b846b-138">Die folgende Abbildung zeigt die Ausgabe des vorangehenden Code Beispiels:</span><span class="sxs-lookup"><span data-stu-id="b846b-138">The following image shows the output from the preceding code example:</span></span>

![Meldungs Feld](images/messagebox-01.png)

## <a name="creating-a-modal-dialog-box"></a><span data-ttu-id="b846b-140">Erstellen eines modalen Dialog Felds</span><span class="sxs-lookup"><span data-stu-id="b846b-140">Creating a Modal Dialog Box</span></span>

<span data-ttu-id="b846b-141">Sie erstellen ein modales Dialogfeld mit der Funktion [**Dialogbox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) .</span><span class="sxs-lookup"><span data-stu-id="b846b-141">You create a modal dialog box by using the [**DialogBox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) function.</span></span> <span data-ttu-id="b846b-142">Sie müssen den Bezeichner oder den Namen einer Dialogfeld Vorlagen-Ressource und einen Zeiger auf die Dialogfeld Prozedur angeben.</span><span class="sxs-lookup"><span data-stu-id="b846b-142">You must specify the identifier or name of a dialog box template resource and a pointer to the dialog box procedure.</span></span> <span data-ttu-id="b846b-143">Die Funktion **Dialogbox** lädt die Vorlage, zeigt das Dialogfeld an und verarbeitet alle Benutzereingaben, bis der Benutzer das Dialogfeld schließt.</span><span class="sxs-lookup"><span data-stu-id="b846b-143">The **DialogBox** function loads the template, displays the dialog box, and processes all user input until the user closes the dialog box.</span></span>

<span data-ttu-id="b846b-144">Im folgenden Beispiel zeigt die Anwendung ein modales Dialogfeld an, wenn der Benutzer im Anwendungsmenü auf **Element löschen** klickt.</span><span class="sxs-lookup"><span data-stu-id="b846b-144">In the following example, the application displays a modal dialog box when the user clicks **Delete Item** from an application menu.</span></span> <span data-ttu-id="b846b-145">Das Dialogfeld enthält ein Bearbeitungs Steuerelement (in dem der Benutzer den Namen eines Elements eingibt) und die Schaltflächen " **OK** " und " **Abbrechen** ".</span><span class="sxs-lookup"><span data-stu-id="b846b-145">The dialog box contains an edit control (in which the user enters the name of an item) and **OK** and **Cancel** buttons.</span></span> <span data-ttu-id="b846b-146">Die Steuerelement Bezeichner für diese Steuerelemente sind ID \_ ItemName, IDOK bzw. IDCANCEL.</span><span class="sxs-lookup"><span data-stu-id="b846b-146">The control identifiers for these controls are ID\_ITEMNAME, IDOK, and IDCANCEL, respectively.</span></span>

<span data-ttu-id="b846b-147">Der erste Teil des Beispiels besteht aus den Anweisungen, die das modale Dialogfeld erstellen.</span><span class="sxs-lookup"><span data-stu-id="b846b-147">The first part of the example consists of the statements that create the modal dialog box.</span></span> <span data-ttu-id="b846b-148">Diese Anweisungen erstellen Sie in der Fenster Prozedur für das Hauptfenster der Anwendung das Dialogfeld, wenn das System eine [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Nachricht mit dem IDM \_ DeleteItem-Menü Bezeichner empfängt.</span><span class="sxs-lookup"><span data-stu-id="b846b-148">These statements, in the window procedure for the application's main window, create the dialog box when the system receives a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message having the IDM\_DELETEITEM menu identifier.</span></span> <span data-ttu-id="b846b-149">Der zweite Teil des Beispiels ist die Dialogfeld Prozedur, die den Inhalt des Bearbeitungs Steuer Elements abruft und das Dialogfeld nach dem Empfang einer **WM- \_ Befehls** Meldung schließt.</span><span class="sxs-lookup"><span data-stu-id="b846b-149">The second part of the example is the dialog box procedure, which retrieves the contents of the edit control and closes the dialog box upon receiving a **WM\_COMMAND** message.</span></span>

<span data-ttu-id="b846b-150">Die folgenden Anweisungen erstellen das modale Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="b846b-150">The following statements create the modal dialog box.</span></span> <span data-ttu-id="b846b-151">Die Dialogfeld Vorlage ist eine Ressource in der ausführbaren Datei der Anwendung und verfügt über den Ressourcen Bezeichner DLG \_ DeleteItem.</span><span class="sxs-lookup"><span data-stu-id="b846b-151">The dialog box template is a resource in the application's executable file and has the resource identifier DLG\_DELETEITEM.</span></span>


```
case WM_COMMAND: 
    switch (LOWORD(wParam)) 
    { 
        case IDM_DELETEITEM: 
            if (DialogBox(hinst, 
                          MAKEINTRESOURCE(DLG_DELETEITEM), 
                          hwnd, 
                          (DLGPROC)DeleteItemProc)==IDOK) 
            {
                // Complete the command; szItemName contains the 
                // name of the item to delete. 
            }

            else 
            {
                // Cancel the command. 
            } 
            break; 
    } 
    return 0L; 
```



<span data-ttu-id="b846b-152">In diesem Beispiel gibt die Anwendung das Hauptfenster als Besitzer Fenster für das Dialogfeld an.</span><span class="sxs-lookup"><span data-stu-id="b846b-152">In this example, the application specifies its main window as the owner window for the dialog box.</span></span> <span data-ttu-id="b846b-153">Wenn das System das Dialogfeld anfänglich anzeigt, ist seine Position relativ zur oberen linken Ecke des Client Bereichs des Besitzer Fensters.</span><span class="sxs-lookup"><span data-stu-id="b846b-153">When the system initially displays the dialog box, its position is relative to the upper left corner of the owner window's client area.</span></span> <span data-ttu-id="b846b-154">Die Anwendung verwendet den Rückgabewert aus [**Dialogbox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) , um zu bestimmen, ob der Vorgang fortgesetzt oder abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b846b-154">The application uses the return value from [**DialogBox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) to determine whether to proceed with the operation or cancel it.</span></span> <span data-ttu-id="b846b-155">Die folgenden Anweisungen definieren die Dialogfeld Prozedur.</span><span class="sxs-lookup"><span data-stu-id="b846b-155">The following statements define the dialog box procedure.</span></span>


```
char szItemName[80]; // receives name of item to delete. 
 
BOOL CALLBACK DeleteItemProc(HWND hwndDlg, 
                             UINT message, 
                             WPARAM wParam, 
                             LPARAM lParam) 
{ 
    switch (message) 
    { 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDOK: 
                    if (!GetDlgItemText(hwndDlg, ID_ITEMNAME, szItemName, 80)) 
                         *szItemName=0; 
 
                    // Fall through. 
 
                case IDCANCEL: 
                    EndDialog(hwndDlg, wParam); 
                    return TRUE; 
            } 
    } 
    return FALSE; 
} 
```



<span data-ttu-id="b846b-156">In diesem Beispiel verwendet die Prozedur [**getdlgitemtext**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemtexta) , um den aktuellen Text aus dem Bearbeitungs Steuerelement abzurufen, das durch ID \_ ItemName identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="b846b-156">In this example, the procedure uses [**GetDlgItemText**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemtexta) to retrieve the current text from the edit control identified by ID\_ITEMNAME.</span></span> <span data-ttu-id="b846b-157">Die Prozedur ruft dann die [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) -Funktion auf, um den Rückgabewert des Dialog Felds abhängig von der empfangenen Nachricht entweder auf IDOK oder IDCANCEL festzulegen, und beginnt damit, das Dialogfeld zu schließen.</span><span class="sxs-lookup"><span data-stu-id="b846b-157">The procedure then calls the [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) function to set the dialog box's return value to either IDOK or IDCANCEL, depending on the message received, and to begin the process of closing the dialog box.</span></span> <span data-ttu-id="b846b-158">Die IDOK-und IDCANCEL-Bezeichner entsprechen den Schaltflächen **OK** und **Abbrechen** .</span><span class="sxs-lookup"><span data-stu-id="b846b-158">The IDOK and IDCANCEL identifiers correspond to the **OK** and **Cancel** buttons.</span></span> <span data-ttu-id="b846b-159">Nachdem die Prozedur **EndDialog** aufgerufen hat, sendet das System zusätzliche Meldungen an die Prozedur, um das Dialogfeld zu zerstören, und gibt den Rückgabewert des Dialog Felds zurück an die Funktion, die das Dialogfeld erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="b846b-159">After the procedure calls **EndDialog**, the system sends additional messages to the procedure to destroy the dialog box and returns the dialog box's return value back to the function that created the dialog box.</span></span>

## <a name="creating-a-modeless-dialog-box"></a><span data-ttu-id="b846b-160">Erstellen eines nicht modalem Dialog Felds</span><span class="sxs-lookup"><span data-stu-id="b846b-160">Creating a Modeless Dialog Box</span></span>

<span data-ttu-id="b846b-161">Sie erstellen ein nicht modalem Dialogfeld mithilfe der Funktion "up [**Dialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) ", indem Sie den Bezeichner oder den Namen einer Dialogfeld Vorlagen Ressource und einen Zeiger auf die Dialogfeld Prozedur angeben.</span><span class="sxs-lookup"><span data-stu-id="b846b-161">You create a modeless dialog box by using the [**CreateDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) function, specifying the identifier or name of a dialog box template resource and a pointer to the dialog box procedure.</span></span> <span data-ttu-id="b846b-162">Mit " **anatedialog** " wird die Vorlage geladen, das Dialogfeld erstellt und optional angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b846b-162">**CreateDialog** loads the template, creates the dialog box, and optionally displays it.</span></span> <span data-ttu-id="b846b-163">Die Anwendung ist für das Abrufen und Verteilen von Benutzereingabe Nachrichten an die Dialogfeld Prozedur zuständig.</span><span class="sxs-lookup"><span data-stu-id="b846b-163">Your application is responsible for retrieving and dispatching user input messages to the dialog box procedure.</span></span>

<span data-ttu-id="b846b-164">Im folgenden Beispiel zeigt die Anwendung ein nicht modalem Dialogfeld an – wenn Sie nicht bereits angezeigt wird –, wenn der Benutzer in einem Anwendungsmenü **auf "Gehe zu** " klickt.</span><span class="sxs-lookup"><span data-stu-id="b846b-164">In the following example, the application displays a modeless dialog box — if it is not already displayed — when the user clicks **Go To** from an application menu.</span></span> <span data-ttu-id="b846b-165">Das Dialogfeld enthält ein Bearbeitungs Steuerelement, ein Kontrollkästchen und Schaltflächen " **OK** " und " **Abbrechen** ".</span><span class="sxs-lookup"><span data-stu-id="b846b-165">The dialog box contains an edit control, a check box, and **OK** and **Cancel** buttons.</span></span> <span data-ttu-id="b846b-166">Die Dialogfeld Vorlage ist eine Ressource in der ausführbaren Datei der Anwendung und verfügt über den Ressourcen Bezeichner DLG \_ goto.</span><span class="sxs-lookup"><span data-stu-id="b846b-166">The dialog box template is a resource in the application's executable file and has the resource identifier DLG\_GOTO.</span></span> <span data-ttu-id="b846b-167">Der Benutzer gibt eine Zeilennummer in das Bearbeitungs Steuerelement ein und überprüft das Kontrollkästchen, um anzugeben, dass die Zeilennummer relativ zur aktuellen Zeile ist.</span><span class="sxs-lookup"><span data-stu-id="b846b-167">The user enters a line number in the edit control and checks the check box to specify that the line number is relative to the current line.</span></span> <span data-ttu-id="b846b-168">Die Steuerelement-IDs sind ID- \_ Zeile, ID- \_ absrel, IDOK und IDCANCEL.</span><span class="sxs-lookup"><span data-stu-id="b846b-168">The control identifiers are ID\_LINE, ID\_ABSREL, IDOK, and IDCANCEL.</span></span>

<span data-ttu-id="b846b-169">Mit den-Anweisungen im ersten Teil des Beispiels wird das nicht modante Dialogfeld erstellt.</span><span class="sxs-lookup"><span data-stu-id="b846b-169">The statements in the first part of the example create the modeless dialog box.</span></span> <span data-ttu-id="b846b-170">Diese Anweisungen erstellen Sie in der Fenster Prozedur für das Hauptfenster der Anwendung das Dialogfeld, wenn die Fenster Prozedur eine [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Nachricht mit dem IDM- \_ goto-Menü Bezeichner empfängt, aber nur, wenn die globale Variable nicht bereits ein gültiges Handle enthält.</span><span class="sxs-lookup"><span data-stu-id="b846b-170">These statements, in the window procedure for the application's main window, create the dialog box when the window procedure receives a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message having the IDM\_GOTO menu identifier, but only if the global variable does not already contain a valid handle.</span></span> <span data-ttu-id="b846b-171">Der zweite Teil des Beispiels ist die Hauptnachrichten Schleife der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="b846b-171">The second part of the example is the application's main message loop.</span></span> <span data-ttu-id="b846b-172">Die-Schleife schließt die [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) -Funktion ein, um sicherzustellen, dass der Benutzer die Dialogfeld-Tastaturschnittstelle im Dialogfeld "nicht modess" verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="b846b-172">The loop includes the [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) function to ensure that the user can use the dialog box keyboard interface in this modeless dialog box.</span></span> <span data-ttu-id="b846b-173">Der dritte Teil des Beispiels ist die Dialogfeld Prozedur.</span><span class="sxs-lookup"><span data-stu-id="b846b-173">The third part of the example is the dialog box procedure.</span></span> <span data-ttu-id="b846b-174">Die Prozedur ruft den Inhalt des Bearbeitungs Steuer Elements und des Kontrollkästchens ab, wenn der Benutzer auf die Schaltfläche **OK** klickt.</span><span class="sxs-lookup"><span data-stu-id="b846b-174">The procedure retrieves the contents of the edit control and check box when the user clicks the **OK** button.</span></span> <span data-ttu-id="b846b-175">Die Prozedur zerstört das Dialogfeld, wenn der Benutzer auf die Schaltfläche **Abbrechen** klickt.</span><span class="sxs-lookup"><span data-stu-id="b846b-175">The procedure destroys the dialog box when the user clicks the **Cancel** button.</span></span>


```
HWND hwndGoto = NULL;  // Window handle of dialog box 
                
...

case WM_COMMAND: 
    switch (LOWORD(wParam)) 
    { 
        case IDM_GOTO: 
            if (!IsWindow(hwndGoto)) 
            { 
                hwndGoto = CreateDialog(hinst, 
                                        MAKEINTRESOURCE(DLG_GOTO), 
                                        hwnd, 
                                        (DLGPROC)GoToProc); 
                ShowWindow(hwndGoto, SW_SHOW); 
            } 
            break; 
    } 
    return 0L; 
```



<span data-ttu-id="b846b-176">In den vorangehenden Anweisungen wird " [**foratedialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) " nur aufgerufen, wenn kein `hwndGoto` gültiges Fenster Handle enthält.</span><span class="sxs-lookup"><span data-stu-id="b846b-176">In the preceding statements, [**CreateDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) is called only if `hwndGoto` does not contain a valid window handle.</span></span> <span data-ttu-id="b846b-177">Dadurch wird sichergestellt, dass die Anwendung nicht gleichzeitig zwei Dialogfelder anzeigt.</span><span class="sxs-lookup"><span data-stu-id="b846b-177">This ensures that the application does not display two dialog boxes at the same time.</span></span> <span data-ttu-id="b846b-178">Zur Unterstützung dieser Überprüfungs Methode muss die Dialogfeld Prozedur auf **null** festgelegt werden, wenn das Dialogfeld zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="b846b-178">To support this method of checking, the dialog procedure must set to **NULL** when it destroys the dialog box.</span></span>

<span data-ttu-id="b846b-179">Die Nachrichten Schleife für eine Anwendung besteht aus den folgenden Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="b846b-179">The message loop for an application consists of the following statements.</span></span>


```
BOOL bRet;

while ((bRet = GetMessage(&msg, NULL, 0, 0)) != 0) 
{ 
    if (bRet == -1)
    {
        // Handle the error and possibly exit
    }
    else if (!IsWindow(hwndGoto) || !IsDialogMessage(hwndGoto, &msg)) 
    { 
        TranslateMessage(&msg); 
        DispatchMessage(&msg); 
    } 
} 
```



<span data-ttu-id="b846b-180">Die-Schleife prüft die Gültigkeit des Fenster Handles auf das Dialogfeld und ruft nur die [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) -Funktion auf, wenn das Handle gültig ist.</span><span class="sxs-lookup"><span data-stu-id="b846b-180">The loop checks the validity of the window handle to the dialog box and only calls the [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) function if the handle is valid.</span></span> <span data-ttu-id="b846b-181">**IsDialogMessage** verarbeitet die Nachricht nur, wenn Sie zum Dialogfeld gehört.</span><span class="sxs-lookup"><span data-stu-id="b846b-181">**IsDialogMessage** only processes the message if it belongs to the dialog box.</span></span> <span data-ttu-id="b846b-182">Andernfalls wird **false** zurückgegeben, und die Schleife sendet die Nachricht an das entsprechende Fenster.</span><span class="sxs-lookup"><span data-stu-id="b846b-182">Otherwise, it returns **FALSE** and the loop dispatches the message to the appropriate window.</span></span>

<span data-ttu-id="b846b-183">Die folgenden Anweisungen definieren die Dialogfeld Prozedur.</span><span class="sxs-lookup"><span data-stu-id="b846b-183">The following statements define the dialog box procedure.</span></span>


```
int iLine;             // Receives line number.
BOOL fRelative;        // Receives check box status. 
 
BOOL CALLBACK GoToProc(HWND hwndDlg, UINT message, WPARAM wParam, LPARAM lParam) 
{ 
    BOOL fError; 
 
    switch (message) 
    { 
        case WM_INITDIALOG: 
            CheckDlgButton(hwndDlg, ID_ABSREL, fRelative); 
            return TRUE; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDOK: 
                    fRelative = IsDlgButtonChecked(hwndDlg, ID_ABSREL); 
                    iLine = GetDlgItemInt(hwndDlg, ID_LINE, &fError, fRelative); 
                    if (fError) 
                    { 
                        MessageBox(hwndDlg, SZINVALIDNUMBER, SZGOTOERR, MB_OK); 
                        SendDlgItemMessage(hwndDlg, ID_LINE, EM_SETSEL, 0, -1L); 
                    } 
                    else 

                    // Notify the owner window to carry out the task. 
 
                    return TRUE; 
 
                case IDCANCEL: 
                    DestroyWindow(hwndDlg); 
                    hwndGoto = NULL; 
                    return TRUE; 
            } 
    } 
    return FALSE; 
} 
```



<span data-ttu-id="b846b-184">In den vorangehenden Anweisungen verarbeitet die Prozedur die [**\_ Befehle**](/windows/desktop/menurc/wm-command) " [**WM \_ InitDialog**](wm-initdialog.md) " und "WM".</span><span class="sxs-lookup"><span data-stu-id="b846b-184">In the preceding statements, the procedure processes the [**WM\_INITDIALOG**](wm-initdialog.md) and [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) messages.</span></span> <span data-ttu-id="b846b-185">Während der **WM \_ InitDialog** -Verarbeitung wird das Kontrollkästchen durch die Prozedur initialisiert, indem der aktuelle Wert der globalen Variablen an [**checkdlgbutton**](https://msdn.microsoft.com/library/Cc410649(v=MSDN.10).aspx)übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="b846b-185">During **WM\_INITDIALOG** processing, the procedure initializes the check box by passing the current value of the global variable to [**CheckDlgButton**](https://msdn.microsoft.com/library/Cc410649(v=MSDN.10).aspx).</span></span> <span data-ttu-id="b846b-186">Die Prozedur gibt dann " **true** " zurück, um das System anzuweisen, den Standardeingabe Fokus festzulegen.</span><span class="sxs-lookup"><span data-stu-id="b846b-186">The procedure then returns **TRUE** to direct the system to set the default input focus.</span></span>

<span data-ttu-id="b846b-187">Während der [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Verarbeitung schließt die Prozedur das Dialogfeld nur dann, wenn der Benutzer auf die Schaltfläche **Abbrechen** klickt, d. –. auf die Schaltfläche mit dem IDCANCEL-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="b846b-187">During [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) processing, the procedure closes the dialog box only if the user clicks the **Cancel** button — that is, the button having the IDCANCEL identifier.</span></span> <span data-ttu-id="b846b-188">Die Prozedur muss [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) aufzurufen, um ein nicht modalem Dialogfeld zu schließen.</span><span class="sxs-lookup"><span data-stu-id="b846b-188">The procedure must call [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) to close a modeless dialog box.</span></span> <span data-ttu-id="b846b-189">Beachten Sie, dass die-Prozedur auch die-Variable auf **null** festlegt, um sicherzustellen, dass andere, von dieser Variable abhängige-Anweisungen ordnungsgemäß funktionieren.</span><span class="sxs-lookup"><span data-stu-id="b846b-189">Notice that the procedure also sets the variable to **NULL** to ensure that other statements that depend on this variable operate correctly.</span></span>

<span data-ttu-id="b846b-190">Wenn der Benutzer auf die Schaltfläche **OK** klickt, ruft die Prozedur den aktuellen Zustand des Kontrollkästchens ab und weist Sie der **frelative** Variablen zu.</span><span class="sxs-lookup"><span data-stu-id="b846b-190">If the user clicks the **OK** button, the procedure retrieves the current state of the check box and assigns it to the **fRelative** variable.</span></span> <span data-ttu-id="b846b-191">Anschließend wird die-Variable verwendet, um die Zeilennummer aus dem Bearbeitungs Steuerelement abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b846b-191">It then uses the variable to retrieve the line number from the edit control.</span></span> <span data-ttu-id="b846b-192">[**Getdlgitemint**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemint) übersetzt den Text im Bearbeitungs Steuerelement in eine ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="b846b-192">[**GetDlgItemInt**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemint) translates the text in the edit control into an integer.</span></span> <span data-ttu-id="b846b-193">Der Wert von **frelative** bestimmt, ob die Funktion die Zahl als einen Wert mit oder ohne Vorzeichen interpretiert.</span><span class="sxs-lookup"><span data-stu-id="b846b-193">The value of **fRelative** determines whether the function interprets the number as a signed or unsigned value.</span></span> <span data-ttu-id="b846b-194">Wenn der Bearbeitungs Steuerelement-Text keine gültige Zahl ist, legt **getdlgitemint** den Wert der **ferror** -Variable auf einen Wert ungleich 0 (null) fest.</span><span class="sxs-lookup"><span data-stu-id="b846b-194">If the edit control text is not a valid number, **GetDlgItemInt** sets the value of the **fError** variable to nonzero.</span></span> <span data-ttu-id="b846b-195">Die Prozedur überprüft diesen Wert, um zu bestimmen, ob eine Fehlermeldung angezeigt oder die Aufgabe durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b846b-195">The procedure checks this value to determine whether to display an error message or carry out the task.</span></span> <span data-ttu-id="b846b-196">Wenn ein Fehler auftritt, sendet die Dialogfeld Prozedur eine Nachricht an das Bearbeitungs Steuerelement und leitet Sie an den Text im Steuerelement weiter, sodass der Benutzer Sie problemlos ersetzen kann.</span><span class="sxs-lookup"><span data-stu-id="b846b-196">In the event of an error, the dialog box procedure sends a message to the edit control, directing it to select the text in the control so that the user can easily replace it.</span></span> <span data-ttu-id="b846b-197">Wenn **getdlgitemint** keinen Fehler zurückgibt, kann die Prozedur entweder die angeforderte Aufgabe selbst ausführen oder eine Nachricht an das Besitzer Fenster senden, um den Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="b846b-197">If **GetDlgItemInt** does not return an error, the procedure can either carry out the requested task itself or send a message to the owner window, directing it to carry out the operation.</span></span>

## <a name="initializing-a-dialog-box"></a><span data-ttu-id="b846b-198">Initialisieren eines Dialog Felds</span><span class="sxs-lookup"><span data-stu-id="b846b-198">Initializing a Dialog Box</span></span>

<span data-ttu-id="b846b-199">Beim Verarbeiten der " [**WM \_ InitDialog**](wm-initdialog.md) "-Nachricht initialisieren Sie das Dialogfeld und seinen Inhalt.</span><span class="sxs-lookup"><span data-stu-id="b846b-199">You initialize the dialog box and its contents while processing the [**WM\_INITDIALOG**](wm-initdialog.md) message.</span></span> <span data-ttu-id="b846b-200">Die häufigste Aufgabe besteht darin, die Steuerelemente zu initialisieren, um die aktuellen Dialogfeld Einstellungen widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="b846b-200">The most common task is to initialize the controls to reflect the current dialog box settings.</span></span> <span data-ttu-id="b846b-201">Eine weitere häufige Aufgabe besteht darin, ein Dialogfeld auf dem Bildschirm oder innerhalb des Besitzer Fensters zu zentrieren.</span><span class="sxs-lookup"><span data-stu-id="b846b-201">Another common task is to center a dialog box on the screen or within its owner window.</span></span> <span data-ttu-id="b846b-202">Eine nützliche Aufgabe für einige Dialogfelder besteht darin, den Eingabefokus auf ein angegebenes Steuerelement festzulegen, anstatt den Standardeingabe Fokus zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="b846b-202">A useful task for some dialog boxes is to set the input focus to a specified control rather than accept the default input focus.</span></span>

<span data-ttu-id="b846b-203">Im folgenden Beispiel zentriert die Dialogfeld Prozedur das Dialogfeld und legt den Eingabefokus bei der Verarbeitung der [**WM \_ InitDialog**](wm-initdialog.md) -Nachricht fest.</span><span class="sxs-lookup"><span data-stu-id="b846b-203">In the following example, the dialog box procedure centers the dialog box and sets the input focus while processing the [**WM\_INITDIALOG**](wm-initdialog.md) message.</span></span> <span data-ttu-id="b846b-204">Um das Dialogfeld zu zentrieren, ruft die Prozedur die Fenster Rechtecke für das Dialogfeld und das Besitzer Fenster ab und berechnet eine neue Position für das Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="b846b-204">To center the dialog box, the procedure retrieves the window rectangles for the dialog box and the owner window and calculates a new position for the dialog box.</span></span> <span data-ttu-id="b846b-205">Um den Eingabefokus festzulegen, überprüft die Prozedur den *wParam* -Parameter, um den Bezeichner des Standardeingabe Fokus zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="b846b-205">To set the input focus, the procedure checks the *wParam* parameter to determine the identifier of the default input focus.</span></span>


```
HWND hwndOwner; 
RECT rc, rcDlg, rcOwner; 

....
 
case WM_INITDIALOG: 

    // Get the owner window and dialog box rectangles. 

    if ((hwndOwner = GetParent(hwndDlg)) == NULL) 
    {
        hwndOwner = GetDesktopWindow(); 
    }

    GetWindowRect(hwndOwner, &rcOwner); 
    GetWindowRect(hwndDlg, &rcDlg); 
    CopyRect(&rc, &rcOwner); 

    // Offset the owner and dialog box rectangles so that right and bottom 
    // values represent the width and height, and then offset the owner again 
    // to discard space taken up by the dialog box. 

    OffsetRect(&rcDlg, -rcDlg.left, -rcDlg.top); 
    OffsetRect(&rc, -rc.left, -rc.top); 
    OffsetRect(&rc, -rcDlg.right, -rcDlg.bottom); 

    // The new position is the sum of half the remaining space and the owner's 
    // original position. 

    SetWindowPos(hwndDlg, 
                 HWND_TOP, 
                 rcOwner.left + (rc.right / 2), 
                 rcOwner.top + (rc.bottom / 2), 
                 0, 0,          // Ignores size arguments. 
                 SWP_NOSIZE); 

    if (GetDlgCtrlID((HWND) wParam) != ID_ITEMNAME) 
    { 
        SetFocus(GetDlgItem(hwndDlg, ID_ITEMNAME)); 
        return FALSE; 
    } 
    return TRUE; 
```



<span data-ttu-id="b846b-206">In den vorangehenden Anweisungen verwendet die Prozedur die [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent) -Funktion, um das Besitzer Fenster Handle in ein Dialogfeld abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b846b-206">In the preceding statements, the procedure uses the [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent) function to retrieve the owner window handle to a dialog box.</span></span> <span data-ttu-id="b846b-207">Die-Funktion gibt das Besitzer Fenster Handle für Dialogfelder und das übergeordnete Fenster Handle für untergeordnete Fenster zurück.</span><span class="sxs-lookup"><span data-stu-id="b846b-207">The function returns the owner window handle to dialog boxes, and the parent window handle to child windows.</span></span> <span data-ttu-id="b846b-208">Da eine Anwendung ein Dialogfeld ohne Besitzer erstellen kann, prüft die Prozedur das zurückgegebene Handle und verwendet die [**GetDesktopWindow**](/windows/desktop/api/winuser/nf-winuser-getdesktopwindow) -Funktion, um das Desktop Fenster Handle bei Bedarf abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b846b-208">Because an application can create a dialog box that has no owner, the procedure checks the returned handle and uses the [**GetDesktopWindow**](/windows/desktop/api/winuser/nf-winuser-getdesktopwindow) function to retrieve the desktop window handle, if necessary.</span></span> <span data-ttu-id="b846b-209">Nach der Berechnung der neuen Position verwendet die Prozedur die [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) -Funktion, um das Dialogfeld zu verschieben. dabei wird der erste HWND-Wert angegeben, \_ um sicherzustellen, dass das Dialogfeld oben im Besitzer Fenster bleibt.</span><span class="sxs-lookup"><span data-stu-id="b846b-209">After calculating the new position, the procedure uses the [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) function to move the dialog box, specifying the HWND\_TOP value to ensure that the dialog box remains on top of the owner window.</span></span>

<span data-ttu-id="b846b-210">Bevor der Eingabefokus festgelegt wird, überprüft die Prozedur den Steuerelement Bezeichner des Standardeingabe Fokus.</span><span class="sxs-lookup"><span data-stu-id="b846b-210">Before setting the input focus, the procedure checks the control identifier of the default input focus.</span></span> <span data-ttu-id="b846b-211">Das System übergibt das Fenster Handle des Standardeingabe Fokus im *wParam* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="b846b-211">The system passes the window handle of the default input focus in the *wParam* parameter.</span></span> <span data-ttu-id="b846b-212">Die [**getdlgctrlid**](/windows/desktop/api/Winuser/nf-winuser-getdlgctrlid) -Funktion gibt den Bezeichner für das Steuerelement zurück, das durch das Fenster Handle identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="b846b-212">The [**GetDlgCtrlID**](/windows/desktop/api/Winuser/nf-winuser-getdlgctrlid) function returns the identifier for the control identified by the window handle.</span></span> <span data-ttu-id="b846b-213">Wenn der Bezeichner nicht mit dem richtigen Bezeichner identisch ist, verwendet die Prozedur die [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) -Funktion, um den Eingabefokus festzulegen.</span><span class="sxs-lookup"><span data-stu-id="b846b-213">If the identifier does not match the correct identifier, the procedure uses the [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) function to set the input focus.</span></span> <span data-ttu-id="b846b-214">Die [**GetDlgItem**](/windows/desktop/api/Winuser/nf-winuser-getdlgitem) -Funktion ist erforderlich, um das Fenster Handle des gewünschten Steuer Elements abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b846b-214">The [**GetDlgItem**](/windows/desktop/api/Winuser/nf-winuser-getdlgitem) function is required to retrieve the window handle of the desired control.</span></span>

## <a name="creating-a-template-in-memory"></a><span data-ttu-id="b846b-215">Erstellen einer Vorlage im Speicher</span><span class="sxs-lookup"><span data-stu-id="b846b-215">Creating a Template in Memory</span></span>

<span data-ttu-id="b846b-216">Anwendungen passen oder ändern den Inhalt von Dialogfeldern abhängig vom aktuellen Status der verarbeiteten Daten.</span><span class="sxs-lookup"><span data-stu-id="b846b-216">Applications sometimes adapt or modify the content of dialog boxes depending on the current state of the data being processed.</span></span> <span data-ttu-id="b846b-217">In solchen Fällen ist es nicht praktikabel, alle möglichen Dialogfeld Vorlagen als Ressourcen in der ausführbaren Datei der Anwendung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="b846b-217">In such cases, it is not practical to provide all possible dialog box templates as resources in the application's executable file.</span></span> <span data-ttu-id="b846b-218">Das Erstellen von Vorlagen im Arbeitsspeicher bietet der Anwendung jedoch mehr Flexibilität bei der Anpassung an jede Situation.</span><span class="sxs-lookup"><span data-stu-id="b846b-218">But creating templates in memory gives the application more flexibility to adapt to any circumstances.</span></span>

<span data-ttu-id="b846b-219">Im folgenden Beispiel erstellt die Anwendung eine Vorlage im Arbeitsspeicher für ein modales Dialogfeld, das die Schaltflächen Nachricht und **OK** und **Hilfe** enthält.</span><span class="sxs-lookup"><span data-stu-id="b846b-219">In the following example, the application creates a template in memory for a modal dialog box that contains a message and **OK** and **Help** buttons.</span></span>

<span data-ttu-id="b846b-220">In einer Dialogfeld Vorlage müssen alle Zeichen folgen, z. b. das Dialogfeld und die Schaltflächen Titel, Unicode-Zeichen folgen sein.</span><span class="sxs-lookup"><span data-stu-id="b846b-220">In a dialog template, all character strings, such as the dialog box and button titles, must be Unicode strings.</span></span> <span data-ttu-id="b846b-221">In diesem Beispiel werden diese Unicode-Zeichen folgen mithilfe der [**multibytetewidechar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) -Funktion generiert.</span><span class="sxs-lookup"><span data-stu-id="b846b-221">This example uses the [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) function to generate these Unicode strings.</span></span>

<span data-ttu-id="b846b-222">Die [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) -Strukturen in einer Dialogfeld Vorlage müssen an den **DWORD** -Grenzen ausgerichtet sein.</span><span class="sxs-lookup"><span data-stu-id="b846b-222">The [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) structures in a dialog template must be aligned on **DWORD** boundaries.</span></span> <span data-ttu-id="b846b-223">Um diese Strukturen auszurichten, wird in diesem Beispiel eine Hilfsroutine verwendet, die einen Eingabe Zeiger annimmt und den nächstgelegenen Zeiger zurückgibt, der an einer **DWORD** -Grenze ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="b846b-223">To align these structures, this example uses a helper routine that takes an input pointer and returns the closest pointer that is aligned on a **DWORD** boundary.</span></span>


```
#define ID_HELP   150
#define ID_TEXT   200

LPWORD lpwAlign(LPWORD lpIn)
{
    ULONG ul;

    ul = (ULONG)lpIn;
    ul ++;
    ul >>=1;
    ul <<=1;
    return (LPWORD)ul;
}

LRESULT DisplayMyMessage(HINSTANCE hinst, HWND hwndOwner, LPSTR lpszMessage)
{
    HGLOBAL hgbl;
    LPDLGTEMPLATE lpdt;
    LPDLGITEMTEMPLATE lpdit;
    LPWORD lpw;
    LPWSTR lpwsz;
    LRESULT ret;
    int nchar;

    hgbl = GlobalAlloc(GMEM_ZEROINIT, 1024);
    if (!hgbl)
        return -1;
 
    lpdt = (LPDLGTEMPLATE)GlobalLock(hgbl);
 
    // Define a dialog box.
 
    lpdt->style = WS_POPUP | WS_BORDER | WS_SYSMENU | DS_MODALFRAME | WS_CAPTION;
    lpdt->cdit = 3;         // Number of controls
    lpdt->x  = 10;  lpdt->y  = 10;
    lpdt->cx = 100; lpdt->cy = 100;

    lpw = (LPWORD)(lpdt + 1);
    *lpw++ = 0;             // No menu
    *lpw++ = 0;             // Predefined dialog box class (by default)

    lpwsz = (LPWSTR)lpw;
    nchar = 1 + MultiByteToWideChar(CP_ACP, 0, "My Dialog", -1, lpwsz, 50);
    lpw += nchar;

    //-----------------------
    // Define an OK button.
    //-----------------------
    lpw = lpwAlign(lpw);    // Align DLGITEMTEMPLATE on DWORD boundary
    lpdit = (LPDLGITEMTEMPLATE)lpw;
    lpdit->x  = 10; lpdit->y  = 70;
    lpdit->cx = 80; lpdit->cy = 20;
    lpdit->id = IDOK;       // OK button identifier
    lpdit->style = WS_CHILD | WS_VISIBLE | BS_DEFPUSHBUTTON;

    lpw = (LPWORD)(lpdit + 1);
    *lpw++ = 0xFFFF;
    *lpw++ = 0x0080;        // Button class

    lpwsz = (LPWSTR)lpw;
    nchar = 1 + MultiByteToWideChar(CP_ACP, 0, "OK", -1, lpwsz, 50);
    lpw += nchar;
    *lpw++ = 0;             // No creation data

    //-----------------------
    // Define a Help button.
    //-----------------------
    lpw = lpwAlign(lpw);    // Align DLGITEMTEMPLATE on DWORD boundary
    lpdit = (LPDLGITEMTEMPLATE)lpw;
    lpdit->x  = 55; lpdit->y  = 10;
    lpdit->cx = 40; lpdit->cy = 20;
    lpdit->id = ID_HELP;    // Help button identifier
    lpdit->style = WS_CHILD | WS_VISIBLE | BS_PUSHBUTTON;

    lpw = (LPWORD)(lpdit + 1);
    *lpw++ = 0xFFFF;
    *lpw++ = 0x0080;        // Button class atom

    lpwsz = (LPWSTR)lpw;
    nchar = 1 + MultiByteToWideChar(CP_ACP, 0, "Help", -1, lpwsz, 50);
    lpw += nchar;
    *lpw++ = 0;             // No creation data

    //-----------------------
    // Define a static text control.
    //-----------------------
    lpw = lpwAlign(lpw);    // Align DLGITEMTEMPLATE on DWORD boundary
    lpdit = (LPDLGITEMTEMPLATE)lpw;
    lpdit->x  = 10; lpdit->y  = 10;
    lpdit->cx = 40; lpdit->cy = 20;
    lpdit->id = ID_TEXT;    // Text identifier
    lpdit->style = WS_CHILD | WS_VISIBLE | SS_LEFT;

    lpw = (LPWORD)(lpdit + 1);
    *lpw++ = 0xFFFF;
    *lpw++ = 0x0082;        // Static class

    for (lpwsz = (LPWSTR)lpw; *lpwsz++ = (WCHAR)*lpszMessage++;);
    lpw = (LPWORD)lpwsz;
    *lpw++ = 0;             // No creation data

    GlobalUnlock(hgbl); 
    ret = DialogBoxIndirect(hinst, 
                           (LPDLGTEMPLATE)hgbl, 
                           hwndOwner, 
                           (DLGPROC)DialogProc); 
    GlobalFree(hgbl); 
    return ret; 
}
```



 

 