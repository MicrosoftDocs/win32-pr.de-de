---
description: Nachdem ein Commit für eine Warteschlange durch Aufrufen von setupcommitfilequeue ausgeführt wurde, beginnt die Verarbeitung der in der Warteschlange befindlichen Vorgänge. Bei jedem Schritt sendet die Warteschlange eine Benachrichtigung an die Rückruf Routine, die im Aufrufen von setupcommitfilequeue angegeben ist.
ms.assetid: 866e1066-b6e0-43d3-8af4-bd37fbc024e2
title: Warteschlangen Benachrichtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 842a3ebc82640789fdb6e730e881d6790a0d642b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356953"
---
# <a name="queue-notifications"></a><span data-ttu-id="e0ee3-104">Warteschlangen Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="e0ee3-104">Queue Notifications</span></span>

<span data-ttu-id="e0ee3-105">Nachdem ein Commit für eine Warteschlange durch Aufrufen von [**setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)ausgeführt wurde, beginnt die Verarbeitung der in der Warteschlange befindlichen Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="e0ee3-105">After a queue is committed by calling [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), it will begin to process the queued operations.</span></span> <span data-ttu-id="e0ee3-106">Bei jedem Schritt sendet die Warteschlange eine Benachrichtigung an die Rückruf Routine, die im Aufrufen von **setupcommitfilequeue** angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="e0ee3-106">At each step, the queue sends a notification to the callback routine specified in the call to **SetupCommitFileQueue**.</span></span>

<span data-ttu-id="e0ee3-107">Im folgenden finden Sie die Syntax, die von [**setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) verwendet wird, um eine Benachrichtigung an die Rückruf Routine zu senden.</span><span class="sxs-lookup"><span data-stu-id="e0ee3-107">Following is the syntax that [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) uses to send a notification to the callback routine.</span></span>

``` syntax
MsgHandler(          //the specified callback routine
    Context,         //context used by the callback routine
    Notification,    //queue notification code
    Param1,          //additional notification information
    Param2               //additional notification information
);
```

<span data-ttu-id="e0ee3-108">Die Werte von *param1* und *Param2* enthalten zusätzliche Informationen, die für die Benachrichtigung relevant sind, die an die Rückruf Routine gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="e0ee3-108">The values of *Param1* and *Param2* contain additional information relevant to the notification being sent to the callback routine.</span></span> <span data-ttu-id="e0ee3-109">Jede Benachrichtigung, Ihre *param1* -und *Param2* -Werte und die Art und Weise, wie die Standard Warteschlangen-Rückruf Routine diese Benachrichtigung verarbeitet, wird in [Datei Warteschlangen Benachrichtigungen](file-queue-notifications.md)ausführlich beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e0ee3-109">Each notification, its *Param1* and *Param2* values, and how the default queue callback routine handles that notification, is described in detail in [File Queue Notifications](file-queue-notifications.md).</span></span>

 

 



