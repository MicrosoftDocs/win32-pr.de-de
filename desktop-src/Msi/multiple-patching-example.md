---
description: Das folgende Beispiel zeigt, wie Sie mit Windows Installer 3,0 und höher Patches in der Reihenfolge anwenden können, in der Sie erstellt wurden.
ms.assetid: 98771652-cec2-4371-8132-a741cf8431fb
title: Beispiel für das mehrfache Patchen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2d10274531ac4906ef61a49caee9ccbcde98bbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357498"
---
# <a name="multiple-patching-example"></a><span data-ttu-id="33af1-103">Beispiel für das mehrfache Patchen</span><span class="sxs-lookup"><span data-stu-id="33af1-103">Multiple Patching Example</span></span>

<span data-ttu-id="33af1-104">Das folgende Beispiel zeigt, wie Sie mit Windows Installer 3,0 und höher Patches in der Reihenfolge anwenden können, in der Sie erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="33af1-104">The following example shows how Windows Installer 3.0 and later can be used to apply patches in the order in which they are authored.</span></span>

## <a name="example"></a><span data-ttu-id="33af1-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="33af1-105">Example</span></span>

<span data-ttu-id="33af1-106">In diesem Beispiel gibt es drei Patches: QFE1, QFE2 und ServicePack1, und Sie verfügen jeweils über eine [msipatchsequence](msipatchsequence-table.md) -Tabelle.</span><span class="sxs-lookup"><span data-stu-id="33af1-106">In this example there are three patches, QFE1, QFE2, and ServicePack1, and they each have a [MsiPatchSequence](msipatchsequence-table.md) table.</span></span> <span data-ttu-id="33af1-107">Diese Patches wurden so verfasst, dass Sie auf Version 1,0 der Anwendung angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="33af1-107">These patches have been authored to be applied to version 1.0 of the application.</span></span>



| <span data-ttu-id="33af1-108">Patchname</span><span class="sxs-lookup"><span data-stu-id="33af1-108">Patch Name</span></span>   | <span data-ttu-id="33af1-109">Patchetyp</span><span class="sxs-lookup"><span data-stu-id="33af1-109">Patch Type</span></span>    | <span data-ttu-id="33af1-110">Sequenznummer</span><span class="sxs-lookup"><span data-stu-id="33af1-110">Sequence Number</span></span> |
|--------------|---------------|-----------------|
| <span data-ttu-id="33af1-111">QFE1</span><span class="sxs-lookup"><span data-stu-id="33af1-111">QFE1</span></span>         | <span data-ttu-id="33af1-112">Kleines Update</span><span class="sxs-lookup"><span data-stu-id="33af1-112">Small Update</span></span>  | <span data-ttu-id="33af1-113">1.1.0</span><span class="sxs-lookup"><span data-stu-id="33af1-113">1.1.0</span></span>           |
| <span data-ttu-id="33af1-114">QFE2</span><span class="sxs-lookup"><span data-stu-id="33af1-114">QFE2</span></span>         | <span data-ttu-id="33af1-115">Kleines Update</span><span class="sxs-lookup"><span data-stu-id="33af1-115">Small Update</span></span>  | <span data-ttu-id="33af1-116">1.2.0</span><span class="sxs-lookup"><span data-stu-id="33af1-116">1.2.0</span></span>           |
| <span data-ttu-id="33af1-117">ServicePack1</span><span class="sxs-lookup"><span data-stu-id="33af1-117">ServicePack1</span></span> | <span data-ttu-id="33af1-118">Geringfügige Aktualisierung</span><span class="sxs-lookup"><span data-stu-id="33af1-118">Minor Upgrade</span></span> | <span data-ttu-id="33af1-119">1.3.0</span><span class="sxs-lookup"><span data-stu-id="33af1-119">1.3.0</span></span>           |



 

<span data-ttu-id="33af1-120">Die [msipatchsequence](msipatchsequence-table.md) -Tabelle jedes Patches weist nur einen Datensatz auf, der die patchfamilie, den Produktcode und die Sequenznummer enthält.</span><span class="sxs-lookup"><span data-stu-id="33af1-120">The [MsiPatchSequence](msipatchsequence-table.md) table of each patch has only one record that contains the patch family, product code, and sequence number.</span></span> <span data-ttu-id="33af1-121">Die drei Patches werden alle auf das gleiche Produkt angewendet und gehören derselben patchfamilie mit dem Namen "AppPatch" an.</span><span class="sxs-lookup"><span data-stu-id="33af1-121">The three patches are all applied to the same product and belong to the same patch family, named AppPatch.</span></span> <span data-ttu-id="33af1-122">Keines der Patches hat das **msidbpatchsequencesupersedebug** -Attribut.</span><span class="sxs-lookup"><span data-stu-id="33af1-122">None of the patches have the **msidbPatchSequenceSupersedeEarlier** attribute.</span></span>

