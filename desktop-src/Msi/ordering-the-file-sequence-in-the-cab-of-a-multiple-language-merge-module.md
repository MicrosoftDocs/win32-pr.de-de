---
description: Mergemodule, sprach Transformationen und CAB-Dateien mit mehreren Sprachen müssen so verfasst werden, dass die Reihenfolge der Dateien mit der in der Dateitabelle angegebenen Reihenfolge übereinstimmt.
ms.assetid: c6ddf5fc-a7c5-49c1-899b-ff9fdff9c028
title: Anordnen der Datei Sequenz im CAB eines Moduls mit mehreren Sprachen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01bdd00d8b09c0605b7ddcf656d87d41e3f53776
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218529"
---
# <a name="ordering-the-file-sequence-in-the-cab-of-a-multiple-language-merge-module"></a><span data-ttu-id="e5e5a-103">Anordnen der Datei Sequenz im CAB eines Moduls mit mehreren Sprachen</span><span class="sxs-lookup"><span data-stu-id="e5e5a-103">Ordering the File Sequence in the CAB of a Multiple Language Merge Module</span></span>

<span data-ttu-id="e5e5a-104">Mergemodule, sprach Transformationen und CAB-Dateien mit mehreren Sprachen müssen so verfasst werden, dass die Reihenfolge der Dateien in der CAB-Datei mit der Installations Reihenfolge der in der [Dateitabelle](file-table.md)angegebenen Dateien übereinstimmt, auch nach der Anwendung der sprach Transformation.</span><span class="sxs-lookup"><span data-stu-id="e5e5a-104">Multiple-language merge modules, language transforms, and cabinet files must be authored such that the order of the files in the .cab matches the installation order of files specified in the [File Table](file-table.md), even after the application of the language transform.</span></span> <span data-ttu-id="e5e5a-105">Wenn die Reihenfolge im Modul und im CAB nicht stimmt, kann das Mergemodul nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e5e5a-105">If the order in the module and in the .cab do not match, the merge module cannot be used.</span></span>

<span data-ttu-id="e5e5a-106">Weisen Sie jeder Datei im Modul eine eindeutige Sequenznummer zu, die unabhängig von Ihrer Sprache ist, und verwenden Sie dann immer diese Sequenznummer für die Datei.</span><span class="sxs-lookup"><span data-stu-id="e5e5a-106">Assign to each file in the module, a unique sequence number that is independent of its language, and then always use that sequence number for the file.</span></span> <span data-ttu-id="e5e5a-107">Verwenden Sie dieselbe Sequenz, wenn Sie die CAB-Datei erstellen und eine sprach Transformation erstellen.</span><span class="sxs-lookup"><span data-stu-id="e5e5a-107">Use the same sequence when building the cabinet file and authoring a language transform.</span></span>

<span data-ttu-id="e5e5a-108">Da das Installationsprogramm nur die Dateien installiert, die in der [Dateitabelle](file-table.md)aufgeführt sind, ermöglicht die Verwendung einer globalen Datei Sequenz in CAB, [File Table](file-table.md)und Language Transform dem Merge-Tool das Überspringen zusätzlicher Dateien, die in der CAB-Datei gespeichert sind, die nicht in der [Dateitabelle](file-table.md)aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="e5e5a-108">Because the Installer only installs the files listed in the [File Table](file-table.md), the use of a global file sequence in the cabinet, [File Table](file-table.md), and language transform enables the merge tool to skip any extra files stored in the cabinet that are not listed in the [File Table](file-table.md).</span></span> <span data-ttu-id="e5e5a-109">Möglicherweise sind andere Dateien in der CAB-Datei vorhanden, Sie dürfen jedoch nicht in der [Dateitabelle](file-table.md)aufgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e5e5a-109">Other files may exist in the cabinet, but they must not be listed in the [File Table](file-table.md).</span></span> <span data-ttu-id="e5e5a-110">Ein Modul, das Code.dll, English. dat, Deutsch. dat und Französisch. dat installiert, kann beispielsweise die folgende globale Datei Sequenz Reihenfolge verwenden.</span><span class="sxs-lookup"><span data-stu-id="e5e5a-110">For example, a module installing Code.dll, English.dat, German.dat, and French.dat can use the following global file sequence order.</span></span>



| <span data-ttu-id="e5e5a-111">File</span><span class="sxs-lookup"><span data-stu-id="e5e5a-111">File</span></span>        | <span data-ttu-id="e5e5a-112">Sequenz</span><span class="sxs-lookup"><span data-stu-id="e5e5a-112">Sequence</span></span> |
|-------------|----------|
| <span data-ttu-id="e5e5a-113">Code.Dll</span><span class="sxs-lookup"><span data-stu-id="e5e5a-113">Code.Dll</span></span>    | <span data-ttu-id="e5e5a-114">1</span><span class="sxs-lookup"><span data-stu-id="e5e5a-114">1</span></span>        |
| <span data-ttu-id="e5e5a-115">Englisch. dat</span><span class="sxs-lookup"><span data-stu-id="e5e5a-115">English.Dat</span></span> | <span data-ttu-id="e5e5a-116">2</span><span class="sxs-lookup"><span data-stu-id="e5e5a-116">2</span></span>        |
| <span data-ttu-id="e5e5a-117">Deutsch. dat</span><span class="sxs-lookup"><span data-stu-id="e5e5a-117">German.Dat</span></span>  | <span data-ttu-id="e5e5a-118">3</span><span class="sxs-lookup"><span data-stu-id="e5e5a-118">3</span></span>        |
| <span data-ttu-id="e5e5a-119">Französisch. dat</span><span class="sxs-lookup"><span data-stu-id="e5e5a-119">French.Dat</span></span>  | <span data-ttu-id="e5e5a-120">4</span><span class="sxs-lookup"><span data-stu-id="e5e5a-120">4</span></span>        |



 

