---
title: Funktions Aufrufattribute
description: Programme können diese Attribute für einzelne Funktionen innerhalb der Schnittstelle verwenden und nur diese Funktion betreffen.
ms.assetid: c54dbcd9-46c9-4755-b4a8-0f78068920b7
keywords:
- IDL-Mittell, Attribute, Funktionsaufrufe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4d53407abf464d7b201c49d9cb2b1d3f3625b9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714082"
---
# <a name="function-call-attributes"></a>Funktions Aufrufattribute

Programme können diese Attribute für einzelne Funktionen innerhalb der Schnittstelle verwenden und nur diese Funktion betreffen.



| Attribut                        | Verbrauch                                                                                                                                                                                                                                                      |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Nachricht**](message.md)       | Der Remote Prozedur Aufrufe muss als asynchrone Meldung vom Client an den Server behandelt werden. Der Client führt den-Rückruf aus und gibt sofort zurück, während der tatsächliche-Rückruf vom Message Queueing-Transport ([**ncadg \_ MQ**](ncadg-mq.md)) verarbeitet wird. |
| [**auch**](maybe.md)           | Der Client, der diesen Remote Prozedur Vorgang durchführt, erwartet keine Antwort, die die Übermittlung oder den Abschluss des Aufrufes angibt. Dies steht im Gegensatz zu [**Nachrichten**](message.md) Vorgängen, bei denen keine Antwort erwartet wird, aber die Übermittlung gewährleistet ist.        |
| [**aus**](broadcast.md)   | Der Remote Prozedur Aufrufe muss an alle Server im Netzwerk gesendet werden. Der Client akzeptiert die erste Rückgabe, nachfolgende Antworten von anderen Servern werden verworfen.                                                                                    |
| [**idempotent**](idempotent.md) | Der Aufruf ändert den Status nicht und gibt die gleichen Informationen zurück, wenn er mit denselben Eingabe Parametern aufgerufen wird.                                                                                                                                     |
| [**Rückruf**](callback.md)     | Gibt eine Funktion an, die sich in der Client Anwendung befindet, die der Server zum Abrufen von Informationen vom Client abrufen kann.                                                                                                                             |
| [**aufzurufen \_ als**](call-as.md)      | Ordnet einem Remote Prozedur aufzurufen eine nicht Remote fähige Funktion zu.                                                                                                                                                                                                   |
| [**nah**](local.md)           | Gibt eine lokale Prozedur an, für die die-Klasse keinen Stub-Code generiert.                                                                                                                                                                                   |



 

Bei nicht-[**Objekt**](object.md) Schnittstellen können Sie auch das [**Kontext \_ handle**](context-handle.md) -Attribut auf eine Funktion anwenden, um die Eigenschaften des Rückgabewerts anzugeben.

 

 




