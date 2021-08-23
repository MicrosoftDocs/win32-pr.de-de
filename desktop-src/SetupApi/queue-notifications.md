---
description: Nachdem für eine Warteschlange ein Committed durch Aufrufen von SetupCommitFileQueue erstellt wurde, beginnt sie mit der Verarbeitung der vorgänge in der Warteschlange. Bei jedem Schritt sendet die Warteschlange eine Benachrichtigung an die Rückrufroutine, die im Aufruf von SetupCommitFileQueue angegeben ist.
ms.assetid: 866e1066-b6e0-43d3-8af4-bd37fbc024e2
title: Warteschlangenbenachrichtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06858eeb5c6e9abe200792f83edcc83503270ed2706450d35ef36d5dddc80d06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665490"
---
# <a name="queue-notifications"></a>Warteschlangenbenachrichtigungen

Nachdem für eine Warteschlange ein Committed durch Aufrufen von [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)erstellt wurde, beginnt sie mit der Verarbeitung der vorgänge in der Warteschlange. Bei jedem Schritt sendet die Warteschlange eine Benachrichtigung an die Rückrufroutine, die im Aufruf von **SetupCommitFileQueue angegeben ist.**

Die folgende Syntax verwendet [**SetupCommitFileQueue,**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) um eine Benachrichtigung an die Rückrufroutine zu senden.

``` syntax
MsgHandler(          //the specified callback routine
    Context,         //context used by the callback routine
    Notification,    //queue notification code
    Param1,          //additional notification information
    Param2               //additional notification information
);
```

Die Werte *von Param1 und* *Param2* enthalten zusätzliche Informationen, die für die Benachrichtigung relevant sind, die an die Rückrufroutine gesendet wird. Jede Benachrichtigung, ihre *Param1-* und *Param2-Werte* sowie die Art und Weise, wie die Standardmäßige Warteschlangenrückrufroutine diese Benachrichtigung behandelt, wird unter [Dateiwarteschlangenbenachrichtigungen ausführlich beschrieben.](file-queue-notifications.md)

 

 



