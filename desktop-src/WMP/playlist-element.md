---
title: PLAYLIST-Element
description: PLAYLIST-Element
ms.assetid: de568529-81f2-476b-ad1b-bb53f7e97b13
keywords:
- Windows Media Player Skins,PLAYLIST-Element
- skins,PLAYLIST-Element
- PLAYLIST-Element
- Referenz für Skins, PLAYLIST-Element
- Elements,PLAYLIST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fed45a2b8d7a0c0c5a2e19a783fbecf1041ecf2550c9f9a3a31e4b7c1aab894d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118336746"
---
# <a name="playlist-element"></a>PLAYLIST-Element

Das **PLAYLIST-Element** bietet eine Möglichkeit zum Organisieren von Medienelementen in einer Liste zur einfachen Bearbeitung mithilfe der folgenden Attribute und Methoden. Der Einfachheit **halber** werden auch vordefinierte PLAYLIST-Elemente bereitgestellt. Benutzerdefinierte Spalten können für eine Wiedergabeliste angegeben werden, indem **COLUMN-Elemente** als untere Elemente des **PLAYLIST-Elements hinzugefügt** werden.

Das **PLAYLIST-Element** unterstützt die folgenden Attribute.



| attribute                                                                                 | BESCHREIBUNG                                                                                                                                |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [allowColumnSorting](playlist-allowcolumnsorting.md)                                     | Gibt einen Wert an, der angibt, ob das Sortieren nach Spaltenheadern zulässig ist, oder ruft einen Wert ab.                                                    |
| [allowItemEditing](playlist-allowitemediting.md)                                         | Gibt einen Wert an, der angibt, ob Elemente in einer Wiedergabeliste die bearbeitungsbasierte Bearbeitung unterstützen, oder ruft diesen ab.                                            |
| [Backgroundcolor](playlist-backgroundcolor.md)                                           | Gibt die Hintergrundfarbe an oder ruft sie ab.                                                                                               |
| [backgroundImage](playlist-backgroundimage.md)                                           | Gibt das Hintergrundbild an oder ruft es ab.                                                                                               |
| [KontrollkästchenVisible](playlist-checkboxesvisible.md)                                       | Gibt einen Wert an, der angibt, ob Kontrollkästchen sichtbar sind, oder ruft einen Wert ab.                                                                  |
| [columnCount](playlist-columncount.md)                                                   | Ruft die Anzahl der angezeigten Spalten ab.                                                                                                     |
| [columnOrder](playlist-columnorder.md)                                                   | Gibt die Reihenfolge der Wiedergabelistenspalten an oder ruft sie ab.                                                                                  |
| [Spalten](playlist-columns.md)                                                           | Definiert die Spalten, die im **PLAYLIST-Element angezeigt** werden.                                                                               |
| [columnsVisible](playlist-columnsvisible.md)                                             | Gibt einen Wert an, der angibt, ob Spalten angezeigt werden, oder ruft einen Wert ab.                                                                       |
| [Kopieren](playlist-copying.md)                                                           | Ruft einen Wert ab, der angibt, ob das **PLAYLIST-Element** kopiert wird.                                                    |
| [disabledItemColor](playlist-disableditemcolor.md)                                       | Gibt die Farbe einer deaktivierten CD-Spur oder von Onlineinhalten im Offlinemodus an oder ruft sie ab.                                                 |
| [dropDownBackgroundImage](playlist-dropdownbackgroundimage.md)                           | Gibt den Namen des Bilds an, das im Hintergrund der Dropdownliste angezeigt wird, oder ruft diesen ab.                                        |
| [dropDownImage](playlist-dropdownimage.md)                                               | Gibt den Namen des Bilds an, das für die Dropdownlistenschaltfläche verwendet wird, die am rechten Rand der Dropdownliste angezeigt wird, oder ruft diesen ab. |
| [Dropdownlist](playlist-dropdownlist.md)                                                 | Gibt einen Wert an, der angibt, welche Elemente in der Dropdownliste für eine bestimmte Instanz des PLAYLIST-Elements angezeigt werden, oder **ruft einen Wert** ab.   |
| [dropDownToolTip](playlist-dropdowntooltip.md)                                           | Gibt die QuickInfo an, die angezeigt wird, wenn der Benutzer auf das **Dropdownmenü des PLAYLIST-Elements** zeigt, oder ruft sie ab.                                |
| [dropDownVisible](playlist-dropdownvisible.md)                                           | Gibt einen Wert an, der angibt, ob der Dropdown-Selektor **des PLAYLIST-Elements** sichtbar ist, oder ruft diesen ab.                                  |
| [editButtonVisible](playlist-editbuttonvisible.md)                                       | Gibt einen Wert an, der  angibt, ob die Wiedergabelistenelement-Bearbeitungsschaltfläche sichtbar ist, oder ruft einen Wert ab.                                         |
| [foregroundColor](playlist-foregroundcolor.md)                                           | Gibt die Vordergrundfarbe an oder ruft sie ab.                                                                                               |
| [hueShift](playlist-hueshift.md)                                                         | Gibt die Menge an, um die der Farbton der Dropdownbilder verschoben wird, oder ruft sie ab.                                                     |
| [Itemcount](playlist-itemcount.md)                                                       | Ruft die Anzahl der Elemente ab, die derzeit im **PLAYLIST-Element angezeigt** werden.                                                             |
| [itemErrorColor](playlist-itemerrorcolor.md)                                             | Gibt die Hervorhebungsfarbe an, die ein Wiedergabelistenelement mit einem Fehlerzustand angibt, oder ruft diese ab.                                     |
| [itemMedia](playlist-itemmedia.md)                                                       | Ruft das **Media-Objekt** ab, das dem angegebenen Index im **PLAYLIST-Element** entspricht.                                               |
| [itemPlayingBackgroundColor](playlist-itemplayingbackgroundcolor.md)                     | Gibt die Hintergrundfarbe des aktuell abspielten Wiedergabelistenelements an oder ruft sie ab.                                                        |
| [itemPlayingColor](playlist-itemplayingcolor.md)                                         | Gibt die Hervorhebungsfarbe an, die das aktuell abspielte Element in der Wiedergabeliste angibt, oder ruft sie ab.                                      |
| [itemPlaylist](playlist-itemplaylist.md)                                                 | Ruft die Wiedergabeliste für das Medienelement ab, das am angegebenen Index im **PLAYLIST-Element angezeigt** wird.                                |
| [itemSelectedBackgroundColor](playlist-itemselectedbackgroundcolor.md)                   | Gibt einen Wert an, der die Hintergrundfarbe eines ausgewählten Elements in der Wiedergabeliste angibt, oder ruft diesen ab.                                         |
| [itemSelectedBackgroundFocusLostColor](playlist-itemselectedbackgroundfocuslostcolor.md) | Gibt einen Wert an, der die Textfarbe eines ausgewählten Elements in der Wiedergabeliste angibt, oder ruft diesen ab.                                               |
| [itemSelectedColor](playlist-itemselectedcolor.md)                                       | Gibt einen Wert an, der die Textfarbe eines ausgewählten Elements in der Wiedergabeliste angibt, oder ruft diesen ab.                                               |
| [itemSelectedFocusLostColor](playlist-itemselectedfocuslostcolor.md)                     | Gibt einen Wert an, der die Textfarbe eines ausgewählten Elements in der Wiedergabeliste angibt, wenn die Wiedergabeliste den Fokus verliert, oder ruft diesen wert ab.                 |
| [leftStatus](playlist-leftstatus.md)                                                     | Gibt den Statustext an, der links und unten im **PLAYLIST-Element** angezeigt wird, oder ruft diesen ab.                          |
| [Playlist](playlist-playlist.md)                                                         | Gibt das Playlist-Objekt an, für das **das** **PLAYLIST-Element** eine Schnittstelle bietet, oder ruft es ab.                                    |
| [playlistItemsVisible](playlist-playlistitemsvisible.md)                                 | Gibt einen Wert an, der angibt, ob Elemente in der Wiedergabeliste sichtbar sind, oder ruft einen Wert ab.                                                       |
| [rightStatus](playlist-rightstatus.md)                                                   | Gibt den Statustext an, der rechts und unten im **PLAYLIST-Element** angezeigt wird, oder ruft diesen ab.                         |
| [Sättigung](playlist-saturation.md)                                                     | Gibt den Sättigungswert der Dropdownbilder an oder ruft sie ab.                                                                       |
| [statusColor](playlist-statuscolor.md)                                                   | Gibt die Farbe der Statuszeile im **PLAYLIST-Element** an oder ruft sie ab.                                                           |
| [statusTextColor](playlist-statustextcolor.md)                                           | Gibt einen Wert an, der die Farbe des Statustexts angibt, oder ruft einen Wert ab.                                                                    |
| [toolbarVisible](playlist-toolbarvisible.md)                                             | Gibt einen Wert an, der angibt, ob die Wiedergabelistensymbolleiste angezeigt wird, oder ruft einen Wert ab.                                                           |



 

