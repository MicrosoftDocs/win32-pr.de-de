---
description: In diesem Thema wird die Unterstützung mehrfach vernetzter Geräte in WSDAPI beschrieben, und es werden Implementierungs Empfehlungen für Client-und Geräte Entwickler bereitgestellt.
ms.assetid: d30ed536-d477-4f50-8c80-aacc35f948b9
title: Implementieren eines mehrfach vernetzten WSD-Geräts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ac3537b96a577db47419d55cb5c6f732f8f7906
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218160"
---
# <a name="implementing-a-multi-homed-wsd-device"></a>Implementieren eines mehrfach vernetzten WSD-Geräts

[WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) und das [Geräte Profil für Webdienste](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) beschreiben nicht die Implementierung von mehrfach vernetzten Geräten. In diesem Thema wird die Unterstützung mehrfach vernetzter Geräte in WSDAPI beschrieben, und es werden Implementierungs Empfehlungen für Client-und Geräte Entwickler bereitgestellt. In diesem Thema wird davon ausgegangen, dass Ermittlungs Nachrichten über IPv4 und IPv6 (falls verfügbar) mit der gleichen Nachrichten-ID und den Informationen zur Anwendungs Sequenzierung gesendet werden.

## <a name="discovery-in-a-multi-homed-environment"></a>Ermittlung in einer mehrfach vernetzten Umgebung

Wie im Abschnitt [Hello](hello-message.md) und [xaddrs](xaddr-validation-rules.md) der [zusätzlichen WS-Discovery Funktionalität](additional-ws-discovery-functionality.md)erwähnt, stellt WSDAPI keine xaddrs in einer Hello-Nachricht bereit. Dies bedeutet, dass dieselbe Hello-Nachricht an alle Netzwerkschnittstellen mit der gleichen Nachrichten-ID und den Informationen zur Anwendungs Sequenzierung gesendet werden kann. Dies erleichtert es der clientkollisions Erkennung, mehrere Hello-Nachrichten vom gleichen Gerät zu verwerfen, wenn ein Client und das Gerät mehr als ein Subnetz gemeinsam verwenden.

Da die [xaddrs](xaddr-validation-rules.md) nicht in der [Hello](hello-message.md) -Nachricht gesendet werden, müssen Client Implementierungen eine [Resolve](resolve-message.md) -Nachricht senden, um die relevante Geräteadresse zu erhalten. Die Auflösung sollte an allen Client Schnittstellen mit derselben Nachrichten-ID gesendet werden, und das Gerät sollte bei Bedarf doppelte Nachrichten filtern. Wenn Sie dieselbe Nachrichten-ID für die Auflösungs Nachricht verwenden, kann das Gerät bei Bedarf eine bevorzugte Schnittstelle für die Kommunikation mit Clients auswählen.

Wenn eine [resolvematch](resolvematches-message.md) -Nachricht gesendet wird, sollte ein Gerät [xaddrs](xaddr-validation-rules.md) bereitstellen, die sich auf die Netzwerkschnittstelle beziehen, über die die Nachricht uniumgewandelt wird. Diese Vorgehensweise hilft bei der Vermeidung mehrerer Client Verbindungsversuche und komplizierter Wiederholungs Logik.

## <a name="metadata-exchange-in-a-multi-homed-environment"></a>Metadatenaustausch in einer mehrfach vernetzten Umgebung

Das Implementieren von Metadatenaustausch in einer mehrfach vernetzten Umgebung ist schwieriger als das Implementieren der Ermittlung aufgrund der metadatenversionierung. Wenn ein Client Metadaten über mehrere Schnittstellen anfordert, kann der Client mehrere [GetResponse](getresponse--metadata-exchange--message.md) -Nachrichten über verschiedene Schnittstellen empfangen. Diese GetResponse-Nachrichten können unterschiedliche **Beziehungs** Metadatenabschnitte mit derselben Metadatenversion enthalten. Dadurch wird der Wert der Metadatenversionsnummer reduziert.

Es gibt einen alternativen Ansatz, bei dem eine einzelne [GetResponse](getresponse--metadata-exchange--message.md) -Nachricht als Antwort mit allen Adressen für den Dienst gesendet wird. Der Nachteil dieser Methode besteht darin, dass private Informationen, wie z. b. die Topologie von indirekt zugänglichen Netzwerken, offengelegt werden können.

Unter Windows Vista enthalten die von WSDAPI bereitgestellten Metadaten nur Adressen, die für die Schnittstelle gültig sind, auf der die metadatenanforderung empfangen wurde.

 

 



