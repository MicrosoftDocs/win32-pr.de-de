---
description: Wenn die Standardrückruffunktion während der Warteschlangenbindung aufgerufen wird, muss der Kontext dafür mithilfe der Funktionen SetupInitDefaultQueueCallback oder SetupInitDefaultQueueCallbackEx initialisiert werden.
ms.assetid: e87f8a66-33e5-4065-98ce-2e904c115b38
title: Committen der Warteschlange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe67c19b91cc25e5107f91fbd241d96147137a38b8544568e57ea3bbbd58981a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887521"
---
# <a name="committing-the-queue"></a>Committen der Warteschlange

Wenn die Standardrückruffunktion während der Warteschlangenbindung aufgerufen wird, muss der Kontext dafür mithilfe der [**Funktionen SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) oder [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) initialisiert werden. Wenn Sie eine benutzerdefinierte Rückruffunktion verwenden, die nie die Standardrückruffunktion aufruft, ist dieser Schritt nicht erforderlich.

Nachdem die Warteschlange erstellt und die Rückruffunktion, die Warteschlangenbenachrichtigungen verarbeiten soll, initialisiert wurde, können Sie [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) aufrufen, um die Vorgänge zu commiten, die in die Warteschlange gestellt wurden.

Im folgenden Beispiel wird [**SetupCommitFileQueue verwendet,**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) um die Warteschlange mithilfe der Standardrückrufroutine zu commiten.

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

Im vorherigen Beispiel ist MyQueue die Warteschlange, für die ein Commit durchgeführt werden soll, OwnerWindow ist das Fenster, das alle Dialogfelder besitzt, die von der Standardrückrufroutine erstellt wurden. SetupDefaultQueueCallback gibt an, dass die Standardrückruffunktion verwendet wird, und *Context* ist ein Zeiger auf die Struktur, die durch den vorherigen Aufruf von [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback)zurückgegeben wurde.

 

 



