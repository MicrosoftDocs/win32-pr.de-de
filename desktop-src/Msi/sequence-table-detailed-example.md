---
description: Im folgenden finden Sie ein Beispiel für eine Sequenz Tabelle.
ms.assetid: 25b3667a-1478-48c4-9c41-4defd25a0103
title: Beispiel für eine detaillierte Sequenz Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4698d5270f2f246fe6e676799ea239e47a950c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352766"
---
# <a name="sequence-table-detailed-example"></a><span data-ttu-id="f0125-103">Beispiel für eine detaillierte Sequenz Tabelle</span><span class="sxs-lookup"><span data-stu-id="f0125-103">Sequence Table Detailed Example</span></span>

<span data-ttu-id="f0125-104">Im folgenden finden Sie ein Beispiel für eine Sequenz Tabelle.</span><span class="sxs-lookup"><span data-stu-id="f0125-104">Here is an example of a sequence table.</span></span>



| <span data-ttu-id="f0125-105">Aktion</span><span class="sxs-lookup"><span data-stu-id="f0125-105">Action</span></span>                                          | <span data-ttu-id="f0125-106">Bedingung</span><span class="sxs-lookup"><span data-stu-id="f0125-106">Condition</span></span>                                                       | <span data-ttu-id="f0125-107">Sequenz</span><span class="sxs-lookup"><span data-stu-id="f0125-107">Sequence</span></span> |
|-------------------------------------------------|-----------------------------------------------------------------|----------|
| [<span data-ttu-id="f0125-108">LaunchConditions</span><span class="sxs-lookup"><span data-stu-id="f0125-108">LaunchConditions</span></span>](launchconditions-action.md) |                                                                 |          |
| [<span data-ttu-id="f0125-109">AppSearch</span><span class="sxs-lookup"><span data-stu-id="f0125-109">AppSearch</span></span>](appsearch-action.md)               |                                                                 | <span data-ttu-id="f0125-110">200</span><span class="sxs-lookup"><span data-stu-id="f0125-110">200</span></span>      |
| [<span data-ttu-id="f0125-111">Ccpsearch</span><span class="sxs-lookup"><span data-stu-id="f0125-111">CCPSearch</span></span>](ccpsearch-action.md)               | <span data-ttu-id="f0125-112">CCP- \_ Test</span><span class="sxs-lookup"><span data-stu-id="f0125-112">CCP\_TEST</span></span>                                                       | <span data-ttu-id="f0125-113">300</span><span class="sxs-lookup"><span data-stu-id="f0125-113">300</span></span>      |
| <span data-ttu-id="f0125-114">Ccpdialog</span><span class="sxs-lookup"><span data-stu-id="f0125-114">CCPDialog</span></span>                                       | <span data-ttu-id="f0125-115">kein \_ CCP- \_ Erfolg</span><span class="sxs-lookup"><span data-stu-id="f0125-115">NOT\_CCP\_SUCCESS</span></span>                                               | <span data-ttu-id="f0125-116">400</span><span class="sxs-lookup"><span data-stu-id="f0125-116">400</span></span>      |
| <span data-ttu-id="f0125-117">Mycustomconfig</span><span class="sxs-lookup"><span data-stu-id="f0125-117">MyCustomConfig</span></span>                                  | <span data-ttu-id="f0125-118">Nicht [ **installiert**](installed.md)</span><span class="sxs-lookup"><span data-stu-id="f0125-118">NOT [**Installed**](installed.md)</span></span>                              | <span data-ttu-id="f0125-119">500</span><span class="sxs-lookup"><span data-stu-id="f0125-119">500</span></span>      |
| [<span data-ttu-id="f0125-120">Costinitialize</span><span class="sxs-lookup"><span data-stu-id="f0125-120">CostInitialize</span></span>](costinitialize-action.md)     |                                                                 | <span data-ttu-id="f0125-121">600</span><span class="sxs-lookup"><span data-stu-id="f0125-121">600</span></span>      |
| [<span data-ttu-id="f0125-122">Datei Kosten</span><span class="sxs-lookup"><span data-stu-id="f0125-122">FileCost</span></span>](filecost-action.md)                 |                                                                 | <span data-ttu-id="f0125-123">700</span><span class="sxs-lookup"><span data-stu-id="f0125-123">700</span></span>      |
| [<span data-ttu-id="f0125-124">Costfinalize</span><span class="sxs-lookup"><span data-stu-id="f0125-124">CostFinalize</span></span>](costfinalize-action.md)         |                                                                 | <span data-ttu-id="f0125-125">800</span><span class="sxs-lookup"><span data-stu-id="f0125-125">800</span></span>      |
| <span data-ttu-id="f0125-126">Installdialog</span><span class="sxs-lookup"><span data-stu-id="f0125-126">InstallDialog</span></span>                                   | <span data-ttu-id="f0125-127">Nicht [ **installiert**](installed.md)</span><span class="sxs-lookup"><span data-stu-id="f0125-127">NOT [**Installed**](installed.md)</span></span>                              | <span data-ttu-id="f0125-128">900</span><span class="sxs-lookup"><span data-stu-id="f0125-128">900</span></span>      |
| <span data-ttu-id="f0125-129">Maintenancedialog</span><span class="sxs-lookup"><span data-stu-id="f0125-129">MaintenanceDialog</span></span>                               | <span data-ttu-id="f0125-130">[**Installiert**](installed.md) Und nicht [  fortsetzen](resume.md)</span><span class="sxs-lookup"><span data-stu-id="f0125-130">[**Installed**](installed.md) AND NOT [**Resume**](resume.md)</span></span> | <span data-ttu-id="f0125-131">1000</span><span class="sxs-lookup"><span data-stu-id="f0125-131">1000</span></span>     |
| <span data-ttu-id="f0125-132">Aktions Dialogfeld</span><span class="sxs-lookup"><span data-stu-id="f0125-132">ActionDialog</span></span>                                    |                                                                 | <span data-ttu-id="f0125-133">1100</span><span class="sxs-lookup"><span data-stu-id="f0125-133">1100</span></span>     |
| [<span data-ttu-id="f0125-134">Register Product</span><span class="sxs-lookup"><span data-stu-id="f0125-134">RegisterProduct</span></span>](registerproduct-action.md)   |                                                                 | <span data-ttu-id="f0125-135">1200</span><span class="sxs-lookup"><span data-stu-id="f0125-135">1200</span></span>     |
| [<span data-ttu-id="f0125-136">InstallValidate</span><span class="sxs-lookup"><span data-stu-id="f0125-136">InstallValidate</span></span>](installvalidate-action.md)   |                                                                 | <span data-ttu-id="f0125-137">1300</span><span class="sxs-lookup"><span data-stu-id="f0125-137">1300</span></span>     |
| [<span data-ttu-id="f0125-138">InstallFiles</span><span class="sxs-lookup"><span data-stu-id="f0125-138">InstallFiles</span></span>](installfiles-action.md)         |                                                                 | <span data-ttu-id="f0125-139">1400</span><span class="sxs-lookup"><span data-stu-id="f0125-139">1400</span></span>     |
| <span data-ttu-id="f0125-140">MyCustomAction</span><span class="sxs-lookup"><span data-stu-id="f0125-140">MyCustomAction</span></span>                                  | <span data-ttu-id="f0125-141">$MyComponent > 2</span><span class="sxs-lookup"><span data-stu-id="f0125-141">$MyComponent > 2</span></span>                                             | <span data-ttu-id="f0125-142">1500</span><span class="sxs-lookup"><span data-stu-id="f0125-142">1500</span></span>     |
| [<span data-ttu-id="f0125-143">InstallFinalize wurde</span><span class="sxs-lookup"><span data-stu-id="f0125-143">InstallFinalize</span></span>](installfinalize-action.md)   |                                                                 | <span data-ttu-id="f0125-144">1600</span><span class="sxs-lookup"><span data-stu-id="f0125-144">1600</span></span>     |



 

