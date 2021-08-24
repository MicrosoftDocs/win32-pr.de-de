---
title: Erstellen eines Owner-Drawn Kombinationsfelds
description: In diesem Thema wird die Verwendung eines vom Besitzer gezeichneten Kombinationsfelds veranschaulicht.
ms.assetid: D866DE82-9734-4E8A-A366-5870C25B7C7B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e90d82192e485e4f833157a1c3ab75e8e39446e1e80f7f9cc27baf5444b4e0bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826465"
---
# <a name="how-to-create-an-owner-drawn-combo-box"></a>Erstellen eines Owner-Drawn Kombinationsfelds

In diesem Thema wird die Verwendung eines vom Besitzer gezeichneten Kombinationsfelds veranschaulicht. Im C++-Codebeispiel wird ein vom Besitzer gezeichnetes Dropdownlistenfeld verwendet, um die vier Lebensmittelgruppen anzuzeigen, die jeweils durch eine Bitmap und einen Namen dargestellt werden. Wenn Sie eine Lebensmittelgruppe auswählen, werden die Lebensmittel in dieser Gruppe in einer Liste angezeigt.

![Screenshot eines Dialogfelds mit einem Listenfeld und einem erweiterten Dropdownlistenfeld mit einem Symbol und einer Bezeichnung für jedes Element](images/cscbx-01.png)

Das Dialogfeld enthält auch ein Listenfeld (IDLIST) und zwei Schaltflächen: **OK** (IDOK) und **Abbrechen** (IDCANCEL). Die KONSTANTEN IDOK und IDCANCEL werden durch die SDK-Headerdateien definiert. Die konstante IDLIST wird in der Headerdatei der Anwendung definiert, ebenso wie der Steuerelementbezeichner IDCOMBO. Weitere Informationen zu Dialogfeldern finden Sie unter [Dialogfelder.](/windows/desktop/dlgbox/dialog-boxes)

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen

### <a name="step-1-create-the-owner-drawn-dialog-box"></a>Schritt 1: Erstellen des dialogfelds "Owner-Drawn"

Im Codebeispiel wird die [**DialogBox-Funktion**](/windows/desktop/api/winuser/nf-winuser-dialogboxa) verwendet, um ein modales Dialogfeld zu erstellen. Die Dialogfeldvorlage IDD \_ SQMEAL definiert die Fensterstile, Schaltflächen und Steuerelementbezeichner für das Kombinationsfeld. Das Kombinationsfeld in diesem Beispiel verwendet die Formate [**CBS \_ DROPDOWNLIST,**](combo-box-styles.md) [**CBS \_ OWNERDRAWFIXED,**](combo-box-styles.md) [**CBS \_ SORT,**](combo-box-styles.md) [**CBS \_ HASSTRINGS,**](combo-box-styles.md) [**WS \_ VSCROLL**](/windows/desktop/winmsg/window-styles)und [**WS \_ TABSTOP.**](/windows/desktop/winmsg/window-styles)


```C++
DialogBox(hInst, MAKEINTRESOURCE(IDD_SQMEAL), 
    hWnd, FoodDlgProc);
```



### <a name="step-2-process-the-wm_initdialog-and-wm_destroy-messages-in-a-dialog-box"></a>Schritt 2: Verarbeiten der \_ WM INITDIALOG- und WM \_ DESTROY-Meldungen in einem Dialogfeld.

Wenn Sie ein Kombinationsfeld in einem Dialogfeld verwenden, reagieren Sie in der Regel auf eine [**WM \_ INITDIALOG-Meldung,**](/windows/desktop/dlgbox/wm-initdialog) indem Sie das Kombinationsfeld initialisieren. Die Anwendung lädt die Bitmaps, die für das vom Besitzer gezeichnete Kombinationsfeld verwendet werden, und ruft dann die anwendungsdefinierte `InitGroupList` Funktion auf, um das Kombinationsfeld zu initialisieren. Außerdem wählt er das erste Listenelement im Kombinationsfeld aus und ruft dann die anwendungsdefinierte `InitFoodList` Funktion auf, um das Listenfeld zu initialisieren.

