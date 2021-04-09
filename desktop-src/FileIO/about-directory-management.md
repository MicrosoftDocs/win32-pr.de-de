---
description: Ein Verzeichnis, das mindestens ein Verzeichnis enthält, ist das übergeordnete Element des enthaltenen Verzeichnisses oder der Verzeichnisse, und jedes enthaltene Verzeichnis ist ein untergeordnetes Element des übergeordneten Verzeichnisses. Die hierarchische Struktur der Verzeichnisse wird als Verzeichnisstruktur bezeichnet.
ms.assetid: e8a7bf82-0f3c-4ad9-9d10-25c4d69733dc
title: Informationen zur Verzeichnis Verwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e3a90b6cc99a480f798e632512770c904291a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862659"
---
# <a name="about-directory-management"></a><span data-ttu-id="c1b15-104">Informationen zur Verzeichnis Verwaltung</span><span class="sxs-lookup"><span data-stu-id="c1b15-104">About Directory Management</span></span>

<span data-ttu-id="c1b15-105">Ein Verzeichnis, das mindestens ein Verzeichnis enthält, ist das über *geordnete* Element des enthaltenen Verzeichnisses oder der Verzeichnisse, und jedes enthaltene Verzeichnis *ist ein unter* geordnetes Element des übergeordneten Verzeichnisses.</span><span class="sxs-lookup"><span data-stu-id="c1b15-105">A directory that contains one or more directories is the *parent* of the contained directory or directories, and each contained directory is a *child* of the parent directory.</span></span> <span data-ttu-id="c1b15-106">Die hierarchische Struktur der Verzeichnisse wird als *Verzeichnis* Struktur bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="c1b15-106">The hierarchical structure of directories is referred to as a *directory tree*.</span></span>

<span data-ttu-id="c1b15-107">Das NTFS-Dateisystem implementiert die logische Verbindung zwischen einem Verzeichnis und den darin enthaltenen Dateien als *Verzeichniseintrags Tabelle*.</span><span class="sxs-lookup"><span data-stu-id="c1b15-107">The NTFS file system implements the logical link between a directory and the files it contains as a *directory entry table*.</span></span> <span data-ttu-id="c1b15-108">Wenn eine Datei in ein Verzeichnis verschoben wird, wird ein Eintrag in der Tabelle für die verschoderte Datei erstellt, und der Name der Datei wird in den Eintrag eingefügt.</span><span class="sxs-lookup"><span data-stu-id="c1b15-108">When a file is moved into a directory, an entry is created in the table for the moved file and the name of the file is placed in the entry.</span></span> <span data-ttu-id="c1b15-109">Wenn eine in einem Verzeichnis enthaltene Datei gelöscht wird, werden der Name und der Eintrag, die der gelöschten Datei entsprechen, ebenfalls aus der Tabelle gelöscht.</span><span class="sxs-lookup"><span data-stu-id="c1b15-109">When a file contained in a directory is deleted, the name and entry corresponding to the deleted file is also deleted from the table.</span></span> <span data-ttu-id="c1b15-110">In einer Verzeichniseintrags Tabelle können mehrere Einträge für eine einzelne Datei vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="c1b15-110">More than one entry for a single file can exist in a directory entry table.</span></span> <span data-ttu-id="c1b15-111">Wenn ein zusätzlicher Eintrag in der Tabelle für eine Datei erstellt wird, wird dieser Eintrag als *hardlink* zu dieser Datei bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="c1b15-111">If an additional entry is created in the table for a file, that entry is referred to as a *hard link* to that file.</span></span> <span data-ttu-id="c1b15-112">Es gibt keine Beschränkung für die Anzahl der festen Links, die für eine einzelne Datei erstellt werden können.</span><span class="sxs-lookup"><span data-stu-id="c1b15-112">There is no limit to the number of hard links that can be created for a single file.</span></span>

<span data-ttu-id="c1b15-113">Verzeichnisse können auch Verbindungen und Analyse Punkte enthalten.</span><span class="sxs-lookup"><span data-stu-id="c1b15-113">Directories can also contain junctions and reparse points.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c1b15-114">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="c1b15-114">In this section</span></span>



| <span data-ttu-id="c1b15-115">Thema</span><span class="sxs-lookup"><span data-stu-id="c1b15-115">Topic</span></span>                                                                                 | <span data-ttu-id="c1b15-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c1b15-116">Description</span></span>                                                                                            |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c1b15-117">Erstellen und Löschen von Verzeichnissen</span><span class="sxs-lookup"><span data-stu-id="c1b15-117">Creating and Deleting Directories</span></span>](creating-and-deleting-directories.md)<br/> | <span data-ttu-id="c1b15-118">Eine Anwendung kann Verzeichnisse Programm gesteuert erstellen und löschen.</span><span class="sxs-lookup"><span data-stu-id="c1b15-118">An application can programmatically create and delete directories.</span></span><br/>                          |
| [<span data-ttu-id="c1b15-119">Verzeichnis Handles</span><span class="sxs-lookup"><span data-stu-id="c1b15-119">Directory Handles</span></span>](obtaining-a-handle-to-a-directory.md)<br/>                 | <span data-ttu-id="c1b15-120">Wenn ein Prozess ein Verzeichnis Objekt erstellt oder öffnet, empfängt es ein Handle für das Objekt.</span><span class="sxs-lookup"><span data-stu-id="c1b15-120">Whenever a process creates or opens a directory object, it receives a handle to the object.</span></span><br/> |
| [<span data-ttu-id="c1b15-121">Reparse Points</span><span class="sxs-lookup"><span data-stu-id="c1b15-121">Reparse Points</span></span>](reparse-points.md)<br/>                                       | <span data-ttu-id="c1b15-122">Beschreibt Analyse Punkte.</span><span class="sxs-lookup"><span data-stu-id="c1b15-122">Describes reparse points.</span></span><br/>                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="c1b15-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c1b15-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1b15-124">Referenz zur Verzeichnis Verwaltung</span><span class="sxs-lookup"><span data-stu-id="c1b15-124">Directory Management Reference</span></span>](directory-management-reference.md)
</dt> </dl>

 

 




