---
description: Die Tabelle RemoveFile enthält eine Liste der Dateien, die von der RemoveFiles-Aktion entfernt werden sollen. Wenn die FileName-Spalte dieser Tabelle auf NULL festgelegt wird, wird die Entfernung leerer Ordner unterstützt.
ms.assetid: 8b3cb0e3-ccc0-4030-8f57-aa124c3b5588
title: RemoveFile-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723e42582821d79842686678c5b310e95cd1e944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866715"
---
# <a name="removefile-table"></a><span data-ttu-id="560b0-104">RemoveFile-Tabelle</span><span class="sxs-lookup"><span data-stu-id="560b0-104">RemoveFile Table</span></span>

<span data-ttu-id="560b0-105">Die Tabelle RemoveFile enthält eine Liste der Dateien, die von der [RemoveFiles-Aktion](removefiles-action.md)entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="560b0-105">The RemoveFile table contains a list of files to be removed by the [RemoveFiles action](removefiles-action.md).</span></span> <span data-ttu-id="560b0-106">Wenn die FileName-Spalte dieser Tabelle auf NULL festgelegt wird, wird die Entfernung leerer Ordner unterstützt.</span><span class="sxs-lookup"><span data-stu-id="560b0-106">Setting the FileName column of this table to Null supports the removal of empty folders.</span></span>

<span data-ttu-id="560b0-107">Die RemoveFile-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="560b0-107">The RemoveFile table has the following columns.</span></span>



| <span data-ttu-id="560b0-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="560b0-108">Column</span></span>      | <span data-ttu-id="560b0-109">Typ</span><span class="sxs-lookup"><span data-stu-id="560b0-109">Type</span></span>                                     | <span data-ttu-id="560b0-110">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="560b0-110">Key</span></span> | <span data-ttu-id="560b0-111">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="560b0-111">Nullable</span></span> |
|-------------|------------------------------------------|-----|----------|
| <span data-ttu-id="560b0-112">Filekey</span><span class="sxs-lookup"><span data-stu-id="560b0-112">FileKey</span></span>     | [<span data-ttu-id="560b0-113">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="560b0-113">Identifier</span></span>](identifier.md)             | <span data-ttu-id="560b0-114">J</span><span class="sxs-lookup"><span data-stu-id="560b0-114">Y</span></span>   | <span data-ttu-id="560b0-115">N</span><span class="sxs-lookup"><span data-stu-id="560b0-115">N</span></span>        |
| <span data-ttu-id="560b0-116">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="560b0-116">Component\_</span></span> | [<span data-ttu-id="560b0-117">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="560b0-117">Identifier</span></span>](identifier.md)             | <span data-ttu-id="560b0-118">N</span><span class="sxs-lookup"><span data-stu-id="560b0-118">N</span></span>   | <span data-ttu-id="560b0-119">N</span><span class="sxs-lookup"><span data-stu-id="560b0-119">N</span></span>        |
| <span data-ttu-id="560b0-120">FileName</span><span class="sxs-lookup"><span data-stu-id="560b0-120">FileName</span></span>    | [<span data-ttu-id="560b0-121">Platzhalter Dateiname</span><span class="sxs-lookup"><span data-stu-id="560b0-121">WildCardFilename</span></span>](wildcardfilename.md) | <span data-ttu-id="560b0-122">N</span><span class="sxs-lookup"><span data-stu-id="560b0-122">N</span></span>   | <span data-ttu-id="560b0-123">J</span><span class="sxs-lookup"><span data-stu-id="560b0-123">Y</span></span>        |
| <span data-ttu-id="560b0-124">Dirproperty</span><span class="sxs-lookup"><span data-stu-id="560b0-124">DirProperty</span></span> | [<span data-ttu-id="560b0-125">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="560b0-125">Identifier</span></span>](identifier.md)             | <span data-ttu-id="560b0-126">N</span><span class="sxs-lookup"><span data-stu-id="560b0-126">N</span></span>   | <span data-ttu-id="560b0-127">N</span><span class="sxs-lookup"><span data-stu-id="560b0-127">N</span></span>        |
| <span data-ttu-id="560b0-128">InstallMode</span><span class="sxs-lookup"><span data-stu-id="560b0-128">InstallMode</span></span> | [<span data-ttu-id="560b0-129">Integer</span><span class="sxs-lookup"><span data-stu-id="560b0-129">Integer</span></span>](integer.md)                   | <span data-ttu-id="560b0-130">N</span><span class="sxs-lookup"><span data-stu-id="560b0-130">N</span></span>   | <span data-ttu-id="560b0-131">N</span><span class="sxs-lookup"><span data-stu-id="560b0-131">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="560b0-132">Spalten</span><span class="sxs-lookup"><span data-stu-id="560b0-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="560b0-133"><span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>Filekey</span><span class="sxs-lookup"><span data-stu-id="560b0-133"><span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey</span></span>
</dt> <dd>

