---
description: Während einer Windows Installer Installation kann das Installationsprogramm nach einem Verzeichnis und einer Datei in diesem Verzeichnis suchen.
ms.assetid: ddf624f9-6f85-4ef6-8dfc-8635a25915d0
title: Suchen nach einem Verzeichnis und einer Datei im Verzeichnis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b4821a53ef0c3f063e943f1f5821b043791dd44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348681"
---
# <a name="searching-for-a-directory-and-a-file-in-the-directory"></a><span data-ttu-id="1bd7b-103">Suchen nach einem Verzeichnis und einer Datei im Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="1bd7b-103">Searching for a Directory and a File in the Directory</span></span>

<span data-ttu-id="1bd7b-104">**So suchen Sie nach einem Verzeichnis und dann nach einer Datei in diesem Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="1bd7b-104">**To search for a directory and then a file in that directory**</span></span>

1.  <span data-ttu-id="1bd7b-105">Suchen Sie zuerst nach dem Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="1bd7b-105">First search for the directory.</span></span>

    <span data-ttu-id="1bd7b-106">Appdir muss als gültige Signatur des Verzeichnisses definiert werden.</span><span class="sxs-lookup"><span data-stu-id="1bd7b-106">AppDir must be defined as the valid signature of the directory.</span></span> <span data-ttu-id="1bd7b-107">Wenn appdir nicht als gültige Signatur definiert ist, hat AppSearch keinen Ort, um die Datei zu finden. wenn die Suche z. b. für c: \\ mydir \\MyApp.exe ist, muss appdir als c: \\ mydir definiert werden.</span><span class="sxs-lookup"><span data-stu-id="1bd7b-107">If AppDir is not defined as a valid signature, AppSearch does not have a place to find the file, for example, if the search is for c:\\MyDir\\MyApp.exe, AppDir should be defined as c:\\MyDir.</span></span> <span data-ttu-id="1bd7b-108">Appdir kann durch Einschließen eines Datensatzes in der [drlocator-Tabelle](drlocator-table.md)oder einer anderen Methode definiert werden.</span><span class="sxs-lookup"><span data-stu-id="1bd7b-108">AppDir might be defined by including a record in the [DrLocator Table](drlocator-table.md), or by some other method.</span></span> <span data-ttu-id="1bd7b-109">In der [Signatur Tabelle](signature-table.md) für die Verzeichnis Suche ist kein Datensatz enthalten.</span><span class="sxs-lookup"><span data-stu-id="1bd7b-109">No record is included in the [Signature Table](signature-table.md) for the directory search.</span></span> <span data-ttu-id="1bd7b-110">Listen Sie die Datei Signatur und den Namen der Dateisuche in der Signatur Tabelle auf.</span><span class="sxs-lookup"><span data-stu-id="1bd7b-110">For the file search, list the file signature and name in the Signature Table.</span></span> <span data-ttu-id="1bd7b-111">Die verbleibenden Felder in diesem Datensatz können NULL sein, um nach einer beliebigen Version von MyApp.exe zu suchen.</span><span class="sxs-lookup"><span data-stu-id="1bd7b-111">The remaining fields in this record can be null to search for any version of MyApp.exe.</span></span>

    <span data-ttu-id="1bd7b-112">[Signatur Tabelle](signature-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="1bd7b-112">[Signature Table](signature-table.md) (partial)</span></span>

    

    | <span data-ttu-id="1bd7b-113">Signatur</span><span class="sxs-lookup"><span data-stu-id="1bd7b-113">Signature</span></span>          | <span data-ttu-id="1bd7b-114">Dateiname</span><span class="sxs-lookup"><span data-stu-id="1bd7b-114">File Name</span></span>            |
    |--------------------|----------------------|
    | <span data-ttu-id="1bd7b-115">Appfile</span><span class="sxs-lookup"><span data-stu-id="1bd7b-115">AppFile</span></span><br/> | <span data-ttu-id="1bd7b-116">MyApp.exe</span><span class="sxs-lookup"><span data-stu-id="1bd7b-116">MyApp.exe</span></span><br/> |

    

     

2.  <span data-ttu-id="1bd7b-117">Verwenden Sie die [AppSearch-Tabelle](appsearch-table.md).</span><span class="sxs-lookup"><span data-stu-id="1bd7b-117">Use the [AppSearch Table](appsearch-table.md).</span></span>

    <span data-ttu-id="1bd7b-118">Geben Sie die Eigenschaft ein, die vom Installationsprogramm festgelegt werden soll, wenn das Verzeichnis mit der Signatur appdir installiert ist.</span><span class="sxs-lookup"><span data-stu-id="1bd7b-118">Enter the property that the Installer is to set if the directory with the signature AppDir is installed.</span></span> <span data-ttu-id="1bd7b-119">Wenn das Installationsprogramm feststellt, dass dieses Verzeichnis installiert ist, wird mydir auf den Verzeichnispfad festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1bd7b-119">If the Installer finds this directory is installed, it sets MYDIR to the directory path.</span></span> <span data-ttu-id="1bd7b-120">Geben Sie die Eigenschaft ein, die vom Installationsprogramm festgelegt werden soll, wenn MyApp.exe installiert ist.</span><span class="sxs-lookup"><span data-stu-id="1bd7b-120">Enter the property that the Installer is to set if MyApp.exe is installed.</span></span>

    <span data-ttu-id="1bd7b-121">[AppSearch-Tabelle](appsearch-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="1bd7b-121">[AppSearch Table](appsearch-table.md) (partial)</span></span>

    

    | <span data-ttu-id="1bd7b-122">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1bd7b-122">Property</span></span>         | <span data-ttu-id="1bd7b-123">Signatur</span><span class="sxs-lookup"><span data-stu-id="1bd7b-123">Signature</span></span>          |
    |------------------|--------------------|
    | <span data-ttu-id="1bd7b-124">"MyDir"</span><span class="sxs-lookup"><span data-stu-id="1bd7b-124">MYDIR</span></span><br/> | <span data-ttu-id="1bd7b-125">AppDir</span><span class="sxs-lookup"><span data-stu-id="1bd7b-125">AppDir</span></span><br/>  |
    | <span data-ttu-id="1bd7b-126">MyApp</span><span class="sxs-lookup"><span data-stu-id="1bd7b-126">MYAPP</span></span><br/> | <span data-ttu-id="1bd7b-127">Appfile</span><span class="sxs-lookup"><span data-stu-id="1bd7b-127">AppFile</span></span><br/> |

    

     

3.  <span data-ttu-id="1bd7b-128">Verwenden Sie die [drlocator-Tabelle](drlocator-table.md).</span><span class="sxs-lookup"><span data-stu-id="1bd7b-128">Use the [DrLocator Table](drlocator-table.md).</span></span>

    <span data-ttu-id="1bd7b-129">Geben Sie in der übergeordneten Spalte die Signatur (appdir) ein, die als Pfad des Verzeichnisses definiert ist.</span><span class="sxs-lookup"><span data-stu-id="1bd7b-129">Enter in the Parent column the signature, AppDir, that is defined as the path of the directory.</span></span> <span data-ttu-id="1bd7b-130">Geben Sie in der Spalte Tiefe die Anzahl der Unterverzeichnis Ebenen an, die in diesem Verzeichnis durchsucht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1bd7b-130">Specify in the Depth column the number of subdirectory levels to search in this directory.</span></span> <span data-ttu-id="1bd7b-131">Appdir muss als Verzeichnis Signatur definiert werden.</span><span class="sxs-lookup"><span data-stu-id="1bd7b-131">AppDir must be defined as the directory signature.</span></span> <span data-ttu-id="1bd7b-132">Appdir kann durch Einschließen eines Datensatzes definiert werden, wie hier gezeigt, oder durch eine andere Methode.</span><span class="sxs-lookup"><span data-stu-id="1bd7b-132">AppDir may be defined by including a record as shown here or by another method.</span></span>

    [<span data-ttu-id="1bd7b-133">Drlocator-Tabelle</span><span class="sxs-lookup"><span data-stu-id="1bd7b-133">DrLocator Table</span></span>](drlocator-table.md)

    

    | <span data-ttu-id="1bd7b-134">Signatur</span><span class="sxs-lookup"><span data-stu-id="1bd7b-134">Signature</span></span> | <span data-ttu-id="1bd7b-135">Parent</span><span class="sxs-lookup"><span data-stu-id="1bd7b-135">Parent</span></span> | <span data-ttu-id="1bd7b-136">Pfad</span><span class="sxs-lookup"><span data-stu-id="1bd7b-136">Path</span></span>      | <span data-ttu-id="1bd7b-137">Tiefe</span><span class="sxs-lookup"><span data-stu-id="1bd7b-137">Depth</span></span> |
    |-----------|--------|-----------|-------|
    | <span data-ttu-id="1bd7b-138">AppDir</span><span class="sxs-lookup"><span data-stu-id="1bd7b-138">AppDir</span></span>    |        | <span data-ttu-id="1bd7b-139">C: \\ meindir</span><span class="sxs-lookup"><span data-stu-id="1bd7b-139">C:\\MyDir</span></span> | <span data-ttu-id="1bd7b-140">0</span><span class="sxs-lookup"><span data-stu-id="1bd7b-140">0</span></span>     |
    | <span data-ttu-id="1bd7b-141">Appfile</span><span class="sxs-lookup"><span data-stu-id="1bd7b-141">AppFile</span></span>   | <span data-ttu-id="1bd7b-142">AppDir</span><span class="sxs-lookup"><span data-stu-id="1bd7b-142">AppDir</span></span> |           | <span data-ttu-id="1bd7b-143">0</span><span class="sxs-lookup"><span data-stu-id="1bd7b-143">0</span></span>     |

    

     

4.  <span data-ttu-id="1bd7b-144">Fügen Sie die Aktion AppSearch in die Aktions Sequenz ein.</span><span class="sxs-lookup"><span data-stu-id="1bd7b-144">Include the AppSearch action in the action sequence.</span></span>

    <span data-ttu-id="1bd7b-145">Wenn MyApp.exe in appdir installiert wird, legt das Installationsprogramm die Eigenschaft MyApp auf den Speicherort der Datei fest.</span><span class="sxs-lookup"><span data-stu-id="1bd7b-145">If MyApp.exe is found to be installed in AppDir, the Installer sets the property MYAPP to the location of file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1bd7b-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1bd7b-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1bd7b-147">Suchen nach vorhandenen Anwendungen, Dateien, Registrierungs Einträgen oder INI-Datei Einträgen</span><span class="sxs-lookup"><span data-stu-id="1bd7b-147">Searching for Existing Applications, Files, Registry Entries or .ini File Entries</span></span>](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)
</dt> </dl>

 

 




