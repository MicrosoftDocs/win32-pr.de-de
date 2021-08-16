---
description: Mehrere Prozesse können über Handles für das gleiche Ereignis-, Mutex-, Semaphor- oder Timerobjekt verfügen, sodass diese Objekte für die prozessübergreifende Synchronisierung verwendet werden können.
ms.assetid: 1738e586-580f-4b74-95dc-ede300b6ac9a
title: Prozessübergreifende Synchronisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0caf4818a05d526a70a1e3257ec6f86d0279f39ce3cf05a4411e49991db6ba15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886350"
---
# <a name="interprocess-synchronization"></a>Prozessübergreifende Synchronisierung

Mehrere Prozesse können über Handles für das gleiche Ereignis-, Mutex-, Semaphor- oder Timerobjekt verfügen, sodass diese Objekte für die prozessübergreifende Synchronisierung verwendet werden können. Der Prozess, der ein -Objekt erstellt, kann das von der Erstellungsfunktion zurückgegebene Handle verwenden ([**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa), [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa), [**CreateSemaphore**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea)oder [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw)). Andere Prozesse können ein Handle für das Objekt öffnen, indem sie dessen Namen oder Vererbung oder Duplizierung verwenden. Weitere Informationen finden Sie in den folgenden Themen:

-   [Objektnamen](object-names.md)
-   [Objektvererbung](object-inheritance.md)
-   [Objektduplizierung](object-duplication.md)

 

 
