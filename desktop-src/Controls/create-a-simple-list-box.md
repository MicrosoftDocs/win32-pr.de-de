---
title: Erstellen eines einfachen Listenfelds
description: In diesem Thema wird veranschaulicht, wie Elemente aus einem einfachen Listenfeld initialisiert und abgerufen werden.
ms.assetid: 4A717010-A1D3-4FFB-8E4E-D5C4F9D8D952
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83a037bfbdb5232cd30d3e13fbc251c22c18c71a76398a351939602301a745d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120063174"
---
# <a name="how-to-create-a-simple-list-box"></a>Erstellen eines einfachen Listenfelds

In diesem Thema wird veranschaulicht, wie Elemente aus einem einfachen Listenfeld initialisiert und abgerufen werden.

Das C++-Codebeispiel in diesem Thema enthält eine Dialogfeldprozedur, die ein Listenfeld mit Informationen über Spieler in einem Sportteam füllt. Wenn der Benutzer den Namen eines Players aus der Liste auswählt, werden Informationen zum Spieler im Dialogfeld angezeigt. Das Fensterformat für das Listenfeld enthält [**LBS \_ SORT,**](list-box-styles.md)was zu einer sortierten Liste von Elementen führt. Der folgende Screenshot zeigt das Dialogfeld.

![Screenshot eines Dialogfelds mit einem gekennzeichneten Listenfeld, Text zum ausgewählten Listenfeldelement und einer Schaltfläche "OK"](images/lb-roster.png)

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen


Die Anwendung muss die folgenden Aufgaben im Zusammenhang mit Listenfelden ausführen:

-   Initialisieren des Listenfelds
-   Abrufen der Benutzerauswahl aus dem Listenfeld

Im folgenden C++-Codebeispiel werden Informationen zu Playern in einem Array von -Strukturen gespeichert. Während der Initialisierung verwendet die Dialogfeldprozedur die [**LB \_ ADDSTRING-Meldung,**](lb-addstring.md) um dem Listenfeld **(IDC \_ LISTBOX \_ EXAMPLE)** nach und nach die Namen von Teammitgliedern hinzuzufügen. Außerdem wird die [**LB \_ SETITEMDATA-Nachricht**](lb-setitemdata.md) verwendet, um dem Listenfeld den Arrayindex des Players als Elementdaten hinzuzufügen. Wenn der Benutzer später einen Player aus dem Listenfeld auswählt, verwendet die Dialogfeldprozedur die [**LB \_ GETITEMDATA-Meldung,**](lb-getitemdata.md) um den entsprechenden Arrayindex abzurufen. Anschließend wird der Arrayindex verwendet, um Playerinformationen aus dem Array abzurufen.



```C++
typedef struct 
{ 
    TCHAR achName[MAX_PATH]; 
    TCHAR achPosition[12]; 
    int nGamesPlayed; 
    int nGoalsScored; 
} Player; 

Player Roster[] = 
{ 
    {TEXT("Haas, Jonathan"), TEXT("Midfield"), 18, 4 }, 
    {TEXT("Pai, Jyothi"), TEXT("Forward"), 36, 12 }, 
    {TEXT("Hanif, Kerim"), TEXT("Back"), 26, 0 }, 
    {TEXT("Anderberg, Michael"), TEXT("Back"), 24, 2 }, 
    {TEXT("Jelitto, Jacek"), TEXT("Midfield"), 26, 3 }, 
    {TEXT("Raposo, Rui"), TEXT("Back"), 24, 3}, 
    {TEXT("Joseph, Brad"), TEXT("Forward"), 13, 3 }, 
    {TEXT("Bouchard, Thomas"), TEXT("Forward"), 28, 5 }, 
    {TEXT("Salmre, Ivo "), TEXT("Midfield"), 27, 7 }, 
    {TEXT("Camp, David"), TEXT("Midfield"), 22, 3 }, 
    {TEXT("Kohl, Franz"), TEXT("Goalkeeper"), 17, 0 }, 
}; 


INT_PTR CALLBACK ListBoxExampleProc(HWND hDlg, UINT message, 
        WPARAM wParam, LPARAM lParam)
{
    switch (message)
    {
    case WM_INITDIALOG:
        {
            // Add items to list. 
            HWND hwndList = GetDlgItem(hDlg, IDC_LISTBOX_EXAMPLE);  
            for (int i = 0; i < ARRAYSIZE(Roster); i++) 
            { 
                int pos = (int)SendMessage(hwndList, LB_ADDSTRING, 0, 
                    (LPARAM) Roster[i].achName); 
                // Set the array index of the player as item data.
                // This enables us to retrieve the item from the array
                // even after the items are sorted by the list box.
                SendMessage(hwndList, LB_SETITEMDATA, pos, (LPARAM) i); 
            } 
            // Set input focus to the list box.
            SetFocus(hwndList); 
            return TRUE;               
        } 

    case WM_COMMAND:
        switch (LOWORD(wParam))
        {
        case IDOK:
        case IDCANCEL:
            EndDialog(hDlg, LOWORD(wParam));
            return TRUE;

        case IDC_LISTBOX_EXAMPLE:
            {
                switch (HIWORD(wParam)) 
                { 
                case LBN_SELCHANGE:
                    {
                        HWND hwndList = GetDlgItem(hDlg, IDC_LISTBOX_EXAMPLE); 

                        // Get selected index.
                        int lbItem = (int)SendMessage(hwndList, LB_GETCURSEL, 0, 0); 

                        // Get item data.
                        int i = (int)SendMessage(hwndList, LB_GETITEMDATA, lbItem, 0);

                        // Do something with the data from Roster[i]
                        TCHAR buff[MAX_PATH];
                        StringCbPrintf (buff, ARRAYSIZE(buff),  
                            TEXT("Position: %s\nGames played: %d\nGoals: %d"), 
                            Roster[i].achPosition, Roster[i].nGamesPlayed, 
                            Roster[i].nGoalsScored);

                        SetDlgItemText(hDlg, IDC_STATISTICS, buff); 
                        return TRUE; 
                    } 
                }
            }
            return TRUE;
        }
    }
    return FALSE;
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

 

 




