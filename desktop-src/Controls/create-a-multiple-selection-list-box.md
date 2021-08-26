---
title: Erstellen eines Multiple-Selection Listenfelds
description: In diesem Thema wird veranschaulicht, wie sie den Inhalt eines Verzeichnisses in einem Listenfeld mit mehrfacher Auswahl anzeigen und darauf zugreifen.
ms.assetid: 5192E171-8CEF-4921-9378-A7C3A52A9024
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f375ca2df82f851401baec79683a54ff28cf14e7a004d08cb0885e60fb036d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920860"
---
# <a name="how-to-create-a-multiple-selection-list-box"></a>Erstellen eines Multiple-Selection Listenfelds

In diesem Thema wird veranschaulicht, wie sie den Inhalt eines Verzeichnisses in einem Listenfeld mit mehrfacher Auswahl anzeigen und darauf zugreifen. In einem Listenfeld mit mehrfacher Auswahl kann der Benutzer mehrere Elemente gleichzeitig auswählen.

Das C++-Codebeispiel in diesem Thema ermöglicht es einem Benutzer, eine Liste von Dateien im aktuellen Verzeichnis anzuzeigen, eine Gruppe von Dateien aus der Liste auszuwählen und diese zu löschen.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen


Die Anwendung für die Verzeichnisauflistung muss die folgenden Aufgaben im Zusammenhang mit listenfeldbezogenen Aufgaben ausführen:

-   Initialisieren Sie das Listenfeld.
-   Rufen Sie die Auswahl des Benutzers aus dem Listenfeld ab.
-   Entfernen Sie die Dateinamen aus dem Listenfeld, nachdem die ausgewählten Dateien gelöscht wurden.

Im folgenden C++-Codebeispiel initialisiert die Dialogfeldprozedur das Listenfeld mit mehrfacher Auswahl (IDC \_ FILELIST), indem die [**DlgDirList-Funktion**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) verwendet wird, um das Listenfeld mit den Namen aller Dateien im aktuellen Verzeichnis zu füllen.

Wenn der Benutzer eine Gruppe von Dateien auswählt und die Schaltfläche **Löschen** auswählt, sendet die Dialogfeldprozedur die [**LB \_ GETSELCOUNT-Nachricht,**](lb-getselcount.md) um die Anzahl der ausgewählten Dateien abzurufen, und die [**LB \_ GETSELITEMS-Nachricht,**](lb-getselitems.md) um ein Array ausgewählter Listenfeldelemente abzurufen. Nach dem Löschen einer Datei entfernt die Dialogfeldprozedur das entsprechende Element aus dem Listenfeld, indem die [**LB \_ DELETESTRING-Nachricht**](lb-deletestring.md) gesendet wird.



```C++
#define BIGBUFF 8192 
 
INT_PTR CALLBACK DlgDelFilesProc(HWND hDlg, UINT message, 
        UINT wParam, LONG lParam) 
{ 
    PTSTR pszCurDir; 
    PTSTR pszFileToDelete; 
    int cSelItems; 
    int cSelItemsInBuffer; 
    TCHAR achBuffer[MAX_PATH]; 
    int aSelItems[BIGBUFF]; 
    int i; 
    BOOL fResult; 
    HWND hListBox;
    int iRet;
 
    switch (message) { 
 
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
                    // first retrieve the list of selected files. 
                    pszFileToDelete = achBuffer; 
                    hListBox = GetDlgItem(hDlg, IDC_FILELIST); 
                    cSelItems = SendMessage(hListBox, 
                            LB_GETSELCOUNT, 0, 0); 
 
                    cSelItemsInBuffer = SendMessage(hListBox, 
                            LB_GETSELITEMS, 512, (LPARAM) aSelItems); 
 
                    if (cSelItems > cSelItemsInBuffer) 
                    { 
                        MessageBox(hDlg, L"Too many items selected.", 
                                NULL, MB_OK); 
                    } 
                    else 
                    { 

                        // Make sure the user really wants to delete the files.
                        iRet = MessageBox(hDlg, 
                            L"Are you sure you want to delete these files?", 
                            L"Deleting Files", MB_YESNO | MB_ICONEXCLAMATION);
                        if (iRet == IDNO)
                            return TRUE;

                        // Go through the list backward because after deleting
                        // an item the indices change for every subsequent 
                        // item. By going backward, the indices are never 
                        // invalidated. 
                        for (i = cSelItemsInBuffer - 1; i >= 0; i--) 
                        { 
                            SendMessage(hListBox, LB_GETTEXT, 
                                        aSelItems[i], 
                                        (LPARAM) pszFileToDelete); 
 
                            fResult = DeleteFile(pszFileToDelete); 
                            if (!fResult) 
                            {                     
                                MessageBox(hDlg, L"Could not delete file.", 
                                    NULL, MB_OK);     
                            } 
                            else 
                            { 
                                SendMessage(hListBox, LB_DELETESTRING, 
                                        aSelItems[i], 0); 
                            } 
                        } 
                        SendMessage(hListBox, LB_SETCARETINDEX, 0, 0); 
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

 

 




