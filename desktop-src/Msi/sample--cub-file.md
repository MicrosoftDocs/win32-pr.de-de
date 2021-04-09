---
description: 'Dieses Beispiel veranschaulicht das Layout einer CUB-Datei, die zwei ICES enthält. Der Installer führt die benutzerdefinierten Aktionen in der folgenden Reihenfolge aus: ICE01 und ICE08.'
ms.assetid: 609cd16a-4421-4082-855d-229f5ba7117b
title: Sample. CUB-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e937b779e2a620ffc17cf936e37f74867f3dfdd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958885"
---
# <a name="sample-cub-file"></a><span data-ttu-id="c9a7e-104">Sample. CUB-Datei</span><span class="sxs-lookup"><span data-stu-id="c9a7e-104">Sample .cub File</span></span>

<span data-ttu-id="c9a7e-105">Dieses Beispiel veranschaulicht das Layout einer CUB-Datei, die zwei [ICES](internal-consistency-evaluators-ices.md)enthält.</span><span class="sxs-lookup"><span data-stu-id="c9a7e-105">This sample illustrates the layout of a .cub file containing two [ICEs](internal-consistency-evaluators-ices.md).</span></span> <span data-ttu-id="c9a7e-106">Der Installer führt die benutzerdefinierten Aktionen in der folgenden Reihenfolge aus: ICE01 und ICE08.</span><span class="sxs-lookup"><span data-stu-id="c9a7e-106">The installer executes the custom actions in the sequence: ICE01 and ICE08.</span></span>

<span data-ttu-id="c9a7e-107">Die benutzerdefinierte Aktion ICE01 ist ein [benutzerdefinierter Aktionstyp 1](custom-action-type-1.md).</span><span class="sxs-lookup"><span data-stu-id="c9a7e-107">The custom action ICE01 is a [Custom Action Type 1](custom-action-type-1.md).</span></span> <span data-ttu-id="c9a7e-108">Es handelt sich um einen Einstiegspunkt für eine DLL, die als Stream in der CUB-Datei gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="c9a7e-108">It is an entry point to a DLL that is stored as a stream in the .cub file.</span></span> <span data-ttu-id="c9a7e-109">Dieser Stream wird in der ice.dll der binären Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="c9a7e-109">This stream is listed in the Binary Table ice.dll.</span></span>

<span data-ttu-id="c9a7e-110">Die benutzerdefinierte Aktion ICE08 ist ein [benutzerdefinierter Aktionstyp 6](custom-action-type-6.md).</span><span class="sxs-lookup"><span data-stu-id="c9a7e-110">The custom action ICE08 is a [Custom Action Type 6](custom-action-type-6.md).</span></span> <span data-ttu-id="c9a7e-111">Es handelt sich um einen Einstiegspunkt für eine Funktion in VBScript, die als Stream in der CUB-Datei gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="c9a7e-111">It is an entry point to a function in VBScript that is stored as a stream in the .cub file.</span></span> <span data-ttu-id="c9a7e-112">Dieser Stream wird in der Binär Tabelle als ice.vbs aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="c9a7e-112">This stream is listed in the Binary Table as ice.vbs.</span></span>

[<span data-ttu-id="c9a7e-113">Binäre Tabelle</span><span class="sxs-lookup"><span data-stu-id="c9a7e-113">Binary Table</span></span>](binary-table.md)



| <span data-ttu-id="c9a7e-114">Name</span><span class="sxs-lookup"><span data-stu-id="c9a7e-114">Name</span></span>    | <span data-ttu-id="c9a7e-115">Daten</span><span class="sxs-lookup"><span data-stu-id="c9a7e-115">Data</span></span>                               |
|---------|------------------------------------|
| <span data-ttu-id="c9a7e-116">ice.vbs</span><span class="sxs-lookup"><span data-stu-id="c9a7e-116">ice.vbs</span></span> | <span data-ttu-id="c9a7e-117">Nicht formatierte Binärdaten von ice.vbs</span><span class="sxs-lookup"><span data-stu-id="c9a7e-117">Unformatted binary data of ice.vbs</span></span> |
| <span data-ttu-id="c9a7e-118">ice.dll</span><span class="sxs-lookup"><span data-stu-id="c9a7e-118">ice.dll</span></span> | <span data-ttu-id="c9a7e-119">Nicht formatierte Binärdaten von ice.dll</span><span class="sxs-lookup"><span data-stu-id="c9a7e-119">Unformatted binary data of ice.dll</span></span> |



 

