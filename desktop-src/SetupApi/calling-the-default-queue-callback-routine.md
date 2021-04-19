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
# <a name="calling-the-default-queue-callback-routine"></a>Aufrufen der Standard Warteschlangen-Rückruf Routine

Wenn die Standard Warteschlangen-Rückruf Routine initialisiert und angegeben wird, wenn [**setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) aufgerufen wird, ruft die Warteschlange intern die Standard Warteschlangen Rückruf Routine auf, und Sie müssen nichts weiter tun.

Wenn Sie eine Filter Rückruf Routine erstellen, die auf der Standard Warteschlangen-Rückruf Routine basiert, um eine Teilmenge der Warteschlangen Benachrichtigungen zu verarbeiten, muss die Filter Rückruf Routine [**setupdefaultqueuecallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) explizit aufrufen.

> [!IMPORTANT]
> Wenn Sie [**setupdefaultqueuecallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) explizit aufrufen, müssen Sie den void-Zeiger übergeben, der entweder von [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) oder [**setupinitdefaultqueuecallbackex**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex)zurückgegeben wurde.

 

> [!Note]  
> Eine Möglichkeit besteht darin, eine Kontext Struktur für Ihre benutzerdefinierte Rückruf Routine zu erstellen, die als eines der Member den von [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) oder [**setupinitdefaultqueuecallbackex**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex)zurückgegebenen void-Zeiger enthält.

 

 

 



