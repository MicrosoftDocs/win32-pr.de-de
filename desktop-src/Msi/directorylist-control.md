---
description: Ein directoriylist-Steuerelement zeigt einen Teil des Pfads an, der derzeit im Steuerelement "pathedit" angezeigt wird. Das Director List-Steuerelement zeigt die Ordner unterhalb des Verzeichnisses an, das zurzeit vom directoriycombo-Steuerelement angezeigt wird.
ms.assetid: 05e70381-28c0-4568-808e-ff2dee8ff790
title: Director List-Steuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee6a1e48a25ae057c836c7b815dae18e7dcf5c3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363564"
---
# <a name="directorylist-control"></a>Director List-Steuerelement

Ein directoriylist-Steuerelement zeigt einen Teil des Pfads an, der derzeit im Steuerelement " [pathedit](pathedit-control.md)" angezeigt wird. Das Director List-Steuerelement zeigt die Ordner unterhalb des Verzeichnisses an, das zurzeit vom [directoriycombo-Steuer](directorycombo-control.md)Element angezeigt wird.

Die Steuerelemente "pathedit", "Director ycombo" und "Director ylist" sind der gleichen Zeichen folgen Wert Eigenschaft zugeordnet. Diese Eigenschaft ist der vom Benutzer ausgewählte Pfad. Geben Sie den Namen der Eigenschaft in die Eigenschafts Spalte der [Steuerelement Tabelle](control-table.md)ein. Diese Eigenschaft muss über einen Anfangswert mit mindestens einem Volume und einer Unterebene verfügen. Geben Sie den Anfangswert für die Eigenschaft in der Spalte Wert der [Eigenschaften Tabelle](property-table.md)an.

Dieses Steuerelement ist für die Verwendung in einem [Dialog Feld zum Durchsuchen](browse-dialog.md) in Verbindung mit dem Steuerelement " [pathedit](pathedit-control.md) " und "Directoren List" vorgesehen.

Das Director List-Steuerelement veröffentlicht die folgenden ControlEvents.



| ControlEvent                                            | BESCHREIBUNG                                                       |
|---------------------------------------------------------|-------------------------------------------------------------------|
| [Directoriylistnew](directorylistnew-controlevent.md)   | Erstellt einen neuen Ordner und wählt das Namensfeld für die Bearbeitung aus.      |
| [Ignorechange](ignorechange-controlevent.md)           | Hebt einen Ordner im aktuellen Verzeichnis hervor, öffnet ihn aber nicht. |
| [Directoren](directorylistup-controlevent.md)     | Wählt das übergeordnete Element des aktuellen Verzeichnisses aus.                      |
| [Directoriylistopen](directorylistopen-controlevent.md) | Hiermit wird ein Verzeichnis ausgewählt und hervorgehoben.                               |



 

Der Inhalt des Textfelds der Steuerelement [Tabelle](control-table.md) wird nie durch das directorylist-Steuerelement angezeigt. Stattdessen gibt dieses Feld den Text Stil an, der vom Steuerelement angezeigt wird, und enthält eine Beschreibung des Steuer Elements, das von den Hilfsprogrammen für die Bildschirm Überprüfung verwendet wird. Um die Schriftart und den Schrift Schnitt einer Text Zeichenfolge festzulegen, stellen Sie die Zeichenfolge der angezeigten Zeichen mit "{ \\ Style}" oder "{&*Style*}" vor. Dabei ist Style ein Bezeichner, der in der TextStyle-Spalte der [TextStyle-Tabelle](textstyle-table.md)aufgeführt ist. Wenn keines dieser beiden vorhanden ist, die [**defaultuifont**](defaultuifont.md) -Eigenschaft jedoch als gültiger Textstil definiert ist, wird diese Schriftart verwendet. Die folgenden Informationen werden von den Hilfsprogrammen der Bildschirm Überprüfung als Beschreibung des Steuer Elements gelesen. Siehe [Barrierefreiheit](accessibility.md).

## <a name="control-attributes"></a>Steuerelement Attribute

Mit diesem Steuerelement können Sie die folgenden Attribute verwenden. Um den Wert eines Attributs mithilfe eines Ereignisses zu ändern, abonnieren Sie das Steuerelement einem ControlEvent in der [EventMapping-Tabelle](eventmapping-table.md) , und Listen Sie den Bezeichner des Attributs in der Attribut-Spalte auf. Geben Sie den Bezeichner des ControlEvent in der Ereignis Spalte ein.



