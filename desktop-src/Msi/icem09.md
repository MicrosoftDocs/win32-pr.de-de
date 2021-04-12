---
description: ICEM09 überprüft, ob das Mergemodul vordefinierte Verzeichnisse sicher verarbeitet.
ms.assetid: 747ae5ee-adc1-4aa7-8239-2379f76bfd0f
title: ICEM09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee4b4d2d52c35d6dd3670daff5150a785e19d0b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216942"
---
# <a name="icem09"></a><span data-ttu-id="4af6a-103">ICEM09</span><span class="sxs-lookup"><span data-stu-id="4af6a-103">ICEM09</span></span>

<span data-ttu-id="4af6a-104">ICEM09 überprüft, ob das Mergemodul vordefinierte Verzeichnisse sicher verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="4af6a-104">ICEM09 verifies the merge module safely handles predefined directories.</span></span> <span data-ttu-id="4af6a-105">Dies geschieht, indem überprüft wird, ob keine Komponente im Modul ein Verzeichnis in einem vordefinierten System Verzeichnis installiert, wie z. b. "ProgramFilesFolder" oder "StartMenuFolder".</span><span class="sxs-lookup"><span data-stu-id="4af6a-105">It does this by verifying that no component in the module installs a directory to a predefined system directory such as "ProgramFilesFolder" or "StartMenuFolder".</span></span> <span data-ttu-id="4af6a-106">Stattdessen sollten Module Verzeichnisse mit eindeutigen Namen verwenden (erstellt mit der Benennungs Konvention für das Mergemodul) und benutzerdefinierte Aktionen verwenden, um das entsprechende Zielverzeichnis als Ziel zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="4af6a-106">Instead, modules should use directories with unique names (created with the merge module naming convention) and use custom actions to target the appropriate target directory.</span></span> <span data-ttu-id="4af6a-107">Bei diesem Ansatz wird verhindert, dass Module in Konflikt mit einer vorhandenen Verzeichnisstruktur in der endgültigen Datenbank stehen.</span><span class="sxs-lookup"><span data-stu-id="4af6a-107">This approach prevents modules from conflicting with an existing directory structure in the final database.</span></span> <span data-ttu-id="4af6a-108">ICEM09 prüft, ob die für diese Technik benötigten benutzerdefinierten Aktionen entweder nicht vorhanden sind (damit das Mergetool Sie generieren kann) oder in der richtigen Form vorhanden sind (sodass Sie erwartungsgemäß funktionieren).</span><span class="sxs-lookup"><span data-stu-id="4af6a-108">ICEM09 checks that the custom actions needed for this technique to work either do not exist (so that the merge tool can generate them) or exist in the correct form (so that they work as expected).</span></span>

<span data-ttu-id="4af6a-109">Wenn eine Warnung oder ein Fehler, der von ICEM09 gemeldet wurde, nicht behoben werden kann, können Probleme für die Clients des Mergemoduls auftreten.</span><span class="sxs-lookup"><span data-stu-id="4af6a-109">Failure to fix a warning or error reported by ICEM09 could cause problems for the clients of your merge module.</span></span> <span data-ttu-id="4af6a-110">Verzeichnis Tabellenzeilen mit primär Schlüsseln, z. b. ProgramFilesFolder, sind häufig in einer Datenbank vorhanden. Wenn Komponenten in Ihrem Modul direkt in vordefinierten Verzeichnissen (z. b. ProgramFilesFolder) installiert werden, können die Verzeichniseinträge im Modul also mit bereits vorhandenen Zeilen kollidieren.</span><span class="sxs-lookup"><span data-stu-id="4af6a-110">Directory table rows with primary keys such as ProgramFilesFolder often exist in a database; therefore, if components in your module install directly to predefined directories such as ProgramFilesFolder, the directory entries in the module may collide with already existing rows.</span></span> <span data-ttu-id="4af6a-111">Diese Bedingung erfordert, dass der Benutzer des Moduls die Quelldateien aus dem Modul aufteilen muss, damit es dem vorhandenen Quellverzeichnis entspricht.</span><span class="sxs-lookup"><span data-stu-id="4af6a-111">This condition would require the user of your module to split the source files from your module in order to match the existing source directory.</span></span>

## <a name="result"></a><span data-ttu-id="4af6a-112">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="4af6a-112">Result</span></span>

