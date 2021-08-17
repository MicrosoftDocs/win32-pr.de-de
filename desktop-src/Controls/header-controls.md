---
title: Informationen zu Headersteuerelementen
description: Ein Headersteuerfeld ist ein Fenster, das in der Regel über Spalten mit Text oder Zahlen positioniert ist. Sie enthält einen Titel für jede Spalte und kann in Teile unterteilt werden.
ms.assetid: b464fb9a-e342-4209-ba6f-15b5388f3914
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a6308def8c760ffab492d7aeea086970740be07ebd559d94791baf3512c178b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412262"
---
# <a name="about-header-controls"></a>Informationen zu Headersteuerelementen

Ein Headersteuerfeld ist ein Fenster, das in der Regel über Spalten mit Text oder Zahlen positioniert ist. Sie enthält einen Titel für jede Spalte und kann in Teile unterteilt werden. Der Benutzer kann die Trennlinien ziehen, die die Teile trennen, um die Breite der einzelnen Spalten zu festlegen. Die folgende Abbildung zeigt ein Header-Steuerelement mit bezeichneten Spalten, die ausführliche Informationen zu Dateien in einem Verzeichnis enthalten.

![Screenshot eines Dialogfelds mit einem Dreispaltenheader-Steuerelement](images/header.png)

Sie können ein Header-Steuerelement erstellen, indem Sie die [**CreateWindowEx-Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) verwenden und dabei die [**Fensterklasse WC \_ HEADER**](common-control-window-classes.md) und die entsprechenden [Headersteuerstile angeben.](header-control-styles.md) Diese Fensterklasse wird registriert, wenn die allgemeine Steuerelement-DLL geladen wird. Um sicherzustellen, dass diese DLL geladen wird, verwenden Sie die [**InitCommonControlsEx-Funktion.**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) Nachdem Sie ein Headersteuerfeld erstellt haben, können Sie es in Teile unterteilen, den Text in jedem Teil festlegen und die Darstellung des Fensters mithilfe von Headerfenstermeldungen steuern.

Ein Headersteuerfeld kann als untergeordnetes Fenster eines anderen Steuerelements erstellt werden, z. B. eines Listenfelds. Das übergeordnete Steuerelement kennt das Headersteuerelementen jedoch nicht und lässt den vom Header in Rechnung genommenen Speicherplatz nicht zu, mit dem Ergebnis, dass Listenelemente hinter dem Header angezeigt werden. Wenn Sie ein Header-Steuerelement in einem Listenfeld oder einem anderen Steuerelement verwenden möchten, muss das übergeordnete Steuerelement vom Besitzer gezeichnet werden, damit alle Elemente an der richtigen Position angezeigt werden.

Listenansichtssteuerelemente verfügen bereits über Headersteuerelemente. Anstatt ein Headersteuerfeld für ein Listenansicht-Steuerelement zu erstellen, verwenden Sie [**LVM \_ GETHEADER**](lvm-getheader.md) oder [**ListView \_ GetHeader,**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getheader) um das vorhandene Steuerelement abzurufen.

