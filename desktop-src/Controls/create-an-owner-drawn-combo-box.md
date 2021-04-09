---
title: Erstellen eines Owner-Drawn Kombinations Felds
description: In diesem Thema wird veranschaulicht, wie ein vom Besitzer gezeichnetes Kombinations Feld verwendet wird.
ms.assetid: D866DE82-9734-4E8A-A366-5870C25B7C7B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5355dd33fe0067165308e9e6e5885b76edbe7ceb
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039641"
---
# <a name="how-to-create-an-owner-drawn-combo-box"></a>Erstellen eines Owner-Drawn Kombinations Felds

In diesem Thema wird veranschaulicht, wie ein vom Besitzer gezeichnetes Kombinations Feld verwendet wird. Das C++-Codebeispiel verwendet ein vom Besitzer gezeichnetes Dropdown-Listenfeld, um die vier Nahrungsmittelgruppen anzuzeigen, die jeweils durch eine Bitmap und einen Namen dargestellt werden. Wenn Sie eine Nahrungsmittel Gruppe auswählen, werden die Nahrungsmittel in dieser Gruppe in einer Liste angezeigt.

![Screenshot mit einem Dialogfeld mit einem Listenfeld und einem erweiterten Dropdown-Listenfeld, in dem ein Symbol und eine Bezeichnung für die einzelnen Elemente angezeigt werden](images/cscbx-01.png)

Das Dialogfeld enthält auch ein Listenfeld (idlist) und zwei Schaltflächen: **OK** (IDOK) und **Abbrechen** (IDCANCEL). Die IDOK-und IDCANCEL-Konstanten werden durch die SDK-Header Dateien definiert. Die idlist-Konstante ist in der Header Datei der Anwendung definiert, ebenso wie der Steuerelement Bezeichner idcombo. Weitere Informationen zu Dialogfeldern finden Sie unter [Dialogfelder](/windows/desktop/dlgbox/dialog-boxes).

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="step-1-create-the-owner-drawn-dialog-box"></a>Schritt 1: Erstellen des Dialog Felds "Owner-Drawn"

Das Codebeispiel verwendet die [**Dialogbox**](/windows/desktop/api/winuser/nf-winuser-dialogboxa) -Funktion, um ein modales Dialogfeld zu erstellen. In der Dialogfeld Vorlage IDD \_ sqmahlzeit werden die Fenster Stile, Schaltflächen und Steuerelement Bezeichner für das Kombinations Feld definiert. Im Kombinations Feld in diesem Beispiel werden die [**Stile \_ CBS DropDownList**](combo-box-styles.md), [**CBS \_ besitzdrawfixed**](combo-box-styles.md), [**CBS \_ Sort**](combo-box-styles.md), [**CBS \_ hasstrings**](combo-box-styles.md), [**WS \_ VScroll**](/windows/desktop/winmsg/window-styles)und [**WS \_ Tabstopp**](/windows/desktop/winmsg/window-styles) verwendet.


```C++
DialogBox(hInst, MAKEINTRESOURCE(IDD_SQMEAL), 
    hWnd, FoodDlgProc);
```



### <a name="step-2-process-the-wm_initdialog-and-wm_destroy-messages-in-a-dialog-box"></a>Schritt 2: Verarbeiten der "WM \_ InitDialog"-und "WM Destroy"- \_ Meldungen in einem Dialogfeld.

Wenn Sie ein Kombinations Feld in einem Dialogfeld verwenden, reagieren Sie in der Regel auf eine " [**WM \_ InitDialog**](/windows/desktop/dlgbox/wm-initdialog) "-Meldung, indem Sie das Kombinations Feld initialisieren. Die Anwendung lädt die für das vom Besitzer gezeichneten Kombinations Feld verwendeten Bitmaps und ruft dann die Anwendungs definierte `InitGroupList` Funktion auf, um das Kombinations Feld zu initialisieren. Außerdem wählt Sie das erste Listenelement im Kombinations Feld aus und ruft dann die Anwendungs definierte `InitFoodList` Funktion auf, um das Listenfeld zu initialisieren.

