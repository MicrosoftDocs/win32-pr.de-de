---
description: ICEM04 überprüft, ob die erforderlichen leeren Tabellen des Mergemoduls leer sind. Fehler beim Beheben eines Fehlers, der dazu führt, dass ICEM04 Berichte zu einer falschen Zusammenführung des Mergemoduls führen können.
ms.assetid: c6f64f5e-be65-485b-8831-e377535bd335
title: ICEM04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2ef993690ae690e0651db1538196998c4dd28c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356829"
---
# <a name="icem04"></a><span data-ttu-id="45d89-104">ICEM04</span><span class="sxs-lookup"><span data-stu-id="45d89-104">ICEM04</span></span>

<span data-ttu-id="45d89-105">ICEM04 überprüft, ob die erforderlichen leeren Tabellen des Mergemoduls leer sind.</span><span class="sxs-lookup"><span data-stu-id="45d89-105">ICEM04 verifies that the merge module's required empty tables are empty.</span></span> <span data-ttu-id="45d89-106">Fehler beim Beheben eines Fehlers, der dazu führt, dass ICEM04 Berichte zu einer falschen Zusammenführung des Mergemoduls führen können.</span><span class="sxs-lookup"><span data-stu-id="45d89-106">Failure to fix an error that ICEM04 reports can result in incorrect merging of the merge module.</span></span>

## <a name="result"></a><span data-ttu-id="45d89-107">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="45d89-107">Result</span></span>

<span data-ttu-id="45d89-108">ICEM04 gibt einen Fehler aus, wenn die erforderlichen leeren Tabellen des Mergemoduls nicht leer sind.</span><span class="sxs-lookup"><span data-stu-id="45d89-108">ICEM04 posts an error when the merge module's required empty tables are not empty.</span></span>

## <a name="example"></a><span data-ttu-id="45d89-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="45d89-109">Example</span></span>

<span data-ttu-id="45d89-110">ICEM04 gibt die folgenden Fehlermeldungen für ein Modul aus, das die angezeigten Datenbankeinträge enthält.</span><span class="sxs-lookup"><span data-stu-id="45d89-110">ICEM04 posts the following error messages for a module that contains the database entries shown.</span></span>

``` syntax
An empty FeatureComponents table is required in a Merge Module.

The Merge Module contains the 'ModuleInstallExecuteSequence' table. It 
must therefore have an empty 'InstallExecuteSequence' table.

Action 'CostInitialize' found in the AdvtExecuteSequence table. This 
table must be empty in a Merge Module
```

<span data-ttu-id="45d89-111">In der folgenden Tabelle wird eine partielle [AdvtExecuteSequence-Tabelle](advtexecutesequence-table.md)gezeigt.</span><span class="sxs-lookup"><span data-stu-id="45d89-111">The following table shows you a partial [AdvtExecuteSequence Table](advtexecutesequence-table.md).</span></span>



| <span data-ttu-id="45d89-112">Aktion</span><span class="sxs-lookup"><span data-stu-id="45d89-112">Action</span></span>         | <span data-ttu-id="45d89-113">Sequenz</span><span class="sxs-lookup"><span data-stu-id="45d89-113">Sequence</span></span> |
|----------------|----------|
| <span data-ttu-id="45d89-114">Costinitialize</span><span class="sxs-lookup"><span data-stu-id="45d89-114">CostInitialize</span></span> | <span data-ttu-id="45d89-115">1</span><span class="sxs-lookup"><span data-stu-id="45d89-115">1</span></span>        |



 

<span data-ttu-id="45d89-116">Die folgende Liste zeigt den partiellen Inhalt von Mergemodule:</span><span class="sxs-lookup"><span data-stu-id="45d89-116">The following list shows you the partial contents of MergeModule:</span></span>

-   <span data-ttu-id="45d89-117">Moduleinstallexecutesequence</span><span class="sxs-lookup"><span data-stu-id="45d89-117">ModuleInstallExecuteSequence</span></span>
-   <span data-ttu-id="45d89-118">Moduleadvtexecutesequence</span><span class="sxs-lookup"><span data-stu-id="45d89-118">ModuleAdvtExecuteSequence</span></span>
-   <span data-ttu-id="45d89-119">InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="45d89-119">InstallUISequence</span></span>

<span data-ttu-id="45d89-120">Das folgende Beispiel zeigt einen anderen möglichen Fehler.</span><span class="sxs-lookup"><span data-stu-id="45d89-120">The following example shows you another possible error.</span></span>

``` syntax
Feature-Component '[1].[2]' found in the FeatureComponents table. The 
FeatureComponents table must be empty in a Merge Module.
```

