---
title: Verwenden Windows Ereignissammlers
description: In diesem Abschnitt werden die Themen aufgeführt, in denen die Aufgaben erläutert werden, die mit dem Windows Event Collector SDK ausgeführt werden können. Codebeispiele und Erklärungen für alle Aufgaben sind in jedem der folgenden Themen enthalten.
ms.assetid: 3396454a-4f43-45d0-951e-3096b9a4a077
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb8b928dddcd3e70848d510a8986962d478bedbe6f2f8bffcbec19c276983328
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006010"
---
# <a name="using-windows-event-collector"></a>Verwenden Windows Ereignissammlers

In diesem Abschnitt werden die Themen aufgeführt, in denen die Aufgaben erläutert werden, die mit dem Windows Event Collector SDK ausgeführt werden können. Codebeispiele und Erklärungen für alle Aufgaben sind in jedem der folgenden Themen enthalten.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Erstellen eines collectorinitiiertes Abonnement](creating-an-event-collector-subscription.md)

    Stellt Informationen und ein C++-Codebeispiel zum Erstellen eines collector-initiierten Abonnements bereit. Mit einem vom Collector initiierten Abonnement können Sie Ereignisse auf einem lokalen Computer (dem Ereignissammler) empfangen, die von einem Remotecomputer (einer Ereignisquelle) weitergeleitet werden.

-   [Einrichten eines von der Quelle initiierten Abonnements](setting-up-a-source-initiated-subscription.md)

    Enthält Informationen und ein C++-Codebeispiel zum Erstellen eines von der Quelle initiierten Abonnements. Mit einem von der Quelle initiierten Abonnement können Sie Ereignisse auf einem lokalen Computer (dem Ereignissammler) empfangen, die von einem Remotecomputer (einer Ereignisquelle) weitergeleitet werden, ohne die Ereignisquellen im Abonnement anzugeben.

-   [Hinzufügen einer Ereignisquelle zu einem vom Collector initiierten Abonnement](adding-an-event-source-to-an-event-collector-subscription.md)

    Stellt Informationen und ein C++-Codebeispiel zum Hinzufügen einer Ereignisquelle (lokaler Computer oder Remotecomputer) zu einem vom Collector initiierten Abonnement bereit. Ein vom Collector initiiertes Abonnement kann erst mit dem Sammeln von Ereignissen beginnen, wenn dem Abonnement eine Ereignisquelle hinzugefügt wurde.

-   [Erstellen von Hardwareereignisabonnements](creating-hardware-event-subscriptions.md)

    Enthält Informationen zum Erstellen eines Ereignisabonnements, um Hardwareereignisse von einem Computer zu empfangen, auf dem ein Baseboard Management Controller (BMC) installiert ist.

-   [Löschen eines Ereignissammlerabonnements](deleting-an-event-collector-subscription.md)

    Enthält Informationen und ein C++-Codebeispiel zum Löschen eines Ereignissammlerabonnements von einem lokalen Computer.

-   [Anzeigen der Eigenschaften eines Ereignissammlerabonnements](displaying-the-properties-of-an-event-collector-subscription.md)

    Stellt Informationen und ein C++-Codebeispiel zum Anzeigen der Eigenschaftswerte eines Event Collector-Abonnements bereit. Eigenschaftswerte können nützliche Informationen bereitstellen, z. B. die Adressen von Ereignisquellen, den Status des Abonnements und der Ereignisquellen sowie Informationen darüber, wie Ereignisse übermittelt werden.

-   [Anzeigen des Status eines Ereignissammlerabonnements](displaying-the-status-of-an-event-collector-subscription.md)

    Enthält Informationen und ein C++-Codebeispiel zum Anzeigen des Laufzeitstatus von Ereignisquellen, die einem Ereignissammlerabonnement zugeordnet sind. Dadurch können Sie Fehlermeldungen anzeigen, mit denen Sie Probleme lösen können, die verhindern, dass ereignisse von einer Ereignisquelle weitergeleitet werden.

-   [Auflisten von Ereignissammlerabonnements](listing-event-collector-subscriptions.md)

    Enthält Informationen und ein C++-Codebeispiel zum Auflisten der Abonnements, die auf einem lokalen Computer vorhanden sind. Sie können die Abonnementnamen, die mit diesem Beispiel abgerufen werden, verwenden, um ein Abonnement zu löschen, einem Abonnement eine Ereignisquelle hinzuzufügen, die Eigenschaften eines Abonnements abzurufen oder den Status eines Abonnements anzuzeigen.

-   [Entfernen einer Ereignisquelle aus einem vom Collector initiierten Abonnement](removing-an-event-source-from-an-event-collector-subscription.md)

    Stellt Informationen und ein C++-Codebeispiel zum Entfernen einer Ereignisquelle aus einem collector-initiierten Abonnement bereit. Sie können eine Ereignisquelle aus einem collector-initiierten Abonnement entfernen, ohne das Abonnement zu deaktivieren.

-   [Wiederholen eines Ereignissammlerabonnements](retrying-an-event-collector-subscription.md)

    Stellt Informationen und ein C++-Codebeispiel für die Wiederholung eines Ereignissammlerabonnements bereit, wenn mindestens eine Ereignisquelle fehlgeschlagen ist. Sie können eine einzelne Ereignisquelle oder das gesamte Abonnement wiederholen.

 

 




