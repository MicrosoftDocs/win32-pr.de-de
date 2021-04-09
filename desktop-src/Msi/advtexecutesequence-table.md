---
description: Die AdvtExecuteSequence-Tabelle listet Aktionen auf, die das Installationsprogramm aufruft, wenn die Ankündigungs Aktion der obersten Ebene ausgeführt wird.
ms.assetid: 8873c161-a709-48b8-a66f-fe2ee9be859f
title: AdvtExecuteSequence-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b68a3f69cc7473b2364f169545743941d752f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864504"
---
# <a name="advtexecutesequence-table"></a><span data-ttu-id="67b8d-103">AdvtExecuteSequence-Tabelle</span><span class="sxs-lookup"><span data-stu-id="67b8d-103">AdvtExecuteSequence Table</span></span>

<span data-ttu-id="67b8d-104">Die AdvtExecuteSequence-Tabelle listet Aktionen auf, die das Installationsprogramm aufruft, wenn die Ankündigungs [Aktion](advertise-action.md) der obersten Ebene ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="67b8d-104">The AdvtExecuteSequence table lists actions the installer calls when the top-level [ADVERTISE action](advertise-action.md) is executed.</span></span>

<span data-ttu-id="67b8d-105">In der AdvtExecuteSequence-Tabelle können nur die folgenden Aktionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="67b8d-105">Only the following actions can be used in the AdvtExecuteSequence table.</span></span> <span data-ttu-id="67b8d-106">Benutzerdefinierte Aktionen können in dieser Tabelle nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="67b8d-106">Custom actions cannot be used in this table.</span></span>

[<span data-ttu-id="67b8d-107">Costfinalize</span><span class="sxs-lookup"><span data-stu-id="67b8d-107">CostFinalize</span></span>](costfinalize-action.md)

[<span data-ttu-id="67b8d-108">Costinitialize</span><span class="sxs-lookup"><span data-stu-id="67b8d-108">CostInitialize</span></span>](costinitialize-action.md)

[<span data-ttu-id="67b8d-109">"Kreateshortcuts"</span><span class="sxs-lookup"><span data-stu-id="67b8d-109">CreateShortcuts</span></span>](createshortcuts-action.md)

[<span data-ttu-id="67b8d-110">InstallFinalize wurde</span><span class="sxs-lookup"><span data-stu-id="67b8d-110">InstallFinalize</span></span>](installfinalize-action.md)

[<span data-ttu-id="67b8d-111">Installinitialisieren</span><span class="sxs-lookup"><span data-stu-id="67b8d-111">InstallInitialize</span></span>](installinitialize-action.md)

[<span data-ttu-id="67b8d-112">InstallValidate</span><span class="sxs-lookup"><span data-stu-id="67b8d-112">InstallValidate</span></span>](installvalidate-action.md)

[<span data-ttu-id="67b8d-113">Msipublishassemblys</span><span class="sxs-lookup"><span data-stu-id="67b8d-113">MsiPublishAssemblies</span></span>](msipublishassemblies-action.md)

[<span data-ttu-id="67b8d-114">PublishComponents</span><span class="sxs-lookup"><span data-stu-id="67b8d-114">PublishComponents</span></span>](publishcomponents-action.md)

[<span data-ttu-id="67b8d-115">Publishfeatures</span><span class="sxs-lookup"><span data-stu-id="67b8d-115">PublishFeatures</span></span>](publishfeatures-action.md)

[<span data-ttu-id="67b8d-116">Publishproduct</span><span class="sxs-lookup"><span data-stu-id="67b8d-116">PublishProduct</span></span>](publishproduct-action.md)

[<span data-ttu-id="67b8d-117">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="67b8d-117">RegisterClassInfo</span></span>](registerclassinfo-action.md)

[<span data-ttu-id="67b8d-118">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="67b8d-118">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)

