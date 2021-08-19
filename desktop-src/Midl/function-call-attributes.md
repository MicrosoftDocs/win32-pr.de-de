---
title: Funktionsaufrufattribute
description: Programme können diese Attribute für einzelne Funktionen innerhalb der Schnittstelle verwenden und wirken sich nur auf diese Funktion aus.
ms.assetid: c54dbcd9-46c9-4755-b4a8-0f78068920b7
keywords:
- IDL MIDL , Attribute, Funktionsaufruf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a3800b62bb6b94aac330ecf0b06761d62227a4ed6100f2fabdde5b61cd952d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895310"
---
# <a name="function-call-attributes"></a>Funktionsaufrufattribute

Programme können diese Attribute für einzelne Funktionen innerhalb der Schnittstelle verwenden und wirken sich nur auf diese Funktion aus.



| attribute                        | Verbrauch                                                                                                                                                                                                                                                      |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Nachricht**](message.md)       | Der Remoteprozeduraufruf muss als asynchrone Nachricht vom Client an den Server behandelt werden. Der Client nimmt den Aufruf vor und gibt sofort zurück, während der tatsächliche Aufruf vom Message Queuing-Transport ([**ncadg \_ mq**](ncadg-mq.md)) verarbeitet wird. |
| [**Vielleicht**](maybe.md)           | Der Client, der diesen Remoteprozeduraufruf vornimmt, erwartet keine Antwort, die die Übermittlung oder den Abschluss des Aufrufs angibt. Dies steht im Gegensatz zu [**Nachrichtenvorgängen,**](message.md) bei denen keine Antwort erwartet wird, die Übermittlung jedoch garantiert ist.        |
| [**Sendung**](broadcast.md)   | Der Remoteprozeduraufruf muss an alle Server im Netzwerk gesendet werden. Der Client akzeptiert die erste Rückgabe, nachfolgende Antworten von anderen Servern werden verworfen.                                                                                    |
| [**idempotent**](idempotent.md) | Der Aufruf ändert den Zustand nicht und gibt bei jedem Aufruf mit denselben Eingabeparametern die gleichen Informationen zurück.                                                                                                                                     |
| [**Rückruf**](callback.md)     | Legt eine Funktion fest, die sich in der Clientanwendung befindet, die der Server aufrufen kann, um Informationen vom Client abzurufen.                                                                                                                             |
| [**aufrufen \_ als**](call-as.md)      | Karten eine nicht remotefähige Funktion zu einem Remoteprozeduraufruf.                                                                                                                                                                                                   |
| [**lokal**](local.md)           | Legt eine lokale Prozedur fest, für die MIDL keinen Stubcode generiert.                                                                                                                                                                                   |



 

Bei [**Nicht-Objektschnittstellen**](object.md) können Sie auch das [**\_ Kontexthandleattribut**](context-handle.md) auf eine Funktion anwenden, um Merkmale des Rückgabewerts anzugeben.

 

 




