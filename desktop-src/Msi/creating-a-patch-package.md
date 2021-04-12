---
description: Entwickler erstellen ein Patchpaket, indem Sie eine Datei für die Patcherstellung erzeugen und Msimsp.exe verwenden, um die uikreatepatchpackageex-Funktion in Patchwiz.dll aufzurufen.
ms.assetid: 8a163653-6ba1-46ea-9832-f998749d29ae
title: Erstellen eines Patchpakets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2561cb6729dc7b4e0e48acd13b6338f08a8ba943
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216379"
---
# <a name="creating-a-patch-package"></a><span data-ttu-id="3d037-103">Erstellen eines Patchpakets</span><span class="sxs-lookup"><span data-stu-id="3d037-103">Creating a Patch Package</span></span>

<span data-ttu-id="3d037-104">Entwickler erstellen ein Patchpaket, indem Sie eine Datei für die Patcherstellung erzeugen und [Msimsp.exe](msimsp-exe.md) verwenden, um die [uikreatepatchpackageex](uicreatepatchpackageex--patchwiz-dll-.md) -Funktion in [Patchwiz.dll](patchwiz-dll.md)aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="3d037-104">Developers create a patch package by generating a patch creation file and using [Msimsp.exe](msimsp-exe.md) to call the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function in [Patchwiz.dll](patchwiz-dll.md).</span></span> <span data-ttu-id="3d037-105">Msimsp.exe und Patchwiz.dll werden im Windows Installer SDK bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="3d037-105">Msimsp.exe and Patchwiz.dll are provided in the Windows Installer SDK.</span></span> <span data-ttu-id="3d037-106">Weitere Informationen finden Sie unter [Beispiel für ein kleines Update-Patching](a-small-update-patching-example.md).</span><span class="sxs-lookup"><span data-stu-id="3d037-106">For more information, see [A Small Update Patching Example](a-small-update-patching-example.md).</span></span>

<span data-ttu-id="3d037-107">Da die Anwendung eines Patches für ein Windows Installer Paket zur Installation der ursprünglichen Quellen mit einer neuen MSI-Datei führt, muss die neue MSI-Datei mit dem Layout der ursprünglichen Quelle kompatibel bleiben.</span><span class="sxs-lookup"><span data-stu-id="3d037-107">Because the application of a patch to a Windows Installer package results in the installation of the original sources using a new .msi file, the new .msi file must remain compatible with the layout of the original source.</span></span>

<span data-ttu-id="3d037-108">Wenn Sie ein Patchpaket erstellen, müssen Sie ein nicht komprimiertes Setup Abbild verwenden, um einen Patch zu erstellen, z. b. ein administratives Image oder ein nicht komprimiertes Setup Abbild von einer CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="3d037-108">When you author a patch package you must use an uncompressed setup image to create a patch, for example, an administrative image or an uncompressed setup image from a CD-ROM.</span></span> <span data-ttu-id="3d037-109">Außerdem müssen Sie die folgenden Einschränkungen einhalten:</span><span class="sxs-lookup"><span data-stu-id="3d037-109">You must also adhere to the following restrictions:</span></span>

-   <span data-ttu-id="3d037-110">Verschieben Sie keine Dateien aus einem Ordner in einen anderen.</span><span class="sxs-lookup"><span data-stu-id="3d037-110">Do not move files from one folder to another.</span></span>
-   <span data-ttu-id="3d037-111">Verschieben Sie Dateien nicht aus einer CAB-Datei in eine andere.</span><span class="sxs-lookup"><span data-stu-id="3d037-111">Do not move files from one cabinet to another.</span></span>
-   <span data-ttu-id="3d037-112">Ändern Sie die Reihenfolge der Dateien in einer CAB-Datei nicht.</span><span class="sxs-lookup"><span data-stu-id="3d037-112">Do not change the order of files in a cabinet.</span></span>
-   <span data-ttu-id="3d037-113">Ändern Sie nicht die Sequenznummer vorhandener Dateien.</span><span class="sxs-lookup"><span data-stu-id="3d037-113">Do not change the sequence number of existing files.</span></span> <span data-ttu-id="3d037-114">Die Sequenznummer ist der Wert, der in der Sequence-Spalte der [File-Tabelle](file-table.md)angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="3d037-114">The sequence number is the value specified in the Sequence column of the [File Table](file-table.md).</span></span>
-   <span data-ttu-id="3d037-115">Alle neuen Dateien, die vom Patch hinzugefügt werden, müssen am Ende der vorhandenen Datei Sequenz abgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3d037-115">Any new files that are added by the patch must be placed at the end of the existing file sequence.</span></span> <span data-ttu-id="3d037-116">Die Sequenznummer einer neuen Datei im aktualisierten Image muss größer als die größte Sequenznummer vorhandener Dateien im Zielbild sein.</span><span class="sxs-lookup"><span data-stu-id="3d037-116">The sequence number of any new file in the upgraded image must be greater than the largest sequence number of existing files in the target image.</span></span>
-   <span data-ttu-id="3d037-117">Ändern Sie die Primärschlüssel in der [Dateitabelle](file-table.md) nicht zwischen den ursprünglichen und neuen MSI-Dateiversionen.</span><span class="sxs-lookup"><span data-stu-id="3d037-117">Do not change the primary keys in the [File Table](file-table.md) between the original and new .msi file versions.</span></span>
    > [!Note]  
    > <span data-ttu-id="3d037-118">Die Datei muss den gleichen Schlüssel in der [Dateitabelle](file-table.md) sowohl für das Ziel Image als auch für das aktualisierte Image aufweisen.</span><span class="sxs-lookup"><span data-stu-id="3d037-118">The file must have the same key in the [File Table](file-table.md) of both the target image and the updated image.</span></span> <span data-ttu-id="3d037-119">Die Zeichen folgen Werte in der Datei Spalte beider Tabellen müssen identisch sein, einschließlich der Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="3d037-119">The string values in the File column of both tables must be identical, including the case.</span></span>

     

