---
description: Die Windows Installer Datenbanktabellen können mithilfe von msidatabaseexport oder der Export-Methode des Datenbankobjekts in ASCII-Textdateien exportiert werden.
ms.assetid: 49210242-bd32-4e5c-b782-a132d670fdfe
title: Text Archivdateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8baba814fd182a7da5e13fbb26eec257be96ab1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865744"
---
# <a name="text-archive-files"></a><span data-ttu-id="82380-103">Text Archivdateien</span><span class="sxs-lookup"><span data-stu-id="82380-103">Text Archive Files</span></span>

<span data-ttu-id="82380-104">Die Windows Installer Datenbanktabellen können mithilfe von [**msidatabaseexport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) oder der [**Export**](database-export.md) -Methode des [**Daten Bank**](database-object.md) Objekts in ASCII-Textdateien exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="82380-104">The Windows Installer database tables can be exported to ASCII text files by using [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) or the [**Export**](database-export.md) method of the [**Database**](database-object.md) object.</span></span> <span data-ttu-id="82380-105">Die Informationen in diesen Textarchiv Dateien können dann mithilfe von [**msidatabaseimport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) oder der [Import](database-import.md) -Methode des **Daten Bank** Objekts wieder in eine Windows Installer Datenbank importiert werden.</span><span class="sxs-lookup"><span data-stu-id="82380-105">The information in these text archive files can then be imported back into a Windows Installer database using [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) or the [Import](database-import.md) method of the **Database** object.</span></span>

<span data-ttu-id="82380-106">Tools wie [msidb.exe](msidb-exe.md) können Textarchiv Dateien exportieren und importieren.</span><span class="sxs-lookup"><span data-stu-id="82380-106">Tools such as [msidb.exe](msidb-exe.md) are capable of exporting and importing text archive files.</span></span> <span data-ttu-id="82380-107">[Windows Installer Skript Beispiele](windows-installer-scripting-examples.md) zum Exportieren und Importieren von Textarchiv Dateien aus einer Datenbank finden Sie unter [Exportieren von Dateien](export-files.md) und [Importieren von Dateien](import-files.md) .</span><span class="sxs-lookup"><span data-stu-id="82380-107">See [Export Files](export-files.md) and [Import Files](import-files.md) for [Windows Installer Scripting Examples](windows-installer-scripting-examples.md) that can export and import text archive files from a database.</span></span>

> [!Note]  
> <span data-ttu-id="82380-108">Text Archivdateien sind nicht als Mittel zum Bearbeiten der Installations Datenbank vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="82380-108">Text archive files are not intended as a means to edit the installation database.</span></span> <span data-ttu-id="82380-109">Zum Erstellen und Ändern eines Installationspakets sollten Sie ein Windows Installer Tabellen Bearbeitungs Tool verwenden, z. b. [Orca](orca-exe.md) oder ein Drittanbieter Tool.</span><span class="sxs-lookup"><span data-stu-id="82380-109">You should use a Windows Installer table editing tool, such as [Orca](orca-exe.md) or a third-party tool, to create and modify an installation package.</span></span>

 

<span data-ttu-id="82380-110">Text Archivdateien können für die folgenden Zwecke verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="82380-110">Text archive files can be used for the following purposes.</span></span>

