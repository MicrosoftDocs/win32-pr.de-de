---
description: Die Tabelle InstallExecuteSequence listet Aktionen auf, die ausgeführt werden, wenn die Installations Aktion der obersten Ebene ausgeführt wird.
ms.assetid: 995d4159-bfc9-48b2-8328-3ae8251d785d
title: InstallExecuteSequence-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7d110debacab19739c3da69abf3948d11bb7aa6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862343"
---
# <a name="installexecutesequence-table"></a><span data-ttu-id="e4550-103">InstallExecuteSequence-Tabelle</span><span class="sxs-lookup"><span data-stu-id="e4550-103">InstallExecuteSequence Table</span></span>

<span data-ttu-id="e4550-104">Die Tabelle InstallExecuteSequence listet Aktionen auf, die ausgeführt werden, wenn die [Installations Aktion](install-action.md) der obersten Ebene ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e4550-104">The InstallExecuteSequence table lists actions that are executed when the top-level [INSTALL action](install-action.md) is executed.</span></span>

<span data-ttu-id="e4550-105">Aktionen in der Installations Sequenz bis zur [InstallValidate-Aktion](installvalidate-action.md)und alle Beendigungs Dialogfelder befinden sich in der [Tabelle InstallUISequence](installuisequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="e4550-105">Actions in the install sequence up to the [InstallValidate action](installvalidate-action.md), and any exit dialog boxes, are located in the [InstallUISequence table](installuisequence-table.md).</span></span> <span data-ttu-id="e4550-106">Alle Aktionen von InstallValidate bis zum Ende der Installations Sequenz befinden sich in der InstallExecuteSequence-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e4550-106">All actions from the InstallValidate through the end of the install sequence are in the InstallExecuteSequence table.</span></span> <span data-ttu-id="e4550-107">Da die InstallExecuteSequence-Tabelle eigenständig sein muss, sind alle erforderlichen Initialisierungs Aktionen wie z. b. die [LaunchConditions](launchconditions-action.md)-, [costinitialize](costinitialize-action.md)-, [filecost](filecost-action.md)-und [costfinalize](costfinalize-action.md) -Aktionen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e4550-107">Because the InstallExecuteSequence table needs to stand alone, it has any necessary initialization actions such as the [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [FileCost](filecost-action.md), and [CostFinalize](costfinalize-action.md) actions.</span></span>

<span data-ttu-id="e4550-108">[Benutzerdefinierte Aktionen](custom-actions.md) , für die eine Benutzeroberfläche erforderlich ist, sollten [**msiprocessmessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) anstelle von erstellten Dialogfeldern verwenden, die mithilfe der [Dialogfeld Tabelle](dialog-table.md)erstellt wurden</span><span class="sxs-lookup"><span data-stu-id="e4550-108">[Custom actions](custom-actions.md) requiring a user interface should use [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) instead of authored dialog boxes created using the [Dialog table](dialog-table.md).</span></span>

<span data-ttu-id="e4550-109">Die InstallExecuteSequence-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="e4550-109">The InstallExecuteSequence table has the following columns.</span></span>



| <span data-ttu-id="e4550-110">Spalte</span><span class="sxs-lookup"><span data-stu-id="e4550-110">Column</span></span>    | <span data-ttu-id="e4550-111">Typ</span><span class="sxs-lookup"><span data-stu-id="e4550-111">Type</span></span>                         | <span data-ttu-id="e4550-112">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="e4550-112">Key</span></span> | <span data-ttu-id="e4550-113">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="e4550-113">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="e4550-114">Aktion</span><span class="sxs-lookup"><span data-stu-id="e4550-114">Action</span></span>    | [<span data-ttu-id="e4550-115">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="e4550-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="e4550-116">J</span><span class="sxs-lookup"><span data-stu-id="e4550-116">Y</span></span>   | <span data-ttu-id="e4550-117">N</span><span class="sxs-lookup"><span data-stu-id="e4550-117">N</span></span>        |
| <span data-ttu-id="e4550-118">Bedingung</span><span class="sxs-lookup"><span data-stu-id="e4550-118">Condition</span></span> | [<span data-ttu-id="e4550-119">Condition</span><span class="sxs-lookup"><span data-stu-id="e4550-119">Condition</span></span>](condition.md)   | <span data-ttu-id="e4550-120">N</span><span class="sxs-lookup"><span data-stu-id="e4550-120">N</span></span>   | <span data-ttu-id="e4550-121">J</span><span class="sxs-lookup"><span data-stu-id="e4550-121">Y</span></span>        |
| <span data-ttu-id="e4550-122">Sequenz</span><span class="sxs-lookup"><span data-stu-id="e4550-122">Sequence</span></span>  | [<span data-ttu-id="e4550-123">Integer</span><span class="sxs-lookup"><span data-stu-id="e4550-123">Integer</span></span>](integer.md)       | <span data-ttu-id="e4550-124">N</span><span class="sxs-lookup"><span data-stu-id="e4550-124">N</span></span>   | <span data-ttu-id="e4550-125">J</span><span class="sxs-lookup"><span data-stu-id="e4550-125">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="e4550-126">Spalten</span><span class="sxs-lookup"><span data-stu-id="e4550-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="e4550-127"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Hinspiel</span><span class="sxs-lookup"><span data-stu-id="e4550-127"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="e4550-128">Der Name der auszuführenden Aktion.</span><span class="sxs-lookup"><span data-stu-id="e4550-128">Name of the action to execute.</span></span> <span data-ttu-id="e4550-129">Dabei handelt es sich entweder um eine integrierte Aktion oder um eine benutzerdefinierte Aktion.</span><span class="sxs-lookup"><span data-stu-id="e4550-129">This is either a built-in action or a custom action.</span></span>

<span data-ttu-id="e4550-130">Primärer Tabellenschlüssel.</span><span class="sxs-lookup"><span data-stu-id="e4550-130">Primary table key.</span></span>

</dd> <dt>

<span data-ttu-id="e4550-131"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Anlage</span><span class="sxs-lookup"><span data-stu-id="e4550-131"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="e4550-132">Dieses Feld enthält einen bedingten Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="e4550-132">This field contains a conditional expression.</span></span> <span data-ttu-id="e4550-133">Wenn der Ausdruck zu false ausgewertet wird, wird die Aktion übersprungen.</span><span class="sxs-lookup"><span data-stu-id="e4550-133">If the expression evaluates to False, then the action is skipped.</span></span> <span data-ttu-id="e4550-134">Wenn die Ausdruckssyntax ungültig ist, wird die Sequenz beendet und gibt iesbadaktiondata zurück.</span><span class="sxs-lookup"><span data-stu-id="e4550-134">If the expression syntax is invalid, then the sequence terminates, returning iesBadActionData.</span></span> <span data-ttu-id="e4550-135">Weitere Informationen zur Syntax von Bedingungs Anweisungen finden Sie unter [Syntax für bedingte](conditional-statement-syntax.md)Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="e4550-135">For information on the syntax of conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4550-136"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenz</span><span class="sxs-lookup"><span data-stu-id="e4550-136"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="e4550-137">Zahl, die die Sequenz Position bestimmt, in der diese Aktion ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e4550-137">Number that determines the sequence position in which this action is to be executed.</span></span>

<span data-ttu-id="e4550-138">Ein positiver Wert stellt die Sequenz Position dar.</span><span class="sxs-lookup"><span data-stu-id="e4550-138">A positive value represents the sequence position.</span></span> <span data-ttu-id="e4550-139">Ein NULL-Wert gibt an, dass die Aktion nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e4550-139">A Null value indicates that the action is not executed.</span></span> <span data-ttu-id="e4550-140">Die folgenden negativen Werte geben an, dass diese Aktion ausgeführt werden soll, wenn das Installationsprogramm das zugehörige Beendigungs Flag zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="e4550-140">The following negative values indicate that this action is to be executed if the installer returns the associated termination flag.</span></span> <span data-ttu-id="e4550-141">Jedes terminierungsflag (negativer Wert) kann mit nur einer Aktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e4550-141">Each termination flag (negative value) can be used with no more than one action.</span></span> <span data-ttu-id="e4550-142">Mehrere Aktionen können über Beendigungs Flags verfügen, müssen jedoch unterschiedliche Flags aufweisen.</span><span class="sxs-lookup"><span data-stu-id="e4550-142">Multiple actions can have termination flags, but they must be different flags.</span></span> <span data-ttu-id="e4550-143">Beendigungs Flags (negative Werte) werden in der Regel in [Dialog Feldern](dialog-boxes.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="e4550-143">Termination flags (negative values) are typically used with [Dialog Boxes](dialog-boxes.md).</span></span>



| <span data-ttu-id="e4550-144">Beendigungs Flag</span><span class="sxs-lookup"><span data-stu-id="e4550-144">Termination flag</span></span>          | <span data-ttu-id="e4550-145">Wert</span><span class="sxs-lookup"><span data-stu-id="e4550-145">Value</span></span> | <span data-ttu-id="e4550-146">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e4550-146">Description</span></span>                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e4550-147">msidoaktionstatus-Erfolg</span><span class="sxs-lookup"><span data-stu-id="e4550-147">msiDoActionStatusSuccess</span></span>  | <span data-ttu-id="e4550-148">-1</span><span class="sxs-lookup"><span data-stu-id="e4550-148">-1</span></span>    | <span data-ttu-id="e4550-149">Erfolgreicher Abschluss.</span><span class="sxs-lookup"><span data-stu-id="e4550-149">Successful completion.</span></span> <span data-ttu-id="e4550-150">Wird mit den Dialogfeldern " [Beenden](exit-dialog.md) " verwendet.</span><span class="sxs-lookup"><span data-stu-id="e4550-150">Used with [Exit](exit-dialog.md) dialog boxes.</span></span>               |
| <span data-ttu-id="e4550-151">msidoaktionstatus ususerexit</span><span class="sxs-lookup"><span data-stu-id="e4550-151">msiDoActionStatusUserExit</span></span> | <span data-ttu-id="e4550-152">-2</span><span class="sxs-lookup"><span data-stu-id="e4550-152">-2</span></span>    | <span data-ttu-id="e4550-153">Der Benutzer beendet die Installation.</span><span class="sxs-lookup"><span data-stu-id="e4550-153">User terminates install.</span></span> <span data-ttu-id="e4550-154">Wird mit [Userexit](userexit-dialog.md) -Dialogfeldern verwendet.</span><span class="sxs-lookup"><span data-stu-id="e4550-154">Used with [UserExit](userexit-dialog.md) dialog boxes.</span></span>     |
| <span data-ttu-id="e4550-155">msidoaktionstatus-Fehler</span><span class="sxs-lookup"><span data-stu-id="e4550-155">msiDoActionStatusFailure</span></span>  | <span data-ttu-id="e4550-156">-3</span><span class="sxs-lookup"><span data-stu-id="e4550-156">-3</span></span>    | <span data-ttu-id="e4550-157">Schwerwiegender Exit wird beendet.</span><span class="sxs-lookup"><span data-stu-id="e4550-157">Fatal exit terminates.</span></span> <span data-ttu-id="e4550-158">Wird mit den Dialogfeldern " [FatalError](fatalerror-dialog.md) " verwendet.</span><span class="sxs-lookup"><span data-stu-id="e4550-158">Used with a [FatalError](fatalerror-dialog.md) dialog boxes.</span></span> |
| <span data-ttu-id="e4550-159">msidoaktionstatus-Suspend</span><span class="sxs-lookup"><span data-stu-id="e4550-159">msiDoActionStatusSuspend</span></span>  | <span data-ttu-id="e4550-160">–4</span><span class="sxs-lookup"><span data-stu-id="e4550-160">-4</span></span>    | <span data-ttu-id="e4550-161">Die Installation wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="e4550-161">Install is suspended.</span></span>                                                                |



 

<span data-ttu-id="e4550-162">NULL, alle anderen negativen Zahlen oder ein NULL-Wert geben an, dass die Aktion nie ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e4550-162">Zero, all other negative numbers, or a Null value indicate that the action is never run.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e4550-163">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e4550-163">Remarks</span></span>

<span data-ttu-id="e4550-164">Der lokalisierte Text für die Fortschrittsanzeige oder die Protokollierung wird in der [Tabelle "aktiontext](actiontext-table.md)" angegeben.</span><span class="sxs-lookup"><span data-stu-id="e4550-164">Localized text for progress display or logging is specified in the [ActionText table](actiontext-table.md).</span></span>

<span data-ttu-id="e4550-165">Ein Beispiel für eine Sequenz Tabelle finden Sie unter [Verwenden einer Sequenz Tabelle](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="e4550-165">For an example of a sequence table, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="e4550-166">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="e4550-166">Validation</span></span>

<dl>

[<span data-ttu-id="e4550-167">ICE03</span><span class="sxs-lookup"><span data-stu-id="e4550-167">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="e4550-168">ICE06</span><span class="sxs-lookup"><span data-stu-id="e4550-168">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="e4550-169">ICE12</span><span class="sxs-lookup"><span data-stu-id="e4550-169">ICE12</span></span>](ice12.md)  
[<span data-ttu-id="e4550-170">ICE13</span><span class="sxs-lookup"><span data-stu-id="e4550-170">ICE13</span></span>](ice13.md)  
[<span data-ttu-id="e4550-171">ICE26</span><span class="sxs-lookup"><span data-stu-id="e4550-171">ICE26</span></span>](ice26.md)  
[<span data-ttu-id="e4550-172">ICE27</span><span class="sxs-lookup"><span data-stu-id="e4550-172">ICE27</span></span>](ice27.md)  
[<span data-ttu-id="e4550-173">ICE28</span><span class="sxs-lookup"><span data-stu-id="e4550-173">ICE28</span></span>](ice28.md)  
[<span data-ttu-id="e4550-174">ICE46</span><span class="sxs-lookup"><span data-stu-id="e4550-174">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="e4550-175">ICE63</span><span class="sxs-lookup"><span data-stu-id="e4550-175">ICE63</span></span>](ice63.md)  
[<span data-ttu-id="e4550-176">ICE75</span><span class="sxs-lookup"><span data-stu-id="e4550-176">ICE75</span></span>](ice75.md)  
[<span data-ttu-id="e4550-177">ICE77</span><span class="sxs-lookup"><span data-stu-id="e4550-177">ICE77</span></span>](ice77.md)  
[<span data-ttu-id="e4550-178">ICE79</span><span class="sxs-lookup"><span data-stu-id="e4550-178">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="e4550-179">ICE82</span><span class="sxs-lookup"><span data-stu-id="e4550-179">ICE82</span></span>](ice82.md)  
[<span data-ttu-id="e4550-180">ICE83</span><span class="sxs-lookup"><span data-stu-id="e4550-180">ICE83</span></span>](ice83.md)  
[<span data-ttu-id="e4550-181">ICE84</span><span class="sxs-lookup"><span data-stu-id="e4550-181">ICE84</span></span>](ice84.md)  
[<span data-ttu-id="e4550-182">ICE86</span><span class="sxs-lookup"><span data-stu-id="e4550-182">ICE86</span></span>](ice86.md)  
</dl>

 

 



