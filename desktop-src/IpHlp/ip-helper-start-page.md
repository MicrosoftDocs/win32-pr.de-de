---
description: Die IP Helper-API (Internet Protocol Helper) ermöglicht das Abrufen und Ändern von Netzwerk Konfigurationseinstellungen für den lokalen Computer.
ms.assetid: 4896a9f8-0486-4380-bf49-d1c9ef114acc
title: IP-Hilfsprogramm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1d50153e1ad890063f33a473058f6a850a9f171
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862447"
---
# <a name="ip-helper"></a>IP-Hilfsprogramm

## <a name="purpose"></a>Zweck

Die IP Helper-API (Internet Protocol Helper) ermöglicht das Abrufen und Ändern von Netzwerk Konfigurationseinstellungen für den lokalen Computer.

## <a name="where-applicable"></a>Anwendungsbereich

Die IP-hilfsprogrammapi ist in jeder Computerumgebung anwendbar, in der die programmgesteuerte Bearbeitung der Netzwerk-und TCP/IP-Konfiguration nützlich ist. Typische Anwendungen sind IP-Routing Protokolle und SNMP (Simple Network Management Protocol)-Agents.

## <a name="developer-audience"></a>Entwicklergruppe

Die IP Helper-API ist für die Verwendung durch C/C++-Programmierer konzipiert. Programmierer sollten auch mit den Konzepten von Windows-Netzwerken und TCP/IP-Netzwerken vertraut sein.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Die IP-hilfsprogrammapi kann auf allen Windows-Plattformen verwendet werden. Nicht alle Betriebssysteme unterstützen alle Funktionen. Wenn bestimmte Implementierungen oder Funktionen von Windows Sockets 2-Platt Form Einschränkungen vorhanden sind, sind Sie in der Dokumentation eindeutig angegeben. Wenn eine IP-Hilfsfunktion auf einer Plattform aufgerufen wird, die die Funktion nicht unterstützt, wird "Error \_ Not \_ supported" zurückgegeben. Spezifischere Informationen dazu, welche Betriebssysteme eine bestimmte Funktion unterstützen, finden Sie in den Abschnitten zu den Anforderungen in der-Dokumentation.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                              | BESCHREIBUNG                                                                                                                                                                                                       |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Neues in IP Helper](what-s-new-in-ip-helper.md)<br/>  | Informationen zu neuen Features für das IP-Hilfsprogramm.<br/>                                                                                                                                                             |
| [Info](about-ip-helper.md)<br/>                  | Allgemeine Informationen zu den Überlegungen und Funktionen der IP-Hilfsprogrammen für Entwickler.<br/>                                                                                               |
| [Verwenden von IP Helper](using-ip-helper.md)<br/>                  | Prozeduren und Programmiertechniken, die mit IP Helper verwendet werden. Dieser Abschnitt enthält grundlegende Programmiertechniken für IP-Hilfsprogramme, wie z. b. die ersten Schritte [mit IP Helper](getting-started-with-ip-helper.md).<br/> |
| [Referenz zum IP-Hilfsprogramm](ip-helper-function-reference.md)<br/> | Referenz Dokumentation für die IP-Hilfsobjekte, Strukturen und Enumerationen.<br/>                                                                                                                     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Sockets 2](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[Routing- und RAS-Dienst](../rras/routing-start-page.md)
</dt> </dl>

 

