---
description: Nachdem alle gewünschten Datei Vorgänge in die Warteschlange eingereiht wurden, muss für die Warteschlange ein Commit ausgeführt werden. Dies bewirkt, dass die in die Warteschlange eingereihten Datei Vorgänge verarbeitet werden.
ms.assetid: 536f47f5-785e-4a83-a500-c769442e3e68
title: Commit für eine Warteschlange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d995f6811dbd19bba9e13f29bc119cdf2f471f74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759792"
---
# <a name="committing-a-queue"></a><span data-ttu-id="4d9c0-104">Commit für eine Warteschlange</span><span class="sxs-lookup"><span data-stu-id="4d9c0-104">Committing a Queue</span></span>

<span data-ttu-id="4d9c0-105">Nachdem alle gewünschten Datei Vorgänge in die Warteschlange eingereiht wurden, muss für die Warteschlange ein Commit ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="4d9c0-105">After all the desired file operations have been queued, the queue must be committed.</span></span> <span data-ttu-id="4d9c0-106">Dies bewirkt, dass die in die Warteschlange eingereihten Datei Vorgänge verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="4d9c0-106">This causes the enqueued file operations to be processed.</span></span>

<span data-ttu-id="4d9c0-107">Eine Datei Warteschlange kann nicht wieder verwendet werden, nachdem ein Commit ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="4d9c0-107">A file queue cannot be reused after it has been committed.</span></span> <span data-ttu-id="4d9c0-108">Die bewährte Vorgehensweise besteht darin, alle erforderlichen Datei Vorgänge für die Datei Warteschlange zu erfassen und die Warteschlange nur einmal zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="4d9c0-108">The best practice is to collect all the required file operations for the file queue and commit the queue only once.</span></span> <span data-ttu-id="4d9c0-109">Wenn eine zusätzliche Verarbeitung der Warteschlange erforderlich ist, nachdem ein Commit ausgeführt wurde, sollte das Handle für die Warteschlange geschlossen und eine neue Datei Warteschlange erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="4d9c0-109">If additional processing of the queue is required after it has been committed, the handle to the queue should be closed and a new file queue created.</span></span> <span data-ttu-id="4d9c0-110">Rufen Sie zum Übertragen der Datei Warteschlange die [**setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) -Funktion auf, und geben Sie eine Rückruf Routine an.</span><span class="sxs-lookup"><span data-stu-id="4d9c0-110">To commit the file queue, call the [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function, specifying a callback routine.</span></span> <span data-ttu-id="4d9c0-111">Die Rückruf Routine empfängt Benachrichtigungen von **setupcommitfilequeue** , wenn die Datei Vorgänge verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="4d9c0-111">The callback routine will receive notifications from **SetupCommitFileQueue** as the file operations are processed.</span></span> <span data-ttu-id="4d9c0-112">Wenn Sie die standardmäßige Warteschlangen Rückruf Routine verwenden möchten, müssen Sie zuerst den erforderlichen Kontext initialisieren, indem Sie entweder [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) oder [**setupinitdefaultqueuecallbackex**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4d9c0-112">If you want to use the default queue callback routine, you must first initialize the necessary context by calling either [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) or [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex).</span></span> <span data-ttu-id="4d9c0-113">Weitere Informationen zur Standard Warteschlangen Rückruf-Routine finden Sie unter [Standard Warteschlangen-Rückruf Routine](default-queue-callback-routine.md).</span><span class="sxs-lookup"><span data-stu-id="4d9c0-113">For more information about the default queue callback routine, see [Default Queue Callback Routine](default-queue-callback-routine.md).</span></span>

> [!Note]  
> <span data-ttu-id="4d9c0-114">[**Setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) sollte aufgerufen werden, bevor die Warteschlange geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="4d9c0-114">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) should be called before the queue is closed.</span></span> <span data-ttu-id="4d9c0-115">Alle Vorgänge, für die ein Commit ausgeführt wird, wenn [**setupclosefilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) aufgerufen wird, werden nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4d9c0-115">Any operations that are uncommitted when [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) is called will not be performed.</span></span>

 

 

 



