---
description: Die duplicatefile-Tabelle enthält eine Liste von Dateien, die dupliziert werden sollen, entweder in ein anderes Verzeichnis als die ursprüngliche Datei oder in dasselbe Verzeichnis, aber mit einem anderen Namen. Die ursprüngliche Datei muss eine Datei sein, die von der InstallFiles-Aktion installiert wird.
ms.assetid: 7fe1b52d-4b06-48cd-afe5-2bd5495bb55e
title: Duplicatefile-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 766f28b7984aedfc682a2bf23378d46ee0519c65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042393"
---
# <a name="duplicatefile-table"></a><span data-ttu-id="d45aa-104">Duplicatefile-Tabelle</span><span class="sxs-lookup"><span data-stu-id="d45aa-104">DuplicateFile Table</span></span>

<span data-ttu-id="d45aa-105">Die duplicatefile-Tabelle enthält eine Liste von Dateien, die dupliziert werden sollen, entweder in ein anderes Verzeichnis als die ursprüngliche Datei oder in dasselbe Verzeichnis, aber mit einem anderen Namen.</span><span class="sxs-lookup"><span data-stu-id="d45aa-105">The DuplicateFile table contains a list of files that are to be duplicated, either to a different directory than the original file or to the same directory but with a different name.</span></span> <span data-ttu-id="d45aa-106">Die ursprüngliche Datei muss eine Datei sein, die von der [InstallFiles-Aktion](installfiles-action.md)installiert wird.</span><span class="sxs-lookup"><span data-stu-id="d45aa-106">The original file must be a file installed by the [InstallFiles action](installfiles-action.md).</span></span>

<span data-ttu-id="d45aa-107">Die duplicatefile-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="d45aa-107">The DuplicateFile table has the following columns.</span></span>



