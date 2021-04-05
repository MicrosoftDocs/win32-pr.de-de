---
title: Auflisten registrierter Entitäten
description: Nachdem ein Client registriert wurde, kann der Client eine Liste aller anderen Clients abrufen, die beim Routing Tabellen-Manager registriert wurden. Einige Clients müssen bestimmte Vorgänge ausführen, wenn ein bestimmter Clienttyp erkannt wird.
ms.assetid: d94de573-7c1e-4179-a41f-5836d2c5d44a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ac92ccf89336d3fbca378209b9e79877d9b426a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037013"
---
# <a name="enumerating-registered-entities"></a><span data-ttu-id="90f48-104">Auflisten registrierter Entitäten</span><span class="sxs-lookup"><span data-stu-id="90f48-104">Enumerating Registered Entities</span></span>

<span data-ttu-id="90f48-105">Nachdem ein Client registriert wurde, kann der Client eine Liste aller anderen Clients abrufen, die beim Routing Tabellen-Manager registriert wurden.</span><span class="sxs-lookup"><span data-stu-id="90f48-105">After a client has registered, the client can obtain a list of all the other clients that have registered with the routing table manager.</span></span> <span data-ttu-id="90f48-106">Einige Clients müssen bestimmte Vorgänge ausführen, wenn ein bestimmter Clienttyp erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="90f48-106">Some clients must perform certain operations if the presence of a particular type of client is detected.</span></span>

<span data-ttu-id="90f48-107">Der Client kann die Funktion [**rtmgetregisteredentities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetregisteredentities) aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="90f48-107">The client can call the [**RtmGetRegisteredEntities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetregisteredentities) function.</span></span> <span data-ttu-id="90f48-108">Ein Puffer von [**RTM- \_ Entitäts \_ Informations**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) Strukturen wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="90f48-108">A buffer of [**RTM\_ENTITY\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) structures is returned.</span></span> <span data-ttu-id="90f48-109">Nachdem der Client diese Informationen verarbeitet hat, sollte der Client [**rtmreleaseentities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentities) aufgerufen werden, um die Handles in den **RTM- \_ Entitäts \_ Informations** Strukturen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="90f48-109">After the client has processed this information, the client should call [**RtmReleaseEntities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentities) to release the handles in the **RTM\_ENTITY\_INFO** structures.</span></span>

<span data-ttu-id="90f48-110">Wenn der Routing Tabellen-Manager-Client im Aufrufen von [**rtmregisterentity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity)eine Rückruffunktion bereitgestellt hat, wird der Client benachrichtigt, wenn sich andere Clients registrieren oder die Registrierung aufheben.</span><span class="sxs-lookup"><span data-stu-id="90f48-110">If the routing table manager client supplied a callback function in the call to [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity), the client is notified when any other clients register or unregister.</span></span>

<span data-ttu-id="90f48-111">Beispielcode, der die Verwendung dieser Funktionen veranschaulicht, finden Sie unter Auflisten [der registrierten Entitäten](enumerate-the-registered-entities.md) und [Verwenden des Ereignis Benachrichtigungs Rückrufs](use-the-event-notification-callback.md).</span><span class="sxs-lookup"><span data-stu-id="90f48-111">For sample code that shows how to use these functions, see [Enumerate the Registered Entities](enumerate-the-registered-entities.md) and [Use the Event Notification Callback](use-the-event-notification-callback.md).</span></span>

 

 




