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
# <a name="controlevent-table"></a><span data-ttu-id="b1337-103">ControlEvent-Tabelle</span><span class="sxs-lookup"><span data-stu-id="b1337-103">ControlEvent Table</span></span>

<span data-ttu-id="b1337-104">Die ControlEvent-Tabelle ermöglicht dem Autor die Angabe der [Steuerungs Ereignisse](control-events.md) , die gestartet werden, wenn ein Benutzer mit einem [PUSHBUTTON-Steuer](pushbutton-control.md)Element, [CheckBox-Steuer](checkbox-control.md)Element oder einem [SelectionTree-Steuer](selectiontree-control.md)Element interagiert.</span><span class="sxs-lookup"><span data-stu-id="b1337-104">The ControlEvent table allows the author to specify the [Control Events](control-events.md) started when a user interacts with a [PushButton Control](pushbutton-control.md), [CheckBox Control](checkbox-control.md), or [SelectionTree Control](selectiontree-control.md).</span></span> <span data-ttu-id="b1337-105">Dies sind die einzigen Steuerelemente, die Benutzer verwenden können, um Steuerungs Ereignisse zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="b1337-105">These are the only controls users can use to initiate control events.</span></span> <span data-ttu-id="b1337-106">Jedes Steuerelement kann mehrere Steuerelement Ereignisse veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="b1337-106">Each control can publish multiple control events.</span></span> <span data-ttu-id="b1337-107">Das Installationsprogramm startet jedes Ereignis in der Reihenfolge, die in der Sortier Spalte angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="b1337-107">The installer starts each event in the order specified in the Ordering column.</span></span> <span data-ttu-id="b1337-108">Ein Schaltflächen-Steuerelement kann beispielsweise Ereignisse veröffentlichen, um einen Übergang zu einem anderen Dialogfeld zu initiieren, die Dialogfeld Sequenz zu beenden und die Datei Installation zu starten.</span><span class="sxs-lookup"><span data-stu-id="b1337-108">For example, a push button control can publish events to initiate a transition to another dialog box, exit the dialog box sequence, and begin file installation.</span></span>

<span data-ttu-id="b1337-109">Beachten Sie, dass jedes Steuerelement nur ein [newdialog](newdialog-controlevent.md) -oder ein [spawndialog](spawndialog-controlevent.md) -Ereignis veröffentlichen kann.</span><span class="sxs-lookup"><span data-stu-id="b1337-109">The exception to note is that each control can publish a most one [NewDialog](newdialog-controlevent.md) or one [SpawnDialog](spawndialog-controlevent.md) event.</span></span> <span data-ttu-id="b1337-110">Wenn Sie mehrere newdialog-und spawndialog-Steuerelement Ereignisse in dieser Tabelle erstellen müssen, schließen Sie auch Bedingungs Anweisungen in die Bedingungs Felder ein, die sicherstellen, dass höchstens ein Ereignis veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="b1337-110">If you need to author multiple NewDialog and SpawnDialog control events in this table, also include conditional statements in the Condition fields that ensure at most one event is published.</span></span> <span data-ttu-id="b1337-111">Wenn mehrere newdialog-und spawndialog-Steuerelement Ereignisse für dasselbe Steuerelement ausgewählt werden, wird nur das Ereignis mit dem größten Wert in der Spalte Reihenfolge beim Aktivieren des Steuer Elements veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="b1337-111">If multiple NewDialog and SpawnDialog control events are selected for the same control, only the event with the largest value in the Ordering column gets published when the control is activated.</span></span>

<span data-ttu-id="b1337-112">Die ControlEvent-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="b1337-112">The ControlEvent table has the following columns.</span></span>



