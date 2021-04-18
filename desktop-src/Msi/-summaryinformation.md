---
description: Die \_ Tabelle SummaryInformation ist eine spezielle Tabelle, die zusammen mit dem Zusammenfassungs Informationsdaten Strom verwendet wird. Sie können den Zusammenfassungs Informationsdaten Strom einer Windows Installer Datenbank durch Exportieren oder Importieren einer Textarchiv Datei mit dem Namen " \_ SummaryInformation. IDT" erhalten oder festlegen.
ms.assetid: b1b42e03-7a05-46d4-9c42-b87906535adb
title: _SummaryInformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 803b89223db8b6fc8074336109221a8300f7c1ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368709"
---
# <a name="_summaryinformation"></a><span data-ttu-id="cc498-104">\_SummaryInformation</span><span class="sxs-lookup"><span data-stu-id="cc498-104">\_SummaryInformation</span></span>

<span data-ttu-id="cc498-105">Die \_ Tabelle SummaryInformation ist eine spezielle Tabelle, die zusammen mit dem [Zusammenfassungs Informationsdaten Strom](summary-information-stream.md)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cc498-105">The \_SummaryInformation table is a special table used with the [Summary Information Stream](summary-information-stream.md).</span></span> <span data-ttu-id="cc498-106">Sie können den Zusammenfassungs Informationsdaten Strom einer Windows Installer Datenbank durch Exportieren oder Importieren einer [Textarchiv Datei](text-archive-files.md) mit dem Namen " \_ SummaryInformation. IDT" erhalten oder festlegen.</span><span class="sxs-lookup"><span data-stu-id="cc498-106">You can get or set the Summary Information Stream of a Windows Installer database by exporting or importing a [text archive file](text-archive-files.md) named \_SummaryInformation.idt.</span></span>

<span data-ttu-id="cc498-107">Die IDT-Datei einer exportierten \_ SummaryInformation-Tabelle weist das folgende Format auf.</span><span class="sxs-lookup"><span data-stu-id="cc498-107">The .idt file of an exported \_SummaryInformation table has the following format.</span></span>

-   <span data-ttu-id="cc498-108">Die erste Zeile enthält die durch Tabstopps getrennten Tabellen Spaltennamen: PropertyId und Value.</span><span class="sxs-lookup"><span data-stu-id="cc498-108">The first row contains the table column names separated by tabs: PropertyId and Value.</span></span> <span data-ttu-id="cc498-109">Eine Liste der Eigenschaften und deren IDs (PID) finden Sie im Abschnitt " [zusammenfassende Informationsstrom](summary-information-stream-property-set.md) -Eigenschaften Satz".</span><span class="sxs-lookup"><span data-stu-id="cc498-109">See the [Summary Information Stream Property Set](summary-information-stream-property-set.md) topic for a list of the properties and their ids (PID).</span></span>
-   <span data-ttu-id="cc498-110">Die zweite Zeile enthält die Spaltendefinitionen, die durch Registerkarten getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="cc498-110">The second row contains the column definitions separated by tabs.</span></span> <span data-ttu-id="cc498-111">Die Spaltendefinitionen werden auf die gleiche Weise wie im grundlegenden IDT- [Archivdatei Format](archive-file-format.md)angegeben.</span><span class="sxs-lookup"><span data-stu-id="cc498-111">The column definitions are specified in the same way as in the basic .idt [archive file format](archive-file-format.md).</span></span> <span data-ttu-id="cc498-112">Die PropertyId-Spalte kann eine kurze Ganzzahl sein, die keine NULL-Werte zulässt.</span><span class="sxs-lookup"><span data-stu-id="cc498-112">The PropertyId column can be a non-nullable short integer.</span></span> <span data-ttu-id="cc498-113">Die Value-Spalte kann eine lokalisierbare Zeichenfolge von 255 Zeichen sein, die keine NULL-Werte zulässt.</span><span class="sxs-lookup"><span data-stu-id="cc498-113">The Value column can be a non-nullable localizable string 255 characters long.</span></span>
-   <span data-ttu-id="cc498-114">Die dritte Zeile ist der Tabellenname und der Name der Primärschlüssel Spalte, die durch Registerkarten getrennt sind: \_ SummaryInformation und PropertyId.</span><span class="sxs-lookup"><span data-stu-id="cc498-114">The third row is the table name and the primary key column name separated by tabs: \_SummaryInformation and PropertyId.</span></span>
-   <span data-ttu-id="cc498-115">Die verbleibenden Zeilen in der Datei stellen die PID und den zugeordneten Wert dar, getrennt durch Registerkarten.</span><span class="sxs-lookup"><span data-stu-id="cc498-115">The remaining rows in the file represent the PID and associated value, separated by tabs.</span></span> <span data-ttu-id="cc498-116">Datum und Uhrzeit in \_ SummaryInformation weisen folgendes Format auf: yyyy/mm/dd hh:: mm:: SS.</span><span class="sxs-lookup"><span data-stu-id="cc498-116">Date and time in\_SummaryInformation are in the format: YYYY/MM/DD hh::mm::ss.</span></span> <span data-ttu-id="cc498-117">Beispiel: 1999/03/22 15:25:45.</span><span class="sxs-lookup"><span data-stu-id="cc498-117">For example, 1999/03/22 15:25:45.</span></span>

<span data-ttu-id="cc498-118">Im folgenden finden Sie ein Beispiel für den [Zusammenfassungs Informationsdaten Strom](summary-information-stream.md) einer Datenbank im IDT-Format.</span><span class="sxs-lookup"><span data-stu-id="cc498-118">The following is an example of the [Summary Information Stream](summary-information-stream.md) of a database in .idt format.</span></span>

``` syntax
PropertyId   Value
i2  l255
_SummaryInformation PropertyId
1   1252
2   Installation Database
3   Internal Quick Test
4   Microsoft Corporation
5   Installer,MSI,Database
6   Installer Internal Release Quick Test
7   Intel;1033
9   {00000002-0001-0000-0000-624474736554}
12  1999/06/21
14  110
15  1
18  Windows Installer
```

<span data-ttu-id="cc498-119">Wenn Sie [**msidatabaseimport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) oder die [Import](database-import.md) -Methode des [**Database**](database-object.md) -Objekts verwenden, um eine Textarchiv Tabelle mit dem Namen \_ "SummaryInformation" in eine Installerdatenbank zu importieren, schreiben Sie den Datenstrom "05summaryinformation" in die Datenbank.</span><span class="sxs-lookup"><span data-stu-id="cc498-119">When you use [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) or the [Import](database-import.md) method of the [**Database**](database-object.md) object to import a text archive table named \_SummaryInformation into an installer database, you write the "05SummaryInformation" stream in the database.</span></span>

 

 



