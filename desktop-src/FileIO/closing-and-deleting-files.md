---
description: Um Betriebssystemressourcen effizient zu verwenden, sollte eine Anwendung Dateien schließen, wenn Sie nicht mehr benötigt werden, indem Sie die CloseHandle-Funktion verwenden. Wenn eine Datei geöffnet ist, wenn eine Anwendung beendet wird, wird Sie vom System automatisch geschlossen.
ms.assetid: 6cf9694a-00c4-4750-8822-c25a1a102fd4
title: Schließen und Löschen von Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3da31fe7ff38a1bbd1555e2685ceab9ae432574
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357019"
---
# <a name="closing-and-deleting-files"></a><span data-ttu-id="9874b-104">Schließen und Löschen von Dateien</span><span class="sxs-lookup"><span data-stu-id="9874b-104">Closing and Deleting Files</span></span>

<span data-ttu-id="9874b-105">Um Betriebssystemressourcen effizient zu verwenden, sollte eine Anwendung Dateien schließen, wenn Sie nicht mehr benötigt werden, indem Sie die [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="9874b-105">To use operating system resources efficiently, an application should close files when they are no longer needed by using the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function.</span></span> <span data-ttu-id="9874b-106">Wenn eine Datei geöffnet ist, wenn eine Anwendung beendet wird, wird Sie vom System automatisch geschlossen.</span><span class="sxs-lookup"><span data-stu-id="9874b-106">If a file is open when an application terminates, the system closes it automatically.</span></span>

<span data-ttu-id="9874b-107">Die [**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) -Funktion kann verwendet werden, um eine Datei beim Schließen zu löschen.</span><span class="sxs-lookup"><span data-stu-id="9874b-107">The [**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) function can be used to delete a file on close.</span></span> <span data-ttu-id="9874b-108">Eine Datei kann erst gelöscht werden, wenn alle Handles geschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="9874b-108">A file cannot be deleted until all handles to it are closed.</span></span> <span data-ttu-id="9874b-109">Wenn eine Datei nicht gelöscht werden kann, kann Ihr Name nicht wieder verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9874b-109">If a file cannot be deleted, its name cannot be reused.</span></span> <span data-ttu-id="9874b-110">Um einen Dateinamen sofort wiederzuverwenden, benennen Sie die vorhandene Datei um.</span><span class="sxs-lookup"><span data-stu-id="9874b-110">To reuse a file name immediately, rename the existing file.</span></span>

<span data-ttu-id="9874b-111">Wenn Sie eine geöffnete Datei oder ein Verzeichnis auf einem Remote Computer löschen, die bereits auf dem Remote Computer ohne den Berechtigungs Satz für die Lese Freigabe geöffnet wurde [**, dürfen Sie**](/windows/desktop/api/WinBase/nf-winbase-openfile) nicht die Datei oder das Verzeichnis für den Lösch [**Vorgang aufrufen.**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)</span><span class="sxs-lookup"><span data-stu-id="9874b-111">If you are deleting an open file or directory on a remote machine and it has already been opened on the remote machine without the read share permission set, do not call [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) or [**OpenFile**](/windows/desktop/api/WinBase/nf-winbase-openfile) to open the file or directory for deletion first.</span></span> <span data-ttu-id="9874b-112">Dies führt zu einer Freigabe Verletzung.</span><span class="sxs-lookup"><span data-stu-id="9874b-112">Doing so will result in a sharing violation.</span></span>

 

 
