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
# <a name="how-to-create-an-owner-drawn-combo-box"></a><span data-ttu-id="37e99-103">Erstellen eines Owner-Drawn Kombinations Felds</span><span class="sxs-lookup"><span data-stu-id="37e99-103">How to Create an Owner-Drawn Combo Box</span></span>

<span data-ttu-id="37e99-104">In diesem Thema wird veranschaulicht, wie ein vom Besitzer gezeichnetes Kombinations Feld verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="37e99-104">This topic demonstrates how to use an owner-drawn combo box.</span></span> <span data-ttu-id="37e99-105">Das C++-Codebeispiel verwendet ein vom Besitzer gezeichnetes Dropdown-Listenfeld, um die vier Nahrungsmittelgruppen anzuzeigen, die jeweils durch eine Bitmap und einen Namen dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="37e99-105">The C++ code example uses an owner-drawn drop-down list box to display the four food groups, each represented by a bitmap and a name.</span></span> <span data-ttu-id="37e99-106">Wenn Sie eine Nahrungsmittel Gruppe auswählen, werden die Nahrungsmittel in dieser Gruppe in einer Liste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="37e99-106">Selecting a food group causes the foods in that group to appear in a list.</span></span>

![Screenshot mit einem Dialogfeld mit einem Listenfeld und einem erweiterten Dropdown-Listenfeld, in dem ein Symbol und eine Bezeichnung für die einzelnen Elemente angezeigt werden](images/cscbx-01.png)

<span data-ttu-id="37e99-108">Das Dialogfeld enthält auch ein Listenfeld (idlist) und zwei Schaltflächen: **OK** (IDOK) und **Abbrechen** (IDCANCEL).</span><span class="sxs-lookup"><span data-stu-id="37e99-108">The dialog box also contains a list box (IDLIST) and two buttons: **OK** (IDOK) and **Cancel** (IDCANCEL).</span></span> <span data-ttu-id="37e99-109">Die IDOK-und IDCANCEL-Konstanten werden durch die SDK-Header Dateien definiert.</span><span class="sxs-lookup"><span data-stu-id="37e99-109">The IDOK and IDCANCEL constants are defined by the SDK header files.</span></span> <span data-ttu-id="37e99-110">Die idlist-Konstante ist in der Header Datei der Anwendung definiert, ebenso wie der Steuerelement Bezeichner idcombo.</span><span class="sxs-lookup"><span data-stu-id="37e99-110">The constant IDLIST is defined in the application's header file, as is the control identifier, IDCOMBO.</span></span> <span data-ttu-id="37e99-111">Weitere Informationen zu Dialogfeldern finden Sie unter [Dialogfelder](/windows/desktop/dlgbox/dialog-boxes).</span><span class="sxs-lookup"><span data-stu-id="37e99-111">For more information about dialog boxes, see [Dialog Boxes](/windows/desktop/dlgbox/dialog-boxes).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="37e99-112">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="37e99-112">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="37e99-113">Technologien</span><span class="sxs-lookup"><span data-stu-id="37e99-113">Technologies</span></span>

