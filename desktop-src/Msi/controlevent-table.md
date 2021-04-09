---
description: Die ControlEvent-Tabelle ermöglicht dem Autor die Angabe der Steuerungs Ereignisse, die gestartet werden, wenn ein Benutzer mit einem PUSHBUTTON-Steuerelement, CheckBox-Steuerelement oder einem SelectionTree-Steuerelement interagiert.
ms.assetid: e34d17e9-cd6b-4a21-9abc-9562ee648c59
title: ControlEvent-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 721dc7ac9a729b8df0623a2958a4d0fe32851307
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868463"
---
# <a name="controlevent-table"></a>ControlEvent-Tabelle

Die ControlEvent-Tabelle ermöglicht dem Autor die Angabe der [Steuerungs Ereignisse](control-events.md) , die gestartet werden, wenn ein Benutzer mit einem [PUSHBUTTON-Steuer](pushbutton-control.md)Element, [CheckBox-Steuer](checkbox-control.md)Element oder einem [SelectionTree-Steuer](selectiontree-control.md)Element interagiert. Dies sind die einzigen Steuerelemente, die Benutzer verwenden können, um Steuerungs Ereignisse zu initiieren. Jedes Steuerelement kann mehrere Steuerelement Ereignisse veröffentlichen. Das Installationsprogramm startet jedes Ereignis in der Reihenfolge, die in der Sortier Spalte angegeben ist. Ein Schaltflächen-Steuerelement kann beispielsweise Ereignisse veröffentlichen, um einen Übergang zu einem anderen Dialogfeld zu initiieren, die Dialogfeld Sequenz zu beenden und die Datei Installation zu starten.

Beachten Sie, dass jedes Steuerelement nur ein [newdialog](newdialog-controlevent.md) -oder ein [spawndialog](spawndialog-controlevent.md) -Ereignis veröffentlichen kann. Wenn Sie mehrere newdialog-und spawndialog-Steuerelement Ereignisse in dieser Tabelle erstellen müssen, schließen Sie auch Bedingungs Anweisungen in die Bedingungs Felder ein, die sicherstellen, dass höchstens ein Ereignis veröffentlicht wird. Wenn mehrere newdialog-und spawndialog-Steuerelement Ereignisse für dasselbe Steuerelement ausgewählt werden, wird nur das Ereignis mit dem größten Wert in der Spalte Reihenfolge beim Aktivieren des Steuer Elements veröffentlicht.

Die ControlEvent-Tabelle weist die folgenden Spalten auf.



| Spalte    | Typ                         | Schlüssel | Nullwerte zulässig |
|-----------|------------------------------|-----|----------|
| Dialog\_  | [Bezeichner](identifier.md) | J   | N        |
| Steuerelement\_ | [Bezeichner](identifier.md) | J   | N        |
| Ereignis     | [Großformatige](formatted.md)   | J   | N        |
| Argument  | [Großformatige](formatted.md)   | J   | N        |
| Bedingung | [Condition](condition.md)   | J   | J        |
| Sortieren  | [Integer](integer.md)       | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialog\_
</dt> <dd>

Ein externer Schlüssel für die erste Spalte der [Dialog Feld Tabelle](dialog-table.md). Durch kombinieren dieses Felds mit dem Steuerelement Feld wird ein eindeutiges \_ Steuerelement identifiziert.

</dd> <dt>

<span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Steuerelement\_
</dt> <dd>

Ein externer Schlüssel für die zweite Spalte der [Steuerelement Tabelle](control-table.md). Durch die Kombination dieses Felds mit dem Dialog Feld wird ein eindeutiges \_ Steuerelement identifiziert.

</dd> <dt>

<span id="Event"></span><span id="event"></span><span id="EVENT"></span>Veranstalter
</dt> <dd>

