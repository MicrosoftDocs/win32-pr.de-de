---
description: Der System Ereignis Benachrichtigungsdienst funktioniert mit dem com+-Ereignis System.
ms.assetid: c51d1f61-6087-4480-b989-31241829781b
title: Sens-Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e32976a716ab0ba5651ce6605fe524d639820696
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355329"
---
# <a name="sens-architecture"></a>Sens-Architektur

Der System Ereignis Benachrichtigungsdienst funktioniert mit dem com+-Ereignis System. Sens ist ein Ereignis Herausgeber für die Klassen von Ereignissen, die er überwacht: Netzwerk-, Anmeldungs-und Strom-/Akku-Ereignisse. Die Anwendung, die eine Benachrichtigung empfängt, wird als Ereignis Abonnent bezeichnet.

Wenn eine Anwendung Benachrichtigungen empfängt, kann Sie auch Filter angeben, die den abonnierten Ereignissen zugeordnet sind. Die Ereignisse "Sens" und "com+" verwenden die Filter, um festzustellen, wann die Anwendung benachrichtigt werden soll.

Benachrichtigungen sind asynchron, sodass die Anwendung, die die Benachrichtigung empfängt, nicht aktiv sein muss, wenn die Benachrichtigung gesendet wird. Wenn eine Anwendung Benachrichtigungen empfängt, kann Sie angeben, ob Sie bei Auftreten des Ereignisses aktiviert oder später benachrichtigt werden soll, wenn Sie aktiv ist.

Das Abonnement kann vorübergehend und gültig sein, bis die Anwendung beendet wird, oder es kann persistent und gültig sein, bis die Anwendung aus dem System entfernt wird.

Ein com+-Ereignisdaten Speicher enthält Informationen über den Ereignis Herausgeber (Sens), Ereignis Abonnenten und Filter. Sens definiert auch eine ausgehende Schnittstelle für jede Ereignisklasse in einer Typbibliothek.



| Ereignisklasse    | GUID                          | Schnittstelle    |
|----------------|-------------------------------|--------------|
| Netzwerkereignisse | sensorguid \_ EventClass- \_ Netzwerk | Isensnetwork |
| Anmeldeereignisse   | sensorguid \_ EventClass- \_ Anmeldung   | Isenslogon   |
| Energie Ereignisse   | sensguid \_ EventClass \_ OnNow   | Isennow   |



 

Um Benachrichtigungen für diese Ereignisse zu erhalten, muss Ihre Anwendung zwei Schritte ausführen:

-   Abonnieren Sie die für Sie interessanten Sens-Ereignisse. Um ein Ereignis zu abonnieren, verwenden Sie die Schnittstellen **ieventabonnement** und **ieventsystem** in COM+-Ereignissen. Sie müssen einen Bezeichner für die Ereignis Klassen und den Sens-Verleger Bezeichner, sensorguid Publisher, angeben \_ . Abonnements sind auf der Ebene pro Ereignis festgelegt, sodass die abonnierende Anwendung auch angeben muss, welche Ereignisse in der Klasse von Interesse sind. Jedes Ereignis entspricht einer Methode in der-Schnittstelle, die der-Ereignisklasse entspricht.
-   Erstellen Sie ein Sink-Objekt mit einer Implementierung für jede Schnittstelle, die Sie verarbeiten. Weitere Informationen zu diesen Schnittstellen und den jeweils unterstützten Ereignissen finden Sie unter [**isensnetwork**](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork), [**isenslogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)und [**isensonnow**](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow) .

Wenn eines der überwachten Ereignisse auftritt, verarbeitet Sens jedes Abonnement mit zugeordneten Filtern und benachrichtigt die Abonnenten über das com+-Ereignis System.

 

 



