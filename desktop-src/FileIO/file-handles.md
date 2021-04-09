---
description: Wenn eine Datei von einem Prozess mithilfe der Funktion "deatefile" geöffnet wird, wird ihr ein Datei Handle zugeordnet, bis der Prozess beendet oder das Handle mit der Funktion "CloseHandle" geschlossen wird.
ms.assetid: c8188e28-ec1b-4746-86f6-5996ff271677
title: Datei Handles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63a54db1935108ab18666fb460a071d77c50f793
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868244"
---
# <a name="file-handles"></a><span data-ttu-id="05a11-103">Datei Handles</span><span class="sxs-lookup"><span data-stu-id="05a11-103">File Handles</span></span>

<span data-ttu-id="05a11-104">Wenn eine Datei von einem Prozess mithilfe der Funktion " [**deatefile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) " geöffnet wird, wird ihr ein *Datei Handle* zugeordnet, bis der Prozess beendet oder das Handle mit der Funktion " [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) " geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="05a11-104">When a file is opened by a process using the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function, a *file handle* is associated with it until either the process terminates or the handle is closed using the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function.</span></span> <span data-ttu-id="05a11-105">Das Datei Handle wird verwendet, um die Datei in vielen Funktionsaufrufen zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="05a11-105">The file handle is used to identify the file in many function calls.</span></span>

<span data-ttu-id="05a11-106">Jedes Datei Handle-und Datei Objekt ist im Allgemeinen für jeden Prozess eindeutig, der eine Datei öffnet – die einzige Ausnahme ist, wenn ein Datei Handle, das von einem Prozess gehalten wird, dupliziert wird oder wenn ein untergeordneter Prozess die Datei Handles des übergeordneten Prozesses erbt.</span><span class="sxs-lookup"><span data-stu-id="05a11-106">Each file handle and file object is generally unique to each process that opens a file—the only exceptions to this are when a file handle held by a process is duplicated, or when a child process inherits the file handles of the parent process.</span></span> <span data-ttu-id="05a11-107">In diesen Fällen sind diese Datei Handles eindeutig, aber sehen Sie sich ein einzelnes, frei gegebenes Datei Objekt an.</span><span class="sxs-lookup"><span data-stu-id="05a11-107">In these situations, these file handles are unique, but see a single, shared file object.</span></span> <span data-ttu-id="05a11-108">Weitere Informationen zum Duplizieren von Datei Handles, die von Prozessen gehalten werden, finden Sie unter [**duplialisierandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="05a11-108">See [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) for more information on duplicating file handles held by processes.</span></span>

<span data-ttu-id="05a11-109">Beachten Sie Folgendes: während die Datei Handles in der Regel für einen Prozess privat sind, ist die Datei, auf die die Datei behandelt, nicht.</span><span class="sxs-lookup"><span data-stu-id="05a11-109">Note that while the file handles are typically private to a process, the file data that the file handles point to is not.</span></span> <span data-ttu-id="05a11-110">Daher müssen Prozesse und Threads, die dieselbe Datei gemeinsam verwenden, Ihren Zugriff synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="05a11-110">Therefore, processes and threads that share the same file must synchronize their access.</span></span> <span data-ttu-id="05a11-111">Bei den meisten Vorgängen in einer Datei identifiziert ein Prozess die Datei über den privaten Pool von Handles.</span><span class="sxs-lookup"><span data-stu-id="05a11-111">For most operations on a file, a process identifies the file through its private pool of handles.</span></span>

 

 
