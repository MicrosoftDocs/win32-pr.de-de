---
description: Nachdem Sie eine Ereignisklasse im COM+-Katalog registriert haben, können Sie Abonnenten zur Ereignisklasse und Abonnements für die Abonnenten hinzufügen.
ms.assetid: 101b1075-3724-4508-9c9e-2f12ac6ab65d
title: Registrieren eines Abonnements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f152834c805bd905019d2afe0e353c0a962452c32ef144cc3c3d445b59fbbed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547110"
---
# <a name="registering-a-subscription"></a>Registrieren eines Abonnements

Nachdem Sie eine Ereignisklasse im COM+-Katalog registriert haben, können Sie Abonnenten zur Ereignisklasse und Abonnements für die Abonnenten hinzufügen. Abonnements können eine einzelne Methode oder alle Methoden einer Schnittstelle abonnieren. Um Aufrufe für mehrere Methoden – aber nicht für jede Methode – einer Schnittstelle zu empfangen, müssen Sie für jede Methode, für die Sie einen Aufruf empfangen möchten, ein Abonnement hinzufügen. Das Verwaltungstool für Komponentendienste kann den COM+-Katalog nach registrierten Ereignisklassen durchsuchen, die die vom Abonnenten implementierten Schnittstellen unterstützen und Ihnen die Auswahl zum Abonnieren bieten. Wählen Sie den Herausgeber aus, der Ihnen die gewünschten Ereignisse anbietet.

Um Abonnenten zur Abonnentenkomponente hinzuzufügen, führen Sie die folgenden Schritte aus:

1.  Nachdem Sie eine neue COM+-Anwendung erstellt und die Abonnentenkomponente installiert haben, klicken Sie mit der rechten Maustaste auf den Ordner **Abonnements,** um den Com+-Assistenten für neue Abonnements zu aktivieren.

2.  Wählen Sie die Ereignisklasse aus, aus der Sie Ereignisse empfangen möchten.

3.  Geben Sie einen Namen für das Abonnement ein.

4.  Aktivieren Sie das Abonnement.

5.  Klicken Sie auf **OK**.

Wenn eine Herausgeberanwendung ein Ereignis ausrufen möchte, instanziiert der Herausgeber das Ereignisklassenobjekt und ruft eine -Methode für dieses auf. COM+ durchsucht den COM+-Katalog, um alle Abonnenten zu finden. Er erstellt das Abonnentenobjekt (direkt, in der Warteschlange oder mit einem Moniker) und übergibt den ursprünglich vom Herausgeber vorgenommenen Methodenaufruf.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrieren einer Ereignisklasse](registering-an-event-class.md)
</dt> </dl>

 

 