| <span data-ttu-id="b1337-113">Spalte</span><span class="sxs-lookup"><span data-stu-id="b1337-113">Column</span></span>    | <span data-ttu-id="b1337-114">Typ</span><span class="sxs-lookup"><span data-stu-id="b1337-114">Type</span></span>                         | <span data-ttu-id="b1337-115">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="b1337-115">Key</span></span> | <span data-ttu-id="b1337-116">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="b1337-116">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="b1337-117">Dialog\_</span><span class="sxs-lookup"><span data-stu-id="b1337-117">Dialog\_</span></span>  | [<span data-ttu-id="b1337-118">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="b1337-118">Identifier</span></span>](identifier.md) | <span data-ttu-id="b1337-119">J</span><span class="sxs-lookup"><span data-stu-id="b1337-119">Y</span></span>   | <span data-ttu-id="b1337-120">N</span><span class="sxs-lookup"><span data-stu-id="b1337-120">N</span></span>        |
| <span data-ttu-id="b1337-121">Steuerelement\_</span><span class="sxs-lookup"><span data-stu-id="b1337-121">Control\_</span></span> | [<span data-ttu-id="b1337-122">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="b1337-122">Identifier</span></span>](identifier.md) | <span data-ttu-id="b1337-123">J</span><span class="sxs-lookup"><span data-stu-id="b1337-123">Y</span></span>   | <span data-ttu-id="b1337-124">N</span><span class="sxs-lookup"><span data-stu-id="b1337-124">N</span></span>        |
| <span data-ttu-id="b1337-125">Ereignis</span><span class="sxs-lookup"><span data-stu-id="b1337-125">Event</span></span>     | [<span data-ttu-id="b1337-126">Großformatige</span><span class="sxs-lookup"><span data-stu-id="b1337-126">Formatted</span></span>](formatted.md)   | <span data-ttu-id="b1337-127">J</span><span class="sxs-lookup"><span data-stu-id="b1337-127">Y</span></span>   | <span data-ttu-id="b1337-128">N</span><span class="sxs-lookup"><span data-stu-id="b1337-128">N</span></span>        |
| <span data-ttu-id="b1337-129">Argument</span><span class="sxs-lookup"><span data-stu-id="b1337-129">Argument</span></span>  | [<span data-ttu-id="b1337-130">Großformatige</span><span class="sxs-lookup"><span data-stu-id="b1337-130">Formatted</span></span>](formatted.md)   | <span data-ttu-id="b1337-131">J</span><span class="sxs-lookup"><span data-stu-id="b1337-131">Y</span></span>   | <span data-ttu-id="b1337-132">N</span><span class="sxs-lookup"><span data-stu-id="b1337-132">N</span></span>        |
| <span data-ttu-id="b1337-133">Bedingung</span><span class="sxs-lookup"><span data-stu-id="b1337-133">Condition</span></span> | [<span data-ttu-id="b1337-134">Condition</span><span class="sxs-lookup"><span data-stu-id="b1337-134">Condition</span></span>](condition.md)   | <span data-ttu-id="b1337-135">J</span><span class="sxs-lookup"><span data-stu-id="b1337-135">Y</span></span>   | <span data-ttu-id="b1337-136">J</span><span class="sxs-lookup"><span data-stu-id="b1337-136">Y</span></span>        |
| <span data-ttu-id="b1337-137">Sortieren</span><span class="sxs-lookup"><span data-stu-id="b1337-137">Ordering</span></span>  | [<span data-ttu-id="b1337-138">Integer</span><span class="sxs-lookup"><span data-stu-id="b1337-138">Integer</span></span>](integer.md)       | <span data-ttu-id="b1337-139">N</span><span class="sxs-lookup"><span data-stu-id="b1337-139">N</span></span>   | <span data-ttu-id="b1337-140">J</span><span class="sxs-lookup"><span data-stu-id="b1337-140">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="b1337-141">Spalten</span><span class="sxs-lookup"><span data-stu-id="b1337-141">Columns</span></span>

<dl> <dt>

<span data-ttu-id="b1337-142"><span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialog\_</span><span class="sxs-lookup"><span data-stu-id="b1337-142"><span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialog\_</span></span>
</dt> <dd>