<span data-ttu-id="560b0-134">Der Primärschlüssel, der zum Identifizieren dieses bestimmten Tabellen Eintrags verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="560b0-134">Primary key used to identify this particular table entry.</span></span>

</dd> <dt>

<span data-ttu-id="560b0-135"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_</span><span class="sxs-lookup"><span data-stu-id="560b0-135"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="560b0-136">Externer Schlüssel die erste Spalte der [Komponenten Tabelle](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="560b0-136">External key the first column of the [Component table](component-table.md).</span></span> <span data-ttu-id="560b0-137">Dieses Feld verweist auf die Komponente, mit der die zu entfernende Datei gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="560b0-137">This field references the component that controls the file to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="560b0-138"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Einfügen</span><span class="sxs-lookup"><span data-stu-id="560b0-138"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>FileName</span></span>
</dt> <dd>

<span data-ttu-id="560b0-139">Diese Spalte enthält den lokalisierbaren Namen der zu entfernenden Datei.</span><span class="sxs-lookup"><span data-stu-id="560b0-139">This column contains the localizable name of the file to be removed.</span></span> <span data-ttu-id="560b0-140">Wenn diese Spalte NULL ist, wird der angegebene Ordner entfernt, wenn er leer ist.</span><span class="sxs-lookup"><span data-stu-id="560b0-140">If this column is null, then the specified folder will be removed if it is empty.</span></span> <span data-ttu-id="560b0-141">Alle Dateien, die dem Platzhalter entsprechen, werden aus dem angegebenen Verzeichnis entfernt.</span><span class="sxs-lookup"><span data-stu-id="560b0-141">All of the files that match the wildcard will be removed from the specified directory.</span></span>

</dd> <dt>

<span data-ttu-id="560b0-142"><span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>Dirproperty</span><span class="sxs-lookup"><span data-stu-id="560b0-142"><span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty</span></span>
</dt> <dd>

<span data-ttu-id="560b0-143">Der Name einer Eigenschaft, deren Wert in den vollständigen Pfad zum Ordner der zu entfernenden Datei aufgelöst werden soll.</span><span class="sxs-lookup"><span data-stu-id="560b0-143">Name of a property whose value is assumed to resolve to the full path to the folder of the file to be removed.</span></span> <span data-ttu-id="560b0-144">Die-Eigenschaft kann der Name eines Verzeichnisses in der [Verzeichnis Tabelle](directory-table.md), eine Eigenschaft, die von der [AppSearch-Tabelle](appsearch-table.md)festgelegt wurde, oder eine beliebige andere Eigenschaft sein, die einen vollständigen Pfad darstellt.</span><span class="sxs-lookup"><span data-stu-id="560b0-144">The property can be the name of a directory in the [Directory table](directory-table.md), a property set by the [AppSearch table](appsearch-table.md), or any other property that represents a full path.</span></span>

</dd> <dt>

<span data-ttu-id="560b0-145"><span id="InstallMode"></span><span id="installmode"></span><span id="INSTALLMODE"></span>' Installmode '</span><span class="sxs-lookup"><span data-stu-id="560b0-145"><span id="InstallMode"></span><span id="installmode"></span><span id="INSTALLMODE"></span>InstallMode</span></span>
</dt> <dd>

<span data-ttu-id="560b0-146">Muss einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="560b0-146">Must be one of the following values.</span></span>



| <span data-ttu-id="560b0-147">Konstante</span><span class="sxs-lookup"><span data-stu-id="560b0-147">Constant</span></span>                                | <span data-ttu-id="560b0-148">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="560b0-148">Hexadecimal</span></span> | <span data-ttu-id="560b0-149">Decimal</span><span class="sxs-lookup"><span data-stu-id="560b0-149">Decimal</span></span> | <span data-ttu-id="560b0-150">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="560b0-150">Description</span></span>                                                                                                   |
|-----------------------------------------|-------------|---------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="560b0-151">**msidbremuvefileinstallmodeoninstall**</span><span class="sxs-lookup"><span data-stu-id="560b0-151">**msidbRemoveFileInstallModeOnInstall**</span></span> | <span data-ttu-id="560b0-152">0x001</span><span class="sxs-lookup"><span data-stu-id="560b0-152">0x001</span></span>       | <span data-ttu-id="560b0-153">1</span><span class="sxs-lookup"><span data-stu-id="560b0-153">1</span></span>       | <span data-ttu-id="560b0-154">Entfernen Sie nur, wenn die zugehörige Komponente installiert wird (msiinstallstatelocal oder msiinstallstaatource).</span><span class="sxs-lookup"><span data-stu-id="560b0-154">Remove only when the associated component is being installed (msiInstallStateLocal or msiInstallStateSource).</span></span> |
| <span data-ttu-id="560b0-155">**msidbremuvefileinstallmodeonremove**</span><span class="sxs-lookup"><span data-stu-id="560b0-155">**msidbRemoveFileInstallModeOnRemove**</span></span>  | <span data-ttu-id="560b0-156">0x002</span><span class="sxs-lookup"><span data-stu-id="560b0-156">0x002</span></span>       | <span data-ttu-id="560b0-157">2</span><span class="sxs-lookup"><span data-stu-id="560b0-157">2</span></span>       | <span data-ttu-id="560b0-158">Nur entfernen, wenn die zugeordnete Komponente entfernt wird (msiinstallstatemissing).</span><span class="sxs-lookup"><span data-stu-id="560b0-158">Remove only when the associated component is being removed (msiInstallStateAbsent).</span></span>                           |
| <span data-ttu-id="560b0-159">**msidbremuvefileinstallmodeonboth**</span><span class="sxs-lookup"><span data-stu-id="560b0-159">**msidbRemoveFileInstallModeOnBoth**</span></span>    | <span data-ttu-id="560b0-160">0x003</span><span class="sxs-lookup"><span data-stu-id="560b0-160">0x003</span></span>       | <span data-ttu-id="560b0-161">3</span><span class="sxs-lookup"><span data-stu-id="560b0-161">3</span></span>       | <span data-ttu-id="560b0-162">Entfernen Sie in einem der obigen Fälle.</span><span class="sxs-lookup"><span data-stu-id="560b0-162">Remove in either of the above cases.</span></span>                                                                          |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="560b0-163">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="560b0-163">Remarks</span></span>

<span data-ttu-id="560b0-164">Die Datei Verweise in dieser Tabelle werden von der [RemoveFiles-Aktion](removefiles-action.md)verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="560b0-164">The file references in this table are processed by the [RemoveFiles action](removefiles-action.md).</span></span>

## <a name="validation"></a><span data-ttu-id="560b0-165">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="560b0-165">Validation</span></span>

<dl>

[<span data-ttu-id="560b0-166">ICE03</span><span class="sxs-lookup"><span data-stu-id="560b0-166">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="560b0-167">ICE06</span><span class="sxs-lookup"><span data-stu-id="560b0-167">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="560b0-168">ICE18</span><span class="sxs-lookup"><span data-stu-id="560b0-168">ICE18</span></span>](ice18.md)  
[<span data-ttu-id="560b0-169">ICE32</span><span class="sxs-lookup"><span data-stu-id="560b0-169">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="560b0-170">ICE45</span><span class="sxs-lookup"><span data-stu-id="560b0-170">ICE45</span></span>](ice45.md)  
[<span data-ttu-id="560b0-171">ICE64</span><span class="sxs-lookup"><span data-stu-id="560b0-171">ICE64</span></span>](ice64.md)  
</dl>

 

 



