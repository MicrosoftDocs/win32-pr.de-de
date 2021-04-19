---
description: Mithilfe von Steuerelementen und Text, die in Dialogfeldern und in den Dialogfeldern platziert werden, kann der Benutzer mit dem Installationsvorgang interagieren
ms.assetid: 2c6204c7-535d-4dda-8394-723ddbf46b96
title: Hinzufügen von Steuerelementen und Text
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 706d071741d742205d0df2b19c4416acf355fd7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360221"
---
# <a name="adding-controls-and-text"></a>Hinzufügen von Steuerelementen und Text

Mithilfe von Steuerelementen und Text, die in Dialogfeldern und in den Dialogfeldern platziert werden, kann der Benutzer mit dem Installationsvorgang interagieren Fügen Sie der Benutzeroberfläche ein Dialogfeld hinzu, indem Sie es in die [Dialogfeld Tabelle](dialog-table.md) einschließen, wie unter [Verwenden der Benutzeroberfläche](using-the-user-interface.md)beschrieben. Füllen Sie Dialogfelder und Plakate mit Steuerelementen aus, indem Sie die [Steuerelement Tabelle](control-table.md) bzw. die [Tabelle "bbcontrol](bbcontrol-table.md)" auffüllen.

Die anfänglichen Attribute des Steuer Elements können in der Spalte Attribute der Steuerelement [Tabelle](control-table.md)angegeben werden. Siehe [Steuerelement Attribute](control-attributes.md).

Um Steuerelement Attribute von einer Bedingung abhängig zu machen, verwenden Sie die [Tabelle "ControlCondition](controlcondition-table.md) ", um ein Steuerelement entsprechend dem Wert einer Eigenschaft oder Bedingungs Anweisung zu deaktivieren, zu aktivieren, auszublenden oder anzuzeigen. Sie können diese Tabelle auch verwenden, um die Angabe des in die [Dialog Feld Tabelle](dialog-table.md)eingegebenen Standard Steuer Elements zu überschreiben.

Damit ein Ereignis ein Steuerelement Attribut ändern kann, abonnieren Sie das Steuerelement einem ControlEvent in der [Tabelle EventMapping](eventmapping-table.md). Ein ControlEvent gibt eine Aktion an, die vom Installationsprogramm ausgeführt werden soll, oder eine Änderung der Attribute eines oder mehrerer Steuerelemente im Dialogfeld. Weitere Informationen finden Sie unter [ControlEvent Overview](controlevent-overview.md). Geben Sie den Bezeichner des Attributs in der Spalte Attribut und den Bezeichner von ControlEvent in der Spalte Ereignis der [Tabelle EventMapping](eventmapping-table.md)ein.

Einige Steuerelemente erleichtern das Sammeln von Informationen vom Benutzer. Beispielsweise kann der Benutzer mithilfe eines Kontrollkästchens den Wert einer Eigenschaft festlegen. Weitere Informationen finden Sie in den [Kontrollkästchen Tabelle](checkbox-table.md), [ComboBox](combobox-table.md)-Tabelle, [ListBox](listbox-table.md)-Tabelle, [RadioButton-Tabelle](radiobutton-table.md)und [ListView-Tabelle](listview-table.md).

Beachten Sie, dass private Eigenschaften aus Sicherheitsgründen von dem Benutzer, der mit der Benutzeroberfläche interagiert, nicht geändert werden können. Wenn eine Eigenschaft von der Benutzeroberfläche festgelegt werden soll, muss Sie eine öffentliche Eigenschaft sein und in Großbuchstaben einen Namen haben. Siehe [Informationen zu Eigenschaften](about-properties.md).

Sie können das Dialogfeld zum Anzeigen von Informationen für den Benutzer oder zum Schreiben in ein Protokoll als Antwort auf Installations Aktionen durch Ausfüllen der [Tabelle "aktiontext](actiontext-table.md)" machen.

Steuerelemente können über ein vordefiniertes Schriftformat verfügen. Um die Schriftart und den Schrift Schnitt einer Text Zeichenfolge festzulegen, stellen Sie die Zeichenfolge der angezeigten Zeichen mit "{ \\ Style}" oder "{&*Style*}" vor. Dabei ist Style ein Bezeichner, der in der TextStyle-Spalte der [TextStyle-Tabelle](textstyle-table.md)aufgeführt ist. Wenn keines dieser beiden vorhanden ist, die [**defaultuifont**](defaultuifont.md) -Eigenschaft jedoch als gültiger Textstil definiert ist, wird diese Schriftart verwendet.

Es wird empfohlen, die [**defaultuifont**](defaultuifont.md) -Eigenschaft jedes Installationspakets mit einer Benutzeroberfläche in der [Eigenschaften Tabelle](property-table.md) auf einen der vordefinierten Stile in der [TextStyle-Tabelle](textstyle-table.md)festzulegen. Wenn diese Eigenschaft nicht angegeben wird, verwendet das Installationsprogramm die System Schriftart. Dies kann dazu führen, dass das Installationsprogramm Text Zeichenfolgen nicht ordnungsgemäß anzeigt, wenn sich die Codepage des Pakets von der standardmäßigen UI-Codepage des Benutzers unterscheidet.

Bei den meisten Steuerelementen wird Text unter Verwendung des Zeichensatzes angezeigt, der von der Codepage der Datenbank angegeben wird. Dadurch wird sichergestellt, dass der richtige Zeichensatz mit den in der Datenbank enthaltenen Informationen verwendet wird. Ausgenommen hiervon sind die Steuerelemente " [Edit](edit-control.md)", " [Director List](directorylist-control.md)", " [pathedit](pathedit-control.md)" und " [directerycombo](directorycombo-control.md) ", die immer Text mit dem standardmäßigen Benutzeroberflächen-Zeichensatz anzeigen. Die Steuerelemente [Text](text-control.md), [ListBox](listbox-control.md)und [ComboBox](combobox-control.md) verwenden den standardmäßigen Benutzeroberflächen-Zeichensatz des Benutzers, wenn das [userslanguage-Steuerelement Attribut](userslanguage-control-attribute.md) festgelegt ist.

In einigen Fällen wird ein Steuerelement möglicherweise falsch neu gezeichnet, wenn ein Dialogfeld abgebrochen wird. Dies muss mit der Reihenfolge geschehen, in der die Steuerelemente \_ nach dem Entfernen des Dialog Felds **Abbrechen** eine WM-Paint-Nachricht empfangen. Um dieses Problem zu beheben, versuchen Sie, die Reihenfolge der Steuerelemente in der Steuerelement Tabelle zu ändern.

Steuerelemente sollten groß genug gemacht werden, um den gesamten Text zu berücksichtigen, der in allen Schriftart Größen Einstellungen angezeigt wird. Steuerelemente sollten groß genug für den gesamten lokalisierten Text erstellt werden, wenn der Text in der Benutzeroberfläche lokalisiert werden kann. Größere Schriftgrößen oder lokalisierte Text können mehr Platz als der ursprüngliche Text erfordern und können von einem zu kleinen Steuerelement abgeschnitten werden. Weitere Informationen zum Lokalisieren von Benutzeroberflächen Text finden Sie im Abschnitt: [ein Lokalisierungs Beispiel](a-localization-example.md).

 

 



