---
description: Ein DirectoryList-Steuerelement zeigt einen Teil des Pfads an, der derzeit im PathEdit-Steuerelement angezeigt wird. Das DirectoryList-Steuerelement zeigt die Ordner unterhalb des Verzeichnisses an, das derzeit vom DirectoryCombo-Steuerelement angezeigt wird.
ms.assetid: 05e70381-28c0-4568-808e-ff2dee8ff790
title: DirectoryList-Steuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ce0cf409f4ca7335bd032f1fc63831db88ace14424ef7a73cd3853c9ff3e2de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086190"
---
# <a name="directorylist-control"></a>DirectoryList-Steuerelement

Ein DirectoryList-Steuerelement zeigt einen Teil des Pfads an, der derzeit im [PathEdit-Steuerelement angezeigt wird.](pathedit-control.md) Das DirectoryList-Steuerelement zeigt die Ordner unterhalb des Verzeichnisses an, das derzeit vom [DirectoryCombo-Steuerelement angezeigt wird.](directorycombo-control.md)

Die Steuerelemente PathEdit, DirectoryCombo und DirectoryList sind derselben Zeichenfolgenwerteigenschaft zugeordnet. Diese Eigenschaft ist der vom Benutzer ausgewählte Pfad. Geben Sie den Namen der Eigenschaft in die Spalte Eigenschaft der [Control-Tabelle ein.](control-table.md) Diese Eigenschaft muss über einen Anfangswert verfügen, der mindestens ein Volume und eine Unterebene enthält. Geben Sie den Anfangswert für die Eigenschaft in der Spalte Wert der [Property -Tabelle an.](property-table.md)

Dieses Steuerelement ist für die Verwendung in einem Dialogfeld zum Durchsuchen [zusammen](browse-dialog.md) mit dem [PathEdit-](pathedit-control.md) und DirectoryList-Steuerelement vorgesehen.

Das DirectoryList-Steuerelement veröffentlicht die folgenden ControlEvents.



| ControlEvent                                            | BESCHREIBUNG                                                       |
|---------------------------------------------------------|-------------------------------------------------------------------|
| [DirectoryListNew](directorylistnew-controlevent.md)   | Erstellt einen neuen Ordner und wählt das Namensfeld für die Bearbeitung aus.      |
| [IgnoreChange](ignorechange-controlevent.md)           | Hebt einen Ordner im aktuellen Verzeichnis hervor, wird aber nicht geöffnet. |
| [DirectoryListUp](directorylistup-controlevent.md)     | Wählt das übergeordnete Element des aktuellen Verzeichnisses aus.                      |
| [DirectoryListOpen](directorylistopen-controlevent.md) | Wählt ein Verzeichnis aus und hebt es hervor.                               |



 

Der Inhalt des Textfelds der [Control-Tabelle](control-table.md) wird nie vom DirectoryList-Steuerelement angezeigt. Stattdessen gibt dieses Feld den Textstil an, der vom -Steuerelement angezeigt werden soll, und enthält eine Beschreibung des Steuerelements, das von Bildschirmüberprüfungs-Hilfsprogrammen verwendet wird. Stellen Sie der Zeichenfolge der angezeigten Zeichen { style} oder {&style } voran, um die Schriftart und den \\ Schriftschnitt einer Textzeichenfolge zu setzen. Dabei ist style ein Bezeichner, der in der TextStyle -Spalte der [TextStyle-Tabelle aufgeführt ist.](textstyle-table.md) Wenn keines dieser Eigenschaften vorhanden ist, die [**DefaultUIFont-Eigenschaft**](defaultuifont.md) jedoch als gültiger Textstil definiert ist, wird diese Schriftart verwendet. Die folgenden Informationen werden von den Bildschirmüberprüfungs-Hilfsprogrammen als Beschreibung des Steuerelements gelesen. Weitere Informationen [finden Sie unter Barrierefreiheit.](accessibility.md)

## <a name="control-attributes"></a>Steuerelementattribute

Sie können die folgenden Attribute mit diesem Steuerelement verwenden. Um den Wert eines Attributs mithilfe eines Ereignisses zu ändern, abonnieren Sie das Steuerelement für ein ControlEvent in der [EventMapping-Tabelle,](eventmapping-table.md) und listen Sie den Bezeichner des Attributs in der Spalte Attribut auf. Geben Sie den Bezeichner des ControlEvents in der Spalte Ereignis ein.



