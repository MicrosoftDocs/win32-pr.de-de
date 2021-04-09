---
description: Wenn eine Tabelle, die nur ASCII-Zeichen enthält, in eine Textarchiv Datei exportiert wird, entspricht die IDT-Datei dem grundlegenden Archivdatei Format.
ms.assetid: 105d2b85-c6e1-4719-83b4-1693c14ef4f4
title: ASCII-Daten in Text Archivdateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d43deeb7918b75a71770ab9d09535972f6e8bb4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864464"
---
# <a name="ascii-data-in-text-archive-files"></a><span data-ttu-id="8bc54-103">ASCII-Daten in Text Archivdateien</span><span class="sxs-lookup"><span data-stu-id="8bc54-103">ASCII Data in Text Archive Files</span></span>

<span data-ttu-id="8bc54-104">Wenn eine Tabelle, die nur ASCII-Zeichen enthält, in eine [Textarchiv Datei](text-archive-files.md)exportiert wird, entspricht die IDT-Datei dem grundlegenden [Archivdatei Format](archive-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="8bc54-104">When a table that contains only ASCII characters is exported to a [text archive file](text-archive-files.md), the .idt file adheres to the basic [archive file format](archive-file-format.md).</span></span> <span data-ttu-id="8bc54-105">Wenn die Tabelle nicht-ASCII-Informationen enthält, wird das Format der Archivdatei um Code Page Informationen erweitert.</span><span class="sxs-lookup"><span data-stu-id="8bc54-105">If the table contains non-ASCII information, the format of the archive file is extended to include code page information.</span></span>

## <a name="text-archive-files-that-contain-only-ascii-characters"></a><span data-ttu-id="8bc54-106">Text Archivdateien, die nur ASCII-Zeichen enthalten</span><span class="sxs-lookup"><span data-stu-id="8bc54-106">Text archive files that contain only ASCII characters</span></span>

<span data-ttu-id="8bc54-107">Wenn eine Tabelle, die nur ASCII-Zeichen enthält, in eine Archivdatei exportiert wird, liegt die IDT-Datei im grundlegenden [Archivdatei Format](archive-file-format.md)vor.</span><span class="sxs-lookup"><span data-stu-id="8bc54-107">When a table that contains only ASCII characters is exported to an archive file, the .idt file is in the basic [archive file format](archive-file-format.md).</span></span> <span data-ttu-id="8bc54-108">Jeder Stream in der Tabelle wird als Datei mit der Dateinamenerweiterung ". ibd" exportiert.</span><span class="sxs-lookup"><span data-stu-id="8bc54-108">Each stream in the table is exported as a file with an .ibd file name extension.</span></span> <span data-ttu-id="8bc54-109">Die ibd-Dateien werden in einem Ordner mit dem gleichen Namen wie die Tabelle gespeichert.</span><span class="sxs-lookup"><span data-stu-id="8bc54-109">The .ibd files are stored in a folder with the same name as the table.</span></span> <span data-ttu-id="8bc54-110">Stellen Sie sich z. b. den Export der folgenden [binären](binary-table.md) Tabelle vor.</span><span class="sxs-lookup"><span data-stu-id="8bc54-110">For example, consider the export of the following [Binary](binary-table.md) table.</span></span>



| <span data-ttu-id="8bc54-111">Name</span><span class="sxs-lookup"><span data-stu-id="8bc54-111">Name</span></span>  | <span data-ttu-id="8bc54-112">Daten</span><span class="sxs-lookup"><span data-stu-id="8bc54-112">Data</span></span>      |
|-------|-----------|
| <span data-ttu-id="8bc54-113">Bücher</span><span class="sxs-lookup"><span data-stu-id="8bc54-113">Books</span></span> | <span data-ttu-id="8bc54-114">Bücher. ibd</span><span class="sxs-lookup"><span data-stu-id="8bc54-114">Books.ibd</span></span> |
| <span data-ttu-id="8bc54-115">Autos</span><span class="sxs-lookup"><span data-stu-id="8bc54-115">Cars</span></span>  | <span data-ttu-id="8bc54-116">Cars. ibd</span><span class="sxs-lookup"><span data-stu-id="8bc54-116">Cars.ibd</span></span>  |



 

<span data-ttu-id="8bc54-117">Die Verzeichnisstruktur nach dem Exportieren der Tabelle lautet wie folgt.</span><span class="sxs-lookup"><span data-stu-id="8bc54-117">The directory structure after exporting this table is as follows.</span></span> <span data-ttu-id="8bc54-118">Die Informationen in der Datenbanktabelle werden in Binary. IDT exportiert.</span><span class="sxs-lookup"><span data-stu-id="8bc54-118">The information in the database table is exported to Binary.idt.</span></span> <span data-ttu-id="8bc54-119">Die beiden Datenströme der Binärdaten werden in "Book. ibd" und "Cars. ibd" exportiert, die im Ordner "Binary" gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="8bc54-119">The two streams of binary data are exported to Book.ibd and Cars.ibd saved in the folder named Binary.</span></span>

``` syntax
Binary.idt
[Binary]
    Books.ibd
    Cars.ibd
```

<span data-ttu-id="8bc54-120">Die binäre IDT-Archivdatei befindet sich im grundlegenden [Archivdatei Format](archive-file-format.md) und sieht wie folgt aus.</span><span class="sxs-lookup"><span data-stu-id="8bc54-120">The Binary.idt archive file is in the basic [archive file format](archive-file-format.md) and would look as follows.</span></span>

``` syntax
Name Data
s72 v0
Binary  Name
Books   Books.ibd
Cars    Cars.ibd
```

## <a name="text-archive-files-that-contain-non--ascii-characters"></a><span data-ttu-id="8bc54-121">Text Archivdateien, die nicht-ASCII-Zeichen enthalten</span><span class="sxs-lookup"><span data-stu-id="8bc54-121">Text archive files that contain non- ASCII characters</span></span>

<span data-ttu-id="8bc54-122">Wenn die Datei nicht-ASCII-Daten enthält, wird das grundlegende [Archivdatei Format](archive-file-format.md) der IDT-Datei so erweitert, dass Sie Code Page Informationen einschließt.</span><span class="sxs-lookup"><span data-stu-id="8bc54-122">If the file contains non-ASCII data, the basic [archive file format](archive-file-format.md) of the .idt file is extended to include code page information.</span></span> <span data-ttu-id="8bc54-123">Die dritte Zeile in der. IDT-Tabelle ist die numerische Codepage, gefolgt von den Namen der Tabellennamen und der Primärschlüssel Spalten, die durch Registerkarten getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="8bc54-123">The third row in the .idt table is the numeric code page followed by the table name and primary key column names separated by tabs.</span></span>

> [!Note]  
> <span data-ttu-id="8bc54-124">Eine IDT-Datei, die nicht-ASCII-Informationen enthält, muss im ASCII-Format gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="8bc54-124">An .idt file that contains non-ASCII information should be saved in the ASCII format.</span></span> <span data-ttu-id="8bc54-125">Eine Textarchiv Datei kann z. b. die Spalten-und Tabellennamen enthalten, die als UTF-8 codiert sind, aber die Archivdatei selbst muss ASCII sein.</span><span class="sxs-lookup"><span data-stu-id="8bc54-125">For example, a text archive file can contain the column and table names encoded as UTF-8, but the archive file itself should be ASCII.</span></span>

 

<span data-ttu-id="8bc54-126">Die folgende in Französisch lokalisierte Aktions Text Tabelle enthält nicht-ASCII-Informationen.</span><span class="sxs-lookup"><span data-stu-id="8bc54-126">The following ActionText table localized into French would contain non-ASCII information.</span></span> <span data-ttu-id="8bc54-127">Die für französische Zeichen folgen verwendete numerische Codepage ist 1252.</span><span class="sxs-lookup"><span data-stu-id="8bc54-127">The numeric code page used for French strings is 1252.</span></span>



| <span data-ttu-id="8bc54-128">Aktion</span><span class="sxs-lookup"><span data-stu-id="8bc54-128">Action</span></span>    | <span data-ttu-id="8bc54-129">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8bc54-129">Description</span></span>                                  | <span data-ttu-id="8bc54-130">Vorlage</span><span class="sxs-lookup"><span data-stu-id="8bc54-130">Template</span></span> |
|-----------|----------------------------------------------|----------|
| <span data-ttu-id="8bc54-131">WERBEEINBLENDUNGEN</span><span class="sxs-lookup"><span data-stu-id="8bc54-131">ADVERTISE</span></span> | <span data-ttu-id="8bc54-132">Veröffentlichung/Information sur l-Anwendung</span><span class="sxs-lookup"><span data-stu-id="8bc54-132">Publication d'informations sur l'application</span></span> |          |



 

<span data-ttu-id="8bc54-133">Die exportierte Archivdatei "aktiontext. IDT" lautet wie folgt.</span><span class="sxs-lookup"><span data-stu-id="8bc54-133">The exported archive file, ActionText.idt, would be as follows.</span></span>

``` syntax
Action   Description Template
s72 L0  L0
1252    ActionText  Action
Advertise   Publication d'informations sur l'application
```

> [!Note]  
> <span data-ttu-id="8bc54-134">Wenn eine Textarchiv Datei nicht-ASCII-Daten enthält, enthält die Archivdatei Code Page Informationen.</span><span class="sxs-lookup"><span data-stu-id="8bc54-134">If a text archive file contains non-ASCII data, the archive file includes code page information.</span></span> <span data-ttu-id="8bc54-135">Archivdateien mit Code Page Informationen können nur zurück in eine Datenbank dieser exakten Codepage oder in eine sprachneutrale Datenbank importiert werden.</span><span class="sxs-lookup"><span data-stu-id="8bc54-135">Archive files with code page information can only be imported back into a database of that exact code page or into a language neutral database.</span></span> <span data-ttu-id="8bc54-136">Bei einer sprach neutralen Datenbank wird die Codepage auf die Codepage der Archivdatei festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8bc54-136">In the case of a language neutral database, the code page is set to the code page of the archive file.</span></span> <span data-ttu-id="8bc54-137">Weitere Informationen zur Behandlung von Codeseiten durch Windows Installer finden Sie im Abschnitt [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="8bc54-137">For more information about how Windows Installer handles code pages see the section [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span>

 

 

 



