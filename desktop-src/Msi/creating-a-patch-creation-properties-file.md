---
description: Um das Beispiel-Patchpaket zu reproduzieren, benötigen Sie ein Software Tool, mit dem ein Windows Installer Patch-Paket erstellt und bearbeitet werden kann.
ms.assetid: 0653d8f6-89b0-4c56-ae51-3c7cb7df2909
title: Erstellen einer Eigenschaften Datei für die Patcherstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2775f8521731b43264df315ae05a874e37dd3ffc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351588"
---
# <a name="creating-a-patch-creation-properties-file"></a><span data-ttu-id="5e172-103">Erstellen einer Eigenschaften Datei für die Patcherstellung</span><span class="sxs-lookup"><span data-stu-id="5e172-103">Creating a Patch Creation Properties File</span></span>

<span data-ttu-id="5e172-104">Um das Beispiel-Patchpaket zu reproduzieren, benötigen Sie ein Software Tool, mit dem ein Windows Installer Patch-Paket erstellt und bearbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5e172-104">To reproduce the sample patch package, you need a software tool capable of creating and editing a Windows Installer patch package.</span></span> <span data-ttu-id="5e172-105">Mehrere Tools zum Erstellen von patchpaketen sind von unabhängigen Softwareanbietern verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5e172-105">Several patch package creation tools are available from independent software vendors.</span></span> <span data-ttu-id="5e172-106">Im Beispiel, das in den folgenden Abschnitten erläutert wird, wird ein Windows Installer Datenbank-Editor namens Orca verwendet, um eine Eigenschaften Datei für die Patcherstellung (PCP-Erweiterung) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5e172-106">The example discussed in the following sections uses a Windows Installer database editor called Orca to author a patch creation properties file (.pcp extension).</span></span> <span data-ttu-id="5e172-107">Die PCP-Datei kann mit den Dienstprogrammen [Msimsp.exe](msimsp-exe.md) und [Patchwiz.dll](patchwiz-dll.md) verwendet werden, um ein Windows Installer Patchpaket (MSP-Erweiterung) zu generieren.</span><span class="sxs-lookup"><span data-stu-id="5e172-107">The .pcp file may be used with the utilities [Msimsp.exe](msimsp-exe.md) and [Patchwiz.dll](patchwiz-dll.md) to generate a Windows Installer patch package (.msp extension).</span></span> <span data-ttu-id="5e172-108">Orca, Msimsp.exe und Patchwiz.dll werden in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="5e172-108">Orca, Msimsp.exe, and Patchwiz.dll are provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="5e172-109">Mit dem SDK wird auch eine leere patcherstellungs-Eigenschaften Datei (Template. PCP) bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="5e172-109">A blank patch creation properties file, template.pcp, is also provided with the SDK.</span></span> <span data-ttu-id="5e172-110">Erstellen Sie eine Kopie von Template. PCP, und benennen Sie diese Kopie MNP2000. PCP um.</span><span class="sxs-lookup"><span data-stu-id="5e172-110">Make a copy of template.pcp and rename this copy MNP2000.pcp.</span></span> <span data-ttu-id="5e172-111">Verwenden Sie den Orca oder einen anderen Daten Bank Editor, um die folgenden Daten in die Properties-Tabelle von MNP2000. PCP einzugeben.</span><span class="sxs-lookup"><span data-stu-id="5e172-111">Use Orca or another database editor to enter the following data into the Properties table of MNP2000.pcp.</span></span> <span data-ttu-id="5e172-112">Die Properties-Tabelle enthält globale Einstellungen für das Patchpaket.</span><span class="sxs-lookup"><span data-stu-id="5e172-112">The Properties table contains global settings for the patch package.</span></span>

[<span data-ttu-id="5e172-113">Eigenschaftentabelle</span><span class="sxs-lookup"><span data-stu-id="5e172-113">Properties Table</span></span>](properties-table-patchwiz-dll-.md)



