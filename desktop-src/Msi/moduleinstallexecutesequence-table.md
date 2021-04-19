---
description: Ein Merge-Tool wertet die moduleinstallexecutesequence-Tabelle aus und fügt dann die berechneten Aktionen in die InstallExecuteSequence-Tabelle mit einer korrekten Sequenznummer ein.
ms.assetid: 6cd04d9a-5489-4fde-951e-aa962e9bd755
title: Moduleinstallexecutesequence-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d294ddfdf06028bf18d518e1086d37a0719f8c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366285"
---
# <a name="moduleinstallexecutesequence-table"></a><span data-ttu-id="0f51a-103">Moduleinstallexecutesequence-Tabelle</span><span class="sxs-lookup"><span data-stu-id="0f51a-103">ModuleInstallExecuteSequence Table</span></span>

<span data-ttu-id="0f51a-104">Ein Merge-Tool wertet die moduleinstallexecutesequence-Tabelle aus und fügt dann die berechneten Aktionen in die [InstallExecuteSequence-Tabelle](installexecutesequence-table.md) mit einer korrekten Sequenznummer ein.</span><span class="sxs-lookup"><span data-stu-id="0f51a-104">A merge tool evaluates the ModuleInstallExecuteSequence table and then inserts the calculated actions into the [InstallExecuteSequence table](installexecutesequence-table.md) with a correct sequence number.</span></span>

<span data-ttu-id="0f51a-105">Die moduleinstallexecutesequence-Tabelle enthält die folgenden Spalten.</span><span class="sxs-lookup"><span data-stu-id="0f51a-105">The ModuleInstallExecuteSequence table contains the following columns.</span></span>



