---
description: Die Signatur Tabelle enthält die Informationen, die eine Datei Signatur eindeutig identifizieren. Weitere Informationen zu Signaturen finden Sie unter digitale Signaturen und Windows Installer.
ms.assetid: 4780356f-e02a-45d9-883c-4f84867dbdea
title: Signatur Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efb75155c4c7b8ddf4a82706bc38f09d0af75260
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348702"
---
# <a name="signature-table"></a><span data-ttu-id="6d514-104">Signatur Tabelle</span><span class="sxs-lookup"><span data-stu-id="6d514-104">Signature Table</span></span>

<span data-ttu-id="6d514-105">Die Signatur Tabelle enthält die Informationen, die eine Datei Signatur eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="6d514-105">The Signature table holds the information that uniquely identifies a file signature.</span></span> <span data-ttu-id="6d514-106">Weitere Informationen zu Signaturen finden Sie unter [digitale Signaturen und Windows Installer](digital-signatures-and-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="6d514-106">For more information regarding signatures see [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md).</span></span>

<span data-ttu-id="6d514-107">Die Signatur Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="6d514-107">The Signature table has the following columns.</span></span>



| <span data-ttu-id="6d514-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="6d514-108">Column</span></span>     | <span data-ttu-id="6d514-109">Typ</span><span class="sxs-lookup"><span data-stu-id="6d514-109">Type</span></span>                               | <span data-ttu-id="6d514-110">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="6d514-110">Key</span></span> | <span data-ttu-id="6d514-111">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="6d514-111">Nullable</span></span> |
|------------|------------------------------------|-----|----------|
| <span data-ttu-id="6d514-112">Signatur</span><span class="sxs-lookup"><span data-stu-id="6d514-112">Signature</span></span>  | [<span data-ttu-id="6d514-113">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="6d514-113">Identifier</span></span>](identifier.md)       | <span data-ttu-id="6d514-114">J</span><span class="sxs-lookup"><span data-stu-id="6d514-114">Y</span></span>   | <span data-ttu-id="6d514-115">N</span><span class="sxs-lookup"><span data-stu-id="6d514-115">N</span></span>        |
| <span data-ttu-id="6d514-116">FileName</span><span class="sxs-lookup"><span data-stu-id="6d514-116">FileName</span></span>   | [<span data-ttu-id="6d514-117">Text</span><span class="sxs-lookup"><span data-stu-id="6d514-117">Text</span></span>](text.md)                   | <span data-ttu-id="6d514-118">N</span><span class="sxs-lookup"><span data-stu-id="6d514-118">N</span></span>   | <span data-ttu-id="6d514-119">N</span><span class="sxs-lookup"><span data-stu-id="6d514-119">N</span></span>        |
| <span data-ttu-id="6d514-120">MinVersion</span><span class="sxs-lookup"><span data-stu-id="6d514-120">MinVersion</span></span> | [<span data-ttu-id="6d514-121">Text</span><span class="sxs-lookup"><span data-stu-id="6d514-121">Text</span></span>](text.md)                   | <span data-ttu-id="6d514-122">N</span><span class="sxs-lookup"><span data-stu-id="6d514-122">N</span></span>   | <span data-ttu-id="6d514-123">J</span><span class="sxs-lookup"><span data-stu-id="6d514-123">Y</span></span>        |
| <span data-ttu-id="6d514-124">MaxVersion</span><span class="sxs-lookup"><span data-stu-id="6d514-124">MaxVersion</span></span> | [<span data-ttu-id="6d514-125">Text</span><span class="sxs-lookup"><span data-stu-id="6d514-125">Text</span></span>](text.md)                   | <span data-ttu-id="6d514-126">N</span><span class="sxs-lookup"><span data-stu-id="6d514-126">N</span></span>   | <span data-ttu-id="6d514-127">J</span><span class="sxs-lookup"><span data-stu-id="6d514-127">Y</span></span>        |
| <span data-ttu-id="6d514-128">MinSize</span><span class="sxs-lookup"><span data-stu-id="6d514-128">MinSize</span></span>    | [<span data-ttu-id="6d514-129">Doubleiteger</span><span class="sxs-lookup"><span data-stu-id="6d514-129">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="6d514-130">N</span><span class="sxs-lookup"><span data-stu-id="6d514-130">N</span></span>   | <span data-ttu-id="6d514-131">J</span><span class="sxs-lookup"><span data-stu-id="6d514-131">Y</span></span>        |
| <span data-ttu-id="6d514-132">MaxSize</span><span class="sxs-lookup"><span data-stu-id="6d514-132">MaxSize</span></span>    | [<span data-ttu-id="6d514-133">Doubleiteger</span><span class="sxs-lookup"><span data-stu-id="6d514-133">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="6d514-134">N</span><span class="sxs-lookup"><span data-stu-id="6d514-134">N</span></span>   | <span data-ttu-id="6d514-135">J</span><span class="sxs-lookup"><span data-stu-id="6d514-135">Y</span></span>        |
| <span data-ttu-id="6d514-136">MinDate</span><span class="sxs-lookup"><span data-stu-id="6d514-136">MinDate</span></span>    | [<span data-ttu-id="6d514-137">Doubleiteger</span><span class="sxs-lookup"><span data-stu-id="6d514-137">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="6d514-138">N</span><span class="sxs-lookup"><span data-stu-id="6d514-138">N</span></span>   | <span data-ttu-id="6d514-139">J</span><span class="sxs-lookup"><span data-stu-id="6d514-139">Y</span></span>        |
| <span data-ttu-id="6d514-140">MaxDate</span><span class="sxs-lookup"><span data-stu-id="6d514-140">MaxDate</span></span>    | [<span data-ttu-id="6d514-141">Doubleiteger</span><span class="sxs-lookup"><span data-stu-id="6d514-141">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="6d514-142">N</span><span class="sxs-lookup"><span data-stu-id="6d514-142">N</span></span>   | <span data-ttu-id="6d514-143">J</span><span class="sxs-lookup"><span data-stu-id="6d514-143">Y</span></span>        |
| <span data-ttu-id="6d514-144">Sprachen</span><span class="sxs-lookup"><span data-stu-id="6d514-144">Languages</span></span>  | [<span data-ttu-id="6d514-145">Text</span><span class="sxs-lookup"><span data-stu-id="6d514-145">Text</span></span>](text.md)                   | <span data-ttu-id="6d514-146">N</span><span class="sxs-lookup"><span data-stu-id="6d514-146">N</span></span>   | <span data-ttu-id="6d514-147">J</span><span class="sxs-lookup"><span data-stu-id="6d514-147">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="6d514-148">Spalten</span><span class="sxs-lookup"><span data-stu-id="6d514-148">Columns</span></span>

<dl> <dt>

<span data-ttu-id="6d514-149"><span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Unter</span><span class="sxs-lookup"><span data-stu-id="6d514-149"><span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Signature</span></span>
</dt> <dd>

<span data-ttu-id="6d514-150">Die Signatur Spalte ist eine eindeutige Datei Signatur.</span><span class="sxs-lookup"><span data-stu-id="6d514-150">The Signature column is a unique file signature.</span></span>

</dd> <dt>

<span data-ttu-id="6d514-151"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Einfügen</span><span class="sxs-lookup"><span data-stu-id="6d514-151"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>FileName</span></span>
</dt> <dd>

<span data-ttu-id="6d514-152">Der Name der Datei.</span><span class="sxs-lookup"><span data-stu-id="6d514-152">The name of the file.</span></span>

</dd> <dt>

<span data-ttu-id="6d514-153"><span id="MinVersion"></span><span id="minversion"></span><span id="MINVERSION"></span>MinVersion</span><span class="sxs-lookup"><span data-stu-id="6d514-153"><span id="MinVersion"></span><span id="minversion"></span><span id="MINVERSION"></span>MinVersion</span></span>
</dt> <dd>

<span data-ttu-id="6d514-154">Die minimale Version der Datei mit einem sprach Vergleich.</span><span class="sxs-lookup"><span data-stu-id="6d514-154">The minimum version of the file, with a language comparison.</span></span> <span data-ttu-id="6d514-155">Wenn dieses Feld angegeben wird, muss die Datei eine Version aufweisen, die mindestens mit MinVersion identisch ist.</span><span class="sxs-lookup"><span data-stu-id="6d514-155">If this field is specified, then the file must have a version that is at least equal to MinVersion.</span></span> <span data-ttu-id="6d514-156">Wenn die Datei eine gleiche Version wie der Wert für das MinVersion-Feld aufweist, die in der Spalte Sprachen angegebene Sprache jedoch unterschiedlich ist, erfüllt die Datei die Signatur Filterkriterien nicht.</span><span class="sxs-lookup"><span data-stu-id="6d514-156">If the file has an equal version to the MinVersion field value but the language specified in the Languages column differs, the file does not satisfy the signature filter criteria.</span></span>

> [!Note]  
> <span data-ttu-id="6d514-157">Die in der Spalte Sprachen angegebene Sprache wird im Vergleich verwendet, und es gibt keine Möglichkeit, die Sprache zu ignorieren.</span><span class="sxs-lookup"><span data-stu-id="6d514-157">The language specified in the Languages column is used in the comparison and there is no way to ignore language.</span></span> <span data-ttu-id="6d514-158">Wenn eine Datei die MinVersion-Feld Anforderung unabhängig von der Sprache erfüllen soll, müssen Sie einen Wert im MinVersion-Feld eingeben, der einen Wert kleiner als der tatsächliche Wert ist.</span><span class="sxs-lookup"><span data-stu-id="6d514-158">If you want a file to meet the MinVersion field requirement regardless of language, you must enter a value in the MinVersion field that is one less than the actual value.</span></span> <span data-ttu-id="6d514-159">Wenn die Mindestversion für den Filter beispielsweise 2.0.2600.1183 ist, verwenden Sie 2.0.2600.1182, um die Datei zu suchen, ohne die Sprachinformationen zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6d514-159">For example, if the minimum version for the filter is 2.0.2600.1183, use 2.0.2600.1182 to find the file without matching the language information.</span></span>

 

</dd> <dt>

<span data-ttu-id="6d514-160"><span id="MaxVersion"></span><span id="maxversion"></span><span id="MAXVERSION"></span>MaxVersion</span><span class="sxs-lookup"><span data-stu-id="6d514-160"><span id="MaxVersion"></span><span id="maxversion"></span><span id="MAXVERSION"></span>MaxVersion</span></span>
</dt> <dd>

<span data-ttu-id="6d514-161">Die maximale Version der Datei.</span><span class="sxs-lookup"><span data-stu-id="6d514-161">The maximum version of the file.</span></span> <span data-ttu-id="6d514-162">Wenn dieses Feld angegeben wird, muss die Datei eine Version aufweisen, die höchstens MaxVersion entspricht.</span><span class="sxs-lookup"><span data-stu-id="6d514-162">If this field is specified, then the file must have a version that is at most equal to MaxVersion.</span></span>

</dd> <dt>

<span data-ttu-id="6d514-163"><span id="MinSize"></span><span id="minsize"></span><span id="MINSIZE"></span>MinSize</span><span class="sxs-lookup"><span data-stu-id="6d514-163"><span id="MinSize"></span><span id="minsize"></span><span id="MINSIZE"></span>MinSize</span></span>
</dt> <dd>

<span data-ttu-id="6d514-164">Die minimale Größe der Datei.</span><span class="sxs-lookup"><span data-stu-id="6d514-164">The minimum size of the file.</span></span> <span data-ttu-id="6d514-165">Wenn dieses Feld angegeben ist, muss die zu überprüfende Datei eine Größe aufweisen, die mindestens MinSize entspricht.</span><span class="sxs-lookup"><span data-stu-id="6d514-165">If this field is specified, then the file under inspection must have a size that is at least equal to MinSize.</span></span> <span data-ttu-id="6d514-166">Dabei muss es sich um eine nicht negative Zahl handeln.</span><span class="sxs-lookup"><span data-stu-id="6d514-166">This must be a non-negative number.</span></span>

</dd> <dt>

<span data-ttu-id="6d514-167"><span id="MaxSize"></span><span id="maxsize"></span><span id="MAXSIZE"></span>MaxSize</span><span class="sxs-lookup"><span data-stu-id="6d514-167"><span id="MaxSize"></span><span id="maxsize"></span><span id="MAXSIZE"></span>MaxSize</span></span>
</dt> <dd>

<span data-ttu-id="6d514-168">Die maximale Größe der Datei.</span><span class="sxs-lookup"><span data-stu-id="6d514-168">The maximum size of the file.</span></span> <span data-ttu-id="6d514-169">Wenn dieses Feld angegeben ist, muss die zu überprüfende Datei eine Größe aufweisen, die höchstens MaxSize entspricht.</span><span class="sxs-lookup"><span data-stu-id="6d514-169">If this field is specified, then the file under inspection must have a size that is at most equal to MaxSize.</span></span> <span data-ttu-id="6d514-170">Dabei muss es sich um eine nicht negative Zahl handeln.</span><span class="sxs-lookup"><span data-stu-id="6d514-170">This must be a non-negative number.</span></span>

</dd> <dt>

<span data-ttu-id="6d514-171"><span id="MinDate"></span><span id="mindate"></span><span id="MINDATE"></span>MinDate</span><span class="sxs-lookup"><span data-stu-id="6d514-171"><span id="MinDate"></span><span id="mindate"></span><span id="MINDATE"></span>MinDate</span></span>
</dt> <dd>

<span data-ttu-id="6d514-172">Der minimale Änderungs Zeitpunkt (Datum und Uhrzeit) der Datei.</span><span class="sxs-lookup"><span data-stu-id="6d514-172">The minimum modification date and time of the file.</span></span> <span data-ttu-id="6d514-173">Wenn dieses Feld angegeben ist, muss die zu überprüfende Datei ein Änderungsdatum und eine Uhrzeit aufweisen, die mindestens MinDate entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6d514-173">If this field is specified, then the file under inspection must have a modification date and time that is at least equal to MinDate.</span></span> <span data-ttu-id="6d514-174">Dabei muss es sich um eine nicht negative Zahl handeln.</span><span class="sxs-lookup"><span data-stu-id="6d514-174">This must be a non-negative number.</span></span> <span data-ttu-id="6d514-175">Das Format dieses Felds besteht aus zwei packenden 16-Bit-Werten vom Typ **Word**.</span><span class="sxs-lookup"><span data-stu-id="6d514-175">The format of this field is two packed 16-bit values of type **WORD**.</span></span> <span data-ttu-id="6d514-176">Der Wert für das hohe Bestell **Wort** gibt das Datum im MS-DOS-Datumsformat an.</span><span class="sxs-lookup"><span data-stu-id="6d514-176">The high order **WORD** value specifies the date in MS-DOS date format.</span></span> <span data-ttu-id="6d514-177">Der **Word** -Wert mit niedriger Ordnung gibt die Zeit im MS-DOS-Zeitformat an.</span><span class="sxs-lookup"><span data-stu-id="6d514-177">The low order **WORD** value specifies the time in MS-DOS time format.</span></span> <span data-ttu-id="6d514-178">Der Wert 0 für den Uhrzeitwert ist Mitternacht.</span><span class="sxs-lookup"><span data-stu-id="6d514-178">A value of 0 for the time value represents midnight.</span></span> <span data-ttu-id="6d514-179">Weitere Informationen finden Sie im Abschnitt mit den Hinweisen.</span><span class="sxs-lookup"><span data-stu-id="6d514-179">See the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="6d514-180"><span id="MaxDate"></span><span id="maxdate"></span><span id="MAXDATE"></span>MaxDate</span><span class="sxs-lookup"><span data-stu-id="6d514-180"><span id="MaxDate"></span><span id="maxdate"></span><span id="MAXDATE"></span>MaxDate</span></span>
</dt> <dd>

<span data-ttu-id="6d514-181">Das maximale Erstellungsdatum der Datei.</span><span class="sxs-lookup"><span data-stu-id="6d514-181">The maximum creation date of the file.</span></span> <span data-ttu-id="6d514-182">Wenn dieses Feld angegeben ist, muss die zu überprüfende Datei ein Erstellungsdatum aufweisen, das höchstens MaxDate entspricht.</span><span class="sxs-lookup"><span data-stu-id="6d514-182">If this field is specified, then the file under inspection must have a creation date that is at most equal to MaxDate.</span></span> <span data-ttu-id="6d514-183">Dabei muss es sich um eine nicht negative Zahl handeln.</span><span class="sxs-lookup"><span data-stu-id="6d514-183">This must be a non-negative number.</span></span> <span data-ttu-id="6d514-184">Das Format dieses Felds besteht aus zwei packenden 16-Bit-Werten vom Typ **Word**.</span><span class="sxs-lookup"><span data-stu-id="6d514-184">The format of this field is two packed 16-bit values of type **WORD**.</span></span> <span data-ttu-id="6d514-185">Der Wert für das hohe Bestell **Wort** gibt das Datum im MS-DOS-Datumsformat an.</span><span class="sxs-lookup"><span data-stu-id="6d514-185">The high order **WORD** value specifies the date in MS-DOS date format.</span></span> <span data-ttu-id="6d514-186">Der **Word** -Wert mit niedriger Ordnung gibt die Zeit im MS-DOS-Zeitformat an.</span><span class="sxs-lookup"><span data-stu-id="6d514-186">The low order **WORD** value specifies the time in MS-DOS time format.</span></span> <span data-ttu-id="6d514-187">Der Wert 0 für den Uhrzeitwert ist Mitternacht.</span><span class="sxs-lookup"><span data-stu-id="6d514-187">A value of 0 for the time value represent midnight.</span></span> <span data-ttu-id="6d514-188">Weitere Informationen finden Sie im Abschnitt mit den Hinweisen.</span><span class="sxs-lookup"><span data-stu-id="6d514-188">See the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="6d514-189"><span id="Languages"></span><span id="languages"></span><span id="LANGUAGES"></span>Sprachen</span><span class="sxs-lookup"><span data-stu-id="6d514-189"><span id="Languages"></span><span id="languages"></span><span id="LANGUAGES"></span>Languages</span></span>
</dt> <dd>

<span data-ttu-id="6d514-190">Die von der Datei unterstützten Sprachen.</span><span class="sxs-lookup"><span data-stu-id="6d514-190">The languages supported by the file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6d514-191">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6d514-191">Remarks</span></span>

<span data-ttu-id="6d514-192">Diese Tabelle wird mit der [AppSearch-Tabelle](appsearch-table.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="6d514-192">This table is used with the [AppSearch Table](appsearch-table.md).</span></span>

<span data-ttu-id="6d514-193">Die Signatur wird mithilfe der [reglocator-Tabelle](reglocator-table.md), der [inilocator](inilocator-table.md)-Tabelle, der [complocator](complocator-table.md)-Tabelle und der [drlocator-Tabelle](drlocator-table.md)durchsucht.</span><span class="sxs-lookup"><span data-stu-id="6d514-193">The signature is searched for using the [RegLocator table](reglocator-table.md), the [IniLocator table](inilocator-table.md), the [CompLocator table](complocator-table.md), and the [DrLocator table](drlocator-table.md).</span></span> <span data-ttu-id="6d514-194">Die Spalten dieser Tabelle sind im Allgemeinen nicht lokalisiert.</span><span class="sxs-lookup"><span data-stu-id="6d514-194">This table's columns are generally not localized.</span></span> <span data-ttu-id="6d514-195">Wenn ein Autor eine Suche nach Produkten in mehreren Sprachen beschließt, kann in der Tabelle für jede Sprache ein separater Eintrag enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="6d514-195">If an author decides to search for products in multiple languages, then there can be a separate entry included in the table for each language.</span></span>

<span data-ttu-id="6d514-196">Die Signatur Tabelle folgt in der Regel den Windows Installer [Datei Versions Regeln](file-versioning-rules.md).</span><span class="sxs-lookup"><span data-stu-id="6d514-196">The Signature table generally follows the Windows Installer [File Versioning Rules](file-versioning-rules.md).</span></span> <span data-ttu-id="6d514-197">Die in der Spalte Sprachen der Signatur Tabelle angegebenen Sprachen werden nur ausgewertet, wenn die Dateiversionen äquivalent sind.</span><span class="sxs-lookup"><span data-stu-id="6d514-197">Languages specified in the Languages column of the Signature table are not evaluated unless the file versions are equivalent.</span></span> <span data-ttu-id="6d514-198">In der Spalte Sprachen wird sichergestellt, dass eine Datei eine bestimmte Sprache hat, wenn Sie die angeforderte Version hat.</span><span class="sxs-lookup"><span data-stu-id="6d514-198">The Languages column will ensure that a file is of a particular language if it is of the requested version.</span></span> <span data-ttu-id="6d514-199">Es ist keine Methode zum Ignorieren der Spalte Sprachen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6d514-199">There is no method available to ignore the Languages column.</span></span> <span data-ttu-id="6d514-200">Ein in die Spalte Sprachen eingegebener NULL-Wert wird als Datei ohne Sprache behandelt und entspricht nicht der Datei Signatur einer Datei, die in der Signatur Tabelle enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="6d514-200">A NULL value entered in the Languages column is treated as a file without a language and does not match the file signature of a file with a language appearing in the Signature table.</span></span> <span data-ttu-id="6d514-201">Im folgenden Beispiel wird nach einer bestimmten Version von MSI.DLL gesucht.</span><span class="sxs-lookup"><span data-stu-id="6d514-201">The following example searches for a particular version of MSI.DLL.</span></span>

[<span data-ttu-id="6d514-202">Drlocator-Tabelle</span><span class="sxs-lookup"><span data-stu-id="6d514-202">DrLocator table</span></span>](drlocator-table.md)

| <span data-ttu-id="6d514-203">Signatur\_</span><span class="sxs-lookup"><span data-stu-id="6d514-203">Signature\_</span></span> | <span data-ttu-id="6d514-204">Parent</span><span class="sxs-lookup"><span data-stu-id="6d514-204">Parent</span></span> | <span data-ttu-id="6d514-205">Pfad</span><span class="sxs-lookup"><span data-stu-id="6d514-205">Path</span></span>                  | <span data-ttu-id="6d514-206">Tiefe</span><span class="sxs-lookup"><span data-stu-id="6d514-206">Depth</span></span> |
|-------------|--------|-----------------------|-------|
| <span data-ttu-id="6d514-207">MsiDll</span><span class="sxs-lookup"><span data-stu-id="6d514-207">MsiDll</span></span>      | <span data-ttu-id="6d514-208">normal</span><span class="sxs-lookup"><span data-stu-id="6d514-208">{null}</span></span> | <span data-ttu-id="6d514-209">c: \\ Windows \\ system32</span><span class="sxs-lookup"><span data-stu-id="6d514-209">c:\\windows\\system32</span></span> | <span data-ttu-id="6d514-210">0</span><span class="sxs-lookup"><span data-stu-id="6d514-210">0</span></span>     |



 

[<span data-ttu-id="6d514-211">AppSearch-Tabelle</span><span class="sxs-lookup"><span data-stu-id="6d514-211">AppSearch Table</span></span>](appsearch-table.md)



| <span data-ttu-id="6d514-212">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6d514-212">Property</span></span> | <span data-ttu-id="6d514-213">Signatur\_</span><span class="sxs-lookup"><span data-stu-id="6d514-213">Signature\_</span></span> |
|----------|-------------|
| <span data-ttu-id="6d514-214">MSIDLL</span><span class="sxs-lookup"><span data-stu-id="6d514-214">MSIDLL</span></span>   | <span data-ttu-id="6d514-215">MsiDll</span><span class="sxs-lookup"><span data-stu-id="6d514-215">MsiDll</span></span>      |



 

<span data-ttu-id="6d514-216">Signatur Tabelle</span><span class="sxs-lookup"><span data-stu-id="6d514-216">Signature table</span></span>



| <span data-ttu-id="6d514-217">Signatur</span><span class="sxs-lookup"><span data-stu-id="6d514-217">Signature</span></span> | <span data-ttu-id="6d514-218">FileName</span><span class="sxs-lookup"><span data-stu-id="6d514-218">FileName</span></span> | <span data-ttu-id="6d514-219">MinVersion</span><span class="sxs-lookup"><span data-stu-id="6d514-219">MinVersion</span></span>    | <span data-ttu-id="6d514-220">MaxVersion</span><span class="sxs-lookup"><span data-stu-id="6d514-220">MaxVersion</span></span> | <span data-ttu-id="6d514-221">MinSize</span><span class="sxs-lookup"><span data-stu-id="6d514-221">MinSize</span></span> | <span data-ttu-id="6d514-222">MaxSize</span><span class="sxs-lookup"><span data-stu-id="6d514-222">MaxSize</span></span> | <span data-ttu-id="6d514-223">MinDate</span><span class="sxs-lookup"><span data-stu-id="6d514-223">MinDate</span></span> | <span data-ttu-id="6d514-224">MaxDate</span><span class="sxs-lookup"><span data-stu-id="6d514-224">MaxDate</span></span> | <span data-ttu-id="6d514-225">Sprachen</span><span class="sxs-lookup"><span data-stu-id="6d514-225">Languages</span></span> |
|-----------|----------|---------------|------------|---------|---------|---------|---------|-----------|
| <span data-ttu-id="6d514-226">MsiDll</span><span class="sxs-lookup"><span data-stu-id="6d514-226">MsiDll</span></span>    | <span data-ttu-id="6d514-227">msi.dll</span><span class="sxs-lookup"><span data-stu-id="6d514-227">msi.dll</span></span>  | <span data-ttu-id="6d514-228">2.0.2600.1106</span><span class="sxs-lookup"><span data-stu-id="6d514-228">2.0.2600.1106</span></span> | <span data-ttu-id="6d514-229">normal</span><span class="sxs-lookup"><span data-stu-id="6d514-229">{null}</span></span>     | <span data-ttu-id="6d514-230">normal</span><span class="sxs-lookup"><span data-stu-id="6d514-230">{null}</span></span>  | <span data-ttu-id="6d514-231">normal</span><span class="sxs-lookup"><span data-stu-id="6d514-231">{null}</span></span>  | <span data-ttu-id="6d514-232">normal</span><span class="sxs-lookup"><span data-stu-id="6d514-232">{null}</span></span>  | <span data-ttu-id="6d514-233">normal</span><span class="sxs-lookup"><span data-stu-id="6d514-233">{null}</span></span>  | <span data-ttu-id="6d514-234">0</span><span class="sxs-lookup"><span data-stu-id="6d514-234">0</span></span>         |



 

<span data-ttu-id="6d514-235">In diesem Fall und unter Windows XP SP1 legt die [AppSearch-Aktion](appsearch-action.md) msidll auf c: \\ Windows System32msi.dll fest, \\ \\ da MSI.DLL eine sprachneutrale Datei ist.</span><span class="sxs-lookup"><span data-stu-id="6d514-235">In this case, and on Windows XP SP1, the [AppSearch action](appsearch-action.md) sets MSIDLL to c:\\windows\\system32\\msi.dll because MSI.DLL is a language neutral file.</span></span> <span data-ttu-id="6d514-236">Wenn der Wert der Sprachen-Spalte von 0 in 1033 geändert wird, kann die AppSearch-Aktion die übereinstimmende msi.dll nicht finden, und die msidll-Eigenschaft ist nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="6d514-236">If the value of the Languages column is changed from 0 to 1033, then the AppSearch action fails to find the matching msi.dll and the MSIDLL property is undefined.</span></span>

<span data-ttu-id="6d514-237">Sie können die Signatur Tabelle nicht zum Abfragen von Sprachen allein verwenden.</span><span class="sxs-lookup"><span data-stu-id="6d514-237">You cannot use the Signature table to query on languages alone.</span></span> <span data-ttu-id="6d514-238">Um nach verschiedenen Sprachversionen einer Datei zu suchen, benötigen Sie einen separaten Eintrag in der Signatur Tabelle für jede Sprachversion.</span><span class="sxs-lookup"><span data-stu-id="6d514-238">To search for different language versions of a file, you must have a separate entry in the Signature table for each language version.</span></span> <span data-ttu-id="6d514-239">Wenn in der Spalte Sprachen mehrere Sprachen bereitgestellt werden, ist die Suche nach einer Datei, die alle diese Sprachen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6d514-239">If multiple languages are provided in the Languages column, then the search is for a file that supports all of those languages.</span></span>

<span data-ttu-id="6d514-240">Das Format der Spalten MinDate und MaxDate sind zwei gepackte 16-Bit-Werte vom Typ **Word**.</span><span class="sxs-lookup"><span data-stu-id="6d514-240">The format of MinDate and MaxDate columns are two packed 16-bit values of type **WORD**.</span></span>

<span data-ttu-id="6d514-241">Datums **Wort**</span><span class="sxs-lookup"><span data-stu-id="6d514-241">Date **WORD**</span></span>



| <span data-ttu-id="6d514-242">Bits</span><span class="sxs-lookup"><span data-stu-id="6d514-242">Bits</span></span> | <span data-ttu-id="6d514-243">Inhalt</span><span class="sxs-lookup"><span data-stu-id="6d514-243">Content</span></span>                                             |
|------|-----------------------------------------------------|
| <span data-ttu-id="6d514-244">0 – 4</span><span class="sxs-lookup"><span data-stu-id="6d514-244">0–4</span></span>  | <span data-ttu-id="6d514-245">Tag des Monats (1-31)</span><span class="sxs-lookup"><span data-stu-id="6d514-245">Day of the month (1-31)</span></span>                             |
| <span data-ttu-id="6d514-246">5-8</span><span class="sxs-lookup"><span data-stu-id="6d514-246">5-8</span></span>  | <span data-ttu-id="6d514-247">Monat (1 = Januar, 2 = Februar usw.)</span><span class="sxs-lookup"><span data-stu-id="6d514-247">Month (1 = January, 2 = February, and so on)</span></span>        |
| <span data-ttu-id="6d514-248">9-15</span><span class="sxs-lookup"><span data-stu-id="6d514-248">9-15</span></span> | <span data-ttu-id="6d514-249">Jahr Offset von 1980 (Hinzufügen von 1980, um das tatsächliche Jahr zu erhalten)</span><span class="sxs-lookup"><span data-stu-id="6d514-249">Year offset from 1980 (add 1980 to get actual year)</span></span> |



 

<span data-ttu-id="6d514-250">Zeit **Wort**</span><span class="sxs-lookup"><span data-stu-id="6d514-250">Time **WORD**</span></span>



| <span data-ttu-id="6d514-251">Bits</span><span class="sxs-lookup"><span data-stu-id="6d514-251">Bits</span></span>  | <span data-ttu-id="6d514-252">Inhalt</span><span class="sxs-lookup"><span data-stu-id="6d514-252">Content</span></span>                     |
|-------|-----------------------------|
| <span data-ttu-id="6d514-253">0 – 4</span><span class="sxs-lookup"><span data-stu-id="6d514-253">0–4</span></span>   | <span data-ttu-id="6d514-254">Sekunden geteilt durch 2</span><span class="sxs-lookup"><span data-stu-id="6d514-254">Seconds divided by 2</span></span>        |
| <span data-ttu-id="6d514-255">5-10</span><span class="sxs-lookup"><span data-stu-id="6d514-255">5-10</span></span>  | <span data-ttu-id="6d514-256">Minuten (0-59)</span><span class="sxs-lookup"><span data-stu-id="6d514-256">Minutes (0-59)</span></span>              |
| <span data-ttu-id="6d514-257">11-15</span><span class="sxs-lookup"><span data-stu-id="6d514-257">11-15</span></span> | <span data-ttu-id="6d514-258">Stunde (0 bis 23 Uhr auf 24 Stunden)</span><span class="sxs-lookup"><span data-stu-id="6d514-258">Hour(0-23 on 24 hour clock)</span></span> |



 

<span data-ttu-id="6d514-259">Die Formel zum Berechnen der Werte für MinDate und MaxDate ist:</span><span class="sxs-lookup"><span data-stu-id="6d514-259">The formula for calculating the MinDate and MaxDate field values is:</span></span>

<span data-ttu-id="6d514-260">((Jahr-1980) \* 512 + Monat \* 32 + Tag) \* 65536 + Stunden \* 2048 + Minuten \* 32 + Sekunden/2</span><span class="sxs-lookup"><span data-stu-id="6d514-260">( (Year - 1980) \* 512 + Month \* 32 + Day ) \* 65536 + Hours \* 2048 + Minutes \* 32 + Seconds/2</span></span>

## <a name="validation"></a><span data-ttu-id="6d514-261">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="6d514-261">Validation</span></span>

<dl>

[<span data-ttu-id="6d514-262">ICE03</span><span class="sxs-lookup"><span data-stu-id="6d514-262">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="6d514-263">ICE06</span><span class="sxs-lookup"><span data-stu-id="6d514-263">ICE06</span></span>](ice06.md)  
</dl>

 

 



