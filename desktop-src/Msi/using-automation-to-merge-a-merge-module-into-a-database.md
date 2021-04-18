---
description: Mergemodule stellen eine Standardmethode für die Bereitstellung von freigegebenen Windows Installer Komponenten und die Einrichtung von Logik für Anwendungen bereit.
ms.assetid: 63ced106-12e3-4483-8bfe-22c54fe7a204
title: Verwenden von Automation zum Zusammenführen eines Mergemoduls zu einer Datenbank
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e28b8cfc1716cdbb296fd0a1410787ae55bb62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347252"
---
# <a name="using-automation-to-merge-a-merge-module-into-a-database"></a><span data-ttu-id="c8239-103">Verwenden von Automation zum Zusammenführen eines Mergemoduls zu einer Datenbank</span><span class="sxs-lookup"><span data-stu-id="c8239-103">Using Automation to Merge a Merge Module into a Database</span></span>

<span data-ttu-id="c8239-104">[Mergemodule](merge-modules.md) stellen eine Standardmethode für die Bereitstellung von freigegebenen Windows Installer [*Komponenten*](c-gly.md)und die Einrichtung von Logik für Anwendungen bereit.</span><span class="sxs-lookup"><span data-stu-id="c8239-104">[Merge Modules](merge-modules.md) provide a standard method for you to deliver shared Windows Installer [*components*](c-gly.md), and setup logic to applications.</span></span>

<span data-ttu-id="c8239-105">Mergemodule müssen mithilfe eines Merge-Tools in ein Installationspaket zusammengeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c8239-105">Merge modules must be merged into an installation package by using a merge tool.</span></span> <span data-ttu-id="c8239-106">Die bewährte Vorgehensweise besteht darin, ein frei verteiltes Mergetool zu erwerben oder eines der mergetools zu erwerben, die von unabhängigen Softwareanbietern verfügbar sind. Sie können z. b. [Mergemod.dll](merge-module-automation.md)verwenden.</span><span class="sxs-lookup"><span data-stu-id="c8239-106">The best practice is to obtain a freely distributed merge tool, or purchase one of the merge tools that are available from independent software vendors, for example, you can use [Mergemod.dll](merge-module-automation.md).</span></span>

<span data-ttu-id="c8239-107">Im folgenden Verfahren wird gezeigt, wie Sie ein Mergemodul in einer Windows Installer-Datenbank zusammenführen, indem Sie die [mergemodulautomatisierung](merge-module-automation.md)verwenden.</span><span class="sxs-lookup"><span data-stu-id="c8239-107">The following procedure shows you how to merge a merge module into a Windows Installer database by using [Merge Module Automation](merge-module-automation.md).</span></span>

<span data-ttu-id="c8239-108">**So führen Sie ein Modul in einer Datenbank zusammen**</span><span class="sxs-lookup"><span data-stu-id="c8239-108">**To merge a module into a database**</span></span>

1.  <span data-ttu-id="c8239-109">Öffnen Sie eine Protokolldatei, indem Sie die [**OpenLog**](merge-openlog.md) -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="c8239-109">Open a log file by using the [**OpenLog**](merge-openlog.md) method.</span></span>

    <span data-ttu-id="c8239-110">Dieser Schritt ist nur erforderlich, wenn Sie eine Protokolldatei erstellen oder eine vorhandene Protokolldatei für den Mergeprozess Anfügen müssen.</span><span class="sxs-lookup"><span data-stu-id="c8239-110">This step is required only if you need to create a log file, or append an existing log file for the merge process.</span></span>

2.  <span data-ttu-id="c8239-111">Öffnen Sie die [MSI](windows-installer-file-extensions.md) -Installations Datenbank, indem Sie die [**OpenDatabase**](merge-opendatabase.md) -Methode des [**Merge-Objekts**](merge-object.md)verwenden.</span><span class="sxs-lookup"><span data-stu-id="c8239-111">Open the [.msi](windows-installer-file-extensions.md) installation database by using the [**OpenDatabase**](merge-opendatabase.md) method of the [**Merge Object**](merge-object.md).</span></span>

    <span data-ttu-id="c8239-112">Dieser Schritt ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c8239-112">This step is required.</span></span>

    <span data-ttu-id="c8239-113">Die Datenbank, die Sie öffnen, ist die Datenbank, die Sie für das Mergemodul erhalten möchten.</span><span class="sxs-lookup"><span data-stu-id="c8239-113">The database that you open is the one that you want to receive the merge module.</span></span>

