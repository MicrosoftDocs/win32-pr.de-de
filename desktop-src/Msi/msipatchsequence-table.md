---
description: Die msipatchsequence-Tabelle enthält alle Informationen, die das Installationsprogramm benötigt, um die Reihenfolge der Anwendung eines kleinen Update Patches relativ zu allen anderen Patches zu bestimmen.
ms.assetid: ae8319ad-8136-4201-9fcf-ea58ce05f88b
title: Msipatchsequence-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e63252b98156a5eac1ebdc5ed5d94c7a42ec93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352568"
---
# <a name="msipatchsequence-table"></a><span data-ttu-id="d2092-103">Msipatchsequence-Tabelle</span><span class="sxs-lookup"><span data-stu-id="d2092-103">MsiPatchSequence Table</span></span>

<span data-ttu-id="d2092-104">Die msipatchsequence-Tabelle enthält alle Informationen, die das Installationsprogramm benötigt, um die Reihenfolge der Anwendung eines [kleinen Update](small-updates.md) Patches relativ zu allen anderen Patches zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="d2092-104">The MsiPatchSequence table contains all the information the installer requires to determine the sequence of application of a [small update](small-updates.md) patch relative to all other patches.</span></span> <span data-ttu-id="d2092-105">Die Tabelle muss sich in der Datenbank der Patchdatei befinden und nicht in einer Transformation im Patch.</span><span class="sxs-lookup"><span data-stu-id="d2092-105">The table must be in the database of the patch file and not in a transform in the patch.</span></span> <span data-ttu-id="d2092-106">Das Installationsprogramm ignoriert diese Tabelle beim Anwenden eines [wichtigen Upgradepatches](major-upgrades.md) .</span><span class="sxs-lookup"><span data-stu-id="d2092-106">The installer ignores this table when applying a [major upgrade](major-upgrades.md) patch.</span></span> <span data-ttu-id="d2092-107">Beim Anwenden eines [geringfügigen Upgradepatches](minor-upgrades.md) verwendet das Installationsprogramm diese Tabelle nur, um ersetzte Patches zu identifizieren, die nicht sequenziert werden dürfen.</span><span class="sxs-lookup"><span data-stu-id="d2092-107">When applying a [minor upgrade](minor-upgrades.md) patch, the installer only uses this table to identify superseded patches that must not be sequenced.</span></span>

<span data-ttu-id="d2092-108">Die **msipatchsequence-Tabelle** weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="d2092-108">The **MsiPatchSequence table** has the following columns.</span></span>



| <span data-ttu-id="d2092-109">Spalte</span><span class="sxs-lookup"><span data-stu-id="d2092-109">Column</span></span>      | <span data-ttu-id="d2092-110">Typ</span><span class="sxs-lookup"><span data-stu-id="d2092-110">Type</span></span>                         | <span data-ttu-id="d2092-111">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="d2092-111">Key</span></span> | <span data-ttu-id="d2092-112">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="d2092-112">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="d2092-113">Patchfamilie</span><span class="sxs-lookup"><span data-stu-id="d2092-113">PatchFamily</span></span> | [<span data-ttu-id="d2092-114">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="d2092-114">Identifier</span></span>](identifier.md) | <span data-ttu-id="d2092-115">J</span><span class="sxs-lookup"><span data-stu-id="d2092-115">Y</span></span>   | <span data-ttu-id="d2092-116">N</span><span class="sxs-lookup"><span data-stu-id="d2092-116">N</span></span>        |
| <span data-ttu-id="d2092-117">ProductCode</span><span class="sxs-lookup"><span data-stu-id="d2092-117">ProductCode</span></span> | [<span data-ttu-id="d2092-118">GUID</span><span class="sxs-lookup"><span data-stu-id="d2092-118">GUID</span></span>](guid.md)             | <span data-ttu-id="d2092-119">J</span><span class="sxs-lookup"><span data-stu-id="d2092-119">Y</span></span>   | <span data-ttu-id="d2092-120">J</span><span class="sxs-lookup"><span data-stu-id="d2092-120">Y</span></span>        |
| <span data-ttu-id="d2092-121">Sequenz</span><span class="sxs-lookup"><span data-stu-id="d2092-121">Sequence</span></span>    | [<span data-ttu-id="d2092-122">Version</span><span class="sxs-lookup"><span data-stu-id="d2092-122">Version</span></span>](version.md)       | <span data-ttu-id="d2092-123">N</span><span class="sxs-lookup"><span data-stu-id="d2092-123">N</span></span>   | <span data-ttu-id="d2092-124">N</span><span class="sxs-lookup"><span data-stu-id="d2092-124">N</span></span>        |
| <span data-ttu-id="d2092-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="d2092-125">Attributes</span></span>  | [<span data-ttu-id="d2092-126">Integer</span><span class="sxs-lookup"><span data-stu-id="d2092-126">Integer</span></span>](integer.md)       | <span data-ttu-id="d2092-127">N</span><span class="sxs-lookup"><span data-stu-id="d2092-127">N</span></span>   | <span data-ttu-id="d2092-128">J</span><span class="sxs-lookup"><span data-stu-id="d2092-128">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="d2092-129">Spalten</span><span class="sxs-lookup"><span data-stu-id="d2092-129">Columns</span></span>

