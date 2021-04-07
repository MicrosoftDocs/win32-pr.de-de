---
description: Entwickeln von Komponenten in der Warteschlange
ms.assetid: 867b7512-82ad-4877-8675-aa2d7e62ff8a
title: Entwickeln von Komponenten in der Warteschlange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8808ef3e6cba8ff561dd94473fca8f00631081f2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748041"
---
# <a name="developing-queued-components"></a>Entwickeln von Komponenten in der Warteschlange

Der in der Warteschlange befindliche Komponenten Dienst erfordert, dass alle Anwendungsmethoden nur \[ in \] Parameter ohne Rückgabewerte enthalten. Da das Server Objekt nicht notwendigerweise verfügbar ist, wenn der Client den-Befehl ausführt, können Server Ergebnisse zurückgegeben werden, indem eine Nachricht gesendet wird, die ein anderes-Objekt erstellt. Auf diese Weise erfolgt die bidirektionale Kommunikation nicht in jedem Fall, sondern nur, wenn dies erforderlich ist, durch eine Reihe von unidirektionalen Nachrichten zwischen Objekten.

Wenn Sie den com+-Dienst in der Warteschlange verwenden möchten, müssen Sie den [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) -Dienst bereits installiert haben. Message Queuing wird nicht automatisch installiert. Message Queuing müssen während der Einrichtung des Betriebssystems **oder mithilfe der** Option "Software" ausgewählt werden. Ein internes Message Queuing Zertifikat wird bei der Anmeldung automatisch erstellt.

Die in der folgenden Tabelle beschriebenen Themen enthalten weitere Überlegungen zu spezielleren Situationen.



| Thema                                                                                           | BESCHREIBUNG                                                                                            |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Übergeben von Objekten als Parameter](passing-objects-as-parameters.md)s<br/>                   | Beschreibt, wie-Objekte als \[ \] Parameter an in die Warteschlange eingereihte Komponenten übergeben werden.<br/>                    |
| [Sicherheitseinschränkungen im Arbeitsgruppen Modus](security-limitations-in-workgroup-mode.md)<br/> | Beschreibt Einschränkungen bei der Verwendung von Message Queuing Authentifizierung im Arbeitsgruppen Modus.<br/>       |
| [Überlegungen zum Threading](threading-considerations.md)<br/>                             | Beschreibt bestimmte Probleme im Zusammenhang mit der Übergabe von Aufzeichnungs Schnittstellen Zeigern zwischen Threads.<br/> |
| [Empfangen einer Antwort](receiving-a-response.md)<br/>                                     | Beschreibt das Erstellen einer Antwort auf einen in der Warteschlange befindlichen Komponenten Aufruf.<br/>                           |



 

 

 




