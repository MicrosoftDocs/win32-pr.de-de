---
title: Rückruf für Benachrichtigungs Rückrufe
description: Wenn der Multicast-Gruppen-Manager benachrichtigt wird, dass neue Empfänger für eine Gruppe auf einer Schnittstelle vorhanden sind, ruft der Multicast-Gruppen-Manager den Rückruf Rückruf für die pmgm- \_ \_ Rückruf Warnung auf \_ .
ms.assetid: b625f8ec-f59b-4151-aa38-48cf8f004966
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c00dc70160b99c3cfc0e41078a3bd5882d930f31
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037178"
---
# <a name="join-alert-callbacks"></a>Rückruf für Benachrichtigungs Rückrufe

Wenn der Multicast-Gruppen-Manager benachrichtigt wird, dass neue Empfänger für eine Gruppe auf einer Schnittstelle vorhanden sind, ruft der Multicast-Gruppen-Manager den Rückruf Rückruf für die [**pmgm- \_ \_ \_ Rückruf Warnung**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) auf. Dieser Rückruf benachrichtigt die Routing Protokolle, dass die neuen Hosts den angegebenen Gruppen beigetreten sind. Daher müssen die Routing Protokolle Multicast Daten für die vom Rückruf angegebenen Gruppen anfordern.

Der Multicast-Gruppen-Manager verwendet einen vordefinierten Satz von Regeln, die verwendet werden, um zu bestimmen, wann dieser Rückruf aufgerufen wird. Dieser Regelsatz basiert sowohl auf dem Typ der vom Client gesendeten joinanforderung als auch auf der Reihenfolge, in der die Joinanforderungen empfangen wurden.

## <a name="wildcard-join-requests"></a>Platzhalter-Joinanforderungen

Wenn ein Platzhalter Join für eine Gruppe ( \* , g) vom ersten Client empfangen wird, ruft der Multicast-Gruppen-Manager den [**pmgm-Rückruf Rückruf- \_ \_ \_ Rückruf**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) Rückruf für alle anderen registrierten Clients auf. Wenn ein Platzhalter Join für eine Gruppe vom zweiten Client empfangen wird, ruft der Multicast-Gruppen-Manager diesen Rückruf an den ersten Client an, um der Gruppe beizutreten.

## <a name="source-specific-join-requests"></a>Joinanforderungen Source-Specific

Der Multicast-Gruppen-Manager ruft diesen Rückruf nicht für nachfolgende Joins in der Gruppe auf.

Wenn ein Quell spezifischer Join für eine Gruppe (n) empfangen wird, ruft der Multicast-Gruppen-Manager den pmgm-Rückruf Rückruf für die [**\_ \_ \_ Rückruf Warnung**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) nur für den Client auf, der die eingehende Schnittstelle für die Quell-s besitzt.

 

 