Ein Bezeichner, der den Ereignistyp angibt, der ausgeführt werden soll, wenn der Benutzer mit dem Steuerelement interagiert, das durch Dialog und Steuerelement angegeben wird \_ \_ . Eine Liste möglicher Werte finden Sie unter [ControlEvent Overview](controlevent-overview.md).

Um eine Eigenschaft mit einem-Steuerelement festzulegen, legen Sie \[ den Eigenschafts \_ Namen \] in dieses Feld und den neuen Wert im Argument-Feld ab. Fügen Sie {} in das Argument Feld ein, um den Nullwert einzugeben.

</dd> <dt>

<span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Gestritten
</dt> <dd>

Ein Wert, der als Modifizierer verwendet wird, wenn ein bestimmtes Ereignis ausgelöst wird.

Beispielsweise ist das-Argument von " [newdialog ControlEvent](newdialog-controlevent.md) " oder " [spawndialog ControlEvent](spawndialog-controlevent.md) " der Name des Dialog Felds, und das-Argument der [Installations Aktion](install-action.md) ist eine Zahl, die die Installations Ebene definiert.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Anlage
</dt> <dd>

Eine Bedingungs Anweisung, die bestimmt, ob das Installationsprogramm das Ereignis in der Ereignis Spalte aktiviert. Das Installationsprogramm löst das-Ereignis aus, wenn die bedingte Anweisung im Bedingungs Feld als true ausgewertet wird. Legen Sie daher 1 in dieser Spalte ab, um sicherzustellen, dass das Installationsprogramm das Ereignis auslöst. Das Installationsprogramm löst das Ereignis nicht aus, wenn das Bedingungs Feld eine Anweisung enthält, die zu false ausgewertet wird. Das Installationsprogramm löst kein Ereignis mit einem leeren im Bedingungs Feld aus, es sei denn, es werden keine anderen Ereignisse des Steuer Elements als true ausgewertet. Wenn keines der Bedingungs Felder für das im Feld "Steuerelement" benannte Steuerelement als " \_ true" ausgewertet wird, löst das Installationsprogramm das ein Ereignis aus, das ein leeres Bedingungs Feld hat, und wenn mehr als ein Bedingungs Feld leer ist, wird das ein Ereignis mit dem größten Wert im Feld "Reihenfolge" ausgelöst. Siehe [Syntax der Bedingungs Anweisung](conditional-statement-syntax.md).

</dd> <dt>

<span id="Ordering"></span><span id="ordering"></span><span id="ORDERING"></span>Stelle
</dt> <dd>

Eine ganze Zahl, die verwendet wird, um mehrere an dasselbe Steuerelement gebundene Ereignisse zu ordnen. Dabei muss es sich um eine nicht negative Zahl handeln. Dieses Feld kann leer gelassen werden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die [Tabelle EventMapping](eventmapping-table.md) listet die Steuerelemente auf, die ein Steuerelement Ereignis abonnieren, und listet das Steuerelement Attribut auf, das geändert werden soll, wenn dieses Ereignis von einem anderen Steuerelement oder dem Installationsprogramm veröffentlicht wird.

Unter Windows XP oder früheren Betriebssystemen können Benutzer ein Steuerungs Ereignis nur durch Interaktion mit einem CheckBox- [Steuer](checkbox-control.md) Element oder einem [PUSHBUTTON-Steuer](pushbutton-control.md)Element veröffentlichen. Mit Windows Server 2003 können Benutzer ein Steuerungs Ereignis nur durch Interaktion mit einem CheckBox- [Steuer](checkbox-control.md)Element, einem [SelectionTree-Steuer](selectiontree-control.md)Element und einem [PUSHBUTTON-Steuer](pushbutton-control.md)Element veröffentlichen. Das Auflisten anderer Steuerelemente im Steuerelement \_ Feld hat keine Auswirkungen.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE20](ice20.md)  
[ICE32](ice32.md)  
[ICE44](ice44.md)  
[ICE46](ice46.md)  
[ICE79](ice79.md)  
[ICE86](ice86.md)  
</dl>

 

 



