---
title: Verwenden von Menüs
description: Dieser Abschnitt enthält Codebeispiele für Aufgaben im Zusammenhang mit Menüs.
ms.assetid: b1391e37-a146-46ec-a329-aa57cfcfd351
keywords:
- Ressourcen, Menüs
- Menüs, erstellen
- Menü Vorlagen Ressourcen
- Ressourcen, Menüvorlage
- Erweitertes Menü-Vorlagen Format
- Format der alten Menüvorlage
- Menü Vorlagen Ressourcen werden geladen.
- Menüs, Klasse
- Menüs, Verknüpfung
- Erstellen von Menüs
- Klassen Menüs
- Kontextmenüs
- Bitmaps für Menü Elemente
- Menüs, gezeichnete Besitzer
- vom Besitzer gezeichnete Menüs
- Bitmaps für benutzerdefinierte Prüfzeichen
- Menüs, Kontrollkästchen
- Menüs, Schriftarten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d216b5fe5e6c25a98b5bdf3abe9d55b4bb0b34f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726752"
---
# <a name="using-menus"></a>Verwenden von Menüs

In diesem Abschnitt werden die folgenden Aufgaben beschrieben:

-   [Verwenden einer Menu-Template-Ressource](#using-a-menu-template-resource)
    -   [Erweitertes Menu-Template Format](#extended-menu-template-format)
    -   [Altes Menu-Template Format](#old-menu-template-format)
    -   [Laden einer Menu-Template Ressource](#loading-a-menu-template-resource)
    -   [Erstellen eines Klassen Menüs](#creating-a-class-menu)
-   [Erstellen eines Kontextmenüs](#creating-a-shortcut-menu)
    -   [Verarbeiten der WM- \_ ContextMenu-Meldung](/windows)
    -   [Erstellen einer Verknüpfung Font-Attributes Menü](#creating-a-shortcut-font-attributes-menu)
    -   [Anzeigen eines Kontextmenüs](#displaying-a-shortcut-menu)
-   [Verwenden von Menu-Item Bitmaps](#using-menu-item-bitmaps)
    -   [Festlegen des Bitmap-Typflags](#setting-the-bitmap-type-flag)
    -   [Erstellen der Bitmap](#creating-the-bitmap)
    -   [Hinzufügen von Linien und Diagrammen zu einem Menü](#adding-lines-and-graphs-to-a-menu)
    -   [Beispiel für Menu-Item Bitmaps](#example-of-menu-item-bitmaps)
-   [Erstellen von Owner-Drawn Menü Elementen](#creating-owner-drawn-menu-items)
    -   [Festlegen des Owner-Drawn Flags](#setting-the-owner-drawn-flag)
    -   [Vom Besitzer gezeichnete Menüs und die WM- \_ MeasureItem-Nachricht](/windows)
    -   [Von einem Besitzer gezeichnete Menüs und die WM- \_ DrawItem-Nachricht](/windows)
    -   [Von einem Besitzer gezeichnete Menüs und die WM- \_ menuchar-Meldung](/windows)
    -   [Festlegen von Schriftarten für Menu-Item Text Zeichenfolgen](#setting-fonts-for-menu-item-text-strings)
    -   [Beispiel für Owner-Drawn Menü Elemente](#example-of-owner-drawn-menu-items)
-   [Verwenden von benutzerdefinierten Häkchen-Bitmaps](#using-custom-check-mark-bitmaps)
    -   [Erstellen von benutzerdefinierten Häkchen Bitmaps](#creating-custom-check-mark-bitmaps)
    -   [Zuordnen von Bitmaps zu einem Menü Element](#associating-bitmaps-with-a-menu-item)
    -   [Festlegen des Häkchen Attributs](#setting-the-check-mark-attribute)
    -   [Simulieren von Kontrollkästchen in einem Menü](#simulating-check-boxes-in-a-menu)
    -   [Beispiel für die Verwendung von benutzerdefinierten Bitmaps für das Häkchen](#example-of-using-custom-check-mark-bitmaps)

## <a name="using-a-menu-template-resource"></a>Verwenden einer Menu-Template-Ressource

In der Regel fügen Sie ein Menü in eine Anwendung ein, indem Sie eine Menü Vorlagen Ressource erstellen und das Menü dann zur Laufzeit laden. In diesem Abschnitt wird das Format einer Menüvorlage beschrieben. Außerdem wird erläutert, wie Sie eine Menü Vorlagen Ressource laden und in Ihrer Anwendung verwenden. Weitere Informationen zum Erstellen einer Menü Vorlagen Ressource finden Sie in der Dokumentation, die in ihren Entwicklungs Tools enthalten ist.

-   [Erweitertes Menu-Template Format](#extended-menu-template-format)
-   [Altes Menu-Template Format](#old-menu-template-format)
-   [Laden einer Menu-Template Ressource](#loading-a-menu-template-resource)
-   [Erstellen eines Klassen Menüs](#creating-a-class-menu)

### <a name="extended-menu-template-format"></a>Erweitertes Menu-Template Format

Das erweiterte Menü Vorlagen Format unterstützt zusätzliche Menüfunktionen. Ebenso wie Standardmenü Vorlagen Ressourcen haben erweiterte Menü Vorlagen Ressourcen den **\_ Menü** Ressourcentyp RT. Das System unterscheidet die beiden Ressourcen Formate durch die Versionsnummer, die der erste Member des Ressourcen Headers ist.

Eine erweiterte Menüvorlage besteht aus einer [**menuex- \_ Vorlagen \_ Header**](menuex-template-header.md) Struktur, gefolgt von einer weiteren [**menuex- \_ Vorlagen \_ Element**](menuex-template-item.md) -Element Definitions Struktur.

### <a name="old-menu-template-format"></a>Altes Menu-Template Format

In einer alten Menüvorlage (Microsoft Windows NT 3,51 und früher) ist ein Menü definiert, aber die neue Menü Funktionalität wird nicht unterstützt. Eine alte Menü Vorlagen Ressource verfügt über den **RT- \_ Menü** Ressourcentyp.

Eine alte Menüvorlage besteht aus einer [**menuitemtemplateheader**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader) -Struktur, gefolgt von einer oder mehreren [**menuitemtemplate**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate) -Strukturen.

### <a name="loading-a-menu-template-resource"></a>Laden einer Menu-Template Ressource

Verwenden Sie zum Laden einer Menü Vorlagen Ressource die [**loadmenu**](/windows/desktop/api/Winuser/nf-winuser-loadmenua) -Funktion, und geben Sie ein Handle für das Modul an, das die Ressource und den Bezeichner der Menüvorlage enthält. Die **loadmenu** -Funktion gibt ein Menü Handle zurück, das Sie verwenden können, um das Menü einem Fenster zuzuweisen. Dieses Fenster wird zum Besitzer Fenster des Menüs, das alle vom Menü generierten Meldungen empfängt.

Verwenden Sie die [**loadmenuindirekte**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) -Funktion, um ein Menü aus einer Menüvorlage zu erstellen, die sich bereits im Arbeitsspeicher befindet. Dies ist nützlich, wenn Ihre Anwendung Menü Vorlagen dynamisch generiert.

Wenn Sie ein Menü einem Fenster zuweisen möchten, verwenden Sie die [**setMenu**](/windows/desktop/api/Winuser/nf-winuser-setmenu) -Funktion, oder geben Sie beim Erstellen eines Fensters das Handle des Menüs im *HMENU* -Parameter der Funktion " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " an. Eine andere Möglichkeit, einem Fenster ein Menü zuzuweisen, besteht darin, eine Menüvorlage anzugeben, wenn Sie eine Fenster Klasse registrieren. die Vorlage identifiziert das angegebene Menü als Klassen Menü für diese Fenster Klasse.

Wenn das System ein bestimmtes Menü automatisch einem Fenster zuweisen soll, geben Sie die Menüvorlage an, wenn Sie die Klasse des Fensters registrieren. Die Vorlage identifiziert das angegebene Menü als Klassen Menü für diese Fenster Klasse. Wenn Sie dann ein Fenster der angegebenen Klasse erstellen, weist das System das angegebene Menü automatisch dem Fenster zu.

Einem Fenster, das ein untergeordnetes Fenster ist, kann kein Menü zugewiesen werden.

Um ein Klassen Menü zu erstellen, schließen Sie den Bezeichner der Menü Vorlagen Ressource als **lpszmenuname** -Member einer [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) -Struktur ein, und übergeben Sie dann einen Zeiger auf die-Struktur an die [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) -Funktion.

### <a name="creating-a-class-menu"></a>Erstellen eines Klassen Menüs

Im folgenden Beispiel wird gezeigt, wie ein Klassen Menü für eine Anwendung erstellt wird, ein Fenster erstellt wird, in dem das Klassen Menü und Menübefehle verarbeiten in der Fenster Prozedur verwendet werden.

Im folgenden ist der relevante Teil der Header Datei der Anwendung aufgeführt:


```
// Menu-template resource identifier 
 
#define IDM_MYMENURESOURCE   3
```



Im folgenden sind die relevanten Teile der Anwendung selbst aufgeführt:


```
HINSTANCE hinst; 
 
int APIENTRY WinMain(HINSTANCE hinstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow) 
{ 
    MSG msg = { };  // message 
    WNDCLASS wc;    // windowclass data 
    HWND hwnd;      // handle to the main window 
 
    // Create the window class for the main window. Specify 
    // the identifier of the menu-template resource as the 
    // lpszMenuName member of the WNDCLASS structure to create 
    // the class menu. 
 
    wc.style = 0; 
    wc.lpfnWndProc = (WNDPROC) MainWndProc; 
    wc.cbClsExtra = 0; 
    wc.cbWndExtra = 0; 
    wc.hInstance = hinstance; 
    wc.hIcon = LoadIcon(NULL, IDI_APPLICATION); 
    wc.hCursor = LoadCursor(NULL, IDC_ARROW); 
    wc.hbrBackground = GetStockObject(WHITE_BRUSH); 
    wc.lpszMenuName =  MAKEINTRESOURCE(IDM_MYMENURESOURCE); 
    wc.lpszClassName = "MainWClass"; 
 
    if (!RegisterClass(&wc)) 
        return FALSE; 
 
    hinst = hinstance; 
 
    // Create the main window. Set the hmenu parameter to NULL so 
    // that the system uses the class menu for the window. 
 
    hwnd = CreateWindow("MainWClass", "Sample Application", 
        WS_OVERLAPPEDWINDOW, CW_USEDEFAULT, CW_USEDEFAULT, 
        CW_USEDEFAULT, CW_USEDEFAULT, NULL, NULL, hinstance, 
        NULL); 
 
    if (hwnd == NULL) 
        return FALSE; 
 
    // Make the window visible and send a WM_PAINT message to the 
    // window procedure. 
 
    ShowWindow(hwnd, nCmdShow); 
    UpdateWindow(hwnd); 
 
    // Start the main message loop. 
 
    while (GetMessage(&msg, NULL, 0, 0)) 
    { 
        TranslateMessage(&msg); 
        DispatchMessage(&msg); 
    } 
    return msg.wParam; 
        UNREFERENCED_PARAMETER(hPrevInstance); 
} 
 
 
LRESULT APIENTRY MainWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
 
    switch (uMsg) 
    { 
        // Process other window messages. 
 
        case WM_COMMAND: 
 
            // Test for the identifier of a command item. 
 
            switch(LOWORD(wParam)) 
            { 
                case IDM_FI_OPEN: 
                    DoFileOpen();   // application-defined 
                    break; 
 
                case IDM_FI_CLOSE: 
                    DoFileClose();  // application-defined 
                    break; 
                // Process other menu commands. 
 
                default: 
                    break; 
 
            } 
            return 0; 
 
        // Process other window messages. 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
```



## <a name="creating-a-shortcut-menu"></a>Erstellen eines Kontextmenüs

Wenn Sie ein Kontextmenü in einer Anwendung verwenden möchten, übergeben Sie das zugehörige Handle an die [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) -Funktion. Eine Anwendung ruft in der Regel **TrackPopupMenuEx** in einer Fenster Prozedur als Reaktion auf eine benutzergenerierte Meldung auf, z. b. [**WM \_ lbuttondown**](/windows/desktop/inputdev/wm-lbuttondown) oder [**WM \_ KeyDown**](/windows/desktop/inputdev/wm-keydown).

Zusätzlich zum Popup-Menü handle erfordert [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) , dass Sie ein Handle für das Besitzer Fenster, die Position des Kontextmenüs (in Bildschirm Koordinaten) und die Maustaste angeben, mit der der Benutzer ein Element auswählen kann.

Die ältere [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) -Funktion wird weiterhin unterstützt, aber neue Anwendungen sollten die [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) -Funktion verwenden. Die **TrackPopupMenuEx** -Funktion erfordert dieselben Parameter wie **TrackPopupMenu**, aber Sie können auch einen Teil des Bildschirms angeben, der vom Menü nicht verdeckt werden soll. Eine Anwendung ruft diese Funktionen in der Regel in einer Fenster Prozedur auf, wenn die [**WM- \_ ContextMenu**](wm-contextmenu.md) -Nachricht verarbeitet wird.

Sie können die Position eines Kontextmenüs angeben, indem Sie x-und y-Koordinaten zusammen mit dem **TPM \_ centeralign**, **TPM \_ leftalign** oder dem **TPM \_ RightAlign** -Flag bereitstellen. Das-Flag gibt die Position des Kontextmenüs in Bezug auf die x-und y-Koordinaten an.

Sie sollten zulassen, dass der Benutzer ein Element aus einem Kontextmenü mithilfe derselben Maustaste zum Anzeigen des Menüs auswählen. Geben Sie hierzu entweder **TPM \_ LeftButton** oder **TPM \_ RightButton** -Flag an, um anzugeben, welche Maustaste der Benutzer zum Auswählen eines Menü Elements verwenden kann.

-   [Verarbeiten der WM- \_ ContextMenu-Meldung](/windows)
-   [Erstellen einer Verknüpfung Font-Attributes Menü](#creating-a-shortcut-font-attributes-menu)
-   [Anzeigen eines Kontextmenüs](#displaying-a-shortcut-menu)

### <a name="processing-the-wm_contextmenu-message"></a>Verarbeiten der WM- \_ ContextMenu-Meldung

Die [**"WM \_ ContextMenu**](wm-contextmenu.md) "-Meldung wird generiert, wenn die Fenster Prozedur einer Anwendung die [**WM- \_ rbuttonup**](/windows/desktop/inputdev/wm-rbuttonup) -oder [**WM \_ ncrbuttonup**](/windows/desktop/inputdev/wm-ncrbuttonup) -Meldung an die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion übergibt. Die Anwendung kann diese Nachricht verarbeiten, um ein Kontextmenü anzuzeigen, das für einen bestimmten Teil des Bildschirms geeignet ist. Wenn in der Anwendung kein Kontextmenü angezeigt wird, sollte die Nachricht zur Standardbehandlung an **defwindowproc** übergeben werden.

Im folgenden finden Sie ein Beispiel der WM-Verarbeitung von [**\_ ContextMenu**](wm-contextmenu.md) , wie Sie in der Fenster Prozedur einer Anwendung angezeigt werden kann. Die nieder wertigen und höherwertigen Wörter des *LPARAM* -Parameters geben die Bildschirm Koordinaten der Maus an, wenn die Rechte Maustaste losgelassen wird (Beachten Sie, dass diese Koordinaten für Systeme mit mehreren Monitoren negative Werte annehmen können). Die von der Anwendung definierte **oncontextmenu** -Funktion gibt **true** zurück, wenn ein Kontextmenü angezeigt wird, andernfalls **false** .


```
case WM_CONTEXTMENU: 
    if (!OnContextMenu(hwnd, GET_X_LPARAM(lParam),
              GET_Y_LPARAM(lParam))) 
        return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    break; 
```



Die folgende Anwendungs definierte oncontextmenu-Funktion zeigt ein Kontextmenü an, wenn sich die angegebene Mausposition im Client Bereich des Fensters befindet. Je nachdem, welcher Teil des Client Bereichs angegeben ist, kann eine anspruchsvollere Funktion eine von mehreren unterschiedlichen Menüs anzeigen. Um das Kontextmenü tatsächlich anzuzeigen, wird in diesem Beispiel eine Anwendungs definierte Funktion namens "displaycontextmenu" aufgerufen. Eine Beschreibung dieser Funktion finden Sie unter [Anzeigen eines Kontextmenüs](#displaying-a-shortcut-menu).


```
BOOL WINAPI OnContextMenu(HWND hwnd, int x, int y) 
{ 
    RECT rc;                    // client area of window 
    POINT pt = { x, y };        // location of mouse click 
 
    // Get the bounding rectangle of the client area. 
 
    GetClientRect(hwnd, &rc); 
 
    // Convert the mouse position to client coordinates. 
 
    ScreenToClient(hwnd, &pt); 
 
    // If the position is in the client area, display a  
    // shortcut menu. 
 
    if (PtInRect(&rc, pt)) 
    { 
        ClientToScreen(hwnd, &pt); 
        DisplayContextMenu(hwnd, pt); 
        return TRUE; 
    } 
 
    // Return FALSE if no menu is displayed. 
 
    return FALSE; 
} 
```



### <a name="creating-a-shortcut-font-attributes-menu"></a>Erstellen einer Verknüpfung Font-Attributes Menü

Das Beispiel in diesem Abschnitt enthält Teile von Code aus einer Anwendung, die ein Kontextmenü erstellt und anzeigt, das es dem Benutzer ermöglicht, Schriftarten und Schriftart Attribute festzulegen. Die Anwendung zeigt das Menü im Client Bereich des Hauptfensters an, wenn der Benutzer mit der linken Maustaste klickt.

Hier ist die Menüvorlage für das Kontextmenü, das in der Ressourcen Definitionsdatei der Anwendung bereitgestellt wird.


```
PopupMenu MENU 
BEGIN 
  POPUP "Dummy Popup" 
    BEGIN 
      POPUP "Fonts" 
        BEGIN 
          MENUITEM "Courier",     IDM_FONT_COURIER 
          MENUITEM "Times Roman", IDM_FONT_TMSRMN 
          MENUITEM "Swiss",       IDM_FONT_SWISS 
          MENUITEM "Helvetica",   IDM_FONT_HELV 
          MENUITEM "Old English", IDM_FONT_OLDENG 
        END 
      POPUP "Sizes" 
        BEGIN 
          MENUITEM "7",  IDM_SIZE_7 
          MENUITEM "8",  IDM_SIZE_8 
          MENUITEM "9",  IDM_SIZE_9 
          MENUITEM "10", IDM_SIZE_10 
          MENUITEM "11", IDM_SIZE_11 
          MENUITEM "12", IDM_SIZE_12 
          MENUITEM "14", IDM_SIZE_14 
        END 
      POPUP "Styles" 
        BEGIN 
          MENUITEM "Bold",        IDM_STYLE_BOLD 
          MENUITEM "Italic",      IDM_STYLE_ITALIC 
          MENUITEM "Strike Out",  IDM_STYLE_SO 
          MENUITEM "Superscript", IDM_STYLE_SUPER 
          MENUITEM "Subscript",   IDM_STYLE_SUB 
        END 
    END 
 
END 
```



Im folgenden Beispiel werden die Fenster Prozedur und die unterstützenden Funktionen verwendet, mit denen das Kontextmenü erstellt und angezeigt wird.


```
LRESULT APIENTRY MenuWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    RECT rc;    // client area             
    POINT pt;   // location of mouse click  
 
    switch (uMsg) 
    { 
        case WM_LBUTTONDOWN: 
 
            // Get the bounding rectangle of the client area. 
 
            GetClientRect(hwnd, (LPRECT) &rc); 
 
            // Get the client coordinates for the mouse click.  
 
            pt.x = GET_X_LPARAM(lParam); 
            pt.y = GET_Y_LPARAM(lParam); 
 
            // If the mouse click took place inside the client 
            // area, execute the application-defined function 
            // that displays the shortcut menu. 
 
            if (PtInRect((LPRECT) &rc, pt)) 
                HandlePopupMenu(hwnd, pt); 
            break; 
        // Process other window messages.  
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
 
 
VOID APIENTRY HandlePopupMenu(HWND hwnd, POINT pt) 
{ 
    HMENU hmenu;            // menu template          
    HMENU hmenuTrackPopup;  // shortcut menu   
 
    //  Load the menu template containing the shortcut menu from the 
    //  application's resources. 
 
    hmenu = LoadMenu(hinst, "PopupMenu"); 
    if (hmenu == NULL) 
        return; 
 
    // Get the first shortcut menu in the menu template. This is the 
    // menu that TrackPopupMenu displays. 
 
    hmenuTrackPopup = GetSubMenu(hmenu, 0); 
 
    // TrackPopup uses screen coordinates, so convert the 
    // coordinates of the mouse click to screen coordinates. 
 
    ClientToScreen(hwnd, (LPPOINT) &pt); 
 
    // Draw and track the shortcut menu.  
 
    TrackPopupMenu(hmenuTrackPopup, TPM_LEFTALIGN | TPM_LEFTBUTTON, 
        pt.x, pt.y, 0, hwnd, NULL); 
 
    // Destroy the menu. 
 
    DestroyMenu(hmenu); 
} 
```



### <a name="displaying-a-shortcut-menu"></a>Anzeigen eines Kontextmenüs

Die im folgenden Beispiel gezeigte Funktion zeigt ein Kontextmenü an.

Die Anwendung enthält eine Menü Ressource, die durch die Zeichenfolge "shortcutexample" identifiziert wird. Die Menüleiste enthält einfach einen Menünamen. Die Anwendung verwendet die [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) -Funktion, um das Menü anzuzeigen, das diesem Menü Element zugeordnet ist. (Die Menüleiste selbst wird nicht angezeigt, da **TrackPopupMenu** ein Handle für ein Menü, ein Untermenü oder ein Kontextmenü erfordert.)


```
VOID APIENTRY DisplayContextMenu(HWND hwnd, POINT pt) 
{ 
    HMENU hmenu;            // top-level menu 
    HMENU hmenuTrackPopup;  // shortcut menu 
 
    // Load the menu resource. 
 
    if ((hmenu = LoadMenu(hinst, "ShortcutExample")) == NULL) 
        return; 
 
    // TrackPopupMenu cannot display the menu bar so get 
    // a handle to the first shortcut menu. 
 
    hmenuTrackPopup = GetSubMenu(hmenu, 0); 
 
    // Display the shortcut menu. Track the right mouse 
    // button. 
 
    TrackPopupMenu(hmenuTrackPopup, 
            TPM_LEFTALIGN | TPM_RIGHTBUTTON, 
            pt.x, pt.y, 0, hwnd, NULL); 
 
    // Destroy the menu. 
 
    DestroyMenu(hmenu); 
} 
```



## <a name="using-menu-item-bitmaps"></a>Verwenden von Menu-Item Bitmaps

Das System kann eine Bitmap anstelle einer Text Zeichenfolge verwenden, um ein Menü Element anzuzeigen. Um eine Bitmap zu verwenden, müssen Sie das **miim- \_ Bitmap** -Flag für das Menü Element festlegen und ein Handle für die Bitmap angeben, das das System für das Menü Element im **hbmpitem** -Member der [**menuiteminfo**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) -Struktur anzeigen soll. In diesem Abschnitt wird beschrieben, wie Bitmaps für Menü Elemente verwendet werden.

-   [Festlegen des Bitmap-Typflags](#setting-the-bitmap-type-flag)
-   [Erstellen der Bitmap](#creating-the-bitmap)
-   [Hinzufügen von Linien und Diagrammen zu einem Menü](#adding-lines-and-graphs-to-a-menu)
-   [Beispiel für Menu-Item Bitmaps](#example-of-menu-item-bitmaps)

### <a name="setting-the-bitmap-type-flag"></a>Festlegen des Bitmap-Typflags

Das **miim \_ Bitmap** -oder **MF- \_ bitmapflag** weist das System an, anstelle einer Text Zeichenfolge eine Bitmap zu verwenden, um ein Menü Element anzuzeigen. Das **miim \_ Bitmap** -oder MF- **\_ bitmapflag** eines Menü Elements muss zur Laufzeit festgelegt werden. es ist nicht möglich, es in der Ressourcen Definitionsdatei festzulegen.

Bei neuen Anwendungen können Sie die [**setmenuiteminfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) -oder [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) -Funktion verwenden, um das **miim- \_ Bitmap** -Typflag festzulegen. Verwenden Sie **setmenuiteminfo**, um ein Menü Element von einem Textelement in ein bitmapelement zu ändern. Verwenden Sie die **InsertMenuItem** -Funktion, um einem Menü ein neues Bitmap-Element hinzuzufügen.

Anwendungen, die für frühere Versionen des Systems geschrieben wurden, können weiterhin die [**modifymenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua)-, [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)-oder [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) -Funktion verwenden, um das **MF- \_ bitmapflag** festzulegen. Wenn Sie ein Menü Element von einem Textzeichen folgen Element in ein bitmapelement ändern möchten, verwenden Sie **modifymenu**. Um einem Menü ein neues bitmapelement hinzuzufügen, verwenden Sie das **MF- \_ Bitmap** -Flag mit der **InsertMenu** -Funktion oder der **AppendMenu** -Funktion.

### <a name="creating-the-bitmap"></a>Erstellen der Bitmap

Wenn Sie das Flag **miim \_ Bitmap** -oder **MF- \_ Bitmaptyp** für ein Menü Element festlegen, müssen Sie auch ein Handle für die Bitmap angeben, das das System für das Menü Element anzeigen soll. Sie können die Bitmap als Bitmap-Ressource bereitstellen oder die Bitmap zur Laufzeit erstellen. Wenn Sie eine Bitmap-Ressource verwenden, können Sie die [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) -Funktion verwenden, um die Bitmap zu laden und Ihr Handle abzurufen.

Um die Bitmap zur Laufzeit zu erstellen, verwenden Sie die Funktionen von Windows Graphics Device Interface (GDI). GDI bietet mehrere Möglichkeiten zum Erstellen einer Bitmap zur Laufzeit, aber Entwickler verwenden normalerweise die folgende Methode:

1.  Verwenden Sie [**die Funktion**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) "Funktion", um einen Gerätekontext zu erstellen, der mit dem vom Hauptfenster der Anwendung verwendeten Gerätekontext kompatibel ist.
2.  Verwenden Sie [**die Funktion**](/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap) "-Funktion", um eine Bitmap zu erstellen, die mit dem Hauptfenster der Anwendung kompatibel ist, oder verwenden [**Sie die Funktion**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) "die Funktion", um eine monochrome Bitmap zu erstellen.
3.  Verwenden Sie die [**SelectObject**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) -Funktion, um die Bitmap in den kompatiblen Gerätekontext auszuwählen.
4.  Verwenden Sie GDI-Zeichnungsfunktionen, z. b. [**Ellipse**](/windows/desktop/api/wingdi/nf-wingdi-ellipse) und [**LineTo**](/windows/desktop/api/wingdi/nf-wingdi-lineto), um ein Bild in die Bitmap zu zeichnen.

Weitere Informationen finden Sie unter [Bitmaps](/windows/desktop/gdi/bitmaps).

### <a name="adding-lines-and-graphs-to-a-menu"></a>Hinzufügen von Linien und Diagrammen zu einem Menü

Im folgenden Codebeispiel wird gezeigt, wie ein Menü erstellt wird, das Menü Element Bitmaps enthält. Es werden zwei Menüs erstellt. Das erste ist ein Diagramm Menü, das drei Menü Element Bitmaps enthält: ein Kreis Diagramm, ein Liniendiagramm und ein Balkendiagramm. Im Beispiel wird veranschaulicht, wie diese Bitmaps aus der Ressourcen Datei der Anwendung geladen werden, und anschließend werden die Menü-und Menü Elemente mithilfe der Funktionen " [**anatepopupmenu**](/windows/desktop/api/Winuser/nf-winuser-createpopupmenu) " und " [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) " erstellt.

Das zweite Menü ist ein Zeilen Menü. Sie enthält Bitmaps, die die vom vordefinierten Stift im System bereitgestellten Linienstile darstellen. Die zeilenweise Bitmaps werden zur Laufzeit mithilfe von GDI-Funktionen erstellt.

Im folgenden finden Sie die Definitionen der Bitmapressourcen in der Ressourcen Definitionsdatei der Anwendung.


```
PIE BITMAP pie.bmp 
LINE BITMAP line.bmp 
BAR BITMAP bar.bmp 
 
```



Im folgenden finden Sie die relevanten Teile der Header Datei der Anwendung.


```
// Menu-item identifiers 
 
#define IDM_SOLID       PS_SOLID 
#define IDM_DASH        PS_DASH 
#define IDM_DASHDOT     PS_DASHDOT 
#define IDM_DASHDOTDOT  PS_DASHDOTDOT 
 
#define IDM_PIE  1 
#define IDM_LINE 2 
#define IDM_BAR  3 
 
// Line-type flags  
 
#define SOLID       0 
#define DOT         1 
#define DASH        2 
#define DASHDOT     3 
#define DASHDOTDOT  4 
 
// Count of pens  
 
#define CPENS 5 
 
// Chart-type flags  
 
#define PIE  1 
#define LINE 2 
#define BAR  3 
 
// Function prototypes  
 
LRESULT APIENTRY MainWndProc(HWND, UINT, WPARAM, LPARAM); 
VOID MakeChartMenu(HWND); 
VOID MakeLineMenu(HWND, HPEN, HBITMAP); 
```



Im folgenden Beispiel wird gezeigt, wie Menüs und Menü Element Bitmaps in einer Anwendung erstellt werden.


```
LRESULT APIENTRY MainWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
 
    static HPEN hpen[CPENS]; 
    static HBITMAP hbmp[CPENS]; 
    int i; 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Create the Chart and Line menus.  
 
            MakeChartMenu(hwnd); 
            MakeLineMenu(hwnd, hpen, hbmp); 
            return 0; 
 
        // Process other window messages. 
 
        case WM_DESTROY: 
 
            for (i = 0; i < CPENS; i++) 
            { 
                DeleteObject(hbmp[i]); 
                DeleteObject(hpen[i]); 
            } 
 
            PostQuitMessage(0); 
            break; 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
 
VOID MakeChartMenu(HWND hwnd) 
{ 
    HBITMAP hbmpPie;    // handle to pie chart bitmap   
    HBITMAP hbmpLine;   // handle to line chart bitmap  
    HBITMAP hbmpBar;    // handle to bar chart bitmap   
    HMENU hmenuMain;    // handle to main menu          
    HMENU hmenuChart;   // handle to Chart menu  
 
    // Load the pie, line, and bar chart bitmaps from the 
    // resource-definition file. 
 
    hbmpPie = LoadBitmap(hinst, MAKEINTRESOURCE(PIE)); 
    hbmpLine = LoadBitmap(hinst, MAKEINTRESOURCE(LINE)); 
    hbmpBar = LoadBitmap(hinst, MAKEINTRESOURCE(BAR)); 
 
    // Create the Chart menu and add it to the menu bar. 
    // Append the Pie, Line, and Bar menu items to the Chart 
    // menu. 
 
    hmenuMain = GetMenu(hwnd); 
    hmenuChart = CreatePopupMenu(); 
    AppendMenu(hmenuMain, MF_STRING | MF_POPUP, (UINT) hmenuChart, 
        "Chart"); 
    AppendMenu(hmenuChart, MF_BITMAP, IDM_PIE, (LPCTSTR) hbmpPie); 
    AppendMenu(hmenuChart, MF_BITMAP, IDM_LINE, 
        (LPCTSTR) hbmpLine); 
    AppendMenu(hmenuChart, MF_BITMAP, IDM_BAR, (LPCTSTR) hbmpBar); 
 
    return; 
} 
 
VOID MakeLineMenu(HWND hwnd, HPEN phpen, HBITMAP phbmp) 
{ 
    HMENU hmenuLines;       // handle to Lines menu      
    HMENU hmenu;            // handle to main menu              
    COLORREF crMenuClr;     // menu-item background color       
    HBRUSH hbrBackground;   // handle to background brush       
    HBRUSH hbrOld;          // handle to previous brush         
    WORD wLineX;            // width of line bitmaps            
    WORD wLineY;            // height of line bitmaps           
    HDC hdcMain;            // handle to main window's DC       
    HDC hdcLines;           // handle to compatible DC          
    HBITMAP hbmpOld;        // handle to previous bitmap        
    int i;                  // loop counter                     
 
    // Create the Lines menu. Add it to the menu bar.  
 
    hmenu = GetMenu(hwnd); 
    hmenuLines = CreatePopupMenu(); 
    AppendMenu(hmenu, MF_STRING | MF_POPUP, 
        (UINT) hmenuLines, "&Lines"); 
 
    // Create a brush for the menu-item background color.  
 
    crMenuClr = GetSysColor(COLOR_MENU); 
    hbrBackground = CreateSolidBrush(crMenuClr); 
 
    // Create a compatible device context for the line bitmaps, 
    // and then select the background brush into it. 
 
    hdcMain = GetDC(hwnd); 
    hdcLines = CreateCompatibleDC(hdcMain); 
    hbrOld = SelectObject(hdcLines, hbrBackground); 
 
    // Get the dimensions of the check-mark bitmap. The width of 
    // the line bitmaps will be five times the width of the 
    // check-mark bitmap. 
 
    wLineX = GetSystemMetrics(SM_CXMENUCHECK) * (WORD) 5; 
    wLineY = GetSystemMetrics(SM_CYMENUCHECK); 
 
    // Create the bitmaps and select them, one at a time, into the 
    // compatible device context. Initialize each bitmap by 
    // filling it with the menu-item background color. 
 
    for (i = 0; i < CPENS; i++) 
    { 
        phbmp[i] = CreateCompatibleBitmap(hdcMain, wLineX, wLineY); 
        if (i == 0) 
            hbmpOld = SelectObject(hdcLines, phbmp[i]); 
        else 
            SelectObject(hdcLines, phbmp[i]); 
        ExtFloodFill(hdcLines, 0, 0, crMenuClr, FLOODFILLBORDER); 
    } 
 
    // Create the pens.  
 
    phpen[0] = CreatePen(PS_SOLID, 1, RGB(0, 0, 0)); 
    phpen[1] = CreatePen(PS_DOT, 1, RGB(0, 0, 0)); 
    phpen[2] = CreatePen(PS_DASH, 1, RGB(0, 0, 0)); 
    phpen[3] = CreatePen(PS_DASHDOT, 1, RGB(0, 0, 0)); 
    phpen[4] = CreatePen(PS_DASHDOTDOT, 1, RGB(0, 0, 0)); 
 
    // Select a pen and a bitmap into the compatible device 
    // context, draw a line into the bitmap, and then append 
    // the bitmap as an item in the Lines menu. 
 
    for (i = 0; i < CPENS; i++) 
    { 
        SelectObject(hdcLines, phbmp[i]); 
        SelectObject(hdcLines, phpen[i]); 
        MoveToEx(hdcLines, 0, wLineY / 2, NULL); 
        LineTo(hdcLines, wLineX, wLineY / 2); 
        AppendMenu(hmenuLines, MF_BITMAP, i + 1, 
            (LPCTSTR) phbmp[i]); 
    } 
 
    // Release the main window's device context and destroy the 
    // compatible device context. Also, destroy the background 
    // brush. 
 
    ReleaseDC(hwnd, hdcMain); 
    SelectObject(hdcLines, hbrOld); 
    DeleteObject(hbrBackground); 
    SelectObject(hdcLines, hbmpOld); 
    DeleteDC(hdcLines); 
 
    return; 
} 
```



### <a name="example-of-menu-item-bitmaps"></a>Beispiel für Menu-Item Bitmaps

Im Beispiel in diesem Thema werden zwei Menüs erstellt, die jeweils mehrere Bitmap-Menü Elemente enthalten. Die Anwendung fügt der Menüleiste des Hauptfensters für jedes Menü einen entsprechenden Menünamen hinzu.

Das erste Menü enthält Menü Elemente, die jeden der drei Diagrammtypen anzeigen: Kreis, Linie und Balken. Die Bitmaps für diese Menü Elemente werden als Ressourcen definiert und mithilfe der [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) -Funktion geladen. Diesem Menü ist der Menü Name "Diagramm" in der Menüleiste zugeordnet.

Das zweite Menü enthält Menü Elemente, die jeden der fünf Zeilen Formate mit der Funktion " [**kreatepen**](/windows/desktop/api/wingdi/nf-wingdi-createpen) " angezeigt werden: **PS \_ Solid**, **PS \_ Dash**, **PS- \_ Punkt**, **PS- \_ DashDot** und **PS- \_ DashDotDot**. Die Anwendung erstellt die Bitmaps für diese Menü Elemente zur Laufzeit mithilfe von GDI-Zeichnungsfunktionen. Diesem Menü ist ein **Zeilen** Menü Name in der Menüleiste zugeordnet.

In der Fenster Prozedur der Anwendung sind zwei statische Arrays von bitmaphandles definiert. Ein Array enthält die Handles der drei Bitmaps, die für das **Diagramm** Menü verwendet werden. Der andere enthält die Handles der fünf Bitmaps, die für das Menü " **Linien** " verwendet werden. Bei der Verarbeitung der [**WM \_ Create**](/windows/desktop/winmsg/wm-create) -Nachricht lädt die Fenster Prozedur die Diagramm Bitmaps, erstellt die Zeilen Bitmaps und fügt dann die entsprechenden Menü Elemente hinzu. Bei der Verarbeitung [**der \_ WM**](/windows/desktop/winmsg/wm-destroy) -Lösch Nachricht löscht die Fenster Prozedur alle Bitmaps.

Im folgenden finden Sie die relevanten Teile der Header Datei der Anwendung.


```
// Menu-item identifiers 
 
#define IDM_PIE         1 
#define IDM_LINE        2 
#define IDM_BAR         3 
 
#define IDM_SOLID       4 
#define IDM_DASH        5 
#define IDM_DASHDOT     6 
#define IDM_DASHDOTDOT  7 
 
// Number of items on the Chart and Lines menus 
 
#define C_LINES         5 
#define C_CHARTS        3 
 
// Bitmap resource identifiers 
 
#define IDB_PIE         1 
#define IDB_LINE        2 
#define IDB_BAR         3 
 
// Dimensions of the line bitmaps 
 
#define CX_LINEBMP      40 
#define CY_LINEBMP      10 
```



Im folgenden sind die relevanten Teile der Fenster Prozedur beschrieben. Die Fenster Prozedur führt den größten Teil ihrer Initialisierung durch Aufrufen der Anwendungs definierten loadchartbitmaps-, createlinebitmaps-und addbitmapmenu-Funktionen aus, die weiter unten in diesem Thema beschrieben werden.


```
LRESULT CALLBACK MainWindowProc( 
        HWND hwnd, 
        UINT uMsg, 
        WPARAM wParam, 
        LPARAM lParam 
        ) 
{ 
    static HBITMAP aHbmLines[C_LINES]; 
    static HBITMAP aHbmChart[C_CHARTS]; 
    int i; 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
             // Call application-defined functions to load the 
             // bitmaps for the Chart menu and create those for 
             // the Lines menu. 
 
            LoadChartBitmaps(aHbmChart); 
            CreateLineBitmaps(aHbmLines); 
 
             // Call an application-defined function to create 
             // menus containing the bitmap menu items. The function 
             // also adds a menu name to the window's menu bar. 
 
            AddBitmapMenu( 
                    hwnd,      // menu bar's owner window 
                    "&Chart",  // text of menu name on menu bar 
                    IDM_PIE,   // ID of first item on menu 
                    aHbmChart, // array of bitmap handles 
                    C_CHARTS   // number of items on menu 
                    ); 
            AddBitmapMenu(hwnd, "&Lines", IDM_SOLID, 
                    aHbmLines, C_LINES); 
            break; 
 
        case WM_DESTROY: 
            for (i = 0; i < C_LINES; i++) 
                DeleteObject(aHbmLines[i]); 
            for (i = 0; i < C_CHARTS; i++) 
                DeleteObject(aHbmChart[i]); 
            PostQuitMessage(0); 
            break; 
 
        // Process additional messages here. 
 
        default: 
            return (DefWindowProc(hwnd, uMsg, wParam, lParam)); 
    } 
    return 0; 
} 
```



Die Anwendungs definierte loadchartbitmaps-Funktion lädt die Bitmapressourcen für das Diagramm Menü, indem die [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) -Funktion wie folgt aufgerufen wird.


```
VOID WINAPI LoadChartBitmaps(HBITMAP *paHbm) 
{ 
    paHbm[0] = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_PIE)); 
    paHbm[1] = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_LINE)); 
    paHbm[2] = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_BAR)); 
} 
```



Die von der Anwendung definierte Funktion "-Funktion" erstellt die Bitmaps für das Menü "Zeilen" mithilfe von GDI-Zeichnungsfunktionen. Die-Funktion erstellt einen Arbeitsspeicher-Gerätekontext (DC) mit denselben Eigenschaften wie der DC des Desktop Fensters. Für jede Linienart erstellt die Funktion eine Bitmap, wählt Sie in den Speicher-DC aus und zeichnet Sie auf.


```
VOID WINAPI CreateLineBitmaps(HBITMAP *paHbm) 
{ 
    HWND hwndDesktop = GetDesktopWindow(); 
    HDC hdcDesktop = GetDC(hwndDesktop); 
    HDC hdcMem = CreateCompatibleDC(hdcDesktop); 
    COLORREF clrMenu = GetSysColor(COLOR_MENU); 
    HBRUSH hbrOld; 
    HPEN hpenOld; 
    HBITMAP hbmOld; 
    int fnDrawMode; 
    int i; 
 
     // Create a brush using the menu background color, 
     // and select it into the memory DC. 
 
    hbrOld = SelectObject(hdcMem, CreateSolidBrush(clrMenu)); 
 
     // Create the bitmaps. Select each one into the memory 
     // DC that was created and draw in it. 
 
    for (i = 0; i < C_LINES; i++) 
    { 
        // Create the bitmap and select it into the DC. 
 
        paHbm[i] = CreateCompatibleBitmap(hdcDesktop, 
                CX_LINEBMP, CY_LINEBMP); 
        hbmOld = SelectObject(hdcMem, paHbm[i]); 
 
        // Fill the background using the brush. 
 
        PatBlt(hdcMem, 0, 0, CX_LINEBMP, CY_LINEBMP, PATCOPY); 
 
        // Create the pen and select it into the DC. 
 
        hpenOld = SelectObject(hdcMem, 
                CreatePen(PS_SOLID + i, 1, RGB(0, 0, 0))); 
 
         // Draw the line. To preserve the background color where 
         // the pen is white, use the R2_MASKPEN drawing mode. 
 
        fnDrawMode = SetROP2(hdcMem, R2_MASKPEN); 
        MoveToEx(hdcMem, 0, CY_LINEBMP / 2, NULL); 
        LineTo(hdcMem, CX_LINEBMP, CY_LINEBMP / 2); 
        SetROP2(hdcMem, fnDrawMode); 
 
        // Delete the pen, and select the old pen and bitmap. 
 
        DeleteObject(SelectObject(hdcMem, hpenOld)); 
        SelectObject(hdcMem, hbmOld); 
    } 
 
    // Delete the brush and select the original brush. 
 
    DeleteObject(SelectObject(hdcMem, hbrOld)); 
 
    // Delete the memory DC and release the desktop DC. 
 
    DeleteDC(hdcMem); 
    ReleaseDC(hwndDesktop, hdcDesktop); 
} 
```



Die Anwendungs definierte addbitmapmenu-Funktion erstellt ein Menü und fügt dieser die angegebene Anzahl von Bitmap-Menü Elementen hinzu. Anschließend wird der Menüleiste des angegebenen Fensters ein entsprechender Menü Name hinzugefügt.


```
VOID WINAPI AddBitmapMenu( 
        HWND hwnd,          // window that owned the menu bar 
        LPSTR lpszText,     // text of menu name on menu bar 
        UINT uID,           // ID of first bitmap menu item 
        HBITMAP *paHbm,     // bitmaps for the menu items 
        int cItems)         // number bitmap menu items 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup = CreatePopupMenu(); 
    MENUITEMINFO mii; 
    int i; 
 
    // Add the bitmap menu items to the menu. 
 
    for (i = 0; i < cItems; i++) 
    { 
        mii.fMask = MIIM_ID | MIIM_BITMAP | MIIM_DATA; 
        mii.wID = uID + i; 
        mii.hbmpItem = &paHbm[i]; 
        InsertMenuItem(hmenuPopup, i, TRUE, &mii); 
    } 
 
    // Add a menu name to the menu bar. 
 
    mii.fMask = MIIM_STRING | MIIM_DATA | MIIM_SUBMENU; 
    mii.fType = MFT_STRING; 
    mii.hSubMenu = hmenuPopup; 
    mii.dwTypeData = lpszText; 
    InsertMenuItem(hmenuBar, 
        GetMenuItemCount(hmenuBar), TRUE, &mii); 
} 
```



## <a name="creating-owner-drawn-menu-items"></a>Erstellen von Owner-Drawn Menü Elementen

Wenn Sie die gesamte Kontrolle über die Darstellung eines Menü Elements benötigen, können Sie ein von einem Besitzer gezeichnetes Menü Element in der Anwendung verwenden. In diesem Abschnitt werden die Schritte beschrieben, die zum Erstellen und Verwenden eines von einem Besitzer gezeichneten Menü Elements erforderlich sind.

-   [Festlegen des Owner-Drawn Flags](#setting-the-owner-drawn-flag)
-   [Vom Besitzer gezeichnete Menüs und die WM- \_ MeasureItem-Nachricht](/windows)
-   [Von einem Besitzer gezeichnete Menüs und die WM- \_ DrawItem-Nachricht](/windows)
-   [Von einem Besitzer gezeichnete Menüs und die WM- \_ menuchar-Meldung](/windows)
-   [Festlegen von Schriftarten für Menu-Item Text Zeichenfolgen](#setting-fonts-for-menu-item-text-strings)
-   [Beispiel für Owner-Drawn Menü Elemente](#example-of-owner-drawn-menu-items)

### <a name="setting-the-owner-drawn-flag"></a>Festlegen des Owner-Drawn Flags

Sie können kein vom Besitzer gezeichnetes Menü Element in der Ressourcen Definitionsdatei Ihrer Anwendung definieren. Stattdessen müssen Sie ein neues Menü Element erstellen oder ein vorhandenes Menü Element ändern, indem Sie das MFT-Menü Kennzeichen für Besitzer **\_ Zeichnen** verwenden.

Mit der [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) -oder der [**setmenuiteminfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) -Funktion können Sie ein vom Besitzer gezeichnetes Menü Element angeben. Verwenden Sie **InsertMenuItem** , um ein neues Menü Element an der angegebenen Position in einer Menüleiste oder einem Menü einzufügen. Verwenden Sie **setmenuiteminfo** , um den Inhalt eines Menüs zu ändern.

Wenn Sie diese beiden Funktionen aufrufen, müssen Sie einen Zeiger auf eine [**menuiteminfo**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) -Struktur angeben, die die Eigenschaften des neuen Menü Elements oder die Eigenschaften angibt, die Sie für ein vorhandenes Menü Element ändern möchten. Um ein Element als vom Besitzer gezeichnetes Element festzulegen, geben Sie den **miim \_ ftype** -Wert für das **fmask** -Element und den **MFT-Besitzer \_ Zeichnungs** Wert für das **ftype** -Element an.

Durch Festlegen der entsprechenden Member der [**menuiteminfo**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) -Struktur können Sie jedem Menü Element einen Anwendungs definierten Wert, der als **Elementdaten** bezeichnet wird, zuordnen. Geben Sie hierzu den **miim- \_ Datenwert** für das **fmask** -Element und den von der Anwendung definierten Wert für das **dwitemdata** -Element an.

Sie können Elementdaten mit jedem beliebigen Menü Elementtyp verwenden, aber dies ist besonders nützlich für Elemente, die vom Besitzer gezeichnet werden. Angenommen, eine-Struktur enthält Informationen, die zum Zeichnen eines Menü Elements verwendet werden. Eine Anwendung kann die Elementdaten für ein Menü Element verwenden, um einen Zeiger auf die Struktur zu speichern. Die Elementdaten werden mit den Nachrichten " [**WM \_ MeasureItem**](../controls/wm-measureitem.md) " und " [**WM \_ DrawItem**](../controls/wm-drawitem.md) " an das Besitzer Fenster des Menüs gesendet. Um die Elementdaten für ein Menü zu einem beliebigen Zeitpunkt abzurufen, verwenden Sie die [**getmenuiteminfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) -Funktion.

Anwendungen, die für frühere Versionen des Systems geschrieben wurden, können weiterhin [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)oder [**modifymenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua) aufrufen, um das MF-Besitzer **\_ Zeichnungs** Flag einem von einem Besitzer gezeichneten Menü Element zuzuweisen.

Wenn Sie eine dieser drei Funktionen aufrufen, können Sie einen Wert als *lpnetwitem* -Parameter übergeben. Dieser Wert kann alle Informationen darstellen, die für Ihre Anwendung von Bedeutung sind, und die der Anwendung zur Verfügung stehen, wenn das Element angezeigt werden soll. Der Wert kann z. b. einen Zeiger auf eine-Struktur enthalten. die-Struktur kann wiederum eine Text Zeichenfolge und ein Handle für die logische Schriftart enthalten, die Ihre Anwendung zum Zeichnen der Zeichenfolge verwendet.

### <a name="owner-drawn-menus-and-the-wm_measureitem-message"></a>Owner-Drawn Menüs und die "WM \_ MeasureItem"-Meldung

Bevor das System zum ersten Mal ein vom Besitzer gezeichnetes Menü Element anzeigt, sendet es die " [**WM \_ MeasureItem**](../controls/wm-measureitem.md) "-Meldung an die Fenster Prozedur des Fensters, das das Menü des Elements besitzt. Diese Meldung enthält einen Zeiger auf eine [**measureitemstruct**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) -Struktur, die das Element identifiziert und die Elementdaten enthält, die einer Anwendung möglicherweise zugewiesen wurden. Die Fenster Prozedur muss die Elemente **ItemWidth** und **ItemHeight** der Struktur ausfüllen, bevor Sie von der Verarbeitung der Nachricht zurückgegeben wird. Das System verwendet die Informationen in diesen Membern beim Erstellen des umgebenden Rechtecks, in dem eine Anwendung das Menü Element zeichnet. Außerdem werden die Informationen verwendet, um zu erkennen, wann der Benutzer das Element auswählt.

### <a name="owner-drawn-menus-and-the-wm_drawitem-message"></a>Owner-Drawn Menüs und die WM- \_ DrawItem-Nachricht

Wenn das Element gezeichnet werden muss (z. b. wenn es zum ersten Mal angezeigt wird oder wenn der Benutzer es auswählt), sendet das System die [**WM \_ DrawItem**](../controls/wm-drawitem.md) -Nachricht an die Fenster Prozedur des Besitzer Fensters des Menüs. Diese Meldung enthält einen Zeiger auf eine [**drawitemstruct**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) -Struktur, die Informationen über das Element enthält, einschließlich der Elementdaten, die einer Anwendung möglicherweise zugewiesen wurden. Außerdem enthält **drawitemstruct** Flags, die den Zustand des Elements angeben (z. b. ob es abgeblendet oder ausgewählt ist), sowie ein umgebenden Rechteck und einen Gerätekontext, den die Anwendung zum Zeichnen des Elements verwendet.

Eine Anwendung muss beim Verarbeiten der [**WM- \_ DrawItem**](../controls/wm-drawitem.md) -Nachricht folgende Aktionen ausführen:

-   Bestimmen Sie den Typ der Zeichnung, der erforderlich ist. Überprüfen Sie hierzu den **itemaction** -Member der [**drawitemstruct**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) -Struktur.
-   Zeichnen Sie das Menü Element entsprechend, indem Sie das umgebende Rechteck und den Gerätekontext verwenden, die aus der [**drawitemstruct**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) -Struktur abgerufen werden. Die Anwendung muss nur innerhalb des umgebenden Rechtecks gezeichnet werden. Aus Leistungsgründen gibt das System keine Teile des Bilds aus, die außerhalb des Rechtecks gezeichnet werden.
-   Stellt alle GDI-Objekte wieder her, die für den Gerätekontext des Menü Elements ausgewählt wurden.

Wenn der Benutzer das Menü Element auswählt, legt das System den **itemaction** -Member [**der drawitemstruct**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) -Struktur auf den Wert für die **ODA- \_ Auswahl** fest und legt den **\_ ausgewählten ODS** -Wert im **ItemState** -Member fest. Dies ist der Hinweis einer Anwendung, um das Menü Element neu zu zeichnen, um anzugeben, dass es ausgewählt ist.

### <a name="owner-drawn-menus-and-the-wm_menuchar-message"></a>Owner-Drawn Menüs und die WM- \_ menuchar-Meldung

Menüs, die keine von einem Besitzer gezeichneten Menüs sind, können ein mnetmonisches Menü angeben, indem Sie einen Unterstrich neben einem Zeichen in der Menü Zeichenfolge einfügen. Dies ermöglicht dem Benutzer das Auswählen des Menüs durch Drücken von alt und drücken des Menüs mnetmonisches Zeichen. In den von einem Besitzer gezeichneten Menüs können Sie jedoch kein mnetmonisches Menü auf diese Weise angeben. Stattdessen muss Ihre Anwendung die [**WM \_ menuchar**](wm-menuchar.md) -Nachricht verarbeiten, um von einem Besitzer gezeichnete Menüs mit Menü-mnetmonics bereitzustellen.

Die " [**WM \_ menuchar**](wm-menuchar.md) "-Meldung wird gesendet, wenn der Benutzer ein Menü "mnetmonic" eingibt, das mit keinem der vordefinierten mmaics des aktuellen Menüs identisch ist. Der in *wParam* enthaltene Wert gibt das ASCII-Zeichen an, das dem Schlüssel entspricht, den der Benutzer mit der Alt-Taste gedrückt hat. Das nieder wertige Wort von *wParam* gibt den Typ des ausgewählten Menüs an und kann einen der folgenden Werte aufweisen:

-   **MF \_ Popup** , wenn das aktuelle Menü ein Untermenü ist.
-   **MF \_ Sysmenu** , wenn das Menü das Systemmenü ist.

Das hochwertige Wort von *wParam* enthält das Menü Handle für das aktuelle Menü. Das Fenster mit den von einem Besitzer gezeichneten Menüs kann [**WM \_ menuchar**](wm-menuchar.md) wie folgt verarbeiten:


```
   case WM_MENUCHAR:
      nIndex = Determine index of menu item to be selected from
               character that was typed and handle to the current
               menu.
      return MAKELRESULT(nIndex, 2);
```



Mit den beiden im höherwertigen Wort des Rückgabewerts wird dem System mitgeteilt, dass das nieder wertige Wort des Rückgabewerts den NULL basierten Index des auszuwählenden Menü Elements enthält.

Die folgenden Konstanten entsprechen den möglichen Rückgabe Werten der WM- [**\_ menuchar**](wm-menuchar.md) -Nachricht.



| Konstante         | Wert | Bedeutung                                                                                                                                                       |
|------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MNC \_ ignorieren**  | 0     | Das System sollte das vom Benutzer gedrückte Zeichen verwerfen und auf dem System Sprecher ein kurzes Signal erstellen.                                                       |
| **MNC- \_ Schließen**   | 1     | Das System sollte das aktive Menü schließen.                                                                                                                      |
| **MNC- \_ Ausführung** | 2     | Das System sollte das im nieder wertigen Wort des Rückgabewerts angegebene Element auswählen. Das Besitzer Fenster empfängt eine [**WM- \_ Befehls**](wm-command.md) Meldung. |
| **MNC \_ SELECT**  | 3     | Das System sollte das im nieder wertigen Wort des Rückgabewerts angegebene Element auswählen.                                                                        |



 

### <a name="setting-fonts-for-menu-item-text-strings"></a>Festlegen von Schriftarten für Menu-Item Text Zeichenfolgen

Dieses Thema enthält ein Beispiel für eine Anwendung, die in einem Menü von einem Besitzer gezeichnete Menü Elemente verwendet. Das Menü enthält Elemente, die die Attribute der aktuellen Schriftart festlegen, und die Elemente werden mit dem entsprechenden Font-Attribut angezeigt.

Hier sehen Sie, wie das Menü in der Ressourcen Definitionsdatei definiert ist. Beachten Sie, dass die Zeichen folgen für die Menü Elemente "regulär", "Fett", "Kursiv" und "Unterstreichung" zur Laufzeit zugewiesen werden, sodass Ihre Zeichen folgen in der Ressourcen Definitionsdatei leer sind.


```
MainMenu MENU 
BEGIN 
    POPUP   "&Character" 
    BEGIN 
        MENUITEM    "",    IDM_REGULAR 
        MENUITEM SEPARATOR 
        MENUITEM    "",    IDM_BOLD 
        MENUITEM    "",    IDM_ITALIC 
        MENUITEM    "",    IDM_ULINE 
    END 
END 
```



Die Fenster Prozedur der Anwendung verarbeitet die Nachrichten, die an der Verwendung von vom Besitzer gezeichneten Menü Elementen beteiligt sind. Die Anwendung verwendet die [**WM \_ Create**](/windows/desktop/winmsg/wm-create) -Nachricht, um Folgendes durchzuführen:

-   Legen Sie für die Menü Elemente das-Flag für den **MF \_** -Besitzer fest.
-   Legen Sie die Text Zeichenfolgen für die Menü Elemente fest.
-   Ruft Handles der Schriftarten ab, die zum Zeichnen der Elemente verwendet werden.
-   Ruft die Text-und Hintergrund Farbwerte für ausgewählte Menü Elemente ab.

Die Text Zeichenfolgen und Schriftart Handles werden in einem Array von Anwendungs definierten myItem-Strukturen gespeichert. Die Anwendungs definierte getafont-Funktion erstellt eine Schriftart, die dem angegebenen Schriftart Attribut entspricht, und gibt ein Handle für die Schriftart zurück. Die Handles werden während der Verarbeitung der WM- [**\_ zerstörungsnachricht**](/windows/desktop/winmsg/wm-destroy) zerstört.

Während der Verarbeitung der " [**WM \_ MeasureItem**](../controls/wm-measureitem.md) "-Nachricht Ruft das Beispiel die Breite und Höhe einer Menü Element Zeichenfolge ab und kopiert diese Werte in die [**measureitemstruct**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) -Struktur. Das System verwendet die Width-und Height-Werte, um die Größe des Menüs zu berechnen.

Während der Verarbeitung der [**WM- \_ DrawItem**](../controls/wm-drawitem.md) -Nachricht wird die Zeichenfolge des Menü Elements mit Raum links neben der Zeichenfolge für das Häkchen-Bitmap gezeichnet. Wenn der Benutzer das Element auswählt, werden die ausgewählten Text-und Hintergrundfarben verwendet, um das Element zu zeichnen.


```
LRESULT APIENTRY MainWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
 
    typedef struct _MYITEM 
    { 
        HFONT hfont; 
        LPSTR psz; 
    } MYITEM;             // structure for item font and string  
 
    MYITEM *pmyitem;      // pointer to item's font and string        
    static MYITEM myitem[CITEMS];   // array of MYITEMS               
    static HMENU hmenu;             // handle to main menu            
    static COLORREF crSelText;  // text color of selected item        
    static COLORREF crSelBkgnd; // background color of selected item  
    COLORREF crText;            // text color of unselected item      
    COLORREF crBkgnd;           // background color unselected item   
    LPMEASUREITEMSTRUCT lpmis;  // pointer to item of data             
    LPDRAWITEMSTRUCT lpdis;     // pointer to item drawing data        
    HDC hdc;                    // handle to screen DC                
    SIZE size;                  // menu-item text extents             
    WORD wCheckX;               // check-mark width                   
    int nTextX;                 // width of menu item                 
    int nTextY;                 // height of menu item                
    int i;                      // loop counter                       
    HFONT hfontOld;             // handle to old font                 
    BOOL fSelected = FALSE;     // menu-item selection flag
    size_t * pcch;
    HRESULT hResult;           
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Modify the Regular, Bold, Italic, and Underline 
            // menu items to make them owner-drawn items. Associate 
            // a MYITEM structure with each item to contain the 
            // string for and font handle to each item. 
 
            hmenu = GetMenu(hwnd); 
            ModifyMenu(hmenu, IDM_REGULAR, MF_BYCOMMAND | 
                MF_CHECKED | MF_OWNERDRAW, IDM_REGULAR, 
                (LPTSTR) &myitem[REGULAR]); 
            ModifyMenu(hmenu, IDM_BOLD, MF_BYCOMMAND | 
                MF_OWNERDRAW, IDM_BOLD, (LPTSTR) &myitem[BOLD]); 
            ModifyMenu(hmenu, IDM_ITALIC, MF_BYCOMMAND | 
                MF_OWNERDRAW, IDM_ITALIC, 
                (LPTSTR) &myitem[ITALIC]); 
            ModifyMenu(hmenu, IDM_ULINE, MF_BYCOMMAND | 
                MF_OWNERDRAW, IDM_ULINE, (LPTSTR) &myitem[ULINE]); 
 
            // Retrieve each item's font handle and copy it into 
            // the hfont member of each item's MYITEM structure. 
            // Also, copy each item's string into the structures. 
 
            myitem[REGULAR].hfont = GetAFont(REGULAR); 
            myitem[REGULAR].psz = "Regular"; 
            myitem[BOLD].hfont = GetAFont(BOLD); 
            myitem[BOLD].psz = "Bold"; 
            myitem[ITALIC].hfont = GetAFont(ITALIC); 
            myitem[ITALIC].psz = "Italic"; 
            myitem[ULINE].hfont = GetAFont(ULINE); 
            myitem[ULINE].psz = "Underline"; 
 
            // Retrieve the text and background colors of the 
            // selected menu text. 
 
            crSelText = GetSysColor(COLOR_HIGHLIGHTTEXT); 
            crSelBkgnd = GetSysColor(COLOR_HIGHLIGHT); 
 
            return 0; 
 
        case WM_MEASUREITEM: 
 
            // Retrieve a device context for the main window.  
 
            hdc = GetDC(hwnd); 
 
            // Retrieve pointers to the menu item's 
            // MEASUREITEMSTRUCT structure and MYITEM structure. 
 
            lpmis = (LPMEASUREITEMSTRUCT) lParam; 
            pmyitem = (MYITEM *) lpmis->itemData; 
 
            // Select the font associated with the item into 
            // the main window's device context. 
 
            hfontOld = SelectObject(hdc, pmyitem->hfont); 
 
            // Retrieve the width and height of the item's string, 
            // and then copy the width and height into the 
            // MEASUREITEMSTRUCT structure's itemWidth and 
            // itemHeight members.
            
            hResult = StringCchLength(pmyitem->psz,STRSAFE_MAX_CCH, pcch);
            if (FAILED(hResult))
            {
            // Add code to fail as securely as possible.
                return;
            } 
 
            GetTextExtentPoint32(hdc, pmyitem->psz, 
                *pcch, &size); 
            lpmis->itemWidth = size.cx; 
            lpmis->itemHeight = size.cy; 
 
            // Select the old font back into the device context, 
            // and then release the device context. 
 
            SelectObject(hdc, hfontOld); 
            ReleaseDC(hwnd, hdc); 
 
            return TRUE; 
 
            break; 
 
        case WM_DRAWITEM: 
 
            // Get pointers to the menu item's DRAWITEMSTRUCT 
            // structure and MYITEM structure. 
 
            lpdis = (LPDRAWITEMSTRUCT) lParam; 
            pmyitem = (MYITEM *) lpdis->itemData; 
 
            // If the user has selected the item, use the selected 
            // text and background colors to display the item. 
 
            if (lpdis->itemState & ODS_SELECTED) 
            { 
                crText = SetTextColor(lpdis->hDC, crSelText); 
                crBkgnd = SetBkColor(lpdis->hDC, crSelBkgnd); 
                fSelected = TRUE; 
            } 
 
            // Remember to leave space in the menu item for the 
            // check-mark bitmap. Retrieve the width of the bitmap 
            // and add it to the width of the menu item. 
 
            wCheckX = GetSystemMetrics(SM_CXMENUCHECK); 
            nTextX = wCheckX + lpdis->rcItem.left; 
            nTextY = lpdis->rcItem.top; 
 
            // Select the font associated with the item into the 
            // item's device context, and then draw the string. 
 
            hfontOld = SelectObject(lpdis->hDC, pmyitem->hfont);
            
            hResult = StringCchLength(pmyitem->psz,STRSAFE_MAX_CCH, pcch);
            if (FAILED(hResult))
            {
            // Add code to fail as securely as possible.
                return;
            } 
 
            ExtTextOut(lpdis->hDC, nTextX, nTextY, ETO_OPAQUE, 
                &lpdis->rcItem, pmyitem->psz, 
                *pcch, NULL); 
 
            // Select the previous font back into the device 
            // context. 
 
            SelectObject(lpdis->hDC, hfontOld); 
 
            // Return the text and background colors to their 
            // normal state (not selected). 
 
            if (fSelected) 
            { 
                SetTextColor(lpdis->hDC, crText); 
                SetBkColor(lpdis->hDC, crBkgnd); 
            } 
 
            return TRUE; 
 
        // Process other messages.  
 
        case WM_DESTROY: 
 
            // Destroy the menu items' font handles.  
 
            for (i = 0; i < CITEMS; i++) 
                DeleteObject(myitem[i].hfont); 
 
            PostQuitMessage(0); 
            break; 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
 
HFONT GetAFont(int fnFont) 
{ 
    static LOGFONT lf;  // structure for font information  
 
    // Get a handle to the ANSI fixed-pitch font, and copy 
    // information about the font to a LOGFONT structure. 
 
    GetObject(GetStockObject(ANSI_FIXED_FONT), sizeof(LOGFONT), 
        &lf); 
 
    // Set the font attributes, as appropriate.  
 
    if (fnFont == BOLD) 
        lf.lfWeight = FW_BOLD; 
    else 
        lf.lfWeight = FW_NORMAL; 
 
    lf.lfItalic = (fnFont == ITALIC); 
    lf.lfItalic = (fnFont == ULINE); 
 
    // Create the font, and then return its handle.  
 
    return CreateFont(lf.lfHeight, lf.lfWidth, 
        lf.lfEscapement, lf.lfOrientation, lf.lfWeight, 
        lf.lfItalic, lf.lfUnderline, lf.lfStrikeOut, lf.lfCharSet, 
        lf.lfOutPrecision, lf.lfClipPrecision, lf.lfQuality, 
        lf.lfPitchAndFamily, lf.lfFaceName); 
} 
```



### <a name="example-of-owner-drawn-menu-items"></a>Beispiel für Owner-Drawn Menü Elemente

Im Beispiel in diesem Thema werden vom Besitzer gezeichnete Menü Elemente in einem Menü verwendet. Die Menü Elemente wählen bestimmte Schriftart Attribute aus, und die Anwendung zeigt jedes Menü Element mit einer Schriftart an, die das entsprechende-Attribut aufweist. Beispielsweise wird das Menü Element **kursiv** formatiert angezeigt. Der Name des **Zeichen** Menüs in der Menüleiste öffnet das Menü.

Die Menüleiste und das Dropdown Menü werden anfänglich durch eine erweiterte Menü Vorlagen Ressource definiert. Da eine Menüvorlage keine von einem Besitzer gezeichneten Elemente angeben kann, enthält das Menü anfänglich vier Text Menü Elemente mit den folgenden Zeichen folgen: "Regular", "Bold", "Kursiv" und "unterstrichen". Die Fenster Prozedur der Anwendung ändert diese in vom Besitzer gezeichnete Elemente, wenn die [**WM \_ Create**](/windows/desktop/winmsg/wm-create) -Nachricht verarbeitet wird. Beim Empfang der **WM \_ Create** -Nachricht Ruft die Fenster Prozedur die Anwendungs definierte OnCreate-Funktion auf, die die folgenden Schritte für jedes Menü Element ausführt:

-   Ordnet eine von der Anwendung definierte myItem-Struktur zu.
-   Ruft den Text des Menü Elements ab und speichert ihn in der von der Anwendung definierten myItem-Struktur.
-   Erstellt die Schriftart, die zum Anzeigen des Menü Elements verwendet wird, und speichert das Handle in der von der Anwendung definierten myItem-Struktur.
-   Ändert den Menü Elementtyp in **MFT \_** -Besitzer zeichnen und speichert einen Zeiger auf die Anwendungs definierte myItem-Struktur als Elementdaten.

Da ein Zeiger auf jede Anwendungs definierte myItem-Struktur als Elementdaten gespeichert wird, wird Sie in Verbindung mit den Nachrichten " [**WM \_ MeasureItem**](../controls/wm-measureitem.md) " und " [**WM \_ DrawItem**](../controls/wm-drawitem.md) " für das entsprechende Menü Element an die Fenster Prozedur übergeben. Der-Zeiger ist im **ItemData** -Member der [**measureitemstruct**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) -Struktur und der [**drawitemstruct**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) -Struktur enthalten.

Bei der ersten Anzeige wird eine [**WM \_ MeasureItem**](../controls/wm-measureitem.md) -Meldung für jedes Menü Element gesendet, das vom Besitzer gezeichnet wird. Die Anwendung verarbeitet diese Nachricht, indem die Schriftart für das Menü Element in einen Gerätekontext ausgewählt und dann der erforderliche Speicherplatz für die Anzeige des Menü Element Texts in dieser Schriftart festgelegt wird. Der Text für Schriftart und Menü Element wird durch die Struktur des Menü Elements `MYITEM` (die von der Anwendung definierte Struktur) angegeben. Die Anwendung bestimmt die Größe des Texts mithilfe der [**GetTextExtentPoint32**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpoint32a) -Funktion.

Die Fenster Prozedur verarbeitet die [**WM- \_ DrawItem**](../controls/wm-drawitem.md) -Nachricht, indem der Menü Element Text in der entsprechenden Schriftart angezeigt wird. Der Schriftart-und Menü Element Text wird durch die Struktur des Menü Elements angegeben `MYITEM` . Die Anwendung wählt Text und Hintergrundfarben aus, die für den Zustand des Menü Elements geeignet sind.

Die Fenster Prozedur verarbeitet die [**WM- \_ zerstörungsnachricht**](/windows/desktop/winmsg/wm-destroy) , um Schriftarten zu zerstören und Arbeitsspeicher freizugeben. Die Anwendung löscht die Schriftart und gibt die von der Anwendung definierte myItem-Struktur für jedes Menü Element frei.

Im folgenden finden Sie die relevanten Teile der Header Datei der Anwendung.


```
// Menu-item identifiers for the Character menu 
 
#define IDM_CHARACTER 10 
#define IDM_REGULAR   11 
#define IDM_BOLD      12 
#define IDM_ITALIC    13 
#define IDM_UNDERLINE 14 
 
// Structure associated with menu items 
 
typedef struct tagMYITEM 
{ 
    HFONT hfont; 
    int   cchItemText; 
    char  szItemText[1]; 
} MYITEM; 
 
#define CCH_MAXITEMTEXT 256 
 
```



Im folgenden sind die relevanten Teile der Fenster Prozedur der Anwendung und die zugehörigen Funktionen beschrieben.


```
LRESULT CALLBACK MainWindowProc( 
        HWND hwnd, 
        UINT uMsg, 
        WPARAM wParam, 
        LPARAM lParam 
        ) 
{ 
    switch (uMsg) 
    { 
        case WM_CREATE: 
            if (!OnCreate(hwnd)) 
                return -1; 
            break; 
 
        case WM_DESTROY: 
            OnDestroy(hwnd); 
            PostQuitMessage(0); 
            break; 
 
        case WM_MEASUREITEM: 
            OnMeasureItem(hwnd, (LPMEASUREITEMSTRUCT) lParam); 
            return TRUE; 
 
        case WM_DRAWITEM: 
            OnDrawItem(hwnd, (LPDRAWITEMSTRUCT) lParam); 
            return TRUE; 
 
        // Additional message processing goes here. 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return 0; 
} 
 
 
BOOL WINAPI OnCreate(HWND hwnd) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
    UINT uID; 
    MYITEM *pMyItem; 
 
    // Get a handle to the pop-up menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Modify each menu item. Assume that the IDs IDM_REGULAR 
    // through IDM_UNDERLINE are consecutive numbers. 
 
    for (uID = IDM_REGULAR; uID <= IDM_UNDERLINE; uID++) 
    { 
         // Allocate an item structure, leaving space for a 
         // string of up to CCH_MAXITEMTEXT characters. 
 
        pMyItem = (MYITEM *) LocalAlloc(LMEM_FIXED, 
                sizeof(MYITEM) + CCH_MAXITEMTEXT); 
 
        // Save the item text in the item structure. 
 
        mii.fMask = MIIM_STRING; 
        mii.dwTypeData = pMyItem->szItemText; 
        mii.cch = CCH_MAXITEMTEXT; 
        GetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
        pMyItem->cchItemText = mii.cch; 
 
        // Reallocate the structure to the minimum required size. 
 
        pMyItem = (MYITEM *) LocalReAlloc(pMyItem, 
                sizeof(MYITEM) + mii.cch, LMEM_MOVEABLE); 
 
        // Create the font used to draw the item. 
 
        pMyItem->hfont = CreateMenuItemFont(uID); 
 
        // Change the item to an owner-drawn item, and save 
        // the address of the item structure as item data. 
 
        mii.fMask = MIIM_FTYPE | MIIM_DATA; 
        mii.fType = MFT_OWNERDRAW; 
        mii.dwItemData = (ULONG_PTR) pMyItem; 
        SetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
    } 
    return TRUE; 
} 
 
HFONT CreateMenuItemFont(UINT uID) 
{ 
    LOGFONT lf;
    HRESULT hr; 
 
    ZeroMemory(&lf, sizeof(lf)); 
    lf.lfHeight = 20; 
    hr = StringCchCopy(lf.lfFaceName, 32, "Times New Roman");
    if (FAILED(hr))
    {
    // TODO: writer error handler
    } 
 
    switch (uID) 
    { 
        case IDM_BOLD: 
            lf.lfWeight = FW_HEAVY; 
            break; 
 
        case IDM_ITALIC: 
            lf.lfItalic = TRUE; 
            break; 
 
        case IDM_UNDERLINE: 
            lf.lfUnderline = TRUE; 
            break; 
    } 
    return CreateFontIndirect(&lf); 
} 
 
VOID WINAPI OnDestroy(HWND hwnd) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
    UINT uID; 
    MYITEM *pMyItem; 
 
    // Get a handle to the menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get  
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Free resources associated with each menu item. 
 
    for (uID = IDM_REGULAR; uID <= IDM_UNDERLINE; uID++) 
    { 
        // Get the item data. 
 
        mii.fMask = MIIM_DATA; 
        GetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
        pMyItem = (MYITEM *) mii.dwItemData; 
 
        // Destroy the font and free the item structure. 
 
        DeleteObject(pMyItem->hfont); 
        LocalFree(pMyItem); 
    } 
} 
 
VOID WINAPI OnMeasureItem(HWND hwnd, LPMEASUREITEMSTRUCT lpmis) 
{ 
    MYITEM *pMyItem = (MYITEM *) lpmis->itemData; 
    HDC hdc = GetDC(hwnd); 
    HFONT hfntOld = (HFONT)SelectObject(hdc, pMyItem->hfont); 
    SIZE size; 
 
    GetTextExtentPoint32(hdc, pMyItem->szItemText, 
            pMyItem->cchItemText, &size); 
 
    lpmis->itemWidth = size.cx; 
    lpmis->itemHeight = size.cy; 
 
    SelectObject(hdc, hfntOld); 
    ReleaseDC(hwnd, hdc); 
} 
 
VOID WINAPI OnDrawItem(HWND hwnd, LPDRAWITEMSTRUCT lpdis) 
{ 
    MYITEM *pMyItem = (MYITEM *) lpdis->itemData; 
    COLORREF clrPrevText, clrPrevBkgnd; 
    HFONT hfntPrev; 
    int x, y; 
 
    // Set the appropriate foreground and background colors. 
 
    if (lpdis->itemState & ODS_SELECTED) 
    { 
        clrPrevText = SetTextColor(lpdis->hDC, 
                GetSysColor(COLOR_HIGHLIGHTTEXT)); 
        clrPrevBkgnd = SetBkColor(lpdis->hDC, 
                GetSysColor(COLOR_HIGHLIGHT)); 
    } 
    else 
    { 
        clrPrevText = SetTextColor(lpdis->hDC, 
                GetSysColor(COLOR_MENUTEXT)); 
        clrPrevBkgnd = SetBkColor(lpdis->hDC, 
                GetSysColor(COLOR_MENU)); 
    } 
 
    // Determine where to draw and leave space for a check mark. 
 
    x = lpdis->rcItem.left; 
    y = lpdis->rcItem.top; 
    x += GetSystemMetrics(SM_CXMENUCHECK); 
 
    // Select the font and draw the text. 
 
    hfntPrev = (HFONT)SelectObject(lpdis->hDC, pMyItem->hfont); 
    ExtTextOut(lpdis->hDC, x, y, ETO_OPAQUE, 
            &lpdis->rcItem, pMyItem->szItemText, 
            pMyItem->cchItemText, NULL); 
 
    // Restore the original font and colors. 
 
    SelectObject(lpdis->hDC, hfntPrev); 
    SetTextColor(lpdis->hDC, clrPrevText); 
    SetBkColor(lpdis->hDC, clrPrevBkgnd); 
} 
```



## <a name="using-custom-check-mark-bitmaps"></a>Verwenden von benutzerdefinierten Häkchen-Bitmaps

Das System stellt eine Standard Bitmap für das Häkchen bereit, die neben einem ausgewählten Menü Element angezeigt wird. Sie können ein einzelnes Menü Element anpassen, indem Sie ein Bitmappaar bereitstellen, um die Standard Bitmap für das Häkchen zu ersetzen. Das System zeigt eine Bitmap an, wenn das Element ausgewählt wird, und das andere, wenn es klar ist. In diesem Abschnitt werden die Schritte zum Erstellen und Verwenden von benutzerdefinierten Prüfzeichen-Bitmaps beschrieben.

-   [Erstellen von benutzerdefinierten Häkchen Bitmaps](#creating-custom-check-mark-bitmaps)
-   [Zuordnen von Bitmaps zu einem Menü Element](#associating-bitmaps-with-a-menu-item)
-   [Festlegen des Häkchen Attributs](#setting-the-check-mark-attribute)
-   [Simulieren von Kontrollkästchen in einem Menü](#simulating-check-boxes-in-a-menu)
-   [Beispiel für die Verwendung von benutzerdefinierten Bitmaps für das Häkchen](#example-of-using-custom-check-mark-bitmaps)

### <a name="creating-custom-check-mark-bitmaps"></a>Erstellen von benutzerdefinierten Häkchen Bitmaps

Eine benutzerdefinierte Bitmap für das Häkchen muss dieselbe Größe aufweisen wie die Standard Bitmap für das Häkchen. Sie können die standardmäßige Häkchen Größe der Bitmap abrufen, indem Sie die [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) -Funktion aufrufen. Das nieder wertige Wort des Rückgabewerts dieser Funktion gibt die Breite an. das höchst wertige Wort gibt die Höhe an.

Sie können Bitmapressourcen verwenden, um Bitmaps für das Häkchen bereitzustellen. Da die erforderliche Bitmapgröße je nach Anzeigetyp variiert, müssen Sie möglicherweise die Größe der Bitmap zur Laufzeit ändern, indem Sie die [**StretchBlt**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) -Funktion verwenden. Abhängig von der Bitmap kann die durch die Größenänderung verursachte Verzerrung zu nicht akzeptablen Ergebnissen führen.

Anstatt eine Bitmap-Ressource zu verwenden, können Sie mithilfe von GDI-Funktionen zur Laufzeit eine Bitmap erstellen.

**So erstellen Sie eine Bitmap zur Laufzeit**

1.  Verwenden Sie [**die Funktion**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) "Funktion", um einen Gerätekontext zu erstellen, der mit dem vom Hauptfenster der Anwendung verwendeten kompatibel ist.

    Der *hdc* -Parameter der Funktion kann entweder **null** oder den Rückgabewert der Funktion angeben. " [**Kreatecompatibledc**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) " gibt ein Handle an den kompatiblen Gerätekontext zurück.

2.  Verwenden Sie [**die Funktion "**](/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap) -Funktion", um eine Bitmap zu erstellen, die mit dem Hauptfenster der Anwendung kompatibel ist.

    Mit den Parametern " *nwidth* " und " *nheight* " der Funktion wird die Größe der Bitmap festgelegt. Sie sollten die von der [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) -Funktion zurückgegebenen Width-und Height-Informationen angeben.

    > [!Note]  
    > Sie können auch die Funktion " [**kreatebitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) " verwenden, um eine monochrome Bitmap zu erstellen.

     

3.  Verwenden Sie die [**SelectObject**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) -Funktion, um die Bitmap in den kompatiblen Gerätekontext auszuwählen.
4.  Verwenden Sie GDI-Zeichnungsfunktionen, z. b. [**Ellipse**](/windows/desktop/api/wingdi/nf-wingdi-ellipse) und [**LineTo**](/windows/desktop/api/wingdi/nf-wingdi-lineto), um ein Bild in die Bitmap zu zeichnen, oder verwenden Sie Funktionen wie [**BitBLT**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) und [**StretchBlt**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) zum Kopieren eines Bilds in die Bitmap.

Weitere Informationen finden Sie unter [Bitmaps](/windows/desktop/gdi/bitmaps).

### <a name="associating-bitmaps-with-a-menu-item"></a>Zuordnen von Bitmaps zu einem Menü Element

Sie ordnen ein paar von Check-Mark-Bitmaps einem Menü Element zu, indem Sie die Handles der Bitmaps an die [**setmenuitembitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) -Funktion übergeben. Der *hbitmapuncheck* -Parameter identifiziert die Clear-Bitmap, und der *hbitmapcheck* -Parameter identifiziert die ausgewählte Bitmap. Wenn Sie ein oder beide Häkchen aus einem Menü Element entfernen möchten, können Sie den Parameter *hbitmapuncheck* oder *hbitmapcheck* oder beides auf **null** festlegen.

### <a name="setting-the-check-mark-attribute"></a>Festlegen des Häkchen Attributs

Die [**checkmenuitem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuitem) -Funktion legt das Häkchen Attribut eines Menü Elements auf "ausgewählt" oder "deaktiviert" fest. Sie können den von **MF \_** aktivierten Wert angeben, um das Häkchen Attribut auf "ausgewählt" festzulegen, und den Wert " **MF \_** deaktiviert", um ihn zu löschen.

Mithilfe der [**setmenuiteminfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) -Funktion können Sie auch den Status der Überprüfung eines Menü Elements festlegen.

Manchmal stellt eine Gruppe von Menü Elementen einen Satz von sich gegenseitig ausschließenden Optionen dar. Mithilfe der [**checkmenuradioitem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem) -Funktion können Sie ein Menü Element aktivieren und gleichzeitig das Häkchen aus allen anderen Menü Elementen in der Gruppe entfernen.

### <a name="simulating-check-boxes-in-a-menu"></a>Simulieren von Kontrollkästchen in einem Menü

Dieses Thema enthält ein Beispiel, das zeigt, wie Kontrollkästchen in einem Menü simuliert werden. Das Beispiel enthält ein Zeichen Menü, dessen Elemente es dem Benutzer ermöglichen, die Attribute "Bold", "Kursiv" und "unterstreichen" der aktuellen Schriftart festzulegen. Wenn ein Schriftart Attribut in Kraft ist, wird im Kontrollkästchen neben dem entsprechenden Menü Element ein Häkchen angezeigt. Andernfalls wird neben dem Element ein leeres Kontrollkästchen angezeigt.

Im Beispiel wird die Standard Bitmap für das Häkchen durch zwei Bitmaps ersetzt: eine Bitmap mit einem aktivierten Kontrollkästchen und die Bitmap mit einem leeren Feld. Das aktivierte Kontrollkästchen Bitmap wird neben dem Menü Element Fett, kursiv oder unterstrichen angezeigt, wenn das Häkchen-Attribut des Elements auf **MF \_ aktiviert** festgelegt ist. Das Kontrollkästchen Bitmap löschen oder leer wird angezeigt, wenn das Häkchen-Attribut auf **MF \_** deaktiviert festgelegt ist.

Das System stellt eine vordefinierte Bitmap bereit, die die für Kontrollkästchen und Options Felder verwendeten Bilder enthält. Im Beispiel werden die Kontrollkästchen aktiviert und leer isoliert, in zwei separate Bitmaps kopiert und dann als ausgewählte und gelöschte Bitmaps für Elemente im Menü **Zeichen** verwendet.

Zum Abrufen eines Handles für das System definierte Kontrollkästchen Bitmap Ruft das Beispiel die [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) -Funktion auf, wobei **null** als *HINSTANCE* -Parameter und **obm- \_ Kontrollkästchen** als *lpbitmapname* -Parameter angegeben wird. Da die Bilder in der Bitmap die gleiche Größe haben, kann das Beispiel diese isolieren, indem Sie die Breite und Höhe der Bitmap durch die Anzahl der Bilder in den Zeilen und Spalten dividiert.

Der folgende Teil einer Ressourcen Definitionsdatei zeigt, wie die Menü Elemente im Menü **Zeichen** definiert werden. Beachten Sie, dass keine Schriftart Attribute anfänglich sind, sodass das Häkchen-Attribut für das **reguläre** Element auf ausgewählt festgelegt ist und das Häkchen-Attribut der restlichen Elemente standardmäßig auf Clear festgelegt ist.


```
#include "men3.h" 
 
MainMenu MENU 
BEGIN 
    POPUP   "&Character" 
    BEGIN 
        MENUITEM    "&Regular",     IDM_REGULAR, CHECKED 
        MENUITEM SEPARATOR 
        MENUITEM    "&Bold",        IDM_BOLD 
        MENUITEM    "&Italic",      IDM_ITALIC 
        MENUITEM    "&Underline",   IDM_ULINE 
    END 
END
```



Dies sind die relevanten Inhalte der Header Datei der Anwendung.


```
// Menu-item identifiers  
 
#define IDM_REGULAR 0x1 
#define IDM_BOLD    0x2 
#define IDM_ITALIC  0x4 
#define IDM_ULINE   0x8 
 
// Check-mark flags  
 
#define CHECK   1 
#define UNCHECK 2 
 
// Font-attribute mask  
 
#define ATTRIBMASK 0xe 
 
// Function prototypes  
 
LRESULT APIENTRY MainWndProc(HWND, UINT, WPARAM, LPARAM); 
HBITMAP GetMyCheckBitmaps(UINT); 
BYTE CheckOrUncheckMenuItem(BYTE, HMENU); 
```



Im folgenden Beispiel werden die Teile der Fenster Prozedur gezeigt, die die Prüfzeichen-Bitmaps erstellen. Legen Sie das Häkchen Attribut der Menü Elemente **Fett**, **kursiv** und unter **Streichung** fest. und zerstören Kontrollkästchen-Bitmaps.


```
LRESULT APIENTRY MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
 
    static HBITMAP hbmpCheck;   // handle to checked bitmap    
    static HBITMAP hbmpUncheck; // handle to unchecked bitmap  
    static HMENU hmenu;         // handle to main menu         
    BYTE fbFontAttrib;          // font-attribute flags        
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Call the application-defined GetMyCheckBitmaps 
            // function to get the predefined checked and 
            // unchecked check box bitmaps. 
 
            hbmpCheck = GetMyCheckBitmaps(CHECK); 
            hbmpUncheck = GetMyCheckBitmaps(UNCHECK); 
 
            // Set the checked and unchecked bitmaps for the menu 
            // items. 
 
            hmenu = GetMenu(hwndMain); 
            SetMenuItemBitmaps(hmenu, IDM_BOLD, MF_BYCOMMAND, 
                hbmpUncheck, hbmpCheck); 
            SetMenuItemBitmaps(hmenu, IDM_ITALIC, MF_BYCOMMAND, 
                hbmpUncheck, hbmpCheck); 
            SetMenuItemBitmaps(hmenu, IDM_ULINE, MF_BYCOMMAND, 
                hbmpUncheck, hbmpCheck); 
 
            return 0; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                // Process the menu commands.  
 
                case IDM_REGULAR: 
                case IDM_BOLD: 
                case IDM_ITALIC: 
                case IDM_ULINE: 
 
                    // CheckOrUncheckMenuItem is an application- 
                    // defined function that sets the menu item 
                    // checkmarks and returns the user-selected 
                    // font attributes. 
 
                    fbFontAttrib = CheckOrUncheckMenuItem( 
                        (BYTE) LOWORD(wParam), hmenu); 
 
                    // Set the font attributes.  
 
                    return 0; 
 
                // Process other command messages.  
 
                default: 
                    break; 
            } 
 
            break; 
 
        // Process other window messages.  
 
        case WM_DESTROY: 
 
            // Destroy the checked and unchecked bitmaps.  
 
            DeleteObject(hbmpCheck); 
            DeleteObject(hbmpUncheck); 
 
            PostQuitMessage(0); 
            break; 
 
        default: 
            return DefWindowProc(hwndMain, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
 
HBITMAP GetMyCheckBitmaps(UINT fuCheck) 
{ 
    COLORREF crBackground;  // background color                  
    HBRUSH hbrBackground;   // background brush                  
    HBRUSH hbrTargetOld;    // original background brush         
    HDC hdcSource;          // source device context             
    HDC hdcTarget;          // target device context             
    HBITMAP hbmpCheckboxes; // handle to check-box bitmap        
    BITMAP bmCheckbox;      // structure for bitmap data         
    HBITMAP hbmpSourceOld;  // handle to original source bitmap  
    HBITMAP hbmpTargetOld;  // handle to original target bitmap  
    HBITMAP hbmpCheck;      // handle to check-mark bitmap       
    RECT rc;                // rectangle for check-box bitmap    
    WORD wBitmapX;          // width of check-mark bitmap        
    WORD wBitmapY;          // height of check-mark bitmap       
 
    // Get the menu background color and create a solid brush 
    // with that color. 
 
    crBackground = GetSysColor(COLOR_MENU); 
    hbrBackground = CreateSolidBrush(crBackground); 
 
    // Create memory device contexts for the source and 
    // destination bitmaps. 
 
    hdcSource = CreateCompatibleDC((HDC) NULL); 
    hdcTarget = CreateCompatibleDC(hdcSource); 
 
    // Get the size of the system default check-mark bitmap and 
    // create a compatible bitmap of the same size. 
 
    wBitmapX = GetSystemMetrics(SM_CXMENUCHECK); 
    wBitmapY = GetSystemMetrics(SM_CYMENUCHECK); 
 
    hbmpCheck = CreateCompatibleBitmap(hdcSource, wBitmapX, 
        wBitmapY); 
 
    // Select the background brush and bitmap into the target DC. 
 
    hbrTargetOld = SelectObject(hdcTarget, hbrBackground); 
    hbmpTargetOld = SelectObject(hdcTarget, hbmpCheck); 
 
    // Use the selected brush to initialize the background color 
    // of the bitmap in the target device context. 
 
    PatBlt(hdcTarget, 0, 0, wBitmapX, wBitmapY, PATCOPY); 
 
    // Load the predefined check box bitmaps and select it 
    // into the source DC. 
 
    hbmpCheckboxes = LoadBitmap((HINSTANCE) NULL, 
        (LPTSTR) OBM_CHECKBOXES); 
 
    hbmpSourceOld = SelectObject(hdcSource, hbmpCheckboxes); 
 
    // Fill a BITMAP structure with information about the 
    // check box bitmaps, and then find the upper-left corner of 
    // the unchecked check box or the checked check box. 
 
    GetObject(hbmpCheckboxes, sizeof(BITMAP), &bmCheckbox); 
 
    if (fuCheck == UNCHECK) 
    { 
        rc.left = 0; 
        rc.right = (bmCheckbox.bmWidth / 4); 
    } 
    else 
    { 
        rc.left = (bmCheckbox.bmWidth / 4); 
        rc.right = (bmCheckbox.bmWidth / 4) * 2; 
    } 
 
    rc.top = 0; 
    rc.bottom = (bmCheckbox.bmHeight / 3); 
 
    // Copy the appropriate bitmap into the target DC. If the 
    // check-box bitmap is larger than the default check-mark 
    // bitmap, use StretchBlt to make it fit; otherwise, just 
    // copy it. 
 
    if (((rc.right - rc.left) > (int) wBitmapX) || 
            ((rc.bottom - rc.top) > (int) wBitmapY)) 
    {
        StretchBlt(hdcTarget, 0, 0, wBitmapX, wBitmapY, 
            hdcSource, rc.left, rc.top, rc.right - rc.left, 
            rc.bottom - rc.top, SRCCOPY); 
    }
 
    else 
    {
        BitBlt(hdcTarget, 0, 0, rc.right - rc.left, 
            rc.bottom - rc.top, 
            hdcSource, rc.left, rc.top, SRCCOPY); 
    }
 
    // Select the old source and destination bitmaps into the 
    // source and destination DCs, and then delete the DCs and 
    // the background brush. 
 
    SelectObject(hdcSource, hbmpSourceOld); 
    SelectObject(hdcTarget, hbrTargetOld); 
    hbmpCheck = SelectObject(hdcTarget, hbmpTargetOld); 
 
    DeleteObject(hbrBackground); 
    DeleteObject(hdcSource); 
    DeleteObject(hdcTarget); 
 
    // Return a handle to the new check-mark bitmap.  
 
    return hbmpCheck; 
} 
 
 
BYTE CheckOrUncheckMenuItem(BYTE bMenuItemID, HMENU hmenu) 
{ 
    DWORD fdwMenu; 
    static BYTE fbAttributes; 
 
    switch (bMenuItemID) 
    { 
        case IDM_REGULAR: 
 
            // Whenever the Regular menu item is selected, add a 
            // check mark to it and then remove checkmarks from 
            // any font-attribute menu items. 
 
            CheckMenuItem(hmenu, IDM_REGULAR, MF_BYCOMMAND | 
                MF_CHECKED); 
 
            if (fbAttributes & ATTRIBMASK) 
            { 
                CheckMenuItem(hmenu, IDM_BOLD, MF_BYCOMMAND | 
                    MF_UNCHECKED); 
                CheckMenuItem(hmenu, IDM_ITALIC, MF_BYCOMMAND | 
                    MF_UNCHECKED); 
                CheckMenuItem(hmenu, IDM_ULINE, MF_BYCOMMAND | 
                    MF_UNCHECKED); 
            } 
            fbAttributes = IDM_REGULAR; 
            return fbAttributes; 
 
        case IDM_BOLD: 
        case IDM_ITALIC: 
        case IDM_ULINE: 
 
            // Toggle the check mark for the selected menu item and 
            // set the font attribute flags appropriately. 
 
            fdwMenu = GetMenuState(hmenu, (UINT) bMenuItemID, 
                MF_BYCOMMAND); 
            if (!(fdwMenu & MF_CHECKED)) 
            { 
                CheckMenuItem(hmenu, (UINT) bMenuItemID, 
                    MF_BYCOMMAND | MF_CHECKED); 
                fbAttributes |= bMenuItemID; 
            }
            else 
            { 
                CheckMenuItem(hmenu, (UINT) bMenuItemID, 
                    MF_BYCOMMAND | MF_UNCHECKED); 
                fbAttributes ^= bMenuItemID; 
            } 
 
            // If any font attributes are currently selected, 
            // remove the check mark from the Regular menu item; 
            // if no attributes are selected, add a check mark 
            // to the Regular menu item. 
 
            if (fbAttributes & ATTRIBMASK) 
            { 
                CheckMenuItem(hmenu, IDM_REGULAR, 
                    MF_BYCOMMAND | MF_UNCHECKED); 
                fbAttributes &= (BYTE) ~IDM_REGULAR; 
            }
            else 
            { 
                CheckMenuItem(hmenu, IDM_REGULAR, 
                    MF_BYCOMMAND | MF_CHECKED); 
                fbAttributes = IDM_REGULAR; 
            } 
 
            return fbAttributes; 
    } 
} 
```



### <a name="example-of-using-custom-check-mark-bitmaps"></a>Beispiel für die Verwendung von benutzerdefinierten Bitmaps für das Häkchen

Im Beispiel in diesem Thema werden Menü Elementen benutzerdefinierte Bitmaps für das Häkchen in zwei Menüs zugewiesen. Die Menü Elemente im ersten Menü geben Zeichen Attribute an: Fett, kursiv und unterstrichen. Jedes Menü Element kann entweder aktiviert oder deaktiviert sein. In diesem Beispiel werden für diese Menü Elemente Kontrollkästchen-Bitmaps verwendet, die den ausgewählten und gelöschten Zuständen eines Kontrollkästchen-Steuer Elements ähneln.

Die Menü Elemente im zweiten Menü geben die Einstellungen für die Absatz Ausrichtung an: Links, zentriert und rechts. Es wird immer nur eines dieser Menü Elemente ausgewählt. In diesem Beispiel werden für diese Menü Elemente Kontrollkästchen-Bitmaps verwendet, die den ausgewählten und unklaren Zuständen eines Optionsfeld-Steuer Elements ähneln.

Die Fenster Prozedur verarbeitet die [**WM \_ Create**](/windows/desktop/winmsg/wm-create) -Nachricht, indem Sie die Anwendungs definierte OnCreate-Funktion aufrufen. `OnCreate` erstellt die vier Bitmaps für das Häkchen und weist diese dann den entsprechenden Menü Elementen mithilfe der [**setmenuitembitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) -Funktion zu.

Um jede Bitmap zu erstellen, ruft OnCreate die Anwendungs definierte Funktion "roatemenubitmaps" auf und gibt einen Zeiger auf eine bitmapspezifische Zeichnungs Funktion an. "Anatemenubitmaps" erstellt eine monochrome Bitmap der erforderlichen Größe, wählt Sie in einen Speichergeräte Kontext aus und löscht den Hintergrund. Anschließend wird die angegebene Zeichnungs Funktion aufgerufen, um in den Vordergrund zu füllen.

Die vier Anwendungs definierten Zeichnungsfunktionen sind "drawcheck", "drawuncheck", " **drawradiocheck**" und "drawradiouncheck". Sie zeichnen ein Rechteck mit einem X, einem leeren Rechteck, einer Ellipse, die eine kleinere Gefüllte Ellipse enthält, bzw. einer leeren Ellipse.

Die Fenster Prozedur verarbeitet die [**WM \_**](/windows/desktop/winmsg/wm-destroy) -Lösch Nachricht, indem die Prüfzeichen-Bitmaps gelöscht werden. Alle bitmaphandles werden mithilfe der [**getmenuiteminfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) -Funktion abgerufen und dann ein Handle an die Funktion übergeben.

Wenn der Benutzer ein Menü Element auswählt, wird eine [**WM- \_ Befehls**](wm-command.md) Meldung an das Besitzer Fenster gesendet. Für Menü Elemente im Menü **Zeichen** Ruft die Fenster Prozedur die Anwendungs definierte checkcharakteritem-Funktion auf. Für Elemente im **Absatz** Menü Ruft die Fenster Prozedur die Anwendungs definierte checkparagraphitem-Funktion auf.

Jedes Element im Menü " **Zeichen** " kann unabhängig voneinander ausgewählt und gelöscht werden. Daher schaltet checkcharakteritem einfach den Überprüfungs Zustand des angegebenen Menü Elements. Zuerst Ruft die Funktion die [**getmenuiteminfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) -Funktion auf, um den aktuellen Menü Element Zustand zu erhalten. Anschließend schaltet er das Flag für aktivierte **MFS \_** -Zustände um und legt den neuen Status durch Aufrufen der Funktion [**setmenuiteminfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) fest.

Im Gegensatz zu Zeichen Attributen kann jeweils nur eine Absatz Ausrichtung ausgewählt werden. Daher prüft checkparagphitem das angegebene Menü Element und entfernt das Häkchen aus allen anderen Elementen im Menü. Zu diesem Zweck wird die [**checkmenuradioitem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem) -Funktion aufgerufen.

Im folgenden finden Sie die relevanten Teile der Header Datei der Anwendung.


```
// Menu-item identifiers for the Character menu 
 
#define IDM_CHARACTER 10 
#define IDM_BOLD      11 
#define IDM_ITALIC    12 
#define IDM_UNDERLINE 13 
 
// Menu-item identifiers for the Paragraph menu 
 
#define IDM_PARAGRAPH 20 
#define IDM_LEFT      21 
#define IDM_CENTER    22 
#define IDM_RIGHT     23 
 
// Function-pointer type for drawing functions 
 
typedef VOID (WINAPI * DRAWFUNC)(HDC hdc, SIZE size); 
 
```



Im folgenden sind die relevanten Teile der Fenster Prozedur der Anwendung und zugehöriger Funktionen beschrieben.


```
LRESULT CALLBACK MainWindowProc( 
        HWND hwnd, 
        UINT uMsg, 
        WPARAM wParam, 
        LPARAM lParam 
        ) 
{ 
    switch (uMsg) 
    { 
        case WM_CREATE: 
            if (!OnCreate(hwnd)) 
                return -1; 
            break; 
 
        case WM_DESTROY: 
            OnDestroy(hwnd); 
            PostQuitMessage(0); 
            break; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDM_BOLD: 
                case IDM_ITALIC: 
                case IDM_UNDERLINE: 
                    CheckCharacterItem(hwnd, LOWORD(wParam)); 
                    break; 
 
                case IDM_LEFT: 
                case IDM_CENTER: 
                case IDM_RIGHT: 
                    CheckParagraphItem(hwnd, LOWORD(wParam)); 
                    break; 
 
                // Process other commands here. 
 
            } 
            break; 
 
        // Process other messages here. 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return 0; 
} 
 
VOID WINAPI CheckCharacterItem(HWND hwnd, UINT uID) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
 
    // Get a handle to the Character menu. 
 
    mii.fMask = MIIM_SUBMENU;  // information to get 
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Get the state of the specified menu item. 
 
    mii.fMask = MIIM_STATE;    // information to get 
    GetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
 
    // Toggle the checked state. 
 
    mii.fState ^= MFS_CHECKED; 
    SetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
} 
 
VOID WINAPI CheckParagraphItem(HWND hwnd, UINT uID) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
 
    // Get a handle to the Paragraph menu. 
 
    mii.fMask = MIIM_SUBMENU;  // information to get 
    GetMenuItemInfo(hmenuBar, IDM_PARAGRAPH, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Check the specified item and uncheck all the others. 
 
    CheckMenuRadioItem( 
            hmenuPopup,         // handle to menu 
            IDM_LEFT,           // first item in range 
            IDM_RIGHT,          // last item in range 
            uID,                // item to check 
            MF_BYCOMMAND        // IDs, not positions 
            ); 
} 
 
BOOL WINAPI OnCreate(HWND hwnd) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
    UINT uID; 
    HBITMAP hbmChecked; 
    HBITMAP hbmUnchecked; 
 
    // Get a handle to the Character menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Create the checked and unchecked bitmaps. 
 
    hbmChecked = CreateMenuBitmap(DrawCheck); 
    hbmUnchecked = CreateMenuBitmap(DrawUncheck); 
 
    // Set the check-mark bitmaps for each menu item. 
 
    for (uID = IDM_BOLD; uID <= IDM_UNDERLINE; uID++) 
    { 
        SetMenuItemBitmaps(hmenuPopup, uID, MF_BYCOMMAND, 
                hbmUnchecked, hbmChecked); 
    } 
 
    // Get a handle to the Paragraph pop-up menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_PARAGRAPH, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Create the checked and unchecked bitmaps. 
 
    hbmChecked = CreateMenuBitmap(DrawRadioCheck); 
    hbmUnchecked = CreateMenuBitmap(DrawRadioUncheck); 
 
    // Set the check-mark bitmaps for each menu item. 
 
    for (uID = IDM_LEFT; uID <= IDM_RIGHT; uID++) 
    { 
        SetMenuItemBitmaps(hmenuPopup, uID, MF_BYCOMMAND, 
                hbmUnchecked, hbmChecked); 
    } 
 
    // Initially check the IDM_LEFT paragraph item. 
 
    CheckMenuRadioItem(hmenuPopup, IDM_LEFT, IDM_RIGHT, 
            IDM_LEFT, MF_BYCOMMAND); 
    return TRUE; 
} 
 
HBITMAP WINAPI CreateMenuBitmap(DRAWFUNC lpfnDraw) 
{ 
    // Create a DC compatible with the desktop window's DC. 
 
    HWND hwndDesktop = GetDesktopWindow(); 
    HDC hdcDesktop = GetDC(hwndDesktop); 
    HDC hdcMem = CreateCompatibleDC(hdcDesktop); 
 
    // Determine the required bitmap size. 
 
    SIZE size = { GetSystemMetrics(SM_CXMENUCHECK), 
                  GetSystemMetrics(SM_CYMENUCHECK) }; 
 
    // Create a monochrome bitmap and select it. 
 
    HBITMAP hbm = CreateBitmap(size.cx, size.cy, 1, 1, NULL); 
    HBITMAP hbmOld = SelectObject(hdcMem, hbm); 
 
    // Erase the background and call the drawing function. 
 
    PatBlt(hdcMem, 0, 0, size.cx, size.cy, WHITENESS); 
    (*lpfnDraw)(hdcMem, size); 
 
    // Clean up. 
 
    SelectObject(hdcMem, hbmOld); 
    DeleteDC(hdcMem); 
    ReleaseDC(hwndDesktop, hdcDesktop); 
    return hbm; 
} 
 
VOID WINAPI DrawCheck(HDC hdc, SIZE size) 
{ 
    HBRUSH hbrOld; 
    hbrOld = SelectObject(hdc, GetStockObject(NULL_BRUSH)); 
    Rectangle(hdc, 0, 0, size.cx, size.cy); 
    MoveToEx(hdc, 0, 0, NULL); 
    LineTo(hdc, size.cx, size.cy); 
    MoveToEx(hdc, 0, size.cy - 1, NULL); 
    LineTo(hdc, size.cx - 1, 0); 
    SelectObject(hdc, hbrOld); 
} 
 
VOID WINAPI DrawUncheck(HDC hdc, SIZE size) 
{ 
    HBRUSH hbrOld; 
    hbrOld = SelectObject(hdc, GetStockObject(NULL_BRUSH)); 
    Rectangle(hdc, 0, 0, size.cx, size.cy); 
    SelectObject(hdc, hbrOld); 
} 
 
VOID WINAPI DrawRadioCheck(HDC hdc, SIZE size) 
{ 
    HBRUSH hbrOld; 
    hbrOld = SelectObject(hdc, GetStockObject(NULL_BRUSH)); 
    Ellipse(hdc, 0, 0, size.cx, size.cy); 
    SelectObject(hdc, GetStockObject(BLACK_BRUSH)); 
    Ellipse(hdc, 2, 2, size.cx - 2, size.cy - 2); 
    SelectObject(hdc, hbrOld); 
} 
 
VOID WINAPI DrawRadioUncheck(HDC hdc, SIZE size) 
{ 
    HBRUSH hbrOld; 
    hbrOld = SelectObject(hdc, GetStockObject(NULL_BRUSH)); 
    Ellipse(hdc, 0, 0, size.cx, size.cy); 
    SelectObject(hdc, hbrOld); 
} 
 
VOID WINAPI OnDestroy(HWND hwnd) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
 
    // Get a handle to the Character menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Get the check-mark bitmaps and delete them. 
 
    mii.fMask = MIIM_CHECKMARKS; 
    GetMenuItemInfo(hmenuPopup, IDM_BOLD, FALSE, &mii); 
    DeleteObject(mii.hbmpChecked); 
    DeleteObject(mii.hbmpUnchecked); 
 
    // Get a handle to the Paragraph menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_PARAGRAPH, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Get the check-mark bitmaps and delete them. 
 
    mii.fMask = MIIM_CHECKMARKS; 
    GetMenuItemInfo(hmenuPopup, IDM_LEFT, FALSE, &mii); 
    DeleteObject(mii.hbmpChecked); 
    DeleteObject(mii.hbmpUnchecked); 
} 
```



 

 