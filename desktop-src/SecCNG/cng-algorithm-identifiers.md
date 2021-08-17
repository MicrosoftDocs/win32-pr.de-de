---
description: Wird verwendet, um Standardverschlüsselungsalgorithmen in verschiedenen CNG-Funktionen und -Strukturen wie der CRYPT \_ INTERFACE \_ REG-Struktur zu identifizieren.
ms.assetid: a05ae7e6-d882-4287-9990-23e4cd340b05
title: CNG-Algorithmusbezeichner (Bcrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1f2f9539f9fc446d0c313d32117890bc3b1eff4ed8261a815e41acdda13cbe4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118908916"
---
# <a name="cng-algorithm-identifiers"></a>CNG-Algorithmusbezeichner

Die folgenden Bezeichner werden verwendet, um Standardverschlüsselungsalgorithmen in verschiedenen CNG-Funktionen und -Strukturen zu identifizieren, z. B. in der [**CRYPT \_ INTERFACE \_ REG-Struktur.**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_interface_reg) Drittanbieter verfügen möglicherweise über zusätzliche Algorithmen, die sie unterstützen.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Konstante/Wert</th>
<th style="text-align: left;">BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_3DES_ALGORITHM"></span><span id="bcrypt_3des_algorithm"></span><dl> <dt><strong>BCRYPT_3DES_ALGORITHM</strong></dt> <dt> &quot; 3DES &quot; </dt> </dl></td>
<td style="text-align: left;">Der standardmäßige symmetrische Verschlüsselungsalgorithmus für die dreifache Datenverschlüsselung.<br/> Standard: SP800-67, SP800-38A<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_3DES_112_ALGORITHM"></span><span id="bcrypt_3des_112_algorithm"></span><dl> <dt><strong>BCRYPT_3DES_112_ALGORITHM</strong></dt> <dt> &quot; &quot; 3DES_112</dt> </dl></td>
<td style="text-align: left;">Der symmetrische 112-Bit-Verschlüsselungsstandardalgorithmus für die dreifache Datenverschlüsselung.<br/> Standard: SP800-67, SP800-38A<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_AES_ALGORITHM"></span><span id="bcrypt_aes_algorithm"></span><dl> <dt><strong>BCRYPT_AES_ALGORITHM</strong></dt> <dt> &quot; AES &quot; </dt> </dl></td>
<td style="text-align: left;">Der erweiterte symmetrische Verschlüsselungsalgorithmus für den Verschlüsselungsstandard.<br/> Standard: FIPS 197<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_AES_CMAC_ALGORITHM"></span><span id="bcrypt_aes_cmac_algorithm"></span><dl> <dt><strong>BCRYPT_AES_CMAC_ALGORITHM</strong></dt> <dt> &quot; AES-CMAC &quot; </dt> </dl></td>
<td style="text-align: left;">Der AES-Verschlüsselungsalgorithmus (Advanced Encryption Standard, verschlüsselungsbasierter Nachrichtenauthentifizierungscode) (CMAC).<br/> Standard: SP 800-38B<br/> <strong>Windows 8:</strong> Die Unterstützung für diesen Algorithmus beginnt.<br/> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_AES_GMAC_ALGORITHM"></span><span id="bcrypt_aes_gmac_algorithm"></span><dl> <dt><strong>BCRYPT_AES_GMAC_ALGORITHM</strong></dt> <dt> &quot; AES-GMAC &quot; </dt> </dl></td>
<td style="text-align: left;">Der AES-Algorithmus (Advanced Encryption Standard) Galois Message Authentication Code (GMAC) für symmetrische Verschlüsselung.<br/> Standard: SP800-38D<br/> <strong>Windows Vista:</strong> Dieser Algorithmus wird ab Windows Vista mit SP1 unterstützt.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_CAPI_KDF_ALGORITHM"></span><span id="bcrypt_capi_kdf_algorithm"></span><dl> <dt><strong>BCRYPT_CAPI_KDF_ALGORITHM</strong></dt> <dt> &quot; &quot; L-CAPI_KDF</dt> </dl></td>
<td style="text-align: left;">Schlüsselableitungsfunktionsalgorithmus der Kryptografie-API (CAPI). Wird von den <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>Funktionen BCryptKeyDerivation</strong></a> und <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>NCryptKeyDerivation</strong></a> verwendet.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_DES_ALGORITHM"></span><span id="bcrypt_des_algorithm"></span><dl> <dt><strong>BCRYPT_DES_ALGORITHM</strong></dt> <dt> &quot; DES &quot; </dt> </dl></td>
<td style="text-align: left;">Der symmetrische Verschlüsselungsalgorithmus der Datenverschlüsselungsstandard.<br/> Standard: FIPS 46-3, FIPS 81<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_DESX_ALGORITHM"></span><span id="bcrypt_desx_algorithm"></span><dl> <dt><strong>BCRYPT_DESX_ALGORITHM</strong></dt> <dt> &quot; DESX &quot; </dt> </dl></td>
<td style="text-align: left;">Der symmetrische Verschlüsselungsalgorithmus für erweiterte Datenverschlüsselungsstandard.<br/> Standard: Keine<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_DH_ALGORITHM"></span><span id="bcrypt_dh_algorithm"></span><dl> <dt><strong>BCRYPT_DH_ALGORITHM</strong></dt> <dt> &quot; DH &quot; </dt> </dl></td>
<td style="text-align: left;">Der Diffie-Hellman Algorithmus für den Schlüsselaustausch.<br/> Standard: PKCS #3<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_DSA_ALGORITHM"></span><span id="bcrypt_dsa_algorithm"></span><dl> <dt><strong>BCRYPT_DSA_ALGORITHM</strong></dt> <dt> &quot; DSA &quot; </dt> </dl></td>
<td style="text-align: left;">Der Algorithmus für digitale Signaturen.<br/> Standard: FIPS 186-2<br/> <strong>Windows 8:</strong> Ab Windows 8 unterstützt dieser Algorithmus FIPS 186-3. Schlüssel kleiner oder gleich 1024 Bits entsprechen FIPS 186-2 und Schlüssel größer als 1024 fips 186-3.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_ECDH_P256_ALGORITHM"></span><span id="bcrypt_ecdh_p256_algorithm"></span><dl> <dt><strong>BCRYPT_ECDH_P256_ALGORITHM</strong></dt> <dt> &quot; ECDH_P256 &quot; </dt> </dl></td>
<td style="text-align: left;">Die 256-Bit-Prim-Elliptikkurve Diffie-Hellman Schlüsselaustauschalgorithmus.<br/> Standard: SP800-56A<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_ECDH_P384_ALGORITHM"></span><span id="bcrypt_ecdh_p384_algorithm"></span><dl> <dt><strong>BCRYPT_ECDH_P384_ALGORITHM</strong></dt> <dt> &quot; &quot; ECDH_P384</dt> </dl></td>
<td style="text-align: left;">Die 384-Bit-Prim-Elliptikkurve Diffie-Hellman Schlüsselaustauschalgorithmus.<br/> Standard: SP800-56A<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_ECDH_P521_ALGORITHM"></span><span id="bcrypt_ecdh_p521_algorithm"></span><dl> <dt><strong>BCRYPT_ECDH_P521_ALGORITHM</strong></dt> <dt> &quot; ECDH_P521 &quot; </dt> </dl></td>
<td style="text-align: left;">Die 521-Bit-Prim-Elliptikkurve Diffie-Hellman Schlüsselaustauschalgorithmus.<br/> Standard: SP800-56A<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_ECDSA_P256_ALGORITHM"></span><span id="bcrypt_ecdsa_p256_algorithm"></span><dl> <dt><strong>BCRYPT_ECDSA_P256_ALGORITHM</strong></dt> <dt> &quot; &quot; ECDSA_P256</dt> </dl></td>
<td style="text-align: left;">Der Digitale Signaturalgorithmus der 256-Bit-Prim-Elliptic Curve (FIPS 186-2).<br/> Standard: FIPS 186-2, X9.62<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_ECDSA_P384_ALGORITHM"></span><span id="bcrypt_ecdsa_p384_algorithm"></span><dl> <dt><strong>BCRYPT_ECDSA_P384_ALGORITHM</strong></dt> <dt> &quot; &quot; ECDSA_P384</dt> </dl></td>
<td style="text-align: left;">Der Digitale Signaturalgorithmus der 384-Bit-Prim-Elliptic Curve (FIPS 186-2).<br/> Standard: FIPS 186-2, X9.62<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_ECDSA_P521_ALGORITHM"></span><span id="bcrypt_ecdsa_p521_algorithm"></span><dl> <dt><strong>BCRYPT_ECDSA_P521_ALGORITHM</strong></dt> <dt> &quot; ECDSA_P521 &quot; </dt> </dl></td>
<td style="text-align: left;">Der Digitale Signaturalgorithmus der 521-Bit-Prim-Elliptic Curve (FIPS 186-2).<br/> Standard: FIPS 186-2, X9.62<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_MD2_ALGORITHM"></span><span id="bcrypt_md2_algorithm"></span><dl> <dt><strong>BCRYPT_MD2_ALGORITHM</strong></dt> <dt> &quot; MD2 &quot; </dt> </dl></td>
<td style="text-align: left;">Der MD2-Hashalgorithmus.<br/> Standard: RFC 1319<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_MD4_ALGORITHM"></span><span id="bcrypt_md4_algorithm"></span><dl> <dt><strong>BCRYPT_MD4_ALGORITHM</strong></dt> <dt> &quot; MD4 &quot; </dt> </dl></td>
<td style="text-align: left;">Der MD4-Hashalgorithmus.<br/> Standard: RFC 1320<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_MD5_ALGORITHM"></span><span id="bcrypt_md5_algorithm"></span><dl> <dt><strong>BCRYPT_MD5_ALGORITHM</strong></dt> <dt> &quot; MD5 &quot; </dt> </dl></td>
<td style="text-align: left;">Der MD5-Hashalgorithmus.<br/> Standard: RFC 1321<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_RC2_ALGORITHM"></span><span id="bcrypt_rc2_algorithm"></span><dl> <dt><strong>BCRYPT_RC2_ALGORITHM</strong></dt> <dt> &quot; RC2 &quot; </dt> </dl></td>
<td style="text-align: left;">Der symmetrische Verschlüsselungsalgorithmus RC2-Block.<br/> Standard: RFC 2268<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_RC4_ALGORITHM"></span><span id="bcrypt_rc4_algorithm"></span><dl> <dt><strong>BCRYPT_RC4_ALGORITHM</strong></dt> <dt> &quot; RC4 &quot; </dt> </dl></td>
<td style="text-align: left;">Der symmetrische RC4-Verschlüsselungsalgorithmus.<br/> Standard: Verschiedene<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_RNG_ALGORITHM"></span><span id="bcrypt_rng_algorithm"></span><dl> <dt><strong>BCRYPT_RNG_ALGORITHM</strong></dt> <dt> &quot; RNG &quot; </dt> </dl></td>
<td style="text-align: left;">Der Zufallszahlengeneratoralgorithmus.<br/> Standard: FIPS 186-2, FIPS 140-2, NIST SP 800-90<br/>
<blockquote>
[!Note]<br />
Ab Windows Vista mit SP1 und Windows Server 2008 basiert der Zufallszahlengenerator auf dem im NIST SP 800-90-Standard angegebenen AES-Indikatormodus.
</blockquote>
<br/> <strong>Windows Vista:</strong> Der Zufallszahlengenerator basiert auf dem hashbasierten Zufallszahlengenerator, der im FIPS 186-2-Standard angegeben ist.<br/> <strong>Windows 8:</strong> Ab Windows 8 unterstützt der RNG-Algorithmus FIPS 186-3. Schlüssel kleiner oder gleich 1024 Bits entsprechen FIPS 186-2 und Schlüssel größer als 1024 fips 186-3.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_RNG_DUAL_EC_ALGORITHM"></span><span id="bcrypt_rng_dual_ec_algorithm"></span><dl> <dt><strong>BCRYPT_RNG_DUAL_EC_ALGORITHM</strong></dt> <dt> &quot; DUALECRNG &quot; </dt> </dl></td>
<td style="text-align: left;">Der Generatoralgorithmus für zufallszahlenbasierte Dual-Elliptic Curves. <br/> Standard: SP800-90.<br/> <strong>Windows 8:</strong> Ab Windows 8 unterstützt der EC-RNG-Algorithmus FIPS 186-3. Schlüssel kleiner oder gleich 1024 Bits entsprechen FIPS 186-2 und Schlüssel größer als 1024 fips 186-3.<br/> <strong>Windows 10:</strong> Ab Windows 10 wurde der Algorithmus für den Zufallszahlengenerator mit doppelter Elliptic Curve entfernt. Vorhandene Verwendungsmöglichkeiten dieses Algorithmus funktionieren weiterhin. der Zufallszahlengenerator basiert jedoch auf dem im NIST SP 800-90-Standard angegebenen AES-Indikatormodus. Neuer Code sollte <strong>BCRYPT_RNG_ALGORITHM</strong>verwenden, und es wird empfohlen, vorhandenen Code so zu ändern, dass <strong>er BCRYPT_RNG_ALGORITHM</strong>verwendet. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_RNG_FIPS186_DSA_ALGORITHM"></span><span id="bcrypt_rng_fips186_dsa_algorithm"></span><dl> <dt><strong>BCRYPT_RNG_FIPS186_DSA_ALGORITHM</strong></dt> <dt> &quot; FIPS186DSARNG &quot; </dt> </dl></td>
<td style="text-align: left;">Der zufallszahlenbasierte Generatoralgorithmus, der für DSA (Digital Signature Algorithm) geeignet ist. <br/> Standard: FIPS 186-2.<br/> <strong>Windows 8:</strong> Die Unterstützung für FIPS 186-3 beginnt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_RSA_ALGORITHM"></span><span id="bcrypt_rsa_algorithm"></span><dl> <dt><strong>BCRYPT_RSA_ALGORITHM</strong></dt> <dt> &quot; RSA &quot; </dt> </dl></td>
<td style="text-align: left;">Der RSA-Algorithmus für den öffentlichen Schlüssel. <br/> Standard: PKCS #1 v1.5 und v2.0.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_RSA_SIGN_ALGORITHM"></span><span id="bcrypt_rsa_sign_algorithm"></span><dl> <dt><strong>BCRYPT_RSA_SIGN_ALGORITHM</strong></dt> <dt> &quot; RSA_SIGN &quot; </dt> </dl></td>
<td style="text-align: left;">Der RSA-Signaturalgorithmus. Dieser Algorithmus wird derzeit nicht unterstützt. Sie können den <strong>BCRYPT_RSA_ALGORITHM</strong> Algorithmus verwenden, um RSA-Signaturvorgänge auszuführen. <br/> Standard: PKCS #1 v1.5 und v2.0.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_SHA1_ALGORITHM"></span><span id="bcrypt_sha1_algorithm"></span><dl> <dt><strong>BCRYPT_SHA1_ALGORITHM</strong></dt> <dt> &quot; SHA1 &quot; </dt> </dl></td>
<td style="text-align: left;">Der sichere 160-Bit-Hashalgorithmus. <br/> Standard: FIPS 180-2, FIPS 198.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_SHA256_ALGORITHM"></span><span id="bcrypt_sha256_algorithm"></span><dl> <dt><strong>BCRYPT_SHA256_ALGORITHM</strong></dt> <dt> &quot; SHA256 &quot; </dt> </dl></td>
<td style="text-align: left;">Der sichere 256-Bit-Hashalgorithmus.<br/> Standard: FIPS 180-2, FIPS 198.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_SHA384_ALGORITHM"></span><span id="bcrypt_sha384_algorithm"></span><dl> <dt><strong>BCRYPT_SHA384_ALGORITHM</strong></dt> <dt> &quot; SHA384 &quot; </dt> </dl></td>
<td style="text-align: left;">Der sichere 384-Bit-Hashalgorithmus. <br/> Standard: FIPS 180-2, FIPS 198.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_SHA512_ALGORITHM"></span><span id="bcrypt_sha512_algorithm"></span><dl> <dt><strong>BCRYPT_SHA512_ALGORITHM</strong></dt> <dt> &quot; SHA512 &quot; </dt> </dl></td>
<td style="text-align: left;">Der sichere 512-Bit-Hashalgorithmus. <br/> Standard: FIPS 180-2, FIPS 198.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_SP800108_CTR_HMAC_ALGORITHM"></span><span id="bcrypt_sp800108_ctr_hmac_algorithm"></span><dl> <dt><strong>BCRYPT_SP800108_CTR_HMAC_ALGORITHM</strong></dt> <dt>L &quot; SP800_108_CTR_HMAC &quot; </dt> </dl></td>
<td style="text-align: left;">Indikatormodus, HMAC-Schlüsselableitungsfunktionsalgorithmus (Hash-Based Message Authentication Code). Wird von den <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>Funktionen BCryptKeyDerivation</strong></a> und <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>NCryptKeyDerivation</strong></a> verwendet.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_SP80056A_CONCAT_ALGORITHM"></span><span id="bcrypt_sp80056a_concat_algorithm"></span><dl> <dt><strong>BCRYPT_SP80056A_CONCAT_ALGORITHM</strong></dt> <dt>L &quot; SP800_56A_CONCAT &quot; </dt> </dl></td>
<td style="text-align: left;">Sp800-56A-Algorithmus für Schlüsselableitungsfunktionen. Wird von den <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>Funktionen BCryptKeyDerivation</strong></a> und <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>NCryptKeyDerivation</strong></a> verwendet.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="_BCRYPT_PBKDF2_ALGORITHM"></span><span id="_bcrypt_pbkdf2_algorithm"></span><dl> <dt> <strong>BCRYPT_PBKDF2_ALGORITHM</strong> </dt> <dt>L &quot; PBKDF2 &quot; </dt> </dl></td>
<td style="text-align: left;">Kennwortbasierter Schlüsselableitungsfunktion 2-Algorithmus (PBKDF2). Wird von den <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>Funktionen BCryptKeyDerivation</strong></a> und <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>NCryptKeyDerivation</strong></a> verwendet.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_ECDSA_ALGORITHM"></span><span id="bcrypt_ecdsa_algorithm"></span><dl> <dt><strong>BCRYPT_ECDSA_ALGORITHM</strong></dt> <dt> &quot; ECDSA &quot; </dt> </dl></td>
<td style="text-align: left;">Generischer Algorithmus für digitale Signatur mit elliptischen Primkurven <strong>(weitere Informationen</strong> finden Sie in den Anmerkungen). <br/> Standard: ANSI X9.62.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_ECDH_ALGORITHM"></span><span id="bcrypt_ecdh_algorithm"></span><dl> <dt><strong>BCRYPT_ECDH_ALGORITHM</strong></dt> <dt> &quot; ECDH &quot; </dt> </dl></td>
<td style="text-align: left;">Generische elliptische Primkurve Diffie-Hellman Schlüsselaustauschalgorithmus (weitere <strong>Informationen</strong> finden Sie in den Anmerkungen). <br/> Standard: SP800-56A.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_XTS_AES_ALGORITHM"></span><span id="bcrypt_xts_aes_algorithm"></span><dl> <dt><strong>BCRYPT_XTS_AES_ALGORITHM</strong></dt> <dt> &quot; XTS-AES &quot; </dt> </dl></td>
<td style="text-align: left;">Der erweiterte symmetrische Verschlüsselungsalgorithmus für den Verschlüsselungsstandard im XTS-Modus. <br/> Standard: SP-800-38E, IEEE Std 1619-2007.<br/> <strong>Windows 10:</strong> Die Unterstützung für diesen Algorithmus beginnt.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Hinweise

Um **BCRYPT \_ ECDSA \_ ALGORITM** oder **BCRYPT \_ ECDH \_ ALGORITHM** zu verwenden, rufen Sie [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) mit **entweder BCRYPT \_ ECDSA \_ ALGORITHM** oder **BCRYPT \_ ECDH \_ ALGORITHM** als *pszAlgId auf.* Verwenden Sie [**dann BCryptSetProperty,**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) um die **Eigenschaft BCRYPT \_ ECC CURVE \_ \_ NAME** auf einen benannten Algorithmus zu setzen, der unter Benannte CNG-Kurven aufgeführt ist.

Um benutzerdefinierte Elliptic Curve-Parameter direkt zu anbieter, verwenden Sie [**BCryptSetProperty,**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) um die **BCRYPT \_ ECC \_ PARAMETERS-Eigenschaft** festzulegen. Laden Sie [das Windows 10 Cryptographic Provider Developer Kit (CPDK) herunter,](https://www.microsoft.com/download/details.aspx?id=30688) um weitere Informationen zu erhalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Bcrypt.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider)
</dt> <dt>

[**NCryptCreatePersistedKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey)
</dt> </dl>

 

 




