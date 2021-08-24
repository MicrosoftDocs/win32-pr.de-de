---
description: Mit der ControlEvent-Tabelle kann der Autor die Control Events angeben, die gestartet werden, wenn ein Benutzer mit einem PushButton-Steuerelement, einem CheckBox-Steuerelement oder einem SelectionTree-Steuerelement interagiert.
ms.assetid: e34d17e9-cd6b-4a21-9abc-9562ee648c59
title: ControlEvent-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fec4837fa7d98289495bbb0773ae7260f957485cd87214dabf1999b1e1a876c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693000"
---
# <a name="controlevent-table"></a>ControlEvent-Tabelle

Mit der ControlEvent-Tabelle kann der Autor die [Steuerelementereignisse](control-events.md) angeben, die gestartet werden, wenn ein Benutzer mit einem [PushButton-Steuerelement,](pushbutton-control.md) [einem CheckBox-Steuerelement](checkbox-control.md)oder einem [SelectionTree-Steuerelement](selectiontree-control.md)interagiert. Dies sind die einzigen Steuerelemente, die Benutzer zum Initiieren von Steuerungsereignissen verwenden können. Jedes Steuerelement kann mehrere Steuerelementereignisse veröffentlichen. Das Installationsprogramm startet jedes Ereignis in der in der Spalte Ordering angegebenen Reihenfolge. Beispielsweise kann ein Schaltflächen-Steuerelement Ereignisse veröffentlichen, um einen Übergang zu einem anderen Dialogfeld zu initiieren, die Dialogfeldsequenz zu beenden und die Dateiinstallation zu starten.

Beachten Sie jedoch, dass jedes Steuerelement die meisten [NewDialog-](newdialog-controlevent.md) oder [SpawnDialog-Ereignisse](spawndialog-controlevent.md) veröffentlichen kann. Wenn Sie mehrere NewDialog- und SpawnDialog-Steuerelementereignisse in dieser Tabelle erstellen müssen, schließen Sie auch bedingte Anweisungen in die Felder Bedingung ein, die sicherstellen, dass höchstens ein Ereignis veröffentlicht wird. Wenn mehrere NewDialog- und SpawnDialog-Steuerelementereignisse für dasselbe Steuerelement ausgewählt sind, wird nur das Ereignis mit dem größten Wert in der Spalte Ordering veröffentlicht, wenn das Steuerelement aktiviert wird.

Die ControlEvent-Tabelle enthält die folgenden Spalten.



| Spalte    | Typ                         | Key | Nullwerte zulässig |
|-----------|------------------------------|-----|----------|
| Dialog\_  | [Identifier](identifier.md) | J   | N        |
| Steuerelement\_ | [Identifier](identifier.md) | J   | N        |
| Ereignis     | [Formatiert](formatted.md)   | J   | N        |
| Argument  | [Formatiert](formatted.md)   | J   | N        |
| Bedingung | [Condition](condition.md)   | J   | J        |
| Sortieren  | [Integer](integer.md)       | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialogfeld\_
</dt> <dd>

Ein externer Schlüssel für die erste Spalte der [Dialogtabelle](dialog-table.md). Durch Kombinieren dieses Felds mit dem Feld Steuerelement \_ wird ein eindeutiges Steuerelement identifiziert.

</dd> <dt>

<span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Steuerung\_
</dt> <dd>

Ein externer Schlüssel für die zweite Spalte der [Control-Tabelle.](control-table.md) Durch Kombinieren dieses Felds mit dem \_ Dialogfeld-Feld wird ein eindeutiges Steuerelement identifiziert.

</dd> <dt>

<span id="Event"></span><span id="event"></span><span id="EVENT"></span>Ereignis
</dt> <dd>

Ein Bezeichner, der den Ereignistyp angibt, der stattfinden soll, wenn der Benutzer mit dem durch Dialog und Steuerelement angegebenen Steuerelement \_ \_ interagiert. Eine Liste der möglichen Werte finden Sie unter [Übersicht über ControlEvent.](controlevent-overview.md)

Um eine Eigenschaft mit einem -Steuerelement festzulegen, legen Sie \[ \_ \] Eigenschaftenname in dieses Feld und den neuen Wert in das Argumentfeld ein. Geben Sie { } in das Argumentfeld ein, um den NULL-Wert einzugeben.

</dd> <dt>

<span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argument
</dt> <dd>

Ein -Wert, der beim Auslösen eines bestimmten Ereignisses als Modifizierer verwendet wird.

Das Argument von [NewDialog ControlEvent](newdialog-controlevent.md) oder [SpawnDialog ControlEvent](spawndialog-controlevent.md) ist beispielsweise der Name des Dialogfelds, und das Argument der [Install-Aktion](install-action.md) ist eine Zahl, die die Installationsebene definiert.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Zustand
</dt> <dd>

Eine bedingte Anweisung, die bestimmt, ob das Installationsprogramm das Ereignis in der Spalte Ereignis aktiviert. Das Installationsprogramm löst das -Ereignis aus, wenn die bedingungsbedingte Anweisung im Feld Bedingung zu True ausgewertet wird. Legen Sie daher eine 1 in diese Spalte ein, um sicherzustellen, dass das -Ereignis vom Installationsprogramm ausgelöst wird. Das Installationsprogramm löst das -Ereignis nicht aus, wenn das Feld Bedingung eine Anweisung enthält, die als False ausgewertet wird. Das Installationsprogramm löst kein Ereignis aus, das im Feld Bedingung leer ist, es sei denn, es werden keine anderen Ereignisse des Steuerelements als TRUE ausgewertet. Wenn keines der Bedingungsfelder für das Im Feld Steuerelement benannte Steuerelement \_ zu True ausgewertet wird, löst das Installationsprogramm das ein Ereignis mit einem leeren Feld Bedingung aus, und wenn mehr als ein Bedingungsfeld leer ist, löst es das ein Ereignis dieser mit dem größten Wert im Feld Ordering aus. Weitere Informationen finden Sie unter [Syntax der bedingten Anweisung.](conditional-statement-syntax.md)

</dd> <dt>

<span id="Ordering"></span><span id="ordering"></span><span id="ORDERING"></span>Bestellung
</dt> <dd>

Eine ganze Zahl, die verwendet wird, um mehrere Ereignisse zu ordnen, die an dasselbe Steuerelement gebunden sind. Dies muss eine nicht negative Zahl sein. Dieses Feld kann leer gelassen werden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die [EventMapping-Tabelle](eventmapping-table.md) listet die Steuerelemente auf, die ein Steuerelementereignis abonnieren, und listet das Steuerelementattribut auf, das geändert werden soll, wenn dieses Ereignis vom anderen Steuerelement oder vom Installationsprogramm veröffentlicht wird.

Unter Windows XP oder früheren Betriebssystemen können Benutzer ein Steuerelementereignis nur veröffentlichen, indem sie mit einem [Kontrollkästchen-Steuerelement](checkbox-control.md) oder [einem Pushbutton-Steuerelement](pushbutton-control.md)interagieren. Mit Windows Server 2003 können Benutzer ein Steuerelementereignis nur veröffentlichen, indem sie mit einem [Kontrollkästchen-Steuerelement,](checkbox-control.md) [einem SelectionTree-Steuerelement](selectiontree-control.md)und einem [Pushbutton-Steuerelement](pushbutton-control.md)interagieren. Das Auflisten anderer Steuerelemente im Feld Steuerelement \_ hat keine Auswirkungen.

## <a name="validation"></a>Überprüfung

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

 

 



