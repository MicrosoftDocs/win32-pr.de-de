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
# <a name="p-security-glossary"></a><span data-ttu-id="a13ff-103">P (Sicherheits Glossar)</span><span class="sxs-lookup"><span data-stu-id="a13ff-103">P (Security Glossary)</span></span>

<span data-ttu-id="a13ff-104">[a](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) P Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span><span class="sxs-lookup"><span data-stu-id="a13ff-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) P Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span></span>

<dl> <dt>

<span data-ttu-id="a13ff-105"><span id="_security_padding_gly"></span><span id="_SECURITY_PADDING_GLY"></span>**Auffüllung**</span><span class="sxs-lookup"><span data-stu-id="a13ff-105"><span id="_security_padding_gly"></span><span id="_SECURITY_PADDING_GLY"></span>**padding**</span></span>
</dt> <dd>

<span data-ttu-id="a13ff-106">Eine Zeichenfolge, die im Allgemeinen hinzugefügt wird, wenn der letzte Klartextblock kurz ist.</span><span class="sxs-lookup"><span data-stu-id="a13ff-106">A string, typically added when the last plaintext block is short.</span></span> <span data-ttu-id="a13ff-107">Wenn die Blocklänge beispielsweise 64 Bits beträgt und der letzte Block nur 40 Bits enthält, müssen dem letzten Block 24 Bits von Auffüll Zeichen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="a13ff-107">For example, if the block length is 64 bits and the last block contains only 40 bits, then 24 bits of padding must be added to the last block.</span></span> <span data-ttu-id="a13ff-108">Die Auffüll Zeichenfolge enthält möglicherweise Nullen, abwechselnde Nullen und solche oder ein anderes Muster.</span><span class="sxs-lookup"><span data-stu-id="a13ff-108">The padding string may contain zeros, alternating zeros and ones, or some other pattern.</span></span> <span data-ttu-id="a13ff-109">Anwendungen, die [*CryptoAPI*](c-gly.md) verwenden, müssen Ihren Klartext keine Auffüll Zeichen hinzufügen, bevor Sie verschlüsselt werden, und Sie müssen Sie nach der Entschlüsselung nicht entfernen.</span><span class="sxs-lookup"><span data-stu-id="a13ff-109">Applications that use [*CryptoAPI*](c-gly.md) need not add padding to their plaintext before it is encrypted, nor do they have to remove it after decrypting.</span></span> <span data-ttu-id="a13ff-110">Dies erfolgt automatisch.</span><span class="sxs-lookup"><span data-stu-id="a13ff-110">This is all handled automatically.</span></span>

</dd> <dt>

<span data-ttu-id="a13ff-111"><span id="_security_password_filter_gly"></span><span id="_SECURITY_PASSWORD_FILTER_GLY"></span>**Kenn Wortfilter**</span><span class="sxs-lookup"><span data-stu-id="a13ff-111"><span id="_security_password_filter_gly"></span><span id="_SECURITY_PASSWORD_FILTER_GLY"></span>**password filter**</span></span>
</dt> <dd>