| <span data-ttu-id="0f51a-106">Spalte</span><span class="sxs-lookup"><span data-stu-id="0f51a-106">Column</span></span>     | <span data-ttu-id="0f51a-107">Typ</span><span class="sxs-lookup"><span data-stu-id="0f51a-107">Type</span></span>                         | <span data-ttu-id="0f51a-108">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="0f51a-108">Key</span></span> | <span data-ttu-id="0f51a-109">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="0f51a-109">Nullable</span></span> |
|------------|------------------------------|-----|----------|
| <span data-ttu-id="0f51a-110">Aktion</span><span class="sxs-lookup"><span data-stu-id="0f51a-110">Action</span></span>     | [<span data-ttu-id="0f51a-111">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="0f51a-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="0f51a-112">J</span><span class="sxs-lookup"><span data-stu-id="0f51a-112">Y</span></span>   | <span data-ttu-id="0f51a-113">N</span><span class="sxs-lookup"><span data-stu-id="0f51a-113">N</span></span>        |
| <span data-ttu-id="0f51a-114">Sequenz</span><span class="sxs-lookup"><span data-stu-id="0f51a-114">Sequence</span></span>   | [<span data-ttu-id="0f51a-115">Integer</span><span class="sxs-lookup"><span data-stu-id="0f51a-115">Integer</span></span>](integer.md)       |     | <span data-ttu-id="0f51a-116">J</span><span class="sxs-lookup"><span data-stu-id="0f51a-116">Y</span></span>        |
| <span data-ttu-id="0f51a-117">Baseaction</span><span class="sxs-lookup"><span data-stu-id="0f51a-117">BaseAction</span></span> | [<span data-ttu-id="0f51a-118">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="0f51a-118">Identifier</span></span>](identifier.md) |     | <span data-ttu-id="0f51a-119">J</span><span class="sxs-lookup"><span data-stu-id="0f51a-119">Y</span></span>        |
| <span data-ttu-id="0f51a-120">Nach</span><span class="sxs-lookup"><span data-stu-id="0f51a-120">After</span></span>      | [<span data-ttu-id="0f51a-121">Integer</span><span class="sxs-lookup"><span data-stu-id="0f51a-121">Integer</span></span>](integer.md)       |     | <span data-ttu-id="0f51a-122">J</span><span class="sxs-lookup"><span data-stu-id="0f51a-122">Y</span></span>        |
| <span data-ttu-id="0f51a-123">Bedingung</span><span class="sxs-lookup"><span data-stu-id="0f51a-123">Condition</span></span>  | [<span data-ttu-id="0f51a-124">Condition</span><span class="sxs-lookup"><span data-stu-id="0f51a-124">Condition</span></span>](condition.md)   |     | <span data-ttu-id="0f51a-125">J</span><span class="sxs-lookup"><span data-stu-id="0f51a-125">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="0f51a-126">Spalten</span><span class="sxs-lookup"><span data-stu-id="0f51a-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="0f51a-127"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Hinspiel</span><span class="sxs-lookup"><span data-stu-id="0f51a-127"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="0f51a-128">Aktion, die in die Sequenz eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0f51a-128">Action to insert into sequence.</span></span> <span data-ttu-id="0f51a-129">Bezieht sich auf eine der [Standard Aktionen](standard-actions.md)des-Installers oder einen Eintrag in der [CustomAction-Tabelle](customaction-table.md)des Merge-Moduls oder in der [Dialog Feld Tabelle](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="0f51a-129">Refers to one of the installer [standard actions](standard-actions.md), or an entry in the merge module's [CustomAction table](customaction-table.md), or [Dialog table](dialog-table.md).</span></span>

<span data-ttu-id="0f51a-130">Wenn eine [Standardaktion](standard-actions.md) in der Aktionsspalte einer mergemodulsequenz-Tabelle verwendet wird, müssen die baseaction-und After-Spalten dieses Datensatzes Null sein.</span><span class="sxs-lookup"><span data-stu-id="0f51a-130">If a [standard action](standard-actions.md) is used in the Action column of a merge module sequence table, the BaseAction and After columns of that record must be null.</span></span>

</dd> <dt>

<span data-ttu-id="0f51a-131"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenz</span><span class="sxs-lookup"><span data-stu-id="0f51a-131"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="0f51a-132">Die Sequenznummer einer Standardaktion.</span><span class="sxs-lookup"><span data-stu-id="0f51a-132">The sequence number of a standard action.</span></span> <span data-ttu-id="0f51a-133">Wenn eine benutzerdefinierte Aktion oder ein benutzerdefiniertes Dialogfeld in die Aktionsspalte dieser Zeile eingegeben wird, muss dieses Feld auf NULL festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="0f51a-133">If a custom action or dialog is entered into the Action column of this row, this field must be set to null.</span></span>

<span data-ttu-id="0f51a-134">Bei Verwendung von [Standard Aktionen](standard-actions.md) in Mergemodul-Sequenz Tabellen sollte der Wert in der Sequence-Spalte die empfohlene Aktions Sequenznummer sein.</span><span class="sxs-lookup"><span data-stu-id="0f51a-134">When using [standard actions](standard-actions.md) in merge module sequence tables, the value in the Sequence column should be the recommended action sequence number.</span></span> <span data-ttu-id="0f51a-135">Wenn sich die Sequenznummer im Mergemodul von der Sequenznummer für die gleiche Aktion in der MSI-Datei Sequenz Tabelle unterscheidet, verwendet das Mergetool die Sequenznummer aus der MSI-Datei.</span><span class="sxs-lookup"><span data-stu-id="0f51a-135">If the sequence number in the merge module differs from that for the same action in the .msi file sequence table, the merge tool uses the sequence number from the .msi file.</span></span> <span data-ttu-id="0f51a-136">Informationen zu den empfohlenen Sequenznummern von Standard Aktionen finden [Sie unter Verwenden einer Sequenz Tabelle](using-a-sequence-table.md) für vorgeschlagene Sequenzen.</span><span class="sxs-lookup"><span data-stu-id="0f51a-136">See the suggested sequences in [Using a Sequence Table](using-a-sequence-table.md) for the recommended sequence numbers of standard actions.</span></span>

</dd> <dt>

<span data-ttu-id="0f51a-137"><span id="BaseAction"></span><span id="baseaction"></span><span id="BASEACTION"></span>Baseaction</span><span class="sxs-lookup"><span data-stu-id="0f51a-137"><span id="BaseAction"></span><span id="baseaction"></span><span id="BASEACTION"></span>BaseAction</span></span>
</dt> <dd>

<span data-ttu-id="0f51a-138">Die baseaction-Spalte kann eine Standardaktion, eine benutzerdefinierte Aktion, die in der benutzerdefinierten Aktionstabelle des Merge-Moduls angegeben ist, oder ein Dialogfeld enthalten, das in der Dialog Tabelle des Moduls angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="0f51a-138">The BaseAction column may contain a standard action, a custom action specified in the merge module's custom action table, or a dialog specified in the module's dialog table.</span></span> <span data-ttu-id="0f51a-139">Die baseaction-Spalte ist ein Schlüssel in der Aktionsspalte dieser Tabelle.</span><span class="sxs-lookup"><span data-stu-id="0f51a-139">The BaseAction column is a key into the Action column of this table.</span></span> <span data-ttu-id="0f51a-140">Dabei kann es sich nicht um einen Fremdschlüssel in einer anderen MERGE-Tabelle oder-Tabelle in der Windows Installer Datei handeln.</span><span class="sxs-lookup"><span data-stu-id="0f51a-140">It cannot be a foreign key into another merge table or table in the Windows Installer file.</span></span> <span data-ttu-id="0f51a-141">Dies bedeutet, dass jede Standardaktion, benutzerdefinierte Aktion oder ein Dialogfeld, das in der Spalte baseaction aufgeführt ist, auch in der Aktionsspalte eines anderen Datensatzes in dieser Tabelle aufgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="0f51a-141">This means that every standard action, custom action, or dialog listed in the BaseAction column must also be listed in the Action column of another record in this table.</span></span>

</dd> <dt>

<span data-ttu-id="0f51a-142"><span id="After"></span><span id="after"></span><span id="AFTER"></span>Nachdem</span><span class="sxs-lookup"><span data-stu-id="0f51a-142"><span id="After"></span><span id="after"></span><span id="AFTER"></span>After</span></span>
</dt> <dd>

<span data-ttu-id="0f51a-143">Boolescher Wert, der ist, ob Action vor oder nach baseaction steht.</span><span class="sxs-lookup"><span data-stu-id="0f51a-143">Boolean for whether Action comes before or after BaseAction.</span></span>



| <span data-ttu-id="0f51a-144">Wert</span><span class="sxs-lookup"><span data-stu-id="0f51a-144">Value</span></span> | <span data-ttu-id="0f51a-145">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0f51a-145">Meaning</span></span>                          |
|-------|----------------------------------|
| <span data-ttu-id="0f51a-146">0</span><span class="sxs-lookup"><span data-stu-id="0f51a-146">0</span></span>     | <span data-ttu-id="0f51a-147">Aktion, die vor baseaction erfolgen soll</span><span class="sxs-lookup"><span data-stu-id="0f51a-147">Action to come before BaseAction</span></span> |
| <span data-ttu-id="0f51a-148">1</span><span class="sxs-lookup"><span data-stu-id="0f51a-148">1</span></span>     | <span data-ttu-id="0f51a-149">Aktion, die nach baseaction erfolgen soll</span><span class="sxs-lookup"><span data-stu-id="0f51a-149">Action to come after BaseAction</span></span>  |



 

</dd> <dt>

<span data-ttu-id="0f51a-150"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Anlage</span><span class="sxs-lookup"><span data-stu-id="0f51a-150"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="0f51a-151">Eine Bedingungs Anweisung, die angibt, ob die Aktion ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0f51a-151">A conditional statement that indicates if the action is to be executed.</span></span> <span data-ttu-id="0f51a-152">Ein NULL-Wert wird als true ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="0f51a-152">A null value evaluates to true.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0f51a-153">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0f51a-153">Remarks</span></span>

<span data-ttu-id="0f51a-154">Wenn die [moduleinstallexecutesequence-Tabelle](installexecutesequence-table.md) vorhanden ist, muss auch die [InstallExecuteSequence-Tabelle](installexecutesequence-table.md) im Mergemodul vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="0f51a-154">If the [ModuleInstallExecuteSequence table](installexecutesequence-table.md) is present, the [InstallExecuteSequence table](installexecutesequence-table.md) must also be present in the merge module.</span></span>

 

 



