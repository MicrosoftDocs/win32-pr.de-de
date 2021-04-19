---
description: Die Installer-Datenbank ermöglicht es dem Entwickler eines Installationspakets, die Übertragung einer Anwendung von einem Quell-in ein Zielimage zu steuern.
ms.assetid: 058cefcd-83dd-4a13-bd55-11d52f9d41f5
title: Verwenden der Installer-Datenbank
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb22b9c66547c849b4c9cbd012e78b22d9301756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350234"
---
# <a name="using-the-installer-database"></a><span data-ttu-id="c0715-103">Verwenden der Installer-Datenbank</span><span class="sxs-lookup"><span data-stu-id="c0715-103">Using the Installer Database</span></span>

<span data-ttu-id="c0715-104">Die [Installer-Datenbank](installer-database.md) ermöglicht es dem Entwickler eines Installationspakets, die Übertragung einer Anwendung von einem Quell-in ein Zielimage zu steuern.</span><span class="sxs-lookup"><span data-stu-id="c0715-104">The [Installer Database](installer-database.md) enables the developer of an installation package to control the transfer of an application from a source to a target image.</span></span> <span data-ttu-id="c0715-105">Das Layout der Quell-und Ziel Images der Anwendung wird in der [Verzeichnis](directory-table.md) Tabelle angegeben, und die Aktionen, mit denen die Anwendung installiert wird, werden in sechs Sequenz Tabellen angegeben:</span><span class="sxs-lookup"><span data-stu-id="c0715-105">The layout of both the source and target images of the application are specified in the [Directory](directory-table.md) table and the actions that install the application are specified in six sequence tables:</span></span>

-   <span data-ttu-id="c0715-106">[InstallUISequence](installuisequence-table.md) -Tabelle</span><span class="sxs-lookup"><span data-stu-id="c0715-106">[InstallUISequence](installuisequence-table.md) table</span></span>
-   <span data-ttu-id="c0715-107">[InstallExecuteSequence](installexecutesequence-table.md) -Tabelle</span><span class="sxs-lookup"><span data-stu-id="c0715-107">[InstallExecuteSequence](installexecutesequence-table.md) table</span></span>
-   <span data-ttu-id="c0715-108">[AdminUISequence](adminuisequence-table.md) -Tabelle</span><span class="sxs-lookup"><span data-stu-id="c0715-108">[AdminUISequence](adminuisequence-table.md) table</span></span>
-   <span data-ttu-id="c0715-109">[AdminExecuteSequence](adminexecutesequence-table.md) -Tabelle</span><span class="sxs-lookup"><span data-stu-id="c0715-109">[AdminExecuteSequence](adminexecutesequence-table.md) table</span></span>
-   <span data-ttu-id="c0715-110">[Advtuisequence](advtuisequence-table.md) -Tabelle</span><span class="sxs-lookup"><span data-stu-id="c0715-110">[AdvtUISequence](advtuisequence-table.md) table</span></span>
-   <span data-ttu-id="c0715-111">[AdvtExecuteSequence](advtexecutesequence-table.md) -Tabelle</span><span class="sxs-lookup"><span data-stu-id="c0715-111">[AdvtExecuteSequence](advtexecutesequence-table.md) table</span></span>

<span data-ttu-id="c0715-112">In den folgenden Abschnitten wird beschrieben, wie die [Installer-Datenbank](installer-database.md)verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="c0715-112">The following sections describe how to use the [Installer Database](installer-database.md):</span></span>

