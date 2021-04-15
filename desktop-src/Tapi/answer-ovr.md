---
description: Der Antwort Vorgang ist eine typische Anwendung der Antwort auf eine angebotene Kommunikationssitzung. Bei erfolgreicher Ausführung bewirkt dieser Vorgang, dass eine Sitzung in den verbundenen Zustand übergeht.
ms.assetid: 34ac0b34-1d1b-4657-a737-27a4ed9326af
title: Antwort
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e08081b32b7ba3a3a24cde3ec37c1a6118582cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529222"
---
# <a name="answer"></a>Antwort

Der Antwort Vorgang ist die typische Reaktion einer Anwendung auf eine angebotene Kommunikationssitzung. Bei erfolgreicher Ausführung bewirkt dieser Vorgang, dass eine Sitzung in den verbundenen Zustand übergeht.

In einigen Telefonieumgebungen (wie z. b. ISDN), in denen Benutzer Warnungen vom Anruf Angebot getrennt sind, kann die Anwendung einen Anruf [annehmen](accept-ovr.md) , bevor Sie antwortet oder den *Angebots* Anruf ablehnen ([Drop](drop-ovr.md)) oder [umleiten](redirect-ovr.md) .

Wenn ein Antwort Vorgang für eine neue Sitzung ausgeführt wird, wenn eine Sitzung bereits aktiv ist, hängt die Auswirkung auf die vorhandene aktive Sitzung von den Funktionen des Dienstanbieters ab. Der erste Anruf kann nicht beeinträchtigt sein, er kann automatisch gelöscht werden, oder er kann automatisch angehalten werden. TAPI sendet die entsprechenden Ereignis Benachrichtigungen zu beiden aufrufen.

Wenn ein Anruf verbunden ist, aber im aktiven Zustand ist, kann er in einer überbrückten Situation mithilfe des Antwort Vorgangs verknüpft werden.

Die Anwendung hat die Möglichkeit, Benutzer Benutzerinformationen zum Zeitpunkt der Antwort zu senden, wenn Sie vom Dienstanbieter unterstützt wird.

**TAPI 2. x:** Siehe [**lineanswer**](/windows/win32/api/tapi/nf-tapi-lineanswer).

**TAPI 3. x:** Siehe [**itbasiccallcontrol:: answer**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-answer).

 

 