<span data-ttu-id="f0125-145">Die folgenden Aktionen in dieser Sequenz Tabelle werden vom Installer definiert und sind Beispiele für Standard Aktionen:</span><span class="sxs-lookup"><span data-stu-id="f0125-145">The following actions in this sequence table are defined by the installer and are examples of standard actions:</span></span>

[<span data-ttu-id="f0125-146">LaunchConditions</span><span class="sxs-lookup"><span data-stu-id="f0125-146">LaunchConditions</span></span>](launchconditions-action.md)

 

[<span data-ttu-id="f0125-147">AppSearch</span><span class="sxs-lookup"><span data-stu-id="f0125-147">AppSearch</span></span>](appsearch-action.md)

 

[<span data-ttu-id="f0125-148">Ccpsearch</span><span class="sxs-lookup"><span data-stu-id="f0125-148">CCPSearch</span></span>](ccpsearch-action.md)

 

[<span data-ttu-id="f0125-149">Costinitialize</span><span class="sxs-lookup"><span data-stu-id="f0125-149">CostInitialize</span></span>](costinitialize-action.md)

 

[<span data-ttu-id="f0125-150">Datei Kosten</span><span class="sxs-lookup"><span data-stu-id="f0125-150">FileCost</span></span>](filecost-action.md)

 

