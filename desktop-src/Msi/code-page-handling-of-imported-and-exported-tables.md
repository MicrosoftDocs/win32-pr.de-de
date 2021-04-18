---
description: Sie können einer Installations Datenbank Lokalisierungs Informationen hinzufügen, indem Sie ASCII-Textarchiv Dateien mithilfe von "msidatabaseexport" und "msidatabaseimport" Importieren und exportieren.
ms.assetid: dc52313b-38e7-43cc-abfd-86966c836fce
title: Code Page Behandlung importierter und exportierter Tabellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b090bead1fa35b451ed12e0e0da0143b98b8918
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345164"
---
# <a name="code-page-handling-of-imported-and-exported-tables"></a><span data-ttu-id="b018e-103">Code Page Behandlung importierter und exportierter Tabellen</span><span class="sxs-lookup"><span data-stu-id="b018e-103">Code Page Handling of Imported and Exported Tables</span></span>

<span data-ttu-id="b018e-104">Sie können einer Installations Datenbank Lokalisierungs Informationen hinzufügen, indem Sie ASCII-Textarchiv Dateien mithilfe von " [**msidatabaseexport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) " und " [**msidatabaseimport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)" Importieren und exportieren.</span><span class="sxs-lookup"><span data-stu-id="b018e-104">You can add localization information to an installation database by importing and exporting ASCII text archive files using [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) and [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span></span> <span data-ttu-id="b018e-105">Da der Daten Bank Zeichen folgen Pool eine ANSI-Codepage verwendet, verfügen sowohl die Datenbank als auch die exportierten [Text Archivdateien](text-archive-files.md) über Codepages.</span><span class="sxs-lookup"><span data-stu-id="b018e-105">Because the database string pool uses an ANSI code page, both the database and exported [Text Archive Files](text-archive-files.md) have code pages.</span></span>

<span data-ttu-id="b018e-106">Wenn eine [Text Archivdatei](text-archive-files.md) aus einer Datenbank exportiert wird, ist die Codepage der Archivdatei mit der übergeordneten Datenbank identisch.</span><span class="sxs-lookup"><span data-stu-id="b018e-106">When a [Text Archive File](text-archive-files.md) is exported from a database, the code page of the archive file is the same as the parent database.</span></span> <span data-ttu-id="b018e-107">Eine Liste numerischer Codepages finden Sie unter [lokalisieren der Fehler-und Aktions Text Tabellen](localizing-the-error-and-actiontext-tables.md).</span><span class="sxs-lookup"><span data-stu-id="b018e-107">For a list of numeric code pages, see [Localizing the Error and ActionText Tables](localizing-the-error-and-actiontext-tables.md).</span></span>

> [!Note]  
> <span data-ttu-id="b018e-108">Durch das Exportieren einer Tabelle in eine Textarchiv Datei werden die Steuerzeichen übersetzt, um Konflikte mit Datei Trennzeichen zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="b018e-108">Exporting a table to a text archive file translates the control characters to avoid conflicts with file delimiters.</span></span>

 

## <a name="ascii-text-archive-files"></a><span data-ttu-id="b018e-109">ASCII-Text Archivdateien</span><span class="sxs-lookup"><span data-stu-id="b018e-109">ASCII Text Archive Files</span></span>

<span data-ttu-id="b018e-110">Die von [**msidatabaseexport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) exportierten ASCII- [Text Archivdateien](text-archive-files.md) werden im folgenden Format erläutert:</span><span class="sxs-lookup"><span data-stu-id="b018e-110">The ASCII [Text Archive Files](text-archive-files.md) exported by [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) are explained in the following format:</span></span>

-   <span data-ttu-id="b018e-111">Die Namen der Tabellen Spalten werden in der ersten Zeile geschrieben.</span><span class="sxs-lookup"><span data-stu-id="b018e-111">The names of the table columns are written on the first line.</span></span>
-   <span data-ttu-id="b018e-112">Die Spalten Formate werden in der zweiten Zeile geschrieben.</span><span class="sxs-lookup"><span data-stu-id="b018e-112">The column formats are written on the second line.</span></span>
-   <span data-ttu-id="b018e-113">Wenn die Tabelle nur ASCII-Daten enthält, ist die dritte Zeile der Textdatei der Tabellenname, gefolgt von einer Liste der Primärschlüssel.</span><span class="sxs-lookup"><span data-stu-id="b018e-113">If the table contains only ASCII data, the third line of the text file is the table name followed by a list of the primary keys.</span></span>
-   <span data-ttu-id="b018e-114">Wenn die Tabelle nicht-ASCII-Daten enthält und die Datenbank mit einer numerischen Codepage versehen ist, wird die Code Page Nummer am Anfang der dritten Zeile angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b018e-114">If the table contains non-ASCII data and the database is stamped with a numeric code page, the code page number appears at the beginning of the third line.</span></span>
-   <span data-ttu-id="b018e-115">Wenn die Datenbank nicht-ASCII-Daten enthält, aber die Datenbank nicht mit der numerischen Codepage versehen ist, wird die aktuelle Systemcode Page-Nummer am Anfang der dritten Zeile geschrieben.</span><span class="sxs-lookup"><span data-stu-id="b018e-115">If the database contains non-ASCII data, but the database is not stamped with the numeric code page, the current system code page number is written at the beginning of the third line.</span></span>
-   <span data-ttu-id="b018e-116">Die verbleibenden Zeilen der Textdatei sind die Daten in der angegebenen Codepage.</span><span class="sxs-lookup"><span data-stu-id="b018e-116">The remaining lines of the text file are the data in the specified code page.</span></span>
-   <span data-ttu-id="b018e-117">Wenn eine Tabelle Streams enthält, exportiert [**msidatabaseexport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) jeden Stream in der Tabelle in eine separate Datei.</span><span class="sxs-lookup"><span data-stu-id="b018e-117">If a table contains streams, [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) exports each stream in the table to a separate file.</span></span>

### <a name="neutral-and-non-neutral-code-pages"></a><span data-ttu-id="b018e-118">Neutrale und nicht neutrale Codepages</span><span class="sxs-lookup"><span data-stu-id="b018e-118">Neutral and Non-Neutral Code Pages</span></span>

<span data-ttu-id="b018e-119">Sie können die Lokalisierung vereinfachen, indem Sie eine Datenbank mit einer neutralen Codepage starten:</span><span class="sxs-lookup"><span data-stu-id="b018e-119">You can facilitate localization by starting with a database that has a neutral code page:</span></span>

-   <span data-ttu-id="b018e-120">Eine leere Datenbank verfügt über eine neutrale Codepage.</span><span class="sxs-lookup"><span data-stu-id="b018e-120">A blank database has a neutral code page.</span></span>
-   <span data-ttu-id="b018e-121">Eine Datenbank, die keine erweiterten Zeichen enthält, die erfordern, dass eine Codepage in ASCII dargestellt wird, verfügt über eine neutrale Codepage.</span><span class="sxs-lookup"><span data-stu-id="b018e-121">A database that does not contain extended characters that require a code page to be represented in ASCII has a neutral code page.</span></span>

<span data-ttu-id="b018e-122">Weitere Informationen finden Sie unter [Erstellen einer Datenbank mit einer neutralen Codepage](creating-a-database-with-a-neutral-code-page.md).</span><span class="sxs-lookup"><span data-stu-id="b018e-122">For more information, see [Creating a Database with a Neutral Code Page](creating-a-database-with-a-neutral-code-page.md).</span></span>

<span data-ttu-id="b018e-123">Neutrale und nicht neutrale Codepages weisen die folgenden Eigenschaften auf:</span><span class="sxs-lookup"><span data-stu-id="b018e-123">Neutral and non-neutral code pages have the following characteristics:</span></span>

-   <span data-ttu-id="b018e-124">Wenn eine [Text Archivdatei](text-archive-files.md) mit einer nicht neutralen Codepage in eine Datenbank mit einer anderen nicht neutralen Codepage importiert wird, gibt das Installationsprogramm einen Fehler zurück, wenn [**msidatabaseimport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b018e-124">If a [Text Archive File](text-archive-files.md) with a non-neutral code page is imported into a database that has a different non-neutral code page, the Installer returns an error when [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) is called.</span></span>
-   <span data-ttu-id="b018e-125">Eine [Text Archivdatei](text-archive-files.md) mit einer neutralen Codepage kann in eine Datenbank mit einer beliebigen Codepage importiert werden.</span><span class="sxs-lookup"><span data-stu-id="b018e-125">A [Text Archive File](text-archive-files.md) that has a neutral code page can be imported into a database that has any code page.</span></span>
-   <span data-ttu-id="b018e-126">Eine [Text Archivdatei](text-archive-files.md) mit einer beliebigen Codepage kann in eine Datenbank mit einer neutralen Codepage importiert werden.</span><span class="sxs-lookup"><span data-stu-id="b018e-126">A [Text Archive File](text-archive-files.md) that has any code page can be imported into a database that has a neutral code page.</span></span>
-   <span data-ttu-id="b018e-127">Wenn Sie eine [Text Archivdatei](text-archive-files.md) mit einer neutralen Codepage in eine Datenbank importieren, wird die Codepage der Datenbank auf die Codepage der Archivdatei festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b018e-127">Importing a [Text Archive File](text-archive-files.md) into a database with a neutral code page sets the code page of the database to the archive file code page.</span></span> <span data-ttu-id="b018e-128">Alle Archivdateien, die anschließend in die Datenbank importiert werden, müssen die gleiche Codepage wie die erste Datei aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b018e-128">All archive files subsequently imported into the database must have the same code page as the first file.</span></span>

<span data-ttu-id="b018e-129">Weitere Informationen finden Sie unter [bestimmen der Codepage der Installations Datenbank](determining-an-installation-database-s-code-page.md) und [Festlegen der Codepage einer Datenbank](setting-the-code-page-of-a-database.md).</span><span class="sxs-lookup"><span data-stu-id="b018e-129">For more information, see [Determining an Installation Database Code Page](determining-an-installation-database-s-code-page.md) and [Setting the Code Page of a Database](setting-the-code-page-of-a-database.md).</span></span>

<span data-ttu-id="b018e-130">Die von [**msidatabaseexport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) exportierten [Text Archivdateien](text-archive-files.md) können mit Versionskontrollsystemen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b018e-130">The [Text Archive Files](text-archive-files.md) that are exported by [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) can be used with version control systems.</span></span> <span data-ttu-id="b018e-131">Verwenden Sie die [Datenbankfunktionen](database-functions.md) oder einen Datenbanktabellen-Editor, um die Datenbank zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="b018e-131">Use the [Database Functions](database-functions.md) or a database table editor to edit the database.</span></span>

<span data-ttu-id="b018e-132">Sie können einer Installations Datenbank Lokalisierungs Informationen hinzufügen, indem Sie einen Datenbanktabellen-Editor oder die Windows Installer-API verwenden.</span><span class="sxs-lookup"><span data-stu-id="b018e-132">You can add localization information to an installation database by using a database table editor or the Windows Installer API.</span></span> <span data-ttu-id="b018e-133">Weitere Informationen finden Sie unter [Code Page Handling of Parameter Strings](code-page-handling-of-parameter-strings.md).</span><span class="sxs-lookup"><span data-stu-id="b018e-133">For more information, see [Code Page Handling of Parameter Strings](code-page-handling-of-parameter-strings.md).</span></span>

 

 



