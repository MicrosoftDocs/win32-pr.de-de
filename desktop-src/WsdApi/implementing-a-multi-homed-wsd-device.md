---
description: In diesem Thema wird die Unterstützung mehrerer Geräte in WSDAPI beschrieben und Implementierungsempfehlungen für Client- und Geräteentwickler ausgegeben.
ms.assetid: d30ed536-d477-4f50-8c80-aacc35f948b9
title: Implementieren eines mehrstufigen WSD-Geräts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24ac83b0fe3b951e02e77ef9efc6241ce5a7e1780106b1e85e4f00b987bbbe05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991740"
---
# <a name="implementing-a-multi-homed-wsd-device"></a>Implementieren eines mehrstufigen WSD-Geräts

[WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) und das [Geräteprofil für Webdienste](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) beschreiben nicht die Implementierung von Geräten mit mehreren Geräten. In diesem Thema wird die Unterstützung mehrerer Geräte in WSDAPI beschrieben und Implementierungsempfehlungen für Client- und Geräteentwickler ausgegeben. In diesem Thema wird davon ausgegangen, dass Ermittlungsmeldungen sowohl über IPv4 als auch über IPv6 (sofern verfügbar) mit der gleichen Nachrichten-ID und den gleichen Anwendungssequenzierungsinformationen gesendet werden.

## <a name="discovery-in-a-multi-homed-environment"></a>Ermittlung in einer Umgebung mit mehreren Homes

Wie im Abschnitt [Hello](hello-message.md) and [XAddrs](xaddr-validation-rules.md) von [Additional WS-Discovery Functionality (Zusätzliche WS-Discovery-Funktionalität)](additional-ws-discovery-functionality.md)erwähnt, stellt WSDAPI in einer Hello-Nachricht keine XAddrs bereit. Dies bedeutet, dass die gleiche Hello-Nachricht an alle Netzwerkschnittstellen mit der gleichen Nachrichten-ID und den gleichen Anwendungssequenzierungsinformationen gesendet werden kann. Dies erleichtert die Erkennung von Clientkonflikten, mehrere Hello-Nachrichten vom selben Gerät zu verwerfen, wenn ein Client und das Gerät mehrere Subnetze gemeinsam nutzen.

Da die [XAddrs](xaddr-validation-rules.md) nicht in der [Hello-Nachricht](hello-message.md) gesendet werden, müssen Clientimplementierungen eine [Resolve-Nachricht](resolve-message.md) senden, um die relevante Geräteadresse abzurufen. Die Auflösung sollte an alle Clientschnittstellen mit der gleichen Nachrichten-ID gesendet werden, und das Gerät sollte doppelte Nachrichten nach Bedarf filtern. Wenn Sie dieselbe Nachrichten-ID für die Resolve-Nachricht verwenden, kann das Gerät bei Bedarf eine bevorzugte Schnittstelle für die Kommunikation mit Clients auswählen.

Beim Senden einer [ResolveMatch-Nachricht](resolvematches-message.md) sollte ein Gerät [XAddrs](xaddr-validation-rules.md) bereitstellen, die sich auf die Netzwerkschnittstelle beziehen, über die die Nachricht unicastiert wird. Diese Vorgehensweise hilft, mehrere Clientverbindungsversuche und komplizierte Wiederholungslogik zu vermeiden.

## <a name="metadata-exchange-in-a-multi-homed-environment"></a>Metadatenaustausch in einer Umgebung mit mehreren Homes

Die Implementierung des Metadatenaustauschs in einer Umgebung mit mehreren Startseiten ist aufgrund der Metadatenversionsierung schwieriger als die Implementierung der Ermittlung. Wenn ein Client Metadaten über mehrere Schnittstellen anfordert, kann der Client mehrere [GetResponse-Nachrichten](getresponse--metadata-exchange--message.md) über verschiedene Schnittstellen empfangen. Diese GetResponse-Nachrichten  können verschiedene Beziehungsmetadatenabschnitte mit derselben Metadatenversion enthalten. Dadurch wird der Wert der Metadatenversionsnummer reduziert.

Es gibt einen alternativen Ansatz, bei dem eine einzelne [GetResponse-Nachricht](getresponse--metadata-exchange--message.md) als Antwort mit allen Adressen für den Dienst gesendet wird. Der Nachteil dieser Methode besteht darin, dass private Informationen, z. B. die Topologie indirekt zugänglicher Netzwerke, offengelegt werden können.

Auf Windows Vista enthalten die von WSDAPI bereitgestellten Metadaten nur Adressen, die für die Schnittstelle gültig sind, für die die Metadatenanforderung empfangen wurde.

 

 



