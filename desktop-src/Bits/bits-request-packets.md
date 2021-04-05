---
title: Bits-Anforderungs Pakete
description: Bits-Anforderungs Pakete
ms.assetid: 4d8fd5f3-7621-438f-926f-38ece7a52f52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6738f77477342f1329818ae7c2ffb5c010b074c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947465"
---
# <a name="bits-request-packets"></a>Bits-Anforderungs Pakete

Anforderungs Pakete beschreiben Client Anforderungen. Es kann immer nur eine ausstehende Anforderung vorhanden sein. Sie müssen eine Bestätigung [für die](bits-response-packets.md) aktuelle Anforderung vom Server erhalten, bevor Sie eine weitere Anforderung senden.

In der folgenden Tabelle werden die Anforderungs Pakete aufgelistet, die für Upload-und Upload-Reply-Aufträge an den BITS-Server gesendet werden. In der Tabelle werden die Pakete in der typischen Reihenfolge aufgelistet, an die Sie an den Server gesendet werden.



| Anforderungspaket                       | Zweck                                                                                                                                                        |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Ping](ping.md)                     | Stellt eine Verbindung her und aushandiert die Sicherheit mit dem Server.                                                                                              |
| [Create-Session](create-session.md) | Fordert eine Uploadsitzung mit dem BITS-Server an.                                                                                                               |
| [Fragment](fragment.md)             | Sendet ein Fragment der Datei an den BITS-Server. Die Anzahl der gesendeten fragmentanforderungen hängt von der ausgewählten Fragmentgröße und der Größe der Uploaddatei ab. |
| [Sitzung schließen](close-session.md)   | Beendet die dateiuploadsitzung mit dem BITS-Server.                                                                                                             |
| [Abbrechen-Sitzung](cancel-session.md) | Beendet die dateiuploadsitzung mit dem BITS-Server. Normalerweise senden Sie das Cancel-Session Paket, wenn der Benutzer den Auftrag abgebrochen hat.                                 |



 

Das Ping-Paket ist optional. Anstatt ein Ping-Paket zu senden, können Sie das Create-Session Paket verwenden, um eine Verbindung herzustellen und Sicherheit auszuhandeln. Es ist jedoch effizienter, das Ping-Paket zu diesem Zweck zu verwenden.

 

 




