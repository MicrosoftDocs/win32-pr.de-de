---
title: Verwenden von Menüs
description: Dieser Abschnitt enthält Codebeispiele für Aufgaben im Zusammenhang mit Menüs.
ms.assetid: b1391e37-a146-46ec-a329-aa57cfcfd351
keywords:
- Ressourcen,Menüs
- Menüs,erstellen
- Menüvorlagenressourcen
- resources,menu-template
- Erweitertes Menüvorlagenformat
- Vorlagenformat im alten Menü
- Laden von Menüvorlagenressourcen
- menus,class
- Menüs, Verknüpfung
- Erstellen von Menüs
- Klassenmenüs
- Kontextmenüs
- Menüelementbitmaps
- Menüs,Besitzer gezeichnet
- Gezeichnete Menüs des Besitzers
- Benutzerdefinierte Häkchenbitmaps
- Menüs, Kontrollkästchen
- Menüs, Schriftarten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f3a71a580a323fa2058613f8c9a14d9c2782bd3ba139e5d182750e5047fe74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971929"
---
# <a name="using-menus"></a>Verwenden von Menüs

In diesem Abschnitt werden die folgenden Aufgaben beschrieben:

-   [Verwenden einer Menu-Template Ressource](#using-a-menu-template-resource)
    -   [Erweitertes Menu-Template Format](#extended-menu-template-format)
    -   [Altes Menu-Template Format](#old-menu-template-format)
    -   [Laden einer Menu-Template Ressource](#loading-a-menu-template-resource)
    -   [Erstellen eines Klassenmenüs](#creating-a-class-menu)
-   [Erstellen eines Kontextmenüs](#creating-a-shortcut-menu)
    -   [Verarbeiten der WM \_ CONTEXTMENU-Nachricht](/windows)
    -   [Erstellen eines Kontextmenüs Font-Attributes](#creating-a-shortcut-font-attributes-menu)
    -   [Anzeigen eines Kontextmenüs](#displaying-a-shortcut-menu)
-   [Verwenden Menu-Item Bitmaps](#using-menu-item-bitmaps)
    -   [Festlegen des Bitmaptypflags](#setting-the-bitmap-type-flag)
    -   [Erstellen der Bitmap](#creating-the-bitmap)
    -   [Hinzufügen von Linien und Diagrammen zu einem Menü](#adding-lines-and-graphs-to-a-menu)
    -   [Beispiel für Menu-Item Bitmaps](#example-of-menu-item-bitmaps)
-   [Erstellen Owner-Drawn Menüelemente](#creating-owner-drawn-menu-items)
    -   [Festlegen des Owner-Drawn Flags](#setting-the-owner-drawn-flag)
    -   [Vom Besitzer gezeichnete Menüs und die WM \_ MEASUREITEM-Meldung](/windows)
    -   [Vom Besitzer gezeichnete Menüs und die WM \_ DRAWITEM-Meldung](/windows)
    -   [Besitzer gezeichnete Menüs und die WM \_ MENUCHAR-Meldung](/windows)
    -   [Festlegen von Schriftarten für Menu-Item Textzeichenfolgen](#setting-fonts-for-menu-item-text-strings)
    -   [Beispiel für Owner-Drawn Menüelemente](#example-of-owner-drawn-menu-items)
-   [Verwenden benutzerdefinierter Häkchenbitmaps](#using-custom-check-mark-bitmaps)
    -   [Erstellen benutzerdefinierter Häkchenbitmaps](#creating-custom-check-mark-bitmaps)
    -   [Zuordnen von Bitmaps zu einem Menüelement](#associating-bitmaps-with-a-menu-item)
    -   [Festlegen des Check-Mark-Attributs](#setting-the-check-mark-attribute)
    -   [Simulieren von Kontrollkästchen in einem Menü](#simulating-check-boxes-in-a-menu)
    -   [Beispiel für die Verwendung benutzerdefinierter Häkchenbitmaps](#example-of-using-custom-check-mark-bitmaps)

## <a name="using-a-menu-template-resource"></a>Verwenden einer Menu-Template Ressource

In der Regel fügen Sie ein Menü in eine Anwendung ein, indem Sie eine Menüvorlagenressource erstellen und das Menü dann zur Laufzeit laden. In diesem Abschnitt wird das Format einer Menüvorlage beschrieben, und es wird erläutert, wie Sie eine Menüvorlagenressource laden und in Ihrer Anwendung verwenden. Informationen zum Erstellen einer Menüvorlagenressource finden Sie in der Dokumentation zu Ihren Entwicklungstools.

-   [Erweitertes Menu-Template Format](#extended-menu-template-format)
-   [Altes Menu-Template Format](#old-menu-template-format)
-   [Laden einer Menu-Template Ressource](#loading-a-menu-template-resource)
-   [Erstellen eines Klassenmenüs](#creating-a-class-menu)

### <a name="extended-menu-template-format"></a>Erweitertes Menu-Template Format

Das erweiterte Menüvorlagenformat unterstützt zusätzliche Menüfunktionen. Wie standarde Menüvorlagenressourcen verfügen auch erweiterte Menüvorlagenressourcen über den **Ressourcentyp RT \_ MENU.** Das System unterscheidet die beiden Ressourcenformate durch die Versionsnummer, die das erste Mitglied des Ressourcenheaders ist.

Eine erweiterte Menüvorlage besteht aus einer [**MENUEX \_ TEMPLATE \_ HEADER-Struktur,**](menuex-template-header.md) gefolgt von einer anderen [**MENUEX \_ TEMPLATE \_ ITEM-Elementdefinitionsstruktur.**](menuex-template-item.md)

### <a name="old-menu-template-format"></a>Altes Menu-Template Format

Eine alte Menüvorlage (Microsoft Windows NT 3.51 und früher) definiert ein Menü, unterstützt jedoch nicht die neue Menüfunktionalität. Eine alte Menüvorlagenressource hat den **Ressourcentyp RT \_ MENU.**

Eine alte Menüvorlage besteht aus einer [**MENUITEMTEMPLATEHEADER-Struktur**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader) gefolgt von einer oder mehreren [**MENUITEMTEMPLATE-Strukturen.**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate)

### <a name="loading-a-menu-template-resource"></a>Laden einer Menu-Template Ressource

Verwenden Sie zum Laden einer Menüvorlagenressource die [**LoadMenu-Funktion,**](/windows/desktop/api/Winuser/nf-winuser-loadmenua) und geben Sie ein Handle für das Modul an, das die Ressource und den Bezeichner der Menüvorlage enthält. Die **LoadMenu-Funktion** gibt ein Menühand handle zurück, mit dem Sie das Menü einem Fenster zuweisen können. Dieses Fenster wird zum Besitzerfenster des Menüs und empfängt alle vom Menü generierten Nachrichten.

Verwenden Sie die [**LoadMenuIndirect-Funktion,**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) um ein Menü aus einer Menüvorlage zu erstellen, die sich bereits im Arbeitsspeicher befindet. Dies ist nützlich, wenn Ihre Anwendung Menüvorlagen dynamisch generiert.

Verwenden Sie zum Zuweisen eines Menüs zu einem Fenster die [**Funktion SetMenu,**](/windows/desktop/api/Winuser/nf-winuser-setmenu) oder geben Sie beim Erstellen eines Fensters das Handle des Menüs im *hMenu-Parameter* der [**CreateWindowEx-Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) an. Sie können einem Fenster auch ein Menü zuweisen, indem Sie beim Registrieren einer Fensterklasse eine Menüvorlage angeben. Die Vorlage identifiziert das angegebene Menü als Klassenmenü für diese Fensterklasse.

Damit das System einem Fenster automatisch ein bestimmtes Menü zu weist, geben Sie die Vorlage des Menüs an, wenn Sie die -Klasse des Fensters registrieren. Die Vorlage identifiziert das angegebene Menü als Klassenmenü für diese Fensterklasse. Wenn Sie dann ein Fenster der angegebenen Klasse erstellen, weist das System dem Fenster automatisch das angegebene Menü zu.

Sie können einem Fenster, das ein untergeordnetes Fenster ist, kein Menü zuweisen.

Um ein Klassenmenü zu erstellen, schließen Sie den Bezeichner der Menüvorlagenressource als **lpszMenuName-Member** einer [**WNDCLASS-Struktur**](/windows/win32/api/winuser/ns-winuser-wndclassa) ein, und übergeben Sie dann einen Zeiger auf die -Struktur an die [**RegisterClass-Funktion.**](/windows/desktop/api/winuser/nf-winuser-registerclassa)

### <a name="creating-a-class-menu"></a>Erstellen eines Klassenmenüs

Das folgende Beispiel zeigt, wie Sie ein Klassenmenü für eine Anwendung erstellen, ein Fenster erstellen, das das Klassenmenü verwendet, und Menübefehle in der Fensterprozedur verarbeiten.

Im Folgenden finden Sie den relevanten Teil der Headerdatei der Anwendung:


```
// Menu-template resource identifier 
 
#define IDM_MYMENURESOURCE   3
```



Im Folgenden finden Sie die relevanten Teile der Anwendung selbst:


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

Um ein Kontextmenü in einer Anwendung zu verwenden, übergeben Sie dessen Handle an die [**TrackPopupMenuEx-Funktion.**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) Eine Anwendung ruft in der Regel **TrackPopupMenuEx** in einer Fensterprozedur als Reaktion auf eine vom Benutzer generierte Nachricht auf, z. B. [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) oder [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown).

Zusätzlich zum Popupmenühandl erfordert [**TrackPopupMenuEx,**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) dass Sie ein Handle für das Besitzerfenster, die Position des Kontextmenüs (in Bildschirmkoordinaten) und die Maustaste angeben, mit der der Benutzer ein Element auswählen kann.

Die ältere [**TrackPopupMenu-Funktion**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) wird weiterhin unterstützt, aber neue Anwendungen sollten die [**TrackPopupMenuEx-Funktion**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) verwenden. Die **TrackPopupMenuEx-Funktion** erfordert die gleichen Parameter wie **TrackPopupMenu.** Sie können aber auch einen Teil des Bildschirms angeben, den das Menü nicht verdeckt. Eine Anwendung ruft diese Funktionen in der Regel in einer Fensterprozedur auf, wenn die [**WM \_ CONTEXTMENU-Nachricht verarbeitet**](wm-contextmenu.md) wird.

Sie können die Position eines Kontextmenüs angeben, indem Sie x- und y-Koordinaten zusammen mit dem **TPM \_ CENTERALIGN-,** **TPM \_ LEFTALIGN-** oder **TPM \_ RIGHTALIGN-Flag** angeben. Das -Flag gibt die Position des Kontextmenüs relativ zu den x- und y-Koordinaten an.

Sie sollten es dem Benutzer ermöglichen, ein Element aus einem Kontextmenü mit der gleichen Maustaste zu wählen, die zum Anzeigen des Menüs verwendet wird. Geben Sie hierzu entweder **das TPM \_ LEFTBUTTON-** oder **TPM \_ RIGHTBUTTON-Flag** an, um anzugeben, welche Maustaste der Benutzer zum Auswählen eines Menüelements verwenden kann.

-   [Verarbeiten der WM \_ CONTEXTMENU-Nachricht](/windows)
-   [Erstellen eines Kontextmenüs Font-Attributes](#creating-a-shortcut-font-attributes-menu)
-   [Anzeigen eines Kontextmenüs](#displaying-a-shortcut-menu)

### <a name="processing-the-wm_contextmenu-message"></a>Verarbeiten der WM \_ CONTEXTMENU-Nachricht

Die [**WM \_ CONTEXTMENU-Meldung**](wm-contextmenu.md) wird generiert, wenn die Fensterprozedur einer Anwendung die [**WM \_ RBUTTONUP-**](/windows/desktop/inputdev/wm-rbuttonup) oder [**WM \_ NCRBUTTONUP-Nachricht**](/windows/desktop/inputdev/wm-ncrbuttonup) an die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) übergibt. Die Anwendung kann diese Meldung verarbeiten, um ein Kontextmenü anzuzeigen, das für einen bestimmten Teil des Bildschirms geeignet ist. Wenn die Anwendung kein Kontextmenü zeigt, sollte sie die Meldung zur Standardbehandlung **an DefWindowProc** übergeben.

Im Folgenden finden Sie ein Beispiel für die Verarbeitung von [**WM \_ CONTEXTMENU-Nachrichten,**](wm-contextmenu.md) wie sie in der Fensterprozedur einer Anwendung angezeigt werden kann. Die niedrigen und hohen Wörter des *lParam-Parameters* geben die Bildschirmkoordinaten der Maus an, wenn die rechte Maustaste losgelassen wird (beachten Sie, dass diese Koordinaten negative Werte auf Systemen mit mehreren Monitoren enthalten können). Die anwendungsdefinierte **OnContextMenu-Funktion** gibt **TRUE** zurück, wenn ein Kontextmenü angezeigt wird, oder **FALSE,** wenn dies nicht der Fall ist.


```
case WM_CONTEXTMENU: 
    if (!OnContextMenu(hwnd, GET_X_LPARAM(lParam),
              GET_Y_LPARAM(lParam))) 
        return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    break; 
```



Die folgende anwendungsdefinierte OnContextMenu-Funktion zeigt ein Kontextmenü an, wenn sich die angegebene Mausposition innerhalb des Clientbereichs des Fensters befindet. Eine komplexere Funktion kann je nachdem, welcher Teil des Clientbereichs angegeben ist, eines von mehreren verschiedenen Menüs anzeigen. Um das Kontextmenü tatsächlich anzuzeigen, ruft dieses Beispiel eine anwendungsdefinierte Funktion namens DisplayContextMenu auf. Eine Beschreibung dieser Funktion finden Sie unter [Anzeigen eines Kontextmenüs.](#displaying-a-shortcut-menu)


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



### <a name="creating-a-shortcut-font-attributes-menu"></a>Erstellen eines Kontextmenüs Font-Attributes

Das Beispiel in diesem Abschnitt enthält Teile von Code aus einer Anwendung, die ein Kontextmenü erstellt und anzeigt, mit dem der Benutzer Schriftarten und Schriftartattribute festlegen kann. Die Anwendung zeigt das Menü immer dann im Clientbereich des Hauptfensters an, wenn der Benutzer mit der linken Maustaste klickt.

Dies ist die Menüvorlage für das Kontextmenü, das in der Ressourcendefinitionsdatei der Anwendung bereitgestellt wird.


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



Das folgende Beispiel enthält die Fensterprozedur und unterstützende Funktionen, die zum Erstellen und Anzeigen des Kontextmenüs verwendet werden.


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

Die Anwendung enthält eine Menüressource, die durch die Zeichenfolge "ShortcutExample" identifiziert wird. Die Menüleiste enthält einfach einen Menünamen. Die Anwendung verwendet die [**TrackPopupMenu-Funktion,**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) um das diesem Menüelement zugeordnete Menü anzuzeigen. (Die Menüleiste selbst wird nicht angezeigt, da **TrackPopupMenu** ein Handle für ein Menü, Untermenü oder Kontextmenü erfordert.)


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



## <a name="using-menu-item-bitmaps"></a>Verwenden Menu-Item Bitmaps

Das System kann eine Bitmap anstelle einer Textzeichenfolge verwenden, um ein Menüelement anzuzeigen. Um eine Bitmap zu verwenden, müssen Sie das **MIIM \_ BITMAP-Flag** für das Menüelement festlegen und ein Handle für die Bitmap angeben, das das System für das Menüelement im **hbmpItem-Element** der [**MENUITEMINFO-Struktur anzeigen**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) soll. In diesem Abschnitt wird beschrieben, wie Bitmaps für Menüelemente verwendet werden.

-   [Festlegen des Bitmaptypflags](#setting-the-bitmap-type-flag)
-   [Erstellen der Bitmap](#creating-the-bitmap)
-   [Hinzufügen von Linien und Diagrammen zu einem Menü](#adding-lines-and-graphs-to-a-menu)
-   [Beispiel für Menu-Item Bitmaps](#example-of-menu-item-bitmaps)

### <a name="setting-the-bitmap-type-flag"></a>Festlegen des Bitmaptypflags

Das **MIIM \_ BITMAP-** oder **MF \_ BITMAP-Flag** weist das System an, eine Bitmap anstelle einer Textzeichenfolge zum Anzeigen eines Menüelements zu verwenden. Das **\_ MIIM-BITMAP-** oder **MF-BITMAP-Flag \_** eines Menüelements muss zur Laufzeit festgelegt werden. Sie können es nicht in der Ressourcendefinitionsdatei festlegen.

Für neue Anwendungen können Sie die [**Funktion SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) oder [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) verwenden, um das **MIIM \_ BITMAP-Typflag** fest zu setzen. Verwenden Sie **SetMenuItemInfo,** um ein Menüelement von einem Textelement in ein Bitmapelement zu ändern. Um einem Menü ein neues Bitmapelement hinzuzufügen, verwenden Sie die **InsertMenuItem-Funktion.**

Anwendungen, die für frühere Versionen des Systems geschrieben wurden, können weiterhin die [**Funktionen ModifyMenu,**](/windows/desktop/api/Winuser/nf-winuser-modifymenua) [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)oder [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) verwenden, um das **MF \_ BITMAP-Flag** zu setzen. Um ein Menüelement von einem Textzeichenfolgenelement in ein Bitmapelement zu ändern, verwenden **Sie ModifyMenu**. Um einem Menü ein neues Bitmapelement hinzuzufügen, verwenden Sie das **MF \_ BITMAP-Flag** mit der **InsertMenu-** oder **AppendMenu-Funktion.**

### <a name="creating-the-bitmap"></a>Erstellen der Bitmap

Wenn Sie das **MIIM \_ BITMAP-** oder **MF BITMAP-Typflag \_** für ein Menüelement festlegen, müssen Sie auch ein Handle für die Bitmap angeben, das das System für das Menüelement anzeigen soll. Sie können die Bitmap als Bitmapressource bereitstellen oder die Bitmap zur Laufzeit erstellen. Wenn Sie eine Bitmapressource verwenden, können Sie die [**LoadBitmap-Funktion**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) verwenden, um die Bitmap zu laden und ihr Handle zu erhalten.

Um die Bitmap zur Laufzeit zu erstellen, verwenden Sie Windows Graphics Device Interface (GDI)-Funktionen. GDI bietet mehrere Möglichkeiten zum Erstellen einer Bitmap zur Laufzeit, entwickler verwenden jedoch in der Regel die folgende Methode:

1.  Verwenden Sie [**die Funktion CreateCompatibleDC,**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) um einen Gerätekontext zu erstellen, der mit dem vom Hauptfenster der Anwendung verwendeten Gerätekontext kompatibel ist.
2.  Verwenden Sie [**die CreateCompatibleBitmap-Funktion,**](/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap) um eine Bitmap zu erstellen, die mit dem Hauptfenster der Anwendung kompatibel ist, oder verwenden Sie die [**CreateBitmap-Funktion,**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) um eine monofarbige Bitmap zu erstellen.
3.  Verwenden Sie die [**SelectObject-Funktion,**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) um die Bitmap im kompatiblen Gerätekontext auszuwählen.
4.  Verwenden Sie GDI-Zeichnungsfunktionen wie [**Ellipse**](/windows/desktop/api/wingdi/nf-wingdi-ellipse) und [**LineTo,**](/windows/desktop/api/wingdi/nf-wingdi-lineto)um ein Bild in die Bitmap zu zeichnen.

Weitere Informationen finden Sie unter [Bitmaps](/windows/desktop/gdi/bitmaps).

### <a name="adding-lines-and-graphs-to-a-menu"></a>Hinzufügen von Linien und Diagrammen zu einem Menü

Das folgende Codebeispiel zeigt, wie Sie ein Menü erstellen, das Menüelementbitmaps enthält. Es werden zwei Menüs erstellt. Die erste ist ein Diagrammmenü, das drei Menüelementbitmaps enthält: ein Kreisdiagramm, ein Liniendiagramm und ein Balkendiagramm. Das Beispiel zeigt, wie sie diese Bitmaps aus der Ressourcendatei der Anwendung laden und dann die [**Funktionen CreatePopupMenu**](/windows/desktop/api/Winuser/nf-winuser-createpopupmenu) und [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) verwenden, um die Menü- und Menüelemente zu erstellen.

Das zweite Menü ist ein Linienmenü. Sie enthält Bitmaps, die die vom vordefinierten Stift im System bereitgestellten Linienstile anzeigen. Die Bitmaps im Linienstil werden zur Laufzeit mithilfe von GDI-Funktionen erstellt.

Hier sind die Definitionen der Bitmapressourcen in der Ressourcendefinitionsdatei der Anwendung.


```
PIE BITMAP pie.bmp 
LINE BITMAP line.bmp 
BAR BITMAP bar.bmp 
 
```



Im Folgenden finden Sie die relevanten Teile der Headerdatei der Anwendung.


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



Das folgende Beispiel zeigt, wie Menüs und Menüelementbitmaps in einer Anwendung erstellt werden.


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

Im Beispiel in diesem Thema werden zwei Menüs erstellt, die jeweils mehrere Bitmapmenüelemente enthalten. Für jedes Menü fügt die Anwendung der Menüleiste des Hauptfensters einen entsprechenden Menünamen hinzu.

Das erste Menü enthält Menüelemente, die jeden der drei Diagrammtypen anzeigen: Kreis, Linie und Balken. Die Bitmaps für diese Menüelemente werden als Ressourcen definiert und mithilfe der [**LoadBitmap-Funktion geladen.**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) Diesem Menü ist ein Menüname "Diagramm" auf der Menüleiste zugeordnet.

Das zweite Menü enthält Menüelemente mit den fünf Linienstilen, die mit der [**CreatePen-Funktion**](/windows/desktop/api/wingdi/nf-wingdi-createpen) verwendet werden: **PS \_ SOLID**, **PS \_ DASH**, **PS \_ DOT**, **PS \_ DASHDOT** und **PS \_ DASHDOT**. Die Anwendung erstellt die Bitmaps für diese Menüelemente zur Laufzeit mithilfe von GDI-Zeichnungsfunktionen. Diesem Menü ist  ein Zeilenmenüname auf der Menüleiste zugeordnet.

In der Fensterprozedur der Anwendung sind zwei statische Arrays von Bitmaphandles definiert. Ein Array enthält die Handles der drei Bitmaps, die für das Menü **Diagramm verwendet** werden. Die andere enthält die Handles der fünf Bitmaps, die für das Menü **Zeilen verwendet** werden. Beim Verarbeiten der [**WM \_ CREATE-Nachricht**](/windows/desktop/winmsg/wm-create) lädt die Fensterprozedur die Diagrammbitmaps, erstellt die Linienbitmaps und fügt dann die entsprechenden Menüelemente hinzu. Beim Verarbeiten der [**WM \_ DESTROY-Nachricht**](/windows/desktop/winmsg/wm-destroy) löscht die Fensterprozedur alle Bitmaps.

Im Folgenden finden Sie die relevanten Teile der Headerdatei der Anwendung.


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



Im Folgenden finden Sie die relevanten Teile der Fensterprozedur. Die Fensterprozedur führt den Großteil der Initialisierung durch, indem die anwendungsdefinierten Funktionen LoadChartBitmaps, CreateLineBitmaps und AddBitmapMenu, die weiter unten in diesem Thema beschrieben werden, aufrufen.


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



Die anwendungsdefinierte LoadChartBitmaps-Funktion lädt die Bitmapressourcen für das Diagrammmenü, indem die [**LoadBitmap-Funktion**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) wie folgt aufruft.


```
VOID WINAPI LoadChartBitmaps(HBITMAP *paHbm) 
{ 
    paHbm[0] = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_PIE)); 
    paHbm[1] = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_LINE)); 
    paHbm[2] = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_BAR)); 
} 
```



Die anwendungsdefinierte CreateLineBitmaps-Funktion erstellt die Bitmaps für das Menü Linien mithilfe von GDI-Zeichnungsfunktionen. Die Funktion erstellt einen Speichergerätekontext (DC) mit den gleichen Eigenschaften wie der Domänencontroller des Desktopfensters. Für jeden Linienstil erstellt die Funktion eine Bitmap, wählt sie im Arbeitsspeicher-DC aus und zeichnet sie.


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



Die anwendungsdefinierte AddBitmapMenu-Funktion erstellt ein Menü und fügt ihr die angegebene Anzahl von Bitmapmenüelementen hinzu. Anschließend wird der Menüleiste des angegebenen Fensters ein entsprechender Menüname hinzufügt.


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



## <a name="creating-owner-drawn-menu-items"></a>Erstellen Owner-Drawn Menüelemente

Wenn Sie die vollständige Kontrolle über die Darstellung eines Menüelements benötigen, können Sie ein vom Besitzer gezeichnetes Menüelement in Ihrer Anwendung verwenden. In diesem Abschnitt werden die Schritte zum Erstellen und Verwenden eines vom Besitzer gezeichneten Menüelements beschrieben.

-   [Festlegen des Owner-Drawn Flags](#setting-the-owner-drawn-flag)
-   [Vom Besitzer gezeichnete Menüs und die WM \_ MEASUREITEM-Meldung](/windows)
-   [Besitzer gezeichnete Menüs und die WM \_ DRAWITEM-Meldung](/windows)
-   [Vom Besitzer gezeichnete Menüs und die WM \_ MENUCHAR-Meldung](/windows)
-   [Festlegen von Schriftarten für Menu-Item Textzeichenfolgen](#setting-fonts-for-menu-item-text-strings)
-   [Beispiel für Owner-Drawn Menüelemente](#example-of-owner-drawn-menu-items)

### <a name="setting-the-owner-drawn-flag"></a>Festlegen des Owner-Drawn Flags

Sie können kein vom Besitzer gezeichnetes Menüelement in der Ressourcendefinitionsdatei Ihrer Anwendung definieren. Stattdessen müssen Sie ein neues Menüelement erstellen oder ein vorhandenes ändern, indem Sie das **MFT \_ OWNERDRAW-Menüflag** verwenden.

Sie können die [**Funktion InsertMenuItem oder**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) verwenden, um ein vom Besitzer gezeichnetes Menüelement anzugeben. Verwenden **Sie InsertMenuItem,** um ein neues Menüelement an der angegebenen Position in eine Menüleiste oder ein Menü einfügungen. Verwenden **Sie SetMenuItemInfo,** um den Inhalt eines Menüs zu ändern.

Wenn Sie diese beiden Funktionen aufrufen, müssen Sie einen Zeiger auf eine [**MENUITEMINFO-Struktur**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) angeben, die die Eigenschaften des neuen Menüelements oder die Eigenschaften angibt, die Sie für ein vorhandenes Menüelement ändern möchten. Um ein Element zu einem vom Besitzer gezeichneten Element zu machen, geben Sie den **MIIM \_ FTYPE-Wert** für das **fMask-Element** und den **MFT \_ OWNERDRAW-Wert** für das **fType-Element** an.

Durch Festlegen der entsprechenden Member der [**MENUITEMINFO-Struktur**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) können Sie jedem Menüelement einen anwendungsdefinierten Wert zuordnen, der als Elementdaten bezeichnet wird. Geben Sie dazu den **MIIM \_ DATA-Wert** für das **fMask-Element** und den anwendungsdefinierten Wert für das **dwItemData-Element** an.

Sie können Elementdaten mit jeder Art von Menüelement verwenden, aber es ist besonders nützlich für vom Besitzer gezeichnete Elemente. Angenommen, eine -Struktur enthält Informationen, die zum Zeichnen eines Menüelements verwendet werden. Eine Anwendung kann die Elementdaten für ein Menüelement verwenden, um einen Zeiger auf die Struktur zu speichern. Die Elementdaten werden mit den Meldungen [**WM \_ MEASUREITEM**](../controls/wm-measureitem.md) und WM DRAWITEM an das [**\_ Besitzerfenster des Menüs**](../controls/wm-drawitem.md) gesendet. Um die Elementdaten für ein Menü jederzeit abzurufen, verwenden Sie die [**GetMenuItemInfo-Funktion.**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa)

Anwendungen, die für frühere Versionen des Systems geschrieben wurden, können [**weiterhin AppendMenu,**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)oder [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua) aufrufen, um das **MF \_ OWNERDRAW-Flag** einem vom Besitzer gezeichneten Menüelement zu zuweisen.

Wenn Sie eine dieser drei Funktionen aufrufen, können Sie einen Wert als *lpNewItem-Parameter* übergeben. Dieser Wert kann alle Informationen darstellen, die für Ihre Anwendung aussagekräftig sind und der Anwendung zur Verfügung stehen, wenn das Element angezeigt werden soll. Beispielsweise könnte der Wert einen Zeiger auf eine -Struktur enthalten. Die -Struktur wiederum kann eine Textzeichenfolge und ein Handle für die logische Schriftart enthalten, die Ihre Anwendung zum Zeichnen der Zeichenfolge verwendet.

### <a name="owner-drawn-menus-and-the-wm_measureitem-message"></a>Owner-Drawn Menüs und die WM \_ MEASUREITEM-Meldung

Bevor das System zum ersten Mal ein vom Besitzer gezeichnetes Menüelement anzeigt, sendet es die [**WM \_ MEASUREITEM-Nachricht**](../controls/wm-measureitem.md) an die Fensterprozedur des Fensters, das das Menü des Elements besitzt. Diese Meldung enthält einen Zeiger auf eine [**MEASUREITEMSTRUCT-Struktur,**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) die das Element identifiziert und die Elementdaten enthält, die ihm möglicherweise von einer Anwendung zugewiesen wurden. Die Fensterprozedur muss die **Member itemWidth** und **itemHeight** der -Struktur ausfüllen, bevor sie von der Verarbeitung der Nachricht zurückkehrt. Das System verwendet die Informationen in diesen Membern beim Erstellen des umgebundenen Rechtecks, in dem eine Anwendung das Menüelement zeichnet. Außerdem werden die Informationen verwendet, um zu erkennen, wann der Benutzer das Element auswählt.

### <a name="owner-drawn-menus-and-the-wm_drawitem-message"></a>Owner-Drawn Menüs und die WM \_ DRAWITEM-Meldung

Wenn das Element gezeichnet werden muss (z. B. wenn es zum ersten Mal angezeigt wird oder wenn der Benutzer es auswählt), sendet das System die [**WM \_ DRAWITEM-Nachricht**](../controls/wm-drawitem.md) an die Fensterprozedur des Besitzerfensters des Menüs. Diese Meldung enthält einen Zeiger auf eine [**DRAWITEMSTRUCT-Struktur,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) die Informationen zum Element enthält, einschließlich der Elementdaten, die ihm möglicherweise von einer Anwendung zugewiesen wurden. Darüber hinaus enthält **DRAWITEMSTRUCT** Flags, die den Zustand des Elements angeben (z. B. ob es grau oder ausgewählt ist), sowie ein umgebundenes Rechteck und einen Gerätekontext, den die Anwendung zum Zeichnen des Elements verwendet.

Eine Anwendung muss beim Verarbeiten der [**WM \_ DRAWITEM-Nachricht Folgendes**](../controls/wm-drawitem.md) tun:

-   Bestimmen Sie den erforderlichen Zeichnungstyp. Überprüfen Sie dazu das **itemAction-Element** der [**DRAWITEMSTRUCT-Struktur.**](/windows/win32/api/winuser/ns-winuser-drawitemstruct)
-   Zeichnen Sie das Menüelement entsprechend, indem Sie das umgebundene Rechteck und den Gerätekontext verwenden, der aus der [**DRAWITEMSTRUCT-Struktur ermittelt**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) wurde. Die Anwendung darf nur innerhalb des umgebundenen Rechtecks zeichnen. Aus Leistungsgründen beschneiden das System keine Teile des Bilds, die außerhalb des Rechtecks gezeichnet werden.
-   Stellen Sie alle GDI-Objekte wieder wieder dar, die für den Gerätekontext des Menüelements ausgewählt wurden.

Wenn der Benutzer das Menüelement auswählt, legt das System das **itemAction-Element** der [**DRAWITEMSTRUCT-Struktur**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) auf den **KONSTRUKT \_ SELECT-Wert** und den **ODS \_ SELECTED-Wert** im **itemState-Element** fest. Dies ist der Hinweis einer Anwendung, das Menüelement neu zu zeichnet, um anzugeben, dass es ausgewählt ist.

### <a name="owner-drawn-menus-and-the-wm_menuchar-message"></a>Owner-Drawn Menüs und die WM \_ MENUCHAR-Meldung

Andere Menüs als besitzergezeichnete Menüs können ein mnemonisches Menü angeben, indem Sie einen Unterstrich neben einem Zeichen in die Menüzeichenfolge einfügen. Dadurch kann der Benutzer das Menü auswählen, indem er ALT und das mnemonische Menüzeichen drückt. In von Besitzern gezeichneten Menüs können Sie jedoch kein mnemonisches Menü auf diese Weise angeben. Stattdessen muss Ihre Anwendung die [**WM \_ MENUCHAR-Nachricht**](wm-menuchar.md) verarbeiten, um Menüs mit Mnemonischen Menüs mit Besitzerzeichen zur Verfügung zu stellen.

Die [**WM \_ MENUCHAR-Meldung**](wm-menuchar.md) wird gesendet, wenn der Benutzer ein mnemonisches Menü ein gibt, das nicht mit den vordefinierten Mnemonischen des aktuellen Menüs übereinstimmen kann. Der in *wParam enthaltene* Wert gibt das ASCII-Zeichen an, das dem Schlüssel entspricht, den der Benutzer mit der ALT-TASTE gedrückt hat. Das niedrige Wort *von wParam* gibt den Typ des ausgewählten Menüs an und kann einer der folgenden Werte sein:

-   **MF \_ POPUP,** wenn das aktuelle Menü ein Untermenü ist.
-   **MF \_ SYSMENU,** wenn das Menü das Systemmenü ist.

Das obere Wort *von wParam* enthält das Menühandli zum aktuellen Menü. Das Fenster mit den vom Besitzer gezeichneten Menüs kann [**WM \_ MENUCHAR**](wm-menuchar.md) wie folgt verarbeiten:


```
   case WM_MENUCHAR:
      nIndex = Determine index of menu item to be selected from
               character that was typed and handle to the current
               menu.
      return MAKELRESULT(nIndex, 2);
```



Die beiden im hohen Wort des Rückgabewerts informieren das System darüber, dass das niedrige Wort des Rückgabewerts den nullbasierten Index des zu wählenden Menüelements enthält.

Die folgenden Konstanten entsprechen den möglichen Rückgabewerten aus der [**WM \_ MENUCHAR-Meldung.**](wm-menuchar.md)



| Konstante         | Wert | Bedeutung                                                                                                                                                       |
|------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MNC \_ IGNORE**  | 0     | Das System sollte das Zeichen verwerfen, das der Benutzer gedrückt hat, und einen kurzen Signalton auf dem Systemlautlauter erstellen.                                                       |
| **MNC \_ CLOSE**   | 1     | Das System sollte das aktive Menü schließen.                                                                                                                      |
| **MNC \_ EXECUTE** | 2     | Das System sollte das Element auswählen, das im Niedrigwertwort des Rückgabewerts angegeben ist. Das Besitzerfenster empfängt eine [**WM \_ COMMAND-Meldung.**](wm-command.md) |
| **MNC \_ SELECT**  | 3     | Das System sollte das Element auswählen, das im Niedrigwertwort des Rückgabewerts angegeben ist.                                                                        |



 

### <a name="setting-fonts-for-menu-item-text-strings"></a>Festlegen von Schriftarten für Menu-Item Textzeichenfolgen

Dieses Thema enthält ein Beispiel aus einer Anwendung, die besitzergezeichnete Menüelemente in einem Menü verwendet. Das Menü enthält Elemente, die die Attribute der aktuellen Schriftart festlegen, und die Elemente werden mit dem entsprechenden Schriftartattribut angezeigt.

So wird das Menü in der Ressourcendefinitionsdatei definiert. Beachten Sie, dass die Zeichenfolgen für die Menüelemente Regular, Bold, Italic und Underline zur Laufzeit zugewiesen werden, sodass ihre Zeichenfolgen in der Ressourcendefinitionsdatei leer sind.


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



Die Fensterprozedur der Anwendung verarbeitet die Nachrichten, die an der Verwendung von Vom Besitzer gezeichneten Menüelementen beteiligt sind. Die Anwendung verwendet die [**WM \_ CREATE-Nachricht,**](/windows/desktop/winmsg/wm-create) um Folgendes zu tun:

-   Legen Sie das **MF \_ OWNERDRAW-Flag** für die Menüelemente fest.
-   Legen Sie die Textzeichenfolgen für die Menüelemente fest.
-   Abrufen von Handles der Schriftarten, die zum Zeichnen der Elemente verwendet werden.
-   Abrufen der Text- und Hintergrundfarbwerte für ausgewählte Menüelemente.

Die Textzeichenfolgen und Schriftarthandles werden in einem Array anwendungsdefinierter MYITEM-Strukturen gespeichert. Die anwendungsdefinierte GetAFont-Funktion erstellt eine Schriftart, die dem angegebenen Schriftartattribut entspricht, und gibt ein Handle an die Schriftart zurück. Die Handles werden während der Verarbeitung der [**WM \_ DESTROY-Nachricht**](/windows/desktop/winmsg/wm-destroy) zerstört.

Während der Verarbeitung der [**WM \_ MEASUREITEM-Nachricht**](../controls/wm-measureitem.md) ruft das Beispiel die Breite und Höhe einer Menüelementzeichenfolge ab und kopiert diese Werte in die [**MEASUREITEMSTRUCT-Struktur.**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) Das System verwendet die Werte für Breite und Höhe, um die Größe des Menüs zu berechnen.

Während der Verarbeitung der [**WM \_ DRAWITEM-Nachricht**](../controls/wm-drawitem.md) wird die Zeichenfolge des Menüelements mit platz links neben der Zeichenfolge für die Häkchenbitmap gezeichnet. Wenn der Benutzer das Element auswählt, werden der ausgewählte Text und die Hintergrundfarben verwendet, um das Element zu zeichnen.


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



### <a name="example-of-owner-drawn-menu-items"></a>Beispiel für Owner-Drawn Menüelemente

Im Beispiel in diesem Thema werden vom Besitzer gezeichnete Menüelemente in einem Menü verwendet. Die Menüelemente wählen bestimmte Schriftartattribute aus, und die Anwendung zeigt jedes Menüelement mit einer Schriftart an, die über das entsprechende Attribut verfügt. Beispielsweise wird das **italische** Menüelement in einer italischen Schriftart angezeigt. Der **Menüname** Zeichen in der Menüleiste öffnet das Menü.

Die Menüleiste und das Dropdownmenü werden anfänglich durch eine erweiterte Menüvorlagenressource definiert. Da eine Menüvorlage keine vom Besitzer gezeichneten Elemente angeben kann, enthält das Menü zunächst vier Textmenüelemente mit den folgenden Zeichenfolgen: "Regular", "Bold", "Italic" und "Underline". Die Fensterprozedur der Anwendung ändert diese elemente in vom Besitzer gezeichnete Elemente, wenn sie die [**WM \_ CREATE-Nachricht**](/windows/desktop/winmsg/wm-create) verarbeitet. Wenn die **WM \_ CREATE-Nachricht** empfangen wird, ruft die Fensterprozedur die anwendungsdefinierte OnCreate-Funktion auf, die die folgenden Schritte für jedes Menüelement ausführt:

-   Ordnet eine anwendungsdefinierte MYITEM-Struktur zu.
-   Ruft den Text des Menüelements ab und speichert ihn in der anwendungsdefinierten MYITEM-Struktur.
-   Erstellt die Schriftart, die zum Anzeigen des Menüelements verwendet wird, und speichert das Handle in der anwendungsdefinierten MYITEM-Struktur.
-   Ändert den Menüelementtyp in **MFT \_ OWNERDRAW** und speichert einen Zeiger auf die anwendungsdefinierte MYITEM-Struktur als Elementdaten.

Da ein Zeiger auf jede anwendungsdefinierte MYITEM-Struktur als Elementdaten gespeichert wird, wird er zusammen mit den [**MELDUNGEN WM \_ MEASUREITEM**](../controls/wm-measureitem.md) und [**WM \_ DRAWITEM**](../controls/wm-drawitem.md) für das entsprechende Menüelement an die Fensterprozedur übergeben. Der Zeiger ist im **itemData-Member** sowohl der [**MEASUREITEMSTRUCT- als**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) auch [**der DRAWITEMSTRUCT-Struktur**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) enthalten.

Eine [**WM \_ MEASUREITEM-Meldung**](../controls/wm-measureitem.md) wird für jedes vom Besitzer gezeichnete Menüelement gesendet, wenn es zum ersten Mal angezeigt wird. Die Anwendung verarbeitet diese Nachricht, indem sie die Schriftart für das Menüelement in einem Gerätekontext auswählt und dann den Speicherplatz bestimmt, der zum Anzeigen des Menüelementtexts in dieser Schriftart erforderlich ist. Die Schriftart und der Menüelementtext werden beide durch die Struktur des Menüelements (die von der Anwendung `MYITEM` definierte Struktur) angegeben. Die Anwendung bestimmt die Größe des Texts mithilfe der [**GetTextExtentPoint32-Funktion.**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpoint32a)

Die Fensterprozedur verarbeitet die [**WM \_ DRAWITEM-Meldung,**](../controls/wm-drawitem.md) indem der Menüelementtext in der entsprechenden Schriftart angezeigt wird. Die Schriftart und der Menüelementtext werden beide durch die Struktur des Menüelements `MYITEM` angegeben. Die Anwendung wählt Text- und Hintergrundfarben aus, die für den Zustand des Menüelements geeignet sind.

Die Fensterprozedur verarbeitet die [**WM \_ DESTROY-Nachricht,**](/windows/desktop/winmsg/wm-destroy) um Schriftarten zu zerstören und Arbeitsspeicher frei zu machen. Die Anwendung löscht die Schriftart und gibt die anwendungsdefinierte MYITEM-Struktur für jedes Menüelement frei.

Im Folgenden sind die relevanten Teile der Headerdatei der Anwendung angegeben.


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



Im Folgenden sind die relevanten Teile der Fensterprozedur der Anwendung und die zugehörigen Funktionen aufgeführt.


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



## <a name="using-custom-check-mark-bitmaps"></a>Verwenden von benutzerdefinierten Häkchenbitmaps

Das System stellt eine Standardmäßige Häkchenbitmap zum Anzeigen neben einem ausgewählten Menüelement bereit. Sie können ein einzelnes Menüelement anpassen, indem Sie ein Bitmappaar bereitstellen, um die Standardmäßige Häkchenbitmap zu ersetzen. Das System zeigt eine Bitmap an, wenn das Element ausgewählt ist, und die andere, wenn es gelöscht wird. In diesem Abschnitt werden die Schritte zum Erstellen und Verwenden von benutzerdefinierten Häkchenbitmaps beschrieben.

-   [Erstellen von benutzerdefinierten Häkchenbitmaps](#creating-custom-check-mark-bitmaps)
-   [Zuordnen von Bitmaps zu einem Menüelement](#associating-bitmaps-with-a-menu-item)
-   [Festlegen des Häkchenattributs](#setting-the-check-mark-attribute)
-   [Simulieren von Kontrollkästchen in einem Menü](#simulating-check-boxes-in-a-menu)
-   [Beispiel für die Verwendung von benutzerdefinierten Häkchenbitmaps](#example-of-using-custom-check-mark-bitmaps)

### <a name="creating-custom-check-mark-bitmaps"></a>Erstellen von benutzerdefinierten Häkchenbitmaps

Eine benutzerdefinierte Häkchenbitmap muss die gleiche Größe wie die Standardmäßige Häkchenbitmap haben. Sie können die Standardmäßige Häkchengröße der Bitmap abrufen, indem Sie die [**GetSystemMetrics-Funktion**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) aufrufen. Das Wort in niedriger Reihenfolge des Rückgabewerts dieser Funktion gibt die Breite an. das Wort in hoher Reihenfolge gibt die Höhe an.

Sie können Bitmapressourcen verwenden, um Bitmaps mit Häkchen bereitzustellen. Da die erforderliche Bitmapgröße jedoch je nach Anzeigetyp variiert, müssen Sie möglicherweise die Größe der Bitmap zur Laufzeit mithilfe der [**StretchBlt-Funktion**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) ändern. Je nach Bitmap kann die Verzerrung, die durch größenabhängige Größen verursacht wird, zu inakzeptablen Ergebnissen führen.

Anstatt eine Bitmapressource zu verwenden, können Sie zur Laufzeit mithilfe von GDI-Funktionen eine Bitmap erstellen.

**So erstellen Sie zur Laufzeit eine Bitmap**

1.  Verwenden Sie die [**CreateCompatibleDC-Funktion,**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) um einen Gerätekontext zu erstellen, der mit dem vom Hauptfenster der Anwendung verwendeten kompatibel ist.

    Der *hdc-Parameter* der Funktion kann entweder **NULL** oder den Rückgabewert der Funktion angeben. [**CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) gibt ein Handle für den kompatiblen Gerätekontext zurück.

2.  Verwenden Sie die [**CreateCompatibleBitmap-Funktion,**](/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap) um eine Bitmap zu erstellen, die mit dem Hauptfenster der Anwendung kompatibel ist.

    Die Parameter *nWidth* und *nHeight* dieser Funktion legen die Größe der Bitmap fest. Sie sollten die Von der [**GetSystemMetrics-Funktion**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) zurückgegebenen Informationen zur Breite und Höhe angeben.

    > [!Note]  
    > Sie können auch die [**CreateBitmap-Funktion**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) verwenden, um eine monocolore Bitmap zu erstellen.

     

3.  Verwenden Sie die [**SelectObject-Funktion,**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) um die Bitmap im kompatiblen Gerätekontext auszuwählen.
4.  Verwenden Sie GDI-Zeichnungsfunktionen wie [**Ellipse**](/windows/desktop/api/wingdi/nf-wingdi-ellipse) und [**LineTo,**](/windows/desktop/api/wingdi/nf-wingdi-lineto)um ein Bild in die Bitmap zu zeichnen, oder verwenden Sie Funktionen wie [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) und [**StretchBlt,**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) um ein Bild in die Bitmap zu kopieren.

Weitere Informationen finden Sie unter [Bitmaps.](/windows/desktop/gdi/bitmaps)

### <a name="associating-bitmaps-with-a-menu-item"></a>Zuordnen von Bitmaps zu einem Menüelement

Sie ordnen ein Paar von Häkchenbitmaps einem Menüelement zu, indem Sie die Handles der Bitmaps an die [**SetMenuItemBitmaps-Funktion**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) übergeben. Der *hBitmapUnchecked-Parameter* identifiziert die eindeutige Bitmap, und der *hBitmapChecked-Parameter* identifiziert die ausgewählte Bitmap. Wenn Sie ein oder beide Häkchen aus einem Menüelement entfernen möchten, können Sie den Parameter *hBitmapUnchecked* oder *hBitmapChecked* oder beides auf **NULL** festlegen.

### <a name="setting-the-check-mark-attribute"></a>Festlegen des Häkchenattributs

Die [**CheckMenuItem-Funktion**](/windows/desktop/api/Winuser/nf-winuser-checkmenuitem) legt das Häkchenattribut eines Menüelements entweder auf ausgewählt oder gelöscht fest. Sie können den **MF \_ CHECKED-Wert** angeben, um das Häkchenattribut auf selected und den **MF \_ UNCHECKED-Wert** auf clear festzulegen.

Sie können den Überprüfungsstatus eines Menüelements auch mithilfe der [**SetMenuItemInfo-Funktion**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) festlegen.

Manchmal stellt eine Gruppe von Menüelementen eine Reihe von sich gegenseitig ausschließenden Optionen dar. Mithilfe der [**CheckMenuRadioItem-Funktion**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem) können Sie ein Menüelement überprüfen und gleichzeitig das Häkchen aus allen anderen Menüelementen in der Gruppe entfernen.

### <a name="simulating-check-boxes-in-a-menu"></a>Simulieren von Kontrollkästchen in einem Menü

Dieses Thema enthält ein Beispiel, das zeigt, wie Kontrollkästchen in einem Menü simuliert werden. Das Beispiel enthält ein Zeichenmenü, dessen Elemente es dem Benutzer ermöglichen, die Fett-, Kursiv- und Unterstreichungsattribute der aktuellen Schriftart festzulegen. Wenn ein Schriftartattribut aktiviert ist, wird im Kontrollkästchen neben dem entsprechenden Menüelement ein Häkchen angezeigt. Andernfalls wird neben dem Element ein leeres Kontrollkästchen angezeigt.

Im Beispiel wird die Standardmarkierungsbitmap durch zwei Bitmaps ersetzt: eine Bitmap mit einem ausgewählten Kontrollkästchen und die Bitmap durch ein leeres Feld. Die ausgewählte Kontrollkästchenbitmap wird neben dem Menüelement Fett, Kursiv oder Unterstrichen angezeigt, wenn das Häkchenattribut des Elements auf **MF \_ CHECKED** festgelegt ist. Die Bitmap für das deaktivieren oder leere Kontrollkästchen wird angezeigt, wenn das Häkchenattribut auf **MF \_ UNCHECKED** festgelegt ist.

Das System stellt eine vordefinierte Bitmap bereit, die die Bilder enthält, die für Kontrollkästchen und Optionsfelder verwendet werden. Im Beispiel werden die ausgewählten und leeren Kontrollkästchen isoliert, in zwei separate Bitmaps kopiert und dann als ausgewählte und gelöschte Bitmaps für Elemente im Menü **Zeichen** verwendet.

Um ein Handle für die systemdefinierte Kontrollkästchenbitmap abzurufen, ruft das Beispiel die [**LoadBitmap-Funktion**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) auf und gibt **NULL** als *hInstance-Parameter* und **OBM \_ CHECKBOXES** als *lpBitmapName-Parameter* an. Da die Bilder in der Bitmap alle die gleiche Größe aufweisen, können sie im Beispiel isoliert werden, indem die Breite und Höhe der Bitmap durch die Anzahl der Bilder in den Zeilen und Spalten dividiert wird.

Der folgende Teil einer Ressourcendefinitionsdatei zeigt, wie die Menüelemente im Menü **Zeichen** definiert werden. Beachten Sie, dass anfänglich keine Schriftartattribute wirksam sind, sodass das Häkchenattribut für das **Reguläre** Element auf ausgewählt und standardmäßig das Häkchenattribut der verbleibenden Elemente auf "Löschen" festgelegt ist.


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



Hier sind die relevanten Inhalte der Headerdatei der Anwendung angegeben.


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



Das folgende Beispiel zeigt die Teile der Fensterprozedur, die die Häkchenbitmaps erstellen. Legen Sie das Häkchenattribut der Menüelemente **Bold**, **Italic** und **Underline** fest. und zerstören Häkchenbitmaps.


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



### <a name="example-of-using-custom-check-mark-bitmaps"></a>Beispiel für die Verwendung von benutzerdefinierten Häkchenbitmaps

Im Beispiel in diesem Thema werden Menüelementen in zwei Menüs benutzerdefinierte Häkchenbitmaps zugewiesen. Die Menüelemente im ersten Menü geben Zeichenattribute an: fett, kursiv und unterstrichen. Jedes Menüelement kann entweder ausgewählt oder gelöscht werden. Für diese Menüelemente werden im Beispiel Bitmaps mit Häkchen verwendet, die den ausgewählten und gelöschten Zuständen eines Kontrollkästchen-Steuerelements ähneln.

Die Menüelemente im zweiten Menü geben Absatzausrichtungseinstellungen an: links, zentriert und rechts. Es wird immer nur eines dieser Menüelemente ausgewählt. Für diese Menüelemente werden im Beispiel Bitmaps mit Häkchen verwendet, die den ausgewählten und eindeutigen Zuständen eines Optionsfeld-Steuerelements ähneln.

Die Fensterprozedur verarbeitet die [**WM \_ CREATE-Nachricht,**](/windows/desktop/winmsg/wm-create) indem die anwendungsdefinierte OnCreate-Funktion aufgerufen wird. `OnCreate` erstellt die vier Häkchenbitmaps und weist sie dann mithilfe der [**SetMenuItemBitmaps-Funktion**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) ihren entsprechenden Menüelementen zu.

Um jede Bitmap zu erstellen, ruft OnCreate die anwendungsdefinierte CreateMenuBitmaps-Funktion auf und gibt einen Zeiger auf eine bitmapspezifische Zeichnungsfunktion an. CreateMenuBitmaps erstellt eine monocolore Bitmap der erforderlichen Größe, wählt sie in einem Speichergerätekontext aus und löscht den Hintergrund. Anschließend ruft sie die angegebene Zeichnungsfunktion auf, um den Vordergrund auszufüllen.

Die vier anwendungsdefinierte Zeichnungsfunktionen sind DrawCheck, DrawUncheck, **DrawRadioCheck** und DrawRadioUncheck. Sie zeichnen ein Rechteck mit einem X, einem leeren Rechteck, einer Ellipse mit einer kleineren gefüllten Ellipse bzw. einer leeren Ellipse.

Die Fensterprozedur verarbeitet die [**WM \_ DESTROY-Nachricht,**](/windows/desktop/winmsg/wm-destroy) indem die Häkchenbitmaps gelöscht werden. Sie ruft jedes Bitmaphandle mithilfe der [**GetMenuItemInfo-Funktion**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) ab und übergibt dann ein Handle an die Funktion.

Wenn der Benutzer ein Menüelement auswählt, wird eine [**WM \_ COMMAND-Meldung**](wm-command.md) an das Besitzerfenster gesendet. Für Menüelemente im Menü **Zeichen** ruft die Fensterprozedur die anwendungsdefinierte CheckCharacterItem-Funktion auf. Für Elemente im **Menü Absatz** ruft die Fensterprozedur die anwendungsdefinierte CheckParagraphItem-Funktion auf.

Jedes Element im Menü **Zeichen** kann unabhängig ausgewählt und gelöscht werden. Daher wechselt CheckCharacterItem einfach den Prüfzustand des angegebenen Menüelements. Zuerst ruft die Funktion die [**GetMenuItemInfo-Funktion**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) auf, um den aktuellen Menüelementzustand abzurufen. Anschließend wechselt das **MFS \_ CHECKED-Statusflag** und legt den neuen Zustand fest, indem die [**SetMenuItemInfo-Funktion**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) aufgerufen wird.

Im Gegensatz zu Zeichenattributen kann jeweils nur eine Absatzausrichtung ausgewählt werden. Daher überprüft CheckParagraphItem das angegebene Menüelement und entfernt das Häkchen aus allen anderen Elementen im Menü. Zu diesem Zweck wird die [**CheckMenuRadioItem-Funktion**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem) aufrufen.

Im Folgenden sind die relevanten Teile der Headerdatei der Anwendung angegeben.


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



Im Folgenden sind die relevanten Teile der Fensterprozedur der Anwendung und die zugehörigen Funktionen aufgeführt.


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



 

 