Im Beispiel ist das vom Besitzer gezeichnete Kombinationsfeld ein Dropdownlistenfeld, das die Namen jeder der vier Lebensmittelgruppen enthält. `InitGroupList` fügt den Namen jeder Lebensmittelgruppe hinzu und verwendet die [**CB \_ SETITEMDATA-Nachricht,**](cb-setitemdata.md) um jedem Listenelement, das eine Lebensmittelgruppe identifiziert, ein Bitmaphandle zuzuordnen.

Das Listenfeld im Beispiel enthält die Namen der Lebensmittel in der ausgewählten Lebensmittelgruppe. **InitAturList** setzt den Inhalt des Listenfelds zurück und fügt dann die Namen der aktuellen Lebensmittelauswahl in das Dropdown-Listenfeld der aktuellen Lebensmittelgruppe ein.


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



Wenn die [**WM \_ DESTROY-Nachricht**](/windows/desktop/winmsg/wm-destroy) empfangen wird, löscht die Anwendung die Bitmaps im vom Besitzer gezeichneten Kombinationsfeld.


```C++
case WM_DESTROY:

    // Call the application-defined function to free the bitmap resources.
    DeleteIconBitmaps();
    break;
```



### <a name="step-3-process-the-wm_measureitem-message"></a>Schritt 3: Verarbeiten der WM \_ MEASUREITEM-Nachricht.

Ein vom Besitzer gezeichnetes Kombinationsfeld sendet die [**WM \_ MEASUREITEM-Meldung**](wm-measureitem.md) an das übergeordnete Fenster oder die Dialogfeldprozedur, sodass die Anwendung die Dimensionen der einzelnen Listenelement festlegen kann. Da das Beispielkombinationsfeld den [**CBS \_ OWNERDRAWFIXED-Stil aufwies,**](combo-box-styles.md) sendet das System die **WM \_ MEASUREITEM-Nachricht** nur einmal. Kombinationsfelder mit dem [**FORMAT CBS \_ OWNERDRAWVARIABLE**](combo-box-styles.md) senden eine **WM \_ MEASUREITEM-Nachricht** für jedes Listenelement.

Der *lParam-Parameter* ist ein Zeiger auf eine [**MEASUREITEMSTRUCT-Struktur,**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) die das Steuerelement und das Listenelement identifiziert. Sie enthält auch die Standarddimensionen des Listenelements. Im Beispiel wird das **elementHeight-Strukturelement** geändert, um sicherzustellen, dass die Listenelemente hoch genug sind, um die Bitmaps für Lebensmittelgruppen aufzunehmen.


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



### <a name="step-4-process-the-wm_drawitem-message"></a>Schritt 4: Verarbeiten der WM \_ DRAWITEM-Nachricht.

Ein vom Besitzer gezeichnetes Kombinationsfeld sendet die [**WM \_ DRAWITEM-Meldung**](wm-drawitem.md) jedes Mal an das übergeordnete Fenster oder die Dialogfeldprozedur, wenn die Anwendung ein Listenelement neu zeichnen muss. Der *lParam-Parameter* ist ein Zeiger auf eine [**DRAWITEMSTRUCT-Struktur,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) die das Steuerelement und das Listenelement identifiziert. Sie enthält auch Informationen, die zum Zeichnen des Elements erforderlich sind.

Die Beispielanwendung zeigt den Listenelementtext und die Bitmap an, die der Lebensmittelgruppe zugeordnet ist. Wenn das Element den Fokus besitzt, zeichnet es auch ein Fokusrechteck. Bevor der Text angezeigt wird, legt das Beispiel die Vordergrund- und Hintergrundfarben basierend auf dem ausgewählten Element fest. Da das Kombinationsfeld den [**CBS \_ HASSTRINGS-Stil**](combo-box-styles.md) hat, behält das Kombinationsfeld den Text für jedes Listenelement bei, das mithilfe der [**CB \_ GETLBTEXT-Nachricht**](cb-getlbtext.md) abgerufen werden kann.

