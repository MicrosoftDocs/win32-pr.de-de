---
description: Com+-Threading Modelle werden um eine Objektsammlung entworfen, die als Apartment bezeichnet wird. Ein Apartment ist eine Sammlung von Kontexten, die in einem Prozess enthalten sind.
ms.assetid: c73fb4c5-20ae-4873-afd2-4f40eb47bade
title: Com+-Threading Modelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5f07b065861c042e68add633368a9c8b8ba41b2
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "103761115"
---
# <a name="com-threading-models"></a>Com+-Threading Modelle

Com+-Threading Modelle werden um eine Objektsammlung entworfen, die als Apartment bezeichnet wird. Ein Apartment ist eine Auflistung von Kontexten, die in einem Prozess enthalten sind, wie in der folgenden Abbildung dargestellt.

![Diagramm, das eine Auflistung von Kontexten in einer Aktivität in einem Apartment innerhalb eines Prozesses anzeigt.](images/6b86fe3b-262a-483a-a418-67d60f9a5d68.png)

Aufrufe innerhalb eines Apartment sind direkt, während Aufrufe über mehrere Apartments hinweg (Prozess übergreifend) indirekt sind und Proxy-und Stub-Code erfordern. Apartments lassen Objekte mit unterschiedlichen Synchronisierungs-und Eintritts Eigenschaften zu und haben zwei Kategorien: Single Thread und Multithreaded. Objekte in einem Single Thread-Apartment (STA) werden auf dem jeweiligen Thread ausgeführt, in dem Sie erstellt wurden. Mit Stas kann jeweils nur eine Methode gleichzeitig ausgeführt werden. Sie sind auf Benutzeroberflächen ausgelegt und verlassen sich auf die Microsoft Windows-Nachrichten Warteschlange, um eingehende Aufrufe zu verarbeiten.

Objekte in einem Multithread-Apartment (MTA) werden in einem beliebigen Thread ausgeführt, sodass eine beliebige Anzahl von Methoden gleichzeitig erfolgen kann. MTAs unterstützen implizit den erneuten Zutritt.

Com+-Klassen sind mit einer **ThreadingModel** -Eigenschaft gekennzeichnet, mit der com+ das Objekt im richtigen Apartment erstellen kann. Um zu ermitteln, in welchem Apartment ein Objekt erstellt wird, verwendet [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) die **ThreadingModel** -Eigenschaft.

Threads müssen [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) aufrufen, bevor Sie com+ verwenden können. Dadurch werden Sie im richtigen Apartment und Kontext erstellt. Das Haupt Thread Apartment wird als erster von **CoInitializeEx** aufgerufener STA festgelegt. Dies ist normalerweise dem Haupt Thread eines Prozesses zugeordnet. **CoInitializeEx** gibt den Typ des Apartment an, das für den Thread erforderlich ist, indem die folgenden Flags festgelegt werden:

-   **Coinit \_ Multithread**– der Thread wird im einzelnen Multithread-Apartment lokalisiert.
-   **Coinit \_ Apartmentthreaded**– platziert den Thread in einem neuen Sta.

Die folgenden Themen in diesem Abschnitt enthalten weitere Informationen zur Verwendung von Threading Modellen und-Apartments in com+:

-   [Threading Modell-Attribut](threading-model-attribute.md)
-   [Neutrale Apartments](neutral-apartments.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Prozesse, Threads und Apartments](/windows/desktop/com/processes--threads--and-apartments)
</dt> <dt>

[**Threading Model**](components.md)
</dt> </dl>

 

 
