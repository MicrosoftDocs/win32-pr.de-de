---
title: Informationen über Header Steuerelemente
description: Ein Header Steuerelement ist ein Fenster, das normalerweise oberhalb der Spalten von Text oder Zahlen positioniert ist. Sie enthält einen Titel für jede Spalte und kann in Teile aufgeteilt werden.
ms.assetid: b464fb9a-e342-4209-ba6f-15b5388f3914
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6d9beaa9dc3bd8eb94d749ec271902a480b853e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730401"
---
# <a name="about-header-controls"></a>Informationen über Header Steuerelemente

Ein Header Steuerelement ist ein Fenster, das normalerweise oberhalb der Spalten von Text oder Zahlen positioniert ist. Sie enthält einen Titel für jede Spalte und kann in Teile aufgeteilt werden. Der Benutzer kann die unter Teiler zum Trennen der Teile ziehen, um die Breite der einzelnen Spalten festzulegen. In der folgenden Abbildung wird ein Header Steuerelement mit beschrifteten Spalten gezeigt, die ausführliche Informationen zu Dateien in einem Verzeichnis zur Verfügung haben.

![Screenshot eines Dialog Felds mit einem drei spaltigen Header Steuerelement](images/header.png)

Sie können ein Header Steuerelement erstellen, indem Sie die Funktion "up- [**windowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " verwenden und dabei die Fenster Klasse " [**WC- \_ Header**](common-control-window-classes.md) " und die entsprechenden [Header Steuerelement Stile](header-control-styles.md)angeben. Diese Fenster Klasse wird beim Laden der allgemeinen Steuerelement-DLL registriert. Um sicherzustellen, dass diese DLL geladen wird, verwenden Sie die [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) -Funktion. Nachdem Sie ein Header Steuerelement erstellt haben, können Sie es in Teile aufteilen, den Text in jedem Teil festlegen und die Darstellung des Fensters mithilfe von Header Fenster Meldungen steuern.

Ein Header Steuerelement kann als untergeordnetes Fenster eines anderen Steuer Elements erstellt werden, z. b. in einem Listenfeld. Das übergeordnete Steuerelement kennt das Header Steuerelement jedoch nicht und lässt den von der Kopfzeile aufgenommenen Platz nicht zu, und das Ergebnis ist, dass Listenelemente hinter dem Header angezeigt werden. Wenn Sie ein Header Steuerelement in einem Listenfeld oder einem anderen Steuerelement verwenden möchten, muss das übergeordnete Steuerelement vom Besitzer gezeichnet werden, damit alle Elemente an der richtigen Position angezeigt werden.

Listenansicht-Steuerelemente haben bereits Header-Steuerelemente. Anstatt ein Header Steuerelement für ein Listenansicht-Steuerelement zu erstellen, verwenden Sie [**LVM \_ ge-Ader**](lvm-getheader.md) oder [**ListView \_ getheiader**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getheader) , um das vorhandene Steuerelement abzurufen.

