---
description: Die Funktionen WSAEventSelect und WSAEnumNetworkEvents werden bereitgestellt, um Anwendungen wie Daemons und Dienste zu unterstützen, die keine Benutzeroberfläche haben (und daher keine Windows-Handles verwenden).
ms.assetid: 4254937c-7ee6-49a3-9f30-09aebaf2265b
title: Asynchrone Benachrichtigung mit Ereignis Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d0495507eacf0960dc98f31594d7f4881d51488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862591"
---
# <a name="asynchronous-notification-using-event-objects"></a><span data-ttu-id="2cb45-103">Asynchrone Benachrichtigung mit Ereignis Objekten</span><span class="sxs-lookup"><span data-stu-id="2cb45-103">Asynchronous Notification Using Event Objects</span></span>

<span data-ttu-id="2cb45-104">Die Funktionen [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) und [**WSAEnumNetworkEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnetworkevents) werden bereitgestellt, um Anwendungen wie Daemons und Dienste zu unterstützen, die keine Benutzeroberfläche haben (und daher keine Windows-Handles verwenden).</span><span class="sxs-lookup"><span data-stu-id="2cb45-104">The [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) and [**WSAEnumNetworkEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnetworkevents) functions are provided to accommodate applications such as daemons and services that have no user interface (and hence do not use Windows handles).</span></span> <span data-ttu-id="2cb45-105">Die **WSAEventSelect** -Funktion verhält sich genau wie die [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="2cb45-105">The **WSAEventSelect** function behaves exactly like the [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) function.</span></span> <span data-ttu-id="2cb45-106">Anstatt zu bewirken, dass eine Windows-Meldung für das Vorkommen eines FD \_ xxx-Netzwerk Ereignisses gesendet wird (z. b \_ . FD Read und FD \_ Write), wird ein Anwendungs bestimmtes Ereignis Objekt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2cb45-106">However, instead of causing a Windows message to be sent on the occurrence of an FD\_XXX network event (for example, FD\_READ and FD\_WRITE), an application-designated event object is set.</span></span>

<span data-ttu-id="2cb45-107">Außerdem wird der Dienstanbieter daran erinnert, dass ein bestimmtes FD \_ xxx-Netzwerk Ereignis aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="2cb45-107">Also, the fact that a particular FD\_XXX network event has occurred is remembered by the service provider.</span></span> <span data-ttu-id="2cb45-108">Die Anwendung kann [**WSAEnumNetworkEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) aufzurufen, damit der aktuelle Inhalt des Netzwerk Ereignis Speichers in einen von der Anwendung bereitgestellten Puffer kopiert und der Netzwerk Ereignisspeicher automatisch gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="2cb45-108">The application can call [**WSAEnumNetworkEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) to have the current contents of the network event memory copied to an application-supplied buffer and to have the network event memory automatically cleared.</span></span> <span data-ttu-id="2cb45-109">Bei Bedarf kann die Anwendung auch ein bestimmtes Ereignis Objekt festlegen, das zusammen mit dem Netzwerk Ereignisspeicher gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="2cb45-109">If needed, the application can also designate a particular event object that is cleared along with the network event memory.</span></span>

 

 