-   [<span data-ttu-id="c0715-113">Verwenden der Verzeichnis Tabelle</span><span class="sxs-lookup"><span data-stu-id="c0715-113">Using the Directory Table</span></span>](using-the-directory-table.md)
-   [<span data-ttu-id="c0715-114">Verwenden einer Sequenz Tabelle</span><span class="sxs-lookup"><span data-stu-id="c0715-114">Using a Sequence Table</span></span>](using-a-sequence-table.md)
-   [<span data-ttu-id="c0715-115">Abrufen eines Daten Bank Handles</span><span class="sxs-lookup"><span data-stu-id="c0715-115">Obtaining a Database Handle</span></span>](obtaining-a-database-handle.md)
-   [<span data-ttu-id="c0715-116">Commit für Datenbanken</span><span class="sxs-lookup"><span data-stu-id="c0715-116">Committing Databases</span></span>](committing-databases.md)
-   [<span data-ttu-id="c0715-117">Importieren und Exportieren</span><span class="sxs-lookup"><span data-stu-id="c0715-117">Importing and Exporting</span></span>](importing-and-exporting.md)
-   [<span data-ttu-id="c0715-118">Daten Bank Zusammenführung</span><span class="sxs-lookup"><span data-stu-id="c0715-118">Merging Databases</span></span>](merging-databases.md)
-   [<span data-ttu-id="c0715-119">Benennen von benutzerdefinierten Tabellen, Eigenschaften und Aktionen</span><span class="sxs-lookup"><span data-stu-id="c0715-119">Naming Custom Tables, Properties, and Actions</span></span>](naming-custom-tables-properties-and-actions.md)
-   [<span data-ttu-id="c0715-120">OLE-Einschränkungen für Streams</span><span class="sxs-lookup"><span data-stu-id="c0715-120">OLE Limitations on Streams</span></span>](ole-limitations-on-streams.md)
-   [<span data-ttu-id="c0715-121">Arbeiten mit Abfragen</span><span class="sxs-lookup"><span data-stu-id="c0715-121">Working with Queries</span></span>](working-with-queries.md)
-   [<span data-ttu-id="c0715-122">Hinzufügen von Binärdaten zu einer Tabelle mithilfe von SQL</span><span class="sxs-lookup"><span data-stu-id="c0715-122">Adding Binary Data to a Table Using SQL</span></span>](adding-binary-data-to-a-table-using-sql.md)
-   [<span data-ttu-id="c0715-123">Arbeiten mit Datensätzen</span><span class="sxs-lookup"><span data-stu-id="c0715-123">Working with Records</span></span>](working-with-records.md)
-   [<span data-ttu-id="c0715-124">Arbeiten mit Ordner Standorten</span><span class="sxs-lookup"><span data-stu-id="c0715-124">Working with Folder Locations</span></span>](working-with-folder-locations.md)
-   [<span data-ttu-id="c0715-125">Angeben der Reihenfolge der Selbstregistrierung</span><span class="sxs-lookup"><span data-stu-id="c0715-125">Specifying the Order of Self Registration</span></span>](specifying-the-order-of-self-registration.md)
-   [<span data-ttu-id="c0715-126">Während des Entfernens auszuführende Aufbereitungs Aktionen</span><span class="sxs-lookup"><span data-stu-id="c0715-126">Conditioning Actions to Run During Removal</span></span>](conditioning-actions-to-run-during-removal.md)
-   [<span data-ttu-id="c0715-127">Aufrufen von Datenbankfunktionen von Programmen</span><span class="sxs-lookup"><span data-stu-id="c0715-127">Calling Database Functions from Programs</span></span>](calling-database-functions-from-programs.md)
-   [<span data-ttu-id="c0715-128">Syntax der bedingten Anweisung</span><span class="sxs-lookup"><span data-stu-id="c0715-128">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
-   [<span data-ttu-id="c0715-129">Spalten Definitions Format</span><span class="sxs-lookup"><span data-stu-id="c0715-129">Column Definition Format</span></span>](column-definition-format.md)
-   [<span data-ttu-id="c0715-130">Bestimmen, ob eine Spalte ein Primärschlüssel oder ein externer Schlüssel ist</span><span class="sxs-lookup"><span data-stu-id="c0715-130">Determining Whether a Column is a Primary or External Key</span></span>](determining-whether-a-column-is-a-primary-or-external-key.md)

 

 