[<span data-ttu-id="c9a7e-120">Tabelle "CustomAction"</span><span class="sxs-lookup"><span data-stu-id="c9a7e-120">CustomAction Table</span></span>](customaction-table.md)



| <span data-ttu-id="c9a7e-121">Aktion</span><span class="sxs-lookup"><span data-stu-id="c9a7e-121">Action</span></span> | <span data-ttu-id="c9a7e-122">type</span><span class="sxs-lookup"><span data-stu-id="c9a7e-122">Type</span></span> | <span data-ttu-id="c9a7e-123">`Source`</span><span class="sxs-lookup"><span data-stu-id="c9a7e-123">Source</span></span>  | <span data-ttu-id="c9a7e-124">Ziel</span><span class="sxs-lookup"><span data-stu-id="c9a7e-124">Target</span></span> |
|--------|------|---------|--------|
| <span data-ttu-id="c9a7e-125">ICE01</span><span class="sxs-lookup"><span data-stu-id="c9a7e-125">ICE01</span></span>  | <span data-ttu-id="c9a7e-126">1</span><span class="sxs-lookup"><span data-stu-id="c9a7e-126">1</span></span>    | <span data-ttu-id="c9a7e-127">ice.dll</span><span class="sxs-lookup"><span data-stu-id="c9a7e-127">ice.dll</span></span> | <span data-ttu-id="c9a7e-128">ICE01</span><span class="sxs-lookup"><span data-stu-id="c9a7e-128">ICE01</span></span>  |
| <span data-ttu-id="c9a7e-129">ICE08</span><span class="sxs-lookup"><span data-stu-id="c9a7e-129">ICE08</span></span>  | <span data-ttu-id="c9a7e-130">6</span><span class="sxs-lookup"><span data-stu-id="c9a7e-130">6</span></span>    | <span data-ttu-id="c9a7e-131">ice.vbs</span><span class="sxs-lookup"><span data-stu-id="c9a7e-131">ice.vbs</span></span> | <span data-ttu-id="c9a7e-132">ICE02</span><span class="sxs-lookup"><span data-stu-id="c9a7e-132">ICE02</span></span>  |



 

<span data-ttu-id="c9a7e-133">\_Icesequence-Tabelle</span><span class="sxs-lookup"><span data-stu-id="c9a7e-133">\_ICESequence Table</span></span>



| <span data-ttu-id="c9a7e-134">Aktion</span><span class="sxs-lookup"><span data-stu-id="c9a7e-134">Action</span></span> | <span data-ttu-id="c9a7e-135">Bedingung</span><span class="sxs-lookup"><span data-stu-id="c9a7e-135">Condition</span></span> | <span data-ttu-id="c9a7e-136">Sequenz</span><span class="sxs-lookup"><span data-stu-id="c9a7e-136">Sequence</span></span> |
|--------|-----------|----------|
| <span data-ttu-id="c9a7e-137">ICE01</span><span class="sxs-lookup"><span data-stu-id="c9a7e-137">ICE01</span></span>  |           | <span data-ttu-id="c9a7e-138">10</span><span class="sxs-lookup"><span data-stu-id="c9a7e-138">10</span></span>       |
| <span data-ttu-id="c9a7e-139">ICE08</span><span class="sxs-lookup"><span data-stu-id="c9a7e-139">ICE08</span></span>  |           | <span data-ttu-id="c9a7e-140">20</span><span class="sxs-lookup"><span data-stu-id="c9a7e-140">20</span></span>       |



 

<span data-ttu-id="c9a7e-141">\_Spezielle Tabelle</span><span class="sxs-lookup"><span data-stu-id="c9a7e-141">\_Special Table</span></span>

