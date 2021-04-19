---
description: Die Datei Gruppe der Tabellen enthält alle Windows Installer Tabellen, die sich auf Dateien beziehen.
ms.assetid: 8f56328e-ed58-41a1-94b6-266e9c117246
title: Datei Tabellen Gruppe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2667a1b9fe2bd9d2f8260523e2386bf7751dce8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355593"
---
# <a name="file-tables-group"></a><span data-ttu-id="179a3-103">Datei Tabellen Gruppe</span><span class="sxs-lookup"><span data-stu-id="179a3-103">File Tables Group</span></span>

![Datei Tabellen Gruppe](images/filegrp.png)

<span data-ttu-id="179a3-105">Weitere Informationen zu diesem Diagramm finden Sie unter [Entity Relationship Diagram-Legende](entity-relationship-diagram-legend.md).</span><span class="sxs-lookup"><span data-stu-id="179a3-105">For more information about this diagram, see the [entity relationship diagram legend](entity-relationship-diagram-legend.md).</span></span>

<span data-ttu-id="179a3-106">Ein Installer-Paket Entwickler sollte die Datei Tabellen Gruppe von Tabellen auffüllen, nachdem die Anwendung in [Komponenten und Funktionen](components-and-features.md) und nach dem Auffüllen der [Gruppe "Core Tables](core-tables-group.md)" unterteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="179a3-106">An installer package developer should consider populating the file table group of tables after breaking the application into [components and features](components-and-features.md) and after populating the [core tables group](core-tables-group.md).</span></span> <span data-ttu-id="179a3-107">Die Datei Tabellen Gruppe enthält alle Dateien, die zur Installation gehören, und die meisten dieser Dateien sind in der [Dateitabelle](file-table.md)aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="179a3-107">The file table group contains all of the files belonging to the installation and most of these files are listed in the [File table](file-table.md).</span></span> <span data-ttu-id="179a3-108">Die [Verzeichnis Tabelle](directory-table.md) wird in der Abbildung nicht angezeigt, ist jedoch eng mit der Datei Tabellen Gruppe verknüpft.</span><span class="sxs-lookup"><span data-stu-id="179a3-108">The [Directory table](directory-table.md) is not shown in the figure but is closely related to the file table group.</span></span> <span data-ttu-id="179a3-109">Die Verzeichnis Tabelle enthält die Verzeichnisstruktur der-Installation.</span><span class="sxs-lookup"><span data-stu-id="179a3-109">The Directory table gives the directory structure of the installation.</span></span>

<span data-ttu-id="179a3-110">Die Datei Gruppe der Tabellen enthält alle Tabellen, die sich auf Dateien beziehen.</span><span class="sxs-lookup"><span data-stu-id="179a3-110">The file group of tables contains all of the tables that are related to files.</span></span>

-   <span data-ttu-id="179a3-111">In der [Dateitabelle](file-table.md) sind die Dateien aufgelistet, die zur Installation gehören.</span><span class="sxs-lookup"><span data-stu-id="179a3-111">The [File table](file-table.md) lists files belonging to the installation.</span></span> <span data-ttu-id="179a3-112">Dateien, die nicht in der Dateitabelle aufgeführt sind, enthalten Datenträger Dateien, die in der Medien Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="179a3-112">Files that are not listed in the File table include disk files, which are listed in Media table.</span></span> <span data-ttu-id="179a3-113">Da jede Datei zu einer Komponente gehört, weist die Dateitabelle einen externen Schlüssel in die Komponenten Tabelle auf.</span><span class="sxs-lookup"><span data-stu-id="179a3-113">Because every file belongs to a component, the File table has an external key into the Component table.</span></span>
-   <span data-ttu-id="179a3-114">Die [Tabelle RemoveFile](removefile-table.md) enthält eine Liste der Dateien, die von der [RemoveFiles-Aktion](removefiles-action.md)entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="179a3-114">The [RemoveFile table](removefile-table.md) contains a list of files to be removed by the [RemoveFiles action](removefiles-action.md).</span></span>
-   <span data-ttu-id="179a3-115">In der [Schriftart Tabelle](font-table.md) sind die Schriftart Dateien aufgelistet, die beim System registriert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="179a3-115">The [Font table](font-table.md) lists font files to be registered with the system.</span></span>
-   <span data-ttu-id="179a3-116">In der [Tabelle selfreg](selfreg-table.md) sind die Moduldateien der Installation aufgeführt, die selbst registriert sind.</span><span class="sxs-lookup"><span data-stu-id="179a3-116">The [SelfReg table](selfreg-table.md) lists module files of the installation that are self-registered.</span></span>
-   <span data-ttu-id="179a3-117">In der [Medien Tabelle](media-table.md) werden die Quell Medien und die Datenträger aufgelistet, die zur Installation gehören.</span><span class="sxs-lookup"><span data-stu-id="179a3-117">The [Media table](media-table.md) lists the source media and disks belonging to the installation.</span></span>
-   <span data-ttu-id="179a3-118">In der [Tabelle BindImage](bindimage-table.md) sind Dateien aufgelistet, die an DLLs gebunden sind, die von ausführbaren Dateien importiert wurden.</span><span class="sxs-lookup"><span data-stu-id="179a3-118">The [BindImage table](bindimage-table.md) lists files that are bound to DLLs imported by executables.</span></span>
-   <span data-ttu-id="179a3-119">In der [Tabelle "muvefile](movefile-table.md) " wird angegeben, welche Dateien während der Installation verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="179a3-119">The [MoveFile table](movefile-table.md) specifies which files are moved during the installation.</span></span>
-   <span data-ttu-id="179a3-120">Die [duplicatefile-Tabelle](duplicatefile-table.md) gibt an, welche Dateien während der Installation dupliziert werden.</span><span class="sxs-lookup"><span data-stu-id="179a3-120">The [DuplicateFile table](duplicatefile-table.md) specifies which files are duplicated during the installation.</span></span>
-   <span data-ttu-id="179a3-121">In der [Tabelle IniFile](inifile-table.md) werden die INI-Dateien und die Informationen aufgelistet, die von der Anwendung in der Datei festgelegt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="179a3-121">The [IniFile table](inifile-table.md) lists the .ini files and the information that the application needs to set in the file.</span></span>
-   <span data-ttu-id="179a3-122">Die [removeinifile-Tabelle](removeinifile-table.md) enthält die Informationen, die eine Anwendung aus einer INI-Datei löschen muss.</span><span class="sxs-lookup"><span data-stu-id="179a3-122">The [RemoveIniFile table](removeinifile-table.md) contains the information an application needs to delete from a .ini file.</span></span>
-   <span data-ttu-id="179a3-123">Die [Umgebungs Tabelle](environment-table.md) wird verwendet, um die Werte von Umgebungsvariablen festzulegen.</span><span class="sxs-lookup"><span data-stu-id="179a3-123">The [Environment table](environment-table.md) is used to set the values of environment variables.</span></span>
-   <span data-ttu-id="179a3-124">Die [Symboltabelle](icon-table.md) enthält Symbol Informationen, die als Teil der Produktankündigung in eine Datei kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="179a3-124">The [Icon table](icon-table.md) provides icon information which is copied to a file as a part of product advertisement.</span></span>
-   <span data-ttu-id="179a3-125">In der [filesfpcatalog-Tabelle](filesfpcatalog-table.md) werden angegebene Dateien mit Katalogdateien für den Systemdatei Schutz verknüpft.</span><span class="sxs-lookup"><span data-stu-id="179a3-125">The [FileSFPCatalog table](filesfpcatalog-table.md) associates specified files with system file protection catalog files.</span></span>

    <span data-ttu-id="179a3-126">**Windows Vista, Windows Server 2003 und Windows XP:** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="179a3-126">**Windows Vista, Windows Server 2003 and Windows XP:** Not supported.</span></span>

-   <span data-ttu-id="179a3-127">Die [sfpcatalog-Tabelle](sfpcatalog-table.md) enthält Kataloge zum Systemdatei Schutz.</span><span class="sxs-lookup"><span data-stu-id="179a3-127">The [SFPCatalog table](sfpcatalog-table.md) contains system file protection catalogs.</span></span>

    <span data-ttu-id="179a3-128">**Windows Vista, Windows Server 2003 und Windows XP:** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="179a3-128">**Windows Vista, Windows Server 2003 and Windows XP:** Not supported.</span></span>

-   <span data-ttu-id="179a3-129">Die [msiflehash-Tabelle](msifilehash-table.md) wird zum Speichern eines 128-Bit-Hashs einer Quelldatei verwendet, die vom Windows Installer Paket bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="179a3-129">The [MsiFileHash table](msifilehash-table.md) is used to store a 128-bit hash of a source file provided by the Windows Installer package.</span></span>

 

 



