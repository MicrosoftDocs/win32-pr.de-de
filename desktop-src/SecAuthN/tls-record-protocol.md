---
description: Das Protokoll für den Transport Layer Security(TLS)-Datensatz schützt Anwendungsdaten mithilfe der Schlüssel, die während des Handshakes erstellt wurden.
ms.assetid: 3ad4cbd9-ce7c-4882-9c53-c935068c0ba7
title: TLS-Datensatzprotokoll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce441de892367b49e1fd4aa285b5398dd5e7c1667d0ea785f6925995c89e1dfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915740"
---
# <a name="tls-record-protocol"></a>TLS-Datensatzprotokoll

Das [*Protokoll für den Transport Layer Security-Datensatz*](../secgloss/t-gly.md) (TLS) schützt Anwendungsdaten mithilfe der Schlüssel, die während des [Handshakes](tls-handshake-protocol.md)erstellt wurden. Das Datensatzprotokoll ist für das Sichern von Anwendungsdaten und die Überprüfung ihrer [*Integrität*](../secgloss/i-gly.md) und ihres Ursprungs verantwortlich. Folgendes wird verwaltet:

-   Aufteilen ausgehender Nachrichten in verwaltbare Blöcke und erneutes Zusammensetzen eingehender Nachrichten.
-   Komprimieren ausgehender Blöcke und Dekomprimieren eingehender Blöcke (optional).
-   Anwenden eines [*Nachrichtenauthentifizierungscode*](../secgloss/m-gly.md) (MAC) auf ausgehende Nachrichten und Überprüfen eingehender Nachrichten mit dem MAC.
-   Verschlüsseln ausgehender Nachrichten und Entschlüsseln eingehender Nachrichten.

Wenn das Datensatzprotokoll abgeschlossen ist, werden die ausgehenden verschlüsselten Daten für den Transport an die TCP-Ebene (Transmission Control Protocol) übergeben.

 

 
