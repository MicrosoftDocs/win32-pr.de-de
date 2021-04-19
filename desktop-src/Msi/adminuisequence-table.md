---
description: In der Tabelle AdminUISequence sind Aktionen aufgeführt, die vom Installationsprogramm nacheinander aufgerufen werden, wenn die Administrator Aktion der obersten Ebene ausgeführt wird und die interne Benutzeroberflächen Ebene auf vollständige Benutzeroberfläche oder reduzierte Benutzeroberfläche festgelegt ist.
ms.assetid: 7227846d-b755-4af9-acc3-e27742a5097a
title: AdminUISequence-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8fb460f65d223e75ebd50a7587f5b3f4adeced8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356115"
---
# <a name="adminuisequence-table"></a><span data-ttu-id="065cf-103">AdminUISequence-Tabelle</span><span class="sxs-lookup"><span data-stu-id="065cf-103">AdminUISequence Table</span></span>

<span data-ttu-id="065cf-104">In der Tabelle AdminUISequence sind Aktionen aufgeführt, die vom Installationsprogramm nacheinander aufgerufen werden, wenn die [Administrator Aktion](admin-action.md) der obersten Ebene ausgeführt wird und die interne Benutzeroberflächen Ebene auf vollständige Benutzeroberfläche oder reduzierte Benutzeroberfläche festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="065cf-104">The AdminUISequence table lists actions that the installer calls in sequence when the top-level [ADMIN action](admin-action.md) is executed and the internal user interface level is set to full UI or reduced UI.</span></span> <span data-ttu-id="065cf-105">Das Installationsprogramm überspringt die Aktionen in dieser Tabelle, wenn die Benutzeroberflächen Ebene auf grundlegende Benutzeroberfläche oder keine Benutzeroberfläche festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="065cf-105">The installer skips the actions in this table if the user interface level is set to basic UI or no UI.</span></span> <span data-ttu-id="065cf-106">Weitere [Informationen finden Sie unter Informationen zur Benutzeroberfläche](about-the-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="065cf-106">See [About the User Interface](about-the-user-interface.md).</span></span>

<span data-ttu-id="065cf-107">Administrator Aktionen in der Installations Sequenz bis zur [InstallValidate-Aktion](installvalidate-action.md)und alle Beendigungs Dialogfelder befinden sich in der Tabelle AdminUISequence.</span><span class="sxs-lookup"><span data-stu-id="065cf-107">ADMIN actions in the install sequence up to the [InstallValidate action](installvalidate-action.md), and any exit dialog boxes, are located in the AdminUISequence table.</span></span> <span data-ttu-id="065cf-108">Alle Aktionen von InstallValidate bis zum Ende der Installations Sequenz befinden sich in der [Tabelle "AdminExecuteSequence](adminexecutesequence-table.md)".</span><span class="sxs-lookup"><span data-stu-id="065cf-108">All actions from the InstallValidate through the end of the install sequence are in the [AdminExecuteSequence table](adminexecutesequence-table.md).</span></span> <span data-ttu-id="065cf-109">Da die AdminExecuteSequence-Tabelle eigenständig sein muss, enthält Sie auch alle notwendigen Initialisierungs Aktionen wie [LaunchConditions](launchconditions-action.md), [costinitialize](costinitialize-action.md), [filecost](filecost-action.md)und [costfinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="065cf-109">Because the AdminExecuteSequence table needs to stand alone, it also contains any necessary initialization actions such as [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [FileCost](filecost-action.md), and [CostFinalize](costfinalize-action.md).</span></span> <span data-ttu-id="065cf-110">Es verfügt auch über die [ExecuteAction-Aktion](executeaction-action.md).</span><span class="sxs-lookup"><span data-stu-id="065cf-110">It also has the [ExecuteAction action](executeaction-action.md).</span></span>

<span data-ttu-id="065cf-111">Die Spalten sind identisch mit denen der [Tabelle InstallUISequence](installuisequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="065cf-111">The columns are identical to those of the [InstallUISequence table](installuisequence-table.md).</span></span> <span data-ttu-id="065cf-112">Die AdminUISequence-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="065cf-112">The AdminUISequence table has the following columns.</span></span>



| <span data-ttu-id="065cf-113">Spalte</span><span class="sxs-lookup"><span data-stu-id="065cf-113">Column</span></span>    | <span data-ttu-id="065cf-114">Typ</span><span class="sxs-lookup"><span data-stu-id="065cf-114">Type</span></span>                         | <span data-ttu-id="065cf-115">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="065cf-115">Key</span></span> | <span data-ttu-id="065cf-116">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="065cf-116">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="065cf-117">Aktion</span><span class="sxs-lookup"><span data-stu-id="065cf-117">Action</span></span>    | [<span data-ttu-id="065cf-118">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="065cf-118">Identifier</span></span>](identifier.md) | <span data-ttu-id="065cf-119">J</span><span class="sxs-lookup"><span data-stu-id="065cf-119">Y</span></span>   | <span data-ttu-id="065cf-120">N</span><span class="sxs-lookup"><span data-stu-id="065cf-120">N</span></span>        |
| <span data-ttu-id="065cf-121">Bedingung</span><span class="sxs-lookup"><span data-stu-id="065cf-121">Condition</span></span> | [<span data-ttu-id="065cf-122">Condition</span><span class="sxs-lookup"><span data-stu-id="065cf-122">Condition</span></span>](condition.md)   | <span data-ttu-id="065cf-123">N</span><span class="sxs-lookup"><span data-stu-id="065cf-123">N</span></span>   | <span data-ttu-id="065cf-124">J</span><span class="sxs-lookup"><span data-stu-id="065cf-124">Y</span></span>        |
| <span data-ttu-id="065cf-125">Sequenz</span><span class="sxs-lookup"><span data-stu-id="065cf-125">Sequence</span></span>  | [<span data-ttu-id="065cf-126">Integer</span><span class="sxs-lookup"><span data-stu-id="065cf-126">Integer</span></span>](integer.md)       | <span data-ttu-id="065cf-127">N</span><span class="sxs-lookup"><span data-stu-id="065cf-127">N</span></span>   | <span data-ttu-id="065cf-128">J</span><span class="sxs-lookup"><span data-stu-id="065cf-128">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="065cf-129">Spalten</span><span class="sxs-lookup"><span data-stu-id="065cf-129">Columns</span></span>

<dl> <dt>

<span data-ttu-id="065cf-130"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Hinspiel</span><span class="sxs-lookup"><span data-stu-id="065cf-130"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="065cf-131">Der Name der auszuführenden Aktion.</span><span class="sxs-lookup"><span data-stu-id="065cf-131">Name of the action to execute.</span></span> <span data-ttu-id="065cf-132">Dabei handelt es sich entweder um eine Standardaktion, einen Assistenten für die Benutzeroberfläche oder um eine benutzerdefinierte Aktion, die in der [Tabelle CustomAction](customaction-table.md)aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="065cf-132">This is either a standard action, a user interface wizard, or a custom action listed in the [CustomAction table](customaction-table.md).</span></span>

<span data-ttu-id="065cf-133">Primärer Tabellenschlüssel.</span><span class="sxs-lookup"><span data-stu-id="065cf-133">Primary table key.</span></span>

</dd> <dt>

<span data-ttu-id="065cf-134"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Anlage</span><span class="sxs-lookup"><span data-stu-id="065cf-134"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="065cf-135">Logischer Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="065cf-135">Logical expression.</span></span> <span data-ttu-id="065cf-136">Wenn der Ausdruck zu false ausgewertet wird, wird die Aktion übersprungen.</span><span class="sxs-lookup"><span data-stu-id="065cf-136">If the expression evaluates to false, the action is skipped.</span></span> <span data-ttu-id="065cf-137">Wenn die Ausdruckssyntax ungültig ist, wird die Sequenz beendet und gibt iesbadaktiondata zurück.</span><span class="sxs-lookup"><span data-stu-id="065cf-137">If the expression syntax is invalid, the sequence terminates, returning iesBadActionData.</span></span> <span data-ttu-id="065cf-138">Weitere Informationen zur Syntax von Bedingungs Anweisungen finden Sie unter [Syntax für bedingte](conditional-statement-syntax.md)Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="065cf-138">For information on the syntax of conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="065cf-139"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenz</span><span class="sxs-lookup"><span data-stu-id="065cf-139"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="065cf-140">Ein positiver Wert gibt die Sequenz Position der Aktion an.</span><span class="sxs-lookup"><span data-stu-id="065cf-140">A positive value indicates the sequence position of the action.</span></span> <span data-ttu-id="065cf-141">Die folgenden negativen Werte geben an, dass die Aktion aufgerufen wird, wenn das Installationsprogramm das terminierungsflag zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="065cf-141">The following negative values indicate that the action is called if the installer returns the termination flag.</span></span> <span data-ttu-id="065cf-142">Jedes terminierungsflag (negativer Wert) kann mit nur einer Aktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="065cf-142">Each termination flag (negative value) can be used with no more than one action.</span></span> <span data-ttu-id="065cf-143">Mehrere Aktionen können über Beendigungs Flags verfügen, müssen jedoch unterschiedliche Flags aufweisen.</span><span class="sxs-lookup"><span data-stu-id="065cf-143">Multiple actions can have termination flags, but they must be different flags.</span></span> <span data-ttu-id="065cf-144">Beendigungs Flags (negative Werte) werden in der Regel in [Dialog Feldern](dialog-boxes.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="065cf-144">Termination flags (negative values) are typically used with [Dialog Boxes](dialog-boxes.md).</span></span>



| <span data-ttu-id="065cf-145">Beendigungs Flag</span><span class="sxs-lookup"><span data-stu-id="065cf-145">Termination flag</span></span>          | <span data-ttu-id="065cf-146">Wert</span><span class="sxs-lookup"><span data-stu-id="065cf-146">Value</span></span> | <span data-ttu-id="065cf-147">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="065cf-147">Description</span></span>                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="065cf-148">msidoaktionstatus-Erfolg</span><span class="sxs-lookup"><span data-stu-id="065cf-148">msiDoActionStatusSuccess</span></span>  | <span data-ttu-id="065cf-149">-1</span><span class="sxs-lookup"><span data-stu-id="065cf-149">-1</span></span>    | <span data-ttu-id="065cf-150">Erfolgreicher Abschluss.</span><span class="sxs-lookup"><span data-stu-id="065cf-150">Successful completion.</span></span> <span data-ttu-id="065cf-151">Wird mit den Dialogfeldern " [Beenden](exit-dialog.md) " verwendet.</span><span class="sxs-lookup"><span data-stu-id="065cf-151">Used with [Exit](exit-dialog.md) dialog boxes.</span></span>               |
| <span data-ttu-id="065cf-152">msidoaktionstatus ususerexit</span><span class="sxs-lookup"><span data-stu-id="065cf-152">msiDoActionStatusUserExit</span></span> | <span data-ttu-id="065cf-153">-2</span><span class="sxs-lookup"><span data-stu-id="065cf-153">-2</span></span>    | <span data-ttu-id="065cf-154">Der Benutzer beendet die Installation.</span><span class="sxs-lookup"><span data-stu-id="065cf-154">User terminates install.</span></span> <span data-ttu-id="065cf-155">Wird mit [Userexit](userexit-dialog.md) -Dialogfeldern verwendet.</span><span class="sxs-lookup"><span data-stu-id="065cf-155">Used with [UserExit](userexit-dialog.md) dialog boxes.</span></span>     |
| <span data-ttu-id="065cf-156">msidoaktionstatus-Fehler</span><span class="sxs-lookup"><span data-stu-id="065cf-156">msiDoActionStatusFailure</span></span>  | <span data-ttu-id="065cf-157">-3</span><span class="sxs-lookup"><span data-stu-id="065cf-157">-3</span></span>    | <span data-ttu-id="065cf-158">Schwerwiegender Exit wird beendet.</span><span class="sxs-lookup"><span data-stu-id="065cf-158">Fatal exit terminates.</span></span> <span data-ttu-id="065cf-159">Wird mit den Dialogfeldern " [FatalError](fatalerror-dialog.md) " verwendet.</span><span class="sxs-lookup"><span data-stu-id="065cf-159">Used with a [FatalError](fatalerror-dialog.md) dialog boxes.</span></span> |
| <span data-ttu-id="065cf-160">msidoaktionstatus-Suspend</span><span class="sxs-lookup"><span data-stu-id="065cf-160">msiDoActionStatusSuspend</span></span>  | <span data-ttu-id="065cf-161">–4</span><span class="sxs-lookup"><span data-stu-id="065cf-161">-4</span></span>    | <span data-ttu-id="065cf-162">Die Installation wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="065cf-162">Install is suspended.</span></span>                                                                |



 

<span data-ttu-id="065cf-163">NULL, alle anderen negativen Zahlen oder ein NULL-Wert geben an, dass die Aktion nie aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="065cf-163">Zero, all other negative numbers, or a null value indicate that the action is never called.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="065cf-164">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="065cf-164">Validation</span></span>

<dl>

[<span data-ttu-id="065cf-165">ICE03</span><span class="sxs-lookup"><span data-stu-id="065cf-165">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="065cf-166">ICE06</span><span class="sxs-lookup"><span data-stu-id="065cf-166">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="065cf-167">ICE12</span><span class="sxs-lookup"><span data-stu-id="065cf-167">ICE12</span></span>](ice12.md)  
[<span data-ttu-id="065cf-168">ICE13</span><span class="sxs-lookup"><span data-stu-id="065cf-168">ICE13</span></span>](ice13.md)  
[<span data-ttu-id="065cf-169">ICE20</span><span class="sxs-lookup"><span data-stu-id="065cf-169">ICE20</span></span>](ice20.md)  
[<span data-ttu-id="065cf-170">ICE26</span><span class="sxs-lookup"><span data-stu-id="065cf-170">ICE26</span></span>](ice26.md)  
[<span data-ttu-id="065cf-171">ICE27</span><span class="sxs-lookup"><span data-stu-id="065cf-171">ICE27</span></span>](ice27.md)  
[<span data-ttu-id="065cf-172">ICE28</span><span class="sxs-lookup"><span data-stu-id="065cf-172">ICE28</span></span>](ice28.md)  
[<span data-ttu-id="065cf-173">ICE46</span><span class="sxs-lookup"><span data-stu-id="065cf-173">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="065cf-174">ICE75</span><span class="sxs-lookup"><span data-stu-id="065cf-174">ICE75</span></span>](ice75.md)  
[<span data-ttu-id="065cf-175">ICE79</span><span class="sxs-lookup"><span data-stu-id="065cf-175">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="065cf-176">ICE82</span><span class="sxs-lookup"><span data-stu-id="065cf-176">ICE82</span></span>](ice82.md)  
[<span data-ttu-id="065cf-177">ICE84</span><span class="sxs-lookup"><span data-stu-id="065cf-177">ICE84</span></span>](ice84.md)  
[<span data-ttu-id="065cf-178">ICE86</span><span class="sxs-lookup"><span data-stu-id="065cf-178">ICE86</span></span>](ice86.md)  
[<span data-ttu-id="065cf-179">ICE96</span><span class="sxs-lookup"><span data-stu-id="065cf-179">ICE96</span></span>](ice96.md)  
[<span data-ttu-id="065cf-180">ICEM04</span><span class="sxs-lookup"><span data-stu-id="065cf-180">ICEM04</span></span>](icem04.md)  
</dl>

 

 



