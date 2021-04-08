---
title: Symbolleiste
description: Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die mit Symbolleisten-Steuerelementen verwendet werden.
ms.assetid: vs|controls|~\controls\toolbar\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e0cadd2eb1560d3486073810e86a143b7fccca5
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "103732096"
---
# <a name="toolbar"></a>Symbolleiste

Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die mit Symbolleisten-Steuerelementen verwendet werden.

### <a name="overviews"></a>Übersichten



| Thema                                                   | Inhalte                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Info](toolbar-controls-overview.md) | Eine Symbolleiste ist ein Steuerelement, das eine oder mehrere Schaltflächen enthält. Jede Schaltfläche, wenn ein Benutzer darauf klickt, sendet eine Befehls Meldung an das übergeordnete Fenster. Die Schaltflächen in einer Symbolleiste entsprechen in der Regel Elementen im Menü der Anwendung und bieten dem Benutzer eine zusätzliche und direktere Möglichkeit zum Zugriff auf die Befehle einer Anwendung.<br/> |
| [Verwenden von Symbolleisten](using-toolbar-controls.md)    | Dieses Thema enthält Implementierungsdetails und Beispielcode für die Verwendung von Symbolleisten-Steuerelementen in Ihren Anwendungen.<br/>                                                                                                                                                                                                                  |



 

### <a name="functions"></a>Functions



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Thema</th>
<th>Inhalte</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-createmappedbitmap"><strong>"Kreatemappedbitmap"</strong></a></td>
<td>Erstellt eine Bitmap für die Verwendung in einer Symbolleiste. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex"><strong>"Kreatetoolbarex"</strong></a></td>
<td>Erstellt ein Symbolleisten Fenster und fügt die angegebenen Schaltflächen der Symbolleiste hinzu.
<blockquote>
[!Note]<br />
Diese Funktion ist veraltet, da Sie nicht alle Funktionen von Symbolleisten unterstützt. Verwenden Sie stattdessen " <a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa"><strong>kreatewindowex</strong></a> ". Beispiele finden Sie unter <a href="using-toolbar-controls.md">Verwenden von Symbol</a>leisten-Steuerelementen.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="messages"></a>Meldungen



