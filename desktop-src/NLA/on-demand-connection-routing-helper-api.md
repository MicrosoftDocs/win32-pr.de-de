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
# <a name="on-demand-connection-routing-helper-api-reference"></a>API-Referenz für den bedarfsgesteuerten Verbindungs Routing

Die folgenden Themen enthalten Details für das Bedarfs gesteuerte Verbindungs Routing Hilfsprogramm.



| Referenz                                                                          | Beschreibung                                                                                                                                                                 |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ondemandgetroutinghint**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-ondemandgetroutinghint)                           | Suchen Sie im Routen Anforderungs Cache nach einem Ziel, und gibt, wenn eine Übereinstimmung gefunden wird, die entsprechende Schnittstellen-ID zurück.<br/>                                               |
| [**Ondemandregisternotification**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-ondemandregisternotification)               | Registrieren Sie sich, um benachrichtigt zu werden, wenn der Routen Anforderungen-Cache geändert wird.<br/>                                                                                               |
| [**Ondemandunregisternotification**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-ondemandunregisternotification)           | Heben Sie die Registrierung für Benachrichtigungen auf, und bereinigen Sie Ressourcen.<br/>                                                                                                             |
| [**Netzwerk \_ Schnittstellen \_ Kontext**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context)                           | Der Schnittstellen Kontext, der Teil der [**\_ \_ Kontext \_ Tabellenstruktur der NET-Schnittstelle**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context_table) ist.<br/>                                       |
| [**NET \_ Interface- \_ Kontext \_ Tabelle**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context_table)              | Die Tabelle der [**Kontext Strukturen der NET- \_ Schnittstelle \_**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context) .<br/>                                                                                |
| [**Getinterfakecontexttableforhostname**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-getinterfacecontexttableforhostname) | Diese Funktion Ruft eine Schnittstellen Kontext Tabelle für den angegebenen Hostnamen und Verbindungsprofil Filter ab.<br/>                                                         |
| [**Freumterfakecontextfähige**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-freeinterfacecontexttable)                     | Diese Funktion gibt die mit der [**getinterfakecontexttableforhostname**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-getinterfacecontexttableforhostname) -Funktion abgerufene Schnittstellen Kontext Tabelle frei.<br/> |



 

 

 