<dl> <dt>

<span data-ttu-id="d2092-130"><span id="PatchFamily"></span><span id="patchfamily"></span><span id="PATCHFAMILY"></span>Patchfamilie</span><span class="sxs-lookup"><span data-stu-id="d2092-130"><span id="PatchFamily"></span><span id="patchfamily"></span><span id="PATCHFAMILY"></span>PatchFamily</span></span>
</dt> <dd>

<span data-ttu-id="d2092-131">Gibt an, dass der Patch Mitglied der patchfamilie ist, die in diesem Feld benannt ist.</span><span class="sxs-lookup"><span data-stu-id="d2092-131">Specifies that the patch is a member of the patch family named in this field.</span></span> <span data-ttu-id="d2092-132">Patches in derselben patchfamilie, die auf dieselbe Produktversion abzielen, werden nach den Werten in der Sequence-Spalte sortiert.</span><span class="sxs-lookup"><span data-stu-id="d2092-132">Patches in the same patch family that target the same product version are sorted by the values in the Sequence column.</span></span> <span data-ttu-id="d2092-133">Die Patches innerhalb der patchfamilie werden in der Reihenfolge der zunehmenden Reihenfolge auf das Ziel Produkt angewendet.</span><span class="sxs-lookup"><span data-stu-id="d2092-133">The patches within the patch family are applied to the target product in the order of increasing sequence.</span></span> <span data-ttu-id="d2092-134">Die patchfamilie wird auch verwendet, um zu bestimmen, welche Patches ersetzt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d2092-134">The PatchFamily is also used to determine which patches are to be superseded.</span></span> <span data-ttu-id="d2092-135">Ein Patch kann in mehreren Zeilen aufgelistet werden und zu mehreren patchfamilien gehören, wenn er für mehr als ein Produkt gilt oder mehrere Korrekturen umfasst.</span><span class="sxs-lookup"><span data-stu-id="d2092-135">A patch may be listed in multiple rows and belong to multiple patch families if it applies to more than one product or includes multiple fixes.</span></span>

<span data-ttu-id="d2092-136">Der-Windows Installer interpretiert den Wert der patchfamilie nicht auf andere Weise als Vergleiche mit anderen patchfamilienwerten.</span><span class="sxs-lookup"><span data-stu-id="d2092-136">The Windows Installer does not interpret the PatchFamily value in any way other than comparisons for equality against other PatchFamily values.</span></span> <span data-ttu-id="d2092-137">Ein patchfamilienwert muss innerhalb von ProductCode eindeutig sein, der auf den Satz von Patches abzielt.</span><span class="sxs-lookup"><span data-stu-id="d2092-137">A PatchFamily value must be unique within the ProductCode targeted by the set of patches.</span></span> <span data-ttu-id="d2092-138">In den komplexen patchszenarien muss der Patch-Familien Bezeichner möglicherweise global eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="d2092-138">In the complex patching scenarios the PatchFamily identifier may need to be globally unique.</span></span>

</dd> <dt>

<span data-ttu-id="d2092-139"><span id="ProductCode"></span><span id="productcode"></span><span id="PRODUCTCODE"></span>ProductCode</span><span class="sxs-lookup"><span data-stu-id="d2092-139"><span id="ProductCode"></span><span id="productcode"></span><span id="PRODUCTCODE"></span>ProductCode</span></span>
</dt> <dd>

