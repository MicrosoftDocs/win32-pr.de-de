---
description: Empfangen einer Antwort
ms.assetid: 48919608-a102-43e2-9ca0-80b17344b5eb
title: Empfangen einer Antwort
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3423f54688fc3894f0d0876eb54cd6f57ffb2a5313c4c9e78b357dfc7676f33c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119381120"
---
# <a name="receiving-a-response"></a>Empfangen einer Antwort

Da Komponenten in der Warteschlange asynchron funktionieren, sollten Clientanwendungen nicht blockiert werden, während auf eine Antwort von einer Anforderung in der Warteschlange gewartet wird. Dennoch ist es häufig hilfreich, wenn die Clientanwendung oder eine zugehörige Anwendung auf dem Clientcomputer schließlich eine Antwort erhält. Beispielsweise kann ein Client benachrichtigt werden, wenn eine angeforderte Transaktion erfolgreich abgeschlossen wurde.

Es gibt eine Vielzahl von Möglichkeiten für eine Komponente in der Warteschlange, eine Antwort asynchron zurück an den Aufrufer zu senden. Beispielsweise könnte eine E-Mail gesendet werden. Alternativ kann der Server lose gekoppelte Ereignisse veröffentlichen, die der Client abonnieren kann.

Eine andere Möglichkeit für einen Client, eine Antwort von einer Warteschlangenkomponente zu erhalten, die auf einem Server ausgeführt wird, besteht im Übergeben der aufgerufenen Methode an ein Benachrichtigungsobjekt. Ein Benachrichtigungsobjekt ist eine Instanz einer Komponente in der Warteschlange, die auf dem Client ausgeführt wird. Ein solches Benachrichtigungsobjekt ist möglicherweise recht einfach und enthält nur eine ganze Zahl, die zur Darstellung eines Fehlerwerts verwendet wird, oder es ist recht komplex und enthält alle Informationen, die zum Rollback einer Transaktion auf dem Client erforderlich sind. In beiden Fällen übergibt der aufrufende Client ein Benachrichtigungsobjekt als Eingabeparameter, wenn er eine Antwort von einer komponente in der Warteschlange erhalten möchte, die auf einem Server ausgeführt wird. Da das Benachrichtigungsobjekt in die Warteschlange gestellt wird, kann der Server für seine Methoden aufrufen, um seinen Zustand zu ändern, der anschließend vom Client ausgelesen werden kann. In diesem Szenario wird der COM+-Komponentendienst in der Warteschlange sowohl auf dem Client als auch auf dem Server verwendet, um asynchrone Kommunikation in beide Richtungen zu ermöglichen.

 

 



