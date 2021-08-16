---
title: Remotezugriff
description: Verwenden Sie den RAS(Remote Access Service), um Clientanwendungen zu erstellen.
ms.assetid: 4e6c04d4-f989-4248-901f-ec15f61582da
keywords:
- RAS des Ras-Diensts
- RAS RAS
- RAS des Ras-Ras-Diensts, Startseite
- RAS RAS , siehe Remotezugriff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e300061c328751f288634faf2f36ab0391ba41d7079e4f42c842d31b3e29397
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788285"
---
# <a name="remote-access"></a>Remotezugriff

## <a name="purpose"></a>Zweck

Verwenden Sie den RAS(Remote Access Service), um Clientanwendungen zu erstellen. Diese Anwendungen zeigen gängige RAS-Dialogfelder an, verwalten Remotezugriffsverbindungen und -geräte und bearbeiten Telefonbucheinträge. RAS bietet auch die nächste Generation von Serverfunktionen für den Ras-Ras-Dienst (RAS) für Windows. Die RRAS-Serverfunktionalität folgt und baut auf dem RAS (Remote Access Service) auf.

## <a name="where-applicable"></a>Anwendungsbereich

Der Remotezugriffsdienst ist in jeder Computerumgebung anwendbar, die eine WAN-Verbindung (Wide Area Network) oder ein VPN (Virtual Private Network) verwendet. Ras ermöglicht es, einen Remoteclientcomputer über eine WAN-Verbindung oder ein VPN mit einem Netzwerkserver zu verbinden. Der Remotecomputer funktioniert dann im LAN des Servers, als ob der Remotecomputer direkt mit dem LAN verbunden wäre. Die RAS-API ermöglicht Programmierern den programmgesteuerten Zugriff auf die Features von RAS.

## <a name="developer-audience"></a>Entwicklergruppe

Die RAS-API ist für die Verwendung durch C/C++-Programmierer konzipiert. Microsoft Visual Basic-Programmierer finden die API möglicherweise auch nützlich. Programmierer sollten mit Netzwerkkonzepten vertraut sein.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Einige der Funktionen in der RAS-API werden nur auf Netzwerkservern und andere Funktionen nur auf Netzwerkclients unterstützt. Ausführlichere Informationen dazu, welche Betriebssysteme eine bestimmte Funktion unterstützen, finden Sie in den Abschnitten zu Anforderungen in der Dokumentation.

Die [erweiterte RAS-Funktionalität](function-comparison-windows-2000-versus-rras-redistributable.md) von RRAS ist für Windows NT Server 4.0 verfügbar, indem [RRAS Redistributable](https://www.microsoft.com/ntserver/nts/downloads/winfeatures/rras/rrasdown.asp)installiert wird. Alle Funktionen von RRAS sind in Windows 2000 Server, Windows Server 2003 und Windows Server 2008 integriert. RRAS-Anwendungen können nicht auf Windows NT Workstation 4.0 oder auf Clientbetriebssystemen wie Windows 95 ausgeführt werden. Ausführlichere Informationen dazu, welche Betriebssysteme eine bestimmte Funktion unterstützen, finden Sie in den Abschnitten zu Anforderungen in der Dokumentation.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                             | Beschreibung                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Remotezugriffsdienst](about-remote-access-service.md)<br/>                               | Remotezugriffsdienst (RAS) bietet Remotezugriffsfunktionen für Clientanwendungen auf Computern, auf denen Windows ausgeführt wird.<br/>                                                                                          |
| [Remotezugriffsdienstverwaltung](about-remote-access-service-administration.md)<br/> | Die Remotezugriffsdienstverwaltung bietet eine Reihe von Funktionen zum Verwalten von Benutzerberechtigungen und Ports auf RAS-Servern. Mit diesen Funktionen können Sie eine RAS-Serververwaltungsanwendung entwickeln.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Routing](routing-start-page.md)
</dt> <dt>

[Routingprotokolle](routing-protocols-start-page.md)
</dt> </dl>

 

 





