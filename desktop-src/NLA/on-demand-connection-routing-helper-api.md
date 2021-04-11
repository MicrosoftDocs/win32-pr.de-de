---
title: API-Referenz für den bedarfsgesteuerten Verbindungs Routing
description: Die folgenden Themen enthalten Details für das Bedarfs gesteuerte Verbindungs Routing Hilfsprogramm.
ms.assetid: 39AFFD16-488E-4CA3-9161-9424F0D15948
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3049c62d7784af6430e8b93240ec79464b098043
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100806"
---
# <a name="on-demand-connection-routing-helper-api-reference"></a><span data-ttu-id="02bad-103">API-Referenz für den bedarfsgesteuerten Verbindungs Routing</span><span class="sxs-lookup"><span data-stu-id="02bad-103">On Demand Connection Routing Helper API reference</span></span>

<span data-ttu-id="02bad-104">Die folgenden Themen enthalten Details für das Bedarfs gesteuerte Verbindungs Routing Hilfsprogramm.</span><span class="sxs-lookup"><span data-stu-id="02bad-104">The following topics provide details for the On Demand Connection Routing Helper.</span></span>



| <span data-ttu-id="02bad-105">Referenz</span><span class="sxs-lookup"><span data-stu-id="02bad-105">Reference</span></span>                                                                          | <span data-ttu-id="02bad-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="02bad-106">Description</span></span>                                                                                                                                                                 |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="02bad-107">**Ondemandgetroutinghint**</span><span class="sxs-lookup"><span data-stu-id="02bad-107">**OnDemandGetRoutingHint**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-ondemandgetroutinghint)                           | <span data-ttu-id="02bad-108">Suchen Sie im Routen Anforderungs Cache nach einem Ziel, und gibt, wenn eine Übereinstimmung gefunden wird, die entsprechende Schnittstellen-ID zurück.</span><span class="sxs-lookup"><span data-stu-id="02bad-108">Look up a destination in the Route Request cache and, if a match is found, returns the corresponding Interface ID.</span></span><br/>                                               |
| [<span data-ttu-id="02bad-109">**Ondemandregisternotification**</span><span class="sxs-lookup"><span data-stu-id="02bad-109">**OnDemandRegisterNotification**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-ondemandregisternotification)               | <span data-ttu-id="02bad-110">Registrieren Sie sich, um benachrichtigt zu werden, wenn der Routen Anforderungen-Cache geändert wird.</span><span class="sxs-lookup"><span data-stu-id="02bad-110">Register to be notified when the Route Requests cache is modified.</span></span><br/>                                                                                               |
| [<span data-ttu-id="02bad-111">**Ondemandunregisternotification**</span><span class="sxs-lookup"><span data-stu-id="02bad-111">**OnDemandUnregisterNotification**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-ondemandunregisternotification)           | <span data-ttu-id="02bad-112">Heben Sie die Registrierung für Benachrichtigungen auf, und bereinigen Sie Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="02bad-112">Unregister for notifications and clean up resources.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="02bad-113">**Netzwerk \_ Schnittstellen \_ Kontext**</span><span class="sxs-lookup"><span data-stu-id="02bad-113">**NET\_INTERFACE\_CONTEXT**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context)                           | <span data-ttu-id="02bad-114">Der Schnittstellen Kontext, der Teil der [**\_ \_ Kontext \_ Tabellenstruktur der NET-Schnittstelle**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context_table) ist.</span><span class="sxs-lookup"><span data-stu-id="02bad-114">The interface context that is part of the [**NET\_INTERFACE\_CONTEXT\_TABLE**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context_table) structure.</span></span><br/>                                       |
| [<span data-ttu-id="02bad-115">**NET \_ Interface- \_ Kontext \_ Tabelle**</span><span class="sxs-lookup"><span data-stu-id="02bad-115">**NET\_INTERFACE\_CONTEXT\_TABLE**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context_table)              | <span data-ttu-id="02bad-116">Die Tabelle der [**Kontext Strukturen der NET- \_ Schnittstelle \_**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context) .</span><span class="sxs-lookup"><span data-stu-id="02bad-116">The table of [**NET\_INTERFACE\_CONTEXT**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context) structures.</span></span><br/>                                                                                |
| [<span data-ttu-id="02bad-117">**Getinterfakecontexttableforhostname**</span><span class="sxs-lookup"><span data-stu-id="02bad-117">**GetInterfaceContextTableForHostName**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-getinterfacecontexttableforhostname) | <span data-ttu-id="02bad-118">Diese Funktion Ruft eine Schnittstellen Kontext Tabelle für den angegebenen Hostnamen und Verbindungsprofil Filter ab.</span><span class="sxs-lookup"><span data-stu-id="02bad-118">This function retrieves an interface context table for the given hostname and connection profile filter.</span></span><br/>                                                         |
| [<span data-ttu-id="02bad-119">**Freumterfakecontextfähige**</span><span class="sxs-lookup"><span data-stu-id="02bad-119">**FreeInterfaceContextTable**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-freeinterfacecontexttable)                     | <span data-ttu-id="02bad-120">Diese Funktion gibt die mit der [**getinterfakecontexttableforhostname**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-getinterfacecontexttableforhostname) -Funktion abgerufene Schnittstellen Kontext Tabelle frei.</span><span class="sxs-lookup"><span data-stu-id="02bad-120">This function frees the interface context table retrieved using the [**GetInterfaceContextTableForHostName**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-getinterfacecontexttableforhostname) function.</span></span><br/> |



 

 

 





