---
description: In der patchtabelle ist die Datei angegeben, die einen bestimmten Patch und den physischen Speicherort der Patchdateien auf den Medien Images erhalten soll.
ms.assetid: 1b624702-de25-4b1a-9dac-21f359ee97f7
title: Patchtabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 061b2082f88a8c7c3967652900bb6bf6e1c29802
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760152"
---
# <a name="patch-table"></a><span data-ttu-id="b2272-103">Patchtabelle</span><span class="sxs-lookup"><span data-stu-id="b2272-103">Patch Table</span></span>

<span data-ttu-id="b2272-104">In der patchtabelle ist die Datei angegeben, die einen bestimmten Patch und den physischen Speicherort der Patchdateien auf den Medien Images erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="b2272-104">The Patch table specifies the file that is to receive a particular patch and the physical location of the patch files on the media images.</span></span>

<span data-ttu-id="b2272-105">Die patchtabelle enthält die folgenden Spalten.</span><span class="sxs-lookup"><span data-stu-id="b2272-105">The Patch table has the following columns.</span></span>



| <span data-ttu-id="b2272-106">Spalte</span><span class="sxs-lookup"><span data-stu-id="b2272-106">Column</span></span>      | <span data-ttu-id="b2272-107">Typ</span><span class="sxs-lookup"><span data-stu-id="b2272-107">Type</span></span>                               | <span data-ttu-id="b2272-108">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="b2272-108">Key</span></span> | <span data-ttu-id="b2272-109">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="b2272-109">Nullable</span></span> |
|-------------|------------------------------------|-----|----------|
| <span data-ttu-id="b2272-110">Datei\_</span><span class="sxs-lookup"><span data-stu-id="b2272-110">File\_</span></span>      | [<span data-ttu-id="b2272-111">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="b2272-111">Identifier</span></span>](identifier.md)       | <span data-ttu-id="b2272-112">J</span><span class="sxs-lookup"><span data-stu-id="b2272-112">Y</span></span>   | <span data-ttu-id="b2272-113">N</span><span class="sxs-lookup"><span data-stu-id="b2272-113">N</span></span>        |
| <span data-ttu-id="b2272-114">Sequenz</span><span class="sxs-lookup"><span data-stu-id="b2272-114">Sequence</span></span>    | [<span data-ttu-id="b2272-115">Integer</span><span class="sxs-lookup"><span data-stu-id="b2272-115">Integer</span></span>](integer.md)             | <span data-ttu-id="b2272-116">J</span><span class="sxs-lookup"><span data-stu-id="b2272-116">Y</span></span>   | <span data-ttu-id="b2272-117">N</span><span class="sxs-lookup"><span data-stu-id="b2272-117">N</span></span>        |
| <span data-ttu-id="b2272-118">Patchgröße</span><span class="sxs-lookup"><span data-stu-id="b2272-118">PatchSize</span></span>   | [<span data-ttu-id="b2272-119">Doubleiteger</span><span class="sxs-lookup"><span data-stu-id="b2272-119">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="b2272-120">N</span><span class="sxs-lookup"><span data-stu-id="b2272-120">N</span></span>   | <span data-ttu-id="b2272-121">N</span><span class="sxs-lookup"><span data-stu-id="b2272-121">N</span></span>        |
| <span data-ttu-id="b2272-122">Attribute</span><span class="sxs-lookup"><span data-stu-id="b2272-122">Attributes</span></span>  | [<span data-ttu-id="b2272-123">Integer</span><span class="sxs-lookup"><span data-stu-id="b2272-123">Integer</span></span>](integer.md)             | <span data-ttu-id="b2272-124">N</span><span class="sxs-lookup"><span data-stu-id="b2272-124">N</span></span>   | <span data-ttu-id="b2272-125">N</span><span class="sxs-lookup"><span data-stu-id="b2272-125">N</span></span>        |
| <span data-ttu-id="b2272-126">Header</span><span class="sxs-lookup"><span data-stu-id="b2272-126">Header</span></span>      | [<span data-ttu-id="b2272-127">Binär (Binary)</span><span class="sxs-lookup"><span data-stu-id="b2272-127">Binary</span></span>](binary.md)               | <span data-ttu-id="b2272-128">N</span><span class="sxs-lookup"><span data-stu-id="b2272-128">N</span></span>   | <span data-ttu-id="b2272-129">J</span><span class="sxs-lookup"><span data-stu-id="b2272-129">Y</span></span>        |
| <span data-ttu-id="b2272-130">Streamref\_</span><span class="sxs-lookup"><span data-stu-id="b2272-130">StreamRef\_</span></span> | [<span data-ttu-id="b2272-131">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="b2272-131">Identifier</span></span>](identifier.md)       | <span data-ttu-id="b2272-132">N</span><span class="sxs-lookup"><span data-stu-id="b2272-132">N</span></span>   | <span data-ttu-id="b2272-133">J</span><span class="sxs-lookup"><span data-stu-id="b2272-133">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="b2272-134">Spalten</span><span class="sxs-lookup"><span data-stu-id="b2272-134">Columns</span></span>

<dl> <dt>

<span data-ttu-id="b2272-135"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Datei\_</span><span class="sxs-lookup"><span data-stu-id="b2272-135"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="b2272-136">Der Patch wird auf die Datei angewendet, die durch den Bezeichner in dieser Spalte angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b2272-136">The patch is applied to the file specified by the identifier in this column.</span></span> <span data-ttu-id="b2272-137">Dies ist ein Primärschlüssel für die Tabelle, und es handelt sich um einen Fremdschlüssel für die [Dateitabelle](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="b2272-137">This is a primary key for the table and it is a foreign key to the [File table](file-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="b2272-138"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenz</span><span class="sxs-lookup"><span data-stu-id="b2272-138"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="b2272-139">Dies ist die Position der Patchdatei in der Reihenfolge der Dateien auf den Medienbildern.</span><span class="sxs-lookup"><span data-stu-id="b2272-139">This is the position of the patch file in the sequence order of files on the media images.</span></span> <span data-ttu-id="b2272-140">Die Reihenfolge der Reihenfolge muss der Reihenfolge der Dateien in der Datei mit dem Patchpaketdatei entsprechen.</span><span class="sxs-lookup"><span data-stu-id="b2272-140">The sequence order must correspond to the order of the files in the patch package cabinet file.</span></span> <span data-ttu-id="b2272-141">Dies ist ein Primärschlüssel für diese Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b2272-141">This is a primary key for this table.</span></span> <span data-ttu-id="b2272-142">Der Höchstwert beträgt 32767 Dateien. zum Erstellen eines Windows Installer Pakets mit weiteren Dateien finden Sie unter Erstellen [eines großen Pakets](authoring-a-large-package.md)Weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="b2272-142">The maximum limit is 32767 files, to create a Windows Installer package with more files, see [Authoring a Large Package](authoring-a-large-package.md).</span></span>

</dd> <dt>

<span data-ttu-id="b2272-143"><span id="PatchSize"></span><span id="patchsize"></span><span id="PATCHSIZE"></span>Patchgröße</span><span class="sxs-lookup"><span data-stu-id="b2272-143"><span id="PatchSize"></span><span id="patchsize"></span><span id="PATCHSIZE"></span>PatchSize</span></span>
</dt> <dd>

<span data-ttu-id="b2272-144">Diese Spalte gibt die Größe des Patches in Bytes an, die als Long Integer-Wert geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="b2272-144">This column gives the size of the patch in bytes written as a long integer.</span></span>

</dd> <dt>

<span data-ttu-id="b2272-145"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Legt</span><span class="sxs-lookup"><span data-stu-id="b2272-145"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>
</dt> <dd>

<span data-ttu-id="b2272-146">Ganze Zahl mit Bitflags, die Patchattribute darstellen.</span><span class="sxs-lookup"><span data-stu-id="b2272-146">Integer containing bit flags representing patch attributes.</span></span> <span data-ttu-id="b2272-147">Fügen Sie in dieser Spalte den Wert 1 ein, um anzugeben, dass der Fehler beim Anwenden dieses Patches kein schwerwiegender Fehler ist.</span><span class="sxs-lookup"><span data-stu-id="b2272-147">Insert a value of 1 in this column to indicate that the failure to apply this patch is not a fatal error.</span></span>



| <span data-ttu-id="b2272-148">Konstante</span><span class="sxs-lookup"><span data-stu-id="b2272-148">Constant</span></span>                         | <span data-ttu-id="b2272-149">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="b2272-149">Hexadecimal</span></span> | <span data-ttu-id="b2272-150">Decimal</span><span class="sxs-lookup"><span data-stu-id="b2272-150">Decimal</span></span> | <span data-ttu-id="b2272-151">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b2272-151">Description</span></span>                                                          |
|----------------------------------|-------------|---------|----------------------------------------------------------------------|
| <span data-ttu-id="b2272-152">(none)</span><span class="sxs-lookup"><span data-stu-id="b2272-152">(none)</span></span>                           | <span data-ttu-id="b2272-153">0x000</span><span class="sxs-lookup"><span data-stu-id="b2272-153">0x000</span></span>       | <span data-ttu-id="b2272-154">0</span><span class="sxs-lookup"><span data-stu-id="b2272-154">0</span></span>       | <span data-ttu-id="b2272-155">Ein Fehler beim Anwenden dieses Patches ist ein schwerwiegender Fehler.</span><span class="sxs-lookup"><span data-stu-id="b2272-155">Failure to apply this patch is a fatal error.</span></span>                        |
| <span data-ttu-id="b2272-156">**msidbpatchattributesnonvital**</span><span class="sxs-lookup"><span data-stu-id="b2272-156">**msidbPatchAttributesNonVital**</span></span> | <span data-ttu-id="b2272-157">0x001</span><span class="sxs-lookup"><span data-stu-id="b2272-157">0x001</span></span>       | <span data-ttu-id="b2272-158">1</span><span class="sxs-lookup"><span data-stu-id="b2272-158">1</span></span>       | <span data-ttu-id="b2272-159">Gibt an, dass der Fehler beim Anwenden dieses Patches kein schwerwiegender Fehler ist.</span><span class="sxs-lookup"><span data-stu-id="b2272-159">Indicates that the failure to apply this patch is not a fatal error.</span></span> |



 

</dd> <dt>

<span data-ttu-id="b2272-160"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>Header</span><span class="sxs-lookup"><span data-stu-id="b2272-160"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>Header</span></span>
</dt> <dd>

<span data-ttu-id="b2272-161">Diese Spalte ist der binäre Stream-patchheader, der für die patchvalidierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b2272-161">This column is the binary stream patch header used for patch validation.</span></span> <span data-ttu-id="b2272-162">Diese Spalte sollte NULL sein, wenn die streamref- \_ Spalte nicht NULL ist.</span><span class="sxs-lookup"><span data-stu-id="b2272-162">This column should be null if the StreamRef\_ column is not null.</span></span> <span data-ttu-id="b2272-163">In diesem Fall wird der patchheader-Stream in der [msipatchheaders-Tabelle](msipatchheaders-table.md) gespeichert, um die in [OLE-Einschränkungen für Streams](ole-limitations-on-streams.md)beschriebene Einschränkung für den Datenstrom Namen zu überwinden.</span><span class="sxs-lookup"><span data-stu-id="b2272-163">In this case, the patch header stream is stored in the [MsiPatchHeaders table](msipatchheaders-table.md) to overcome the stream name limitation described in [OLE Limitations on Streams](ole-limitations-on-streams.md).</span></span>

</dd> <dt>

<span data-ttu-id="b2272-164"><span id="StreamRef_"></span><span id="streamref_"></span><span id="STREAMREF_"></span>Streamref\_</span><span class="sxs-lookup"><span data-stu-id="b2272-164"><span id="StreamRef_"></span><span id="streamref_"></span><span id="STREAMREF_"></span>StreamRef\_</span></span>
</dt> <dd>

<span data-ttu-id="b2272-165">Externer Schlüssel in die msipatchheaders-Tabelle, die die Zeile angibt, die den patchheader-Stream enthält.</span><span class="sxs-lookup"><span data-stu-id="b2272-165">External key into the MsiPatchHeaders table specifying the row that contains the patch header stream.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b2272-166">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b2272-166">Remarks</span></span>

<span data-ttu-id="b2272-167">Diese Tabelle wird von der [Aktion PATCHFILES](patchfiles-action.md)verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="b2272-167">This table is processed by the [PatchFiles action](patchfiles-action.md).</span></span> <span data-ttu-id="b2272-168">Sie wird normalerweise durch eine Transformation aus einem Patchpaket zum Installationspaket hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b2272-168">It is usually added to the install package by a transform from a patch package.</span></span> <span data-ttu-id="b2272-169">Sie wird in der Regel nicht direkt in ein Installationspaket verfasst.</span><span class="sxs-lookup"><span data-stu-id="b2272-169">It is usually not authored directly into an install package.</span></span>

## <a name="validation"></a><span data-ttu-id="b2272-170">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="b2272-170">Validation</span></span>

<dl>

[<span data-ttu-id="b2272-171">ICE03</span><span class="sxs-lookup"><span data-stu-id="b2272-171">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="b2272-172">ICE06</span><span class="sxs-lookup"><span data-stu-id="b2272-172">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="b2272-173">ICE29</span><span class="sxs-lookup"><span data-stu-id="b2272-173">ICE29</span></span>](ice29.md)  
[<span data-ttu-id="b2272-174">ICE45</span><span class="sxs-lookup"><span data-stu-id="b2272-174">ICE45</span></span>](ice45.md)  
</dl>

 

 



