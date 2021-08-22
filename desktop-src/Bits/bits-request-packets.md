---
title: BITS-Anforderungspakete
description: BITS-Anforderungspakete
ms.assetid: 4d8fd5f3-7621-438f-926f-38ece7a52f52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60921c9adb8e1312a6b74cd129e591db5a3be7807394807b984eb3fff153b3a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588680"
---
# <a name="bits-request-packets"></a>BITS-Anforderungspakete

Anforderungspakete beschreiben Clientanforderungen. Es kann zu einem bestimmten Zeitpunkt nur eine ausstehende Anforderung sein. Sie müssen eine [Bestätigung für](bits-response-packets.md) die aktuelle Anforderung vom Server erhalten, bevor Sie eine weitere Anforderung senden.

In der folgenden Tabelle sind die Anforderungspakete aufgeführt, die für Upload- und Upload-Reply-Aufträge an den BITS-Server gesendet werden. In der Tabelle sind die Pakete in der typischen Reihenfolge aufgeführt, in der sie an den Server gesendet werden.



| Anforderungspaket                       | Zweck                                                                                                                                                        |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Pingen](ping.md)                     | Stellt eine Verbindung ein und handelt die Sicherheit mit dem Server aus.                                                                                              |
| [Create-Session](create-session.md) | Fordert eine Uploadsitzung mit dem BITS-Server an.                                                                                                               |
| [Fragment](fragment.md)             | Sendet ein Fragment der Datei an den BITS-Server. Die Anzahl der gesendeten Fragmentanforderungen hängt von der von Ihnen wählen Fragmentgröße und der Größe der Uploaddatei ab. |
| [Close-Session](close-session.md)   | Beendet die Dateiuploadsitzung mit dem BITS-Server.                                                                                                             |
| [Cancel-Session](cancel-session.md) | Beendet die Dateiuploadsitzung mit dem BITS-Server. In der Regel senden Sie das Cancel-Session Paket, wenn der Benutzer den Auftrag abgebrochen hat.                                 |



 

Das Ping-Paket ist optional. Anstatt ein Ping-Paket zu senden, können Sie das Create-Session verwenden, um eine Verbindung herzustellen und die Sicherheit auszuhandeln. Es ist jedoch effizienter, das Ping-Paket für diesen Zweck zu verwenden.

 

 




