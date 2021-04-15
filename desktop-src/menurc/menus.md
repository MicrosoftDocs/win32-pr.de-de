---
title: Menüs (Menüs und andere Ressourcen)
description: In diesem Abschnitt werden Menüs erläutert.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\menus.htm
keywords:
- Ressourcen, Menüs
- Menüs, Info
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c376aa1d2f55fa482ca7a2f98f57ae15236bf26b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391344"
---
# <a name="menus-menus-and-other-resources"></a>Menüs (Menüs und andere Ressourcen)

In diesem Abschnitt werden die Menüs beschrieben und erläutert, wie Sie verwendet werden.

### <a name="in-this-section"></a>In diesem Abschnitt



| Name                                 | BESCHREIBUNG                                                  |
|--------------------------------------|--------------------------------------------------------------|
| [Informationen zu Menüs](about-menus.md)       | Erläutert Menüs.<br/>                                  |
| [Verwenden von Menüs](using-menus.md)       | Stellt Codebeispiele für Aufgaben im Zusammenhang mit Menüs bereit.<br/> |
| [Menü Verweis](menu-reference.md) | Enthält die API-Referenz.<br/>                       |



 

### <a name="menu-functions"></a>Menüfunktionen



| Name                                                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua)                                 | Fügt ein neues Element am Ende der angegebenen Menüleiste, des Dropdown Menüs, des Untermenüs oder des Kontextmenüs an. Sie können diese Funktion verwenden, um den Inhalt, die Darstellung und das Verhalten des Menü Elements anzugeben. <br/>                                                                                                                                                                                                  |
| [**Checkmenuitem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuitem)                           | Legt den Zustand des Häkchen Attributs für das angegebene Menü Element auf "ausgewählt" oder "deaktiviert" fest.<br/>                                                                                                                                                                                                                                                                                                      |
| [**Checkmenuradioitem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem)                 | Überprüft ein angegebenes Menü Element und legt es als Radio Element fest. Gleichzeitig löscht die-Funktion alle anderen Menü Elemente in der zugeordneten Gruppe und löscht das Flag für das Radio-Element-Type für diese Elemente.<br/>                                                                                                                                                                                                    |
| [**"Kreatemdeu"**](/windows/desktop/api/Winuser/nf-winuser-createmenu)                                 | Erstellt ein Menü. Das Menü ist anfänglich leer, kann jedoch mithilfe der Funktionen [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema), [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua)und [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua) mit Menü Elementen gefüllt werden. <br/>                                                                                                                                                                        |
| [**CreatePopupMenu**](/windows/desktop/api/Winuser/nf-winuser-createpopupmenu)                       | Erstellt ein Dropdown Menü, ein Untermenü oder ein Kontextmenü. Das Menü ist anfänglich leer. Sie können Menü Elemente mithilfe der [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) -Funktion einfügen oder anfügen. Sie können auch die [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua) -Funktion verwenden, um Menü Elemente einzufügen, und die [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) -Funktion, um Menü Elemente anzufügen.<br/>                                                  |
| [**DeleteMenu**](/windows/desktop/api/Winuser/nf-winuser-deletemenu)                                 | Löscht ein Element aus dem angegebenen Menü. Wenn das Menü Element ein Menü oder ein Untermenü öffnet, zerstört diese Funktion das Handle im Menü oder Untermenü und gibt den vom Menü oder Untermenü verwendeten Arbeitsspeicher frei. <br/>                                                                                                                                                                                                     |
| [**DestroyMenu**](/windows/desktop/api/Winuser/nf-winuser-destroymenu)                               | Zerstört das angegebene Menü und gibt den Arbeitsspeicher frei, den das Menü einnimmt. <br/>                                                                                                                                                                                                                                                                                                                          |
| [**DrawMenuBar**](/windows/desktop/api/Winuser/nf-winuser-drawmenubar)                               | Zeichnet die Menüleiste des angegebenen Fensters neu. Wenn die Menüleiste geändert wird, nachdem das System das Fenster erstellt hat, muss diese Funktion aufgerufen werden, um die geänderte Menüleiste zu zeichnen. <br/>                                                                                                                                                                                                                         |
| [**EnableMenuItem**](/windows/desktop/api/Winuser/nf-winuser-enablemenuitem)                         | Aktiviert, deaktiviert oder deaktiviert das angegebene Menü Element. <br/>                                                                                                                                                                                                                                                                                                                                              |
| [**Endmenü**](/windows/desktop/api/Winuser/nf-winuser-endmenu)                                       | Beendet das aktive Menü des aufrufenden Threads.<br/>                                                                                                                                                                                                                                                                                                                                                             |
| [**GetMenu**](/windows/desktop/api/Winuser/nf-winuser-getmenu)                                       | Ruft ein Handle für das Menü ab, das dem angegebenen Fenster zugewiesen ist. <br/>                                                                                                                                                                                                                                                                                                                                  |
| [**GetMenuBarInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenubarinfo)                         | Ruft Informationen zur angegebenen Menüleiste ab.<br/>                                                                                                                                                                                                                                                                                                                                                |
| [**Getmenucheckmarkdimensions**](/windows/desktop/api/Winuser/nf-winuser-getmenucheckmarkdimensions) | Ruft die Dimensionen der Standard Bitmap für das Häkchen ab. Das System zeigt diese Bitmap neben den ausgewählten Menü Elementen an. Vor dem Aufrufen der [**setmenuitembitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) -Funktion zum Ersetzen der Standard Bitmap für das Häkchen für ein Menü Element muss eine Anwendung die richtige Bitmapgröße durch Aufrufen von [**getmenucheckmarkdimensions**](/windows/desktop/api/Winuser/nf-winuser-getmenucheckmarkdimensions)bestimmen. <br/> |
| [**Getmenudefaultitem**](/windows/desktop/api/Winuser/nf-winuser-getmenudefaultitem)                 | Bestimmt das Standardmenü Element im angegebenen Menü.<br/>                                                                                                                                                                                                                                                                                                                                            |
| [**Getmenuinfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuinfo)                               | Ruft Informationen zu einem angegebenen Menü ab.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| [**Getmenuitemcount**](/windows/desktop/api/Winuser/nf-winuser-getmenuitemcount)                     | Ruft die Anzahl der Elemente im angegebenen Menü ab. <br/>                                                                                                                                                                                                                                                                                                                                              |
| [**Getmenuitemid**](/windows/desktop/api/Winuser/nf-winuser-getmenuitemid)                           | Ruft den Menü Element Bezeichner eines Menü Elements ab, das sich an der angegebenen Position in einem Menü befindet. <br/>                                                                                                                                                                                                                                                                                                    |
| [**Getmenuiteminfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa)                       | Ruft Informationen zu einem Menü Element ab.<br/>                                                                                                                                                                                                                                                                                                                                                           |
| [**Getmenuitemrect**](/windows/desktop/api/Winuser/nf-winuser-getmenuitemrect)                       | Ruft das umgebende Rechteck für das angegebene Menü Element ab.<br/>                                                                                                                                                                                                                                                                                                                                      |
| [**Getmenustate**](/windows/desktop/api/Winuser/nf-winuser-getmenustate)                             | Ruft die menüflags ab, die dem angegebenen Menü Element zugeordnet sind. Wenn das Menü Element ein Untermenü öffnet, gibt diese Funktion auch die Anzahl der Elemente im Untermenü zurück. <br/>                                                                                                                                                                                                                                |
| [**GetMenuString**](/windows/desktop/api/Winuser/nf-winuser-getmenustringa)                           | Kopiert die Text Zeichenfolge des angegebenen Menü Elements in den angegebenen Puffer. <br/>                                                                                                                                                                                                                                                                                                                      |
| [**Getsubmenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu)                                 | Ruft ein Handle für das Dropdown Menü oder Untermenü ab, das durch das angegebene Menü Element aktiviert ist. <br/>                                                                                                                                                                                                                                                                                                         |
| [**Getsystemmenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu)                           | Ermöglicht der Anwendung den Zugriff auf das Menü Fenster (auch als Systemmenü oder Menüsteuerung bezeichnet) zum Kopieren und ändern. <br/>                                                                                                                                                                                                                                                                  |
| [**Hilitemenuitem**](/windows/desktop/api/Winuser/nf-winuser-hilitemenuitem)                         | Hebt die Hervorhebung aus einem Element in einer Menüleiste hervor oder entfernt Sie. <br/>                                                                                                                                                                                                                                                                                                                                |
| [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema)                         | Fügt ein neues Menü Element an der angegebenen Position in einem Menü ein.<br/>                                                                                                                                                                                                                                                                                                                                       |
| [**IsMenu**](/windows/desktop/api/Winuser/nf-winuser-ismenu)                                         | Bestimmt, ob ein Handle ein Menü Handle ist. <br/>                                                                                                                                                                                                                                                                                                                                                     |
| [**Loadmenu**](/windows/desktop/api/Winuser/nf-winuser-loadmenua)                                     | Lädt die angegebene Menü Ressource aus der ausführbaren Datei (. exe), die einer Anwendungs Instanz zugeordnet ist. <br/>                                                                                                                                                                                                                                                                                        |
| [**Loadmenuindirekte**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta)                     | Lädt die angegebene Menüvorlage in den Arbeitsspeicher. <br/>                                                                                                                                                                                                                                                                                                                                                      |
| [**Menuitemfrompoint**](/windows/desktop/api/Winuser/nf-winuser-menuitemfrompoint)                   | Bestimmt, welches Menü Element ggf. an der angegebenen Position liegt.<br/>                                                                                                                                                                                                                                                                                                                                  |
| [**Modifymenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua)                                 | Ändert ein vorhandenes Menü Element. Diese Funktion wird verwendet, um den Inhalt, die Darstellung und das Verhalten des Menü Elements anzugeben. <br/>                                                                                                                                                                                                                                                                           |
| [**Removemenu**](/windows/desktop/api/Winuser/nf-winuser-removemenu)                                 | Löscht ein Menü Element oder trennt ein Untermenü aus dem angegebenen Menü. Wenn das Menü Element ein Dropdown Menü oder ein Untermenü öffnet, zerstört [**removemenu**](/windows/desktop/api/Winuser/nf-winuser-removemenu) das Menü oder dessen Handle nicht, sodass das Menü wieder verwendet werden kann. Bevor diese Funktion aufgerufen wird, sollte die [**getsubmenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu) -Funktion ein Handle für das Dropdown Menü oder das Untermenü abrufen. <br/>                         |
| [**SetMenu**](/windows/desktop/api/Winuser/nf-winuser-setmenu)                                       | Weist dem angegebenen Fenster ein neues Menü zu. <br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**Setmenudefaultitem**](/windows/desktop/api/Winuser/nf-winuser-setmenudefaultitem)                 | Legt das Standardmenü Element für das angegebene Menü fest.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| [**Setmenuinfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo)                               | Legt Informationen für ein angegebenes Menü fest.<br/>                                                                                                                                                                                                                                                                                                                                                             |
| [**Setmenuitembitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps)                 | Ordnet die angegebene Bitmap einem Menü Element zu. Unabhängig davon, ob das Menü Element aktiviert oder deaktiviert ist, zeigt das System die entsprechende Bitmap neben dem Menü Element an. <br/>                                                                                                                                                                                                                                   |
| [**Setmenuiteminfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa)                       | Ändert Informationen zu einem Menü Element.<br/>                                                                                                                                                                                                                                                                                                                                                             |
| [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu)                         | Zeigt ein Kontextmenü an der angegebenen Position an und verfolgt die Auswahl der Elemente im Menü. Das Kontextmenü kann an beliebiger Stelle auf dem Bildschirm angezeigt werden.<br/>                                                                                                                                                                                                                                             |
| [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex)                     | Zeigt ein Kontextmenü an der angegebenen Position an und verfolgt die Auswahl von Elementen im Kontextmenü. Das Kontextmenü kann an beliebiger Stelle auf dem Bildschirm angezeigt werden.<br/>                                                                                                                                                                                                                                    |



 

