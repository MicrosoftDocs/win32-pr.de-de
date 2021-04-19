---
title: Verwalten von Objekt Lebensdauern durch Verweis Zählung
description: Verwalten von Objekt Lebensdauern durch Verweis Zählung
ms.assetid: 7f9da5a9-0435-431c-8f90-56e2e489c431
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aac184baea9198721e6cdf9c0444a8c6431db08
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2020
ms.locfileid: "106338248"
---
# <a name="managing-object-lifetimes-through-reference-counting"></a>Verwalten von Objekt Lebensdauern durch Verweis Zählung

In herkömmlichen Objekt Systemen wird der Lebenszyklus von Objekten – d. h. die Probleme im Zusammenhang mit der Erstellung und Löschung von Objekten – implizit von der Sprache (oder der Sprachlaufzeit) oder explizit von Anwendungs Programmierern behandelt.

In einem weiter entwickelten, dezentral konstruierten System, das aus wiederverwendeten Komponenten besteht, ist es nicht mehr wahr, dass ein Client oder sogar ein Programmierer immer "weiß", wie die Lebensdauer einer Komponente behandelt werden soll. Für einen Client mit den richtigen Sicherheits Berechtigungen ist es immer noch relativ einfach, Objekte über eine einfache Anforderung zu erstellen. das Löschen von Objekten ist jedoch eine andere Sache. Es ist nicht unbedingt klar, wenn ein Objekt nicht mehr benötigt wird und gelöscht werden soll. (Leser, die mit der Garbage Collection vertraut sind, wie z. b. Java, unterliegen möglicherweise nicht, aber Java-Objekte umfassen keine Computer-oder sogar Prozess Grenzen, und daher ist die Garbage Collection auf Objekte beschränkt, die innerhalb eines einzelnen Prozess Raums Leben. Außerdem erzwingt Java die Verwendung einer einzelnen Programmiersprache.) Auch wenn der ursprüngliche Client mit dem-Objekt ausgeführt wird, kann das Objekt nicht einfach heruntergefahren werden, da einige andere Clients oder Clients möglicherweise noch einen Verweis darauf haben.

Eine Möglichkeit, um sicherzustellen, dass ein Objekt nicht mehr benötigt wird, besteht darin, vollständig von einem zugrunde liegenden Kommunikationskanal zu abhängen, um das System zu informieren, wenn alle Verbindungen zu einem prozessübergreifenden oder kanalübergreifenden Objekt verschwunden sind. Allerdings sind Schemas, die diese Methode verwenden, aus verschiedenen Gründen nicht zulässig. Ein Problem besteht darin, dass es einen wesentlichen Unterschied zwischen dem prozessübergreifenden/Netzwerk übergreifenden Programmiermodell und dem Programmiermodell mit einem einzelnen Prozess erfordern könnte. Im prozessübergreifenden/Netzwerk übergreifenden Programmiermodell stellt das Kommunikationssystem die für die Verwaltung der Objekt Lebensdauer erforderlichen Hooks bereit, während die Objekte im Einzel Prozess-Programmiermodell direkt ohne einen Beteiligten Kommunikationskanal verbunden sind. Ein weiteres Problem besteht darin, dass dieses Schema auch zu einer Ebene der vom System bereitgestellten Software führen könnte, die die Komponenten Leistung in der Prozess internen Groß-/Kleinschreibung beeinträchtigt. Außerdem würde ein Mechanismus, der auf der expliziten Überwachung basiert, tendenziell nicht in Bezug auf Tausende oder Millionen von Objekten skaliert werden.

COM bietet einen skalierbaren und verteilten Ansatz zu diesem Satz von Problemen. Clients weisen ein Objekt an, wenn es verwendet wird, und wenn es abgeschlossen ist, und Objekte löschen sich selbst, wenn Sie nicht mehr benötigt werden. Dieser Ansatz gibt an, dass alle Objekte auf sich selbst verweisen. Programmiersprachen, wie z. b. Java, die von Natur aus über eigene Lebensdauer Verwaltungs Schemas verfügen, wie z. b. Garbage Collection, können COM-Objekte verwenden, um COM-Objekte intern zu implementieren und zu verwenden, sodass der Programmierer keinen Umgang mit diesem

Ebenso wie eine Anwendung Arbeitsspeicher freigeben muss, nachdem der Arbeitsspeicher nicht mehr verwendet wird, ist der Client eines Objekts dafür verantwortlich, seine Verweise auf das Objekt freizugeben, wenn das Objekt nicht mehr benötigt wird. In einem objektorientierten System kann der Client dies nur durchführen, indem er dem Objekt eine Anweisung zum Freigeben von sich selbst erteilt.

Es ist wichtig, dass die Zuordnung eines Objekts aufgehoben wird, wenn es nicht mehr verwendet wird. Die Schwierigkeit besteht darin, zu bestimmen, wann das Zuweisen eines Objekts angebracht ist. Dies ist mit automatischen Variablen (auf dem Stapel zugeordnete Variablen) leicht – Sie können nicht außerhalb des Blocks verwendet werden, in dem Sie deklariert sind, sodass der Compiler Sie zuordnet, wenn das Ende des Blocks erreicht ist. Bei COM-Objekten, die dynamisch zugeordnet werden, müssen die Clients eines Objekts entscheiden, wann das Objekt nicht mehr verwendet werden muss – insbesondere lokale oder Remote Objekte, die möglicherweise gleichzeitig von mehreren Clients verwendet werden. Das Objekt muss warten, bis alle Clients damit fertig sind, bevor es freigegeben wird. Da com-Objekte über Schnittstellen Zeiger manipuliert werden und von Objekten in verschiedenen Prozessen oder anderen Computern verwendet werden können, kann das System die Clients eines Objekts nicht nachverfolgen.

Die com-Methode, um zu bestimmen, wann es angemessen ist, das Zuordnen eines Objekts zu übernehmen, ist die manuelle Verweis Zählung Jedes Objekt verwaltet einen Verweis Zähler, der nachverfolgt, wie viele Clients mit dem Objekt verbunden sind, d. h., wie viele Zeiger auf eine beliebige Schnittstelle in einem beliebigen Client vorhanden sind.

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Implementieren der Verweis Zählung](implementing-reference-counting.md)
-   [Regeln für die Verwaltung von Verweis Zählungen](rules-for-managing-reference-counts.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden und Implementieren von IUnknown](using-and-implementing-iunknown.md)
</dt> </dl>

 

 




