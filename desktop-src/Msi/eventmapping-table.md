---
description: Die Tabelle EventMapping listet die Steuerelemente auf, die einige Steuerelement Ereignisse abonnieren, und listet das Attribut auf, das geändert werden soll, wenn das Ereignis von einem anderen Steuerelement oder dem Windows Installer veröffentlicht wird.
ms.assetid: 63c9ba3e-aa8a-475b-8360-4aec78ed19db
title: EventMapping-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e9a7b5b4283b5d70102123dcb11e3e9e844221
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864239"
---
# <a name="eventmapping-table"></a>EventMapping-Tabelle

Die Tabelle EventMapping listet die Steuerelemente auf, die einige Steuerelement Ereignisse abonnieren, und listet das Attribut auf, das geändert werden soll, wenn das Ereignis von einem anderen Steuerelement oder dem Windows Installer veröffentlicht wird.

Die EventMapping-Tabelle weist die folgenden Spalten auf.



| Spalte    | Typ                         | Schlüssel | Nullwerte zulässig |
|-----------|------------------------------|-----|----------|
| Dialog\_  | [Bezeichner](identifier.md) | J   | N        |
| Steuerelement\_ | [Bezeichner](identifier.md) | J   | N        |
| Ereignis     | [Bezeichner](identifier.md) | J   | N        |
| Attribut | [Bezeichner](identifier.md) | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialog\_
</dt> <dd>

Ein externer Schlüssel für die erste Spalte der [Dialog Feld Tabelle](dialog-table.md). Dieses Feld und das Steuerelement \_ Feld identifizieren ein Steuerelement.

</dd> <dt>

<span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Steuerelement\_
</dt> <dd>

Ein externer Schlüssel für die zweite Spalte der [Steuerelement Tabelle](control-table.md). In diesem Feld und dem Dialog \_ Feld wird ein Steuerelement identifiziert.

</dd> <dt>

<span id="Event"></span><span id="event"></span><span id="EVENT"></span>Veranstalter
</dt> <dd>

Dieses Feld ist ein Bezeichner, der den Ereignistyp angibt, der vom Steuerelement abonniert wird. Weitere Informationen finden Sie unter [ControlEvent Overview](controlevent-overview.md).

</dd> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Versehen
</dt> <dd>

Der Name des Steuerelement \_ Attributs, das festgelegt wird, wenn das Ereignis in der Ereignis Spalte empfangen wird. Das-Argument des-Ereignisses wird als Argument des-Attribut Aufrufes zum Ändern dieses Attributs des-Steuer Elements übermittelt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die [ControlEvent-Tabelle](controlevent-table.md) gibt die Steuerelement Ereignisse an, die gestartet werden, wenn ein Benutzer mit einem [PUSHBUTTON-Steuer](pushbutton-control.md)Element, [CheckBox-Steuer](checkbox-control.md)Element oder [SelectionTree-Steuer](selectiontree-control.md)Element interagiert. Dies sind die einzigen Steuerelemente, die ein Benutzer verwenden kann, um Steuerungs Ereignisse zu initiieren.

Mehrere Steuerelemente in einem Dialogfeld können dasselbe Ereignis abonnieren.

In der folgenden Liste sind die typischen Verwendungen der Tabelle EventMapping aufgeführt:

-   So abonnieren Sie [ein Text-Steuer](text-control.md) Element für eine [Action Text ControlEvent](actiontext-controlevent.md)-, [Action Data ControlEvent](actiondata-controlevent.md)-, [scriptinprogress ControlEvent](scriptinprogress-controlevent.md) -oder [timeremaineing ControlEvent](timeremaining-controlevent.md) -Datei, die vom Windows Installer veröffentlicht wurde.
-   Zum Abonnieren eines [ProgressBar-Steuer](progressbar-control.md) Elements oder eines [Billboard-Steuer](billboard-control.md) Elements für einen [setProgress-ControlEvent](setprogress-controlevent.md).
-   , Um ein [directoriycombo-Steuer](directorycombo-control.md) Element für [ignorechange ControlEvent](ignorechange-controlevent.md)zu abonnieren.
-   Zum automatischen Deaktivieren eines [PUSHBUTTON-Steuer](pushbutton-control.md) Elements, das sich im gleichen Dialogfeld mit einem [SelectionTree-Steuer](selectiontree-control.md)Element befindet. Um die Schaltfläche "Push" zu deaktivieren, wenn im [SelectionTree-Steuer](selectiontree-control.md)Element keine Features aufgelistet sind, verwenden Sie die EventMapping-Tabelle, um das PUSHBUTTON-Steuerelement einem [selectionnoitems-ControlEvent](selectionnoitems-controlevent.md)zu abonnieren. Geben Sie im Feld Attribute der Tabelle EventMapping den Wert **enable** ein.
-   Zum Anzeigen eines [Text Steuer](text-control.md) Elements, das den Pfad zum Installations Speicherort für das Feature anzeigt, das in einem [SelectionTree-Steuer](selectiontree-control.md) Element im gleichen Dialogfeld ausgewählt ist. Verwenden Sie die Tabelle EventMapping, um das [Text Steuer](text-control.md) Element sowohl einem [selectionpathon ControlEvent](selectionpathon-controlevent.md) als auch dem [selectionpath ControlEvent](selectionpath-controlevent.md) zu abonnieren, das vom [SelectionTree-Steuer](selectiontree-control.md)Element veröffentlicht wurde.
-   Wenn Sie ein [Text Steuer](text-control.md) Element anzeigen möchten, das eine Beschreibung des Elements anzeigt, das in einem [SelectionTree-Steuer](selectiontree-control.md) Element im gleichen Dialogfeld hervorgehoben ist, verwenden Sie die EventMapping-Tabelle, um das [Text Steuer](text-control.md) Element einem [selectiondescription ControlEvent](selectiondescription-controlevent.md), [selectionsize ControlEvent](selectionsize-controlevent.md) oder [selectionaction ControlEvent](selectionaction-controlevent.md)zu abonnieren. Geben Sie im Feld Attribut der Tabelle EventMapping den **Text** ein.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



