---
description: Die familyfileranges-Tabelle enthält Informationen zu bestimmten Dateien eines aktualisierten Bilds mit Bereichen, die nie überschrieben werden sollten.
ms.assetid: 2e77605a-d909-4a17-977c-18281a96c36c
title: Familyfileranges-Tabelle (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2940d45d82efae3e61842ee0f6b4e46e3f77ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130677"
---
# <a name="familyfileranges-table-patchwizdll"></a><span data-ttu-id="6ab37-103">Familyfileranges-Tabelle (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="6ab37-103">FamilyFileRanges Table (Patchwiz.dll)</span></span>

<span data-ttu-id="6ab37-104">Die familyfileranges-Tabelle enthält Informationen zu bestimmten Dateien eines aktualisierten Bilds mit Bereichen, die nie überschrieben werden sollten.</span><span class="sxs-lookup"><span data-stu-id="6ab37-104">The FamilyFileRanges table contains information about particular files of an upgraded image with ranges that should never be overwritten.</span></span> <span data-ttu-id="6ab37-105">Diese Tabelle ist in der Datenbank für die Patcherstellung (PCP-Datei) optional und wird von der [uikreatepatchpackageex](uicreatepatchpackageex--patchwiz-dll-.md) -Funktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="6ab37-105">This table is optional in the patch creation database (.pcp file) and is used by the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function.</span></span>

<span data-ttu-id="6ab37-106">Die familyfileranges-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="6ab37-106">The FamilyFileRanges table has the following columns.</span></span>



| <span data-ttu-id="6ab37-107">Spalte</span><span class="sxs-lookup"><span data-stu-id="6ab37-107">Column</span></span>        | <span data-ttu-id="6ab37-108">Typ</span><span class="sxs-lookup"><span data-stu-id="6ab37-108">Type</span></span> | <span data-ttu-id="6ab37-109">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="6ab37-109">Key</span></span> | <span data-ttu-id="6ab37-110">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="6ab37-110">Nullable</span></span> |
|---------------|------|-----|----------|
| <span data-ttu-id="6ab37-111">Familie</span><span class="sxs-lookup"><span data-stu-id="6ab37-111">Family</span></span>        | <span data-ttu-id="6ab37-112">text</span><span class="sxs-lookup"><span data-stu-id="6ab37-112">text</span></span> | <span data-ttu-id="6ab37-113">J</span><span class="sxs-lookup"><span data-stu-id="6ab37-113">Y</span></span>   | <span data-ttu-id="6ab37-114">N</span><span class="sxs-lookup"><span data-stu-id="6ab37-114">N</span></span>        |
| <span data-ttu-id="6ab37-115">FTK</span><span class="sxs-lookup"><span data-stu-id="6ab37-115">FTK</span></span>           | <span data-ttu-id="6ab37-116">text</span><span class="sxs-lookup"><span data-stu-id="6ab37-116">text</span></span> | <span data-ttu-id="6ab37-117">J</span><span class="sxs-lookup"><span data-stu-id="6ab37-117">Y</span></span>   | <span data-ttu-id="6ab37-118">N</span><span class="sxs-lookup"><span data-stu-id="6ab37-118">N</span></span>        |
| <span data-ttu-id="6ab37-119">Retainoffsets</span><span class="sxs-lookup"><span data-stu-id="6ab37-119">RetainOffsets</span></span> | <span data-ttu-id="6ab37-120">text</span><span class="sxs-lookup"><span data-stu-id="6ab37-120">text</span></span> |     | <span data-ttu-id="6ab37-121">N</span><span class="sxs-lookup"><span data-stu-id="6ab37-121">N</span></span>        |
| <span data-ttu-id="6ab37-122">Retainlängen</span><span class="sxs-lookup"><span data-stu-id="6ab37-122">RetainLengths</span></span> | <span data-ttu-id="6ab37-123">text</span><span class="sxs-lookup"><span data-stu-id="6ab37-123">text</span></span> |     | <span data-ttu-id="6ab37-124">N</span><span class="sxs-lookup"><span data-stu-id="6ab37-124">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="6ab37-125">Spalten</span><span class="sxs-lookup"><span data-stu-id="6ab37-125">Columns</span></span>

<dl> <dt>

<span data-ttu-id="6ab37-126"><span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Ärzte</span><span class="sxs-lookup"><span data-stu-id="6ab37-126"><span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Family</span></span>
</dt> <dd>

<span data-ttu-id="6ab37-127">Fremdschlüssel für die Spalte "Family" der [Tabelle "ImageFamilies" (Patchwiz.dll)](imagefamilies-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="6ab37-127">Foreign key to the Family column of the [ImageFamilies Table (Patchwiz.dll)](imagefamilies-table-patchwiz-dll-.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ab37-128"><span id="FTK"></span><span id="ftk"></span>FTK</span><span class="sxs-lookup"><span data-stu-id="6ab37-128"><span id="FTK"></span><span id="ftk"></span>FTK</span></span>
</dt> <dd>

<span data-ttu-id="6ab37-129">Fremdschlüssel in den [Datei Tabellen](file-table.md) aller aktualisierten Images in der Abbild Familie.</span><span class="sxs-lookup"><span data-stu-id="6ab37-129">Foreign key into the [File tables](file-table.md) of all the upgraded images in the image family.</span></span>

</dd> <dt>

<span data-ttu-id="6ab37-130"><span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>Retainoffsets</span><span class="sxs-lookup"><span data-stu-id="6ab37-130"><span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets</span></span>
</dt> <dd>

<span data-ttu-id="6ab37-131">Der Offset der Bereiche, die nicht überschrieben werden können.</span><span class="sxs-lookup"><span data-stu-id="6ab37-131">The offset of the ranges that cannot be overwritten.</span></span> <span data-ttu-id="6ab37-132">Der Wert in diesem Feld ist eine Liste der Bereichs Offset Zahlen für Bereiche, die in den Zieldateien nicht überschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6ab37-132">The value in this field is a list of the range offset numbers for ranges that are not to be overwritten in the target files.</span></span> <span data-ttu-id="6ab37-133">Die Reihenfolge und die Anzahl der Bereiche in der Liste müssen mit den Elementen in der Spalte "retainlängen" identisch sein.</span><span class="sxs-lookup"><span data-stu-id="6ab37-133">The order and number of the ranges in the list must match the items in the RetainLengths column.</span></span>

<span data-ttu-id="6ab37-134">Die Werte können Decimal oder hexadezimal sein.</span><span class="sxs-lookup"><span data-stu-id="6ab37-134">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="6ab37-135">[Patchwiz.dll](patchwiz-dll.md) behandelt den Wert als hexadezimal, wenn der Wert "0x" vorangestellt ist.</span><span class="sxs-lookup"><span data-stu-id="6ab37-135">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="6ab37-136">Die Spalten sind Zeichen folgen Spalten, und Patchwiz.dll konvertiert die Werte in ulongs.</span><span class="sxs-lookup"><span data-stu-id="6ab37-136">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> <dt>

<span data-ttu-id="6ab37-137"><span id="RetainLengths"></span><span id="retainlengths"></span><span id="RETAINLENGTHS"></span>Retainlängen</span><span class="sxs-lookup"><span data-stu-id="6ab37-137"><span id="RetainLengths"></span><span id="retainlengths"></span><span id="RETAINLENGTHS"></span>RetainLengths</span></span>
</dt> <dd>

<span data-ttu-id="6ab37-138">Die Länge in Bytes der Bereiche, die nicht überschrieben werden können.</span><span class="sxs-lookup"><span data-stu-id="6ab37-138">The length in bytes of the ranges that cannot be overwritten.</span></span> <span data-ttu-id="6ab37-139">Der Wert in diesem Feld ist eine Liste der Bereichs Längen Zahlen für Bereiche, die in Zieldateien beibehalten werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6ab37-139">The value in this field is a list of range length numbers for ranges to retain in target files.</span></span> <span data-ttu-id="6ab37-140">Die Reihenfolge und die Anzahl der Bereiche in der Liste müssen mit den Elementen in der retainoffsets-Spalte identisch sein.</span><span class="sxs-lookup"><span data-stu-id="6ab37-140">The order and number of the ranges in the list must match the items in the RetainOffsets column.</span></span>

<span data-ttu-id="6ab37-141">Die Werte können Decimal oder hexadezimal sein.</span><span class="sxs-lookup"><span data-stu-id="6ab37-141">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="6ab37-142">[Patchwiz.dll](patchwiz-dll.md) behandelt den Wert als hexadezimal, wenn der Wert "0x" vorangestellt ist.</span><span class="sxs-lookup"><span data-stu-id="6ab37-142">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="6ab37-143">Die Spalten sind Zeichen folgen Spalten, und Patchwiz.dll konvertiert die Werte in ulongs.</span><span class="sxs-lookup"><span data-stu-id="6ab37-143">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6ab37-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6ab37-144">Remarks</span></span>

<span data-ttu-id="6ab37-145">Die in retainoffsets und retainlängen eingegebenen Offsets und Längen dürfen keine überlappenden Bereiche angeben.</span><span class="sxs-lookup"><span data-stu-id="6ab37-145">The offsets and lengths entered in RetainOffsets and RetainLengths must not specify overlapping ranges.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ab37-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6ab37-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ab37-147">Patchen ausgewählter Bereiche einer Datei</span><span class="sxs-lookup"><span data-stu-id="6ab37-147">Patching Selected Regions of a File</span></span>](patching-selected-regions-of-a-file.md)
</dt> </dl>

 

 



