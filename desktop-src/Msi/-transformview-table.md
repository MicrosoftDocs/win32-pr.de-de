---
description: Dies ist eine schreibgeschützte temporäre Tabelle, die zum Anzeigen von Transformationen mit dem Transformations Ansichtsmodus verwendet wird. Diese Tabelle wird nie vom Installationsprogramm persistent gespeichert.
ms.assetid: 4763ac0e-900f-45f1-bee5-34d413c5e401
title: _TransformView Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08cc513b1aae388d01cda178bfbefdc88874f6d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528883"
---
# <a name="_transformview-table"></a><span data-ttu-id="af4b3-104">\_Transformview-Tabelle</span><span class="sxs-lookup"><span data-stu-id="af4b3-104">\_TransformView Table</span></span>

<span data-ttu-id="af4b3-105">Dies ist eine schreibgeschützte temporäre Tabelle, die zum Anzeigen von Transformationen mit dem Transformations Ansichtsmodus verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="af4b3-105">This is a read-only temporary table used to view transforms with the transform view mode.</span></span> <span data-ttu-id="af4b3-106">Diese Tabelle wird nie vom Installationsprogramm persistent gespeichert.</span><span class="sxs-lookup"><span data-stu-id="af4b3-106">This table is never persisted by the installer.</span></span>

<span data-ttu-id="af4b3-107">Um den Transformations Ansichtsmodus aufzurufen, rufen Sie ein Handle ab, und öffnen Sie die Verweis Datenbank.</span><span class="sxs-lookup"><span data-stu-id="af4b3-107">To invoke the transform view mode, obtain a handle and open the reference database.</span></span> <span data-ttu-id="af4b3-108">Siehe Abrufen [eines Daten Bank Handles](obtaining-a-database-handle.md).</span><span class="sxs-lookup"><span data-stu-id="af4b3-108">See [Obtaining a Database Handle](obtaining-a-database-handle.md).</span></span> <span data-ttu-id="af4b3-109">[**Msidatabaseapplytransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) mit msitransform- \_ Fehler \_ viewtransform abrufen.</span><span class="sxs-lookup"><span data-stu-id="af4b3-109">Call [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) with MSITRANSFORM\_ERROR\_VIEWTRANSFORM.</span></span> <span data-ttu-id="af4b3-110">Dadurch wird verhindert, dass die Transformation auf die Datenbank angewendet wird, und der Transformations Inhalt wird in die \_ transformview-Tabelle integriert.</span><span class="sxs-lookup"><span data-stu-id="af4b3-110">This stops the transform from being applied to the database and dumps the transform contents into the \_TransformView table.</span></span> <span data-ttu-id="af4b3-111">Auf die Daten in der Tabelle kann mithilfe von SQL-Abfragen zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="af4b3-111">The data in the table can be accessed using SQL queries.</span></span> <span data-ttu-id="af4b3-112">Siehe [Arbeiten mit Abfragen](working-with-queries.md).</span><span class="sxs-lookup"><span data-stu-id="af4b3-112">See [Working with Queries](working-with-queries.md).</span></span>

<span data-ttu-id="af4b3-113">Die \_ transformview-Tabelle wird nicht gelöscht, wenn eine andere Transformation angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="af4b3-113">The \_TransformView table is not cleared when another transform is applied.</span></span> <span data-ttu-id="af4b3-114">Die Tabelle spiegelt die kumulative Auswirkung aufeinander folgender Anwendungen wider.</span><span class="sxs-lookup"><span data-stu-id="af4b3-114">The table reflects the cumulative effect of successive applications.</span></span> <span data-ttu-id="af4b3-115">Um die Transformationen separat anzuzeigen, müssen Sie die Tabelle freigeben.</span><span class="sxs-lookup"><span data-stu-id="af4b3-115">To view the transforms separately you must release the table.</span></span>

<span data-ttu-id="af4b3-116">Die \_ transformview-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="af4b3-116">The \_TransformView Table has the following columns.</span></span>



