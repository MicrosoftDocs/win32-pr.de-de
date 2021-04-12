---
description: Nachdem Sie eine Ereignisklasse im com+-Katalog registriert haben, können Sie der-Ereignisklasse Abonnenten und Abonnements für die Abonnenten hinzufügen.
ms.assetid: 101b1075-3724-4508-9c9e-2f12ac6ab65d
title: Registrieren eines Abonnements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a03d5710fc792cad6282683d51df21d2ede10451
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393174"
---
# <a name="registering-a-subscription"></a>Registrieren eines Abonnements

Nachdem Sie eine Ereignisklasse im com+-Katalog registriert haben, können Sie der-Ereignisklasse Abonnenten und Abonnements für die Abonnenten hinzufügen. Abonnements können eine einzelne Methode oder alle Methoden einer Schnittstelle abonnieren. Zum Empfangen von Aufrufen für mehr als eine Methode – aber nicht für jede Methode – einer Schnittstelle müssen Sie für jede Methode, an die Sie einen Aufruf erhalten möchten, ein Abonnement hinzufügen. Mit dem Verwaltungs Tool Komponenten Dienste können Sie den com+-Katalog nach registrierten Ereignis Klassen durchsuchen, die die vom Abonnenten implementierten Schnittstellen unterstützen. Sie können auch abonnieren. Wählen Sie den Herausgeber aus, der Ihnen die gewünschten Ereignisse anbietet.

Führen Sie die folgenden Schritte aus, um der Abonnenten Komponente Abonnenten hinzuzufügen:

1.  Nachdem Sie eine neue COM+-Anwendung erstellt und die Abonnenten Komponente installiert haben, klicken Sie mit der rechten Maustaste auf den Ordner **Abonnements** , um den com+-Assistenten für neue Abonnements zu aktivieren

2.  Wählen Sie die Ereignisklasse aus, von der Sie Ereignisse empfangen möchten.

3.  Geben Sie einen Namen für das Abonnement ein.

4.  Aktivieren Sie das Abonnement.

5.  Klicken Sie auf **OK**.

Wenn eine Verleger Anwendung ein Ereignis auslösen möchte, instanziiert der Verleger das Ereignis Klassenobjekt und ruft eine Methode dafür auf. Com+ durchsucht den com+-Katalog, um alle Abonnenten zu suchen. Er erstellt das Abonnenten Objekt (direkt, in der Warteschlange oder mit einem Moniker) und übergibt den Methodenaufruf, der ursprünglich vom Verleger erstellt wurde.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrieren einer Ereignisklasse](registering-an-event-class.md)
</dt> </dl>

 

 