Die folgende Funktion ist veraltet.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Name</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-insertmenua"><strong>InsertMenu</strong></a></td>
<td>Fügt ein neues Menü Element in ein Menü ein und verschiebt andere Elemente im Menü.
<blockquote>
[!Note]<br />
Die <a href="/windows/desktop/api/Winuser/nf-winuser-insertmenua"><strong>InsertMenu</strong></a> -Funktion wurde durch die <a href="/windows/desktop/api/Winuser/nf-winuser-insertmenuitema"><strong>InsertMenuItem</strong></a> -Funktion abgelöst. Sie können jedoch immer noch <strong>InsertMenu</strong>verwenden, wenn Sie keine der erweiterten Features von <strong>InsertMenuItem</strong>benötigen.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="menu-notifications"></a>Menü Benachrichtigungen



| Name                                                  | BESCHREIBUNG                                                                                                                                                                          |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM- \_ Befehl**](wm-command.md)                     | Wird gesendet, wenn der Benutzer ein Befehls Element aus einem Menü auswählt, wenn ein Steuerelement eine Benachrichtigungs Meldung an das übergeordnete Fenster sendet oder wenn eine Tastenkombination für die Zugriffstaste übersetzt wird. <br/> |
| [**WM- \_ ContextMenu**](wm-contextmenu.md)             | Benachrichtigt ein Fenster, dass der Benutzer im Fenster auf die Rechte Maustaste geklickt hat (mit der *rechten Maustaste geklickt* hat).<br/>                                                                            |
| [**WM- \_ entermenuloop**](wm-entermenuloop.md)         | Informiert die Hauptfenster Prozedur einer Anwendung, dass eine Menü modale Schleife eingegeben wurde. <br/>                                                                                  |
| [**WM- \_ exitmenuloop**](wm-exitmenuloop.md)           | Teilt der Hauptfenster Prozedur einer Anwendung mit, dass eine modale Menü Schleife beendet wurde. <br/>                                                                                   |
| [**WM \_ gettitlebarinfoex**](wm-gettitlebarinfoex.md) | Wird gesendet, um erweiterte Titelleisten Informationen anzufordern. Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.<br/>                                  |
| [**WM ( \_ MenuCommand)**](wm-menucommand.md)             | Wird gesendet, wenn der Benutzer eine Auswahl aus einem Menü trifft. <br/>                                                                                                                        |
| [**WM- \_ menudrag**](wm-menudrag.md)                   | Wird an den Besitzer eines Drag & Drop-Menüs gesendet, wenn der Benutzer ein Menü Element zieht. <br/>                                                                                               |
| [**WM \_ menugetobject**](wm-menugetobject.md)         | Wird an den Besitzer eines Drag & Drop-Menüs gesendet, wenn der Maus Cursor in ein Menü Element oder von der Mitte des Elements zum oberen oder unteren Rand des Elements bewegt wird. <br/>                |
| [**WM- \_ menurbuttonup**](wm-menurbuttonup.md)         | Wird gesendet, wenn der Benutzer die Rechte Maustaste loslässt, während sich der Cursor auf einem Menü Element befindet. <br/>                                                                                   |
| [**WM- \_ nextmenu**](wm-nextmenu.md)                   | Wird an eine Anwendung gesendet, wenn mit der nach-rechts-oder der nach-links-Taste zwischen der Menüleiste und dem Systemmenü gewechselt wird. <br/>                                                      |
| [**WM- \_ uninitmenupopup**](wm-uninitmenupopup.md)     | Wird gesendet, wenn ein Dropdown Menü oder ein Untermenü zerstört wurde. <br/>                                                                                                                |



 

