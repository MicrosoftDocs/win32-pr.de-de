---
description: Eine Textarchiv Datei für eine Windows Installer Datenbank enthält die Dateinamenerweiterung. IDT.
ms.assetid: 91d81fb2-3a41-477a-85c2-e68bfe482b9c
title: Archivdatei Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaf39383b961c305bf621793784332342f369a30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864471"
---
# <a name="archive-file-format"></a><span data-ttu-id="93a87-103">Archivdatei Format</span><span class="sxs-lookup"><span data-stu-id="93a87-103">Archive File Format</span></span>

<span data-ttu-id="93a87-104">Eine [Textarchiv Datei](text-archive-files.md) für eine Windows Installer Datenbank enthält die Dateinamenerweiterung. IDT.</span><span class="sxs-lookup"><span data-stu-id="93a87-104">A [text archive file](text-archive-files.md) for a Windows Installer database carries an .idt file name extension.</span></span> <span data-ttu-id="93a87-105">Wenn eine gesamte Datenbank in Archivdateien exportiert wird, verfügt jede Tabelle in der Datenbank über eine separate IDT-Datei.</span><span class="sxs-lookup"><span data-stu-id="93a87-105">When an entire database is exported to archive files, each table in the database has a separate .idt file.</span></span> <span data-ttu-id="93a87-106">Wenn eine Tabelle eine Datenstrom Spalte enthält, wird jeder Stream in der Tabelle durch eine Datei mit der Dateinamenerweiterung ". ibd" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="93a87-106">If a table contains a stream column, each stream in the table is represented by a file with an .ibd file name extension.</span></span> <span data-ttu-id="93a87-107">Die ibd-Dateien werden in einem Ordner mit dem gleichen Namen wie die Tabelle gespeichert.</span><span class="sxs-lookup"><span data-stu-id="93a87-107">The .ibd files are stored in a folder with the same name as the table.</span></span>

## <a name="idt-file-format"></a><span data-ttu-id="93a87-108">IDT-Datei Format</span><span class="sxs-lookup"><span data-stu-id="93a87-108">.idt File Format</span></span>

<span data-ttu-id="93a87-109">Die IDT-Datei einer exportierten Datenbanktabelle, die nur ASCII-Zeichen enthält, weist das folgende grundlegende Format auf.</span><span class="sxs-lookup"><span data-stu-id="93a87-109">The .idt file of an exported database table that contains only ASCII characters has the following basic format.</span></span>

-   <span data-ttu-id="93a87-110">Die erste Zeile enthält die Namen der Tabellen Spalten, die durch Registerkarten getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="93a87-110">The first row contains the table column names separated by tabs.</span></span>
-   <span data-ttu-id="93a87-111">Die zweite Zeile enthält die Spaltendefinitionen, die durch Registerkarten getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="93a87-111">The second row contains the column definitions separated by tabs.</span></span>
-   <span data-ttu-id="93a87-112">Wenn die Datei nur ASCII-Daten enthält, ist die dritte Zeile Tabellenname und Primärschlüssel Spaltennamen durch Registerkarten getrennt.</span><span class="sxs-lookup"><span data-stu-id="93a87-112">If the file contain only ASCII data, the third row is table name and primary key column names separated by tabs.</span></span>
-   <span data-ttu-id="93a87-113">Die verbleibenden Zeilen in der Datei stellen Zeilen in der Tabelle dar, wobei die Spalten durch Registerkarten getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="93a87-113">The remaining rows in the file represent rows in the table, with columns separated by tabs.</span></span>

> [!Note]  
> <span data-ttu-id="93a87-114">Wenn die Datei nicht-ASCII-Daten enthält, ist die dritte Zeile die numerische Codepage, gefolgt von den Namen der Tabellennamen und der Primärschlüssel Spalten, die durch Registerkarten getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="93a87-114">If the file contains non-ASCII data, the third row is the numeric code page followed by the table name and primary key column names separated by tabs.</span></span> <span data-ttu-id="93a87-115">Eine IDT-Datei, die nicht-ASCII-Informationen enthält, muss im ASCII-Format gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="93a87-115">An .idt file that contains non-ASCII information should be saved in the ASCII format.</span></span> <span data-ttu-id="93a87-116">Eine Textarchiv Datei kann z. b. die Spalten-und Tabellennamen enthalten, die als UTF-8 codiert sind, aber die Archivdatei selbst muss ASCII sein.</span><span class="sxs-lookup"><span data-stu-id="93a87-116">For example, a text archive file can contain the column and table names encoded as UTF-8, but the archive file itself should be ASCII.</span></span> <span data-ttu-id="93a87-117">Weitere Informationen finden Sie [im Abschnitt ASCII-Daten in Text Archivdateien](ascii-data-in-text-archive-files.md).</span><span class="sxs-lookup"><span data-stu-id="93a87-117">See the section [ASCII Data in Text Archive Files](ascii-data-in-text-archive-files.md).</span></span>

 

