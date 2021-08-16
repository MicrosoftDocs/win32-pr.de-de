---
title: Wiederverwendung von Objekten
description: Wiederverwendung von Objekten
ms.assetid: 07055fea-bdfe-4c7a-be07-2edcbf609dd9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71b6ef6d28b23ff2fcda5ed46d9b99a6634389793e48275c36e2f8a708f7266d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118309421"
---
# <a name="reusing-objects"></a>Wiederverwendung von Objekten

Ein wichtiges Ziel jedes Objektmodells ist es, Objektautoren die Wiederverwendung und Erweiterung von Objekten zu ermöglichen, die von anderen als Teile ihrer eigenen Implementierungen bereitgestellt werden. Eine Möglichkeit, dies in Microsoft Visual C++ und anderen Sprachen zu tun, ist die Implementierungsvererbung, die es einem Objekt ermöglicht, einige seiner Funktionen von einem anderen Objekt zu erben ("Unterklasse"), während andere Funktionen überschrieben werden.

Das Problem bei der systemweiten Objektinteraktion mit herkömmlicher Implementierungsvererbung ist, dass der Vertrag (die Schnittstelle) zwischen Objekten in einer Implementierungshierarchie nicht eindeutig definiert ist. Tatsächlich ist es implizit und mehrdeutig. Wenn das übergeordnete oder untergeordnete Objekt seine Implementierung ändert, kann das Verhalten verwandter Komponenten undefiniert oder unteilbar implementiert werden. In jeder einzelnen Anwendung, in der die Implementierung von einem einzelnen Entwicklungsteam verwaltet werden kann, das alle Komponenten gleichzeitig aktualisiert, ist dies nicht immer ein hauptanliegend. In einer Umgebung, in der die Komponenten eines Teams durch die Blackbox-Wiederverwendung anderer Komponenten erstellt werden, die von anderen Teams erstellt wurden, gefährdet diese Art von Instabilität die Wiederverwendung. Darüber hinaus funktioniert die Implementierungsvererbung in der Regel nur innerhalb von Prozessgrenzen. Dies macht die herkömmliche Implementierungsvererbung für große, sich entwickelnde Systeme, die aus Softwarekomponenten bestehen, die von vielen Entwicklungsteams erstellt wurden, unpraktisch.

Der Schlüssel zum Erstellen wiederverwendbarer Komponenten besteht in der Möglichkeit, das Objekt als nicht transparente Box zu behandeln. Dies bedeutet, dass der Code, der versucht, ein anderes Objekt wiederzuverwenden, nichts über die interne Struktur oder Implementierung der verwendeten Komponente weiß und nichts wissen muss. Anders ausgedrückt: Der Code, der versucht, eine Komponente wiederzuverwenden, hängt vom Verhalten des Objekts und nicht von seiner genauen Implementierung ab.

Um eine Blackbox-Wiederverwendbarkeit zu erreichen, übernimmt COM andere eingerichtete Wiederverwendbarkeitsmechanismen, z. B. *Ein-/Delegierung* und *Aggregation.*

> [!NOTE]  
> Der Einfachheit halber wird das  objekt, das wiederverwendet wird, als inneres Objekt bezeichnet, und das Objekt, das dieses innere Objekt verwendet, ist das *äußere Objekt*.

 

Es ist wichtig, sich in beiden Mechanismen daran zu erinnern, wie das äußere Objekt seinen Clients angezeigt wird. Für die Clients implementieren beide Objekte alle Schnittstellen, auf die der Client einen Zeiger erhalten kann. Der Client behandelt das äußere Objekt als ein nicht transparentes Feld und ist daher weder für die interne Struktur des äußeren Objekts wichtig, noch muss er sich um die interne Struktur des äußeren Objekts kümmern– der Client kümmert sich nur um das Verhalten.

Weitere Informationen finden Sie in den folgenden Themen:

-   [Ein-/Delegierung](containment-delegation.md)
-   [Aggregation](aggregation.md)

 

 




