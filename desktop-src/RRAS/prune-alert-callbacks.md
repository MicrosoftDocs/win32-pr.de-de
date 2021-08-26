---
title: Löschen von Warnungsrückrufen
description: Wenn der Multicastgruppen-Manager benachrichtigt wird, dass Empfänger eine Gruppe auf einer Schnittstelle verlassen, ruft der Multicastgruppen-Manager den PMGM \_ PRUNE \_ ALERT \_ CALLBACK-Rückruf auf.
ms.assetid: 34eb6941-9488-481f-93ca-821789acc140
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b5aa4d95742a2976ea46367b0f1af9442528c2821dc9d27b09b9e1c29eee6d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036399"
---
# <a name="prune-alert-callbacks"></a>Löschen von Warnungsrückrufen

Wenn der Multicastgruppen-Manager benachrichtigt wird, dass Empfänger eine Gruppe auf einer Schnittstelle verlassen, ruft der Multicastgruppen-Manager den [**PMGM \_ PRUNE \_ ALERT \_ CALLBACK-Rückruf**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) auf. Dieser Rückruf benachrichtigt die Routingprotokolle, dass Clients nicht mehr zur angegebenen Gruppe gehören. Daher müssen die Routingprotokolle keine Multicastdaten mehr für die angegebenen Gruppen anfordern.

Der Multicastgruppen-Manager verfügt über einen vordefinierten Satz von Regeln, mit denen bestimmt wird, wann dieser Rückruf aufgerufen wird. Diese Regeln basieren sowohl auf dem Typ der vom Client gesendeten Löschanforderung als auch auf der Reihenfolge, in der die Bereinigungsanforderungen empfangen wurden.

## <a name="wildcard-prune-requests"></a>Platzhalter für Prune Requests

Wenn ein Platzhalterlöschung für eine Gruppe ( \* , g) empfangen wird und die letzte Schnittstelle für den vorletzten Client entfernt wird (d. h. wenn Schnittstellen nur für einen einzelnen Client verbleiben), ruft der Multicastgruppen-Manager den RÜCKRUFRÜCKRUF FÜR [**PMGM \_ PRUNE \_ ALERT \_ CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) für diesen verbleibenden Client auf. Nachdem die endgültige Schnittstelle für den letzten Client entfernt wurde (d. h., wenn keine anderen Schnittstellen verbleiben), wird dieser Rückruf für alle anderen Clients aufgerufen, die beim Multicastgruppen-Manager registriert sind.

## <a name="source-specific-prune-requests"></a>Source-Specific Prune-Anforderungen

Wenn ein quellspezifischer Prune für eine Gruppe (s, g) empfangen wird, ruft der Multicastgruppen-Manager den [**PMGM \_ PRUNE \_ ALERT \_ CALLBACK-Rückruf**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) nur für den Client auf, der die eingehende Schnittstelle für die Quell-s besitzt.

 

 