<span data-ttu-id="33af1-123">[Msipatchsequence-Tabelle](msipatchsequence-table.md) für das QFE1 [Small Update](small-updates.md).</span><span class="sxs-lookup"><span data-stu-id="33af1-123">[MsiPatchSequence Table](msipatchsequence-table.md) for the QFE1 [small update](small-updates.md).</span></span> 

| <span data-ttu-id="33af1-124">Patchfamilie</span><span class="sxs-lookup"><span data-stu-id="33af1-124">PatchFamily</span></span> | <span data-ttu-id="33af1-125">ProductCode</span><span class="sxs-lookup"><span data-stu-id="33af1-125">ProductCode</span></span>                            | <span data-ttu-id="33af1-126">Sequenz</span><span class="sxs-lookup"><span data-stu-id="33af1-126">Sequence</span></span> | <span data-ttu-id="33af1-127">Attribute</span><span class="sxs-lookup"><span data-stu-id="33af1-127">Attributes</span></span> |
|-------------|----------------------------------------|----------|------------|
| <span data-ttu-id="33af1-128">AppPatch</span><span class="sxs-lookup"><span data-stu-id="33af1-128">AppPatch</span></span>    | <span data-ttu-id="33af1-129">{18a9233c-0b34-4127-a966-c257386270bc}</span><span class="sxs-lookup"><span data-stu-id="33af1-129">{18A9233C-0B34-4127-A966-C257386270BC}</span></span> | <span data-ttu-id="33af1-130">1.1.0</span><span class="sxs-lookup"><span data-stu-id="33af1-130">1.1.0</span></span>    |            |



 

<span data-ttu-id="33af1-131">[Msipatchsequence-Tabelle](msipatchsequence-table.md) für das QFE2 [Small Update](small-updates.md).</span><span class="sxs-lookup"><span data-stu-id="33af1-131">[MsiPatchSequence Table](msipatchsequence-table.md) for the QFE2 [small update](small-updates.md).</span></span> 

| <span data-ttu-id="33af1-132">Patchfamilie</span><span class="sxs-lookup"><span data-stu-id="33af1-132">PatchFamily</span></span> | <span data-ttu-id="33af1-133">ProductCode</span><span class="sxs-lookup"><span data-stu-id="33af1-133">ProductCode</span></span>                            | <span data-ttu-id="33af1-134">Sequenz</span><span class="sxs-lookup"><span data-stu-id="33af1-134">Sequence</span></span> | <span data-ttu-id="33af1-135">Attribute</span><span class="sxs-lookup"><span data-stu-id="33af1-135">Attributes</span></span> |
|-------------|----------------------------------------|----------|------------|
| <span data-ttu-id="33af1-136">AppPatch</span><span class="sxs-lookup"><span data-stu-id="33af1-136">AppPatch</span></span>    | <span data-ttu-id="33af1-137">{18a9233c-0b34-4127-a966-c257386270bc}</span><span class="sxs-lookup"><span data-stu-id="33af1-137">{18A9233C-0B34-4127-A966-C257386270BC}</span></span> | <span data-ttu-id="33af1-138">1.2.0</span><span class="sxs-lookup"><span data-stu-id="33af1-138">1.2.0</span></span>    |            |



 

