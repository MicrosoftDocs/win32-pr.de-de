---
title: Verwenden der Windows-Ereignis Sammlung
description: In diesem Abschnitt werden die Themen aufgeführt, in denen die Aufgaben erläutert werden, die mit dem Windows-Ereignis Sammler-SDK ausgeführt werden können. Code Beispiele und Erläuterungen für alle Aufgaben sind in den folgenden Themen enthalten.
ms.assetid: 3396454a-4f43-45d0-951e-3096b9a4a077
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc618ced4cefc7f17fb63b27bb1e097e65b3adac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339411"
---
# <a name="using-windows-event-collector"></a>Verwenden der Windows-Ereignis Sammlung

In diesem Abschnitt werden die Themen aufgeführt, in denen die Aufgaben erläutert werden, die mit dem Windows-Ereignis Sammler-SDK ausgeführt werden können. Code Beispiele und Erläuterungen für alle Aufgaben sind in den folgenden Themen enthalten.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Erstellen eines vom Collector initiierten Abonnements](creating-an-event-collector-subscription.md)

    Enthält Informationen und ein C++-Codebeispiel zum Erstellen eines vom Collector initiierten Abonnements. Ein vom Collector initiiertes Abonnement ermöglicht Ihnen das Empfangen von Ereignissen auf einem lokalen Computer (dem Ereignis Sammler), die von einem Remote Computer (einer Ereignis Quelle) weitergeleitet werden.

-   [Einrichten eines von der Quelle initiierten Abonnements](setting-up-a-source-initiated-subscription.md)

    Enthält Informationen und ein C++-Codebeispiel zum Erstellen eines Quell initiierten Abonnements. Mit einem Quell initiierten Abonnement können Sie Ereignisse auf einem lokalen Computer (dem Ereignis Sammler) empfangen, die von einem Remote Computer (einer Ereignis Quelle) weitergeleitet werden, ohne die Ereignis Quellen im Abonnement anzugeben.

-   [Hinzufügen einer Ereignis Quelle zu einem vom Collector initiierten Abonnement](adding-an-event-source-to-an-event-collector-subscription.md)

    Enthält Informationen und ein C++-Codebeispiel zum Hinzufügen einer Ereignis Quelle (lokaler Computer oder Remote Computer) zu einem vom Collector initiierten Abonnement. Ein vom Collector initiiertes Abonnement kann erst mit dem Erfassen von Ereignissen beginnen, wenn dem Abonnement eine Ereignis Quelle hinzugefügt wurde.

-   [Erstellen von Hardware Ereignis Abonnements](creating-hardware-event-subscriptions.md)

    Enthält Informationen zum Erstellen eines Ereignis Abonnements, um Hardware Ereignisse von einem Computer zu empfangen, auf dem ein Baseboard-Verwaltungs Controller (BMC) installiert ist.

-   [Löschen eines Ereignis Sammler Abonnements](deleting-an-event-collector-subscription.md)

    Enthält Informationen und ein C++-Codebeispiel zum Löschen eines Ereignis Sammler Abonnements von einem lokalen Computer.

-   [Anzeigen der Eigenschaften eines Ereignis Sammler Abonnements](displaying-the-properties-of-an-event-collector-subscription.md)

    Stellt Informationen und ein C++-Codebeispiel zum Anzeigen der Eigenschaftswerte eines Ereignis Sammler Abonnements bereit. Eigenschaftswerte können nützliche Informationen bereitstellen, z. b. die Adressen von Ereignis Quellen, den Status des Abonnements und die Ereignis Quellen sowie Informationen zur Übermittlung von Ereignissen.

-   [Anzeigen des Status eines Ereignis Sammler Abonnements](displaying-the-status-of-an-event-collector-subscription.md)

    Enthält Informationen und ein C++-Codebeispiel zum Anzeigen des Lauf Zeit Status von Ereignis Quellen, die einem Ereignis Sammler Abonnement zugeordnet sind. Dies ermöglicht es Ihnen, Fehlermeldungen anzuzeigen, die helfen können, Probleme zu beheben, die verhindern, dass Ereignisse von einer Ereignis Quelle weitergeleitet werden.

-   [Auflisten von Event Collector-Abonnements](listing-event-collector-subscriptions.md)

    Enthält Informationen und ein C++-Codebeispiel zum Auflisten der Abonnements, die auf einem lokalen Computer vorhanden sind. Sie können die Abonnement Namen, die in diesem Beispiel abgerufen werden, zum Löschen eines Abonnements, Hinzufügen einer Ereignis Quelle zu einem Abonnement, Abrufen der Eigenschaften eines Abonnements oder Anzeigen des Status eines Abonnements verwenden.

-   [Entfernen einer Ereignis Quelle aus einem vom Collector initiierten Abonnement](removing-an-event-source-from-an-event-collector-subscription.md)

    Enthält Informationen und ein C++-Codebeispiel zum Entfernen einer Ereignis Quelle aus einem vom Collector initiierten Abonnement. Sie können eine Ereignis Quelle aus einem vom Collector initiierten Abonnement entfernen, ohne das Abonnement zu deaktivieren.

-   [Wiederholungsversuch für ein Ereignis Sammler Abonnement](retrying-an-event-collector-subscription.md)

    Enthält Informationen und ein C++-Codebeispiel zum Wiederholen eines Ereignis Sammler Abonnements, wenn mindestens eine Ereignis Quelle fehlgeschlagen ist. Sie können eine einzelne Ereignis Quelle wiederholen, oder Sie können das gesamte Abonnement wiederholen.

 

 




