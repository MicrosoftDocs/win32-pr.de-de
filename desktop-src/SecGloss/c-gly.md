---
description: Enthält Definitionen von Sicherheits Begriffen, die mit dem Buchstaben C beginnen.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: db46def4-bfdc-4801-a57d-d568e94a2dbb
title: C (Sicherheits Glossar)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 863422525326ec0a04a597d33a29553006bb014b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362590"
---
# <a name="c-security-glossary"></a><span data-ttu-id="44049-103">C (Sicherheits Glossar)</span><span class="sxs-lookup"><span data-stu-id="44049-103">C (Security Glossary)</span></span>

<span data-ttu-id="44049-104">[a](a-gly.md) [B](b-gly.md) C [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span><span class="sxs-lookup"><span data-stu-id="44049-104">[A](a-gly.md) [B](b-gly.md) C [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span></span>

<dl> <dt>

<span data-ttu-id="44049-105"><span id="_security_ca_gly"></span><span id="_SECURITY_CA_GLY"></span>**Etwa**</span><span class="sxs-lookup"><span data-stu-id="44049-105"><span id="_security_ca_gly"></span><span id="_SECURITY_CA_GLY"></span>**CA**</span></span>
</dt> <dd>

<span data-ttu-id="44049-106">Siehe *Zertifizierungs* Stelle.</span><span class="sxs-lookup"><span data-stu-id="44049-106">See *certification authority*.</span></span>

</dd> <dt>

<span data-ttu-id="44049-107"><span id="_security_ca_certificate_gly"></span><span id="_SECURITY_CA_CERTIFICATE_GLY"></span>**Zertifizierungsstellen Zertifikat**</span><span class="sxs-lookup"><span data-stu-id="44049-107"><span id="_security_ca_certificate_gly"></span><span id="_SECURITY_CA_CERTIFICATE_GLY"></span>**CA certificate**</span></span>
</dt> <dd>

<span data-ttu-id="44049-108">Identifiziert die Zertifizierungsstelle (Certification Authority, ca), die Server-und Client Authentifizierungs Zertifikate für die Server und Clients ausgibt, von denen diese Zertifikate angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="44049-108">Identifies the certification authority (CA) that issues server and client authentication certificates to the servers and clients that request these certificates.</span></span> <span data-ttu-id="44049-109">Da das Zertifizierungsstellenzertifikat auch einen öffentlichen Schlüssel enthält, der in digitalen Signaturen verwendet wird, wird es auch als Signaturzertifikat bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="44049-109">Because it contains a public key used in digital signatures, it is also referred to as a signature certificate.</span></span> <span data-ttu-id="44049-110">Wenn es sich um eine Stammzertifizierungsstelle handelt, wird das Zertifizierungsstellenzertifikat auch als Stammzertifikat bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="44049-110">If the CA is a root authority, the CA certificate may be referred to as a root certificate.</span></span> <span data-ttu-id="44049-111">Gelegentlich ist in diesem Zusammenhang auch die Rede von einem Sitezertifikat.</span><span class="sxs-lookup"><span data-stu-id="44049-111">Also sometimes known as a site certificate.</span></span>

</dd> <dt>

<span data-ttu-id="44049-112"><span id="_security_ca_hierarchy_gly"></span><span id="_SECURITY_CA_HIERARCHY_GLY"></span>**Zertifizierungsstellen Hierarchie**</span><span class="sxs-lookup"><span data-stu-id="44049-112"><span id="_security_ca_hierarchy_gly"></span><span id="_SECURITY_CA_HIERARCHY_GLY"></span>**CA hierarchy**</span></span>
</dt> <dd>

<span data-ttu-id="44049-113">Eine Zertifizierungsstellen Hierarchie (ca) enthält mehrere Zertifizierungsstellen.</span><span class="sxs-lookup"><span data-stu-id="44049-113">A certification authority (CA) hierarchy contains multiple CAs.</span></span> <span data-ttu-id="44049-114">Es ist so organisiert, dass jede Zertifizierungsstelle von einer anderen Zertifizierungsstelle auf einer höheren Ebene der Hierarchie zertifiziert wird, bis der obere Teil der Hierarchie, auch bekannt als Stamm Zertifizierungsstelle, erreicht wird.</span><span class="sxs-lookup"><span data-stu-id="44049-114">It is organized such that each CA is certified by another CA in a higher level of the hierarchy until the top of the hierarchy, also known as the root authority, is reached.</span></span>

</dd> <dt>

<span data-ttu-id="44049-115"><span id="_security_calg_dh_ephem_gly"></span><span id="_SECURITY_CALG_DH_EPHEM_GLY"></span>**calg \_ dh- \_ ephem**</span><span class="sxs-lookup"><span data-stu-id="44049-115"><span id="_security_calg_dh_ephem_gly"></span><span id="_SECURITY_CALG_DH_EPHEM_GLY"></span>**CALG\_DH\_EPHEM**</span></span>
</dt> <dd>

<span data-ttu-id="44049-116">Der CryptoAPI-Algorithmusbezeichner für den Diffie-Hellman Schlüsselaustausch Algorithmus, wenn er für die Generierung von kurzlebigen Schlüsseln verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="44049-116">The CryptoAPI algorithm identifier for the Diffie-Hellman key-exchange algorithm when used for the generation of ephemeral keys.</span></span>

<span data-ttu-id="44049-117">Siehe auch [*Diffie-Hellman (kurzlebige) Schlüsselaustausch Algorithmus*](d-gly.md).</span><span class="sxs-lookup"><span data-stu-id="44049-117">See also [*Diffie-Hellman (ephemeral) key-exchange algorithm*](d-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="44049-118"><span id="_security_calg_dh_sf_gly"></span><span id="_SECURITY_CALG_DH_SF_GLY"></span>**"calg \_ dh \_ SF"**</span><span class="sxs-lookup"><span data-stu-id="44049-118"><span id="_security_calg_dh_sf_gly"></span><span id="_SECURITY_CALG_DH_SF_GLY"></span>**CALG\_DH\_SF**</span></span>
</dt> <dd>

<span data-ttu-id="44049-119">Der CryptoAPI-Algorithmusbezeichner für den Diffie-Hellman Schlüsselaustausch Algorithmus, wenn er für die Generierung von Speicher-und vorwärts Schlüsseln verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="44049-119">The CryptoAPI algorithm identifier for the Diffie-Hellman key-exchange algorithm when used for the generation of store-and-forward keys.</span></span>

<span data-ttu-id="44049-120">Siehe auch [*Diffie-Hellman-Schlüsselaustausch Algorithmus (speichern und Weiterleiten)*](d-gly.md).</span><span class="sxs-lookup"><span data-stu-id="44049-120">See also [*Diffie-Hellman (store and forward) key-exchange algorithm*](d-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="44049-121"><span id="_security_calg_hmac_gly"></span><span id="_SECURITY_CALG_HMAC_GLY"></span>**HMAC (calg) \_**</span><span class="sxs-lookup"><span data-stu-id="44049-121"><span id="_security_calg_hmac_gly"></span><span id="_SECURITY_CALG_HMAC_GLY"></span>**CALG\_HMAC**</span></span>
</dt> <dd>

<span data-ttu-id="44049-122">Der CryptoAPI-Algorithmusbezeichner für den Hash basierten Nachrichtenauthentifizierungscode-Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="44049-122">The CryptoAPI algorithm identifier for the hash-based Message Authentication Code algorithm.</span></span>

<span data-ttu-id="44049-123">Siehe auch [*Hash basiertes Nachrichtenauthentifizierungscode*](h-gly.md).</span><span class="sxs-lookup"><span data-stu-id="44049-123">See also [*Hash-Based Message Authentication Code*](h-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="44049-124"><span id="_security_calg_mac_gly"></span><span id="_SECURITY_CALG_MAC_GLY"></span>**calg- \_ Mac**</span><span class="sxs-lookup"><span data-stu-id="44049-124"><span id="_security_calg_mac_gly"></span><span id="_SECURITY_CALG_MAC_GLY"></span>**CALG\_MAC**</span></span>
</dt> <dd>

<span data-ttu-id="44049-125">Der CryptoAPI-Algorithmusbezeichner für den Nachrichtenauthentifizierungscode-Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="44049-125">The CryptoAPI algorithm identifier for the Message Authentication Code algorithm.</span></span>

<span data-ttu-id="44049-126">Siehe auch [*Nachrichtenauthentifizierungscode*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="44049-126">See also [*Message Authentication Code*](m-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="44049-127"><span id="_security_calg_md2_gly"></span><span id="_SECURITY_CALG_MD2_GLY"></span>**Calg \_ MD2**</span><span class="sxs-lookup"><span data-stu-id="44049-127"><span id="_security_calg_md2_gly"></span><span id="_SECURITY_CALG_MD2_GLY"></span>**CALG\_MD2**</span></span>
</dt> <dd>

<span data-ttu-id="44049-128">Der CryptoAPI-Algorithmusbezeichner für den MD2-Hash Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="44049-128">The CryptoAPI algorithm identifier for the MD2 hash algorithm.</span></span>

<span data-ttu-id="44049-129">Siehe auch [*MD2-Algorithmus*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="44049-129">See also [*MD2 algorithm*](m-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="44049-130"><span id="_security_calg_md5_gly"></span><span id="_SECURITY_CALG_MD5_GLY"></span>**Calg \_ MD5**</span><span class="sxs-lookup"><span data-stu-id="44049-130"><span id="_security_calg_md5_gly"></span><span id="_SECURITY_CALG_MD5_GLY"></span>**CALG\_MD5**</span></span>
</dt> <dd>

<span data-ttu-id="44049-131">Der CryptoAPI-Algorithmusbezeichner für den MD5-Hash Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="44049-131">The CryptoAPI algorithm identifier for the MD5 hash algorithm.</span></span>

<span data-ttu-id="44049-132">Siehe auch [*MD5-Algorithmus*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="44049-132">See also [*MD5 algorithm*](m-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="44049-133"><span id="_security_calg_rc2_gly"></span><span id="_SECURITY_CALG_RC2_GLY"></span>**Calg \_ RC2**</span><span class="sxs-lookup"><span data-stu-id="44049-133"><span id="_security_calg_rc2_gly"></span><span id="_SECURITY_CALG_RC2_GLY"></span>**CALG\_RC2**</span></span>
</dt> <dd>

<span data-ttu-id="44049-134">Der kryptografiealgorithmusbezeichner für den RC2-Blockchiffre Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="44049-134">The CryptoAPI algorithm identifier for the RC2 block cipher algorithm.</span></span>

<span data-ttu-id="44049-135">Siehe auch [*RC2-Block Algorithmus*](r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="44049-135">See also [*RC2 block algorithm*](r-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="44049-136"><span id="_security_calg_rc4_gly"></span><span id="_SECURITY_CALG_RC4_GLY"></span>**Calg \_ RC4**</span><span class="sxs-lookup"><span data-stu-id="44049-136"><span id="_security_calg_rc4_gly"></span><span id="_SECURITY_CALG_RC4_GLY"></span>**CALG\_RC4**</span></span>
</dt> <dd>

<span data-ttu-id="44049-137">Der kryptografiealgorithmusbezeichner für den RC4-streamchiffre Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="44049-137">The CryptoAPI algorithm identifier for the RC4 stream cipher algorithm.</span></span>

<span data-ttu-id="44049-138">Siehe auch [*RC4-streamalgorithmus*](r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="44049-138">See also [*RC4 stream algorithm*](r-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="44049-139"><span id="_security_calg_rsa_keyx_gly"></span><span id="_SECURITY_CALG_RSA_KEYX_GLY"></span>**calg \_ RSA \_ Keyx**</span><span class="sxs-lookup"><span data-stu-id="44049-139"><span id="_security_calg_rsa_keyx_gly"></span><span id="_SECURITY_CALG_RSA_KEYX_GLY"></span>**CALG\_RSA\_KEYX**</span></span>
</dt> <dd>

<span data-ttu-id="44049-140">Der CryptoAPI-Algorithmusbezeichner für den RSA-Algorithmus für öffentliche Schlüssel bei Verwendung für den Schlüsselaustausch.</span><span class="sxs-lookup"><span data-stu-id="44049-140">The CryptoAPI algorithm identifier for the RSA public key algorithm when used for key exchange.</span></span>

<span data-ttu-id="44049-141">Siehe auch [*RSA-Algorithmus für öffentliche Schlüssel*](r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="44049-141">See also [*RSA public key algorithm*](r-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="44049-142"><span id="_security_calg_rsa_sign_gly"></span><span id="_SECURITY_CALG_RSA_SIGN_GLY"></span>**calg- \_ RSA- \_ Zeichen**</span><span class="sxs-lookup"><span data-stu-id="44049-142"><span id="_security_calg_rsa_sign_gly"></span><span id="_SECURITY_CALG_RSA_SIGN_GLY"></span>**CALG\_RSA\_SIGN**</span></span>
</dt> <dd>

<span data-ttu-id="44049-143">Der CryptoAPI-Algorithmusbezeichner für den RSA-Algorithmus für öffentliche Schlüssel, wenn er zum Generieren digitaler Signaturen verwendet wird</span><span class="sxs-lookup"><span data-stu-id="44049-143">The CryptoAPI algorithm identifier for the RSA public key algorithm when used to generate digital signatures.</span></span>

<span data-ttu-id="44049-144">Siehe auch [*RSA-Algorithmus für öffentliche Schlüssel*](r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="44049-144">See also [*RSA public key algorithm*](r-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="44049-145"><span id="_security_calg_sha_gly"></span><span id="_SECURITY_CALG_SHA_GLY"></span>**calg \_ SHA**</span><span class="sxs-lookup"><span data-stu-id="44049-145"><span id="_security_calg_sha_gly"></span><span id="_SECURITY_CALG_SHA_GLY"></span>**CALG\_SHA**</span></span>
</dt> <dd>

<span data-ttu-id="44049-146">Der CryptoAPI-Algorithmusbezeichner für den Secure-Hash-Algorithmus (SHA-1).</span><span class="sxs-lookup"><span data-stu-id="44049-146">The CryptoAPI algorithm identifier for the Secure Hash Algorithm (SHA-1).</span></span>

<span data-ttu-id="44049-147">Siehe auch [*Secure Hash-Algorithmus*](s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="44049-147">See also [*Secure Hash Algorithm*](s-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="44049-148"><span id="_security_cast_gly"></span><span id="_SECURITY_CAST_GLY"></span>**Darsteller**</span><span class="sxs-lookup"><span data-stu-id="44049-148"><span id="_security_cast_gly"></span><span id="_SECURITY_CAST_GLY"></span>**CAST**</span></span>
</dt> <dd>

<span data-ttu-id="44049-149">Eine Gruppe von des-ähnlichen symmetrischen Blockchiffren, die von C. M entwickelt wurden.</span><span class="sxs-lookup"><span data-stu-id="44049-149">A group of DES-like symmetric block ciphers developed by C. M.</span></span> <span data-ttu-id="44049-150">Adams und S. E.</span><span class="sxs-lookup"><span data-stu-id="44049-150">Adams and S. E.</span></span> <span data-ttu-id="44049-151">Tavares.</span><span class="sxs-lookup"><span data-stu-id="44049-151">Tavares.</span></span> <span data-ttu-id="44049-152">Prov \_ MS \_ Exchange-Anbieter Typen geben einen bestimmten Umwandlungs Algorithmus an, der eine 64-Bit-Blockgröße verwendet.</span><span class="sxs-lookup"><span data-stu-id="44049-152">PROV\_MS\_EXCHANGE provider types specify a particular CAST algorithm that uses a 64-bit block size.</span></span>

</dd> <dt>

<span data-ttu-id="44049-153"><span id="_security_cbc_gly"></span><span id="_SECURITY_CBC_GLY"></span>**CBC**</span><span class="sxs-lookup"><span data-stu-id="44049-153"><span id="_security_cbc_gly"></span><span id="_SECURITY_CBC_GLY"></span>**CBC**</span></span>
</dt> <dd>

<span data-ttu-id="44049-154">Siehe *Cipher Block Chaining*.</span><span class="sxs-lookup"><span data-stu-id="44049-154">See *Cipher Block Chaining*.</span></span>

</dd> <dt>

<span data-ttu-id="44049-155"><span id="_security_certificate_gly"></span><span id="_SECURITY_CERTIFICATE_GLY"></span>**stellt**</span><span class="sxs-lookup"><span data-stu-id="44049-155"><span id="_security_certificate_gly"></span><span id="_SECURITY_CERTIFICATE_GLY"></span>**certificate**</span></span>
</dt> <dd>

<span data-ttu-id="44049-156">Eine digital signierte Anweisung mit Informationen über eine Entität und ihren öffentlichen Schlüssel, die zwei Informationen verbindet.</span><span class="sxs-lookup"><span data-stu-id="44049-156">A digitally signed statement that contains information about an entity and the entity's public key, thus binding these two pieces of information together.</span></span> <span data-ttu-id="44049-157">Ein Zertifikat wird von einer vertrauenswürdigen Organisation (oder Entität) ausgestellt, die als Zertifizierungsstelle ( *Certification Authority* , ca) bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="44049-157">A certificate is issued by a trusted organization (or entity) called a *certification authority* (CA) after the CA has verified that the entity is who it says it is.</span></span>

<span data-ttu-id="44049-158">Zertifikate können verschiedene Datentypen enthalten.</span><span class="sxs-lookup"><span data-stu-id="44049-158">Certificates can contain different types of data.</span></span> <span data-ttu-id="44049-159">Beispielsweise enthält ein X.509-Zertifikat folgende Zertifikatdaten: Format, Seriennummer, Algorithmus der Signatur, Name der ausstellenden Zertifizierungsstelle, Name und öffentlicher Schlüssel der Entität, die das Zertifikat anfordert, sowie Signatur der Zertifizierungsstelle.</span><span class="sxs-lookup"><span data-stu-id="44049-159">For example, an X.509 certificate includes the format of the certificate, the serial number of the certificate, the algorithm used to sign the certificate, the name of the CA that issued the certificate, the name and public key of the entity requesting the certificate, and the CA's signature.</span></span>

</dd> <dt>

<span data-ttu-id="44049-160"><span id="_security_certificate_blob_gly"></span><span id="_SECURITY_CERTIFICATE_BLOB_GLY"></span>**zertifikatblob**</span><span class="sxs-lookup"><span data-stu-id="44049-160"><span id="_security_certificate_blob_gly"></span><span id="_SECURITY_CERTIFICATE_BLOB_GLY"></span>**certificate BLOB**</span></span>
</dt> <dd>

<span data-ttu-id="44049-161">Ein BLOB, das die Zertifikatsdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="44049-161">A BLOB that contains the certificate data.</span></span>

<span data-ttu-id="44049-162">Ein zertifikatblob wird durch Aufrufe von " **cryptencodeobject**" erstellt.</span><span class="sxs-lookup"><span data-stu-id="44049-162">A certificate BLOB is created by calls to **CryptEncodeObject**.</span></span> <span data-ttu-id="44049-163">Der Prozess ist vollständig, wenn die Ausgabe des Aufrufes alle Zertifikatsdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="44049-163">The process is complete when the output of the call contains all the certificate data.</span></span>

</dd> <dt>

<span data-ttu-id="44049-164"><span id="_security_certificate_context_gly"></span><span id="_SECURITY_CERTIFICATE_CONTEXT_GLY"></span>**Zertifikat Kontext**</span><span class="sxs-lookup"><span data-stu-id="44049-164"><span id="_security_certificate_context_gly"></span><span id="_SECURITY_CERTIFICATE_CONTEXT_GLY"></span>**certificate context**</span></span>
</dt> <dd>

<span data-ttu-id="44049-165">Eine CERT- \_ Kontext Struktur, die ein Handle für einen Zertifikat Speicher, einen Zeiger auf das ursprünglich codierte zertifikatblob, einen Zeiger auf eine CERT \_ Info-Struktur und einen Codierungstyp Member enthält.</span><span class="sxs-lookup"><span data-stu-id="44049-165">A CERT\_CONTEXT structure that contains a handle to a certificate store, a pointer to the original encoded certificate BLOB, a pointer to a CERT\_INFO structure, and an encoding type member.</span></span> <span data-ttu-id="44049-166">Dabei handelt es sich um die **CERT \_ Info** -Struktur, die den größten Teil der Zertifikat Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="44049-166">It is the **CERT\_INFO** structure that contains most of the certificate information.</span></span>

</dd> <dt>

<span data-ttu-id="44049-167"><span id="_security_certificate_encode_decode_functions_gly"></span><span id="_SECURITY_CERTIFICATE_ENCODE_DECODE_FUNCTIONS_GLY"></span>**zertifikatcodieren/Decodieren von Funktionen**</span><span class="sxs-lookup"><span data-stu-id="44049-167"><span id="_security_certificate_encode_decode_functions_gly"></span><span id="_SECURITY_CERTIFICATE_ENCODE_DECODE_FUNCTIONS_GLY"></span>**certificate encode/decode functions**</span></span>
</dt> <dd>

<span data-ttu-id="44049-168">Funktionen, die die Übersetzung von Zertifikaten und verknüpften Materialien in standardmäßige Binär Formate verwalten, die in verschiedenen Umgebungen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="44049-168">Functions that manage the translation of certificates and related material into standard, binary formats that can be used in different environments.</span></span>

</dd> <dt>

<span data-ttu-id="44049-169"><span id="_security_certificate_encoding_type_gly"></span><span id="_SECURITY_CERTIFICATE_ENCODING_TYPE_GLY"></span>**zertifikatcodierungstyp**</span><span class="sxs-lookup"><span data-stu-id="44049-169"><span id="_security_certificate_encoding_type_gly"></span><span id="_SECURITY_CERTIFICATE_ENCODING_TYPE_GLY"></span>**certificate encoding type**</span></span>
</dt> <dd>

<span data-ttu-id="44049-170">Definiert, wie das Zertifikat codiert wird.</span><span class="sxs-lookup"><span data-stu-id="44049-170">Defines how the certificate is encoded.</span></span> <span data-ttu-id="44049-171">Der zertifikatcodierungstyp wird in dem nieder wertigen Wort der **DWORD**-Struktur (Encoding Type) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="44049-171">The certificate encoding type is stored in the low-order word of the encoding type (**DWORD**) structure.</span></span>

</dd> <dt>

<span data-ttu-id="44049-172"><span id="_security_certificate_management_over_cms_gly"></span><span id="_SECURITY_CERTIFICATE_MANAGEMENT_OVER_CMS_GLY"></span>**Zertifikat Verwaltung über CMS**</span><span class="sxs-lookup"><span data-stu-id="44049-172"><span id="_security_certificate_management_over_cms_gly"></span><span id="_SECURITY_CERTIFICATE_MANAGEMENT_OVER_CMS_GLY"></span>**Certificate Management over CMS**</span></span>
</dt> <dd>

<span data-ttu-id="44049-173">Markets.</span><span class="sxs-lookup"><span data-stu-id="44049-173">CMC.</span></span> <span data-ttu-id="44049-174">Zertifikat Verwaltung über CMS.</span><span class="sxs-lookup"><span data-stu-id="44049-174">Certificate Management over CMS.</span></span> <span data-ttu-id="44049-175">Bei CMC handelt es sich um ein Zertifikat Verwaltungs Protokoll, das Cryptographic Message Syntax (CMS) verwendet.</span><span class="sxs-lookup"><span data-stu-id="44049-175">CMC is a certificate management protocol that uses Cryptographic Message Syntax (CMS).</span></span> <span data-ttu-id="44049-176">Vor dem Senden der Anforderung an einen Registrierungs Server umschließt Microsoft die Anforderung von SMTP-Zertifikaten in ein Objekt vom Typ [*PKCS \# 7*](p-gly.md) (CMS).</span><span class="sxs-lookup"><span data-stu-id="44049-176">Microsoft wraps CMC certificate requests in a [*PKCS \#7*](p-gly.md) (CMS) request object before sending the request to an enrollment server.</span></span>

</dd> <dt>

<span data-ttu-id="44049-177"><span id="_security_certificate_name_blob_gly"></span><span id="_SECURITY_CERTIFICATE_NAME_BLOB_GLY"></span>**zertifikatnamensblob**</span><span class="sxs-lookup"><span data-stu-id="44049-177"><span id="_security_certificate_name_blob_gly"></span><span id="_SECURITY_CERTIFICATE_NAME_BLOB_GLY"></span>**certificate name BLOB**</span></span>
</dt> <dd>

<span data-ttu-id="44049-178">Eine codierte Darstellung der Namensinformationen, die in Zertifikaten enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="44049-178">An encoded representation of the name information that is included in certificates.</span></span> <span data-ttu-id="44049-179">Jedes BLOB des Namens wird einer **Zertifikat \_ Namen- \_ blobstruktur** zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="44049-179">Each name BLOB is mapped to a **CERT\_NAME\_BLOB** structure.</span></span>

<span data-ttu-id="44049-180">Beispielsweise werden der Aussteller und die Antragsteller Informationen, auf die von einer **CERT \_ Info** -Struktur verwiesen wird, in zwei **CERT \_ Name- \_ BLOB** -Strukturen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="44049-180">For example, the issuer and subject information referenced by a **CERT\_INFO** structure is stored in two **CERT\_NAME\_BLOB** structures.</span></span>

</dd> <dt>

<span data-ttu-id="44049-181"><span id="_security_certificate_policy_gly"></span><span id="_SECURITY_CERTIFICATE_POLICY_GLY"></span>**Zertifikat Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="44049-181"><span id="_security_certificate_policy_gly"></span><span id="_SECURITY_CERTIFICATE_POLICY_GLY"></span>**certificate policy**</span></span>
</dt> <dd>

<span data-ttu-id="44049-182">Ein benannter Satz von Regeln, die die Anwendbarkeit von Zertifikaten für eine bestimmte Anwendungsklasse mit allgemeinen Sicherheitsanforderungen angeben.</span><span class="sxs-lookup"><span data-stu-id="44049-182">A named set of rules that indicate the applicability of certificates for a specific class of applications with common security requirements.</span></span> <span data-ttu-id="44049-183">Eine solche Richtlinie kann z. b. bestimmte Zertifikate auf elektronische Datenaustausch Transaktionen innerhalb der vorgegebenen Preislimits beschränken.</span><span class="sxs-lookup"><span data-stu-id="44049-183">Such a policy might, for example, limit certain certificates to electronic data interchange transactions within given price limits.</span></span>

</dd> <dt>

<span data-ttu-id="44049-184"><span id="_security_certificate_request_gly"></span><span id="_SECURITY_CERTIFICATE_REQUEST_GLY"></span>**Zertifikat Anforderung**</span><span class="sxs-lookup"><span data-stu-id="44049-184"><span id="_security_certificate_request_gly"></span><span id="_SECURITY_CERTIFICATE_REQUEST_GLY"></span>**certificate request**</span></span>
</dt> <dd>

<span data-ttu-id="44049-185">Eine speziell formatierte elektronische Nachricht (die an eine Zertifizierungsstelle gesendet wird), die zum Anfordern eines Zertifikats verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="44049-185">A specially formatted electronic message (sent to a CA) used to request a certificate.</span></span> <span data-ttu-id="44049-186">Die Anforderung muss die Informationen enthalten, die von der Zertifizierungsstelle zum Authentifizieren der Anforderung benötigt werden, sowie den öffentlichen Schlüssel der Entität, die das Zertifikat anfordert.</span><span class="sxs-lookup"><span data-stu-id="44049-186">The request must contain the information required by the CA to authenticate the request, plus the public key of the entity requesting the certificate.</span></span>

<span data-ttu-id="44049-187">Alle Informationen, die zum Erstellen der Anforderung erforderlich sind, werden **einer \_ Zertifikat \_ Anforderungs** Informationsstruktur zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="44049-187">All the information necessary to create the request is mapped to a **CERT\_REQUEST\_INFO** structure.</span></span>

</dd> <dt>

<span data-ttu-id="44049-188"><span id="_security_certificate_revocation_list_gly"></span><span id="_SECURITY_CERTIFICATE_REVOCATION_LIST_GLY"></span>**Zertifikat Sperr Liste**</span><span class="sxs-lookup"><span data-stu-id="44049-188"><span id="_security_certificate_revocation_list_gly"></span><span id="_SECURITY_CERTIFICATE_REVOCATION_LIST_GLY"></span>**certificate revocation list**</span></span>
</dt> <dd>

<span data-ttu-id="44049-189">CRL Ein Dokument, das von einer Zertifizierungsstelle (Certification Authority, ca) verwaltet und veröffentlicht wird und die von der Zertifizierungsstelle ausgestellten Zertifikate auflistet, die nicht mehr gültig sind</span><span class="sxs-lookup"><span data-stu-id="44049-189">(CRL) A document maintained and published by a certification authority (CA) that lists certificates issued by the CA that are no longer valid.</span></span>

</dd> <dt>

<span data-ttu-id="44049-190"><span id="_security_certificate_server_gly"></span><span id="_SECURITY_CERTIFICATE_SERVER_GLY"></span>**Zertifikat Server**</span><span class="sxs-lookup"><span data-stu-id="44049-190"><span id="_security_certificate_server_gly"></span><span id="_SECURITY_CERTIFICATE_SERVER_GLY"></span>**certificate server**</span></span>
</dt> <dd>

<span data-ttu-id="44049-191">Ein Server, der Zertifikate für eine bestimmte Zertifizierungsstelle ausgibt.</span><span class="sxs-lookup"><span data-stu-id="44049-191">A server that issues certificates for a particular CA.</span></span> <span data-ttu-id="44049-192">Die Zertifikat Server Software bietet anpassbare Dienste zum Ausstellen und Verwalten von Zertifikaten, die in Sicherheitssystemen verwendet werden, die Kryptografie mit öffentlichem Schlüssel verwenden.</span><span class="sxs-lookup"><span data-stu-id="44049-192">The certificate server software provides customizable services for issuing and managing certificates used in security systems that employ public key cryptography.</span></span>

</dd> <dt>

<span data-ttu-id="44049-193"><span id="_security_certificate_services_gly"></span><span id="_SECURITY_CERTIFICATE_SERVICES_GLY"></span>**Zertifikat Dienste**</span><span class="sxs-lookup"><span data-stu-id="44049-193"><span id="_security_certificate_services_gly"></span><span id="_SECURITY_CERTIFICATE_SERVICES_GLY"></span>**Certificate Services**</span></span>
</dt> <dd>

<span data-ttu-id="44049-194">Ein Software Dienst, der Zertifikate für eine bestimmte *Zertifizierungs* Stelle ausgibt.</span><span class="sxs-lookup"><span data-stu-id="44049-194">A software service that issues certificates for a particular *certification authority* (CA).</span></span> <span data-ttu-id="44049-195">Es bietet anpassbare Dienste zum Ausstellen und Verwalten von Zertifikaten für das Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="44049-195">It provides customizable services for issuing and managing certificates for the enterprise.</span></span> <span data-ttu-id="44049-196">Zertifikate können verwendet werden, um Authentifizierungs Unterstützung bereitzustellen, einschließlich sicherer e-Mail, webbasierter Authentifizierung und Smartcard-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="44049-196">Certificates can be used to provide authentication support, including secure email, web-based authentication, and smart card authentication.</span></span>

</dd> <dt>

<span data-ttu-id="44049-197"><span id="_security_certificate_store_gly"></span><span id="_SECURITY_CERTIFICATE_STORE_GLY"></span>**Zertifikat Speicher**</span><span class="sxs-lookup"><span data-stu-id="44049-197"><span id="_security_certificate_store_gly"></span><span id="_SECURITY_CERTIFICATE_STORE_GLY"></span>**certificate store**</span></span>
</dt> <dd>

<span data-ttu-id="44049-198">Normalerweise handelt es sich um einen permanenten Speicher, in dem Zertifikate, Zertifikatsperrlisten (CRL) und Zertifikatvertrauenslisten (CTL) gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="44049-198">Typically, a permanent storage where certificates, certificate revocation lists (CRLs), and certificate trust lists (CTLs) are stored.</span></span> <span data-ttu-id="44049-199">Zertifikatspeicher können jedoch auch ausschließlich im Speicher erstellt und geöffnet werden, wenn Sie Zertifikate verwenden, die nicht im permanenten Speicher abgelegt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="44049-199">It is possible, however, to create and open a certificate store solely in memory when working with certificates that do not need to be put in permanent storage.</span></span>

<span data-ttu-id="44049-200">Der Zertifikat Speicher ist ein zentraler Bestandteil der Zertifikat Funktionalität in CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="44049-200">The certificate store is central to much of the certificate functionality in CryptoAPI.</span></span>

</dd> <dt>

<span data-ttu-id="44049-201"><span id="_security_certificate_store_functions_gly"></span><span id="_SECURITY_CERTIFICATE_STORE_FUNCTIONS_GLY"></span>**Zertifikat Speicherfunktionen**</span><span class="sxs-lookup"><span data-stu-id="44049-201"><span id="_security_certificate_store_functions_gly"></span><span id="_SECURITY_CERTIFICATE_STORE_FUNCTIONS_GLY"></span>**certificate store functions**</span></span>
</dt> <dd>

<span data-ttu-id="44049-202">Funktionen, die die Speicher-und Abruf Daten verwalten, wie z. b. Zertifikate, Zertifikat Sperr Listen (CRLs) und Zertifikat Vertrauens Listen (Certificate Trust Lists, CTLs).</span><span class="sxs-lookup"><span data-stu-id="44049-202">Functions that manage the storage and retrieval data such as certificates, certificate revocation lists (CRLs), and certificate trust lists (CTLs).</span></span> <span data-ttu-id="44049-203">Diese Funktionen können in allgemeine Zertifikat Funktionen, Funktionen für die Zertifikat Sperr Liste und Funktionen für Zertifikat Vertrauens Listen aufgeteilt werden.</span><span class="sxs-lookup"><span data-stu-id="44049-203">These functions can be separated into common certificate functions, certificate revocation list functions, and certificate trust list functions.</span></span>

</dd> <dt>

<span data-ttu-id="44049-204"><span id="_security_certificate_template_gly"></span><span id="_SECURITY_CERTIFICATE_TEMPLATE_GLY"></span>**Zertifikat Vorlage**</span><span class="sxs-lookup"><span data-stu-id="44049-204"><span id="_security_certificate_template_gly"></span><span id="_SECURITY_CERTIFICATE_TEMPLATE_GLY"></span>**certificate template**</span></span>
</dt> <dd>

<span data-ttu-id="44049-205">Ein Windows-Konstrukt, das Zertifikate erstellt (d. h., das Format und der Inhalt werden vorab angegeben), basierend auf der vorgesehenen Verwendung.</span><span class="sxs-lookup"><span data-stu-id="44049-205">A Windows construct that profiles certificates (that is, it prespecifies the format and content) based on their intended usage.</span></span> <span data-ttu-id="44049-206">Beim Anfordern eines [*Zertifikats*](/windows) von einer Windows-Unternehmens Zertifizierungsstelle ( *Certification Authority* , ca) werden Zertifikatanforderer je nach Zugriffsrechten in einer Vielzahl von Zertifikat Typen ausgewählt, die auf Zertifikat Vorlagen basieren, wie z. b. Benutzer-und Code Signatur.</span><span class="sxs-lookup"><span data-stu-id="44049-206">When requesting a [*certificate*](/windows) from a Windows enterprise *certification authority* (CA), certificate requesters are, depending on their access rights, able to select from a variety of certificate types that are based on certificate templates, such as User and Code Signing.</span></span>

</dd> <dt>

<span data-ttu-id="44049-207"><span id="_security_certificate_trust_list_gly"></span><span id="_SECURITY_CERTIFICATE_TRUST_LIST_GLY"></span>**Zertifikat Vertrauens Liste**</span><span class="sxs-lookup"><span data-stu-id="44049-207"><span id="_security_certificate_trust_list_gly"></span><span id="_SECURITY_CERTIFICATE_TRUST_LIST_GLY"></span>**certificate trust list**</span></span>
</dt> <dd>

<span data-ttu-id="44049-208">CTL Eine vordefinierte Liste von Elementen, die von einer vertrauenswürdigen Entität signiert wurden.</span><span class="sxs-lookup"><span data-stu-id="44049-208">(CTL) A predefined list of items that have been signed by a trusted entity.</span></span> <span data-ttu-id="44049-209">Eine Zertifikatvertrauensliste kann beispielsweise eine Hashliste mit Zertifikaten sein oder eine Liste mit Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="44049-209">A CTL can be anything, such as a list of hashes of certificates, or a list of file names.</span></span> <span data-ttu-id="44049-210">Alle Elemente in der Liste werden von der signierenden Entität authentifiziert (genehmigt).</span><span class="sxs-lookup"><span data-stu-id="44049-210">All the items in the list are authenticated (approved) by the signing entity.</span></span>

</dd> <dt>

<span data-ttu-id="44049-211"><span id="_security_certification_authority_gly"></span><span id="_SECURITY_CERTIFICATION_AUTHORITY_GLY"></span>**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="44049-211"><span id="_security_certification_authority_gly"></span><span id="_SECURITY_CERTIFICATION_AUTHORITY_GLY"></span>**certification authority**</span></span>
</dt> <dd>

<span data-ttu-id="44049-212">Etwa Eine Entität, mit der Zertifikate ausgestellt werden, die bestätigen, dass der Empfänger, der Computer oder die Organisation, der das Zertifikat anfordert, die Bedingungen einer festgelegten Richtlinie erfüllt.</span><span class="sxs-lookup"><span data-stu-id="44049-212">(CA) An entity entrusted to issue certificates that assert that the recipient individual, computer, or organization requesting the certificate fulfills the conditions of an established policy.</span></span>

</dd> <dt>

<span data-ttu-id="44049-213"><span id="_security_cfb_gly"></span><span id="_SECURITY_CFB_GLY"></span>**CFB**</span><span class="sxs-lookup"><span data-stu-id="44049-213"><span id="_security_cfb_gly"></span><span id="_SECURITY_CFB_GLY"></span>**CFB**</span></span>
</dt> <dd>

<span data-ttu-id="44049-214">Siehe *Chiffre Feedback*.</span><span class="sxs-lookup"><span data-stu-id="44049-214">See *Cipher Feedback*.</span></span>

</dd> <dt>

<span data-ttu-id="44049-215"><span id="_security_chaining_mode_gly"></span><span id="_SECURITY_CHAINING_MODE_GLY"></span>**Verkettungs Modus**</span><span class="sxs-lookup"><span data-stu-id="44049-215"><span id="_security_chaining_mode_gly"></span><span id="_SECURITY_CHAINING_MODE_GLY"></span>**chaining mode**</span></span>
</dt> <dd>

<span data-ttu-id="44049-216">Ein Blockchiffre Modus, der Feedback durch Kombinieren von verschlüsseltem Text und Klartext einführt.</span><span class="sxs-lookup"><span data-stu-id="44049-216">A block cipher mode that introduces feedback by combining ciphertext and plaintext.</span></span>

<span data-ttu-id="44049-217">Siehe auch Verschlüsselungs *Block Verkettung*.</span><span class="sxs-lookup"><span data-stu-id="44049-217">See also *Cipher Block Chaining*.</span></span>

</dd> <dt>

<span data-ttu-id="44049-218"><span id="_security_cipher_gly"></span><span id="_SECURITY_CIPHER_GLY"></span>**Verschlüsselungs**</span><span class="sxs-lookup"><span data-stu-id="44049-218"><span id="_security_cipher_gly"></span><span id="_SECURITY_CIPHER_GLY"></span>**cipher**</span></span>
</dt> <dd>

<span data-ttu-id="44049-219">Ein kryptografischer Algorithmus, der zum Verschlüsseln von Daten verwendet wird. Das heißt, um Klartext mithilfe eines vordefinierten Schlüssels in Chiffre Text umzuwandeln.</span><span class="sxs-lookup"><span data-stu-id="44049-219">A cryptographic algorithm used to encrypt data; that is, to transform plaintext into ciphertext using a predefined key.</span></span>

</dd> <dt>

<span data-ttu-id="44049-220"><span id="_security_cipher_block_chaining_gly"></span><span id="_SECURITY_CIPHER_BLOCK_CHAINING_GLY"></span>**Chiffre Block Verkettung**</span><span class="sxs-lookup"><span data-stu-id="44049-220"><span id="_security_cipher_block_chaining_gly"></span><span id="_SECURITY_CIPHER_BLOCK_CHAINING_GLY"></span>**Cipher Block Chaining**</span></span>
</dt> <dd>

<span data-ttu-id="44049-221">CBC Eine Methode zum Betreiben eines symmetrischen Blockchiffre, der Feedback verwendet, um zuvor generierten Chiffre Text mit neuem Klartext zu kombinieren.</span><span class="sxs-lookup"><span data-stu-id="44049-221">(CBC) A method of operating a symmetric block cipher that uses feedback to combine previously generated ciphertext with new plaintext.</span></span>

<span data-ttu-id="44049-222">Jeder Klartext-Block wird mit dem Chiffre Text des vorherigen Blocks durch eine bitweise **Xor** -Operation kombiniert, bevor er verschlüsselt wird.</span><span class="sxs-lookup"><span data-stu-id="44049-222">Each plaintext block is combined with the ciphertext of the previous block by a bitwise-**XOR** operation before it is encrypted.</span></span> <span data-ttu-id="44049-223">Durch die Kombination von "Chiffre Text" und "nur" wird sichergestellt, dass die Verschlüsselung in einem anderen Chiffre Text Block erfolgt, selbst wenn der Klartext viele identische Blöcke enthält.</span><span class="sxs-lookup"><span data-stu-id="44049-223">Combining ciphertext and plaintext ensures that even if the plaintext contains many identical blocks, they will each encrypt to a different ciphertext block.</span></span>

<span data-ttu-id="44049-224">Wenn der Microsoft-Basis Kryptografieanbieter verwendet wird, ist CBC der Standard Verschlüsselungs Modus.</span><span class="sxs-lookup"><span data-stu-id="44049-224">When the Microsoft Base Cryptographic Provider is used, CBC is the default cipher mode.</span></span>

</dd> <dt>

<span data-ttu-id="44049-225"><span id="_security_cipher_block_chaining_mac_gly"></span><span id="_SECURITY_CIPHER_BLOCK_CHAINING_MAC_GLY"></span>**Verschlüsselungs Block Verkettung von Mac**</span><span class="sxs-lookup"><span data-stu-id="44049-225"><span id="_security_cipher_block_chaining_mac_gly"></span><span id="_SECURITY_CIPHER_BLOCK_CHAINING_MAC_GLY"></span>**Cipher Block Chaining MAC**</span></span>
</dt> <dd>

<span data-ttu-id="44049-226">Eine Blockchiffre Methode, die die Basisdaten mit einer Blockchiffre verschlüsselt und dann den letzten verschlüsselten Block als Hashwert verwendet.</span><span class="sxs-lookup"><span data-stu-id="44049-226">A block cipher method that encrypts the base data with a block cipher and then uses the last encrypted block as the hash value.</span></span> <span data-ttu-id="44049-227">Der Verschlüsselungsalgorithmus, der verwendet wird, um den [*Nachrichtenauthentifizierungscode*](m-gly.md) (Mac) zu erstellen, ist der Verschlüsselungsalgorithmus, der beim Erstellen des Sitzungsschlüssels angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="44049-227">The encryption algorithm used to build the [*Message Authentication Code*](m-gly.md) (MAC) is the one that was specified when the session key was created.</span></span>

</dd> <dt>

<span data-ttu-id="44049-228"><span id="_security_cipher_feedback_gly"></span><span id="_SECURITY_CIPHER_FEEDBACK_GLY"></span>**Chiffre Feedback**</span><span class="sxs-lookup"><span data-stu-id="44049-228"><span id="_security_cipher_feedback_gly"></span><span id="_SECURITY_CIPHER_FEEDBACK_GLY"></span>**Cipher Feedback**</span></span>
</dt> <dd>

<span data-ttu-id="44049-229">CFB Ein Blockchiffre Modus, der kleine Inkremente von Klartext in Chiffre Text verarbeitet, anstatt einen gesamten Block gleichzeitig zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="44049-229">(CFB) A block cipher mode that processes small increments of plaintext into ciphertext, instead of processing an entire block at a time.</span></span>

<span data-ttu-id="44049-230">In diesem Modus wird ein UMSCHALT Register verwendet, das eine Länge von Blöcken hat und in Abschnitte aufgeteilt ist.</span><span class="sxs-lookup"><span data-stu-id="44049-230">This mode uses a shift register that is one block size in length and divided into sections.</span></span> <span data-ttu-id="44049-231">Wenn die Blockgröße z. b. 64 Bits beträgt, bei der acht Bits gleichzeitig verarbeitet werden, dann ist das UMSCHALT Register in acht Abschnitte unterteilt.</span><span class="sxs-lookup"><span data-stu-id="44049-231">For example, if the block size is 64 bits with eight bits processed at a time, then the shift register would be divided into eight sections.</span></span>

</dd> <dt>

<span data-ttu-id="44049-232"><span id="_security_cipher_mode_gly"></span><span id="_SECURITY_CIPHER_MODE_GLY"></span>**Chiffre Modus**</span><span class="sxs-lookup"><span data-stu-id="44049-232"><span id="_security_cipher_mode_gly"></span><span id="_SECURITY_CIPHER_MODE_GLY"></span>**cipher mode**</span></span>
</dt> <dd>

<span data-ttu-id="44049-233">Ein Blockchiffre Modus (jeder Block wird einzeln verschlüsselt), der mithilfe der **cryptsetkeyparam** -Funktion angegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="44049-233">A block cipher mode (each block is encrypted individually) that can be specified by using the **CryptSetKeyParam** function.</span></span> <span data-ttu-id="44049-234">Wenn die Anwendung nicht explizit einen dieser Modi angibt, wird der Verschlüsselungs Modus für Verschlüsselungs Blöcke (Verschlüsselungs Block Verkettung, CBC) verwendet.</span><span class="sxs-lookup"><span data-stu-id="44049-234">If the application does not explicitly specify one of these modes, then the cipher block chaining (CBC) cipher mode is used.</span></span>

<span data-ttu-id="44049-235">ECB: ein Blockchiffre Modus, der kein Feedback verwendet.</span><span class="sxs-lookup"><span data-stu-id="44049-235">ECB: A block cipher mode that uses no feedback.</span></span>

<span data-ttu-id="44049-236">CBC: ein Blockchiffre Modus, der Feedback durch Kombinieren von verschlüsseltem Text und Klartext einführt.</span><span class="sxs-lookup"><span data-stu-id="44049-236">CBC: A block cipher mode that introduces feedback by combining ciphertext and plaintext.</span></span>

<span data-ttu-id="44049-237">CFB: ein Blockchiffre Modus, der kleine Inkremente von Klartext in Chiffre Text verarbeitet, anstatt einen gesamten Block gleichzeitig zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="44049-237">CFB: A block cipher mode that processes small increments of plaintext into ciphertext, instead of processing an entire block at a time.</span></span>

<span data-ttu-id="44049-238">OFB: ein Blockchiffre Modus, der das Feedback wie CFB verwendet.</span><span class="sxs-lookup"><span data-stu-id="44049-238">OFB: A block cipher mode that uses feedback similar to CFB.</span></span>

</dd> <dt>

<span data-ttu-id="44049-239"><span id="_security_ciphertext_gly"></span><span id="_SECURITY_CIPHERTEXT_GLY"></span>**Chiffre Text**</span><span class="sxs-lookup"><span data-stu-id="44049-239"><span id="_security_ciphertext_gly"></span><span id="_SECURITY_CIPHERTEXT_GLY"></span>**ciphertext**</span></span>
</dt> <dd>

<span data-ttu-id="44049-240">Eine Meldung, die verschlüsselt wurde.</span><span class="sxs-lookup"><span data-stu-id="44049-240">A message that has been encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="44049-241"><span id="_security_cleartext_gly"></span><span id="_SECURITY_CLEARTEXT_GLY"></span>**Klartext**</span><span class="sxs-lookup"><span data-stu-id="44049-241"><span id="_security_cleartext_gly"></span><span id="_SECURITY_CLEARTEXT_GLY"></span>**cleartext**</span></span>
</dt> <dd>

<span data-ttu-id="44049-242">Siehe [*Klartext*](p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="44049-242">See [*plaintext*](p-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="44049-243"><span id="_security_client_gly"></span><span id="_SECURITY_CLIENT_GLY"></span>**ent**</span><span class="sxs-lookup"><span data-stu-id="44049-243"><span id="_security_client_gly"></span><span id="_SECURITY_CLIENT_GLY"></span>**client**</span></span>
</dt> <dd>

<span data-ttu-id="44049-244">Die Anwendung anstelle der Serveranwendung, die eine Verbindung mit einem Server initiiert.</span><span class="sxs-lookup"><span data-stu-id="44049-244">The application, rather than the server application, that initiates a connection to a server.</span></span>

<span data-ttu-id="44049-245">Mit [*Server*](s-gly.md)vergleichen.</span><span class="sxs-lookup"><span data-stu-id="44049-245">Compare with [*server*](s-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="44049-246"><span id="_security_client_certificate_gly"></span><span id="_SECURITY_CLIENT_CERTIFICATE_GLY"></span>**Client Zertifikat**</span><span class="sxs-lookup"><span data-stu-id="44049-246"><span id="_security_client_certificate_gly"></span><span id="_SECURITY_CLIENT_CERTIFICATE_GLY"></span>**client certificate**</span></span>
</dt> <dd>

<span data-ttu-id="44049-247">Bezieht sich auf ein Zertifikat, das für die Client Authentifizierung verwendet wird, z. b. das Authentifizieren eines Webbrowsers auf einem Webserver.</span><span class="sxs-lookup"><span data-stu-id="44049-247">Refers to a certificate used for client authentication, such as authenticating a web browser on a web server.</span></span> <span data-ttu-id="44049-248">Wenn ein Webbrowser Client versucht, auf einen gesicherten Webserver zuzugreifen, sendet der Client sein Zertifikat an den Server, damit es die Identität des Clients überprüfen kann.</span><span class="sxs-lookup"><span data-stu-id="44049-248">When a web browser client attempts to access a secured web server, the client sends its certificate to the server to allow it to verify the client's identity.</span></span>

</dd> <dt>

<span data-ttu-id="44049-249"><span id="_security_cmc_gly"></span><span id="_SECURITY_CMC_GLY"></span>**Markets**</span><span class="sxs-lookup"><span data-stu-id="44049-249"><span id="_security_cmc_gly"></span><span id="_SECURITY_CMC_GLY"></span>**CMC**</span></span>
</dt> <dd>

<span data-ttu-id="44049-250">Weitere Informationen finden Sie unter *Zertifikat Verwaltung über CMS*.</span><span class="sxs-lookup"><span data-stu-id="44049-250">See *Certificate Management over CMS*.</span></span>

</dd> <dt>

<span data-ttu-id="44049-251"><span id="_security_cng_gly"></span><span id="_SECURITY_CNG_GLY"></span>**CNG**</span><span class="sxs-lookup"><span data-stu-id="44049-251"><span id="_security_cng_gly"></span><span id="_SECURITY_CNG_GLY"></span>**CNG**</span></span>
</dt> <dd>

<span data-ttu-id="44049-252">Siehe *Cryptography API: Next Generation*.</span><span class="sxs-lookup"><span data-stu-id="44049-252">See *Cryptography API: Next Generation*.</span></span>

</dd> <dt>

<span data-ttu-id="44049-253"><span id="_security_communication_protocol_gly"></span><span id="_SECURITY_COMMUNICATION_PROTOCOL_GLY"></span>**Kommunikationsprotokoll**</span><span class="sxs-lookup"><span data-stu-id="44049-253"><span id="_security_communication_protocol_gly"></span><span id="_SECURITY_COMMUNICATION_PROTOCOL_GLY"></span>**communication protocol**</span></span>
</dt> <dd>

<span data-ttu-id="44049-254">Die Methode, in der Daten serialisiert (in eine Zeichenfolge von einem und Nullen konvertiert) und deserialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="44049-254">The method in which data is serialized (converted to a string of ones and zeros) and deserialized.</span></span> <span data-ttu-id="44049-255">Das Protokoll wird von Software-und Daten Übertragungs Hardware gesteuert.</span><span class="sxs-lookup"><span data-stu-id="44049-255">The protocol is controlled by both software and data-transmission hardware.</span></span>

<span data-ttu-id="44049-256">Ein vereinfachtes Kommunikationsprotokoll, das in der Regel in Bezug auf Ebenen erläutert wird, kann aus einer Anwendungsschicht, einer Codieren/Decodieren Schicht und einer Hardwareebene bestehen.</span><span class="sxs-lookup"><span data-stu-id="44049-256">Typically discussed in terms of layers, a simplified communication protocol might consist of an application layer, encode/decode layer, and hardware layer.</span></span>

</dd> <dt>

<span data-ttu-id="44049-257"><span id="_security_constrained_delegation_gly"></span><span id="_SECURITY_CONSTRAINED_DELEGATION_GLY"></span>**eingeschränkte Delegierung**</span><span class="sxs-lookup"><span data-stu-id="44049-257"><span id="_security_constrained_delegation_gly"></span><span id="_SECURITY_CONSTRAINED_DELEGATION_GLY"></span>**constrained delegation**</span></span>
</dt> <dd>

<span data-ttu-id="44049-258">Das Verhalten, mit dem der Serveranforderungen im Auftrag des Clients nur an eine angegebene Liste von Diensten weiterleiten kann.</span><span class="sxs-lookup"><span data-stu-id="44049-258">Behavior that allows the server to forward requests on behalf of the client only to a specified list of services.</span></span>

<span data-ttu-id="44049-259">**Windows XP:** Die eingeschränkte Delegierung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="44049-259">**Windows XP:** Constrained delegation is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="44049-260"><span id="_security_context_gly"></span><span id="_SECURITY_CONTEXT_GLY"></span>**Kontext**</span><span class="sxs-lookup"><span data-stu-id="44049-260"><span id="_security_context_gly"></span><span id="_SECURITY_CONTEXT_GLY"></span>**context**</span></span>
</dt> <dd>

<span data-ttu-id="44049-261">Die für eine Verbindung relevanten Sicherheitsdaten.</span><span class="sxs-lookup"><span data-stu-id="44049-261">The security data relevant to a connection.</span></span> <span data-ttu-id="44049-262">Ein Kontext enthält Informationen, z. b. einen Sitzungsschlüssel und eine Dauer der Sitzung.</span><span class="sxs-lookup"><span data-stu-id="44049-262">A context contains information such as a session key and duration of the session.</span></span>

</dd> <dt>

<span data-ttu-id="44049-263"><span id="_security_context_function_gly"></span><span id="_SECURITY_CONTEXT_FUNCTION_GLY"></span>**Context-Funktion**</span><span class="sxs-lookup"><span data-stu-id="44049-263"><span id="_security_context_function_gly"></span><span id="_SECURITY_CONTEXT_FUNCTION_GLY"></span>**context function**</span></span>
</dt> <dd>

<span data-ttu-id="44049-264">Zum Herstellen einer Verbindung mit einem Kryptografiedienstanbieter (CSP) verwendete Funktionen.</span><span class="sxs-lookup"><span data-stu-id="44049-264">Functions used to connect to a cryptographic service provider (CSP).</span></span> <span data-ttu-id="44049-265">Mit diesen Funktionen können Anwendungen einen bestimmten CSP mithilfe des Namens auswählen oder einen bestimmten CSP mit einer erforderlichen Funktionsklasse erhalten.</span><span class="sxs-lookup"><span data-stu-id="44049-265">These functions enable applications to choose a specific CSP by name or get one with a needed class of functionality.</span></span>

</dd> <dt>

<span data-ttu-id="44049-266"><span id="_security_countersignature_gly"></span><span id="_SECURITY_COUNTERSIGNATURE_GLY"></span>**gegen Signatur**</span><span class="sxs-lookup"><span data-stu-id="44049-266"><span id="_security_countersignature_gly"></span><span id="_SECURITY_COUNTERSIGNATURE_GLY"></span>**countersignature**</span></span>
</dt> <dd>

<span data-ttu-id="44049-267">Eine Signatur einer vorhandenen Signatur und Nachricht oder eine Signatur einer vorhandenen Signatur.</span><span class="sxs-lookup"><span data-stu-id="44049-267">A signature of an existing signature and message or a signature of an existing signature.</span></span> <span data-ttu-id="44049-268">Eine gegen Signatur wird verwendet, um den verschlüsselten Hash einer vorhandenen Signatur zu signieren oder um eine Nachricht mit einem Zeitstempel zu versehen.</span><span class="sxs-lookup"><span data-stu-id="44049-268">A countersignature is used to sign the encrypted hash of an existing signature or to time stamp a message.</span></span>

</dd> <dt>

<span data-ttu-id="44049-269"><span id="_security_credentials_gly"></span><span id="_SECURITY_CREDENTIALS_GLY"></span>**Daten**</span><span class="sxs-lookup"><span data-stu-id="44049-269"><span id="_security_credentials_gly"></span><span id="_SECURITY_CREDENTIALS_GLY"></span>**credentials**</span></span>
</dt> <dd>

<span data-ttu-id="44049-270">Zuvor authentifizierte Anmeldedaten, die von einem [*Sicherheits Prinzipal*](s-gly.md) zum Einrichten der eigenen Identität verwendet werden, z. b. ein Kennwort oder ein Kerberos-Protokoll Ticket.</span><span class="sxs-lookup"><span data-stu-id="44049-270">Previously authenticated logon data used by a [*security principal*](s-gly.md) to establish its own identity, such as a password, or a Kerberos protocol ticket.</span></span>

</dd> <dt>

<span data-ttu-id="44049-271"><span id="_security_crl_gly"></span><span id="_SECURITY_CRL_GLY"></span>**CRL**</span><span class="sxs-lookup"><span data-stu-id="44049-271"><span id="_security_crl_gly"></span><span id="_SECURITY_CRL_GLY"></span>**CRL**</span></span>
</dt> <dd>

<span data-ttu-id="44049-272">Siehe *Zertifikat Sperr Liste*.</span><span class="sxs-lookup"><span data-stu-id="44049-272">See *certificate revocation list*.</span></span>

</dd> <dt>

<span data-ttu-id="44049-273"><span id="_security_crypt_asn_encoding_gly"></span><span id="_SECURITY_CRYPT_ASN_ENCODING_GLY"></span>**Crypt- \_ ASN- \_ Codierung**</span><span class="sxs-lookup"><span data-stu-id="44049-273"><span id="_security_crypt_asn_encoding_gly"></span><span id="_SECURITY_CRYPT_ASN_ENCODING_GLY"></span>**CRYPT\_ASN\_ENCODING**</span></span>
</dt> <dd>

<span data-ttu-id="44049-274">Codierungstyp, der die Zertifikat Codierung angibt.</span><span class="sxs-lookup"><span data-stu-id="44049-274">Encoding type that specifies certificate encoding.</span></span> <span data-ttu-id="44049-275">Zertifikat Codierungs Typen werden im nieder wertigen Wort eines **DWORD** gespeichert (Wert: 0x00000001).</span><span class="sxs-lookup"><span data-stu-id="44049-275">Certificate encoding types are stored in the low-order word of a **DWORD** (value is: 0x00000001).</span></span> <span data-ttu-id="44049-276">Dieser Codierungstyp ist funktional identisch mit dem \_ \_ Codierungstyp X509 ASN Encoding.</span><span class="sxs-lookup"><span data-stu-id="44049-276">This encoding type is functionally the same as the X509\_ASN\_ENCODING encoding type.</span></span>

</dd> <dt>

<span data-ttu-id="44049-277"><span id="_security_cryptoanalysis_gly"></span><span id="_SECURITY_CRYPTOANALYSIS_GLY"></span>**kryptanalysis**</span><span class="sxs-lookup"><span data-stu-id="44049-277"><span id="_security_cryptoanalysis_gly"></span><span id="_SECURITY_CRYPTOANALYSIS_GLY"></span>**cryptanalysis**</span></span>
</dt> <dd>

<span data-ttu-id="44049-278">Cryptanalysis ist die Kunst und Wissenschaft des unterbrechenden verschlüsselten Texts.</span><span class="sxs-lookup"><span data-stu-id="44049-278">Cryptanalysis is the art and science of breaking ciphertext.</span></span> <span data-ttu-id="44049-279">Im Gegensatz dazu ist die Art und Wissenschaft der sicheren Aufbewahrung von Nachrichten Kryptografie.</span><span class="sxs-lookup"><span data-stu-id="44049-279">In contrast, the art and science of keeping messages secure is cryptography.</span></span>

</dd> <dt>

<span data-ttu-id="44049-280"><span id="_security_cryptoapi_gly"></span><span id="_SECURITY_CRYPTOAPI_GLY"></span>**CryptoAPI**</span><span class="sxs-lookup"><span data-stu-id="44049-280"><span id="_security_cryptoapi_gly"></span><span id="_SECURITY_CRYPTOAPI_GLY"></span>**CryptoAPI**</span></span>
</dt> <dd>

<span data-ttu-id="44049-281">Anwendungsprogrammierschnittstelle, mit der Anwendungsentwickler Windows-basierten Anwendungen Authentifizierung, Codierung und Verschlüsselung hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="44049-281">Application programming interface that enables application developers to add authentication, encoding, and encryption to Windows-based applications.</span></span>

</dd> <dt>

<span data-ttu-id="44049-282"><span id="_security_cryptographic_algorithm_gly"></span><span id="_SECURITY_CRYPTOGRAPHIC_ALGORITHM_GLY"></span>**kryptografischer Algorithmus**</span><span class="sxs-lookup"><span data-stu-id="44049-282"><span id="_security_cryptographic_algorithm_gly"></span><span id="_SECURITY_CRYPTOGRAPHIC_ALGORITHM_GLY"></span>**cryptographic algorithm**</span></span>
</dt> <dd>

<span data-ttu-id="44049-283">Eine mathematische Funktion, die für die Verschlüsselung und Entschlüsselung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="44049-283">A mathematical function used for encryption and decryption.</span></span> <span data-ttu-id="44049-284">Die meisten Kryptografiealgorithmen basieren auf einer Ersetzungs Chiffre, einer Umsetzungs Chiffre oder einer Kombination aus beidem.</span><span class="sxs-lookup"><span data-stu-id="44049-284">Most cryptographic algorithms are based on a substitution cipher, a transposition cipher, or a combination of both.</span></span>

</dd> <dt>

<span data-ttu-id="44049-285"><span id="_security_cryptographic_digest_gly"></span><span id="_SECURITY_CRYPTOGRAPHIC_DIGEST_GLY"></span>**Kryptografischer Digest**</span><span class="sxs-lookup"><span data-stu-id="44049-285"><span id="_security_cryptographic_digest_gly"></span><span id="_SECURITY_CRYPTOGRAPHIC_DIGEST_GLY"></span>**Cryptographic Digest**</span></span>
</dt> <dd>

<span data-ttu-id="44049-286">Eine unidirektionale Hash Funktion, die eine Eingabe Zeichenfolge variabler Länge annimmt und Sie in eine Ausgabe Zeichenfolge mit fester Länge konvertiert (als kryptografiedigest bezeichnet). Diese Ausgabe Zeichenfolge mit fester Länge ist für jede andere Eingabe Zeichenfolge probabilistisch eindeutig und kann daher als Fingerabdruck einer Datei fungieren.</span><span class="sxs-lookup"><span data-stu-id="44049-286">A one-way hash function that takes a variable-length input string and converts it to a fixed-length output string (called a cryptographic digest.) This fixed-length output string is probabilistically unique for every different input string and thus can act as a fingerprint of a file.</span></span> <span data-ttu-id="44049-287">Wenn eine Datei mit einem kryptografischen Digest heruntergeladen wird, berechnet der Empfänger den Digest neu.</span><span class="sxs-lookup"><span data-stu-id="44049-287">When a file with a cryptographic digest is downloaded, the receiver recomputes the digest.</span></span> <span data-ttu-id="44049-288">Wenn die Ausgabe Zeichenfolge mit dem in der Datei enthaltenen Digest übereinstimmt, hat der Empfänger den Nachweis, dass die empfangene Datei nicht manipuliert wurde und mit der ursprünglich gesendeten Datei identisch ist.</span><span class="sxs-lookup"><span data-stu-id="44049-288">If the output string matches the digest contained in the file, the receiver has proof that the received file was not tampered with and is identical to the file originally sent.</span></span>

</dd> <dt>

<span data-ttu-id="44049-289"><span id="_security_cryptographic_key_gly"></span><span id="_SECURITY_CRYPTOGRAPHIC_KEY_GLY"></span>**Kryptografischer Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="44049-289"><span id="_security_cryptographic_key_gly"></span><span id="_SECURITY_CRYPTOGRAPHIC_KEY_GLY"></span>**cryptographic key**</span></span>
</dt> <dd>

<span data-ttu-id="44049-290">Ein kryptografischer Schlüssel ist ein Datenelement, das zum Initialisieren eines Kryptografiealgorithmus erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="44049-290">A cryptographic key is a piece of data that is required to initialize a cryptographic algorithm.</span></span> <span data-ttu-id="44049-291">Kryptografiesysteme sind in der Regel so konzipiert, dass Ihre Sicherheit nur von der Sicherheit Ihrer Kryptografieschlüssel abhängt, nicht z. b. durch die Beibehaltung der geheimen Algorithmen.</span><span class="sxs-lookup"><span data-stu-id="44049-291">Cryptographic systems are generally designed so that their security depends only on the security of their cryptographic keys and not, for example, on keeping their algorithms secret.</span></span>

<span data-ttu-id="44049-292">Es gibt viele verschiedene Arten von Kryptografieschlüsseln, die der verschiedensten Kryptografiealgorithmen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="44049-292">There are many different types of cryptographic keys, corresponding to the wide variety of cryptographic algorithms.</span></span> <span data-ttu-id="44049-293">Schlüssel können nach dem Typ des verwendeten Algorithmus klassifiziert werden (z. b. als symmetrische oder asymmetrische Schlüssel).</span><span class="sxs-lookup"><span data-stu-id="44049-293">Keys can be classified according to the type of algorithm they are used with (for example, as symmetric or asymmetric keys).</span></span> <span data-ttu-id="44049-294">Sie können auch basierend auf Ihrer Lebensdauer innerhalb eines Systems klassifiziert werden (z. b. als langlebige oder Sitzungsschlüssel).</span><span class="sxs-lookup"><span data-stu-id="44049-294">They can also be classified based on their lifetime within a system (for example, as long-lived or session keys).</span></span>

</dd> <dt>

<span data-ttu-id="44049-295"><span id="_security_cryptographic_service_provider_gly"></span><span id="_SECURITY_CRYPTOGRAPHIC_SERVICE_PROVIDER_GLY"></span>**Kryptografiedienstanbieter**</span><span class="sxs-lookup"><span data-stu-id="44049-295"><span id="_security_cryptographic_service_provider_gly"></span><span id="_SECURITY_CRYPTOGRAPHIC_SERVICE_PROVIDER_GLY"></span>**cryptographic service provider**</span></span>
</dt> <dd>

<span data-ttu-id="44049-296">CSP Ein unabhängiges Softwaremodul, das tatsächlich Kryptografiealgorithmen für Authentifizierung, Codierung und Verschlüsselung ausführt.</span><span class="sxs-lookup"><span data-stu-id="44049-296">(CSP) An independent software module that actually performs cryptography algorithms for authentication, encoding, and encryption.</span></span>

</dd> <dt>

<span data-ttu-id="44049-297"><span id="_security_cryptography_gly"></span><span id="_SECURITY_CRYPTOGRAPHY_GLY"></span>**Kryptografie**</span><span class="sxs-lookup"><span data-stu-id="44049-297"><span id="_security_cryptography_gly"></span><span id="_SECURITY_CRYPTOGRAPHY_GLY"></span>**cryptography**</span></span>
</dt> <dd>

<span data-ttu-id="44049-298">Die Kunst und Wissenschaft der Informationssicherheit.</span><span class="sxs-lookup"><span data-stu-id="44049-298">The art and science of information security.</span></span> <span data-ttu-id="44049-299">Es umfasst Informationen Vertraulichkeit, Datenintegrität, Entitäts Authentifizierung und Daten Ursprungs Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="44049-299">It includes information confidentiality, data integrity, entity authentication, and data origin authentication.</span></span>

</dd> <dt>

<span data-ttu-id="44049-300"><span id="_security_cryptography_api_gly"></span><span id="_SECURITY_CRYPTOGRAPHY_API_GLY"></span>**Kryptografieapi**</span><span class="sxs-lookup"><span data-stu-id="44049-300"><span id="_security_cryptography_api_gly"></span><span id="_SECURITY_CRYPTOGRAPHY_API_GLY"></span>**Cryptography API**</span></span>
</dt> <dd>

<span data-ttu-id="44049-301">Siehe *CryptoAPI*.</span><span class="sxs-lookup"><span data-stu-id="44049-301">See *CryptoAPI*.</span></span>

</dd> <dt>

<span data-ttu-id="44049-302"><span id="_security_cryptography_api__next_generation_gly"></span><span id="_SECURITY_CRYPTOGRAPHY_API__NEXT_GENERATION_GLY"></span>**Kryptografieapi: nächste Generation**</span><span class="sxs-lookup"><span data-stu-id="44049-302"><span id="_security_cryptography_api__next_generation_gly"></span><span id="_SECURITY_CRYPTOGRAPHY_API__NEXT_GENERATION_GLY"></span>**Cryptography API: Next Generation**</span></span>
</dt> <dd>

<span data-ttu-id="44049-303">CNG Die zweite Generierung der *kryptoapi*.</span><span class="sxs-lookup"><span data-stu-id="44049-303">(CNG) The second generation of the *CryptoAPI*.</span></span> <span data-ttu-id="44049-304">CNG ermöglicht es Ihnen, vorhandene Algorithmusanbieter durch ihre eigenen Anbieter zu ersetzen und neue Algorithmen hinzuzufügen, sobald Sie verfügbar werden.</span><span class="sxs-lookup"><span data-stu-id="44049-304">CNG allows you to replace existing algorithm providers with your own providers and add new algorithms as they become available.</span></span> <span data-ttu-id="44049-305">Mit CNG können auch dieselben APIs in Anwendungen für den Benutzer-und Kernelmodus verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="44049-305">CNG also allows the same APIs to be used from user and kernel mode applications.</span></span>

</dd> <dt>

<span data-ttu-id="44049-306"><span id="_security_cryptology_gly"></span><span id="_SECURITY_CRYPTOLOGY_GLY"></span>**ration**</span><span class="sxs-lookup"><span data-stu-id="44049-306"><span id="_security_cryptology_gly"></span><span id="_SECURITY_CRYPTOLOGY_GLY"></span>**cryptology**</span></span>
</dt> <dd>

<span data-ttu-id="44049-307">Der Branch der Mathematik, der sowohl Kryptografie als auch Cryptanalysis umfasst.</span><span class="sxs-lookup"><span data-stu-id="44049-307">The branch of mathematics that encompasses both cryptography and cryptanalysis.</span></span>

</dd> <dt>

<span data-ttu-id="44049-308"><span id="_security_cryptospi_gly"></span><span id="_SECURITY_CRYPTOSPI_GLY"></span>**Kryptospi**</span><span class="sxs-lookup"><span data-stu-id="44049-308"><span id="_security_cryptospi_gly"></span><span id="_SECURITY_CRYPTOSPI_GLY"></span>**CryptoSPI**</span></span>
</dt> <dd>

<span data-ttu-id="44049-309">Die Systemprogramm Schnittstelle, die mit einem *Kryptografiedienstanbieter* (CSP) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="44049-309">The system program interface used with a *cryptographic service provider* (CSP).</span></span>

</dd> <dt>

<span data-ttu-id="44049-310"><span id="_security_csp_gly"></span><span id="_SECURITY_CSP_GLY"></span>**CSP**</span><span class="sxs-lookup"><span data-stu-id="44049-310"><span id="_security_csp_gly"></span><span id="_SECURITY_CSP_GLY"></span>**CSP**</span></span>
</dt> <dd>

<span data-ttu-id="44049-311">Siehe *Kryptografiedienstanbieter*.</span><span class="sxs-lookup"><span data-stu-id="44049-311">See *cryptographic service provider*.</span></span>

</dd> <dt>

<span data-ttu-id="44049-312"><span id="_security_csp_family_gly"></span><span id="_SECURITY_CSP_FAMILY_GLY"></span>**CSP-Familie**</span><span class="sxs-lookup"><span data-stu-id="44049-312"><span id="_security_csp_family_gly"></span><span id="_SECURITY_CSP_FAMILY_GLY"></span>**CSP family**</span></span>
</dt> <dd>

<span data-ttu-id="44049-313">Eine eindeutige Gruppe von CSPs, die denselben Satz von Datenformaten verwenden und ihre Funktion auf die gleiche Weise ausführen.</span><span class="sxs-lookup"><span data-stu-id="44049-313">A unique group of CSPs that use the same set of data formats and perform their function in the same way.</span></span> <span data-ttu-id="44049-314">Auch wenn zwei CSP-Familien denselben Algorithmus verwenden (z. b. die RC2-Blockchiffre), machen die unterschiedlichen Paddingschemas, Schlüssellängen oder Standard Modi jede Gruppe eindeutig.</span><span class="sxs-lookup"><span data-stu-id="44049-314">Even when two CSP families use the same algorithm (for example, the RC2 block cipher), their different padding schemes, keys lengths, or default modes make each group distinct.</span></span> <span data-ttu-id="44049-315">CryptoAPI wurde so entworfen, dass jeder CSP-Typ eine bestimmte Familie darstellt.</span><span class="sxs-lookup"><span data-stu-id="44049-315">CryptoAPI has been designed so that each CSP type represents a particular family.</span></span>

</dd> <dt>

<span data-ttu-id="44049-316"><span id="_security_csp_name_gly"></span><span id="_SECURITY_CSP_NAME_GLY"></span>**CSP-Name**</span><span class="sxs-lookup"><span data-stu-id="44049-316"><span id="_security_csp_name_gly"></span><span id="_SECURITY_CSP_NAME_GLY"></span>**CSP name**</span></span>
</dt> <dd>

<span data-ttu-id="44049-317">Der Textname des CSP.</span><span class="sxs-lookup"><span data-stu-id="44049-317">The textual name of the CSP.</span></span> <span data-ttu-id="44049-318">Wenn der CSP von Microsoft signiert wurde, muss dieser Name genau mit dem CSP-Namen übereinstimmen, der im Export Kompatibilitäts Zertifikat (ECC) angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="44049-318">If the CSP has been signed by Microsoft, this name must exactly match the CSP name that was specified in the Export Compliance Certificate (ECC).</span></span>

</dd> <dt>

<span data-ttu-id="44049-319"><span id="_security_csp_type_gly"></span><span id="_SECURITY_CSP_TYPE_GLY"></span>**CSP-Typ**</span><span class="sxs-lookup"><span data-stu-id="44049-319"><span id="_security_csp_type_gly"></span><span id="_SECURITY_CSP_TYPE_GLY"></span>**CSP type**</span></span>
</dt> <dd>

<span data-ttu-id="44049-320">Gibt die einem Anbieter zugeordnete CSP-Familie an.</span><span class="sxs-lookup"><span data-stu-id="44049-320">Indicates the CSP family associated with a provider.</span></span> <span data-ttu-id="44049-321">Wenn eine Anwendung eine Verbindung mit einem CSP eines bestimmten Typs herstellt, wird jede der kryptoapi-Funktionen standardmäßig in einer von der-Familie vorgeschriebenen Weise ausgeführt, die diesem CSP-Typ entspricht.</span><span class="sxs-lookup"><span data-stu-id="44049-321">When an application connects to a CSP of a particular type, each of the CryptoAPI functions will, by default, operate in a way prescribed by the family that corresponds to that CSP type.</span></span>

</dd> <dt>

<span data-ttu-id="44049-322"><span id="_security_ctl_gly"></span><span id="_SECURITY_CTL_GLY"></span>**CTL**</span><span class="sxs-lookup"><span data-stu-id="44049-322"><span id="_security_ctl_gly"></span><span id="_SECURITY_CTL_GLY"></span>**CTL**</span></span>
</dt> <dd>

<span data-ttu-id="44049-323">Siehe *Zertifikat Vertrauens Liste*.</span><span class="sxs-lookup"><span data-stu-id="44049-323">See *certificate trust list*.</span></span>

</dd> <dt>

<span data-ttu-id="44049-324"><span id="_security_cylink_mek_gly"></span><span id="_SECURITY_CYLINK_MEK_GLY"></span>**Cylink- \_ MEK**</span><span class="sxs-lookup"><span data-stu-id="44049-324"><span id="_security_cylink_mek_gly"></span><span id="_SECURITY_CYLINK_MEK_GLY"></span>**CYLINK\_MEK**</span></span>
</dt> <dd>

<span data-ttu-id="44049-325">Ein Verschlüsselungsalgorithmus, der eine 40-Bit-Variante eines des-Schlüssels verwendet, bei der 16 Bits des 56-Bit-des-Schlüssels auf 0 (null) festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="44049-325">An encryption algorithm that uses a 40-bit variant of a DES key where 16 bits of the 56-bit DES key are set to zero.</span></span> <span data-ttu-id="44049-326">Dieser Algorithmus wird entsprechend der Angabe in der IETF-Entwurfs Spezifikation für 40-Bit-des implementiert.</span><span class="sxs-lookup"><span data-stu-id="44049-326">This algorithm is implemented as specified in the IETF Draft specification for 40-bit DES.</span></span> <span data-ttu-id="44049-327">Die Entwurfs Spezifikation zum Zeitpunkt der Erstellung dieses Artikels finden Sie unter FTP://FTP.ietf.org/Internet-Drafts/draft-hoffman-des40-02.txt.</span><span class="sxs-lookup"><span data-stu-id="44049-327">The draft specification, at the time of this writing can be found at ftp://ftp.ietf.org/internet-drafts/draft-hoffman-des40-02.txt.</span></span> <span data-ttu-id="44049-328">Dieser Algorithmus wird mit dem **ALG- \_ ID** -Wert calg \_ Cylink \_ MEK verwendet.</span><span class="sxs-lookup"><span data-stu-id="44049-328">This algorithm is used with the **ALG\_ID** value CALG\_CYLINK\_MEK.</span></span>

</dd> </dl>

 

 