<span data-ttu-id="d2092-140">Ein Wert in diesem Feld ist optional.</span><span class="sxs-lookup"><span data-stu-id="d2092-140">A value in this field is optional.</span></span> <span data-ttu-id="d2092-141">Wenn ein [Produktcode](product-codes.md) -GUID in dieses Feld eingegeben wird und der Patch auf das angegebene Produkt angewendet wird, wird der Patch sortiert und als Mitglied der angegebenen patchfamilie angewendet.</span><span class="sxs-lookup"><span data-stu-id="d2092-141">If a [product code](product-codes.md) GUID is entered in this field and the patch is being applied to the specified product, the patch is sorted and applied as a member of the specified PatchFamily.</span></span> <span data-ttu-id="d2092-142">Wenn ein Produktcode-GUID in dieses Feld eingegeben wird und der Patch nicht auf das von ProductCode angegebene Produkt angewendet wird, wird diese Zeile ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d2092-142">If a product code GUID is entered in this field and the patch is not being applied to the product specified by ProductCode, this row is ignored.</span></span> <span data-ttu-id="d2092-143">Wenn der Wert in ProductCode NULL ist, wird der Patch sortiert und als Mitglied der patchfamily für alle Ziele des Patches unabhängig vom Produktcode angewendet.</span><span class="sxs-lookup"><span data-stu-id="d2092-143">If the value in ProductCode is NULL, the patch is sorted and applied as a member of PatchFamily for all targets of the patch regardless of the product code.</span></span>

<span data-ttu-id="d2092-144">Ein Patch kann mehrere Zeilen in derselben patchfamilie und einen anderen ProductCode für jedes Produkt enthalten, das auf den Patch ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="d2092-144">A patch can have multiple rows in the same PatchFamily and a different ProductCode for each product targeted by the patch.</span></span> <span data-ttu-id="d2092-145">Eine Zeile für die patchfamilie kann NULL für ProductCode angeben.</span><span class="sxs-lookup"><span data-stu-id="d2092-145">One row for the PatchFamily can specify NULL for ProductCode.</span></span> <span data-ttu-id="d2092-146">Wenn das Ziel Produkt einer Zeile mit einem ProductCode ungleich Null entspricht, verwendet das Installationsprogramm die übereinstimmende Zeile und ignoriert die Zeile mit dem NULL-ProductCode.</span><span class="sxs-lookup"><span data-stu-id="d2092-146">If the target product matches a row with a non-NULL ProductCode, the installer uses the matching row and ignores the row with the NULL ProductCode.</span></span> <span data-ttu-id="d2092-147">Wenn keiner der angegebenen Produktcodes mit dem Ziel identisch ist, wird der Patch entsprechend des Produktcodes sortiert und als Mitglied der patchfamily für alle Ziele des Patches angewendet.</span><span class="sxs-lookup"><span data-stu-id="d2092-147">If none of the specified product codes match the target, the patch is sorted and applied as a member of PatchFamily for all targets of the patch regardless of the product code.</span></span>

</dd> <dt>

<span data-ttu-id="d2092-148"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenz</span><span class="sxs-lookup"><span data-stu-id="d2092-148"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="d2092-149">Der Wert in der Sequenz Spalte gibt die Sequenz dieses Patches in der angegebenen patchfamilie an.</span><span class="sxs-lookup"><span data-stu-id="d2092-149">The value in the Sequence column specifies the sequence of this patch within the specified PatchFamily.</span></span> <span data-ttu-id="d2092-150">Der Wert in der Sequenz wird im Format der [Versions](version.md) Daten ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="d2092-150">The value in Sequence is expressed in the format of [Version](version.md) data.</span></span> <span data-ttu-id="d2092-151">Der Wert enthält zwischen 1 und 4 Felder, und jedes Feld hat einen Bereich von 0 bis 65535.</span><span class="sxs-lookup"><span data-stu-id="d2092-151">The value contains between 1 and 4 fields and each field has a range of 0 to 65535.</span></span> <span data-ttu-id="d2092-152">Member von patchfamily werden sortiert und auf das Ziel Produkt in der Reihenfolge der Vergrößerung von Sequenz Werten angewendet.</span><span class="sxs-lookup"><span data-stu-id="d2092-152">Members of PatchFamily are sorted and applied to the target product in the order of increasing Sequence values.</span></span> <span data-ttu-id="d2092-153">Beispielsweise werden die folgenden sechs Werte vergrößert: 1, 1,1, 1,2, 2,01, 2.01.1, 2.01.1.1.</span><span class="sxs-lookup"><span data-stu-id="d2092-153">For example, the following six values are increasing: 1, 1.1, 1.2, 2.01, 2.01.1, 2.01.1.1.</span></span>

