---
title: Windows projiziertes Datei System Glossar
description: Besondere Begriffe, die in projfs verwendet werden.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: c6eac8faa83e2c898e4b1a3ada5c24ef81151b22
ms.sourcegitcommit: a48b68a75323edfb902eb04fbe6d0ecba6988c21
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/21/2020
ms.locfileid: "106338649"
---
# <a name="windows-projected-file-system-glossary"></a><span data-ttu-id="1a51d-103">Windows projiziertes Datei System Glossar</span><span class="sxs-lookup"><span data-stu-id="1a51d-103">Windows Projected File System glossary</span></span>

<span data-ttu-id="1a51d-104">Besondere Begriffe, die in projfs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1a51d-104">Special terms used in ProjFS.</span></span>

<dl>
<dt>

<span data-ttu-id="1a51d-105"><span id="projfs.glossary_backing_store"></span><span id="PROJFS.GLOSSARY_BACKING_STORE"></span>**Sicherungs Speicher**</span><span class="sxs-lookup"><span data-stu-id="1a51d-105"><span id="projfs.glossary_backing_store"></span><span id="PROJFS.GLOSSARY_BACKING_STORE"></span>**backing store**</span></span>
</dt>
<dd>

<span data-ttu-id="1a51d-106">Vom Anbieter erhaltene hierarchische Daten, die als Dateien und Verzeichnisse in das Dateisystem projiziert werden.</span><span class="sxs-lookup"><span data-stu-id="1a51d-106">Provider-maintained hierarchical data that is projected into the file system as files and directories.</span></span>
</dd>

<dt>

<span data-ttu-id="1a51d-107"><span id="projfs.glossary_dirty_placeholder"></span><span id="PROJFS.GLOSSARY_DIRTY_PLACEHOLDER"></span>**Platzhalter für Dirty**</span><span class="sxs-lookup"><span data-stu-id="1a51d-107"><span id="projfs.glossary_dirty_placeholder"></span><span id="PROJFS.GLOSSARY_DIRTY_PLACEHOLDER"></span>**dirty placeholder**</span></span>
</dt>
<dd>

<span data-ttu-id="1a51d-108">Eine Datei oder ein Verzeichnis, das lokal geändert wurde und kein Cache seines Zustands im Speicher des Anbieters mehr ist.</span><span class="sxs-lookup"><span data-stu-id="1a51d-108">A file or directory that has been locally modified and is no longer a cache of its state in the provider's store.</span></span>  <span data-ttu-id="1a51d-109">Siehe [Cache Status im virtualisierungsstamm](cache-state.md).</span><span class="sxs-lookup"><span data-stu-id="1a51d-109">See [Cache State in the Virtualization Root](cache-state.md).</span></span>
</dd>

<dt>

<span data-ttu-id="1a51d-110"><span id="projfs.glossary_full_file_directory"></span><span id="PROJFS.GLOSSARY_FULL_FILE_DIRECTORY"></span>**vollständige Datei/Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="1a51d-110"><span id="projfs.glossary_full_file_directory"></span><span id="PROJFS.GLOSSARY_FULL_FILE_DIRECTORY"></span>**full file/directory**</span></span>
</dt>
<dd>

<span data-ttu-id="1a51d-111">Eine Datei oder ein Verzeichnis, die im lokalen Dateisystem erstellt wurde, oder eine Datei, die geändert wurde, sodass Sie nicht mehr in den Sicherungs Speicher versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="1a51d-111">A file or directory that was created in the local file system, or a file that has been modified, making it no longer a cache of its state in the backing store.</span></span>  <span data-ttu-id="1a51d-112">Siehe [Cache Status im virtualisierungsstamm](cache-state.md).</span><span class="sxs-lookup"><span data-stu-id="1a51d-112">See [Cache State in the Virtualization Root](cache-state.md).</span></span>
</dd>

<dt>

<span data-ttu-id="1a51d-113"><span id="projfs.glossary_hydrated_placeholder"></span><span id="PROJFS.GLOSSARY_HYDRATED_PLACEHOLDER"></span>**Platzhalter**</span><span class="sxs-lookup"><span data-stu-id="1a51d-113"><span id="projfs.glossary_hydrated_placeholder"></span><span id="PROJFS.GLOSSARY_HYDRATED_PLACEHOLDER"></span>**hydrated placeholder**</span></span>
</dt>
<dd>

<span data-ttu-id="1a51d-114">Eine Datei, deren Inhalt und Metadaten auf dem Datenträger zwischengespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="1a51d-114">A file whose content and metadata have been cached to disk.</span></span>  <span data-ttu-id="1a51d-115">Siehe [Cache Status im virtualisierungsstamm](cache-state.md).</span><span class="sxs-lookup"><span data-stu-id="1a51d-115">See [Cache State in the Virtualization Root](cache-state.md).</span></span>
</dd>

<dt>

