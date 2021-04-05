---
description: Ein TAPI-Telefoniedienstanbieter (DSP) ist eine Dynamic Link Library (dll), die die Kommunikation von Geräten über einen Satz exportierter Dienstfunktionen unterstützt.
ms.assetid: 6e4fb295-940e-4f76-ad43-fad7da90094a
title: Informationen zum Telefoniedienstanbieter (TSP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5200a4291bdd91aba9f93a5552fecf4b52d24ee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750792"
---
# <a name="about-the-telephony-service-provider-tsp"></a>Informationen zum Telefoniedienstanbieter (TSP)

\[ Die TSPS h323 und ipconf sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Ein TAPI-Telefoniedienstanbieter (DSP) ist eine Dynamic Link Library (dll), die die Kommunikation von Geräten über einen Satz exportierter Dienstfunktionen unterstützt. Eine TAPI-Anwendung verwendet standardisierte Befehle, TAPI übergibt die Bildung an den Telefoniedienstanbieter, und der TSP verarbeitet die spezifischen Befehle, die mit dem Gerät ausgetauscht werden müssen.

In den folgenden Abschnitten werden die in Microsoft Windows bereitgestellten TSPS kurz beschrieben:

-   [H323-TSP](h323-tsp.md)
-   [Ipconf-TSP](ipconf-tsp.md)
-   [Gerätetreiber-TSP im Kernelmodus](kernel-mode-device-driver-tsp.md)
-   [NDIS-Proxy-TSP](ndis-proxy-tsp.md)
-   [Remote-TSP](remote-tsp.md)
-   [TSP von Drittanbietern](third-party-tsp.md)
-   [Unimodem-TSP](unimodem-tsp.md)

Ausführliche Informationen finden Sie im Ressourcenkit für das Ziel Betriebssystem. TSPS von Drittanbietern für spezialisierte Kommunikationsgeräte werden in der Regel vom Hersteller bereitgestellt und mit dem Gerät installiert.

In den folgenden Themen wird beschrieben, wie ein TSP erstellt wird, der in der Microsoft-Telefonieumgebung ordnungsgemäß funktioniert und wie ein TSP/MSP-paar erstellt wird:

-   [Telefoniedienstanbieter-Schnittstelle (TSPI)](telephony-service-provider-interface-tspi-.md)
-   [TSPI-Referenz](tspi-reference.md)
-   [Medien Dienstanbieter](./media-service-providers-start-page.md)

> [!Note]  
> Ein TSP ist eine vom Benutzer erstellte DLL. Wenn Sie einen TSP für eine 64-Bit-Windows-Plattform erstellen, müssen Sie Sie als 64-Bit-DLL oder DLLs kompilieren.

 

 

 