<span data-ttu-id="4af6a-113">ICEM09 meldet einen Fehler oder eine Warnung, wenn eine Modul Komponente ein Verzeichnis in einem vordefinierten System Verzeichnis installiert, wodurch ein möglicher namens Konflikt mit der vorhandenen Verzeichnisstruktur verursacht wird.</span><span class="sxs-lookup"><span data-stu-id="4af6a-113">ICEM09 reports an error or warning when a module component installs a directory to a pre-defined system directory, causing a possible name conflict with the existing directory structure.</span></span>

## <a name="example"></a><span data-ttu-id="4af6a-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4af6a-114">Example</span></span>

<span data-ttu-id="4af6a-115">ICEM09 veröffentlicht die folgenden Warnungen für ein Modul, das die angezeigten Datenbankeinträge enthält.</span><span class="sxs-lookup"><span data-stu-id="4af6a-115">ICEM09 posts the following warnings for a module containing the database entries shown.</span></span>

``` syntax
Warning: The component 'Component1.<GUID>' installs directly into the pre-defined 
directory 'ProgramFilesFolder'. It is recommended that merge modules alias 
all such directories to unique names.
```

<span data-ttu-id="4af6a-116">Benennen Sie das mergemodulverzeichnis um, sodass es nicht mit einer Windows Installer-Eigenschaft identisch ist und daher eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="4af6a-116">Rename the merge module directory so it does not match a Windows Installer property and therefore is unique.</span></span> <span data-ttu-id="4af6a-117">Legen Sie dann eine Eigenschaft mit demselben Namen auf den Wert des Windows Installer Verzeichnisses fest.</span><span class="sxs-lookup"><span data-stu-id="4af6a-117">Then set a property of the same name to the value of the Windows Installer directory.</span></span> <span data-ttu-id="4af6a-118">Wenn die Verzeichnis Auflösung stattfindet, hat das Verzeichnis eine Eigenschaft mit demselben Namen, sodass der Installationsort des Verzeichnisses der Wert der Eigenschaft ist.</span><span class="sxs-lookup"><span data-stu-id="4af6a-118">When directory resolution takes place, the directory has a property of the same name, so the install location of the directory is the value of the property.</span></span> <span data-ttu-id="4af6a-119">Dateien werden vom unterschiedlichen Quell Speicherort an denselben Ziel Speicherort verschoben.</span><span class="sxs-lookup"><span data-stu-id="4af6a-119">Files move from the distinct source location to the same target location.</span></span> <span data-ttu-id="4af6a-120">Bei diesem Prozess sollten die Mergekonflikte vollständig entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="4af6a-120">This process should completely remove the merge conflicts.</span></span>

``` syntax
Warning: The 'ModuleInstallExecuteSequence' table contains a type 51 action 
(StartMenuFolder.<GUID>) for a pre-defined directory, but this action 
does not have sequence number '1'
```

<span data-ttu-id="4af6a-121">Wenn die Aktion nicht die Sequenznummer 1 hat, wird Sie möglicherweise nicht früh genug in der Zieldatenbank zusammengeführt, um effektiv arbeiten zu können.</span><span class="sxs-lookup"><span data-stu-id="4af6a-121">If the action does not have sequence number 1, it may not merge in to the target database early enough in the sequence to work effectively.</span></span>

<span data-ttu-id="4af6a-122">Legen Sie die Sequenznummer auf 1 fest, um diese Warnung zu beheben.</span><span class="sxs-lookup"><span data-stu-id="4af6a-122">To fix this warning, set the sequence number to 1.</span></span> <span data-ttu-id="4af6a-123">Beachten Sie, dass die meisten aktuellen mergetools (aber nicht einige ältere Versionen) diese benutzerdefinierten Aktionen zur mergezeit generieren, sodass es nicht immer notwendig ist, die Aktionen explizit im Mergemodul zu verfassen.</span><span class="sxs-lookup"><span data-stu-id="4af6a-123">Note that most current merge tools (but not some older versions) will generate these custom actions at merge time, so it is not always necessary to explicitly author the actions into the merge module.</span></span>

``` syntax
Warning: The 'CustomAction' table contains a type 51 action (MyAppDataFolderAction) 
for a pre-defined directory, but the name is not the same as the target directory. 
Many merge tools will generate duplicate actions."
```

<span data-ttu-id="4af6a-124">Da die CustomAction-Spalte der Primärschlüssel der CustomAction-Tabelle ist, können einige Merge-Tools doppelte Aktionen generieren, da der vordefinierte Aktionsname anders ist.</span><span class="sxs-lookup"><span data-stu-id="4af6a-124">Because the CustomAction column is the primary key of CustomAction table, some merge tools may generate duplicate actions because the pre-authored action name is different.</span></span>

