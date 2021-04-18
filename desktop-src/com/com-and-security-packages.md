---
title: COM-und Sicherheitspakete
description: Windows unterstützt NTLMSSP (LAN Manager Security Support Provider), das Kerberos V5-Authentifizierungsprotokoll und das SChannel-Sicherheitspaket, das die Protokolle PCT 1,0, SSL 2,0, SSL 3,0 und TLS 1,0 bereitstellt.
ms.assetid: a0c095a8-93b7-4350-aac6-a9a066cccffd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6720ddd56869c5ce93ae70eb313fbe12c140b42
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341438"
---
# <a name="com-and-security-packages"></a>COM-und Sicherheitspakete

Windows unterstützt NTLMSSP (LAN Manager Security Support Provider), das Kerberos V5-Authentifizierungsprotokoll und das SChannel-Sicherheitspaket, das die Protokolle PCT 1,0, SSL 2,0, SSL 3,0 und TLS 1,0 bereitstellt. Unterstützt wird auch das spogo, das auf verfügbare Sicherheitspakete prüft und das geeignetste-Paket auswählt.

In der folgenden Tabelle sind die Authentifizierungs Ebenen aufgeführt, die von den verschiedenen Sicherheitspaketen unterstützt werden.



| Server/Client-Authentifizierung                                                                                           | Unterstützung von Sicherheitspaketen                                         |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| Keines der beiden kann den Namen der anderen erhalten.<br/>                                                                      | Keine<br/>                                                  |
| Der Client kann den Server authentifizieren, aber nicht umgekehrt.<br/>                                                 | Schannel<br/>                                              |
| Der Client kann den Server nicht ermitteln, aber der Server kann die Benutzer-ID des Clients erhalten.<br/>                    | NTLMSSP<br/>                                               |
| Gegenseitige Authentifizierung: sowohl der Client als auch der Server können den Namen des anderen kennen, wenn die Berechtigung gewährt wird.<br/> | NTLMSSP (lokal), Kerberos V5-Protokoll und SChannel<br/> |



 

Weitere Informationen zu diesen Sicherheitspaketen finden Sie in den folgenden Themen in diesem Abschnitt:

-   [NTLMSSP](ntlmssp.md)
-   [Kerberos V5-Protokoll](kerberos-v5-protocol.md)
-   [SChannel](schannel.md)
-   [Spogo](snego.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sicherheit in com](security-in-com.md)
</dt> </dl>

 

 





