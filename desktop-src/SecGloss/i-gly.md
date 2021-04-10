---
description: Enthält Definitionen von Sicherheits Begriffen, die mit dem Buchstaben I beginnen.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: af511aed-88f5-4b12-ad44-317925297f70
title: I (Sicherheits Glossar)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1d3e727128c2494f313bdffc879b5c5e47a28ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042600"
---
# <a name="i-security-glossary"></a>I (Sicherheits Glossar)

[a](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) I J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_iis_gly"></span><span id="_SECURITY_IIS_GLY"></span>**Ausschalten**
</dt> <dd>

Software Dienste, die die Erstellung, Konfiguration und Verwaltung von Websites sowie andere Internet Funktionen unterstützen. Internetinformationsdienste include Network News Transfer Protocol (NNTP), File Transfer Protocol (FTP) und Simple Mail Transfer Protocol (SMTP). IIS umfasst verschiedene Funktionen für die Sicherheit, ermöglicht CGI-Anwendungen und bietet Gopher-und FTP-Server.

</dd> <dt>

<span id="_security_impersonation_gly"></span><span id="_SECURITY_IMPERSONATION_GLY"></span>**Identitätswechsel**
</dt> <dd>

Ein Mechanismus, mit dem ein Server Prozess mithilfe der Sicherheits Anmelde Informationen des Clients oder eines anderen Benutzers ausgeführt werden kann, der die Anmelde Informationen verwendet. Wenn der Server die Identität des Clients annimmt, werden alle Vorgänge, die vom Server ausgeführt werden, mithilfe der Anmelde Informationen des Clients (Identität des Benutzers) ausgeführt. Durch den Identitätswechsel kann der Server nicht auf Remote Ressourcen im Namen des Clients zugreifen. Hierfür ist eine Delegierung erforderlich.

</dd> <dt>

<span id="_security_impersonation_token_gly"></span><span id="_SECURITY_IMPERSONATION_TOKEN_GLY"></span>**Identitätswechsel Token**
</dt> <dd>

Ein Zugriffs Token, das erstellt wurde, um die Sicherheitsinformationen eines Client Prozesses zu erfassen, sodass ein Server die Identität des Client Prozesses in sicherheitsvorgängen annehmen kann.

Siehe auch [*Zugriffs Token*](a-gly.md) und [*primäres Token*](p-gly.md).

</dd> <dt>

<span id="_security_initialization_vector_gly"></span><span id="_SECURITY_INITIALIZATION_VECTOR_GLY"></span>**Initialisierungs Vektor**
</dt> <dd>

(IV) eine Sequenz zufälliger bytes, die vor der Verschlüsselung durch eine Blockchiffre an den Anfang des Klartext angehängt werden. Wenn Sie den Initialisierungs Vektor am Anfang des Klartext hinzufügen, ist es nicht mehr möglich, den ursprünglichen Chiffre Text für zwei Nachrichten gleich zu lassen. Wenn Nachrichten z. b. immer mit einem gemeinsamen Header (einem Brief Kopf oder einer "von"-Zeile) beginnen, wäre Ihr ursprünglicher Chiffre Text immer identisch, wobei angenommen wird, dass derselbe Kryptografiealgorithmus und derselbe symmetrische Schlüssel verwendet wurden. Durch das Hinzufügen eines zufälligen Initialisierungs Vektors wird dies vermieden.

</dd> <dt>

<span id="_security_inner_data_gly"></span><span id="_SECURITY_INNER_DATA_GLY"></span>**Innere Daten**
</dt> <dd>

Alle codierten Daten, die als Nachricht für eine andere codierte Nachricht verwendet werden. Eine eingeschlossene Nachricht und Ihr Hashwert können z. b. die inneren Daten für eine zweite Nachricht sein.

</dd> <dt>

<span id="_security_inner_content_gly"></span><span id="_SECURITY_INNER_CONTENT_GLY"></span>**innerer Inhalt**
</dt> <dd>

Erweiterte Daten, z. b. mit einer digitalen Signatur. Dieser Begriff wird hauptsächlich bei der Erörterung von erweiterten Daten in einer PKCS \# 7-Nachricht verwendet.

</dd> <dt>

<span id="_security_integrity_gly"></span><span id="_SECURITY_INTEGRITY_GLY"></span>**Integrität**
</dt> <dd>

Die Vollständigkeit und Genauigkeit einer Nachricht, nachdem Sie gesendet oder gespeichert wurde.

</dd> <dt>

<span id="_security_integrity_sid_gly"></span><span id="_SECURITY_INTEGRITY_SID_GLY"></span>**Integritäts-sid**
</dt> <dd>

Eine [*Sicherheits*](s-gly.md) -ID (SID), die eine Integritäts Ebene darstellt. Eine Integritäts-sid in der [*System-Zugriffs Steuerungs Liste*](s-gly.md) (SACL) der Sicherheits Beschreibung eines Objekts gibt die Integritäts Stufe des Objekts an. Integritäts-SIDs in einem Zugriffs Token geben die Integritäts Stufe des Tokens an.

</dd> <dt>

<span id="_security_interrupt_request_level_gly"></span><span id="_SECURITY_INTERRUPT_REQUEST_LEVEL_GLY"></span>**IRQL**
</dt> <dd>

Eine Interrupt Request Level (unql) definiert die Hardware Priorität, mit der ein Prozessor zu einem beliebigen Zeitpunkt arbeitet. In der Windows-Treibermodell kann ein Thread, der mit einem niedrigen "iriql" ausgeführt wird, unterbrochen werden, um Code bei einem höheren "iriql" auszuführen.

</dd> <dt>

<span id="_security_iv_gly"></span><span id="_SECURITY_IV_GLY"></span>**Heinrich**
</dt> <dd>

Siehe *Initialisierungs Vektor*.

</dd> </dl>

 

 