| <span data-ttu-id="af4b3-117">Spalte</span><span class="sxs-lookup"><span data-stu-id="af4b3-117">Column</span></span>  | <span data-ttu-id="af4b3-118">Typ</span><span class="sxs-lookup"><span data-stu-id="af4b3-118">Type</span></span>                         | <span data-ttu-id="af4b3-119">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="af4b3-119">Key</span></span> | <span data-ttu-id="af4b3-120">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="af4b3-120">Nullable</span></span> |
|---------|------------------------------|-----|----------|
| <span data-ttu-id="af4b3-121">Tabelle</span><span class="sxs-lookup"><span data-stu-id="af4b3-121">Table</span></span>   | [<span data-ttu-id="af4b3-122">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="af4b3-122">Identifier</span></span>](identifier.md) | <span data-ttu-id="af4b3-123">J</span><span class="sxs-lookup"><span data-stu-id="af4b3-123">Y</span></span>   | <span data-ttu-id="af4b3-124">N</span><span class="sxs-lookup"><span data-stu-id="af4b3-124">N</span></span>        |
| <span data-ttu-id="af4b3-125">Column</span><span class="sxs-lookup"><span data-stu-id="af4b3-125">Column</span></span>  | [<span data-ttu-id="af4b3-126">Text</span><span class="sxs-lookup"><span data-stu-id="af4b3-126">Text</span></span>](text.md)             | <span data-ttu-id="af4b3-127">J</span><span class="sxs-lookup"><span data-stu-id="af4b3-127">Y</span></span>   | <span data-ttu-id="af4b3-128">N</span><span class="sxs-lookup"><span data-stu-id="af4b3-128">N</span></span>        |
| <span data-ttu-id="af4b3-129">Zeile</span><span class="sxs-lookup"><span data-stu-id="af4b3-129">Row</span></span>     | [<span data-ttu-id="af4b3-130">Text</span><span class="sxs-lookup"><span data-stu-id="af4b3-130">Text</span></span>](text.md)             | <span data-ttu-id="af4b3-131">J</span><span class="sxs-lookup"><span data-stu-id="af4b3-131">Y</span></span>   | <span data-ttu-id="af4b3-132">J</span><span class="sxs-lookup"><span data-stu-id="af4b3-132">Y</span></span>        |
| <span data-ttu-id="af4b3-133">Daten</span><span class="sxs-lookup"><span data-stu-id="af4b3-133">Data</span></span>    | [<span data-ttu-id="af4b3-134">Text</span><span class="sxs-lookup"><span data-stu-id="af4b3-134">Text</span></span>](text.md)             | <span data-ttu-id="af4b3-135">N</span><span class="sxs-lookup"><span data-stu-id="af4b3-135">N</span></span>   | <span data-ttu-id="af4b3-136">J</span><span class="sxs-lookup"><span data-stu-id="af4b3-136">Y</span></span>        |
| <span data-ttu-id="af4b3-137">Aktuell</span><span class="sxs-lookup"><span data-stu-id="af4b3-137">Current</span></span> | [<span data-ttu-id="af4b3-138">Text</span><span class="sxs-lookup"><span data-stu-id="af4b3-138">Text</span></span>](text.md)             | <span data-ttu-id="af4b3-139">N</span><span class="sxs-lookup"><span data-stu-id="af4b3-139">N</span></span>   | <span data-ttu-id="af4b3-140">J</span><span class="sxs-lookup"><span data-stu-id="af4b3-140">Y</span></span>        |



 

## <a name="column"></a><span data-ttu-id="af4b3-141">Column</span><span class="sxs-lookup"><span data-stu-id="af4b3-141">Column</span></span>

<dl> <dt>

<span data-ttu-id="af4b3-142"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Glaub</span><span class="sxs-lookup"><span data-stu-id="af4b3-142"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="af4b3-143">Der Name einer geänderten Datenbanktabelle.</span><span class="sxs-lookup"><span data-stu-id="af4b3-143">Name of an altered database table.</span></span>

</dd> <dt>

<span data-ttu-id="af4b3-144"><span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Kolumne</span><span class="sxs-lookup"><span data-stu-id="af4b3-144"><span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Column</span></span>
</dt> <dd>

<span data-ttu-id="af4b3-145">Der Name einer geänderten Tabellenspalte oder INSERT, DELETE, CREATE oder Drop.</span><span class="sxs-lookup"><span data-stu-id="af4b3-145">Name of an altered table column or INSERT, DELETE, CREATE, or DROP.</span></span>

</dd> <dt>

<span data-ttu-id="af4b3-146"><span id="Row"></span><span id="row"></span><span id="ROW"></span>Zeile</span><span class="sxs-lookup"><span data-stu-id="af4b3-146"><span id="Row"></span><span id="row"></span><span id="ROW"></span>Row</span></span>
</dt> <dd>

