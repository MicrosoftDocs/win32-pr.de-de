---
description: Msiviewgetcolumninfo und die ColumnInfo-Eigenschaft des View-Objekts verwenden das folgende Format, um Daten Bank Spaltendefinitionen zu beschreiben.
ms.assetid: 77379664-26f2-4c1d-8c44-d9be2376efa9
title: Spalten Definitions Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e43e7f70c942fda32bf5003571fa687250e971d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216381"
---
# <a name="column-definition-format"></a><span data-ttu-id="c078f-103">Spalten Definitions Format</span><span class="sxs-lookup"><span data-stu-id="c078f-103">Column Definition Format</span></span>

<span data-ttu-id="c078f-104">[**Msiviewgetcolumninfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo) und die [**ColumnInfo-Eigenschaft**](view-columninfo.md) des [**View**](view-object.md) -Objekts verwenden das folgende Format, um Daten Bank Spaltendefinitionen zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="c078f-104">[**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo) and the [**ColumnInfo Property**](view-columninfo.md) of the [**View**](view-object.md) object use the following format to describe database column definitions.</span></span> <span data-ttu-id="c078f-105">Jede Spalte wird durch eine Zeichenfolge im entsprechenden Daten Satz Feld beschrieben, das von der Funktion oder der Eigenschaft zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c078f-105">Each column is described by a string in the corresponding record field returned by the function or property.</span></span> <span data-ttu-id="c078f-106">Die Definitions Zeichenfolge besteht aus einem einzelnen Buchstaben, der den Datentyp gefolgt von der Breite der Spalte darstellt (falls zutreffend, bytes, andernfalls).</span><span class="sxs-lookup"><span data-stu-id="c078f-106">The definition string consists of a single letter representing the data type followed by the width of the column (in characters when applicable, bytes otherwise).</span></span> <span data-ttu-id="c078f-107">Eine Breite von 0 (null) kennzeichnet eine unbegrenzte Breite (z. b. lange Textfelder und Streams).</span><span class="sxs-lookup"><span data-stu-id="c078f-107">A width of zero designates an unbounded width (for example, long text fields and streams).</span></span> <span data-ttu-id="c078f-108">Ein Großbuchstabe gibt an, dass NULL-Werte in der Spalte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="c078f-108">An uppercase letter indicates that null values are allowed in the column.</span></span>



| <span data-ttu-id="c078f-109">Spalten Deskriptor</span><span class="sxs-lookup"><span data-stu-id="c078f-109">Column descriptor</span></span> | <span data-ttu-id="c078f-110">Definitions Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c078f-110">Definition string</span></span>                 |
|-------------------|-----------------------------------|
| <span data-ttu-id="c078f-111">Hymnen?</span><span class="sxs-lookup"><span data-stu-id="c078f-111">s?</span></span>                | <span data-ttu-id="c078f-112">String, Variable Length (? = 1-255)</span><span class="sxs-lookup"><span data-stu-id="c078f-112">String, variable length (?=1-255)</span></span> |
| <span data-ttu-id="c078f-113">S0</span><span class="sxs-lookup"><span data-stu-id="c078f-113">s0</span></span>                | <span data-ttu-id="c078f-114">Zeichenfolge, Variable Länge</span><span class="sxs-lookup"><span data-stu-id="c078f-114">String, variable length</span></span>           |
| <span data-ttu-id="c078f-115">i2</span><span class="sxs-lookup"><span data-stu-id="c078f-115">i2</span></span>                | <span data-ttu-id="c078f-116">Kurze Ganzzahl</span><span class="sxs-lookup"><span data-stu-id="c078f-116">Short integer</span></span>                     |
| <span data-ttu-id="c078f-117">i4</span><span class="sxs-lookup"><span data-stu-id="c078f-117">i4</span></span>                | <span data-ttu-id="c078f-118">Lange ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="c078f-118">Long integer</span></span>                      |
| <span data-ttu-id="c078f-119">v0</span><span class="sxs-lookup"><span data-stu-id="c078f-119">v0</span></span>                | <span data-ttu-id="c078f-120">Binärer Stream</span><span class="sxs-lookup"><span data-stu-id="c078f-120">Binary Stream</span></span>                     |
| <span data-ttu-id="c078f-121">selbst?</span><span class="sxs-lookup"><span data-stu-id="c078f-121">g?</span></span>                | <span data-ttu-id="c078f-122">Temporäre Zeichenfolge (? = 0-255)</span><span class="sxs-lookup"><span data-stu-id="c078f-122">Temporary string (?=0-255)</span></span>        |
| <span data-ttu-id="c078f-123">IStGH?</span><span class="sxs-lookup"><span data-stu-id="c078f-123">j?</span></span>                | <span data-ttu-id="c078f-124">Temporäre Ganzzahl (? = 0, 1, 2, 4)</span><span class="sxs-lookup"><span data-stu-id="c078f-124">Temporary integer (?=0,1,2,4)</span></span>     |
| <span data-ttu-id="c078f-125">O0</span><span class="sxs-lookup"><span data-stu-id="c078f-125">O0</span></span>                | <span data-ttu-id="c078f-126">Temporäres Objekt</span><span class="sxs-lookup"><span data-stu-id="c078f-126">Temporary object</span></span>                  |



 

