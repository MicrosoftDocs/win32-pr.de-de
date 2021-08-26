---
title: Erstellen einer Verzeichnisliste in einer ListBox
description: In diesem Thema wird veranschaulicht, wie Sie ein Listenfeld mit einer einzelnen Auswahl verwenden, um den Inhalt eines Verzeichnisses anzuzeigen und darauf zu zugreifen.
ms.assetid: 11C0DB10-59BA-47C4-8687-101A2A85D660
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 926dc09e1e8cee85d230b0715684e084350c97c64b6f6cafb8228cc82cc61dc4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920470"
---
# <a name="how-to-create-a-directory-listing-in-a-single-selection-listbox"></a>Erstellen einer Verzeichnisliste in einem ListBox-Listenfeld mit nur einer Auswahl

In diesem Thema wird veranschaulicht, wie Sie ein Listenfeld mit einer einzelnen Auswahl verwenden, um den Inhalt eines Verzeichnisses anzuzeigen und darauf zu zugreifen. Das Listenfeld mit einzelner Auswahl ist der Standardtyp des Listenfelds. Ein Benutzer kann nur ein Element gleichzeitig aus einem Listenfeld mit einer einzelnen Auswahl auswählen.

Im C++-Codebeispiel in diesem Thema kann ein Benutzer eine Liste von Dateien im aktuellen Verzeichnis anzeigen, eine Datei aus der Liste auswählen und löschen.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen


Die Anwendung für die Verzeichnisauflistung muss die folgenden Aufgaben im Zusammenhang mit Listenfelden ausführen:

-   Initialisieren Sie das Listenfeld.
-   Rufen Sie die Auswahl des Benutzers aus dem Listenfeld ab.
-   Entfernen Sie den Dateinamen aus dem Listenfeld, nachdem die ausgewählte Datei gelöscht wurde.

Im folgenden C++-Codebeispiel initialisiert die Dialogfeldprozedur das Einzelauswahllistenfeld (IDC FILELIST) mithilfe der \_ [**DlgDirList-Funktion,**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) um das Listenfeld mit den Namen aller Dateien im aktuellen Verzeichnis zu füllen. Wenn der Benutzer eine Datei auswählt und die Schaltfläche Löschen auswählt, ruft die [**DlgDirSelectEx-Funktion**](/windows/desktop/api/Winuser/nf-winuser-dlgdirselectexa) den Namen der ausgewählten Datei ab.  Der Code löscht die Datei mithilfe der [**DeleteFile-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea) und aktualisiert das Verzeichnislistenfeld, indem die [**LB \_ DELETESTRING-Nachricht gesendet**](lb-deletestring.md) wird.



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

[Referenz zum Listenfeld-Steuerelement](bumper-list-box-list-box-control-reference.md)
</dt> <dt>

[Informationen zu Listenfeldern](about-list-boxes.md)
</dt> <dt>

[Verwenden von Listenfeldern](using-list-boxes.md)
</dt> </dl>

 

 