Im Beispiel handelt es sich bei dem vom Besitzer gezeichneten Kombinations Feld um ein Dropdown-Listenfeld, das die Namen der jeweiligen vier Lebensmittelgruppen enthält. `InitGroupList` Fügt den Namen der einzelnen Nahrungsmittelgruppen hinzu und verwendet die [**CB \_ -Nachricht**](cb-setitemdata.md) , um jedem Listenelement, das eine Nahrungsmittel Gruppe identifiziert, ein Bitmap-Handle zuzuordnen.

Das Listenfeld im Beispiel enthält die Namen der Nahrungsmittel in der ausgewählten Lebensmittelgruppe. **Initfoodlist** setzt den Inhalt des Listen Felds zurück und fügt dann die Namen der aktuellen nahrungsmittelauswahl in das Dropdown-Listenfeld aktuelle Nahrungsmittel Gruppe ein.


```C++
case WM_INITDIALOG:

    // Call an application-defined function to load bitmap resources.
    if (!LoadIconBitmaps())
    {
        EndDialog(hDlg, -1);
        break;
    }

    // Initialize the food groups combo box and select the first item.
    InitGroupList(hDlg);
    SendDlgItemMessage(hDlg, IDCOMBO, CB_SETCURSEL, 0, 0); 

    // Initialize the food list box and select the first item.
    InitFoodList(hDlg);
    SendDlgItemMessage(hDlg, IDLIST, LB_SETCURSEL, 0, 0); 

     return (INT_PTR)TRUE;
```



Beim Empfang der [**WM- \_**](/windows/desktop/winmsg/wm-destroy) Lösch Nachricht löscht die Anwendung die Bitmaps im vom Besitzer gezeichneten Kombinations Feld.


```C++
case WM_DESTROY:

    // Call the application-defined function to free the bitmap resources.
    DeleteIconBitmaps();
    break;
```



### <a name="step-3-process-the-wm_measureitem-message"></a>Schritt 3: Verarbeiten der "WM \_ MeasureItem"-Nachricht.

Ein vom Besitzer gezeichnetes Kombinations Feld sendet die [**WM \_ MeasureItem**](wm-measureitem.md) -Nachricht an das übergeordnete Fenster oder die entsprechende Dialogfeld Prozedur, sodass die Anwendung die Dimensionen der einzelnen Listenelemente festlegen kann. Da das Kombinations Feld "Beispiel" den Typ " [**CBS \_ besitzdrawfixed**](combo-box-styles.md) " hat, sendet das System die " **WM \_ MeasureItem** "-Meldung nur einmal. Kombinations Felder mit dem CBS-Besitzer " [**\_ besitzdrawvariable**](combo-box-styles.md) " senden eine **WM \_ MeasureItem** -Nachricht für jedes Listenelement.

Der *LPARAM* -Parameter ist ein Zeiger auf eine [**measureitemstruct**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) -Struktur, die das Steuerelement und das Listenelement identifiziert. Sie enthält auch die Standardabmessungen des Listen Elements. Im Beispiel wird der **ItemHeight** -Strukturmember geändert, um sicherzustellen, dass die Listenelemente hoch genug sind, um die Bitmaps der Nahrungsmittel Gruppe aufzunehmen.


```C++
case WM_MEASUREITEM:
    {
    // Set the height of the items in the food groups combo box.
    LPMEASUREITEMSTRUCT lpmis = (LPMEASUREITEMSTRUCT) lParam;

    if (lpmis->itemHeight < CY_BITMAP + 2)
        lpmis->itemHeight = CY_BITMAP + 2;

    break;
    }
```



### <a name="step-4-process-the-wm_drawitem-message"></a>Schritt 4: Verarbeiten der WM- \_ DrawItem-Nachricht.