<span data-ttu-id="af4b3-147">Eine Liste der Primärschlüssel Werte, die durch Registerkarten getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="af4b3-147">A list of the primary key values separated by tabs.</span></span> <span data-ttu-id="af4b3-148">NULL-Primärschlüssel Werte werden durch ein einzelnes Leerzeichen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="af4b3-148">Null primary key values are represented by a single space character.</span></span> <span data-ttu-id="af4b3-149">Ein NULL-Wert in dieser Spalte gibt eine Schema Änderung an.</span><span class="sxs-lookup"><span data-stu-id="af4b3-149">A Null value in this column indicates a schema change.</span></span>

</dd> <dt>

<span data-ttu-id="af4b3-150"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Vorrats</span><span class="sxs-lookup"><span data-stu-id="af4b3-150"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span></span>
</dt> <dd>

<span data-ttu-id="af4b3-151">Daten, Name eines Datenstroms oder Spaltendefinition.</span><span class="sxs-lookup"><span data-stu-id="af4b3-151">Data, name of a data stream, or a column definition.</span></span>

</dd> <dt>

<span data-ttu-id="af4b3-152"><span id="Current"></span><span id="current"></span><span id="CURRENT"></span>Strömung</span><span class="sxs-lookup"><span data-stu-id="af4b3-152"><span id="Current"></span><span id="current"></span><span id="CURRENT"></span>Current</span></span>
</dt> <dd>

<span data-ttu-id="af4b3-153">Aktueller Wert aus Verweis Datenbank oder Spalte a-Nummer.</span><span class="sxs-lookup"><span data-stu-id="af4b3-153">Current value from reference database, or column a number.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="af4b3-154">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="af4b3-154">Remarks</span></span>

<span data-ttu-id="af4b3-155">Die \_ transformview wird durch eine Sperr Anzahl im Arbeitsspeicher gespeichert, die mit dem folgenden SQL-Befehl freigegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="af4b3-155">The \_TransformView is held in memory by a lock count, that can be released with the following SQL command.</span></span>

<span data-ttu-id="af4b3-156">"Alter Table \_ transformview Free".</span><span class="sxs-lookup"><span data-stu-id="af4b3-156">"ALTER TABLE \_TransformView FREE".</span></span>

<span data-ttu-id="af4b3-157">Auf die Daten in der Tabelle kann mithilfe von SQL-Abfragen zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="af4b3-157">The data in the table can be accessed using SQL queries.</span></span> <span data-ttu-id="af4b3-158">Die SQL-Sprache verfügt über zwei Hauptbereiche: Datendefinitionssprache (Data Definition Language, DDL), die zum Definieren aller Objekte in einer SQL-Datenbank verwendet wird, und DML (Data Manipulation Language), die zum auswählen, einfügen, aktualisieren und Löschen von Daten in den Objekten verwendet werden, die mithilfe von DDL definiert wurden.</span><span class="sxs-lookup"><span data-stu-id="af4b3-158">The SQL language has two main divisions: Data Definition Language (DDL) that is used to define all the objects in an SQL database, and Data Manipulation Language (DML) that is used to select, insert, update, and delete data in the objects defined using DDL.</span></span>

<span data-ttu-id="af4b3-159">Die Transformations Vorgänge der Daten Bearbeitungs Sprache (DML) werden wie folgt angegeben.</span><span class="sxs-lookup"><span data-stu-id="af4b3-159">The Data Manipulation Language (DML) transform operations are indicated as follows.</span></span> <span data-ttu-id="af4b3-160">DML (Data Manipulation Language) sind die Anweisungen in SQL, die im Gegensatz zum Definieren von Daten bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="af4b3-160">Data Manipulation Language (DML) are those statements in SQL that manipulate, as opposed to define, data.</span></span>



| <span data-ttu-id="af4b3-161">Transformations Vorgang</span><span class="sxs-lookup"><span data-stu-id="af4b3-161">Transform operation</span></span> | <span data-ttu-id="af4b3-162">SQL-Ergebnis</span><span class="sxs-lookup"><span data-stu-id="af4b3-162">SQL result</span></span>                                    |
|---------------------|-----------------------------------------------|
| <span data-ttu-id="af4b3-163">Ändern von Daten</span><span class="sxs-lookup"><span data-stu-id="af4b3-163">Modify data</span></span>         | <span data-ttu-id="af4b3-164">glaub Kolumne Zeile Vorrats {Aktueller Wert}</span><span class="sxs-lookup"><span data-stu-id="af4b3-164">{table} {column} {row} {data} {current value}</span></span> |
| <span data-ttu-id="af4b3-165">Zeile einfügen</span><span class="sxs-lookup"><span data-stu-id="af4b3-165">Insert row</span></span>          | <span data-ttu-id="af4b3-166">glaub "Insert" {Row} NULL NULL</span><span class="sxs-lookup"><span data-stu-id="af4b3-166">{table} "INSERT" {row} NULL NULL</span></span>              |
| <span data-ttu-id="af4b3-167">Zeile löschen</span><span class="sxs-lookup"><span data-stu-id="af4b3-167">Delete row</span></span>          | <span data-ttu-id="af4b3-168">glaub "Delete" {Row} NULL NULL</span><span class="sxs-lookup"><span data-stu-id="af4b3-168">{table} "DELETE" {row} NULL NULL</span></span>              |



 

