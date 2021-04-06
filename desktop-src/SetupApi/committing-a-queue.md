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
# <a name="committing-a-queue"></a>Commit für eine Warteschlange

Nachdem alle gewünschten Datei Vorgänge in die Warteschlange eingereiht wurden, muss für die Warteschlange ein Commit ausgeführt werden. Dies bewirkt, dass die in die Warteschlange eingereihten Datei Vorgänge verarbeitet werden.

Eine Datei Warteschlange kann nicht wieder verwendet werden, nachdem ein Commit ausgeführt wurde. Die bewährte Vorgehensweise besteht darin, alle erforderlichen Datei Vorgänge für die Datei Warteschlange zu erfassen und die Warteschlange nur einmal zu übertragen. Wenn eine zusätzliche Verarbeitung der Warteschlange erforderlich ist, nachdem ein Commit ausgeführt wurde, sollte das Handle für die Warteschlange geschlossen und eine neue Datei Warteschlange erstellt werden. Rufen Sie zum Übertragen der Datei Warteschlange die [**setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) -Funktion auf, und geben Sie eine Rückruf Routine an. Die Rückruf Routine empfängt Benachrichtigungen von **setupcommitfilequeue** , wenn die Datei Vorgänge verarbeitet werden. Wenn Sie die standardmäßige Warteschlangen Rückruf Routine verwenden möchten, müssen Sie zuerst den erforderlichen Kontext initialisieren, indem Sie entweder [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) oder [**setupinitdefaultqueuecallbackex**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex)aufrufen. Weitere Informationen zur Standard Warteschlangen Rückruf-Routine finden Sie unter [Standard Warteschlangen-Rückruf Routine](default-queue-callback-routine.md).

> [!Note]  
> [**Setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) sollte aufgerufen werden, bevor die Warteschlange geschlossen wird. Alle Vorgänge, für die ein Commit ausgeführt wird, wenn [**setupclosefilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) aufgerufen wird, werden nicht ausgeführt.

 

 

 