| <span data-ttu-id="5e172-114">Name</span><span class="sxs-lookup"><span data-stu-id="5e172-114">Name</span></span>                               | <span data-ttu-id="5e172-115">Wert</span><span class="sxs-lookup"><span data-stu-id="5e172-115">Value</span></span>                                  |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="5e172-116">Allowproductcodemismatches</span><span class="sxs-lookup"><span data-stu-id="5e172-116">AllowProductCodeMismatches</span></span>         | <span data-ttu-id="5e172-117">1</span><span class="sxs-lookup"><span data-stu-id="5e172-117">1</span></span>                                      |
| <span data-ttu-id="5e172-118">Allowproductversionmajormismatches</span><span class="sxs-lookup"><span data-stu-id="5e172-118">AllowProductVersionMajorMismatches</span></span> | <span data-ttu-id="5e172-119">1</span><span class="sxs-lookup"><span data-stu-id="5e172-119">1</span></span>                                      |
| <span data-ttu-id="5e172-120">Apipatchingsymbolflags</span><span class="sxs-lookup"><span data-stu-id="5e172-120">ApiPatchingSymbolFlags</span></span>             | <span data-ttu-id="5e172-121">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5e172-121">0x00000000</span></span>                             |
| <span data-ttu-id="5e172-122">Dontremuvetempfolder. beendet</span><span class="sxs-lookup"><span data-stu-id="5e172-122">DontRemoveTempFolderWhenFinished</span></span>   | <span data-ttu-id="5e172-123">1</span><span class="sxs-lookup"><span data-stu-id="5e172-123">1</span></span>                                      |
| <span data-ttu-id="5e172-124">Incluentwholefilesonly</span><span class="sxs-lookup"><span data-stu-id="5e172-124">IncludeWholeFilesOnly</span></span>              | <span data-ttu-id="5e172-125">0</span><span class="sxs-lookup"><span data-stu-id="5e172-125">0</span></span>                                      |
| <span data-ttu-id="5e172-126">ListOf patchguidstoreplace</span><span class="sxs-lookup"><span data-stu-id="5e172-126">ListOfPatchGUIDsToReplace</span></span>          |                                        |
| <span data-ttu-id="5e172-127">Listoftargetproductcodes</span><span class="sxs-lookup"><span data-stu-id="5e172-127">ListOfTargetProductCodes</span></span>           | \*                                     |
| <span data-ttu-id="5e172-128">Patchguid</span><span class="sxs-lookup"><span data-stu-id="5e172-128">PatchGUID</span></span>                          | <span data-ttu-id="5e172-129">{5406b219-A1ac-4bc4-8695-72292c8195ac}</span><span class="sxs-lookup"><span data-stu-id="5e172-129">{5406B219-A1AC-4BC4-8695-72292C8195AC}</span></span> |
| <span data-ttu-id="5e172-130">Patchoutputpath</span><span class="sxs-lookup"><span data-stu-id="5e172-130">PatchOutputPath</span></span>                    | <span data-ttu-id="5e172-131">c: \\ Output. msp</span><span class="sxs-lookup"><span data-stu-id="5e172-131">c:\\output.msp</span></span>                         |
| <span data-ttu-id="5e172-132">Patchsourcelist</span><span class="sxs-lookup"><span data-stu-id="5e172-132">PatchSourceList</span></span>                    | <span data-ttu-id="5e172-133">Patchsourcelist</span><span class="sxs-lookup"><span data-stu-id="5e172-133">PatchSourceList</span></span>                        |



 

<span data-ttu-id="5e172-134">Verwenden Sie den Datenbank-Editor, um die folgenden Daten in die Tabelle ImageFamilies von MNP2000. PCP einzugeben.</span><span class="sxs-lookup"><span data-stu-id="5e172-134">Use the database editor to enter the following data into the ImageFamilies table of MNP2000.pcp.</span></span> <span data-ttu-id="5e172-135">Die Tabelle "ImageFamilies" enthält Informationen, die der [Medien Tabelle](media-table.md) beim Patchen hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5e172-135">The ImageFamilies table contains information to be added to the [Media table](media-table.md) during patching.</span></span>

[<span data-ttu-id="5e172-136">Tabelle "ImageFamilies"</span><span class="sxs-lookup"><span data-stu-id="5e172-136">ImageFamilies Table</span></span>](imagefamilies-table-patchwiz-dll-.md)