Das **PLAYLIST-Element** unterstützt die folgenden Methoden.



| Methode                                                              | BESCHREIBUNG                                                                                                               |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [abortCopy](playlist-abortcopy.md)                                 | Bricht einen Kopiervorgang ab.                                                                                                 |
| [addSelectedToPlaylist](playlist-addselectedtoplaylist.md)         | Fügt der Wiedergabeliste das ausgewählte Element hinzu.                                                                                   |
| [copy](playlist-copy.md)                                           | Startet einen Kopiervorgang von der CD.                                                                                      |
| [deleteSelected](playlist-deleteselected.md)                       | Löscht das ausgewählte Element aus der Wiedergabeliste.                                                                              |
| [deleteSelectedFromLibrary](playlist-deleteselectedfromlibrary.md) | Löscht das ausgewählte Element aus der Wiedergabeliste und aus der Bibliothek.                                                         |
| [getNextCheckedItem](playlist-getnextcheckeditem.md)               | Ruft den Index des nächsten überprüften Elements in der Wiedergabeliste nach dem angegebenen Index ab.                               |
| [getNextCheckedItem2](playlist-getnextcheckeditem2.md)             | Ruft den Index des nächsten überprüften Elements in der Wiedergabeliste nach dem angegebenen Index ab. Funktioniert mit geschachtelten Wiedergabelisten.  |
| [getNextSelectedItem](playlist-getnextselecteditem.md)             | Ruft den Index des nächsten ausgewählten Elements in der Wiedergabeliste nach dem angegebenen Index ab.                              |
| [getNextSelectedItem2](playlist-getnextselecteditem2.md)           | Ruft den Index des nächsten ausgewählten Elements in der Wiedergabeliste nach dem angegebenen Index ab. Funktioniert mit geschachtelten Wiedergabelisten. |
| [moveSelectedDown](playlist-moveselecteddown.md)                   | Verschiebt das ausgewählte Element um eine Position in der Liste nach unten.                                                                    |
| [moveSelectedUp](playlist-moveselectedup.md)                       | Verschiebt das ausgewählte Element um eine Position in der Liste nach oben.                                                                      |
| [setCheckedState](playlist-setcheckedstate.md)                     | Gibt an, dass das indizierte Element in der Wiedergabeliste überprüft wird.                                                               |
| [setCheckedState2](playlist-setcheckedstate2.md)                   | Legt den überprüften Zustand des Elements mit dem angegebenen Index im **PLAYLIST-Element** fest. Funktioniert mit geschachtelten Wiedergabelisten.     |
| [setColumnResizeMode](playlist-setcolumnresizemode.md)             | Gibt an, wie die größe der indizierten Spalte selbst ist.                                                                            |
| [setColumnWidth](playlist-setcolumnwidth.md)                       | Gibt die Spaltenbreite an und ändert den Größenänderungsmodus der Spalte in "wmpcrmFixed".                                    |
| [setSelectedState](playlist-setselectedstate.md)                   | Gibt an, dass das indizierte Element in der Wiedergabeliste ausgewählt ist.                                                              |
| [setSelectedState2](playlist-setselectedstate2.md)                 | Legt den ausgewählten Zustand des Elements mit dem angegebenen Index im **PLAYLIST-Element** fest. Funktioniert mit geschachtelten Wiedergabelisten.    |
| [sortColumn](playlist-sortcolumn.md)                               | Sortiert die Daten in der angegebenen Spalte.                                                                                   |



 

Das **PLAYLIST-Element** unterstützt die Ambient-Attribute und kann die Ambient-Ereignishandler implementieren, sofern nicht anders angegeben. Weitere Informationen finden Sie unter [Ambient Attributes (Umgebungsattribute)](ambient-attributes.md) [und Ambient Event Handlers (Umgebungsereignishandler).](ambient-event-handlers.md)

Vordefinierte Wiedergabelisten sind normale **PLAYLIST-Elemente** mit verschiedenen allgemeinen Attributeinstellungen, die standardmäßig angegeben sind. Die folgenden vordefinierten Wiedergabelisten sind verfügbar.



| Vordefinierte WIEDERGABELISTE                      | BESCHREIBUNG                                                       |
|------------------------------------------|-------------------------------------------------------------------|
| [DROPDOWNPLAYLIST](dropdownplaylist.md) | Eine Dropdownliste, **in** der keine Elemente sichtbar sind.                   |
| [ITEMSPLAYLIST](itemsplaylist.md)       | Eine Dropdownliste, **in** der keine Elemente oder Spaltenüberschriften sichtbar sind. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Referenz zur Skinprogrammierung**](skin-programming-reference.md)
</dt> </dl>

 

 