<span data-ttu-id="a13ff-112">Eine DLL, die die Durchsetzung von Kenn Wort Richtlinien und Änderungs Benachrichtigungen bereitstellt</span><span class="sxs-lookup"><span data-stu-id="a13ff-112">A DLL that provides password policy enforcement and change notification.</span></span> <span data-ttu-id="a13ff-113">Die von Kenn Wort Filtern implementierten Funktionen werden von der [*lokalen Sicherheits Autorität*](l-gly.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="a13ff-113">The functions implemented by password filters are called by the [*Local Security Authority*](l-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="a13ff-114"><span id="_security_persistent_storage_gly"></span><span id="_SECURITY_PERSISTENT_STORAGE_GLY"></span>**persistenter Speicher**</span><span class="sxs-lookup"><span data-stu-id="a13ff-114"><span id="_security_persistent_storage_gly"></span><span id="_SECURITY_PERSISTENT_STORAGE_GLY"></span>**persistent storage**</span></span>
</dt> <dd>

<span data-ttu-id="a13ff-115">Jedes Speichermedium, das intakt bleibt, wenn die Stromversorgung getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="a13ff-115">Any storage medium that remains intact when the power to it is disconnected.</span></span> <span data-ttu-id="a13ff-116">Viele [*Zertifikat*](c-gly.md) Speicher Datenbanken sind Formen des permanenten Speichers.</span><span class="sxs-lookup"><span data-stu-id="a13ff-116">Many [*certificate store*](c-gly.md) databases are forms of persistent storage.</span></span>

</dd> <dt>

<span data-ttu-id="a13ff-117"><span id="_security_pkcs_gly"></span><span id="_SECURITY_PKCS_GLY"></span>**PKCS**</span><span class="sxs-lookup"><span data-stu-id="a13ff-117"><span id="_security_pkcs_gly"></span><span id="_SECURITY_PKCS_GLY"></span>**PKCS**</span></span>
</dt> <dd>

<span data-ttu-id="a13ff-118">Siehe *Kryptografiestandards für öffentliche Schlüssel*.</span><span class="sxs-lookup"><span data-stu-id="a13ff-118">See *Public Key Cryptography Standards*.</span></span>

</dd> <dt>

<span data-ttu-id="a13ff-119"><span id="_security_pkcs_1_standard_gly"></span><span id="_SECURITY_PKCS_1_STANDARD_GLY"></span>**PKCS \# 1**</span><span class="sxs-lookup"><span data-stu-id="a13ff-119"><span id="_security_pkcs_1_standard_gly"></span><span id="_SECURITY_PKCS_1_STANDARD_GLY"></span>**PKCS \#1**</span></span>
</dt> <dd>

<span data-ttu-id="a13ff-120">Die empfohlenen Standards für die Implementierung der Kryptografie mit öffentlichem Schlüssel, die auf dem RSA-Algorithmus basiert, wie in [RFC 3447](https://tools.ietf.org/html/rfc3447)definiert.</span><span class="sxs-lookup"><span data-stu-id="a13ff-120">The recommended standards for the implementation of public-key cryptography based on the RSA algorithm as defined in [RFC 3447](https://tools.ietf.org/html/rfc3447).</span></span>

</dd> <dt>

<span data-ttu-id="a13ff-121"><span id="_security_pkcs_12_standard_gly"></span><span id="_SECURITY_PKCS_12_STANDARD_GLY"></span>**PKCS \# 12**</span><span class="sxs-lookup"><span data-stu-id="a13ff-121"><span id="_security_pkcs_12_standard_gly"></span><span id="_SECURITY_PKCS_12_STANDARD_GLY"></span>**PKCS \#12**</span></span>
</dt> <dd>

<span data-ttu-id="a13ff-122">Der Standard mäßig von RSA Data Security, Inc. entwickelte und beibegefasste Syntax Standard für den persönlichen Informationsaustausch Dieser Syntax Standard gibt ein portables Format zum Speichern oder transportieren der privaten Schlüssel, Zertifikate und sonstigen geheimen Schlüssel eines Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="a13ff-122">The Personal Information Exchange Syntax Standard, developed and maintained by RSA Data Security, Inc. This syntax standard specifies a portable format for storing or transporting a user's private keys, certificates, and miscellaneous secrets.</span></span>

<span data-ttu-id="a13ff-123">Siehe auch *Kryptografiestandards* für [*Zertifikate*](c-gly.md) und öffentliche Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="a13ff-123">See also [*certificate*](c-gly.md) and *Public Key Cryptography Standards*.</span></span>

</dd> <dt>

<span data-ttu-id="a13ff-124"><span id="_security_pkcs_7_signed_data_gly"></span><span id="_SECURITY_PKCS_7_SIGNED_DATA_GLY"></span>**Mit PKCS \# 7 signierte Daten**</span><span class="sxs-lookup"><span data-stu-id="a13ff-124"><span id="_security_pkcs_7_signed_data_gly"></span><span id="_SECURITY_PKCS_7_SIGNED_DATA_GLY"></span>**PKCS \#7 Signed Data**</span></span>
</dt> <dd>

<span data-ttu-id="a13ff-125">Ein Datenobjekt, das mit dem öffentlichen Schlüssel Kryptografiestandard \# 7 (PKCS \# 7) signiert ist und die Informationen kapselt, die zum Signieren einer Datei verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a13ff-125">A data object that is signed with the Public Key Cryptography Standard \#7 (PKCS \#7) and that encapsulates the information used to sign a file.</span></span> <span data-ttu-id="a13ff-126">In der Regel enthält Sie das Zertifikat des Signatur Gebers und das Stamm [*Zertifikat*](r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="a13ff-126">Typically, it includes the signer's certificate and the [*root certificate*](r-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="a13ff-127"><span id="_security_pkcs_7_standard_gly"></span><span id="_SECURITY_PKCS_7_STANDARD_GLY"></span>**PKCS \# 7**</span><span class="sxs-lookup"><span data-stu-id="a13ff-127"><span id="_security_pkcs_7_standard_gly"></span><span id="_SECURITY_PKCS_7_STANDARD_GLY"></span>**PKCS \#7**</span></span>
</dt> <dd>

<span data-ttu-id="a13ff-128">Der Cryptographic Message Syntax (CMS)-Standard.</span><span class="sxs-lookup"><span data-stu-id="a13ff-128">The Cryptographic Message Syntax Standard.</span></span> <span data-ttu-id="a13ff-129">Eine allgemeine Syntax für Daten, bei denen Kryptografie eingesetzt werden könnte, beispielsweise digitale Signaturen und Verschlüsselungen.</span><span class="sxs-lookup"><span data-stu-id="a13ff-129">A general syntax for data to which cryptography may be applied, such as digital signatures and encryption.</span></span> <span data-ttu-id="a13ff-130">Außerdem wird eine Syntax für die Verteilung von Zertifikaten oder Zertifikat Sperr Listen sowie anderer Nachrichten Attribute (z. b. Zeitstempel) für die Nachricht bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="a13ff-130">It also provides a syntax for disseminating certificates or certificate revocation lists and other message attributes, such as time stamps, to the message.</span></span>

</dd> <dt>

<span data-ttu-id="a13ff-131"><span id="_security_pkcs_7_asn_encoding_gly"></span><span id="_SECURITY_PKCS_7_ASN_ENCODING_GLY"></span>**PKCS \_ 7- \_ ASN- \_ Codierung**</span><span class="sxs-lookup"><span data-stu-id="a13ff-131"><span id="_security_pkcs_7_asn_encoding_gly"></span><span id="_SECURITY_PKCS_7_ASN_ENCODING_GLY"></span>**PKCS\_7\_ASN\_ENCODING**</span></span>
</dt> <dd>

<span data-ttu-id="a13ff-132">Ein [*Nachrichten Codierungstyp*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="a13ff-132">A [*message encoding type*](m-gly.md).</span></span> <span data-ttu-id="a13ff-133">Nachrichten Codierungs Typen werden im höherwertigen Wort eines **DWORD** gespeichert (Wert: 0x00010000 bis).</span><span class="sxs-lookup"><span data-stu-id="a13ff-133">Message encoding types are stored in the high-order word of a **DWORD** (value is: 0x00010000).</span></span>

</dd> <dt>

<span data-ttu-id="a13ff-134"><span id="_security_plaintext_gly"></span><span id="_SECURITY_PLAINTEXT_GLY"></span>**nur**</span><span class="sxs-lookup"><span data-stu-id="a13ff-134"><span id="_security_plaintext_gly"></span><span id="_SECURITY_PLAINTEXT_GLY"></span>**plaintext**</span></span>
</dt> <dd>

<span data-ttu-id="a13ff-135">Eine unverschlüsselte Nachricht.</span><span class="sxs-lookup"><span data-stu-id="a13ff-135">A message that is not encrypted.</span></span> <span data-ttu-id="a13ff-136">Nachrichten, die nicht verschlüsselt sind, werden mitunter auch als Klartextnachrichten bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="a13ff-136">Plaintext messages are sometimes referred to as cleartext messages.</span></span>

</dd> <dt>

<span data-ttu-id="a13ff-137"><span id="_security_portable_executable_pe_image_gly"></span><span id="_SECURITY_PORTABLE_EXECUTABLE_PE_IMAGE_GLY"></span>**Bild der portablen ausführbaren Datei (PE)**</span><span class="sxs-lookup"><span data-stu-id="a13ff-137"><span id="_security_portable_executable_pe_image_gly"></span><span id="_SECURITY_PORTABLE_EXECUTABLE_PE_IMAGE_GLY"></span>**Portable Executable (PE) Image**</span></span>
</dt> <dd>

<span data-ttu-id="a13ff-138">Das standardmäßige ausführbare Windows-Format.</span><span class="sxs-lookup"><span data-stu-id="a13ff-138">The standard Windows executable format.</span></span>

</dd> <dt>

<span data-ttu-id="a13ff-139"><span id="_security_prf_gly"></span><span id="_SECURITY_PRF_GLY"></span>**PRF**</span><span class="sxs-lookup"><span data-stu-id="a13ff-139"><span id="_security_prf_gly"></span><span id="_SECURITY_PRF_GLY"></span>**PRF**</span></span>
</dt> <dd>

<span data-ttu-id="a13ff-140">Siehe *Pseudo Zufallsfunktion*.</span><span class="sxs-lookup"><span data-stu-id="a13ff-140">See *Pseudo-Random Function*.</span></span>

</dd> <dt>

<span data-ttu-id="a13ff-141"><span id="_security_primary_credentials_gly"></span><span id="_SECURITY_PRIMARY_CREDENTIALS_GLY"></span>**primäre Anmelde Informationen**</span><span class="sxs-lookup"><span data-stu-id="a13ff-141"><span id="_security_primary_credentials_gly"></span><span id="_SECURITY_PRIMARY_CREDENTIALS_GLY"></span>**primary credentials**</span></span>
</dt> <dd>

<span data-ttu-id="a13ff-142">Das \_ Authentifizierungs Paket MsV1 0 definiert einen primären Zeichen folgen Wert für die Anmelde Informationen: die primäre Anmelde Informations Zeichenfolge enthält die Anmelde Informationen, die bei der ersten Anmeldung bereitgestellt werden</span><span class="sxs-lookup"><span data-stu-id="a13ff-142">The MsV1\_0 authentication package defines a primary credential key string value: The primary credentials string holds the credentials provided at initial logon time.</span></span> <span data-ttu-id="a13ff-143">Sie enthält den Benutzernamen und sowohl die Groß-/Kleinschreibung als auch die Groß-/Kleinschreibung für das Kennwort des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="a13ff-143">It includes the user name and both case-sensitive and case-insensitive forms of the user's password.</span></span>

<span data-ttu-id="a13ff-144">Weitere Informationen finden Sie unter [*ergänzende Anmelde*](s-gly.md)Informationen.</span><span class="sxs-lookup"><span data-stu-id="a13ff-144">See also [*supplemental credentials*](s-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="a13ff-145"><span id="_security_primary_service_provider_gly"></span><span id="_SECURITY_PRIMARY_SERVICE_PROVIDER_GLY"></span>**primärer Dienstanbieter**</span><span class="sxs-lookup"><span data-stu-id="a13ff-145"><span id="_security_primary_service_provider_gly"></span><span id="_SECURITY_PRIMARY_SERVICE_PROVIDER_GLY"></span>**primary service provider**</span></span>
</dt> <dd>

<span data-ttu-id="a13ff-146">Der Dienstanbieter, der die Steuerungs Schnittstellen für die Karte bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="a13ff-146">The service provider that supplies the control interfaces to the card.</span></span> <span data-ttu-id="a13ff-147">Jede Smartcard kann Ihren primären Dienstanbieter in der Smartcard-Datenbank registrieren.</span><span class="sxs-lookup"><span data-stu-id="a13ff-147">Each smart card can register its primary service provider in the smart card database.</span></span>

</dd> <dt>

<span data-ttu-id="a13ff-148"><span id="_security_primary_token_gly"></span><span id="_SECURITY_PRIMARY_TOKEN_GLY"></span>**primäres Token**</span><span class="sxs-lookup"><span data-stu-id="a13ff-148"><span id="_security_primary_token_gly"></span><span id="_SECURITY_PRIMARY_TOKEN_GLY"></span>**primary token**</span></span>
</dt> <dd>

<span data-ttu-id="a13ff-149">Ein Zugriffs Token, das in der Regel nur vom Windows-Kernel erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a13ff-149">An access token that is typically created only by the Windows kernel.</span></span> <span data-ttu-id="a13ff-150">Sie kann einem Prozess zugewiesen werden, der die Standard Sicherheitsinformationen für diesen Prozess darstellt.</span><span class="sxs-lookup"><span data-stu-id="a13ff-150">It may be assigned to a process to represent the default security information for that process.</span></span>

<span data-ttu-id="a13ff-151">Siehe auch [*Zugriffs Token*](a-gly.md) und Identitätswechsel [*Token*](i-gly.md).</span><span class="sxs-lookup"><span data-stu-id="a13ff-151">See also [*access token*](a-gly.md) and [*impersonation token*](i-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="a13ff-152"><span id="_security_principal_gly"></span><span id="_SECURITY_PRINCIPAL_GLY"></span>**Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="a13ff-152"><span id="_security_principal_gly"></span><span id="_SECURITY_PRINCIPAL_GLY"></span>**principal**</span></span>
</dt> <dd>

<span data-ttu-id="a13ff-153">Siehe [*Sicherheits Prinzipal*](s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="a13ff-153">See [*security principal*](s-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="a13ff-154"><span id="_security_privacy_gly"></span><span id="_SECURITY_PRIVACY_GLY"></span>**Datenschutz**</span><span class="sxs-lookup"><span data-stu-id="a13ff-154"><span id="_security_privacy_gly"></span><span id="_SECURITY_PRIVACY_GLY"></span>**privacy**</span></span>
</dt> <dd>

<span data-ttu-id="a13ff-155">Die Bedingung, dass Sie von der Sicht oder dem geheimen Schlüssel isoliert werden.</span><span class="sxs-lookup"><span data-stu-id="a13ff-155">The condition of being isolated from view or secret.</span></span> <span data-ttu-id="a13ff-156">In Bezug auf Nachrichten sind private Nachrichten verschlüsselte Nachrichten, deren Text aus der Ansicht ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="a13ff-156">With respect to messages, private messages are encrypted messages whose text is hidden from view.</span></span> <span data-ttu-id="a13ff-157">In Bezug auf Schlüssel ist ein privater Schlüssel ein geheimer Schlüssel, der von anderen Personen verborgen ist.</span><span class="sxs-lookup"><span data-stu-id="a13ff-157">With respect to keys, a private key is a secret key concealed from others.</span></span>

</dd> <dt>

<span data-ttu-id="a13ff-158"><span id="_security_private_key_gly"></span><span id="_SECURITY_PRIVATE_KEY_GLY"></span>**privater Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="a13ff-158"><span id="_security_private_key_gly"></span><span id="_SECURITY_PRIVATE_KEY_GLY"></span>**private key**</span></span>
</dt> <dd>

<span data-ttu-id="a13ff-159">Die geheime Hälfte eines Schlüssel Paars, das in einem Algorithmus für öffentliche Schlüssel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a13ff-159">The secret half of a key pair used in a public key algorithm.</span></span> <span data-ttu-id="a13ff-160">Private Schlüssel werden normalerweise zur Verschlüsselung von symmetrischen Sitzungsschlüsseln, zur digitalen Signierung von Nachrichten oder zur Entschlüsselung von Nachrichten, die mit dem entsprechenden öffentlichen Schlüssel verschlüsselt wurden, verwendet.</span><span class="sxs-lookup"><span data-stu-id="a13ff-160">Private keys are typically used to encrypt a symmetric session key, digitally sign a message, or decrypt a message that has been encrypted with the corresponding public key.</span></span>

<span data-ttu-id="a13ff-161">Siehe auch *öffentlicher Schlüssel*.</span><span class="sxs-lookup"><span data-stu-id="a13ff-161">See also *public key*.</span></span>

</dd> <dt>

<span data-ttu-id="a13ff-162"><span id="_security_private_key_blob_gly"></span><span id="_SECURITY_PRIVATE_KEY_BLOB_GLY"></span>**BLOB des privaten Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="a13ff-162"><span id="_security_private_key_blob_gly"></span><span id="_SECURITY_PRIVATE_KEY_BLOB_GLY"></span>**private key BLOB**</span></span>
</dt> <dd>

<span data-ttu-id="a13ff-163">Ein Schlüssel-BLOB, das ein ganzes öffentliches/privates Schlüsselpaar enthält.</span><span class="sxs-lookup"><span data-stu-id="a13ff-163">A key BLOB that contains a complete public/private key pair.</span></span> <span data-ttu-id="a13ff-164">Private schlüsselblobschlüssel werden von Verwaltungsprogrammen verwendet, um Schlüsselpaare zu transportieren.</span><span class="sxs-lookup"><span data-stu-id="a13ff-164">Private key BLOBs are used by administrative programs to transport key pairs.</span></span> <span data-ttu-id="a13ff-165">Da der private Schlüsselteil des Schlüssel Paars äußerst vertraulich ist, werden diese BLOB in der Regel mit einer symmetrischen Chiffre verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="a13ff-165">As the private key portion of the key pair is extremely confidential, these BLOBs are typically kept encrypted with a symmetric cipher.</span></span> <span data-ttu-id="a13ff-166">Diese Schlüsselblob können auch von erweiterten Anwendungen verwendet werden, bei denen die Schlüsselpaare innerhalb der Anwendung gespeichert werden, anstatt sich auf den Speichermechanismus des CSP zu verlassen.</span><span class="sxs-lookup"><span data-stu-id="a13ff-166">These key BLOBs can also be used by advanced applications where the key pairs are stored within the application, rather than relying on the CSP's storage mechanism.</span></span> <span data-ttu-id="a13ff-167">Ein Schlüsselblob wird durch Aufrufen der **CryptExportKey** -Funktion erstellt.</span><span class="sxs-lookup"><span data-stu-id="a13ff-167">A key BLOB is created by calling the **CryptExportKey** function.</span></span>

</dd> <dt>

<span data-ttu-id="a13ff-168"><span id="_security_privilege_gly"></span><span id="_SECURITY_PRIVILEGE_GLY"></span>**Ehre**</span><span class="sxs-lookup"><span data-stu-id="a13ff-168"><span id="_security_privilege_gly"></span><span id="_SECURITY_PRIVILEGE_GLY"></span>**privilege**</span></span>
</dt> <dd>

<span data-ttu-id="a13ff-169">Das Recht eines Benutzers zur Durchführung verschiedener Systemvorgänge wie Herunterfahren des Systems, Laden von Gerätetreibern oder Ändern der Systemzeit.</span><span class="sxs-lookup"><span data-stu-id="a13ff-169">The right of a user to perform various system-related operations, such as shutting down the system, loading device drivers, or changing the system time.</span></span> <span data-ttu-id="a13ff-170">Das Zugriffs Token eines Benutzers enthält eine Liste der Berechtigungen, die der Benutzer oder die Benutzergruppen innehat.</span><span class="sxs-lookup"><span data-stu-id="a13ff-170">A user's access token contains a list of the privileges held by either the user or the user's groups.</span></span>

</dd> <dt>

<span data-ttu-id="a13ff-171"><span id="_security_process_gly"></span><span id="_SECURITY_PROCESS_GLY"></span>**ESS**</span><span class="sxs-lookup"><span data-stu-id="a13ff-171"><span id="_security_process_gly"></span><span id="_SECURITY_PROCESS_GLY"></span>**process**</span></span>
</dt> <dd>

<span data-ttu-id="a13ff-172">Der Sicherheitskontext, in dem eine Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a13ff-172">The security context under which an application runs.</span></span> <span data-ttu-id="a13ff-173">Der Sicherheitskontext ist normalerweise einem Benutzer zugeordnet, sodass alle Anwendungen, die unter einem bestimmten Prozess ausgeführt werden, die Rechte und Berechtigungen des entsprechenden Benutzers übernehmen.</span><span class="sxs-lookup"><span data-stu-id="a13ff-173">Typically, the security context is associated with a user, so all applications running under a given process take on the permissions and privileges of the owning user.</span></span>

</dd> <dt>

<span data-ttu-id="a13ff-174"><span id="_security_prov_dss_gly"></span><span id="_SECURITY_PROV_DSS_GLY"></span>**Prov- \_ DSS**</span><span class="sxs-lookup"><span data-stu-id="a13ff-174"><span id="_security_prov_dss_gly"></span><span id="_SECURITY_PROV_DSS_GLY"></span>**PROV\_DSS**</span></span>
</dt> <dd>

<span data-ttu-id="a13ff-175">Siehe *Prov \_ DSS Provider Type*.</span><span class="sxs-lookup"><span data-stu-id="a13ff-175">See *PROV\_DSS provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="a13ff-176"><span id="_security_prov_dss_provider_type_gly"></span><span id="_SECURITY_PROV_DSS_PROVIDER_TYPE_GLY"></span>**Prov \_ DSS-Anbietertyp**</span><span class="sxs-lookup"><span data-stu-id="a13ff-176"><span id="_security_prov_dss_provider_type_gly"></span><span id="_SECURITY_PROV_DSS_PROVIDER_TYPE_GLY"></span>**PROV\_DSS Provider Type**</span></span>
</dt> <dd>

<span data-ttu-id="a13ff-177">Der vordefinierte Anbietertyp, der nur digitale Signaturen und Hashes unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a13ff-177">Predefined provider type that only supports digital signatures and hashes.</span></span> <span data-ttu-id="a13ff-178">Er gibt den DSA-Signatur Algorithmus und die MD5-und SHA-1-Hash Algorithmen an.</span><span class="sxs-lookup"><span data-stu-id="a13ff-178">It specifies the DSA signature algorithm, and the MD5 and SHA-1 hashing algorithms.</span></span>

</dd> <dt>

<span data-ttu-id="a13ff-179"><span id="_security_prov_dss_dh_gly"></span><span id="_SECURITY_PROV_DSS_DH_GLY"></span>**Prov \_ DSS \_ dh**</span><span class="sxs-lookup"><span data-stu-id="a13ff-179"><span id="_security_prov_dss_dh_gly"></span><span id="_SECURITY_PROV_DSS_DH_GLY"></span>**PROV\_DSS\_DH**</span></span>
</dt> <dd>

<span data-ttu-id="a13ff-180">Siehe *Prov \_ DSS \_ dh-Anbietertyp*.</span><span class="sxs-lookup"><span data-stu-id="a13ff-180">See *PROV\_DSS\_DH provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="a13ff-181"><span id="_security_prov_dss_dh_provider_type_gly"></span><span id="_SECURITY_PROV_DSS_DH_PROVIDER_TYPE_GLY"></span>**Prov \_ DSS \_ dh-Anbietertyp**</span><span class="sxs-lookup"><span data-stu-id="a13ff-181"><span id="_security_prov_dss_dh_provider_type_gly"></span><span id="_SECURITY_PROV_DSS_DH_PROVIDER_TYPE_GLY"></span>**PROV\_DSS\_DH provider type**</span></span>
</dt> <dd>

<span data-ttu-id="a13ff-182">Der vordefinierte Anbietertyp, der Schlüsselaustausch-, digitale Signatur-und Hash Algorithmen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="a13ff-182">Predefined provider type that provides key exchange, digital signature, and hashing algorithms.</span></span> <span data-ttu-id="a13ff-183">Dies ähnelt dem Prov- \_ DSS-Anbietertyp.</span><span class="sxs-lookup"><span data-stu-id="a13ff-183">It is similar to the PROV\_DSS provider type.</span></span>

</dd> <dt>

<span data-ttu-id="a13ff-184"><span id="_security_prov_fortezza_gly"></span><span id="_SECURITY_PROV_FORTEZZA_GLY"></span>**Prov- \_ Fortezza**</span><span class="sxs-lookup"><span data-stu-id="a13ff-184"><span id="_security_prov_fortezza_gly"></span><span id="_SECURITY_PROV_FORTEZZA_GLY"></span>**PROV\_FORTEZZA**</span></span>
</dt> <dd>

<span data-ttu-id="a13ff-185">Siehe *Prov \_ Fortezza-Anbietertyp*.</span><span class="sxs-lookup"><span data-stu-id="a13ff-185">See *PROV\_FORTEZZA provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="a13ff-186"><span id="_security_prov_fortezza_provider_type_gly"></span><span id="_SECURITY_PROV_FORTEZZA_PROVIDER_TYPE_GLY"></span>**Prov \_ Fortezza-Anbietertyp**</span><span class="sxs-lookup"><span data-stu-id="a13ff-186"><span id="_security_prov_fortezza_provider_type_gly"></span><span id="_SECURITY_PROV_FORTEZZA_PROVIDER_TYPE_GLY"></span>**PROV\_FORTEZZA provider type**</span></span>
</dt> <dd>

<span data-ttu-id="a13ff-187">Der vordefinierte Anbietertyp, der Schlüsselaustausch-, digitale Signatur-, Verschlüsselungs-und Hash Algorithmen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="a13ff-187">Predefined provider type that provides key exchange, digital signature, encryption, and hashing algorithms.</span></span> <span data-ttu-id="a13ff-188">Die kryptografischen Protokolle und Algorithmen, die von diesem Anbietertyp angegeben werden, sind im Besitz des National Institute of Standards and Technology (NIST).</span><span class="sxs-lookup"><span data-stu-id="a13ff-188">The cryptographic protocols and algorithms specified by this provider type are owned by the National Institute of Standards and Technology (NIST).</span></span>

</dd> <dt>

<span data-ttu-id="a13ff-189"><span id="_security_prov_ms_exchange_gly"></span><span id="_SECURITY_PROV_MS_EXCHANGE_GLY"></span>**Prov \_ MS \_ Exchange**</span><span class="sxs-lookup"><span data-stu-id="a13ff-189"><span id="_security_prov_ms_exchange_gly"></span><span id="_SECURITY_PROV_MS_EXCHANGE_GLY"></span>**PROV\_MS\_EXCHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="a13ff-190">Siehe *Prov \_ MS \_ Exchange-Anbietertyp*.</span><span class="sxs-lookup"><span data-stu-id="a13ff-190">See *PROV\_MS\_EXCHANGE provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="a13ff-191"><span id="_security_prov_ms_exchange_provider_type_gly"></span><span id="_SECURITY_PROV_MS_EXCHANGE_PROVIDER_TYPE_GLY"></span>**Prov \_ MS \_ Exchange-Anbietertyp**</span><span class="sxs-lookup"><span data-stu-id="a13ff-191"><span id="_security_prov_ms_exchange_provider_type_gly"></span><span id="_SECURITY_PROV_MS_EXCHANGE_PROVIDER_TYPE_GLY"></span>**PROV\_MS\_EXCHANGE provider type**</span></span>
</dt> <dd>

<span data-ttu-id="a13ff-192">Der vordefinierte Anbietertyp, der für die Anforderungen von Microsoft Exchange konzipiert ist, sowie andere Anwendungen, die mit Microsoft Mail kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="a13ff-192">Predefined provider type designed for the needs of Microsoft Exchange, as well as other applications that are compatible with Microsoft Mail.</span></span> <span data-ttu-id="a13ff-193">Es stellt Schlüsselaustausch-, digitale Signatur-, Verschlüsselungs-und Hash Algorithmen bereit.</span><span class="sxs-lookup"><span data-stu-id="a13ff-193">It provides key exchange, digital signature, encryption, and hashing algorithms.</span></span>

</dd> <dt>

<span data-ttu-id="a13ff-194"><span id="_security_prov_rsa_full_gly"></span><span id="_SECURITY_PROV_RSA_FULL_GLY"></span>**Prov \_ RSA \_ Full**</span><span class="sxs-lookup"><span data-stu-id="a13ff-194"><span id="_security_prov_rsa_full_gly"></span><span id="_SECURITY_PROV_RSA_FULL_GLY"></span>**PROV\_RSA\_FULL**</span></span>
</dt> <dd>

<span data-ttu-id="a13ff-195">Siehe *Prov \_ RSA \_ Full Provider Type*.</span><span class="sxs-lookup"><span data-stu-id="a13ff-195">See *PROV\_RSA\_FULL provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="a13ff-196"><span id="_security_prov_rsa_full_provider_type_gly"></span><span id="_SECURITY_PROV_RSA_FULL_PROVIDER_TYPE_GLY"></span>**Prov \_ RSA \_ Full-Anbietertyp**</span><span class="sxs-lookup"><span data-stu-id="a13ff-196"><span id="_security_prov_rsa_full_provider_type_gly"></span><span id="_SECURITY_PROV_RSA_FULL_PROVIDER_TYPE_GLY"></span>**PROV\_RSA\_FULL provider type**</span></span>
</dt> <dd>

<span data-ttu-id="a13ff-197">Der von Microsoft und RSA Data Security, Inc. definierte vordefinierte Anbietertyp. Dieser allgemeine Anbietertyp stellt Schlüsselaustausch-, digitale Signatur-, Verschlüsselungs-und Hash Algorithmen bereit.</span><span class="sxs-lookup"><span data-stu-id="a13ff-197">Predefined provider type defined by Microsoft and RSA Data Security, Inc. This general purpose provider type provides key exchange, digital signature, encryption, and hashing algorithms.</span></span> <span data-ttu-id="a13ff-198">Die Algorithmen "Schlüsselaustausch", "digitale Signatur" und "Verschlüsselung" basieren auf Kryptografie mit öffentlichem RSA-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="a13ff-198">The key exchange, digital signature, and encryption algorithms are based on RSA public key cryptography.</span></span>

</dd> <dt>

<span data-ttu-id="a13ff-199"><span id="_security_prov_rsa_sig_gly"></span><span id="_SECURITY_PROV_RSA_SIG_GLY"></span>**Prov \_ RSA \_ sig**</span><span class="sxs-lookup"><span data-stu-id="a13ff-199"><span id="_security_prov_rsa_sig_gly"></span><span id="_SECURITY_PROV_RSA_SIG_GLY"></span>**PROV\_RSA\_SIG**</span></span>
</dt> <dd>

<span data-ttu-id="a13ff-200">Siehe *Prov \_ RSA \_ sig-Anbietertyp*.</span><span class="sxs-lookup"><span data-stu-id="a13ff-200">See *PROV\_RSA\_SIG provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="a13ff-201"><span id="_security_prov_rsa_sig_provider_type_gly"></span><span id="_SECURITY_PROV_RSA_SIG_PROVIDER_TYPE_GLY"></span>**Prov \_ RSA \_ sig-Anbietertyp**</span><span class="sxs-lookup"><span data-stu-id="a13ff-201"><span id="_security_prov_rsa_sig_provider_type_gly"></span><span id="_SECURITY_PROV_RSA_SIG_PROVIDER_TYPE_GLY"></span>**PROV\_RSA\_SIG provider type**</span></span>
</dt> <dd>

<span data-ttu-id="a13ff-202">Der von Microsoft und der RSA-Datensicherheit definierte vordefinierte Anbietertyp.</span><span class="sxs-lookup"><span data-stu-id="a13ff-202">Predefined provider type defined by Microsoft and RSA Data Security.</span></span> <span data-ttu-id="a13ff-203">Dieser Anbietertyp ist eine Teilmenge von Prov \_ RSA \_ Full, die nur digitale Signaturen und Hash Algorithmen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="a13ff-203">This provider type is a subset of PROV\_RSA\_FULL that provides only digital signature and hashing algorithms.</span></span> <span data-ttu-id="a13ff-204">Der Algorithmus für die digitale Signatur ist ein RSA-Algorithmus für öffentliche Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="a13ff-204">The digital signature algorithm is an RSA public key algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="a13ff-205"><span id="_security_prov_ssl_gly"></span><span id="_SECURITY_PROV_SSL_GLY"></span>**Prov- \_ SSL**</span><span class="sxs-lookup"><span data-stu-id="a13ff-205"><span id="_security_prov_ssl_gly"></span><span id="_SECURITY_PROV_SSL_GLY"></span>**PROV\_SSL**</span></span>
</dt> <dd>

<span data-ttu-id="a13ff-206">Siehe *Prov- \_ SSL-Anbietertyp*.</span><span class="sxs-lookup"><span data-stu-id="a13ff-206">See *PROV\_SSL provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="a13ff-207"><span id="_security_prov_ssl_provider_type_gly"></span><span id="_SECURITY_PROV_SSL_PROVIDER_TYPE_GLY"></span>**Prov- \_ SSL-Anbietertyp**</span><span class="sxs-lookup"><span data-stu-id="a13ff-207"><span id="_security_prov_ssl_provider_type_gly"></span><span id="_SECURITY_PROV_SSL_PROVIDER_TYPE_GLY"></span>**PROV\_SSL provider type**</span></span>
</dt> <dd>

<span data-ttu-id="a13ff-208">Der vordefinierte Anbietertyp, der das Secure Sockets Layer (SSL)-Protokoll unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a13ff-208">Predefined provider type that supports the Secure Sockets Layer (SSL) protocol.</span></span> <span data-ttu-id="a13ff-209">Dieser Typ stellt Schlüssel Verschlüsselung, digitale Signatur, Verschlüsselung und Hash Algorithmen bereit.</span><span class="sxs-lookup"><span data-stu-id="a13ff-209">This type provides key encryption, digital signature, encryption, and hashing algorithms.</span></span> <span data-ttu-id="a13ff-210">Eine Spezifikation, die SSL erläutert, ist in Netscape Communications Corp verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a13ff-210">A specification explaining SSL is available from Netscape Communications Corp.</span></span>

</dd> <dt>

<span data-ttu-id="a13ff-211"><span id="_security_provider_gly"></span><span id="_SECURITY_PROVIDER_GLY"></span>**ab**</span><span class="sxs-lookup"><span data-stu-id="a13ff-211"><span id="_security_provider_gly"></span><span id="_SECURITY_PROVIDER_GLY"></span>**provider**</span></span>
</dt> <dd>

<span data-ttu-id="a13ff-212">Siehe [*Kryptografiedienstanbieter*](c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="a13ff-212">See [*Cryptographic Service Provider*](c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="a13ff-213"><span id="_security_provider_name_gly"></span><span id="_SECURITY_PROVIDER_NAME_GLY"></span>**Anbieter Name**</span><span class="sxs-lookup"><span data-stu-id="a13ff-213"><span id="_security_provider_name_gly"></span><span id="_SECURITY_PROVIDER_NAME_GLY"></span>**provider name**</span></span>
</dt> <dd>

<span data-ttu-id="a13ff-214">Ein Name, der zum Identifizieren eines CSP verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a13ff-214">A name used to identify a CSP.</span></span> <span data-ttu-id="a13ff-215">Beispielsweise die Microsoft-Basis-Kryptografieanbieter Version 1,0.</span><span class="sxs-lookup"><span data-stu-id="a13ff-215">For example, the Microsoft Base Cryptographic Provider version 1.0.</span></span> <span data-ttu-id="a13ff-216">Der Anbieter Name wird in der Regel verwendet, wenn die **CryptAcquireContext** -Funktion aufgerufen wird, um eine Verbindung mit einem CSP herzustellen.</span><span class="sxs-lookup"><span data-stu-id="a13ff-216">The provider name is typically used when calling the **CryptAcquireContext** function to connect to a CSP.</span></span>

</dd> <dt>

<span data-ttu-id="a13ff-217"><span id="_security_provider_type_gly"></span><span id="_SECURITY_PROVIDER_TYPE_GLY"></span>**Anbietertyp**</span><span class="sxs-lookup"><span data-stu-id="a13ff-217"><span id="_security_provider_type_gly"></span><span id="_SECURITY_PROVIDER_TYPE_GLY"></span>**provider type**</span></span>
</dt> <dd>

<span data-ttu-id="a13ff-218">Ein Begriff, mit dem ein Kryptografiedienstanbieter (kryptografischen Service Provider, CSP) identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="a13ff-218">A term used to identify a type of cryptographic service provider (CSP).</span></span> <span data-ttu-id="a13ff-219">CSPs werden in unterschiedlichen Anbieter Typen gruppiert, die eine bestimmte Familie von Standarddaten Formaten und-Protokollen darstellen.</span><span class="sxs-lookup"><span data-stu-id="a13ff-219">CSPs are grouped into different provider types that represent a specific families of standard data formats and protocols.</span></span> <span data-ttu-id="a13ff-220">Im Gegensatz zum eindeutigen Anbieter Namen eines CSP sind Anbieter Typen für einen bestimmten CSP nicht eindeutig.</span><span class="sxs-lookup"><span data-stu-id="a13ff-220">In contrast to a CSP's unique provider name, provider types are not unique for a given CSP.</span></span> <span data-ttu-id="a13ff-221">Der Anbietertyp wird normalerweise verwendet, wenn die **CryptAcquireContext** -Funktion aufgerufen wird, um eine Verbindung mit einem CSP herzustellen.</span><span class="sxs-lookup"><span data-stu-id="a13ff-221">The provider type is typically used when calling the **CryptAcquireContext** function to connect to a CSP.</span></span>

</dd> <dt>

<span data-ttu-id="a13ff-222"><span id="_security_pseudo_random_function_gly"></span><span id="_SECURITY_PSEUDO_RANDOM_FUNCTION_GLY"></span>**Pseudo Zufallsfunktion**</span><span class="sxs-lookup"><span data-stu-id="a13ff-222"><span id="_security_pseudo_random_function_gly"></span><span id="_SECURITY_PSEUDO_RANDOM_FUNCTION_GLY"></span>**pseudo-random function**</span></span>
</dt> <dd>

<span data-ttu-id="a13ff-223">PRF Eine Funktion, die einen Schlüssel, eine Bezeichnung und einen Ausgangswert als Eingabe annimmt und dann eine Ausgabe beliebiger Länge erzeugt.</span><span class="sxs-lookup"><span data-stu-id="a13ff-223">(PRF) A function that takes a key, label, and seed as input, then produces an output of arbitrary length.</span></span>

</dd> <dt>

<span data-ttu-id="a13ff-224"><span id="_security_public_private_key_pair_gly"></span><span id="_SECURITY_PUBLIC_PRIVATE_KEY_PAIR_GLY"></span>**öffentliches/privates Schlüsselpaar**</span><span class="sxs-lookup"><span data-stu-id="a13ff-224"><span id="_security_public_private_key_pair_gly"></span><span id="_SECURITY_PUBLIC_PRIVATE_KEY_PAIR_GLY"></span>**public/private key pair**</span></span>
</dt> <dd>

<span data-ttu-id="a13ff-225">Ein Satz kryptografischer Schlüssel für eine Kryptografie mit öffentlichen Schlüsseln.</span><span class="sxs-lookup"><span data-stu-id="a13ff-225">A set of cryptographic keys used for public key cryptography.</span></span> <span data-ttu-id="a13ff-226">Ein CSP verwaltet für jeden Benutzer in der Regel zwei öffentliche/private Schlüsselpaare: ein Exchange-Schlüsselpaar und ein Schlüsselpaar für digitale Signaturen.</span><span class="sxs-lookup"><span data-stu-id="a13ff-226">For each user, a CSP usually maintains two public/private key pairs: an exchange key pair and a digital signature key pair.</span></span> <span data-ttu-id="a13ff-227">Beide Schlüsselpaare werden sitzungsübergreifend beibehalten.</span><span class="sxs-lookup"><span data-stu-id="a13ff-227">Both key pairs are maintained from session to session.</span></span>

<span data-ttu-id="a13ff-228">Siehe [*Austausch Schlüssel*](e-gly.md) paar und [*Signatur Schlüsselpaar*](s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="a13ff-228">See [*exchange key pair*](e-gly.md) and [*signature key pair*](s-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="a13ff-229"><span id="_security_public_key_gly"></span><span id="_SECURITY_PUBLIC_KEY_GLY"></span>**öffentlicher Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="a13ff-229"><span id="_security_public_key_gly"></span><span id="_SECURITY_PUBLIC_KEY_GLY"></span>**public key**</span></span>
</dt> <dd>

<span data-ttu-id="a13ff-230">Ein kryptografischer Schlüssel, der normalerweise zum Entschlüsseln eines Sitzungsschlüssels oder einer digitalen Signatur verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a13ff-230">A cryptographic key typically used when decrypting a session key or a digital signature.</span></span> <span data-ttu-id="a13ff-231">Der öffentliche Schlüssel kann auch zum Verschlüsseln einer Nachricht verwendet werden. Dadurch wird sichergestellt, dass nur die Person mit dem entsprechenden privaten Schlüssel die Nachricht entschlüsseln kann.</span><span class="sxs-lookup"><span data-stu-id="a13ff-231">The public key can also be used to encrypt a message, guaranteeing that only the person with the corresponding private key can decrypt the message.</span></span>

<span data-ttu-id="a13ff-232">Siehe auch *privater Schlüssel*.</span><span class="sxs-lookup"><span data-stu-id="a13ff-232">See also *private key*.</span></span>

</dd> <dt>

<span data-ttu-id="a13ff-233"><span id="_security_public_key_algorithm_gly"></span><span id="_SECURITY_PUBLIC_KEY_ALGORITHM_GLY"></span>**Algorithmus für öffentliche Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="a13ff-233"><span id="_security_public_key_algorithm_gly"></span><span id="_SECURITY_PUBLIC_KEY_ALGORITHM_GLY"></span>**public key algorithm**</span></span>
</dt> <dd>

<span data-ttu-id="a13ff-234">Eine asymmetrische Verschlüsselung, bei der zwei Schlüssel verwendet werden: eine für die Verschlüsselung, der öffentliche Schlüssel und die andere für die Entschlüsselung, der private Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="a13ff-234">An asymmetric cipher that uses two keys, one for encryption, the public key, and the other for decryption, the private key.</span></span> <span data-ttu-id="a13ff-235">Gemäß den Schlüsselnamen kann der öffentliche Schlüssel, der zum Codieren von Klartext verwendet wird, allen Benutzern zur Verfügung gestellt werden.</span><span class="sxs-lookup"><span data-stu-id="a13ff-235">As implied by the key names, the public key used to encode plaintext can be made available to anyone.</span></span> <span data-ttu-id="a13ff-236">Der private Schlüssel muss jedoch geheim bleiben.</span><span class="sxs-lookup"><span data-stu-id="a13ff-236">However, the private key must remain secret.</span></span> <span data-ttu-id="a13ff-237">Der Chiffre Text kann nur mit dem privaten Schlüssel entschlüsselt werden.</span><span class="sxs-lookup"><span data-stu-id="a13ff-237">Only the private key can decrypt the ciphertext.</span></span> <span data-ttu-id="a13ff-238">Der in diesem Prozess verwendete Algorithmus für öffentliche Schlüssel ist langsam (in der Reihenfolge der 1.000-mal langsamer als symmetrische Algorithmen) und wird in der Regel zum Verschlüsseln von Sitzungs Schlüsseln oder zum digitalen Signieren einer Nachricht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a13ff-238">The public key algorithm used in this process is slow (on the order of 1,000 times slower than symmetric algorithms), and is typically used to encrypt session keys or digitally sign a message.</span></span>

<span data-ttu-id="a13ff-239">Siehe auch *öffentlichen* und *privaten Schlüssel*.</span><span class="sxs-lookup"><span data-stu-id="a13ff-239">See also *public key* and *private key*.</span></span>

</dd> <dt>

<span data-ttu-id="a13ff-240"><span id="_security_public_key_blob_gly"></span><span id="_SECURITY_PUBLIC_KEY_BLOB_GLY"></span>**BLOB für öffentliche Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="a13ff-240"><span id="_security_public_key_blob_gly"></span><span id="_SECURITY_PUBLIC_KEY_BLOB_GLY"></span>**public key BLOB**</span></span>
</dt> <dd>

<span data-ttu-id="a13ff-241">Ein BLOB, das verwendet wird, um den Teil des öffentlichen Schlüssels eines öffentlichen/privaten Schlüssel Paars zu speichern.</span><span class="sxs-lookup"><span data-stu-id="a13ff-241">A BLOB used to store the public key portion of a public/private key pair.</span></span> <span data-ttu-id="a13ff-242">Blobschlüssel für öffentliche Schlüssel werden nicht verschlüsselt, weil der öffentliche Schlüssel, der in enthalten ist, nicht geheim ist.</span><span class="sxs-lookup"><span data-stu-id="a13ff-242">Public key BLOBs are not encrypted as the public key contained within is not secret.</span></span> <span data-ttu-id="a13ff-243">Ein öffentliches Schlüsselblob wird durch Aufrufen der **CryptExportKey** -Funktion erstellt.</span><span class="sxs-lookup"><span data-stu-id="a13ff-243">A public key BLOB is created by calling the **CryptExportKey** function.</span></span>

</dd> <dt>

<span data-ttu-id="a13ff-244"><span id="_security_public_key_cryptography_standards_gly"></span><span id="_SECURITY_PUBLIC_KEY_CRYPTOGRAPHY_STANDARDS_GLY"></span>**Kryptografiestandards für öffentliche Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="a13ff-244"><span id="_security_public_key_cryptography_standards_gly"></span><span id="_SECURITY_PUBLIC_KEY_CRYPTOGRAPHY_STANDARDS_GLY"></span>**Public Key Cryptography Standards**</span></span>
</dt> <dd>

<span data-ttu-id="a13ff-245">PKCS Eine Reihe von Syntax Standards für die Kryptografie mit öffentlichem Schlüssel, die Sicherheitsfunktionen abdeckt, einschließlich Methoden zum Signieren von Daten, Austauschen von Schlüsseln, Anfordern von Zertifikaten, Verschlüsselung und Entschlüsselung von öffentlichem Schlüsseln und andere Sicherheitsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="a13ff-245">(PKCS) A set of syntax standards for public key cryptography covering security functions, including methods for signing data, exchanging keys, requesting certificates, public key encryption and decryption, and other security functions.</span></span>

</dd> <dt>

<span data-ttu-id="a13ff-246"><span id="_security_public_key_encryption_gly"></span><span id="_SECURITY_PUBLIC_KEY_ENCRYPTION_GLY"></span>**Verschlüsselung mit öffentlichem Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="a13ff-246"><span id="_security_public_key_encryption_gly"></span><span id="_SECURITY_PUBLIC_KEY_ENCRYPTION_GLY"></span>**public key encryption**</span></span>
</dt> <dd>

<span data-ttu-id="a13ff-247">Eine Verschlüsselung mit Schlüsselpaaren: Mit einem Schlüssel werden die Daten verschlüsselt, mit dem anderen entschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="a13ff-247">Encryption that uses a pair of keys, one key to encrypt data and the other key to decrypt data.</span></span> <span data-ttu-id="a13ff-248">Bei symmetrischen Verschlüsselungsalgorithmen wird hingegen der gleiche Schlüssel sowohl zur Verschlüsselung als auch zur Entschlüsselung verwendet.</span><span class="sxs-lookup"><span data-stu-id="a13ff-248">In contrast, symmetric encryption algorithms that use the same key for both encryption and decryption.</span></span> <span data-ttu-id="a13ff-249">In der Praxis wird die Kryptografie mit öffentlichem Schlüssel in der Regel verwendet, um den Sitzungsschlüssel zu schützen, der von einem symmetrischen Verschlüsselungsalgorithmus verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a13ff-249">In practice, public key cryptography is typically used to protect the session key used by a symmetric encryption algorithm.</span></span> <span data-ttu-id="a13ff-250">In diesem Fall wird der Sitzungsschlüssel, mit dem Daten verschlüsselt wurden, mit dem öffentlichen Schlüssel verschlüsselt, und der private Schlüssel wird zum Entschlüsseln der Daten verwendet.</span><span class="sxs-lookup"><span data-stu-id="a13ff-250">In this case, the public key is used to encrypt the session key, which in turn was used to encrypt some data, and the private key is used for decryption.</span></span> <span data-ttu-id="a13ff-251">Neben dem Schutz von Sitzungsschlüsseln kann die Verschlüsselung mit öffentlichem Schlüssel noch zum digitalen Signieren von Nachrichten (mit dem privaten Schlüssel) sowie zum Überprüfen der Signatur (mit dem öffentlichen Schlüssel) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a13ff-251">In addition to protecting session keys, public key cryptography may also be used to digitally sign a message (using the private key) and validate the signature (using the public key).</span></span>

<span data-ttu-id="a13ff-252">Siehe auch *Algorithmus für öffentliche Schlüssel*.</span><span class="sxs-lookup"><span data-stu-id="a13ff-252">See also *public key algorithm*.</span></span>

</dd> </dl>

 

 



