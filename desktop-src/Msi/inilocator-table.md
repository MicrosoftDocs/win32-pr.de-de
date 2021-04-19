---
description: Die Tabelle "inilocator" enthält die Informationen, die erforderlich sind, um eine Datei oder ein Verzeichnis mithilfe einer INI-Datei zu suchen oder nach einem bestimmten INI-Eintrag zu suchen. Die INI-Datei muss im Microsoft Windows-Standardverzeichnis vorhanden sein.
ms.assetid: 5a3c6077-34ef-48c8-b4e6-ecb1deb40f96
title: Inilocator-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89583a2d69fd88dd4b5624920e2374aa7e203103
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358840"
---
# <a name="inilocator-table"></a><span data-ttu-id="da8fa-104">Inilocator-Tabelle</span><span class="sxs-lookup"><span data-stu-id="da8fa-104">IniLocator Table</span></span>

<span data-ttu-id="da8fa-105">Die Tabelle "inilocator" enthält die Informationen, die erforderlich sind, um eine Datei oder ein Verzeichnis mithilfe einer INI-Datei zu suchen oder nach einem bestimmten INI-Eintrag zu suchen.</span><span class="sxs-lookup"><span data-stu-id="da8fa-105">The IniLocator table holds the information needed to search for a file or directory using an .ini file or to search for a particular .ini entry itself.</span></span> <span data-ttu-id="da8fa-106">Die INI-Datei muss im Microsoft Windows-Standardverzeichnis vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="da8fa-106">The .ini file must be present in the default Microsoft Windows directory.</span></span>

<span data-ttu-id="da8fa-107">Die inilocator-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="da8fa-107">The IniLocator table has the following columns.</span></span>



