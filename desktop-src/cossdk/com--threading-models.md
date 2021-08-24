---
description: COM+-Threadingmodelle sind für eine Objektsammlung konzipiert, die als Apartment bezeichnet wird. Ein Apartment ist eine Sammlung von Kontexten, die in einem Prozess enthalten sind.
ms.assetid: c73fb4c5-20ae-4873-afd2-4f40eb47bade
title: COM+-Threadingmodelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd0949a27291be43b5981f24f4985fac6911937b2c9fa85785b4d662bd1bf546
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793675"
---
# <a name="com-threading-models"></a>COM+-Threadingmodelle

COM+-Threadingmodelle sind für eine Objektsammlung konzipiert, die als Apartment bezeichnet wird. Ein Apartment ist eine Sammlung von Kontexten, die in einem Prozess enthalten sind, wie in der folgenden Abbildung dargestellt.

![Diagramm, das eine Auflistung von Kontexten in einer Aktivität innerhalb eines Apartments innerhalb eines Prozesses zeigt.](images/6b86fe3b-262a-483a-a418-67d60f9a5d68.png)

Aufrufe innerhalb eines Apartments sind direkt, während Aufrufe zwischen Apartments (out-of-process) indirekt sind und Proxy- und Stubcode erfordern. Apartments ermöglichen Objekte mit unterschiedlichen Synchronisierungs- und Wiederinvarianzeigenschaften und weisen zwei Kategorien auf: Singlethread und Multithread. Objekte in einem Singlethread-Apartment (STA) werden für den bestimmten Thread ausgeführt, in dem sie erstellt wurden. STAs ermöglichen jeweils nur die Gleichzeitige Ausführung einer Methode. Sie sind für Benutzeroberflächen konzipiert und basieren auf der Microsoft Windows Nachrichtenwarteschlange, um eingehende Anrufe zu verarbeiten.

Objekte in einem Multithread-Apartment (MTA) werden in einem beliebigen Thread ausgeführt und ermöglichen die gleichzeitige Ausführung einer beliebigen Anzahl von Methoden. MTAs unterstützen die Reentrance implizit.

COM+-Klassen sind mit einer **ThreadingModel-Eigenschaft** markiert, die es COM+ ermöglicht, das Objekt im richtigen Apartment zu erstellen. Um zu bestimmen, in welchem Apartment ein Objekt erstellt wird, verwendet [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) die **ThreadingModel-Eigenschaft.**

Threads müssen [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) aufrufen, bevor sie COM+ verwenden können. Dadurch werden sie im richtigen Apartment und Kontext erstellt. Das Hauptthread-Apartment wird als erstes STA bestimmt, das von **CoInitializeEx** aufgerufen wird. Dies ist normalerweise dem Hauptthread eines Prozesses zugeordnet. **CoInitializeEx** gibt den Typ des Apartments an, der vom Thread benötigt wird, indem die folgenden Flags festgelegt werden:

-   **COINIT \_ MULTITHREADED**– Sucht den Thread im einzelnen Multithread-Apartment.
-   **COINIT \_ APARTMENTTHREADED**– Platziert den Thread in ein neues STA.

Die folgenden Themen in diesem Abschnitt enthalten weitere Informationen zur Verwendung von Threadingmodellen und Apartment in COM+:

-   [Threadingmodellattribut](threading-model-attribute.md)
-   [Neutrale Apartments](neutral-apartments.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Prozesse, Threads und Apartment](/windows/desktop/com/processes--threads--and-apartments)
</dt> <dt>

[**ThreadingModel**](components.md)
</dt> </dl>

 

 
