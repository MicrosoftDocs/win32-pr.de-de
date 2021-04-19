---
description: Wenn die Standard Rückruffunktion während der Warteschlangen Verpflichtung aufgerufen wird, muss der Kontext dafür mithilfe der SetupInitDefaultQueueCallback-Funktion oder der setupinitdefaultqueuecallbackex-Funktion initialisiert werden.
ms.assetid: e87f8a66-33e5-4065-98ce-2e904c115b38
title: Committen der Warteschlange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ed721c60457a77a168218aa0294bf448889129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350275"
---
# <a name="committing-the-queue"></a><span data-ttu-id="33296-103">Committen der Warteschlange</span><span class="sxs-lookup"><span data-stu-id="33296-103">Committing the Queue</span></span>

<span data-ttu-id="33296-104">Wenn die Standard Rückruffunktion während der Warteschlangen Verpflichtung aufgerufen wird, muss der Kontext dafür mithilfe der [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) -Funktion oder der [**setupinitdefaultqueuecallbackex**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) -Funktion initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="33296-104">If the default callback function is going to be called during the queue commitment, the context for it must be initialized using the [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) or [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) functions.</span></span> <span data-ttu-id="33296-105">Wenn Sie eine benutzerdefinierte Rückruffunktion verwenden, die nie die Standard Rückruffunktion aufruft, ist dieser Schritt nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="33296-105">If you are using a custom callback function that never calls the default callback function, this step is not necessary.</span></span>

<span data-ttu-id="33296-106">Nachdem die Warteschlange erstellt wurde und die Rückruffunktion, die Warteschlangen Benachrichtigungen verarbeitet, initialisiert wurde, können Sie [**setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) aufrufen, um einen Commit für die Vorgänge durchzusetzen, die in die Warteschlange eingereiht wurden.</span><span class="sxs-lookup"><span data-stu-id="33296-106">After the queue is built and the callback function that will process queue notifications has been initialized, you can call [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) to commit the operations that have been enqueued.</span></span>

<span data-ttu-id="33296-107">Im folgenden Beispiel wird [**setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) verwendet, um mithilfe der Standard Rückruf Routine einen Commit für die Warteschlange durchzusetzen.</span><span class="sxs-lookup"><span data-stu-id="33296-107">The following example uses [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) to commit the queue using the default callback routine.</span></span>

``` syntax
test = SetupCommitFileQueue (
     OwnerWindow,          //window that will own dialog boxes
                           //created by the callback routine
     MyQueue,              //the queue to commit
  
                           //use the default callback routine
     SetupDefaultQueueCallback,  
  
     Context               //context information that will be 
                           //  used by the callback routine
);
```

<span data-ttu-id="33296-108">Im vorherigen Beispiel ist myQueue die zu Commit Ende Warteschlange, Besitzer Window das Fenster, das alle von der Standard Rückruf Routine erstellten Dialogfelder besitzt, setupdefaultqueuecallback gibt an, dass die Standard Rückruffunktion verwendet wird, und *context* ist ein Zeiger auf die Struktur, die durch den vorherigen Aufrufs von [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback)zurückgegeben</span><span class="sxs-lookup"><span data-stu-id="33296-108">In the preceding example, MyQueue is the queue to commit, OwnerWindow is the window that will own any dialog boxes created by the default callback routine, SetupDefaultQueueCallback specifies that the default callback function will be used, and *Context* is a pointer to the structure returned by the previous call to [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback).</span></span>

 

 



