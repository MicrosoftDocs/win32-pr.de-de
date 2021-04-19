---
description: Ein Merge-Tool wertet die moduleadvtexecutesequence-Tabelle aus und fügt dann die berechneten Aktionen in die AdvtExecuteSequence-Tabelle mit einer korrekten Sequenznummer ein.
ms.assetid: ed2d1159-da78-4dc5-98a2-2cc876380c43
title: Moduleadvtexecutesequence-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 699e544df7e0a92b0fee92c753e36a8b9a86ee5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362636"
---
# <a name="moduleadvtexecutesequence-table"></a><span data-ttu-id="23a77-103">Moduleadvtexecutesequence-Tabelle</span><span class="sxs-lookup"><span data-stu-id="23a77-103">ModuleAdvtExecuteSequence Table</span></span>

<span data-ttu-id="23a77-104">Ein Merge-Tool wertet die moduleadvtexecutesequence-Tabelle aus und fügt dann die berechneten Aktionen in die [AdvtExecuteSequence-Tabelle](advtexecutesequence-table.md) mit einer korrekten Sequenznummer ein.</span><span class="sxs-lookup"><span data-stu-id="23a77-104">A merge tool evaluates the ModuleAdvtExecuteSequence table and then inserts the calculated actions into the [AdvtExecuteSequence table](advtexecutesequence-table.md) with a correct sequence number.</span></span>

<span data-ttu-id="23a77-105">Die moduleadvtexecutesequence-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="23a77-105">The ModuleAdvtExecuteSequence table has the following columns.</span></span>



