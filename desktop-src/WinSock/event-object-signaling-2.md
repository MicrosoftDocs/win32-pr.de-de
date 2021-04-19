---
description: Wspeventselect verhält sich genau wie wspasyncselect, mit dem Unterschied, dass anstelle einer Windows-Meldung nach dem Auftreten eines beliebigen nominierten FD \_ xxx-Netzwerk Ereignisses (z. b \_ . FD Read, FD \_ Write usw.) ein bestimmtes Ereignis Objekt festgelegt wird.
ms.assetid: 28f6eb78-1bb8-4eda-aac5-017975890502
title: Ereignis Objekt Signalisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e42854a1f4e116c8dba100025007362898d183f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346941"
---
# <a name="event-object-signaling"></a><span data-ttu-id="192dd-103">Ereignis Objekt Signalisierung</span><span class="sxs-lookup"><span data-stu-id="192dd-103">Event Object Signaling</span></span>

<span data-ttu-id="192dd-104">[**Wspeventselect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)) verhält sich genau wie [**wspasyncselect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) , mit dem Unterschied, dass anstelle einer Windows-Meldung nach dem Auftreten eines beliebigen nominierten FD \_ xxx-Netzwerk Ereignisses (z. b. FD \_ Read, FD \_ Write usw.) ein bestimmtes Ereignis Objekt festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="192dd-104">[**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)) behaves exactly like [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) except that, rather than cause a Windows message to be sent upon the occurrence of any nominated FD\_XXX network event (for example, FD\_READ, FD\_WRITE, etc.), a designated event object is set.</span></span>

<span data-ttu-id="192dd-105">Außerdem wird der Dienstanbieter daran erinnert, dass ein bestimmtes FD \_ xxx-Netzwerk Ereignis aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="192dd-105">Also, the fact that a particular FD\_XXX network event has occurred is remembered by the service provider.</span></span> <span data-ttu-id="192dd-106">Dies ist erforderlich, da das Vorkommen eines und aller nominierten Netzwerkereignisse dazu führt, dass ein einzelnes Ereignis Objekt signalisiert wird.</span><span class="sxs-lookup"><span data-stu-id="192dd-106">This is needed since the occurrence of any and all nominated network events will result in a single event object becoming signaled.</span></span> <span data-ttu-id="192dd-107">Ein Aufruf von [**wspenumnetworkevents**](/previous-versions/windows/hardware/network/ff566284(v=vs.85)) bewirkt, dass der aktuelle Inhalt des Netzwerk Ereignis Speichers in einen vom Client bereitgestellten Puffer kopiert und der Netzwerk Ereignisspeicher gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="192dd-107">A call to [**WSPEnumNetworkEvents**](/previous-versions/windows/hardware/network/ff566284(v=vs.85)) causes the current contents of the network event memory to be copied to a client-supplied buffer and the network event memory to be cleared.</span></span> <span data-ttu-id="192dd-108">Der Client kann auch ein bestimmtes Ereignis Objekt festlegen, das atomisch zusammen mit dem Netzwerk Ereignisspeicher gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="192dd-108">The client may also designate a particular event object to be cleared atomically along with the network event memory.</span></span>

 

 