[<span data-ttu-id="f0125-151">Costfinalize</span><span class="sxs-lookup"><span data-stu-id="f0125-151">CostFinalize</span></span>](costfinalize-action.md)

 

[<span data-ttu-id="f0125-152">Register Product</span><span class="sxs-lookup"><span data-stu-id="f0125-152">RegisterProduct</span></span>](registerproduct-action.md)

 

[<span data-ttu-id="f0125-153">InstallFiles</span><span class="sxs-lookup"><span data-stu-id="f0125-153">InstallFiles</span></span>](installfiles-action.md)

 

[<span data-ttu-id="f0125-154">InstallFiles</span><span class="sxs-lookup"><span data-stu-id="f0125-154">InstallFiles</span></span>](installfiles-action.md)

 

[<span data-ttu-id="f0125-155">InstallValidate</span><span class="sxs-lookup"><span data-stu-id="f0125-155">InstallValidate</span></span>](installvalidate-action.md)

<span data-ttu-id="f0125-156">Die folgenden Aktionen wurden vom Autor der Tabelle definiert und sind Beispiele für [benutzerdefinierte Aktionen](custom-actions.md) . Sie müssen in der [Tabelle CustomAction](customaction-table.md)aufgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="f0125-156">The following actions were defined by the table's author and are examples of [custom actions](custom-actions.md) and must be listed in the [CustomAction table](customaction-table.md):</span></span>

<span data-ttu-id="f0125-157">Mycustomconfig</span><span class="sxs-lookup"><span data-stu-id="f0125-157">MyCustomConfig</span></span>

 

<span data-ttu-id="f0125-158">MyCustomAction</span><span class="sxs-lookup"><span data-stu-id="f0125-158">MyCustomAction</span></span>

