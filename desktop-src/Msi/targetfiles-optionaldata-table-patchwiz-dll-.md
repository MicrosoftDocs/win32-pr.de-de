---
description: Die Tabelle "targetfiles \_ OptionalData" enthält Informationen zu bestimmten Dateien in einem Zielimage. Diese Tabelle ist in der Datenbank für die Patcherstellung (PCP-Datei) optional und wird von der uikreatepatchpackageex-Funktion verwendet.
ms.assetid: 577b1674-1e44-42e1-b011-c0fb561b514c
title: TargetFiles_OptionalData Tabelle (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 859ac2e03f68c28eff5ebf7f5afa2bf53ab69299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960148"
---
# <a name="targetfiles_optionaldata-table-patchwizdll"></a><span data-ttu-id="c9516-104">Targetfiles \_ (OptionalData-Tabelle) (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="c9516-104">TargetFiles\_OptionalData Table (Patchwiz.dll)</span></span>

<span data-ttu-id="c9516-105">Die Tabelle "targetfiles \_ OptionalData" enthält Informationen zu bestimmten Dateien in einem Zielimage.</span><span class="sxs-lookup"><span data-stu-id="c9516-105">The TargetFiles\_OptionalData table contains information about specific files in a target image.</span></span> <span data-ttu-id="c9516-106">Diese Tabelle ist in der Datenbank für die Patcherstellung (PCP-Datei) optional und wird von der [uikreatepatchpackageex](uicreatepatchpackageex--patchwiz-dll-.md) -Funktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="c9516-106">This table is optional in the patch creation database (.pcp file) and is used by the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function.</span></span>

<span data-ttu-id="c9516-107">Die Tabelle "targetfiles \_ OptionalData" enthält die folgenden Spalten.</span><span class="sxs-lookup"><span data-stu-id="c9516-107">The TargetFiles\_OptionalData table has the following columns.</span></span>



| <span data-ttu-id="c9516-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="c9516-108">Column</span></span>        | <span data-ttu-id="c9516-109">Typ</span><span class="sxs-lookup"><span data-stu-id="c9516-109">Type</span></span> | <span data-ttu-id="c9516-110">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="c9516-110">Key</span></span> | <span data-ttu-id="c9516-111">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="c9516-111">Nullable</span></span> |
|---------------|------|-----|----------|
| <span data-ttu-id="c9516-112">Ziel</span><span class="sxs-lookup"><span data-stu-id="c9516-112">Target</span></span>        | <span data-ttu-id="c9516-113">text</span><span class="sxs-lookup"><span data-stu-id="c9516-113">text</span></span> | <span data-ttu-id="c9516-114">J</span><span class="sxs-lookup"><span data-stu-id="c9516-114">Y</span></span>   | <span data-ttu-id="c9516-115">N</span><span class="sxs-lookup"><span data-stu-id="c9516-115">N</span></span>        |
| <span data-ttu-id="c9516-116">FTK</span><span class="sxs-lookup"><span data-stu-id="c9516-116">FTK</span></span>           | <span data-ttu-id="c9516-117">text</span><span class="sxs-lookup"><span data-stu-id="c9516-117">text</span></span> | <span data-ttu-id="c9516-118">J</span><span class="sxs-lookup"><span data-stu-id="c9516-118">Y</span></span>   | <span data-ttu-id="c9516-119">N</span><span class="sxs-lookup"><span data-stu-id="c9516-119">N</span></span>        |
| <span data-ttu-id="c9516-120">SymbolPath</span><span class="sxs-lookup"><span data-stu-id="c9516-120">SymbolPaths</span></span>   | <span data-ttu-id="c9516-121">text</span><span class="sxs-lookup"><span data-stu-id="c9516-121">text</span></span> |     | <span data-ttu-id="c9516-122">J</span><span class="sxs-lookup"><span data-stu-id="c9516-122">Y</span></span>        |
| <span data-ttu-id="c9516-123">Ignoreoffsets</span><span class="sxs-lookup"><span data-stu-id="c9516-123">IgnoreOffsets</span></span> | <span data-ttu-id="c9516-124">text</span><span class="sxs-lookup"><span data-stu-id="c9516-124">text</span></span> |     | <span data-ttu-id="c9516-125">J</span><span class="sxs-lookup"><span data-stu-id="c9516-125">Y</span></span>        |
| <span data-ttu-id="c9516-126">Ignorelengths</span><span class="sxs-lookup"><span data-stu-id="c9516-126">IgnoreLengths</span></span> | <span data-ttu-id="c9516-127">text</span><span class="sxs-lookup"><span data-stu-id="c9516-127">text</span></span> |     | <span data-ttu-id="c9516-128">J</span><span class="sxs-lookup"><span data-stu-id="c9516-128">Y</span></span>        |
| <span data-ttu-id="c9516-129">Retainoffsets</span><span class="sxs-lookup"><span data-stu-id="c9516-129">RetainOffsets</span></span> | <span data-ttu-id="c9516-130">text</span><span class="sxs-lookup"><span data-stu-id="c9516-130">text</span></span> |     | <span data-ttu-id="c9516-131">J</span><span class="sxs-lookup"><span data-stu-id="c9516-131">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="c9516-132">Spalten</span><span class="sxs-lookup"><span data-stu-id="c9516-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="c9516-133"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Spar</span><span class="sxs-lookup"><span data-stu-id="c9516-133"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Target</span></span>
</dt> <dd>

<span data-ttu-id="c9516-134">Fremdschlüssel für die Ziel Spalte der [TargetImages-Tabelle (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="c9516-134">Foreign key to the Target column of the [TargetImages Table (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md).</span></span>

</dd> <dt>

<span data-ttu-id="c9516-135"><span id="FTK"></span><span id="ftk"></span>FTK</span><span class="sxs-lookup"><span data-stu-id="c9516-135"><span id="FTK"></span><span id="ftk"></span>FTK</span></span>
</dt> <dd>

<span data-ttu-id="c9516-136">Fremdschlüssel in die [Dateitabelle](file-table.md) des zielbilds.</span><span class="sxs-lookup"><span data-stu-id="c9516-136">Foreign key into the [File table](file-table.md) of target image.</span></span>

</dd> <dt>

<span data-ttu-id="c9516-137"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPath</span><span class="sxs-lookup"><span data-stu-id="c9516-137"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span></span>
</dt> <dd>

<span data-ttu-id="c9516-138">Der Wert in diesem Feld wird der durch Semikolons getrennten Liste der Ordner in der SymbolPath-Spalte der [TargetImages-Tabelle (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md) hinzugefügt, wenn der Patch generiert wird, und kann zum Hinzufügen von Symbol Dateien für eine bestimmte Datei verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c9516-138">The value in this field is added to the semicolon delimited list of folders in the SymbolPaths column of the [TargetImages Table (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md) when the patch is generated, and can be used to add symbol files for a specific file.</span></span>

</dd> <dt>

<span data-ttu-id="c9516-139"><span id="IgnoreOffsets"></span><span id="ignoreoffsets"></span><span id="IGNOREOFFSETS"></span>Ignoreoffsets</span><span class="sxs-lookup"><span data-stu-id="c9516-139"><span id="IgnoreOffsets"></span><span id="ignoreoffsets"></span><span id="IGNOREOFFSETS"></span>IgnoreOffsets</span></span>
</dt> <dd>

<span data-ttu-id="c9516-140">Der Wert in diesem Feld ist eine durch Trennzeichen getrennte Liste von Bereichs Offset Zahlen für die Bereiche, die in der Zieldatei ignoriert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c9516-140">The value in this field is a comma delimited list of range offset numbers for the ranges to be ignored in the Target file.</span></span> <span data-ttu-id="c9516-141">Die Reihenfolge und die Anzahl der Bereiche in der Liste müssen mit den Elementen in der Spalte ignorelengths identisch sein.</span><span class="sxs-lookup"><span data-stu-id="c9516-141">The order and number of the ranges in the list must match the items in the IgnoreLengths column.</span></span> <span data-ttu-id="c9516-142">Diese Spalte ist optional.</span><span class="sxs-lookup"><span data-stu-id="c9516-142">This column is optional.</span></span>

<span data-ttu-id="c9516-143">Die Werte können Decimal oder hexadezimal sein.</span><span class="sxs-lookup"><span data-stu-id="c9516-143">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="c9516-144">[Patchwiz.dll](patchwiz-dll.md) behandelt den Wert als hexadezimal, wenn der Wert "0x" vorangestellt ist.</span><span class="sxs-lookup"><span data-stu-id="c9516-144">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="c9516-145">Die Spalten sind Zeichen folgen Spalten, und Patchwiz.dll konvertiert die Werte in ulongs.</span><span class="sxs-lookup"><span data-stu-id="c9516-145">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> <dt>

<span data-ttu-id="c9516-146"><span id="IgnoreLengths"></span><span id="ignorelengths"></span><span id="IGNORELENGTHS"></span>Ignorelengths</span><span class="sxs-lookup"><span data-stu-id="c9516-146"><span id="IgnoreLengths"></span><span id="ignorelengths"></span><span id="IGNORELENGTHS"></span>IgnoreLengths</span></span>
</dt> <dd>

<span data-ttu-id="c9516-147">Der Wert in diesem Feld ist eine durch Trennzeichen getrennte Liste von Bereichs Längen in Bytes für die Bereiche, die in der Zieldatei ignoriert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c9516-147">The value in this field is a comma delimited list of range lengths in bytes for the ranges to be ignored in the Target file.</span></span> <span data-ttu-id="c9516-148">Die Reihenfolge und die Anzahl der Bereiche in der Liste müssen mit den Elementen in der ignoreoffsets-Spalte identisch sein.</span><span class="sxs-lookup"><span data-stu-id="c9516-148">The order and number of the ranges in the list must match the items in the IgnoreOffsets column.</span></span> <span data-ttu-id="c9516-149">Diese Spalte ist optional.</span><span class="sxs-lookup"><span data-stu-id="c9516-149">This column is optional.</span></span>

<span data-ttu-id="c9516-150">Die Werte können Decimal oder hexadezimal sein.</span><span class="sxs-lookup"><span data-stu-id="c9516-150">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="c9516-151">[Patchwiz.dll](patchwiz-dll.md) behandelt den Wert als hexadezimal, wenn der Wert "0x" vorangestellt ist.</span><span class="sxs-lookup"><span data-stu-id="c9516-151">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="c9516-152">Die Spalten sind Zeichen folgen Spalten, und Patchwiz.dll konvertiert die Werte in ulongs.</span><span class="sxs-lookup"><span data-stu-id="c9516-152">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> <dt>

<span data-ttu-id="c9516-153"><span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>Retainoffsets</span><span class="sxs-lookup"><span data-stu-id="c9516-153"><span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets</span></span>
</dt> <dd>

<span data-ttu-id="c9516-154">Der Wert in diesem Feld ist eine durch Trennzeichen getrennte Liste von Bereichs Offset Zahlen für die Bereiche, die in der Zieldatei beibehalten werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c9516-154">The value in this field is a comma delimited list of range offset numbers for the ranges to be retained in the Target file.</span></span> <span data-ttu-id="c9516-155">Die Reihenfolge und die Anzahl der Bereiche in der Liste müssen mit den Elementen in der Spalte "retainoffsets" des entsprechenden Datensatzes in der [Tabelle "familyfileranges" (Patchwiz.dll)](familyfileranges-table-patchwiz-dll-.md) übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="c9516-155">The order and number of the ranges in the list must match the items in the RetainOffsets column of the corresponding record in the [FamilyFileRanges Table (Patchwiz.dll)](familyfileranges-table-patchwiz-dll-.md)</span></span>

<span data-ttu-id="c9516-156">Die Werte können Decimal oder hexadezimal sein.</span><span class="sxs-lookup"><span data-stu-id="c9516-156">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="c9516-157">[Patchwiz.dll](patchwiz-dll.md) behandelt den Wert als hexadezimal, wenn der Wert "0x" vorangestellt ist.</span><span class="sxs-lookup"><span data-stu-id="c9516-157">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="c9516-158">Die Spalten sind Zeichen folgen Spalten, und Patchwiz.dll konvertiert die Werte in ulongs.</span><span class="sxs-lookup"><span data-stu-id="c9516-158">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="c9516-159">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c9516-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9516-160">Patchen ausgewählter Bereiche einer Datei</span><span class="sxs-lookup"><span data-stu-id="c9516-160">Patching Selected Regions of a File</span></span>](patching-selected-regions-of-a-file.md)
</dt> </dl>

 

 



