---
title: Erstellen eines einzeiligen Bearbeitungs Steuer Elements
description: In diesem Thema wird veranschaulicht, wie ein Dialogfeld erstellt wird, das ein einzeilige Bearbeitungs Steuerelement enthält.
ms.assetid: 742DF606-9998-46D0-8D0A-F79508AAFFC0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0d5d39a4c9fbc806de6ca151606e770eb0cea9b
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104039853"
---
# <a name="how-to-create-a-single-line-edit-control"></a><span data-ttu-id="8aa7f-103">Erstellen eines einzeiligen Bearbeitungs Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="8aa7f-103">How to Create a Single Line Edit Control</span></span>

<span data-ttu-id="8aa7f-104">In diesem Thema wird veranschaulicht, wie ein Dialogfeld erstellt wird, das ein einzeilige Bearbeitungs Steuerelement enthält.</span><span class="sxs-lookup"><span data-stu-id="8aa7f-104">This topic demonstrates how to create a dialog box that contains a single-line edit control.</span></span>

<span data-ttu-id="8aa7f-105">Das einzeilige Bearbeitungs Steuerelement hat das Format " [**es- \_ Kennwort**](edit-control-styles.md) ".</span><span class="sxs-lookup"><span data-stu-id="8aa7f-105">The single-line edit control has the [**ES\_PASSWORD**](edit-control-styles.md) style.</span></span> <span data-ttu-id="8aa7f-106">Standardmäßig wird für Bearbeitungs Steuerelemente mit diesem Stil ein Sternchen für jedes Zeichen angezeigt, das vom Benutzer eingegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8aa7f-106">By default, edit controls with this style display an asterisk for each character that is typed by the user.</span></span> <span data-ttu-id="8aa7f-107">In diesem Beispiel wird jedoch die Nachricht [**EM \_ setpasswordchar**](em-setpasswordchar.md) verwendet, um das Standard Zeichen von einem Sternchen in ein Pluszeichen (+) zu ändern.</span><span class="sxs-lookup"><span data-stu-id="8aa7f-107">This example, however, uses the [**EM\_SETPASSWORDCHAR**](em-setpasswordchar.md) message to change the default character from an asterisk to a plus sign (+).</span></span> <span data-ttu-id="8aa7f-108">Der folgende Screenshot zeigt das Dialogfeld, nachdem der Benutzer ein Kennwort eingegeben hat.</span><span class="sxs-lookup"><span data-stu-id="8aa7f-108">The following screen shot shows the dialog box after the user has entered a password.</span></span>

![Screenshot eines Dialog Felds mit einem Bearbeitungs Steuerelement zum Eingeben eines Kennworts](images/passworddlg.png)

> [!Note]  
> <span data-ttu-id="8aa7f-110">Comctl32.dll Version 6 ist nicht Verteil Bar.</span><span class="sxs-lookup"><span data-stu-id="8aa7f-110">Comctl32.dll version 6 is not redistributable.</span></span> <span data-ttu-id="8aa7f-111">Wenn Sie Comctl32.dll Version 6 verwenden möchten, geben Sie ihn in einem Manifest an.</span><span class="sxs-lookup"><span data-stu-id="8aa7f-111">To use Comctl32.dll version 6, specify it in a manifest.</span></span> <span data-ttu-id="8aa7f-112">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8aa7f-112">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="what-you-need-to-know"></a><span data-ttu-id="8aa7f-113">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="8aa7f-113">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="8aa7f-114">Technologien</span><span class="sxs-lookup"><span data-stu-id="8aa7f-114">Technologies</span></span>