<span data-ttu-id="af4b3-169">Die DDL-Transformations Vorgänge (Data Definition Language, Datendefinitionssprache) werden wie folgt angegeben.</span><span class="sxs-lookup"><span data-stu-id="af4b3-169">The Data Definition Language (DDL) transform operations are indicated as follows.</span></span> <span data-ttu-id="af4b3-170">DDL (Data Definition Language) sind die Anweisungen in SQL, die definieren, dass Daten nicht bearbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="af4b3-170">Data Definition Language (DDL) are those statements in SQL that define, as opposed to manipulate, data.</span></span>



| <span data-ttu-id="af4b3-171">Transformations Vorgang</span><span class="sxs-lookup"><span data-stu-id="af4b3-171">Transform operation</span></span> | <span data-ttu-id="af4b3-172">SQL-Ergebnis</span><span class="sxs-lookup"><span data-stu-id="af4b3-172">SQL result</span></span>                                   |
|---------------------|----------------------------------------------|
| <span data-ttu-id="af4b3-173">Hinzufügen einer Spalte</span><span class="sxs-lookup"><span data-stu-id="af4b3-173">Add column</span></span>          | <span data-ttu-id="af4b3-174">glaub Kolumne NULL {DEFN} {Spaltennummer}</span><span class="sxs-lookup"><span data-stu-id="af4b3-174">{table} {column} NULL {defn} {column number}</span></span> |
| <span data-ttu-id="af4b3-175">Tabelle hinzufügen</span><span class="sxs-lookup"><span data-stu-id="af4b3-175">Add table</span></span>           | <span data-ttu-id="af4b3-176">glaub "Create" Null Null Null</span><span class="sxs-lookup"><span data-stu-id="af4b3-176">{table} "CREATE" NULL NULL NULL</span></span>              |
| <span data-ttu-id="af4b3-177">Löschen einer Tabelle</span><span class="sxs-lookup"><span data-stu-id="af4b3-177">Drop table</span></span>          | <span data-ttu-id="af4b3-178">glaub "Drop" Null Null Null</span><span class="sxs-lookup"><span data-stu-id="af4b3-178">{table} "DROP" NULL NULL NULL</span></span>                |



 

<span data-ttu-id="af4b3-179">Wenn die Anwendung einer Transformation diese Tabelle hinzufügt, empfängt das Datenfeld Text, der als 16-Bit-Ganzzahl interpretiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="af4b3-179">When the application of a transform adds this table, the Data field receives text that can be interpreted as a 16-bit integer value.</span></span> <span data-ttu-id="af4b3-180">Der Wert beschreibt die Spalte mit dem Namen im Feld Spalte.</span><span class="sxs-lookup"><span data-stu-id="af4b3-180">The value describes the column named in the Column field.</span></span> <span data-ttu-id="af4b3-181">Sie können den ganzzahligen Wert mit den Konstanten in der folgenden Tabelle vergleichen, um die Definition der geänderten Spalte zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="af4b3-181">You can compare the integer value to the constants in the following table to determine the definition of the altered column.</span></span>



