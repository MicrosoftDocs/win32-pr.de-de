---
description: Enthält Definitionen von Sicherheits Begriffen, die mit dem Buchstaben "P" beginnen.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a
title: P (Sicherheits Glossar)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd5b580295c35bc021ade53d3cb922ce8fe13d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866631"
---
# <a name="p-security-glossary"></a>P (Sicherheits Glossar)

[a](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) P Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_padding_gly"></span><span id="_SECURITY_PADDING_GLY"></span>**Auffüllung**
</dt> <dd>

Eine Zeichenfolge, die im Allgemeinen hinzugefügt wird, wenn der letzte Klartextblock kurz ist. Wenn die Blocklänge beispielsweise 64 Bits beträgt und der letzte Block nur 40 Bits enthält, müssen dem letzten Block 24 Bits von Auffüll Zeichen hinzugefügt werden. Die Auffüll Zeichenfolge enthält möglicherweise Nullen, abwechselnde Nullen und solche oder ein anderes Muster. Anwendungen, die [*CryptoAPI*](c-gly.md) verwenden, müssen Ihren Klartext keine Auffüll Zeichen hinzufügen, bevor Sie verschlüsselt werden, und Sie müssen Sie nach der Entschlüsselung nicht entfernen. Dies erfolgt automatisch.

</dd> <dt>

<span id="_security_password_filter_gly"></span><span id="_SECURITY_PASSWORD_FILTER_GLY"></span>**Kenn Wortfilter**
</dt> <dd>

Eine DLL, die die Durchsetzung von Kenn Wort Richtlinien und Änderungs Benachrichtigungen bereitstellt Die von Kenn Wort Filtern implementierten Funktionen werden von der [*lokalen Sicherheits Autorität*](l-gly.md)aufgerufen.

</dd> <dt>

<span id="_security_persistent_storage_gly"></span><span id="_SECURITY_PERSISTENT_STORAGE_GLY"></span>**persistenter Speicher**
</dt> <dd>

Jedes Speichermedium, das intakt bleibt, wenn die Stromversorgung getrennt ist. Viele [*Zertifikat*](c-gly.md) Speicher Datenbanken sind Formen des permanenten Speichers.

</dd> <dt>

<span id="_security_pkcs_gly"></span><span id="_SECURITY_PKCS_GLY"></span>**PKCS**
</dt> <dd>

Siehe *Kryptografiestandards für öffentliche Schlüssel*.

</dd> <dt>

<span id="_security_pkcs_1_standard_gly"></span><span id="_SECURITY_PKCS_1_STANDARD_GLY"></span>**PKCS \# 1**
</dt> <dd>

