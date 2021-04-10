---
title: Warnungs Rückrufe löschen
description: Wenn der Multicast-Gruppen-Manager benachrichtigt wird, dass Empfänger eine Gruppe auf einer Schnittstelle belassen, ruft der Multicast-Gruppen-Manager den pmgm- \_ \_ \_ Rückruf Rückruf Rückruf auf.
ms.assetid: 34eb6941-9488-481f-93ca-821789acc140
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a81dab70eaded0fd1fe21bd1b5ec1b5ca495272
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037496"
---
# <a name="prune-alert-callbacks"></a>Warnungs Rückrufe löschen

Wenn der Multicast-Gruppen-Manager benachrichtigt wird, dass Empfänger eine Gruppe auf einer Schnittstelle belassen, ruft der Multicast-Gruppen-Manager den [**pmgm- \_ \_ \_ Rückruf**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) Rückruf Rückruf auf. Dieser Rückruf benachrichtigt die Routing Protokolle, dass Clients nicht mehr zur angegebenen Gruppe gehören. Daher müssen die Routing Protokolle die Anforderung von Multicast Daten für die angegebenen Gruppen nicht mehr anfordern.

Der Multicast-Gruppen-Manager verfügt über einen vordefinierten Satz von Regeln, mit denen bestimmt wird, wann dieser Rückruf aufgerufen wird. Diese Regeln basieren sowohl auf dem Typ der vom Client gesendeten Anforderung zum Löschen von Anforderungen als auch auf der Reihenfolge, in der die Anforderungen für die Anforderung empfangen wurden.

## <a name="wildcard-prune-requests"></a>Platzhalter zum Löschen von Anforderungen

Wenn ein Platzhalter für eine Gruppe ( \* , g) empfangen wird und die letzte Schnittstelle für den zweit-bis letzten Client entfernt wird (d. h. wenn nur Schnittstellen für einen einzelnen Client verbleiben), ruft der Multicast-Gruppen-Manager den [**pmgm- \_ \_ \_ Rückruf**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) Rückruf Rückruf für den verbleibenden Client auf. Nachdem die endgültige Schnittstelle für den letzten Client entfernt wurde (d. h., wenn keine anderen Schnittstellen verbleiben), wird dieser Rückruf für alle anderen Clients aufgerufen, die beim Multicast-Gruppen-Manager registriert sind.

## <a name="source-specific-prune-requests"></a>Source-Specific Anforderungen löschen

Wenn eine Quell spezifische Sicherung für eine Gruppe (n) empfangen wird, ruft der Multicast-Gruppen-Manager den pmgm-Rückruf Rückruf Rückruf nur für den Client auf, der die eingehende Schnittstelle für die Quelle s besitzt. [**\_ \_ \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback)

 

 




