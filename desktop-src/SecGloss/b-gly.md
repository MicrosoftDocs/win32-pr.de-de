---
description: Enthält Definitionen von Sicherheits Begriffen, die mit dem Buchstaben B beginnen.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 2e570727-7da0-4e17-bf5d-6fe0e6aef65b
title: B (Sicherheits Glossar)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40aedaebddb86ddf9f32a9a3d86cf4cf4a613642
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355312"
---
# <a name="b-security-glossary"></a><span data-ttu-id="28984-103">B (Sicherheits Glossar)</span><span class="sxs-lookup"><span data-stu-id="28984-103">B (Security Glossary)</span></span>

<span data-ttu-id="28984-104">[a](a-gly.md) B [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span><span class="sxs-lookup"><span data-stu-id="28984-104">[A](a-gly.md) B [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span></span>

<dl> <dt>

<span data-ttu-id="28984-105"><span id="_security_backup_authority_gly"></span><span id="_SECURITY_BACKUP_AUTHORITY_GLY"></span>**Sicherungs Autorität**</span><span class="sxs-lookup"><span data-stu-id="28984-105"><span id="_security_backup_authority_gly"></span><span id="_SECURITY_BACKUP_AUTHORITY_GLY"></span>**backup authority**</span></span>
</dt> <dd>

<span data-ttu-id="28984-106">Eine vertrauenswürdige Anwendung, die auf einem sicheren Computer ausgeführt wird, der sekundären Speicher für die Sitzungsschlüssel der Clients bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="28984-106">A trusted application running on a secure computer that provides secondary storage for the session keys of its clients.</span></span> <span data-ttu-id="28984-107">Die Sicherungs Stelle speichert Sitzungsschlüssel als schlüsselblobspeicher, die mit dem öffentlichen Schlüssel der Sicherungs Autorität verschlüsselt werden.</span><span class="sxs-lookup"><span data-stu-id="28984-107">The backup authority stores session keys as key BLOBs that are encrypted with the backup authority's public key.</span></span>

</dd> <dt>

<span data-ttu-id="28984-108"><span id="_security_base_content_type_gly"></span><span id="_SECURITY_BASE_CONTENT_TYPE_GLY"></span>**Basis Inhaltstyp**</span><span class="sxs-lookup"><span data-stu-id="28984-108"><span id="_security_base_content_type_gly"></span><span id="_SECURITY_BASE_CONTENT_TYPE_GLY"></span>**base content type**</span></span>
</dt> <dd>

<span data-ttu-id="28984-109">Ein Typ von Daten, die in einer PKCS 7-Meldung enthalten sind \# .</span><span class="sxs-lookup"><span data-stu-id="28984-109">A type of data contained in a PKCS \#7 message.</span></span> <span data-ttu-id="28984-110">Basis Inhaltstypen enthalten nur Daten, keine kryptografischen Erweiterungen wie Hashes oder Signaturen.</span><span class="sxs-lookup"><span data-stu-id="28984-110">Base content types only contain data, no cryptographic enhancements such as hashes or signatures.</span></span> <span data-ttu-id="28984-111">Derzeit ist der einzige Basis Inhaltstyp der Daten Inhaltstyp.</span><span class="sxs-lookup"><span data-stu-id="28984-111">Currently, the only base content type is the Data content type.</span></span>

</dd> <dt>

<span data-ttu-id="28984-112"><span id="_security_base_cryptographic_functions_gly"></span><span id="_SECURITY_BASE_CRYPTOGRAPHIC_FUNCTIONS_GLY"></span>**grundlegende Kryptografiefunktionen**</span><span class="sxs-lookup"><span data-stu-id="28984-112"><span id="_security_base_cryptographic_functions_gly"></span><span id="_SECURITY_BASE_CRYPTOGRAPHIC_FUNCTIONS_GLY"></span>**base cryptographic functions**</span></span>
</dt> <dd>

<span data-ttu-id="28984-113">Die niedrigste Funktionsebene in der CryptoAPI-Architektur.</span><span class="sxs-lookup"><span data-stu-id="28984-113">The lowest level of functions in the CryptoAPI architecture.</span></span> <span data-ttu-id="28984-114">Sie werden von Anwendungen und anderen kryptoapi-Funktionen auf hoher Ebene verwendet, um den Zugriff auf vom CSP bereitgestellte Kryptografiealgorithmen, eine sichere Schlüsselgenerierung und eine sichere Speicherung von geheimen Schlüsseln bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="28984-114">They are used by applications and other high-level CryptoAPI functions to provide access to CSP-provided cryptographic algorithms, secure key generation, and secure storage of secrets.</span></span>

<span data-ttu-id="28984-115">Siehe auch [*Kryptografiedienstanbieter*](c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="28984-115">See also [*cryptographic service providers*](c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="28984-116"><span id="_security_basic_encoding_rules_gly"></span><span id="_SECURITY_BASIC_ENCODING_RULES_GLY"></span>**Grundlegende Codierungsregeln**</span><span class="sxs-lookup"><span data-stu-id="28984-116"><span id="_security_basic_encoding_rules_gly"></span><span id="_SECURITY_BASIC_ENCODING_RULES_GLY"></span>**Basic Encoding Rules**</span></span>
</dt> <dd>

<span data-ttu-id="28984-117">Mini Der Regelsatz, der zum Codieren von ASN. 1-Daten in einen Stream von Bits (Nullen oder solche) für die externe Speicherung oder Übertragung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="28984-117">(BER) The set of rules used to encode ASN.1 defined data into a stream of bits (zeros or ones) for external storage or transmission.</span></span> <span data-ttu-id="28984-118">Ein einzelnes ASN. 1-Objekt kann über mehrere äquivalente ber-Codierungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="28984-118">A single ASN.1 object may have several equivalent BER encodes.</span></span> <span data-ttu-id="28984-119">BER wird in der CCITT-Empfehlung X. 209 definiert.</span><span class="sxs-lookup"><span data-stu-id="28984-119">BER is defined in CCITT Recommendation X.209.</span></span> <span data-ttu-id="28984-120">Dies ist eine der beiden Codierungs Methoden, die derzeit von CryptoAPI verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="28984-120">This is one of the two encoding methods currently used by CryptoAPI.</span></span>

</dd> <dt>

<span data-ttu-id="28984-121"><span id="_security_ber_gly"></span><span id="_SECURITY_BER_GLY"></span>**Mini**</span><span class="sxs-lookup"><span data-stu-id="28984-121"><span id="_security_ber_gly"></span><span id="_SECURITY_BER_GLY"></span>**BER**</span></span>
</dt> <dd>

<span data-ttu-id="28984-122">Siehe *grundlegende Codierungsregeln*.</span><span class="sxs-lookup"><span data-stu-id="28984-122">See *Basic Encoding Rules*.</span></span>

</dd> <dt>

<span data-ttu-id="28984-123"><span id="_security_big_endian_gly"></span><span id="_SECURITY_BIG_ENDIAN_GLY"></span>**Big-tedian**</span><span class="sxs-lookup"><span data-stu-id="28984-123"><span id="_security_big_endian_gly"></span><span id="_SECURITY_BIG_ENDIAN_GLY"></span>**big-endian**</span></span>
</dt> <dd>

<span data-ttu-id="28984-124">Ein Arbeitsspeicher-oder Datenformat, in dem das signifikanteste Byte an der unteren Adresse gespeichert wird oder zuerst eingeht.</span><span class="sxs-lookup"><span data-stu-id="28984-124">A memory or data format in which the most significant byte is stored at the lower address or arrives first.</span></span>

<span data-ttu-id="28984-125">Siehe auch [*Little-*](l-gly.md)Deutsch.</span><span class="sxs-lookup"><span data-stu-id="28984-125">See also [*little-endian*](l-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="28984-126"><span id="_security_blob_gly"></span><span id="_SECURITY_BLOB_GLY"></span>**BLOB**</span><span class="sxs-lookup"><span data-stu-id="28984-126"><span id="_security_blob_gly"></span><span id="_SECURITY_BLOB_GLY"></span>**BLOB**</span></span>
</dt> <dd>

<span data-ttu-id="28984-127">Eine generische Sequenz von Bits, die eine oder mehrere Header Strukturen fester Länge sowie kontextspezifische Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="28984-127">A generic sequence of bits that contain one or more fixed-length header structures plus context specific data.</span></span>

<span data-ttu-id="28984-128">Siehe auch [*schlüsselblobnamen*](k-gly.md), [*zertifikatblobnamen*](c-gly.md), [*zertifikatblobblobnamen*](c-gly.md)und [*attributblob.*](a-gly.md)</span><span class="sxs-lookup"><span data-stu-id="28984-128">See also [*key BLOBs*](k-gly.md), [*certificate BLOBs*](c-gly.md), [*certificate name BLOBs*](c-gly.md), and [*attribute BLOBs*](a-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="28984-129"><span id="_security_block_cipher_gly"></span><span id="_SECURITY_BLOCK_CIPHER_GLY"></span>**Chiffre Block**</span><span class="sxs-lookup"><span data-stu-id="28984-129"><span id="_security_block_cipher_gly"></span><span id="_SECURITY_BLOCK_CIPHER_GLY"></span>**block cipher**</span></span>
</dt> <dd>

<span data-ttu-id="28984-130">Ein Verschlüsselungsalgorithmus, der Daten in diskreten Einheiten (als Blöcke bezeichnet) und nicht als kontinuierlichen Stream von Bits verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="28984-130">A cipher algorithm that encrypts data in discrete units (called blocks), rather than as a continuous stream of bits.</span></span> <span data-ttu-id="28984-131">Die häufigste Blockgröße ist 64 Bits.</span><span class="sxs-lookup"><span data-stu-id="28984-131">The most common block size is 64 bits.</span></span> <span data-ttu-id="28984-132">Beispielsweise ist des ein Blockchiffre.</span><span class="sxs-lookup"><span data-stu-id="28984-132">For example, DES is a block cipher.</span></span>

<span data-ttu-id="28984-133">Siehe auch [*streamchiffre*](s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="28984-133">See also [*stream cipher*](s-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="28984-134"><span id="_security_bulk_encryption_key_gly"></span><span id="_SECURITY_BULK_ENCRYPTION_KEY_GLY"></span>**Massen Verschlüsselungsschlüssel**</span><span class="sxs-lookup"><span data-stu-id="28984-134"><span id="_security_bulk_encryption_key_gly"></span><span id="_SECURITY_BULK_ENCRYPTION_KEY_GLY"></span>**bulk encryption key**</span></span>
</dt> <dd>

<span data-ttu-id="28984-135">Ein Sitzungsschlüssel, der von einem Hauptschlüssel abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="28984-135">A session key derived from a master key.</span></span> <span data-ttu-id="28984-136">Massen Verschlüsselungsschlüssel werden bei der [*SChannel*](s-gly.md) -Verschlüsselung verwendet.</span><span class="sxs-lookup"><span data-stu-id="28984-136">Bulk encryption keys are used in [*Schannel*](s-gly.md) encryption.</span></span>

</dd> </dl>

 

 