-   [Header-Steuerelementgröße und -position](#header-control-size-and-position)
-   [Elemente](#items)
-   [Owner-Drawn Header-Steuerelemente](#owner-drawn-header-controls)
-   [Headersteuersteuerfilter](#header-control-filters)
-   [Nachrichtenverarbeitung für Standardheadersteuersatz](#default-header-control-message-processing)

## <a name="header-control-size-and-position"></a>Header-Steuerelementgröße und -position

In der Regel müssen Sie die Größe und Position eines Header-Steuerelements so festlegen, dass es in die Grenzen eines bestimmten Rechtecks passt, z. B. den Clientbereich eines Fensters. Mithilfe der [**\_ HDM-LAYOUT-Meldung**](hdm-layout.md) können Sie die entsprechenden Werte für Größe und Position aus dem Header-Steuerelement abrufen.

Beim Senden [**von \_ HDM-LAYOUT**](hdm-layout.md)geben Sie die Adresse einer [**HDLAYOUT-Struktur**](/windows/win32/api/commctrl/ns-commctrl-hdlayout) an, die die Koordinaten des Rechtecks enthält, das das Headersteuerfeld belegen soll, und stellt einen Zeiger auf eine [**WINDOWPOS-Struktur**](/windows/win32/api/winuser/ns-winuser-windowpos) zur Auswahl. Das -Steuerelement füllt die **WINDOWPOS-Struktur** mit Größen- und Positionswerten, die für die Positionierung des Steuerelements am oberen Ende des angegebenen Rechtecks geeignet sind. Der Höhenwert ist die Summe der Höhe der horizontalen Rahmen des Steuerelements und der durchschnittlichen Höhe der Zeichen in der Schriftart, die derzeit im Gerätekontext des Steuerelements ausgewählt ist.

Wenn Sie [**HDM \_ LAYOUT verwenden**](hdm-layout.md) möchten, um die Anfangsgröße und -position eines Header-Steuerelements festlegen zu können, legen Sie den anfänglichen Sichtbarkeitszustand des Steuerelements so fest, dass es ausgeblendet wird. Nach dem **Senden von \_ HDM-LAYOUT** zum Abrufen der Werte für Größe und Position können Sie die [**Funktion SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) verwenden, um die neue Größe, Position und den Sichtbarkeitszustand zu festlegen.

## <a name="items"></a>Elemente

Ein Headersteuerelemente verfügt in der Regel über mehrere Headerelemente, die die Spalten des Steuerelements definieren. Sie fügen einem Headersteuerelement ein Element hinzu, indem Sie die [**HDM \_ INSERTITEM-Nachricht**](hdm-insertitem.md) an das Steuerelement senden. Die Nachricht enthält die Adresse einer [**HDITEM-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-hditema) Diese Struktur definiert die Eigenschaften des Headerelements, die eine Zeichenfolge, ein Bitmapbild, eine Anfangsgröße und einen anwendungsdefinierten **LPARAM-Wert enthalten** können.

Das **fmt-Element** der [**HDITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-hditema) eines Elements kann entweder das **HDF \_ STRING-** oder **HDF \_ BITMAP-Flag** enthalten, um anzugeben, ob das Steuerelement die Zeichenfolge oder Bitmap des Elements anzeigt. Wenn Sie sowohl eine Zeichenfolge als auch eine Bitmap anzeigen möchten, erstellen Sie ein vom Besitzer gezeichnetes Element, indem Sie das **fmt-Element** so festlegen, dass es das **HDF \_ OWNERDRAW-Flag** enthält. Die **HDITEM-Struktur** gibt auch Formatierungsflags an, die dem Steuerelement mitteilen, ob die Zeichenfolge oder Bitmap im Rechteck des Elements zentriert, links ausgerichtet oder rechts ausgerichtet werden soll.

[**HDM \_ INSERTITEM gibt**](hdm-insertitem.md) den Index des neu hinzugefügten Elements zurück. Sie können den Index in anderen Nachrichten verwenden, um Eigenschaften zu setzen oder Informationen zum Element abzurufen. Sie können ein Element löschen, indem Sie die [**HDM \_ DELETEITEM-Nachricht**](hdm-deleteitem.md) verwenden und dabei den Index des zu löschenden Elements angeben.

Sie können die [**HDM \_ SETITEM-Nachricht**](hdm-setitem.md) verwenden, um die Eigenschaften eines vorhandenen Headerelements und die [**HDM \_ GETITEM-Nachricht**](hdm-getitem.md) zum Abrufen der aktuellen Eigenschaften eines Elements fest. Um die Anzahl der Elemente in einem Headersteuerelementen abzurufen, verwenden Sie die [**HDM \_ GETITEMCOUNT-Nachricht.**](hdm-getitemcount.md)

## <a name="owner-drawn-header-controls"></a>Owner-Drawn Headersteuerelemente

Sie können einzelne Elemente eines Headersteuerelementes als vom Besitzer gezeichnete Elemente definieren. Wenn Sie diese Technik verwenden, erhalten Sie mehr Kontrolle als sonst über die Darstellung eines Headerelements.

Sie können die [**HDM \_ INSERTITEM-Nachricht**](hdm-insertitem.md) verwenden, um ein neues vom Besitzer gezeichnetes Element in ein Headersteuerelement oder die [**HDM \_ SETITEM-Nachricht**](hdm-setitem.md) zu verwenden, um ein vorhandenes Element in ein vom Besitzer gezeichnetes Element zu ändern. Beide Nachrichten enthalten die Adresse einer [**HDITEM-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-hditema) für die das **fmt-Member** auf den **HDF \_ OWNERDRAW-Wert festgelegt sein** sollte.

Wenn ein Headersteuerelement ein vom Besitzer gezeichnetes Element zeichnen muss, sendet es die [**WM \_ DRAWITEM-Nachricht**](wm-drawitem.md) an das übergeordnete Fenster. Der *wParam-Parameter* der Nachricht ist der bezeichner des untergeordneten Fensters des Headersteuerzeichens, und der *lParam-Parameter* ist eine Adresse einer [**DRAWITEMSTRUCT-Struktur.**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) Das übergeordnete Fenster verwendet die Informationen in der -Struktur, um das Element zu zeichnen. Für ein vom Besitzer gezeichnetes Element in einem Headersteuerelement enthält die **DRAWITEMSTRUCT-Struktur** die folgenden Informationen.



| Member         | Beschreibung                                                                                                                                            |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CtlType**    | [**ODT \_ HEADER**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) owner-drawn-Steuerelementtyp.                                                                                        |
| **CtlID**      | Bezeichner des untergeordneten Fensters des Headersteuerzeichens.                                                                                                         |
| **Itemid**     | Index des zu zeichneten Elements.                                                                                                                         |
| **itemAction** | [**VEREerbung \_ DRAWENTIRE-Zeichenaktionsflag.**](/windows/win32/api/winuser/ns-winuser-drawitemstruct)                                                                                         |
| **itemState**  | [**ODS \_**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) SELECTED-Zeichenaktionsflag, wenn sich der Cursor auf dem Element befindet und die Maustaste gedrückt ist. Andernfalls ist dieser Member 0 (null). |
| **hwndItem**   | Handle für das Header-Steuerelement.                                                                                                                          |
| **Hdc**        | Handle für den Gerätekontext des Header-Steuerelements.                                                                                                    |
| **rcItem**     | Koordinaten des zu zeichneten Headerelements. Die Koordinaten sind relativ zur oberen linken Ecke des Header-Steuerelements.                               |
| **Itemdata**   | Anwendungsdefinierter 32-Bit-Wert, der dem Element zugeordnet ist.                                                                                             |



 

## <a name="header-control-filters"></a>Headersteuersteuerfilter

Durch Angeben des [**HDS \_ FILTERBAR-Fensterstils**](header-control-styles.md) für ein Header-Steuerelement können Sie die Platzierung von Filterbearbeitungsfeldern unterhalb der Spaltenüberschriften aktivieren. Neben dem Bearbeitungsfeld wird eine Filterschaltfläche angezeigt. Sie können die Filterung implementieren, indem Sie auf [HDN-Benachrichtigungscodes \_ BEGINFILTEREDIT,](hdn-beginfilteredit.md) [HDN \_ ENDFILTEREDIT,](hdn-endfilteredit.md) [HDN \_ FILTERBTNCLICK](hdn-filterbtnclick.md)oder [HDN \_ FILTERCHANGE](hdn-filterchange.md) reagieren.

Standardmäßig enthält das Bearbeitungsfeld eine Eingabeaufforderung für den Benutzer. Sie können das Bearbeitungsfeld mithilfe von [**Header \_ ClearFilter**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearfilter) oder Header ClearAllFilters in diesem [**\_ Standardzustand wiederherstellen.**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearallfilters)

Das folgende Codebeispiel zeigt, wie sie das Headersteuersatz-Steuerelement aus einem Listenansicht-Steuerelement abrufen und eine Filterleiste hinzufügen.


```
// hList is the HWND of the list-view control.
HWND hHeader = ListView_GetHeader(hList);
LONG_PTR styles = GetWindowLongPtr(hHeader, GWL_STYLE);
SetWindowLongPtr(g_hHeader, GWL_STYLE, styles | HDS_FILTERBAR);
```



## <a name="default-header-control-message-processing"></a>Nachrichtenverarbeitung für Standardheadersteuersatz

In diesem Abschnitt werden die Fenstermeldungen beschrieben, die von der Fensterprozedur für die [**WC \_ HEADER-Fensterklasse**](common-control-window-classes.md) verarbeitet werden.



| `Message`                                            | Verarbeitung ausgeführt                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ CREATE**](/windows/desktop/winmsg/wm-create)                 | Initialisiert das Headersteuerobjekt.                                                                                                                                                                                                                                                                               |
| [**WM \_ DESTROY**](/windows/desktop/winmsg/wm-destroy)               | Initialisiert das Header-Steuerelement.                                                                                                                                                                                                                                                                             |
| [**WM \_ ERASEBKGND**](/windows/desktop/winmsg/wm-erasebkgnd)         | Füllt den Hintergrund des Header-Steuerelements mithilfe der aktuellen Hintergrundfarbe des Steuerelements.                                                                                                                                                                                                                      |
| [**WM \_ GETDLGCODE**](/windows/desktop/dlgbox/wm-getdlgcode)         | Gibt eine Kombination der [**DLGC-Werte \_ WANTTAB**](/windows/desktop/dlgbox/wm-getdlgcode) und [**DLGC \_ WANTWS**](/windows/desktop/dlgbox/wm-getdlgcode) zurück.                                                                                                                     |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)               | Gibt das Handle an die aktuelle Schriftart zurück, die vom Headersteuerfeld zum Zeichnen des Texts verwendet wird.                                                                                                                                                                                                                 |
| [**WM \_ LBUTTONDBLCLK**](/windows/desktop/inputdev/wm-lbuttondblclk) | Erfasst Mauseingaben. Wenn sich der Mauszeiger auf einem Unterteiler befindet, sendet das Steuerelement den [HDN BEGINTRACK-Benachrichtigungscode \_ ](hdn-begintrack.md) und beginnt mit dem Ziehen des Unterteilers. Wenn sich der Cursor auf einem Element befindet, wird das Element im gedrückten Zustand angezeigt.                                                            |
| [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)     | Identisch mit der [**\_ WM-LBUTTONDBLCLK-Nachricht.**](/windows/desktop/inputdev/wm-lbuttondblclk)                                                                                                                                                                                                                                       |
| [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup)         | Gibt die Mausaufnahme frei. Wenn das Steuerelement die Mausbewegung verfolgt hat, sendet es den [HDN ENDTRACK-Benachrichtigungscode \_ ](hdn-endtrack.md) und umrext das Headersteuerelement. Andernfalls sendet das Steuerelement den [HDN ITEMCLICK-Benachrichtigungscode \_ ](hdn-itemclick.md) und schreibt das Headerelement neu, auf das geklickt wurde. |
| [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove)         | Wenn ein Trennzeichen gezogen wird, sendet das Steuerelement den [HDN \_ TRACK-Benachrichtigungscode](hdn-track.md) und zeigt das Element an der neuen Position an. Wenn die linke Maustaste gedrückt ist und sich der Cursor auf einem Element befindet, wird das Element im gedrückten Zustand angezeigt.                                                      |
| [**WM \_ NCCREATE**](/windows/desktop/winmsg/wm-nccreate)             | Ordnet eine interne Datenstruktur zu und initialisiert sie.                                                                                                                                                                                                                                                         |
| [**WM \_ NCDESTROY**](/windows/desktop/winmsg/wm-ncdestroy)           | Gibt die vom Headersteuerelement zugeordneten Ressourcen frei, nachdem das Headersteuerelement nicht initialisiert wurde.                                                                                                                                                                                                                |
| [**WM \_ PAINT**](/windows/desktop/gdi/wm-paint)                      | Zeichnet den ungültigen Bereich des Headersteuerelements. Wenn der *wParam-Parameter* ungleich NULL ist, geht das Steuerelement davon aus, dass der Wert ein HDC ist und zeichnet mit diesem Gerätekontext.                                                                                                                                    |
| [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor)           | Legt die Cursorform fest, je nachdem, ob sich der Cursor auf einem Trennelement oder in einem Headerelement befindet.                                                                                                                                                                                                                   |
| [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont)               | Wählt ein neues Schriftarthandle im Gerätekontext für das Headersteuerelement aus.                                                                                                                                                                                                                                     |



 

 

 