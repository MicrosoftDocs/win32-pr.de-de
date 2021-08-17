---
description: Die IP-Hilfs-API (Internet Protocol Helper) ermöglicht das Abrufen und Ändern der Netzwerkkonfigurationseinstellungen für den lokalen Computer.
ms.assetid: 4896a9f8-0486-4380-bf49-d1c9ef114acc
title: IP-Hilfsprogramm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6262543d1644fbe62858f2c90064f42d2c1348b2f3c56033813f453d33470ce3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146773"
---
# <a name="ip-helper"></a>IP-Hilfsprogramm

## <a name="purpose"></a>Zweck

Die IP-Hilfs-API (Internet Protocol Helper) ermöglicht das Abrufen und Ändern der Netzwerkkonfigurationseinstellungen für den lokalen Computer.

## <a name="where-applicable"></a>Anwendungsbereich

Die IP-Hilfs-API ist in allen Computingumgebungen anwendbar, in denen die programmgesteuerte Bearbeitung der Netzwerk- und TCP/IP-Konfiguration nützlich ist. Typische Anwendungen sind IP-Routingprotokolle und SNMP-Agents (Simple Network Management Protocol).

## <a name="developer-audience"></a>Entwicklergruppe

Die IP-Hilfs-API ist für die Verwendung durch C/C++-Programmierer konzipiert. Programmierer sollten auch mit den Netzwerkkonzepten Windows TCP/IP vertraut sein.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Die IP-Hilfs-API kann auf allen Windows verwendet werden. Nicht alle Betriebssysteme unterstützen alle Funktionen. Wenn bestimmte Implementierungen oder Funktionen von Windows Sockets 2-Plattformeinschränkungen vorhanden sind, sind sie in der Dokumentation eindeutig angegeben. Wenn eine IP-Hilfsfunktion auf einer Plattform aufgerufen wird, die die Funktion nicht unterstützt, wird ERROR \_ NOT \_ SUPPORTED zurückgegeben. Spezifischere Informationen dazu, welche Betriebssysteme eine bestimmte Funktion unterstützen, finden Sie in den Abschnitten anforderungen der Dokumentation.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                              | Beschreibung                                                                                                                                                                                                       |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Neues im IP-Hilfsfeld](what-s-new-in-ip-helper.md)<br/>  | Informationen zu neuen Features für das IP-Hilfsfeature.<br/>                                                                                                                                                             |
| [Informationen zum IP-Hilfsfeld](about-ip-helper.md)<br/>                  | Allgemeine Informationen zu Den Entwicklern zur Programmierung von IP-Hilfsprogrammierungsfunktionen.<br/>                                                                                               |
| [Verwenden des IP-Hilfsers](using-ip-helper.md)<br/>                  | Prozeduren und Programmiertechniken, die mit dem IP-Hilfsprogramm verwendet werden. Dieser Abschnitt enthält grundlegende Programmiertechniken für DAS IP-Hilfsprogramm, z. B. Erste Schritte [Mit IP-Hilfsprogramm](getting-started-with-ip-helper.md).<br/> |
| [Referenz zum IP-Hilfsprogramm](ip-helper-function-reference.md)<br/> | Referenzdokumentation für die IP-Hilfsfunktionen, -Strukturen und -Enumerationen.<br/>                                                                                                                     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Sockets 2](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[Routing- und RAS-Dienst](../rras/routing-start-page.md)
</dt> </dl>

 

