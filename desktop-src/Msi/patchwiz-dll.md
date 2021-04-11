---
description: Zum Generieren eines Patchpakets empfiehlt es sich, ein patcherstellungs Tool wie Msimsp.exe und Patchwiz.dll zu verwenden.
ms.assetid: aca3bbd2-440a-405f-bddc-5f9cc831b811
title: Patchwiz.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6dc1135a9e2c09bb8a96e041f77bae39f0057ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218521"
---
# <a name="patchwizdll"></a><span data-ttu-id="84acd-103">Patchwiz.dll</span><span class="sxs-lookup"><span data-stu-id="84acd-103">Patchwiz.dll</span></span>

<span data-ttu-id="84acd-104">Zum Generieren eines Patchpakets empfiehlt es sich, ein patcherstellungs Tool wie [Msimsp.exe](msimsp-exe.md) und Patchwiz.dll zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="84acd-104">To generate a patch package, it is recommended that you use a patch creation tool such as [Msimsp.exe](msimsp-exe.md) and Patchwiz.dll.</span></span> <span data-ttu-id="84acd-105">Patchwiz.dll Version 4,0 ist kompatibel mit Paketen und Patches, die mit früheren Versionen der Patchwiz.dll erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="84acd-105">Patchwiz.dll version 4.0 is compatible with packages and patches that were authored using earlier versions of the Patchwiz.dll.</span></span> <span data-ttu-id="84acd-106">Das Patchwiz.dll Tool ist nur in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="84acd-106">The Patchwiz.dll tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="84acd-107">Patchwiz.dll Version 4,0 verfügt über eine neue Funktion, [uikreatepatchpackageex (Patchwiz.dll)](uicreatepatchpackageex--patchwiz-dll-.md), die die Funktionalität von [uikreatepatchpackage (Patchwiz.dll)](uicreatepatchpackage-patchwiz-dll-.md)erweitert.</span><span class="sxs-lookup"><span data-stu-id="84acd-107">Patchwiz.dll version 4.0 has one new function, [UiCreatePatchPackageEx (Patchwiz.dll)](uicreatepatchpackageex--patchwiz-dll-.md), that extends the functionality of [UiCreatePatchPackage (Patchwiz.dll)](uicreatepatchpackage-patchwiz-dll-.md).</span></span> <span data-ttu-id="84acd-108">Diese Funktionen nehmen eine patcherstellungs-Eigenschaften Datei (PCP-Datei) an und generieren ein Installer- [Patchpaket](patch-packages.md).</span><span class="sxs-lookup"><span data-stu-id="84acd-108">These functions take a patch creation properties file (.pcp file) and generate an installer [Patch Package](patch-packages.md).</span></span>

<span data-ttu-id="84acd-109">Bei der PCP-Datei handelt es sich um eine binäre Datenbankdatei mit demselben Format wie eine Windows Installer Datenbank (MSI-Datei), jedoch mit einem anderen Datenbankschema.</span><span class="sxs-lookup"><span data-stu-id="84acd-109">The .pcp file is a binary database file with the same format as a Windows Installer database (.msi file), but with a different database schema.</span></span> <span data-ttu-id="84acd-110">Daher kann eine PCP-Datei mit denselben Tools erstellt werden, die für eine Installerdatenbank verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="84acd-110">Therefore a .pcp file can be authored by using the same tools used for an installer database.</span></span>

<span data-ttu-id="84acd-111">Sie können eine PCP-Datei erstellen, indem Sie einen Tabellen-Editor wie [Orca.exe](orca-exe.md) zum Eingeben von Informationen in die leere PCP-Datenbank verwenden, die mit dem Windows Installer SDK (Template. PCP) bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="84acd-111">You can create a .pcp file by using a table editor such as [Orca.exe](orca-exe.md) to enter information into the blank .pcp database provided with the Windows Installer SDK, Template.pcp.</span></span> <span data-ttu-id="84acd-112">Weitere Informationen finden Sie unter [Beispiel für ein kleines Update-Patching](a-small-update-patching-example.md).</span><span class="sxs-lookup"><span data-stu-id="84acd-112">For more information, see [A Small Update Patching Example](a-small-update-patching-example.md).</span></span>

<span data-ttu-id="84acd-113">Die folgenden Datenbanktabellen sind in jeder PCP-Datei erforderlich:</span><span class="sxs-lookup"><span data-stu-id="84acd-113">The following database tables are required in every .pcp file:</span></span>