Ein vom Besitzer gezeichnetes Kombinations Feld sendet die [**WM \_ DrawItem**](wm-drawitem.md) -Nachricht an das übergeordnete Fenster oder die entsprechende Dialogfeld Prozedur, wenn die Anwendung ein Listenelement neu zeichnen muss. Der *LPARAM* -Parameter ist ein Zeiger auf eine [**drawitemstruct**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) -Struktur, die das Steuerelement und das Listenelement identifiziert. Sie enthält außerdem Informationen, die zum Zeichnen des Elements erforderlich sind.

Die Beispielanwendung zeigt den Listenelement Text und die Bitmap an, die der Nahrungsmittel Gruppe zugeordnet ist. Wenn das Element den Fokus besitzt, zeichnet es auch ein Fokus Rechteck. Bevor der Text angezeigt wird, werden im Beispiel die Vordergrund-und Hintergrundfarben basierend auf dem ausgewählten Element festgelegt. Da das Kombinations Feld den [**CBS \_ hasstrings**](combo-box-styles.md) -Stil hat, verwaltet das Kombinations Feld den Text für jedes Listenelement, das mithilfe der [**CB \_ getlbtext**](cb-getlbtext.md) -Nachricht abgerufen werden kann.

Welche Bitmaps für das Listenelement verwendet werden, hängt von der Nahrungsmittel Gruppe ab. `InitGroupList` verwendet die CB-Eigenschaft " [**\_ logdata**](cb-setitemdata.md) ", um jedem Listenelement ein Bitmap-Handle zuzuordnen. Die Fenster Prozedur ruft das Bitmap-Handle aus dem **ItemData** -Member der [**drawitemstruct**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) -Struktur ab. Das System verwendet zwei Bitmaps für jedes Lebensmittelgruppen Symbol: eine monochrome Bitmap mit dem srcand-Raster Vorgang zum Löschen des unregelmäßigen Bereichs hinter dem Bild und eine Farb Bitmap mit dem srcpaint-Raster Vorgang zum Zeichnen des Bilds.


```C++
case WM_DRAWITEM:
    {
    COLORREF clrBackground;
    COLORREF clrForeground;
    TEXTMETRIC tm;
    int x;
    int y;
    HRESULT hr;
    size_t cch;

    LPDRAWITEMSTRUCT lpdis = (LPDRAWITEMSTRUCT) lParam;
       
    if (lpdis->itemID == -1) // Empty item)
        break;

    // Get the food icon from the item data.
    hbmIcon = (HBITMAP) lpdis->itemData;

    // The colors depend on whether the item is selected.
    clrForeground = SetTextColor(lpdis->hDC, 
        GetSysColor(lpdis->itemState & ODS_SELECTED ?
        COLOR_HIGHLIGHTTEXT : COLOR_WINDOWTEXT));

    clrBackground = SetBkColor(lpdis->hDC, 
        GetSysColor(lpdis->itemState & ODS_SELECTED ?
        COLOR_HIGHLIGHT : COLOR_WINDOW));

    // Calculate the vertical and horizontal position.
    GetTextMetrics(lpdis->hDC, &tm);
    y = (lpdis->rcItem.bottom + lpdis->rcItem.top - tm.tmHeight) / 2;
    x = LOWORD(GetDialogBaseUnits()) / 4;

    // Get and display the text for the list item.
    SendMessage(lpdis->hwndItem, CB_GETLBTEXT,
        lpdis->itemID, (LPARAM) achTemp);

    hr = StringCchLength(achTemp, 256, &cch);
    if (FAILED(hr))
    {
        // TODO: Write error handler.
    }

    ExtTextOut(lpdis->hDC, CX_BITMAP + 2 * x, y,
        ETO_CLIPPED | ETO_OPAQUE, &lpdis->rcItem,
        achTemp, (UINT)cch, NULL);

    // Restore the previous colors.
    SetTextColor(lpdis->hDC, clrForeground);
    SetBkColor(lpdis->hDC, clrBackground);
    
    //  Draw the food icon for the item. 
    HDC hdc = CreateCompatibleDC(lpdis->hDC); 
    if (hdc == NULL) 
        break; 
 
    SelectObject(hdc, hbmMask); 
    BitBlt(lpdis->hDC, x, lpdis->rcItem.top + 1, 
        CX_BITMAP, CY_BITMAP, hdc, 0, 0, SRCAND); 
 
    SelectObject(hdc, hbmIcon); 
    BitBlt(lpdis->hDC, x, lpdis->rcItem.top + 1, 
        CX_BITMAP, CY_BITMAP, hdc, 0, 0, SRCPAINT); 
 
    DeleteDC(hdc); 
  
    // If the item has the focus, draw the focus rectangle.
    if (lpdis->itemState & ODS_FOCUS)
        DrawFocusRect(lpdis->hDC, &lpdis->rcItem);

    break;
    }
```