<span data-ttu-id="45d89-121">Wenn ein Mergemodul eine Modul Sequenz Tabelle enthält, muss es die entsprechende leere Sequenz Tabelle enthalten, unabhängig davon, ob die Modul Sequenz Tabelle leer ist.</span><span class="sxs-lookup"><span data-stu-id="45d89-121">If a merge module contains a module sequence table, it must contain the corresponding empty sequence table, whether or not the module sequence table is empty.</span></span> <span data-ttu-id="45d89-122">Wenn das Mergemodul z. b. die [moduleadminexecutesequence-Tabelle](moduleadminexecutesequence-table.md)enthält, muss es auch eine leere AdminExecuteSequence-Tabelle enthalten.</span><span class="sxs-lookup"><span data-stu-id="45d89-122">For example, if the merge module contains the [ModuleAdminExecuteSequence Table](moduleadminexecutesequence-table.md), it must also contain an empty AdminExecuteSequence table.</span></span>

<span data-ttu-id="45d89-123">Die [FeatureComponents-Tabelle](featurecomponents-table.md) ist in allen Mergemodulen erforderlich und muss leer sein.</span><span class="sxs-lookup"><span data-stu-id="45d89-123">The [FeatureComponents Table](featurecomponents-table.md) is required in all merge modules and must be empty.</span></span>

<span data-ttu-id="45d89-124">Im folgenden Verfahren wird gezeigt, wie Sie Fehler beheben.</span><span class="sxs-lookup"><span data-stu-id="45d89-124">The following procedure shows you how to fix errors.</span></span>

<span data-ttu-id="45d89-125">**So beheben Sie die Fehler**</span><span class="sxs-lookup"><span data-stu-id="45d89-125">**To fix errors**</span></span>

1.  <span data-ttu-id="45d89-126">Fügen Sie dem Mergemodul eine leere [FeatureComponents-Tabelle](featurecomponents-table.md) hinzu.</span><span class="sxs-lookup"><span data-stu-id="45d89-126">Add an empty [FeatureComponents Table](featurecomponents-table.md) to the merge module.</span></span>
2.  <span data-ttu-id="45d89-127">Fügen Sie dem Mergemodul eine leere [InstallExecuteSequence-Tabelle](installexecutesequence-table.md) hinzu.</span><span class="sxs-lookup"><span data-stu-id="45d89-127">Add an empty [InstallExecuteSequence Table](installexecutesequence-table.md) to the merge module.</span></span>
3.  <span data-ttu-id="45d89-128">Entfernen Sie die Aktion "costinitialize" aus der [Tabelle "AdvtExecuteSequence](advtexecutesequence-table.md)".</span><span class="sxs-lookup"><span data-stu-id="45d89-128">Remove the 'CostInitialize' action from the [AdvtExecuteSequence Table](advtexecutesequence-table.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="45d89-129">Diese Tabelle muss in einem Mergemodul leer sein.</span><span class="sxs-lookup"><span data-stu-id="45d89-129">This table must be empty in a merge module.</span></span> <span data-ttu-id="45d89-130">Aktionen sollten nur in der Tabelle "moduleadvtexecutesequence" angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="45d89-130">Actions should only appear in the ModuleAdvtExecuteSequence table.</span></span>

     

## <a name="tables-used-during-execution"></a><span data-ttu-id="45d89-131">Während der Ausführung verwendete Tabellen</span><span class="sxs-lookup"><span data-stu-id="45d89-131">Tables Used During Execution</span></span>

<span data-ttu-id="45d89-132">In der folgenden Liste sind die Tabellen aufgeführt, die während der Ausführung verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="45d89-132">The following list identifies the tables that are used during execution:</span></span>

-   [<span data-ttu-id="45d89-133">FeatureComponents-Tabelle</span><span class="sxs-lookup"><span data-stu-id="45d89-133">FeatureComponents Table</span></span>](featurecomponents-table.md)
-   <span data-ttu-id="45d89-134">Modul \* Sequenz Tabellen und entsprechende \* Sequenz Tabellen.</span><span class="sxs-lookup"><span data-stu-id="45d89-134">Module\*Sequence tables and corresponding \*Sequence tables.</span></span>

## <a name="related-topics"></a><span data-ttu-id="45d89-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="45d89-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45d89-136">Informationen zu Mergemodulen</span><span class="sxs-lookup"><span data-stu-id="45d89-136">About Merge Modules</span></span>](about-merge-modules.md)
</dt> <dt>

[<span data-ttu-id="45d89-137">Eisverweis für Mergemodul</span><span class="sxs-lookup"><span data-stu-id="45d89-137">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



