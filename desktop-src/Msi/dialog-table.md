---
description: Die Dialog Feld Tabelle enthält alle Dialogfelder, die in der Benutzeroberfläche (User Interface, UI) im vollständigen und reduzierten Modus angezeigt werden.
ms.assetid: 981386dd-4fee-4003-8c62-16933cc5bd14
title: Dialog Feld Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09a210ad051eec950dcff8f8f940a1df11bf74c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866340"
---
# <a name="dialog-table"></a>Dialog Feld Tabelle

Die Dialog Feld Tabelle enthält alle Dialogfelder, die in der Benutzeroberfläche (User Interface, UI) im vollständigen und reduzierten Modus angezeigt werden.

Die Dialog Feld Tabelle enthält die folgenden Spalten.



| Spalte           | Typ                               | Schlüssel | Nullwerte zulässig |
|------------------|------------------------------------|-----|----------|
| Dialog           | [Bezeichner](identifier.md)       | J   | N        |
| Hcentering       | [Integer](integer.md)             | N   | N        |
| Vcentering       | [Integer](integer.md)             | N   | N        |
| Breite            | [Integer](integer.md)             | N   | N        |
| Höhe           | [Integer](integer.md)             | N   | N        |
| Attribute       | [Doubleiteger](doubleinteger.md) | N   | J        |
| Titel            | [Großformatige](formatted.md)         | N   | J        |
| \_Zuerst Steuern   | [Bezeichner](identifier.md)       | N   | N        |
| Standard Steuerelement \_ | [Bezeichner](identifier.md)       | N   | J        |
| Abbrechen von Steuerelementen \_  | [Bezeichner](identifier.md)       | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Dialog"></span><span id="dialog"></span><span id="DIALOG"></span>Dialog
</dt> <dd>

Der Primärschlüssel und der Name des Dialog Felds.

</dd> <dt>

<span id="HCentering"></span><span id="hcentering"></span><span id="HCENTERING"></span>Hcentering
</dt> <dd>

Die horizontale Position des Dialog Felds.

Der Bereich liegt zwischen 0 und 100, wobei 0 am linken Rand des Bildschirms und 100 am rechten Rand liegt.

</dd> <dt>

<span id="VCentering"></span><span id="vcentering"></span><span id="VCENTERING"></span>Vcentering
</dt> <dd>

Die vertikale Position des Dialog Felds.

Der Bereich liegt zwischen 0 und 100, wobei 0 am oberen Rand des Bildschirms und 100 am unteren Rand liegt.

</dd> <dt>

<span id="Width"></span><span id="width"></span><span id="WIDTH"></span>Breite
</dt> <dd>

Die Breite der rechteckigen Grenze des Dialog Felds.

Diese Zahl darf nicht negativ sein.

</dd> <dt>

<span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>Flugh
</dt> <dd>

Die Höhe der rechteckigen Grenze des Dialog Felds.

Diese Zahl darf nicht negativ sein.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Legt
</dt> <dd>

Ein 32-Bit-Wort, das die Attributflags angibt, die auf dieses Dialogfeld angewendet werden sollen.

Diese Zahl darf nicht negativ sein. Weitere Informationen finden Sie unter [Dialog](dialog-style-bits.md)Feld "Bits".

</dd> <dt>

<span id="Title"></span><span id="title"></span><span id="TITLE"></span>Tel
</dt> <dd>

Eine lokalisierbare Text Zeichenfolge, die den Titel angibt, der in der Titelleiste des Dialog Felds angezeigt werden soll.

</dd> <dt>

<span id="Control_First"></span><span id="control_first"></span><span id="CONTROL_FIRST"></span>\_Zuerst Steuern
</dt> <dd>

Ein externer Schlüssel für die zweite Spalte der [Steuerelement Tabelle](control-table.md).