| Thema                                                         | Inhalte                                                                                                                                                                                                |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TB \_ AddBitmap**](tb-addbitmap.md)                         | Fügt der Liste der für eine Symbolleiste verfügbaren Schaltflächen Bilder mindestens ein Bild hinzu. <br/>                                                                                                               |
| [**TB ( \_ AddButtons)**](tb-addbuttons.md)                       | Fügt einer Symbolleiste eine oder mehrere Schaltflächen hinzu.<br/>                                                                                                                                                       |
| [**TB \_ AddString**](tb-addstring.md)                         | Fügt eine neue Zeichenfolge zum Zeichen folgen Pool der Symbolleiste hinzu.<br/>                                                                                                                                              |
| [**TB \_ AutoSize**](tb-autosize.md)                           | Bewirkt, dass die Größe einer Symbolleiste geändert wird. <br/>                                                                                                                                                             |
| [**TB- \_ ButtonCount**](tb-buttoncount.md)                     | Ruft die Anzahl der Schaltflächen auf der Symbolleiste ab. <br/>                                                                                                                                  |
| [**TB \_ buttonstructsize**](tb-buttonstructsize.md)           | Gibt die Größe der [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) -Struktur an. <br/>                                                                                                                           |
| [**TB \_ changebitmap**](tb-changebitmap.md)                   | Ändert die Bitmap für eine Schaltfläche in einer Symbolleiste.<br/>                                                                                                                                                |
| [**TB \_ checkbutton**](tb-checkbutton.md)                     | Überprüft oder überprüft eine angegebene Schaltfläche in einer Symbolleiste.<br/>                                                                                                                                              |
| [**TB \_ commandto Index**](tb-commandtoindex.md)               | Ruft den NULL basierten Index für die Schaltfläche ab, die dem angegebenen Befehls Bezeichner zugeordnet ist. <br/>                                                                                             |
| [**TB \_ Anpassen**](tb-customize.md)                         | Zeigt das Dialogfeld **Symbolleiste anpassen** an.<br/>                                                                                                                                               |
| [**TB \_ DeleteButton**](tb-deletebutton.md)                   | Löscht eine Schaltfläche auf der Symbolleiste. <br/>                                                                                                                                                          |
| [**TB ( \_ enablebutton)**](tb-enablebutton.md)                   | Aktiviert oder deaktiviert die angegebene Schaltfläche in einer Symbolleiste.<br/>                                                                                                                                       |
| [**TB \_ getanchorhervor Hebung**](tb-getanchorhighlight.md)       | Ruft die Anker Hervorhebungs Einstellung für eine Symbolleiste ab. <br/>                                                                                                                                       |
| [**TB \_ getbitmap**](tb-getbitmap.md)                         | Ruft den Index der Bitmap ab, die einer Schaltfläche in einer Symbolleiste zugeordnet ist. <br/>                                                                                                                    |
| [**TB \_ getbitmapflags**](tb-getbitmapflags.md)               | Ruft die Flags ab, die den Typ der zu verwendenden Bitmap beschreiben.<br/>                                                                                                                             |
| [**TB \_ getbutton**](tb-getbutton.md)                         | Ruft Informationen über die angegebene Schaltfläche in einer Symbolleiste ab.<br/>                                                                                                                               |
| [**TB \_ getbuttoninfo**](tb-getbuttoninfo.md)                 | Ruft erweiterte Informationen für eine Schaltfläche in einer Symbolleiste ab. <br/>                                                                                                                                   |
| [**TB \_ getbuttonsize**](tb-getbuttonsize.md)                 | Ruft die aktuelle Breite und Höhe von Symbolleisten Schaltflächen in Pixel ab. <br/>                                                                                                                       |
| [**TB \_ getbuttontext**](tb-getbuttontext.md)                 | Ruft den Anzeige Text einer Schaltfläche auf einer Symbolleiste ab.<br/>                                                                                                                                         |
| [**TB \_ getcolorscheme**](tb-getcolorscheme.md)               | Ruft die Farbschema Informationen aus dem Symbolleisten-Steuerelement ab. <br/>                                                                                                                            |
| [**TB \_ getdisabledimagelist**](tb-getdisabledimagelist.md)   | Ruft die Bildliste ab, die ein ToolBar-Steuerelement verwendet, um inaktive Schaltflächen anzuzeigen. <br/>                                                                                                           |
| [**TB \_ getextendecodstyle**](tb-getextendedstyle.md)           | Ruft die erweiterten Stile für ein Symbolleisten-Steuerelement ab. <br/>                                                                                                                                        |
| [**TB \_ gethotimagelist**](tb-gethotimagelist.md)             | Ruft die Bildliste ab, die ein ToolBar-Steuerelement verwendet, um Hot-Schaltflächen anzuzeigen.<br/>                                                                                                                 |
| [**TB \_ gethotitem**](tb-gethotitem.md)                       | Ruft den Index des aktiven Elements auf einer Symbolleiste ab. <br/>                                                                                                                                           |
| [**TB \_ getidealsize**](tb-getidealsize.md)                   | Ruft die ideale Größe der Symbolleiste ab.<br/>                                                                                                                                                          |
| [**TB \_ GetImageList**](tb-getimagelist.md)                   | Ruft die Bildliste ab, die ein ToolBar-Steuerelement verwendet, um Schaltflächen im Standardzustand anzuzeigen. Ein Symbolleisten-Steuerelement verwendet diese Bildliste zum Anzeigen von Schaltflächen, wenn diese nicht heiß oder deaktiviert sind.<br/> |
| [**TB \_ getimagelistcount**](tb-getimagelistcount.md)         | Ruft die Anzahl der Bildlisten ab, die der Symbolleiste zugeordnet sind.<br/>                                                                                                                                  |
| [**TB \_ getinsertmark**](tb-getinsertmark.md)                 | Ruft die aktuelle Einfügemarke für die Symbolleiste ab. <br/>                                                                                                                                       |
| [**TB \_ getinsertmarkcolor**](tb-getinsertmarkcolor.md)       | Ruft die Farbe ab, die zum Zeichnen der Einfügemarke für die Symbolleiste verwendet wird. <br/>                                                                                                                        |
| [**TB \_ getitemdropdownrect**](tb-getitemdropdownrect.md)     | Ruft das umgebende Rechteck des Dropdown Fensters für ein Symbolleisten Element mit der [**btns- \_ Dropdown**](toolbar-control-and-button-styles.md)Liste für den Stil ab.<br/>                                  |
| [**TB \_ GetItemRect**](tb-getitemrect.md)                     | Ruft das umgebende Rechteck einer Schaltfläche in einer Symbolleiste ab. <br/>                                                                                                                                  |
| [**TB \_ getmaxsize**](tb-getmaxsize.md)                       | Ruft die Gesamtgröße aller sichtbaren Schaltflächen und Trennzeichen auf der Symbolleiste ab. <br/>                                                                                                       |
| [**TB \_ getmetrics**](tb-getmetrics.md)                       | Ruft die Metriken eines Symbolleisten-Steuer Elements ab.<br/>                                                                                                                                                  |
| [**TB- \_ GetObject**](tb-getobject.md)                         | Ruft das [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) -Element für ein ToolBar-Steuerelement ab. <br/>                                                                                                                     |
| [**TB \_ getpadding**](tb-getpadding.md)                       | Ruft die Auffüll Zeichen für ein Symbolleisten-Steuerelement ab. <br/>                                                                                                                                                |
| [**TB \_ getpressedimagelist**](tb-getpressedimagelist.md)     | Ruft die Bildliste ab, die ein ToolBar-Steuerelement verwendet, um Schaltflächen in einem gedrückten Zustand anzuzeigen.<br/>                                                                                                       |
| [**TB \_ GetRect**](tb-getrect.md)                             | Ruft das umgebende Rechteck für eine angegebene Symbolleisten Schaltfläche ab. <br/>                                                                                                                            |
| [**TB- \_ GetRows**](tb-getrows.md)                             | Ruft die Anzahl der Zeilen von Schaltflächen in einer Symbolleiste mit dem [**tbstyle- \_ wrapable**](toolbar-control-and-button-styles.md) -Stil ab. <br/>                                        |
| [**TB \_ GetState**](tb-getstate.md)                           | Ruft Informationen zum Zustand der angegebenen Schaltfläche in einer Symbolleiste ab, z. b. ob Sie aktiviert, gedrückt oder aktiviert ist. <br/>                                                             |
| [**TB \_ GetString**](tb-getstring.md)                         | Ruft eine Zeichenfolge aus dem Zeichen folgen Pool einer Symbolleiste ab.<br/>                                                                                                                                             |
| [**TB \_ GetStyle**](tb-getstyle.md)                           | Ruft die Formate ab, die derzeit für ein ToolBar-Steuerelement verwendet werden. <br/>                                                                                                                                |
| [**TB \_ gettextrows**](tb-gettextrows.md)                     | Ruft die maximale Anzahl von Textzeilen ab, die auf einer Symbolleisten Schaltfläche angezeigt werden können. <br/>                                                                                                        |
| [**TB \_ gettooltips**](tb-gettooltips.md)                     | Ruft das Handle für das QuickInfo-Steuerelement ab, das der Symbolleiste zugeordnet ist. <br/>                                                                                                           |
| [**TB \_ getunicodeformat**](tb-getunicodeformat.md)           | Ruft das Unicode-Zeichenformat Flag für das-Steuerelement ab. <br/>                                                                                                                                |
| [**TB- \_ Hash Beschleunigung**](tb-hasaccelerator.md)               | **Zur internen Verwendung vorgesehen. wird nicht für die Verwendung in Anwendungen empfohlen.**<br/> Ruft die Anzahl der Symbolleisten Schaltflächen ab, die über das angegebene Zugriffstasten Zeichen verfügen. <br/>                      |
| [**TB ( \_ hidebutton)**](tb-hidebutton.md)                       | Blendet die angegebene Schaltfläche in einer Symbolleiste ein oder aus.<br/>                                                                                                                                            |
| [**TB- \_ HitTest**](tb-hittest.md)                             | Bestimmt, wo sich ein Punkt in einem ToolBar-Steuerelement befindet. <br/>                                                                                                                                         |
| [**TB \_ unbestimmt**](tb-indeterminate.md)                 | Legt den unbestimmten Zustand der angegebenen Schaltfläche in einer Symbolleiste fest oder löscht ihn.<br/>                                                                                                                 |
| [**TB ( \_ InsertButton)**](tb-insertbutton.md)                   | Fügt eine Schaltfläche in eine Symbolleiste ein.<br/>                                                                                                                                                               |
| [**TB \_ insertmarkhittest**](tb-insertmarkhittest.md)         | Ruft die einfügemarkierungsinformationen für einen Punkt in einer Symbolleiste ab. <br/>                                                                                                                          |
| [**TB ( \_ isbuttoncheck)**](tb-isbuttonchecked.md)             | Bestimmt, ob die angegebene Schaltfläche in einer Symbolleiste aktiviert ist. <br/>                                                                                                                            |
| [**TB \_ isbuttonaktivierte**](tb-isbuttonenabled.md)             | Bestimmt, ob die angegebene Schaltfläche in einer Symbolleiste aktiviert ist. <br/>                                                                                                                            |
| [**TB \_ isbuttonhidden**](tb-isbuttonhidden.md)               | Bestimmt, ob die angegebene Schaltfläche in einer Symbolleiste ausgeblendet ist. <br/>                                                                                                                             |
| [**TB \_ isbuttonhervor gehoben**](tb-isbuttonhighlighted.md)     | Überprüft den Hervorhebungs Zustand einer Symbolleisten-Schaltfläche. <br/>                                                                                                                                             |
| [**TB \_ isbuttonindeend**](tb-isbuttonindeterminate.md) | Bestimmt, ob die angegebene Schaltfläche in einer Symbolleiste unbestimmt ist. <br/>                                                                                                                      |
| [**TB \_ isbuttonpressed**](tb-isbuttonpressed.md)             | Bestimmt, ob die angegebene Schaltfläche in einer Symbolleiste gedrückt ist. <br/>                                                                                                                            |
| [**TB- \_ loadimages**](tb-loadimages.md)                       | Lädt System definierte Schaltflächen Bilder in die Bildliste eines Symbolleisten-Steuer Elements.<br/>                                                                                                                      |
| [**TB \_ mapaccelerator**](tb-mapaccelerator.md)               | Bestimmt die ID der Schaltfläche, die dem angegebenen Zugriffstasten Zeichen entspricht.<br/>                                                                                                     |
| [**TB \_ markbutton**](tb-markbutton.md)                       | Legt den Hervorhebungs Zustand einer angegebenen Schaltfläche in einem Symbolleisten-Steuerelement fest.<br/>                                                                                                                             |
| [**TB- \_ Schaltfläche**](tb-movebutton.md)                       | Verschiebt eine Schaltfläche von einem Index zu einem anderen. <br/>                                                                                                                                                   |
| [**TB ( \_ Drucktaste)**](tb-pressbutton.md)                     | Drückt die angegebene Schaltfläche in einer Symbolleiste oder gibt diese frei.<br/>                                                                                                                                       |
| [**TB \_ replacebitmap**](tb-replacebitmap.md)                 | Ersetzt eine vorhandene Bitmap durch eine neue Bitmap.<br/>                                                                                                                                               |
| [**TB \_ saverestore**](tb-saverestore.md)                     | Senden Sie diese Nachricht, um das Speichern oder Wiederherstellen eines Symbolleisten Zustands zu initiieren.<br/>                                                                                                                           |
| [**TB \_**](tb-setanchorhighlight.md)       | Legt die Anker Hervorhebungs Einstellung für eine Symbolleiste fest. <br/>                                                                                                                                            |
| [**TB \_ setbitmapsize**](tb-setbitmapsize.md)                 | Legt die Größe der bitzugeordneten Bilder fest, die einer Symbolleiste hinzugefügt werden sollen. <br/>                                                                                                                             |
| [**TB \_ setboundingsize**](tb-setboundingsize.md)             | **Zur internen Verwendung vorgesehen. wird nicht für die Verwendung in Anwendungen empfohlen.**<br/> Legt die Begrenzungs Größe für ein mehrspaltige Symbolleisten-Steuerelement fest. <br/>                                               |
| [**TB \_ SetButtonInfo**](tb-setbuttoninfo.md)                 | Legt die Informationen für eine vorhandene Schaltfläche in einer Symbolleiste fest.<br/>                                                                                                                                    |
| [**TB \_ setbuttonsize**](tb-setbuttonsize.md)                 | Legt die Größe der Schaltflächen auf einer Symbolleiste fest.<br/>                                                                                                                                                       |
| [**TB \_ setbuttonwidth**](tb-setbuttonwidth.md)               | Legt die minimale und maximale Schaltflächen breite im Symbolleisten-Steuerelement fest.<br/>                                                                                                                           |
| [**TB \_ setcmdid**](tb-setcmdid.md)                           | Legt den Befehls Bezeichner einer Symbolleisten Schaltfläche fest. <br/>                                                                                                                                            |
| [**TB \_ SetColorScheme**](tb-setcolorscheme.md)               | Legt die Farbschema Informationen für das Symbolleisten-Steuerelement fest. <br/>                                                                                                                                  |
| [**TB \_ SetDisabledImageList**](tb-setdisabledimagelist.md)   | Legt die Bildliste fest, die das Symbolleisten-Steuerelement zum Anzeigen deaktivierter Schaltflächen verwendet. <br/>                                                                                                          |
| [**TB \_ setdrawtextflags**](tb-setdrawtextflags.md)           | Legt die textzeichenflags für die Symbolleiste fest. <br/>                                                                                                                                                |
| [**TB/ \_ textendecodstyle**](tb-setextendedstyle.md)           | Legt die erweiterten Stile für ein Symbolleisten-Steuerelement fest. <br/>                                                                                                                                             |
| [**TB \_ SetHotImageList**](tb-sethotimagelist.md)             | Legt die Bildliste fest, die das Symbolleisten-Steuerelement zum Anzeigen von Hot-Schaltflächen verwendet.<br/>                                                                                                                |
| [**TB \_**](tb-sethotitem.md)                       | Legt das heiße Element in einer Symbolleiste fest.<br/>                                                                                                                                                              |
| [**TB \_ SETHOTITEM2**](tb-sethotitem2.md)                     | Legt das heiße Element in einer Symbolleiste fest.<br/>                                                                                                                                                              |
| [**TB \_ SetImageList**](tb-setimagelist.md)                   | Legt die Bildliste fest, die die Symbolleiste zum Anzeigen von Schaltflächen verwendet, die sich in Ihrem Standardzustand befinden.<br/>                                                                                                |
| [**TB- \_ Einzug**](tb-setindent.md)                         | Legt den Einzug für die erste Schaltfläche in einem Symbolleisten-Steuerelement fest. <br/>                                                                                                                             |
| [**TB- \_ Einfügemarke**](tb-setinsertmark.md)                 | Legt die aktuelle Einfügemarke für die Symbolleiste fest. <br/>                                                                                                                                            |
| [**TB-Wert für " \_ tmarksertmarkcolor"**](tb-setinsertmarkcolor.md)       | Legt die Farbe fest, mit der die Einfügemarke für die Symbolleiste gezeichnet wird. <br/>                                                                                                                             |
| [**TB \_ setlistgap**](tb-setlistgap.md)                       | Legt den Abstand zwischen den Symbolleisten-Schaltflächen auf einer bestimmten Symbolleiste fest.<br/>                                                                                                                         |
| [**TB \_ setmaxtextrows**](tb-setmaxtextrows.md)               | Legt die maximale Anzahl der auf einer Symbolleisten Schaltfläche angezeigten Textzeilen fest. <br/>                                                                                                                         |
| [**TB \_ setmetrics**](tb-setmetrics.md)                       | Legt die Metriken eines Symbolleisten-Steuer Elements fest.<br/>                                                                                                                                                       |
| [**TB- \_ setPadding**](tb-setpadding.md)                       | Legt die Auffüll Zeichen für ein Symbolleisten-Steuerelement fest.<br/>                                                                                                                                                      |
| [**TB \_ SetParent**](tb-setparent.md)                         | Legt das Fenster fest, in das das Symbolleisten-Steuerelement Benachrichtigungs Codes sendet. <br/>                                                                                                                      |
| [**TB \_ setpressedimagelist**](tb-setpressedimagelist.md)     | Legt die Bildliste fest, die von der Symbolleiste zum Anzeigen von Schaltflächen mit gedrücktem Zustand verwendet wird.<br/>                                                                                                    |
| [**TB- \_ Sekunden**](tb-setrows.md)                             | Legt die Anzahl der Zeilen von Schaltflächen in einer Symbolleiste fest.<br/>                                                                                                                                             |
| [**TB \_ SetState**](tb-setstate.md)                           | Legt den Zustand für die angegebene Schaltfläche in einer Symbolleiste fest.<br/>                                                                                                                                        |
| [**TB- \_ SetStyle**](tb-setstyle.md)                           | Legt den Stil für ein Symbolleisten-Steuerelement fest. <br/>                                                                                                                                                       |
| [**TB \_ SetToolTips**](tb-settooltips.md)                     | Verknüpft ein QuickInfo-Steuerelement mit einer Symbolleiste. <br/>                                                                                                                                                |
| [**TB-- \_ Code Format**](tb-setunicodeformat.md)           | Legt das Unicode-Zeichenformat Flag für das-Steuerelement fest. Mit dieser Meldung können Sie den Zeichensatz ändern, der vom Steuerelement zur Laufzeit verwendet wird, anstatt das Steuerelement neu erstellen zu müssen. <br/>    |
| [**TB \_ SetWindowTheme**](tb-setwindowtheme.md)               | Legt den visuellen Stil eines Symbolleisten-Steuer Elements fest.<br/>                                                                                                                                                  |
| [**TB \_ TranslateAccelerator**](tb-translateaccelerator.md)   | Übergibt eine Tastatur Meldung an die Symbolleiste.<br/>                                                                                                                                                    |



 