-   [Größe und Position des Header Steuer Elements](#header-control-size-and-position)
-   [Elemente](#items)
-   [Vom Besitzer gezeichnete Header Steuerelemente](#owner-drawn-header-controls)
-   [Header Steuerelement Filter](#header-control-filters)
-   [Nachrichtenverarbeitung für Standard Header Steuerelemente](#default-header-control-message-processing)

## <a name="header-control-size-and-position"></a>Größe und Position des Header Steuer Elements

In der Regel müssen Sie die Größe und Position eines Header Steuer Elements so festlegen, dass es in die Begrenzungen eines bestimmten Rechtecks passt, z. b. den Client Bereich eines Fensters. Mithilfe der [**HDM- \_ layoutnachricht**](hdm-layout.md) können Sie die entsprechenden Größen-und Positionswerte aus dem Header Steuerelement abrufen.

Beim Senden des [**HDM- \_ Layouts**](hdm-layout.md)geben Sie die Adresse einer [**hdlayout**](/windows/win32/api/commctrl/ns-commctrl-hdlayout) -Struktur an, die die Koordinaten des Rechtecks enthält, das das Header Steuerelement belegen soll, und stellt einen Zeiger auf eine [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) -Struktur bereit. Das-Steuerelement füllt die **WINDOWPOS** -Struktur mit Größen-und Positions Werten für die Positionierung des Steuer Elements am oberen Rand des angegebenen Rechtecks. Der Height-Wert ist die Summe der Höhe der horizontalen Rahmen des Steuer Elements und die durchschnittliche Höhe der Zeichen in der Schriftart, die derzeit im Gerätekontext des Steuer Elements ausgewählt ist.

Wenn Sie das [**HDM- \_ Layout**](hdm-layout.md) verwenden möchten, um die anfängliche Größe und Position eines Header Steuer Elements festzulegen, legen Sie den ursprünglichen Sichtbarkeits Zustand des Steuer Elements so fest, dass es ausgeblendet ist. Nachdem Sie das **HDM- \_ Layout** zum Abrufen der Größen-und Positionswerte gesendet haben, können Sie die Funktion [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) verwenden, um die neue Größe, Position und den Status der Sichtbarkeit festzulegen.

## <a name="items"></a>Items

Ein Header Steuerelement verfügt in der Regel über mehrere Header Elemente, die die Spalten des Steuer Elements definieren. Sie fügen ein Element zu einem Header-Steuerelement hinzu, indem Sie die [**HDM \_ InsertItem**](hdm-insertitem.md) -Nachricht an das-Steuerelement senden. Die Meldung enthält die Adresse einer [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) -Struktur. Diese Struktur definiert die Eigenschaften des Header Elements, das eine Zeichenfolge, ein Bitmap-Bild, eine Anfangs Größe und einen Anwendungs definierten **LPARAM** -Wert enthalten kann.

Der **fmt** -Member der [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) -Struktur eines Elements kann entweder die **HDF- \_ Zeichenfolge** oder das **HDF- \_ Bitmap** -Flag enthalten, um anzugeben, ob das Steuerelement die Zeichenfolge oder die Bitmap des Elements anzeigt. Wenn Sie sowohl eine Zeichenfolge als auch eine Bitmap anzeigen möchten, erstellen Sie ein vom Besitzer gezeichnetes Element, indem Sie den **fmt** -Member so festlegen, dass er das **HDF-Besitzer \_ Zeichnungs** Flag einschließt. Die **HDITEM** -Struktur gibt auch formatierungsflags an, die dem Steuerelement mitteilen, ob die Zeichenfolge oder Bitmap zentriert, linksbündig oder rechtsbündig ausgerichtet werden soll.

[**HDM \_ InsertItem**](hdm-insertitem.md) gibt den Index des neu hinzugefügten Elements zurück. Sie können den Index in anderen Nachrichten verwenden, um Eigenschaften festzulegen oder Informationen über das Element abzurufen. Sie können ein Element mithilfe der [**HDM \_ DeleteItem**](hdm-deleteitem.md) -Nachricht löschen, indem Sie den Index des zu löschenden Elements angeben.

Sie können die [**HDM \_ SetItem**](hdm-setitem.md) -Nachricht verwenden, um die Eigenschaften eines vorhandenen Header Elements festzulegen, und die [**HDM \_ GetItem**](hdm-getitem.md) -Nachricht, um die aktuellen Eigenschaften eines Elements abzurufen. Um die Anzahl der Elemente in einem Header Steuerelement abzurufen, verwenden Sie die [**HDM \_ GetItemCount**](hdm-getitemcount.md) -Nachricht.

## <a name="owner-drawn-header-controls"></a>Owner-Drawn Header-Steuerelemente

Sie können einzelne Elemente eines Header Steuer Elements als vom Besitzer gezeichnete Elemente definieren. Wenn Sie diese Technik verwenden, erhalten Sie mehr Kontrolle, als Sie andernfalls über das Aussehen eines Header Elements verfügen würden.

Sie können die [**HDM \_ InsertItem**](hdm-insertitem.md) -Nachricht verwenden, um ein neues, vom Besitzer gezeichnetes Element in ein Header Steuerelement oder die [**HDM \_**](hdm-setitem.md) -Nachricht "-Nachricht" einzufügen, um ein vorhandenes Element in ein vom Besitzer gezeichnetes Element zu ändern Beide Meldungen enthalten die Adresse einer [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) -Struktur, für die das **fmt** -Element auf den **HDF-Besitzer \_ Zeichnen** -Wert festgelegt werden muss.

Wenn ein Header Steuerelement ein vom Besitzer gezeichnetes Element zeichnen muss, sendet es die [**WM \_ DrawItem**](wm-drawitem.md) -Nachricht an das übergeordnete Fenster. Der *wParam* -Parameter der Nachricht ist der Bezeichner des untergeordneten Fensters des Header Steuer Elements, und der *LPARAM* -Parameter ist eine Adresse einer [**drawitemstruct**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) -Struktur. Das übergeordnete Fenster verwendet die Informationen in der-Struktur, um das Element zu zeichnen. Für ein vom Besitzer gezeichnetes Element in einem Header Steuerelement enthält die **drawitemstruct** -Struktur die folgenden Informationen.



| Member         | BESCHREIBUNG                                                                                                                                            |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ctltype**    | [**ODT \_ Vom Header**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) Besitzer gezeichneter Steuer ungstyp.                                                                                        |
| **Ctlid**      | Bezeichner des übergeordneten Fensters des Header Steuer Elements.                                                                                                         |
| **Itemid**     | Der Index des Elements, das gezeichnet werden soll.                                                                                                                         |
| **Member itemaction** | [**ODA \_ Drawentire**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) Drawing-Action-Flag.                                                                                         |
| **itemState**  | [**ODS \_ Ausgewähltes**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) Zeichnungs-Action-Flag, wenn sich der Cursor auf dem Element befindet und die Maustaste gedrückt ist. Andernfalls ist dieser Member 0 (null). |
| **hwnditem**   | Handle für das Header Steuerelement.                                                                                                                          |
| **HDC**        | Handle für den Gerätekontext des Header Steuer Elements.                                                                                                    |
| **rcItem**     | Koordinaten des Header Elements, das gezeichnet werden soll. Die Koordinaten sind relativ zur linken oberen Ecke des Header Steuer Elements.                               |
| **ItemData**   | Der Anwendungs definierte 32-Bit-Wert, der dem Element zugeordnet ist.                                                                                             |



 

## <a name="header-control-filters"></a>Header Steuerelement Filter

Wenn Sie den [**HDS \_**](header-control-styles.md) -Filter leisten Fenster Stil für ein Header Steuerelement angeben, können Sie die Platzierung der Filter Bearbeitungsfelder unterhalb der Spaltenüberschriften aktivieren. Neben dem Bearbeitungsfeld wird eine Filter Schaltfläche angezeigt. Sie können die Filterung implementieren, indem Sie auf die Benachrichtigungs Codes [Hdn \_ beginfilteredit](hdn-beginfilteredit.md), [Hdn \_ endfilteredit](hdn-endfilteredit.md), [Hdn \_ filterbtnclick](hdn-filterbtnclick.md)oder [Hdn \_ FilterChange](hdn-filterchange.md) Antworten.

Standardmäßig enthält das Bearbeitungsfeld eine Eingabeaufforderung, in der der Benutzer Text eingeben kann. Sie können das Bearbeitungsfeld in diesem Standardzustand wiederherstellen, indem Sie den [**Header \_ ClearFilter**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearfilter) oder den [**Header \_ ClearAllFilters**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearallfilters)verwenden.

Im folgenden Codebeispiel wird gezeigt, wie das Header Steuerelement aus einem Listenansicht-Steuerelement abgerufen und eine Filter Leiste hinzugefügt wird.


```
// hList is the HWND of the list-view control.
HWND hHeader = ListView_GetHeader(hList);
LONG_PTR styles = GetWindowLongPtr(hHeader, GWL_STYLE);
SetWindowLongPtr(g_hHeader, GWL_STYLE, styles | HDS_FILTERBAR);
```



## <a name="default-header-control-message-processing"></a>Nachrichtenverarbeitung für Standard Header Steuerelemente

In diesem Abschnitt werden die Fenster Meldungen beschrieben, die von der Fenster Prozedur für die [**WC- \_ Header**](common-control-window-classes.md) Fenster Klasse behandelt werden.



| `Message`                                            | Verarbeitung wird ausgeführt                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ Erstellen**](/windows/desktop/winmsg/wm-create)                 | Initialisiert das Header Steuerelement.                                                                                                                                                                                                                                                                               |
| [**WM \_ zerstören**](/windows/desktop/winmsg/wm-destroy)               | Hebt die Initialisierung des Header Steuer Elements auf.                                                                                                                                                                                                                                                                             |
| [**WM- \_ erasebkgnd**](/windows/desktop/winmsg/wm-erasebkgnd)         | Füllt den Hintergrund des Header Steuer Elements mithilfe der aktuellen Hintergrundfarbe des Steuer Elements.                                                                                                                                                                                                                      |
| [**WM \_ getdlgcode**](/windows/desktop/dlgbox/wm-getdlgcode)         | Gibt eine Kombination der [**dlgc \_ wanttab**](/windows/desktop/dlgbox/wm-getdlgcode) -und [**dlgc- \_ wantpfeile**](/windows/desktop/dlgbox/wm-getdlgcode) -Werte zurück.                                                                                                                     |
| [**WM- \_ getFont**](/windows/desktop/winmsg/wm-getfont)               | Gibt das Handle für die aktuelle Schriftart zurück, die vom Header Steuerelement verwendet wird, um den Text zu zeichnen.                                                                                                                                                                                                                 |
| [**WM \_ lbuttondblclk**](/windows/desktop/inputdev/wm-lbuttondblclk) | Erfasst Maus Eingaben. Wenn sich der Mauszeiger auf einem unter Teiler befindet, sendet das Steuerelement den [Hdn \_ BeginTrack](hdn-begintrack.md) -Benachrichtigungs Code und beginnt mit dem Ziehen des unter Teilers. Wenn sich der Cursor auf einem Element befindet, wird das Element im gedrückten Zustand angezeigt.                                                            |
| [**WM \_ lbuttondown**](/windows/desktop/inputdev/wm-lbuttondown)     | Identisch mit der [**WM- \_ lbuttondblclk**](/windows/desktop/inputdev/wm-lbuttondblclk) -Meldung.                                                                                                                                                                                                                                       |
| [**WM- \_ lbuttonup**](/windows/desktop/inputdev/wm-lbuttonup)         | Gibt die Maus Aufzeichnung frei. Wenn das Steuerelement die Mausbewegung verfolgt, sendet es den [Hdn- \_ EndTrack](hdn-endtrack.md) -Benachrichtigungs Code und zeichnet das Header Steuerelement neu. Andernfalls sendet das Steuerelement den [Hdn \_ itemClick](hdn-itemclick.md) -Benachrichtigungs Code und zeichnet das Header Element, auf das geklickt wurde, neu. |
| [**WM- \_ mouseelmove**](/windows/desktop/inputdev/wm-mousemove)         | Wenn ein unter Teiler gezogen wird, sendet das Steuerelement den [Hdn \_ ](hdn-track.md) -Nachverfolgung-Benachrichtigungs Code und zeigt das Element an der neuen Position an. Wenn die linke Maustaste gedrückt ist und sich der Cursor auf einem Element befindet, wird das Element im gedrückten Zustand angezeigt.                                                      |
| [**WM- \_ nccreate**](/windows/desktop/winmsg/wm-nccreate)             | Ordnet eine interne Datenstruktur zu und initialisiert sie.                                                                                                                                                                                                                                                         |
| [**WM \_ ncdestroy**](/windows/desktop/winmsg/wm-ncdestroy)           | Gibt die Ressourcen frei, die vom Header-Steuerelement zugeordnet werden, nachdem das Header Steuerelement nicht initialisiert wurde.                                                                                                                                                                                                                |
| [**WM- \_ Paint**](/windows/desktop/gdi/wm-paint)                      | Zeichnet den ungültigen Bereich des Header Steuer Elements. Wenn der *wParam* -Parameter ungleich NULL ist, geht das Steuerelement davon aus, dass es sich bei dem Wert um einen HDC handelt und zeichnet sich durch den Gerätekontext aus.                                                                                                                                    |
| [**WM- \_ SetCursor**](/windows/desktop/menurc/wm-setcursor)           | Legt die Cursor Form fest, je nachdem, ob sich der Cursor auf einem unter Teiler oder in einem Header Element befindet.                                                                                                                                                                                                                   |
| [**WM- \_ setFont**](/windows/desktop/winmsg/wm-setfont)               | Wählt ein neues Schriftart Handle in den Gerätekontext für das Header Steuerelement aus.                                                                                                                                                                                                                                     |



 

 

 