| <span data-ttu-id="da8fa-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="da8fa-108">Column</span></span>      | <span data-ttu-id="da8fa-109">Typ</span><span class="sxs-lookup"><span data-stu-id="da8fa-109">Type</span></span>                         | <span data-ttu-id="da8fa-110">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="da8fa-110">Key</span></span> | <span data-ttu-id="da8fa-111">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="da8fa-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="da8fa-112">Signatur\_</span><span class="sxs-lookup"><span data-stu-id="da8fa-112">Signature\_</span></span> | [<span data-ttu-id="da8fa-113">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="da8fa-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="da8fa-114">J</span><span class="sxs-lookup"><span data-stu-id="da8fa-114">Y</span></span>   | <span data-ttu-id="da8fa-115">N</span><span class="sxs-lookup"><span data-stu-id="da8fa-115">N</span></span>        |
| <span data-ttu-id="da8fa-116">FileName</span><span class="sxs-lookup"><span data-stu-id="da8fa-116">FileName</span></span>    | [<span data-ttu-id="da8fa-117">FileName</span><span class="sxs-lookup"><span data-stu-id="da8fa-117">FileName</span></span>](text.md)         | <span data-ttu-id="da8fa-118">N</span><span class="sxs-lookup"><span data-stu-id="da8fa-118">N</span></span>   | <span data-ttu-id="da8fa-119">N</span><span class="sxs-lookup"><span data-stu-id="da8fa-119">N</span></span>        |
| <span data-ttu-id="da8fa-120">`Section`</span><span class="sxs-lookup"><span data-stu-id="da8fa-120">Section</span></span>     | [<span data-ttu-id="da8fa-121">Text</span><span class="sxs-lookup"><span data-stu-id="da8fa-121">Text</span></span>](text.md)             | <span data-ttu-id="da8fa-122">N</span><span class="sxs-lookup"><span data-stu-id="da8fa-122">N</span></span>   | <span data-ttu-id="da8fa-123">N</span><span class="sxs-lookup"><span data-stu-id="da8fa-123">N</span></span>        |
| <span data-ttu-id="da8fa-124">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="da8fa-124">Key</span></span>         | [<span data-ttu-id="da8fa-125">Text</span><span class="sxs-lookup"><span data-stu-id="da8fa-125">Text</span></span>](text.md)             | <span data-ttu-id="da8fa-126">N</span><span class="sxs-lookup"><span data-stu-id="da8fa-126">N</span></span>   | <span data-ttu-id="da8fa-127">N</span><span class="sxs-lookup"><span data-stu-id="da8fa-127">N</span></span>        |
| <span data-ttu-id="da8fa-128">Feld</span><span class="sxs-lookup"><span data-stu-id="da8fa-128">Field</span></span>       | [<span data-ttu-id="da8fa-129">Integer</span><span class="sxs-lookup"><span data-stu-id="da8fa-129">Integer</span></span>](integer.md)       | <span data-ttu-id="da8fa-130">N</span><span class="sxs-lookup"><span data-stu-id="da8fa-130">N</span></span>   | <span data-ttu-id="da8fa-131">J</span><span class="sxs-lookup"><span data-stu-id="da8fa-131">Y</span></span>        |
| <span data-ttu-id="da8fa-132">Typ</span><span class="sxs-lookup"><span data-stu-id="da8fa-132">Type</span></span>        | [<span data-ttu-id="da8fa-133">Integer</span><span class="sxs-lookup"><span data-stu-id="da8fa-133">Integer</span></span>](integer.md)       | <span data-ttu-id="da8fa-134">N</span><span class="sxs-lookup"><span data-stu-id="da8fa-134">N</span></span>   | <span data-ttu-id="da8fa-135">J</span><span class="sxs-lookup"><span data-stu-id="da8fa-135">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="da8fa-136">Spalten</span><span class="sxs-lookup"><span data-stu-id="da8fa-136">Columns</span></span>

<dl> <dt>

<span data-ttu-id="da8fa-137"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Unter\_</span><span class="sxs-lookup"><span data-stu-id="da8fa-137"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span></span>
</dt> <dd>

<span data-ttu-id="da8fa-138">Ein externer Schlüssel in die erste Spalte der [Signatur Tabelle](signature-table.md).</span><span class="sxs-lookup"><span data-stu-id="da8fa-138">An external key into the first column of the [Signature table](signature-table.md).</span></span> <span data-ttu-id="da8fa-139">Die Signatur \_ stellt eine eindeutige Signatur dar und ist auch der externe Schlüssel in Spalte 1 der Signatur Tabelle.</span><span class="sxs-lookup"><span data-stu-id="da8fa-139">The Signature\_ represents a unique signature and is also the external key into column one of the Signature table.</span></span> <span data-ttu-id="da8fa-140">Wenn diese Signatur in der Signatur Tabelle vorhanden ist, wird die Suche nach einer Datei durchsucht.</span><span class="sxs-lookup"><span data-stu-id="da8fa-140">If this signature is present in the Signature table, then the search is for a file.</span></span> <span data-ttu-id="da8fa-141">Wenn dieser Schlüssel in der Signatur Tabelle nicht vorhanden ist und der Wert der Type-Spalte **msidblocatortyperawvalue** ist, wird die Suche nach dem von der Tabelle inilocator angegebenen INI-Eintrag durchsucht.</span><span class="sxs-lookup"><span data-stu-id="da8fa-141">If this key is absent from the Signature table, and the value of the Type column is **msidbLocatorTypeRawValue**, the search is for the .ini entry specified by the IniLocator table.</span></span> <span data-ttu-id="da8fa-142">Andernfalls ist die Suche nach einem Verzeichnis, das von der Tabelle "inilocator" angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="da8fa-142">Otherwise the search is for a directory specified by the IniLocator table.</span></span>

</dd> <dt>

<span data-ttu-id="da8fa-143"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Einfügen</span><span class="sxs-lookup"><span data-stu-id="da8fa-143"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>FileName</span></span>
</dt> <dd>

<span data-ttu-id="da8fa-144">Der Name der INI-Datei.</span><span class="sxs-lookup"><span data-stu-id="da8fa-144">The .ini file name.</span></span>

</dd> <dt>

<span data-ttu-id="da8fa-145"><span id="Section"></span><span id="section"></span><span id="SECTION"></span>Sektions</span><span class="sxs-lookup"><span data-stu-id="da8fa-145"><span id="Section"></span><span id="section"></span><span id="SECTION"></span>Section</span></span>
</dt> <dd>

<span data-ttu-id="da8fa-146">Der Abschnitts Name innerhalb der INI-Datei.</span><span class="sxs-lookup"><span data-stu-id="da8fa-146">Section name within the .ini file.</span></span>

</dd> <dt>

<span data-ttu-id="da8fa-147"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Wichtigen</span><span class="sxs-lookup"><span data-stu-id="da8fa-147"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="da8fa-148">Der Schlüsselwert innerhalb des Abschnitts.</span><span class="sxs-lookup"><span data-stu-id="da8fa-148">Key value within the section.</span></span>

</dd> <dt>

<span data-ttu-id="da8fa-149"><span id="Field"></span><span id="field"></span><span id="FIELD"></span>Flächen</span><span class="sxs-lookup"><span data-stu-id="da8fa-149"><span id="Field"></span><span id="field"></span><span id="FIELD"></span>Field</span></span>
</dt> <dd>

<span data-ttu-id="da8fa-150">Das Feld in der. ini-Zeile.</span><span class="sxs-lookup"><span data-stu-id="da8fa-150">The field in the .ini line.</span></span> <span data-ttu-id="da8fa-151">Wenn Field NULL oder 0 ist, wird die gesamte Zeile gelesen.</span><span class="sxs-lookup"><span data-stu-id="da8fa-151">If Field is Null or 0, then the entire line is read.</span></span> <span data-ttu-id="da8fa-152">Dabei muss es sich um eine nicht negative Zahl handeln.</span><span class="sxs-lookup"><span data-stu-id="da8fa-152">This must be a non-negative number.</span></span>

</dd> <dt>

<span data-ttu-id="da8fa-153"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Sorte</span><span class="sxs-lookup"><span data-stu-id="da8fa-153"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Type</span></span>
</dt> <dd>

<span data-ttu-id="da8fa-154">Ein Wert, der bestimmt, ob der INI-Wert ein Datei Speicherort, ein Verzeichnis Speicherort oder ein RAW. ini-Wert ist.</span><span class="sxs-lookup"><span data-stu-id="da8fa-154">A value that determines whether the .ini value is a file location, a directory location, or raw .ini value.</span></span>

<span data-ttu-id="da8fa-155">In der folgenden Tabelle sind gültige Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="da8fa-155">The following table lists valid values.</span></span> <span data-ttu-id="da8fa-156">Wenn nicht vorhanden, wird Type auf 1 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="da8fa-156">If absent, Type is set to be 1.</span></span>



| <span data-ttu-id="da8fa-157">Konstante</span><span class="sxs-lookup"><span data-stu-id="da8fa-157">Constant</span></span>                      | <span data-ttu-id="da8fa-158">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="da8fa-158">Hexadecimal</span></span> | <span data-ttu-id="da8fa-159">Decimal</span><span class="sxs-lookup"><span data-stu-id="da8fa-159">Decimal</span></span> | <span data-ttu-id="da8fa-160">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="da8fa-160">Description</span></span>           |
|-------------------------------|-------------|---------|-----------------------|
| <span data-ttu-id="da8fa-161">**msidbloprojekttypedirectory**</span><span class="sxs-lookup"><span data-stu-id="da8fa-161">**msidbLocatorTypeDirectory**</span></span> | <span data-ttu-id="da8fa-162">0x000</span><span class="sxs-lookup"><span data-stu-id="da8fa-162">0x000</span></span>       | <span data-ttu-id="da8fa-163">0</span><span class="sxs-lookup"><span data-stu-id="da8fa-163">0</span></span>       | <span data-ttu-id="da8fa-164">Ein Verzeichnis Speicherort.</span><span class="sxs-lookup"><span data-stu-id="da8fa-164">A directory location.</span></span> |
| <span data-ttu-id="da8fa-165">**msidblo-typefilename**</span><span class="sxs-lookup"><span data-stu-id="da8fa-165">**msidbLocatorTypeFileName**</span></span>  | <span data-ttu-id="da8fa-166">0x001</span><span class="sxs-lookup"><span data-stu-id="da8fa-166">0x001</span></span>       | <span data-ttu-id="da8fa-167">1</span><span class="sxs-lookup"><span data-stu-id="da8fa-167">1</span></span>       | <span data-ttu-id="da8fa-168">Ein Datei Speicherort.</span><span class="sxs-lookup"><span data-stu-id="da8fa-168">A file location.</span></span>      |
| <span data-ttu-id="da8fa-169">**msidbloserortyperawvalue**</span><span class="sxs-lookup"><span data-stu-id="da8fa-169">**msidbLocatorTypeRawValue**</span></span>  | <span data-ttu-id="da8fa-170">0x002</span><span class="sxs-lookup"><span data-stu-id="da8fa-170">0x002</span></span>       | <span data-ttu-id="da8fa-171">2</span><span class="sxs-lookup"><span data-stu-id="da8fa-171">2</span></span>       | <span data-ttu-id="da8fa-172">Ein "RAW. ini"-Wert.</span><span class="sxs-lookup"><span data-stu-id="da8fa-172">A raw .ini value.</span></span>     |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="da8fa-173">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="da8fa-173">Remarks</span></span>

<span data-ttu-id="da8fa-174">Diese Tabelle wird mit der [AppSearch-Tabelle](appsearch-table.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="da8fa-174">This table is used with the [AppSearch Table](appsearch-table.md).</span></span>

<span data-ttu-id="da8fa-175">Die Spalten dieser Tabelle sind im Allgemeinen nicht lokalisiert.</span><span class="sxs-lookup"><span data-stu-id="da8fa-175">This table's columns are generally not localized.</span></span> <span data-ttu-id="da8fa-176">Wenn ein Autor eine Suche nach Produkten in mehreren Sprachen beschließt, kann in der Tabelle für jede Sprache ein separater Eintrag enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="da8fa-176">If an author decides to search for products in multiple languages, then there can be a separate entry included in the table for each language.</span></span>

<span data-ttu-id="da8fa-177">Der zugeordnete lokalisierte Text für die Statusanzeige oder Protokollierung wird in der [Tabelle "aktiontext](actiontext-table.md)" angegeben.</span><span class="sxs-lookup"><span data-stu-id="da8fa-177">Associated localized text for progress display or logging is specified in the [ActionText table](actiontext-table.md).</span></span>

<span data-ttu-id="da8fa-178">Weitere Informationen finden Sie [untersuchen nach vorhandenen Anwendungen, Dateien, Registrierungs Einträgen oder INI-Datei Einträgen](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span><span class="sxs-lookup"><span data-stu-id="da8fa-178">See [Searching for Existing Applications, Files, Registry Entries or .ini File Entries](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span></span>

## <a name="validation"></a><span data-ttu-id="da8fa-179">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="da8fa-179">Validation</span></span>

<dl>

[<span data-ttu-id="da8fa-180">ICE03</span><span class="sxs-lookup"><span data-stu-id="da8fa-180">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="da8fa-181">ICE06</span><span class="sxs-lookup"><span data-stu-id="da8fa-181">ICE06</span></span>](ice06.md)  
</dl>

 

 



