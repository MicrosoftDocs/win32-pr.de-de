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
# <a name="interprocess-synchronization"></a><span data-ttu-id="e4262-103">Prozessübergreifende Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="e4262-103">Interprocess Synchronization</span></span>

<span data-ttu-id="e4262-104">Mehrere Prozesse können über Handles zum gleichen Ereignis, Mutex, Semaphor oder Timer-Objekt verfügen, sodass diese Objekte verwendet werden können, um die prozessübergreifende Synchronisierung zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="e4262-104">Multiple processes can have handles to the same event, mutex, semaphore, or timer object, so these objects can be used to accomplish interprocess synchronization.</span></span> <span data-ttu-id="e4262-105">Der Prozess, mit dem ein Objekt erstellt wird, kann das Handle verwenden, das von der Erstellungs Funktion ("[**kreateevent**](/windows/win32/api/synchapi/nf-synchapi-createeventa)", " [**kreatemutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa)", " [**kreatesemaphore**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea)" oder " [**kreatewaitabletimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw)")</span><span class="sxs-lookup"><span data-stu-id="e4262-105">The process that creates an object can use the handle returned by the creation function ([**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa), [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa), [**CreateSemaphore**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea), or [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw)).</span></span> <span data-ttu-id="e4262-106">Andere Prozesse können mithilfe Ihres Namens oder durch Vererbung oder Duplizierung ein Handle für das Objekt öffnen.</span><span class="sxs-lookup"><span data-stu-id="e4262-106">Other processes can open a handle to the object by using its name, or through inheritance or duplication.</span></span> <span data-ttu-id="e4262-107">Weitere Informationen finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="e4262-107">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="e4262-108">Objektnamen</span><span class="sxs-lookup"><span data-stu-id="e4262-108">Object Names</span></span>](object-names.md)
-   [<span data-ttu-id="e4262-109">Objektvererbung</span><span class="sxs-lookup"><span data-stu-id="e4262-109">Object Inheritance</span></span>](object-inheritance.md)
-   [<span data-ttu-id="e4262-110">Objekt Duplizierung</span><span class="sxs-lookup"><span data-stu-id="e4262-110">Object Duplication</span></span>](object-duplication.md)

 

 
