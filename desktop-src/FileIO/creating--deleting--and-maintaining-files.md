---
description: Funktionen, die verwendet werden, um Dateien zu erstellen, zu löschen und zu verwalten.
ms.assetid: b9cf0ddf-efda-4997-bcc3-3056026c1264
title: Erstellen, löschen und warten von Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 921388e84ac44a42e0c24880b1b56971ba84c12b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352309"
---
# <a name="creating-deleting-and-maintaining-files"></a><span data-ttu-id="11701-103">Erstellen, löschen und warten von Dateien</span><span class="sxs-lookup"><span data-stu-id="11701-103">Creating, Deleting, and Maintaining Files</span></span>

<span data-ttu-id="11701-104">In den folgenden Themen wird beschrieben, wie Dateien erstellt, gelöscht und gewartet werden.</span><span class="sxs-lookup"><span data-stu-id="11701-104">The following topics describe how to create, delete, and maintain files.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="11701-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="11701-105">In this section</span></span>



| <span data-ttu-id="11701-106">Thema</span><span class="sxs-lookup"><span data-stu-id="11701-106">Topic</span></span>                                                                   | <span data-ttu-id="11701-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="11701-107">Description</span></span>                                                                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="11701-108">Benennen von Dateien, Pfaden und Namespaces</span><span class="sxs-lookup"><span data-stu-id="11701-108">Naming Files, Paths, and Namespaces</span></span>](naming-a-file.md)<br/>     | <span data-ttu-id="11701-109">Regeln, Konventionen und Einschränkungen von Namen für Dateien und Verzeichnisse, einschließlich Benennungs Konventionen, kurzen Dateinamen im Vergleich zu langen Dateinamen, voll qualifizierten Pfaden im Vergleich zu relativen Pfaden, Einschränkung der maximalen Pfad Länge, 8,3-Dateinamen und Namespaces.</span><span class="sxs-lookup"><span data-stu-id="11701-109">Rules, conventions, and limitations of names for files and directories, including naming conventions, short file names vs. long file names, fully qualified paths vs. relative paths, maximum path length limitation, 8.3 file names, and namespaces.</span></span><br/>            |
| [<span data-ttu-id="11701-110">Erstellen und Öffnen von Dateien</span><span class="sxs-lookup"><span data-stu-id="11701-110">Creating and Opening Files</span></span>](creating-and-opening-files.md)<br/> | <span data-ttu-id="11701-111">Überlegungen zum Erstellen oder öffnen [**einer Datei mithilfe der Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) "Funktion".</span><span class="sxs-lookup"><span data-stu-id="11701-111">Considerations for creating or opening a file by using the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="11701-112">Verschieben und Ersetzen von Dateien</span><span class="sxs-lookup"><span data-stu-id="11701-112">Moving and Replacing Files</span></span>](moving-and-replacing-files.md)<br/> | <span data-ttu-id="11701-113">Überlegungen zum Verschieben und Ersetzen von Dateien mithilfe der CopyFileEx-, der-Funktion, der ReplaceFile-Funktion und der-Funktion von "muvefileex".</span><span class="sxs-lookup"><span data-stu-id="11701-113">Considerations for moving and replacing files by using the CopyFileEx, CreateFile, Replacefile, and MoveFileEx functions.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="11701-114">Schließen und Löschen von Dateien</span><span class="sxs-lookup"><span data-stu-id="11701-114">Closing and Deleting Files</span></span>](closing-and-deleting-files.md)<br/> | <span data-ttu-id="11701-115">Um Betriebssystemressourcen effizient zu verwenden, sollte eine Anwendung Dateien schließen, wenn Sie nicht mehr benötigt werden, indem Sie die [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="11701-115">To use operating system resources efficiently, an application should close files when they are no longer needed by using the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function.</span></span> <span data-ttu-id="11701-116">Wenn eine Datei geöffnet ist, wenn eine Anwendung beendet wird, wird Sie vom System automatisch geschlossen.</span><span class="sxs-lookup"><span data-stu-id="11701-116">If a file is open when an application terminates, the system closes it automatically.</span></span><br/> |
| [<span data-ttu-id="11701-117">Defragmentieren von Dateien</span><span class="sxs-lookup"><span data-stu-id="11701-117">Defragmenting Files</span></span>](defragmenting-files.md)<br/>               | <span data-ttu-id="11701-118">*Defragmentierung* ist der Prozess, bei dem Teile von Dateien auf einem Datenträger verschoben werden, um Dateien zu defragmentieren, d. h. der Prozess des Verschiebens von Datei Clustern auf einem Datenträger, um Sie zusammenhängend zu machen.</span><span class="sxs-lookup"><span data-stu-id="11701-118">*Defragmentation* is the process of moving portions of files around on a disk to defragment files, that is, the process of moving file clusters on a disk to make them contiguous.</span></span><br/>                                                                               |



 

 