| Attributbezeichner                                               | Hexadezimales Bit                  | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IndirectPropertyName](indirectpropertyname-control-attribute.md) |                                  | Dies ist der Name einer indirekten Eigenschaft, die dem Steuerelement zugeordnet ist. Wenn das Indirekte Attributbit festgelegt ist, zeigt das Steuerelement den Wert der Eigenschaft mit diesem Namen an oder ändert diesen. Wenn das Indirekte Attributbit festgelegt ist, ist dieser Name auch der Wert der Eigenschaft, die in der Property -Spalte der [Control-Tabelle aufgeführt ist.](control-table.md)                        |
| [Position](position-control-attribute.md)                         |                                  | Position des Steuerelements im Dialogfeld. Geben Sie die Breite, Höhe und Koordinaten der linken Ecke des Steuerelements in die Spalten Width, Height, X und Y der [Tabelle Control ein.](control-table.md) Verwenden [Sie Installationseinheiten](installer-units.md) für Länge und Entfernung.<br/>                                                                             |
| [PropertyName](propertyname-control-attribute.md)                 |                                  | Dies ist der Name der Eigenschaft, die diesem Steuerelement zugeordnet ist. Wenn das Indirekte Attributbit nicht festgelegt ist, zeigt das Steuerelement den Wert der Eigenschaft mit diesem Namen an oder ändert diesen. Dieses Attribut wird in der Property -Spalte der [Control-Tabelle angegeben.](control-table.md)                                                                                        |
| [PropertyValue](propertyvalue-control-attribute.md)               |                                  | Der aktuelle Wert der Eigenschaft, die von diesem Steuerelement angezeigt oder geändert wird. Wenn das Indirekte Attributbit nicht festgelegt ist, ist dies der Wert von PropertyName. Wenn das Indirekte Attributbit festgelegt ist, ist dies der Wert von IndirectPropertyName. Wenn sich das Attribut ändert, spiegelt das Steuerelement den neuen Wert wider.                                                                           |
| [Text](text-control-attribute.md)                                 |                                  | Um Text in Sprachbildschirmen anzuzeigen, geben Sie den Text in die Spalte Text der [Steuertabelle ein.](control-table.md) Weitere Informationen [finden Sie unter Barrierefreiheit.](accessibility.md)                                                                                                                                                                                                                 |
| [Visible](visible-control-attribute.md)                           | 0x00000000 0x00000001<br/> | Ausgeblendetes Steuerelement. Sichtbares Steuerelement.<br/> Fügen Sie dieses Bit in das Bitwort der Spalte Attribute in die [Control-Tabelle](control-table.md)ein, um das Steuerelement bei seiner Erstellung sichtbar oder ausgeblendet zu machen.<br/> Sie können ein Steuerelement auch mithilfe der [ControlCondition-Tabelle ausblenden oder anzeigen.](controlcondition-table.md)<br/>                                     |
| [Aktiviert](enabled-control-attribute.md)                           | 0x00000000 0x00000002<br/> | Steuerelement in einem deaktivierten Zustand. Steuerelement in einem aktivierten Zustand.<br/> Fügen Sie dieses Bit in das Bitwort in die Spalte Attribute des [Steuerelements](control-table.md) ein, um das Steuerelement bei der Erstellung zu aktivieren.<br/> Sie können ein Steuerelement auch mithilfe der [ControlCondition-Tabelle aktivieren oder deaktivieren.](controlcondition-table.md)<br/>                                   |
| [Sunken](sunken-control-attribute.md)                             | 0x00000000 0x00000004<br/> | Zeigt den standardmäßigen visuellen Stil an. Zeigt das Steuerelement mit einem versenkten 3D-Look an.<br/> Schließen Sie diese Bits in das Bitwort in die Spalte Attribute der [Control-Tabelle ein.](control-table.md)<br/>                                                                                                                                                             |
| [Indirekt](indirect-control-attribute.md)                         | 0x00000000 0x00000008<br/> | Das -Steuerelement zeigt den Wert der -Eigenschaft in der Property -Spalte der [Control-Tabelle](control-table.md)an oder ändert diesen. Das -Steuerelement zeigt den Wert der Eigenschaft an, in der der Bezeichner in der Spalte Eigenschaft der Control-Tabelle aufgeführt ist, oder ändert diesen.<br/> Bestimmt, ob indirekt auf die diesem Steuerelement zugeordnete Eigenschaft verwiesen wird.<br/> |
| [RTLRO](rtlro-control-attribute.md)                               | 0x00000000 0x00000020<br/> | Text im Steuerelement wird in der Lese reihenfolge von links nach rechts angezeigt. Text im Steuerelement wird in der Lese reihenfolge von rechts nach links angezeigt.<br/>                                                                                                                                                                                                                              |
| [RightAligned](rightaligned-control-attribute.md)                 | 0x00000000 0x00000040<br/> | Text im Steuerelement wird linksbündig ausgerichtet. Text im Steuerelement wird rechtsbündig ausgerichtet.<br/>                                                                                                                                                                                                                                                                       |
| [LeftScroll](leftscroll-control-attribute.md)                     | 0x00000000 0x00000080<br/> | Die Scrollleiste befindet sich auf der rechten Seite des Steuerelements. Die Scrollleiste befindet sich auf der linken Seite des Steuerelements.<br/>                                                                                                                                                                                                                                         |
| [BiDi-Steuerelement](bidi-control-attribute.md)                         | 0x000000E0                       | Legen Sie diesen Wert für eine Kombination der [Attribute RTLRO,](rtlro-control-attribute.md) [RightAligned](rightaligned-control-attribute.md)und [LeftScroll](leftscroll-control-attribute.md) fest.                                                                                                                                                                          |



 

## <a name="remarks"></a>Hinweise

Dieses Steuerelement kann mithilfe der CreateWindowEx-Funktion aus der WC \_ [**LISTVIEW-Klasse erstellt**](/windows/win32/api/winuser/nf-winuser-createwindowexa) werden. Sie verfügt über **die TABSTOP-Formate LVS \_ LIST,** **LVS \_ EDITLABELS,** **\_ WS VSCROLL,** **LVS \_ SHAREIMAGELISTS,** **LVS \_ AUTOARRANGE,** **LVS \_ SINGLESEL,** **WS \_ BORDER,** **LVS \_ SORTASCENDING,** **WS \_ CHILD,** **WS \_ GROUP** und **WS. \_**

Mit diesem Steuerelement kann der Benutzer einen Unterordner der aktuellen Auswahl auswählen. Mit zusätzlichen Schaltflächen kann der Benutzer auch einen neuen Ordner in der aktuellen Auswahl auswählen oder eine Ebene im Pfad nach oben verschieben. Wenn der Benutzer  die Schaltfläche Neuen Ordner erstellen in einem Ordner auswählt, in dem bereits ein neuer Ordner vorhanden ist, wird kein zweiter neuer Ordner erstellt, und der Name des vorhandenen neuen Ordners wird zur Bearbeitung ausgewählt.

 

