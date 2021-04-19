---
description: Ein Sicherheitskontext ist der Satz von Sicherheits Attributen und Regeln, die während einer Kommunikationssitzung wirksam sind.
ms.assetid: 6c87448b-5b8d-4694-ac3f-be83a258fbb0
title: SSPI-Kontext Semantik
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcb604e09b1a2458ef05204aefbe754af26b210
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362864"
---
# <a name="sspi-context-semantics"></a>SSPI-Kontext Semantik

Ein [*Sicherheitskontext*](../secgloss/s-gly.md) ist der Satz von Sicherheits Attributen und Regeln, die während einer Kommunikationssitzung wirksam sind. Hierzu gehören Informationen wie die Identitäten des Prinzipals und Informationen über die verwendeten Schlüssel, Chiffren und Algorithmen. Bei der [*Security Support Provider-Schnittstelle (Security Support Provider Interface*](../secgloss/s-gly.md) , SSPI) ist ein Sicherheitskontext eine nicht transparente Struktur, die über einen Austausch mit der [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) -Funktion und der [**akzeptsecuritycontext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) -Funktion erstellt wird.

Weitere Informationen zu den Kontext Attributen finden Sie unter [Kontext Anforderungen](context-requirements.md).

Das SSPI-Modell unterstützt drei Arten von Sicherheits Kontexten.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>type</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="connection-oriented-contexts.md">Connection</a></td>
<td>Ein Verbindungs orientierter Kontext ist der gängigste Sicherheitskontext und der einfachste zu verwendende <a href="/windows/desktop/SecGloss/c-gly"><em>Kontext</em></a> . Der Aufrufer ist für das gesamte Nachrichtenformat und für den Speicherort der Daten in der Nachricht verantwortlich. Der Aufrufer ist auch für den Speicherort der sicherheitsrelevanten Felder innerhalb einer Nachricht zuständig, wie z. b. den Speicherort der Signatur Daten.<br/></td>
</tr>
<tr class="even">
<td><a href="datagram-contexts.md">Datagramm</a></td>
<td>Ein <a href="/windows/desktop/SecGloss/d-gly"><em>datagrammorientierter</em></a>Kontext bietet zusätzliche Unterstützung für die Datagramm-Kommunikation im DCE-Stil. Sie kann auch generisch für eine Datagramm-orientierte Transport Anwendung verwendet werden.<br/>
<blockquote>
<p>[!Important]</p>
<p>Das <a href="microsoft-kerberos.md">Microsoft Kerberos</a> -Paket unterstützt keine datagrammkontexte im Benutzer-zu-Benutzer-Modus.<br/></p>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="stream-contexts.md">Datenstrom</a></td>
<td>Ein Datenstrom orientierter Kontext ist für die Blockierung und Nachrichten Formatierung innerhalb des Sicherheitspakets verantwortlich. Der Aufrufer ist nicht an der Formatierung interessiert, sondern vielmehr an einem unformatierten Datenstrom.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kontext Anforderungen](context-requirements.md)
</dt> <dt>

[Verbindungs orientierte Kontexte](connection-oriented-contexts.md)
</dt> <dt>

[Datagramm-Kontexte](datagram-contexts.md)
</dt> <dt>

[Streamkontexte](stream-contexts.md)
</dt> </dl>

 

 
