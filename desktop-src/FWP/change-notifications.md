---
title: Änderungsbenachrichtigungen
description: Die Änderungsbenachrichtigungen der Basisfilter-Engine (Base Filtering Engine, BFE) folgen dem Veröffentlichungs-/Abonnementmuster.
ms.assetid: 443f1767-5694-4584-ba0f-229275900774
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0038dc851cb15414dbc0180f205104725bf069b599632a93ae6e257fe7a1f84
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078500"
---
# <a name="change-notifications"></a>Änderungsbenachrichtigungen

Die Änderungsbenachrichtigungen der Basisfilter-Engine (Base Filtering Engine, BFE) folgen dem Veröffentlichungs-/Abonnementmuster: Um eine der veröffentlichten Änderungsbenachrichtigungen zu erhalten, muss eine Anwendung sie abonnieren.

Die veröffentlichten BFE-Änderungsbenachrichtigungen sind Hinzufügen und [](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context_subscription0)Entfernen für Aufrufe, Filter, Anbieter, Anbieterkontexte und [**Unterebenen.**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer_subscription0) [](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout_subscription0) [](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_subscription0) [](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_subscription0)

Um eine der oben genannten Benachrichtigungen zu abonnieren, ruft eine Anwendung die entsprechende [**Fwpm \* SubscribeChanges0-Verwaltungsfunktion**](fwp-mgmt-functions.md) auf (z. B. [**FwpmCalloutSubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscribechanges0)). Die Rückruffunktion, die als Argument an **Fwpm \* SubscribeChanges0** übergeben wird, wird von BFE aufgerufen, wenn die Änderung erfolgt, für die sie abonniert wurde.

Um eine der oben genannten Benachrichtigungen zu kündigen, ruft eine Anwendung die entsprechende **Fwpm \* UnsubscribeChanges0-Verwaltungsfunktion** auf (z. B. [**FwpmCalloutUnsubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutunsubscribechanges0)).

Um die aktuellen Abonnements für eine der oben genannten Benachrichtigungen anzuzeigen, ruft eine Anwendung die entsprechende [**Fwpm \* SubscriptionsGet0-Verwaltungsfunktion**](fwp-mgmt-functions.md) auf (z. B. [**FwpmCalloutSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscriptionsget0)).

Vom BFE werden die folgenden Änderungsbenachrichtigungen angeboten:

-   Asynchron: Der Funktionsaufruf, der eine Benachrichtigung ausgelöst hat, kann zurückgeben, bevor die Benachrichtigung an alle Abonnenten gesendet wurde.
-   Unzuverlässig: Es wird nicht garantiert, dass Benachrichtigungen erfolgreich übermittelt werden.

Abonnenten erhalten keine Benachrichtigungen über Änderungen, die mit dem Sitzungshand handle vorgenommen wurden, das sie zum Abonnieren verwendet haben. Im Allgemeinen müssen Abonnenten nur über die Änderungen informiert werden, die von anderen vorgenommen wurden. Sie wissen bereits, welche Änderungen selbst vorgenommen wurden.

 

 




