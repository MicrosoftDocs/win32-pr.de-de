---
title: NLM-Schnittstellen
description: NLM-Schnittstellen
ms.assetid: 57cc2a07-4551-428c-a303-9b1a4510f225
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07751a3f28c713b699cf60aa391d7141b19db0fcafd3ef13437f951c944dcb04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117798507"
---
# <a name="nlm-interfaces"></a>NLM-Schnittstellen

Es folgen die NLM-Schnittstellen.

| Schnittstelle                                                            | BESCHREIBUNG                                                                                                                                                                                                              |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumNetworkConnections**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-ienumnetworkconnections)           | Stellt einen Standardenumerator für Netzwerkverbindungen bereit. Sie listet aktive, getrennte oder alle Netzwerkverbindungen innerhalb eines Netzwerks auf. Diese Schnittstelle kann über die [**INetwork-Schnittstelle**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) abgerufen werden. |
| [**IEnumNetworks**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-ienumnetworks)                               | Listet alle auf dem Server verfügbaren Netzwerke auf. Diese Schnittstelle kann über die [**INetwork-Schnittstelle**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) abgerufen werden.                                                                                         |
| [**INetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork)                                         | Stellt ein Netzwerk auf dem Server dar. Sie kann auch eine Sammlung von Netzwerkverbindungen mit einer ähnlichen Netzwerksignatur darstellen.                                                                                          |
| [**INetworkConnection**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkconnection)                     | Stellt eine einzelne Netzwerkverbindung dar.                                                                                                                                                                                  |
| [**INetworkConnectionCost**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkconnectioncost)                | Wird verwendet, um die aktuellen Netzwerkkosten und den Datenplanstatus einer Verbindung abzufragen.                                                                                                                                    |
| [**INetworkConnectionCostEvents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkconnectioncostevents) | Wird verwendet, um eine Anwendung über Ereignisse zur Änderung des Kosten- und Datenplanstatus für eine Verbindung zu benachrichtigen.                                                                                                                               |
| [**INetworkConnectionEvents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkconnectionevents)         | Eine Senkenschnittstelle, die ein Client implementiert, um Ereignisse im Zusammenhang mit Netzwerkverbindungen zu empfangen. Anwendungen, die an Ereignissen auf niedrigerer Ebene interessiert sind, z. B. Authentifizierungsänderungen, implementieren diese Schnittstelle.       |
| [**INetworkCostManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkcostmanager)                   | Wird verwendet, um computerweite Kosten- und Datenplanstatusinformationen abzufragen, die entweder einer Verbindung zugeordnet sind, die für die computerweite Internetverbindung verwendet wird, oder zum ersten Hop des Routings an ein bestimmtes Ziel auf einer Verbindung. |
| [**INetworkCostManagerEvents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkcostmanagerevents)       | Wird verwendet, um eine Anwendung über computerweite Kosten- und Datenplanereignisse zu benachrichtigen.                                                                                                                                         |
| [**INetworkEvents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkevents)                             | Eine Senkenschnittstelle, die ein Client implementiert, um netzwerkbezogene Ereignisse zu empfangen. Diese APIs sind alle Rückruffunktionen, die automatisch aufgerufen werden, wenn die entsprechenden Ereignisse ausgelöst werden.                                  |
| [**INetworkListManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager)                   | Stellt eine Reihe von Methoden zum Ausführen von Netzwerklistenverwaltungsfunktionen bereit.                                                                                                                                                  |
| [**INetworkListManagerEvents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanagerevents)       | Eine Senkenschnittstelle, die ein Client implementiert, um Ereignisse im Zusammenhang mit dem Netzwerklisten-Manager zu empfangen. Anwendungen, die an Ereignissen mit höherer Granularität wie Internetkonnektivität interessiert sind, implementieren die -Schnittstelle.   |



 

 

 