| <span data-ttu-id="d45aa-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="d45aa-108">Column</span></span>      | <span data-ttu-id="d45aa-109">Typ</span><span class="sxs-lookup"><span data-stu-id="d45aa-109">Type</span></span>                         | <span data-ttu-id="d45aa-110">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="d45aa-110">Key</span></span> | <span data-ttu-id="d45aa-111">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="d45aa-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="d45aa-112">Filekey</span><span class="sxs-lookup"><span data-stu-id="d45aa-112">FileKey</span></span>     | [<span data-ttu-id="d45aa-113">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="d45aa-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="d45aa-114">J</span><span class="sxs-lookup"><span data-stu-id="d45aa-114">Y</span></span>   | <span data-ttu-id="d45aa-115">N</span><span class="sxs-lookup"><span data-stu-id="d45aa-115">N</span></span>        |
| <span data-ttu-id="d45aa-116">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="d45aa-116">Component\_</span></span> | [<span data-ttu-id="d45aa-117">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="d45aa-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="d45aa-118">N</span><span class="sxs-lookup"><span data-stu-id="d45aa-118">N</span></span>   | <span data-ttu-id="d45aa-119">N</span><span class="sxs-lookup"><span data-stu-id="d45aa-119">N</span></span>        |
| <span data-ttu-id="d45aa-120">Datei\_</span><span class="sxs-lookup"><span data-stu-id="d45aa-120">File\_</span></span>      | [<span data-ttu-id="d45aa-121">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="d45aa-121">Identifier</span></span>](identifier.md) | <span data-ttu-id="d45aa-122">N</span><span class="sxs-lookup"><span data-stu-id="d45aa-122">N</span></span>   | <span data-ttu-id="d45aa-123">N</span><span class="sxs-lookup"><span data-stu-id="d45aa-123">N</span></span>        |
| <span data-ttu-id="d45aa-124">Destname</span><span class="sxs-lookup"><span data-stu-id="d45aa-124">DestName</span></span>    | [<span data-ttu-id="d45aa-125">Filename</span><span class="sxs-lookup"><span data-stu-id="d45aa-125">Filename</span></span>](filename.md)     | <span data-ttu-id="d45aa-126">N</span><span class="sxs-lookup"><span data-stu-id="d45aa-126">N</span></span>   | <span data-ttu-id="d45aa-127">J</span><span class="sxs-lookup"><span data-stu-id="d45aa-127">Y</span></span>        |
| <span data-ttu-id="d45aa-128">DestFolder</span><span class="sxs-lookup"><span data-stu-id="d45aa-128">DestFolder</span></span>  | [<span data-ttu-id="d45aa-129">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="d45aa-129">Identifier</span></span>](identifier.md) | <span data-ttu-id="d45aa-130">N</span><span class="sxs-lookup"><span data-stu-id="d45aa-130">N</span></span>   | <span data-ttu-id="d45aa-131">J</span><span class="sxs-lookup"><span data-stu-id="d45aa-131">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="d45aa-132">Spalten</span><span class="sxs-lookup"><span data-stu-id="d45aa-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="d45aa-133"><span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>Filekey</span><span class="sxs-lookup"><span data-stu-id="d45aa-133"><span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey</span></span>
</dt> <dd>

<span data-ttu-id="d45aa-134">Ein primärer Schlüssel, ein nicht lokalisiertes Token, das einen eindeutigen duplicatefile-Datensatz identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d45aa-134">A primary key, a non-localized token, identifying a unique DuplicateFile record.</span></span>

</dd> <dt>

<span data-ttu-id="d45aa-135"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_</span><span class="sxs-lookup"><span data-stu-id="d45aa-135"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="d45aa-136">Ein externer Schlüssel für die erste Spalte der [Komponenten Tabelle](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="d45aa-136">An external key to the first column of the [Component table](component-table.md).</span></span> <span data-ttu-id="d45aa-137">Wenn die durch den Schlüssel identifizierte Komponente nicht für die Installation oder Entfernung ausgewählt ist, wird für diesen duplicatefile-Datensatz keine Aktion ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d45aa-137">If the component identified by the key is not selected for installation or removal, then no action is taken on this DuplicateFile record.</span></span>

</dd> <dt>

<span data-ttu-id="d45aa-138"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Datei\_</span><span class="sxs-lookup"><span data-stu-id="d45aa-138"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="d45aa-139">Der Fremdschlüssel in die Dateitabelle, die die ursprüngliche zu [duplizierende](file-table.md) Datei darstellt.</span><span class="sxs-lookup"><span data-stu-id="d45aa-139">Foreign key into the [File table](file-table.md) representing the original file that is to be duplicated.</span></span>

</dd> <dt>

<span data-ttu-id="d45aa-140"><span id="DestName"></span><span id="destname"></span><span id="DESTNAME"></span>Destname</span><span class="sxs-lookup"><span data-stu-id="d45aa-140"><span id="DestName"></span><span id="destname"></span><span id="DESTNAME"></span>DestName</span></span>
</dt> <dd>

<span data-ttu-id="d45aa-141">Lokalisier barer Name, der an die doppelte Datei übergeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="d45aa-141">Localizable name to be given to the duplicate file.</span></span> <span data-ttu-id="d45aa-142">Wenn dieses Feld leer ist, erhält die Zieldatei den gleichen Namen wie die ursprüngliche Datei.</span><span class="sxs-lookup"><span data-stu-id="d45aa-142">If this field is blank, then the destination file is given the same name as the original file.</span></span>

</dd> <dt>

<span data-ttu-id="d45aa-143"><span id="DestFolder"></span><span id="destfolder"></span><span id="DESTFOLDER"></span>DestFolder</span><span class="sxs-lookup"><span data-stu-id="d45aa-143"><span id="DestFolder"></span><span id="destfolder"></span><span id="DESTFOLDER"></span>DestFolder</span></span>
</dt> <dd>

<span data-ttu-id="d45aa-144">Der Name einer Eigenschaft, bei der es sich um den vollständigen Pfad handelt, in den die doppelte Datei kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d45aa-144">Name of a property that is the full path to where the duplicate file is to be copied.</span></span> <span data-ttu-id="d45aa-145">Wenn dieses Verzeichnis mit dem Verzeichnis identisch ist, das die ursprüngliche Datei enthält, und der Name für die vorgeschlagene doppelte Datei mit der ursprünglichen Datei identisch ist, findet keine Aktion statt.</span><span class="sxs-lookup"><span data-stu-id="d45aa-145">If this directory is the same as the directory containing the original file and the name for the proposed duplicate file is the same as the original, then no action takes place.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d45aa-146">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d45aa-146">Remarks</span></span>

<span data-ttu-id="d45aa-147">Die Tabelle wird von der [duplicatefiles-Aktion](duplicatefiles-action.md) und der [RemoveDuplicateFiles-Aktion](removeduplicatefiles-action.md)verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="d45aa-147">The table is processed by the [DuplicateFiles action](duplicatefiles-action.md) and the [RemoveDuplicateFiles action](removeduplicatefiles-action.md).</span></span>

## <a name="validation"></a><span data-ttu-id="d45aa-148">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="d45aa-148">Validation</span></span>

<dl>

[<span data-ttu-id="d45aa-149">ICE03</span><span class="sxs-lookup"><span data-stu-id="d45aa-149">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="d45aa-150">ICE06</span><span class="sxs-lookup"><span data-stu-id="d45aa-150">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="d45aa-151">ICE18</span><span class="sxs-lookup"><span data-stu-id="d45aa-151">ICE18</span></span>](ice18.md)  
[<span data-ttu-id="d45aa-152">ICE32</span><span class="sxs-lookup"><span data-stu-id="d45aa-152">ICE32</span></span>](ice32.md)  
</dl>

 

 