| Attribut Bezeichner                                               | Hexadezimales Bit                  | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Derekpropertyname](indirectpropertyname-control-attribute.md) |                                  | Dies ist der Name einer indirekten Eigenschaft, die dem Steuerelement zugeordnet ist. Wenn das indirekte Attribut Bit festgelegt ist, zeigt das Steuerelement den Wert der Eigenschaft mit diesem Namen an oder ändert ihn. Wenn das indirekte Attribut Bit festgelegt ist, ist dieser Name auch der Wert der Eigenschaft, die in der Eigenschafts Spalte der [Steuerelement Tabelle](control-table.md)aufgeführt ist.                        |
| [Position](position-control-attribute.md)                         |                                  | Position des-Steuer Elements im Dialogfeld. Geben Sie die Breite, Höhe und Koordinaten der Steuerelemente der linken Ecke des Steuer Elements in die Spalten Width, Height, X und Y der [Steuerelement Tabelle](control-table.md)ein. Verwenden Sie die [Installer-Einheiten](installer-units.md) für Länge und Entfernung.<br/>                                                                             |
| [PropertyName](propertyname-control-attribute.md)                 |                                  | Dies ist der Name der Eigenschaft, die diesem Steuerelement zugeordnet ist. Wenn das indirekte Attribut Bit nicht festgelegt ist, zeigt das Steuerelement den Wert der Eigenschaft mit diesem Namen an oder ändert ihn. Dieses Attribut wird in der-Eigenschaften Spalte der [Steuerelement Tabelle](control-table.md)angegeben.                                                                                        |
| [PropertyValue](propertyvalue-control-attribute.md)               |                                  | Aktueller Wert der Eigenschaft, die von diesem Steuerelement angezeigt oder geändert wird. Wenn das indirekte Attribut Bit nicht festgelegt ist, ist dies der Wert von PropertyName. Wenn das indirekte Attribut Bit festgelegt ist, ist dies der Wert von deretpropertyname. Wenn sich das Attribut ändert, spiegelt das-Steuerelement den neuen Wert wider.                                                                           |
| [Text](text-control-attribute.md)                                 |                                  | Geben Sie den Text in die Text-Spalte der [Steuerelement Tabelle](control-table.md)ein, um Text in Bildschirmlesern anzuzeigen. Siehe [Barrierefreiheit](accessibility.md).                                                                                                                                                                                                                 |
| [Visible](visible-control-attribute.md)                           | 0x00000000 0x00000001<br/> | Verborgenes Steuerelement. Sichtbares Steuerelement.<br/> Fügen Sie dieses Bit in das bitwort der Attribut Spalte in der [Steuerelement Tabelle](control-table.md)ein., damit das Steuerelement bei der Erstellung sichtbar oder ausgeblendet wird.<br/> Sie können ein Steuerelement auch mithilfe der [Tabelle "ControlCondition](controlcondition-table.md)" ausblenden oder anzeigen.<br/>                                     |
| [Aktiviert](enabled-control-attribute.md)                           | 0x00000000 0x00000002<br/> | Steuerelement in deaktiviertem Zustand. Steuerelement im aktivierten Zustand.<br/> Fügen Sie dieses Bit in das bitwort in die Spalte Attribute des [Steuer](control-table.md) Elements ein, um das Steuerelement bei der Erstellung zu aktivieren.<br/> Sie können ein Steuerelement auch mithilfe der [Tabelle "ControlCondition](controlcondition-table.md)" aktivieren oder deaktivieren.<br/>                                   |
| [Sunken](sunken-control-attribute.md)                             | 0x00000000 0x00000004<br/> | Zeigt den visuellen Standardstil an. Zeigt das Steuerelement mit einem abgesenkten 3D-Bild an.<br/> Fügen Sie diese Bits in das bitwort in die Spalte Attribute der [Steuerelement Tabelle](control-table.md)ein.<br/>                                                                                                                                                             |
| [Indirekt](indirect-control-attribute.md)                         | 0x00000000 0x00000008<br/> | Das-Steuerelement zeigt den Wert der-Eigenschaft in der-Eigenschaften Spalte der [Steuerelement Tabelle](control-table.md)an oder ändert ihn. Das-Steuerelement zeigt den Wert der-Eigenschaft an oder ändert den Wert der-Eigenschaft, die den Bezeichner enthält<br/> Bestimmt, ob indirekt auf die diesem Steuerelement zugeordnete Eigenschaft verwiesen wird.<br/> |
| [Rtlro](rtlro-control-attribute.md)                               | 0x00000000 0x00000020<br/> | Der Text im Steuerelement wird in der Lesefolge von links nach rechts angezeigt. Der Text im Steuerelement wird in der Lesefolge von rechts nach links angezeigt.<br/>                                                                                                                                                                                                                              |
| [Rechtsbündig](rightaligned-control-attribute.md)                 | 0x00000000 0x00000040<br/> | Der Text im-Steuerelement wird linksbündig ausgerichtet. Der Text im-Steuerelement wird rechtsbündig ausgerichtet.<br/>                                                                                                                                                                                                                                                                       |
| [Leftscroll](leftscroll-control-attribute.md)                     | 0x00000000 0x00000080<br/> | Die Scrollleiste befindet sich auf der rechten Seite des-Steuer Elements. Die Scrollleiste befindet sich auf der linken Seite des-Steuer Elements.<br/>                                                                                                                                                                                                                                         |
| [Bidi-Steuerelement](bidi-control-attribute.md)                         | 0x000000e0                       | Legen Sie diesen Wert für eine Kombination der Attribute [rtlro](rtlro-control-attribute.md), [rightausgerichtete](rightaligned-control-attribute.md)und [leftscroll](leftscroll-control-attribute.md) fest.                                                                                                                                                                          |



 

## <a name="remarks"></a>Bemerkungen

Dieses Steuerelement kann \_ über die ListView-Klasse von WC mithilfe der Funktion "up- [**windowex**](/windows/win32/api/winuser/nf-winuser-createwindowexa) " erstellt werden. Sie enthält die **LVS- \_ Liste**, **LVS \_ EditLabels**, **WS \_ VScroll**, **LVS \_ shareimagelists**, **LVS \_ AutoArrange**, **LVS \_ SingleSel**, **WS \_ Border**, **LVS \_ SortAscending**, **WS \_ Child**, **WS \_ Group** und **WS \_ Tabstopp** Styles.

Mit diesem Steuerelement kann der Benutzer einen Unterordner der aktuellen Auswahl auswählen. Mit zusätzlichen Schaltflächen ermöglicht es dem Benutzer auch, einen neuen Ordner in der aktuellen Auswahl auszuwählen oder eine Ebene im Pfad zu Stufen. Wenn der Benutzer die Schaltfläche **neuen Ordner erstellen** in einem Ordner auswählt, in dem bereits ein neuer Ordner vorhanden ist, wird kein zweiter neuer Ordner erstellt, und der vorhandene Name des neuen Ordners wird zur Bearbeitung ausgewählt.

 

