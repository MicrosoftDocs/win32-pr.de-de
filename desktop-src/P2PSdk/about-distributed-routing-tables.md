---
description: Eine verteilte Routing Tabelle (DRT) ist als Netz von zusammen hängenten Knoten vorhanden, wobei jeder Knoten eine Instanz einer Anwendung ist, die die DRT-API verwendet.
ms.assetid: 257ad7ea-636b-45f2-b514-4a213939d107
title: Informationen zu verteilten Routing Tabellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dfca9f81cc609d97584ef5a11f999722c696858
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865183"
---
# <a name="about-distributed-routing-tables"></a>Informationen zu verteilten Routing Tabellen

Eine verteilte Routing Tabelle (DRT) ist als Netz von zusammen hängenten Knoten vorhanden, wobei jeder Knoten eine Instanz einer Anwendung ist, die die DRT-API verwendet. Knoten, die Schlüssel veröffentlichen, sind dafür verantwortlich, anderen Knoten das Veröffentlichen und Auflösen von Schlüsseln zu unterstützen. Knoten können auch in eine "nur auflösen"-Weise einbezogen werden, die keine Unterstützung für Peers erfordert. Das DRT-Protokoll wird über einen UDP/IPv6-Transport ausgeführt.

Ein Knoten, der einen Schlüssel veröffentlicht, erstellt und verwaltet eine lokale Routing Tabelle mit anderen Knoten im Mesh. Diese Routing Tabelle ist so optimiert, dass der Knoten schnell einen bestimmten Schlüssel im Mesh finden kann, indem er den Schlüssel direkt in der lokalen Routing Tabelle findet oder wenn andere Knoten die Schlüssel numerisch in der Nähe des Ziels veröffentlichen. Diese Aktion wird wiederholt, bis der erforderliche Schlüssel gefunden wird, oder der Knoten bestimmt, dass kein solcher Schlüssel vorhanden ist.

Bei DRT-Schlüsseln handelt es sich um 256-Bit-Ganzzahlen ohne Vorzeichen. Die Nähe zwischen Schlüsseln wird durch den numerischen Unterschied zwischen den Schlüsseln definiert. Der DRT-Keyspace gilt als zirkulär. Beispielsweise werden der erste mögliche Schlüsselwert und der letzte mögliche Schlüsselwert als Nachbarn betrachtet.

In einem sicheren DRT sind Knoten erforderlich, um die von Ihnen veröffentlichten Schlüssel zu authentifizieren. Der Mechanismus, mit dem Knoten authentifiziert werden, muss mithilfe der DRT-API festgelegt werden, wenn das DRT initialisiert wird. Dies erfolgt durch Auswählen eines Sicherheits Anbieters für das DRT. Ein Sicherheitsanbieter ist ein Modul, das Token zum Authentifizieren von Schlüsseln erzeugen und Token überprüfen kann, die von anderen Knoten erstellt werden. Es muss die in dieser Dokumentation definierte Sicherheitsanbieter Schnittstelle implementieren. Windows 7 DRT ist mit zwei vollständig implementierten Sicherheitsanbietern ausgeliefert, die zum Erstellen von Windows-Anwendungen verwendet werden können.

Während der Initialisierung muss eine Anwendung auch das DRT mit einem Bootstrap-Anbieter bereitstellen. Der Bootstrap-Anbieter ist ein Modul, das die Netzwerk Endpunkte von Knoten abrufen kann, die bereits im DRT-Mesh vorhanden sind, und von der DRT aufgerufen wird, wenn ein neuer Knoten eingerichtet wird. Wie das Sicherheitsanbieter Modul muss der Bootstrap-Anbieter eine klar definierte Schnittstelle implementieren. Windows 7 DRT wird mit zwei vollständig implementierten Bootstrap-Anbietern ausgeliefert.

Der DRT berücksichtigt die unmittelbaren Nachbarn eines Schlüssel besonderen. Die fünf nächstgelegenen Schlüssel sind numerisch kleiner, und die fünf nächsten Schlüssel, die numerisch größer als ein veröffentlichter Schlüssel sind, bilden eine Blatt Menge. Der DRT meldet mithilfe der DRT-API Änderungen an der Blatt Gruppe eines Schlüssels.

## <a name="drt-life-cycle-and-state-transitions"></a>DRT-Lebenszyklus und Zustandsübergänge

Eine Anwendung kann eine lokale DRT-Instanz mithilfe der [**drtopen**](/windows/desktop/api/drt/nf-drt-drtopen) -Funktion initialisieren. Diese Funktion löst den Bootstrapping-Prozess aus, bei dem die DRT-API auf dem Bootstrap-Anbieter aufruft, um die Schlüssel und Netzwerk Endpunkte anderer Knoten zu erlernen, die bereits an der DRT teilnehmen. Wenn der Bootstrap-Anbieter erfolgreich mindestens einen anderen Knoten eingibt, wechselt der DRT in den aktiven DRT- \_ Zustand. In diesem Zustand kann die Anwendung nach Schlüsseln suchen, die von anderen Knoten veröffentlicht werden, und es können Schlüssel veröffentlicht werden, die aufgelöst werden können. Wenn der Bootstrap-Anbieter andere Knoten nicht finden kann, wechselt der DRT in den \_ Zustand DRT allein. Der DRT bleibt im Zustand "DRT \_ allein", und es wird versucht, in regelmäßigen Abständen Bootstrap durchführen, um Peers zu finden und in den aktiven DRT-Zustand zu wechseln \_ .

Ein Knoten kann von DRT aktiv in diese Zustände übergehen \_ .

| Lebenszyklus Status | Bedingungen                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| nur DRT \_       | Der lokale Knoten hat keine anderen Knoten in der DRT erkannt. In diesem Status lauscht der Knoten weiterhin auf andere Knoten innerhalb des DRT.<br/> Wenn der DRT ein anderer Knoten Beitritt, wechselt der lokale Knoten in den aktiven DRT- \_ Zustand. Wenn das Netzwerk nicht herunter ist, geht es in "DRT \_ No Network" über \_ . Im Falle eines schwerwiegenden Fehlers mit der DRT wechselt der Knoten in den Zustand DRT \_ Faulted.<br/> |
| DRT \_ kein \_ Netzwerk | Wenn ein Knoten die Netzwerk Konnektivität verliert, wechselt er in den Zustand "DRT \_ ohne \_ Netzwerk". An diesem Punkt kann die Anwendung auf die Wiederherstellung der Netzwerkverbindung warten und das DRT schließen.<br/>                                                                                                                                                                                                                    |
| DRT \_ Faulted     | Schwerwiegender Fehler im lokalen Knoten. Beispielsweise, wenn der physische Arbeitsspeicher auf dem lokalen Computer nicht mehr vorhanden ist.<br/> Während ein Knoten in diesen Zustand versetzt wird, muss die Anwendung die [**drtclose**](/windows/desktop/api/drt/nf-drt-drtclose) -API anrufen, das Problem beheben und das DRT mit [**drtopen**](/windows/desktop/api/drt/nf-drt-drtopen)erneut initialisieren.<br/>                                                                                                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des Tabellen-API für verteilten Routing](using-the-distributed-routing-table-api.md)
</dt> <dt>

[Tabellen-API Referenz zu verteiltem Routing](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 




