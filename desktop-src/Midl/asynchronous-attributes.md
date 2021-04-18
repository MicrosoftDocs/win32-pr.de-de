---
title: Asynchrone Attribute
description: Wenn ein Programm eine Prozedur in einer Schnittstelle aufruft, kann die Prozedur synchron oder asynchron ausgeführt werden.
ms.assetid: 3e6c6c13-1524-41b2-96dc-3885eadb847c
keywords:
- IDL-Mittell, Attribute-mittlerer l, asynchronen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00aca2276bf1fa5178f1dca3ae4803544066d983
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106337424"
---
# <a name="asynchronous-attributes"></a>Asynchrone Attribute

Wenn ein Programm eine Prozedur in einer Schnittstelle aufruft, kann die Prozedur synchron oder asynchron ausgeführt werden. Eine synchrone Prozedur bewirkt, dass das aufrufende Programm wartet, bis die Prozedur zurückkehrt, bevor das Programm fortfahren kann. Eine asynchrone Prozedur wird sofort zurückgegeben, ohne auf Ergebnisse zu warten. Das aufrufende Programm muss zu einem späteren Zeitpunkt erneut mit der Schnittstellen Prozedur synchronisiert werden, um Daten zu empfangen. Weitere Informationen finden Sie unter [Asynchronous RPC](/windows/desktop/Rpc/asynchronous-rpc).

Sie können die folgenden Attribute verwenden, um die Unterstützung für asynchrone Remote Prozedur Aufrufe bereitzustellen.



| Attribut                         | Verbrauch                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**async**](async.md)            | Definiert bei Anwendung auf einen Funktionsparameter ein Handle, das dem Aufrufer das Ausführen eines asynchronen Aufrufs ermöglicht und sofort zurückgegeben wird, ohne auf Ergebnisse zu warten, und eine spätere Synchronisierung mit der aufgerufenen Funktion, um Daten zu empfangen, nachdem der Aufruf abgeschlossen wurde. Das [**Async**](async.md) -Attribut wird auch in ACF-Dateien verwendet, um ein asynchrones Handle für eine Prozedur oder eine gesamte Schnittstelle zu definieren. Bei COM-Schnittstellen ist diese Schnittstelle veraltet und kann nicht für neue Schnittstellen verwendet werden. |
| [**Async- \_ UUID**](async-uuid.md) | Weist den Mittel l-Compiler an, sowohl synchrone als auch asynchrone Versionen einer COM-Schnittstelle zu definieren.                                                                                                                                                                                                                                                                                                                                                                                      |
| [**auch**](maybe.md)            | Der Client, der diesen Remote Prozedur Vorgang durchführt, erwartet keine Antwort, die die Übermittlung oder den Abschluss des Aufrufes anzeigt, und die Übermittlung ist nicht garantiert. Dies steht im Gegensatz zu **Nachrichten** Vorgängen, bei denen keine Antwort erwartet wird, aber die Übermittlung gewährleistet ist.                                                                                                                                                                                                                    |
| [**Nachricht**](message.md)        | Der Remote Prozedur Aufrufe muss als asynchrone Meldung vom Client an den Server behandelt werden. Der Client führt den-Rückruf aus und gibt sofort zurück, während der tatsächliche-Rückruf vom Message Queueing-Transport ([**ncadg \_ MQ**](ncadg-mq.md)) verarbeitet wird.                                                                                                                                                                                                                              |



 

 

 