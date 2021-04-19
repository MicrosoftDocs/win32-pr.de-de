---
description: Wenn die Standard Warteschlangen-Rückruf Routine initialisiert und angegeben wird, wenn setupcommitfilequeue aufgerufen wird, ruft die Warteschlange intern die Standard Warteschlangen Rückruf Routine auf, und Sie müssen nichts weiter tun.
ms.assetid: a976c275-f128-490d-a544-efbfc6fd87f4
title: Aufrufen der Standard Warteschlangen-Rückruf Routine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b24449fc1fcd92d8041de6f104092f45925a495b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369859"
---
# <a name="calling-the-default-queue-callback-routine"></a><span data-ttu-id="818d1-103">Aufrufen der Standard Warteschlangen-Rückruf Routine</span><span class="sxs-lookup"><span data-stu-id="818d1-103">Calling the Default Queue Callback Routine</span></span>

<span data-ttu-id="818d1-104">Wenn die Standard Warteschlangen-Rückruf Routine initialisiert und angegeben wird, wenn [**setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) aufgerufen wird, ruft die Warteschlange intern die Standard Warteschlangen Rückruf Routine auf, und Sie müssen nichts weiter tun.</span><span class="sxs-lookup"><span data-stu-id="818d1-104">If the default queue callback routine is initialized and specified when [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) is called, the queue calls the default queue callback routine internally and you need do nothing more.</span></span>

<span data-ttu-id="818d1-105">Wenn Sie eine Filter Rückruf Routine erstellen, die auf der Standard Warteschlangen-Rückruf Routine basiert, um eine Teilmenge der Warteschlangen Benachrichtigungen zu verarbeiten, muss die Filter Rückruf Routine [**setupdefaultqueuecallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) explizit aufrufen.</span><span class="sxs-lookup"><span data-stu-id="818d1-105">If you create a filter callback routine that relies on the default queue callback routine to handle a subset of the queue notifications, your filter callback routine must call [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) explicitly.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="818d1-106">Wenn Sie [**setupdefaultqueuecallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) explizit aufrufen, müssen Sie den void-Zeiger übergeben, der entweder von [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) oder [**setupinitdefaultqueuecallbackex**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex)zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="818d1-106">When you call [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) explicitly, you must pass in the void pointer returned by either [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) or [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex).</span></span>

 

> [!Note]  
> <span data-ttu-id="818d1-107">Eine Möglichkeit besteht darin, eine Kontext Struktur für Ihre benutzerdefinierte Rückruf Routine zu erstellen, die als eines der Member den von [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) oder [**setupinitdefaultqueuecallbackex**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex)zurückgegebenen void-Zeiger enthält.</span><span class="sxs-lookup"><span data-stu-id="818d1-107">One way to do this is to create a context structure for your custom callback routine that includes as one of its members the void pointer returned by [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) or [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex).</span></span>

 

 

 



