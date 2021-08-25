---
description: Die EventMapping-Tabelle listet die Steuerelemente auf, die einige Steuerelementereignisse abonnieren, und listet das Attribut auf, das geändert werden soll, wenn das Ereignis von einem anderen Steuerelement oder vom Windows Installer veröffentlicht wird.
ms.assetid: 63c9ba3e-aa8a-475b-8360-4aec78ed19db
title: EventMapping-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f17380e3e91669926ef50532c36fec71f44d61eb2ed7273d053defe45fa874e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963110"
---
# <a name="eventmapping-table"></a>EventMapping-Tabelle

Die EventMapping-Tabelle listet die Steuerelemente auf, die einige Steuerelementereignisse abonnieren, und listet das Attribut auf, das geändert werden soll, wenn das Ereignis von einem anderen Steuerelement oder vom Windows Installer veröffentlicht wird.

Die EventMapping-Tabelle weist die folgenden Spalten auf.



| Spalte    | Typ                         | Key | Nullwerte zulässig |
|-----------|------------------------------|-----|----------|
| Dialog\_  | [Identifier](identifier.md) | J   | N        |
| Steuerelement\_ | [Identifier](identifier.md) | J   | N        |
| Ereignis     | [Identifier](identifier.md) | J   | N        |
| attribute | [Identifier](identifier.md) | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialogfeld\_
</dt> <dd>

Ein externer Schlüssel für die erste Spalte der [Dialogtabelle](dialog-table.md). Dieses Feld und das Feld Steuerelement \_ identifizieren zusammen ein Steuerelement.

</dd> <dt>

<span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Steuerung\_
</dt> <dd>

Ein externer Schlüssel für die zweite Spalte der [Steuertabelle](control-table.md). Dieses Feld und das \_ Dialogfeld -Feld identifizieren zusammen ein Steuerelement.

</dd> <dt>

<span id="Event"></span><span id="event"></span><span id="EVENT"></span>Ereignis
</dt> <dd>

Dieses Feld ist ein Bezeichner, der den Typ des Ereignisses angibt, das vom -Steuerelement abonniert wird. Weitere Informationen finden Sie unter [ControlEvent Overview](controlevent-overview.md).

</dd> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attribut
</dt> <dd>

Der Name des \_ Control-Attributs, das festgelegt wird, wenn das Ereignis in der Spalte Ereignis empfangen wird. Das Argument des Ereignisses wird als Argument des Attributaufrufs übergeben, um dieses Attribut des Steuerelements zu ändern.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die [ControlEvent-Tabelle](controlevent-table.md) gibt die Steuerelementereignisse an, die gestartet werden, wenn ein Benutzer mit einem [PushButton-Steuerelement,](pushbutton-control.md) [einem CheckBox-Steuerelement](checkbox-control.md)oder einem [SelectionTree-Steuerelement](selectiontree-control.md)interagiert. Dies sind die einzigen Steuerelemente, die ein Benutzer verwenden kann, um Steuerungsereignisse zu initiieren.

Mehr als ein Steuerelement in einem Dialogfeld kann dasselbe Ereignis abonnieren.

In der folgenden Liste sind die typischen Verwendungsmöglichkeiten für die EventMapping-Tabelle aufgeführt:

-   So abonnieren Sie ein [Textsteuerelement](text-control.md) für ein [ActionText ControlEvent,](actiontext-controlevent.md) [ActionData ControlEvent,](actiondata-controlevent.md) [ScriptInProgress ControlEvent](scriptinprogress-controlevent.md) oder [TimeRemaining ControlEvent,](timeremaining-controlevent.md) das vom Windows Installer veröffentlicht wurde.
-   So abonnieren Sie ein [ProgressBar-Steuerelement](progressbar-control.md) oder [ein Control-Steuerelement von](billboard-control.md) [SetProgress .](setprogress-controlevent.md)
-   So abonnieren Sie ein [DirectoryCombo-Steuerelement](directorycombo-control.md) für ein [IgnoreChange ControlEvent](ignorechange-controlevent.md).
-   So deaktivieren Sie automatisch ein [PushButton-Steuerelement,](pushbutton-control.md) das sich im gleichen Dialogfeld mit einem [SelectionTree-Steuerelement](selectiontree-control.md)befindet. Um die Schaltfläche "Push" zu deaktivieren, wenn im [SelectionTree-Steuerelement](selectiontree-control.md)keine Features aufgeführt sind, verwenden Sie die EventMapping-Tabelle, um das PushButton-Steuerelement einem [SelectionNoItems ControlEvent](selectionnoitems-controlevent.md)zu abonnieren. Geben Sie **Aktivieren** in das Feld Attribute der EventMapping-Tabelle ein.
-   So zeigen Sie ein [Textsteuerelement](text-control.md) an, das den Pfad zum Installationsspeicherort für das Feature anzeigt, das im selben Dialogfeld in einem [SelectionTree-Steuerelement](selectiontree-control.md) ausgewählt ist. Verwenden Sie die EventMapping-Tabelle, um das [Textsteuerelement](text-control.md) sowohl einem [SelectionPathOn ControlEvent](selectionpathon-controlevent.md) als auch einem [SelectionPath ControlEvent](selectionpath-controlevent.md) zu abonnieren, das vom [SelectionTree-Steuerelement](selectiontree-control.md)veröffentlicht wurde.
-   Um ein [Textsteuerelement](text-control.md) anzuzeigen, das eine Beschreibung des Elements anzeigt, das in einem [SelectionTree-Steuerelement](selectiontree-control.md) hervorgehoben ist, das sich im gleichen Dialogfeld befindet, verwenden Sie die EventMapping-Tabelle, um das [Textsteuerelement](text-control.md) für [selectionDescription ControlEvent,](selectiondescription-controlevent.md) [SelectionSize ControlEvent](selectionsize-controlevent.md) oder [SelectionAction ControlEvent](selectionaction-controlevent.md)zu abonnieren. Geben Sie **Text** in das Feld Attribut der EventMapping-Tabelle ein.

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