### <a name="step-5-process-the-wm_command-message"></a>Schritt 5: Verarbeiten der WM- \_ Befehls Meldung.

Wenn ein Ereignis in einem Dialogfeld-Steuerelement auftritt, benachrichtigt das-Steuerelement die Dialogfeld Prozedur mithilfe einer [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung. Im Beispiel werden Benachrichtigungs Meldungen aus dem Kombinations Feld, dem Listenfeld und der Schaltfläche **OK** verarbeitet. Der Bezeichner des Steuer Elements befindet sich im nieder wertigen Wort von *wParam*, und der Benachrichtigungs Code befindet sich im höherwertigen Wort von *wParam*.

Wenn der Steuerelement Bezeichner idcombo ist, ist im Kombinations Feld ein Ereignis aufgetreten. In der Antwort ignoriert die Dialogfeld Prozedur alle anderen Kombinations Feld Ereignisse außer [**CBN \_ selendok**](cbn-selendok.md), das angibt, dass eine Auswahl getroffen wurde, das Dropdown-Listenfeld geschlossen wurde und die vorgenommenen Änderungen akzeptiert werden sollen. Die Dialogfeld Prozedur ruft `InitFoodList` auf, um den Inhalt des Listen Felds zurückzusetzen und die Namen der aktuellen Auswahl im Dropdown-Listenfeld hinzuzufügen.

Wenn der Steuerelement Bezeichner "idlist" ist, ist im Listenfeld ein Ereignis aufgetreten. Dies bewirkt, dass die Dialogfeld Prozedur alle Listenfeld Ereignisse außer [**LBN \_ dblclk**](lbn-dblclk.md)ignoriert, was darauf hinweist, dass der Benutzer auf ein Listenelement Doppel geklickt hat. Dieses Ereignis wird auf die gleiche Weise verarbeitet, wie wenn eine Schaltfläche " **OK** " ausgewählt wurde.

Wenn der Steuerelement Bezeichner IDOK ist, hat der Benutzer die Schaltfläche **OK** ausgewählt. In der Antwort fügt die Dialogfeld Prozedur den Namen des ausgewählten Nahrungsmittel in das mehrzeilige Bearbeitungs Steuerelement der Anwendung ein und ruft dann die [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) -Funktion auf, um das Dialogfeld zu schließen.

Wenn der Steuerelement Bezeichner IDCANCEL ist, hat der Benutzer auf die Schaltfläche " **Abbrechen** " geklickt. In der Antwort Ruft die Dialogfeld Prozedur [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) auf, um das Dialogfeld zu schließen.


```C++
case WM_COMMAND:
        switch (LOWORD(wParam)) 
        { 
            case IDCOMBO: 
                if (HIWORD(wParam) == CBN_SELENDOK) 
                { 
                    InitFoodList(hDlg); 
                    SendDlgItemMessage(hDlg, IDLIST, 
                        LB_SETCURSEL, 0, 0); 
                } 
                break; 
 
            case IDLIST: 
                if (HIWORD(wParam) != LBN_DBLCLK) 
                    break; 
 
            // For a double-click, process the OK case. 
            case IDOK: 
 
                // Get the text for the selected list item. 
                hwnd = GetDlgItem(hDlg, IDLIST); 

                // Here it is assumed the text can fit into achTemp.
                // If there is doubt, call LB_GETTEXTLENGTH first.
                SendMessage(hwnd, LB_GETTEXT, 
                    SendMessage(hwnd, LB_GETCURSEL, 0, 0), 
                    (LPARAM) achTemp); 
 
                // TODO: Do something with the selected text.
 
                EndDialog(hDlg, 0); 
                break; 
 
            case IDCANCEL: 
                hwnd = GetDlgItem(hDlg, IDCOMBO); 
                if (SendMessage(hwnd, CB_GETDROPPEDSTATE, 0, 0)) 
                    SendMessage(hwnd, CB_SHOWDROPDOWN, FALSE, 0); 
                else EndDialog(hDlg, 0); 
        } 
        break; 
```



## <a name="complete-example"></a>Vollständiges Beispiel

Im folgenden finden Sie die Dialogfeld Prozedur und die unterstützenden Funktionen für das Dialogfeld **quadratische Mahlzeit** .


```C++
#define ID_BREAD 0
#define ID_DAIRY 1
#define ID_FRUIT 2
#define ID_MEAT  3

#define CX_BITMAP 24
#define CY_BITMAP 24

HBITMAP hbmBread;
HBITMAP hbmDairy;
HBITMAP hbmMeat;
HBITMAP hbmFruit;
HBITMAP hbmMask;

HBITMAP hbmIcon;
```

```C++
// Message handler for Square Meal dialog box.
INT_PTR CALLBACK FoodDlgProc(HWND hDlg, UINT message, WPARAM wParam, 
    LPARAM lParam)
{
    UNREFERENCED_PARAMETER(lParam);
    TCHAR achTemp[256];
    HWND hwnd;

    switch (message)
    {
    case WM_INITDIALOG:

        // Call an application-defined function to load bitmap resources.
        if (!LoadIconBitmaps())
        {
            EndDialog(hDlg, -1);
            break;
        }

        // Initialize the food groups combo box and select the first item.
        InitGroupList(hDlg);
        SendDlgItemMessage(hDlg, IDCOMBO, CB_SETCURSEL, 0, 0); 

        // Initialize the food list box and select the first item.
        InitFoodList(hDlg);
        SendDlgItemMessage(hDlg, IDLIST, LB_SETCURSEL, 0, 0); 

         return (INT_PTR)TRUE;
   
    case WM_MEASUREITEM:
        {
        // Set the height of the items in the food groups combo box.
        LPMEASUREITEMSTRUCT lpmis = (LPMEASUREITEMSTRUCT) lParam;

        if (lpmis->itemHeight < CY_BITMAP + 2)
            lpmis->itemHeight = CY_BITMAP + 2;

        break;
        }

    case WM_DRAWITEM:
        {
        COLORREF clrBackground;
        COLORREF clrForeground;
        TEXTMETRIC tm;
        int x;
        int y;
        HRESULT hr;
        size_t cch;

        LPDRAWITEMSTRUCT lpdis = (LPDRAWITEMSTRUCT) lParam;
           
        if (lpdis->itemID == -1) // Empty item)
            break;

        // Get the food icon from the item data.
        hbmIcon = (HBITMAP) lpdis->itemData;

        // The colors depend on whether the item is selected.
        clrForeground = SetTextColor(lpdis->hDC, 
            GetSysColor(lpdis->itemState & ODS_SELECTED ?
            COLOR_HIGHLIGHTTEXT : COLOR_WINDOWTEXT));

        clrBackground = SetBkColor(lpdis->hDC, 
            GetSysColor(lpdis->itemState & ODS_SELECTED ?
            COLOR_HIGHLIGHT : COLOR_WINDOW));

        // Calculate the vertical and horizontal position.
        GetTextMetrics(lpdis->hDC, &tm);
        y = (lpdis->rcItem.bottom + lpdis->rcItem.top - tm.tmHeight) / 2;
        x = LOWORD(GetDialogBaseUnits()) / 4;

        // Get and display the text for the list item.
        SendMessage(lpdis->hwndItem, CB_GETLBTEXT,
            lpdis->itemID, (LPARAM) achTemp);

        hr = StringCchLength(achTemp, 256, &cch);
        if (FAILED(hr))
        {
            // TODO: Write error handler.
        }

        ExtTextOut(lpdis->hDC, CX_BITMAP + 2 * x, y,
            ETO_CLIPPED | ETO_OPAQUE, &lpdis->rcItem,
            achTemp, (UINT)cch, NULL);

        // Restore the previous colors.
        SetTextColor(lpdis->hDC, clrForeground);
        SetBkColor(lpdis->hDC, clrBackground);
        
        //  Draw the food icon for the item. 
        HDC hdc = CreateCompatibleDC(lpdis->hDC); 
        if (hdc == NULL) 
            break; 
 
        SelectObject(hdc, hbmMask); 
        BitBlt(lpdis->hDC, x, lpdis->rcItem.top + 1, 
            CX_BITMAP, CY_BITMAP, hdc, 0, 0, SRCAND); 
 
        SelectObject(hdc, hbmIcon); 
        BitBlt(lpdis->hDC, x, lpdis->rcItem.top + 1, 
            CX_BITMAP, CY_BITMAP, hdc, 0, 0, SRCPAINT); 
 
        DeleteDC(hdc); 
      
        // If the item has the focus, draw the focus rectangle.
        if (lpdis->itemState & ODS_FOCUS)
            DrawFocusRect(lpdis->hDC, &lpdis->rcItem);

        break;
        }

    case WM_COMMAND:
            switch (LOWORD(wParam)) 
            { 
                case IDCOMBO: 
                    if (HIWORD(wParam) == CBN_SELENDOK) 
                    { 
                        InitFoodList(hDlg); 
                        SendDlgItemMessage(hDlg, IDLIST, 
                            LB_SETCURSEL, 0, 0); 
                    } 
                    break; 
 
                case IDLIST: 
                    if (HIWORD(wParam) != LBN_DBLCLK) 
                        break; 
 
                // For a double-click, process the OK case. 
                case IDOK: 
 
                    // Get the text for the selected list item. 
                    hwnd = GetDlgItem(hDlg, IDLIST); 

                    // Here it is assumed the text can fit into achTemp.
                    // If there is doubt, call LB_GETTEXTLENGTH first.
                    SendMessage(hwnd, LB_GETTEXT, 
                        SendMessage(hwnd, LB_GETCURSEL, 0, 0), 
                        (LPARAM) achTemp); 
 
                    // TODO: Do something with the selected text.
 
                    EndDialog(hDlg, 0); 
                    break; 
 
                case IDCANCEL: 
                    hwnd = GetDlgItem(hDlg, IDCOMBO); 
                    if (SendMessage(hwnd, CB_GETDROPPEDSTATE, 0, 0)) 
                        SendMessage(hwnd, CB_SHOWDROPDOWN, FALSE, 0); 
                    else EndDialog(hDlg, 0); 
            } 
            break; 

    case WM_DESTROY:

        // Call the application-defined function to free the bitmap resources.
        DeleteIconBitmaps();
        break;
    }
    return (INT_PTR)FALSE;
}

// Loads string resources and adds them as items to the drop-down list of
//   the food groups combo box. The bitmap handle of each item&#39;s icon is
//   stored as item data for easy access when the item needs to be drawn.
// 
void InitGroupList(HWND hDlg)
{
    TCHAR achTemp[256];
    DWORD dwIndex;

    // Get the handle of the food groups combo box.
    HWND hwndGroupsBox = GetDlgItem(hDlg, IDCOMBO);

    LoadString(hInst, IDS_BREAD, achTemp, sizeof(achTemp)/sizeof(TCHAR));
    dwIndex = SendMessage(hwndGroupsBox, CB_ADDSTRING, 0, (LPARAM) achTemp);
    SendMessage(hwndGroupsBox, CB_SETITEMDATA, dwIndex, (LPARAM) hbmBread);
    
    LoadString(hInst, IDS_DAIRY, achTemp, sizeof(achTemp)/sizeof(TCHAR)); 
    dwIndex = SendMessage(hwndGroupsBox, CB_ADDSTRING, 0, (LPARAM) achTemp);
    SendMessage(hwndGroupsBox, CB_SETITEMDATA, dwIndex, (LPARAM) hbmDairy);

    LoadString(hInst, IDS_FRUIT, achTemp, sizeof(achTemp)/sizeof(TCHAR));
    dwIndex = SendMessage(hwndGroupsBox, CB_ADDSTRING, 0, (LPARAM) achTemp);
    SendMessage(hwndGroupsBox, CB_SETITEMDATA, dwIndex, (LPARAM) hbmFruit); 

    LoadString(hInst, IDS_MEAT, achTemp, sizeof(achTemp)/sizeof(TCHAR)); 
    dwIndex = SendMessage(hwndGroupsBox, CB_ADDSTRING, 0, (LPARAM) achTemp);
    SendMessage(hwndGroupsBox, CB_SETITEMDATA, dwIndex, (LPARAM) hbmMeat);

    return;
}

// Fills the food list based on the selected item in the food groups
//   combo box.
void InitFoodList(HWND hDlg)
{
    TCHAR achTemp[256];

    HWND hwndGroupsBox = GetDlgItem(hDlg, IDCOMBO);
    HWND hwndFoodList = GetDlgItem(hDlg, IDLIST);

    // Clear the list contents.
    SendMessage(hwndFoodList, LB_RESETCONTENT, 0, 0);

    // Find out which food group is selected.
    int idFoodGroup = SendMessage(hwndGroupsBox, CB_GETCURSEL, 0, 0);

    switch (idFoodGroup)
    {
    case ID_BREAD:
        LoadString(hInst, IDS_OAT, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_WHEAT, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_RYE, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);
        break;

    case ID_DAIRY:
        LoadString(hInst, IDS_CHEDDAR, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_MILK, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_PROCESSED, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_SWISS, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);
        
        break;

    case ID_FRUIT:
        LoadString(hInst, IDS_APPLES, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_BANANAS, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_ORANGES, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        break;

    case ID_MEAT:
        LoadString(hInst, IDS_BEEF, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_CHICKEN, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_PORK, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        break;

    default:
        break;
    }

    return;
}

// Loads the food icon bitmaps from the application resources.
//
BOOL LoadIconBitmaps(void)
{
    hbmBread = LoadBitmap(hInst, MAKEINTRESOURCE(IDB_BREAD));

    if (hbmBread != NULL)
         hbmDairy = LoadBitmap(hInst, MAKEINTRESOURCE(IDB_DAIRY));

    if (hbmDairy != NULL)
         hbmMeat = LoadBitmap(hInst, MAKEINTRESOURCE(IDB_MEAT));

    if (hbmMeat != NULL)
        hbmFruit = LoadBitmap(hInst, MAKEINTRESOURCE(IDB_FRUIT));
    
    if (hbmFruit != NULL)
        hbmMask = LoadBitmap(hInst, MAKEINTRESOURCE(IDB_MASK));

    if (hbmMask != NULL)
        return TRUE;
        
    return FALSE;
}

// Frees the icon bitmps.
//
void DeleteIconBitmaps(void)
{
    FreeResource(reinterpret_cast<HGLOBAL>(hbmBread));
    FreeResource(reinterpret_cast<HGLOBAL>(hbmDairy));
    FreeResource(reinterpret_cast<HGLOBAL>(hbmMeat));
    FreeResource(reinterpret_cast<HGLOBAL>(hbmFruit));
    FreeResource(reinterpret_cast<HGLOBAL>(hbmMask));
}
```


## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Kombinations Feldern](using-combo-boxes.md)
</dt> </dl>

 

 