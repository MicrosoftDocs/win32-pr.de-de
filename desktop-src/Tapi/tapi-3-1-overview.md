---
description: TAPI Version 3,1 ist eine COM-basierte API, die klassische und IP-Telefonie zusammenfasst. Mögliche Anwendungen reichen von einfachen sprach aufrufen über das Public-Switched-Telefon Netzwerk (PSTN) bis hin zu Multicast-Multimedia-IP-Konferenzen mit Dienst Qualität (Quality of Service, QoS).
ms.assetid: 1f7ccef8-5aad-48e7-90e9-a378dd83a870
title: TAPI 3,1 (Übersicht)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b30b70ccdc1c4a0985107d2bd2fc36bfbe4e3fca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368736"
---
# <a name="tapi-31-overview"></a>TAPI 3,1 (Übersicht)

TAPI Version 3,1 ist eine COM-basierte API, die klassische und IP-Telefonie zusammenfasst. Mögliche Anwendungen reichen von einfachen sprach aufrufen über das Public-Switched-Telefon Netzwerk (PSTN) bis hin zu Multicast-Multimedia-IP-Konferenzen mit Dienst Qualität (Quality of Service, QoS).

Weitere Informationen zu TAPI 3,1-IP-Telefoniefunktionen finden Sie im Whitepaper "IP-Telefonie mit TAPI 3", das sich auf der Microsoft-Website befindet.

Es gibt vier Hauptkomponenten zu TAPI 3,1:

-   COM-API
-   TAPI-Server
-   Telefoniedienstanbieter (TSPS)
-   Medienstrom Anbieter (MSPs)

Das folgende Diagramm veranschaulicht die TAPI 3,1-Architektur:

![TAPI 3-Architektur](images/callarc-gif-1.png)

Die API wird als Suite von Component Object Model (com)-Objekten implementiert. Das Verschieben von TAPI in das objektorientierte com-Modell ermöglicht Entwicklern das Schreiben von TAPI-fähigen Anwendungen in vielen Sprachen, wie z. b. Java, Visual Basic oder C/C++. Die Verwendung von com ermöglicht Komponenten Upgrades von TAPI-Funktionen.

Der TAPI-Server Prozess (tapisrv) abstrahiert die TAPI Service Provider Interface (TSPI) von TAPI 3. x und TAPI 2. x und ermöglicht so die Verwendung von TAPI 2. x-Telefoniedienstanbietern mit TAPI 3. x, wobei der interne Status von TAPI beibehalten wird. Tapisrv ist als Dienst Prozess innerhalb von svchost implementiert.

[Dienstanbieter](./tapi-service-providers.md) : abstrakte anbieterspezifische Medien Transportmechanismen. Sie sind in der Regel paarweise vorhanden – einem Telefoniedienstanbieter (TSP) für die Callcenter-Steuerung und einem Media Service Provider (MSP) für die Mediensteuerung.

[Telefoniedienstanbieter](./telephony-service-providers-start-page.md) (TSPS) sind dafür verantwortlich, das Protokoll unabhängige Aufrufmodell von TAPI in Protokoll spezifische Aufrufe der Steuerungsmechanismen aufzulösen. TAPI 3,1 bietet Abwärtskompatibilität mit TAPI 2,1 TSPS. Zwei IP-Telefoniedienstanbieter (und die zugehörigen MSPs) werden standardmäßig mit TAPI 3,1 ausgeliefert: dem H. 323 TSP und dem IP-Multicast Konferenz-TSP.

[Media Service Providers](media-service-providers-start-page.md) (MSPs) bieten eine einheitliche Methode für den Zugriff auf die Mediendaten Ströme in einem-Befehl, wobei die DirectShow<sup>TM</sup> -API als primärer Mediendaten Strom Handler unterstützt wird. TAPI-MSPs implementieren DirectShow-Schnittstellen für einen bestimmten TSP und sind für alle Telefoniedienste erforderlich, die DirectShow-Streaming verwenden. Generische Streams werden von der Anwendung behandelt.

 

 
