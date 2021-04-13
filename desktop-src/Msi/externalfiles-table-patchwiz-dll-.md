---
description: Die externalfiles-Tabelle enthält Informationen zu bestimmten Dateien, die nicht Teil eines regulären zielbilds sind.
ms.assetid: c75591c2-5266-4a99-8104-53815f6550e2
title: Externalfiles-Tabelle (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71f0002961408be9f43685ef40cd2ccff729e48b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528196"
---
# <a name="externalfiles-table-patchwizdll"></a><span data-ttu-id="04842-103">Externalfiles-Tabelle (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="04842-103">ExternalFiles Table (Patchwiz.dll)</span></span>

<span data-ttu-id="04842-104">Die externalfiles-Tabelle enthält Informationen zu bestimmten Dateien, die nicht Teil eines regulären zielbilds sind.</span><span class="sxs-lookup"><span data-stu-id="04842-104">The ExternalFiles table contains information about specific files that are not part of a regular target image.</span></span> <span data-ttu-id="04842-105">Diese Dateien können in Produkten vorhanden sein, die von einem anderen Produkt, Upgrade oder Patch aktualisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="04842-105">These files may exist in products that have been updated by another product, upgrade, or patch.</span></span> <span data-ttu-id="04842-106">Diese Tabelle ist in der Datenbank für die Patcherstellung (PCP-Datei) optional und wird von der [uikreatepatchpackageex](uicreatepatchpackageex--patchwiz-dll-.md) -Funktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="04842-106">This table is optional in the patch creation database (.pcp file) and is used by the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function.</span></span>

<span data-ttu-id="04842-107">Die externalfiles-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="04842-107">The ExternalFiles table has the following columns.</span></span>



| <span data-ttu-id="04842-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="04842-108">Column</span></span>        | <span data-ttu-id="04842-109">Typ</span><span class="sxs-lookup"><span data-stu-id="04842-109">Type</span></span>    | <span data-ttu-id="04842-110">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="04842-110">Key</span></span> | <span data-ttu-id="04842-111">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="04842-111">Nullable</span></span> |
|---------------|---------|-----|----------|
| <span data-ttu-id="04842-112">Familie</span><span class="sxs-lookup"><span data-stu-id="04842-112">Family</span></span>        | <span data-ttu-id="04842-113">text</span><span class="sxs-lookup"><span data-stu-id="04842-113">text</span></span>    | <span data-ttu-id="04842-114">J</span><span class="sxs-lookup"><span data-stu-id="04842-114">Y</span></span>   | <span data-ttu-id="04842-115">N</span><span class="sxs-lookup"><span data-stu-id="04842-115">N</span></span>        |
| <span data-ttu-id="04842-116">FTK</span><span class="sxs-lookup"><span data-stu-id="04842-116">FTK</span></span>           | <span data-ttu-id="04842-117">text</span><span class="sxs-lookup"><span data-stu-id="04842-117">text</span></span>    | <span data-ttu-id="04842-118">J</span><span class="sxs-lookup"><span data-stu-id="04842-118">Y</span></span>   | <span data-ttu-id="04842-119">N</span><span class="sxs-lookup"><span data-stu-id="04842-119">N</span></span>        |
| <span data-ttu-id="04842-120">FilePath</span><span class="sxs-lookup"><span data-stu-id="04842-120">FilePath</span></span>      | <span data-ttu-id="04842-121">text</span><span class="sxs-lookup"><span data-stu-id="04842-121">text</span></span>    | <span data-ttu-id="04842-122">J</span><span class="sxs-lookup"><span data-stu-id="04842-122">Y</span></span>   | <span data-ttu-id="04842-123">N</span><span class="sxs-lookup"><span data-stu-id="04842-123">N</span></span>        |
| <span data-ttu-id="04842-124">SymbolPath</span><span class="sxs-lookup"><span data-stu-id="04842-124">SymbolPaths</span></span>   | <span data-ttu-id="04842-125">text</span><span class="sxs-lookup"><span data-stu-id="04842-125">text</span></span>    |     | <span data-ttu-id="04842-126">J</span><span class="sxs-lookup"><span data-stu-id="04842-126">Y</span></span>        |
| <span data-ttu-id="04842-127">Ignoreoffsets</span><span class="sxs-lookup"><span data-stu-id="04842-127">IgnoreOffsets</span></span> | <span data-ttu-id="04842-128">text</span><span class="sxs-lookup"><span data-stu-id="04842-128">text</span></span>    |     | <span data-ttu-id="04842-129">J</span><span class="sxs-lookup"><span data-stu-id="04842-129">Y</span></span>        |
| <span data-ttu-id="04842-130">Ignorelengths</span><span class="sxs-lookup"><span data-stu-id="04842-130">IgnoreLengths</span></span> | <span data-ttu-id="04842-131">text</span><span class="sxs-lookup"><span data-stu-id="04842-131">text</span></span>    |     | <span data-ttu-id="04842-132">J</span><span class="sxs-lookup"><span data-stu-id="04842-132">Y</span></span>        |
| <span data-ttu-id="04842-133">Retainoffsets</span><span class="sxs-lookup"><span data-stu-id="04842-133">RetainOffsets</span></span> | <span data-ttu-id="04842-134">text</span><span class="sxs-lookup"><span data-stu-id="04842-134">text</span></span>    |     | <span data-ttu-id="04842-135">N</span><span class="sxs-lookup"><span data-stu-id="04842-135">N</span></span>        |
| <span data-ttu-id="04842-136">Auftrag</span><span class="sxs-lookup"><span data-stu-id="04842-136">Order</span></span>         | <span data-ttu-id="04842-137">integer</span><span class="sxs-lookup"><span data-stu-id="04842-137">integer</span></span> |     | <span data-ttu-id="04842-138">J</span><span class="sxs-lookup"><span data-stu-id="04842-138">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="04842-139">Spalten</span><span class="sxs-lookup"><span data-stu-id="04842-139">Columns</span></span>

<dl> <dt>

<span data-ttu-id="04842-140"><span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Ärzte</span><span class="sxs-lookup"><span data-stu-id="04842-140"><span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Family</span></span>
</dt> <dd>

<span data-ttu-id="04842-141">Fremdschlüssel für die Spalte "Family" der [Tabelle "ImageFamilies" (Patchwiz.dll)](imagefamilies-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="04842-141">Foreign key to the Family column of the [ImageFamilies Table (Patchwiz.dll)](imagefamilies-table-patchwiz-dll-.md).</span></span>

</dd> <dt>

<span data-ttu-id="04842-142"><span id="FTK"></span><span id="ftk"></span>FTK</span><span class="sxs-lookup"><span data-stu-id="04842-142"><span id="FTK"></span><span id="ftk"></span>FTK</span></span>
</dt> <dd>

<span data-ttu-id="04842-143">Fremdschlüssel in die [Dateitabelle](file-table.md) der MSI-Datei des aktualisierten Abbilds.</span><span class="sxs-lookup"><span data-stu-id="04842-143">Foreign key into [File table](file-table.md) of the .msi file of the upgraded image.</span></span>

</dd> <dt>

<span data-ttu-id="04842-144"><span id="FilePath"></span><span id="filepath"></span><span id="FILEPATH"></span>FilePath</span><span class="sxs-lookup"><span data-stu-id="04842-144"><span id="FilePath"></span><span id="filepath"></span><span id="FILEPATH"></span>FilePath</span></span>
</dt> <dd>

<span data-ttu-id="04842-145">Vollständiger Pfad der externen Datei, einschließlich des Datei namens.</span><span class="sxs-lookup"><span data-stu-id="04842-145">Full path of the external file including the file name.</span></span> <span data-ttu-id="04842-146">Das Feld "filePath" wird verwendet, um die in der FTK-Spalte angegebene Datei zu suchen.</span><span class="sxs-lookup"><span data-stu-id="04842-146">FilePath field is used to locate the file specified in the FTK column.</span></span>

</dd> <dt>

<span data-ttu-id="04842-147"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPath</span><span class="sxs-lookup"><span data-stu-id="04842-147"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span></span>
</dt> <dd>

<span data-ttu-id="04842-148">Vollständiger Pfad für Symbol Dateien der Datei, die in der FTK-Spalte angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="04842-148">Full path searched for symbol files of the file specified in the FTK column.</span></span>

</dd> <dt>

<span data-ttu-id="04842-149"><span id="IgnoreOffsets"></span><span id="ignoreoffsets"></span><span id="IGNOREOFFSETS"></span>Ignoreoffsets</span><span class="sxs-lookup"><span data-stu-id="04842-149"><span id="IgnoreOffsets"></span><span id="ignoreoffsets"></span><span id="IGNOREOFFSETS"></span>IgnoreOffsets</span></span>
</dt> <dd>

<span data-ttu-id="04842-150">Der Wert in diesem Feld ist eine durch Trennzeichen getrennte Liste von Bereichs Offset Zahlen für die Bereiche, die in der externen Datei ignoriert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="04842-150">The value in this field is a comma-delimited list of range offset numbers for the ranges to be ignored in the external file.</span></span> <span data-ttu-id="04842-151">Die Reihenfolge und die Anzahl der Bereiche in der Liste müssen mit den Elementen in der Spalte ignorelengths identisch sein.</span><span class="sxs-lookup"><span data-stu-id="04842-151">The order and number of the ranges in the list must match the items in the IgnoreLengths column.</span></span> <span data-ttu-id="04842-152">Diese Spalte ist optional.</span><span class="sxs-lookup"><span data-stu-id="04842-152">This column is optional.</span></span>

<span data-ttu-id="04842-153">Die Werte können Decimal oder hexadezimal sein.</span><span class="sxs-lookup"><span data-stu-id="04842-153">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="04842-154">[Patchwiz.dll](patchwiz-dll.md) behandelt den Wert als hexadezimal, wenn der Wert "0x" vorangestellt ist.</span><span class="sxs-lookup"><span data-stu-id="04842-154">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="04842-155">Die Spalten sind Zeichen folgen Spalten, und Patchwiz.dll konvertiert die Werte in ulongs.</span><span class="sxs-lookup"><span data-stu-id="04842-155">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> <dt>

<span data-ttu-id="04842-156"><span id="IgnoreLengths"></span><span id="ignorelengths"></span><span id="IGNORELENGTHS"></span>Ignorelengths</span><span class="sxs-lookup"><span data-stu-id="04842-156"><span id="IgnoreLengths"></span><span id="ignorelengths"></span><span id="IGNORELENGTHS"></span>IgnoreLengths</span></span>
</dt> <dd>

<span data-ttu-id="04842-157">Der Wert in diesem Feld ist eine durch Trennzeichen getrennte Liste von Bereichs Längen in Bytes, die in der externen Datei ignoriert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="04842-157">The value in this field is a comma-delimited list of range lengths in bytes for the ranges to be ignored in the external file.</span></span> <span data-ttu-id="04842-158">Die Reihenfolge und die Anzahl der Bereiche in der Liste müssen mit den Elementen in der ignoreoffsets-Spalte identisch sein.</span><span class="sxs-lookup"><span data-stu-id="04842-158">The order and number of the ranges in the list must match the items in the IgnoreOffsets column.</span></span> <span data-ttu-id="04842-159">Diese Spalte ist optional.</span><span class="sxs-lookup"><span data-stu-id="04842-159">This column is optional.</span></span>

<span data-ttu-id="04842-160">Die Werte können Decimal oder hexadezimal sein.</span><span class="sxs-lookup"><span data-stu-id="04842-160">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="04842-161">[Patchwiz.dll](patchwiz-dll.md) behandelt den Wert als hexadezimal, wenn der Wert "0x" vorangestellt ist.</span><span class="sxs-lookup"><span data-stu-id="04842-161">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="04842-162">Die Spalten sind Zeichen folgen Spalten, und Patchwiz.dll konvertiert die Werte in ulongs.</span><span class="sxs-lookup"><span data-stu-id="04842-162">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> <dt>

<span data-ttu-id="04842-163"><span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>Retainoffsets</span><span class="sxs-lookup"><span data-stu-id="04842-163"><span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets</span></span>
</dt> <dd>

<span data-ttu-id="04842-164">Der Wert in diesem Feld ist eine durch Trennzeichen getrennte Liste von Bereichs Offset Zahlen für die Bereiche, die in der externen Datei aufbewahrt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="04842-164">The value in this field is a comma-delimited list of range offset numbers for the ranges to be retained in the External file.</span></span> <span data-ttu-id="04842-165">Die Reihenfolge und die Anzahl der Bereiche in der Liste müssen mit den Elementen in der Spalte "retainoffsets" des entsprechenden Datensatzes in der [Tabelle "familyfileranges" (Patchwiz.dll)](familyfileranges-table-patchwiz-dll-.md)übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="04842-165">The order and number of the ranges in the list must match the items in the RetainOffsets column of the corresponding record in the [FamilyFileRanges Table (Patchwiz.dll)](familyfileranges-table-patchwiz-dll-.md).</span></span>

<span data-ttu-id="04842-166">Die Werte können Decimal oder hexadezimal sein.</span><span class="sxs-lookup"><span data-stu-id="04842-166">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="04842-167">[Patchwiz.dll](patchwiz-dll.md) behandelt den Wert als hexadezimal, wenn der Wert "0x" vorangestellt ist.</span><span class="sxs-lookup"><span data-stu-id="04842-167">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="04842-168">Die Spalten sind Zeichen folgen Spalten, und Patchwiz.dll konvertiert die Werte in ulongs.</span><span class="sxs-lookup"><span data-stu-id="04842-168">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> <dt>

<span data-ttu-id="04842-169"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="04842-169"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Order</span></span>
</dt> <dd>

<span data-ttu-id="04842-170">Wenn für dieselbe externe Datei mindestens zwei Versionen angegeben sind, enthält die Tabelle möglicherweise mehrere Datensätze mit übereinstimmenden Werten in den Feldern FTK und Family.</span><span class="sxs-lookup"><span data-stu-id="04842-170">If two or more versions are specified for the same external file, the table may contain multiple records with matching values in the FTK and Family fields.</span></span> <span data-ttu-id="04842-171">In diesem Fall kann das Feld Order die Reihenfolge externer Dateien angeben, die beim Erstellen des Patches verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="04842-171">In this case, the Order field may specify the order of external files to use when creating the patch.</span></span> <span data-ttu-id="04842-172">Die Reihenfolge ist von der ältesten zur neuesten Version.</span><span class="sxs-lookup"><span data-stu-id="04842-172">The order is from the oldest to the most recent version.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="04842-173">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="04842-173">Remarks</span></span>

<span data-ttu-id="04842-174">Diese Tabelle akzeptiert Umgebungsvariablen als Pfade, die mit Version 4,0 von Patchwiz.dll beginnen.</span><span class="sxs-lookup"><span data-stu-id="04842-174">This table accepts environment variables as paths beginning with version 4.0 of Patchwiz.dll.</span></span>

## <a name="related-topics"></a><span data-ttu-id="04842-175">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="04842-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04842-176">Patchen ausgewählter Bereiche einer Datei</span><span class="sxs-lookup"><span data-stu-id="04842-176">Patching Selected Regions of a File</span></span>](patching-selected-regions-of-a-file.md)
</dt> </dl>

 

 