<span data-ttu-id="b1337-143">Ein externer Schlüssel für die erste Spalte der [Dialog Feld Tabelle](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="b1337-143">An external key to the first column of the [Dialog table](dialog-table.md).</span></span> <span data-ttu-id="b1337-144">Durch kombinieren dieses Felds mit dem Steuerelement Feld wird ein eindeutiges \_ Steuerelement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="b1337-144">Combining this field with the Control\_ field identifies a unique control.</span></span>

</dd> <dt>

<span data-ttu-id="b1337-145"><span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Steuerelement\_</span><span class="sxs-lookup"><span data-stu-id="b1337-145"><span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Control\_</span></span>
</dt> <dd>

<span data-ttu-id="b1337-146">Ein externer Schlüssel für die zweite Spalte der [Steuerelement Tabelle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="b1337-146">An external key to the second column of the [Control table](control-table.md).</span></span> <span data-ttu-id="b1337-147">Durch die Kombination dieses Felds mit dem Dialog Feld wird ein eindeutiges \_ Steuerelement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="b1337-147">Combining this field with the Dialog\_ field identifies a unique control.</span></span>

</dd> <dt>

<span data-ttu-id="b1337-148"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Veranstalter</span><span class="sxs-lookup"><span data-stu-id="b1337-148"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Event</span></span>
</dt> <dd>

<span data-ttu-id="b1337-149">Ein Bezeichner, der den Ereignistyp angibt, der ausgeführt werden soll, wenn der Benutzer mit dem Steuerelement interagiert, das durch Dialog und Steuerelement angegeben wird \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="b1337-149">An identifier that specifies the type of event that should take place when the user interacts with the control specified by Dialog\_ and Control\_.</span></span> <span data-ttu-id="b1337-150">Eine Liste möglicher Werte finden Sie unter [ControlEvent Overview](controlevent-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b1337-150">For a list of possible values see [ControlEvent Overview](controlevent-overview.md).</span></span>

<span data-ttu-id="b1337-151">Um eine Eigenschaft mit einem-Steuerelement festzulegen, legen Sie \[ den Eigenschafts \_ Namen \] in dieses Feld und den neuen Wert im Argument-Feld ab.</span><span class="sxs-lookup"><span data-stu-id="b1337-151">To set a property with a control, put \[Property\_Name\] in this field and the new value in the argument field.</span></span> <span data-ttu-id="b1337-152">Fügen Sie {} in das Argument Feld ein, um den Nullwert einzugeben.</span><span class="sxs-lookup"><span data-stu-id="b1337-152">Put { } into the argument field to enter the null value.</span></span>

</dd> <dt>

<span data-ttu-id="b1337-153"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Gestritten</span><span class="sxs-lookup"><span data-stu-id="b1337-153"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argument</span></span>
</dt> <dd>

<span data-ttu-id="b1337-154">Ein Wert, der als Modifizierer verwendet wird, wenn ein bestimmtes Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="b1337-154">A value used as a modifier when triggering a particular event.</span></span>

<span data-ttu-id="b1337-155">Beispielsweise ist das-Argument von " [newdialog ControlEvent](newdialog-controlevent.md) " oder " [spawndialog ControlEvent](spawndialog-controlevent.md) " der Name des Dialog Felds, und das-Argument der [Installations Aktion](install-action.md) ist eine Zahl, die die Installations Ebene definiert.</span><span class="sxs-lookup"><span data-stu-id="b1337-155">For example, the argument of the [NewDialog ControlEvent](newdialog-controlevent.md) or the [SpawnDialog ControlEvent](spawndialog-controlevent.md) is the name of the dialog box and the argument of the [Install action](install-action.md) is a number defining the install level.</span></span>

</dd> <dt>

<span data-ttu-id="b1337-156"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Anlage</span><span class="sxs-lookup"><span data-stu-id="b1337-156"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="b1337-157">Eine Bedingungs Anweisung, die bestimmt, ob das Installationsprogramm das Ereignis in der Ereignis Spalte aktiviert.</span><span class="sxs-lookup"><span data-stu-id="b1337-157">A conditional statement that determines whether the installer activates the event in the Event column.</span></span> <span data-ttu-id="b1337-158">Das Installationsprogramm löst das-Ereignis aus, wenn die bedingte Anweisung im Bedingungs Feld als true ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="b1337-158">The installer triggers the event if the conditional statement in the Condition field evaluates to True.</span></span> <span data-ttu-id="b1337-159">Legen Sie daher 1 in dieser Spalte ab, um sicherzustellen, dass das Installationsprogramm das Ereignis auslöst.</span><span class="sxs-lookup"><span data-stu-id="b1337-159">Therefore put a 1 in this column to ensure that the installer triggers the event.</span></span> <span data-ttu-id="b1337-160">Das Installationsprogramm löst das Ereignis nicht aus, wenn das Bedingungs Feld eine Anweisung enthält, die zu false ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="b1337-160">The installer does not trigger the event if the Condition field contains a statement that evaluates to False.</span></span> <span data-ttu-id="b1337-161">Das Installationsprogramm löst kein Ereignis mit einem leeren im Bedingungs Feld aus, es sei denn, es werden keine anderen Ereignisse des Steuer Elements als true ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="b1337-161">The installer does not trigger an event with a blank in the Condition field unless no other events of the control evaluate to True.</span></span> <span data-ttu-id="b1337-162">Wenn keines der Bedingungs Felder für das im Feld "Steuerelement" benannte Steuerelement als " \_ true" ausgewertet wird, löst das Installationsprogramm das ein Ereignis aus, das ein leeres Bedingungs Feld hat, und wenn mehr als ein Bedingungs Feld leer ist, wird das ein Ereignis mit dem größten Wert im Feld "Reihenfolge" ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="b1337-162">If none of the Condition fields for the control named in the Control\_ field evaluate to True, the installer triggers the one event having a blank Condition field, and if more than one Condition field is blank it triggers the one event of these with the largest value in the Ordering field.</span></span> <span data-ttu-id="b1337-163">Siehe [Syntax der Bedingungs Anweisung](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="b1337-163">See [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1337-164"><span id="Ordering"></span><span id="ordering"></span><span id="ORDERING"></span>Stelle</span><span class="sxs-lookup"><span data-stu-id="b1337-164"><span id="Ordering"></span><span id="ordering"></span><span id="ORDERING"></span>Ordering</span></span>
</dt> <dd>

<span data-ttu-id="b1337-165">Eine ganze Zahl, die verwendet wird, um mehrere an dasselbe Steuerelement gebundene Ereignisse zu ordnen.</span><span class="sxs-lookup"><span data-stu-id="b1337-165">An integer used to order several events tied to the same control.</span></span> <span data-ttu-id="b1337-166">Dabei muss es sich um eine nicht negative Zahl handeln.</span><span class="sxs-lookup"><span data-stu-id="b1337-166">This must be a non-negative number.</span></span> <span data-ttu-id="b1337-167">Dieses Feld kann leer gelassen werden.</span><span class="sxs-lookup"><span data-stu-id="b1337-167">This field may be left blank.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b1337-168">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b1337-168">Remarks</span></span>

<span data-ttu-id="b1337-169">Die [Tabelle EventMapping](eventmapping-table.md) listet die Steuerelemente auf, die ein Steuerelement Ereignis abonnieren, und listet das Steuerelement Attribut auf, das geändert werden soll, wenn dieses Ereignis von einem anderen Steuerelement oder dem Installationsprogramm veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="b1337-169">The [EventMapping table](eventmapping-table.md) lists the controls that subscribe to some control event and lists the control attribute to be changed when that event is published by the another control or the installer.</span></span>

<span data-ttu-id="b1337-170">Unter Windows XP oder früheren Betriebssystemen können Benutzer ein Steuerungs Ereignis nur durch Interaktion mit einem CheckBox- [Steuer](checkbox-control.md) Element oder einem [PUSHBUTTON-Steuer](pushbutton-control.md)Element veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="b1337-170">On Windows XP or earlier operating systems, users can publish a control event only by interacting with a [Checkbox Control](checkbox-control.md) or [Pushbutton Control](pushbutton-control.md).</span></span> <span data-ttu-id="b1337-171">Mit Windows Server 2003 können Benutzer ein Steuerungs Ereignis nur durch Interaktion mit einem CheckBox- [Steuer](checkbox-control.md)Element, einem [SelectionTree-Steuer](selectiontree-control.md)Element und einem [PUSHBUTTON-Steuer](pushbutton-control.md)Element veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="b1337-171">With Windows Server 2003, users can publish a control event only by interacting with a [Checkbox Control](checkbox-control.md), [SelectionTree Control](selectiontree-control.md), and [Pushbutton Control](pushbutton-control.md).</span></span> <span data-ttu-id="b1337-172">Das Auflisten anderer Steuerelemente im Steuerelement \_ Feld hat keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="b1337-172">Listing other controls in the Control\_ field has no effect.</span></span>

## <a name="validation"></a><span data-ttu-id="b1337-173">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="b1337-173">Validation</span></span>

<dl>

[<span data-ttu-id="b1337-174">ICE03</span><span class="sxs-lookup"><span data-stu-id="b1337-174">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="b1337-175">ICE06</span><span class="sxs-lookup"><span data-stu-id="b1337-175">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="b1337-176">ICE17</span><span class="sxs-lookup"><span data-stu-id="b1337-176">ICE17</span></span>](ice17.md)  
[<span data-ttu-id="b1337-177">ICE20</span><span class="sxs-lookup"><span data-stu-id="b1337-177">ICE20</span></span>](ice20.md)  
[<span data-ttu-id="b1337-178">ICE32</span><span class="sxs-lookup"><span data-stu-id="b1337-178">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="b1337-179">ICE44</span><span class="sxs-lookup"><span data-stu-id="b1337-179">ICE44</span></span>](ice44.md)  
[<span data-ttu-id="b1337-180">ICE46</span><span class="sxs-lookup"><span data-stu-id="b1337-180">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="b1337-181">ICE79</span><span class="sxs-lookup"><span data-stu-id="b1337-181">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="b1337-182">ICE86</span><span class="sxs-lookup"><span data-stu-id="b1337-182">ICE86</span></span>](ice86.md)  
</dl>

 

 



