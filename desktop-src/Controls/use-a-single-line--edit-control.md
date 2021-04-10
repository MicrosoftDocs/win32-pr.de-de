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
# <a name="how-to-create-a-single-line-edit-control"></a>Erstellen eines einzeiligen Bearbeitungs Steuer Elements

In diesem Thema wird veranschaulicht, wie ein Dialogfeld erstellt wird, das ein einzeilige Bearbeitungs Steuerelement enthält.

Das einzeilige Bearbeitungs Steuerelement hat das Format " [**es- \_ Kennwort**](edit-control-styles.md) ". Standardmäßig wird für Bearbeitungs Steuerelemente mit diesem Stil ein Sternchen für jedes Zeichen angezeigt, das vom Benutzer eingegeben wird. In diesem Beispiel wird jedoch die Nachricht [**EM \_ setpasswordchar**](em-setpasswordchar.md) verwendet, um das Standard Zeichen von einem Sternchen in ein Pluszeichen (+) zu ändern. Der folgende Screenshot zeigt das Dialogfeld, nachdem der Benutzer ein Kennwort eingegeben hat.

![Screenshot eines Dialog Felds mit einem Bearbeitungs Steuerelement zum Eingeben eines Kennworts](images/passworddlg.png)

> [!Note]  
> Comctl32.dll Version 6 ist nicht Verteil Bar. Wenn Sie Comctl32.dll Version 6 verwenden möchten, geben Sie ihn in einem Manifest an. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).

 

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="step-1-create-an-instance-of-the-password-dialog-box"></a>Schritt 1: Erstellen Sie eine Instanz des Dialog Felds "Kennwort".

Im folgenden C++-Codebeispiel wird die Dialogbox-Funktion verwendet, um ein modales Dialogfeld zu erstellen. Das **IDD- \_ Kennwort** für die Dialogfeld Vorlage wird als Parameter übergeben. Unter anderem werden die Fenster Stile, Schaltflächen und Dimensionen des Dialog Felds Kennwort definiert.


```C++
DialogBox(hInst,                   // application instance
    MAKEINTRESOURCE(IDD_PASSWORD), // dialog box resource
    hWnd,                          // owner window
    PasswordProc                    // dialog box window procedure
    );
```



### <a name="step-2-initialize-the-dialog-box-and-process-user-input"></a>Schritt 2: Initialisieren Sie das Dialogfeld, und verarbeiten Sie die Benutzereingaben.

Mit der Fenster Prozedur im folgenden Beispiel wird das Kenn Wort Dialogfeld initialisiert und Benachrichtigungs Meldungen und Benutzereingaben verarbeitet.

Während der Initialisierung wird das standardmäßige Kenn Wort Zeichen von der Fenster Prozedur in ein **+** Vorzeichen geändert und der Standardwert für PUSHBUTTON auf **Abbrechen** festgelegt.

Bei der Verarbeitung von Benutzereingaben ändert die Fenster Prozedur die Standard-Schaltfläche "Push" von " **Abbrechen** " in " **OK** ", sobald der Benutzer Text im Bearbeitungs Steuerelement eingibt. Wenn der Benutzer auf die Schaltfläche " **OK** " drückt, verwendet die Fenster Prozedur die Nachrichten " [**EM \_ LineLength**](em-linelength.md) " und " [**EM \_ getline**](em-getline.md) ", um den Text abzurufen.



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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Bearbeitungs Steuerelementen](about-edit-controls.md)
</dt> <dt>

[Steuerelement Verweis bearbeiten](bumper-edit-control-edit-control-reference.md)
</dt> <dt>

[Verwenden von Bearbeitungs Steuerelementen](/windows/desktop/Controls/using-edit-controls)
</dt> <dt>

[Steuerelement bearbeiten](edit-controls.md)
</dt> </dl>

 

 