<span data-ttu-id="1a51d-116"><span id="projfs.glossary_placeholder"></span><span id="PROJFS.GLOSSARY_PLACEHOLDER"></span>**Platzhalter**</span><span class="sxs-lookup"><span data-stu-id="1a51d-116"><span id="projfs.glossary_placeholder"></span><span id="PROJFS.GLOSSARY_PLACEHOLDER"></span>**placeholder**</span></span>
</dt>
<dd>

<span data-ttu-id="1a51d-117">Eine Datei oder ein Verzeichnis, die auf dem Datenträger nicht vollständig vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="1a51d-117">A file or directory that is not fully present on disk.</span></span>  <span data-ttu-id="1a51d-118">Siehe [Cache Status im virtualisierungsstamm](cache-state.md).</span><span class="sxs-lookup"><span data-stu-id="1a51d-118">See [Cache State in the Virtualization Root](cache-state.md).</span></span>
</dd>

<dt>

<span data-ttu-id="1a51d-119"><span id="projfs.glossary_tombstone"></span><span id="PROJFS.GLOSSARY_TOMBSTONE"></span>**Tombstone**</span><span class="sxs-lookup"><span data-stu-id="1a51d-119"><span id="projfs.glossary_tombstone"></span><span id="PROJFS.GLOSSARY_TOMBSTONE"></span>**tombstone**</span></span>
</dt>
<dd>

<span data-ttu-id="1a51d-120">Ein spezieller ausgeblendeter Platzhalter, der ein Element darstellt, das aus dem lokalen Dateisystem gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="1a51d-120">A special hidden placeholder that represents an item that has been deleted from the local file system.</span></span>  <span data-ttu-id="1a51d-121">Siehe [Cache Status im virtualisierungsstamm](cache-state.md).</span><span class="sxs-lookup"><span data-stu-id="1a51d-121">See [Cache State in the Virtualization Root](cache-state.md).</span></span>
</dd>

<dt>

<span data-ttu-id="1a51d-122"><span id="projfs.glossary_virtual_file_directory"></span><span id="PROJFS.GLOSSARY_virtual_file_directory"></span>**virtuelle Datei/Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="1a51d-122"><span id="projfs.glossary_virtual_file_directory"></span><span id="PROJFS.GLOSSARY_virtual_file_directory"></span>**virtual file/directory**</span></span>
</dt>
<dd>

<span data-ttu-id="1a51d-123">Eine Datei oder ein Verzeichnis, die physisch nicht auf dem Datenträger vorhanden ist, jedoch in enumerationsergebnisse projiziert wird.</span><span class="sxs-lookup"><span data-stu-id="1a51d-123">A file or directory that does not physically exist on disk, but is projected into enumeration results.</span></span>  <span data-ttu-id="1a51d-124">Siehe [Cache Status im virtualisierungsstamm](cache-state.md).</span><span class="sxs-lookup"><span data-stu-id="1a51d-124">See [Cache State in the Virtualization Root](cache-state.md).</span></span>
</dd>

<dt>

<span data-ttu-id="1a51d-125"><span id="projfs.glossary_virtualization_instance"></span><span id="PROJFS.GLOSSARY_VIRTUALIZATION_INSTANCE"></span>**virtualisierungsinstanz**</span><span class="sxs-lookup"><span data-stu-id="1a51d-125"><span id="projfs.glossary_virtualization_instance"></span><span id="PROJFS.GLOSSARY_VIRTUALIZATION_INSTANCE"></span>**virtualization instance**</span></span>
</dt>
<dd>

<span data-ttu-id="1a51d-126">Ein in-Memory-Objekt, das die Kommunikation zwischen dem Anbieter und projfs für den Satz von Dateien und Verzeichnissen verwaltet, die sich unter einem bestimmten virtualisierungsstamm befinden.</span><span class="sxs-lookup"><span data-stu-id="1a51d-126">An in-memory object that manages communication between the provider and ProjFS for the set of files and directories located under a particular virtualization root.</span></span>
</dd>

<dt>

<span data-ttu-id="1a51d-127"><span id="projfs.glossary_virtualization_root"></span><span id="PROJFS.GLOSSARY_VIRTUALIZATION_ROOT"></span>**virtualisierungsstamm**</span><span class="sxs-lookup"><span data-stu-id="1a51d-127"><span id="projfs.glossary_virtualization_root"></span><span id="PROJFS.GLOSSARY_VIRTUALIZATION_ROOT"></span>**virtualization root**</span></span>
</dt>
<dd>

<span data-ttu-id="1a51d-128">Ein Verzeichnis im Dateisystem, in dem die Daten des Anbieters projiziert werden.</span><span class="sxs-lookup"><span data-stu-id="1a51d-128">A directory in the file system under which the provider's data is projected.</span></span>
</dd>

</dl>

<!--
<dt>

<span id="projfs.glossary_"></span><span id="PROJFS.GLOSSARY_"></span>**TERM**
</dt>
<dd>

DEFINITION
</dd>
-->