<span data-ttu-id="c9a7e-142">ICE01 und ICE08 erfordern nicht die Einbindung spezieller Verarbeitungs Tabellen.</span><span class="sxs-lookup"><span data-stu-id="c9a7e-142">ICE01 and ICE08 do not require the inclusion of special processing tables.</span></span> <span data-ttu-id="c9a7e-143">Wenn die CUB-Datei spezielle Tabellen enthält, müssen Sie auch in der \_ Validierungs Tabelle enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="c9a7e-143">When the .cub file contains special tables they must also be included in the \_Validation Table.</span></span>

[<span data-ttu-id="c9a7e-144">\_Validierungs Tabelle</span><span class="sxs-lookup"><span data-stu-id="c9a7e-144">\_Validation Table</span></span>](-validation-table.md)



| <span data-ttu-id="c9a7e-145">Tabelle</span><span class="sxs-lookup"><span data-stu-id="c9a7e-145">Table</span></span>         | <span data-ttu-id="c9a7e-146">Spalte</span><span class="sxs-lookup"><span data-stu-id="c9a7e-146">Column</span></span>    | <span data-ttu-id="c9a7e-147">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="c9a7e-147">Nullable</span></span> | <span data-ttu-id="c9a7e-148">MinValue</span><span class="sxs-lookup"><span data-stu-id="c9a7e-148">MinValue</span></span> | <span data-ttu-id="c9a7e-149">MaxValue</span><span class="sxs-lookup"><span data-stu-id="c9a7e-149">MaxValue</span></span> | <span data-ttu-id="c9a7e-150">KeyTable</span><span class="sxs-lookup"><span data-stu-id="c9a7e-150">KeyTable</span></span> | <span data-ttu-id="c9a7e-151">KeyColumn</span><span class="sxs-lookup"><span data-stu-id="c9a7e-151">KeyColumn</span></span> | <span data-ttu-id="c9a7e-152">Category</span><span class="sxs-lookup"><span data-stu-id="c9a7e-152">Category</span></span>                         | <span data-ttu-id="c9a7e-153">Set</span><span class="sxs-lookup"><span data-stu-id="c9a7e-153">Set</span></span> | <span data-ttu-id="c9a7e-154">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c9a7e-154">Description</span></span> |
|---------------|-----------|----------|----------|----------|----------|-----------|----------------------------------|-----|-------------|
| <span data-ttu-id="c9a7e-155">Binary</span><span class="sxs-lookup"><span data-stu-id="c9a7e-155">Binary</span></span>        | <span data-ttu-id="c9a7e-156">Name</span><span class="sxs-lookup"><span data-stu-id="c9a7e-156">Name</span></span>      | <span data-ttu-id="c9a7e-157">N</span><span class="sxs-lookup"><span data-stu-id="c9a7e-157">N</span></span>        |          |          |          |           | [<span data-ttu-id="c9a7e-158">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="c9a7e-158">Identifier</span></span>](identifier.md)     |     |             |
| <span data-ttu-id="c9a7e-159">Binary</span><span class="sxs-lookup"><span data-stu-id="c9a7e-159">Binary</span></span>        | <span data-ttu-id="c9a7e-160">Daten</span><span class="sxs-lookup"><span data-stu-id="c9a7e-160">Data</span></span>      | <span data-ttu-id="c9a7e-161">N</span><span class="sxs-lookup"><span data-stu-id="c9a7e-161">N</span></span>        |          |          |          |           | [<span data-ttu-id="c9a7e-162">Binär (Binary)</span><span class="sxs-lookup"><span data-stu-id="c9a7e-162">Binary</span></span>](binary.md)             |     |             |
| <span data-ttu-id="c9a7e-163">CustomAction</span><span class="sxs-lookup"><span data-stu-id="c9a7e-163">CustomAction</span></span>  | <span data-ttu-id="c9a7e-164">Aktion</span><span class="sxs-lookup"><span data-stu-id="c9a7e-164">Action</span></span>    | <span data-ttu-id="c9a7e-165">N</span><span class="sxs-lookup"><span data-stu-id="c9a7e-165">N</span></span>        |          |          |          |           | [<span data-ttu-id="c9a7e-166">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="c9a7e-166">Identifier</span></span>](identifier.md)     |     |             |
| <span data-ttu-id="c9a7e-167">CustomAction</span><span class="sxs-lookup"><span data-stu-id="c9a7e-167">CustomAction</span></span>  | <span data-ttu-id="c9a7e-168">type</span><span class="sxs-lookup"><span data-stu-id="c9a7e-168">Type</span></span>      | <span data-ttu-id="c9a7e-169">N</span><span class="sxs-lookup"><span data-stu-id="c9a7e-169">N</span></span>        |          |          |          |           | [<span data-ttu-id="c9a7e-170">Integer</span><span class="sxs-lookup"><span data-stu-id="c9a7e-170">Integer</span></span>](integer.md)           |     |             |
| <span data-ttu-id="c9a7e-171">CustomAction</span><span class="sxs-lookup"><span data-stu-id="c9a7e-171">CustomAction</span></span>  | <span data-ttu-id="c9a7e-172">`Source`</span><span class="sxs-lookup"><span data-stu-id="c9a7e-172">Source</span></span>    | <span data-ttu-id="c9a7e-173">J</span><span class="sxs-lookup"><span data-stu-id="c9a7e-173">Y</span></span>        |          |          |          |           | [<span data-ttu-id="c9a7e-174">CustomSource</span><span class="sxs-lookup"><span data-stu-id="c9a7e-174">CustomSource</span></span>](customsource.md) |     |             |
| <span data-ttu-id="c9a7e-175">CustomAction</span><span class="sxs-lookup"><span data-stu-id="c9a7e-175">CustomAction</span></span>  | <span data-ttu-id="c9a7e-176">Ziel</span><span class="sxs-lookup"><span data-stu-id="c9a7e-176">Target</span></span>    | <span data-ttu-id="c9a7e-177">J</span><span class="sxs-lookup"><span data-stu-id="c9a7e-177">Y</span></span>        |          |          |          |           | [<span data-ttu-id="c9a7e-178">Großformatige</span><span class="sxs-lookup"><span data-stu-id="c9a7e-178">Formatted</span></span>](formatted.md)       |     |             |
| <span data-ttu-id="c9a7e-179">\_Icesequence</span><span class="sxs-lookup"><span data-stu-id="c9a7e-179">\_ICESequence</span></span> | <span data-ttu-id="c9a7e-180">Aktion</span><span class="sxs-lookup"><span data-stu-id="c9a7e-180">Action</span></span>    | <span data-ttu-id="c9a7e-181">N</span><span class="sxs-lookup"><span data-stu-id="c9a7e-181">N</span></span>        |          |          |          |           | [<span data-ttu-id="c9a7e-182">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="c9a7e-182">Identifier</span></span>](identifier.md)     |     |             |
| <span data-ttu-id="c9a7e-183">\_Icesequence</span><span class="sxs-lookup"><span data-stu-id="c9a7e-183">\_ICESequence</span></span> | <span data-ttu-id="c9a7e-184">Bedingung</span><span class="sxs-lookup"><span data-stu-id="c9a7e-184">Condition</span></span> | <span data-ttu-id="c9a7e-185">J</span><span class="sxs-lookup"><span data-stu-id="c9a7e-185">Y</span></span>        |          |          |          |           | [<span data-ttu-id="c9a7e-186">Condition</span><span class="sxs-lookup"><span data-stu-id="c9a7e-186">Condition</span></span>](condition.md)       |     |             |
| <span data-ttu-id="c9a7e-187">\_Icesequence</span><span class="sxs-lookup"><span data-stu-id="c9a7e-187">\_ICESequence</span></span> | <span data-ttu-id="c9a7e-188">Sequenz</span><span class="sxs-lookup"><span data-stu-id="c9a7e-188">Sequence</span></span>  | <span data-ttu-id="c9a7e-189">J</span><span class="sxs-lookup"><span data-stu-id="c9a7e-189">Y</span></span>        |          |          |          |           | [<span data-ttu-id="c9a7e-190">Integer</span><span class="sxs-lookup"><span data-stu-id="c9a7e-190">Integer</span></span>](integer.md)           |     |             |



 

 

 



