---
description: Ein Sicherheitskontext ist der Satz von Sicherheitsattributen und -regeln, die während einer Kommunikationssitzung wirksam werden.
ms.assetid: 6c87448b-5b8d-4694-ac3f-be83a258fbb0
title: SSPI-Kontextsemantik
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423ce097d1ab71cf50983285f3ca8731497ed5a9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482536"
---
# <a name="sspi-context-semantics"></a>SSPI-Kontextsemantik

Ein [*Sicherheitskontext*](../secgloss/s-gly.md) ist der Satz von Sicherheitsattributen und -regeln, die während einer Kommunikationssitzung wirksam werden. Dies schließt Informationen wie die Identitäten des Prinzipals und Informationen zu den verwendeten Schlüsseln, Verschlüsselungen und Algorithmen ein. Bei [*der Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) ist ein Sicherheitskontext eine nicht transparente Struktur, die durch einen Austausch erstellt wird, der die [**InitializeSecurityContext (General)-Funktion**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) und die [**AcceptSecurityContext (General)-Funktion**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) umfasst.

Weitere Informationen zu den Kontextattributen finden Sie unter [Kontextanforderungen.](context-requirements.md)

Das SSPI-Modell unterstützt drei Arten von Sicherheitskontexten.




| type | BESCHREIBUNG | 
|------|-------------|
| <a href="connection-oriented-contexts.md">Connection</a> | Ein verbindungsorientierter <a href="/windows/desktop/SecGloss/c-gly"><em>Kontext</em></a> ist der gängigste und am einfachsten zu verwendende Sicherheitskontext. Der Aufrufer ist für das gesamte Nachrichtenformat und den Speicherort der Daten in der Nachricht verantwortlich. Der Aufrufer ist auch für den Speicherort der sicherheitsrelevanten Felder innerhalb einer Nachricht verantwortlich, z. B. für den Speicherort der Signaturdaten.<br /> | 
| <a href="datagram-contexts.md">Datagramm</a> | Ein <a href="/windows/desktop/SecGloss/d-gly"><em>Datagramm-orientierter</em></a>Kontext bietet zusätzliche Unterstützung für die DcE-Datagrammkommunikation. Sie kann auch generisch für eine datagramorientierte Transportanwendung verwendet werden.<br /><blockquote><p>[!Important]</p><p>Das <a href="microsoft-kerberos.md">Microsoft Kerberos-Paket</a> unterstützt keine Datagrammkontexte im Benutzer-zu-Benutzer-Modus.<br /></p></blockquote><br /> | 
| <a href="stream-contexts.md">STREAM</a> | Ein streamorientierter Kontext ist für die Blockierung und Nachrichtenformatierung im Sicherheitspaket verantwortlich. Der Aufrufer ist nicht an der Formatierung interessiert, sondern an einem unformatierten Datenstrom.<br /> | 




 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kontextanforderungen](context-requirements.md)
</dt> <dt>

[Verbindungsorientierte Kontexte](connection-oriented-contexts.md)
</dt> <dt>

[Datagrammkontexte](datagram-contexts.md)
</dt> <dt>

[Streamkontexte](stream-contexts.md)
</dt> </dl>

 

 