| <span data-ttu-id="af4b3-182">bit</span><span class="sxs-lookup"><span data-stu-id="af4b3-182">Bit</span></span>                                                                                                       | <span data-ttu-id="af4b3-183">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="af4b3-183">Description</span></span>                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af4b3-184"><span id="Bits_07"></span><span id="bits_07"></span><span id="BITS_07"></span>Bits 0 7</span><span class="sxs-lookup"><span data-stu-id="af4b3-184"><span id="Bits_07"></span><span id="bits_07"></span><span id="BITS_07"></span>Bits 0 7</span></span><br/>         | <span data-ttu-id="af4b3-185">Hexadezimalwert: 0x0000 0x0100</span><span class="sxs-lookup"><span data-stu-id="af4b3-185">Hexadecimal: 0x0000 0x0100</span></span><br/> <span data-ttu-id="af4b3-186">Dezimalzahl: 0 255</span><span class="sxs-lookup"><span data-stu-id="af4b3-186">Decimal: 0 255</span></span><br/> <span data-ttu-id="af4b3-187">Spaltenbreite</span><span class="sxs-lookup"><span data-stu-id="af4b3-187">Column width</span></span><br/>                                                                                                                                                                                                                                  |
| <span data-ttu-id="af4b3-188"><span id="Bit_8"></span><span id="bit_8"></span><span id="BIT_8"></span>Bit 8</span><span class="sxs-lookup"><span data-stu-id="af4b3-188"><span id="Bit_8"></span><span id="bit_8"></span><span id="BIT_8"></span>Bit 8</span></span><br/>                  | <span data-ttu-id="af4b3-189">Hexadezimalwert: 0x0100</span><span class="sxs-lookup"><span data-stu-id="af4b3-189">Hexadecimal: 0x0100</span></span><br/> <span data-ttu-id="af4b3-190">Dezimalzahl: 256</span><span class="sxs-lookup"><span data-stu-id="af4b3-190">Decimal: 256</span></span><br/> <span data-ttu-id="af4b3-191">Eine persistente Spalte.</span><span class="sxs-lookup"><span data-stu-id="af4b3-191">A persistent column.</span></span> <span data-ttu-id="af4b3-192">NULL bedeutet eine temporäre Spalte.</span><span class="sxs-lookup"><span data-stu-id="af4b3-192">Zero means a temporary column.</span></span> <br/>                                                                                                                                                                                                   |
| <span data-ttu-id="af4b3-193"><span id="Bit_9"></span><span id="bit_9"></span><span id="BIT_9"></span>Bit 9</span><span class="sxs-lookup"><span data-stu-id="af4b3-193"><span id="Bit_9"></span><span id="bit_9"></span><span id="BIT_9"></span>Bit 9</span></span><br/>                  | <span data-ttu-id="af4b3-194">Hexadezimalwert: 0x0200</span><span class="sxs-lookup"><span data-stu-id="af4b3-194">Hexadecimal: 0x0200</span></span><br/> <span data-ttu-id="af4b3-195">Dezimalzahl: 1023</span><span class="sxs-lookup"><span data-stu-id="af4b3-195">Decimal: 1023</span></span><br/> <span data-ttu-id="af4b3-196">Eine lokalisierbare Spalte.</span><span class="sxs-lookup"><span data-stu-id="af4b3-196">A localizable column.</span></span> <span data-ttu-id="af4b3-197">NULL bedeutet, dass die Spalte nicht lokalisiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="af4b3-197">Zero means the column cannot be localized.</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="af4b3-198"><span id="Bits_1011"></span><span id="bits_1011"></span><span id="BITS_1011"></span>Bits 10 11</span><span class="sxs-lookup"><span data-stu-id="af4b3-198"><span id="Bits_1011"></span><span id="bits_1011"></span><span id="BITS_1011"></span>Bits 10 11</span></span><br/> | <span data-ttu-id="af4b3-199">Hexadezimalwert: 0x0000</span><span class="sxs-lookup"><span data-stu-id="af4b3-199">Hexadecimal: 0x0000</span></span><br/> <span data-ttu-id="af4b3-200">Dezimalwert: 0</span><span class="sxs-lookup"><span data-stu-id="af4b3-200">Decimal: 0</span></span><br/> <span data-ttu-id="af4b3-201">Lange ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="af4b3-201">Long integer</span></span><br/> <span data-ttu-id="af4b3-202">Hexadezimalwert: 0x0400</span><span class="sxs-lookup"><span data-stu-id="af4b3-202">Hexadecimal: 0x0400</span></span><br/> <span data-ttu-id="af4b3-203">Dezimalzahl: 1024</span><span class="sxs-lookup"><span data-stu-id="af4b3-203">Decimal: 1024</span></span><br/> <span data-ttu-id="af4b3-204">Kurze Ganzzahl</span><span class="sxs-lookup"><span data-stu-id="af4b3-204">Short integer</span></span><br/> <span data-ttu-id="af4b3-205">Hexadezimalwert: 0x0800</span><span class="sxs-lookup"><span data-stu-id="af4b3-205">Hexadecimal: 0x0800</span></span><br/> <span data-ttu-id="af4b3-206">Dezimalzahl: 2048</span><span class="sxs-lookup"><span data-stu-id="af4b3-206">Decimal: 2048</span></span><br/> <span data-ttu-id="af4b3-207">Binary-Objekt</span><span class="sxs-lookup"><span data-stu-id="af4b3-207">Binary object</span></span><br/> <span data-ttu-id="af4b3-208">Hexadezimal: 0x0c00</span><span class="sxs-lookup"><span data-stu-id="af4b3-208">Hexadecimal: 0x0C00</span></span><br/> <span data-ttu-id="af4b3-209">Dezimalzahl: 3072</span><span class="sxs-lookup"><span data-stu-id="af4b3-209">Decimal: 3072</span></span><br/> <span data-ttu-id="af4b3-210">String</span><span class="sxs-lookup"><span data-stu-id="af4b3-210">String</span></span><br/> |
| <span data-ttu-id="af4b3-211"><span id="Bit_12"></span><span id="bit_12"></span><span id="BIT_12"></span>Bit 12</span><span class="sxs-lookup"><span data-stu-id="af4b3-211"><span id="Bit_12"></span><span id="bit_12"></span><span id="BIT_12"></span>Bit 12</span></span><br/>              | <span data-ttu-id="af4b3-212">Hexadezimalwert: 0x1000</span><span class="sxs-lookup"><span data-stu-id="af4b3-212">Hexadecimal: 0x1000</span></span><br/> <span data-ttu-id="af4b3-213">Dezimalzahl: 4096</span><span class="sxs-lookup"><span data-stu-id="af4b3-213">Decimal: 4096</span></span><br/> <span data-ttu-id="af4b3-214">Nullable-Spalte.</span><span class="sxs-lookup"><span data-stu-id="af4b3-214">Nullable column.</span></span> <span data-ttu-id="af4b3-215">NULL bedeutet, dass die Spalte keine NULL-Werte zulässt.</span><span class="sxs-lookup"><span data-stu-id="af4b3-215">Zero means the column is non-nullable.</span></span><br/>                                                                                                                                                                                               |
| <span data-ttu-id="af4b3-216"><span id="Bit_13"></span><span id="bit_13"></span><span id="BIT_13"></span>Bit 13</span><span class="sxs-lookup"><span data-stu-id="af4b3-216"><span id="Bit_13"></span><span id="bit_13"></span><span id="BIT_13"></span>Bit 13</span></span><br/>              | <span data-ttu-id="af4b3-217">Hexadezimalwert: 0x2000</span><span class="sxs-lookup"><span data-stu-id="af4b3-217">Hexadecimal: 0x2000</span></span><br/> <span data-ttu-id="af4b3-218">Dezimalzahl: 8192</span><span class="sxs-lookup"><span data-stu-id="af4b3-218">Decimal: 8192</span></span><br/> <span data-ttu-id="af4b3-219">Primärschlüssel Spalte.</span><span class="sxs-lookup"><span data-stu-id="af4b3-219">Primary key column.</span></span> <span data-ttu-id="af4b3-220">NULL bedeutet, dass diese Spalte kein Primärschlüssel ist.</span><span class="sxs-lookup"><span data-stu-id="af4b3-220">Zero means this column is not a primary key.</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="af4b3-221"><span id="Bits_1415"></span><span id="bits_1415"></span><span id="BITS_1415"></span>Bits 14 15</span><span class="sxs-lookup"><span data-stu-id="af4b3-221"><span id="Bits_1415"></span><span id="bits_1415"></span><span id="BITS_1415"></span>Bits 14 15</span></span><br/> | <span data-ttu-id="af4b3-222">Hexadezimalwert: 0x4000 0X8000</span><span class="sxs-lookup"><span data-stu-id="af4b3-222">Hexadecimal: 0x4000 0x8000</span></span><br/> <span data-ttu-id="af4b3-223">Dezimalzahl: 16384 32768</span><span class="sxs-lookup"><span data-stu-id="af4b3-223">Decimal: 16384 32768</span></span><br/> <span data-ttu-id="af4b3-224">Reserviert</span><span class="sxs-lookup"><span data-stu-id="af4b3-224">Reserved</span></span><br/>                                                                                                                                                                                                                                |



 

<span data-ttu-id="af4b3-225">Ein Skript Beispiel, in dem die \_ transformview-Tabelle veranschaulicht wird, finden Sie unter [View a Transform](view-a-transform.md).</span><span class="sxs-lookup"><span data-stu-id="af4b3-225">For a script sample that demonstrates the \_TransformView table, see [View a Transform](view-a-transform.md).</span></span>

 

 




