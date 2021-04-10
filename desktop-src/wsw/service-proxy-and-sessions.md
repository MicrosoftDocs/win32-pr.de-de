---
title: Dienst Proxy und-Sitzungen
description: Der Dienst Proxy weist ein spezielles Verhalten für Sitzungs basierte und nicht Sitzungs basierte Kanal Bindungen auf.
ms.assetid: 6dc9de95-b97c-4acc-9d45-d5e6ebb6bd77
keywords:
- Dienst Proxy-und Sitzungs-Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc8477a8cd03579e1d8cbfe4509f89890af8482
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104039861"
---
# <a name="service-proxy-and-sessions"></a>Dienst Proxy und-Sitzungen

Der [Dienst Proxy](service-proxy.md) weist ein spezielles Verhalten für Sitzungs basierte und nicht Sitzungs basierte Kanal Bindungen auf. Der Dienst Proxy stellt eine Sitzungs basierte Semantik bereit, wenn die zugrunde liegende kanalbindung Sitzungs basiert ist. In diesem Fall wird ein einzelner Kanal für die Dienst Aufrufe verwendet. Wenn die kanalbindung jedoch nicht Sitzungs basiert ist, erstellt der Dienst Proxy einen separaten Kanal für jeden-Rückruf. Beachten Sie jedoch, dass nicht Sitzungs basierte Kanäle in einem Pool zusammengefasst und möglicherweise wieder verwendet werden. Bei der Wiederverwendung eines Kanals hält der Dienst Proxy den Kanal geöffnet, wenn der zugrunde liegende Kanal nicht einen Fehler verursacht hat oder der-Vorgang für einen Kanal dazu geführt hat, dass der Kanal des Dienst Proxys fehlerhaft ist. Beachten Sie, dass. Wenn ein Kanal geöffnet ist, wird er im Falle eines Fehlers geöffnet, solange der Dienst Proxy geöffnet ist und nur geschlossen wird, wenn der Dienst Proxy geschlossen wird.


Wenn die kanalbindung Sitzungs basiert ist und der zugrunde liegende Kanal fehlerhaft ist, wechselt der Dienst Proxy-Zustands Automat in den Status des [**WS- \_ Dienst Proxy \_ \_ Zustands \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) . Im Fall einer nicht Sitzungs basierten channelbindung bewirkt ein Fehler im zugrunde liegenden Kanal nicht, dass der Proxy in den Status des **WS- \_ Dienst \_ Proxy \_ Zustands \_** übergeht.

Weitere Informationen zum Dienst Proxy und dessen Beziehung zum Status finden Sie im Thema zu [Dienst Proxys](service-proxy.md) . Beispiele für verschiedene Kanal Bindungen finden Sie in den folgenden Beispielen:

-   nicht-Sitzungs kanalbindung, [httpcalculatorclieintexample](httpcalculatorclientexample.md)
-   Sitzungs basierte kanalbindung, [sessionfullcalculatorclieintexample](sessionfullcalculatorclientexample.md)

 

 




