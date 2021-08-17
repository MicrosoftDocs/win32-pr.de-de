---
title: Verwalten der Objektlebensdauer durch Verweiszählung
description: Verwalten der Objektlebensdauer durch Verweiszählung
ms.assetid: 7f9da5a9-0435-431c-8f90-56e2e489c431
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 292f2c75352eef5680eb9a4d8367f76f88c19138dd834b71068740bee18f2315
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118310560"
---
# <a name="managing-object-lifetimes-through-reference-counting"></a>Verwalten der Objektlebensdauer durch Verweiszählung

In herkömmlichen Objektsystemen wird der Lebenszyklus von Objekten – d. h. die Probleme im Zusammenhang mit der Erstellung und Löschung von Objekten – implizit von der Sprache (oder der Laufzeit der Sprache) oder explizit von Anwendungsprogrammierern behandelt.

In einem ständig weiterentwickelten, weiterentwickelten System, das aus wiederverwendeten Komponenten besteht, ist es nicht mehr wahr, dass jeder Client oder sogar jeder Programmierer immer weiß, wie er mit der Lebensdauer einer Komponente umgehen kann. Für einen Client mit den richtigen Sicherheitsberechtigungen ist es immer noch relativ einfach, Objekte über eine einfache Anforderung zu erstellen, aber das Löschen von Objekten ist eine andere Frage. Es ist nicht unbedingt klar, wann ein Objekt nicht mehr benötigt wird und gelöscht werden sollte. (Leser, die mit Garbage Collection-Programmierumgebungen wie Java vertraut sind, können nicht zustimmen. Java-Objekte erstrecken sich jedoch nicht über Computer- oder sogar Prozessgrenzen, und daher ist die Garbage Collection auf Objekte beschränkt, die in einem einzelnen Prozessbereich leben. Darüber hinaus erzwingt Java die Verwendung einer einzelnen Programmiersprache.) Selbst wenn der ursprüngliche Client mit dem -Objekt fertig ist, kann er das Objekt nicht einfach herunterfahren, da einige andere Clients möglicherweise noch über einen Verweis darauf verfügen.

Eine Möglichkeit, sicherzustellen, dass ein Objekt nicht mehr benötigt wird, besteht in der vollständigen Abhängigkeit von einem zugrunde liegenden Kommunikationskanal, um das System zu informieren, wenn alle Verbindungen mit einem prozess- oder kanalübergreifenden Objekt nicht mehr möglich sind. Schemas, die diese Methode verwenden, sind jedoch aus verschiedenen Gründen nicht akzeptabel. Ein Problem ist, dass es einen größeren Unterschied zwischen dem prozessübergreifenden/netzwerkübergreifenden Programmiermodell und dem Einzelprozessprogrammiermodell erfordern könnte. Im prozessübergreifenden/netzwerkübergreifenden Programmiermodell stellt das Kommunikationssystem die Hooks zur Verfügung, die für die Verwaltung der Objektlebensdauer erforderlich sind, während objekte im Programmiermodell mit einem einzelnen Prozess direkt ohne einen intervenenden Kommunikationskanal verbunden sind. Ein weiteres Problem ist, dass dieses Schema auch zu einer Ebene von vom System bereitgestellter Software führen kann, die die Komponentenleistung im Prozessfall beeinträchtigen würde. Darüber hinaus würde ein Mechanismus, der auf expliziter Überwachung basiert, in der Regel nicht auf viele Tausende oder Millionen von Objekten skaliert.

COM bietet einen skalierbaren und verteilten Ansatz für diese Gruppe von Problemen. Clients teilen einem Objekt mit, wann es verwendet wird und wann es fertig ist, und Objekte löschen sich selbst, wenn sie nicht mehr benötigt werden. Dieser Ansatz macht es vor, dass alle Objekte Verweise auf sich selbst zählen. Programmiersprachen wie Java, die grundsätzlich über eigene Verwaltungsschemas für die Lebensdauer verfügen, z. B. garbage collection, können die COM-Verweiszählung verwenden, um COM-Objekte intern zu implementieren und zu verwenden, sodass der Programmierer diesen Umgang vermeiden kann.

So wie eine Anwendung Arbeitsspeicher frei geben muss, den sie zugeordnet hat, sobald der Arbeitsspeicher nicht mehr verwendet wird, ist ein Client eines Objekts dafür verantwortlich, seine Verweise auf das Objekt frei zu geben, wenn dieses Objekt nicht mehr benötigt wird. In einem objektorientierten System kann der Client dies nur tun, indem er dem Objekt eine Anweisung gibt, sich selbst frei zu geben.

Es ist wichtig, dass die Standortverteilung eines Objekts wieder auffing, wenn es nicht mehr verwendet wird. Die Schwierigkeit besteht darin, zu bestimmen, wann die Verlagerung eines Objekts sinnvoll ist. Dies ist bei automatischen Variablen (denen, die im Stapel zugeordnet sind) einfach– sie können nicht außerhalb des Blocks verwendet werden, in dem sie deklariert werden, sodass der Compiler sie wieder zu ihrer Verwendung auflistet, wenn das Ende des Blocks erreicht ist. Bei COM-Objekten, die dynamisch zugeordnet werden, müssen die Clients eines Objekts entscheiden, wann sie das Objekt nicht mehr verwenden müssen– insbesondere lokale oder Remoteobjekte, die möglicherweise von mehreren Clients gleichzeitig verwendet werden. Das -Objekt muss warten, bis alle Clients damit fertig sind, bevor es sich selbst frei gibt. Da COM-Objekte über Schnittstellenzeer bearbeitet werden und von Objekten in verschiedenen Prozessen oder auf anderen Computern verwendet werden können, kann das System die Clients eines Objekts nicht nachverfolgen.

Die Methode von COM, um zu bestimmen, wann die Entfernung eines Objekts angemessen ist, ist die manuelle Verweiszählung. Jedes -Objekt verwaltet einen Verweiszähler, der verfolgt, wie viele Clients mit ihm verbunden sind, d.&a; wie viele Zeiger auf eine seiner Schnittstellen in jedem Client vorhanden sind.

Weitere Informationen finden Sie in den folgenden Themen:

-   [Implementieren der Verweiszählung](implementing-reference-counting.md)
-   [Regeln zum Verwalten der Verweisanzahl](rules-for-managing-reference-counts.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden und Implementieren von IUnknown](using-and-implementing-iunknown.md)
</dt> </dl>

 

 




