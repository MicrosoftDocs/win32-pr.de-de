---
title: Änderungs Benachrichtigungen
description: Die Änderungs Benachrichtigungen für die Basis Filter-Engine (BFE) folgen dem Veröffentlichen/Abonnieren-Muster.
ms.assetid: 443f1767-5694-4584-ba0f-229275900774
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c7a3a2069525cc44823ed975fade3b5f100efd8
ms.sourcegitcommit: 60ad94096619da5476f9bbcd4cc231b40b6f5358
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "103948453"
---
# <a name="change-notifications"></a>Änderungs Benachrichtigungen

Die Änderungs Benachrichtigungen für die Basis Filter-Engine (BFE) folgen dem Veröffentlichen/Abonnieren-Muster: um eine der veröffentlichten Änderungs Benachrichtigungen zu empfangen, muss Sie von einer Anwendung abonniert werden.

Die veröffentlichten BFE-Änderungs Benachrichtigungen sind "Add" und "Remove [**" für Legenden**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout_subscription0), [**Filter**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_subscription0), [**Anbieter**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_subscription0), [**Anbieter Kontexte**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context_subscription0)und [**untergeordnete Ebenen**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer_subscription0).

Um eine der obigen Benachrichtigungen zu abonnieren, ruft eine Anwendung die entsprechende [**fwpm- \* SubscribeChanges0**](fwp-mgmt-functions.md) Verwaltungsfunktion auf (z. b. [**FwpmCalloutSubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscribechanges0)). Die Rückruffunktion, die als Argument an **fwpm \* SubscribeChanges0** übermittelt wird, wird von BFE aufgerufen, wenn die Änderung, die Sie abonniert hat, erfolgt.

Um eine der obigen Benachrichtigungen abzubestellen, ruft eine Anwendung die entsprechende **fwpm- \* UnsubscribeChanges0** Verwaltungsfunktion auf (z. b. [**FwpmCalloutUnsubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutunsubscribechanges0)).

Um die aktuellen Abonnements für eine der obigen Benachrichtigungen anzuzeigen, ruft eine Anwendung die entsprechende [**fwpm- \* SubscriptionsGet0**](fwp-mgmt-functions.md) Verwaltungsfunktion auf (z. b. [**FwpmCalloutSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscriptionsget0)).

Die von den BFE angebotenen Änderungs Benachrichtigungen lauten:

-   Asynchronous – der Funktions Aufrufwert, der eine Benachrichtigung ausgelöst hat, kann zurückgeben, bevor die Benachrichtigung an alle Abonnenten gesendet wurde.
-   Unzuverlässig – es wird keine Garantie gegeben, dass Benachrichtigungen erfolgreich zugestellt werden.

Abonnenten erhalten keine Benachrichtigungen zu Änderungen, die mit dem Sitzungs handle vorgenommen wurden, das Sie zum Abonnieren verwendet haben. Im Allgemeinen müssen Abonnenten nur über die von anderen vorgenommenen Änderungen informiert werden. Sie wissen bereits, welche Änderungen von sich selbst vorgenommen wurden.

 

 




