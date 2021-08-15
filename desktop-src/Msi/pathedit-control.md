---
description: Das PathEdit-Steuerelement zeigt ein Bearbeitungsfeld an, mit dem ein Benutzer den Endabschnitt eines Pfads auswählen kann.
ms.assetid: 074ef4d5-3ac1-4bdb-90c5-9798d89a749f
title: PathEdit-Steuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ed7655cc893c30f417c9a7ef374eb6d4ade10dfd618ca328e1be2fc7a0e0a9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118377613"
---
# <a name="pathedit-control"></a>PathEdit-Steuerelement

Das PathEdit-Steuerelement zeigt ein Bearbeitungsfeld an, mit dem ein Benutzer den Endabschnitt eines Pfads auswählen kann. Dieses Steuerelement unterstützt die Eingabe des ausgewählten Ordnernamens oder des gesamten Pfads in das Bearbeitungsfeld. Ein Benutzer kann auch einen Universal Naming Convention (UNC) zu einem Laufwerk ohne Laufwerkbuchstaben eingeben. Wenn der Benutzer ein Endsegment für den Pfad ein gibt, der für das aktuelle Volume ungültig ist, kann das PathEdit-Steuerelement den Fokus nicht auf das nächste Steuerelement übertragen.

Die Steuerelemente PathEdit, [DirectoryCombo](directorycombo-control.md)und [DirectoryList](directorylist-control.md) sind derselben Zeichenfolgenwerteigenschaft zugeordnet. Diese Eigenschaft ist der vom Benutzer ausgewählte Pfad. Geben Sie den Namen der Eigenschaft in die Spalte Eigenschaft der [Control-Tabelle ein.](control-table.md) Diese Eigenschaft muss über einen Anfangswert verfügen, der mindestens ein Volume und eine Unterebene enthält. Geben Sie den Anfangswert für die Eigenschaft in der Spalte Wert der [Property -Tabelle an.](property-table.md)

Dieses Steuerelement ist für die Verwendung in einem [Dialogfeld zum](browse-dialog.md) Durchsuchen zusammen mit den Steuerelementen PathEdit [und DirectoryList](directorylist-control.md) vorgesehen.

## <a name="control-attributes"></a>Steuerelementattribute

Sie können die folgenden Attribute mit diesem Steuerelement verwenden. Um den Wert eines Attributs mithilfe eines Ereignisses zu ändern, abonnieren Sie das Steuerelement für ein ControlEvent in der [EventMapping-Tabelle,](eventmapping-table.md) und listen Sie den Bezeichner des Attributs in der Spalte Attribut auf. Geben Sie den Bezeichner des ControlEvents in der Spalte Ereignis ein.



