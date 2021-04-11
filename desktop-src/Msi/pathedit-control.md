---
description: Das Steuerelement "pathedit" zeigt ein Bearbeitungsfeld an, das es einem Benutzer ermöglicht, den Endabschnitt eines Pfades auszuwählen.
ms.assetid: 074ef4d5-3ac1-4bdb-90c5-9798d89a749f
title: Pathedit-Steuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65d1237199f202e6c674ab4526ccd4747b02c09b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104216035"
---
# <a name="pathedit-control"></a>Pathedit-Steuerelement

Das Steuerelement "pathedit" zeigt ein Bearbeitungsfeld an, das es einem Benutzer ermöglicht, den Endabschnitt eines Pfades auszuwählen. Dieses Steuerelement unterstützt das Eingeben des ausgewählten Ordner namens oder des gesamten Pfads im Bearbeitungsfeld. Ein Benutzer kann auch einen Universal Naming Convention (UNC)-Pfad zu einem Laufwerk ohne Laufwerk Buchstaben eingeben. Wenn der Benutzer ein Endsegment für den Pfad eingibt, der für das aktuelle Volume ungültig ist, kann das pathedit-Steuerelement den Fokus nicht auf das nächste Steuerelement übertragen.

Die Steuerelemente "pathedit", " [Director ycombo](directorycombo-control.md)" und " [Directoren List](directorylist-control.md) " sind der gleichen Zeichen folgen Wert Eigenschaft zugeordnet. Diese Eigenschaft ist der vom Benutzer ausgewählte Pfad. Geben Sie den Namen der Eigenschaft in die Eigenschafts Spalte der [Steuerelement Tabelle](control-table.md)ein. Diese Eigenschaft muss über einen Anfangswert mit mindestens einem Volume und einer Unterebene verfügen. Geben Sie den Anfangswert für die Eigenschaft in der Spalte Wert der [Eigenschaften Tabelle](property-table.md)an.

Dieses Steuerelement ist für die Verwendung in einem [Dialog Feld zum Durchsuchen](browse-dialog.md) in Verbindung mit den Steuerelementen "pathedit" und " [Directoren List](directorylist-control.md) " vorgesehen.

## <a name="control-attributes"></a>Steuerelement Attribute

Mit diesem Steuerelement können Sie die folgenden Attribute verwenden. Um den Wert eines Attributs mithilfe eines Ereignisses zu ändern, abonnieren Sie das Steuerelement einem ControlEvent in der [EventMapping-Tabelle](eventmapping-table.md) , und Listen Sie den Bezeichner des Attributs in der Attribut-Spalte auf. Geben Sie den Bezeichner des ControlEvent in der Ereignis Spalte ein.