-   <span data-ttu-id="3d037-120">Erstellen Sie kein Paket mit [Datei Tabellen](file-table.md) Schlüsseln, die sich nur in der Groß-/Kleinschreibung unterscheiden. vermeiden Sie z. b. das folgende Tabellen Beispiel.</span><span class="sxs-lookup"><span data-stu-id="3d037-120">Do not author a package with [File Table](file-table.md) keys that differ only in case, for example, avoid the following table example.</span></span>

    

    | <span data-ttu-id="3d037-121">File</span><span class="sxs-lookup"><span data-stu-id="3d037-121">File</span></span>       | <span data-ttu-id="3d037-122">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="3d037-122">Component\_</span></span> | <span data-ttu-id="3d037-123">FileName</span><span class="sxs-lookup"><span data-stu-id="3d037-123">FileName</span></span>   |
    |------------|-------------|------------|
    | <span data-ttu-id="3d037-124">ReadMe.txt</span><span class="sxs-lookup"><span data-stu-id="3d037-124">readme.txt</span></span> | <span data-ttu-id="3d037-125">Comp1</span><span class="sxs-lookup"><span data-stu-id="3d037-125">Comp1</span></span>       | <span data-ttu-id="3d037-126">ReadMe.txt</span><span class="sxs-lookup"><span data-stu-id="3d037-126">readme.txt</span></span> |
    | <span data-ttu-id="3d037-127">ReadMe.txt</span><span class="sxs-lookup"><span data-stu-id="3d037-127">ReadMe.txt</span></span> | <span data-ttu-id="3d037-128">Comp2</span><span class="sxs-lookup"><span data-stu-id="3d037-128">Comp2</span></span>       | <span data-ttu-id="3d037-129">ReadMe.txt</span><span class="sxs-lookup"><span data-stu-id="3d037-129">readme.txt</span></span> |

    

     

    <span data-ttu-id="3d037-130">Der Windows Installer kann das Beispiel der vorherigen Tabelle zulassen, wenn Comp1 und Comp2 in unterschiedlichen Verzeichnissen installiert sind. Sie können jedoch [Msimsp.exe](msimsp-exe.md) oder [Patchwiz.dll](patchwiz-dll.md) nicht verwenden, um einen Patch für das Paket zu generieren.</span><span class="sxs-lookup"><span data-stu-id="3d037-130">The Windows Installer can allow the previous table example when Comp1 and Comp2 are installed on different directories, but then you cannot use [Msimsp.exe](msimsp-exe.md) or [Patchwiz.dll](patchwiz-dll.md) to generate a patch for the package.</span></span> <span data-ttu-id="3d037-131">Msimsp.exe und Patchwiz.dll Makecab.exe aufgerufen, bei dem die Groß-und Kleinschreibung nicht beachtet wird.</span><span class="sxs-lookup"><span data-stu-id="3d037-131">Msimsp.exe and Patchwiz.dll call Makecab.exe, which is case-insensitive and fails.</span></span>

    <span data-ttu-id="3d037-132">Wenn Sie beim Setup Zusammenführungs Module verwenden, stellen Sie sicher, dass die oben aufgeführten Richtlinien von Datei Sequenznummern und-Layout befolgt werden.</span><span class="sxs-lookup"><span data-stu-id="3d037-132">When using merge modules in the setup, ensure that file sequence numbers and layout adhere to the above guidelines.</span></span>

 

 



