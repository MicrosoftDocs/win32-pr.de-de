---
description: Die \_ Validierungs Tabelle ist eine Systemtabelle, die die Spaltennamen und die Spaltenwerte für alle Tabellen in der Datenbank enthält.
ms.assetid: 52b1c537-efb6-4bb8-9e7f-b4848be52a71
title: _Validation Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 666f00ccccda11706dce6a8d7e04e0efea91b7cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864543"
---
# <a name="_validation-table"></a><span data-ttu-id="9a6a2-103">\_Validierungs Tabelle</span><span class="sxs-lookup"><span data-stu-id="9a6a2-103">\_Validation Table</span></span>

<span data-ttu-id="9a6a2-104">Die \_ Validierungs Tabelle ist eine Systemtabelle, die die Spaltennamen und die Spaltenwerte für alle Tabellen in der Datenbank enthält.</span><span class="sxs-lookup"><span data-stu-id="9a6a2-104">The \_Validation table is a system table that contains the column names and the column values for all of the tables in the database.</span></span> <span data-ttu-id="9a6a2-105">Sie wird während des Daten Bank Überprüfungsprozesses verwendet, um sicherzustellen, dass alle Spalten berücksichtigt werden und die richtigen Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="9a6a2-105">It is used during the database validation process to ensure that all columns are accounted for and have the correct values.</span></span> <span data-ttu-id="9a6a2-106">Diese Tabelle wird nicht mit der Installer-Datenbank ausgeliefert.</span><span class="sxs-lookup"><span data-stu-id="9a6a2-106">This table is not shipped with the installer database.</span></span>

<span data-ttu-id="9a6a2-107">Die \_ Validierungs Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="9a6a2-107">The \_Validation table has the following columns.</span></span>