-   <span data-ttu-id="82380-111">Text Archivdateien können mit Versionskontrollsystemen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="82380-111">Text archive files can be used with version control systems.</span></span>
-   <span data-ttu-id="82380-112">Entfernen Sie Speicherplatz, und reduzieren Sie die endgültige Größe von MSI-Dateien.</span><span class="sxs-lookup"><span data-stu-id="82380-112">To remove wasted storage space and reduce the final size of .msi files.</span></span> <span data-ttu-id="82380-113">Weitere Informationen finden Sie [unter Reduzieren der Größe einer MSI-Datei](reducing-the-size-of-an--msi-file.md).</span><span class="sxs-lookup"><span data-stu-id="82380-113">See [Reducing the Size of an .msi File](reducing-the-size-of-an--msi-file.md).</span></span>
-   <span data-ttu-id="82380-114">Zum Hinzufügen von Lokalisierungs Informationen zu einer Installations Datenbank.</span><span class="sxs-lookup"><span data-stu-id="82380-114">To add localization information to an installation database.</span></span> <span data-ttu-id="82380-115">Weitere Informationen finden Sie unter [Code Page Handling of importierte and exportierte Tables](code-page-handling-of-imported-and-exported-tables.md).</span><span class="sxs-lookup"><span data-stu-id="82380-115">For more information, see [Code Page Handling of Imported and Exported Tables](code-page-handling-of-imported-and-exported-tables.md).</span></span>

-   <span data-ttu-id="82380-116">, Um die Codepage einer Datenbank zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="82380-116">To determine the code page of a database.</span></span> <span data-ttu-id="82380-117">Weitere Informationen finden Sie unter [bestimmen der Codepage einer Installations Datenbank](determining-an-installation-database-s-code-page.md).</span><span class="sxs-lookup"><span data-stu-id="82380-117">See [Determining an Installation Database's Code Page](determining-an-installation-database-s-code-page.md).</span></span>
-   <span data-ttu-id="82380-118">, Um die Codepage einer Datenbank festzulegen.</span><span class="sxs-lookup"><span data-stu-id="82380-118">To set the code page of a database.</span></span> <span data-ttu-id="82380-119">Siehe [Festlegen der Codepage einer Datenbank](setting-the-code-page-of-a-database.md).</span><span class="sxs-lookup"><span data-stu-id="82380-119">See [Setting the code page of a database](setting-the-code-page-of-a-database.md).</span></span>
-   <span data-ttu-id="82380-120">, Um den Grenzwert einer Daten Bank Spalte zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="82380-120">To increase the limit of a database column.</span></span> <span data-ttu-id="82380-121">Exportieren Sie die Tabelle mithilfe von " [**msidatabaseexport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)", bearbeiten Sie die exportierte IDT-Datei, und importieren Sie dann die Tabelle mithilfe von " [**msidatabaseimport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)".</span><span class="sxs-lookup"><span data-stu-id="82380-121">Export the table using [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta), edit the exported .idt file, and then import the table using [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span></span> <span data-ttu-id="82380-122">Autoren können die Spaltendatentypen, die NULL-Zulässigkeit oder die Lokalisierungs Attribute von Spalten in Standard Tabellen nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="82380-122">Authors cannot change the column data types, nullability, or localization attributes of any columns in standard tables.</span></span> <span data-ttu-id="82380-123">Siehe auch [Erstellen eines großen Pakets](authoring-a-large-package.md).</span><span class="sxs-lookup"><span data-stu-id="82380-123">See also [Authoring a Large Package](authoring-a-large-package.md).</span></span>

<span data-ttu-id="82380-124">Auf den folgenden Seiten werden Textarchiv Seiten und deren Formate beschrieben.</span><span class="sxs-lookup"><span data-stu-id="82380-124">The following pages describe text archive pages and their formats.</span></span>

-   [<span data-ttu-id="82380-125">Archivdatei Format</span><span class="sxs-lookup"><span data-stu-id="82380-125">Archive File Format</span></span>](archive-file-format.md)
-   [<span data-ttu-id="82380-126">ASCII-Daten in Text Archivdateien</span><span class="sxs-lookup"><span data-stu-id="82380-126">ASCII Data in Text Archive Files</span></span>](ascii-data-in-text-archive-files.md)
-   [<span data-ttu-id="82380-127">\_Forcecodepage</span><span class="sxs-lookup"><span data-stu-id="82380-127">\_ForceCodepage</span></span>](-forcecodepage.md)
-   [<span data-ttu-id="82380-128">\_SummaryInformation</span><span class="sxs-lookup"><span data-stu-id="82380-128">\_SummaryInformation</span></span>](-summaryinformation.md)

 

 