</dd> <dt>

<span data-ttu-id="d2092-154"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Legt</span><span class="sxs-lookup"><span data-stu-id="d2092-154"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>
</dt> <dd>

<span data-ttu-id="d2092-155">Das vorhanden sein des **msidbpatchsequencesupersedefrühere** -Attributs in einer Zeile gibt an, dass der Patch für [kleine](small-updates.md) Updates die von allen Patches bereitgestellten Updates mit geringeren Sequenz Werten in derselben patchfamilie ablöst.</span><span class="sxs-lookup"><span data-stu-id="d2092-155">The presence of the **msidbPatchSequenceSupersedeEarlier** attribute in a row indicates that the [small update](small-updates.md) patch supersedes the updates provided by all patches with lesser Sequence values in the same PatchFamily.</span></span> <span data-ttu-id="d2092-156">Dieser Patch enthält alle Fixes, die von früheren Patches in der angegebenen patchfamilie bereitgestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="d2092-156">This patch contains all fixes provided by earlier patches in the specified PatchFamily.</span></span> <span data-ttu-id="d2092-157">Dieses Attribut bedeutet nicht, dass dieser Patch die früheren Patches in allen Fällen ablöst, weil die früheren Patches mehreren patchfamilien angehören können.</span><span class="sxs-lookup"><span data-stu-id="d2092-157">This attribute does not mean that this patch supersedes the earlier patches in all cases because the earlier patches can belong to multiple patch families.</span></span>

<span data-ttu-id="d2092-158">Ein [kleiner Update](small-updates.md) Patch kann unter keinen Umständen ein [geringfügiges Upgrade](minor-upgrades.md) oder ein [wichtiges Upgradepatch](major-upgrades.md) ersetzen, auch wenn **msidbpatchsequencesupersedefrüher** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d2092-158">A [small update](small-updates.md) patch cannot supersede a [minor upgrade](minor-upgrades.md) or [major upgrade](major-upgrades.md) patch under any circumstances, even if the **msidbPatchSequenceSupersedeEarlier** is set.</span></span> 

| <span data-ttu-id="d2092-159">Name</span><span class="sxs-lookup"><span data-stu-id="d2092-159">Name</span></span>                                   | <span data-ttu-id="d2092-160">Wert</span><span class="sxs-lookup"><span data-stu-id="d2092-160">Value</span></span> | <span data-ttu-id="d2092-161">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d2092-161">Meaning</span></span>                                                           |
|----------------------------------------|-------|-------------------------------------------------------------------|
|                                        | <span data-ttu-id="d2092-162">0x00</span><span class="sxs-lookup"><span data-stu-id="d2092-162">0x00</span></span>  | <span data-ttu-id="d2092-163">Gibt einen einfachen Sequenzierungs Wert an.</span><span class="sxs-lookup"><span data-stu-id="d2092-163">Indicates a simple sequencing value.</span></span>                              |
| <span data-ttu-id="d2092-164">**msidbpatchsequencesupersede früher**</span><span class="sxs-lookup"><span data-stu-id="d2092-164">**msidbPatchSequenceSupersedeEarlier**</span></span> | <span data-ttu-id="d2092-165">0x01</span><span class="sxs-lookup"><span data-stu-id="d2092-165">0x01</span></span>  | <span data-ttu-id="d2092-166">Gibt einen Patch an, durch den frühere Patches in dieser Familie abgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="d2092-166">Indicates a patch that supersedes earlier patches in this family.</span></span> |



 

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="d2092-167">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="d2092-167">Validation</span></span>

<dl>

[<span data-ttu-id="d2092-168">ICE03</span><span class="sxs-lookup"><span data-stu-id="d2092-168">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="d2092-169">ICE06</span><span class="sxs-lookup"><span data-stu-id="d2092-169">ICE06</span></span>](ice06.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="d2092-170">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d2092-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2092-171">Wird in Windows Installer 2,0 und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d2092-171">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



