---
description: Mit Windows Sockets 2 (Winsock) können Programmierer Erweiterte Internet-, Intranet-und andere netzwerkfähige Anwendungen erstellen, um Anwendungsdaten über das Netzwerk hinweg unabhängig vom verwendeten Netzwerkprotokoll zu übertragen.
ms.assetid: 1ec8758a-40fd-4c98-b839-c2409ef712d6
title: Windows Sockets 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df253572d2fca117dbc8b45b451f8c3bacc2f360
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130409"
---
# <a name="windows-sockets-2"></a>Windows Sockets 2

## <a name="purpose"></a>Zweck

Mit Windows Sockets 2 (Winsock) können Programmierer Erweiterte Internet-, Intranet-und andere netzwerkfähige Anwendungen erstellen, um Anwendungsdaten über das Netzwerk hinweg unabhängig vom verwendeten Netzwerkprotokoll zu übertragen. Mit Winsock erhalten Programmierer Zugriff auf Erweiterte Funktionen von Microsoft® Windows® Netzwerk, wie z. b. Multicast und Quality of Service (QoS).

Winsock folgt dem Windows Open System Architecture (WOSA)-Modell. Es definiert eine Standard-Service Provider Interface (SPI) zwischen der Anwendungsprogrammierschnittstelle (Application Programming Interface, API) mit den exportierten Funktionen und den Protokoll stapeln. Dabei wird das socketparadigma verwendet, das zuerst von der UNIX Software Distribution (BSD) UNIX populär gemacht wurde. Es wurde später für Windows in Windows Sockets 1,1 angepasst, mit dem Windows Sockets 2-Anwendungen abwärts kompatibel sind. Winsock-Programmierung, die zuvor um TCP/IP zentriert war. Einige Programmierpraktiken, die mit TCP/IP funktionieren, funktionieren nicht bei jedem Protokoll. Folglich werden von der Windows Sockets 2-API bei Bedarf Funktionen zum Verarbeiten mehrerer Protokolle hinzugefügt.

## <a name="developer-audience"></a>Entwicklergruppe

Windows Sockets 2 ist für die Verwendung durch C/C++-Programmierer konzipiert. Vertrautheit mit Windows-Netzwerken ist erforderlich.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Windows Sockets 2 kann auf allen Windows-Plattformen verwendet werden. Wenn bestimmte Implementierungen oder Funktionen von Windows Sockets 2-Platt Form Einschränkungen vorhanden sind, sind Sie in der Dokumentation eindeutig angegeben.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Neuerungen bei Windows Sockets](what-s-new-for-windows-sockets-2.md)<br/>                 | Informationen zu neuen Features für Windows Sockets.<br/>                                                                                                                                                                                                                                 |
| [Winsock-Netzwerkprotokoll Unterstützung in Windows](network-protocol-support-in-windows.md)<br/> | Informationen zur Unterstützung von Netzwerkprotokollen für Windows Sockets unter verschiedenen Windows-Versionen.<br/>                                                                                                                                                                                    |
| [Informationen zu Winsock](about-winsock.md)<br/>                                                     | Allgemeine Informationen zu den Überlegungen, zur Architektur und zu den Funktionen von Windows Sockets, die Entwicklern zur Verfügung stehen.<br/>                                                                                                                                                       |
| [Verwenden von Winsock](using-winsock.md)<br/>                                                     | Prozeduren und Programmiertechniken, die mit Windows Sockets verwendet werden. Dieser Abschnitt enthält grundlegende Winsock-Programmiertechniken, wie z. b. die ersten Schritte [mit Winsock](getting-started-with-winsock.md), sowie erweiterte Techniken, die für erfahrene Winsock-Entwickler nützlich sind.<br/> |
| [Winsock-Referenz](winsock-reference.md)<br/>                                             | Dokumentation der Windows Sockets-API.<br/>                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IP-Hilfsdienst](../iphlp/ip-helper-start-page.md)
</dt> <dt>

[Quality of Service (QoS, Dienstqualität)](/previous-versions/windows/desktop/qos/qos-start-page)
</dt> </dl>

 

 
