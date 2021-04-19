---
description: In der Tabelle InstallUISequence sind Aktionen aufgeführt, die ausgeführt werden, wenn die Installations Aktion der obersten Ebene ausgeführt wird und die Ebene der internen Benutzeroberfläche auf vollständige Benutzeroberfläche oder reduzierte Benutzeroberfläche festgelegt ist.
ms.assetid: 076d7c14-e302-4465-aed5-27a4b1f70ac8
title: InstallUISequence-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19a4d8d3033645ac1f414e3aff67be2a26d7a6ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373274"
---
# <a name="installuisequence-table"></a><span data-ttu-id="4409c-103">InstallUISequence-Tabelle</span><span class="sxs-lookup"><span data-stu-id="4409c-103">InstallUISequence Table</span></span>

<span data-ttu-id="4409c-104">In der Tabelle InstallUISequence sind Aktionen aufgeführt, die ausgeführt werden, wenn die [Installations Aktion](install-action.md) der obersten Ebene ausgeführt wird und die Ebene der internen Benutzeroberfläche auf vollständige Benutzeroberfläche oder reduzierte Benutzeroberfläche festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="4409c-104">The InstallUISequence table lists actions that are executed when the top-level [INSTALL action](install-action.md) is executed and the internal user interface level is set to full UI or reduced UI.</span></span> <span data-ttu-id="4409c-105">Das Installationsprogramm überspringt die Aktionen in dieser Tabelle, wenn die Benutzeroberflächen Ebene auf grundlegende Benutzeroberfläche oder keine Benutzeroberfläche festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="4409c-105">The installer skips the actions in this table if the user interface level is set to basic UI or no UI.</span></span> <span data-ttu-id="4409c-106">Weitere [Informationen finden Sie unter Informationen zur Benutzeroberfläche](about-the-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="4409c-106">See [About the User Interface](about-the-user-interface.md).</span></span>

<span data-ttu-id="4409c-107">Aktionen in der Installations Sequenz bis zur [InstallValidate-Aktion](installvalidate-action.md)und die Dialogfelder beenden befinden sich in der Tabelle InstallUISequence.</span><span class="sxs-lookup"><span data-stu-id="4409c-107">Actions in the install sequence up to the [InstallValidate action](installvalidate-action.md), and the exit dialog boxes, are located in the InstallUISequence table.</span></span> <span data-ttu-id="4409c-108">Alle Aktionen von InstallValidate bis zum Ende der Installations Sequenz befinden sich in der [InstallExecuteSequence-Tabelle](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="4409c-108">All actions from the InstallValidate through the end of the install sequence are in the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="4409c-109">Da die InstallExecuteSequence-Tabelle eigenständig sein muss, sind alle erforderlichen Initialisierungs Aktionen wie z. b. [LaunchConditions](launchconditions-action.md), [costinitialize](costinitialize-action.md), [filecost](filecost-action.md)und die Aktion " [costfinalize](costfinalize-action.md)" und " [ExecuteAction](executeaction-action.md)" erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4409c-109">Because the InstallExecuteSequence table needs to stand alone, it has any necessary initialization actions such as the [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [FileCost](filecost-action.md), and the [CostFinalize](costfinalize-action.md), and [ExecuteAction action](executeaction-action.md).</span></span>

<span data-ttu-id="4409c-110">Die Tabelle "InstallUISequence" weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="4409c-110">The InstallUISequence table has the following columns.</span></span>



| <span data-ttu-id="4409c-111">Spalte</span><span class="sxs-lookup"><span data-stu-id="4409c-111">Column</span></span>    | <span data-ttu-id="4409c-112">Typ</span><span class="sxs-lookup"><span data-stu-id="4409c-112">Type</span></span>                         | <span data-ttu-id="4409c-113">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="4409c-113">Key</span></span> | <span data-ttu-id="4409c-114">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="4409c-114">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="4409c-115">Aktion</span><span class="sxs-lookup"><span data-stu-id="4409c-115">Action</span></span>    | [<span data-ttu-id="4409c-116">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="4409c-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="4409c-117">J</span><span class="sxs-lookup"><span data-stu-id="4409c-117">Y</span></span>   | <span data-ttu-id="4409c-118">N</span><span class="sxs-lookup"><span data-stu-id="4409c-118">N</span></span>        |
| <span data-ttu-id="4409c-119">Bedingung</span><span class="sxs-lookup"><span data-stu-id="4409c-119">Condition</span></span> | [<span data-ttu-id="4409c-120">Condition</span><span class="sxs-lookup"><span data-stu-id="4409c-120">Condition</span></span>](condition.md)   | <span data-ttu-id="4409c-121">N</span><span class="sxs-lookup"><span data-stu-id="4409c-121">N</span></span>   | <span data-ttu-id="4409c-122">J</span><span class="sxs-lookup"><span data-stu-id="4409c-122">Y</span></span>        |
| <span data-ttu-id="4409c-123">Sequenz</span><span class="sxs-lookup"><span data-stu-id="4409c-123">Sequence</span></span>  | [<span data-ttu-id="4409c-124">Integer</span><span class="sxs-lookup"><span data-stu-id="4409c-124">Integer</span></span>](integer.md)       | <span data-ttu-id="4409c-125">N</span><span class="sxs-lookup"><span data-stu-id="4409c-125">N</span></span>   | <span data-ttu-id="4409c-126">J</span><span class="sxs-lookup"><span data-stu-id="4409c-126">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="4409c-127">Spalten</span><span class="sxs-lookup"><span data-stu-id="4409c-127">Columns</span></span>

<dl> <dt>

<span data-ttu-id="4409c-128"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Hinspiel</span><span class="sxs-lookup"><span data-stu-id="4409c-128"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="4409c-129">Der Name der auszuführenden Aktion.</span><span class="sxs-lookup"><span data-stu-id="4409c-129">Name of the action to execute.</span></span> <span data-ttu-id="4409c-130">Dabei handelt es sich entweder um eine integrierte Aktion, eine benutzerdefinierte Aktion oder einen Assistenten für die Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="4409c-130">This is either a built-in action, a custom action, or a user interface wizard.</span></span>

<span data-ttu-id="4409c-131">Primärer Tabellenschlüssel.</span><span class="sxs-lookup"><span data-stu-id="4409c-131">Primary table key.</span></span>

</dd> <dt>

<span data-ttu-id="4409c-132"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Anlage</span><span class="sxs-lookup"><span data-stu-id="4409c-132"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="4409c-133">Dieses Feld enthält einen bedingten Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="4409c-133">This field contains a conditional expression.</span></span> <span data-ttu-id="4409c-134">Wenn der Ausdruck zu false ausgewertet wird, wird die Aktion übersprungen.</span><span class="sxs-lookup"><span data-stu-id="4409c-134">If the expression evaluates to False, then the action is skipped.</span></span> <span data-ttu-id="4409c-135">Wenn die Ausdruckssyntax ungültig ist, wird die Sequenz beendet und gibt iesbadaktiondata zurück.</span><span class="sxs-lookup"><span data-stu-id="4409c-135">If the expression syntax is invalid, then the sequence terminates, returning iesBadActionData.</span></span> <span data-ttu-id="4409c-136">Weitere Informationen zur Syntax von Bedingungs Anweisungen finden Sie unter [Syntax für bedingte](conditional-statement-syntax.md)Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="4409c-136">For information on the syntax of conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="4409c-137"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenz</span><span class="sxs-lookup"><span data-stu-id="4409c-137"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="4409c-138">Die Zahl in dieser Spalte bestimmt die Sequenz Position, in der diese Aktion ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4409c-138">The number in this column determines the sequence position in which this action is run.</span></span>

<span data-ttu-id="4409c-139">Ein positiver Wert stellt die Sequenz Position dar.</span><span class="sxs-lookup"><span data-stu-id="4409c-139">A positive value represents the sequence position.</span></span> <span data-ttu-id="4409c-140">Ein NULL-Wert gibt an, dass die Aktion nie ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4409c-140">A Null value indicates that the action is never run.</span></span> <span data-ttu-id="4409c-141">Die folgenden negativen Werte geben an, dass diese Aktion ausgeführt wird, wenn das Installationsprogramm das zugehörige Beendigungs Flag zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="4409c-141">The following negative values indicate that this action is executed if the installer returns the associated termination flag.</span></span> <span data-ttu-id="4409c-142">Jedes terminierungsflag (negativer Wert) kann mit nur einer Aktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4409c-142">Each termination flag (negative value) can be used with no more than one action.</span></span> <span data-ttu-id="4409c-143">Mehrere Aktionen können über Beendigungs Flags verfügen, müssen jedoch unterschiedliche Flags aufweisen.</span><span class="sxs-lookup"><span data-stu-id="4409c-143">Multiple actions can have termination flags, but they must be different flags.</span></span> <span data-ttu-id="4409c-144">Beendigungs Flags (negative Werte) werden in der Regel in [Dialog Feldern](dialog-boxes.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="4409c-144">Termination flags (negative values) are typically used with [Dialog Boxes](dialog-boxes.md).</span></span>



| <span data-ttu-id="4409c-145">Beendigungs Flag</span><span class="sxs-lookup"><span data-stu-id="4409c-145">Termination flag</span></span>          | <span data-ttu-id="4409c-146">Wert</span><span class="sxs-lookup"><span data-stu-id="4409c-146">Value</span></span> | <span data-ttu-id="4409c-147">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4409c-147">Description</span></span>                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4409c-148">msidoaktionstatus-Erfolg</span><span class="sxs-lookup"><span data-stu-id="4409c-148">msiDoActionStatusSuccess</span></span>  | <span data-ttu-id="4409c-149">-1</span><span class="sxs-lookup"><span data-stu-id="4409c-149">-1</span></span>    | <span data-ttu-id="4409c-150">Erfolgreicher Abschluss.</span><span class="sxs-lookup"><span data-stu-id="4409c-150">Successful completion.</span></span> <span data-ttu-id="4409c-151">Wird mit den Dialogfeldern " [Beenden](exit-dialog.md) " verwendet.</span><span class="sxs-lookup"><span data-stu-id="4409c-151">Used with [Exit](exit-dialog.md) dialog boxes.</span></span>               |
| <span data-ttu-id="4409c-152">msidoaktionstatus ususerexit</span><span class="sxs-lookup"><span data-stu-id="4409c-152">msiDoActionStatusUserExit</span></span> | <span data-ttu-id="4409c-153">-2</span><span class="sxs-lookup"><span data-stu-id="4409c-153">-2</span></span>    | <span data-ttu-id="4409c-154">Der Benutzer beendet die Installation.</span><span class="sxs-lookup"><span data-stu-id="4409c-154">User terminates install.</span></span> <span data-ttu-id="4409c-155">Wird mit [Userexit](userexit-dialog.md) -Dialogfeldern verwendet.</span><span class="sxs-lookup"><span data-stu-id="4409c-155">Used with [UserExit](userexit-dialog.md) dialog boxes.</span></span>     |
| <span data-ttu-id="4409c-156">msidoaktionstatus-Fehler</span><span class="sxs-lookup"><span data-stu-id="4409c-156">msiDoActionStatusFailure</span></span>  | <span data-ttu-id="4409c-157">-3</span><span class="sxs-lookup"><span data-stu-id="4409c-157">-3</span></span>    | <span data-ttu-id="4409c-158">Schwerwiegender Exit wird beendet.</span><span class="sxs-lookup"><span data-stu-id="4409c-158">Fatal exit terminates.</span></span> <span data-ttu-id="4409c-159">Wird mit den Dialogfeldern " [FatalError](fatalerror-dialog.md) " verwendet.</span><span class="sxs-lookup"><span data-stu-id="4409c-159">Used with a [FatalError](fatalerror-dialog.md) dialog boxes.</span></span> |
| <span data-ttu-id="4409c-160">msidoaktionstatus-Suspend</span><span class="sxs-lookup"><span data-stu-id="4409c-160">msiDoActionStatusSuspend</span></span>  | <span data-ttu-id="4409c-161">–4</span><span class="sxs-lookup"><span data-stu-id="4409c-161">-4</span></span>    | <span data-ttu-id="4409c-162">Die Installation wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="4409c-162">Install is suspended.</span></span>                                                                |



 

<span data-ttu-id="4409c-163">NULL, alle anderen negativen Zahlen oder ein NULL-Wert geben an, dass die Aktion nie ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4409c-163">Zero, all other negative numbers, or a Null value indicate that the action is never run.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4409c-164">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4409c-164">Remarks</span></span>

<span data-ttu-id="4409c-165">Der zugeordnete lokalisierte Text für die Statusanzeige oder Protokollierung wird in der [Tabelle "aktiontext](actiontext-table.md)" angegeben.</span><span class="sxs-lookup"><span data-stu-id="4409c-165">Associated localized text for progress display or logging is specified in the [ActionText table](actiontext-table.md).</span></span>

<span data-ttu-id="4409c-166">Ein Beispiel für eine Sequenz Tabelle finden Sie unter [Verwenden einer Sequenz Tabelle](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="4409c-166">For an example of a sequence table, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="4409c-167">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="4409c-167">Validation</span></span>

<dl>

[<span data-ttu-id="4409c-168">ICE03</span><span class="sxs-lookup"><span data-stu-id="4409c-168">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="4409c-169">ICE06</span><span class="sxs-lookup"><span data-stu-id="4409c-169">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="4409c-170">ICE12</span><span class="sxs-lookup"><span data-stu-id="4409c-170">ICE12</span></span>](ice12.md)  
[<span data-ttu-id="4409c-171">ICE13</span><span class="sxs-lookup"><span data-stu-id="4409c-171">ICE13</span></span>](ice13.md)  
[<span data-ttu-id="4409c-172">ICE20</span><span class="sxs-lookup"><span data-stu-id="4409c-172">ICE20</span></span>](ice20.md)  
[<span data-ttu-id="4409c-173">ICE26</span><span class="sxs-lookup"><span data-stu-id="4409c-173">ICE26</span></span>](ice26.md)  
[<span data-ttu-id="4409c-174">ICE27</span><span class="sxs-lookup"><span data-stu-id="4409c-174">ICE27</span></span>](ice27.md)  
[<span data-ttu-id="4409c-175">ICE28</span><span class="sxs-lookup"><span data-stu-id="4409c-175">ICE28</span></span>](ice28.md)  
[<span data-ttu-id="4409c-176">ICE46</span><span class="sxs-lookup"><span data-stu-id="4409c-176">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="4409c-177">ICE75</span><span class="sxs-lookup"><span data-stu-id="4409c-177">ICE75</span></span>](ice75.md)  
[<span data-ttu-id="4409c-178">ICE79</span><span class="sxs-lookup"><span data-stu-id="4409c-178">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="4409c-179">ICE82</span><span class="sxs-lookup"><span data-stu-id="4409c-179">ICE82</span></span>](ice82.md)  
[<span data-ttu-id="4409c-180">ICE86</span><span class="sxs-lookup"><span data-stu-id="4409c-180">ICE86</span></span>](ice86.md)  
</dl>

 

 



