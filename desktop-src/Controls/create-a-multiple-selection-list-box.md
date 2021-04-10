---
title: So erstellen Sie ein Multiple-Selection Listenfeld
description: In diesem Thema wird veranschaulicht, wie Sie den Inhalt eines Verzeichnisses in einem Listenfeld Mehrfachauswahl anzeigen und darauf zugreifen können.
ms.assetid: 5192E171-8CEF-4921-9378-A7C3A52A9024
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abd47b1d582d53a66bc77284927aef4230043e92
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104039857"
---
# <a name="how-to-create-a-multiple-selection-list-box"></a>So erstellen Sie ein Multiple-Selection Listenfeld

In diesem Thema wird veranschaulicht, wie Sie den Inhalt eines Verzeichnisses in einem Listenfeld Mehrfachauswahl anzeigen und darauf zugreifen können. Im Listenfeld Mehrfachauswahl kann der Benutzer mehrere Elemente gleichzeitig auswählen.

Mit dem C++-Codebeispiel in diesem Thema kann ein Benutzer eine Liste der Dateien im aktuellen Verzeichnis anzeigen, eine Gruppe von Dateien aus der Liste auswählen und diese löschen.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen


Die Verzeichnis Auflistungs Anwendung muss die folgenden Aufgaben im Listenfeld – Verwandte Aufgaben ausführen:

-   Initialisieren Sie das Listenfeld.
-   Rufen Sie die Auswahl des Benutzers aus dem Listenfeld ab.
-   Entfernen Sie die Dateinamen aus dem Listenfeld, nachdem die ausgewählten Dateien gelöscht wurden.

Im folgenden C++-Codebeispiel initialisiert die Dialogfeld Prozedur das Listenfeld Mehrfachauswahl (IDC \_ FileList) mithilfe der [**dlgdirlist**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) -Funktion, um das Listenfeld mit den Namen aller Dateien im aktuellen Verzeichnis auszufüllen.

Wenn der Benutzer eine Gruppe von Dateien auswählt und auf die Schaltfläche **Löschen** klickt, sendet die Dialogfeld Prozedur die [**lb- \_ getselcount**](lb-getselcount.md) -Nachricht, um die Anzahl ausgewählter Dateien abzurufen, und die [**lb \_ getselitems**](lb-getselitems.md) -Nachricht, um ein Array ausgewählter Listenfeld Elemente abzurufen. Nach dem Löschen einer Datei entfernt die Dialogfeld Prozedur das entsprechende Element aus dem Listenfeld, indem die [**lb- \_ deletestring**](lb-deletestring.md) -Nachricht gesendet wird.



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

[Listenfeld-Steuerelement Verweis](bumper-list-box-list-box-control-reference.md)
</dt> <dt>

[Informationen zu Listenfeldern](about-list-boxes.md)
</dt> <dt>

[Verwenden von Listenfeldern](using-list-boxes.md)
</dt> </dl>

 

 




