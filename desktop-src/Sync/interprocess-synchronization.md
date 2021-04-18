---
description: Mehrere Prozesse können über Handles zum gleichen Ereignis, Mutex, Semaphor oder Timer-Objekt verfügen, sodass diese Objekte verwendet werden können, um die prozessübergreifende Synchronisierung zu erreichen.
ms.assetid: 1738e586-580f-4b74-95dc-ede300b6ac9a
title: Prozessübergreifende Synchronisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7c18fb26d6a64fdc2d785d16c7bccb8b007c3f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357921"
---
# <a name="interprocess-synchronization"></a>Prozessübergreifende Synchronisierung

Mehrere Prozesse können über Handles zum gleichen Ereignis, Mutex, Semaphor oder Timer-Objekt verfügen, sodass diese Objekte verwendet werden können, um die prozessübergreifende Synchronisierung zu erreichen. Der Prozess, mit dem ein Objekt erstellt wird, kann das Handle verwenden, das von der Erstellungs Funktion ("[**kreateevent**](/windows/win32/api/synchapi/nf-synchapi-createeventa)", " [**kreatemutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa)", " [**kreatesemaphore**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea)" oder " [**kreatewaitabletimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw)") Andere Prozesse können mithilfe Ihres Namens oder durch Vererbung oder Duplizierung ein Handle für das Objekt öffnen. Weitere Informationen finden Sie unter den folgenden Themen:

-   [Objektnamen](object-names.md)
-   [Objektvererbung](object-inheritance.md)
-   [Objekt Duplizierung](object-duplication.md)

 

 
