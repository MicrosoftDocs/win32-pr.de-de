---
description: Microsoft-Netzwerkmonitor 3 (NetMon) ist ein Paket Analysetool, das zum Überprüfen des Netzwerkverkehrs verwendet wird.
ms.assetid: 015a6a6d-9e07-4f22-b931-dcce77051bef
title: Herunterladen von Netmon und Beispiel-DPWS-Filtern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47790b26164ec0ed2792d1d1e1f2ad4ba5d77d38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343817"
---
# <a name="downloading-netmon-and-sample-dpws-filters"></a>Herunterladen von Netmon und Beispiel-DPWS-Filtern

Microsoft-Netzwerkmonitor 3 (NetMon) ist ein Paket Analysetool, das zum Überprüfen des Netzwerkverkehrs verwendet wird. NetMon muss heruntergeladen werden, bevor die Schritte zur Problembehandlung bei der [Überprüfung von Netzwerk Ablauf Verfolgungen für UDP-WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md) und untersuchen [von Netzwerk Ablauf Verfolgungen für den HTTP-Metadatenaustausch](inspecting-network-traces-for-http-metadata-exchange.md) befolgt werden können Nachdem Netmon heruntergeladen wurde, können DPWS-Filter verwendet werden, um den relevanten Datenverkehr zu isolieren.

## <a name="downloading-netmon"></a>NetMon wird heruntergeladen

Um Netmon herunterzuladen, navigieren Sie zu [Microsoft-Netzwerkmonitor](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=983b941d-06cb-4658-b7f6-3088333d062f) , und befolgen Sie die Anweisungen. Weitere Informationen zu Netmon finden Sie unter "Informationen zu Netzwerkmonitor 3,0" in der Hilfe-und Support Knowledge Base unter [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741) .

## <a name="sample-dpws-filters"></a>Beispiel-DPWS-Filter

Manchmal müssen WS-Discovery-und Metadatenaustausch-Problembehandlung in einem ausgelasteten Netzwerk stattfinden. Die Beispiel Filter können verwendet werden, um die NetMon-Ausgabe auf den gewünschten Datenverkehr zu beschränken. Weitere Informationen zur Verwendung von Netmon-Filtern finden Sie unter [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741) .

Das folgende Beispiel zeigt einen Filter, der die Ausgabe auf den gesamten Broadcast WS-Discovery-Datenverkehr beschränkt.

> [!Note]  
> Dieser Filter erfasst keinen Datenverkehr von Stapeln, die nicht auf Multicast-WS-Discovery Meldungen reagieren, die von Port 3702 stammen. Wenn ein solcher Stapel verwendet wird, muss dieser Beispiel Filter vor der Verwendung geändert werden.

 

``` syntax
// All broadcast WS-Discovery traffic
UDP.Port == 3702
```

Das folgende Beispiel zeigt einen Filter, der die Ausgabe auf HTTP-Nachrichten einschränkt, die an WSDAPI-Stapel am Standardport gesendet werden.

> [!Note]  
> Dienste können relevante HTTP-Nachrichten von anderen Ports als 5357 senden. Wenn der Datenverkehr von anderen Ports von Interesse ist, muss dieser Beispiel Filter vor der Verwendung geändert werden.

 

``` syntax
// HTTP messages sent to WSDAPI stacks on default port
TCP.Port == 5357
```

Das folgende Beispiel zeigt einen Filter, der die Ausgabe auf IPv4-Multicast Datenverkehr beschränkt.

``` syntax
// All IPv4 multicast traffic
IPv4.DestinationAddress == 239.255.255.250
```

Das folgende Beispiel zeigt einen Filter, der die Ausgabe auf IPv6-Multicast Datenverkehr beschränkt.

``` syntax
// All IPv6 multicast traffic
IPv6.DestinationAddress == FF02::C
```

Einige Filter können kombiniert werden, um die Ergebnisse weiter einzuschränken. Das folgende Beispiel zeigt einen Filter, der die Ausgabe auf IPv4-Multicast WS-Discovery-Datenverkehr beschränkt.

``` syntax
// All IPv4 multicast WS-Discovery traffic
UDP.Port==3702 && IPv4.DestinationAddress=239.255.255.250
```

Wenn diese Filter verwendet werden, kann relevanter Datenverkehr aus den Netmon-Ergebnissen ausgeschlossen werden. Ein Ausschluss kann auftreten, wenn sich Dienste an anderen Ports als den Standardports (5357/5358) befinden und wenn ein DPWS-Stapel nicht auf Nachrichten mit dem Standardport antwortet. In diesen Fällen müssen die Filter vor der Verwendung geändert werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WSDAPI-Diagnose Prozeduren](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Ersten Schritte mit der WSDAPI-Problembehandlung](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