<span data-ttu-id="4af6a-125">Um diese Warnung zu beheben, benennen Sie die Aktion mit dem Zielverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="4af6a-125">To fix this warning, name the action the same as the target directory.</span></span> <span data-ttu-id="4af6a-126">Beachten Sie, dass die meisten aktuellen mergetools (aber nicht einige ältere Versionen) diese benutzerdefinierten Aktionen zur mergezeit generieren, sodass es nicht immer notwendig ist, die Aktionen explizit im Mergemodul zu verfassen.</span><span class="sxs-lookup"><span data-stu-id="4af6a-126">Note that most current merge tools (but not some older versions) generate these custom actions at merge time, so it is not always necessary to explicitly author the actions into the merge module.</span></span>

[<span data-ttu-id="4af6a-127">Verzeichnis Tabelle</span><span class="sxs-lookup"><span data-stu-id="4af6a-127">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="4af6a-128">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="4af6a-128">Directory</span></span>          | <span data-ttu-id="4af6a-129">Über \_ geordnetes Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="4af6a-129">Directory\_Parent</span></span> | <span data-ttu-id="4af6a-130">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="4af6a-130">DefaultDir</span></span> |
|--------------------|-------------------|------------|
| <span data-ttu-id="4af6a-131">ProgramFilesFolder</span><span class="sxs-lookup"><span data-stu-id="4af6a-131">ProgramFilesFolder</span></span> | <span data-ttu-id="4af6a-132">Directory1</span><span class="sxs-lookup"><span data-stu-id="4af6a-132">Directory1</span></span>        | <span data-ttu-id="4af6a-133">A</span><span class="sxs-lookup"><span data-stu-id="4af6a-133">A</span></span>          |
| <span data-ttu-id="4af6a-134">Startmenü Ordner</span><span class="sxs-lookup"><span data-stu-id="4af6a-134">StartMenuFolder</span></span>    | <span data-ttu-id="4af6a-135">Directory2</span><span class="sxs-lookup"><span data-stu-id="4af6a-135">Directory2</span></span>        | <span data-ttu-id="4af6a-136">b:c</span><span class="sxs-lookup"><span data-stu-id="4af6a-136">B:C</span></span>        |
| <span data-ttu-id="4af6a-137">AppDataFolder</span><span class="sxs-lookup"><span data-stu-id="4af6a-137">AppDataFolder</span></span>      | <span data-ttu-id="4af6a-138">Directory3</span><span class="sxs-lookup"><span data-stu-id="4af6a-138">Directory3</span></span>        | <span data-ttu-id="4af6a-139">D</span><span class="sxs-lookup"><span data-stu-id="4af6a-139">D</span></span>          |
| <span data-ttu-id="4af6a-140">Mypicturesfolder</span><span class="sxs-lookup"><span data-stu-id="4af6a-140">MyPicturesFolder</span></span>   | <span data-ttu-id="4af6a-141">Directory4</span><span class="sxs-lookup"><span data-stu-id="4af6a-141">Directory4</span></span>        | <span data-ttu-id="4af6a-142">E</span><span class="sxs-lookup"><span data-stu-id="4af6a-142">E</span></span>          |



 

[<span data-ttu-id="4af6a-143">Komponenten Tabelle</span><span class="sxs-lookup"><span data-stu-id="4af6a-143">Component Table</span></span>](component-table.md)



| <span data-ttu-id="4af6a-144">Komponente</span><span class="sxs-lookup"><span data-stu-id="4af6a-144">Component</span></span>               | <span data-ttu-id="4af6a-145">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="4af6a-145">Directory</span></span>          |
|-------------------------|--------------------|
| <span data-ttu-id="4af6a-146">Component1.<GUID></span><span class="sxs-lookup"><span data-stu-id="4af6a-146">Component1.<GUID></span></span> | <span data-ttu-id="4af6a-147">ProgramFilesFolder</span><span class="sxs-lookup"><span data-stu-id="4af6a-147">ProgramFilesFolder</span></span> |
| <span data-ttu-id="4af6a-148">Component2.<GUID></span><span class="sxs-lookup"><span data-stu-id="4af6a-148">Component2.<GUID></span></span> | <span data-ttu-id="4af6a-149">Startmenü Ordner</span><span class="sxs-lookup"><span data-stu-id="4af6a-149">StartMenuFolder</span></span>    |
| <span data-ttu-id="4af6a-150">Component3.<GUID></span><span class="sxs-lookup"><span data-stu-id="4af6a-150">Component3.<GUID></span></span> | <span data-ttu-id="4af6a-151">AppDataFolder</span><span class="sxs-lookup"><span data-stu-id="4af6a-151">AppDataFolder</span></span>      |
| <span data-ttu-id="4af6a-152">Component4.<GUID></span><span class="sxs-lookup"><span data-stu-id="4af6a-152">Component4.<GUID></span></span> | <span data-ttu-id="4af6a-153">Mypicturesfolder</span><span class="sxs-lookup"><span data-stu-id="4af6a-153">MyPicturesFolder</span></span>   |



 

[<span data-ttu-id="4af6a-154">Tabelle "CustomAction"</span><span class="sxs-lookup"><span data-stu-id="4af6a-154">CustomAction Table</span></span>](customaction-table.md)



| <span data-ttu-id="4af6a-155">CustomAction</span><span class="sxs-lookup"><span data-stu-id="4af6a-155">CustomAction</span></span>                 | <span data-ttu-id="4af6a-156">type</span><span class="sxs-lookup"><span data-stu-id="4af6a-156">Type</span></span> | <span data-ttu-id="4af6a-157">`Source`</span><span class="sxs-lookup"><span data-stu-id="4af6a-157">Source</span></span>                       | <span data-ttu-id="4af6a-158">Ziel</span><span class="sxs-lookup"><span data-stu-id="4af6a-158">Target</span></span>              |
|------------------------------|------|------------------------------|---------------------|
| <span data-ttu-id="4af6a-159">Startmenü Folder.<GUID></span><span class="sxs-lookup"><span data-stu-id="4af6a-159">StartMenuFolder.<GUID></span></span> | <span data-ttu-id="4af6a-160">51</span><span class="sxs-lookup"><span data-stu-id="4af6a-160">51</span></span>   | <span data-ttu-id="4af6a-161">Startmenü Folder.<GUID></span><span class="sxs-lookup"><span data-stu-id="4af6a-161">StartMenuFolder.<GUID></span></span> | <span data-ttu-id="4af6a-162">\[Startmenü Ordner\]</span><span class="sxs-lookup"><span data-stu-id="4af6a-162">\[StartMenuFolder\]</span></span> |
| <span data-ttu-id="4af6a-163">Myappdatafolderaction</span><span class="sxs-lookup"><span data-stu-id="4af6a-163">MyAppDataFolderAction</span></span>        | <span data-ttu-id="4af6a-164">51</span><span class="sxs-lookup"><span data-stu-id="4af6a-164">51</span></span>   | <span data-ttu-id="4af6a-165">AppDataFolder.<GUID></span><span class="sxs-lookup"><span data-stu-id="4af6a-165">AppDataFolder.<GUID></span></span>   | <span data-ttu-id="4af6a-166">\[AppDataFolder\]</span><span class="sxs-lookup"><span data-stu-id="4af6a-166">\[AppDataFolder\]</span></span>   |



 

[<span data-ttu-id="4af6a-167">Moduleinstallexecutesequence-Tabelle</span><span class="sxs-lookup"><span data-stu-id="4af6a-167">ModuleInstallExecuteSequence Table</span></span>](moduleinstallexecutesequence-table.md)



| <span data-ttu-id="4af6a-168">Aktion</span><span class="sxs-lookup"><span data-stu-id="4af6a-168">Action</span></span>                       | <span data-ttu-id="4af6a-169">Sequenz</span><span class="sxs-lookup"><span data-stu-id="4af6a-169">Sequence</span></span> | <span data-ttu-id="4af6a-170">Baseaction</span><span class="sxs-lookup"><span data-stu-id="4af6a-170">BaseAction</span></span> | <span data-ttu-id="4af6a-171">Nach</span><span class="sxs-lookup"><span data-stu-id="4af6a-171">After</span></span> | <span data-ttu-id="4af6a-172">Bedingung</span><span class="sxs-lookup"><span data-stu-id="4af6a-172">Condition</span></span> |
|------------------------------|----------|------------|-------|-----------|
| <span data-ttu-id="4af6a-173">Startmenü Folder.<GUID></span><span class="sxs-lookup"><span data-stu-id="4af6a-173">StartMenuFolder.<GUID></span></span> | <span data-ttu-id="4af6a-174">100</span><span class="sxs-lookup"><span data-stu-id="4af6a-174">100</span></span>      |            |       |           |



 

## <a name="related-topics"></a><span data-ttu-id="4af6a-175">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4af6a-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4af6a-176">Eisverweis für Mergemodul</span><span class="sxs-lookup"><span data-stu-id="4af6a-176">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