### <a name="notifications"></a>Benachrichtigungen



| Thema                                                            | Inhalte                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ char (Symbolleiste)](nm-char-toolbar.md)                        | Wird von der Symbolleiste gesendet, wenn eine " [**WM \_ char**](/windows/desktop/inputdev/wm-char) "-Meldung empfangen wird. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.<br/>                                                                                                                                       |
| [NM \_ Klick (Symbolleiste)](nm-click-toolbar.md)                      | Wird von einem ToolBar-Steuerelement gesendet, wenn der Benutzer mit der linken Maustaste auf ein Element klickt. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.<br/>                                                                                                                                     |
| [NM \_ customdraw (Symbolleiste)](nm-customdraw-toolbar.md)            | Wird von der Symbolleiste gesendet, um das übergeordnete Fenster über Zeichnungsvorgänge zu benachrichtigen. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.<br/>                                                                                                                                              |
| [NM \_ dblclk (Symbolleiste)](nm-dblclk-toolbar.md)                    | Benachrichtigt das übergeordnete Fenster eines Symbolleisten-Steuer Elements, dass der Benutzer die linke Maustaste im Steuerelement doppelt geklickt hat. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.<br/>                                                                                             |
| [NM- \_ KeyDown (Symbolleiste)](nm-keydown-toolbar.md)                  | Wird von einem Steuerelement gesendet, wenn das Steuerelement den Tastaturfokus besitzt und der Benutzer eine Taste drückt. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet. <br/>                                                                                                                                 |
| [NM- \_ ldown](nm-ldown-toolbar.md)                                | Benachrichtigt das übergeordnete Fenster einer Symbolleiste, dass die linke Maustaste gedrückt wurde. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.<br/>                                                                                                                                        |
| [NM \_ rclick (Symbolleiste)](nm-rclick-toolbar.md)                    | Wird von einem ToolBar-Steuerelement gesendet, wenn der Benutzer mit der rechten Maustaste auf die Symbolleiste klickt. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.<br/>                                                                                                                                |
| [NM \_ rdblclk (Symbolleiste)](nm-rdblclk-toolbar.md)                  | Benachrichtigt das übergeordnete Fenster eines Steuer Elements, dass der Benutzer die Rechte Maustaste im Steuerelement doppelt geklickt hat. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.<br/>                                                                                                         |
| [NM \_ releasedcapture (Symbolleiste)](nm-releasedcapture-toolbar-.md) | Benachrichtigt das übergeordnete Fenster eines Symbolleisten-Steuer Elements, dass das Steuerelement die Maus Aufzeichnung freigibt. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet. <br/>                                                                                                                               |
| [NM- \_ tooltipscreated (Symbolleiste)](nm-tooltipscreated-toolbar-.md) | Benachrichtigt das übergeordnete Fenster einer Symbolleiste, dass die Symbolleiste ein QuickInfo-Steuerelement erstellt hat. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet. <br/>                                                                                                                                    |
| [TBN \_ beginanpassung](tbn-beginadjust.md)                          | Benachrichtigt das übergeordnete Fenster einer Symbolleiste, dass der Benutzer mit dem Anpassen einer Symbolleiste begonnen hat. Dieser Nachrichten Code wird in Form einer [**WM- \_ Benachrichtigungs**](wm-notify.md) Meldung gesendet. <br/>                                                                                                                                          |
| [TBN- \_ BeginDrag](tbn-begindrag.md)                              | Benachrichtigt das übergeordnete Fenster einer Symbolleiste, dass der Benutzer mit dem Ziehen einer Schaltfläche auf einer Symbolleiste begonnen hat. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet. <br/>                                                                                                                            |
| [TBN- \_ custhelp](tbn-custhelp.md)                                | Benachrichtigt das übergeordnete Fenster einer Symbolleiste, dass der Benutzer die Schaltfläche "Hilfe" im Dialogfeld "Symbolleiste anpassen" ausgewählt hat. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.<br/>                                                                                                       |
| [TBN- \_ Delta Schaltfläche](tbn-deletingbutton.md)                    | Wird von einem Symbolleisten-Steuerelement gesendet, wenn eine Schaltfläche gelöscht wird. <br/>                                                                                                                                                                                                                                                |
| [TBN- \_ dragout](tbn-dragout.md)                                  | Wird von einem ToolBar-Steuerelement gesendet, wenn der Benutzer auf eine Schaltfläche klickt, und verschiebt den Cursor dann von der Schaltfläche. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet. <br/>                                                                                                                     |
| [TBN- \_ DragOver](tbn-dragover.md)                                | Gibt an, ob eine [**TB- \_ markbutton**](tb-markbutton.md) -Nachricht für eine Schaltfläche gesendet werden soll, die gezogen wird. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.<br/>                                                                                           |
| [TBN- \_ Dropdown](tbn-dropdown.md)                                | Wird von einem ToolBar-Steuerelement gesendet, wenn der Benutzer auf eine Dropdown-Schaltfläche klickt Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet. <br/>                                                                                                                                                     |
| [TBN- \_ dupaccelerator](tbn-dupaccelerator.md)                    | Gibt an, ob eine Zugriffstaste auf zwei oder mehr aktiven Symbolleisten verwendet werden kann. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.<br/>                                                                                                                                      |
| [TBN- \_ endanpassung](tbn-endadjust.md)                              | Benachrichtigt das übergeordnete Fenster einer Symbolleiste, dass der Benutzer die Anpassung einer Symbolleiste beendet hat. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet. <br/>                                                                                                                                   |
| [TBN- \_ EndDrag](tbn-enddrag.md)                                  | Benachrichtigt das übergeordnete Fenster der Symbolleiste, dass der Benutzer das Ziehen einer Schaltfläche auf einer Symbolleiste beendet hat. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet. <br/>                                                                                                                        |
| [TBN \_ getbuttoninfo](tbn-getbuttoninfo.md)                      | Ruft Informationen zur Symbolleisten Anpassung ab und benachrichtigt das übergeordnete Fenster der Symbolleiste über alle Änderungen, die an der Symbolleiste vorgenommen werden. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet. <br/>                                                                                        |
| [TBN \_ getdispinfo](tbn-getdispinfo.md)                          | Ruft Anzeigeinformationen für ein Symbolleisten Element ab. Diese Benachrichtigung wird in Form einer WM-Benachrichtigungs Meldung gesendet. [**\_**](wm-notify.md)<br/>                                                                                                                                                                           |
| [TBN- \_ getinfotip](tbn-getinfotip.md)                            | Ruft Infotipp-Informationen für ein Symbolleisten Element ab. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.<br/>                                                                                                                                                                      |
| [TBN- \_ GetObject](tbn-getobject.md)                              | Wird von einem ToolBar-Steuerelement gesendet, das den [**tbstyle \_ registerdrop**](toolbar-control-and-button-styles.md) -Stil verwendet, um ein Ablage Zielobjekt anzufordern, wenn der Zeiger über eine seiner Schaltflächen weitergeleitet wird. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.<br/> |
| [TBN- \_ hubänderung](tbn-hotitemchange.md)                      | Wird von einem ToolBar-Steuerelement gesendet, wenn sich das heiße Element (hervorgehoben) ändert. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet. <br/>                                                                                                                                                    |
| [TBN \_ initcustomize](tbn-initcustomize.md)                      | Benachrichtigt das übergeordnete Fenster einer Symbolleiste, dass die Anpassung gestartet wurde. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.<br/>                                                                                                                                                       |
| [TBN- \_ mapaccelerator](tbn-mapaccelerator.md)                    | Fordert den Index der Schaltfläche auf der Symbolleiste an, die dem angegebenen Beschleunigungs Zeichen entspricht. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.<br/>                                                                                                                  |
| [TBN- \_ querydelete](tbn-querydelete.md)                          | Benachrichtigt das übergeordnete Fenster der Symbolleiste, ob eine Schaltfläche aus einer Symbolleiste gelöscht werden kann, während der Benutzer die Symbolleiste anpasst. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet. <br/>                                                                                        |
| [TBN- \_ queryinsert](tbn-queryinsert.md)                          | Benachrichtigt das übergeordnete Fenster der Symbolleiste, ob links neben der angegebenen Schaltfläche eine Schaltfläche eingefügt werden kann, während der Benutzer eine Symbolleiste anpasst. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.<br/>                                                                     |
| [TBN- \_ zurück Setzung](tbn-reset.md)                                      | Benachrichtigt das übergeordnete Fenster der Symbolleiste, dass der Benutzer den Inhalt des Dialog Felds Symbolleiste anpassen zurückgesetzt hat. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.<br/>                                                                                                          |
| [TBN- \_ Wiederherstellung](tbn-restore.md)                                  | Benachrichtigt das übergeordnete Fenster einer Symbolleiste, dass gerade eine Symbolleiste wieder hergestellt wird. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.<br/>                                                                                                                                 |
| [TBN- \_ Speicher](tbn-save.md)                                        | Benachrichtigt das übergeordnete Fenster einer Symbolleiste, dass gerade eine Symbolleiste gespeichert wird. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.<br/>                                                                                                                                    |
| [TBN \_ toolbarchange](tbn-toolbarchange.md)                      | Benachrichtigt das übergeordnete Fenster der Symbolleiste, dass der Benutzer eine Symbolleiste angepasst hat. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet. <br/>                                                                                                                                          |
| [TBN \_ wrapaccelerator](tbn-wrapaccelerator.md)                  | Fordert den Index der Schaltfläche in einem oder mehreren Symbolleisten an, der dem angegebenen Zugriffstasten Zeichen entspricht. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.<br/>                                                                                                         |
| [TBN \_ wraphotitem](tbn-wraphotitem.md)                          | Benachrichtigt eine Anwendung mit zwei oder mehr Symbolleisten, dass das heiße Element gerade geändert wird. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.<br/>                                                                                                                                |



 