| <span data-ttu-id="5e172-137">Familie</span><span class="sxs-lookup"><span data-stu-id="5e172-137">Family</span></span>  | <span data-ttu-id="5e172-138">Mediasrcpropname</span><span class="sxs-lookup"><span data-stu-id="5e172-138">MediaSrcPropName</span></span> | <span data-ttu-id="5e172-139">Mediadiskid</span><span class="sxs-lookup"><span data-stu-id="5e172-139">MediaDiskId</span></span> | <span data-ttu-id="5e172-140">Filesequencestart</span><span class="sxs-lookup"><span data-stu-id="5e172-140">FileSequenceStart</span></span> | <span data-ttu-id="5e172-141">Diskprompt</span><span class="sxs-lookup"><span data-stu-id="5e172-141">DiskPrompt</span></span> | <span data-ttu-id="5e172-142">VolumeLabel</span><span class="sxs-lookup"><span data-stu-id="5e172-142">VolumeLabel</span></span> |
|---------|------------------|-------------|-------------------|------------|-------------|
| <span data-ttu-id="5e172-143">Mnpapps</span><span class="sxs-lookup"><span data-stu-id="5e172-143">MNPapps</span></span> | <span data-ttu-id="5e172-144">Mnpsrcpropname</span><span class="sxs-lookup"><span data-stu-id="5e172-144">MNPSrcPropName</span></span>   | <span data-ttu-id="5e172-145">2</span><span class="sxs-lookup"><span data-stu-id="5e172-145">2</span></span>           | <span data-ttu-id="5e172-146">1000</span><span class="sxs-lookup"><span data-stu-id="5e172-146">1000</span></span>              |            |             |



 

<span data-ttu-id="5e172-147">Geben Sie die folgenden Daten in die Tabelle "UpgradedImages" von MNP2000. PCP ein.</span><span class="sxs-lookup"><span data-stu-id="5e172-147">Enter the following data into the UpgradedImages table of MNP2000.pcp.</span></span> <span data-ttu-id="5e172-148">Die Tabelle UpgradedImages enthält Informationen zu dem aktualisierten Image, das Sie in [Planen eines kleinen Update Patches](planning-a-small-update-patch.md)erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="5e172-148">The UpgradedImages table contains information about the Upgraded image you created in [Planning a Small Update Patch](planning-a-small-update-patch.md).</span></span>

[<span data-ttu-id="5e172-149">UpgradedImages-Tabelle</span><span class="sxs-lookup"><span data-stu-id="5e172-149">UpgradedImages Table</span></span>](upgradedimages-table-patchwiz-dll-.md)



| <span data-ttu-id="5e172-150">Upgraded</span><span class="sxs-lookup"><span data-stu-id="5e172-150">Upgraded</span></span>   | <span data-ttu-id="5e172-151">Msipath</span><span class="sxs-lookup"><span data-stu-id="5e172-151">MsiPath</span></span>                                           | <span data-ttu-id="5e172-152">Patchmsipath</span><span class="sxs-lookup"><span data-stu-id="5e172-152">PatchMsiPath</span></span> | <span data-ttu-id="5e172-153">SymbolPath</span><span class="sxs-lookup"><span data-stu-id="5e172-153">SymbolPaths</span></span> | <span data-ttu-id="5e172-154">Familie</span><span class="sxs-lookup"><span data-stu-id="5e172-154">Family</span></span>  |
|------------|---------------------------------------------------|--------------|-------------|---------|
| <span data-ttu-id="5e172-155">MNP \_ korrigiert</span><span class="sxs-lookup"><span data-stu-id="5e172-155">MNP\_fixed</span></span> | <span data-ttu-id="5e172-156">C: \\ Hinweis zum \_ Aktualisieren des Installer- \\ Patches \\ \\MNP2000.msi</span><span class="sxs-lookup"><span data-stu-id="5e172-156">C:\\Note\_Installer\\Patch\\Upgraded\\MNP2000.msi</span></span> |              |             | <span data-ttu-id="5e172-157">Mnpapps</span><span class="sxs-lookup"><span data-stu-id="5e172-157">MNPapps</span></span> |



 

<span data-ttu-id="5e172-158">Geben Sie die folgenden Daten in die Tabelle TargetImages von MNP2000. PCP ein.</span><span class="sxs-lookup"><span data-stu-id="5e172-158">Enter the following data into the TargetImages table of MNP2000.pcp.</span></span> <span data-ttu-id="5e172-159">Die Tabelle TargetImages enthält Informationen zum Zielimage.</span><span class="sxs-lookup"><span data-stu-id="5e172-159">The TargetImages table contains information about the Target image.</span></span>