[<span data-ttu-id="67b8d-119">Registermimeinfo</span><span class="sxs-lookup"><span data-stu-id="67b8d-119">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

[<span data-ttu-id="67b8d-120">Registerprogidinfo</span><span class="sxs-lookup"><span data-stu-id="67b8d-120">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)

<span data-ttu-id="67b8d-121">Die Spalten sind identisch mit denen der [InstallExecuteSequence-Tabelle](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="67b8d-121">The columns are identical to those of the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="67b8d-122">Die AdvtExecuteSequence-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="67b8d-122">The AdvtExecuteSequence table has the following columns.</span></span>



| <span data-ttu-id="67b8d-123">Spalte</span><span class="sxs-lookup"><span data-stu-id="67b8d-123">Column</span></span>    | <span data-ttu-id="67b8d-124">Typ</span><span class="sxs-lookup"><span data-stu-id="67b8d-124">Type</span></span>                         | <span data-ttu-id="67b8d-125">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="67b8d-125">Key</span></span> | <span data-ttu-id="67b8d-126">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="67b8d-126">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="67b8d-127">Aktion</span><span class="sxs-lookup"><span data-stu-id="67b8d-127">Action</span></span>    | [<span data-ttu-id="67b8d-128">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="67b8d-128">Identifier</span></span>](identifier.md) | <span data-ttu-id="67b8d-129">J</span><span class="sxs-lookup"><span data-stu-id="67b8d-129">Y</span></span>   | <span data-ttu-id="67b8d-130">N</span><span class="sxs-lookup"><span data-stu-id="67b8d-130">N</span></span>        |
| <span data-ttu-id="67b8d-131">Bedingung</span><span class="sxs-lookup"><span data-stu-id="67b8d-131">Condition</span></span> | [<span data-ttu-id="67b8d-132">Condition</span><span class="sxs-lookup"><span data-stu-id="67b8d-132">Condition</span></span>](condition.md)   | <span data-ttu-id="67b8d-133">N</span><span class="sxs-lookup"><span data-stu-id="67b8d-133">N</span></span>   | <span data-ttu-id="67b8d-134">J</span><span class="sxs-lookup"><span data-stu-id="67b8d-134">Y</span></span>        |
| <span data-ttu-id="67b8d-135">Sequenz</span><span class="sxs-lookup"><span data-stu-id="67b8d-135">Sequence</span></span>  | [<span data-ttu-id="67b8d-136">Integer</span><span class="sxs-lookup"><span data-stu-id="67b8d-136">Integer</span></span>](integer.md)       | <span data-ttu-id="67b8d-137">N</span><span class="sxs-lookup"><span data-stu-id="67b8d-137">N</span></span>   | <span data-ttu-id="67b8d-138">J</span><span class="sxs-lookup"><span data-stu-id="67b8d-138">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="67b8d-139">Spalten</span><span class="sxs-lookup"><span data-stu-id="67b8d-139">Columns</span></span>

<dl> <dt>

<span data-ttu-id="67b8d-140"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Hinspiel</span><span class="sxs-lookup"><span data-stu-id="67b8d-140"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="67b8d-141">Der Name der [Standardaktion](standard-actions.md) , die vom Installationsprogramm ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="67b8d-141">Name of the [standard action](standard-actions.md) the installer is to execute.</span></span> <span data-ttu-id="67b8d-142">Dies ist der Primärschlüssel der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="67b8d-142">This is the primary key of the table.</span></span>

</dd> <dt>

<span data-ttu-id="67b8d-143"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Anlage</span><span class="sxs-lookup"><span data-stu-id="67b8d-143"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="67b8d-144">Logischer Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="67b8d-144">Logical expression.</span></span> <span data-ttu-id="67b8d-145">Wenn der Ausdruck zu false ausgewertet wird, wird die Aktion übersprungen.</span><span class="sxs-lookup"><span data-stu-id="67b8d-145">If the expression evaluates to false, the action is skipped.</span></span> <span data-ttu-id="67b8d-146">Wenn die Ausdruckssyntax ungültig ist, wird die Sequenz beendet und gibt iesbadaktiondata zurück.</span><span class="sxs-lookup"><span data-stu-id="67b8d-146">If the expression syntax is invalid, the sequence terminates, returning iesBadActionData.</span></span> <span data-ttu-id="67b8d-147">Weitere Informationen zur Syntax von Bedingungs Anweisungen finden Sie unter [Syntax für bedingte](conditional-statement-syntax.md)Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="67b8d-147">For information on the syntax of conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="67b8d-148"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenz</span><span class="sxs-lookup"><span data-stu-id="67b8d-148"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="67b8d-149">Ein positiver Wert gibt die Sequenz Position der Aktion an.</span><span class="sxs-lookup"><span data-stu-id="67b8d-149">A positive value indicates the sequence position of the action.</span></span> <span data-ttu-id="67b8d-150">Die folgenden negativen Werte geben an, dass die Aktion aufgerufen wird, wenn das Installationsprogramm das terminierungsflag zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="67b8d-150">The following negative values indicate that the action is called if the installer returns the termination flag.</span></span> <span data-ttu-id="67b8d-151">Jedes terminierungsflag (negativer Wert) kann mit nur einer Aktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="67b8d-151">Each termination flag (negative value) can be used with no more than one action.</span></span> <span data-ttu-id="67b8d-152">Mehrere Aktionen können über Beendigungs Flags verfügen, müssen jedoch unterschiedliche Flags aufweisen.</span><span class="sxs-lookup"><span data-stu-id="67b8d-152">Multiple actions can have termination flags, but they must be different flags.</span></span> <span data-ttu-id="67b8d-153">Beendigungs Flags (negative Werte) werden in der Regel in [Dialog Feldern](dialog-boxes.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="67b8d-153">Termination flags (negative values) are typically used with [Dialog Boxes](dialog-boxes.md).</span></span>



| <span data-ttu-id="67b8d-154">Beendigungs Flag</span><span class="sxs-lookup"><span data-stu-id="67b8d-154">Termination flag</span></span>          | <span data-ttu-id="67b8d-155">Wert</span><span class="sxs-lookup"><span data-stu-id="67b8d-155">Value</span></span> | <span data-ttu-id="67b8d-156">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="67b8d-156">Description</span></span>                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="67b8d-157">msidoaktionstatus-Erfolg</span><span class="sxs-lookup"><span data-stu-id="67b8d-157">msiDoActionStatusSuccess</span></span>  | <span data-ttu-id="67b8d-158">-1</span><span class="sxs-lookup"><span data-stu-id="67b8d-158">-1</span></span>    | <span data-ttu-id="67b8d-159">Erfolgreicher Abschluss.</span><span class="sxs-lookup"><span data-stu-id="67b8d-159">Successful completion.</span></span> <span data-ttu-id="67b8d-160">Wird mit den Dialogfeldern " [Beenden](exit-dialog.md) " verwendet.</span><span class="sxs-lookup"><span data-stu-id="67b8d-160">Used with [Exit](exit-dialog.md) dialog boxes.</span></span>               |
| <span data-ttu-id="67b8d-161">msidoaktionstatus ususerexit</span><span class="sxs-lookup"><span data-stu-id="67b8d-161">msiDoActionStatusUserExit</span></span> | <span data-ttu-id="67b8d-162">-2</span><span class="sxs-lookup"><span data-stu-id="67b8d-162">-2</span></span>    | <span data-ttu-id="67b8d-163">Der Benutzer beendet die Installation.</span><span class="sxs-lookup"><span data-stu-id="67b8d-163">User terminates install.</span></span> <span data-ttu-id="67b8d-164">Wird mit [Userexit](userexit-dialog.md) -Dialogfeldern verwendet.</span><span class="sxs-lookup"><span data-stu-id="67b8d-164">Used with [UserExit](userexit-dialog.md) dialog boxes.</span></span>     |
| <span data-ttu-id="67b8d-165">msidoaktionstatus-Fehler</span><span class="sxs-lookup"><span data-stu-id="67b8d-165">msiDoActionStatusFailure</span></span>  | <span data-ttu-id="67b8d-166">-3</span><span class="sxs-lookup"><span data-stu-id="67b8d-166">-3</span></span>    | <span data-ttu-id="67b8d-167">Schwerwiegender Exit wird beendet.</span><span class="sxs-lookup"><span data-stu-id="67b8d-167">Fatal exit terminates.</span></span> <span data-ttu-id="67b8d-168">Wird mit den Dialogfeldern " [FatalError](fatalerror-dialog.md) " verwendet.</span><span class="sxs-lookup"><span data-stu-id="67b8d-168">Used with a [FatalError](fatalerror-dialog.md) dialog boxes.</span></span> |
| <span data-ttu-id="67b8d-169">msidoaktionstatus-Suspend</span><span class="sxs-lookup"><span data-stu-id="67b8d-169">msiDoActionStatusSuspend</span></span>  | <span data-ttu-id="67b8d-170">–4</span><span class="sxs-lookup"><span data-stu-id="67b8d-170">-4</span></span>    | <span data-ttu-id="67b8d-171">Die Installation wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="67b8d-171">Install is suspended.</span></span>                                                                |



 

<span data-ttu-id="67b8d-172">NULL, alle anderen negativen Zahlen oder ein NULL-Wert geben an, dass die Aktion nie aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="67b8d-172">Zero, all other negative numbers, or a null value indicate that the action is never called.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="67b8d-173">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="67b8d-173">Validation</span></span>

<dl>

[<span data-ttu-id="67b8d-174">ICE03</span><span class="sxs-lookup"><span data-stu-id="67b8d-174">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="67b8d-175">ICE06</span><span class="sxs-lookup"><span data-stu-id="67b8d-175">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="67b8d-176">ICE12</span><span class="sxs-lookup"><span data-stu-id="67b8d-176">ICE12</span></span>](ice12.md)  
[<span data-ttu-id="67b8d-177">ICE13</span><span class="sxs-lookup"><span data-stu-id="67b8d-177">ICE13</span></span>](ice13.md)  
[<span data-ttu-id="67b8d-178">ICE27</span><span class="sxs-lookup"><span data-stu-id="67b8d-178">ICE27</span></span>](ice27.md)  
[<span data-ttu-id="67b8d-179">ICE46</span><span class="sxs-lookup"><span data-stu-id="67b8d-179">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="67b8d-180">ICE72</span><span class="sxs-lookup"><span data-stu-id="67b8d-180">ICE72</span></span>](ice72.md)  
[<span data-ttu-id="67b8d-181">ICE79</span><span class="sxs-lookup"><span data-stu-id="67b8d-181">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="67b8d-182">ICE82</span><span class="sxs-lookup"><span data-stu-id="67b8d-182">ICE82</span></span>](ice82.md)  
[<span data-ttu-id="67b8d-183">ICE83</span><span class="sxs-lookup"><span data-stu-id="67b8d-183">ICE83</span></span>](ice83.md)  
[<span data-ttu-id="67b8d-184">ICE84</span><span class="sxs-lookup"><span data-stu-id="67b8d-184">ICE84</span></span>](ice84.md)  
[<span data-ttu-id="67b8d-185">ICE86</span><span class="sxs-lookup"><span data-stu-id="67b8d-185">ICE86</span></span>](ice86.md)  
[<span data-ttu-id="67b8d-186">ICEM04</span><span class="sxs-lookup"><span data-stu-id="67b8d-186">ICEM04</span></span>](icem04.md)  
</dl>

 

 