| Attribut Bezeichner                                               | Hexadezimales Bit                  | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Derekpropertyname](indirectpropertyname-control-attribute.md) |                                  | Dies ist der Name einer indirekten Eigenschaft, die dem Steuerelement zugeordnet ist. Wenn das indirekte Attribut Bit festgelegt ist, zeigt das Steuerelement den Wert der Eigenschaft mit diesem Namen an oder ändert ihn. Wenn das indirekte Attribut Bit festgelegt ist, ist dieser Name auch der Wert der Eigenschaft, die in der Eigenschafts Spalte der [Steuerelement Tabelle](control-table.md)aufgeführt ist.                                                                                                                                                                              |
| [Position](position-control-attribute.md)                         |                                  | Position des-Steuer Elements im Dialogfeld. Geben Sie die Breite, Höhe und Koordinaten der Steuerelemente der linken Ecke des Steuer Elements in die Spalten Width, Height, X und Y der [Steuerelement Tabelle](control-table.md)ein. Verwenden Sie die [Installer-Einheiten](installer-units.md) für Länge und Entfernung.<br/>                                                                                                                                                                                                                                   |
| [PropertyName](propertyname-control-attribute.md)                 |                                  | Dies ist der Name der Eigenschaft, die diesem Steuerelement zugeordnet ist. Wenn das indirekte Attribut Bit nicht festgelegt ist, zeigt das Steuerelement den Wert der Eigenschaft mit diesem Namen an oder ändert ihn. Dieses Attribut wird in der-Eigenschaften Spalte der [Steuerelement Tabelle](control-table.md)angegeben.                                                                                                                                                                                                                                              |
| [PropertyValue](propertyvalue-control-attribute.md)               |                                  | Aktueller Wert der Eigenschaft, die von diesem Steuerelement angezeigt oder geändert wird. Wenn das indirekte Attribut Bit nicht festgelegt ist, ist dies der Wert von PropertyName. Wenn das indirekte Attribut Bit festgelegt ist, ist dies der Wert von deretpropertyname. Wenn sich das Attribut ändert, spiegelt das-Steuerelement den neuen Wert wider.                                                                                                                                                                                                                                 |
| [Text](text-control-attribute.md)                                 |                                  | Um die Schriftart und den Schrift Schnitt einer Text Zeichenfolge festzulegen, stellen Sie die Zeichenfolge der angezeigten Zeichen mit "{ \\ Style}" oder "{&Style}" vor. Dabei ist Style ein Bezeichner, der in der TextStyle-Spalte der [TextStyle-Tabelle](textstyle-table.md)aufgeführt ist. Wenn keines dieser beiden vorhanden ist, die [**defaultuifont**](defaultuifont.md) -Eigenschaft jedoch als gültiger Textstil definiert ist, wird diese Schriftart verwendet. Fügen Sie zum Angeben der Anzahl von Zeichen, die der Benutzer eingeben kann, {n} nach allen Schriftart Spezifikationen an, wobei n eine positive ganze Zahl ist.<br/> |
| [Visible](visible-control-attribute.md)                           | 0x00000000 0x00000001<br/> | Verborgenes Steuerelement. Sichtbares Steuerelement.<br/> Fügen Sie dieses Bit in das bitwort der Attributspalte in der [Steuerelement Tabelle](control-table.md) ein, damit das Steuerelement bei der Erstellung sichtbar oder ausgeblendet wird.<br/> Sie können ein Steuerelement auch mithilfe der [Tabelle "ControlCondition](controlcondition-table.md)" ausblenden oder anzeigen.<br/>                                                                                                                                                                                           |
| [Aktiviert](enabled-control-attribute.md)                           | 0x00000000 0x00000002<br/> | Steuerelement in deaktiviertem Zustand. Steuerelement im aktivierten Zustand.<br/> Fügen Sie dieses Bit in das bitwort in die Spalte Attribute des [Steuer](control-table.md) Elements ein, um das Steuerelement bei der Erstellung zu aktivieren.<br/> Sie können ein Steuerelement auch mithilfe der [Tabelle "ControlCondition](controlcondition-table.md)" aktivieren oder deaktivieren.<br/>                                                                                                                                                                                         |
| [Sunken](sunken-control-attribute.md)                             | 0x00000000 0x00000004<br/> | Zeigt den visuellen Standardstil an. Zeigt das Steuerelement mit einem abgesenkten 3D-Bild an.<br/> Fügen Sie diese Bits in das bitwort in die Spalte Attribute der [Steuerelement Tabelle](control-table.md)ein.<br/>                                                                                                                                                                                                                                                                                                                  |
| [Indirekt](indirect-control-attribute.md)                         | 0x00000000 0x00000008<br/> | Das-Steuerelement zeigt den Wert der-Eigenschaft in der-Eigenschaften Spalte der [Steuerelement Tabelle](control-table.md)an oder ändert ihn. Das-Steuerelement zeigt den Wert der-Eigenschaft an oder ändert den Wert der-Eigenschaft, die den Bezeichner enthält<br/> Bestimmt, ob indirekt auf die diesem Steuerelement zugeordnete Eigenschaft verwiesen wird.<br/>                                                                                                                                                       |
| [Rtlro](rtlro-control-attribute.md)                               | 0x00000000 0x00000020<br/> | Der Text im Steuerelement wird in der Lesefolge von links nach rechts angezeigt. Der Text im Steuerelement wird in der Lesefolge von rechts nach links angezeigt.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| [Rechtsbündig](rightaligned-control-attribute.md)                 | 0x00000000 0x00000040<br/> | Der Text im-Steuerelement wird linksbündig ausgerichtet. Der Text im-Steuerelement wird rechtsbündig ausgerichtet.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="remarks"></a>Bemerkungen

Das pathedit-Steuerelement wird vom [Bearbeitungs](edit-control.md) Steuerelement abgeleitet.

Aus Gründen der Kompatibilität mit Sprachausgaben müssen Sie beim Erstellen eines Dialog Felds mit einem pathedit-Steuerelement als erstes aktives Steuerelement das Textfeld, das zum Bearbeitungsfeld gehört, zum ersten aktiven Steuerelement in der [Dialogfeld Tabelle](dialog-table.md)machen. Da der statische Text beim Erstellen des Dialog Felds nicht den Fokus haben kann, hat das Bearbeitungsfeld den Fokus anfänglich. Dadurch wird sichergestellt, dass Bildschirm Sprachausgaben die richtigen Informationen anzeigen.

 

 




