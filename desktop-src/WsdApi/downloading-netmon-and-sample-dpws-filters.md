---
description: Microsoft-Netzwerkmonitor 3 (Netmon) ist eine Paketanalyse zum Untersuchen des Netzwerkdatenverkehrs.
ms.assetid: 015a6a6d-9e07-4f22-b931-dcce77051bef
title: Herunterladen von Netmon- und DPWS-Beispielfiltern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8a6f92f2680807101a3c82664f4b0b3ae5a877f0d9f5797da9c9c0b6ea2b158
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030220"
---
# <a name="downloading-netmon-and-sample-dpws-filters"></a>Herunterladen von Netmon- und DPWS-Beispielfiltern

Microsoft-Netzwerkmonitor 3 (Netmon) ist eine Paketanalyse zum Untersuchen des Netzwerkdatenverkehrs. Netmon muss heruntergeladen werden, bevor die Schritte zur Problembehandlung unter [Überprüfen von Netzwerkablaufverfolgungen für die UDP-WS-Ermittlung](inspecting-network-traces-for-udp-ws-discovery.md) und [Untersuchen von Netzwerkablaufverfolgungen für HTTP-Metadaten Exchange](inspecting-network-traces-for-http-metadata-exchange.md) befolgt werden können. Nachdem Netmon heruntergeladen wurde, können DPWS-Filter verwendet werden, um den für Sie interessanten Datenverkehr zu isolieren.

## <a name="downloading-netmon"></a>Herunterladen von Netmon

Um Netmon herunterzuladen, wechseln Sie zu [Microsoft-Netzwerkmonitor,](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=983b941d-06cb-4658-b7f6-3088333d062f) und befolgen Sie die Anweisungen. Weitere Informationen zu Netmon finden Sie unter "Informationen zu Netzwerkmonitor 3.0" im Knowledge Base Hilfe und Support unter [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741) .

## <a name="sample-dpws-filters"></a>DPWS-Beispielfilter

Manchmal muss die Problembehandlung für WS-Discovery- und Metadatenaustausch in einem ausgelasteten Netzwerk erfolgen. Die Beispielfilter können verwendet werden, um die Netmon-Ausgabe auf den für Sie interessanten Datenverkehr zu beschränken. Weitere Informationen zur Verwendung von Netmon-Filtern finden Sie unter [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741) .

Das folgende Beispiel zeigt einen Filter, der die Ausgabe auf den gesamten Broadcast- WS-Discovery Datenverkehr beschränkt.

> [!Note]  
> Dieser Filter erfasst keinen Datenverkehr von Stapeln, die nicht auf Multicast-WS-Discovery Nachrichten reagieren, die an Port 3702 stammen. Wenn ein solcher Stapel verwendet wird, muss dieser Beispielfilter vor der Verwendung geändert werden.

 

``` syntax
// All broadcast WS-Discovery traffic
UDP.Port == 3702
```

Das folgende Beispiel zeigt einen Filter, der die Ausgabe auf HTTP-Nachrichten beschränkt, die an WSDAPI-Stapel am Standardport gesendet werden.

> [!Note]  
> Dienste können relevante HTTP-Nachrichten von anderen Ports als 5357 senden. Wenn Datenverkehr von anderen Ports von Interesse ist, muss dieser Beispielfilter vor der Verwendung geändert werden.

 

``` syntax
// HTTP messages sent to WSDAPI stacks on default port
TCP.Port == 5357
```

Das folgende Beispiel zeigt einen Filter, der die Ausgabe auf IPv4-Multicastdatenverkehr beschränkt.

``` syntax
// All IPv4 multicast traffic
IPv4.DestinationAddress == 239.255.255.250
```

Das folgende Beispiel zeigt einen Filter, der die Ausgabe auf IPv6-Multicastdatenverkehr beschränkt.

``` syntax
// All IPv6 multicast traffic
IPv6.DestinationAddress == FF02::C
```

Einige Filter können kombiniert werden, um die Ergebnisse weiter einzuschränken. Das folgende Beispiel zeigt einen Filter, der die Ausgabe auf IPv4-Multicast WS-Discovery Datenverkehr beschränkt.

``` syntax
// All IPv4 multicast WS-Discovery traffic
UDP.Port==3702 && IPv4.DestinationAddress=239.255.255.250
```

Wenn diese Filter verwendet werden, kann relevanter Datenverkehr aus den Netmon-Ergebnissen ausgeschlossen werden. Der Ausschluss kann auftreten, wenn sich Dienste an anderen Ports als den Standardports (5357/5358) befinden und wenn ein DPWS-Stapel nicht auf Nachrichten reagiert, die den Standardport verwenden. In diesen Fällen müssen die Filter vor der Verwendung geändert werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WSDAPI-Diagnoseverfahren](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Erste Schritte mit WSDAPI-Problembehandlung](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