Die empfohlenen Standards für die Implementierung der Kryptografie mit öffentlichem Schlüssel, die auf dem RSA-Algorithmus basiert, wie in [RFC 3447](https://tools.ietf.org/html/rfc3447)definiert.

</dd> <dt>

<span id="_security_pkcs_12_standard_gly"></span><span id="_SECURITY_PKCS_12_STANDARD_GLY"></span>**PKCS \# 12**
</dt> <dd>

Der Standard mäßig von RSA Data Security, Inc. entwickelte und beibegefasste Syntax Standard für den persönlichen Informationsaustausch Dieser Syntax Standard gibt ein portables Format zum Speichern oder transportieren der privaten Schlüssel, Zertifikate und sonstigen geheimen Schlüssel eines Benutzers an.

Siehe auch *Kryptografiestandards* für [*Zertifikate*](c-gly.md) und öffentliche Schlüssel.

</dd> <dt>

<span id="_security_pkcs_7_signed_data_gly"></span><span id="_SECURITY_PKCS_7_SIGNED_DATA_GLY"></span>**Mit PKCS \# 7 signierte Daten**
</dt> <dd>

Ein Datenobjekt, das mit dem öffentlichen Schlüssel Kryptografiestandard \# 7 (PKCS \# 7) signiert ist und die Informationen kapselt, die zum Signieren einer Datei verwendet werden. In der Regel enthält Sie das Zertifikat des Signatur Gebers und das Stamm [*Zertifikat*](r-gly.md).

</dd> <dt>

<span id="_security_pkcs_7_standard_gly"></span><span id="_SECURITY_PKCS_7_STANDARD_GLY"></span>**PKCS \# 7**
</dt> <dd>

Der Cryptographic Message Syntax (CMS)-Standard. Eine allgemeine Syntax für Daten, bei denen Kryptografie eingesetzt werden könnte, beispielsweise digitale Signaturen und Verschlüsselungen. Außerdem wird eine Syntax für die Verteilung von Zertifikaten oder Zertifikat Sperr Listen sowie anderer Nachrichten Attribute (z. b. Zeitstempel) für die Nachricht bereitstellt.

</dd> <dt>

<span id="_security_pkcs_7_asn_encoding_gly"></span><span id="_SECURITY_PKCS_7_ASN_ENCODING_GLY"></span>**PKCS \_ 7- \_ ASN- \_ Codierung**
</dt> <dd>

Ein [*Nachrichten Codierungstyp*](m-gly.md). Nachrichten Codierungs Typen werden im höherwertigen Wort eines **DWORD** gespeichert (Wert: 0x00010000 bis).

</dd> <dt>

<span id="_security_plaintext_gly"></span><span id="_SECURITY_PLAINTEXT_GLY"></span>**nur**
</dt> <dd>

Eine unverschlüsselte Nachricht. Nachrichten, die nicht verschlüsselt sind, werden mitunter auch als Klartextnachrichten bezeichnet.

</dd> <dt>

<span id="_security_portable_executable_pe_image_gly"></span><span id="_SECURITY_PORTABLE_EXECUTABLE_PE_IMAGE_GLY"></span>**Bild der portablen ausführbaren Datei (PE)**
</dt> <dd>

Das standardmäßige ausführbare Windows-Format.

</dd> <dt>

<span id="_security_prf_gly"></span><span id="_SECURITY_PRF_GLY"></span>**PRF**
</dt> <dd>

Siehe *Pseudo Zufallsfunktion*.

</dd> <dt>

<span id="_security_primary_credentials_gly"></span><span id="_SECURITY_PRIMARY_CREDENTIALS_GLY"></span>**primäre Anmelde Informationen**
</dt> <dd>

Das \_ Authentifizierungs Paket MsV1 0 definiert einen primären Zeichen folgen Wert für die Anmelde Informationen: die primäre Anmelde Informations Zeichenfolge enthält die Anmelde Informationen, die bei der ersten Anmeldung bereitgestellt werden Sie enthält den Benutzernamen und sowohl die Groß-/Kleinschreibung als auch die Groß-/Kleinschreibung für das Kennwort des Benutzers.

Weitere Informationen finden Sie unter [*ergänzende Anmelde*](s-gly.md)Informationen.

</dd> <dt>

<span id="_security_primary_service_provider_gly"></span><span id="_SECURITY_PRIMARY_SERVICE_PROVIDER_GLY"></span>**primärer Dienstanbieter**
</dt> <dd>

Der Dienstanbieter, der die Steuerungs Schnittstellen für die Karte bereitstellt. Jede Smartcard kann Ihren primären Dienstanbieter in der Smartcard-Datenbank registrieren.

</dd> <dt>

<span id="_security_primary_token_gly"></span><span id="_SECURITY_PRIMARY_TOKEN_GLY"></span>**primäres Token**
</dt> <dd>

Ein Zugriffs Token, das in der Regel nur vom Windows-Kernel erstellt wird. Sie kann einem Prozess zugewiesen werden, der die Standard Sicherheitsinformationen für diesen Prozess darstellt.

Siehe auch [*Zugriffs Token*](a-gly.md) und Identitätswechsel [*Token*](i-gly.md).

</dd> <dt>

<span id="_security_principal_gly"></span><span id="_SECURITY_PRINCIPAL_GLY"></span>**Prinzipal**
</dt> <dd>

Siehe [*Sicherheits Prinzipal*](s-gly.md).

</dd> <dt>

<span id="_security_privacy_gly"></span><span id="_SECURITY_PRIVACY_GLY"></span>**Datenschutz**
</dt> <dd>

Die Bedingung, dass Sie von der Sicht oder dem geheimen Schlüssel isoliert werden. In Bezug auf Nachrichten sind private Nachrichten verschlüsselte Nachrichten, deren Text aus der Ansicht ausgeblendet ist. In Bezug auf Schlüssel ist ein privater Schlüssel ein geheimer Schlüssel, der von anderen Personen verborgen ist.

</dd> <dt>

<span id="_security_private_key_gly"></span><span id="_SECURITY_PRIVATE_KEY_GLY"></span>**privater Schlüssel**
</dt> <dd>

Die geheime Hälfte eines Schlüssel Paars, das in einem Algorithmus für öffentliche Schlüssel verwendet wird. Private Schlüssel werden normalerweise zur Verschlüsselung von symmetrischen Sitzungsschlüsseln, zur digitalen Signierung von Nachrichten oder zur Entschlüsselung von Nachrichten, die mit dem entsprechenden öffentlichen Schlüssel verschlüsselt wurden, verwendet.

Siehe auch *öffentlicher Schlüssel*.

</dd> <dt>

<span id="_security_private_key_blob_gly"></span><span id="_SECURITY_PRIVATE_KEY_BLOB_GLY"></span>**BLOB des privaten Schlüssels**
</dt> <dd>

Ein Schlüssel-BLOB, das ein ganzes öffentliches/privates Schlüsselpaar enthält. Private schlüsselblobschlüssel werden von Verwaltungsprogrammen verwendet, um Schlüsselpaare zu transportieren. Da der private Schlüsselteil des Schlüssel Paars äußerst vertraulich ist, werden diese BLOB in der Regel mit einer symmetrischen Chiffre verschlüsselt. Diese Schlüsselblob können auch von erweiterten Anwendungen verwendet werden, bei denen die Schlüsselpaare innerhalb der Anwendung gespeichert werden, anstatt sich auf den Speichermechanismus des CSP zu verlassen. Ein Schlüsselblob wird durch Aufrufen der **CryptExportKey** -Funktion erstellt.

</dd> <dt>

<span id="_security_privilege_gly"></span><span id="_SECURITY_PRIVILEGE_GLY"></span>**Ehre**
</dt> <dd>

Das Recht eines Benutzers zur Durchführung verschiedener Systemvorgänge wie Herunterfahren des Systems, Laden von Gerätetreibern oder Ändern der Systemzeit. Das Zugriffs Token eines Benutzers enthält eine Liste der Berechtigungen, die der Benutzer oder die Benutzergruppen innehat.

</dd> <dt>

<span id="_security_process_gly"></span><span id="_SECURITY_PROCESS_GLY"></span>**ESS**
</dt> <dd>

Der Sicherheitskontext, in dem eine Anwendung ausgeführt wird. Der Sicherheitskontext ist normalerweise einem Benutzer zugeordnet, sodass alle Anwendungen, die unter einem bestimmten Prozess ausgeführt werden, die Rechte und Berechtigungen des entsprechenden Benutzers übernehmen.

</dd> <dt>

<span id="_security_prov_dss_gly"></span><span id="_SECURITY_PROV_DSS_GLY"></span>**Prov- \_ DSS**
</dt> <dd>

Siehe *Prov \_ DSS Provider Type*.

</dd> <dt>

<span id="_security_prov_dss_provider_type_gly"></span><span id="_SECURITY_PROV_DSS_PROVIDER_TYPE_GLY"></span>**Prov \_ DSS-Anbietertyp**
</dt> <dd>

Der vordefinierte Anbietertyp, der nur digitale Signaturen und Hashes unterstützt. Er gibt den DSA-Signatur Algorithmus und die MD5-und SHA-1-Hash Algorithmen an.

</dd> <dt>

<span id="_security_prov_dss_dh_gly"></span><span id="_SECURITY_PROV_DSS_DH_GLY"></span>**Prov \_ DSS \_ dh**
</dt> <dd>

Siehe *Prov \_ DSS \_ dh-Anbietertyp*.

</dd> <dt>

<span id="_security_prov_dss_dh_provider_type_gly"></span><span id="_SECURITY_PROV_DSS_DH_PROVIDER_TYPE_GLY"></span>**Prov \_ DSS \_ dh-Anbietertyp**
</dt> <dd>

Der vordefinierte Anbietertyp, der Schlüsselaustausch-, digitale Signatur-und Hash Algorithmen bereitstellt. Dies ähnelt dem Prov- \_ DSS-Anbietertyp.

</dd> <dt>

<span id="_security_prov_fortezza_gly"></span><span id="_SECURITY_PROV_FORTEZZA_GLY"></span>**Prov- \_ Fortezza**
</dt> <dd>

Siehe *Prov \_ Fortezza-Anbietertyp*.

</dd> <dt>

<span id="_security_prov_fortezza_provider_type_gly"></span><span id="_SECURITY_PROV_FORTEZZA_PROVIDER_TYPE_GLY"></span>**Prov \_ Fortezza-Anbietertyp**
</dt> <dd>

Der vordefinierte Anbietertyp, der Schlüsselaustausch-, digitale Signatur-, Verschlüsselungs-und Hash Algorithmen bereitstellt. Die kryptografischen Protokolle und Algorithmen, die von diesem Anbietertyp angegeben werden, sind im Besitz des National Institute of Standards and Technology (NIST).

</dd> <dt>

<span id="_security_prov_ms_exchange_gly"></span><span id="_SECURITY_PROV_MS_EXCHANGE_GLY"></span>**Prov \_ MS \_ Exchange**
</dt> <dd>

Siehe *Prov \_ MS \_ Exchange-Anbietertyp*.

</dd> <dt>

<span id="_security_prov_ms_exchange_provider_type_gly"></span><span id="_SECURITY_PROV_MS_EXCHANGE_PROVIDER_TYPE_GLY"></span>**Prov \_ MS \_ Exchange-Anbietertyp**
</dt> <dd>

Der vordefinierte Anbietertyp, der für die Anforderungen von Microsoft Exchange konzipiert ist, sowie andere Anwendungen, die mit Microsoft Mail kompatibel sind. Es stellt Schlüsselaustausch-, digitale Signatur-, Verschlüsselungs-und Hash Algorithmen bereit.

</dd> <dt>

<span id="_security_prov_rsa_full_gly"></span><span id="_SECURITY_PROV_RSA_FULL_GLY"></span>**Prov \_ RSA \_ Full**
</dt> <dd>

Siehe *Prov \_ RSA \_ Full Provider Type*.

</dd> <dt>

<span id="_security_prov_rsa_full_provider_type_gly"></span><span id="_SECURITY_PROV_RSA_FULL_PROVIDER_TYPE_GLY"></span>**Prov \_ RSA \_ Full-Anbietertyp**
</dt> <dd>

Der von Microsoft und RSA Data Security, Inc. definierte vordefinierte Anbietertyp. Dieser allgemeine Anbietertyp stellt Schlüsselaustausch-, digitale Signatur-, Verschlüsselungs-und Hash Algorithmen bereit. Die Algorithmen "Schlüsselaustausch", "digitale Signatur" und "Verschlüsselung" basieren auf Kryptografie mit öffentlichem RSA-Schlüssel.

</dd> <dt>

<span id="_security_prov_rsa_sig_gly"></span><span id="_SECURITY_PROV_RSA_SIG_GLY"></span>**Prov \_ RSA \_ sig**
</dt> <dd>

Siehe *Prov \_ RSA \_ sig-Anbietertyp*.

</dd> <dt>

<span id="_security_prov_rsa_sig_provider_type_gly"></span><span id="_SECURITY_PROV_RSA_SIG_PROVIDER_TYPE_GLY"></span>**Prov \_ RSA \_ sig-Anbietertyp**
</dt> <dd>

Der von Microsoft und der RSA-Datensicherheit definierte vordefinierte Anbietertyp. Dieser Anbietertyp ist eine Teilmenge von Prov \_ RSA \_ Full, die nur digitale Signaturen und Hash Algorithmen bereitstellt. Der Algorithmus für die digitale Signatur ist ein RSA-Algorithmus für öffentliche Schlüssel.

</dd> <dt>

<span id="_security_prov_ssl_gly"></span><span id="_SECURITY_PROV_SSL_GLY"></span>**Prov- \_ SSL**
</dt> <dd>

Siehe *Prov- \_ SSL-Anbietertyp*.

</dd> <dt>

<span id="_security_prov_ssl_provider_type_gly"></span><span id="_SECURITY_PROV_SSL_PROVIDER_TYPE_GLY"></span>**Prov- \_ SSL-Anbietertyp**
</dt> <dd>

Der vordefinierte Anbietertyp, der das Secure Sockets Layer (SSL)-Protokoll unterstützt. Dieser Typ stellt Schlüssel Verschlüsselung, digitale Signatur, Verschlüsselung und Hash Algorithmen bereit. Eine Spezifikation, die SSL erläutert, ist in Netscape Communications Corp verfügbar.

</dd> <dt>

<span id="_security_provider_gly"></span><span id="_SECURITY_PROVIDER_GLY"></span>**ab**
</dt> <dd>

Siehe [*Kryptografiedienstanbieter*](c-gly.md).

</dd> <dt>

<span id="_security_provider_name_gly"></span><span id="_SECURITY_PROVIDER_NAME_GLY"></span>**Anbieter Name**
</dt> <dd>

Ein Name, der zum Identifizieren eines CSP verwendet wird. Beispielsweise die Microsoft-Basis-Kryptografieanbieter Version 1,0. Der Anbieter Name wird in der Regel verwendet, wenn die **CryptAcquireContext** -Funktion aufgerufen wird, um eine Verbindung mit einem CSP herzustellen.

</dd> <dt>

<span id="_security_provider_type_gly"></span><span id="_SECURITY_PROVIDER_TYPE_GLY"></span>**Anbietertyp**
</dt> <dd>

Ein Begriff, mit dem ein Kryptografiedienstanbieter (kryptografischen Service Provider, CSP) identifiziert wird. CSPs werden in unterschiedlichen Anbieter Typen gruppiert, die eine bestimmte Familie von Standarddaten Formaten und-Protokollen darstellen. Im Gegensatz zum eindeutigen Anbieter Namen eines CSP sind Anbieter Typen für einen bestimmten CSP nicht eindeutig. Der Anbietertyp wird normalerweise verwendet, wenn die **CryptAcquireContext** -Funktion aufgerufen wird, um eine Verbindung mit einem CSP herzustellen.

</dd> <dt>

<span id="_security_pseudo_random_function_gly"></span><span id="_SECURITY_PSEUDO_RANDOM_FUNCTION_GLY"></span>**Pseudo Zufallsfunktion**
</dt> <dd>

PRF Eine Funktion, die einen Schlüssel, eine Bezeichnung und einen Ausgangswert als Eingabe annimmt und dann eine Ausgabe beliebiger Länge erzeugt.

</dd> <dt>

<span id="_security_public_private_key_pair_gly"></span><span id="_SECURITY_PUBLIC_PRIVATE_KEY_PAIR_GLY"></span>**öffentliches/privates Schlüsselpaar**
</dt> <dd>

Ein Satz kryptografischer Schlüssel für eine Kryptografie mit öffentlichen Schlüsseln. Ein CSP verwaltet für jeden Benutzer in der Regel zwei öffentliche/private Schlüsselpaare: ein Exchange-Schlüsselpaar und ein Schlüsselpaar für digitale Signaturen. Beide Schlüsselpaare werden sitzungsübergreifend beibehalten.

Siehe [*Austausch Schlüssel*](e-gly.md) paar und [*Signatur Schlüsselpaar*](s-gly.md).

</dd> <dt>

<span id="_security_public_key_gly"></span><span id="_SECURITY_PUBLIC_KEY_GLY"></span>**öffentlicher Schlüssel**
</dt> <dd>

Ein kryptografischer Schlüssel, der normalerweise zum Entschlüsseln eines Sitzungsschlüssels oder einer digitalen Signatur verwendet wird. Der öffentliche Schlüssel kann auch zum Verschlüsseln einer Nachricht verwendet werden. Dadurch wird sichergestellt, dass nur die Person mit dem entsprechenden privaten Schlüssel die Nachricht entschlüsseln kann.

Siehe auch *privater Schlüssel*.

</dd> <dt>

<span id="_security_public_key_algorithm_gly"></span><span id="_SECURITY_PUBLIC_KEY_ALGORITHM_GLY"></span>**Algorithmus für öffentliche Schlüssel**
</dt> <dd>

Eine asymmetrische Verschlüsselung, bei der zwei Schlüssel verwendet werden: eine für die Verschlüsselung, der öffentliche Schlüssel und die andere für die Entschlüsselung, der private Schlüssel. Gemäß den Schlüsselnamen kann der öffentliche Schlüssel, der zum Codieren von Klartext verwendet wird, allen Benutzern zur Verfügung gestellt werden. Der private Schlüssel muss jedoch geheim bleiben. Der Chiffre Text kann nur mit dem privaten Schlüssel entschlüsselt werden. Der in diesem Prozess verwendete Algorithmus für öffentliche Schlüssel ist langsam (in der Reihenfolge der 1.000-mal langsamer als symmetrische Algorithmen) und wird in der Regel zum Verschlüsseln von Sitzungs Schlüsseln oder zum digitalen Signieren einer Nachricht verwendet.

Siehe auch *öffentlichen* und *privaten Schlüssel*.

</dd> <dt>

<span id="_security_public_key_blob_gly"></span><span id="_SECURITY_PUBLIC_KEY_BLOB_GLY"></span>**BLOB für öffentliche Schlüssel**
</dt> <dd>

Ein BLOB, das verwendet wird, um den Teil des öffentlichen Schlüssels eines öffentlichen/privaten Schlüssel Paars zu speichern. Blobschlüssel für öffentliche Schlüssel werden nicht verschlüsselt, weil der öffentliche Schlüssel, der in enthalten ist, nicht geheim ist. Ein öffentliches Schlüsselblob wird durch Aufrufen der **CryptExportKey** -Funktion erstellt.

</dd> <dt>

<span id="_security_public_key_cryptography_standards_gly"></span><span id="_SECURITY_PUBLIC_KEY_CRYPTOGRAPHY_STANDARDS_GLY"></span>**Kryptografiestandards für öffentliche Schlüssel**
</dt> <dd>

PKCS Eine Reihe von Syntax Standards für die Kryptografie mit öffentlichem Schlüssel, die Sicherheitsfunktionen abdeckt, einschließlich Methoden zum Signieren von Daten, Austauschen von Schlüsseln, Anfordern von Zertifikaten, Verschlüsselung und Entschlüsselung von öffentlichem Schlüsseln und andere Sicherheitsfunktionen.

</dd> <dt>

<span id="_security_public_key_encryption_gly"></span><span id="_SECURITY_PUBLIC_KEY_ENCRYPTION_GLY"></span>**Verschlüsselung mit öffentlichem Schlüssel**
</dt> <dd>

Eine Verschlüsselung mit Schlüsselpaaren: Mit einem Schlüssel werden die Daten verschlüsselt, mit dem anderen entschlüsselt. Bei symmetrischen Verschlüsselungsalgorithmen wird hingegen der gleiche Schlüssel sowohl zur Verschlüsselung als auch zur Entschlüsselung verwendet. In der Praxis wird die Kryptografie mit öffentlichem Schlüssel in der Regel verwendet, um den Sitzungsschlüssel zu schützen, der von einem symmetrischen Verschlüsselungsalgorithmus verwendet wird. In diesem Fall wird der Sitzungsschlüssel, mit dem Daten verschlüsselt wurden, mit dem öffentlichen Schlüssel verschlüsselt, und der private Schlüssel wird zum Entschlüsseln der Daten verwendet. Neben dem Schutz von Sitzungsschlüsseln kann die Verschlüsselung mit öffentlichem Schlüssel noch zum digitalen Signieren von Nachrichten (mit dem privaten Schlüssel) sowie zum Überprüfen der Signatur (mit dem öffentlichen Schlüssel) verwendet werden.

Siehe auch *Algorithmus für öffentliche Schlüssel*.

</dd> </dl>

 

 



