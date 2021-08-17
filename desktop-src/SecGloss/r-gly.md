---
description: Enthält Definitionen von Sicherheitsbegriffen, die mit dem Buchstaben R beginnen.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: ce589e18-02ac-42c2-b76b-776deb686bbd
title: R (Sicherheitsglossar)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a566a939746cd65c6336e8f31ff05a7ee3f0a3b7954e9d790d3f15a8163f138b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118895289"
---
# <a name="r-security-glossary"></a>R (Sicherheitsglossar)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q R [S](s-gly.md) T [U](t-gly.md) [](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_rc2_gly"></span><span id="_SECURITY_RC2_GLY"></span>**RC2**
</dt> <dd>

Der [*CryptoAPI-Algorithmusname*](c-gly.md) für den RC2-Algorithmus.

Siehe auch *RC2-Blockalgorithmus*.

</dd> <dt>

<span id="_security_rc2_block_algorithm_gly"></span><span id="_SECURITY_RC2_BLOCK_ALGORITHM_GLY"></span>**RC2-Blockalgorithmus**
</dt> <dd>

Ein [*Datenverschlüsselungsalgorithmus,*](e-gly.md) der auf der RC2-64-Bit-Symmetrischen Blockchiffre basiert. RC2 wird durch PROV \_ RSA \_ FULL-Anbietertypen angegeben. [*CryptoAPI*](c-gly.md) verweist auf diesen Algorithmus durch seinen Bezeichner (CALG \_ RC2), Name (RC2) und Klasse (ALG \_ CLASS DATA \_ \_ ENCRYPT).

</dd> <dt>

<span id="_security_rc4_gly"></span><span id="_SECURITY_RC4_GLY"></span>**RC4**
</dt> <dd>

Der [*CryptoAPI-Algorithmusname*](c-gly.md) für den RC4-Algorithmus.

Siehe auch *RC4-Streamalgorithmus.*

</dd> <dt>

<span id="_security_rc4_stream_algorithm_gly"></span><span id="_SECURITY_RC4_STREAM_ALGORITHM_GLY"></span>**RC4-Streamalgorithmus**
</dt> <dd>

Ein [*Datenverschlüsselungsalgorithmus,*](e-gly.md) der auf dem symmetrischen RC4-Datenstromchiffren basiert. RC4 wird durch PROV \_ RSA \_ FULL-Anbietertypen angegeben. [*CryptoAPI*](c-gly.md) verweist auf diesen Algorithmus durch seinen Bezeichner (CALG \_ RC4), Name (RC4) und Klasse (ALG \_ CLASS DATA \_ \_ ENCRYPT).

</dd> <dt>

<span id="_security_rdn_gly"></span><span id="_SECURITY_RDN_GLY"></span>**Rdn**
</dt> <dd>

Siehe *relativer Distinguished Name*.

</dd> <dt>

<span id="_security_reader_gly"></span><span id="_SECURITY_READER_GLY"></span>**Leser**
</dt> <dd>

Ein Standardgerät innerhalb des [*Smartcard-Subsystems.*](s-gly.md) Ein Schnittstellengerät (Interface Device, IFD), das bidirektionale Eingaben/Ausgaben für eine Smartcard unterstützt. Sie kann einem gesamten System, einer oder mehrere Lesergruppen oder einem bestimmten Terminal zugeordnet werden. Mit dem Smartcardsubsystem kann ein Reader dem Terminal zugeordnet werden, dem er zugewiesen ist. Derzeit ist jedoch nur ein Terminal auf einem Computer vorhanden.

</dd> <dt>

<span id="_security_reader_driver_gly"></span><span id="_SECURITY_READER_DRIVER_GLY"></span>**Readertreiber**
</dt> <dd>

Ein bestimmter Treiber, der Treiberdienste einem bestimmten Hardwarelesegerät zu ordnet. Sie muss dem Smartcard-Klassentreiber Karteneinfüge- und Entfernungsereignisse für die Weiterleitung an den Smartcard-Ressourcen-Manager übermitteln und der Karte Datenaustauschfunktionen durch ein beliebiges Unformatiert-, T=0-, T=1- oder PTS-Protokoll bereitstellen. [](s-gly.md)

</dd> <dt>

<span id="_security_reader_group_gly"></span><span id="_SECURITY_READER_GROUP_GLY"></span>**Readergruppe**
</dt> <dd>

Eine logische Gruppe von Readern. Lesergruppen können vom System definiert oder von Benutzern oder Administratoren erstellt werden. Lesergruppen werden von Smartcardfunktionen verwendet, die auf Gruppen von Lesern angewendet werden können. Um Namenskonflikte mit benutzerdefinierten Gruppen zu vermeiden, reserviert Microsoft die Verwendung eines beliebigen Namens, der das Dollarzeichen ($) enthält.

