---
title: Wieder verwenden von Objekten
description: Wieder verwenden von Objekten
ms.assetid: 07055fea-bdfe-4c7a-be07-2edcbf609dd9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03a830eb539823b0350c9ce41a096cda821bb0cb
ms.sourcegitcommit: 917c90b6ed4af323fedada331211b40396876424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/08/2020
ms.locfileid: "104516695"
---
# <a name="reusing-objects"></a>Wieder verwenden von Objekten

Ein wichtiges Ziel eines Objektmodells besteht darin, Objekt Autoren die Wiederverwendung und Erweiterung von Objekten zu ermöglichen, die von anderen Benutzern als Teile ihrer eigenen Implementierungen bereitgestellt werden. Eine Möglichkeit, dies in Microsoft Visual C++ und anderen Sprachen zu erreichen, ist die Verwendung der *Implementierungsvererbung*, mit der ein Objekt einige seiner Funktionen von einem anderen Objekt erben kann, während andere Funktionen außer Kraft gesetzt werden.

Das Problem bei der systemweiten Objekt Interaktion mit herkömmlicher Implementierungs Vererbung besteht darin, dass der Vertrag (die Schnittstelle) zwischen Objekten in einer Implementierungs Hierarchie nicht eindeutig definiert ist. Tatsächlich ist Sie implizit und mehrdeutig. Wenn das übergeordnete oder untergeordnete Objekt seine Implementierung ändert, kann das Verhalten verwandter Komponenten nicht definiert oder nicht dauerhaft implementiert werden. In jeder einzelnen Anwendung, in der die Implementierung von einem einzelnen Engineering-Team verwaltet werden kann, das alle Komponenten gleichzeitig aktualisiert, ist dies nicht immer ein wichtiger Grund. In einer Umgebung, in der die Komponenten eines Teams durch die Wiederverwendung durch Blackbox anderer von anderen Teams erstellter Komponenten erstellt werden, gefährdet diese Art von Instabilität die Wiederverwendung. Außerdem funktioniert die Implementierungs Vererbung in der Regel nur innerhalb der Prozess Grenzen. Dadurch wird die herkömmliche Implementierungs Vererbung für große, sich entwickelnde Systeme, die aus den von vielen Engineering Teams erstellten Softwarekomponenten bestehen, nicht praktikabel.

Der Schlüssel zum Aufbau wiederverwendbarer Komponenten ist, dass das Objekt als undurchsichtiges Feld behandelt werden kann. Dies bedeutet, dass der Code Abschnitt, der versucht, ein anderes Objekt wiederzuverwenden, nichts kennt und nichts über die interne Struktur oder Implementierung der verwendeten Komponente wissen muss. Anders ausgedrückt: der Code, der versucht, eine Komponente wiederzuverwenden, hängt vom Verhalten des Objekts und nicht von der exakten Implementierung ab.

Um die Wiederverwendbarkeit von Blackbox zu erreichen, übernimmt com andere bewährte Mechanismen für die Wiederverwendbarkeit *, wie z* *. b*

> [!NOTE]  
> Der Zweck wird das Objekt, das wieder verwendet wird, als internes *Objekt* bezeichnet, und das Objekt, das dieses innere Objekt verwendet, ist das *äußere Objekt*.

 

Es ist wichtig, sich in beiden Mechanismen daran zu erinnern, wie das äußere Objekt seinen Clients angezeigt wird. Wenn die Clients betroffen sind, implementieren beide Objekte alle Schnittstellen, auf die der Client einen Zeiger erhalten kann. Der Client behandelt das äußere Objekt als ein undurchsichtiges Feld und ist daher nicht relevant, und es muss sich nicht um die interne Struktur des äußeren Objekts kümmern. "der Client kümmert sich nur um das Verhalten.

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Einschluss/Delegierung](containment-delegation.md)
-   [Aggregation](aggregation.md)

 

 




