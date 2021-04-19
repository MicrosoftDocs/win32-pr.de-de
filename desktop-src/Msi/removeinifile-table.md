---
description: Die removeinifile-Tabelle enthält die Informationen, die eine Anwendung aus einer INI-Datei löschen muss.
ms.assetid: 702cf86e-02f4-4ea7-8573-b500ac550aae
title: Removeinifile-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b57b4ba6f2c42ee636f1b9e21e798e27665f102a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369062"
---
# <a name="removeinifile-table"></a><span data-ttu-id="173a0-103">Removeinifile-Tabelle</span><span class="sxs-lookup"><span data-stu-id="173a0-103">RemoveIniFile Table</span></span>

<span data-ttu-id="173a0-104">Die removeinifile-Tabelle enthält die Informationen, die eine Anwendung aus einer INI-Datei löschen muss.</span><span class="sxs-lookup"><span data-stu-id="173a0-104">The RemoveIniFile table contains the information an application needs to delete from a .ini file.</span></span>

<span data-ttu-id="173a0-105">Die removeinifile-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="173a0-105">The RemoveIniFile table has the following columns.</span></span>



| <span data-ttu-id="173a0-106">Spalte</span><span class="sxs-lookup"><span data-stu-id="173a0-106">Column</span></span>        | <span data-ttu-id="173a0-107">Typ</span><span class="sxs-lookup"><span data-stu-id="173a0-107">Type</span></span>                         | <span data-ttu-id="173a0-108">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="173a0-108">Key</span></span> | <span data-ttu-id="173a0-109">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="173a0-109">Nullable</span></span> |
|---------------|------------------------------|-----|----------|
| <span data-ttu-id="173a0-110">Removeinifile</span><span class="sxs-lookup"><span data-stu-id="173a0-110">RemoveIniFile</span></span> | [<span data-ttu-id="173a0-111">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="173a0-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="173a0-112">J</span><span class="sxs-lookup"><span data-stu-id="173a0-112">Y</span></span>   | <span data-ttu-id="173a0-113">N</span><span class="sxs-lookup"><span data-stu-id="173a0-113">N</span></span>        |
| <span data-ttu-id="173a0-114">FileName</span><span class="sxs-lookup"><span data-stu-id="173a0-114">FileName</span></span>      | [<span data-ttu-id="173a0-115">FileName</span><span class="sxs-lookup"><span data-stu-id="173a0-115">FileName</span></span>](text.md)         | <span data-ttu-id="173a0-116">N</span><span class="sxs-lookup"><span data-stu-id="173a0-116">N</span></span>   | <span data-ttu-id="173a0-117">N</span><span class="sxs-lookup"><span data-stu-id="173a0-117">N</span></span>        |
| <span data-ttu-id="173a0-118">Dirproperty</span><span class="sxs-lookup"><span data-stu-id="173a0-118">DirProperty</span></span>   | [<span data-ttu-id="173a0-119">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="173a0-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="173a0-120">N</span><span class="sxs-lookup"><span data-stu-id="173a0-120">N</span></span>   | <span data-ttu-id="173a0-121">J</span><span class="sxs-lookup"><span data-stu-id="173a0-121">Y</span></span>        |
| <span data-ttu-id="173a0-122">`Section`</span><span class="sxs-lookup"><span data-stu-id="173a0-122">Section</span></span>       | [<span data-ttu-id="173a0-123">Großformatige</span><span class="sxs-lookup"><span data-stu-id="173a0-123">Formatted</span></span>](formatted.md)   | <span data-ttu-id="173a0-124">N</span><span class="sxs-lookup"><span data-stu-id="173a0-124">N</span></span>   | <span data-ttu-id="173a0-125">N</span><span class="sxs-lookup"><span data-stu-id="173a0-125">N</span></span>        |
| <span data-ttu-id="173a0-126">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="173a0-126">Key</span></span>           | [<span data-ttu-id="173a0-127">Großformatige</span><span class="sxs-lookup"><span data-stu-id="173a0-127">Formatted</span></span>](formatted.md)   | <span data-ttu-id="173a0-128">N</span><span class="sxs-lookup"><span data-stu-id="173a0-128">N</span></span>   | <span data-ttu-id="173a0-129">N</span><span class="sxs-lookup"><span data-stu-id="173a0-129">N</span></span>        |
| <span data-ttu-id="173a0-130">Wert</span><span class="sxs-lookup"><span data-stu-id="173a0-130">Value</span></span>         | [<span data-ttu-id="173a0-131">Großformatige</span><span class="sxs-lookup"><span data-stu-id="173a0-131">Formatted</span></span>](formatted.md)   | <span data-ttu-id="173a0-132">N</span><span class="sxs-lookup"><span data-stu-id="173a0-132">N</span></span>   | <span data-ttu-id="173a0-133">J</span><span class="sxs-lookup"><span data-stu-id="173a0-133">Y</span></span>        |
| <span data-ttu-id="173a0-134">Aktion</span><span class="sxs-lookup"><span data-stu-id="173a0-134">Action</span></span>        | [<span data-ttu-id="173a0-135">Integer</span><span class="sxs-lookup"><span data-stu-id="173a0-135">Integer</span></span>](integer.md)       | <span data-ttu-id="173a0-136">N</span><span class="sxs-lookup"><span data-stu-id="173a0-136">N</span></span>   | <span data-ttu-id="173a0-137">N</span><span class="sxs-lookup"><span data-stu-id="173a0-137">N</span></span>        |
| <span data-ttu-id="173a0-138">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="173a0-138">Component\_</span></span>   | [<span data-ttu-id="173a0-139">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="173a0-139">Identifier</span></span>](identifier.md) | <span data-ttu-id="173a0-140">N</span><span class="sxs-lookup"><span data-stu-id="173a0-140">N</span></span>   | <span data-ttu-id="173a0-141">N</span><span class="sxs-lookup"><span data-stu-id="173a0-141">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="173a0-142">Spalten</span><span class="sxs-lookup"><span data-stu-id="173a0-142">Columns</span></span>

<dl> <dt>

<span data-ttu-id="173a0-143"><span id="RemoveIniFile"></span><span id="removeinifile"></span><span id="REMOVEINIFILE"></span>Removeinifile</span><span class="sxs-lookup"><span data-stu-id="173a0-143"><span id="RemoveIniFile"></span><span id="removeinifile"></span><span id="REMOVEINIFILE"></span>RemoveIniFile</span></span>
</dt> <dd>

<span data-ttu-id="173a0-144">Der Schlüssel für diese Tabelle.</span><span class="sxs-lookup"><span data-stu-id="173a0-144">The key for this table.</span></span>

</dd> <dt>

<span data-ttu-id="173a0-145"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Einfügen</span><span class="sxs-lookup"><span data-stu-id="173a0-145"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>FileName</span></span>
</dt> <dd>

<span data-ttu-id="173a0-146">Der Name der INI-Datei, in der die Informationen gelöscht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="173a0-146">The .ini file name in which to delete the information.</span></span>

</dd> <dt>

<span data-ttu-id="173a0-147"><span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>Dirproperty</span><span class="sxs-lookup"><span data-stu-id="173a0-147"><span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty</span></span>
</dt> <dd>

<span data-ttu-id="173a0-148">Der Name einer Eigenschaft, deren Wert in den vollständigen Pfad zum Ordner der zu entfernenden ini-Datei aufgelöst werden soll.</span><span class="sxs-lookup"><span data-stu-id="173a0-148">Name of a property whose value is assumed to resolve to the full path to the folder of the .ini file to be removed.</span></span> <span data-ttu-id="173a0-149">Die-Eigenschaft kann der Name eines Verzeichnisses in der [Verzeichnis Tabelle](directory-table.md), eine Eigenschaft, die von der [AppSearch-Tabelle](appsearch-table.md)festgelegt wurde, oder eine beliebige andere Eigenschaft sein, die einen vollständigen Pfad darstellt.</span><span class="sxs-lookup"><span data-stu-id="173a0-149">The property can be the name of a directory in the [Directory table](directory-table.md), a property set by the [AppSearch table](appsearch-table.md), or any other property that represents a full path.</span></span>

</dd> <dt>

<span data-ttu-id="173a0-150"><span id="Section"></span><span id="section"></span><span id="SECTION"></span>Sektions</span><span class="sxs-lookup"><span data-stu-id="173a0-150"><span id="Section"></span><span id="section"></span><span id="SECTION"></span>Section</span></span>
</dt> <dd>

<span data-ttu-id="173a0-151">Der lokalisierbare Abschnitt der INI-Datei.</span><span class="sxs-lookup"><span data-stu-id="173a0-151">The localizable .ini file section.</span></span>

</dd> <dt>

<span data-ttu-id="173a0-152"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Wichtigen</span><span class="sxs-lookup"><span data-stu-id="173a0-152"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="173a0-153">Der lokalisierbare ini-Datei Schlüssel unterhalb des Abschnitts.</span><span class="sxs-lookup"><span data-stu-id="173a0-153">The localizable .ini file key below the section.</span></span>

</dd> <dt>

<span data-ttu-id="173a0-154"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert</span><span class="sxs-lookup"><span data-stu-id="173a0-154"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="173a0-155">Der lokalisierbare Wert, der gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="173a0-155">The localizable value to be deleted.</span></span> <span data-ttu-id="173a0-156">Der Wert ist erforderlich, wenn action den Wert 4 hat.</span><span class="sxs-lookup"><span data-stu-id="173a0-156">The value is required when Action is 4.</span></span>

</dd> <dt>

<span data-ttu-id="173a0-157"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Hinspiel</span><span class="sxs-lookup"><span data-stu-id="173a0-157"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="173a0-158">Der Typ der Änderung, die vorgenommen werden soll.</span><span class="sxs-lookup"><span data-stu-id="173a0-158">The type of modification to be made.</span></span>



| <span data-ttu-id="173a0-159">Konstante</span><span class="sxs-lookup"><span data-stu-id="173a0-159">Constant</span></span>                         | <span data-ttu-id="173a0-160">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="173a0-160">Hexadecimal</span></span> | <span data-ttu-id="173a0-161">Decimal</span><span class="sxs-lookup"><span data-stu-id="173a0-161">Decimal</span></span> | <span data-ttu-id="173a0-162">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="173a0-162">Meaning</span></span>                          |
|----------------------------------|-------------|---------|----------------------------------|
| <span data-ttu-id="173a0-163">**msidbinifileaktionremoveline**</span><span class="sxs-lookup"><span data-stu-id="173a0-163">**msidbIniFileActionRemoveLine**</span></span> | <span data-ttu-id="173a0-164">0x002</span><span class="sxs-lookup"><span data-stu-id="173a0-164">0x002</span></span>       | <span data-ttu-id="173a0-165">2</span><span class="sxs-lookup"><span data-stu-id="173a0-165">2</span></span>       | <span data-ttu-id="173a0-166">Löscht den Eintrag ". ini".</span><span class="sxs-lookup"><span data-stu-id="173a0-166">Deletes .ini entry.</span></span>              |
| <span data-ttu-id="173a0-167">**msidbinifileaktionremovetag**</span><span class="sxs-lookup"><span data-stu-id="173a0-167">**msidbIniFileActionRemoveTag**</span></span>  | <span data-ttu-id="173a0-168">0x004</span><span class="sxs-lookup"><span data-stu-id="173a0-168">0x004</span></span>       | <span data-ttu-id="173a0-169">4</span><span class="sxs-lookup"><span data-stu-id="173a0-169">4</span></span>       | <span data-ttu-id="173a0-170">Löscht ein Tag aus einem INI-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="173a0-170">Deletes a tag from a .ini entry.</span></span> |



 

</dd> <dt>

<span data-ttu-id="173a0-171"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_</span><span class="sxs-lookup"><span data-stu-id="173a0-171"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="173a0-172">Externer Schlüssel in erste Spalte der [Komponenten Tabelle](component-table.md) , die auf die Komponente verweist, die das Löschen des ini-Werts steuert.</span><span class="sxs-lookup"><span data-stu-id="173a0-172">External key into first column of the [Component table](component-table.md) referencing the component that controls the deletion of the .ini value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="173a0-173">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="173a0-173">Remarks</span></span>

<span data-ttu-id="173a0-174">Die Informationen der INI-Datei werden gelöscht, wenn die entsprechende Komponente zur Installation ausgewählt wurde, entweder lokal oder über die Quelle ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="173a0-174">The .ini file information is deleted when the corresponding Component has been selected to be installed, either locally or run from source.</span></span>

<span data-ttu-id="173a0-175">Diese Tabelle wird beim Ausführen der [RemoveIniValues-Aktion](removeinivalues-action.md) bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="173a0-175">This table is referred to when the [RemoveIniValues action](removeinivalues-action.md) is executed.</span></span>

<span data-ttu-id="173a0-176">Wenn die Verzeichnis \_ Spalte als NULL angegeben wird, ist der Speicherort der INI-Datei der standardmäßige Windows-ini-Speicherort, der standardmäßig das Windows-Verzeichnis ist.</span><span class="sxs-lookup"><span data-stu-id="173a0-176">If the Directory\_ column is specified as null, the ini file location is the standard Windows ini location which is the Windows directory by default.</span></span>

<span data-ttu-id="173a0-177">Wenn Sie den letzten Wert aus einem Abschnitt entfernen, wird dieser Abschnitt gelöscht.</span><span class="sxs-lookup"><span data-stu-id="173a0-177">Removing the last value from a section deletes that section.</span></span> <span data-ttu-id="173a0-178">Es gibt keine andere Möglichkeit, einen vollständigen Abschnitt zu löschen, außer alle seine Werte zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="173a0-178">There is no other way to delete an entire section other than removing all its values.</span></span>

## <a name="validation"></a><span data-ttu-id="173a0-179">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="173a0-179">Validation</span></span>

<dl>

[<span data-ttu-id="173a0-180">ICE03</span><span class="sxs-lookup"><span data-stu-id="173a0-180">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="173a0-181">ICE06</span><span class="sxs-lookup"><span data-stu-id="173a0-181">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="173a0-182">ICE32</span><span class="sxs-lookup"><span data-stu-id="173a0-182">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="173a0-183">ICE40</span><span class="sxs-lookup"><span data-stu-id="173a0-183">ICE40</span></span>](ice40.md)  
[<span data-ttu-id="173a0-184">ICE46</span><span class="sxs-lookup"><span data-stu-id="173a0-184">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="173a0-185">ICE69</span><span class="sxs-lookup"><span data-stu-id="173a0-185">ICE69</span></span>](ice69.md)  
</dl>

 

 



