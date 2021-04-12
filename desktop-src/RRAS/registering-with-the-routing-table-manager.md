---
title: Registrieren beim Routing Tabellen-Manager
description: Bevor ein Client auf die Routing Tabelle zugreifen kann, muss er sich zunächst mithilfe der rtmregisterentity-Funktion beim Routing Tabellen-Manager registrieren.
ms.assetid: 9bdbe138-d31b-42bb-9c51-5f1c5e8a4ca7
keywords:
- Routing Table Manager Version 2 RRAS, registrieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1ce5a1b350ec5420b3fc32a4e5a68a213a61151
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206685"
---
# <a name="registering-with-the-routing-table-manager"></a><span data-ttu-id="c8470-104">Registrieren beim Routing Tabellen-Manager</span><span class="sxs-lookup"><span data-stu-id="c8470-104">Registering with the Routing Table Manager</span></span>

<span data-ttu-id="c8470-105">Bevor ein Client auf die Routing Tabelle zugreifen kann, muss er sich zunächst mithilfe der [**rtmregisterentity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity) -Funktion beim Routing Tabellen-Manager registrieren.</span><span class="sxs-lookup"><span data-stu-id="c8470-105">Before a client can access the routing table, it first must register with the routing table manager using the [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity) function.</span></span>

<span data-ttu-id="c8470-106">Wenn ein Client registriert wird, übergibt er eine [**RTM- \_ Entitäts \_ Informations**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) Struktur an den Routing Tabellen-Manager.</span><span class="sxs-lookup"><span data-stu-id="c8470-106">When a client registers, it passes to the routing table manager an [**RTM\_ENTITY\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) structure.</span></span> <span data-ttu-id="c8470-107">Diese Struktur enthält die Informationen, mit denen ein Client, die Adressfamilie und die Instanz des Routing Tabellen-Managers, mit dem der Client registriert wird, eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="c8470-107">This structure contains the information that uniquely identifies a client, the address family, and the instance of the routing table manager with which the client is registering.</span></span> <span data-ttu-id="c8470-108">Ein Client kann auch den [**RTM- \_ Ereignis \_ Rückruf**](/windows/win32/api/rtmv2/nc-rtmv2-_event_callback) Rückruf einrichten.</span><span class="sxs-lookup"><span data-stu-id="c8470-108">A client can also establish the [**RTM\_EVENT\_CALLBACK**](/windows/win32/api/rtmv2/nc-rtmv2-_event_callback) callback.</span></span> <span data-ttu-id="c8470-109">Der Routing Tabellen-Manager verwendet diesen Rückruf, um den Client über Ereignisse wie Änderungs Benachrichtigungen und Client Registrierungen zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="c8470-109">The routing table manager will use this callback to notify the client of events such as change notifications and client registrations.</span></span>

<span data-ttu-id="c8470-110">Der Routing Tabellen-Manager schließt die Registrierungs Verarbeitung ab und gibt ein Handle an den Client zurück.</span><span class="sxs-lookup"><span data-stu-id="c8470-110">The routing table manager completes its registration processing and returns a handle to the client.</span></span> <span data-ttu-id="c8470-111">Der Client muss dieses Handle für alle nachfolgenden Aufrufe von RTMv2-Funktionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="c8470-111">The client must use this handle for all subsequent calls to RTMv2 functions.</span></span>

<span data-ttu-id="c8470-112">Die in RTMv2 verwendete [**rtmregisterentity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity) -Funktion ist analog zur [**rtmregisterclient**](rtmregisterclient.md) -Funktion, die in RTMv1 verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c8470-112">The [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity) function that is used in RTMv2 is analogous to the [**RtmRegisterClient**](rtmregisterclient.md) function that is used in RTMv1.</span></span> <span data-ttu-id="c8470-113">Die **rtmregisterclient** -Funktion ist veraltet, außer bei Clients, die IPX verwenden.</span><span class="sxs-lookup"><span data-stu-id="c8470-113">The **RtmRegisterClient** function is obsolete, except for clients using IPX.</span></span>

<span data-ttu-id="c8470-114">Nachdem die Interaktion eines Clients mit dem Routing Tabellen-Manager abgeschlossen ist, muss er [**rtmderegisterentity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterentity)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c8470-114">Once a client has finished interacting with the routing table manager, it must call [**RtmDeregisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterentity).</span></span> <span data-ttu-id="c8470-115">Der Routing Tabellen-Manager zerstört das Handle, das dem Client zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c8470-115">The routing table manager destroys the handle associated with the client.</span></span> <span data-ttu-id="c8470-116">Um Speicher Verluste zu vermeiden, muss der Client sicherstellen, dass alle Handles freigegeben werden und alle Routen und nächsten Hops gelöscht werden, die er besitzt, bevor **rtmderegisterentity** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c8470-116">To avoid memory leaks, the client must ensure that it releases all handles and deletes all the routes and next hops that it owns before calling **RtmDeregisterEntity**.</span></span>

<span data-ttu-id="c8470-117">Beispielcode, der die Verwendung dieser Funktionen veranschaulicht, finden Sie unter [registrieren beim Routing Tabellen-Manager](register-with-the-routing-table-manager.md) und [Verwenden des Ereignis Benachrichtigungs Rückrufs](use-the-event-notification-callback.md).</span><span class="sxs-lookup"><span data-stu-id="c8470-117">For sample code that shows how to use these functions, see [Register with the Routing Table Manager](register-with-the-routing-table-manager.md) and [Use the Event Notification Callback](use-the-event-notification-callback.md).</span></span>

 

 




