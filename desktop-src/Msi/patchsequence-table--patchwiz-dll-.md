---
description: Die Tabelle "patchsequence" wird verwendet, um die msipatchsequence-Tabelle in einem Patch zu generieren. Die Tabelle erfordert die Version von PATCHWIZ.DLL, die mit Windows Installer&\# 160; 3.0 verfügbar ist.
ms.assetid: bdeccb3b-57c0-4424-9602-348b8048fd46
title: Patchsequence-Tabelle (PATCHWIZ.DLL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 382e940d3c0cb6c7be2c8360ab98f2afaf13c799
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868847"
---
# <a name="patchsequence-table-patchwizdll"></a><span data-ttu-id="b0c0c-104">Patchsequence-Tabelle (PATCHWIZ.DLL)</span><span class="sxs-lookup"><span data-stu-id="b0c0c-104">PatchSequence Table (PATCHWIZ.DLL)</span></span>

<span data-ttu-id="b0c0c-105">Die Tabelle "patchsequence" wird verwendet, um die [msipatchsequence-Tabelle](msipatchsequence-table.md) in einem Patch zu generieren.</span><span class="sxs-lookup"><span data-stu-id="b0c0c-105">The PatchSequence Table is used to generate the [MsiPatchSequence Table](msipatchsequence-table.md) in a patch.</span></span> <span data-ttu-id="b0c0c-106">Die Tabelle erfordert die Version von [PATCHWIZ.DLL](patchwiz-dll.md) , die in Windows Installer 3,0 verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="b0c0c-106">The table requires the version of [PATCHWIZ.DLL](patchwiz-dll.md) that is available with Windows Installer 3.0.</span></span>

<span data-ttu-id="b0c0c-107">In der folgenden Tabelle sind die Spalten der Tabelle patchsequence aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="b0c0c-107">The following table identifies the columns of the PatchSequence Table.</span></span>



| <span data-ttu-id="b0c0c-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="b0c0c-108">Column</span></span>      | <span data-ttu-id="b0c0c-109">Typ</span><span class="sxs-lookup"><span data-stu-id="b0c0c-109">Type</span></span>       | <span data-ttu-id="b0c0c-110">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="b0c0c-110">Key</span></span> | <span data-ttu-id="b0c0c-111">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="b0c0c-111">Nullable</span></span> |
|-------------|------------|-----|----------|
| <span data-ttu-id="b0c0c-112">Patchfamilie</span><span class="sxs-lookup"><span data-stu-id="b0c0c-112">PatchFamily</span></span> | <span data-ttu-id="b0c0c-113">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="b0c0c-113">Identifier</span></span> | <span data-ttu-id="b0c0c-114">J</span><span class="sxs-lookup"><span data-stu-id="b0c0c-114">Y</span></span>   | <span data-ttu-id="b0c0c-115">N</span><span class="sxs-lookup"><span data-stu-id="b0c0c-115">N</span></span>        |
| <span data-ttu-id="b0c0c-116">Ziel</span><span class="sxs-lookup"><span data-stu-id="b0c0c-116">Target</span></span>      | <span data-ttu-id="b0c0c-117">Text</span><span class="sxs-lookup"><span data-stu-id="b0c0c-117">Text</span></span>       | <span data-ttu-id="b0c0c-118">J</span><span class="sxs-lookup"><span data-stu-id="b0c0c-118">Y</span></span>   | <span data-ttu-id="b0c0c-119">J</span><span class="sxs-lookup"><span data-stu-id="b0c0c-119">Y</span></span>        |
| <span data-ttu-id="b0c0c-120">Sequenz</span><span class="sxs-lookup"><span data-stu-id="b0c0c-120">Sequence</span></span>    | <span data-ttu-id="b0c0c-121">Version</span><span class="sxs-lookup"><span data-stu-id="b0c0c-121">Version</span></span>    |     | <span data-ttu-id="b0c0c-122">J</span><span class="sxs-lookup"><span data-stu-id="b0c0c-122">Y</span></span>        |
| <span data-ttu-id="b0c0c-123">Ablösen</span><span class="sxs-lookup"><span data-stu-id="b0c0c-123">Supersede</span></span>   | <span data-ttu-id="b0c0c-124">Integer</span><span class="sxs-lookup"><span data-stu-id="b0c0c-124">Integer</span></span>    |     | <span data-ttu-id="b0c0c-125">J</span><span class="sxs-lookup"><span data-stu-id="b0c0c-125">Y</span></span>        |



 

### <a name="columns"></a><span data-ttu-id="b0c0c-126">Spalten</span><span class="sxs-lookup"><span data-stu-id="b0c0c-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="b0c0c-127"><span id="PatchFamily"></span><span id="patchfamily"></span><span id="PATCHFAMILY"></span>Patchfamilie</span><span class="sxs-lookup"><span data-stu-id="b0c0c-127"><span id="PatchFamily"></span><span id="patchfamily"></span><span id="PATCHFAMILY"></span>PatchFamily</span></span>
</dt> <dd>

<span data-ttu-id="b0c0c-128">Der Bezeichner, der die Sequenz Familien angibt, zu denen dieser Patch gehört.</span><span class="sxs-lookup"><span data-stu-id="b0c0c-128">The identifier that indicates the sequence families to which this patch belongs.</span></span>

<span data-ttu-id="b0c0c-129">Die Werte in den Spalten Ziel und patchfamilie definieren den Primärschlüssel für die Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b0c0c-129">The values in the Target and PatchFamily columns together define the primary key for the table.</span></span> <span data-ttu-id="b0c0c-130">Ein Patch, der zu mehreren Sequenz Familien gehört oder je nach Produktcode über unterschiedliche Sequenzen verfügt, kann für jede Kopplung eine Zeile aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b0c0c-130">A patch that belongs to multiple sequence families, or has different sequences depending on the product code of the target, can have one row for each pairing.</span></span> <span data-ttu-id="b0c0c-131">Dieser Wert wird verwendet, um die patchfamily-Spalte der [msipatchsequence-Tabelle](msipatchsequence-table.md) aufzufüllen, die zum Patch gehört.</span><span class="sxs-lookup"><span data-stu-id="b0c0c-131">This value is used to populate the PatchFamily column of the [MsiPatchSequence Table](msipatchsequence-table.md) that belongs to the patch.</span></span>

</dd> <dt>

<span data-ttu-id="b0c0c-132"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Spar</span><span class="sxs-lookup"><span data-stu-id="b0c0c-132"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Target</span></span>
</dt> <dd>

<span data-ttu-id="b0c0c-133">Die Ziel Spalte wird verwendet, um die patchfamilie nach Produktcode zu filtern.</span><span class="sxs-lookup"><span data-stu-id="b0c0c-133">The Target column is used to filter the PatchFamily by product code.</span></span>

<span data-ttu-id="b0c0c-134">Ein NULL-Wert in dieser Spalte gibt an, dass diese patchfamilie für alle Ziele des Patches gilt.</span><span class="sxs-lookup"><span data-stu-id="b0c0c-134">A NULL value in this column indicates that this PatchFamily applies to all targets of the patch.</span></span> <span data-ttu-id="b0c0c-135">Wenn diese Spalte einen Fremdschlüssel für die [TargetImages-Tabelle](targetimages-table-patchwiz-dll-.md)enthält, wird der Produktcode des angegebenen Bilds abgerufen und verwendet, um den Product Code-Wert in der Zeile des neuen Patches der [msipatchsequence-Tabelle](msipatchsequence-table.md)aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="b0c0c-135">If this column contains a foreign key to the [TargetImages Table](targetimages-table-patchwiz-dll-.md), the product code of the specified image is retrieved and used to populate the product code value in the new patch's row of the [MsiPatchSequence Table](msipatchsequence-table.md).</span></span> <span data-ttu-id="b0c0c-136">Wenn diese Spalte eine GUID enthält, wird die GUID verwendet, um den Product Code-Wert der Zeile in der msipatchsequence-Tabelle aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="b0c0c-136">If this column contains a GUID, the GUID is used to populate the product code value of the row in the MsiPatchSequence Table.</span></span>

</dd> <dt>

<span data-ttu-id="b0c0c-137"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenz</span><span class="sxs-lookup"><span data-stu-id="b0c0c-137"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="b0c0c-138">Der Wert in der Sequenz Spalte wird verwendet, um die Sequence-Spalte der [msipatchsequence-Tabelle](msipatchsequence-table.md) der neuen Patchdatei aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="b0c0c-138">The value in the Sequence column is used to populate the Sequence column of the [MsiPatchSequence Table](msipatchsequence-table.md) of the new patch file.</span></span>

<span data-ttu-id="b0c0c-139">Wenn der Wert NULL ist, wird automatisch eine Sequenznummer generiert.</span><span class="sxs-lookup"><span data-stu-id="b0c0c-139">If the value is NULL, a sequence number is generated automatically.</span></span>

</dd> <dt>

<span data-ttu-id="b0c0c-140"><span id="Supersede"></span><span id="supersede"></span><span id="SUPERSEDE"></span>Ablösen</span><span class="sxs-lookup"><span data-stu-id="b0c0c-140"><span id="Supersede"></span><span id="supersede"></span><span id="SUPERSEDE"></span>Supersede</span></span>
</dt> <dd>

<span data-ttu-id="b0c0c-141">Der Wert **msidbpatchsequencesupersedefrühere** oder 1 in diesem Feld gibt an, dass dieser Patch frühere [kleine Updates](small-updates.md) in den Sequenz Familien ersetzt, zu denen dieser Patch gehört.</span><span class="sxs-lookup"><span data-stu-id="b0c0c-141">A value of **msidbPatchSequenceSupersedeEarlier** or 1 in this field indicates that this patch supersedes earlier [small updates](small-updates.md) in the sequence families to which this patch belongs.</span></span>

<span data-ttu-id="b0c0c-142">Der Wert in dieser Spalte wird verwendet, um die Spalte Attribute der Zeile des neuen Patches in der [msipatchsequence-Tabelle](msipatchsequence-table.md) festzulegen.</span><span class="sxs-lookup"><span data-stu-id="b0c0c-142">The value in this column is used to set the Attributes column of the new patch's row in the [MsiPatchSequence Table](msipatchsequence-table.md) .</span></span>

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="b0c0c-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b0c0c-143">Remarks</span></span>

<span data-ttu-id="b0c0c-144">Verfügbar ab Windows Installer 3,0.</span><span class="sxs-lookup"><span data-stu-id="b0c0c-144">Available beginning in Windows Installer 3.0.</span></span>

 

 



