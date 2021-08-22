---
description: Enthält Definitionen von Sicherheitsbegriffen, die mit dem Buchstaben K beginnen.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: f17042c3-ba1a-408f-af55-5f171b0dee33
title: K (Sicherheitsglossar)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7c92abf9b3df1eb49f0caaee90ccbce8755d003478683aba35570d9ea99fa2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118895593"
---
# <a name="k-security-glossary"></a>K (Sicherheitsglossar)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J K [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) T [U](t-gly.md) [](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_kca_gly"></span><span id="_SECURITY_KCA_GLY"></span>**Kca**
</dt> <dd>

Weitere Informationen *finden Sie unter Schlüsselzertifizierungsstelle.*

</dd> <dt>

<span id="_security_kdc_gly"></span><span id="_SECURITY_KDC_GLY"></span>**Kdc**
</dt> <dd>

Siehe *Schlüsselverteilungscenter*.

</dd> <dt>

<span id="_security_kea_gly"></span><span id="_SECURITY_KEA_GLY"></span>**Kea**
</dt> <dd>

Weitere Informationen *finden Sie unter Schlüsselaustauschalgorithmus*.

</dd> <dt>

<span id="_security_kerberos_protocol_gly"></span><span id="_SECURITY_KERBEROS_PROTOCOL_GLY"></span>**Kerberos-Protokoll**
</dt> <dd>

Ein Protokoll, mit dem die Interaktion von Clients und Netzwerkauthentifizierungsdiensten definiert wird. Clients erhalten Tickets vom Kerberos Key Distribution Center (KDC), die sie beim Herstellen einer Verbindung an den Server übergeben. Kerberos-Tickets stellen die Netzwerkanmeldeinformationen des Clients dar.

</dd> <dt>

<span id="_security_key_blob_gly"></span><span id="_SECURITY_KEY_BLOB_GLY"></span>**SchlüsselBLOB**
</dt> <dd>

Ein BLOB, das einen verschlüsselten privaten Schlüssel enthält. Schlüsselblobs bieten eine Möglichkeit, Schlüssel außerhalb des CSP zu speichern. Schlüsselblobs werden erstellt, indem ein vorhandener Schlüssel aus dem CSP exportiert wird, indem die **CryptExportKey-Funktion aufruft.** Später kann das Schlüsselblob durch Aufrufen der **CryptImportKey-Funktion** in einen Anbieter importiert werden (häufig in einen anderen CSP auf einem anderen Computer). Dadurch wird ein Schlüssel im CSP erstellt, der ein Duplikat des exportierten Schlüssels ist.

Siehe auch [*einfaches SchlüsselBLOB,*](s-gly.md) [*Blob mit öffentlichem Schlüssel*](p-gly.md)und BLOB mit [*privatem Schlüssel.*](p-gly.md)

</dd> <dt>

<span id="_security_key_blob_format_gly"></span><span id="_SECURITY_KEY_BLOB_FORMAT_GLY"></span>**SchlüsselBLOB-Format**
</dt> <dd>

Das Format des Schlüsselblobs, wenn ein öffentlicher Schlüssel oder Sitzungsschlüssel aus einem CSP exportiert wird. Das Format wird vom Anbietertyp des exportierenden CSP angegeben. Ein SchlüsselBLOB wird durch Aufrufen von **CryptExportKey erstellt.**

Siehe auch [*Blob mit öffentlichem Schlüssel*](p-gly.md) und blob mit [*einfachem Schlüssel.*](s-gly.md)

</dd> <dt>

<span id="_security_key_certification_authority_gly"></span><span id="_SECURITY_KEY_CERTIFICATION_AUTHORITY_GLY"></span>**Schlüsselzertifizierungsstelle**
</dt> <dd>

