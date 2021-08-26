---
title: SNMP-Dienst
description: Die Microsoft Windows Implementierung des Simple Network Management Protocol (SNMP) wird verwendet, um Remotegeräte zu konfigurieren, die Netzwerkleistung zu überwachen, die Netzwerkauslastung zu überwachen und Netzwerkfehler oder ungeeigneten Zugriff zu erkennen. Wichtig Die Microsoft Windows SNMP-API unterstützt nur Protokollversionen bis zu SNMPv2C. Spätere Versionen des Protokolls werden nicht unterstützt.
ms.assetid: fbaddb10-804b-4230-8986-717edc19a2f5
keywords:
- SNMP SNMP
- SNMP SNMP , Startseite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dfb56450edbb6d5f18daa635e30e08e5914eb48fefb28013a66276dbc9a0a05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886390"
---
# <a name="snmp-service"></a>SNMP-Dienst

\[SNMP ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen [Windows Remoteverwaltung](/windows/desktop/WinRM/portal), bei dem es sich um die Microsoft-Implementierung von WS-Man handelt.\]

## <a name="purpose"></a>Zweck

Die Microsoft Windows Implementierung des Simple Network Management Protocol (SNMP) wird verwendet, um Remotegeräte zu konfigurieren, die Netzwerkleistung zu überwachen, die Netzwerknutzung zu überwachen und Netzwerkfehler oder ungeeigneten Zugriff zu erkennen.

> [!IMPORTANT]
> Die Microsoft Windows SNMP-API unterstützt nur Protokollversionen bis zu SNMPv2C. Spätere Versionen des Protokolls werden nicht unterstützt.

 

## <a name="where-applicable"></a>Anwendungsbereich

SNMP verwendet eine verteilte Architektur, die aus Verwaltungsanwendungen und Agent-Anwendungen besteht. Der SNMP-Dienst implementiert einen SNMP-Agent. Um die vom SNMP-Dienst bereitstellten Informationen verwenden zu können, benötigen Sie mindestens einen Host, auf dem eine SNMP-Verwaltungsanwendung ausgeführt wird. Sie können SNMP-Verwaltungssoftware von Drittanbietern verwenden oder Eine eigene SNMP-Verwaltungssoftwareanwendung entwickeln. Zu diesem Zweck sind die folgenden APIs verfügbar:

-   SNMP Verwaltungs-API, eine Reihe von Funktionen, die verwendet werden können, um schnell grundlegende SNMP-Verwaltungssysteme zu entwickeln.
-   WinSNMP-API, Version 2.0, eine Reihe von Funktionen zum Codieren, Decodieren, Senden und Empfangen von SNMP-Nachrichten

Darüber hinaus definiert die API für den SNMP-Erweiterungs-Agent die Schnittstelle zwischen dem SNMP-Dienst und den DLLs des SNMP-Erweiterungs-Agents von Drittanbietern. Die Funktionen der SNMP-Hilfsprogramm-API können verwendet werden, um die Verarbeitung von SNMP-Nachrichten zu vereinfachen.

## <a name="developer-audience"></a>Entwicklergruppe

Die im vorherigen Abschnitt aufgeführten APIs sind für die Verwendung durch C/C++-Programmierer konzipiert. Kenntnisse im Umgang mit SNMP und SNMPv2C sowie kenntnisse über Netzwerk- und Netzwerkverwaltungskonzepte sind erforderlich.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Weitere Informationen zum Betriebssystem, das für die Verwendung einer bestimmten Funktion erforderlich ist, finden Sie im Abschnitt Anforderungen der Referenzseite für diese Funktion.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                | BESCHREIBUNG                                                                                                                                     |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [Neu in SNMP](new-in-snmp.md)<br/>                                                            | Informationen zu SNMP-Updates.<br/>                                                                                                      |
| [Simple Network Management-Protokoll (SNMP)](simple-network-management-protocol-snmp-.md)<br/> | Informationen und API-Referenz für SNMP, einschließlich der Funktionen SNMP Verwaltungs-API, SNMP-Erweiterungs-Agent-API und SNMP-Hilfsprogramm-API.<br/> |
| [WinSNMP-API](snmp-reference.md)<br/>                                                         | Informationen und API-Referenz für die Microsoft Windows SNMP-Anwendungsprogrammierschnittstelle (WinSNMP-API). <br/>                       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Dynamic Host Configuration-Protokoll (DHCP)](/previous-versions/windows/desktop/dhcp/dhcp-start-page)
</dt> <dt>

[Netzwerkverwaltung](/windows/desktop/NetMgmt/network-management)
</dt> <dt>

[Routing- und RAS-Dienst](/windows/desktop/RRAS/portal)
</dt> </dl>

 

