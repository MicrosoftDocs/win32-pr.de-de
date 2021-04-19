---
description: ICE12 überprüft die Tabellen CustomAction, Directory, AdminExecuteSequence, AdminUISequence, AdvtExecuteSequence, InstallExecuteSequence und InstallUISequence der Windows Installer Datenbank.
ms.assetid: c1576aff-ff05-49be-8679-a8bfd01977f5
title: ICE12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d02756bd357c6e85f60b0c41b72a4a66965fedb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368848"
---
# <a name="ice12"></a><span data-ttu-id="0e98a-103">ICE12</span><span class="sxs-lookup"><span data-stu-id="0e98a-103">ICE12</span></span>

<span data-ttu-id="0e98a-104">ICE12 fragt die Tabellen [CustomAction](customaction-table.md), [Directory](directory-table.md), [AdminExecuteSequence](adminexecutesequence-table.md), [AdminUISequence](adminuisequence-table.md), [AdvtExecuteSequence](advtexecutesequence-table.md), [InstallExecuteSequence](installexecutesequence-table.md)und [InstallUISequence](installuisequence-table.md) ab, um Folgendes zu überprüfen:</span><span class="sxs-lookup"><span data-stu-id="0e98a-104">ICE12 queries the [CustomAction](customaction-table.md), [Directory](directory-table.md), [AdminExecuteSequence](adminexecutesequence-table.md), [AdminUISequence](adminuisequence-table.md), [AdvtExecuteSequence](advtexecutesequence-table.md), [InstallExecuteSequence](installexecutesequence-table.md), and [InstallUISequence](installuisequence-table.md) tables to validate the following:</span></span>