-   [<span data-ttu-id="37e99-114">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="37e99-114">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="37e99-115">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="37e99-115">Prerequisites</span></span>

-   <span data-ttu-id="37e99-116">C/C++</span><span class="sxs-lookup"><span data-stu-id="37e99-116">C/C++</span></span>
-   <span data-ttu-id="37e99-117">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="37e99-117">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="37e99-118">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="37e99-118">Instructions</span></span>

### <a name="step-1-create-the-owner-drawn-dialog-box"></a><span data-ttu-id="37e99-119">Schritt 1: Erstellen des Dialog Felds "Owner-Drawn"</span><span class="sxs-lookup"><span data-stu-id="37e99-119">Step 1: Create the Owner-Drawn Dialog Box</span></span>

<span data-ttu-id="37e99-120">Das Codebeispiel verwendet die [**Dialogbox**](/windows/desktop/api/winuser/nf-winuser-dialogboxa) -Funktion, um ein modales Dialogfeld zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="37e99-120">The code example uses the [**DialogBox**](/windows/desktop/api/winuser/nf-winuser-dialogboxa) function to create a modal dialog box.</span></span> <span data-ttu-id="37e99-121">In der Dialogfeld Vorlage IDD \_ sqmahlzeit werden die Fenster Stile, Schaltflächen und Steuerelement Bezeichner für das Kombinations Feld definiert.</span><span class="sxs-lookup"><span data-stu-id="37e99-121">The dialog box template, IDD\_SQMEAL, defines the window styles, buttons, and control identifiers for the combo box.</span></span> <span data-ttu-id="37e99-122">Im Kombinations Feld in diesem Beispiel werden die [**Stile \_ CBS DropDownList**](combo-box-styles.md), [**CBS \_ besitzdrawfixed**](combo-box-styles.md), [**CBS \_ Sort**](combo-box-styles.md), [**CBS \_ hasstrings**](combo-box-styles.md), [**WS \_ VScroll**](/windows/desktop/winmsg/window-styles)und [**WS \_ Tabstopp**](/windows/desktop/winmsg/window-styles) verwendet.</span><span class="sxs-lookup"><span data-stu-id="37e99-122">The combo box in this example uses the [**CBS\_DROPDOWNLIST**](combo-box-styles.md), [**CBS\_OWNERDRAWFIXED**](combo-box-styles.md), [**CBS\_SORT**](combo-box-styles.md), [**CBS\_HASSTRINGS**](combo-box-styles.md), [**WS\_VSCROLL**](/windows/desktop/winmsg/window-styles), and [**WS\_TABSTOP**](/windows/desktop/winmsg/window-styles) styles.</span></span>


```C++
DialogBox(hInst, MAKEINTRESOURCE(IDD_SQMEAL), 
    hWnd, FoodDlgProc);
```



### <a name="step-2-process-the-wm_initdialog-and-wm_destroy-messages-in-a-dialog-box"></a><span data-ttu-id="37e99-123">Schritt 2: Verarbeiten der "WM \_ InitDialog"-und "WM Destroy"- \_ Meldungen in einem Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="37e99-123">Step 2: Process the WM\_INITDIALOG and WM\_DESTROY messages in a dialog box.</span></span>

<span data-ttu-id="37e99-124">Wenn Sie ein Kombinations Feld in einem Dialogfeld verwenden, reagieren Sie in der Regel auf eine " [**WM \_ InitDialog**](/windows/desktop/dlgbox/wm-initdialog) "-Meldung, indem Sie das Kombinations Feld initialisieren.</span><span class="sxs-lookup"><span data-stu-id="37e99-124">When you use a combo box in a dialog box, you usually respond to a [**WM\_INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) message by initializing the combo box.</span></span> <span data-ttu-id="37e99-125">Die Anwendung lädt die für das vom Besitzer gezeichneten Kombinations Feld verwendeten Bitmaps und ruft dann die Anwendungs definierte `InitGroupList` Funktion auf, um das Kombinations Feld zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="37e99-125">The application loads the bitmaps used for the owner-drawn combo box and then calls the application-defined `InitGroupList` function to initialize the combo box.</span></span> <span data-ttu-id="37e99-126">Außerdem wählt Sie das erste Listenelement im Kombinations Feld aus und ruft dann die Anwendungs definierte `InitFoodList` Funktion auf, um das Listenfeld zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="37e99-126">It also selects the first list item in the combo box and then calls the application-defined `InitFoodList` function to initialize the list box.</span></span>

<span data-ttu-id="37e99-127">Im Beispiel handelt es sich bei dem vom Besitzer gezeichneten Kombinations Feld um ein Dropdown-Listenfeld, das die Namen der jeweiligen vier Lebensmittelgruppen enthält.</span><span class="sxs-lookup"><span data-stu-id="37e99-127">In the example, the owner-drawn combo box is a drop-down list box that contains the names of each of the four food groups.</span></span> <span data-ttu-id="37e99-128">`InitGroupList` Fügt den Namen der einzelnen Nahrungsmittelgruppen hinzu und verwendet die [**CB \_ -Nachricht**](cb-setitemdata.md) , um jedem Listenelement, das eine Nahrungsmittel Gruppe identifiziert, ein Bitmap-Handle zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="37e99-128">`InitGroupList` adds the name of each food group , and uses the [**CB\_SETITEMDATA**](cb-setitemdata.md) message to associate a bitmap handle with each list item that identifies a food group.</span></span>

<span data-ttu-id="37e99-129">Das Listenfeld im Beispiel enthält die Namen der Nahrungsmittel in der ausgewählten Lebensmittelgruppe.</span><span class="sxs-lookup"><span data-stu-id="37e99-129">The list box in the example contains the names of foods in the selected food group.</span></span> <span data-ttu-id="37e99-130">**Initfoodlist** setzt den Inhalt des Listen Felds zurück und fügt dann die Namen der aktuellen nahrungsmittelauswahl in das Dropdown-Listenfeld aktuelle Nahrungsmittel Gruppe ein.</span><span class="sxs-lookup"><span data-stu-id="37e99-130">**InitFoodList** resets the contents of the list box, then adds the names of the current food selection in the current food group drop-down list box.</span></span>


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



<span data-ttu-id="37e99-131">Beim Empfang der [**WM- \_**](/windows/desktop/winmsg/wm-destroy) Lösch Nachricht löscht die Anwendung die Bitmaps im vom Besitzer gezeichneten Kombinations Feld.</span><span class="sxs-lookup"><span data-stu-id="37e99-131">When it receives the [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message, the application deletes the bitmaps in the owner-drawn combo box.</span></span>


```C++
case WM_DESTROY:

    // Call the application-defined function to free the bitmap resources.
    DeleteIconBitmaps();
    break;
```



### <a name="step-3-process-the-wm_measureitem-message"></a><span data-ttu-id="37e99-132">Schritt 3: Verarbeiten der "WM \_ MeasureItem"-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="37e99-132">Step 3: Process the WM\_MEASUREITEM message.</span></span>

<span data-ttu-id="37e99-133">Ein vom Besitzer gezeichnetes Kombinations Feld sendet die [**WM \_ MeasureItem**](wm-measureitem.md) -Nachricht an das übergeordnete Fenster oder die entsprechende Dialogfeld Prozedur, sodass die Anwendung die Dimensionen der einzelnen Listenelemente festlegen kann.</span><span class="sxs-lookup"><span data-stu-id="37e99-133">An owner-drawn combo box sends the [**WM\_MEASUREITEM**](wm-measureitem.md) message to its parent window or dialog box procedure so that the application can set the dimensions of each list item.</span></span> <span data-ttu-id="37e99-134">Da das Kombinations Feld "Beispiel" den Typ " [**CBS \_ besitzdrawfixed**](combo-box-styles.md) " hat, sendet das System die " **WM \_ MeasureItem** "-Meldung nur einmal.</span><span class="sxs-lookup"><span data-stu-id="37e99-134">Because the example combo box has the [**CBS\_OWNERDRAWFIXED**](combo-box-styles.md) style, the system sends the **WM\_MEASUREITEM** message only once.</span></span> <span data-ttu-id="37e99-135">Kombinations Felder mit dem CBS-Besitzer " [**\_ besitzdrawvariable**](combo-box-styles.md) " senden eine **WM \_ MeasureItem** -Nachricht für jedes Listenelement.</span><span class="sxs-lookup"><span data-stu-id="37e99-135">Combo boxes with the [**CBS\_OWNERDRAWVARIABLE**](combo-box-styles.md) style send a **WM\_MEASUREITEM** message for each list item.</span></span>

<span data-ttu-id="37e99-136">Der *LPARAM* -Parameter ist ein Zeiger auf eine [**measureitemstruct**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) -Struktur, die das Steuerelement und das Listenelement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="37e99-136">The *lParam* parameter is a pointer to a [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure that identifies the control and list item.</span></span> <span data-ttu-id="37e99-137">Sie enthält auch die Standardabmessungen des Listen Elements.</span><span class="sxs-lookup"><span data-stu-id="37e99-137">It also contains the default dimensions of the list item.</span></span> <span data-ttu-id="37e99-138">Im Beispiel wird der **ItemHeight** -Strukturmember geändert, um sicherzustellen, dass die Listenelemente hoch genug sind, um die Bitmaps der Nahrungsmittel Gruppe aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="37e99-138">The example modifies the **itemHeight** structure member to ensure that the list items are high enough to accommodate the food-group bitmaps.</span></span>


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



### <a name="step-4-process-the-wm_drawitem-message"></a><span data-ttu-id="37e99-139">Schritt 4: Verarbeiten der WM- \_ DrawItem-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="37e99-139">Step 4: Process the WM\_DRAWITEM message.</span></span>

<span data-ttu-id="37e99-140">Ein vom Besitzer gezeichnetes Kombinations Feld sendet die [**WM \_ DrawItem**](wm-drawitem.md) -Nachricht an das übergeordnete Fenster oder die entsprechende Dialogfeld Prozedur, wenn die Anwendung ein Listenelement neu zeichnen muss.</span><span class="sxs-lookup"><span data-stu-id="37e99-140">An owner-drawn combo box sends the [**WM\_DRAWITEM**](wm-drawitem.md) message to its parent window or dialog box procedure each time the application must repaint a list item.</span></span> <span data-ttu-id="37e99-141">Der *LPARAM* -Parameter ist ein Zeiger auf eine [**drawitemstruct**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) -Struktur, die das Steuerelement und das Listenelement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="37e99-141">The *lParam* parameter is a pointer to a [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure that identifies the control and list item.</span></span> <span data-ttu-id="37e99-142">Sie enthält außerdem Informationen, die zum Zeichnen des Elements erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="37e99-142">It also contains information needed to paint the item.</span></span>

<span data-ttu-id="37e99-143">Die Beispielanwendung zeigt den Listenelement Text und die Bitmap an, die der Nahrungsmittel Gruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="37e99-143">The example application displays the list-item text and the bitmap associated with the food group.</span></span> <span data-ttu-id="37e99-144">Wenn das Element den Fokus besitzt, zeichnet es auch ein Fokus Rechteck.</span><span class="sxs-lookup"><span data-stu-id="37e99-144">If the item has the focus, it also draws a focus rectangle.</span></span> <span data-ttu-id="37e99-145">Bevor der Text angezeigt wird, werden im Beispiel die Vordergrund-und Hintergrundfarben basierend auf dem ausgewählten Element festgelegt.</span><span class="sxs-lookup"><span data-stu-id="37e99-145">Before displaying the text, the example sets the foreground and background colors, based on the item selected.</span></span> <span data-ttu-id="37e99-146">Da das Kombinations Feld den [**CBS \_ hasstrings**](combo-box-styles.md) -Stil hat, verwaltet das Kombinations Feld den Text für jedes Listenelement, das mithilfe der [**CB \_ getlbtext**](cb-getlbtext.md) -Nachricht abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="37e99-146">Because the combo box has the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the combo box maintains the text for each list item that can be retrieved using the [**CB\_GETLBTEXT**](cb-getlbtext.md) message.</span></span>

<span data-ttu-id="37e99-147">Welche Bitmaps für das Listenelement verwendet werden, hängt von der Nahrungsmittel Gruppe ab.</span><span class="sxs-lookup"><span data-stu-id="37e99-147">The bitmaps used for the list item depend on the food group.</span></span> <span data-ttu-id="37e99-148">`InitGroupList` verwendet die CB-Eigenschaft " [**\_ logdata**](cb-setitemdata.md) ", um jedem Listenelement ein Bitmap-Handle zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="37e99-148">`InitGroupList` uses the [**CB\_SETITEMDATA**](cb-setitemdata.md) message to associate a bitmap handle with each list item.</span></span> <span data-ttu-id="37e99-149">Die Fenster Prozedur ruft das Bitmap-Handle aus dem **ItemData** -Member der [**drawitemstruct**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) -Struktur ab.</span><span class="sxs-lookup"><span data-stu-id="37e99-149">The window procedure retrieves the bitmap handle from the **itemData** member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure.</span></span> <span data-ttu-id="37e99-150">Das System verwendet zwei Bitmaps für jedes Lebensmittelgruppen Symbol: eine monochrome Bitmap mit dem srcand-Raster Vorgang zum Löschen des unregelmäßigen Bereichs hinter dem Bild und eine Farb Bitmap mit dem srcpaint-Raster Vorgang zum Zeichnen des Bilds.</span><span class="sxs-lookup"><span data-stu-id="37e99-150">The system uses two bitmaps for each food group symbol: a monochrome bitmap with the SRCAND raster operation to erase the irregular region behind the image, and a color bitmap with the SRCPAINT raster operation to paint the image.</span></span>


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



### <a name="step-5-process-the-wm_command-message"></a><span data-ttu-id="37e99-151">Schritt 5: Verarbeiten der WM- \_ Befehls Meldung.</span><span class="sxs-lookup"><span data-stu-id="37e99-151">Step 5: Process the WM\_COMMAND message.</span></span>

<span data-ttu-id="37e99-152">Wenn ein Ereignis in einem Dialogfeld-Steuerelement auftritt, benachrichtigt das-Steuerelement die Dialogfeld Prozedur mithilfe einer [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.</span><span class="sxs-lookup"><span data-stu-id="37e99-152">When an event occurs in a dialog box control, the control notifies the dialog box procedure by means of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span> <span data-ttu-id="37e99-153">Im Beispiel werden Benachrichtigungs Meldungen aus dem Kombinations Feld, dem Listenfeld und der Schaltfläche **OK** verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="37e99-153">The example processes notification messages from the combo box, the list box, and the **OK** button.</span></span> <span data-ttu-id="37e99-154">Der Bezeichner des Steuer Elements befindet sich im nieder wertigen Wort von *wParam*, und der Benachrichtigungs Code befindet sich im höherwertigen Wort von *wParam*.</span><span class="sxs-lookup"><span data-stu-id="37e99-154">The control identifier is in the low-order word of *wParam*, and the notification code is in the high-order word of *wParam*.</span></span>

<span data-ttu-id="37e99-155">Wenn der Steuerelement Bezeichner idcombo ist, ist im Kombinations Feld ein Ereignis aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="37e99-155">If the control identifier is IDCOMBO, an event has occurred in the combo box.</span></span> <span data-ttu-id="37e99-156">In der Antwort ignoriert die Dialogfeld Prozedur alle anderen Kombinations Feld Ereignisse außer [**CBN \_ selendok**](cbn-selendok.md), das angibt, dass eine Auswahl getroffen wurde, das Dropdown-Listenfeld geschlossen wurde und die vorgenommenen Änderungen akzeptiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="37e99-156">In response, the dialog box procedure ignores all other combo box events except [**CBN\_SELENDOK**](cbn-selendok.md), which indicates that a selection was made, the drop down list box was closed, and the changes made should be accepted.</span></span> <span data-ttu-id="37e99-157">Die Dialogfeld Prozedur ruft `InitFoodList` auf, um den Inhalt des Listen Felds zurückzusetzen und die Namen der aktuellen Auswahl im Dropdown-Listenfeld hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="37e99-157">The dialog box procedure calls `InitFoodList` to reset the contents of the list box and to add the names of the current selections in the drop-down list box.</span></span>

<span data-ttu-id="37e99-158">Wenn der Steuerelement Bezeichner "idlist" ist, ist im Listenfeld ein Ereignis aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="37e99-158">If the control identifier is IDLIST, an event has occurred in the list box.</span></span> <span data-ttu-id="37e99-159">Dies bewirkt, dass die Dialogfeld Prozedur alle Listenfeld Ereignisse außer [**LBN \_ dblclk**](lbn-dblclk.md)ignoriert, was darauf hinweist, dass der Benutzer auf ein Listenelement Doppel geklickt hat.</span><span class="sxs-lookup"><span data-stu-id="37e99-159">This causes the dialog box procedure to ignore all list box events except [**LBN\_DBLCLK**](lbn-dblclk.md), which indicates that the user has double-clicked a list item.</span></span> <span data-ttu-id="37e99-160">Dieses Ereignis wird auf die gleiche Weise verarbeitet, wie wenn eine Schaltfläche " **OK** " ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="37e99-160">This event is processed in the same way as if an **OK** button had been chosen.</span></span>

<span data-ttu-id="37e99-161">Wenn der Steuerelement Bezeichner IDOK ist, hat der Benutzer die Schaltfläche **OK** ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="37e99-161">If the control identifier is IDOK, the user has chosen the **OK** button.</span></span> <span data-ttu-id="37e99-162">In der Antwort fügt die Dialogfeld Prozedur den Namen des ausgewählten Nahrungsmittel in das mehrzeilige Bearbeitungs Steuerelement der Anwendung ein und ruft dann die [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) -Funktion auf, um das Dialogfeld zu schließen.</span><span class="sxs-lookup"><span data-stu-id="37e99-162">In response, the dialog box procedure inserts the name of the selected food into the application's multi-line edit control, then calls the [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) function to close the dialog box.</span></span>

<span data-ttu-id="37e99-163">Wenn der Steuerelement Bezeichner IDCANCEL ist, hat der Benutzer auf die Schaltfläche " **Abbrechen** " geklickt.</span><span class="sxs-lookup"><span data-stu-id="37e99-163">If the control identifier is IDCANCEL, the user has clicked the **Cancel** button.</span></span> <span data-ttu-id="37e99-164">In der Antwort Ruft die Dialogfeld Prozedur [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) auf, um das Dialogfeld zu schließen.</span><span class="sxs-lookup"><span data-stu-id="37e99-164">In response, the dialog box procedure calls [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) to close the dialog box.</span></span>


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



## <a name="complete-example"></a><span data-ttu-id="37e99-165">Vollständiges Beispiel</span><span class="sxs-lookup"><span data-stu-id="37e99-165">Complete example</span></span>

<span data-ttu-id="37e99-166">Im folgenden finden Sie die Dialogfeld Prozedur und die unterstützenden Funktionen für das Dialogfeld **quadratische Mahlzeit** .</span><span class="sxs-lookup"><span data-stu-id="37e99-166">Following is the dialog box procedure and the supporting functions for the **Square Meal** dialog box.</span></span>


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


## <a name="related-topics"></a><span data-ttu-id="37e99-167">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="37e99-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37e99-168">Verwenden von Kombinations Feldern</span><span class="sxs-lookup"><span data-stu-id="37e99-168">Using Combo Boxes</span></span>](using-combo-boxes.md)
</dt> </dl>

 

 