[<span data-ttu-id="5e172-160">TargetImages-Tabelle</span><span class="sxs-lookup"><span data-stu-id="5e172-160">TargetImages Table</span></span>](targetimages-table-patchwiz-dll-.md)



| <span data-ttu-id="5e172-161">Ziel</span><span class="sxs-lookup"><span data-stu-id="5e172-161">Target</span></span>     | <span data-ttu-id="5e172-162">Msipath</span><span class="sxs-lookup"><span data-stu-id="5e172-162">MsiPath</span></span>                                         | <span data-ttu-id="5e172-163">SymbolPath</span><span class="sxs-lookup"><span data-stu-id="5e172-163">SymbolPaths</span></span> | <span data-ttu-id="5e172-164">Upgraded</span><span class="sxs-lookup"><span data-stu-id="5e172-164">Upgraded</span></span>   | <span data-ttu-id="5e172-165">Auftrag</span><span class="sxs-lookup"><span data-stu-id="5e172-165">Order</span></span> | <span data-ttu-id="5e172-166">Productvalidateflags</span><span class="sxs-lookup"><span data-stu-id="5e172-166">ProductValidateFlags</span></span> | <span data-ttu-id="5e172-167">Ignoremissingsrcfiles</span><span class="sxs-lookup"><span data-stu-id="5e172-167">IgnoreMissingSrcFiles</span></span> |
|------------|-------------------------------------------------|-------------|------------|-------|----------------------|-----------------------|
| <span data-ttu-id="5e172-168">MNP- \_ Fehler</span><span class="sxs-lookup"><span data-stu-id="5e172-168">MNP\_error</span></span> | <span data-ttu-id="5e172-169">C: \\ Hinweis \_ zur \\MNP2000.msi des installerpatchziels \\ \\</span><span class="sxs-lookup"><span data-stu-id="5e172-169">C:\\Note\_Installer\\Patch\\Target\\MNP2000.msi</span></span> |             | <span data-ttu-id="5e172-170">MNP \_ korrigiert</span><span class="sxs-lookup"><span data-stu-id="5e172-170">MNP\_fixed</span></span> | <span data-ttu-id="5e172-171">1</span><span class="sxs-lookup"><span data-stu-id="5e172-171">1</span></span>     |                      | <span data-ttu-id="5e172-172">0</span><span class="sxs-lookup"><span data-stu-id="5e172-172">0</span></span>                     |



 

<span data-ttu-id="5e172-173">Belassen Sie für das Beispiel Patch-Paket die folgenden Tabellen in MNP2000. PCP leer.</span><span class="sxs-lookup"><span data-stu-id="5e172-173">For the sample patch package, leave the following tables in MNP2000.pcp blank.</span></span>

[<span data-ttu-id="5e172-174">Tabelle "upgradedfiles" ( \_ OptionalData)</span><span class="sxs-lookup"><span data-stu-id="5e172-174">UpgradedFiles\_OptionalData Table</span></span>](upgradedfiles-optionaldata-table-patchwiz-dll-.md)

[<span data-ttu-id="5e172-175">Familyfileranges-Tabelle</span><span class="sxs-lookup"><span data-stu-id="5e172-175">FamilyFileRanges Table</span></span>](familyfileranges-table-patchwiz-dll-.md)

[<span data-ttu-id="5e172-176">Targetfiles ( \_ OptionalData-Tabelle)</span><span class="sxs-lookup"><span data-stu-id="5e172-176">TargetFiles\_OptionalData Table</span></span>](targetfiles-optionaldata-table-patchwiz-dll-.md)

[<span data-ttu-id="5e172-177">Externalfiles-Tabelle</span><span class="sxs-lookup"><span data-stu-id="5e172-177">ExternalFiles Table</span></span>](externalfiles-table-patchwiz-dll-.md)

[<span data-ttu-id="5e172-178">Tabelle "Upgrade dfilestoignore"</span><span class="sxs-lookup"><span data-stu-id="5e172-178">UpgradedFilesToIgnore Table</span></span>](upgradedfilestoignore-table-patchwiz-dll-.md)

[<span data-ttu-id="5e172-179">Fortsetzen</span><span class="sxs-lookup"><span data-stu-id="5e172-179">Continue</span></span>](generating-a-patch-package.md)

 

 