(KCA) Eine vertrauenswürdige Entität, die in der Regel eine sichere Datenbank von Verbundnachrichten speichert, die mit dem privaten Schlüssel des KCA signiert sind. In praktischen Implementierungen bestehen die zusammengesetzten Nachrichten aus dem Namen des Benutzers, dem öffentlichen Schlüssel des Benutzers und allen anderen wichtigen Informationen zum Benutzer. Wenn die empfangende Anwendung eine signierte Nachricht von einem Benutzer erhält, kann die Anwendung den mit der Nachricht empfangenen öffentlichen Schlüssel überprüfen, indem sie ihn mit dem in der KCA-Datenbank gespeicherten öffentlichen Schlüssel vergleicht.

</dd> <dt>

<span id="_security_key_container_gly"></span><span id="_SECURITY_KEY_CONTAINER_GLY"></span>**Schlüsselcontainer**
</dt> <dd>

Ein Teil der Schlüsseldatenbank, der alle Schlüsselpaare (Austausch- und Signaturschlüsselpaare) enthält, die zu einem bestimmten Benutzer gehören. Jeder Container hat einen eindeutigen Namen, der beim Aufrufen der **CryptAcquireContext-Funktion** verwendet wird, um ein Handle für den Container zu erhalten.

</dd> <dt>

<span id="_security_key_database_gly"></span><span id="_SECURITY_KEY_DATABASE_GLY"></span>**Schlüsseldatenbank**
</dt> <dd>

Eine Datenbank, die die persistenten kryptografischen Schlüssel für einen bestimmten CSP enthält. Die Datenbank enthält mindestens einen Schlüsselcontainer, in dem alle kryptografischen Schlüsselpaare für einen bestimmten Benutzer einzeln gespeichert werden.

Siehe auch *Schlüsselcontainer*.

</dd> <dt>

<span id="_security_key_distribution_center_gly"></span><span id="_SECURITY_KEY_DISTRIBUTION_CENTER_GLY"></span>**Schlüsselverteilungscenter**
</dt> <dd>

(KDC) Ein Netzwerkdienst, der Sitzungstickets und temporäre Sitzungsschlüssel zur Verfügung stellt, die im Kerberos V5-Authentifizierungsprotokoll verwendet werden. Das KDC wird als privilegierter Prozess auf allen Domänencontrollern ausgeführt.

Siehe auch *Kerberos-Protokoll*.

</dd> <dt>

<span id="_security_key_exchange_algorithm_gly"></span><span id="_SECURITY_KEY_EXCHANGE_ALGORITHM_GLY"></span>**Schlüsselaustauschalgorithmus**
</dt> <dd>

Ein Algorithmus zum Verschlüsseln und Entschlüsseln von Austauschschlüsseln (symmetrische Sitzungsschlüssel). Einige gängige Schlüsselaustauschalgorithmen sind Diffie-Hellman und KEA, der von einem PROV FORTEZZA-Anbietertyp angegebene \_ Schlüsselaustauschalgorithmus. Der KEA-Algorithmus ist eine verbesserte Version des Diffie-Hellman Algorithmus. Jeder Anbietertyp kann nur einen Schlüsselaustauschalgorithmus angeben.

</dd> <dt>

<span id="_security_key_exchange_algorithm_name_gly"></span><span id="_SECURITY_KEY_EXCHANGE_ALGORITHM_NAME_GLY"></span>**Key Exchange Algorithm**
</dt> <dd>

(KEA) Der von einem PROV \_ FORTEZZA-Anbietertyp angegebene Schlüsselaustauschalgorithmus. Dieser Algorithmus ist eine verbesserte Version des Diffie-Hellman Algorithmus.

</dd> <dt>

<span id="_security_key_exchange_certificate_gly"></span><span id="_SECURITY_KEY_EXCHANGE_CERTIFICATE_GLY"></span>**Schlüsselaustauschzertifikat**
</dt> <dd>

Ein Zertifikat, das zum Verschlüsseln von Informationen verwendet wird, die an eine andere Partei gesendet werden. Das Schlüsselaustauschzertifikat der Zertifizierungsstelle kann von einem Client verwendet werden, um an die Zertifizierungsstelle gesendete Informationen zu verschlüsseln.

</dd> <dt>

