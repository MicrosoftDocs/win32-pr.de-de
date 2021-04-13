---
description: Die UpgradedImages-Tabelle enthält Informationen zu den aktualisierten Images des Produkts.
ms.assetid: f4ee2cc8-8a49-4e4a-b8cf-b4ae2bc7e753
title: UpgradedImages-Tabelle (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48dcecc94786cbe783f21e6e005b645586f2e894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348958"
---
# <a name="upgradedimages-table-patchwizdll"></a><span data-ttu-id="f4dc8-103">UpgradedImages-Tabelle (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="f4dc8-103">UpgradedImages Table (Patchwiz.dll)</span></span>

<span data-ttu-id="f4dc8-104">Die UpgradedImages-Tabelle enthält Informationen zu den aktualisierten Images des Produkts.</span><span class="sxs-lookup"><span data-stu-id="f4dc8-104">The UpgradedImages table contains information about the upgraded images of the product.</span></span> <span data-ttu-id="f4dc8-105">Bei dem aktualisierten Image muss es sich um ein vollständig dekomprimiertes Setup Image der neuesten Version des Produkts handeln, z. b. ein administratives Image oder ein nicht komprimiertes Setup Abbild von einer CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="f4dc8-105">The upgraded image should be a fully uncompressed setup image of the latest version of the product, for example, an administrative image or an uncompressed setup image from a CD-ROM.</span></span> <span data-ttu-id="f4dc8-106">Ein Windows Installer Patch-Paket aktualisiert ein Zielimage in ein aktualisiertes Image.</span><span class="sxs-lookup"><span data-stu-id="f4dc8-106">A Windows Installer patch package updates a target image into an upgraded image.</span></span> <span data-ttu-id="f4dc8-107">Die UpgradedImages-Tabelle ist in der Datenbank für die Patcherstellung (PCP-Datei) erforderlich und wird von [uikreatepatchpackageex](uicreatepatchpackageex--patchwiz-dll-.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="f4dc8-107">The UpgradedImages table is required in the patch creation database (.pcp file) and is used by [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md).</span></span>

<span data-ttu-id="f4dc8-108">In jeder Datenbank der Patcherstellung (PCP-Datei) ist eine UpgradedImages-Tabelle erforderlich, die mindestens einen Datensatz enthält.</span><span class="sxs-lookup"><span data-stu-id="f4dc8-108">An UpgradedImages table containing at least one record is required in every patch creation database (.pcp file).</span></span> <span data-ttu-id="f4dc8-109">Diese Tabelle wird von [uikreatepatchpackageex](uicreatepatchpackageex--patchwiz-dll-.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="f4dc8-109">This table is used by [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md).</span></span>

<span data-ttu-id="f4dc8-110">Die UpgradedImages-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="f4dc8-110">The UpgradedImages table has the following columns.</span></span>



| <span data-ttu-id="f4dc8-111">Spalte</span><span class="sxs-lookup"><span data-stu-id="f4dc8-111">Column</span></span>       | <span data-ttu-id="f4dc8-112">Typ</span><span class="sxs-lookup"><span data-stu-id="f4dc8-112">Type</span></span> | <span data-ttu-id="f4dc8-113">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="f4dc8-113">Key</span></span> | <span data-ttu-id="f4dc8-114">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="f4dc8-114">Nullable</span></span> |
|--------------|------|-----|----------|
| <span data-ttu-id="f4dc8-115">Upgraded</span><span class="sxs-lookup"><span data-stu-id="f4dc8-115">Upgraded</span></span>     | <span data-ttu-id="f4dc8-116">text</span><span class="sxs-lookup"><span data-stu-id="f4dc8-116">text</span></span> | <span data-ttu-id="f4dc8-117">J</span><span class="sxs-lookup"><span data-stu-id="f4dc8-117">Y</span></span>   | <span data-ttu-id="f4dc8-118">N</span><span class="sxs-lookup"><span data-stu-id="f4dc8-118">N</span></span>        |
| <span data-ttu-id="f4dc8-119">Msipath</span><span class="sxs-lookup"><span data-stu-id="f4dc8-119">MsiPath</span></span>      | <span data-ttu-id="f4dc8-120">text</span><span class="sxs-lookup"><span data-stu-id="f4dc8-120">text</span></span> |     | <span data-ttu-id="f4dc8-121">N</span><span class="sxs-lookup"><span data-stu-id="f4dc8-121">N</span></span>        |
| <span data-ttu-id="f4dc8-122">Patchmsipath</span><span class="sxs-lookup"><span data-stu-id="f4dc8-122">PatchMsiPath</span></span> | <span data-ttu-id="f4dc8-123">text</span><span class="sxs-lookup"><span data-stu-id="f4dc8-123">text</span></span> |     | <span data-ttu-id="f4dc8-124">J</span><span class="sxs-lookup"><span data-stu-id="f4dc8-124">Y</span></span>        |
| <span data-ttu-id="f4dc8-125">SymbolPath</span><span class="sxs-lookup"><span data-stu-id="f4dc8-125">SymbolPaths</span></span>  | <span data-ttu-id="f4dc8-126">text</span><span class="sxs-lookup"><span data-stu-id="f4dc8-126">text</span></span> |     | <span data-ttu-id="f4dc8-127">J</span><span class="sxs-lookup"><span data-stu-id="f4dc8-127">Y</span></span>        |
| <span data-ttu-id="f4dc8-128">Familie</span><span class="sxs-lookup"><span data-stu-id="f4dc8-128">Family</span></span>       | <span data-ttu-id="f4dc8-129">text</span><span class="sxs-lookup"><span data-stu-id="f4dc8-129">text</span></span> |     | <span data-ttu-id="f4dc8-130">N</span><span class="sxs-lookup"><span data-stu-id="f4dc8-130">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="f4dc8-131">Spalten</span><span class="sxs-lookup"><span data-stu-id="f4dc8-131">Columns</span></span>

<dl> <dt>

<span data-ttu-id="f4dc8-132"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Aktualisiert</span><span class="sxs-lookup"><span data-stu-id="f4dc8-132"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Upgraded</span></span>
</dt> <dd>

<span data-ttu-id="f4dc8-133">Das aktualisierte Feld ist ein beliebiger Bezeichner, um die Ziel Images mit einem aktualisierten Image des Produkts zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="f4dc8-133">The Upgraded field is an arbitrary identifier to connect the target images with an upgraded image of the product.</span></span>

</dd> <dt>

<span data-ttu-id="f4dc8-134"><span id="MsiPath"></span><span id="msipath"></span><span id="MSIPATH"></span>Msipath</span><span class="sxs-lookup"><span data-stu-id="f4dc8-134"><span id="MsiPath"></span><span id="msipath"></span><span id="MSIPATH"></span>MsiPath</span></span>
</dt> <dd>

<span data-ttu-id="f4dc8-135">Dieses Feld gibt den vollständigen Pfad, einschließlich des Datei namens, zum Speicherort der MSI-Datei für das aktualisierte Image an.</span><span class="sxs-lookup"><span data-stu-id="f4dc8-135">This field specifies the full path, including the file name, to the location of the .msi file for the upgraded image.</span></span> <span data-ttu-id="f4dc8-136">Dies ist der Speicherort der Quelldateien für das aktualisierte Image.</span><span class="sxs-lookup"><span data-stu-id="f4dc8-136">This is the location of the source files for the upgraded image.</span></span>

</dd> <dt>

<span data-ttu-id="f4dc8-137"><span id="PatchMsiPath"></span><span id="patchmsipath"></span><span id="PATCHMSIPATH"></span>Patchmsipath</span><span class="sxs-lookup"><span data-stu-id="f4dc8-137"><span id="PatchMsiPath"></span><span id="patchmsipath"></span><span id="PATCHMSIPATH"></span>PatchMsiPath</span></span>
</dt> <dd>

<span data-ttu-id="f4dc8-138">Der optionale patchmsipath verweist auf eine geänderte Kopie der aktualisierten Installations Datenbank, die zusätzliche, für den patchinstallations Vorgang spezifische Vorgänge enthält.</span><span class="sxs-lookup"><span data-stu-id="f4dc8-138">The optional patchMsiPath points to a modified copy of the upgraded installation database that contains additional authoring specific to the patch installation process.</span></span> <span data-ttu-id="f4dc8-139">Beispielsweise zusätzliche Dialogfelder oder benutzerdefinierte Aktionen, die von der [**Patch**](patch.md) -Eigenschaft abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="f4dc8-139">For example, additional dialogs or custom actions conditioned on the [**PATCH**](patch.md) property.</span></span>

</dd> <dt>

<span data-ttu-id="f4dc8-140"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPath</span><span class="sxs-lookup"><span data-stu-id="f4dc8-140"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span></span>
</dt> <dd>

<span data-ttu-id="f4dc8-141">Eine durch Semikolons getrennte Liste von Ordnern, die nach Symbol Dateien durchsucht werden sollen, die zur Optimierung der Generierung des binären Patches verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f4dc8-141">A semicolon delimited list of folders that are to be searched for symbol files that may be used to optimize the generation of the binary patch.</span></span> <span data-ttu-id="f4dc8-142">Beachten Sie, dass die Unterverzeichnisse der in diesem Feld angegebenen Ordner nicht durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="f4dc8-142">Note that the subdirectories of folders specified in this field are not searched.</span></span> <span data-ttu-id="f4dc8-143">Ein optimierter binärer Patch kann kleiner sein.</span><span class="sxs-lookup"><span data-stu-id="f4dc8-143">An optimized binary patch may be smaller.</span></span> <span data-ttu-id="f4dc8-144">Visual C++ müssen auf dem Computer installiert sein, der den Patch erzeugt und zum Erstellen der Symbol Dateien verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f4dc8-144">Visual C++ must be installed on the computer generating the patch and used to create the symbol files.</span></span> <span data-ttu-id="f4dc8-145">Dieses Feld ist optional, und das Installationsprogramm erstellt einen binären Patch, auch wenn keine Symbol Dateien angegeben sind oder wenn die Symbol Dateien nicht zum Patchwiz.dll verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="f4dc8-145">This field is optional, and the installer creates a binary patch even if no symbol files are specified or if the symbol files become unavailable to Patchwiz.dll.</span></span>

</dd> <dt>

<span data-ttu-id="f4dc8-146"><span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Ärzte</span><span class="sxs-lookup"><span data-stu-id="f4dc8-146"><span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Family</span></span>
</dt> <dd>

<span data-ttu-id="f4dc8-147">Fremdschlüssel in der [Tabelle "ImageFamilies](imagefamilies-table-patchwiz-dll-.md)".</span><span class="sxs-lookup"><span data-stu-id="f4dc8-147">Foreign key into the [ImageFamilies table](imagefamilies-table-patchwiz-dll-.md).</span></span> <span data-ttu-id="f4dc8-148">Jedes aktualisierte Image darf nur einer Familie angehören.</span><span class="sxs-lookup"><span data-stu-id="f4dc8-148">Each upgraded image must belong to only one family.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f4dc8-149">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f4dc8-149">Remarks</span></span>

<span data-ttu-id="f4dc8-150">Obwohl jedes aktualisierte Image in einer separaten Bild Familie gruppiert werden kann, kann das Gruppieren von aktualisierten Bildern, die gemeinsam Dateien gemeinsam nutzen, die. msp-Datei verkleinern.</span><span class="sxs-lookup"><span data-stu-id="f4dc8-150">Although each upgraded image can be grouped into a separate image family, grouping upgraded images that share files together may make the .msp smaller.</span></span>

<span data-ttu-id="f4dc8-151">Diese Tabelle akzeptiert Umgebungsvariablen als Pfade, die mit Version 4,0 von Patchwiz.dll beginnen.</span><span class="sxs-lookup"><span data-stu-id="f4dc8-151">This table accepts environment variables as paths beginning with version 4.0 of Patchwiz.dll.</span></span>

 

 