Welche Bitmaps für das Listenelement verwendet werden, hängt von der Lebensmittelgruppe ab. `InitGroupList` verwendet die [**CB \_ SETITEMDATA-Nachricht,**](cb-setitemdata.md) um jedem Listenelement ein Bitmaphandle zuzuordnen. Die Fensterprozedur ruft das Bitmaphandle aus dem **itemData-Member** der [**DRAWITEMSTRUCT-Struktur**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) ab. Das System verwendet zwei Bitmaps für jedes Lebensmittelgruppensymbol: eine monocolore Bitmap mit dem SRCAND-Rastervorgang, um den unregelmäßigen Bereich hinter dem Bild zu löschen, und eine Farbbitmap mit dem SRCPAINT-Rastervorgang, um das Bild zu zeichnen.


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



### <a name="step-5-process-the-wm_command-message"></a>Schritt 5: Verarbeiten der WM \_ COMMAND-Nachricht.

Wenn ein Ereignis in einem Dialogfeldsteuerelement auftritt, benachrichtigt das Steuerelement die Dialogfeldprozedur mithilfe einer [**WM \_ COMMAND-Meldung.**](/windows/desktop/menurc/wm-command) Im Beispiel werden Benachrichtigungsmeldungen aus dem Kombinationsfeld, dem Listenfeld und der Schaltfläche **OK** verarbeitet. Der Steuerelementbezeichner befindet sich im Wort mit niedriger Reihenfolge von *wParam,* und der Benachrichtigungscode befindet sich im Wort in hoher Reihenfolge von *wParam.*

Wenn der Steuerelementbezeichner IDCOMBO ist, ist im Kombinationsfeld ein Ereignis aufgetreten. Als Reaktion ignoriert die Dialogfeldprozedur alle anderen Kombinationsfeldereignisse außer [**CBN \_ SELENDOK.**](cbn-selendok.md)Dies gibt an, dass eine Auswahl getroffen wurde, das Dropdownlistenfeld geschlossen wurde und die vorgenommenen Änderungen akzeptiert werden sollten. Die Dialogfeldprozedur ruft `InitFoodList` auf, um den Inhalt des Listenfelds zurückzusetzen und die Namen der aktuellen Auswahl im Dropdownlistenfeld hinzuzufügen.

Wenn der Steuerelementbezeichner IDLIST ist, ist ein Ereignis im Listenfeld aufgetreten. Dies bewirkt, dass die Dialogfeldprozedur alle Listenfeldereignisse außer [**LBN \_ DBLCLK**](lbn-dblclk.md)ignoriert. Dies gibt an, dass der Benutzer auf ein Listenelement doppelklickt. Dieses Ereignis wird auf die gleiche Weise verarbeitet, als ob eine SCHALTFLÄCHE **OK** ausgewählt worden wäre.

Wenn der Steuerelementbezeichner IDOK ist, hat der Benutzer die Schaltfläche **OK** ausgewählt. Als Antwort fügt die Dialogfeldprozedur den Namen des ausgewählten Essens in das Mehrzeilen-Bearbeitungssteuerelement der Anwendung ein und ruft dann die [**EndDialog-Funktion**](/windows/desktop/api/winuser/nf-winuser-enddialog) auf, um das Dialogfeld zu schließen.

Wenn der Steuerelementbezeichner IDCANCEL ist, hat der Benutzer auf die Schaltfläche **Abbrechen** geklickt. Als Antwort ruft die Dialogfeldprozedur [**EndDialog auf,**](/windows/desktop/api/winuser/nf-winuser-enddialog) um das Dialogfeld zu schließen.


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

Im Folgenden werden die Dialogfeldprozedur und die unterstützenden Funktionen für das Dialogfeld **Square Menu** angezeigt.


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

[Verwenden von Kombinationsfeldern](using-combo-boxes.md)
</dt> </dl>

 

 