### <a name="menu-structures"></a>Menüstrukturen



| Name                                                       | BESCHREIBUNG                                                                                                                                                     |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Mdinextmenu**](/windows/win32/api/winuser/ns-winuser-mdinextmenu)                         | Enthält Informationen über das Menü, das aktiviert werden soll. <br/>                                                                                                |
| [**Menubarinfo**](/windows/win32/api/winuser/ns-winuser-menubarinfo)                         | Enthält Informationen zur Menüleiste.<br/>                                                                                                                       |
| [**menuex- \_ Vorlagen \_ Header**](menuex-template-header.md) | Definiert den Header für eine erweiterte Menüvorlage. Diese Struktur Definition dient lediglich der Erläuterung. Es ist in keiner Standard Header Datei vorhanden. <br/> |
| [**menuex- \_ Vorlagen \_ Element**](menuex-template-item.md)     | Definiert ein Menü Element in einer erweiterten Menüvorlage. Diese Struktur Definition dient lediglich der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.<br/>  |
| [**Menugetobjectinfo**](/windows/win32/api/winuser/ns-winuser-menugetobjectinfo)             | Enthält Informationen über das Menü, in dem sich der Mauszeiger befindet.<br/>                                                                                     |
| [**Menuinfo**](/windows/win32/api/winuser/ns-winuser-menuinfo)                               | Enthält Informationen zu einem Menü.<br/>                                                                                                                   |
| [**Menuiteminfo zuordnet**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)                       | Enthält Informationen zu einem Menü Element. <br/>                                                                                                             |
| [**Menuitemtemplate**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate)               | Definiert ein Menü Element in einer Menüvorlage. <br/>                                                                                                             |
| [**Menuitemtemplateheader**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader)   | Definiert den Header für eine Menüvorlage. Eine komplette Menüvorlage besteht aus einer Kopfzeile und einer oder mehreren Menü Element Listen. <br/>                              |
| [**Tpmparametriams**](/windows/win32/api/winuser/ns-winuser-tpmparams)                             | Enthält erweiterte Parameter für die [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) -Funktion.<br/>                                                          |



 

 