<span data-ttu-id="e5e5a-121">Sprach Transformationen können dann erstellt werden, um die [Dateitabelle](file-table.md) des Moduls für Englisch, Deutsch oder Französisch zu ändern.</span><span class="sxs-lookup"><span data-stu-id="e5e5a-121">Language transforms can then be authored to modify the [File Table](file-table.md) of the module for English, German, or French.</span></span>

<span data-ttu-id="e5e5a-122">[Dateitabelle](file-table.md) (partiell für Englisch)</span><span class="sxs-lookup"><span data-stu-id="e5e5a-122">[File Table](file-table.md) (partial for English)</span></span>



| <span data-ttu-id="e5e5a-123">File</span><span class="sxs-lookup"><span data-stu-id="e5e5a-123">File</span></span>        | <span data-ttu-id="e5e5a-124">Sequenz</span><span class="sxs-lookup"><span data-stu-id="e5e5a-124">Sequence</span></span> |
|-------------|----------|
| <span data-ttu-id="e5e5a-125">Code.Dll</span><span class="sxs-lookup"><span data-stu-id="e5e5a-125">Code.Dll</span></span>    | <span data-ttu-id="e5e5a-126">1</span><span class="sxs-lookup"><span data-stu-id="e5e5a-126">1</span></span>        |
| <span data-ttu-id="e5e5a-127">Englisch. dat</span><span class="sxs-lookup"><span data-stu-id="e5e5a-127">English.Dat</span></span> | <span data-ttu-id="e5e5a-128">2</span><span class="sxs-lookup"><span data-stu-id="e5e5a-128">2</span></span>        |



 

<span data-ttu-id="e5e5a-129">[Dateitabelle](file-table.md) (partiell für Deutsch)</span><span class="sxs-lookup"><span data-stu-id="e5e5a-129">[File Table](file-table.md) (partial for German)</span></span>



| <span data-ttu-id="e5e5a-130">File</span><span class="sxs-lookup"><span data-stu-id="e5e5a-130">File</span></span>       | <span data-ttu-id="e5e5a-131">Sequenz</span><span class="sxs-lookup"><span data-stu-id="e5e5a-131">Sequence</span></span> |
|------------|----------|
| <span data-ttu-id="e5e5a-132">Code.Dll</span><span class="sxs-lookup"><span data-stu-id="e5e5a-132">Code.Dll</span></span>   | <span data-ttu-id="e5e5a-133">1</span><span class="sxs-lookup"><span data-stu-id="e5e5a-133">1</span></span>        |
| <span data-ttu-id="e5e5a-134">Deutsch. dat</span><span class="sxs-lookup"><span data-stu-id="e5e5a-134">German.Dat</span></span> | <span data-ttu-id="e5e5a-135">3</span><span class="sxs-lookup"><span data-stu-id="e5e5a-135">3</span></span>        |



 

<span data-ttu-id="e5e5a-136">[Dateitabelle](file-table.md) (teilweise für Französisch)</span><span class="sxs-lookup"><span data-stu-id="e5e5a-136">[File Table](file-table.md) (partial for French)</span></span>



| <span data-ttu-id="e5e5a-137">File</span><span class="sxs-lookup"><span data-stu-id="e5e5a-137">File</span></span>       | <span data-ttu-id="e5e5a-138">Sequenz</span><span class="sxs-lookup"><span data-stu-id="e5e5a-138">Sequence</span></span> |
|------------|----------|
| <span data-ttu-id="e5e5a-139">Code.Dll</span><span class="sxs-lookup"><span data-stu-id="e5e5a-139">Code.Dll</span></span>   | <span data-ttu-id="e5e5a-140">1</span><span class="sxs-lookup"><span data-stu-id="e5e5a-140">1</span></span>        |
| <span data-ttu-id="e5e5a-141">Französisch. dat</span><span class="sxs-lookup"><span data-stu-id="e5e5a-141">French.Dat</span></span> | <span data-ttu-id="e5e5a-142">4</span><span class="sxs-lookup"><span data-stu-id="e5e5a-142">4</span></span>        |



 

<span data-ttu-id="e5e5a-143">Weitere Informationen finden Sie unter [Erstellen einer sprach Transformation für ein Mergemodul mehrerer Sprachen](authoring-a-language-transform-for-a-multiple-language-merge-module.md) und [Erstellen von Mergemodul-Datei Tabellen](authoring-merge-module-file-tables.md).</span><span class="sxs-lookup"><span data-stu-id="e5e5a-143">For more information, see [Authoring a Language Transform for a Multiple Language Merge Module](authoring-a-language-transform-for-a-multiple-language-merge-module.md) and [Authoring Merge Module File Tables](authoring-merge-module-file-tables.md).</span></span>

 

 



