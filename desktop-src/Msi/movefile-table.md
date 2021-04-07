---
description: Diese Tabelle enthält eine Liste der Dateien, die aus einem angegebenen Quellverzeichnis in ein bestimmtes Zielverzeichnis verschoben oder kopiert werden sollen.
ms.assetid: 9ba47bdc-90c8-444a-ba8b-71c723b54556
title: "\"Muvefile\"-Tabelle"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2340626e745627c3c6146998c851a076d21ab81a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760165"
---
# <a name="movefile-table"></a><span data-ttu-id="0f84a-103">"Muvefile"-Tabelle</span><span class="sxs-lookup"><span data-stu-id="0f84a-103">MoveFile Table</span></span>

<span data-ttu-id="0f84a-104">Diese Tabelle enthält eine Liste der Dateien, die aus einem angegebenen Quellverzeichnis in ein bestimmtes Zielverzeichnis verschoben oder kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0f84a-104">This table contains a list of files to be moved or copied from a specified source directory to a specified destination directory.</span></span>

<span data-ttu-id="0f84a-105">Die "muvefile"-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="0f84a-105">The MoveFile table has the following columns.</span></span>



| <span data-ttu-id="0f84a-106">Spalte</span><span class="sxs-lookup"><span data-stu-id="0f84a-106">Column</span></span>       | <span data-ttu-id="0f84a-107">Typ</span><span class="sxs-lookup"><span data-stu-id="0f84a-107">Type</span></span>                         | <span data-ttu-id="0f84a-108">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="0f84a-108">Key</span></span> | <span data-ttu-id="0f84a-109">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="0f84a-109">Nullable</span></span> |
|--------------|------------------------------|-----|----------|
| <span data-ttu-id="0f84a-110">Filekey</span><span class="sxs-lookup"><span data-stu-id="0f84a-110">FileKey</span></span>      | [<span data-ttu-id="0f84a-111">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="0f84a-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="0f84a-112">J</span><span class="sxs-lookup"><span data-stu-id="0f84a-112">Y</span></span>   | <span data-ttu-id="0f84a-113">N</span><span class="sxs-lookup"><span data-stu-id="0f84a-113">N</span></span>        |
| <span data-ttu-id="0f84a-114">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="0f84a-114">Component\_</span></span>  | [<span data-ttu-id="0f84a-115">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="0f84a-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="0f84a-116">N</span><span class="sxs-lookup"><span data-stu-id="0f84a-116">N</span></span>   | <span data-ttu-id="0f84a-117">N</span><span class="sxs-lookup"><span data-stu-id="0f84a-117">N</span></span>        |
| <span data-ttu-id="0f84a-118">SourceName</span><span class="sxs-lookup"><span data-stu-id="0f84a-118">SourceName</span></span>   | [<span data-ttu-id="0f84a-119">Text</span><span class="sxs-lookup"><span data-stu-id="0f84a-119">Text</span></span>](text.md)             | <span data-ttu-id="0f84a-120">N</span><span class="sxs-lookup"><span data-stu-id="0f84a-120">N</span></span>   | <span data-ttu-id="0f84a-121">J</span><span class="sxs-lookup"><span data-stu-id="0f84a-121">Y</span></span>        |
| <span data-ttu-id="0f84a-122">Destname</span><span class="sxs-lookup"><span data-stu-id="0f84a-122">DestName</span></span>     | [<span data-ttu-id="0f84a-123">Filename</span><span class="sxs-lookup"><span data-stu-id="0f84a-123">Filename</span></span>](filename.md)     | <span data-ttu-id="0f84a-124">N</span><span class="sxs-lookup"><span data-stu-id="0f84a-124">N</span></span>   | <span data-ttu-id="0f84a-125">J</span><span class="sxs-lookup"><span data-stu-id="0f84a-125">Y</span></span>        |
| <span data-ttu-id="0f84a-126">Quellordner</span><span class="sxs-lookup"><span data-stu-id="0f84a-126">SourceFolder</span></span> | [<span data-ttu-id="0f84a-127">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="0f84a-127">Identifier</span></span>](identifier.md) | <span data-ttu-id="0f84a-128">N</span><span class="sxs-lookup"><span data-stu-id="0f84a-128">N</span></span>   | <span data-ttu-id="0f84a-129">J</span><span class="sxs-lookup"><span data-stu-id="0f84a-129">Y</span></span>        |
| <span data-ttu-id="0f84a-130">DestFolder</span><span class="sxs-lookup"><span data-stu-id="0f84a-130">DestFolder</span></span>   | [<span data-ttu-id="0f84a-131">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="0f84a-131">Identifier</span></span>](identifier.md) | <span data-ttu-id="0f84a-132">N</span><span class="sxs-lookup"><span data-stu-id="0f84a-132">N</span></span>   | <span data-ttu-id="0f84a-133">N</span><span class="sxs-lookup"><span data-stu-id="0f84a-133">N</span></span>        |
| <span data-ttu-id="0f84a-134">Optionen</span><span class="sxs-lookup"><span data-stu-id="0f84a-134">Options</span></span>      | [<span data-ttu-id="0f84a-135">Integer</span><span class="sxs-lookup"><span data-stu-id="0f84a-135">Integer</span></span>](integer.md)       | <span data-ttu-id="0f84a-136">N</span><span class="sxs-lookup"><span data-stu-id="0f84a-136">N</span></span>   | <span data-ttu-id="0f84a-137">N</span><span class="sxs-lookup"><span data-stu-id="0f84a-137">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="0f84a-138">Spalten</span><span class="sxs-lookup"><span data-stu-id="0f84a-138">Columns</span></span>

<dl> <dt>

<span data-ttu-id="0f84a-139"><span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>Filekey</span><span class="sxs-lookup"><span data-stu-id="0f84a-139"><span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey</span></span>
</dt> <dd>

<span data-ttu-id="0f84a-140">Primärschlüssel, der einen bestimmten "vfile"-Datensatz eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="0f84a-140">Primary key that uniquely identifies a particular MoveFile record.</span></span>

</dd> <dt>

<span data-ttu-id="0f84a-141"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_</span><span class="sxs-lookup"><span data-stu-id="0f84a-141"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="0f84a-142">Externer Schlüssel in der [Komponenten Tabelle](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="0f84a-142">External key into the [Component table](component-table.md).</span></span> <span data-ttu-id="0f84a-143">Wenn die Komponente, auf die von diesem Schlüssel verwiesen wird, nicht für die Installation oder Entfernung ausgewählt ist, wird für diesen Eintrag keine Aktion ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0f84a-143">If the component referenced by this key is not selected for installation or removal, then no action is taken on this MoveFile entry.</span></span>

</dd> <dt>

<span data-ttu-id="0f84a-144"><span id="SourceName"></span><span id="sourcename"></span><span id="SOURCENAME"></span>SourceName</span><span class="sxs-lookup"><span data-stu-id="0f84a-144"><span id="SourceName"></span><span id="sourcename"></span><span id="SOURCENAME"></span>SourceName</span></span>
</dt> <dd>

<span data-ttu-id="0f84a-145">Diese Spalte enthält den lokalisierbaren Namen der Quelldateien, die verschoben oder kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0f84a-145">This column contains the localizable name of the source files to be moved or copied.</span></span> <span data-ttu-id="0f84a-146">Diese Spalte kann leer gelassen werden.</span><span class="sxs-lookup"><span data-stu-id="0f84a-146">This column may be left blank.</span></span> <span data-ttu-id="0f84a-147">Weitere Informationen finden Sie in der Beschreibung der sourcefolder-Spalte.</span><span class="sxs-lookup"><span data-stu-id="0f84a-147">See the description of the SourceFolder column.</span></span> <span data-ttu-id="0f84a-148">Dieses Feld muss einen langen Dateinamen enthalten und darf Platzhalter Zeichen ( \* und?) enthalten.</span><span class="sxs-lookup"><span data-stu-id="0f84a-148">This field must contain a long file name and may contain wildcard characters (\* and ?).</span></span>

</dd> <dt>

<span data-ttu-id="0f84a-149"><span id="DestName"></span><span id="destname"></span><span id="DESTNAME"></span>Destname</span><span class="sxs-lookup"><span data-stu-id="0f84a-149"><span id="DestName"></span><span id="destname"></span><span id="DESTNAME"></span>DestName</span></span>
</dt> <dd>

<span data-ttu-id="0f84a-150">Diese Spalte enthält den lokalisierbaren Namen, der der ursprünglichen Datei nach dem Verschieben oder kopieren übergeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="0f84a-150">This column contains the localizable name to be given to the original file after it is moved or copied.</span></span> <span data-ttu-id="0f84a-151">Wenn dieses Feld leer ist, erhält die Zieldatei den gleichen Namen wie die Quelldatei.</span><span class="sxs-lookup"><span data-stu-id="0f84a-151">If this field is blank, then the destination file is given the same name as the source file.</span></span>

</dd> <dt>

<span data-ttu-id="0f84a-152"><span id="SourceFolder"></span><span id="sourcefolder"></span><span id="SOURCEFOLDER"></span>Quellordner</span><span class="sxs-lookup"><span data-stu-id="0f84a-152"><span id="SourceFolder"></span><span id="sourcefolder"></span><span id="SOURCEFOLDER"></span>SourceFolder</span></span>
</dt> <dd>

<span data-ttu-id="0f84a-153">Diese Spalte enthält den Namen einer Eigenschaft mit einem Wert, der in den vollständigen Pfad des Quell Verzeichnisses aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="0f84a-153">This column contains the name of a property having a value that resolves to the full path to the source directory.</span></span> <span data-ttu-id="0f84a-154">Wenn die Spalte SourceName leer bleibt, wird angenommen, dass die in der Spalte sourcefolder benannte Eigenschaft den vollständigen Pfad zur Quelldatei selbst (einschließlich des Datei namens) enthält.</span><span class="sxs-lookup"><span data-stu-id="0f84a-154">If the SourceName column is left blank, then the property named in the SourceFolder column is assumed to contain the full path to the source file itself (including the file name).</span></span>

</dd> <dt>

<span data-ttu-id="0f84a-155"><span id="DestFolder"></span><span id="destfolder"></span><span id="DESTFOLDER"></span>DestFolder</span><span class="sxs-lookup"><span data-stu-id="0f84a-155"><span id="DestFolder"></span><span id="destfolder"></span><span id="DESTFOLDER"></span>DestFolder</span></span>
</dt> <dd>

<span data-ttu-id="0f84a-156">Der Name einer Eigenschaft, deren Wert in den vollständigen Pfad zum Zielverzeichnis aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="0f84a-156">The name of a property whose value resolves to the full path to the destination directory.</span></span>

</dd> <dt>

<span data-ttu-id="0f84a-157"><span id="Options"></span><span id="options"></span><span id="OPTIONS"></span>Optionen</span><span class="sxs-lookup"><span data-stu-id="0f84a-157"><span id="Options"></span><span id="options"></span><span id="OPTIONS"></span>Options</span></span>
</dt> <dd>

<span data-ttu-id="0f84a-158">Ganzzahliger Wert, der den Betriebsmodus angibt.</span><span class="sxs-lookup"><span data-stu-id="0f84a-158">Integer value specifying the operating mode.</span></span>



| <span data-ttu-id="0f84a-159">Konstante</span><span class="sxs-lookup"><span data-stu-id="0f84a-159">Constant</span></span>                     | <span data-ttu-id="0f84a-160">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="0f84a-160">Hexadecimal</span></span> | <span data-ttu-id="0f84a-161">Decimal</span><span class="sxs-lookup"><span data-stu-id="0f84a-161">Decimal</span></span> | <span data-ttu-id="0f84a-162">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0f84a-162">Meaning</span></span>               |
|------------------------------|-------------|---------|-----------------------|
| <span data-ttu-id="0f84a-163">(none)</span><span class="sxs-lookup"><span data-stu-id="0f84a-163">(none)</span></span>                       | <span data-ttu-id="0f84a-164">0x000</span><span class="sxs-lookup"><span data-stu-id="0f84a-164">0x000</span></span>       | <span data-ttu-id="0f84a-165">0</span><span class="sxs-lookup"><span data-stu-id="0f84a-165">0</span></span>       | <span data-ttu-id="0f84a-166">Kopieren Sie die Quelldatei.</span><span class="sxs-lookup"><span data-stu-id="0f84a-166">Copy the source file.</span></span> |
| <span data-ttu-id="0f84a-167">**msidbmuvemeflitionsmove**</span><span class="sxs-lookup"><span data-stu-id="0f84a-167">**msidbMoveFileOptionsMove**</span></span> | <span data-ttu-id="0f84a-168">0x001</span><span class="sxs-lookup"><span data-stu-id="0f84a-168">0x001</span></span>       | <span data-ttu-id="0f84a-169">1</span><span class="sxs-lookup"><span data-stu-id="0f84a-169">1</span></span>       | <span data-ttu-id="0f84a-170">Verschieben Sie die Quelldatei.</span><span class="sxs-lookup"><span data-stu-id="0f84a-170">Move the source file.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0f84a-171">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0f84a-171">Remarks</span></span>

<span data-ttu-id="0f84a-172">Wenn ein " \* "-Platzhalter in die Spalte "SourceName" der Tabelle "muvefile" eingegeben wird und in der Spalte "destname" ein Ziel Dateiname angegeben ist, behalten alle verschobener oder kopierten Dateien die Namen in den Quellen bei.</span><span class="sxs-lookup"><span data-stu-id="0f84a-172">If a "\*" wildcard is entered in the SourceName column of the MoveFile table and a destination file name is specified in the DestName column, all moved or copied files retain the names in the sources.</span></span>

<span data-ttu-id="0f84a-173">Diese Tabelle wird von der [Aktion "muvefiles](movefiles-action.md)" verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="0f84a-173">This table is processed by the [MoveFiles action](movefiles-action.md).</span></span>

## <a name="validation"></a><span data-ttu-id="0f84a-174">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="0f84a-174">Validation</span></span>

<dl>

[<span data-ttu-id="0f84a-175">ICE03</span><span class="sxs-lookup"><span data-stu-id="0f84a-175">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="0f84a-176">ICE06</span><span class="sxs-lookup"><span data-stu-id="0f84a-176">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="0f84a-177">ICE18</span><span class="sxs-lookup"><span data-stu-id="0f84a-177">ICE18</span></span>](ice18.md)  
[<span data-ttu-id="0f84a-178">ICE32</span><span class="sxs-lookup"><span data-stu-id="0f84a-178">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="0f84a-179">ICE45</span><span class="sxs-lookup"><span data-stu-id="0f84a-179">ICE45</span></span>](ice45.md)  
[<span data-ttu-id="0f84a-180">ICE85</span><span class="sxs-lookup"><span data-stu-id="0f84a-180">ICE85</span></span>](ice85.md)  
</dl>

 

 



