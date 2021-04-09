---
title: SNMP-Dienst
description: Die Microsoft Windows-Implementierung des Simple Network Management Protocol (SNMP) wird verwendet, um Remote Geräte zu konfigurieren, die Netzwerkleistung zu überwachen, die Netzwerk Verwendung zu überwachen und Netzwerkfehler oder nicht geeigneten Zugriff zu erkennen. Wichtig die Microsoft Windows SNMP-API unterstützt nur Protokoll Versionen bis SNMPv2C. Spätere Versionen des Protokolls werden nicht unterstützt.
ms.assetid: fbaddb10-804b-4230-8986-717edc19a2f5
keywords:
- SNMP-SNMP
- SNMP-SNMP, Startseite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71df55c79244c0f74ef685271834adc01ca7e981
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039487"
---
# <a name="snmp-service"></a>SNMP-Dienst

\[SNMP ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen [Windows-Remoteverwaltung](/windows/desktop/WinRM/portal), bei dem es sich um die Microsoft-Implementierung von WS-man handelt.\]

## <a name="purpose"></a>Zweck

Die Microsoft Windows-Implementierung des Simple Network Management Protocol (SNMP) wird verwendet, um Remote Geräte zu konfigurieren, die Netzwerkleistung zu überwachen, die Netzwerk Verwendung zu überwachen und Netzwerkfehler oder nicht geeigneten Zugriff zu erkennen.

> [!IMPORTANT]
> Die Microsoft Windows SNMP-API unterstützt nur Protokoll Versionen bis SNMPv2C. Spätere Versionen des Protokolls werden nicht unterstützt.

 

## <a name="where-applicable"></a>Anwendungsbereich

SNMP verwendet eine verteilte Architektur, bestehend aus Verwaltungs Anwendungen und Agent-Anwendungen. Der SNMP-Dienst implementiert einen SNMP-Agent. Um die Informationen zu verwenden, die der SNMP-Dienst bereitstellt, muss mindestens ein Host vorhanden sein, auf dem eine SNMP-Verwaltungs Anwendung ausgeführt wird. Sie können SNMP-Verwaltungssoftware von Drittanbietern verwenden, oder Sie können eine eigene SNMP-Verwaltungssoftware Anwendung entwickeln. Zu diesem Zweck stehen die folgenden APIs zur Verfügung:

-   SNMP-Verwaltungs-API, eine Reihe von Funktionen, die verwendet werden können, um schnell einfache SNMP-Verwaltungssysteme zu entwickeln
-   WinSNMP-API, Version 2,0, eine Reihe von Funktionen zum Codieren, decodieren, senden und empfangen von SNMP-Nachrichten

Darüber hinaus definiert die SNMP-Erweiterungs-Agent-API die Schnittstelle zwischen dem SNMP-Dienst und den DLLs des SNMP-Erweiterungs-Agents von Drittanbietern. Die API-Funktionen des SNMP-Hilfsprogramms können zur Vereinfachung der Verarbeitung von SNMP-Nachrichten verwendet werden.

## <a name="developer-audience"></a>Entwicklergruppe

Die im vorherigen Abschnitt aufgeführten APIs sind für die Verwendung durch C/C++-Programmierer konzipiert. Eine Vertrautheit mit SNMP und SNMPv2C sowie ein funktionierendes wissen über Netzwerk-und Netzwerk Verwaltungs Konzepte sind erforderlich.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Weitere Informationen zum Betriebssystem, das für die Verwendung einer bestimmten Funktion erforderlich ist, finden Sie im Abschnitt "Anforderungen" der Referenzseite für diese Funktion.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                | BESCHREIBUNG                                                                                                                                     |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [Neues in SNMP](new-in-snmp.md)<br/>                                                            | Informationen zu Updates von SNMP.<br/>                                                                                                      |
| [Simple Network Management-Protokoll (SNMP)](simple-network-management-protocol-snmp-.md)<br/> | Informationen und API-Referenz für SNMP, einschließlich der SNMP-Verwaltungs-API, der SNMP-Erweiterungs-Agent-API und der API-Funktionen des SNMP-Hilfsprogramms<br/> |
| [WinSNMP-API](snmp-reference.md)<br/>                                                         | Informationen und API-Referenz für die Microsoft Windows SNMP-Anwendungsprogrammierschnittstelle (WinSNMP-API). <br/>                       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Dynamic Host Configuration-Protokoll (DHCP)](/previous-versions/windows/desktop/dhcp/dhcp-start-page)
</dt> <dt>

[Netzwerkverwaltung](/windows/desktop/NetMgmt/network-management)
</dt> <dt>

[Routing- und RAS-Dienst](/windows/desktop/RRAS/portal)
</dt> </dl>

 

