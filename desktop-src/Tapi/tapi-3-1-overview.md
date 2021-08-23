---
description: TAPI Version 3.1 ist eine COM-basierte API, die klassische Telefonie und IP-Telefonie zusammenfasst. Mögliche Anwendungen reichen von einfachen Sprachanrufen über das public Switched Telephone Network (PSTN) bis zu Multicast-Multimedia-IP-Konferenz mit Servicequalität (Quality of Service, QOS).
ms.assetid: 1f7ccef8-5aad-48e7-90e9-a378dd83a870
title: ÜBERSICHT ÜBER TAPI 3.1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c55aff75690894cc8c8a0d5e692b0c9b019a39116a617dbf2a4ae050200f6892
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139897"
---
# <a name="tapi-31-overview"></a>ÜBERSICHT ÜBER TAPI 3.1

TAPI Version 3.1 ist eine COM-basierte API, die klassische Telefonie und IP-Telefonie zusammenfasst. Mögliche Anwendungen reichen von einfachen Sprachanrufen über das public Switched Telephone Network (PSTN) bis zu Multicast-Multimedia-IP-Konferenz mit Servicequalität (Quality of Service, QOS).

Weitere Informationen zu TAPI 3.1 IP-Telefoniefunktionen finden Sie im Whitepaper "IP-Telefonie mit TAPI 3" auf der Microsoft-Website.

TapI 3.1 enthält vier Hauptkomponenten:

-   COM-API
-   TAPI-Server
-   Telefoniedienstanbieter (TSPs)
-   Media Stream Providers (MSPs)

Das folgende Diagramm veranschaulicht die TAPI 3.1-Architektur:

![tapi 3-Architektur](images/callarc-gif-1.png)

Die API wird als suite of Component Object Model (COM)-Objekte implementiert. Durch das Verschieben von TAPI in das objektorientierte COM-Modell können Entwickler TAPI-fähige Anwendungen in vielen Sprachen schreiben, z. B. Java, Visual Basic oder C/C++. Die Verwendung von COM ermöglicht Komponentenupgrades von TAPI-Features.

Der TAPI-Serverprozess (TAPISRV) abstrahiert die TAPI-Dienstanbieterschnittstelle (TAPI Service Provider Interface, TSPI) aus TAPI 3.x und TAPI 2.x, sodass TAPI 2.x-Telefoniedienstanbieter mit TAPI 3.x verwendet werden können, wodurch der interne Zustand von TAPI beibehalten wird. TAPISRV wird als Dienstprozess in SVCHOST implementiert.

[Dienstanbieter](./tapi-service-providers.md) abstrahieren anbieterspezifische Medientransportmechanismen. Sie sind in der Regel paarweise vorhanden– ein Telefoniedienstanbieter (TSP) für die Anrufsteuerung und ein Media Service Provider (MSP) für die Mediensteuerung.

[Telefoniedienstanbieter](./telephony-service-providers-start-page.md) (TSPs) sind für die Auflösung des protokollunabhängigen Aufrufmodells von TAPI in protokollspezifische Aufrufsteuerungsmechanismen verantwortlich. TAPI 3.1 bietet Abwärtskompatibilität mit TAPI 2.1-TSPs. Zwei IP-Telefoniedienstanbieter (und die zugehörigen MSPs) werden standardmäßig mit TAPI 3.1 bereitgestellt: dem H.323-TSP und dem IP-Multicastkonferenz-TSP.

[Media Service Providers](media-service-providers-start-page.md) (MSPs) bieten eine einheitliche Möglichkeit für den Zugriff auf die Medienstreams in einem Aufruf und unterstützen die DirectShow<sup>TM-API</sup> als primären Medienstreamhandler. TAPI-MSPs implementieren DirectShow-Schnittstellen für einen bestimmten TSP und sind für jeden Telefoniedienst erforderlich, der DirectShow-Streaming verwendet. Generische Streams werden von der Anwendung verarbeitet.

 

 
