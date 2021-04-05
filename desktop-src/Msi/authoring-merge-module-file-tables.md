---
description: Eine Dateitabelle ist in jedem Mergemodul erforderlich und sollte über einen Datensatz für jede Datei verfügen, die vom Mergemodul an das Ziel Installationspaket übermittelt wird.
ms.assetid: 436933c7-6e5d-4b4e-9147-c60a26871dbe
title: Erstellen von Mergemodul-Datei Tabellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e2687ed69c1a0362f96db896a5fdf4237ac4681
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042154"
---
# <a name="authoring-merge-module-file-tables"></a><span data-ttu-id="2b3f3-103">Erstellen von Mergemodul-Datei Tabellen</span><span class="sxs-lookup"><span data-stu-id="2b3f3-103">Authoring Merge Module File Tables</span></span>

<span data-ttu-id="2b3f3-104">Eine [Dateitabelle](file-table.md) ist in jedem Mergemodul erforderlich und sollte über einen Datensatz für jede Datei verfügen, die vom Mergemodul an das Ziel Installationspaket übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="2b3f3-104">A [File Table](file-table.md) is required in every merge module, and should have a record for each file that is being delivered to the target installation package by the merge module.</span></span> <span data-ttu-id="2b3f3-105">Wenn das Mergemodul in eine MSI-Datei zusammengeführt wird, wird jede Datei in der Dateitabelle des Mergemoduls in einer CAB- [*Datei*](c-gly.md) in der MSM-Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="2b3f3-105">When the merge module is merged into a .msi file, every file in the merge module File Table is stored inside a [*cabinet file*](c-gly.md) in the .msm file.</span></span> <span data-ttu-id="2b3f3-106">Der Name der CAB-Module in einem Mergemodul lautet immer wie folgt: MergeModule.CABinet.</span><span class="sxs-lookup"><span data-stu-id="2b3f3-106">The name of the cabinet in a merge module is always the following: MergeModule.CABinet.</span></span>

<span data-ttu-id="2b3f3-107">Weitere Informationen finden Sie unter [Erstellen von MergeModule.CABinet](generating-mergemodule-cabinet-cabinet-files.md)-CAB-Dateien.</span><span class="sxs-lookup"><span data-stu-id="2b3f3-107">For more information, see [Generating MergeModule.CABinet Cabinet Files](generating-mergemodule-cabinet-cabinet-files.md).</span></span>

-   <span data-ttu-id="2b3f3-108">Da die Dateien eines Mergemoduls immer in einer CAB-Datei gespeichert werden, ist es nicht erforderlich, die Bitflags **msidbfileattributesnoncompressed** oder **msidbfileattributescompressed** in der Spalte Attribute der [Dateitabelle](file-table.md)festzulegen.</span><span class="sxs-lookup"><span data-stu-id="2b3f3-108">Because the files of a merge module are always stored inside a cabinet file, it is not necessary to set the **msidbFileAttributesNoncompressed** or **msidbFileAttributesCompressed** bit flags in the Attributes column of the [File Table](file-table.md).</span></span>
-   <span data-ttu-id="2b3f3-109">Die Namen der Dateien in MergeModule.CABinet müssen mit dem Primärschlüssel in der [Dateitabelle](file-table.md)des Mergemoduls identisch sein.</span><span class="sxs-lookup"><span data-stu-id="2b3f3-109">The names of files in MergeModule.CABinet must match the primary key in the merge module's [File Table](file-table.md).</span></span>

    <span data-ttu-id="2b3f3-110">Die Datei Spalte ist der Primärschlüssel der [Dateitabelle](file-table.md) , und die Einträge in diesem Feld müssen der Konvention folgen, die unter [Benennen von primär Schlüsseln in mergemoduldatenbanken](naming-primary-keys-in-merge-module-databases.md)beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="2b3f3-110">The File column is the primary key of the [File Table](file-table.md) and the entries in this field must follow the convention that is described in [Naming Primary Keys in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md).</span></span>

-   <span data-ttu-id="2b3f3-111">Datei Sequenznummern werden in der Sequence-Spalte der [File-Tabelle](file-table.md)angegeben.</span><span class="sxs-lookup"><span data-stu-id="2b3f3-111">File sequence numbers are specified in the Sequence column of the [File Table](file-table.md).</span></span>

    <span data-ttu-id="2b3f3-112">Dateien müssen in der [Dateitabelle](file-table.md) des Merge-Moduls in derselben Reihenfolge aufgelistet werden, in der Sie in MergeModule.CABinet gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="2b3f3-112">Files must be listed in the merge module's [File Table](file-table.md) in the same sequence that they are stored in MergeModule.CABinet.</span></span> <span data-ttu-id="2b3f3-113">Die Sequenznummern von Dateien müssen nicht aufeinander folgen, aber Sie müssen derselben Reihenfolge wie die Dateien entsprechen, die in der CAB-Datei gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="2b3f3-113">The sequence numbers of files do not need to be consecutive, but they must follow the same sequence as the files that are stored inside the cabinet.</span></span> <span data-ttu-id="2b3f3-114">Beispielsweise können die ersten, zweiten und dritten Dateien, die in der CAB-Datei gespeichert sind, über die Sequenznummer 100, 200 und 300 verfügen.</span><span class="sxs-lookup"><span data-stu-id="2b3f3-114">For example, the first, second, and third files stored in the cabinet can have the sequence numbers 100, 200, and 300.</span></span>

-   <span data-ttu-id="2b3f3-115">Das Installationsprogramm überspringt zusätzliche Dateien, die in MergeModule.CABinet enthalten sind und nicht in der [Dateitabelle](file-table.md)aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="2b3f3-115">The Installer skips extra files included in MergeModule.CABinet that are not listed in the [File Table](file-table.md).</span></span>

    <span data-ttu-id="2b3f3-116">Eine CAB-Datei kann alle Dateien enthalten, die für ein Mergemodul erforderlich sind, das mehrere Sprachen mithilfe von Transformationen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2b3f3-116">One cabinet file can contain all the files necessary for a merge module that supports multiple languages using transforms.</span></span> <span data-ttu-id="2b3f3-117">Allen Sprachdateien kann eine eindeutige Sequenznummer in der CAB-Datei zugewiesen werden, und dann kann eine Transformation Dateien hinzufügen oder aus der [Dateitabelle](file-table.md) entfernen, wenn dies für eine bestimmte Sprache erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="2b3f3-117">All the language files can be given a unique sequence number in the cabinet, and then a transform can add or remove files from the [File Table](file-table.md) when needed for a specific language.</span></span> <span data-ttu-id="2b3f3-118">Weitere Informationen finden Sie unter [Erstellen mehrerer sprachmergemodule](authoring-multiple-language-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="2b3f3-118">For more information, see [Authoring Multiple Language Merge Modules](authoring-multiple-language-merge-modules.md).</span></span>

<span data-ttu-id="2b3f3-119">Weitere Informationen finden Sie unter [File Table](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="2b3f3-119">For more information, see [File Table](file-table.md).</span></span>

 

 