</dd> <dt>

<span id="_security_reader_helper_driver_gly"></span><span id="_SECURITY_READER_HELPER_DRIVER_GLY"></span>**Reader-Hilfstreiber**
</dt> <dd>

Bietet allgemeine Unterstützungsroutinen für Smartcardtreiber und zusätzliche T=0- und T=1-Protokollunterstützung für bestimmte Treiber bei Bedarf.

</dd> <dt>

<span id="_security_reference_count_gly"></span><span id="_SECURITY_REFERENCE_COUNT_GLY"></span>**Verweisanzahl**
</dt> <dd>

Ein ganzzahliger Wert, der zum Nachverfolgen eines COM-Objekts verwendet wird. Wenn ein Objekt erstellt wird, wird die Verweisanzahl auf 1 festgelegt. Jedes Mal, wenn eine Schnittstelle an das Objekt gebunden ist, wird die Verweisanzahl erhöht. Wenn die Schnittstellenverbindung zerstört wird, wird die Verweisanzahl dekrementiert. Das Objekt wird zerstört, wenn die Verweisanzahl 0 (null) erreicht. Alle Schnittstellen zu diesem Objekt sind dann ungültig.

</dd> <dt>

<span id="_security_relative_distinguished_name_gly"></span><span id="_SECURITY_RELATIVE_DISTINGUISHED_NAME_GLY"></span>**Relativer Distinguished Name**
</dt> <dd>

(RDN) Eine Entität, die als Betreff in einer Zertifikatanforderung enthalten ist. Die Elemente in einem RDN werden durch ihre Attribute definiert und müssen keinen Namen enthalten. In Bezug auf [*CryptoAPI*](c-gly.md)wird ein RDN durch eine CERT RDN-Struktur definiert, die wiederum auf ein Array von \_ CERT \_ RDN \_ ATTR-Attributstrukturen verweist. Jede Attributstruktur gibt ein einzelnes Attribut an.

</dd> <dt>

<span id="_security_relative_identifier_gly"></span><span id="_SECURITY_RELATIVE_IDENTIFIER_GLY"></span>**Relativer Bezeichner**
</dt> <dd>

(RID) Der Teil einer [*Sicherheits-ID*](s-gly.md) (SID), der einen Benutzer oder eine Gruppe in Bezug auf die Autorität identifiziert, die die SID ausgestellt hat.

</dd> <dt>

<span id="_security_relocated_store_gly"></span><span id="_SECURITY_RELOCATED_STORE_GLY"></span>**Verschobener Speicher**
</dt> <dd>

Ein [*Zertifikatspeicher,*](c-gly.md) der von seinem Standardregistrierungsspeicherort an einen anderen Speicherort in der Registrierung verschoben wurde.

</dd> <dt>

<span id="_security_remote_store_gly"></span><span id="_SECURITY_REMOTE_STORE_GLY"></span>**Remotespeicher**
</dt> <dd>

Ein [*Zertifikatspeicher auf*](c-gly.md) einem anderen Computer, z. B. einem Dateiserver oder einem anderen freigegebenen Remotecomputer.

</dd> <dt>

<span id="_security_reply_apdu_gly"></span><span id="_SECURITY_REPLY_APDU_GLY"></span>**Antwort-APDU**
</dt> <dd>

Eine [*Anwendungsprotokoll-Dateneinheit*](a-gly.md) (Application Protocol Data Unit, APDU), die als Antwort an ein empfangenes APDU gesendet wird.

</dd> <dt>

<span id="_security_repudiation_gly"></span><span id="_SECURITY_REPUDIATION_GLY"></span>**Ablehnung**
</dt> <dd>

Die Möglichkeit eines Benutzers, die Verantwortung für die Durchführung einer Aktion von sich zu weisen, ohne dass das Gegenteil bewiesen werden kann. Beispielsweise ein Benutzer, der eine Datei gelöscht hat und dies erfolgreich verweigern kann.

</dd> <dt>

<span id="_security_resource_manager_gly"></span><span id="_SECURITY_RESOURCE_MANAGER_GLY"></span>**Resource Manager**
</dt> <dd>

Das Modul des [*Smartcardsubsystems,*](s-gly.md) das den Zugriff auf mehrere Leser und Smartcards verwaltet. Der Ressourcen-Manager identifiziert und verfolgt Ressourcen, ordnet Leser und Ressourcen mehreren Anwendungen zu und unterstützt Transaktionsprimitiven für den Zugriff auf Dienste, die auf einer bestimmten Karte verfügbar sind.

</dd> <dt>

<span id="_security_resource_manager_api_gly"></span><span id="_SECURITY_RESOURCE_MANAGER_API_GLY"></span>**Resource Manager-API**
</dt> <dd>

Eine Reihe von Windows, die direkten Zugriff auf die Dienste des Ressourcen-Managers ermöglichen.

