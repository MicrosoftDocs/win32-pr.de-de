---
title: NLM-Schnittstellen
description: NLM-Schnittstellen
ms.assetid: 57cc2a07-4551-428c-a303-9b1a4510f225
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 322086a2860ff9bade47c9971662931f9ecada60
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471797"
---
# <a name="nlm-interfaces"></a>NLM-Schnittstellen

Im folgenden finden Sie die NLM-Schnittstellen.

| Schnittstelle                                                            | BESCHREIBUNG                                                                                                                                                                                                              |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ienumnetworkconnections**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-ienumnetworkconnections)           | Stellt einen Standardenumerator für Netzwerkverbindungen bereit. Es listet aktive, getrennte oder alle Netzwerkverbindungen innerhalb eines Netzwerks auf. Diese Schnittstelle kann von der [**iNetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) -Schnittstelle abgerufen werden. |
| [**Ienumnetworks**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-ienumnetworks)                               | Listet alle auf dem Server verfügbaren Netzwerke auf. Diese Schnittstelle kann von der [**iNetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) -Schnittstelle abgerufen werden.                                                                                         |
| [**INetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork)                                         | Stellt ein Netzwerk auf dem Server dar. Sie kann auch eine Auflistung von Netzwerkverbindungen mit einer ähnlichen Netzwerk Signatur darstellen.                                                                                          |
| [**Inetworkconnection**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkconnection)                     | Stellt eine einzelne Netzwerkverbindung dar.                                                                                                                                                                                  |
| [**Inetworkconnectioncost**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkconnectioncost)                | Dient zum Abfragen der aktuellen Netzwerkkosten und des Daten Plan Status, der einer Verbindung zugeordnet ist.                                                                                                                                    |
| [**Inetworkconnectioncostevents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkconnectioncostevents) | Wird verwendet, um eine Anwendung über Kosten-und Daten Plan Status Änderungs Ereignisse für eine Verbindung zu benachrichtigen.                                                                                                                               |
| [**Inetworkconnectionevents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkconnectionevents)         | Eine Sink-Schnittstelle, die ein Client implementiert, um Ereignisse im Zusammenhang mit Netzwerkverbindungen zu empfangen. Anwendungen, die an Ereignissen mit niedrigerer Granularität wie z. b. Authentifizierungs Änderungen interessiert sind, implementieren diese Schnittstelle.       |
| [**Inetworkcostmanager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkcostmanager)                   | Wird zum Abfragen von Computer weiten Kosten-und Daten Plan Statusinformationen verwendet, die entweder einer für die Computer weiten Internet Verbindung verwendeten Verbindung oder dem ersten Hop des Routings an ein bestimmtes Ziel in einer Verbindung zugeordnet sind. |
| [**Inetworkcostmanagerevents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkcostmanagerevents)       | Wird verwendet, um eine Anwendung über Computer weite Kosten und Daten Plan bezogene Ereignisse zu benachrichtigen.                                                                                                                                         |
| [**Inetworkevents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkevents)                             | Eine Sink-Schnittstelle, die ein Client implementiert, um netzwerkbezogene Ereignisse zu empfangen. Bei diesen APIs handelt es sich um Rückruf Funktionen, die automatisch aufgerufen werden, wenn die jeweiligen Ereignisse ausgelöst werden.                                  |
| [**Inetworklistmanager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager)                   | Stellt eine Reihe von Methoden zum Ausführen von Verwaltungsfunktionen für Netzwerk Listen bereit.                                                                                                                                                  |
| [**Inetworklistmanagerevents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanagerevents)       | Eine Sink-Schnittstelle, die ein Client implementiert, um Ereignisse im Zusammenhang mit dem Netzwerk Listen-Manager zu empfangen Anwendungen, die an größeren Ereignissen wie Internet Konnektivität interessiert sind, implementieren die-Schnittstelle.   |



 

 

 




