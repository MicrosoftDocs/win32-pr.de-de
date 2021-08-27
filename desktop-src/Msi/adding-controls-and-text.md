---
description: Steuerelemente und Text, die in Dialogfeldern und Werbeelementen platziert werden, ermöglichen es dem Benutzer, mit dem Installationsprozess zu interagieren.
ms.assetid: 2c6204c7-535d-4dda-8394-723ddbf46b96
title: Hinzufügen von Steuerelementen und Text
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58602c4d793b25e1670373773ac8d3f5be2399c6351e56ebe2de1579c78ddcc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046030"
---
# <a name="adding-controls-and-text"></a>Hinzufügen von Steuerelementen und Text

Steuerelemente und Text, die in Dialogfeldern und Werbeelementen platziert werden, ermöglichen es dem Benutzer, mit dem Installationsprozess zu interagieren. Fügen Sie der Benutzeroberfläche ein Dialogfeld hinzu, indem Sie es wie unter [Verwenden des Benutzeroberfläche](using-the-user-interface.md)beschrieben in die Tabelle [Dialog](dialog-table.md) einfügen. Füllen Sie Dialogfelder und Fenster mit Steuerelementen, indem Sie die [Tabelle Control](control-table.md) bzw. [die BBControl-Tabelle](bbcontrol-table.md)auffüllen.

Die anfänglichen Attribute des Steuerelements können in der Attributes -Spalte der [Control-Tabelle](control-table.md)angegeben werden. Weitere Informationen finden Sie unter [Steuerelementattribute.](control-attributes.md)

Um Steuerelementattribute von einer Bedingung abhängig zu machen, verwenden Sie die [ControlCondition-Tabelle,](controlcondition-table.md) um ein Steuerelement entsprechend dem Wert einer Eigenschaft oder bedingten Anweisung zu deaktivieren, zu aktivieren, auszublenden oder anzuzeigen. Sie können diese Tabelle auch verwenden, um die Spezifikation des in die [Dialogtabelle](dialog-table.md)eingegebenen Standardsteuerelements zu überschreiben.

Damit ein Ereignis ein Steuerelementattribut ändert, abonnieren Sie das Steuerelement in der [EventMapping-Tabelle](eventmapping-table.md)auf ein ControlEvent. Ein ControlEvent gibt eine Aktion an, die vom Installationsprogramm ausgeführt werden soll, oder eine Änderung der Attribute eines oder mehrerer Steuerelemente im Dialogfeld. Weitere Informationen finden Sie [unter Übersicht über ControlEvent.](controlevent-overview.md) Geben Sie den Bezeichner des Attributs in der Spalte Attribute und den Bezeichner von ControlEvent in der Spalte Event der [EventMapping-Tabelle](eventmapping-table.md)ein.

Einige Steuerelemente erleichtern das Sammeln von Informationen vom Benutzer. Mit einem Kontrollkästchen kann der Benutzer beispielsweise den Wert einer Eigenschaft festlegen. Sehen Sie sich die [CheckBox-Tabelle,](checkbox-table.md)die [ComboBox-Tabelle,](combobox-table.md)die [ListBox-Tabelle,](listbox-table.md)die [RadioButton-Tabelle](radiobutton-table.md)und die [ListView-Tabelle](listview-table.md)an.

Beachten Sie, dass private Eigenschaften aus Sicherheitsgründen nicht vom Benutzer geändert werden können, der mit der Benutzeroberfläche interagiert. Wenn eine Eigenschaft von der Benutzeroberfläche festgelegt werden soll, muss sie eine öffentliche Eigenschaft sein und in Großbuchstaben einen Namen aufweisen. Weitere Informationen finden Sie unter [Informationen zu Eigenschaften.](about-properties.md)

Sie können das Dialogfeld entweder so gestalten, dass dem Benutzer Informationen angezeigt werden, oder sie als Reaktion auf Installationsaktionen in ein Protokoll schreiben, indem Sie die [ActionText-Tabelle](actiontext-table.md)ausfüllen.

Steuerelemente können einen vordefinierten Schriftschnitt aufweisen. Um die Schriftart und den Schriftschnitt einer Textzeichenfolge festzulegen, stellen Sie der Zeichenfolge der angezeigten Zeichen { \\ style} oder {&*Format*} voran. Wobei style ein Bezeichner ist, der in der TextStyle-Spalte der [TextStyle-Tabelle](textstyle-table.md)aufgeführt ist. Wenn keine dieser Eigenschaften vorhanden ist, die [**DefaultUIFont-Eigenschaft**](defaultuifont.md) jedoch als gültiger Textstil definiert ist, wird diese Schriftart verwendet.

Es wird empfohlen, die [**DefaultUIFont-Eigenschaft**](defaultuifont.md) jedes Installationspakets mit einer Benutzeroberfläche in der [Tabelle Property](property-table.md) auf einen der vordefinierten Stile festzulegen, die in der [TextStyle-Tabelle](textstyle-table.md)aufgeführt sind. Wenn diese Eigenschaft nicht angegeben ist, verwendet das Installationsprogramm die Schriftart System. Dies kann dazu führen, dass das Installationsprogramm Textzeichenfolgen nicht ordnungsgemäß anzeigt, wenn sich die Codepage des Pakets von der Standardcodepage der Benutzeroberfläche des Benutzers unterscheidet.

Für die meisten Steuerelemente wird Text mithilfe des Zeichensatzes angezeigt, der von der Codepage der Datenbank angegeben wird. Dadurch wird sichergestellt, dass der richtige Zeichensatz mit den in der Datenbank enthaltenen Informationen verwendet wird. Ausnahmen sind die Steuerelemente [Edit](edit-control.md), [DirectoryList,](directorylist-control.md) [PathEdit](pathedit-control.md)und [DirectoryCombo,](directorycombo-control.md) die text immer mithilfe des Standardzeichensatzes der Benutzeroberfläche des Benutzers anzeigen. Die Steuerelemente [Text,](text-control.md) [ListBox](listbox-control.md)und [ComboBox](combobox-control.md) verwenden den Standardzeichensatz der Benutzeroberfläche des Benutzers, wenn das [UsersLanguage-Steuerelementattribut](userslanguage-control-attribute.md) festgelegt ist.

In einigen Fällen wird ein Steuerelement möglicherweise falsch neu gezeichnet, wenn ein Dialogfeld abgebrochen wird. Dies hat mit der Reihenfolge zu tun, in der die Steuerelemente WM PAINT-Meldungen empfangen, \_ nachdem das Dialogfeld **Abbrechen** entfernt wurde. Versuchen Sie, die Reihenfolge der Steuerelemente in der Control-Tabelle zu ändern, um dies zu beheben.

Steuerelemente sollten groß genug sein, um den gesamten Text aufzunehmen, der in allen Schriftgradeinstellungen angezeigt wird. Steuerelemente sollten groß genug sein, um den gesamten lokalisierten Text aufzunehmen, wenn der Text auf der Benutzeroberfläche lokalisiert werden kann. Größere Schriftgrade oder lokalisierter Text können mehr Platz als der ursprüngliche Text erfordern und durch ein Steuerelement abgeschnitten werden, das zu klein ist. Weitere Informationen zum Lokalisieren von Benutzeroberflächentext finden Sie im [Abschnitt: Ein Lokalisierungsbeispiel.](a-localization-example.md)

 

 



