---
description: Nachdem die Warteschlange den Commit für Ihre Vorgänge abgeschlossen hat, sollte Sie mithilfe der Funktion setupclosefilequeue mit dem Handle geschlossen werden, das von setupopenfilequeue erstellt wurde.
ms.assetid: 4cb21699-e476-4832-9678-2bf36f3bda08
title: Schließen der Datei Warteschlange und der INF-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35b4005e3ce9d084d759612d70cd9fd256fe9ba4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106361708"
---
# <a name="closing-the-file-queue-and-inf-file"></a><span data-ttu-id="5f0f8-103">Schließen der Datei Warteschlange und der INF-Datei</span><span class="sxs-lookup"><span data-stu-id="5f0f8-103">Closing the File Queue and INF File</span></span>

<span data-ttu-id="5f0f8-104">Nachdem die Warteschlange den Commit für Ihre Vorgänge abgeschlossen hat, sollte Sie mithilfe der Funktion [**setupclosefilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) mit dem Handle geschlossen werden, das von [**setupopenfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="5f0f8-104">After the queue has finished committing its operations, it should be closed using the [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) function with the handle that was created by [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue).</span></span> <span data-ttu-id="5f0f8-105">Der Standard Warteschlangen Rückruf muss zerstört und neu erstellt werden, bevor ein Commit für eine andere Warteschlange ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="5f0f8-105">The default queue callback must be destroyed and recreated before another queue can be committed.</span></span>

<span data-ttu-id="5f0f8-106">Wenn ein Standardkontext für die Verwendung durch die standardmäßige Rückruf Routine initiiert wurde, sollte Sie auch durch Aufrufen der [**setuptermdefaultqueuecallback**](/windows/desktop/api/Setupapi/nf-setupapi-setuptermdefaultqueuecallback) -Funktion beendet werden.</span><span class="sxs-lookup"><span data-stu-id="5f0f8-106">If a default context was initiated for use by the default callback routine, it should also be terminated by calling the [**SetupTermDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setuptermdefaultqueuecallback) function.</span></span> <span data-ttu-id="5f0f8-107">Der *Kontext* ist ein Zeiger auf die-Struktur, die von der [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) -Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5f0f8-107">The *Context* is a pointer to the structure returned by the [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) function.</span></span>

<span data-ttu-id="5f0f8-108">Wenn der Zugriff auf die INF-Informationen nicht mehr benötigt wird, rufen Sie die Funktion [**setupcloseinffile**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile) mit dem Handle auf, das von [**setupopenfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) erstellt wurde, um Systemressourcen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="5f0f8-108">When access to the INF information is no longer needed, call the [**SetupCloseInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile) function with the handle that was created by [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) to free system resources.</span></span>

 

 