### <a name="structures"></a>Strukturen



| Thema                                      | Inhalte                                                                                                                                                                                                                                                                |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ColorMap**](/windows/desktop/api/Commctrl/ns-commctrl-colormap)               | Enthält Informationen, die von der Funktion " [**kreatemappedbitmap**](/windows/desktop/api/Commctrl/nf-commctrl-createmappedbitmap) " zum Zuordnen der Farben der Bitmap verwendet werden. <br/>                                                                                                                                 |
| [**Nmtbcustomdraw**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbcustomdraw)   | Enthält Informationen zu einem von einem ToolBar-Steuerelement gesendeten [nm- \_ customdraw](nm-customdraw-toolbar.md) -Benachrichtigungs Code. <br/>                                                                                                                                |
| [**Nmtbdispinfo**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbdispinfoa)       | Enthält und empfängt Anzeigeinformationen für ein Symbolleisten Element. Diese Struktur wird mit dem [TBN \_ getdispinfo](tbn-getdispinfo.md) -Benachrichtigungs Code verwendet. <br/>                                                                                                    |
| [**Nmtbgetinfotip**](/windows/win32/api/commctrl/ns-commctrl-nmtbgetinfotipa)   | Enthält Infotipp-Informationen für ein Symbolleisten Element und empfängt diese. Diese Struktur wird mit dem " [TBN \_ getinfotip](tbn-getdispinfo.md) "-Benachrichtigungs Code verwendet. <br/>                                                                                                     |
| [**Nmtbhutitem**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem)         | Enthält Informationen, die mit dem [TBN-SBN \_ ](tbn-hotitemchange.md) -Benachrichtigungs Code verwendet werden. <br/>                                                                                                                                                           |
| [**Nmtbrestore**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore)         | Ermöglicht es Anwendungen, die Informationen zu extrahieren, die beim Speichern des Symbolleisten Zustands in [**nmtbsave**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) platziert wurden. Diese Struktur wird an Anwendungen übermittelt, wenn Sie einen [TBN- \_ Wiederherstellungs](tbn-restore.md) Benachrichtigungs Code erhalten.<br/>             |
| [**Nmtbsave**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave)               | Diese Struktur wird an Anwendungen übermittelt, wenn Sie einen [TBN- \_ Speicher](tbn-save.md) Benachrichtigungs Code erhalten. Sie enthält Informationen über die Schaltfläche, die gerade gespeichert wird. Anwendungen können die Werte der Mitglieder ändern, um zusätzliche Informationen zu speichern. <br/> |
| [**Nmtoolbar**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara)             | Enthält Informationen zum Verarbeiten von Symbolleisten-Benachrichtigungs Codes. Diese Struktur ersetzt die **TBNOTIFY** -Struktur. <br/>                                                                                                                                      |
| [**Tbaddbitmap**](/windows/win32/api/commctrl/ns-commctrl-tbaddbitmap)         | Fügt einer Symbolleiste eine Bitmap hinzu, die Schaltflächen Bilder enthält.<br/>                                                                                                                                                                                                      |
| [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)               | Enthält Informationen über eine Schaltfläche in einer Symbolleiste.<br/>                                                                                                                                                                                                            |
| [**Tbbuttoninfo**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa)       | Enthält Informationen für eine bestimmte Schaltfläche in einer Symbolleiste oder empfängt diese.<br/>                                                                                                                                                                                         |
| [**Tbinsertmark**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark)       | Enthält Informationen über die Einfügemarke in einem ToolBar-Steuerelement. <br/>                                                                                                                                                                                            |
| [**Tbmetrics**](/windows/desktop/api/Commctrl/ns-commctrl-tbmetrics)             | Definiert die Metriken einer Symbolleiste, die zum Verkleinern oder Erweitern von Symbolleisten Elementen verwendet werden.<br/>                                                                                                                                                                            |
| [**Tbreplacebitmap**](/windows/desktop/api/Commctrl/ns-commctrl-tbreplacebitmap) | Wird mit der [**TB \_ replacebitmap**](tb-replacebitmap.md) -Meldung verwendet, um eine Symbolleisten-Bitmap durch eine andere zu ersetzen.<br/>                                                                                                                                              |
| [**Tbsaveparameams**](/windows/win32/api/commctrl/ns-commctrl-tbsaveparamsa)       | Gibt den Speicherort in der Registrierung an, an dem die [**TB \_ saverestore**](tb-saverestore.md) -Nachricht Informationen über den Status einer Symbolleiste speichert und abruft. <br/>                                                                                           |



 

