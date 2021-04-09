---
title: Bits-Antwort Pakete
description: Bits-Antwort Pakete
ms.assetid: 30755476-daa9-42ea-8fb3-5b505fc9dd75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 755e28b749d201a2c90640ea9e456f012f790453
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855484"
---
# <a name="bits-response-packets"></a>Bits-Antwort Pakete

In der folgenden Tabelle sind die Antwort Pakete aufgelistet, die für Upload-und Upload-Reply-Aufträge an den Bits-Client gesendet wurden. In der Tabelle werden die Pakete in der typischen Reihenfolge aufgelistet, an die Sie an den Client gesendet werden.



| Antwortpaket                                      | Zweck                                                                                                                                                                                     |
|------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bestätigung für Ping](ack-for-ping.md)                     | Bestätigt die [Ping](ping.md) -Anforderung.                                                                                                                                                  |
| [Bestätigung für Create-Session](ack-for-create-session.md) | Bestätigt die [Create-Session-](create-session.md) Anforderung und gibt einen Sitzungs Bezeichner zurück, den der BITS-Client für alle nachfolgenden Anforderungen verwendet, um diese Datei Übertragungs Sitzung zu identifizieren. |
| [Bestätigung für Fragment](ack-for-fragment.md)             | Bestätigt die [fragmentanforderung](fragment.md) und schreibt das Fragment in die Uploaddatei auf dem Server.                                                                                 |
| [Bestätigung für Close-Session](ack-for-close-session.md)   | Bestätigt die Anforderung zum [Schließen der Sitzung](close-session.md) und gibt alle der Sitzung zugeordneten Ressourcen frei.                                                                         |
| [Bestätigung für Cancel-Session](ack-for-cancel-session.md) | Bestätigt die [Abbruch Sitzungs](cancel-session.md) Anforderung und gibt alle der Sitzung zugeordneten Ressourcen frei.                                                                       |



 

 

 




