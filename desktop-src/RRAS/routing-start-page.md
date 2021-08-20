---
title: Routing
description: Die Routing-APIs ermöglichen das Erstellen von Anwendungen zum Verwalten der Routingfunktionen des Betriebssystems.
ms.assetid: 66e1bbb4-73c8-40fc-9575-ffe76d4b697b
keywords:
- Routing-RAS
- Routing-RAS, Startseite
- RRAS RAS
- RRAS RAS , siehe Routing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe5745af9d7c4cc3da5fbe50e745506a54cfc629ebbbe3cff6aa021d8ea14acc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672510"
---
# <a name="routing"></a>Routing

## <a name="purpose"></a>Zweck

Die Routing-APIs ermöglichen das Erstellen von Anwendungen zum Verwalten der Routingfunktionen des Betriebssystems.

## <a name="where-applicable"></a>Anwendungsbereich

Das Routing ermöglicht es einem Computer, als Netzwerkrouter zu fungieren.

## <a name="developer-audience"></a>Entwicklergruppe

Die Routing-APIs sind für die Verwendung durch C/C++-Programmierer konzipiert. Programmierer sollten auch mit Netzwerkkonzepten vertraut sein.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Routing ist eine serverbasierte Technologie. Alle Funktionen des Routings sind in Windows Server 2000 und Windows Server 2003 integriert. Routinganwendungen können nicht auf Windows NT Workstation 4.0 oder auf Clientbetriebssystemen wie Windows 95 ausgeführt werden. Ausführlichere Informationen dazu, welche Betriebssysteme eine bestimmte Funktion unterstützen, finden Sie in den Abschnitten zu Anforderungen in der Dokumentation.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                               | Beschreibung                                                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Routerverwaltung](about-router-management.md)<br/>                                         | Mit der Routerverwaltungs-API können Entwickler Anwendungen erstellen, um den Routerdienst auf einem Computer zu verwalten, auf dem Windows Server 2000 server und höher ausgeführt wird.<br/>                                                                                                                                                     |
| [Router-Manager und Verwaltungsinformationsbasis](/windows/desktop/RRAS/about-router-management-with-mib)<br/> | Die MIB-APIs (Management Information Base) für die Routerverwaltung ermöglichen das Abfragen und Festlegen der Werte von MIB-Variablen, die von einem der Router-Manager oder einem der Routingprotokolle exportiert werden, die vom Router-Manager-Dienst verwendet werden. Mit dieser API unterstützt der Router das Simple Network Management Protocol (SNMP).<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Funktionen des IP-Hilfsprogramms](../iphlp/ip-helper-start-page.md)
</dt> <dt>

[Remotezugriff](remote-access-start-page.md)
</dt> <dt>

[Routingprotokolle](routing-protocols-start-page.md)
</dt> </dl>

 

