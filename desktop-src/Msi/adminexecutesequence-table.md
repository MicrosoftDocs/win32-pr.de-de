---
description: Die Tabelle AdminExecuteSequence listet Aktionen auf, die der Installer nacheinander aufruft, wenn die Administrator Aktion der obersten Ebene ausgeführt wird.
ms.assetid: 33a2ef50-519b-424e-b510-55c21c5706a3
title: AdminExecuteSequence-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0c62ae43f8436ab210765e5402751c5722b78b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357524"
---
# <a name="adminexecutesequence-table"></a><span data-ttu-id="1e826-103">AdminExecuteSequence-Tabelle</span><span class="sxs-lookup"><span data-stu-id="1e826-103">AdminExecuteSequence Table</span></span>

<span data-ttu-id="1e826-104">Die Tabelle AdminExecuteSequence listet Aktionen auf, die der Installer nacheinander aufruft, wenn die [Administrator Aktion](admin-action.md) der obersten Ebene ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1e826-104">The AdminExecuteSequence table lists actions that the installer calls in sequence when the top-level [ADMIN action](admin-action.md) is executed.</span></span>

<span data-ttu-id="1e826-105">Administrator Aktionen in der Installations Sequenz, bis zur [InstallValidate-Aktion](installvalidate-action.md) und zu beliebigen Beendigungs Dialogfeldern, befinden sich in der [Tabelle AdminUISequence](adminuisequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="1e826-105">ADMIN actions in the install sequence, up to the [InstallValidate action](installvalidate-action.md) and any exit dialog boxes, are located in the [AdminUISequence table](adminuisequence-table.md).</span></span>

<span data-ttu-id="1e826-106">Administrator Aktionen aus der InstallValidate-Aktion bis zum Ende der Installations Sequenz befinden sich in der AdminExecuteSequence-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="1e826-106">ADMIN actions from the InstallValidate action through the end of the install sequence are in the AdminExecuteSequence table.</span></span> <span data-ttu-id="1e826-107">Da die AdminExecuteSequence-Tabelle eigenständig sein muss, enthält Sie auch alle notwendigen Initialisierungs Aktionen wie [LaunchConditions](launchconditions-action.md), [costinitialize](costinitialize-action.md), [filecost](filecost-action.md)und [costfinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="1e826-107">Because the AdminExecuteSequence table needs to stand alone, it also contains any necessary initialization actions such as [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [FileCost](filecost-action.md), and [CostFinalize](costfinalize-action.md).</span></span>

<span data-ttu-id="1e826-108">[Benutzerdefinierte Aktionen](custom-actions.md) , für die eine Benutzeroberfläche erforderlich ist, sollten [**msiprocessmessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) anstelle von erstellten Dialogfeldern verwenden, die mithilfe der [Dialogfeld Tabelle](dialog-table.md)erstellt wurden</span><span class="sxs-lookup"><span data-stu-id="1e826-108">[Custom actions](custom-actions.md) requiring a user interface should use [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) instead of authored dialog boxes created using the [Dialog table](dialog-table.md).</span></span>

<span data-ttu-id="1e826-109">Die Spalten sind identisch mit denen der [InstallExecuteSequence-Tabelle](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="1e826-109">The columns are identical to those of the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="1e826-110">Die AdminExecuteSequence-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="1e826-110">The AdminExecuteSequence table has the following columns.</span></span>



| <span data-ttu-id="1e826-111">Spalte</span><span class="sxs-lookup"><span data-stu-id="1e826-111">Column</span></span>    | <span data-ttu-id="1e826-112">Typ</span><span class="sxs-lookup"><span data-stu-id="1e826-112">Type</span></span>                         | <span data-ttu-id="1e826-113">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="1e826-113">Key</span></span> | <span data-ttu-id="1e826-114">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="1e826-114">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="1e826-115">Aktion</span><span class="sxs-lookup"><span data-stu-id="1e826-115">Action</span></span>    | [<span data-ttu-id="1e826-116">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="1e826-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="1e826-117">J</span><span class="sxs-lookup"><span data-stu-id="1e826-117">Y</span></span>   | <span data-ttu-id="1e826-118">N</span><span class="sxs-lookup"><span data-stu-id="1e826-118">N</span></span>        |
| <span data-ttu-id="1e826-119">Bedingung</span><span class="sxs-lookup"><span data-stu-id="1e826-119">Condition</span></span> | [<span data-ttu-id="1e826-120">Condition</span><span class="sxs-lookup"><span data-stu-id="1e826-120">Condition</span></span>](condition.md)   | <span data-ttu-id="1e826-121">N</span><span class="sxs-lookup"><span data-stu-id="1e826-121">N</span></span>   | <span data-ttu-id="1e826-122">J</span><span class="sxs-lookup"><span data-stu-id="1e826-122">Y</span></span>        |
| <span data-ttu-id="1e826-123">Sequenz</span><span class="sxs-lookup"><span data-stu-id="1e826-123">Sequence</span></span>  | [<span data-ttu-id="1e826-124">Integer</span><span class="sxs-lookup"><span data-stu-id="1e826-124">Integer</span></span>](integer.md)       | <span data-ttu-id="1e826-125">N</span><span class="sxs-lookup"><span data-stu-id="1e826-125">N</span></span>   | <span data-ttu-id="1e826-126">J</span><span class="sxs-lookup"><span data-stu-id="1e826-126">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="1e826-127">Spalten</span><span class="sxs-lookup"><span data-stu-id="1e826-127">Columns</span></span>

<dl> <dt>

<span data-ttu-id="1e826-128"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Hinspiel</span><span class="sxs-lookup"><span data-stu-id="1e826-128"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="1e826-129">Der Name der auszuführenden Aktion.</span><span class="sxs-lookup"><span data-stu-id="1e826-129">Name of the action to execute.</span></span> <span data-ttu-id="1e826-130">Dabei handelt es sich entweder um eine Standardaktion oder eine benutzerdefinierte Aktion, die in der [Tabelle CustomAction](customaction-table.md)aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="1e826-130">This is either a standard action or a custom action listed in the [CustomAction table](customaction-table.md).</span></span>

<span data-ttu-id="1e826-131">Primärer Tabellenschlüssel.</span><span class="sxs-lookup"><span data-stu-id="1e826-131">Primary table key.</span></span>

</dd> <dt>

<span data-ttu-id="1e826-132"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Anlage</span><span class="sxs-lookup"><span data-stu-id="1e826-132"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="1e826-133">Logischer Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="1e826-133">Logical expression.</span></span> <span data-ttu-id="1e826-134">Wenn der Ausdruck zu false ausgewertet wird, wird die Aktion übersprungen.</span><span class="sxs-lookup"><span data-stu-id="1e826-134">If the expression evaluates to false, the action is skipped.</span></span> <span data-ttu-id="1e826-135">Wenn die Ausdruckssyntax ungültig ist, wird die Sequenz beendet und gibt iesbadaktiondata zurück.</span><span class="sxs-lookup"><span data-stu-id="1e826-135">If the expression syntax is invalid, the sequence terminates, returning iesBadActionData.</span></span> <span data-ttu-id="1e826-136">Weitere Informationen zur Syntax von Bedingungs Anweisungen finden Sie unter [Syntax für bedingte](conditional-statement-syntax.md)Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="1e826-136">For information on the syntax of conditional statements see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="1e826-137"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenz</span><span class="sxs-lookup"><span data-stu-id="1e826-137"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="1e826-138">Ein positiver Wert gibt die Sequenz Position der Aktion an.</span><span class="sxs-lookup"><span data-stu-id="1e826-138">A positive value indicates the sequence position of the action.</span></span> <span data-ttu-id="1e826-139">Die folgenden negativen Werte geben an, dass die Aktion aufgerufen wird, wenn das Installationsprogramm das terminierungsflag zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="1e826-139">The following negative values indicate that the action is called if the installer returns the termination flag.</span></span> <span data-ttu-id="1e826-140">Jedes terminierungsflag (negativer Wert) kann mit nur einer Aktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1e826-140">Each termination flag (negative value) can be used with no more than one action.</span></span> <span data-ttu-id="1e826-141">Mehrere Aktionen können über Beendigungs Flags verfügen, müssen jedoch unterschiedliche Flags aufweisen.</span><span class="sxs-lookup"><span data-stu-id="1e826-141">Multiple actions can have termination flags, but they must be different flags.</span></span> <span data-ttu-id="1e826-142">Beendigungs Flags (negative Werte) werden in der Regel in [Dialog Feldern](dialog-boxes.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="1e826-142">Termination flags (negative values) are typically used with [Dialog Boxes](dialog-boxes.md).</span></span>



| <span data-ttu-id="1e826-143">Beendigungs Flag</span><span class="sxs-lookup"><span data-stu-id="1e826-143">Termination flag</span></span>          | <span data-ttu-id="1e826-144">Wert</span><span class="sxs-lookup"><span data-stu-id="1e826-144">Value</span></span> | <span data-ttu-id="1e826-145">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1e826-145">Description</span></span>                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1e826-146">msidoaktionstatus-Erfolg</span><span class="sxs-lookup"><span data-stu-id="1e826-146">msiDoActionStatusSuccess</span></span>  | <span data-ttu-id="1e826-147">-1</span><span class="sxs-lookup"><span data-stu-id="1e826-147">-1</span></span>    | <span data-ttu-id="1e826-148">Erfolgreicher Abschluss.</span><span class="sxs-lookup"><span data-stu-id="1e826-148">Successful completion.</span></span> <span data-ttu-id="1e826-149">Wird mit den Dialogfeldern " [Beenden](exit-dialog.md) " verwendet.</span><span class="sxs-lookup"><span data-stu-id="1e826-149">Used with [Exit](exit-dialog.md) dialog boxes.</span></span>               |
| <span data-ttu-id="1e826-150">msidoaktionstatus ususerexit</span><span class="sxs-lookup"><span data-stu-id="1e826-150">msiDoActionStatusUserExit</span></span> | <span data-ttu-id="1e826-151">-2</span><span class="sxs-lookup"><span data-stu-id="1e826-151">-2</span></span>    | <span data-ttu-id="1e826-152">Der Benutzer beendet die Installation.</span><span class="sxs-lookup"><span data-stu-id="1e826-152">User terminates install.</span></span> <span data-ttu-id="1e826-153">Wird mit [Userexit](userexit-dialog.md) -Dialogfeldern verwendet.</span><span class="sxs-lookup"><span data-stu-id="1e826-153">Used with [UserExit](userexit-dialog.md) dialog boxes.</span></span>     |
| <span data-ttu-id="1e826-154">msidoaktionstatus-Fehler</span><span class="sxs-lookup"><span data-stu-id="1e826-154">msiDoActionStatusFailure</span></span>  | <span data-ttu-id="1e826-155">-3</span><span class="sxs-lookup"><span data-stu-id="1e826-155">-3</span></span>    | <span data-ttu-id="1e826-156">Schwerwiegender Exit wird beendet.</span><span class="sxs-lookup"><span data-stu-id="1e826-156">Fatal exit terminates.</span></span> <span data-ttu-id="1e826-157">Wird mit den Dialogfeldern " [FatalError](fatalerror-dialog.md) " verwendet.</span><span class="sxs-lookup"><span data-stu-id="1e826-157">Used with a [FatalError](fatalerror-dialog.md) dialog boxes.</span></span> |
| <span data-ttu-id="1e826-158">msidoaktionstatus-Suspend</span><span class="sxs-lookup"><span data-stu-id="1e826-158">msiDoActionStatusSuspend</span></span>  | <span data-ttu-id="1e826-159">–4</span><span class="sxs-lookup"><span data-stu-id="1e826-159">-4</span></span>    | <span data-ttu-id="1e826-160">Die Installation wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="1e826-160">Install is suspended.</span></span>                                                                |



 

<span data-ttu-id="1e826-161">NULL, alle anderen negativen Zahlen oder ein NULL-Wert geben an, dass die Aktion nie aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="1e826-161">Zero, all other negative numbers, or a null value indicate that the action is never called.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="1e826-162">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="1e826-162">Validation</span></span>

<dl>

[<span data-ttu-id="1e826-163">ICE03</span><span class="sxs-lookup"><span data-stu-id="1e826-163">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="1e826-164">ICE06</span><span class="sxs-lookup"><span data-stu-id="1e826-164">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="1e826-165">ICE12</span><span class="sxs-lookup"><span data-stu-id="1e826-165">ICE12</span></span>](ice12.md)  
[<span data-ttu-id="1e826-166">ICE13</span><span class="sxs-lookup"><span data-stu-id="1e826-166">ICE13</span></span>](ice13.md)  
[<span data-ttu-id="1e826-167">ICE26</span><span class="sxs-lookup"><span data-stu-id="1e826-167">ICE26</span></span>](ice26.md)  
[<span data-ttu-id="1e826-168">ICE27</span><span class="sxs-lookup"><span data-stu-id="1e826-168">ICE27</span></span>](ice27.md)  
[<span data-ttu-id="1e826-169">ICE28</span><span class="sxs-lookup"><span data-stu-id="1e826-169">ICE28</span></span>](ice28.md)  
[<span data-ttu-id="1e826-170">ICE75</span><span class="sxs-lookup"><span data-stu-id="1e826-170">ICE75</span></span>](ice75.md)  
[<span data-ttu-id="1e826-171">ICE77</span><span class="sxs-lookup"><span data-stu-id="1e826-171">ICE77</span></span>](ice77.md)  
[<span data-ttu-id="1e826-172">ICE79</span><span class="sxs-lookup"><span data-stu-id="1e826-172">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="1e826-173">ICE82</span><span class="sxs-lookup"><span data-stu-id="1e826-173">ICE82</span></span>](ice82.md)  
[<span data-ttu-id="1e826-174">ICE84</span><span class="sxs-lookup"><span data-stu-id="1e826-174">ICE84</span></span>](ice84.md)  
[<span data-ttu-id="1e826-175">ICE86</span><span class="sxs-lookup"><span data-stu-id="1e826-175">ICE86</span></span>](ice86.md)  
[<span data-ttu-id="1e826-176">ICEM04</span><span class="sxs-lookup"><span data-stu-id="1e826-176">ICEM04</span></span>](icem04.md)  
</dl>

 

 