-   [<span data-ttu-id="84acd-114">Properties-Tabelle (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="84acd-114">Properties Table (Patchwiz.dll)</span></span>](properties-table-patchwiz-dll-.md)
-   [<span data-ttu-id="84acd-115">Tabelle "ImageFamilies" (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="84acd-115">ImageFamilies Table (Patchwiz.dll)</span></span>](imagefamilies-table-patchwiz-dll-.md)
-   [<span data-ttu-id="84acd-116">UpgradedImages-Tabelle (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="84acd-116">UpgradedImages Table (Patchwiz.dll)</span></span>](upgradedimages-table-patchwiz-dll-.md)
-   [<span data-ttu-id="84acd-117">TargetImages-Tabelle (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="84acd-117">TargetImages Table (Patchwiz.dll)</span></span>](targetimages-table-patchwiz-dll-.md)

<span data-ttu-id="84acd-118">Die folgenden Datenbanktabellen sind optional:</span><span class="sxs-lookup"><span data-stu-id="84acd-118">The following database tables are optional:</span></span>

-   [<span data-ttu-id="84acd-119">Tabelle "upgradedfiles" \_ (OptionalData) (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="84acd-119">UpgradedFiles\_OptionalData Table (Patchwiz.dll)</span></span>](upgradedfiles-optionaldata-table-patchwiz-dll-.md)
-   [<span data-ttu-id="84acd-120">Familyfileranges-Tabelle (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="84acd-120">FamilyFileRanges Table (Patchwiz.dll)</span></span>](familyfileranges-table-patchwiz-dll-.md)
-   [<span data-ttu-id="84acd-121">Targetfiles \_ (OptionalData-Tabelle) (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="84acd-121">TargetFiles\_OptionalData Table (Patchwiz.dll)</span></span>](targetfiles-optionaldata-table-patchwiz-dll-.md)
-   [<span data-ttu-id="84acd-122">Externalfiles-Tabelle (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="84acd-122">ExternalFiles Table (Patchwiz.dll)</span></span>](externalfiles-table-patchwiz-dll-.md)
-   [<span data-ttu-id="84acd-123">Tabelle "Upgrade dfilestoignore" (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="84acd-123">UpgradedFilesToIgnore Table (Patchwiz.dll)</span></span>](upgradedfilestoignore-table-patchwiz-dll-.md)

<span data-ttu-id="84acd-124">Die folgende Tabelle ist in PCP-Dateien erforderlich, deren minimumrequirements dmsiversion 300 in der [Properties](properties-table-patchwiz-dll-.md) -Tabelle entspricht.</span><span class="sxs-lookup"><span data-stu-id="84acd-124">The following table is required in .pcp files that have a MinimumRequiredMsiVersion equal to 300 in the [Properties](properties-table-patchwiz-dll-.md) table.</span></span>

-   [<span data-ttu-id="84acd-125">Patchmetadata-Tabelle (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="84acd-125">PatchMetadata Table (Patchwiz.dll)</span></span>](patchmetadata-table--patchwiz-dll-.md)

> [!Note]  
> <span data-ttu-id="84acd-126">Die Tabelle ist optional, wenn minimumrequirements dmsiversion nicht gleich 300 ist.</span><span class="sxs-lookup"><span data-stu-id="84acd-126">The table is optional if MinimumRequiredMsiVersion is not equal to 300.</span></span>

 

<span data-ttu-id="84acd-127">Die mit Windows Installer 3,0 veröffentlichte Version von Patchwiz.dll kann automatisch Informationen zur Patchsequenzierung generieren und Sie der [msipatchsequence-Tabelle](msipatchsequence-table.md) eines neuen Patches hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="84acd-127">The version of Patchwiz.dll released with Windows Installer 3.0 can automatically generate patch sequencing information and add it to the [MsiPatchSequence Table](msipatchsequence-table.md) of a new patch.</span></span> <span data-ttu-id="84acd-128">Die [Tabelle "patchsequence](patchsequence-table--patchwiz-dll-.md) " kann verwendet werden, um patchsequenzierungs Informationen manuell der Tabelle "msipatchsequence" hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="84acd-128">The [PatchSequence Table](patchsequence-table--patchwiz-dll-.md) can be used to manually add patch sequencing information the MsiPatchSequence Table.</span></span> <span data-ttu-id="84acd-129">Weitere Informationen finden Sie unter [Erstellen von Patchsequenzinformationen](generating-patch-sequence-information---patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="84acd-129">For more information, see [Generating Patch Sequence Information](generating-patch-sequence-information---patchwiz-dll-.md).</span></span>

<span data-ttu-id="84acd-130">Ab Patchwiz.dll Version 2,0 können Sie die Geschwindigkeit der nachfolgenden Patcherstellung mithilfe von [patchinformations Caching (Patchwiz.dll)](patch-information-caching-patchwiz-dll-.md)erhöhen.</span><span class="sxs-lookup"><span data-stu-id="84acd-130">Beginning with Patchwiz.dll version 2.0, you can increase the speed of subsequent patch creation by using [Patch Information Caching (Patchwiz.dll)](patch-information-caching-patchwiz-dll-.md).</span></span>

<span data-ttu-id="84acd-131">Wenn Sie öffentliche Symbole für die Ziel-und upgradeabbild-Binärdateien verwenden, können binäre patchgrößen um ungefähr eine Hälfte reduziert werden.</span><span class="sxs-lookup"><span data-stu-id="84acd-131">Using public symbols for your target and upgrade image binaries can reduce binary patch sizes by approximately one half.</span></span> <span data-ttu-id="84acd-132">Weitere Informationen finden Sie unter [Verwenden von Symbolen, um die binäre Patchgröße zu verringern](using-symbols-to-reduce-binary-patch-size.md).</span><span class="sxs-lookup"><span data-stu-id="84acd-132">For more information, see [Using Symbols to Reduce Binary Patch Size](using-symbols-to-reduce-binary-patch-size.md).</span></span>

<span data-ttu-id="84acd-133">Sie können angeben, dass bestimmte Bereiche der Zieldatei beim Patchen nicht überschrieben werden sollen und dass die Informationen in diesen Regionen beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="84acd-133">You can specify that certain regions of the target file be preserved from being overwritten during patching and that the information in those regions be retained.</span></span> <span data-ttu-id="84acd-134">Weitere Informationen finden Sie unter [Patchen ausgewählter Bereiche einer Datei](patching-selected-regions-of-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="84acd-134">For more information, see [Patching Selected Regions of a File](patching-selected-regions-of-a-file.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="84acd-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="84acd-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84acd-136">Veröffentlichte Versionen, Tools und verteilbare Dateien</span><span class="sxs-lookup"><span data-stu-id="84acd-136">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



