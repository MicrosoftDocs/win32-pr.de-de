---
title: Prüfsummen und Objekt Anzahl
description: Prüfsummen und Objekt Anzahlen sind Erkennungs Strategien, die es einer Anwendung ermöglichen, einen teilweisen Update Status zu erkennen.
ms.assetid: 14829a74-c186-4250-beac-036c5ecc5913
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc643ec7cd896a7c73df0be5738887a330392140
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104470756"
---
# <a name="checksums-and-object-counts"></a>Prüfsummen und Objekt Anzahl

Prüfsummen und Objekt Anzahlen sind Erkennungs Strategien, die es einer Anwendung ermöglichen, einen teilweisen Update Status zu erkennen. Prüfsummen können auch zum Erkennen von Inkonsistenzen verwendet werden, die durch die Konfliktlösung Sowohl Prüfsummen als auch Objekt Zählungen erfordern einen Speicherort zum Speichern des Werts, der zum Überprüfen einer Prüfsumme oder Objekt Anzahl verwendet wird. Dies kann sich auf einem "Master"-Objekt befinden, das für die anwendungsspezifische Beziehung oder für ein übergeordnetes Objekt ausgewählt ist, unter dem die verknüpften Objekte gespeichert werden.

Für Prüfsummen überprüfen Anwendungen, die die verknüpften Objekte lesen, die Prüfsumme, indem Sie ein lokales Ergebnis berechnen und mit dem gespeicherten Wert vergleichen. Wenn die Werte nicht identisch sind, befindet sich das Replikat in einem teilweisen Update Status, und die Objekte können nicht verwendet werden.

Bei der Objekt Anzahl zählen Anwendungen zum zählen der verknüpften Objekte (in der Regel untergeordnete Elemente eines einzelnen übergeordneten Elements) und vergleichen die Anzahl mit dem gespeicherten Wert. Wenn die Anzahl nicht stimmt, befindet sich das Replikat in einem teilweisen Update Status, und die Objekte können nicht verwendet werden.

Wichtige Hinweise:

-   Damit der Prüfsummen Ansatz funktioniert, muss mindestens ein Attribut, das zum Berechnen der Prüfsumme verwendet wird, aktualisiert werden. Der Algorithmus, der zum Berechnen der Prüfsumme verwendet wird, muss die Unterschiede in der Eingabe zuverlässig widerspiegeln. Wenn viele verschiedene Eingaben die gleiche Prüfsumme haben, erkennt der Algorithmus teilweise Updates nicht zuverlässig. Die Eingabe mit Werten wie der **objectGUID** des Quell Computers und dem Datum und der Uhrzeit des Updates sind ebenfalls hilfreich.
-   Objekt Zähler funktionieren am besten, wenn Sie mit neuen Objekt Sätzen oder in Kombination mit Konsistenz-GUIDs verwendet werden (Weitere Informationen finden Sie im nächsten Abschnitt). Die Anwendung, die das Update durchführt, muss entweder die Anzahl der Objekte, die sich im Container befinden, wenn das Update abgeschlossen ist, oder eine andere Methode zum Kennzeichnen des Containers beim Fortsetzen des Updates verwenden (z. b. wenn die Anzahl auf NULL festgelegt wird). Nachdem Sie das Update abgeschlossen haben, markiert die Quell Anwendung den Container mit der Anzahl der enthaltenen Objekte.

 

 




