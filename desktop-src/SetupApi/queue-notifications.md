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
# <a name="queue-notifications"></a>Warteschlangen Benachrichtigungen

Nachdem ein Commit für eine Warteschlange durch Aufrufen von [**setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)ausgeführt wurde, beginnt die Verarbeitung der in der Warteschlange befindlichen Vorgänge. Bei jedem Schritt sendet die Warteschlange eine Benachrichtigung an die Rückruf Routine, die im Aufrufen von **setupcommitfilequeue** angegeben ist.

Im folgenden finden Sie die Syntax, die von [**setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) verwendet wird, um eine Benachrichtigung an die Rückruf Routine zu senden.

``` syntax
MsgHandler(          //the specified callback routine
    Context,         //context used by the callback routine
    Notification,    //queue notification code
    Param1,          //additional notification information
    Param2               //additional notification information
);
```

Die Werte von *param1* und *Param2* enthalten zusätzliche Informationen, die für die Benachrichtigung relevant sind, die an die Rückruf Routine gesendet wird. Jede Benachrichtigung, Ihre *param1* -und *Param2* -Werte und die Art und Weise, wie die Standard Warteschlangen-Rückruf Routine diese Benachrichtigung verarbeitet, wird in [Datei Warteschlangen Benachrichtigungen](file-queue-notifications.md)ausführlich beschrieben.

 

 



