---
description: Die IniFile-Tabelle enthält die ini-Informationen, die von der Anwendung in einer INI-Datei festgelegt werden müssen.
ms.assetid: fdb1a627-da6b-4da1-87a7-7f1c94d3836e
title: INIFILE-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d63ae37f7c8ed5c50b9b425b0462b445f7acb5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042144"
---
# <a name="inifile-table"></a><span data-ttu-id="2c98f-103">INIFILE-Tabelle</span><span class="sxs-lookup"><span data-stu-id="2c98f-103">IniFile Table</span></span>

<span data-ttu-id="2c98f-104">Die IniFile-Tabelle enthält die ini-Informationen, die von der Anwendung in einer INI-Datei festgelegt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="2c98f-104">The IniFile table contains the .ini information that the application needs to set in an .ini file.</span></span>

<span data-ttu-id="2c98f-105">Die IniFile-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="2c98f-105">The IniFile table has the following columns.</span></span>



| <span data-ttu-id="2c98f-106">Spalte</span><span class="sxs-lookup"><span data-stu-id="2c98f-106">Column</span></span>      | <span data-ttu-id="2c98f-107">Typ</span><span class="sxs-lookup"><span data-stu-id="2c98f-107">Type</span></span>                         | <span data-ttu-id="2c98f-108">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="2c98f-108">Key</span></span> | <span data-ttu-id="2c98f-109">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="2c98f-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="2c98f-110">INIFILE</span><span class="sxs-lookup"><span data-stu-id="2c98f-110">IniFile</span></span>     | [<span data-ttu-id="2c98f-111">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="2c98f-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="2c98f-112">J</span><span class="sxs-lookup"><span data-stu-id="2c98f-112">Y</span></span>   | <span data-ttu-id="2c98f-113">N</span><span class="sxs-lookup"><span data-stu-id="2c98f-113">N</span></span>        |
| <span data-ttu-id="2c98f-114">FileName</span><span class="sxs-lookup"><span data-stu-id="2c98f-114">FileName</span></span>    | [<span data-ttu-id="2c98f-115">FileName</span><span class="sxs-lookup"><span data-stu-id="2c98f-115">FileName</span></span>](text.md)         | <span data-ttu-id="2c98f-116">N</span><span class="sxs-lookup"><span data-stu-id="2c98f-116">N</span></span>   | <span data-ttu-id="2c98f-117">N</span><span class="sxs-lookup"><span data-stu-id="2c98f-117">N</span></span>        |
| <span data-ttu-id="2c98f-118">Dirproperty</span><span class="sxs-lookup"><span data-stu-id="2c98f-118">DirProperty</span></span> | [<span data-ttu-id="2c98f-119">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="2c98f-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="2c98f-120">N</span><span class="sxs-lookup"><span data-stu-id="2c98f-120">N</span></span>   | <span data-ttu-id="2c98f-121">J</span><span class="sxs-lookup"><span data-stu-id="2c98f-121">Y</span></span>        |
| <span data-ttu-id="2c98f-122">`Section`</span><span class="sxs-lookup"><span data-stu-id="2c98f-122">Section</span></span>     | [<span data-ttu-id="2c98f-123">Großformatige</span><span class="sxs-lookup"><span data-stu-id="2c98f-123">Formatted</span></span>](formatted.md)   | <span data-ttu-id="2c98f-124">N</span><span class="sxs-lookup"><span data-stu-id="2c98f-124">N</span></span>   | <span data-ttu-id="2c98f-125">N</span><span class="sxs-lookup"><span data-stu-id="2c98f-125">N</span></span>        |
| <span data-ttu-id="2c98f-126">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="2c98f-126">Key</span></span>         | [<span data-ttu-id="2c98f-127">Großformatige</span><span class="sxs-lookup"><span data-stu-id="2c98f-127">Formatted</span></span>](formatted.md)   | <span data-ttu-id="2c98f-128">N</span><span class="sxs-lookup"><span data-stu-id="2c98f-128">N</span></span>   | <span data-ttu-id="2c98f-129">N</span><span class="sxs-lookup"><span data-stu-id="2c98f-129">N</span></span>        |
| <span data-ttu-id="2c98f-130">Wert</span><span class="sxs-lookup"><span data-stu-id="2c98f-130">Value</span></span>       | [<span data-ttu-id="2c98f-131">Großformatige</span><span class="sxs-lookup"><span data-stu-id="2c98f-131">Formatted</span></span>](formatted.md)   | <span data-ttu-id="2c98f-132">N</span><span class="sxs-lookup"><span data-stu-id="2c98f-132">N</span></span>   | <span data-ttu-id="2c98f-133">N</span><span class="sxs-lookup"><span data-stu-id="2c98f-133">N</span></span>        |
| <span data-ttu-id="2c98f-134">Aktion</span><span class="sxs-lookup"><span data-stu-id="2c98f-134">Action</span></span>      | [<span data-ttu-id="2c98f-135">Integer</span><span class="sxs-lookup"><span data-stu-id="2c98f-135">Integer</span></span>](integer.md)       | <span data-ttu-id="2c98f-136">N</span><span class="sxs-lookup"><span data-stu-id="2c98f-136">N</span></span>   | <span data-ttu-id="2c98f-137">N</span><span class="sxs-lookup"><span data-stu-id="2c98f-137">N</span></span>        |
| <span data-ttu-id="2c98f-138">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="2c98f-138">Component\_</span></span> | [<span data-ttu-id="2c98f-139">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="2c98f-139">Identifier</span></span>](identifier.md) | <span data-ttu-id="2c98f-140">N</span><span class="sxs-lookup"><span data-stu-id="2c98f-140">N</span></span>   | <span data-ttu-id="2c98f-141">N</span><span class="sxs-lookup"><span data-stu-id="2c98f-141">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="2c98f-142">Spalten</span><span class="sxs-lookup"><span data-stu-id="2c98f-142">Columns</span></span>

<dl> <dt>

<span data-ttu-id="2c98f-143"><span id="IniFile"></span><span id="inifile"></span><span id="INIFILE"></span>INIFILE</span><span class="sxs-lookup"><span data-stu-id="2c98f-143"><span id="IniFile"></span><span id="inifile"></span><span id="INIFILE"></span>IniFile</span></span>
</dt> <dd>

<span data-ttu-id="2c98f-144">Der Schlüssel für diese Tabelle.</span><span class="sxs-lookup"><span data-stu-id="2c98f-144">The key for this table.</span></span>

</dd> <dt>

<span data-ttu-id="2c98f-145"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Einfügen</span><span class="sxs-lookup"><span data-stu-id="2c98f-145"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>FileName</span></span>
</dt> <dd>

<span data-ttu-id="2c98f-146">Der lokalisierbare Name der INI-Datei, in die die Informationen geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2c98f-146">The localizable name of the .ini file in which to write the information.</span></span>

</dd> <dt>

<span data-ttu-id="2c98f-147"><span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>Dirproperty</span><span class="sxs-lookup"><span data-stu-id="2c98f-147"><span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty</span></span>
</dt> <dd>

<span data-ttu-id="2c98f-148">Der Name einer Eigenschaft mit einem Wert, der in den vollständigen Pfad des Ordners aufgelöst wird, der die INI-Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="2c98f-148">Name of a property having a value that resolves to the full path of the folder containing the .ini file.</span></span> <span data-ttu-id="2c98f-149">Die-Eigenschaft kann der Name eines Verzeichnisses in der [Verzeichnis Tabelle](directory-table.md), eine Eigenschaft, die von der [AppSearch-Tabelle](appsearch-table.md)festgelegt wurde, oder eine beliebige andere Eigenschaft sein, die einen vollständigen Pfad darstellt.</span><span class="sxs-lookup"><span data-stu-id="2c98f-149">The property can be the name of a directory in the [Directory table](directory-table.md), a property set by the [AppSearch table](appsearch-table.md), or any other property that represents a full path.</span></span> <span data-ttu-id="2c98f-150">Wenn dieses Feld leer bleibt, wird die INI-Datei im Ordner mit dem vollständigen Pfad erstellt, der von der [**windowsfolder**](windowsfolder.md) -Eigenschaft angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2c98f-150">If this field is left blank, the .ini file is created in the folder having the full path specified by the [**WindowsFolder**](windowsfolder.md) property.</span></span>

</dd> <dt>

<span data-ttu-id="2c98f-151"><span id="Section"></span><span id="section"></span><span id="SECTION"></span>Sektions</span><span class="sxs-lookup"><span data-stu-id="2c98f-151"><span id="Section"></span><span id="section"></span><span id="SECTION"></span>Section</span></span>
</dt> <dd>

<span data-ttu-id="2c98f-152">Der lokalisierbare Abschnitt der INI-Datei.</span><span class="sxs-lookup"><span data-stu-id="2c98f-152">The localizable .ini file section.</span></span>

</dd> <dt>

<span data-ttu-id="2c98f-153"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Wichtigen</span><span class="sxs-lookup"><span data-stu-id="2c98f-153"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="2c98f-154">Der lokalisierbare ini-Datei Schlüssel innerhalb des Abschnitts.</span><span class="sxs-lookup"><span data-stu-id="2c98f-154">The localizable .ini file key within the section.</span></span>

</dd> <dt>

<span data-ttu-id="2c98f-155"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert</span><span class="sxs-lookup"><span data-stu-id="2c98f-155"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="2c98f-156">Der lokalisierbare Wert, der geschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="2c98f-156">The localizable value to be written.</span></span>

</dd> <dt>

<span data-ttu-id="2c98f-157"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Hinspiel</span><span class="sxs-lookup"><span data-stu-id="2c98f-157"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="2c98f-158">Der Typ der Änderung, die vorgenommen werden soll.</span><span class="sxs-lookup"><span data-stu-id="2c98f-158">The type of modification to be made.</span></span>



| <span data-ttu-id="2c98f-159">Konstante</span><span class="sxs-lookup"><span data-stu-id="2c98f-159">Constant</span></span>                         | <span data-ttu-id="2c98f-160">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="2c98f-160">Hexadecimal</span></span> | <span data-ttu-id="2c98f-161">Decimal</span><span class="sxs-lookup"><span data-stu-id="2c98f-161">Decimal</span></span> | <span data-ttu-id="2c98f-162">Modifikation (Modification)</span><span class="sxs-lookup"><span data-stu-id="2c98f-162">Modification</span></span>                                                                     |
|----------------------------------|-------------|---------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2c98f-163">**msidbinifileaktionaddline**</span><span class="sxs-lookup"><span data-stu-id="2c98f-163">**msidbIniFileActionAddLine**</span></span>    | <span data-ttu-id="2c98f-164">0x000</span><span class="sxs-lookup"><span data-stu-id="2c98f-164">0x000</span></span>       | <span data-ttu-id="2c98f-165">0</span><span class="sxs-lookup"><span data-stu-id="2c98f-165">0</span></span>       | <span data-ttu-id="2c98f-166">Erstellt oder aktualisiert einen INI-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="2c98f-166">Creates or updates a .ini entry.</span></span>                                                 |
| <span data-ttu-id="2c98f-167">**msidbinifileaktionkreateline**</span><span class="sxs-lookup"><span data-stu-id="2c98f-167">**msidbIniFileActionCreateLine**</span></span> | <span data-ttu-id="2c98f-168">0x001</span><span class="sxs-lookup"><span data-stu-id="2c98f-168">0x001</span></span>       | <span data-ttu-id="2c98f-169">1</span><span class="sxs-lookup"><span data-stu-id="2c98f-169">1</span></span>       | <span data-ttu-id="2c98f-170">Erstellt einen INI-Eintrag nur, wenn der Eintrag nicht bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="2c98f-170">Creates a .ini entry only if the entry does not already exist.</span></span>                   |
| <span data-ttu-id="2c98f-171">**msidbinifileaktionaddtag**</span><span class="sxs-lookup"><span data-stu-id="2c98f-171">**msidbIniFileActionAddTag**</span></span>     | <span data-ttu-id="2c98f-172">0x003</span><span class="sxs-lookup"><span data-stu-id="2c98f-172">0x003</span></span>       | <span data-ttu-id="2c98f-173">3</span><span class="sxs-lookup"><span data-stu-id="2c98f-173">3</span></span>       | <span data-ttu-id="2c98f-174">Erstellt einen neuen Eintrag oder fügt einen neuen durch Trennzeichen getrennten Wert an einen vorhandenen Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="2c98f-174">Creates a new entry or appends a new comma-separated value to an existing entry.</span></span> |



 

</dd> <dt>

<span data-ttu-id="2c98f-175"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_</span><span class="sxs-lookup"><span data-stu-id="2c98f-175"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="2c98f-176">Externer Schlüssel in die erste Spalte der [Komponenten Tabelle](component-table.md) , die auf die Komponente verweist, mit der die Installation des ini-Werts gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="2c98f-176">External key into the first column of the [Component table](component-table.md) referencing the component that controls the installation of the .ini value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2c98f-177">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2c98f-177">Remarks</span></span>

<span data-ttu-id="2c98f-178">Die Informationen der INI-Datei werden geschrieben, wenn die entsprechende Komponente als lokal oder von der Quelle ausgeführt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="2c98f-178">The .ini file information is written out when the corresponding component has been selected to be installed as local or run from source.</span></span>

<span data-ttu-id="2c98f-179">Auf diese Tabelle wird verwiesen, wenn die Aktion " [Write](writeinivalues-action.md) " oder die [RemoveIniValues](removeinivalues-action.md) -Aktion ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2c98f-179">This table is referred to when the [WriteIniValues action](writeinivalues-action.md) or the [RemoveIniValues action](removeinivalues-action.md) is executed.</span></span>

## <a name="validation"></a><span data-ttu-id="2c98f-180">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="2c98f-180">Validation</span></span>

<dl>

[<span data-ttu-id="2c98f-181">ICE03</span><span class="sxs-lookup"><span data-stu-id="2c98f-181">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="2c98f-182">ICE06</span><span class="sxs-lookup"><span data-stu-id="2c98f-182">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="2c98f-183">ICE32</span><span class="sxs-lookup"><span data-stu-id="2c98f-183">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="2c98f-184">ICE46</span><span class="sxs-lookup"><span data-stu-id="2c98f-184">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="2c98f-185">ICE69</span><span class="sxs-lookup"><span data-stu-id="2c98f-185">ICE69</span></span>](ice69.md)  
[<span data-ttu-id="2c98f-186">ICE88</span><span class="sxs-lookup"><span data-stu-id="2c98f-186">ICE88</span></span>](ice88.md)  
[<span data-ttu-id="2c98f-187">ICE91</span><span class="sxs-lookup"><span data-stu-id="2c98f-187">ICE91</span></span>](ice91.md)  
</dl>

 

 



