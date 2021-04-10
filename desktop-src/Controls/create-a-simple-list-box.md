---
title: Erstellen eines einfachen Listen Felds
description: In diesem Thema wird veranschaulicht, wie Elemente aus einem einfachen Listenfeld initialisiert und abgerufen werden.
ms.assetid: 4A717010-A1D3-4FFB-8E4E-D5C4F9D8D952
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ca2230b265d61e9a59a8892e14127d25bf2cfd2
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104039851"
---
# <a name="how-to-create-a-simple-list-box"></a>Erstellen eines einfachen Listen Felds

In diesem Thema wird veranschaulicht, wie Elemente aus einem einfachen Listenfeld initialisiert und abgerufen werden.

Das C++-Codebeispiel in diesem Thema enthält eine Dialogfeld Prozedur, in der ein Listenfeld mit Informationen zu Playern in einem Sport Team ausgefüllt wird. Wenn der Benutzer den Namen eines Players aus der Liste auswählt, werden Informationen über den Player im Dialogfeld angezeigt. Der Fenster Stil für das Listenfeld enthält die [**lbs- \_ Sortierung**](list-box-styles.md), die zu einer sortierten Liste von Elementen führt. Der folgende Screenshot zeigt das Dialogfeld.

![Screenshot eines Dialog Felds mit einem beschrifteten Listenfeld, Text zum ausgewählten Listenfeld Element und einer Schaltfläche "OK"](images/lb-roster.png)

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen


Die Anwendung muss die folgenden Aufgaben im Listenfeld – Verwandte Aufgaben ausführen:

-   Listenfeld initialisieren
-   Abrufen der Auswahl des Benutzers aus dem Listenfeld

Im folgenden C++-Codebeispiel werden Informationen zu Playern in einem Array von-Strukturen gespeichert. Während der Initialisierung verwendet die Dialogfeld Prozedur die [**lb- \_ AddString**](lb-addstring.md) -Nachricht, um die Namen der Teammitglieder dem Listenfeld (**IDC- \_ ListBox- \_ Beispiel**) einzeln hinzuzufügen. Außerdem wird mit der LB-Nachricht " [**\_ abtitemdata**](lb-setitemdata.md) " der Array Index des Players als Elementdaten dem Listenfeld hinzugefügt. Wenn der Benutzer später einen Player aus dem Listenfeld auswählt, verwendet die Dialogfeld Prozedur die [**lb- \_ GetItemData**](lb-getitemdata.md) -Nachricht, um den entsprechenden Array Index abzurufen. Anschließend wird der Array Index verwendet, um Player Informationen aus dem Array abzurufen.



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

[Listenfeld-Steuerelement Verweis](bumper-list-box-list-box-control-reference.md)
</dt> <dt>

[Informationen zu Listenfeldern](about-list-boxes.md)
</dt> <dt>

[Verwenden von Listenfeldern](using-list-boxes.md)
</dt> </dl>

 

 




