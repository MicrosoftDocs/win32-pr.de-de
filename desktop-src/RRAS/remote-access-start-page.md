---
title: Remotezugriff
description: Verwenden Sie RAS (Remote Access Service), um Client Anwendungen zu erstellen.
ms.assetid: 4e6c04d4-f989-4248-901f-ec15f61582da
keywords:
- RAS-Dienst RAS
- RAS-RAS
- RAS-Dienst-RAS, Startseite
- RAS-RAS, siehe Remote Zugriff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95a4b1c06656b51395c8c4fc666e59d6115bd839
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104101298"
---
# <a name="remote-access"></a>Remotezugriff

## <a name="purpose"></a>Zweck

Verwenden Sie RAS (Remote Access Service), um Client Anwendungen zu erstellen. Diese Anwendungen zeigen allgemeine RAS-Dialogfelder an, verwalten RAS-Verbindungen und-Geräte und bearbeiten Telefonbucheinträge. RAS bietet auch die nächste Generation von Serverfunktionen für den RAS-Dienst (RAS) für Windows. Die RRAS-Server Funktion folgt und baut auf dem RAS-Dienst (Remote Access Service) auf.

## <a name="where-applicable"></a>Anwendungsbereich

Der RAS-Dienst ist in jeder Computerumgebung anwendbar, in der eine WAN-Verbindung (Wide Area Network) oder ein virtuelles privates Netzwerk (VPN) verwendet wird. RAS ermöglicht das Herstellen einer Verbindung zwischen einem Remote Client Computer und einem Netzwerkserver über eine WAN-Verbindung oder ein VPN. Der Remote Computer fungiert dann im LAN des Servers, als wäre der Remote Computer direkt mit dem LAN verbunden. Mithilfe der RAS-API können Programmierer Programm gesteuert auf die Features von RAS zugreifen.

## <a name="developer-audience"></a>Entwicklergruppe

Die RAS-API ist für die Verwendung durch C/C++-Programmierer konzipiert. Microsoft Visual Basic Programmierer können die API auch nützlich finden. Programmierer sollten mit den Netzwerk Konzepten vertraut sein.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Einige der Funktionen in der RAS-API werden nur auf Netzwerkservern unterstützt, und andere Funktionen werden nur auf Netzwerk Clients unterstützt. Spezifischere Informationen dazu, welche Betriebssysteme eine bestimmte Funktion unterstützen, finden Sie in den Abschnitten zu den Anforderungen in der-Dokumentation.

Die [erweiterte RAS-Funktionalität](function-comparison-windows-2000-versus-rras-redistributable.md) von RRAS ist für Windows NT Server 4,0 verfügbar, indem die [weitervertreibbare RRAS](https://www.microsoft.com/ntserver/nts/downloads/winfeatures/rras/rrasdown.asp)-Datei installiert wird. Die gesamte Funktionalität von RRAS ist in Windows 2000 Server, Windows Server 2003 und Windows Server 2008 integriert. RRAS-Anwendungen können nicht auf Windows NT-Arbeitsstationen 4,0 oder Client Betriebssystemen wie Windows 95 ausgeführt werden. Spezifischere Informationen dazu, welche Betriebssysteme eine bestimmte Funktion unterstützen, finden Sie in den Abschnitten zu den Anforderungen in der-Dokumentation.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                             | BESCHREIBUNG                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [RAS-Dienst](about-remote-access-service.md)<br/>                               | RAS-Dienst (RAS) bietet Remote Zugriffs Funktionen für Client Anwendungen auf Computern, auf denen Windows ausgeführt wird.<br/>                                                                                          |
| [Remote Zugriffs Dienst-Verwaltung](about-remote-access-service-administration.md)<br/> | Die Remote Zugriffs-Dienst Verwaltung bietet eine Reihe von Funktionen zum Verwalten von Benutzerberechtigungen und Ports auf RAS-Servern. Mithilfe dieser Funktionen können Sie eine RAS-Server-Verwaltungs Anwendung entwickeln.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Routing](routing-start-page.md)
</dt> <dt>

[Routing Protokolle](routing-protocols-start-page.md)
</dt> </dl>

 

 





