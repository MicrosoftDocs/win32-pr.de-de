---
description: Jede Datei, die vom Mergemodul an das Ziel Installationspaket übermittelt wird, muss in einer CAB-Datei gespeichert werden, die als Stream in der MSM-Datei eingebettet ist. Der Name dieses CAB ist immer MergeModule.CABinet.
ms.assetid: 884df249-977e-4e8e-8978-15331a7c1d8a
title: Erstellen von MergeModule.CABinet-CAB-Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a26eb9bb3daf92d81e21267b2f56706b74d9179
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360650"
---
# <a name="generating-mergemodulecabinet-cabinet-files"></a><span data-ttu-id="2b363-104">Erstellen von MergeModule.CABinet-CAB-Dateien</span><span class="sxs-lookup"><span data-stu-id="2b363-104">Generating MergeModule.CABinet Cabinet Files</span></span>

<span data-ttu-id="2b363-105">Jede Datei, die vom Mergemodul an das Ziel Installationspaket übermittelt wird, muss in einer CAB-Datei gespeichert werden, die als Stream in der MSM-Datei eingebettet ist.</span><span class="sxs-lookup"><span data-stu-id="2b363-105">Every file that is delivered to the target installation package by the merge module must be stored inside of a cabinet file embedded as a stream inside the .msm file.</span></span> <span data-ttu-id="2b363-106">Der Name dieses CAB ist immer MergeModule.CABinet.</span><span class="sxs-lookup"><span data-stu-id="2b363-106">The name of this cabinet is always MergeModule.CABinet.</span></span>

<span data-ttu-id="2b363-107">Die Namen der Dateien in MergeModule.CABinet müssen mit den primär Schlüsseln übereinstimmen, die in der [Dateitabelle](file-table.md) des Mergemoduls verwendet werden, und müssen der in [Benennen von primär Schlüsseln in mergemoduldatenbanken](naming-primary-keys-in-merge-module-databases.md)beschriebenen Konvention entsprechen.</span><span class="sxs-lookup"><span data-stu-id="2b363-107">The names of files in MergeModule.CABinet must match the primary keys used in the merge module's [File table](file-table.md) and must adhere to the convention described in [Naming Primary Keys in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md).</span></span>

<span data-ttu-id="2b363-108">Das Installationsprogramm überspringt zusätzliche Dateien, die in MergeModule.CABinet enthalten sind und nicht in der [Dateitabelle](file-table.md)des Mergemoduls aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="2b363-108">The installer skips extra files included in MergeModule.CABinet that are not listed in the merge module's [File table](file-table.md).</span></span> <span data-ttu-id="2b363-109">Die Sequenznummern von Dateien, die in der Dateitabelle angegeben sind, müssen nicht aufeinander folgen, aber Sie müssen derselben Reihenfolge wie die in MergeModule.CABinet gespeicherten Dateien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="2b363-109">The sequence numbers of files specified in the File table do not need to be consecutive, but they must follow the same sequence as the files stored inside MergeModule.CABinet.</span></span> <span data-ttu-id="2b363-110">Weitere Informationen finden Sie unter [Erstellen von Mergemodul-Datei Tabellen](authoring-merge-module-file-tables.md).</span><span class="sxs-lookup"><span data-stu-id="2b363-110">For more information, see [Authoring Merge Module File Tables](authoring-merge-module-file-tables.md).</span></span>

<span data-ttu-id="2b363-111">Dies bedeutet, dass eine einzelne CAB-Datei alle Dateien enthalten kann, die für ein Mergemodul erforderlich sind, um mehrere Sprachen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="2b363-111">This means that a single cabinet file can contain all the files needed for a merge module to support multiple languages.</span></span> <span data-ttu-id="2b363-112">Allen Sprachdateien können eindeutige Sequenznummern in der CAB-Datei zugewiesen werden. Anschließend kann eine sprach Transformation verwendet werden, um Dateien aus der Dateitabelle hinzuzufügen oder zu entfernen, um ein Mergemodul für eine bestimmte Sprache zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2b363-112">All the language files can be given unique sequence numbers in the cabinet and then a language transform can be used to add or remove files from the File table to obtain a merge module for a particular language.</span></span> <span data-ttu-id="2b363-113">Weitere Informationen finden Sie unter [Erstellen mehrerer sprachmergemodule](authoring-multiple-language-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="2b363-113">For details, see [Authoring Multiple Language Merge Modules](authoring-multiple-language-merge-modules.md).</span></span>

<span data-ttu-id="2b363-114">MergeModule.CABinet kann dem Mergemodul hinzugefügt werden, indem eine temporäre [ \_ Streams-Tabelle](-streams-table.md)geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="2b363-114">MergeModule.CABinet can be added to the merge module by opening a temporary [\_Streams Table](-streams-table.md).</span></span> <span data-ttu-id="2b363-115">Beispielsweise kann das mit dem Windows Installer SDK bereitgestellte Tool Msidb.exe verwendet werden, um dem Mergemodul den MergeModule.CABinet hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="2b363-115">For example, the tool Msidb.exe provided with the Windows Installer SDK can be used to add the MergeModule.CABinet to the merge module.</span></span> <span data-ttu-id="2b363-116">Weitere Informationen finden Sie unter [Einschließen einer CAB-Datei in eine-Installation](including-a-cabinet-file-in-an-installation.md).</span><span class="sxs-lookup"><span data-stu-id="2b363-116">For more information, see [Including a Cabinet File in an Installation](including-a-cabinet-file-in-an-installation.md).</span></span>

 

 