-   <span data-ttu-id="0e98a-105">Die [costfinalize-Aktion](costfinalize-action.md) findet in jeder Sequenz Tabelle statt, die Aktionen vom Typ [benutzerdefinierte Aktionstyp 35](custom-action-type-35.md) oder [benutzerdefinierter Aktionstyp 51](custom-action-type-51.md)enthält.</span><span class="sxs-lookup"><span data-stu-id="0e98a-105">That the [CostFinalize action](costfinalize-action.md) occurs in any sequence table containing actions of the type [Custom Action Type 35](custom-action-type-35.md) or [Custom Action Type 51](custom-action-type-51.md).</span></span>
-   <span data-ttu-id="0e98a-106">Jeder [benutzerdefinierte Aktionstyp 35](custom-action-type-35.md) kommt nach der [costfinalize-Aktion](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="0e98a-106">That every [Custom Action Type 35](custom-action-type-35.md) comes after the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="0e98a-107">in den Sequenz Tabellen.</span><span class="sxs-lookup"><span data-stu-id="0e98a-107">in the sequence tables.</span></span>
-   <span data-ttu-id="0e98a-108">Jeder [benutzerdefinierte Aktionstyp 51](custom-action-type-51.md) , der über einen Fremdschlüssel für die Verzeichnis Tabelle in der Quell Spalte der Tabelle "CustomAction" verfügt, kommt vor der [Aktion "costfinalize](costfinalize-action.md) " in den Sequenz Tabellen.</span><span class="sxs-lookup"><span data-stu-id="0e98a-108">That every [Custom Action Type 51](custom-action-type-51.md) that has a foreign key to the Directory table in the Source column of the CustomAction table comes before the [CostFinalize action](costfinalize-action.md) in the sequence tables.</span></span>

<span data-ttu-id="0e98a-109">Beachten Sie, dass ICE12 den formatierten Text in der Ziel Spalte der Tabelle "CustomAction" nicht überprüft.</span><span class="sxs-lookup"><span data-stu-id="0e98a-109">Note that ICE12 does not validate the formatted text in the Target column of the CustomAction table.</span></span>

## <a name="result"></a><span data-ttu-id="0e98a-110">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="0e98a-110">Result</span></span>

<span data-ttu-id="0e98a-111">ICE12 gibt eine Fehlermeldung aus, wenn die Validierung der benutzerdefinierten Aktionen, die eine Verzeichnis Eigenschaft festlegen, fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="0e98a-111">ICE12 posts an error message if validation of the custom actions that set a directory property fails.</span></span>

## <a name="example"></a><span data-ttu-id="0e98a-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0e98a-112">Example</span></span>

<span data-ttu-id="0e98a-113">ICE12 würde drei Fehler für das gezeigte Beispiel Posten.</span><span class="sxs-lookup"><span data-stu-id="0e98a-113">ICE12 would post three errors for the example shown.</span></span>

-   <span data-ttu-id="0e98a-114">Für CA1 wurde der Ordner "MyFolder" in der Verzeichnis Tabelle nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="0e98a-114">For CA1, Folder 'MyFolder' not found in Directory table</span></span>
-   <span data-ttu-id="0e98a-115">Für "Ca2" kommt die Sequenz "80" vor "costfinalize" in der Tabelle "InstallExecuteSequence".</span><span class="sxs-lookup"><span data-stu-id="0e98a-115">For CA2, Sequence '80' comes before CostFinalize in the InstallExecuteSequence table.</span></span> <span data-ttu-id="0e98a-116">Der Wert muss nach ( CF@100 ) liegen.</span><span class="sxs-lookup"><span data-stu-id="0e98a-116">It must come after (CF@100)</span></span>
-   <span data-ttu-id="0e98a-117">Für CA3 kommt die Sequenz "125" nach "costfinalize" in der Tabelle "InstallExecuteSequence".</span><span class="sxs-lookup"><span data-stu-id="0e98a-117">For CA3, Sequence '125' comes after CostFinalize in the InstallExecuteSequence table.</span></span> <span data-ttu-id="0e98a-118">Er muss vor () stehen. CF@100</span><span class="sxs-lookup"><span data-stu-id="0e98a-118">It must come before (CF@100)</span></span>

<span data-ttu-id="0e98a-119">[CustomAction-Tabelle](customaction-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="0e98a-119">[CustomAction Table](customaction-table.md) (partial)</span></span>



| <span data-ttu-id="0e98a-120">Aktion</span><span class="sxs-lookup"><span data-stu-id="0e98a-120">Action</span></span> | <span data-ttu-id="0e98a-121">type</span><span class="sxs-lookup"><span data-stu-id="0e98a-121">Type</span></span> | <span data-ttu-id="0e98a-122">`Source`</span><span class="sxs-lookup"><span data-stu-id="0e98a-122">Source</span></span>        |
|--------|------|---------------|
| <span data-ttu-id="0e98a-123">KA1</span><span class="sxs-lookup"><span data-stu-id="0e98a-123">CA1</span></span>    | <span data-ttu-id="0e98a-124">35</span><span class="sxs-lookup"><span data-stu-id="0e98a-124">35</span></span>   | <span data-ttu-id="0e98a-125">MyFolder</span><span class="sxs-lookup"><span data-stu-id="0e98a-125">MyFolder</span></span>      |
| <span data-ttu-id="0e98a-126">Ca2</span><span class="sxs-lookup"><span data-stu-id="0e98a-126">CA2</span></span>    | <span data-ttu-id="0e98a-127">35</span><span class="sxs-lookup"><span data-stu-id="0e98a-127">35</span></span>   | <span data-ttu-id="0e98a-128">Verzeichnis Windows befinden</span><span class="sxs-lookup"><span data-stu-id="0e98a-128">WindowsFolder</span></span> |
| <span data-ttu-id="0e98a-129">CA3</span><span class="sxs-lookup"><span data-stu-id="0e98a-129">CA3</span></span>    | <span data-ttu-id="0e98a-130">51</span><span class="sxs-lookup"><span data-stu-id="0e98a-130">51</span></span>   | <span data-ttu-id="0e98a-131">Verzeichnis Windows befinden</span><span class="sxs-lookup"><span data-stu-id="0e98a-131">WindowsFolder</span></span> |



 

[<span data-ttu-id="0e98a-132">Verzeichnis Tabelle</span><span class="sxs-lookup"><span data-stu-id="0e98a-132">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="0e98a-133">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="0e98a-133">Directory</span></span>     | <span data-ttu-id="0e98a-134">Über \_ geordnetes Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="0e98a-134">Directory\_Parent</span></span> | <span data-ttu-id="0e98a-135">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="0e98a-135">DefaultDir</span></span>    |
|---------------|-------------------|---------------|
| <span data-ttu-id="0e98a-136">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="0e98a-136">TARGETDIR</span></span>     |                   | <span data-ttu-id="0e98a-137">SourceDir</span><span class="sxs-lookup"><span data-stu-id="0e98a-137">SourceDir</span></span>     |
| <span data-ttu-id="0e98a-138">Verzeichnis Windows befinden</span><span class="sxs-lookup"><span data-stu-id="0e98a-138">WindowsFolder</span></span> | <span data-ttu-id="0e98a-139">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="0e98a-139">TARGETDIR</span></span>         | <span data-ttu-id="0e98a-140">Verzeichnis Windows befinden</span><span class="sxs-lookup"><span data-stu-id="0e98a-140">WindowsFolder</span></span> |



 

<span data-ttu-id="0e98a-141">[InstallExecuteSequence-Tabelle](installexecutesequence-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="0e98a-141">[InstallExecuteSequence Table](installexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="0e98a-142">Aktion</span><span class="sxs-lookup"><span data-stu-id="0e98a-142">Action</span></span>       | <span data-ttu-id="0e98a-143">Sequenz</span><span class="sxs-lookup"><span data-stu-id="0e98a-143">Sequence</span></span> |
|--------------|----------|
| <span data-ttu-id="0e98a-144">Costfinalize</span><span class="sxs-lookup"><span data-stu-id="0e98a-144">CostFinalize</span></span> | <span data-ttu-id="0e98a-145">100</span><span class="sxs-lookup"><span data-stu-id="0e98a-145">100</span></span>      |
| <span data-ttu-id="0e98a-146">Ca2</span><span class="sxs-lookup"><span data-stu-id="0e98a-146">CA2</span></span>          | <span data-ttu-id="0e98a-147">80</span><span class="sxs-lookup"><span data-stu-id="0e98a-147">80</span></span>       |
| <span data-ttu-id="0e98a-148">CA3</span><span class="sxs-lookup"><span data-stu-id="0e98a-148">CA3</span></span>          | <span data-ttu-id="0e98a-149">125</span><span class="sxs-lookup"><span data-stu-id="0e98a-149">125</span></span>      |



 

<span data-ttu-id="0e98a-150">Um den Fehler für CA1 zu beheben, ändern Sie den Eintrag in der Quell Spalte in der Tabelle CustomAction in einen vorhandenen Eintrag in der Verzeichnis Tabelle, oder fügen Sie der Verzeichnis Tabelle den Eintrag MyFolder hinzu.</span><span class="sxs-lookup"><span data-stu-id="0e98a-150">To fix the error for CA1 change its entry in its Source column in the CustomAction table to an existing entry in the Directory table or add MyFolder to the Directory table.</span></span>

<span data-ttu-id="0e98a-151">Um den Fehler für "Ca2" zu beheben, ändern Sie die zugehörige Sequenz in der InstallExecuteSequence-Tabelle so, dass Sie nach der Aktion "costfinalize" angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="0e98a-151">To fix the error for CA2, change its sequence in the InstallExecuteSequence table such that it comes after the CostFinalize action.</span></span>

<span data-ttu-id="0e98a-152">Um den Fehler für CA3 zu beheben, ändern Sie die zugehörige Reihenfolge in der InstallExecuteSequence-Tabelle so, dass Sie vor der costfinalize-Aktion steht.</span><span class="sxs-lookup"><span data-stu-id="0e98a-152">To fix the error for CA3, change its sequence in the InstallExecuteSequence table such that it comes before the CostFinalize action.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e98a-153">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0e98a-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e98a-154">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="0e98a-154">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



