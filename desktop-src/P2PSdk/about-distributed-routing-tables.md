---
description: Eine verteilte Routingtabelle (Distributed Routing Table, DRT) ist als Netz aus knotenverfeinerten Knoten vorhanden, wobei jeder Knoten eine Instanz einer Anwendung ist, die die DRT-API verwendet.
ms.assetid: 257ad7ea-636b-45f2-b514-4a213939d107
title: Informationen zu verteilten Routingtabellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc8e82b25fee0bb6733bb21db82193d14e6cc8d621148b6d5c671fb04a3b2d85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011838"
---
# <a name="about-distributed-routing-tables"></a>Informationen zu verteilten Routingtabellen

Eine verteilte Routingtabelle (Distributed Routing Table, DRT) ist als Netz aus knotenverfeinerten Knoten vorhanden, wobei jeder Knoten eine Instanz einer Anwendung ist, die die DRT-API verwendet. Knoten, die Schlüssel veröffentlichen, sind für die Unterstützung der Veröffentlichung und Auflösung von Schlüsseln anderer Knoten verantwortlich. Knoten können auch "nur auflösen" verwendet werden, was nicht erfordert, dass sie Peers unterstützen. Das DRT-Protokoll wird über einen UDP/IPv6-Transport ausgeführt.

Ein Knoten, der einen Schlüssel veröffentlicht, erstellt und verwaltet eine lokale Routingtabelle anderer Knoten im Mesh. Diese Routingtabelle ist so optimiert, dass der Knoten schnell einen bestimmten Schlüssel im Netz finden kann, indem er den Schlüssel direkt in der lokalen Routingtabelle findet oder andere Knoten fragt, die Schlüssel numerisch in der Nähe des Ziels veröffentlichen. Diese Aktion wird wiederholt, bis der erforderliche Schlüssel gefunden wird oder der Knoten feststellt, dass kein solcher Schlüssel vorhanden ist.

DRT-Schlüssel sind 256-Bit-Ganzzahlen ohne Vorzeichen. Die Nähe zwischen Schlüsseln wird durch den numerischen Unterschied zwischen ihnen definiert. Der DRT-Keyspace wird als kreisförmiger Schlüsselbereich betrachtet. Beispielsweise werden der erste mögliche Schlüsselwert und der letzte mögliche Schlüsselwert als Nachbarn betrachtet.

In einem sicheren DRT sind Knoten erforderlich, um die von ihnen veröffentlichten Schlüssel zu authentifizieren. Der Mechanismus, mit dem Knoten Schlüssel authentifizieren, muss mithilfe der DRT-API festgelegt werden, wenn das DRT initialisiert wird. Wählen Sie dazu einen Sicherheitsanbieter für das DRT aus. Ein Sicherheitsanbieter ist ein Modul, das Token erstellen kann, die zum Authentifizieren von Schlüsseln verwendet werden, und Token überprüfen kann, die von anderen Knoten erzeugt werden. Sie muss die In dieser Dokumentation definierte Schnittstelle des Sicherheitsanbieters implementieren. Das Windows 7 DRT ist mit zwei vollständig implementierten Sicherheitsanbietern ausgestattet, die zum Erstellen Windows verwendet werden können.

Während der Initialisierung muss eine Anwendung das DRT auch mit einem Bootstrapanbieter ausliefern. Der Bootstrapanbieter ist ein Modul, das die Netzwerkendpunkte von Knoten abrufen kann, die bereits im DRT-Netz vorhanden sind, und wird vom DRT aufgerufen, wenn ein neuer Knoten eingerichtet wird. Wie das Sicherheitsanbietermodul muss der Bootstrapanbieter eine klar definierte Schnittstelle implementieren. Das Windows 7 DRT wird mit zwei vollständig implementierten Bootstrapanbietern ausgestattet.

Das DRT betrachtet die unmittelbaren Nachbarn eines Schlüssels als sonderbar. Die fünf nächstgelegenen Schlüssel, die numerisch kleiner sind, und die fünf schlüsseln, die numerisch größer als ein veröffentlichter Schlüssel sind, bilden einen sogenannten Blattsatz. Das DRT meldet Änderungen am Blattsatz eines Schlüssels über die DRT-API.

## <a name="drt-life-cycle-and-state-transitions"></a>DRT-Lebenszyklus und Zustandsübergänge

Eine Anwendung kann eine lokale DRT-Instanz mithilfe der [**DrtOpen-Funktion initialisieren.**](/windows/desktop/api/drt/nf-drt-drtopen) Diese Funktion löst den Bootstrappingprozess aus, bei dem die DRT-API den Bootstrapanbieter aufruft, um die Schlüssel und Netzwerkendpunkte anderer Knoten zu erlernen, die bereits am DRT teilnehmen. Wenn der Bootstrapanbieter erfolgreich mindestens einen anderen Knoten findet, geht das DRT in den STATUS DRT \_ ACTIVE über. In diesem Zustand kann die Anwendung nach Schlüsseln suchen, die von anderen Knoten veröffentlicht wurden, und Schlüssel veröffentlichen, die aufgelöst werden können. Wenn der Bootstrapanbieter andere Knoten nicht erfolgreich finden kann, geht das DRT in den ZUSTAND DRT \_ ALONE über. Das DRT bleibt im EIGENSTÄNDIGEN DRT-Zustand und versucht in regelmäßigen Abständen, einen Bootstrap-Versuch zu unternehmen, um Peers zu finden und in den \_ DRT \_ ACTIVE-Zustand zu wechseln.

Ein Knoten kann von DRT ACTIVE in diese Zustände \_ überwechseln.

| Lebenszyklusstatus | Bedingungen                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DRT \_ ALLEIN       | Der lokale Knoten hat keine anderen Knoten im DRT gefunden. In diesem Zustand lauset der Knoten weiterhin auf andere Knoten innerhalb des DRT.<br/> Wenn ein anderer Knoten dem DRT beitritt, wechselt der lokale Knoten in den STATUS DRT \_ ACTIVE. Wenn das Netzwerk nicht mehr besteht, wird es zu DRT \_ NO \_ NETWORK überwechseln. Im Falle eines schwerwiegenden Fehlers mit dem DRT geht der Knoten in den ZUSTAND DRT \_ FAULTED über.<br/> |
| DRT \_ NO \_ NETWORK | Wenn ein Knoten die Netzwerkkonnektivität verliert, geht er in den STATUS DRT \_ NO \_ NETWORK über. An diesem Punkt kann die Anwendung auf die Wiederherstellung der Netzwerkkonnektivität warten und das DRT schließen.<br/>                                                                                                                                                                                                                    |
| \_DRT-FEHLER     | Innerhalb des lokalen Knotens ist ein schwerwiegender Fehler aufgetreten. Beispiel: Auf dem lokalen Computer ist nicht genügend physischer Arbeitsspeicher verfügbar.<br/> Während ein Knoten in diesen Zustand eintritt, muss die Anwendung die [**DrtClose-API**](/windows/desktop/api/drt/nf-drt-drtclose) aufrufen, das Problem beheben und das DRT mit [**DrtOpen erneut initialisieren.**](/windows/desktop/api/drt/nf-drt-drtopen)<br/>                                                                                                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des distributed routing Tabellen-API](using-the-distributed-routing-table-api.md)
</dt> <dt>

[Distributed Routing Tabellen-API Reference](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 




