---
title: Erstellen einer Verzeichnisliste in einem Listenfeld
description: In diesem Thema wird veranschaulicht, wie Sie ein Listenfeld mit einfacher Auswahl verwenden, um den Inhalt eines Verzeichnisses anzuzeigen und darauf zuzugreifen.
ms.assetid: 11C0DB10-59BA-47C4-8687-101A2A85D660
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03829990605271574a2030486ac5aba428867ec3
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103949224"
---
# <a name="how-to-create-a-directory-listing-in-a-single-selection-listbox"></a>Erstellen einer Verzeichnisliste in einem Listenfeld mit einfacher Auswahl

In diesem Thema wird veranschaulicht, wie Sie ein Listenfeld mit einfacher Auswahl verwenden, um den Inhalt eines Verzeichnisses anzuzeigen und darauf zuzugreifen. Das Listenfeld für die einfache Auswahl ist der Standard Listen Feldtyp. Ein Benutzer kann jeweils nur ein Element in einem Listenfeld mit einer einzelnen Auswahl auswählen.

Mit dem C++-Codebeispiel in diesem Thema kann ein Benutzer eine Liste der Dateien im aktuellen Verzeichnis anzeigen, eine Datei aus der Liste auswählen und diese löschen.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen


Die Verzeichnis Auflistungs Anwendung muss die folgenden Aufgaben im Zusammenhang mit dem Listenfeld ausführen:

-   Initialisieren Sie das Listenfeld.
-   Rufen Sie die Auswahl des Benutzers aus dem Listenfeld ab.
-   Entfernen Sie den Dateinamen aus dem Listenfeld, nachdem die ausgewählte Datei gelöscht wurde.

Im folgenden C++-Codebeispiel initialisiert die Dialogfeld Prozedur das Listenfeld für die einfache Auswahl (IDC \_ FileList) mithilfe der [**dlgdirlist**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) -Funktion, um das Listenfeld mit den Namen aller Dateien im aktuellen Verzeichnis auszufüllen. Wenn der Benutzer eine Datei auswählt und auf die Schaltfläche **Löschen** klickt, ruft die [**DlgDirSelectEx**](/windows/desktop/api/Winuser/nf-winuser-dlgdirselectexa) -Funktion den Namen der ausgewählten Datei ab. Der Code löscht die Datei mit der [**DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea) -Funktion und aktualisiert das Listenfeld Verzeichnis durch Senden der [**lb- \_ deletestring**](lb-deletestring.md) -Nachricht.



```C++
INT_PTR CALLBACK DlgDelFileProc(HWND hDlg, UINT message, 
        UINT wParam, LONG lParam) 
{ 
    PTSTR pszCurDir; 
    PTSTR pszFileToDelete; 
    int iLBItem; 
    int cStringsRemaining; 
    int iRet; 
    TCHAR achBuffer[MAX_PATH]; 
    TCHAR achTemp[MAX_PATH]; 
    BOOL fResult;     
 
    switch (message) 
    { 
        case WM_INITDIALOG: 
 
           // Initialize the list box by filling it with files from 
           // the current directory. 
           pszCurDir = achBuffer; 
           GetCurrentDirectory(MAX_PATH, pszCurDir); 
           DlgDirList(hDlg, pszCurDir, IDC_FILELIST, IDS_PATHTOFILL, 0); 
           SetFocus(GetDlgItem(hDlg, IDC_FILELIST)); 
           return FALSE; 
 
        case WM_COMMAND: 
 
            switch (LOWORD(wParam)) 
            { 
                case IDOK: 
 
                    // When the user presses the DEL (IDOK) button, 
                    // first retrieve the selected file. 
                    pszFileToDelete = achBuffer; 
                    DlgDirSelectEx(hDlg, pszFileToDelete, MAX_PATH, 
                        IDC_FILELIST); 

                    // Make sure the user really wants to delete the file.
                    achTemp[MAX_PATH];
                    StringCbPrintf (achTemp, ARRAYSIZE(achTemp),  
                            TEXT("Are you sure you want to delete %s?"), 
                            pszFileToDelete);
                    iRet = MessageBox(hDlg, achTemp, L"Deleting Files", 
                        MB_YESNO | MB_ICONEXCLAMATION);
                    if (iRet == IDNO)
                        return TRUE;;

                    // Delete the file.
                    fResult = DeleteFile(pszFileToDelete); 
                    if (!fResult) 
                    { 
                        MessageBox(hDlg, L"Could not delete file.", 
                            NULL, MB_OK); 
                    } 
                    else // Remove the filename from the list box.
                    { 
                        // Get the selected item.
                        iLBItem = SendMessage(GetDlgItem(hDlg, IDC_FILELIST), 
                            LB_GETCURSEL, 0, 0); 
 
                        // Delete the selected item.
                        cStringsRemaining = SendMessage(GetDlgItem(hDlg, IDC_FILELIST), 
                            LB_DELETESTRING, iLBItem, 0); 
 
                        // If this is not the last item, set the selection to 
                        // the item immediately following the one just deleted.
                        // Otherwise, set the selection to the last item.
                         if (cStringsRemaining > iLBItem) 
                        { 
                            SendMessage(GetDlgItem(hDlg, IDC_FILELIST), 
                                LB_SETCURSEL, iLBItem, 0); 
                        } 
                        else 
                        { 
                            SendMessage(GetDlgItem(hDlg, IDC_FILELIST), 
                                LB_SETCURSEL, cStringsRemaining, 0); 
                        } 
                    } 
                    return TRUE; 
 
                case IDCANCEL: 
 
                    // Destroy the dialog box. 
                     EndDialog(hDlg, TRUE); 
                    return TRUE; 
 
                default: 
                    return FALSE; 
            } 
 
        default: 
            return FALSE; 
    } 
} 
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Listenfeld-Steuerelement Verweis](bumper-list-box-list-box-control-reference.md)
</dt> <dt>

[Informationen zu Listenfeldern](about-list-boxes.md)
</dt> <dt>

[Verwenden von Listenfeldern](using-list-boxes.md)
</dt> </dl>

 

 