-   [<span data-ttu-id="8aa7f-115">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="8aa7f-115">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="8aa7f-116">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="8aa7f-116">Prerequisites</span></span>

-   <span data-ttu-id="8aa7f-117">C/C++</span><span class="sxs-lookup"><span data-stu-id="8aa7f-117">C/C++</span></span>
-   <span data-ttu-id="8aa7f-118">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="8aa7f-118">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="8aa7f-119">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="8aa7f-119">Instructions</span></span>

### <a name="step-1-create-an-instance-of-the-password-dialog-box"></a><span data-ttu-id="8aa7f-120">Schritt 1: Erstellen Sie eine Instanz des Dialog Felds "Kennwort".</span><span class="sxs-lookup"><span data-stu-id="8aa7f-120">Step 1: Create an instance of the password dialog box.</span></span>

<span data-ttu-id="8aa7f-121">Im folgenden C++-Codebeispiel wird die Dialogbox-Funktion verwendet, um ein modales Dialogfeld zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8aa7f-121">The following C++ code example uses the DialogBox function to create a modal dialog box.</span></span> <span data-ttu-id="8aa7f-122">Das **IDD- \_ Kennwort** für die Dialogfeld Vorlage wird als Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="8aa7f-122">The dialog box template **IDD\_PASSWORD** is passed as a parameter.</span></span> <span data-ttu-id="8aa7f-123">Unter anderem werden die Fenster Stile, Schaltflächen und Dimensionen des Dialog Felds Kennwort definiert.</span><span class="sxs-lookup"><span data-stu-id="8aa7f-123">It defines, among other things, the window styles, buttons, and dimensions of the password dialog box.</span></span>


```C++
DialogBox(hInst,                   // application instance
    MAKEINTRESOURCE(IDD_PASSWORD), // dialog box resource
    hWnd,                          // owner window
    PasswordProc                    // dialog box window procedure
    );
```



### <a name="step-2-initialize-the-dialog-box-and-process-user-input"></a><span data-ttu-id="8aa7f-124">Schritt 2: Initialisieren Sie das Dialogfeld, und verarbeiten Sie die Benutzereingaben.</span><span class="sxs-lookup"><span data-stu-id="8aa7f-124">Step 2: Initialize the dialog box and process user input.</span></span>

<span data-ttu-id="8aa7f-125">Mit der Fenster Prozedur im folgenden Beispiel wird das Kenn Wort Dialogfeld initialisiert und Benachrichtigungs Meldungen und Benutzereingaben verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="8aa7f-125">The window procedure in the following example initializes the password dialog box and processes notification messages and user input.</span></span>

<span data-ttu-id="8aa7f-126">Während der Initialisierung wird das standardmäßige Kenn Wort Zeichen von der Fenster Prozedur in ein **+** Vorzeichen geändert und der Standardwert für PUSHBUTTON auf **Abbrechen** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8aa7f-126">During initialization, the window procedure changes the default password character to a **+** sign and sets the default pushbutton to **Cancel**.</span></span>

<span data-ttu-id="8aa7f-127">Bei der Verarbeitung von Benutzereingaben ändert die Fenster Prozedur die Standard-Schaltfläche "Push" von " **Abbrechen** " in " **OK** ", sobald der Benutzer Text im Bearbeitungs Steuerelement eingibt.</span><span class="sxs-lookup"><span data-stu-id="8aa7f-127">During user input processing, the window procedure changes the default push button from **CANCEL** to **OK** as soon as the user enters text in the edit control.</span></span> <span data-ttu-id="8aa7f-128">Wenn der Benutzer auf die Schaltfläche " **OK** " drückt, verwendet die Fenster Prozedur die Nachrichten " [**EM \_ LineLength**](em-linelength.md) " und " [**EM \_ getline**](em-getline.md) ", um den Text abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8aa7f-128">If the user presses the **OK** button, the window procedure uses the [**EM\_LINELENGTH**](em-linelength.md) and [**EM\_GETLINE**](em-getline.md) messages to retrieve the text.</span></span>



```C++
INT_PTR CALLBACK PasswordProc(HWND hDlg, UINT message, WPARAM wParam, LPARAM lParam) 
{ 
    TCHAR lpszPassword[16]; 
    WORD cchPassword; 

    switch (message) 
    { 
        case WM_INITDIALOG: 
            // Set password character to a plus sign (+) 
            SendDlgItemMessage(hDlg, 
                               IDE_PASSWORDEDIT, 
                               EM_SETPASSWORDCHAR, 
                               (WPARAM) '+', 
                               (LPARAM) 0); 

            // Set the default push button to "Cancel." 
            SendMessage(hDlg, 
                        DM_SETDEFID, 
                        (WPARAM) IDCANCEL, 
                        (LPARAM) 0); 

            return TRUE; 

        case WM_COMMAND: 
            // Set the default push button to "OK" when the user enters text. 
            if(HIWORD (wParam) == EN_CHANGE && 
                                LOWORD(wParam) == IDE_PASSWORDEDIT) 
            {
                SendMessage(hDlg, 
                            DM_SETDEFID, 
                            (WPARAM) IDOK, 
                            (LPARAM) 0); 
            }
            switch(wParam) 
            { 
                case IDOK: 
                    // Get number of characters. 
                    cchPassword = (WORD) SendDlgItemMessage(hDlg, 
                                                            IDE_PASSWORDEDIT, 
                                                            EM_LINELENGTH, 
                                                            (WPARAM) 0, 
                                                            (LPARAM) 0); 
                    if (cchPassword >= 16) 
                    { 
                        MessageBox(hDlg, 
                                   L"Too many characters.", 
                                   L"Error", 
                                   MB_OK); 

                        EndDialog(hDlg, TRUE); 
                        return FALSE; 
                    } 
                    else if (cchPassword == 0) 
                    { 
                        MessageBox(hDlg, 
                                   L"No characters entered.", 
                                   L"Error", 
                                   MB_OK); 

                        EndDialog(hDlg, TRUE); 
                        return FALSE; 
                    } 

                    // Put the number of characters into first word of buffer. 
                    *((LPWORD)lpszPassword) = cchPassword; 

                    // Get the characters. 
                    SendDlgItemMessage(hDlg, 
                                       IDE_PASSWORDEDIT, 
                                       EM_GETLINE, 
                                       (WPARAM) 0,       // line 0 
                                       (LPARAM) lpszPassword); 

                    // Null-terminate the string. 
                    lpszPassword[cchPassword] = 0; 

                    MessageBox(hDlg, 
                               lpszPassword, 
                               L"Did it work?", 
                               MB_OK); 

                    // Call a local password-parsing function. 
                    ParsePassword(lpszPassword); 

                    EndDialog(hDlg, TRUE); 
                    return TRUE; 

                case IDCANCEL: 
                    EndDialog(hDlg, TRUE); 
                    return TRUE; 
            } 
            return 0; 
    } 
    return FALSE; 
    
    UNREFERENCED_PARAMETER(lParam); 
}
```



## <a name="related-topics"></a><span data-ttu-id="8aa7f-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8aa7f-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8aa7f-130">Informationen zu Bearbeitungs Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="8aa7f-130">About Edit Controls</span></span>](about-edit-controls.md)
</dt> <dt>

[<span data-ttu-id="8aa7f-131">Steuerelement Verweis bearbeiten</span><span class="sxs-lookup"><span data-stu-id="8aa7f-131">Edit Control Reference</span></span>](bumper-edit-control-edit-control-reference.md)
</dt> <dt>

[<span data-ttu-id="8aa7f-132">Verwenden von Bearbeitungs Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="8aa7f-132">Using Edit Controls</span></span>](/windows/desktop/Controls/using-edit-controls)
</dt> <dt>

[<span data-ttu-id="8aa7f-133">Steuerelement bearbeiten</span><span class="sxs-lookup"><span data-stu-id="8aa7f-133">Edit Control</span></span>](edit-controls.md)
</dt> </dl>

 

 