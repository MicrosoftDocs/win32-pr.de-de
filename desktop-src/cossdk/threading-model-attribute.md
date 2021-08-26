---
description: COM+ verwaltet Threads für Sie. Jede COM-Komponente verfügt über eine ThreadingModel-Eigenschaft, die Sie beim Entwickeln der Komponente angeben können. Diese Eigenschaft bestimmt, wie die Komponentenobjekte Threads für die Methodenausführung zugewiesen werden.
ms.assetid: 5fae8475-3d2e-4939-80a7-bc9a677a50b3
title: Threadingmodellattribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dba6ae625e4413516066f7180a4eb6870fe4f90df38947fc2476cfbcc7dfadb3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070240"
---
# <a name="threading-model-attribute"></a>Threadingmodellattribut

COM+ verwaltet Threads für Sie. Jede COM-Komponente verfügt über eine **ThreadingModel-Eigenschaft,** die Sie beim Entwickeln der Komponente angeben können. Diese Eigenschaft bestimmt, wie die Objekte der Komponente Threads für die Methodenausführung zugewiesen werden.

Sie können das Component Services-Verwaltungstool verwenden, um die threading-model-Eigenschaft zu sehen, indem Sie mit  der rechten Maustaste auf eine Komponente im Ordner **Komponenten** klicken, auf **Eigenschaften** klicken und dann auf die Registerkarte Parallelität klicken. Unter **Threadingmodell** lauten die möglichen Werte wie folgt:

-   **Hauptthread-Apartment**
-   **SingleThread-Apartment**
-   **Free Thread Apartment**
-   **Neutrales Apartment**
-   **Beliebiges Apartment**

Das bevorzugte Threadingmodell für COM+ ist das [neutrale Apartment](neutral-apartments.md). Wenn Sie jedoch kein Threadingmodell für Ihre Komponente angeben, verwendet COM+ das Hauptthread-Apartment, das die Standardeinstellung ist.

> [!Note]  
> Ausführlichere Informationen finden Sie unter [Auswählen des Threadingmodells.](/windows/desktop/com/choosing-the-threading-model)

 

Die folgende Tabelle zeigt das Programmiermodell für Apartment in COM+.



| Modell                     | Wohnung                                                 | Free                               | Beide                               | Neutral                      | Nicht angegeben                      |
|---------------------------|-----------------------------------------------------------|------------------------------------|------------------------------------|------------------------------|------------------------------------|
| Singlethreading, nicht Main | Erstellt im aktuellen Apartment                              | In Multithread-Apartment erstellt | Erstellt im aktuellen Apartment       | In neutralem Apartment erstellt | Erstellt im Hauptthread-Apartment |
| Singlethreading, Main     | Erstellt im aktuellen Apartment                              | In Multithread-Apartment erstellt | Erstellt im aktuellen Apartment       | In neutralem Apartment erstellt | Erstellt im aktuellen Apartment       |
| Multithreaded             | Erstellt im Singlethread-Apartment des Hosts                 | In Multithread-Apartment erstellt | In Multithread-Apartment erstellt | In neutralem Apartment erstellt | Erstellt im Hauptthread-Apartment |
| Neutral (im STA-Thread)   | Erstellt im Singlethread-Host-Apartment für diesen Thread | In Multithread-Apartment erstellt | In neutralem Apartment erstellt       | In neutralem Apartment erstellt | Erstellt im Hauptthread-Apartment |
| Neutral (im MTA-Thread)   | Erstellt im Singlethread-Apartment des Hosts                 | In Multithread-Apartment erstellt | In neutralem Apartment erstellt       | In neutralem Apartment erstellt | Erstellt im Hauptthread-Apartment |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ThreadingModel**](components.md)
</dt> </dl>

 

 