</dd> <dt>

<span id="_security_resource_manager_context_gly"></span><span id="_SECURITY_RESOURCE_MANAGER_CONTEXT_GLY"></span>**Resource Manager-Kontext**
</dt> <dd>

Der Kontext, der vom Ressourcen-Manager beim Zugriff auf die Smartcard-Datenbank verwendet wird. Der Ressourcen-Manager-Kontext wird hauptsächlich von den Abfrage- und Verwaltungsfunktionen beim Zugriff auf die Datenbank verwendet. Der Bereich des Resource Manager-Kontexts kann der aktuelle Benutzer oder das System sein.

</dd> <dt>

<span id="_security_revocation_list_gly"></span><span id="_SECURITY_REVOCATION_LIST_GLY"></span>**Sperrliste**
</dt> <dd>

Weitere Informationen [*finden Sie unter Zertifikatsperrliste.*](c-gly.md)

</dd> <dt>

<span id="_security_rid_gly"></span><span id="_SECURITY_RID_GLY"></span>**los**
</dt> <dd>

Siehe *relativer Bezeichner*.

</dd> <dt>

<span id="_security_root_authority_gly"></span><span id="_SECURITY_ROOT_AUTHORITY_GLY"></span>**Stammzertifizierungsstelle**
</dt> <dd>

Die [*Zertifizierungsstelle*](c-gly.md) am Anfang einer Zertifizierungsstellenhierarchie. Die Stammzertifizierungsstelle zertifiziert Zertifizierungsstellen in der nächsten Hierarchieebene.

</dd> <dt>

<span id="_security_root_certificate_gly"></span><span id="_SECURITY_ROOT_CERTIFICATE_GLY"></span>**Stammzertifikat**
</dt> <dd>

Ein selbstsigniertes [*Zertifizierungsstellenzertifikat,*](c-gly.md) das eine Zertifizierungsstelle identifiziert. Es wird als Stammzertifikat bezeichnet, da es sich um das Zertifikat für die Stammzertifizierungsstelle handelt. Die Stammzertifizierungsstelle muss ihr eigenes Zertifizierungsstellenzertifikat signieren, da es definitionsgemäß keine höhere Zertifizierungsstelle zum Signieren des Zertifizierungsstellenzertifikats gibt.

</dd> <dt>

<span id="_security_rsa_gly"></span><span id="_SECURITY_RSA_GLY"></span>**Rsa**
</dt> <dd>

RSA Data Security, Inc., ein wichtiger Entwickler und Herausgeber von Public [*Key Cryptography Standards*](p-gly.md) (PKCS). "RSA" im Namen steht für die Namen der drei Entwickler und Besitzer des Unternehmens: Rsaest, Shamir und Adleman.

</dd> <dt>

<span id="_security_rsa_keyx_gly"></span><span id="_SECURITY_RSA_KEYX_GLY"></span>**RSA \_ KEYX**
</dt> <dd>

Der [*CryptoAPI-Algorithmusname*](c-gly.md) für den RSA-Schlüsselaustauschalgorithmus. CryptoAPI verweist auch über den Algorithmusbezeichner (CALG RSA KEYX) und die Klasse \_ \_ (ALG CLASS KEY EXCHANGE) auf \_ diesen \_ \_ Algorithmus.

</dd> <dt>

<span id="_security_rsa_sign_gly"></span><span id="_SECURITY_RSA_SIGN_GLY"></span>**RSA \_ SIGN**
</dt> <dd>

Der CryptoAPI-Algorithmusname für den RSA-Signaturalgorithmus. CryptoAPI verweist auch über den Algorithmusbezeichner (CALG RSA SIGN) und die Klasse \_ \_ (ALG CLASS SIGNATURE) auf \_ diesen \_ Algorithmus.

</dd> <dt>

<span id="_security_rsa_public_key_algorithm_gly"></span><span id="_SECURITY_RSA_PUBLIC_KEY_ALGORITHM_GLY"></span>**RSA-Algorithmus für öffentliche Schlüssel**
</dt> <dd>

Ein Schlüsselaustausch- und Signaturalgorithmus, der auf der beliebten VERSCHLÜSSELUNG für öffentliche RSA-Schlüssel basiert. Dieser Algorithmus wird von den PROV \_ RSA \_ FULL-, PROV \_ RSA \_ SIG-, PROV \_ MS \_ EXCHANGE- und PROV \_ SSL-Anbietertypen verwendet. CryptoAPI verweist auf diesen Algorithmus durch seine Bezeichner (CALG RSA KEYX und \_ \_ CALG RSA SIGN), Namen (RSA KEYX und RSA SIGN) und Klasse \_ \_ \_ \_ (ALG \_ CLASS KEY \_ \_ EXCHANGE).

</dd> </dl>

 

 



