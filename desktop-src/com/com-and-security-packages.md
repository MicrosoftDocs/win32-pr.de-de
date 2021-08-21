---
title: COM- und Sicherheitspakete
description: Windows unterstützt NTLMSSP (LAN Manager-Sicherheitssupportanbieter), das Kerberos v5-Authentifizierungsprotokoll und das Schannel-Sicherheitspaket, das die Protokolle PCT 1.0, SSL 2.0, SSL 3.0 und TLS 1.0 bereitstellt.
ms.assetid: a0c095a8-93b7-4350-aac6-a9a066cccffd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15ec80a1ea610725716da3640b6e38b2fd0f3282ce6ce778e632c6a5c8e72c8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048718"
---
# <a name="com-and-security-packages"></a>COM- und Sicherheitspakete

Windows unterstützt NTLMSSP (LAN Manager-Sicherheitssupportanbieter), das Kerberos v5-Authentifizierungsprotokoll und das Schannel-Sicherheitspaket, das die Protokolle PCT 1.0, SSL 2.0, SSL 3.0 und TLS 1.0 bereitstellt. Unterstützt wird auch Snego, das nach verfügbaren Sicherheitspaketen sucht und das am besten geeignete auswählt.

Die folgende Tabelle zeigt die Authentifizierungsebenen, die von den verschiedenen Sicherheitspaketen unterstützt werden.



| Server-/Clientauthentifizierung                                                                                           | Unterstützung von Sicherheitspaketen                                         |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| Keiner der beiden kann den Namen des anderen abrufen.<br/>                                                                      | Keine<br/>                                                  |
| Der Client kann den Server authentifizieren, aber nicht umgekehrt.<br/>                                                 | Schannel<br/>                                              |
| Der Client kann den Server nicht ermitteln, aber der Server kann die Benutzer-ID des Clients abrufen.<br/>                    | Ntlmssp<br/>                                               |
| Gegenseitige Authentifizierung: Sowohl der Client als auch der Server können den Namen des anderen kennen, wenn die Berechtigung erteilt wird.<br/> | NTLMSSP (lokal), Kerberos v5-Protokoll und Schannel<br/> |



 

Weitere Informationen zu diesen Sicherheitspaketen finden Sie in den folgenden Themen in diesem Abschnitt:

-   [Ntlmssp](ntlmssp.md)
-   [Kerberos v5-Protokoll](kerberos-v5-protocol.md)
-   [Schannel](schannel.md)
-   [Snego](snego.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sicherheit in COM](security-in-com.md)
</dt> </dl>

 

 





