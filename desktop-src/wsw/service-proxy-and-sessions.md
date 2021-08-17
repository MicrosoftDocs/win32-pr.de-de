---
title: Dienstproxy und Sitzungen
description: Der Dienstproxy weist spezielle Verhaltensweisen für sitzungsbasierte und nicht sitzungsbasierte Kanalbindungen auf.
ms.assetid: 6dc9de95-b97c-4acc-9d45-d5e6ebb6bd77
keywords:
- Webdienste für Dienstproxys und Sitzungen für Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d845bd341f1343338031619a72fd5dbd307fe1a92175b3753d83b373d73c812
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962889"
---
# <a name="service-proxy-and-sessions"></a>Dienstproxy und Sitzungen

Der [Dienstproxy](service-proxy.md) weist spezielle Verhaltensweisen für sitzungsbasierte und nicht sitzungsbasierte Kanalbindungen auf. Der Dienstproxy stellt sitzungsbasierte Semantik bereit, wenn die zugrunde liegende Kanalbindung sitzungsbasiert ist. In diesem Fall wird ein einzelner Kanal verwendet, um Aufrufe zu bedienen. Wenn die Kanalbindung jedoch nicht sitzungsbasiert ist, erstellt der Dienstproxy einen separaten Kanal für jeden Aufruf. Beachten Sie jedoch, dass nicht sitzungsbasierte Kanäle in einem Pool zusammengefasst und möglicherweise wiederverwendet werden. Bei der Wiederverwendung eines Kanals hält der Dienstproxy den Kanal geöffnet, wenn der zugrunde liegende Kanal nicht fehlerhaft war oder der Aufruf eines Kanals dazu geführt hat, dass der Dienstproxy den Kanal fehlerhaft hat. Beachten Sie dies. mit Ausnahme eines Fehlers wird ein Kanal geöffnet, solange der Dienstproxy geöffnet ist und nur geschlossen wird, wenn der Dienstproxy geschlossen wird.


Wenn die Kanalbindung sitzungsbasiert ist und der zugrunde liegende Kanal fehlerhaft ist, wechselt der Dienstproxystatuscomputer in den [**Zustand WS \_ SERVICE PROXY \_ STATE \_ \_ FAULTED.**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) Bei nicht sitzungsbasierter Kanalbindung führt ein Fehler im zugrunde liegenden Kanal nicht dazu, dass der Proxy in den **WS \_ SERVICE PROXY \_ STATE \_ \_ FAULTED-Zustand** übergreift.

Weitere Informationen zum Dienstproxy und seiner Beziehung zum Status finden Sie im Thema [Dienstproxy.](service-proxy.md) Beispiele für verschiedene Kanalbindungen finden Sie in den folgenden Beispielen:

-   Nicht-Sitzungskanalbindung, [HttpCalculatorClientExample](httpcalculatorclientexample.md)
-   sitzungsbasierte Kanalbindung, [SessionfullCalculatorClientExample](sessionfullcalculatorclientexample.md)

 

 