### <a name="constants"></a>Konstanten



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Thema</th>
<th>Inhalte</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="toolbar-button-states.md">Symbolleisten Schaltflächen</a></td>
<td>In diesem Abschnitt sind die Zustände aufgeführt, die eine Symbolleisten-Schaltfläche haben <br/></td>
</tr>
<tr class="even">
<td><a href="toolbar-control-and-button-styles.md">ToolBar-Steuerelement und Schaltflächen Stile</a></td>
<td>Die folgenden Fenster Stile sind spezifisch für Symbolleisten. Sie werden mit anderen Fenster Stilen kombiniert, wenn die Symbolleiste erstellt wird.<br/> <strong>Hinweis</strong> Für allgemeine Steuerelemente, <a href="common-control-versions.md">Version 6,00</a>, sind Schaltflächen unabhängig von der Stil Einstellung immer transparent, wenn ein <a href="themes-overview.md">visueller Stil</a> mit der Symbolleiste verwendet wird. Andernfalls ist das Transparenz Verhalten normal, wie durch die Verwendung des <a href="toolbar-control-and-button-styles.md"><strong>TBSTYLE_FLAT</strong></a> oder <a href="toolbar-control-and-button-styles.md"><strong>TBSTYLE_TRANSPARENT</strong></a> Stils angegeben.
<blockquote>
[!Note]<br />
Comctl32.dll Version 6 ist nicht Verteil Bar, aber in Windows oder höher enthalten. Wenn Sie Comctl32.dll Version 6 verwenden möchten, geben Sie ihn in einem Manifest an. Weitere Informationen zu Manifesten finden Sie unter <a href="cookbook-overview.md">Aktivieren von visuellen Stilen</a>.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="toolbar-extended-styles.md">Erweiterte Toolbar-Stile</a></td>
<td>In diesem Abschnitt werden die von Symbolleisten-Steuerelementen unterstützten erweiterten Stile aufgelistet<br/></td>
</tr>
<tr class="even">
<td><a href="toolbar-standard-button-image-index-values.md">Bild-/Indexwerte der Symbolleiste Standard</a></td>
<td>In diesem Abschnitt werden die Indexwerte von Bildern in Standard Bitmaps angegeben.<br/></td>
</tr>
</tbody>
</table>



 

