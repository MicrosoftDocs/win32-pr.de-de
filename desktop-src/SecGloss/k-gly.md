---
description: Enthält Definitionen von Sicherheits Begriffen, die mit dem Buchstaben K beginnen.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: f17042c3-ba1a-408f-af55-5f171b0dee33
title: K (Sicherheits Glossar)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33e7d1b474b774b5cdb7a0b8d05a512a8d291573
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960128"
---
# <a name="k-security-glossary"></a>K (Sicherheits Glossar)

[a](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J K [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_kca_gly"></span><span id="_SECURITY_KCA_GLY"></span>**KCA**
</dt> <dd>

Siehe *Key Certification Authority*.

</dd> <dt>

<span id="_security_kdc_gly"></span><span id="_SECURITY_KDC_GLY"></span>**KDC**
</dt> <dd>

Siehe *Schlüsselverteilungscenter*.

</dd> <dt>

<span id="_security_kea_gly"></span><span id="_SECURITY_KEA_GLY"></span>**KEA**
</dt> <dd>

Siehe *Algorithmus für den Schlüsselaustausch*.

</dd> <dt>

<span id="_security_kerberos_protocol_gly"></span><span id="_SECURITY_KERBEROS_PROTOCOL_GLY"></span>**Kerberos-Protokoll**
</dt> <dd>

Ein Protokoll, mit dem die Interaktion von Clients und Netzwerkauthentifizierungsdiensten definiert wird. Clients erhalten Tickets vom Kerberos Key Distribution Center (KDC), die sie beim Herstellen einer Verbindung an den Server übergeben. Kerberos-Tickets stellen die Netzwerkanmeldeinformationen des Clients dar.

</dd> <dt>

<span id="_security_key_blob_gly"></span><span id="_SECURITY_KEY_BLOB_GLY"></span>**Schlüsselblob**
</dt> <dd>

Ein BLOB, das einen verschlüsselten privaten Schlüssel enthält. Schlüsselblobspeicher bieten eine Möglichkeit zum Speichern von Schlüsseln außerhalb des CSP. Schlüsselblobzeichen werden erstellt, indem ein vorhandener Schlüssel vom CSP exportiert wird, indem die **CryptExportKey** -Funktion aufgerufen wird. Später kann das Schlüsselblob durch Aufrufen der **cryptimportkey** -Funktion in einen Anbieter (häufig ein anderer CSP auf einem anderen Computer) importiert werden. Dadurch wird ein Schlüssel im CSP erstellt, bei dem es sich um ein Duplikat der exportierten handelt.

Siehe auch [*einfaches Schlüsselblob*](s-gly.md), [*öffentliches Schlüsselblob*](p-gly.md)und [*BLOB für den privaten Schlüssel*](p-gly.md).

</dd> <dt>

<span id="_security_key_blob_format_gly"></span><span id="_SECURITY_KEY_BLOB_FORMAT_GLY"></span>**Schlüssel-BLOB-Format**
</dt> <dd>

Das Format des Schlüsselblobs, wenn ein öffentlicher oder ein Sitzungsschlüssel von einem CSP exportiert wird. Das Format wird durch den Anbietertyp des exportierenden CSP angegeben. Ein Schlüsselblob wird erstellt, indem **CryptExportKey** aufgerufen wird.

Siehe auch [*BLOB*](p-gly.md) und [*einfaches Schlüsselblob*](s-gly.md)für öffentliche Schlüssel.

</dd> <dt>

<span id="_security_key_certification_authority_gly"></span><span id="_SECURITY_KEY_CERTIFICATION_AUTHORITY_GLY"></span>**Key Certification Authority**
</dt> <dd>

(KCA) Eine vertrauenswürdige Entität, die in der Regel eine sichere Datenbank von Verbund Nachrichten speichert, die mit dem privaten Schlüssel der KCA signiert sind. Bei praktischen Implementierungen bestehen die Verbund Nachrichten aus dem Namen des Benutzers, dem öffentlichen Schlüssel des Benutzers und allen anderen wichtigen Informationen über den Benutzer. Wenn die empfangende Anwendung eine signierte Nachricht von einem Benutzer erhält, kann die Anwendung dann den mit der Nachricht empfangenen öffentlichen Schlüssel überprüfen, indem Sie Sie mit dem in der KCA-Datenbank gespeicherten öffentlichen Schlüssel vergleicht.

</dd> <dt>

<span id="_security_key_container_gly"></span><span id="_SECURITY_KEY_CONTAINER_GLY"></span>**Schlüssel Container**
</dt> <dd>

Ein Teil der Schlüssel Datenbank, der alle Schlüsselpaare (Exchange-und Signatur Schlüsselpaare) enthält, die zu einem bestimmten Benutzer gehören. Jeder Container verfügt über einen eindeutigen Namen, der beim Aufrufen der **CryptAcquireContext** -Funktion verwendet wird, um ein Handle für den Container zu erhalten.

</dd> <dt>

<span id="_security_key_database_gly"></span><span id="_SECURITY_KEY_DATABASE_GLY"></span>**Schlüssel Datenbank**
</dt> <dd>

Eine Datenbank, die die persistenten Kryptografieschlüssel für einen bestimmten CSP enthält. Die Datenbank enthält einen oder mehrere Schlüssel Container, die einzeln alle Kryptografieschlüsselpaare für einen bestimmten Benutzer speichern.

Siehe auch *Key Container*.

</dd> <dt>

<span id="_security_key_distribution_center_gly"></span><span id="_SECURITY_KEY_DISTRIBUTION_CENTER_GLY"></span>**Schlüsselverteilungscenter**
</dt> <dd>

KDC Ein Netzwerkdienst, der Sitzungs Tickets und temporäre Sitzungsschlüssel für das Kerberos V5-Authentifizierungsprotokoll bereitstellt. Der KDC wird auf allen Domänen Controllern als privilegierter Prozess ausgeführt.

Siehe auch *Kerberos-Protokoll*.

</dd> <dt>

<span id="_security_key_exchange_algorithm_gly"></span><span id="_SECURITY_KEY_EXCHANGE_ALGORITHM_GLY"></span>**Algorithmus für den Schlüsselaustausch**
</dt> <dd>

Ein Algorithmus, der zum Verschlüsseln und Entschlüsseln von Exchange-Schlüsseln (symmetrische Sitzungsschlüssel) verwendet wird. Einige gängige Schlüsselaustausch Algorithmen umfassen Diffie-Hellman und Kea, den Schlüsselaustausch Algorithmus, der durch einen Prov \_ Fortezza-Anbietertyp angegeben wird. Der KEA-Algorithmus ist eine verbesserte Version des Diffie-Hellman Algorithmus. Jeder Anbietertyp kann nur einen Schlüsselaustausch Algorithmus angeben.

</dd> <dt>

<span id="_security_key_exchange_algorithm_name_gly"></span><span id="_SECURITY_KEY_EXCHANGE_ALGORITHM_NAME_GLY"></span>**Algorithmus für den Schlüsselaustausch**
</dt> <dd>

(KEA) Der Schlüsselaustausch Algorithmus, der durch einen Prov- \_ Fortezza-Anbietertyp angegeben wird. Dieser Algorithmus ist eine verbesserte Version des Diffie-Hellman Algorithmus.

</dd> <dt>

<span id="_security_key_exchange_certificate_gly"></span><span id="_SECURITY_KEY_EXCHANGE_CERTIFICATE_GLY"></span>**Schlüsselaustausch Zertifikat**
</dt> <dd>

Ein Zertifikat zum Verschlüsseln von Informationen, die an eine andere Partei gesendet werden. Das Zertifikat der Zertifizierungsstelle (Certification Authority, ca) kann von einem Client verwendet werden, um Informationen zu verschlüsseln, die an die Zertifizierungsstelle gesendet werden.

</dd> <dt>

<span id="_security_key_exchange_functions_gly"></span><span id="_SECURITY_KEY_EXCHANGE_FUNCTIONS_GLY"></span>**Schlüsselaustausch Funktionen**
</dt> <dd>

Eine Reihe von Funktionen, die zum austauschen oder übertragen von Schlüsseln verwendet werden. Schlüsselaustausch Funktionen können auch verwendet werden, um vollständig authentifizierte dreiphasige Schlüsselaustausch Vorgänge zu implementieren.

</dd> <dt>

<span id="_security_key_exchange_key_pair_gly"></span><span id="_SECURITY_KEY_EXCHANGE_KEY_PAIR_GLY"></span>**Schlüsselaustausch-Schlüsselpaar**
</dt> <dd>

Siehe [*Exchange-Schlüsselpaar*](e-gly.md).

</dd> <dt>

<span id="_security_key_exchange_private_key_gly"></span><span id="_SECURITY_KEY_EXCHANGE_PRIVATE_KEY_GLY"></span>**privater Schlüsselaustausch Schlüssel**
</dt> <dd>

Der private Schlüssel eines Exchange-Schlüssel Paars.

Siehe auch [*Exchange-Schlüsselpaar*](e-gly.md).

</dd> <dt>

<span id="_security_key_exchange_protocol_gly"></span><span id="_SECURITY_KEY_EXCHANGE_PROTOCOL_GLY"></span>**Schlüsselaustausch Protokoll**
</dt> <dd>

Ein Protokoll, mit dem zwei Parteien Informationen austauschen, um einen gemeinsamen geheimen Schlüssel einzurichten. Der gemeinsame geheime Schlüssel wird dann in der Regel als symmetrischer Verschlüsselungsschlüssel verwendet.

</dd> <dt>

<span id="_security_key_exchange_public_key_gly"></span><span id="_SECURITY_KEY_EXCHANGE_PUBLIC_KEY_GLY"></span>**öffentlicher Schlüsselaustausch Schlüssel**
</dt> <dd>

Der öffentliche Schlüssel eines Exchange-Schlüssel Paars.

Siehe auch [*Exchange-Schlüsselpaar*](e-gly.md).

</dd> <dt>

<span id="_security_key_generation_functions_gly"></span><span id="_SECURITY_KEY_GENERATION_FUNCTIONS_GLY"></span>**Schlüssel Generierungs Funktionen**
</dt> <dd>

Eine Reihe von Funktionen, die von Anwendungen verwendet werden, um kryptografische Schlüssel zu generieren und anzupassen. Diese Funktionen umfassen die vollständige Unterstützung für das Ändern von Verkettungs Modi, Initialisierungs Vektoren und anderen Verschlüsselungsfunktionen.

</dd> <dt>

<span id="_security_key_length_gly"></span><span id="_SECURITY_KEY_LENGTH_GLY"></span>**Schlüssellänge**
</dt> <dd>

Werte, die von einigen Anbietern angegeben werden, die die Länge der öffentlichen/privaten Schlüsselpaare und Sitzungsschlüssel angeben, die mit diesem Anbieter verwendet werden.

</dd> <dt>

<span id="_security_key_pair_gly"></span><span id="_SECURITY_KEY_PAIR_GLY"></span>**Schlüsselpaar**
</dt> <dd>

Einen privaten Schlüssel und den zugehörigen öffentlichen Schlüssel.

</dd> <dt>

<span id="_security_key_storage_provider_gly"></span><span id="_SECURITY_KEY_STORAGE_PROVIDER_GLY"></span>**Schlüsselspeicher Anbieter**
</dt> <dd>

KSP Ein unabhängiges Softwaremodul, das Funktionen zum Erstellen, verwalten, speichern und Abrufen [*privater Schlüssel*](p-gly.md)implementiert.

</dd> <dt>

<span id="_security_ksp_gly"></span><span id="_SECURITY_KSP_GLY"></span>**KSP**
</dt> <dd>

Siehe *Schlüsselspeicher Anbieter*.

</dd> </dl>

 

 