<span data-ttu-id="c078f-127">Die zum Beschreiben von Spalten verwendeten Zeichen folgen haben die folgende Beziehung zu den SQL-Abfrage Zeichenfolgen, die von CREATE und Alter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c078f-127">The strings used to describe columns have the following relationship to the SQL query strings used by CREATE and ALTER.</span></span> <span data-ttu-id="c078f-128">Weitere Informationen finden Sie unter [SQL-Syntax](sql-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="c078f-128">For more information, see [SQL Syntax](sql-syntax.md).</span></span>



| <span data-ttu-id="c078f-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c078f-129">Returned value</span></span> | <span data-ttu-id="c078f-130">SQL-Syntax</span><span class="sxs-lookup"><span data-stu-id="c078f-130">SQL syntax</span></span>                |
|----------------|---------------------------|
| <span data-ttu-id="c078f-131">S0</span><span class="sxs-lookup"><span data-stu-id="c078f-131">s0</span></span>             | <span data-ttu-id="c078f-132">LONGCHAR</span><span class="sxs-lookup"><span data-stu-id="c078f-132">LONGCHAR</span></span>                  |
| <span data-ttu-id="c078f-133">L0</span><span class="sxs-lookup"><span data-stu-id="c078f-133">l0</span></span>             | <span data-ttu-id="c078f-134">LONGCHAR lokalisierbar</span><span class="sxs-lookup"><span data-stu-id="c078f-134">LONGCHAR LOCALIZABLE</span></span>      |
| <span data-ttu-id="c078f-135">Hymnen \#</span><span class="sxs-lookup"><span data-stu-id="c078f-135">s \#</span></span>           | <span data-ttu-id="c078f-136">CHAR ( \# )</span><span class="sxs-lookup"><span data-stu-id="c078f-136">CHAR(\#)</span></span>                  |
| <span data-ttu-id="c078f-137">Hymnen \#</span><span class="sxs-lookup"><span data-stu-id="c078f-137">s \#</span></span>           | <span data-ttu-id="c078f-138">Zeichen ( \# )</span><span class="sxs-lookup"><span data-stu-id="c078f-138">CHARACTER(\#)</span></span>             |
| <span data-ttu-id="c078f-139">int \#</span><span class="sxs-lookup"><span data-stu-id="c078f-139">l \#</span></span>           | <span data-ttu-id="c078f-140">CHAR ( \# ) lokalisierbar</span><span class="sxs-lookup"><span data-stu-id="c078f-140">CHAR(\#) LOCALIZABLE</span></span>      |
| <span data-ttu-id="c078f-141">int \#</span><span class="sxs-lookup"><span data-stu-id="c078f-141">l \#</span></span>           | <span data-ttu-id="c078f-142">\#Lokalisier bares Zeichen ()</span><span class="sxs-lookup"><span data-stu-id="c078f-142">CHARACTER(\#) LOCALIZABLE</span></span> |
| <span data-ttu-id="c078f-143">i2</span><span class="sxs-lookup"><span data-stu-id="c078f-143">i2</span></span>             | <span data-ttu-id="c078f-144">SHORT</span><span class="sxs-lookup"><span data-stu-id="c078f-144">SHORT</span></span>                     |
| <span data-ttu-id="c078f-145">i2</span><span class="sxs-lookup"><span data-stu-id="c078f-145">i2</span></span>             | <span data-ttu-id="c078f-146">INT</span><span class="sxs-lookup"><span data-stu-id="c078f-146">INT</span></span>                       |
| <span data-ttu-id="c078f-147">i2</span><span class="sxs-lookup"><span data-stu-id="c078f-147">i2</span></span>             | <span data-ttu-id="c078f-148">INTEGER</span><span class="sxs-lookup"><span data-stu-id="c078f-148">INTEGER</span></span>                   |
| <span data-ttu-id="c078f-149">i4</span><span class="sxs-lookup"><span data-stu-id="c078f-149">i4</span></span>             | <span data-ttu-id="c078f-150">LONG</span><span class="sxs-lookup"><span data-stu-id="c078f-150">LONG</span></span>                      |
| <span data-ttu-id="c078f-151">v0</span><span class="sxs-lookup"><span data-stu-id="c078f-151">v0</span></span>             | <span data-ttu-id="c078f-152">OBJECT</span><span class="sxs-lookup"><span data-stu-id="c078f-152">OBJECT</span></span>                    |



 

<span data-ttu-id="c078f-153">Wenn der Buchstabe nicht groß geschrieben ist, muss die SQL-Anweisung mit Not Null angehängt werden.</span><span class="sxs-lookup"><span data-stu-id="c078f-153">If the letter is not capitalized, the SQL statement should be appended with NOT NULL.</span></span>