| <span data-ttu-id="23a77-106">Spalte</span><span class="sxs-lookup"><span data-stu-id="23a77-106">Column</span></span>     | <span data-ttu-id="23a77-107">Typ</span><span class="sxs-lookup"><span data-stu-id="23a77-107">Type</span></span>                         | <span data-ttu-id="23a77-108">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="23a77-108">Key</span></span> | <span data-ttu-id="23a77-109">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="23a77-109">Nullable</span></span> |
|------------|------------------------------|-----|----------|
| <span data-ttu-id="23a77-110">Aktion</span><span class="sxs-lookup"><span data-stu-id="23a77-110">Action</span></span>     | [<span data-ttu-id="23a77-111">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="23a77-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="23a77-112">J</span><span class="sxs-lookup"><span data-stu-id="23a77-112">Y</span></span>   | <span data-ttu-id="23a77-113">N</span><span class="sxs-lookup"><span data-stu-id="23a77-113">N</span></span>        |
| <span data-ttu-id="23a77-114">Sequenz</span><span class="sxs-lookup"><span data-stu-id="23a77-114">Sequence</span></span>   | [<span data-ttu-id="23a77-115">Integer</span><span class="sxs-lookup"><span data-stu-id="23a77-115">Integer</span></span>](integer.md)       |     | <span data-ttu-id="23a77-116">J</span><span class="sxs-lookup"><span data-stu-id="23a77-116">Y</span></span>        |
| <span data-ttu-id="23a77-117">Baseaction</span><span class="sxs-lookup"><span data-stu-id="23a77-117">BaseAction</span></span> | [<span data-ttu-id="23a77-118">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="23a77-118">Identifier</span></span>](identifier.md) |     | <span data-ttu-id="23a77-119">J</span><span class="sxs-lookup"><span data-stu-id="23a77-119">Y</span></span>        |
| <span data-ttu-id="23a77-120">Nach</span><span class="sxs-lookup"><span data-stu-id="23a77-120">After</span></span>      | [<span data-ttu-id="23a77-121">Integer</span><span class="sxs-lookup"><span data-stu-id="23a77-121">Integer</span></span>](integer.md)       |     | <span data-ttu-id="23a77-122">J</span><span class="sxs-lookup"><span data-stu-id="23a77-122">Y</span></span>        |
| <span data-ttu-id="23a77-123">Bedingung</span><span class="sxs-lookup"><span data-stu-id="23a77-123">Condition</span></span>  | [<span data-ttu-id="23a77-124">Condition</span><span class="sxs-lookup"><span data-stu-id="23a77-124">Condition</span></span>](condition.md)   |     | <span data-ttu-id="23a77-125">J</span><span class="sxs-lookup"><span data-stu-id="23a77-125">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="23a77-126">Spalten</span><span class="sxs-lookup"><span data-stu-id="23a77-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="23a77-127"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Hinspiel</span><span class="sxs-lookup"><span data-stu-id="23a77-127"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="23a77-128">Aktion, die in die Sequenz eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="23a77-128">Action to insert into sequence.</span></span> <span data-ttu-id="23a77-129">Bezieht sich auf eine der [Standard Aktionen](standard-actions.md)des-Installers oder einen Eintrag in der [CustomAction-Tabelle](customaction-table.md) oder- [Dialog Tabelle](dialog-table.md)des Merge-Moduls.</span><span class="sxs-lookup"><span data-stu-id="23a77-129">Refers to one of the installer [standard actions](standard-actions.md), or an entry in the merge module's [CustomAction table](customaction-table.md) or [Dialog table](dialog-table.md).</span></span>

<span data-ttu-id="23a77-130">Wenn eine [Standardaktion](standard-actions.md) in der Aktionsspalte einer mergemodulsequenz-Tabelle verwendet wird, müssen die baseaction-und After-Spalten dieses Datensatzes Null sein.</span><span class="sxs-lookup"><span data-stu-id="23a77-130">If a [standard action](standard-actions.md) is used in the Action column of a merge module sequence table, the BaseAction and After columns of that record must be Null.</span></span>

</dd> <dt>

<span data-ttu-id="23a77-131"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenz</span><span class="sxs-lookup"><span data-stu-id="23a77-131"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="23a77-132">Die Sequenznummer einer Standardaktion.</span><span class="sxs-lookup"><span data-stu-id="23a77-132">The sequence number of a standard action.</span></span> <span data-ttu-id="23a77-133">Wenn eine benutzerdefinierte Aktion oder ein benutzerdefiniertes Dialogfeld in die Aktionsspalte dieser Zeile eingegeben wird, muss dieses Feld auf NULL festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="23a77-133">If a custom action or dialog is entered into the Action column of this row, this field must be set to Null.</span></span>

<span data-ttu-id="23a77-134">Bei Verwendung von [Standard Aktionen](standard-actions.md) in Mergemodul-Sequenz Tabellen sollte der Wert in der Sequence-Spalte die empfohlene Aktions Sequenznummer sein.</span><span class="sxs-lookup"><span data-stu-id="23a77-134">When using [standard actions](standard-actions.md) in merge module sequence tables, the value in the Sequence column should be the recommended action sequence number.</span></span> <span data-ttu-id="23a77-135">Wenn sich die Sequenznummer im Mergemodul von der Sequenznummer für die gleiche Aktion in der MSI-Datei Sequenz Tabelle unterscheidet, verwendet das Mergetool die Sequenznummer aus der MSI-Datei.</span><span class="sxs-lookup"><span data-stu-id="23a77-135">If the sequence number in the merge module differs from that for the same action in the .msi file sequence table, the merge tool uses the sequence number from the .msi file.</span></span> <span data-ttu-id="23a77-136">Informationen zu den empfohlenen Sequenznummern von Standard Aktionen finden [Sie unter Verwenden einer Sequenz Tabelle](using-a-sequence-table.md) für vorgeschlagene Sequenzen.</span><span class="sxs-lookup"><span data-stu-id="23a77-136">See the suggested sequences in [Using a Sequence Table](using-a-sequence-table.md) for the recommended sequence numbers of standard actions.</span></span>

</dd> <dt>

<span data-ttu-id="23a77-137"><span id="BaseAction"></span><span id="baseaction"></span><span id="BASEACTION"></span>Baseaction</span><span class="sxs-lookup"><span data-stu-id="23a77-137"><span id="BaseAction"></span><span id="baseaction"></span><span id="BASEACTION"></span>BaseAction</span></span>
</dt> <dd>

<span data-ttu-id="23a77-138">Die baseaction-Spalte kann eine Standardaktion, eine benutzerdefinierte Aktion, die in der benutzerdefinierten Aktionstabelle des Merge-Moduls angegeben ist, oder ein Dialogfeld enthalten, das in der Dialog Tabelle des Moduls angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="23a77-138">The BaseAction column can contain a standard action, a custom action specified in the merge module's custom action table, or a dialog specified in the module's dialog table.</span></span> <span data-ttu-id="23a77-139">Die baseaction-Spalte ist ein Schlüssel in der Aktionsspalte dieser Tabelle.</span><span class="sxs-lookup"><span data-stu-id="23a77-139">The BaseAction column is a key into the Action column of this table.</span></span> <span data-ttu-id="23a77-140">Dabei kann es sich nicht um einen Fremdschlüssel in einer anderen MERGE-Tabelle oder-Tabelle in der MSI-Datei handeln.</span><span class="sxs-lookup"><span data-stu-id="23a77-140">It cannot be a foreign key into another merge table or table in the .msi file.</span></span> <span data-ttu-id="23a77-141">Dies bedeutet, dass jede Standardaktion, benutzerdefinierte Aktion oder ein Dialogfeld, das in der Spalte baseaction aufgeführt ist, auch in der Aktionsspalte eines anderen Datensatzes in dieser Tabelle aufgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="23a77-141">This means that every standard action, custom action, or dialog listed in the BaseAction column must also be listed in the Action column of another record in this table.</span></span>

</dd> <dt>

<span data-ttu-id="23a77-142"><span id="After"></span><span id="after"></span><span id="AFTER"></span>Nachdem</span><span class="sxs-lookup"><span data-stu-id="23a77-142"><span id="After"></span><span id="after"></span><span id="AFTER"></span>After</span></span>
</dt> <dd>

<span data-ttu-id="23a77-143">Boolescher Wert, der ist, ob Action vor oder nach baseaction steht.</span><span class="sxs-lookup"><span data-stu-id="23a77-143">Boolean for whether Action comes before or after BaseAction.</span></span>



| <span data-ttu-id="23a77-144">Wert</span><span class="sxs-lookup"><span data-stu-id="23a77-144">Value</span></span> | <span data-ttu-id="23a77-145">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="23a77-145">Meaning</span></span>                          |
|-------|----------------------------------|
| <span data-ttu-id="23a77-146">0</span><span class="sxs-lookup"><span data-stu-id="23a77-146">0</span></span>     | <span data-ttu-id="23a77-147">Aktion, die vor baseaction erfolgen soll</span><span class="sxs-lookup"><span data-stu-id="23a77-147">Action to come before BaseAction</span></span> |
| <span data-ttu-id="23a77-148">1</span><span class="sxs-lookup"><span data-stu-id="23a77-148">1</span></span>     | <span data-ttu-id="23a77-149">Aktion, die nach baseaction erfolgen soll</span><span class="sxs-lookup"><span data-stu-id="23a77-149">Action to come after BaseAction</span></span>  |



 

</dd> <dt>

<span data-ttu-id="23a77-150"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Anlage</span><span class="sxs-lookup"><span data-stu-id="23a77-150"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="23a77-151">Eine Bedingungs Anweisung, die angibt, ob die Aktion ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="23a77-151">A conditional statement that indicates if the action is be executed.</span></span> <span data-ttu-id="23a77-152">NULL wird als true ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="23a77-152">Null evaluates to true.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="23a77-153">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="23a77-153">Remarks</span></span>

<span data-ttu-id="23a77-154">Wenn diese Tabelle vorhanden ist, muss auch die [AdvtExecuteSequence-Tabelle](advtexecutesequence-table.md) im Mergemodul vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="23a77-154">If this table is present the [AdvtExecuteSequence table](advtexecutesequence-table.md) must also be present in the merge module.</span></span>

 

 