<span data-ttu-id="f0125-159">Die verbleibenden Einträge im Feld "Aktion" sind Fremdschlüssel in der [Dialog Tabelle](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="f0125-159">The remaining entries in the Action field are foreign keys into the [Dialog table](dialog-table.md).</span></span> <span data-ttu-id="f0125-160">Sie geben die Namen von Dialogfeldern an, die angezeigt werden, wenn das Bedingungs Feld als true ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="f0125-160">They specify the names of dialog boxes that will displayed if the condition field evaluates to True.</span></span>

<span data-ttu-id="f0125-161">Ccpdialog</span><span class="sxs-lookup"><span data-stu-id="f0125-161">CCPDialog</span></span>

 

<span data-ttu-id="f0125-162">Installdialog</span><span class="sxs-lookup"><span data-stu-id="f0125-162">InstallDialog</span></span>

 

<span data-ttu-id="f0125-163">Maintenancedialog</span><span class="sxs-lookup"><span data-stu-id="f0125-163">MaintenanceDialog</span></span>

 

<span data-ttu-id="f0125-164">Aktions Dialogfeld</span><span class="sxs-lookup"><span data-stu-id="f0125-164">ActionDialog</span></span>

<span data-ttu-id="f0125-165">Die Spalte Bedingung bewirkt, dass die Aktion vom Installer übersprungen wird, wenn die Eigenschaft oder der Ausdruck in diesem Feld den Wert false hat.</span><span class="sxs-lookup"><span data-stu-id="f0125-165">The Condition column causes the installer to skip the action if the property or expression in this field is False.</span></span> <span data-ttu-id="f0125-166">Die [**installierte**](installed.md) Eigenschaft und die [**Resume**](resume.md) -Eigenschaft sind Beispiele für Eigenschaften, die vom Installationsprogramm festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f0125-166">The [**Installed**](installed.md) property and the [**RESUME**](resume.md) property are example of properties that are set by the installer.</span></span> <span data-ttu-id="f0125-167">Die [**installierte**](installed.md) Eigenschaft ist auf true festgelegt, wenn das Produkt bereits installiert ist, und die Eigenschaft [**wieder aufnehmen**](resume.md) festgelegt wird, wenn eine angehaltene Installation fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="f0125-167">The [**Installed**](installed.md) property is set to true if the product is already installed and the [**RESUME**](resume.md) property is set if resuming a suspended installation.</span></span> <span data-ttu-id="f0125-168">Die Eigenschaften "CCP \_ -Test" und "Not \_ CCP \_ Success" sind Beispiele für Eigenschaften, die von dem Benutzer, der die Anwendung installiert, an der Befehlszeile festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="f0125-168">The CCP\_TEST and the NOT\_CCP\_SUCCESS properties are examples of properties that can be set at the command line by the user installing the application.</span></span>

<span data-ttu-id="f0125-169">Alle Aktionen werden nacheinander mit den folgenden Bedingungs Schritten ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="f0125-169">All actions run in sequence with the following conditional steps:</span></span>

-   <span data-ttu-id="f0125-170">Die cppsearch wird nur ausgeführt, wenn der CCP- \_ Test festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f0125-170">The CPPSearch is run only if CCP\_TEST is set.</span></span>
-   <span data-ttu-id="f0125-171">Ccpdialog wird nur ausgeführt, wenn kein \_ CCP- \_ Erfolg festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="f0125-171">CCPDialog is run only if NOT\_CCP\_SUCCESS is set.</span></span>
-   <span data-ttu-id="f0125-172">Maintenancedialog wird nur ausgeführt, wenn dieses Produkt bereits installiert ist, und wenn es sich nicht um eine Installation handelt, die nach dem aussetzen fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="f0125-172">MaintenanceDialog is run only if this product is already installed and if this is not an installation that is being resume after being suspended.</span></span>
-   <span data-ttu-id="f0125-173">"MyCustomAction" wird nur ausgeführt, wenn der Ausdruck in der Spalte Bedingung "true" ist.</span><span class="sxs-lookup"><span data-stu-id="f0125-173">MyCustomAction is run only if the expression in the Condition column is True.</span></span> <span data-ttu-id="f0125-174">Der Ausdruck $MyComponent > 2 bezieht sich auf den Aktionszustand der Komponente namens MyComponent.</span><span class="sxs-lookup"><span data-stu-id="f0125-174">The expression $MyComponent > 2 refers to the action state of the component called MyComponent.</span></span> <span data-ttu-id="f0125-175">Diese Bedingung gibt an, dass "MyCustomAction" nur ausgeführt werden soll, wenn "MyComponent" als installiert festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f0125-175">This condition indicates that MyCustomAction should only be run if MyComponent is set to be installed.</span></span> <span data-ttu-id="f0125-176">Weitere Informationen zu Aktions Zuständen und Auswahl Zuständen finden Sie unter der [**featurerequeststate**](session-featurerequeststate.md) -Eigenschaft, der [Feature-Tabelle](feature-table.md)und der [InstallFiles-Aktion](installfiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="f0125-176">For more information on Action states and Selection states, see the [**FeatureRequestState**](session-featurerequeststate.md) property, the [Feature table](feature-table.md), and the [InstallFiles action](installfiles-action.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0125-177">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f0125-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0125-178">Verwenden von Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f0125-178">Using Properties</span></span>](using-properties.md)
</dt> <dt>

[<span data-ttu-id="f0125-179">Syntax der bedingten Anweisung</span><span class="sxs-lookup"><span data-stu-id="f0125-179">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
</dt> </dl>

 

 