> [!Note]  
> <span data-ttu-id="93a87-118">In den speziellen [ \_ forcecodepage](-forcecodepage.md) -und [ \_ SummaryInformation](-summaryinformation.md) . IDT-Dateien werden erweiterte Formate verwendet.</span><span class="sxs-lookup"><span data-stu-id="93a87-118">The special [\_ForceCodepage](-forcecodepage.md) and [\_SummaryInformation](-summaryinformation.md) .idt files use extended formats.</span></span> <span data-ttu-id="93a87-119">\_Beschreibungen ihrer Formate finden Sie in den Abschnitten "forcecodepage" und " \_ SummaryInformation".</span><span class="sxs-lookup"><span data-stu-id="93a87-119">See the \_ForceCodepage and \_SummaryInformation sections for descriptions of their formats.</span></span>

 

## <a name="column-definitions"></a><span data-ttu-id="93a87-120">Spaltendefinitionen</span><span class="sxs-lookup"><span data-stu-id="93a87-120">Column Definitions</span></span>

<span data-ttu-id="93a87-121">Spaltendefinitionen werden durch Zeichen angegeben.</span><span class="sxs-lookup"><span data-stu-id="93a87-121">Column definitions are indicated by characters.</span></span>

-   <span data-ttu-id="93a87-122">Das erste Zeichen gibt den Spaltentyp an.</span><span class="sxs-lookup"><span data-stu-id="93a87-122">The first character indicates the column type.</span></span> <span data-ttu-id="93a87-123">Ein Kleinbuchstabe gibt eine Spalte an, die keine NULL-Werte zulässt, und ein Großbuchstabe gibt an, dass die Spalte NULL-Werte enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="93a87-123">A lowercase letter indicates a non-nullable column and an uppercase letter indicates that the column can contain null values.</span></span>

    | <span data-ttu-id="93a87-124">Zeichen</span><span class="sxs-lookup"><span data-stu-id="93a87-124">Character</span></span> | <span data-ttu-id="93a87-125">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="93a87-125">Meaning</span></span>                   |
    |-----------|---------------------------|
    | <span data-ttu-id="93a87-126">s, s</span><span class="sxs-lookup"><span data-stu-id="93a87-126">s, S</span></span>      | <span data-ttu-id="93a87-127">Zeichen folgen Spalte</span><span class="sxs-lookup"><span data-stu-id="93a87-127">String Column</span></span>             |
    | <span data-ttu-id="93a87-128">l, l</span><span class="sxs-lookup"><span data-stu-id="93a87-128">l, L</span></span>      | <span data-ttu-id="93a87-129">Lokalisierbare Zeichen folgen Spalte</span><span class="sxs-lookup"><span data-stu-id="93a87-129">Localizable String Column</span></span> |
    | <span data-ttu-id="93a87-130">v, v</span><span class="sxs-lookup"><span data-stu-id="93a87-130">v, V</span></span>      | <span data-ttu-id="93a87-131">Binäre Spalte</span><span class="sxs-lookup"><span data-stu-id="93a87-131">Binary Column</span></span>             |
    | <span data-ttu-id="93a87-132">i, i</span><span class="sxs-lookup"><span data-stu-id="93a87-132">i, I</span></span>      | <span data-ttu-id="93a87-133">Ganzzahlige Spalte</span><span class="sxs-lookup"><span data-stu-id="93a87-133">Integer Column</span></span>            |

    

     

-   <span data-ttu-id="93a87-134">Das zweite Zeichen gibt die Größe der Spaltendaten an.</span><span class="sxs-lookup"><span data-stu-id="93a87-134">The second character indicates the column data size.</span></span>

    > [!Note]  
    > <span data-ttu-id="93a87-135">Der Windows Installer verwendet die angegebene Spaltengröße nicht, um die Größe der Zeichenfolge zu begrenzen, die in ein Zeichen folgen Spalten Feld eingegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="93a87-135">The Windows Installer does not actually use the specified column size to limit the size of the string that can be entered into a string column field.</span></span> <span data-ttu-id="93a87-136">Einige Erstellungs Tools verwenden jedoch die angegebene Spaltengröße, um die Größe einer gültigen Zeichenfolge einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="93a87-136">However, some authoring tools do use the specified column size to limit the size of a valid string.</span></span> <span data-ttu-id="93a87-137">Es wird empfohlen, dass Zeichen folgen, die in eine Spalte eingegeben werden, die angegebene Größen Anforderung erfüllen.</span><span class="sxs-lookup"><span data-stu-id="93a87-137">It is recommended that strings entered into any column meet the specified size requirement.</span></span>

     

    

    | <span data-ttu-id="93a87-138">Spalten Definition</span><span class="sxs-lookup"><span data-stu-id="93a87-138">Column Definition</span></span> | <span data-ttu-id="93a87-139">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="93a87-139">Meaning</span></span>                                    |
    |-------------------|--------------------------------------------|
    | <span data-ttu-id="93a87-140">s255</span><span class="sxs-lookup"><span data-stu-id="93a87-140">s255</span></span>              | <span data-ttu-id="93a87-141">Zeichen folgen Spalte 255 Long, die keine NULL-Werte zulässt</span><span class="sxs-lookup"><span data-stu-id="93a87-141">Non-Nullable String Column 255 long</span></span>        |
    | <span data-ttu-id="93a87-142">L50</span><span class="sxs-lookup"><span data-stu-id="93a87-142">L50</span></span>               | <span data-ttu-id="93a87-143">In der lokalisierbare Zeichen folgen Spalte 50 Long</span><span class="sxs-lookup"><span data-stu-id="93a87-143">Nullable Localizable String Column 50 long</span></span> |
    | <span data-ttu-id="93a87-144">I2, I2</span><span class="sxs-lookup"><span data-stu-id="93a87-144">i2, I2</span></span>            | <span data-ttu-id="93a87-145">Kurze ganzzahlige Spalte</span><span class="sxs-lookup"><span data-stu-id="93a87-145">Short Integer Column</span></span>                       |
    | <span data-ttu-id="93a87-146">I4, I4</span><span class="sxs-lookup"><span data-stu-id="93a87-146">i4, I4</span></span>            | <span data-ttu-id="93a87-147">Lange ganzzahlige Spalte</span><span class="sxs-lookup"><span data-stu-id="93a87-147">Long Integer Column</span></span>                        |

    

     

