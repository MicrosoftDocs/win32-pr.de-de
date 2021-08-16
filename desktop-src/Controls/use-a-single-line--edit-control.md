---
title: Erstellen eines Einzeilen-Bearbeitungssteuerelements
description: In diesem Thema wird veranschaulicht, wie Sie ein Dialogfeld erstellen, das ein einzeiliges Bearbeitungssteuerelement enthält.
ms.assetid: 742DF606-9998-46D0-8D0A-F79508AAFFC0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 597c3e611f53af56a42f837c4d85a43f97ff846e371314b130d72c568aaf860e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829115"
---
# <a name="how-to-create-a-single-line-edit-control"></a>Erstellen eines Einzeilen-Bearbeitungssteuerelements

In diesem Thema wird veranschaulicht, wie Sie ein Dialogfeld erstellen, das ein einzeiliges Bearbeitungssteuerelement enthält.

Das Einzeilen-Bearbeitungssteuerelement weist das [**ES \_ PASSWORD-Format**](edit-control-styles.md) auf. Standardmäßig zeigen Bearbeitungssteuerelemente mit diesem Stil ein Sternchen für jedes Vom Benutzer eingegebene Zeichen an. In diesem Beispiel wird jedoch die [**EM \_ SETPASSWORDCHAR-Nachricht**](em-setpasswordchar.md) verwendet, um das Standardzeichen von einem Sternchen in ein Pluszeichen (+) zu ändern. Der folgende Screenshot zeigt das Dialogfeld, nachdem der Benutzer ein Kennwort eingegeben hat.

![Screenshot eines Dialogfelds, das ein Bearbeitungssteuerelement für die Eingabe eines Kennworts enthält](images/passworddlg.png)

> [!Note]  
> Comctl32.dll Version 6 ist nicht verteilbar. Um Comctl32.dll Version 6 zu verwenden, geben Sie sie in einem Manifest an. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen.](cookbook-overview.md)

 

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen

### <a name="step-1-create-an-instance-of-the-password-dialog-box"></a>Schritt 1: Erstellen Sie eine Instanz des Kennwortdialogfelds.

Im folgenden C++-Codebeispiel wird die DialogBox-Funktion verwendet, um ein modales Dialogfeld zu erstellen. Die Dialogfeldvorlage **IDD \_ PASSWORD** wird als Parameter übergeben. Sie definiert unter anderem die Fensterstile, Schaltflächen und Dimensionen des Kennwortdialogfelds.


```C++
DialogBox(hInst,                   // application instance
    MAKEINTRESOURCE(IDD_PASSWORD), // dialog box resource
    hWnd,                          // owner window
    PasswordProc                    // dialog box window procedure
    );
```



### <a name="step-2-initialize-the-dialog-box-and-process-user-input"></a>Schritt 2: Initialisieren des Dialogfelds und Verarbeiten von Benutzereingaben.

Die Fensterprozedur im folgenden Beispiel initialisiert das Kennwortdialogfeld und verarbeitet Benachrichtigungsmeldungen und Benutzereingaben.

Während der Initialisierung ändert die Fensterprozedur das Standardkennwortzeichen in ein **+** -Zeichen und legt das Standard-Pushbutton auf **Abbrechen** fest.

Während der Verarbeitung von Benutzereingaben ändert die Fensterprozedur die Standardtastentaste von **ABBRECHEN** in **OK,** sobald der Benutzer Text in das Bearbeitungssteuerelement eingibt. Wenn der Benutzer auf die Schaltfläche **OK** klickt, verwendet die Fensterprozedur die [**EM \_ LINELENGTH-**](em-linelength.md) und [**EM \_ GETLINE-Meldungen,**](em-getline.md) um den Text abzurufen.



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

[Informationen zum Bearbeiten von Steuerelementen](about-edit-controls.md)
</dt> <dt>

[Steuerelementverweis bearbeiten](bumper-edit-control-edit-control-reference.md)
</dt> <dt>

[Verwenden von Bearbeitungssteuerelementen](/windows/desktop/Controls/using-edit-controls)
</dt> <dt>

[Steuerelement bearbeiten](edit-controls.md)
</dt> </dl>

 

 