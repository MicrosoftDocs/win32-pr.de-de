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
# <a name="eventmapping-table"></a><span data-ttu-id="29bcc-103">EventMapping-Tabelle</span><span class="sxs-lookup"><span data-stu-id="29bcc-103">EventMapping Table</span></span>

<span data-ttu-id="29bcc-104">Die Tabelle EventMapping listet die Steuerelemente auf, die einige Steuerelement Ereignisse abonnieren, und listet das Attribut auf, das geändert werden soll, wenn das Ereignis von einem anderen Steuerelement oder dem Windows Installer veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="29bcc-104">The EventMapping Table lists the controls that subscribe to some control events, and lists the attribute to be changed when the event is published by another control or the Windows Installer.</span></span>

<span data-ttu-id="29bcc-105">Die EventMapping-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="29bcc-105">The EventMapping Table has the following columns.</span></span>



| <span data-ttu-id="29bcc-106">Spalte</span><span class="sxs-lookup"><span data-stu-id="29bcc-106">Column</span></span>    | <span data-ttu-id="29bcc-107">Typ</span><span class="sxs-lookup"><span data-stu-id="29bcc-107">Type</span></span>                         | <span data-ttu-id="29bcc-108">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="29bcc-108">Key</span></span> | <span data-ttu-id="29bcc-109">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="29bcc-109">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="29bcc-110">Dialog\_</span><span class="sxs-lookup"><span data-stu-id="29bcc-110">Dialog\_</span></span>  | [<span data-ttu-id="29bcc-111">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="29bcc-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="29bcc-112">J</span><span class="sxs-lookup"><span data-stu-id="29bcc-112">Y</span></span>   | <span data-ttu-id="29bcc-113">N</span><span class="sxs-lookup"><span data-stu-id="29bcc-113">N</span></span>        |
| <span data-ttu-id="29bcc-114">Steuerelement\_</span><span class="sxs-lookup"><span data-stu-id="29bcc-114">Control\_</span></span> | [<span data-ttu-id="29bcc-115">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="29bcc-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="29bcc-116">J</span><span class="sxs-lookup"><span data-stu-id="29bcc-116">Y</span></span>   | <span data-ttu-id="29bcc-117">N</span><span class="sxs-lookup"><span data-stu-id="29bcc-117">N</span></span>        |
| <span data-ttu-id="29bcc-118">Ereignis</span><span class="sxs-lookup"><span data-stu-id="29bcc-118">Event</span></span>     | [<span data-ttu-id="29bcc-119">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="29bcc-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="29bcc-120">J</span><span class="sxs-lookup"><span data-stu-id="29bcc-120">Y</span></span>   | <span data-ttu-id="29bcc-121">N</span><span class="sxs-lookup"><span data-stu-id="29bcc-121">N</span></span>        |
| <span data-ttu-id="29bcc-122">Attribut</span><span class="sxs-lookup"><span data-stu-id="29bcc-122">Attribute</span></span> | [<span data-ttu-id="29bcc-123">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="29bcc-123">Identifier</span></span>](identifier.md) | <span data-ttu-id="29bcc-124">N</span><span class="sxs-lookup"><span data-stu-id="29bcc-124">N</span></span>   | <span data-ttu-id="29bcc-125">N</span><span class="sxs-lookup"><span data-stu-id="29bcc-125">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="29bcc-126">Spalten</span><span class="sxs-lookup"><span data-stu-id="29bcc-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="29bcc-127"><span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialog\_</span><span class="sxs-lookup"><span data-stu-id="29bcc-127"><span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialog\_</span></span>
</dt> <dd>

<span data-ttu-id="29bcc-128">Ein externer Schlüssel für die erste Spalte der [Dialog Feld Tabelle](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="29bcc-128">An external key to the first column of the [Dialog Table](dialog-table.md).</span></span> <span data-ttu-id="29bcc-129">Dieses Feld und das Steuerelement \_ Feld identifizieren ein Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="29bcc-129">This field and the Control\_ field together identify a control.</span></span>

</dd> <dt>

<span data-ttu-id="29bcc-130"><span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Steuerelement\_</span><span class="sxs-lookup"><span data-stu-id="29bcc-130"><span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Control\_</span></span>
</dt> <dd>

<span data-ttu-id="29bcc-131">Ein externer Schlüssel für die zweite Spalte der [Steuerelement Tabelle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="29bcc-131">An external key to the second column of the [Control Table](control-table.md).</span></span> <span data-ttu-id="29bcc-132">In diesem Feld und dem Dialog \_ Feld wird ein Steuerelement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="29bcc-132">This field and the Dialog\_ field together identify a control.</span></span>

</dd> <dt>

<span data-ttu-id="29bcc-133"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Veranstalter</span><span class="sxs-lookup"><span data-stu-id="29bcc-133"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Event</span></span>
</dt> <dd>

<span data-ttu-id="29bcc-134">Dieses Feld ist ein Bezeichner, der den Ereignistyp angibt, der vom Steuerelement abonniert wird.</span><span class="sxs-lookup"><span data-stu-id="29bcc-134">This field is an identifier that specifies the type of event that is subscribed to by the control.</span></span> <span data-ttu-id="29bcc-135">Weitere Informationen finden Sie unter [ControlEvent Overview](controlevent-overview.md).</span><span class="sxs-lookup"><span data-stu-id="29bcc-135">For more information, see [ControlEvent Overview](controlevent-overview.md).</span></span>

</dd> <dt>

<span data-ttu-id="29bcc-136"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Versehen</span><span class="sxs-lookup"><span data-stu-id="29bcc-136"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attribute</span></span>
</dt> <dd>

<span data-ttu-id="29bcc-137">Der Name des Steuerelement \_ Attributs, das festgelegt wird, wenn das Ereignis in der Ereignis Spalte empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="29bcc-137">The name of the Control\_ attribute that is set when the event in the Event column is received.</span></span> <span data-ttu-id="29bcc-138">Das-Argument des-Ereignisses wird als Argument des-Attribut Aufrufes zum Ändern dieses Attributs des-Steuer Elements übermittelt.</span><span class="sxs-lookup"><span data-stu-id="29bcc-138">The Argument of the event is passed as the argument of the attribute call to change this attribute of the control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="29bcc-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="29bcc-139">Remarks</span></span>

<span data-ttu-id="29bcc-140">Die [ControlEvent-Tabelle](controlevent-table.md) gibt die Steuerelement Ereignisse an, die gestartet werden, wenn ein Benutzer mit einem [PUSHBUTTON-Steuer](pushbutton-control.md)Element, [CheckBox-Steuer](checkbox-control.md)Element oder [SelectionTree-Steuer](selectiontree-control.md)Element interagiert.</span><span class="sxs-lookup"><span data-stu-id="29bcc-140">The [ControlEvent Table](controlevent-table.md) specifies the control events that are started when a user interacts with a [PushButton Control](pushbutton-control.md), [CheckBox Control](checkbox-control.md), or [SelectionTree Control](selectiontree-control.md).</span></span> <span data-ttu-id="29bcc-141">Dies sind die einzigen Steuerelemente, die ein Benutzer verwenden kann, um Steuerungs Ereignisse zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="29bcc-141">These are the only controls that a user can use to initiate control events.</span></span>

<span data-ttu-id="29bcc-142">Mehrere Steuerelemente in einem Dialogfeld können dasselbe Ereignis abonnieren.</span><span class="sxs-lookup"><span data-stu-id="29bcc-142">More than one control on a dialog box can subscribe to the same event.</span></span>

<span data-ttu-id="29bcc-143">In der folgenden Liste sind die typischen Verwendungen der Tabelle EventMapping aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="29bcc-143">The following list identifies the typical uses for the EventMapping Table:</span></span>

-   <span data-ttu-id="29bcc-144">So abonnieren Sie [ein Text-Steuer](text-control.md) Element für eine [Action Text ControlEvent](actiontext-controlevent.md)-, [Action Data ControlEvent](actiondata-controlevent.md)-, [scriptinprogress ControlEvent](scriptinprogress-controlevent.md) -oder [timeremaineing ControlEvent](timeremaining-controlevent.md) -Datei, die vom Windows Installer veröffentlicht wurde.</span><span class="sxs-lookup"><span data-stu-id="29bcc-144">To subscribe a [Text Control](text-control.md) to an [ActionText ControlEvent](actiontext-controlevent.md), [ActionData ControlEvent](actiondata-controlevent.md), [ScriptInProgress ControlEvent](scriptinprogress-controlevent.md) or [TimeRemaining ControlEvent](timeremaining-controlevent.md) published by the Windows Installer.</span></span>
-   <span data-ttu-id="29bcc-145">Zum Abonnieren eines [ProgressBar-Steuer](progressbar-control.md) Elements oder eines [Billboard-Steuer](billboard-control.md) Elements für einen [setProgress-ControlEvent](setprogress-controlevent.md).</span><span class="sxs-lookup"><span data-stu-id="29bcc-145">To subscribe a [ProgressBar Control](progressbar-control.md) or [Billboard Control](billboard-control.md) to a [SetProgress ControlEvent](setprogress-controlevent.md).</span></span>
-   <span data-ttu-id="29bcc-146">, Um ein [directoriycombo-Steuer](directorycombo-control.md) Element für [ignorechange ControlEvent](ignorechange-controlevent.md)zu abonnieren.</span><span class="sxs-lookup"><span data-stu-id="29bcc-146">To subscribe a [DirectoryCombo Control](directorycombo-control.md) to an [IgnoreChange ControlEvent](ignorechange-controlevent.md).</span></span>
-   <span data-ttu-id="29bcc-147">Zum automatischen Deaktivieren eines [PUSHBUTTON-Steuer](pushbutton-control.md) Elements, das sich im gleichen Dialogfeld mit einem [SelectionTree-Steuer](selectiontree-control.md)Element befindet.</span><span class="sxs-lookup"><span data-stu-id="29bcc-147">To automatically disable a [PushButton Control](pushbutton-control.md) located on the same dialog with a [SelectionTree Control](selectiontree-control.md).</span></span> <span data-ttu-id="29bcc-148">Um die Schaltfläche "Push" zu deaktivieren, wenn im [SelectionTree-Steuer](selectiontree-control.md)Element keine Features aufgelistet sind, verwenden Sie die EventMapping-Tabelle, um das PUSHBUTTON-Steuerelement einem [selectionnoitems-ControlEvent](selectionnoitems-controlevent.md)zu abonnieren.</span><span class="sxs-lookup"><span data-stu-id="29bcc-148">To disable the push button when no features are listed in the [SelectionTree Control](selectiontree-control.md), use the EventMapping Table to subscribe the PushButton control to a [SelectionNoItems ControlEvent](selectionnoitems-controlevent.md).</span></span> <span data-ttu-id="29bcc-149">Geben Sie im Feld Attribute der Tabelle EventMapping den Wert **enable** ein.</span><span class="sxs-lookup"><span data-stu-id="29bcc-149">Enter **Enable** in the Attributes field of the EventMapping Table.</span></span>
-   <span data-ttu-id="29bcc-150">Zum Anzeigen eines [Text Steuer](text-control.md) Elements, das den Pfad zum Installations Speicherort für das Feature anzeigt, das in einem [SelectionTree-Steuer](selectiontree-control.md) Element im gleichen Dialogfeld ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="29bcc-150">To display a [Text Control](text-control.md) that shows the path to the installation location for the feature that is selected in a [SelectionTree Control](selectiontree-control.md) on the same dialog.</span></span> <span data-ttu-id="29bcc-151">Verwenden Sie die Tabelle EventMapping, um das [Text Steuer](text-control.md) Element sowohl einem [selectionpathon ControlEvent](selectionpathon-controlevent.md) als auch dem [selectionpath ControlEvent](selectionpath-controlevent.md) zu abonnieren, das vom [SelectionTree-Steuer](selectiontree-control.md)Element veröffentlicht wurde.</span><span class="sxs-lookup"><span data-stu-id="29bcc-151">Use the EventMapping Table to subscribe the [Text Control](text-control.md) to both a [SelectionPathOn ControlEvent](selectionpathon-controlevent.md) and [SelectionPath ControlEvent](selectionpath-controlevent.md) published by the [SelectionTree Control](selectiontree-control.md).</span></span>
-   <span data-ttu-id="29bcc-152">Wenn Sie ein [Text Steuer](text-control.md) Element anzeigen möchten, das eine Beschreibung des Elements anzeigt, das in einem [SelectionTree-Steuer](selectiontree-control.md) Element im gleichen Dialogfeld hervorgehoben ist, verwenden Sie die EventMapping-Tabelle, um das [Text Steuer](text-control.md) Element einem [selectiondescription ControlEvent](selectiondescription-controlevent.md), [selectionsize ControlEvent](selectionsize-controlevent.md) oder [selectionaction ControlEvent](selectionaction-controlevent.md)zu abonnieren.</span><span class="sxs-lookup"><span data-stu-id="29bcc-152">To display a [Text Control](text-control.md) that shows a description of the item highlighted in a [SelectionTree Control](selectiontree-control.md) located on the same dialog, use the EventMapping Table to subscribe the [Text Control](text-control.md) to a [SelectionDescription ControlEvent](selectiondescription-controlevent.md), [SelectionSize ControlEvent](selectionsize-controlevent.md) or [SelectionAction ControlEvent](selectionaction-controlevent.md).</span></span> <span data-ttu-id="29bcc-153">Geben Sie im Feld Attribut der Tabelle EventMapping den **Text** ein.</span><span class="sxs-lookup"><span data-stu-id="29bcc-153">Enter **Text** in the Attribute field of the EventMapping Table.</span></span>

## <a name="validation"></a><span data-ttu-id="29bcc-154">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="29bcc-154">Validation</span></span>

<dl>

[<span data-ttu-id="29bcc-155">ICE03</span><span class="sxs-lookup"><span data-stu-id="29bcc-155">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="29bcc-156">ICE06</span><span class="sxs-lookup"><span data-stu-id="29bcc-156">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="29bcc-157">ICE32</span><span class="sxs-lookup"><span data-stu-id="29bcc-157">ICE32</span></span>](ice32.md)  
</dl>

 

 



