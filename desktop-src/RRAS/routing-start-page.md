---
title: Routing
description: Die Routing-APIs ermöglichen das Erstellen von Anwendungen, um die Routing Funktionen des Betriebssystems zu verwalten.
ms.assetid: 66e1bbb4-73c8-40fc-9575-ffe76d4b697b
keywords:
- Routing-RAS
- Routing-RAS, Startseite
- RRAS-RAS
- RRAS-RAS, siehe Routing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40e3b2a92a6c54f47693d657315ec0a48e660061
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858442"
---
# <a name="routing"></a>Routing

## <a name="purpose"></a>Zweck

Die Routing-APIs ermöglichen das Erstellen von Anwendungen, um die Routing Funktionen des Betriebssystems zu verwalten.

## <a name="where-applicable"></a>Anwendungsbereich

Das Routing ermöglicht es, dass ein Computer als Netzwerk Router fungiert.

## <a name="developer-audience"></a>Entwicklergruppe

Die Routing-APIs sind für die Verwendung durch C/C++-Programmierer konzipiert. Programmierer sollten auch mit den Netzwerk Konzepten vertraut sein.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Das Routing ist eine serverbasierte Technologie. Die gesamte Funktionalität des Routings ist in Windows 2000 Server und Windows Server 2003 integriert. Routing Anwendungen können nicht auf Windows NT-Arbeitsstationen 4,0 oder Client Betriebssystemen (z. b. Windows 95) ausgeführt werden. Spezifischere Informationen dazu, welche Betriebssysteme eine bestimmte Funktion unterstützen, finden Sie in den Abschnitten zu den Anforderungen in der-Dokumentation.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                               | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Routerverwaltung](about-router-management.md)<br/>                                         | Mithilfe der routerverwaltungs-API können Entwickler Anwendungen erstellen, um den Routerdienst auf einem Computer zu verwalten, auf dem Windows 2000 Server und spätere Betriebssysteme ausgeführt werden.<br/>                                                                                                                                                     |
| [Routermanager und Verwaltungs Informationsbasis](/windows/desktop/RRAS/about-router-management-with-mib)<br/> | Die MIB-APIs (Management Information Base) für die Routerverwaltung ermöglichen es, die Werte von MIB-Variablen abzufragen und festzulegen, die von einem der routermanager oder einem der Routing Protokolle exportiert werden, die der routermanager-Dienst verwendet. Wenn Sie diese API verwenden, unterstützt der Router das Simple Network Management-Protokoll (SNMP).<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Funktionen des IP-Hilfsprogramms](../iphlp/ip-helper-start-page.md)
</dt> <dt>

[Remotezugriff](remote-access-start-page.md)
</dt> <dt>

[Routing Protokolle](routing-protocols-start-page.md)
</dt> </dl>

 

