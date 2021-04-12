---
description: Com+ verwaltet Threads für Sie. Jede COM-Komponente verfügt über eine ThreadingModel-Eigenschaft, die Sie beim Entwickeln der Komponente angeben können. Diese Eigenschaft bestimmt, wie die Komponenten Objekte Threads zur Methoden Ausführung zugewiesen werden.
ms.assetid: 5fae8475-3d2e-4939-80a7-bc9a677a50b3
title: Threading Modell-Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91960a753b29ac5f5209a5bafa31c362f3dfe08d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104392998"
---
# <a name="threading-model-attribute"></a>Threading Modell-Attribut

Com+ verwaltet Threads für Sie. Jede COM-Komponente verfügt über eine **ThreadingModel** -Eigenschaft, die Sie beim Entwickeln der Komponente angeben können. Diese Eigenschaft bestimmt, wie die Objekte der Komponente Threads zur Methoden Ausführung zugewiesen werden.

Mithilfe des Verwaltungs Programms Komponenten Dienste können Sie die Threading-Model-Eigenschaft anzeigen, indem Sie mit der rechten Maustaste auf eine Komponente im Ordner **Komponenten** klicken, auf **Eigenschaften** klicken und dann **auf die Register** Karte Parallelität klicken. Unter dem **Threading Modell** sind folgende Werte möglich:

-   **Haupt Thread Apartment**
-   **Single Thread-Apartment**
-   **Kostenloses Thread Apartment**
-   **Neutrales Apartment**
-   **Beliebige Wohnungen**

Das bevorzugte Threading Modell für com+ ist das [neutrale Apartment](neutral-apartments.md). Wenn Sie jedoch kein Threading Modell für Ihre Komponente angeben, verwendet com+ das Haupt Thread-Apartment, das die Standardeinstellung ist.

> [!Note]  
> Ausführlichere Informationen finden Sie unter [auswählen des Threading Modells](/windows/desktop/com/choosing-the-threading-model).

 

In der folgenden Tabelle wird das Programmiermodell für Apartments in com+ angezeigt.



| Modell                     | Apartment                                                 | Kostenlos                               | Both                               | Neutral                      | Nicht angegeben                      |
|---------------------------|-----------------------------------------------------------|------------------------------------|------------------------------------|------------------------------|------------------------------------|
| Single Thread, nicht Haupt | In aktuellem Apartment erstellt                              | Im Multithread-Apartment erstellt | In aktuellem Apartment erstellt       | In neutralem Apartment erstellt | Erstellt in Haupt Thread-Apartment |
| Single Thread, Main     | In aktuellem Apartment erstellt                              | Im Multithread-Apartment erstellt | In aktuellem Apartment erstellt       | In neutralem Apartment erstellt | In aktuellem Apartment erstellt       |
| Multithread             | Erstellt im Single Thread-Host-Apartment                 | Im Multithread-Apartment erstellt | Im Multithread-Apartment erstellt | In neutralem Apartment erstellt | Erstellt in Haupt Thread-Apartment |
| Neutral (auf STA-Thread)   | Erstellt im Single Thread-Host für diesen Thread | Im Multithread-Apartment erstellt | In neutralem Apartment erstellt       | In neutralem Apartment erstellt | Erstellt in Haupt Thread-Apartment |
| Neutral (im MTA-Thread)   | Erstellt im Single Thread-Host-Apartment                 | Im Multithread-Apartment erstellt | In neutralem Apartment erstellt       | In neutralem Apartment erstellt | Erstellt in Haupt Thread-Apartment |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Threading Model**](components.md)
</dt> </dl>

 

 