3.  <span data-ttu-id="c8239-114">Öffnen Sie das [MSM](windows-installer-file-extensions.md) -Mergemodul mithilfe der [**OpenModule**](merge-openmodule.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="c8239-114">Open the [.msm](windows-installer-file-extensions.md) merge module by using the [**OpenModule**](merge-openmodule.md) method.</span></span>

    <span data-ttu-id="c8239-115">Dieser Schritt ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c8239-115">This step is required.</span></span>

    <span data-ttu-id="c8239-116">Dies ist das Mergemodul, das in der Datenbank zusammengeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c8239-116">This is the merge module that is being merged into the database.</span></span> <span data-ttu-id="c8239-117">Ein Modul muss geöffnet werden, bevor es mit einer Installations Datenbank zusammengeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="c8239-117">A module must be opened before it can be merged with an installation database.</span></span>

4.  <span data-ttu-id="c8239-118">Führen Sie das Modul mit der [**Merge**](merge-object.md) -Methode oder der [**mergeex**](merge-mergeex.md) -Methode in der Installations Datenbank zusammen.</span><span class="sxs-lookup"><span data-stu-id="c8239-118">Merge the module into the installation database by calling the [**Merge**](merge-object.md) method or [**MergeEx**](merge-mergeex.md) method.</span></span>

    <span data-ttu-id="c8239-119">Dieser Schritt ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c8239-119">This step is required.</span></span>

    <span data-ttu-id="c8239-120">Die [**Merge**](merge-object.md) -Methode oder die [**mergeex**](merge-mergeex.md) -Methode kann nur einmal aufgerufen werden, um eine bestimmte Kombination aus [MSI](windows-installer-file-extensions.md) -und MSM-Dateien zusammenzuführen.</span><span class="sxs-lookup"><span data-stu-id="c8239-120">The [**Merge**](merge-object.md) method or [**MergeEx**](merge-mergeex.md) method can only be called one time to merge a specific combination of [.msi](windows-installer-file-extensions.md) and .msm files.</span></span>

    > [!Note]  
    > <span data-ttu-id="c8239-121">Die [**mergeex**](merge-mergeex.md) -Methode ist nur in [Mergemod.dll Version 2,0](merge-module-automation.md) oder höher und nur bei Verwendung der [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c8239-121">The [**MergeEx**](merge-mergeex.md) method is only available in [Mergemod.dll version 2.0](merge-module-automation.md) or later, and only when using the [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) interface.</span></span>

     

5.  <span data-ttu-id="c8239-122">Rufen Sie die [**Errors**](merge-errors.md) -Eigenschaft ab, und untersuchen Sie die Auflistung von [**Fehler**](error-object.md) Objekten, die für Mergekonflikte oder andere Fehler zurückgegeben</span><span class="sxs-lookup"><span data-stu-id="c8239-122">Retrieve the [**Errors**](merge-errors.md) property and examine the collection of [**Error**](error-object.md) objects it returns for merge conflicts or other errors.</span></span>

    <span data-ttu-id="c8239-123">Sie müssen alle Fehler beheben.</span><span class="sxs-lookup"><span data-stu-id="c8239-123">You must resolve any errors.</span></span>

    <span data-ttu-id="c8239-124">Der Abruf ist nicht destruktiv, und mehrere Instanzen der Fehlersammlung können durch wiederholtes Lesen der [**Errors**](merge-errors.md) -Eigenschaft abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c8239-124">The retrieval is nondestructive, and multiple instances of the error collection can be retrieved by repeatedly reading the [**Errors**](merge-errors.md) property.</span></span>

6.  <span data-ttu-id="c8239-125">Ordnen Sie die Komponenten des Mergemoduls den Funktionen mithilfe der [**Connect**](merge-connect.md) -Methode zu.</span><span class="sxs-lookup"><span data-stu-id="c8239-125">Associate the components of the merge module with the features by using the [**Connect**](merge-connect.md) method.</span></span>

    <span data-ttu-id="c8239-126">Dieser Schritt ist nur erforderlich, wenn Sie über vorhandene Features verfügen und Features zum Zusammenführen mit der Installations Datenbank hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="c8239-126">This step is only required if you have existing features and you want to add features to merge into the installation database.</span></span>

    <span data-ttu-id="c8239-127">Eine Funktion muss vorhanden sein, bevor Sie diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="c8239-127">A feature must exist before you call this method.</span></span> <span data-ttu-id="c8239-128">Weitere Informationen finden Sie unter [Verbinden eines Mergemoduls mit mehreren Features](connecting-a-merge-module-to-multiple-features.md).</span><span class="sxs-lookup"><span data-stu-id="c8239-128">For more information, see [Connecting a Merge Module to Multiple Features](connecting-a-merge-module-to-multiple-features.md).</span></span>

7.  <span data-ttu-id="c8239-129">Extrahieren Sie ggf. Quelldateien aus dem Modul, indem Sie eine oder mehrere der folgenden Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="c8239-129">If necessary, extract source files from the module by doing one or more of the following:</span></span>
    -   <span data-ttu-id="c8239-130">Extrahieren Sie mithilfe von [**ExtractFiles**](merge-extractfiles.md) oder [**extractfilesex**](merge-extractfilesex.md) Dateien aus einer eingebetteten CAB-Datei, und kopieren Sie Sie in ein bestimmtes Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="c8239-130">Use [**ExtractFiles**](merge-extractfiles.md) or [**ExtractFilesEx**](merge-extractfilesex.md) to extract files from an embedded .cab file and then copy into a specified directory.</span></span>
        > [!Note]  
        > <span data-ttu-id="c8239-131">[**Extractfilesex**](merge-extractfilesex.md) erfordert [Mergemod.dll-Version 2,0](merge-module-automation.md) oder höher.</span><span class="sxs-lookup"><span data-stu-id="c8239-131">[**ExtractFilesEx**](merge-extractfilesex.md) requires [Mergemod.dll version 2.0](merge-module-automation.md) or later.</span></span>

         

    -   <span data-ttu-id="c8239-132">Extrahieren Sie mithilfe von [**ExtractCab**](merge-extractcab.md) Dateien aus einer eingebetteten CAB-Datei, und speichern Sie Sie dann in einer angegebenen Datei.</span><span class="sxs-lookup"><span data-stu-id="c8239-132">Use [**ExtractCAB**](merge-extractcab.md) to extract files from an embedded .cab file, and then save in a specified file.</span></span>
    -   <span data-ttu-id="c8239-133">Verwenden Sie " [**kreatesourceimage**](merge-createsourceimage.md) ", um Dateien aus einem Modul zu extrahieren, und kopieren Sie dann nach dem Merge in ein Quell Abbild auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="c8239-133">Use [**CreateSourceImage**](merge-createsourceimage.md) to extract files from a module, and then after the merge, copy to a source image on disk.</span></span>
        > [!Note]  
        > <span data-ttu-id="c8239-134">" [**Kreatesourceimage**](merge-createsourceimage.md) " ist nur in [Mergemod.dll Version 2,0](merge-module-automation.md) oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c8239-134">[**CreateSourceImage**](merge-createsourceimage.md) is only available in [Mergemod.dll version 2.0](merge-module-automation.md) or later.</span></span>

         
8.  <span data-ttu-id="c8239-135">Schließen Sie das aktuelle geöffnete Mergemodul mit der [**closemodule**](merge-closemodule.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="c8239-135">Close the current open merge module by using the [**CloseModule**](merge-closemodule.md) method.</span></span>

    <span data-ttu-id="c8239-136">Dieser Schritt ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c8239-136">This step is required.</span></span>

9.  <span data-ttu-id="c8239-137">Schließen Sie die Open-Installations Datenbank mithilfe der [**CloseDatabase**](merge-closedatabase.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="c8239-137">Close the open installation database by using the [**CloseDatabase**](merge-closedatabase.md) method.</span></span>

    <span data-ttu-id="c8239-138">Dieser Schritt ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c8239-138">This step is required.</span></span>

    <span data-ttu-id="c8239-139">Durch das Schließen einer Datenbank werden alle Abhängigkeitsinformationen gelöscht, aber keine Fehler, die nicht abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c8239-139">Closing a database clears all dependency information, but does not affect any errors that are not retrieved.</span></span>

10. <span data-ttu-id="c8239-140">Schließen Sie die aktuelle Protokolldatei mit der [**closelog**](merge-closelog.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="c8239-140">Close the current log file by using the [**CloseLog**](merge-closelog.md) method.</span></span>

    <span data-ttu-id="c8239-141">Dieser Schritt ist erforderlich, wenn Sie über eine geöffnete Protokolldatei verfügen.</span><span class="sxs-lookup"><span data-stu-id="c8239-141">This step is required if you have an open log file.</span></span>

<span data-ttu-id="c8239-142">Nachdem das Modul mithilfe von [Mergemod.dll](merge-module-automation.md)in der Datenbank zusammengeführt wurde, muss die [Medien Tabelle](media-table.md) aktualisiert werden, damit das gewünschte Layout des Quell Bilds beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="c8239-142">After the module has been merged into the database using [Mergemod.dll](merge-module-automation.md), the [Media Table](media-table.md) must be updated to describe the desired source image layout.</span></span> <span data-ttu-id="c8239-143">Der von Mergemod.dll bereitgestellte Mergeprozess aktualisiert die Medien Tabelle nicht, da der Consumer des Mergemoduls verschiedene Möglichkeiten zum Layout des Quell Bilds auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="c8239-143">The merge process provided by Mergemod.dll does not update the Media Table because the consumer of the merge module can select various ways to layout the source image.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c8239-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c8239-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8239-145">Veröffentlichte Versionen, Tools und verteilbare Dateien</span><span class="sxs-lookup"><span data-stu-id="c8239-145">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