<span id="_security_key_exchange_functions_gly"></span><span id="_SECURITY_KEY_EXCHANGE_FUNCTIONS_GLY"></span>**Schlüsselaustauschfunktionen**
</dt> <dd>

Eine Reihe von Funktionen, die zum Austauschen oder Übertragen von Schlüsseln verwendet werden. Schlüsselaustauschfunktionen können auch verwendet werden, um vollständig authentifizierte Dreiphasen-Schlüsselaustausche zu implementieren.

</dd> <dt>

<span id="_security_key_exchange_key_pair_gly"></span><span id="_SECURITY_KEY_EXCHANGE_KEY_PAIR_GLY"></span>**Schlüsselaustausch-Schlüsselpaar**
</dt> <dd>

Weitere Informationen finden [*Sie unter Austauschschlüsselpaar*](e-gly.md).

</dd> <dt>

<span id="_security_key_exchange_private_key_gly"></span><span id="_SECURITY_KEY_EXCHANGE_PRIVATE_KEY_GLY"></span>**Privater Schlüsselaustauschschlüssel**
</dt> <dd>

Der private Schlüssel eines Austauschschlüsselpaars.

Siehe auch [*Austauschschlüsselpaar*](e-gly.md).

</dd> <dt>

<span id="_security_key_exchange_protocol_gly"></span><span id="_SECURITY_KEY_EXCHANGE_PROTOCOL_GLY"></span>**Schlüsselaustauschprotokoll**
</dt> <dd>

Ein Protokoll, mit dem zwei Parteien Informationen austauschen, um ein gemeinsames Geheimnis zu erstellen. Das gemeinsame Geheimnis wird dann in der Regel als symmetrischer Verschlüsselungsschlüssel verwendet.

</dd> <dt>

<span id="_security_key_exchange_public_key_gly"></span><span id="_SECURITY_KEY_EXCHANGE_PUBLIC_KEY_GLY"></span>**Öffentlicher Schlüssel für den Schlüsselaustausch**
</dt> <dd>

Der öffentliche Schlüssel eines Austauschschlüsselpaars.

Siehe auch [*Austauschschlüsselpaar*](e-gly.md).

</dd> <dt>

<span id="_security_key_generation_functions_gly"></span><span id="_SECURITY_KEY_GENERATION_FUNCTIONS_GLY"></span>**Schlüsselgenerierungsfunktionen**
</dt> <dd>

Eine Reihe von Funktionen, die von Anwendungen zum Generieren und Anpassen kryptografischer Schlüssel verwendet werden. Diese Funktionen umfassen vollständige Unterstützung für das Ändern von Verkettungsmodi, Initialisierungsvektoren und anderen Verschlüsselungsfeatures.

</dd> <dt>

<span id="_security_key_length_gly"></span><span id="_SECURITY_KEY_LENGTH_GLY"></span>**Schlüssellänge**
</dt> <dd>

Werte, die von einigen Anbietern angegeben werden, die die Länge der öffentlichen/privaten Schlüsselpaare und Sitzungsschlüssel angeben, die mit diesem Anbieter verwendet werden.

</dd> <dt>

<span id="_security_key_pair_gly"></span><span id="_SECURITY_KEY_PAIR_GLY"></span>**Schlüsselpaar**
</dt> <dd>

Ein privater Schlüssel und der zugehörige öffentliche Schlüssel.

</dd> <dt>

<span id="_security_key_storage_provider_gly"></span><span id="_SECURITY_KEY_STORAGE_PROVIDER_GLY"></span>**Schlüsselspeicheranbieter**
</dt> <dd>

(KSP) Ein unabhängiges Softwaremodul, das Funktionen zum Erstellen, Verwalten, Speichern und Abrufen privater [*Schlüssel implementiert.*](p-gly.md)

</dd> <dt>

<span id="_security_ksp_gly"></span><span id="_SECURITY_KSP_GLY"></span>**Ksp**
</dt> <dd>

Weitere Informationen *finden Sie unter Schlüsselspeicheranbieter.*

</dd> </dl>

 

 