| Attributbezeichner                                               | Hexadezimales Bit                  | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IndirectPropertyName](indirectpropertyname-control-attribute.md) |                                  | Dies ist der Name einer indirekten Eigenschaft, die dem Steuerelement zugeordnet ist. Wenn das Indirekte Attributbit festgelegt ist, zeigt das Steuerelement den Wert der Eigenschaft mit diesem Namen an oder ändert diesen. Wenn das Indirekte Attributbit festgelegt ist, ist dieser Name auch der Wert der Eigenschaft, die in der Property -Spalte der [Control-Tabelle aufgeführt ist.](control-table.md)                                                                                                                                                                              |
| [Position](position-control-attribute.md)                         |                                  | Position des Steuerelements im Dialogfeld. Geben Sie die Breite, Höhe und Koordinaten der linken Ecke des Steuerelements in die Spalten Width, Height, X und Y der [Tabelle Control ein.](control-table.md) Verwenden [Sie Installationseinheiten](installer-units.md) für Länge und Entfernung.<br/>                                                                                                                                                                                                                                   |
| [PropertyName](propertyname-control-attribute.md)                 |                                  | Dies ist der Name der Eigenschaft, die diesem Steuerelement zugeordnet ist. Wenn das Indirekte Attributbit nicht festgelegt ist, zeigt das Steuerelement den Wert der Eigenschaft mit diesem Namen an oder ändert diesen. Dieses Attribut wird in der Property -Spalte der [Control-Tabelle angegeben.](control-table.md)                                                                                                                                                                                                                                              |
| [PropertyValue](propertyvalue-control-attribute.md)               |                                  | Der aktuelle Wert der Eigenschaft, die von diesem Steuerelement angezeigt oder geändert wird. Wenn das Indirekte Attributbit nicht festgelegt ist, ist dies der Wert von PropertyName. Wenn das Indirekte Attributbit festgelegt ist, ist dies der Wert von IndirectPropertyName. Wenn sich das Attribut ändert, spiegelt das Steuerelement den neuen Wert wider.                                                                                                                                                                                                                                 |
| [Text](text-control-attribute.md)                                 |                                  | Stellen Sie der Zeichenfolge der angezeigten Zeichen { style} oder {&style} voran, um die Schriftart und den \\ Schriftschnitt einer Textzeichenfolge zu setzen. Dabei ist style ein Bezeichner, der in der TextStyle -Spalte der [TextStyle-Tabelle aufgeführt ist.](textstyle-table.md) Wenn keines dieser Eigenschaften vorhanden ist, die [**DefaultUIFont-Eigenschaft**](defaultuifont.md) jedoch als gültiger Textstil definiert ist, wird diese Schriftart verwendet. Um die Anzahl der Zeichen anzugeben, die der Benutzer eingeben kann, fügen Sie {n} nach allen Schriftartspezifikationen an, wobei n eine positive ganze Zahl ist.<br/> |
| [Visible](visible-control-attribute.md)                           | 0x00000000 0x00000001<br/> | Ausgeblendetes Steuerelement. Sichtbares Steuerelement.<br/> Fügen Sie dieses Bit in das Bitwort der Attributes -Spalte in die [Control-Tabelle](control-table.md) ein, um das Steuerelement bei seiner Erstellung sichtbar oder ausgeblendet zu machen.<br/> Sie können ein Steuerelement auch mithilfe der [ControlCondition-Tabelle ausblenden oder anzeigen.](controlcondition-table.md)<br/>                                                                                                                                                                                           |
| [Aktiviert](enabled-control-attribute.md)                           | 0x00000000 0x00000002<br/> | Steuerelement in einem deaktivierten Zustand. Steuerelement in einem aktivierten Zustand.<br/> Fügen Sie dieses Bit in das Bitwort in die Spalte Attribute des [Steuerelements](control-table.md) ein, um das Steuerelement bei der Erstellung zu aktivieren.<br/> Sie können ein Steuerelement auch mithilfe der [ControlCondition-Tabelle aktivieren oder deaktivieren.](controlcondition-table.md)<br/>                                                                                                                                                                                         |
| [Sunken](sunken-control-attribute.md)                             | 0x00000000 0x00000004<br/> | Zeigt den standardmäßigen visuellen Stil an. Zeigt das Steuerelement mit einem versenkten 3D-Look an.<br/> Schließen Sie diese Bits in das Bitwort in die Spalte Attribute der [Control-Tabelle ein.](control-table.md)<br/>                                                                                                                                                                                                                                                                                                                  |
| [Indirekt](indirect-control-attribute.md)                         | 0x00000000 0x00000008<br/> | Das -Steuerelement zeigt den Wert der -Eigenschaft in der Property -Spalte der [Control-Tabelle](control-table.md)an oder ändert diesen. Das -Steuerelement zeigt den Wert der Eigenschaft an, in der der Bezeichner in der Spalte Eigenschaft der Control-Tabelle aufgeführt ist, oder ändert diesen.<br/> Bestimmt, ob indirekt auf die diesem Steuerelement zugeordnete Eigenschaft verwiesen wird.<br/>                                                                                                                                                       |
| [RTLRO](rtlro-control-attribute.md)                               | 0x00000000 0x00000020<br/> | Text im Steuerelement wird in der Lese reihenfolge von links nach rechts angezeigt. Text im Steuerelement wird in der Lese reihenfolge von rechts nach links angezeigt.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| [RightAligned](rightaligned-control-attribute.md)                 | 0x00000000 0x00000040<br/> | Text im Steuerelement wird linksbündig ausgerichtet. Text im Steuerelement wird rechtsbündig ausgerichtet.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="remarks"></a>Hinweise

Das PathEdit-Steuerelement wird vom [Edit-Steuerelement](edit-control.md) abgeleitet.

Zur Kompatibilität mit sprachaktiven Bildschirmen müssen Sie beim Erstellen eines Dialogfelds mit einem PathEdit-Steuerelement als erstes aktives Steuerelement das Textfeld, das zum Bearbeitungsfeld gehört, zum ersten aktiven Steuerelement in der [Tabelle Dialog machen.](dialog-table.md) Da der statische Text den Fokus nicht übernehmen kann, hat das Bearbeitungsfeld beim Erstellen des Dialogfelds anfänglich den Fokus. Dadurch wird sichergestellt, dass die Sprachbildschirme die richtigen Informationen anzeigen.

 

 




