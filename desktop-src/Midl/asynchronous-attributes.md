---
title: Asynchrone Attribute
description: Wenn ein Programm eine Prozedur in einer Schnittstelle aufruft, kann die Prozedur synchron oder asynchron ausgeführt werden.
ms.assetid: 3e6c6c13-1524-41b2-96dc-3885eadb847c
keywords:
- IDL MIDL , Attribute MIDL , asynchron
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14ad045be5c3f5980c99fac0e924181c31ae7859f801608c7bb53fe3d81a2b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807853"
---
# <a name="asynchronous-attributes"></a>Asynchrone Attribute

Wenn ein Programm eine Prozedur in einer Schnittstelle aufruft, kann die Prozedur synchron oder asynchron ausgeführt werden. Eine synchrone Prozedur bewirkt, dass das aufrufende Programm wartet, bis die Prozedur zurückgegeben wird, bevor das Programm fortgesetzt werden kann. Eine asynchrone Prozedur wird sofort zurückgegeben, ohne auf Ergebnisse zu warten. Das aufrufende Programm muss später mit der Schnittstellenprozedur neu synchronisiert werden, um Daten zu empfangen. Weitere Informationen finden Sie unter Asynchronous [RPC](/windows/desktop/Rpc/asynchronous-rpc).

Sie können die folgenden Attribute verwenden, um asynchrone Remoteprozeduraufrufe zu unterstützen.



| attribute                         | Verwendung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Asynchrone**](async.md)            | Definiert bei Anwendung auf einen Funktionsparameter ein Handle, mit dem der Aufrufer einen asynchronen Aufruf ausführen und sofort zurückkehren kann, ohne auf Ergebnisse zu warten, und später mit der aufgerufenen Funktion neu synchronisiert wird, um Daten nach Abschluss des Aufrufs zu empfangen. Das [**asynchrone**](async.md) Attribut wird auch in ACF-Dateien verwendet, um ein asynchrones Handle für eine Prozedur oder eine gesamte Schnittstelle zu definieren. Bei COM-Schnittstellen ist diese Schnittstelle veraltet und kann nicht für neue Schnittstellen verwendet werden. |
| [**Async \_ uuid**](async-uuid.md) | Leitet den MIDL-Compiler an, sowohl synchrone als auch asynchrone Versionen einer COM-Schnittstelle zu definieren.                                                                                                                                                                                                                                                                                                                                                                                      |
| [**Vielleicht**](maybe.md)            | Der Client, der diesen Remoteprozeduraufruf vorgibt, erwartet keine Antwort, die auf die Übermittlung oder den Abschluss des Aufrufs hinweist, und die Übermittlung ist nicht garantiert. Dies steht im Gegensatz zu **Nachrichtenvorgängen,** bei denen keine Antwort erwartet wird, die Übermittlung jedoch garantiert ist.                                                                                                                                                                                                                    |
| [**Nachricht**](message.md)        | Der Remoteprozeduraufruf soll als asynchrone Nachricht vom Client an den Server behandelt werden. Der Client macht den Aufruf und gibt sofort zurück, während der tatsächliche Aufruf vom Message Queuing-Transport ([**ncadg mq ) \_ verarbeitet wird.**](ncadg-mq.md)                                                                                                                                                                                                                              |



 

 

 