Durch kombinieren dieses Felds mit dem Dialogfeld wird ein eindeutiges Steuerelement in der [Steuerelement Tabelle](control-table.md) angegeben, das den Fokus erhält, wenn das Dialogfeld geöffnet wird. In der Regel kann dies ein [Bearbeitungs Steuer](edit-control.md)Element, ein [SelectionTree-Steuer](selectiontree-control.md)Element oder ein beliebiges anderes Steuerelement sein, das den Fokus nehmen kann. Wenn das [PUSHBUTTON-Steuer](pushbutton-control.md) Element das einzige Steuerelement ist, das im Dialogfeld vorhanden ist, das den Fokus übernehmen kann, muss auch das im Feld "controldefault" eingegebene PUSHBUTTON in das erste Feld des Steuer Elements eingegeben werden. Diese Spalte wird in einem [Fehler Dialogfeld](error-dialog.md) ignoriert.

Da statischer Text keinen Fokus haben kann, muss ein [Text Steuer](text-control.md) Element, das ein [Bearbeitungs Steuer](edit-control.md)Element, das [pathedit-Steuer](pathedit-control.md)Element, das [ListView-Steuer](listview-control.md)Element, das [ComboBox-Steuer](combobox-control.md) Element oder das [volumeselectcombo-Steuer](volumeselectcombo-control.md) Element beschreibt, das erste Steuerelement im Dialogfeld sein, damit die Kompatibilität mit

</dd> <dt>

<span id="Control_Default"></span><span id="control_default"></span><span id="CONTROL_DEFAULT"></span>Standard Steuerelement \_
</dt> <dd>

Ein externer Schlüssel für die zweite Spalte der [Steuerelement Tabelle](control-table.md).

Das Kombinieren dieses Felds mit dem Dialogfeld gibt das Standard Steuerelement an, das den Fokus erhält, wenn das Dialogfeld geöffnet wird. In der Regel kann dies ein [PUSHBUTTON-Steuer](pushbutton-control.md)Element sein. Wenn kein PUSHBUTTON-Steuerelement im Dialogfeld den Fokus hat, entspricht die Rückgabetaste dem Klicken auf das Standard Steuerelement. Wenn diese Spalte leer bleibt, gibt es kein Standard Steuerelement. Diese Spalte wird in einem [Fehler Dialogfeld](error-dialog.md) ignoriert.

</dd> <dt>

<span id="Control_Cancel"></span><span id="control_cancel"></span><span id="CONTROL_CANCEL"></span>Abbrechen von Steuerelementen \_
</dt> <dd>

Ein externer Schlüssel für die zweite Spalte der [Steuerelement Tabelle](control-table.md).

Durch kombinieren dieses Felds mit dem Dialog Feld wird ein Steuerelement angegeben, das die Installation abbricht. Dieses Steuerelement ist an Ereignisse in der [ControlEvent-Tabelle](controlevent-table.md) gekoppelt, die zum Abbrechen der Installation verwendet wird. Wenn Sie die ESC-Taste drücken oder auf die Schaltfläche Schließen klicken, entspricht das Klicken auf das Cancel-Steuerelement. Diese Spalte wird in einem [Fehler Dialogfeld](error-dialog.md) ignoriert.

zu ziehen und sie dort abzulegen.

Das Cancel-Steuerelement wird während des Rollbacks oder beim Entfernen von gesicherten Dateien ausgeblendet. Der interne Benutzeroberflächen Handler blendet das Steuerelement aus, wenn eine installmessage \_ commondata-Nachricht empfangen wird.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die ganzzahligen Werte für "width" und "Height" befinden sich in den [Installations Einheiten](installer-units.md)und nicht in den Dialog

Die beiden zentrieren-Werte werden für nachfolgende Dialogfelder in einer Assistenten Sequenz ignoriert. Dialog Feldpositionen werden vom Benutzer oder als für das vorherige Dialogfeld festgelegt. Diese Dialogfeld Sequenzen werden von einem [newdialog-ControlEvent](newdialog-controlevent.md)erstellt.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE13](ice13.md)  
[ICE20](ice20.md)  
[ICE23](ice23.md)  
[ICE27](ice27.md)  
[ICE32](ice32.md)  
[ICE44](ice44.md)  
[ICE45](ice45.md)  
[ICE46](ice46.md)  
</dl>

 

 