<span data-ttu-id="33af1-139">[Msipatchsequence-Tabelle](msipatchsequence-table.md) für ServicePack1 [Minor Upgrade](minor-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="33af1-139">[MsiPatchSequence Table](msipatchsequence-table.md) for ServicePack1 [minor upgrade](minor-upgrades.md).</span></span> 

| <span data-ttu-id="33af1-140">Patchfamilie</span><span class="sxs-lookup"><span data-stu-id="33af1-140">PatchFamily</span></span> | <span data-ttu-id="33af1-141">ProductCode</span><span class="sxs-lookup"><span data-stu-id="33af1-141">ProductCode</span></span>                            | <span data-ttu-id="33af1-142">Sequenz</span><span class="sxs-lookup"><span data-stu-id="33af1-142">Sequence</span></span> | <span data-ttu-id="33af1-143">Attribute</span><span class="sxs-lookup"><span data-stu-id="33af1-143">Attributes</span></span> |
|-------------|----------------------------------------|----------|------------|
| <span data-ttu-id="33af1-144">AppPatch</span><span class="sxs-lookup"><span data-stu-id="33af1-144">AppPatch</span></span>    | <span data-ttu-id="33af1-145">{18a9233c-0b34-4127-a966-c257386270bc}</span><span class="sxs-lookup"><span data-stu-id="33af1-145">{18A9233C-0B34-4127-A966-C257386270BC}</span></span> | <span data-ttu-id="33af1-146">1.3.0</span><span class="sxs-lookup"><span data-stu-id="33af1-146">1.3.0</span></span>    |            |



 

<span data-ttu-id="33af1-147">Wenn ein Benutzerversion 1,0 des Produkts installiert und dann QFE2 anwendet und dann zu einem späteren Zeitpunkt QFE1 anwendet, stellt Windows Installer sicher, dass die effektive Sequenz der Patchanwendung für das Produkt QFE1 vor QFE2 angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="33af1-147">If a user installs version 1.0 of the product, and then applies QFE2, and then at a later date decides to apply QFE1, Windows Installer ensures that the effective sequence of patch application to the product is QFE1 applied ahead of QFE2.</span></span> <span data-ttu-id="33af1-148">Wenn der Benutzer ServicePack1 anwendet, wendet QFE2 und QFE1 zu einem späteren Zeitpunkt an. Windows Installer stellt sicher, dass die effektive Sequenz der Patchanwendung für das Produkt QFE1 vor QFE2 und vor ServicePack1 liegt.</span><span class="sxs-lookup"><span data-stu-id="33af1-148">If the user applies ServicePack1, then applies QFE2 and QFE1 together at a later date, Windows Installer ensures that the effective sequence of patch application to the product is QFE1 ahead of QFE2 and ahead of ServicePack1.</span></span>

<span data-ttu-id="33af1-149">Wenn in ServicePack1 **msidbpatchsequencesupersedefrüher** in der Attribute-Spalte der [msipatchsequence](msipatchsequence-table.md) -Tabelle festgelegt ist, bedeutet dies, dass die Service Pack alle Änderungen in QFE1 und QFE2 enthält.</span><span class="sxs-lookup"><span data-stu-id="33af1-149">If ServicePack1 has **msidbPatchSequenceSupersedeEarlier** set in the Attributes column of its [MsiPatchSequence](msipatchsequence-table.md) table, this means that the service pack contains all the changes in QFE1 and QFE2.</span></span> <span data-ttu-id="33af1-150">In diesem Fall werden QFE1 und QFE2 nicht angewendet, wenn ServicePack1 angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="33af1-150">In this case, QFE1 and QFE2 are not applied when ServicePack1 is applied.</span></span>

<span data-ttu-id="33af1-151">**Windows Installer 2,0:** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="33af1-151">**Windows Installer 2.0:** Not supported.</span></span> <span data-ttu-id="33af1-152">Frühere Versionen als Windows Installer 3,0 können nur einen Patch pro Transaktion installieren, und Patches werden in der Reihenfolge angewendet, in der Sie bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="33af1-152">Versions earlier than Windows Installer 3.0 can install only one patch per transaction and patches are applied in the sequence that they are provided.</span></span> <span data-ttu-id="33af1-153">Wenn QFE2 im vorherigen Beispiel zuerst angewendet und dann QFE1 angewendet wird, werden zwei Transaktionen und die Patches auf Version 1,0 der Anwendung in der Sequenz QFE2 gefolgt von QFE1 angewendet.</span><span class="sxs-lookup"><span data-stu-id="33af1-153">For the preceding example, if QFE2 is applied first and then QFE1 is applied, that is two transactions and the patches are applied to version 1.0 of the application in the sequence QFE2 followed by QFE1.</span></span> <span data-ttu-id="33af1-154">Wenn ServicePack1 zuerst angewendet wird, kann QFE1 oder QFE2 nicht in einer späteren Transaktion angewendet werden, da ServicePack1 ein kleineres Upgrade ist, bei dem die Anwendungs Version geändert wird.</span><span class="sxs-lookup"><span data-stu-id="33af1-154">If ServicePack1 is applied first, then QFE1 or QFE2 cannot be applied in a later transaction because ServicePack1 is a minor upgrade that changes the application version.</span></span> <span data-ttu-id="33af1-155">QFE1 und QFE2 können nur auf Version 1,0 der Anwendung angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="33af1-155">QFE1 and QFE2 can only be applied to version 1.0 of the application.</span></span>

 

 



