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
# <a name="committing-the-queue"></a>Committen der Warteschlange

Wenn die Standard Rückruffunktion während der Warteschlangen Verpflichtung aufgerufen wird, muss der Kontext dafür mithilfe der [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) -Funktion oder der [**setupinitdefaultqueuecallbackex**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) -Funktion initialisiert werden. Wenn Sie eine benutzerdefinierte Rückruffunktion verwenden, die nie die Standard Rückruffunktion aufruft, ist dieser Schritt nicht erforderlich.

Nachdem die Warteschlange erstellt wurde und die Rückruffunktion, die Warteschlangen Benachrichtigungen verarbeitet, initialisiert wurde, können Sie [**setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) aufrufen, um einen Commit für die Vorgänge durchzusetzen, die in die Warteschlange eingereiht wurden.

Im folgenden Beispiel wird [**setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) verwendet, um mithilfe der Standard Rückruf Routine einen Commit für die Warteschlange durchzusetzen.

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

Im vorherigen Beispiel ist myQueue die zu Commit Ende Warteschlange, Besitzer Window das Fenster, das alle von der Standard Rückruf Routine erstellten Dialogfelder besitzt, setupdefaultqueuecallback gibt an, dass die Standard Rückruffunktion verwendet wird, und *context* ist ein Zeiger auf die Struktur, die durch den vorherigen Aufrufs von [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback)zurückgegeben

 

 