| <span data-ttu-id="9a6a2-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="9a6a2-108">Column</span></span>      | <span data-ttu-id="9a6a2-109">Typ</span><span class="sxs-lookup"><span data-stu-id="9a6a2-109">Type</span></span>                               | <span data-ttu-id="9a6a2-110">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="9a6a2-110">Key</span></span> | <span data-ttu-id="9a6a2-111">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="9a6a2-111">Nullable</span></span> |
|-------------|------------------------------------|-----|----------|
| <span data-ttu-id="9a6a2-112">Tabelle</span><span class="sxs-lookup"><span data-stu-id="9a6a2-112">Table</span></span>       | [<span data-ttu-id="9a6a2-113">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="9a6a2-113">Identifier</span></span>](identifier.md)       | <span data-ttu-id="9a6a2-114">J</span><span class="sxs-lookup"><span data-stu-id="9a6a2-114">Y</span></span>   | <span data-ttu-id="9a6a2-115">N</span><span class="sxs-lookup"><span data-stu-id="9a6a2-115">N</span></span>        |
| <span data-ttu-id="9a6a2-116">Column</span><span class="sxs-lookup"><span data-stu-id="9a6a2-116">Column</span></span>      | [<span data-ttu-id="9a6a2-117">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="9a6a2-117">Identifier</span></span>](identifier.md)       | <span data-ttu-id="9a6a2-118">J</span><span class="sxs-lookup"><span data-stu-id="9a6a2-118">Y</span></span>   | <span data-ttu-id="9a6a2-119">N</span><span class="sxs-lookup"><span data-stu-id="9a6a2-119">N</span></span>        |
| <span data-ttu-id="9a6a2-120">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="9a6a2-120">Nullable</span></span>    | [<span data-ttu-id="9a6a2-121">Text</span><span class="sxs-lookup"><span data-stu-id="9a6a2-121">Text</span></span>](text.md)                   | <span data-ttu-id="9a6a2-122">N</span><span class="sxs-lookup"><span data-stu-id="9a6a2-122">N</span></span>   | <span data-ttu-id="9a6a2-123">N</span><span class="sxs-lookup"><span data-stu-id="9a6a2-123">N</span></span>        |
| <span data-ttu-id="9a6a2-124">MinValue</span><span class="sxs-lookup"><span data-stu-id="9a6a2-124">MinValue</span></span>    | [<span data-ttu-id="9a6a2-125">Doubleiteger</span><span class="sxs-lookup"><span data-stu-id="9a6a2-125">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="9a6a2-126">N</span><span class="sxs-lookup"><span data-stu-id="9a6a2-126">N</span></span>   | <span data-ttu-id="9a6a2-127">J</span><span class="sxs-lookup"><span data-stu-id="9a6a2-127">Y</span></span>        |
| <span data-ttu-id="9a6a2-128">MaxValue</span><span class="sxs-lookup"><span data-stu-id="9a6a2-128">MaxValue</span></span>    | [<span data-ttu-id="9a6a2-129">Doubleiteger</span><span class="sxs-lookup"><span data-stu-id="9a6a2-129">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="9a6a2-130">N</span><span class="sxs-lookup"><span data-stu-id="9a6a2-130">N</span></span>   | <span data-ttu-id="9a6a2-131">J</span><span class="sxs-lookup"><span data-stu-id="9a6a2-131">Y</span></span>        |
| <span data-ttu-id="9a6a2-132">KeyTable</span><span class="sxs-lookup"><span data-stu-id="9a6a2-132">KeyTable</span></span>    | [<span data-ttu-id="9a6a2-133">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="9a6a2-133">Identifier</span></span>](identifier.md)       | <span data-ttu-id="9a6a2-134">N</span><span class="sxs-lookup"><span data-stu-id="9a6a2-134">N</span></span>   | <span data-ttu-id="9a6a2-135">J</span><span class="sxs-lookup"><span data-stu-id="9a6a2-135">Y</span></span>        |
| <span data-ttu-id="9a6a2-136">KeyColumn</span><span class="sxs-lookup"><span data-stu-id="9a6a2-136">KeyColumn</span></span>   | [<span data-ttu-id="9a6a2-137">Integer</span><span class="sxs-lookup"><span data-stu-id="9a6a2-137">Integer</span></span>](integer.md)             | <span data-ttu-id="9a6a2-138">N</span><span class="sxs-lookup"><span data-stu-id="9a6a2-138">N</span></span>   | <span data-ttu-id="9a6a2-139">J</span><span class="sxs-lookup"><span data-stu-id="9a6a2-139">Y</span></span>        |
| <span data-ttu-id="9a6a2-140">Category</span><span class="sxs-lookup"><span data-stu-id="9a6a2-140">Category</span></span>    | [<span data-ttu-id="9a6a2-141">Text</span><span class="sxs-lookup"><span data-stu-id="9a6a2-141">Text</span></span>](text.md)                   | <span data-ttu-id="9a6a2-142">N</span><span class="sxs-lookup"><span data-stu-id="9a6a2-142">N</span></span>   | <span data-ttu-id="9a6a2-143">J</span><span class="sxs-lookup"><span data-stu-id="9a6a2-143">Y</span></span>        |
| <span data-ttu-id="9a6a2-144">Set</span><span class="sxs-lookup"><span data-stu-id="9a6a2-144">Set</span></span>         | [<span data-ttu-id="9a6a2-145">Text</span><span class="sxs-lookup"><span data-stu-id="9a6a2-145">Text</span></span>](text.md)                   | <span data-ttu-id="9a6a2-146">N</span><span class="sxs-lookup"><span data-stu-id="9a6a2-146">N</span></span>   | <span data-ttu-id="9a6a2-147">J</span><span class="sxs-lookup"><span data-stu-id="9a6a2-147">Y</span></span>        |
| <span data-ttu-id="9a6a2-148">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9a6a2-148">Description</span></span> | [<span data-ttu-id="9a6a2-149">Text</span><span class="sxs-lookup"><span data-stu-id="9a6a2-149">Text</span></span>](text.md)                   | <span data-ttu-id="9a6a2-150">N</span><span class="sxs-lookup"><span data-stu-id="9a6a2-150">N</span></span>   | <span data-ttu-id="9a6a2-151">J</span><span class="sxs-lookup"><span data-stu-id="9a6a2-151">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="9a6a2-152">Spalten</span><span class="sxs-lookup"><span data-stu-id="9a6a2-152">Columns</span></span>

<dl> <dt>

<span data-ttu-id="9a6a2-153"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Glaub</span><span class="sxs-lookup"><span data-stu-id="9a6a2-153"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="9a6a2-154">Wird verwendet, um eine bestimmte Tabelle zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="9a6a2-154">Used to identify a particular table.</span></span> <span data-ttu-id="9a6a2-155">Dieser Schlüssel und der Spalten Schlüssel bilden den Primärschlüssel der \_ Validierungs Tabelle.</span><span class="sxs-lookup"><span data-stu-id="9a6a2-155">This key and the Column key form the primary key of the \_Validation table.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a2-156"><span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Kolumne</span><span class="sxs-lookup"><span data-stu-id="9a6a2-156"><span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Column</span></span>
</dt> <dd>

<span data-ttu-id="9a6a2-157">Wird verwendet, um eine bestimmte Spalte der Tabelle zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="9a6a2-157">Used to identify a particular column of the table.</span></span> <span data-ttu-id="9a6a2-158">Dieser Schlüssel und der Tabellenschlüssel bilden den Primärschlüssel der \_ Validierungs Tabelle.</span><span class="sxs-lookup"><span data-stu-id="9a6a2-158">This key and the Table key form the primary key of the \_Validation table.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a2-159"><span id="Nullable"></span><span id="nullable"></span><span id="NULLABLE"></span>Werte zulässt</span><span class="sxs-lookup"><span data-stu-id="9a6a2-159"><span id="Nullable"></span><span id="nullable"></span><span id="NULLABLE"></span>Nullable</span></span>
</dt> <dd>

<span data-ttu-id="9a6a2-160">Gibt an, ob die Spalte einen NULL-Wert enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="9a6a2-160">Identifies whether the column may contain a Null value.</span></span>

<span data-ttu-id="9a6a2-161">Diese Spalte kann einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="9a6a2-161">This column may have one of the following values.</span></span>



| <span data-ttu-id="9a6a2-162">String</span><span class="sxs-lookup"><span data-stu-id="9a6a2-162">String</span></span> | <span data-ttu-id="9a6a2-163">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9a6a2-163">Meaning</span></span>                                   |
|--------|-------------------------------------------|
| <span data-ttu-id="9a6a2-164">J</span><span class="sxs-lookup"><span data-stu-id="9a6a2-164">Y</span></span>      | <span data-ttu-id="9a6a2-165">Ja, die Spalte kann einen NULL-Wert aufweisen.</span><span class="sxs-lookup"><span data-stu-id="9a6a2-165">Yes, the column may have a Null value.</span></span>    |
| <span data-ttu-id="9a6a2-166">N</span><span class="sxs-lookup"><span data-stu-id="9a6a2-166">N</span></span>      | <span data-ttu-id="9a6a2-167">Nein, die Spalte darf keinen NULL-Wert aufweisen.</span><span class="sxs-lookup"><span data-stu-id="9a6a2-167">No, the column may not have a Null value.</span></span> |



 

</dd> <dt>

<span data-ttu-id="9a6a2-168"><span id="MinValue"></span><span id="minvalue"></span><span id="MINVALUE"></span>MinValue</span><span class="sxs-lookup"><span data-stu-id="9a6a2-168"><span id="MinValue"></span><span id="minvalue"></span><span id="MINVALUE"></span>MinValue</span></span>
</dt> <dd>

<span data-ttu-id="9a6a2-169">Dieses Feld gilt für Spalten mit einem numerischen Wert.</span><span class="sxs-lookup"><span data-stu-id="9a6a2-169">This field applies to columns having numeric value.</span></span> <span data-ttu-id="9a6a2-170">Das Feld enthält den minimal zulässigen Wert.</span><span class="sxs-lookup"><span data-stu-id="9a6a2-170">The field contains the minimum permissible value.</span></span> <span data-ttu-id="9a6a2-171">Dies kann der Minimalwert für eine ganze Zahl oder der minimale Wert für eine Datums-oder Versions Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="9a6a2-171">This can be the minimum value for an integer or the minimum value for a date or version string.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a2-172"><span id="MaxValue"></span><span id="maxvalue"></span><span id="MAXVALUE"></span>MaxValue</span><span class="sxs-lookup"><span data-stu-id="9a6a2-172"><span id="MaxValue"></span><span id="maxvalue"></span><span id="MAXVALUE"></span>MaxValue</span></span>
</dt> <dd>

<span data-ttu-id="9a6a2-173">Dieses Feld gilt für Spalten mit einem numerischen Wert.</span><span class="sxs-lookup"><span data-stu-id="9a6a2-173">This field applies to columns having numeric value.</span></span> <span data-ttu-id="9a6a2-174">Das Feld ist der maximal zulässige Wert.</span><span class="sxs-lookup"><span data-stu-id="9a6a2-174">The field is the maximum permissible value.</span></span> <span data-ttu-id="9a6a2-175">Dies kann der Höchstwert für eine ganze Zahl oder der Höchstwert für eine Datums-oder Versions Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="9a6a2-175">This may be the maximum value for an integer or the maximum value for a date or version string.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a2-176"><span id="KeyTable"></span><span id="keytable"></span><span id="KEYTABLE"></span>KeyTable</span><span class="sxs-lookup"><span data-stu-id="9a6a2-176"><span id="KeyTable"></span><span id="keytable"></span><span id="KEYTABLE"></span>KeyTable</span></span>
</dt> <dd>

<span data-ttu-id="9a6a2-177">Dieses Feld gilt für Spalten, bei denen es sich um externe Schlüssel handelt.</span><span class="sxs-lookup"><span data-stu-id="9a6a2-177">This field applies to columns that are external keys.</span></span> <span data-ttu-id="9a6a2-178">Das in column identifizierte Feld muss mit der durch KeyColumn angegebenen Spaltennummer in der Tabelle in keytable verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="9a6a2-178">The field identified in Column must link to the column number specified by KeyColumn in the table named in KeyTable.</span></span> <span data-ttu-id="9a6a2-179">Dabei kann es sich um eine durch Semikolons getrennte Liste von Tabellen handeln.</span><span class="sxs-lookup"><span data-stu-id="9a6a2-179">This can be a list of tables separated by semicolons.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a2-180"><span id="KeyColumn"></span><span id="keycolumn"></span><span id="KEYCOLUMN"></span>KeyColumn</span><span class="sxs-lookup"><span data-stu-id="9a6a2-180"><span id="KeyColumn"></span><span id="keycolumn"></span><span id="KEYCOLUMN"></span>KeyColumn</span></span>
</dt> <dd>

<span data-ttu-id="9a6a2-181">Dieses Feld gilt für Tabellen Spalten, bei denen es sich um externe Schlüssel handelt.</span><span class="sxs-lookup"><span data-stu-id="9a6a2-181">This field applies to table columns that are external keys.</span></span> <span data-ttu-id="9a6a2-182">Das in column identifizierte Feld muss mit der durch KeyColumn angegebenen Spaltennummer in der Tabelle in keytable verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="9a6a2-182">The field identified in Column must link to the column number specified by KeyColumn in the table named in KeyTable.</span></span> <span data-ttu-id="9a6a2-183">Der zulässige Bereich des KeyColumn-Felds ist 1-32.</span><span class="sxs-lookup"><span data-stu-id="9a6a2-183">The permissible range of the KeyColumn field is 1-32.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a2-184"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Kategorie</span><span class="sxs-lookup"><span data-stu-id="9a6a2-184"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Category</span></span>
</dt> <dd>

<span data-ttu-id="9a6a2-185">Dies ist der Datentyp, der im Datenbankfeld enthalten ist, das in den Tabellen-und Spalten Spalten der \_ Validierungs Tabelle angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="9a6a2-185">This is the type of data contained by the database field specified by the Table and Column columns of the \_Validation table.</span></span> <span data-ttu-id="9a6a2-186">Wenn dies ein Typ mit einem numerischen Wert ist, z. b. " [Integer](integer.md)", " [doubleinteger](doubleinteger.md) " oder " [time/date](time-date.md)", geben Sie in dieses Feld NULL ein, und geben Sie den Wertebereich mithilfe der Spalten MinValue und MaxValue an.</span><span class="sxs-lookup"><span data-stu-id="9a6a2-186">If this is a type having a numeric value, such as [Integer](integer.md), [DoubleInteger](doubleinteger.md) or [Time/Date](time-date.md), then enter null into this field and specify the value's range using the MinValue and MaxValue columns.</span></span> <span data-ttu-id="9a6a2-187">Verwenden Sie die Spalte Kategorie, um die nicht numerischen Datentypen anzugeben, die in den [Spaltendatentypen](column-data-types.md)beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="9a6a2-187">Use the Category column to specify the non-numeric data types described in [Column Data Types](column-data-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a6a2-188"><span id="Set"></span><span id="set"></span><span id="SET"></span>Set</span><span class="sxs-lookup"><span data-stu-id="9a6a2-188"><span id="Set"></span><span id="set"></span><span id="SET"></span>Set</span></span>
</dt> <dd>

<span data-ttu-id="9a6a2-189">Dies ist eine Liste zulässiger Werte für dieses Feld, die durch Semikolons getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="9a6a2-189">This is a list of permissible values for this field separated by semicolons.</span></span> <span data-ttu-id="9a6a2-190">Dieses Feld wird in der Regel für Enumerationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="9a6a2-190">This field is usually used for enumerations.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a2-191"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9a6a2-191"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="9a6a2-192">Eine Beschreibung der Daten, die in der Spalte gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="9a6a2-192">A description of the data that is stored in the column.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="9a6a2-193">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="9a6a2-193">Validation</span></span>

<dl>

[<span data-ttu-id="9a6a2-194">ICE03</span><span class="sxs-lookup"><span data-stu-id="9a6a2-194">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="9a6a2-195">ICE06</span><span class="sxs-lookup"><span data-stu-id="9a6a2-195">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="9a6a2-196">ICE32</span><span class="sxs-lookup"><span data-stu-id="9a6a2-196">ICE32</span></span>](ice32.md)  
</dl>

## <a name="remarks"></a><span data-ttu-id="9a6a2-197">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9a6a2-197">Remarks</span></span>

<span data-ttu-id="9a6a2-198">Das Kategoriefeld dieser Tabelle gilt nur für Zeichen folgen Daten.</span><span class="sxs-lookup"><span data-stu-id="9a6a2-198">The Category field of this table only applies to string data.</span></span> <span data-ttu-id="9a6a2-199">Wenn das Spalten Feld auf eine Spalte mit Binärdaten verweist, muss der binäre Datentyp im Feld "Category" angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9a6a2-199">If the Column field refers to a column with binary data, the binary data type must be specified in the Category field.</span></span> <span data-ttu-id="9a6a2-200">Ganzzahlige Datenspalten Typen ignorieren das Kategoriefeld während der Validierung.</span><span class="sxs-lookup"><span data-stu-id="9a6a2-200">Integer data Column types ignore the Category field during validation.</span></span>

 

 



