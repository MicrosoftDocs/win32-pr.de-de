---
description: 'Nachdem die Datei Kosten verarbeitet wurde, verfügt das Installationsprogramm über alle Informationen, die zum Verarbeiten der beiden Datei Bearbeitungs Aktionen erforderlich sind: duplicatefiles und muvefiles.'
ms.assetid: 2e6d6eb3-1e71-46e6-a946-d9cc0b209325
title: Datei Installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472c58db3dc2e9094a26d57f871359a38930877b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131785"
---
# <a name="file-installation"></a><span data-ttu-id="eb1f7-103">Datei Installation</span><span class="sxs-lookup"><span data-stu-id="eb1f7-103">File Installation</span></span>

<span data-ttu-id="eb1f7-104">Nachdem die [Datei Kosten](file-costing.md) verarbeitet wurde, verfügt das Installationsprogramm über alle Informationen, die zum Verarbeiten der beiden Datei Bearbeitungs Aktionen erforderlich sind: [duplicatefiles](duplicatefiles-action.md) und [muvefiles](movefiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="eb1f7-104">Once [file costing](file-costing.md) has been completed, the installer has all the information required to process the two file manipulation actions: [DuplicateFiles](duplicatefiles-action.md) and [MoveFiles](movefiles-action.md).</span></span>

<span data-ttu-id="eb1f7-105">Verwenden Sie die [duplicatefiles-Aktion](duplicatefiles-action.md) , um die Dateien anzugeben, die das Installationsprogramm in der [duplicatefile-Tabelle](duplicatefile-table.md)duplizieren soll.</span><span class="sxs-lookup"><span data-stu-id="eb1f7-105">Use the [DuplicateFiles action](duplicatefiles-action.md) to specify the files the installer is to duplicate in the [DuplicateFile table](duplicatefile-table.md).</span></span> <span data-ttu-id="eb1f7-106">Verwenden Sie die [Aktion movefiles](movefiles-action.md), um zu bestimmen, welche Dateien verschoben werden sollen, indem Sie die [MoveFile-Tabelle](movefile-table.md)Abfragen.</span><span class="sxs-lookup"><span data-stu-id="eb1f7-106">Use the [MoveFiles action](movefiles-action.md)to determine which files to move by querying the [MoveFile table](movefile-table.md).</span></span>

<span data-ttu-id="eb1f7-107">Beachten Sie, dass das Options Feld der [Tabelle "muvefile](movefile-table.md) " angibt, ob die ursprüngliche Datei aus Ihrem aktuellen Speicherort gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="eb1f7-107">Note that the Options field of the [MoveFile table](movefile-table.md) specifies whether or not the original file is to be deleted from its current location.</span></span> <span data-ttu-id="eb1f7-108">Dateien, die von der Aktion "muvefiles" verschoben oder kopiert werden, werden bei der Installation des Produkts nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="eb1f7-108">Files that are moved or copied by the MoveFiles action are not deleted when the product is uninstalled.</span></span>

<span data-ttu-id="eb1f7-109">Die [Aktion InstallFiles](installfiles-action.md) wird aufgerufen, sobald alle anderen Datei Bearbeitungsvorgänge abgeschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="eb1f7-109">The [InstallFiles action](installfiles-action.md) is called once all other file manipulation operations have completed.</span></span> <span data-ttu-id="eb1f7-110">Die Aktion InstallFiles verarbeitet die [Medien Tabelle](media-table.md), die [Dateitabelle](file-table.md)und die [Komponenten Tabelle](component-table.md) , um zu bestimmen, welche Dateien aus der Quelle in das Ziel kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="eb1f7-110">The InstallFiles action processes the [Media table](media-table.md), the [File table](file-table.md), and the [Component table](component-table.md) to determine which files will be copied from the source to the destination.</span></span>

<span data-ttu-id="eb1f7-111">Mit der [Aktion InstallFiles](installfiles-action.md) wird die Verzeichnisstruktur erstellt, die für die Installation aller Dateien erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="eb1f7-111">The [InstallFiles action](installfiles-action.md) creates the directory structure necessary to install all files.</span></span> <span data-ttu-id="eb1f7-112">Wenn ein explizit leerer Ordner installiert werden muss, kann die Aktion "up [Folder](createfolders-action.md) " aufgerufen werden, um Sie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="eb1f7-112">If an explicitly empty folder is required to be installed, the [CreateFolders action](createfolders-action.md) may be called to create it.</span></span>

 

 



