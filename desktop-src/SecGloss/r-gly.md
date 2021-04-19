---
description: Enthält Definitionen von Sicherheits Begriffen, die mit dem Buchstaben R beginnen.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: ce589e18-02ac-42c2-b76b-776deb686bbd
title: R (Sicherheits Glossar)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc85a0da8aa4a0b985b8be040ef95e37068e8a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357890"
---
# <a name="r-security-glossary"></a>R (Sicherheits Glossar)

[a](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q R [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_rc2_gly"></span><span id="_SECURITY_RC2_GLY"></span>**RC2**
</dt> <dd>

Der Name des [*CryptoAPI*](c-gly.md) -Algorithmus für den RC2-Algorithmus.

Siehe auch *RC2-Block Algorithmus*.

</dd> <dt>

<span id="_security_rc2_block_algorithm_gly"></span><span id="_SECURITY_RC2_BLOCK_ALGORITHM_GLY"></span>**RC2-Block Algorithmus**
</dt> <dd>

Ein Daten [*Verschlüsselungs*](e-gly.md) Algorithmus, der auf der 64-Bit-Chiffre des symmetrischen Blocks RC2 basiert. RC2 wird von Prov \_ RSA \_ Full Provider Types angegeben. [*CryptoAPI*](c-gly.md) verweist auf diesen Algorithmus anhand seines Bezeichners (calg \_ RC2), des Namens (RC2) und der-Klasse (ALG \_ Class \_ Data \_ Verschlüsselungen).

</dd> <dt>

<span id="_security_rc4_gly"></span><span id="_SECURITY_RC4_GLY"></span>**RC4**
</dt> <dd>

Der Name des [*CryptoAPI*](c-gly.md) -Algorithmus für den RC4-Algorithmus.

Siehe auch *RC4-streamalgorithmus*.

</dd> <dt>

<span id="_security_rc4_stream_algorithm_gly"></span><span id="_SECURITY_RC4_STREAM_ALGORITHM_GLY"></span>**RC4-streamalgorithmus**
</dt> <dd>

Ein Daten [*Verschlüsselungs*](e-gly.md) Algorithmus, der auf der Verschlüsselung des symmetrischen RC4-Streams basiert. RC4 wird durch Prov \_ RSA \_ Full-Anbieter Typen angegeben. [*CryptoAPI*](c-gly.md) verweist auf diesen Algorithmus durch seinen Bezeichner (calg \_ RC4), den Namen (RC4) und die Klasse (Datenverschlüsselung der ALG- \_ Klasse \_ \_ ).

</dd> <dt>

<span id="_security_rdn_gly"></span><span id="_SECURITY_RDN_GLY"></span>**RDN**
</dt> <dd>

Siehe *relativer Distinguished Name*.

</dd> <dt>

<span id="_security_reader_gly"></span><span id="_SECURITY_READER_GLY"></span>**Reader**
</dt> <dd>

Ein Standardgerät innerhalb des [*Smartcard*](s-gly.md) -Subsystems. Ein Schnittstellen Gerät (IFD), das bidirektionale Eingabe/Ausgabe für eine Smartcard unterstützt. Sie kann einem ganzen System, einer oder mehreren Lesergruppen oder einem bestimmten Terminal zugeordnet werden. Mit dem Smartcard-Subsystem kann ein Reader dem Terminal zugewiesen werden, dem er zugewiesen ist. Zurzeit ist jedoch nur ein Terminal auf einem Computer vorhanden.

</dd> <dt>

<span id="_security_reader_driver_gly"></span><span id="_SECURITY_READER_DRIVER_GLY"></span>**Reader-Treiber**
</dt> <dd>

Ein bestimmter Treiber, der Treiber Dienste einem bestimmten Hardware Lese Gerät zuordnet. Er muss Karten Einfügungs-und Entfernungs Ereignisse an den [*Smartcard*](s-gly.md) -Klassen Treiber für die Weiterleitung an den Smartcard-Ressourcen-Manager übermitteln und Datenaustauschfunktionen für die Karte durch jedes RAW-, t = 0-, t = 1-oder PTS-Protokoll bereitstellen.

</dd> <dt>

<span id="_security_reader_group_gly"></span><span id="_SECURITY_READER_GROUP_GLY"></span>**Lesergruppe**
</dt> <dd>

Eine logische Gruppe von Lesern. Lesergruppen können vom System definiert oder von Benutzern oder Administratoren erstellt werden. Lesergruppen werden von Smartcardfunktionen verwendet, die auf Gruppen von Lesern reagieren können. Um Namenskonflikte mit benutzerdefinierten Gruppen zu vermeiden, reserviert Microsoft die Verwendung eines beliebigen Namens, der das Dollarzeichen ($) enthält.

</dd> <dt>

<span id="_security_reader_helper_driver_gly"></span><span id="_SECURITY_READER_HELPER_DRIVER_GLY"></span>**Reader-Hilfstreiber**
</dt> <dd>

Bietet allgemeine Support Routinen für Smartcard-Treiber und zusätzliche t = 0-und t = 1-Protokoll Unterstützung für bestimmte Treiber nach Bedarf.

</dd> <dt>

<span id="_security_reference_count_gly"></span><span id="_SECURITY_REFERENCE_COUNT_GLY"></span>**Verweis Anzahl**
</dt> <dd>

Ein ganzzahliger Wert, der zum Nachverfolgen eines COM-Objekts verwendet wird. Wenn ein Objekt erstellt wird, wird der Verweis Zähler auf 1 festgelegt. Jedes Mal, wenn eine Schnittstelle an das Objekt gebunden ist, wird der Verweis Zähler inkrementiert. Wenn die Schnittstellen Verbindung zerstört wird, wird der Verweis Zähler verringert. Das Objekt wird zerstört, wenn der Verweis Zähler Null erreicht. Alle Schnittstellen für dieses Objekt sind dann ungültig.

</dd> <dt>

<span id="_security_relative_distinguished_name_gly"></span><span id="_SECURITY_RELATIVE_DISTINGUISHED_NAME_GLY"></span>**relativer definierter Name**
</dt> <dd>

RDN Eine Entität, die in einer Anforderung für ein Zertifikat als Betreff eingeschlossen ist. Die Elemente in einem RDN werden durch ihre Attribute definiert und müssen keinen Namen enthalten. Im Hinblick auf die [*kryptoapi*](c-gly.md)wird ein RDN durch eine Zertifikat- \_ RDN-Struktur definiert, die wiederum auf ein Array von Zertifikat- \_ RDN- \_ Attribut Strukturen verweist. Jede Attribut Struktur gibt ein einzelnes Attribut an.

</dd> <dt>

<span id="_security_relative_identifier_gly"></span><span id="_SECURITY_RELATIVE_IDENTIFIER_GLY"></span>**relativer Bezeichner**
</dt> <dd>

Gesagt Der Teil einer [*Sicherheits*](s-gly.md) -ID (SID), die einen Benutzer oder eine Gruppe in Bezug auf die Zertifizierungsstelle identifiziert, die die SID ausgegeben hat.

</dd> <dt>

<span id="_security_relocated_store_gly"></span><span id="_SECURITY_RELOCATED_STORE_GLY"></span>**Speicher verschoben**
</dt> <dd>

Ein [*Zertifikat Speicher*](c-gly.md) , der vom Standard Registrierungs Speicherort an einen anderen Speicherort in der Registrierung verschoben wurde.

</dd> <dt>

<span id="_security_remote_store_gly"></span><span id="_SECURITY_REMOTE_STORE_GLY"></span>**Remote Speicher**
</dt> <dd>

Ein [*Zertifikat Speicher*](c-gly.md) , der sich auf einem anderen Computer befindet, z. b. ein Dateiserver oder ein anderer frei gegebener Remote Computer.

</dd> <dt>

<span id="_security_reply_apdu_gly"></span><span id="_SECURITY_REPLY_APDU_GLY"></span>**Antwort-APDU**
</dt> <dd>

Eine [*Anwendungsprotokoll-Dateneinheit*](a-gly.md) (APDU), die als Antwort auf eine empfangene APDU gesendet wird.

</dd> <dt>

<span id="_security_repudiation_gly"></span><span id="_SECURITY_REPUDIATION_GLY"></span>**Nichtabstreitbarkeits**
</dt> <dd>

Die Möglichkeit eines Benutzers, die Verantwortung für die Durchführung einer Aktion von sich zu weisen, ohne dass das Gegenteil bewiesen werden kann. Beispielsweise ein Benutzer, der eine Datei gelöscht hat und den Vorgang erfolgreich ablehnen kann.

</dd> <dt>

<span id="_security_resource_manager_gly"></span><span id="_SECURITY_RESOURCE_MANAGER_GLY"></span>**Ressourcen-Manager**
</dt> <dd>

Das Modul des [*Smartcard*](s-gly.md) -Subsystems, das den Zugriff auf mehrere Reader und Smartcards verwaltet. Der Ressourcen-Manager ermittelt und überwacht Ressourcen, ordnet Leser und Ressourcen über mehrere Anwendungen zu und unterstützt Transaktions primitive für den Zugriff auf Dienste, die auf einer bestimmten Karte verfügbar sind.

</dd> <dt>

<span id="_security_resource_manager_api_gly"></span><span id="_SECURITY_RESOURCE_MANAGER_API_GLY"></span>**Resource Manager-API**
</dt> <dd>

Eine Reihe von Windows-Funktionen, die direkten Zugriff auf die Dienste des Ressourcen-Managers bereitstellen.

</dd> <dt>

<span id="_security_resource_manager_context_gly"></span><span id="_SECURITY_RESOURCE_MANAGER_CONTEXT_GLY"></span>**Resource Manager-Kontext**
</dt> <dd>

Der Kontext, der vom Ressourcen-Manager beim Zugriff auf die smartcarddatenbank verwendet wird. Der Resource Manager-Kontext wird hauptsächlich von den Abfrage-und Verwaltungsfunktionen verwendet, wenn auf die Datenbank zugegriffen wird. Der Bereich des Resource Manager-Kontexts kann der aktuelle Benutzer oder das System sein.

</dd> <dt>

<span id="_security_revocation_list_gly"></span><span id="_SECURITY_REVOCATION_LIST_GLY"></span>**Sperr Liste**
</dt> <dd>

Siehe [*Zertifikat Sperr Liste*](c-gly.md).

</dd> <dt>

<span id="_security_rid_gly"></span><span id="_SECURITY_RID_GLY"></span>**Gesagt**
</dt> <dd>

Siehe *relativer Bezeichner*.

</dd> <dt>

<span id="_security_root_authority_gly"></span><span id="_SECURITY_ROOT_AUTHORITY_GLY"></span>**Stamm Zertifizierungsstelle**
</dt> <dd>

Die [*Zertifizierungsstelle (Certification Authority*](c-gly.md) , ca) am Anfang einer Zertifizierungsstellen Hierarchie. Die Stammzertifizierungsstelle zertifiziert Zertifizierungsstellen in der nächsten Hierarchieebene.

</dd> <dt>

<span id="_security_root_certificate_gly"></span><span id="_SECURITY_ROOT_CERTIFICATE_GLY"></span>**Stamm Zertifikat**
</dt> <dd>

Ein selbst signiertes [*Zertifizierungs*](c-gly.md) stellen Zertifikat, das eine Zertifizierungsstelle identifiziert. Es wird als Stamm Zertifikat bezeichnet, da es das Zertifikat für die Stamm Zertifizierungsstelle ist. Die Stamm Zertifizierungsstelle muss Ihr eigenes Zertifizierungsstellen Zertifikat signieren, da sie definitionsgemäß keine höhere Zertifizierungsstelle zum Signieren des Zertifizierungsstellen Zertifikats hat.

</dd> <dt>

<span id="_security_rsa_gly"></span><span id="_SECURITY_RSA_GLY"></span>**RSA**
</dt> <dd>

RSA Data Security, Inc., ein bedeutender Entwickler und Herausgeber von [*Public Key Kryptografie Standards*](p-gly.md) (PKCS). Die "RSA" im Namen steht für die Namen der drei Entwickler und der Besitzer des Unternehmens: Rivest, Shamir und Adleman.

</dd> <dt>

<span id="_security_rsa_keyx_gly"></span><span id="_SECURITY_RSA_KEYX_GLY"></span>**RSA- \_ Keyx**
</dt> <dd>

Der Name des [*CryptoAPI*](c-gly.md) -Algorithmus für den RSA-Schlüsselaustausch Algorithmus. CryptoAPI verweist auf diesen Algorithmus auch durch den Algorithmusbezeichner (calg \_ RSA \_ Keyx) und die Klasse (ALG \_ Class \_ Key \_ Exchange).

</dd> <dt>

<span id="_security_rsa_sign_gly"></span><span id="_SECURITY_RSA_SIGN_GLY"></span>**RSA- \_ Zeichen**
</dt> <dd>

Der Name des CryptoAPI-Algorithmus für den RSA-Signatur Algorithmus. CryptoAPI verweist auf diesen Algorithmus auch über den Algorithmusbezeichner (calg \_ RSA \_ Sign) und die Klasse (ALG- \_ Klassen \_ Signatur).

</dd> <dt>

<span id="_security_rsa_public_key_algorithm_gly"></span><span id="_SECURITY_RSA_PUBLIC_KEY_ALGORITHM_GLY"></span>**RSA-Algorithmus für öffentliche Schlüssel**
</dt> <dd>

Ein Schlüsselaustausch-und Signatur Algorithmus, der auf der gängigen RSA-Verschlüsselung mit öffentlichem Schlüssel basiert. Dieser Algorithmus wird von Prov \_ RSA \_ Full, Prov \_ RSA \_ SIG, Prov \_ MS \_ Exchange und Prov \_ SSL Provider Types verwendet. CryptoAPI verweist auf diesen Algorithmus von seinen bezeichnerschlüsseln (calg \_ RSA \_ Keyx und calg \_ RSA \_ Sign), Names (RSA \_ Keyx und RSA \_ Sign) und Class (ALG \_ Class \_ Key \_ Exchange).

</dd> </dl>

 

 



