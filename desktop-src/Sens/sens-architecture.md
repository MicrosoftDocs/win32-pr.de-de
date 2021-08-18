---
description: Der Systemereignisbenachrichtigungsdienst funktioniert mit dem COM+-Ereignissystem.
ms.assetid: c51d1f61-6087-4480-b989-31241829781b
title: SENS-Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586ad8ae9c5ec50f4f36c07ed592599cf5e09775bd7f450844c83cc42a4c580f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118890409"
---
# <a name="sens-architecture"></a>SENS-Architektur

Der Systemereignisbenachrichtigungsdienst funktioniert mit dem COM+-Ereignissystem. SENS ist ein Ereignisherausgeber für die Klassen von Ereignissen, die überwacht werden: Netzwerk-, Anmelde- und Energie-/Akkuereignisse. Die Anwendung, die eine Benachrichtigung empfängt, wird als Ereignis-Abonnent bezeichnet.

Wenn eine Anwendung Benachrichtigungen abonniert, kann sie auch Filter angeben, die den abonnierten Ereignissen zugeordnet sind. SENS- und COM+-Ereignisse verwenden die Filter, um weiter zu bestimmen, wann die Anwendung benachrichtigt werden soll.

Benachrichtigungen sind asynchron, sodass die Anwendung, die die Benachrichtigung empfängt, nicht aktiv sein muss, wenn die Benachrichtigung gesendet wird. Wenn eine Anwendung Benachrichtigungen abonniert, kann sie angeben, ob sie aktiviert werden soll, wenn das Ereignis eintritt, oder später benachrichtigt werden soll, wenn es aktiv ist.

Das Abonnement kann nur vorübergehend und gültig sein, bis die Anwendung nicht mehr ausgeführt wird, oder es kann persistent und gültig sein, bis die Anwendung aus dem System entfernt wird.

Ein COM+-Ereignisdatenspeicher enthält Informationen über den Ereignisherausgeber (SENS), Ereignis-Abonnenten und Filter. SENS definiert auch eine ausgehende Schnittstelle für jede Ereignisklasse in einer Typbibliothek.



| Ereignisklasse    | GUID                          | Schnittstelle    |
|----------------|-------------------------------|--------------|
| Netzwerkereignisse | SENSGUID \_ EVENTCLASS \_ NETWORK | ISensNetwork |
| Anmeldeereignisse   | SENSGUID \_ EVENTCLASS \_ LOGON   | ISensLogon   |
| Energieereignisse   | SENSGUID \_ EVENTCLASS \_ ONNOW   | ISensOnNow   |



 

Um Benachrichtigungen für eines dieser Ereignisse zu erhalten, muss Ihre Anwendung zwei Aktionen durchführen:

-   Abonnieren Sie die SENS-Ereignisse, die Sie interessieren. Um ein Ereignis zu abonnieren, verwenden Sie die Schnittstellen **IEventSubscription** und **IEventSystem** in COM+-Ereignissen. Sie müssen einen Bezeichner für die Ereignisklassen und den SENS-Herausgeberbezeichner SENSGUID \_ PUBLISHER bereitstellen. Abonnements befinden sich pro Ereignisebene, sodass die abonnierende Anwendung auch angeben muss, welche Ereignisse innerhalb der Klasse von Interesse sind. Jedes Ereignis entspricht einer Methode in der Schnittstelle, die ihrer Ereignisklasse entspricht.
-   Erstellen Sie ein Senkenobjekt mit einer Implementierung für jede Schnittstelle, die Sie behandeln. Weitere Informationen zu diesen Schnittstellen und den jeweils unterstützten Ereignissen finden Sie unter [**ISensNetwork,**](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork) [**ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)und [**ISensOnNow.**](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow)

Wenn eines der überwachten Ereignisse auftritt, verarbeitet SENS jedes Abonnement mit allen zugeordneten Filtern und benachrichtigt die Abonnenten über das COM+-Ereignissystem.

 

 