| <span data-ttu-id="c078f-154">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c078f-154">Returned value</span></span> | <span data-ttu-id="c078f-155">SQL-Syntax</span><span class="sxs-lookup"><span data-stu-id="c078f-155">SQL syntax</span></span>        |
|----------------|-------------------|
| <span data-ttu-id="c078f-156">S0</span><span class="sxs-lookup"><span data-stu-id="c078f-156">s0</span></span>             | <span data-ttu-id="c078f-157">LONGCHAR not NULL</span><span class="sxs-lookup"><span data-stu-id="c078f-157">LONGCHAR NOT NULL</span></span> |



 

<span data-ttu-id="c078f-158">Das Installationsprogramm schränkt die Spaltenlänge nicht intern auf den Wert ein, der im Spalten Definitions Format angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="c078f-158">The installer does not internally limit the length of columns to the value specified by the column definition format.</span></span> <span data-ttu-id="c078f-159">Wenn die in ein Feld eingegebenen Daten die angegebene Spaltenlänge überschreiten, kann das Paket die [Paket](package-validation.md)Überprüfung nicht durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="c078f-159">If the data entered into a field exceeds the specified column length, the package fails to pass [package validation](package-validation.md).</span></span> <span data-ttu-id="c078f-160">Um die Validierung in diesem Fall zu übergeben, müssen entweder die Daten oder das Datenbankschema geändert werden.</span><span class="sxs-lookup"><span data-stu-id="c078f-160">To pass validation in this case, either the data or the database schema must be changed.</span></span> <span data-ttu-id="c078f-161">Die einzige Möglichkeit zum Ändern der Spaltenlänge einer Standardtabelle besteht darin, die Tabelle mithilfe von " [**msidatabaseexport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)" zu exportieren, die exportierte IDT-Datei zu bearbeiten und dann die Tabelle mithilfe von " [**msidatabaseimport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)" zu importieren.</span><span class="sxs-lookup"><span data-stu-id="c078f-161">The only means to change the column length of a standard table is by exporting the table using [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta), editing the exported .idt file, and then importing the table using [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span></span> <span data-ttu-id="c078f-162">Autoren können die Spaltendatentypen, die NULL-Zulässigkeit oder die Lokalisierungs Attribute von Spalten in Standard Tabellen nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="c078f-162">Authors cannot change the column data types, nullability, or localization attributes of any columns in standard tables.</span></span> <span data-ttu-id="c078f-163">Autoren können benutzerdefinierte Tabellen mit Spalten Attributen erstellen, die Spalten Attribute aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c078f-163">Authors can create custom tables with columns having any column attributes.</span></span>

<span data-ttu-id="c078f-164">Wenn Sie [**msidatabasemerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) verwenden, um eine Verweis Datenbank in eine Zieldatenbank zusammenzuführen, müssen die Spaltennamen, die Anzahl der Primärschlüssel und die Spaltendatentypen identisch sein.</span><span class="sxs-lookup"><span data-stu-id="c078f-164">When using [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) to merge a reference database into a target database, the column names, number of primary keys, and column data types must match.</span></span> <span data-ttu-id="c078f-165">**Msidatabasemerge** ignoriert die Attribute für Lokalisierung und Spaltenlänge.</span><span class="sxs-lookup"><span data-stu-id="c078f-165">**MsiDatabaseMerge** ignores the localization and column length attributes.</span></span> <span data-ttu-id="c078f-166">Wenn eine Spalte in der Verweis Datenbank eine Länge von 0 (null) oder größer als die Länge der Spalte in der Zieldatenbank aufweist, erhöht **msidatabasemerge** die Spaltenlänge in der Zieldatenbank auf die Länge in der Verweis Datenbank.</span><span class="sxs-lookup"><span data-stu-id="c078f-166">If a column in the reference database has a length that is 0 or greater than the that column's length in the target database, **MsiDatabaseMerge** increases the column length in the target database to the length in the reference database.</span></span>

<span data-ttu-id="c078f-167">Wenn Sie Mergmod.dll Version 2,0 verwenden, ändert die Anwendung eines Mergemoduls zu einer MSI-Datei nie die Spaltenlänge oder die Spaltentypen einer vorhandenen Datenbanktabelle.</span><span class="sxs-lookup"><span data-stu-id="c078f-167">When using Mergmod.dll version 2.0, the application of a merge module to a .msi file never changes the length of columns or the column types of an existing database table.</span></span> <span data-ttu-id="c078f-168">Die Anwendung eines Mergemoduls kann jedoch das Schema einer vorhandenen Datenbanktabelle ändern, wenn das Modul einer Tabelle neue Spalten hinzufügt, für die es gültig ist, Spalten hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="c078f-168">The application of a merge module can however change the schema of an existing database table if the module adds new columns to a table for which it is valid to add columns.</span></span> <span data-ttu-id="c078f-169">Bei Verwendung einer Mergemod.dll Version, die kleiner als Version 2,0 ist, ändert die Anwendung eines Mergemoduls nie die Spaltenlänge und ändert niemals das Schema der Zieldatenbank.</span><span class="sxs-lookup"><span data-stu-id="c078f-169">When using a Mergemod.dll version less than version 2.0, the application of a merge module never changes the length of columns and never changes the schema of the target database.</span></span>

 

 