## <a name="control-character-translation"></a><span data-ttu-id="93a87-148">Steuerzeichen Übersetzung</span><span class="sxs-lookup"><span data-stu-id="93a87-148">Control Character Translation</span></span>

<span data-ttu-id="93a87-149">Durch das Exportieren einer Tabelle in eine Textarchiv Datei werden die Steuerzeichen übersetzt, um Konflikte mit Datei Trennzeichen zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="93a87-149">Exporting a table to a text archive file translates the control characters to avoid conflicts with file delimiters.</span></span> <span data-ttu-id="93a87-150">Beim Schreiben in die IDT-Datei werden die Steuerzeichen wie folgt übersetzt.</span><span class="sxs-lookup"><span data-stu-id="93a87-150">While writing into the .idt file, the control characters are translated as follows.</span></span>



| <span data-ttu-id="93a87-151">Steuerzeichen</span><span class="sxs-lookup"><span data-stu-id="93a87-151">Control Character</span></span> | <span data-ttu-id="93a87-152">Übersetzung in. IDT</span><span class="sxs-lookup"><span data-stu-id="93a87-152">Translation in .idt</span></span> | <span data-ttu-id="93a87-153">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="93a87-153">Meaning</span></span>         |
|-------------------|---------------------|-----------------|
| <span data-ttu-id="93a87-154">NULL</span><span class="sxs-lookup"><span data-stu-id="93a87-154">NULL</span></span>              | <span data-ttu-id="93a87-155">21</span><span class="sxs-lookup"><span data-stu-id="93a87-155">21</span></span>                  | <span data-ttu-id="93a87-156">Null</span><span class="sxs-lookup"><span data-stu-id="93a87-156">Null</span></span>            |
| <span data-ttu-id="93a87-157">BS</span><span class="sxs-lookup"><span data-stu-id="93a87-157">BS</span></span>                | <span data-ttu-id="93a87-158">27</span><span class="sxs-lookup"><span data-stu-id="93a87-158">27</span></span>                  | <span data-ttu-id="93a87-159">Rückraum</span><span class="sxs-lookup"><span data-stu-id="93a87-159">Back Space</span></span>      |
| <span data-ttu-id="93a87-160">HT</span><span class="sxs-lookup"><span data-stu-id="93a87-160">HT</span></span>                | <span data-ttu-id="93a87-161">16</span><span class="sxs-lookup"><span data-stu-id="93a87-161">16</span></span>                  | <span data-ttu-id="93a87-162">Registerkarte</span><span class="sxs-lookup"><span data-stu-id="93a87-162">Tab</span></span>             |
| <span data-ttu-id="93a87-163">LF</span><span class="sxs-lookup"><span data-stu-id="93a87-163">LF</span></span>                | <span data-ttu-id="93a87-164">25</span><span class="sxs-lookup"><span data-stu-id="93a87-164">25</span></span>                  | <span data-ttu-id="93a87-165">Zeilenvorschub</span><span class="sxs-lookup"><span data-stu-id="93a87-165">Line Feed</span></span>       |
| <span data-ttu-id="93a87-166">FF</span><span class="sxs-lookup"><span data-stu-id="93a87-166">FF</span></span>                | <span data-ttu-id="93a87-167">24</span><span class="sxs-lookup"><span data-stu-id="93a87-167">24</span></span>                  | <span data-ttu-id="93a87-168">Formular Feed</span><span class="sxs-lookup"><span data-stu-id="93a87-168">Form Feed</span></span>       |
| <span data-ttu-id="93a87-169">CR</span><span class="sxs-lookup"><span data-stu-id="93a87-169">CR</span></span>                | <span data-ttu-id="93a87-170">17</span><span class="sxs-lookup"><span data-stu-id="93a87-170">17</span></span>                  | <span data-ttu-id="93a87-171">Wagen Rücklauf</span><span class="sxs-lookup"><span data-stu-id="93a87-171">Carriage Return</span></span> |



 

 

 



