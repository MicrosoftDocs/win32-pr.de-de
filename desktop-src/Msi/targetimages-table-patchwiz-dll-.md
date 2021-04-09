---
description: Die Tabelle TargetImages enthält Informationen zu den Ziel Images des Produkts. Ein Windows Installer Patch-Paket aktualisiert ein Zielimage in ein aktualisiertes Image.
ms.assetid: 4681715e-9918-4d7b-8f33-1cca2bb34eb7
title: TargetImages-Tabelle (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bbb8e7bae92fbc25b217808aaae709f079d65dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868451"
---
# <a name="targetimages-table-patchwizdll"></a><span data-ttu-id="7daa2-104">TargetImages-Tabelle (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="7daa2-104">TargetImages Table (Patchwiz.dll)</span></span>

<span data-ttu-id="7daa2-105">Die Tabelle TargetImages enthält Informationen zu den Ziel Images des Produkts.</span><span class="sxs-lookup"><span data-stu-id="7daa2-105">The TargetImages table contains information about the target images of the product.</span></span> <span data-ttu-id="7daa2-106">Ein Windows Installer Patch-Paket aktualisiert ein Zielimage in ein aktualisiertes Image.</span><span class="sxs-lookup"><span data-stu-id="7daa2-106">A Windows Installer patch package updates a target image into an upgraded image.</span></span>

<span data-ttu-id="7daa2-107">In jeder Datenbank der Patcherstellung (PCP-Datei) ist eine TargetImages-Tabelle erforderlich, die mindestens einen Datensatz enthält.</span><span class="sxs-lookup"><span data-stu-id="7daa2-107">A TargetImages table containing at least one record is required in every patch creation database (.pcp file).</span></span> <span data-ttu-id="7daa2-108">Diese Tabelle wird von der [uikreatepatchpackage](uicreatepatchpackage-patchwiz-dll-.md) -Funktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="7daa2-108">This table is used by the [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) function.</span></span>

<span data-ttu-id="7daa2-109">Die TargetImages-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="7daa2-109">The TargetImages table has the following columns.</span></span>



| <span data-ttu-id="7daa2-110">Spalte</span><span class="sxs-lookup"><span data-stu-id="7daa2-110">Column</span></span>                | <span data-ttu-id="7daa2-111">Typ</span><span class="sxs-lookup"><span data-stu-id="7daa2-111">Type</span></span>    | <span data-ttu-id="7daa2-112">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="7daa2-112">Key</span></span> | <span data-ttu-id="7daa2-113">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="7daa2-113">Nullable</span></span> |
|-----------------------|---------|-----|----------|
| <span data-ttu-id="7daa2-114">Ziel</span><span class="sxs-lookup"><span data-stu-id="7daa2-114">Target</span></span>                | <span data-ttu-id="7daa2-115">text</span><span class="sxs-lookup"><span data-stu-id="7daa2-115">text</span></span>    | <span data-ttu-id="7daa2-116">J</span><span class="sxs-lookup"><span data-stu-id="7daa2-116">Y</span></span>   | <span data-ttu-id="7daa2-117">N</span><span class="sxs-lookup"><span data-stu-id="7daa2-117">N</span></span>        |
| <span data-ttu-id="7daa2-118">Msipath</span><span class="sxs-lookup"><span data-stu-id="7daa2-118">MsiPath</span></span>               | <span data-ttu-id="7daa2-119">text</span><span class="sxs-lookup"><span data-stu-id="7daa2-119">text</span></span>    |     | <span data-ttu-id="7daa2-120">N</span><span class="sxs-lookup"><span data-stu-id="7daa2-120">N</span></span>        |
| <span data-ttu-id="7daa2-121">SymbolPath</span><span class="sxs-lookup"><span data-stu-id="7daa2-121">SymbolPaths</span></span>           | <span data-ttu-id="7daa2-122">text</span><span class="sxs-lookup"><span data-stu-id="7daa2-122">text</span></span>    |     | <span data-ttu-id="7daa2-123">J</span><span class="sxs-lookup"><span data-stu-id="7daa2-123">Y</span></span>        |
| <span data-ttu-id="7daa2-124">Upgraded</span><span class="sxs-lookup"><span data-stu-id="7daa2-124">Upgraded</span></span>              | <span data-ttu-id="7daa2-125">text</span><span class="sxs-lookup"><span data-stu-id="7daa2-125">text</span></span>    |     | <span data-ttu-id="7daa2-126">N</span><span class="sxs-lookup"><span data-stu-id="7daa2-126">N</span></span>        |
| <span data-ttu-id="7daa2-127">Auftrag</span><span class="sxs-lookup"><span data-stu-id="7daa2-127">Order</span></span>                 | <span data-ttu-id="7daa2-128">integer</span><span class="sxs-lookup"><span data-stu-id="7daa2-128">integer</span></span> |     | <span data-ttu-id="7daa2-129">N</span><span class="sxs-lookup"><span data-stu-id="7daa2-129">N</span></span>        |
| <span data-ttu-id="7daa2-130">Productvalidateflags</span><span class="sxs-lookup"><span data-stu-id="7daa2-130">ProductValidateFlags</span></span>  | <span data-ttu-id="7daa2-131">text</span><span class="sxs-lookup"><span data-stu-id="7daa2-131">text</span></span>    |     | <span data-ttu-id="7daa2-132">J</span><span class="sxs-lookup"><span data-stu-id="7daa2-132">Y</span></span>        |
| <span data-ttu-id="7daa2-133">Ignoremissingsrcfiles</span><span class="sxs-lookup"><span data-stu-id="7daa2-133">IgnoreMissingSrcFiles</span></span> | <span data-ttu-id="7daa2-134">integer</span><span class="sxs-lookup"><span data-stu-id="7daa2-134">integer</span></span> |     | <span data-ttu-id="7daa2-135">N</span><span class="sxs-lookup"><span data-stu-id="7daa2-135">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="7daa2-136">Spalten</span><span class="sxs-lookup"><span data-stu-id="7daa2-136">Columns</span></span>

<dl> <dt>

<span data-ttu-id="7daa2-137"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Spar</span><span class="sxs-lookup"><span data-stu-id="7daa2-137"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Target</span></span>
</dt> <dd>

<span data-ttu-id="7daa2-138">Der Bezeichner für ein Zielbild.</span><span class="sxs-lookup"><span data-stu-id="7daa2-138">Identifier for a target image.</span></span> <span data-ttu-id="7daa2-139">Das Patchpaket aktualisiert das in dieser Spalte angegebene Zielbild auf das aktualisierte Image, das in der aktualisierten Spalte angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="7daa2-139">The patch package updates the target image specified in this column to the upgraded image specified in the Upgraded column.</span></span> <span data-ttu-id="7daa2-140">Es gibt ein oder mehrere Ziel Images für jedes aktualisierte Image.</span><span class="sxs-lookup"><span data-stu-id="7daa2-140">There are one or more target images for each upgraded image.</span></span> <span data-ttu-id="7daa2-141">Das Zielimage muss ein vollständig dekomprimiertes Setup Abbild des Produkts sein, z. b. ein administratives Image oder ein nicht komprimiertes Setup Abbild auf einer CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="7daa2-141">The target image must be a fully uncompressed setup image of the product, such as an administrative image or an uncompressed setup image on a CD-ROM.</span></span> <span data-ttu-id="7daa2-142">Beachten Sie, dass die [uikreatepatchpackageex](uicreatepatchpackageex--patchwiz-dll-.md) -Funktion keine binären Patches für Dateien in kabinatendateien generiert.</span><span class="sxs-lookup"><span data-stu-id="7daa2-142">Note that the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function does not generate binary patches for files in cabinets.</span></span> <span data-ttu-id="7daa2-143">Der Wert in diesem Feld wird mit dem Wert im Feld aktualisiert verwendet, um die Namen der Transformationen zu generieren, die das Installationsprogramm dem Patchpaket hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="7daa2-143">The value in this field is used with the value in the Upgraded field to generate the names of the transforms that the installer adds to the patch package.</span></span>

</dd> <dt>

<span data-ttu-id="7daa2-144"><span id="MsiPath"></span><span id="msipath"></span><span id="MSIPATH"></span>Msipath</span><span class="sxs-lookup"><span data-stu-id="7daa2-144"><span id="MsiPath"></span><span id="msipath"></span><span id="MSIPATH"></span>MsiPath</span></span>
</dt> <dd>

<span data-ttu-id="7daa2-145">Dieses Feld gibt den vollständigen Pfad, einschließlich des Datei namens, zum Speicherort der MSI-Datei für das Zielbild an.</span><span class="sxs-lookup"><span data-stu-id="7daa2-145">This field specifies the full path, including the file name, to the location of the .msi file for the target image.</span></span> <span data-ttu-id="7daa2-146">Dies ist der Speicherort der Quelldateien für das Zielimage.</span><span class="sxs-lookup"><span data-stu-id="7daa2-146">This is the location of the source files for the target image.</span></span>

</dd> <dt>

<span data-ttu-id="7daa2-147"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPath</span><span class="sxs-lookup"><span data-stu-id="7daa2-147"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span></span>
</dt> <dd>

<span data-ttu-id="7daa2-148">Eine durch Semikolons getrennte Liste von Ordnern, die nach Symbol Dateien durchsucht werden sollen, die zur Optimierung der Generierung des binären Patches verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="7daa2-148">A semicolon delimited list of folders that are to be searched for symbol files that may be used to optimize the generation of the binary patch.</span></span> <span data-ttu-id="7daa2-149">Beachten Sie, dass die Unterverzeichnisse der in diesem Feld angegebenen Ordner nicht durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="7daa2-149">Note that the subdirectories of folders specified in this field are not searched.</span></span> <span data-ttu-id="7daa2-150">Ein optimierter binärer Patch kann kleiner sein.</span><span class="sxs-lookup"><span data-stu-id="7daa2-150">An optimized binary patch may be smaller.</span></span> <span data-ttu-id="7daa2-151">Microsoft Visual C++ müssen auf dem Computer installiert sein, der den Patch erzeugt und zum Erstellen der Symbol Dateien verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7daa2-151">Microsoft Visual C++ must be installed on the computer generating the patch and used to create the symbol files.</span></span> <span data-ttu-id="7daa2-152">Dieses Feld ist optional, und das Installationsprogramm erstellt einen binären Patch, auch wenn keine Symbol Dateien angegeben sind oder wenn die Symbol Dateien nicht zum Patchwiz.dll verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="7daa2-152">This field is optional, and the installer creates a binary patch even if no symbol files are specified or if the symbol files become unavailable to Patchwiz.dll.</span></span>

</dd> <dt>

<span data-ttu-id="7daa2-153"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7daa2-153"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Upgraded</span></span>
</dt> <dd>

<span data-ttu-id="7daa2-154">Fremdschlüssel für die aktualisierte Spalte der [UpgradedImages-Tabelle](upgradedimages-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="7daa2-154">Foreign key to the Upgraded column of the [UpgradedImages table](upgradedimages-table-patchwiz-dll-.md).</span></span> <span data-ttu-id="7daa2-155">Die [uikreatepatchpackageex](uicreatepatchpackageex--patchwiz-dll-.md) -Funktion ignoriert alle aktualisierten Images, auf die nicht durch mindestens einen Datensatz der TargetImages-Tabelle verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="7daa2-155">The [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function ignores any upgraded image that is not referenced by at least one record of the TargetImages table.</span></span>

</dd> <dt>

<span data-ttu-id="7daa2-156"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="7daa2-156"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Order</span></span>
</dt> <dd>

<span data-ttu-id="7daa2-157">Relative Reihenfolge des zielbilds.</span><span class="sxs-lookup"><span data-stu-id="7daa2-157">Relative order of the target image.</span></span> <span data-ttu-id="7daa2-158">Da mehrere Ziele für ein aktualisiertes Image gepatcht werden können, bietet das Feld Order die Möglichkeit, die Transformationen in der Liste patchtransformationen zu sequenzieren.</span><span class="sxs-lookup"><span data-stu-id="7daa2-158">Because multiple targets can be patched to an upgraded image, the Order field provides a means to sequence the transforms in the patch transforms list.</span></span> <span data-ttu-id="7daa2-159">Im Allgemeinen ist die Reihenfolge vom ältesten zum neuesten Image.</span><span class="sxs-lookup"><span data-stu-id="7daa2-159">Commonly, the order is from oldest to newest image.</span></span>

</dd> <dt>

<span data-ttu-id="7daa2-160"><span id="ProductValidateFlags"></span><span id="productvalidateflags"></span><span id="PRODUCTVALIDATEFLAGS"></span>Productvalidateflags</span><span class="sxs-lookup"><span data-stu-id="7daa2-160"><span id="ProductValidateFlags"></span><span id="productvalidateflags"></span><span id="PRODUCTVALIDATEFLAGS"></span>ProductValidateFlags</span></span>
</dt> <dd>

<span data-ttu-id="7daa2-161">Das Feld productvalidateflags dient zum Angeben der Produkt Überprüfung, um zu vermeiden, dass irrelevante Transformationen angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="7daa2-161">The ProductValidateFlags field is used to specify product checking to avoid applying irrelevant transforms.</span></span> <span data-ttu-id="7daa2-162">Der in diesem Feld eingegebene Wert muss eine 8-stellige hexadezimal Zahl und einer der gültigen Werte für den *ivalidation* -Parameter der [**msikreatetransformsummaryinfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) -Funktion sein.</span><span class="sxs-lookup"><span data-stu-id="7daa2-162">The value entered in this field must be an 8-digit hex integer and one of the valid values for the *iValidation* parameter of the [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) function.</span></span> <span data-ttu-id="7daa2-163">Der Standardwert ist 0x00000922, der gleich **msitransform Validate \_ \_ Updateversion** msitransform Validate  +  **\_ \_ netzwequalbaseversion**  +  **msitransform \_ Validate \_ UpgradeCode**  +  **msitransform \_ Validate \_ Product** ist.</span><span class="sxs-lookup"><span data-stu-id="7daa2-163">The default value is 0x00000922 which equals **MSITRANSFORM\_VALIDATE\_UPDATEVERSION** + **MSITRANSFORM\_VALIDATE\_NEWEQUALBASEVERSION** + **MSITRANSFORM\_VALIDATE\_UPGRADECODE** + **MSITRANSFORM\_VALIDATE\_PRODUCT**.</span></span>

</dd> <dt>

<span data-ttu-id="7daa2-164"><span id="IgnoreMissingSrcFiles"></span><span id="ignoremissingsrcfiles"></span><span id="IGNOREMISSINGSRCFILES"></span>Ignoremissingsrcfiles</span><span class="sxs-lookup"><span data-stu-id="7daa2-164"><span id="IgnoreMissingSrcFiles"></span><span id="ignoremissingsrcfiles"></span><span id="IGNOREMISSINGSRCFILES"></span>IgnoreMissingSrcFiles</span></span>
</dt> <dd>

<span data-ttu-id="7daa2-165">Wenn dieses Feld auf einen Wert ungleich 0 (null) festgelegt ist, werden Dateien, die im Zielbild fehlen, vom Installationsprogramm ignoriert und während des Patchens unverändert gelassen.</span><span class="sxs-lookup"><span data-stu-id="7daa2-165">If this field is set to a nonzero value, files missing from the target image are ignored by the installer and left unchanged during patching.</span></span> <span data-ttu-id="7daa2-166">Dadurch können Patches erstellt werden, ohne dass das gesamte Bild erforderlich ist. Es sind nur die geänderten Dateien des Produkts und die MSI-Datei erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7daa2-166">This enables patches to be made without requiring the entire image; only the changed files of the product and the .msi file are required.</span></span> <span data-ttu-id="7daa2-167">Dadurch kann die Zeit, die zum Generieren des Patches erforderlich ist, reduziert werden.</span><span class="sxs-lookup"><span data-stu-id="7daa2-167">This may reduce the time required to generate the patch.</span></span>

> [!Note]  
> <span data-ttu-id="7daa2-168">Verwenden Sie nicht den ignoremissingsrcfiles-Wert mit trustmsi, der in der [Properties-Tabelle](properties-table-patchwiz-dll-.md)auf 1 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7daa2-168">Do not use the IgnoreMissingSrcFiles value with TrustMsi set to 1 in the [Properties Table](properties-table-patchwiz-dll-.md).</span></span>

 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7daa2-169">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7daa2-169">Remarks</span></span>

<span data-ttu-id="7daa2-170">Diese Tabelle akzeptiert Umgebungsvariablen als Pfade, die mit Version 4,0 von Patchwiz.dll beginnen.</span><span class="sxs-lookup"><span data-stu-id="7daa2-170">This table accepts environment variables as paths beginning with version 4.0 of Patchwiz.dll.</span></span>

 

 



