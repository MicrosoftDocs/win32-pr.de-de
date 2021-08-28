---
description: Wird verwendet, um Standardverschlüsselungsalgorithmen in verschiedenen CNG-Funktionen und -Strukturen zu identifizieren, z. B. der CRYPT \_ INTERFACE \_ REG-Struktur.
ms.assetid: a05ae7e6-d882-4287-9990-23e4cd340b05
title: CNG-Algorithmusbezeichner (Bcrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e853d7cd0d1dd34104d3cffa20f301c11e45304c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481886"
---
# <a name="cng-algorithm-identifiers"></a>CNG-Algorithmusbezeichner

Die folgenden Bezeichner werden verwendet, um Standardverschlüsselungsalgorithmen in verschiedenen CNG-Funktionen und -Strukturen zu identifizieren, z. B. der [**CRYPT \_ INTERFACE \_ REG-Struktur.**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_interface_reg) Drittanbieter verfügen möglicherweise über zusätzliche Algorithmen, die sie unterstützen.




| Konstante/Wert | BESCHREIBUNG | 
|----------------|-------------|
| <span id="BCRYPT_3DES_ALGORITHM"></span><span id="bcrypt_3des_algorithm"></span><dl><dt><strong>BCRYPT_3DES_ALGORITHM</strong></dt><dt>"3DES"</dt></dl> | Der symmetrische Verschlüsselungsalgorithmus für die Verschlüsselung mit dreifacher Datenverschlüsselung.<br /> Standard: SP800-67, SP800-38A<br /> | 
| <span id="BCRYPT_3DES_112_ALGORITHM"></span><span id="bcrypt_3des_112_algorithm"></span><dl><dt><strong>BCRYPT_3DES_112_ALGORITHM</strong></dt><dt>"3DES_112"</dt></dl> | Der symmetrische Verschlüsselungsalgorithmus für die 112-Bit-Verschlüsselung mit dreifacher Datenverschlüsselung.<br /> Standard: SP800-67, SP800-38A<br /> | 
| <span id="BCRYPT_AES_ALGORITHM"></span><span id="bcrypt_aes_algorithm"></span><dl><dt><strong>BCRYPT_AES_ALGORITHM</strong></dt><dt>"AES"</dt></dl> | Der erweiterte symmetrische Verschlüsselungsalgorithmus für den Verschlüsselungsstandard.<br /> Standard: FIPS 197<br /> | 
| <span id="BCRYPT_AES_CMAC_ALGORITHM"></span><span id="bcrypt_aes_cmac_algorithm"></span><dl><dt><strong>BCRYPT_AES_CMAC_ALGORITHM</strong></dt><dt>"AES-CMAC"</dt></dl> | Der symmetrische Verschlüsselungsalgorithmus des erweiterten Verschlüsselungsstandards (Advanced Encryption Standard, AES), der auf verschlüsselungsbasiertem Nachrichtenauthentifizierungscode (Message Authentication Code, CMAC) basiert.<br /> Standard: SP 800-38B<br /><strong>Windows 8:</strong> Die Unterstützung für diesen Algorithmus beginnt.<br /><br /> | 
| <span id="BCRYPT_AES_GMAC_ALGORITHM"></span><span id="bcrypt_aes_gmac_algorithm"></span><dl><dt><strong>BCRYPT_AES_GMAC_ALGORITHM</strong></dt><dt>"AES-GMAC"</dt></dl> | Der symmetrische Verschlüsselungsalgorithmus advanced encryption standard (AES) Galois Message Authentication Code (GMAC).<br /> Standard: SP800-38D<br /><strong>Windows Vista:</strong> Dieser Algorithmus wird ab Windows Vista mit SP1 unterstützt.<br /> | 
| <span id="BCRYPT_CAPI_KDF_ALGORITHM"></span><span id="bcrypt_capi_kdf_algorithm"></span><dl><dt><strong>BCRYPT_CAPI_KDF_ALGORITHM</strong></dt><dt>L"CAPI_KDF"</dt></dl> | Krypto-API -Schlüsselableitungsfunktionsalgorithmus (CAPI). Wird von den <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>Funktionen BCryptKeyDerivation</strong></a> und <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>NCryptKeyDerivation</strong></a> verwendet.<br /> | 
| <span id="BCRYPT_DES_ALGORITHM"></span><span id="bcrypt_des_algorithm"></span><dl><dt><strong>BCRYPT_DES_ALGORITHM</strong></dt><dt>"DES"</dt></dl> | Der symmetrische Standardverschlüsselungsalgorithmus für die Datenverschlüsselung.<br /> Standard: FIPS 46-3, FIPS 81<br /> | 
| <span id="BCRYPT_DESX_ALGORITHM"></span><span id="bcrypt_desx_algorithm"></span><dl><dt><strong>BCRYPT_DESX_ALGORITHM</strong></dt><dt>"DESX"</dt></dl> | Der symmetrische Standardverschlüsselungsalgorithmus für die erweiterte Datenverschlüsselung.<br /> Standard: Keine<br /> | 
| <span id="BCRYPT_DH_ALGORITHM"></span><span id="bcrypt_dh_algorithm"></span><dl><dt><strong>BCRYPT_DH_ALGORITHM</strong></dt><dt>"DH"</dt></dl> | Der Diffie-Hellman Schlüsselaustauschalgorithmus.<br /> Standard: PKCS-#3<br /> | 
| <span id="BCRYPT_DSA_ALGORITHM"></span><span id="bcrypt_dsa_algorithm"></span><dl><dt><strong>BCRYPT_DSA_ALGORITHM</strong></dt><dt>"DSA"</dt></dl> | Der Algorithmus für digitale Signaturen.<br /> Standard: FIPS 186-2<br /><strong>Windows 8:</strong> Ab Windows 8 unterstützt dieser Algorithmus FIPS 186-3. Schlüssel kleiner oder gleich 1.024 Bits sind fips 186-2 und Schlüssel größer als 1024 bis FIPS 186-3.<br /> | 
| <span id="BCRYPT_ECDH_P256_ALGORITHM"></span><span id="bcrypt_ecdh_p256_algorithm"></span><dl><dt><strong>BCRYPT_ECDH_P256_ALGORITHM</strong></dt><dt>"ECDH_P256"</dt></dl> | Die elliptische 256-Bit-Primkurve Diffie-Hellman Schlüsselaustauschalgorithmus.<br /> Standard: SP800-56A<br /> | 
| <span id="BCRYPT_ECDH_P384_ALGORITHM"></span><span id="bcrypt_ecdh_p384_algorithm"></span><dl><dt><strong>BCRYPT_ECDH_P384_ALGORITHM</strong></dt><dt>"ECDH_P384"</dt></dl> | Die elliptische 384-Bit-Primkurve Diffie-Hellman Schlüsselaustauschalgorithmus.<br /> Standard: SP800-56A<br /> | 
| <span id="BCRYPT_ECDH_P521_ALGORITHM"></span><span id="bcrypt_ecdh_p521_algorithm"></span><dl><dt><strong>BCRYPT_ECDH_P521_ALGORITHM</strong></dt><dt>"ECDH_P521"</dt></dl> | Die elliptische 521-Bit-Primkurve Diffie-Hellman Schlüsselaustauschalgorithmus.<br /> Standard: SP800-56A<br /> | 
| <span id="BCRYPT_ECDSA_P256_ALGORITHM"></span><span id="bcrypt_ecdsa_p256_algorithm"></span><dl><dt><strong>BCRYPT_ECDSA_P256_ALGORITHM</strong></dt><dt>"ECDSA_P256"</dt></dl> | Der 256-Bit-Algorithmus für die digitale Signatur der elliptischen Primkurve (FIPS 186-2).<br /> Standard: FIPS 186-2, X9.62<br /> | 
| <span id="BCRYPT_ECDSA_P384_ALGORITHM"></span><span id="bcrypt_ecdsa_p384_algorithm"></span><dl><dt><strong>BCRYPT_ECDSA_P384_ALGORITHM</strong></dt><dt>"ECDSA_P384"</dt></dl> | Der 384-Bit-Algorithmus für die digitale Signatur der elliptischen Primkurve (FIPS 186-2).<br /> Standard: FIPS 186-2, X9.62<br /> | 
| <span id="BCRYPT_ECDSA_P521_ALGORITHM"></span><span id="bcrypt_ecdsa_p521_algorithm"></span><dl><dt><strong>BCRYPT_ECDSA_P521_ALGORITHM</strong></dt><dt>"ECDSA_P521"</dt></dl> | Der 521-Bit-Algorithmus für die digitale Signatur der elliptischen Primkurve (FIPS 186-2).<br /> Standard: FIPS 186-2, X9.62<br /> | 
| <span id="BCRYPT_MD2_ALGORITHM"></span><span id="bcrypt_md2_algorithm"></span><dl><dt><strong>BCRYPT_MD2_ALGORITHM</strong></dt><dt>"MD2"</dt></dl> | Der MD2-Hashalgorithmus.<br /> Standard: RFC 1319<br /> | 
| <span id="BCRYPT_MD4_ALGORITHM"></span><span id="bcrypt_md4_algorithm"></span><dl><dt><strong>BCRYPT_MD4_ALGORITHM</strong></dt><dt>"MD4"</dt></dl> | Der MD4-Hashalgorithmus.<br /> Standard: RFC 1320<br /> | 
| <span id="BCRYPT_MD5_ALGORITHM"></span><span id="bcrypt_md5_algorithm"></span><dl><dt><strong>BCRYPT_MD5_ALGORITHM</strong></dt><dt>"MD5"</dt></dl> | Der MD5-Hashalgorithmus.<br /> Standard: RFC 1321<br /> | 
| <span id="BCRYPT_RC2_ALGORITHM"></span><span id="bcrypt_rc2_algorithm"></span><dl><dt><strong>BCRYPT_RC2_ALGORITHM</strong></dt><dt>"RC2"</dt></dl> | Der symmetrische Verschlüsselungsalgorithmus des RC2-Blocks.<br /> Standard: RFC 2268<br /> | 
| <span id="BCRYPT_RC4_ALGORITHM"></span><span id="bcrypt_rc4_algorithm"></span><dl><dt><strong>BCRYPT_RC4_ALGORITHM</strong></dt><dt>"RC4"</dt></dl> | Der symmetrische RC4-Verschlüsselungsalgorithmus.<br /> Standard: Verschiedene<br /> | 
| <span id="BCRYPT_RNG_ALGORITHM"></span><span id="bcrypt_rng_algorithm"></span><dl><dt><strong>BCRYPT_RNG_ALGORITHM</strong></dt><dt>"RNG"</dt></dl> | Der Algorithmus des Zufallszahlengenerators.<br /> Standard: FIPS 186-2, FIPS 140-2, NIST SP 800-90<br /><blockquote>[!Note]<br />Ab Windows Vista mit SP1 und Windows Server 2008 basiert der Zufallszahlengenerator auf dem im NIST SP 800-90-Standard angegebenen AES-Indikatormodus.</blockquote><br /><strong>Windows Vista:</strong> Der Zufallszahlengenerator basiert auf dem hashbasierten Zufallszahlengenerator, der im FIPS 186-2-Standard angegeben ist.<br /><strong>Windows 8:</strong> Ab Windows 8 unterstützt der RNG-Algorithmus FIPS 186-3. Schlüssel kleiner oder gleich 1.024 Bits sind fips 186-2 und Schlüssel größer als 1024 bis FIPS 186-3.<br /> | 
| <span id="BCRYPT_RNG_DUAL_EC_ALGORITHM"></span><span id="bcrypt_rng_dual_ec_algorithm"></span><dl><dt><strong>BCRYPT_RNG_DUAL_EC_ALGORITHM</strong></dt><dt>"DUALECRNG"</dt></dl> | Der Generatoralgorithmus für die duale elliptische Kurve mit Zufallszahlen. <br /> Standard: SP800-90.<br /><strong>Windows 8:</strong> Ab Windows 8 unterstützt der EC RNG-Algorithmus FIPS 186-3. Schlüssel kleiner oder gleich 1.024 Bits sind fips 186-2 und Schlüssel größer als 1024 bis FIPS 186-3.<br /><strong>Windows 10:</strong> Ab Windows 10 wurde der Algorithmus des Generators für die duale Elliptic Curve-Zufallszahl entfernt. Vorhandene Verwendungen dieses Algorithmus funktionieren weiterhin. Der Zufallszahlengenerator basiert jedoch auf dem im NIST SP 800-90-Standard angegebenen AES-Indikatormodus. Neuer Code sollte <strong>BCRYPT_RNG_ALGORITHM</strong>verwenden, und es wird empfohlen, vorhandenen Code so zu ändern, dass <strong>er</strong>BCRYPT_RNG_ALGORITHM. <br /> | 
| <span id="BCRYPT_RNG_FIPS186_DSA_ALGORITHM"></span><span id="bcrypt_rng_fips186_dsa_algorithm"></span><dl><dt><strong>BCRYPT_RNG_FIPS186_DSA_ALGORITHM</strong></dt><dt>"FIPS186DSARNG"</dt></dl> | Der algorithmus für den Zufallszahlengenerator, der für DSA (Digital Signature Algorithm) geeignet ist. <br /> Standard: FIPS 186-2.<br /><strong>Windows 8:</strong> Die Unterstützung für FIPS 186-3 beginnt.<br /> | 
| <span id="BCRYPT_RSA_ALGORITHM"></span><span id="bcrypt_rsa_algorithm"></span><dl><dt><strong>BCRYPT_RSA_ALGORITHM</strong></dt><dt>"RSA"</dt></dl> | Der RSA-Algorithmus für öffentliche Schlüssel. <br /> Standard: PKCS #1 v1.5 und v2.0.<br /> | 
| <span id="BCRYPT_RSA_SIGN_ALGORITHM"></span><span id="bcrypt_rsa_sign_algorithm"></span><dl><dt><strong>BCRYPT_RSA_SIGN_ALGORITHM</strong></dt><dt>"RSA_SIGN"</dt></dl> | Der RSA-Signaturalgorithmus. Dieser Algorithmus wird derzeit nicht unterstützt. Sie können den <strong>algorithmus</strong> BCRYPT_RSA_ALGORITHM verwenden, um RSA-Signaturvorgänge durchzuführen. <br /> Standard: PKCS #1 v1.5 und v2.0.<br /> | 
| <span id="BCRYPT_SHA1_ALGORITHM"></span><span id="bcrypt_sha1_algorithm"></span><dl><dt><strong>BCRYPT_SHA1_ALGORITHM</strong></dt><dt>"SHA1"</dt></dl> | Der sichere 160-Bit-Hashalgorithmus. <br /> Standard: FIPS 180-2, FIPS 198.<br /> | 
| <span id="BCRYPT_SHA256_ALGORITHM"></span><span id="bcrypt_sha256_algorithm"></span><dl><dt><strong>BCRYPT_SHA256_ALGORITHM</strong></dt><dt>"SHA256"</dt></dl> | Der sichere 256-Bit-Hashalgorithmus.<br /> Standard: FIPS 180-2, FIPS 198.<br /> | 
| <span id="BCRYPT_SHA384_ALGORITHM"></span><span id="bcrypt_sha384_algorithm"></span><dl><dt><strong>BCRYPT_SHA384_ALGORITHM</strong></dt><dt>"SHA384"</dt></dl> | Der sichere 384-Bit-Hashalgorithmus. <br /> Standard: FIPS 180-2, FIPS 198.<br /> | 
| <span id="BCRYPT_SHA512_ALGORITHM"></span><span id="bcrypt_sha512_algorithm"></span><dl><dt><strong>BCRYPT_SHA512_ALGORITHM</strong></dt><dt>"SHA512"</dt></dl> | Der sichere 512-Bit-Hashalgorithmus. <br /> Standard: FIPS 180-2, FIPS 198.<br /> | 
| <span id="BCRYPT_SP800108_CTR_HMAC_ALGORITHM"></span><span id="bcrypt_sp800108_ctr_hmac_algorithm"></span><dl><dt><strong>BCRYPT_SP800108_CTR_HMAC_ALGORITHM</strong></dt><dt>L"SP800_108_CTR_HMAC"</dt></dl> | Indikatormodus, HMAC-Schlüsselableitungsfunktionsalgorithmus (Hash-Based Message Authentication Code). Wird von den <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>Funktionen BCryptKeyDerivation</strong></a> und <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>NCryptKeyDerivation</strong></a> verwendet.<br /> | 
| <span id="BCRYPT_SP80056A_CONCAT_ALGORITHM"></span><span id="bcrypt_sp80056a_concat_algorithm"></span><dl><dt><strong>BCRYPT_SP80056A_CONCAT_ALGORITHM</strong></dt><dt>L"SP800_56A_CONCAT"</dt></dl> | Sp800-56A-Algorithmus für Schlüsselableitungsfunktionen. Wird von den <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>Funktionen BCryptKeyDerivation</strong></a> und <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>NCryptKeyDerivation</strong></a> verwendet.<br /> | 
| <span id="_BCRYPT_PBKDF2_ALGORITHM"></span><span id="_bcrypt_pbkdf2_algorithm"></span><dl><dt><strong>BCRYPT_PBKDF2_ALGORITHM</strong></dt><dt>L"PBKDF2"</dt></dl> | Kennwortbasierter Schlüsselableitungsfunktion 2-Algorithmus (PBKDF2). Wird von den <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>Funktionen BCryptKeyDerivation</strong></a> und <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>NCryptKeyDerivation</strong></a> verwendet.<br /> | 
| <span id="BCRYPT_ECDSA_ALGORITHM"></span><span id="bcrypt_ecdsa_algorithm"></span><dl><dt><strong>BCRYPT_ECDSA_ALGORITHM</strong></dt><dt>"ECDSA"</dt></dl> | Generischer Algorithmus für digitale Signatur mit elliptischen Primkurven <strong>(weitere Informationen</strong> finden Sie in den Anmerkungen). <br /> Standard: ANSI X9.62.<br /> | 
| <span id="BCRYPT_ECDH_ALGORITHM"></span><span id="bcrypt_ecdh_algorithm"></span><dl><dt><strong>BCRYPT_ECDH_ALGORITHM</strong></dt><dt>"ECDH"</dt></dl> | Generische elliptische Primkurve Diffie-Hellman Schlüsselaustauschalgorithmus (weitere Informationen finden Sie in <strong>den</strong> Anmerkungen). <br /> Standard: SP800-56A.<br /> | 
| <span id="BCRYPT_XTS_AES_ALGORITHM"></span><span id="bcrypt_xts_aes_algorithm"></span><dl><dt><strong>BCRYPT_XTS_AES_ALGORITHM</strong></dt><dt>"XTS-AES"</dt></dl> | Der erweiterte symmetrische Verschlüsselungsalgorithmus für den Verschlüsselungsstandard im XTS-Modus. <br /> Standard: SP-800-38E, IEEE Std 1619-2007.<br /><strong>Windows 10:</strong> Die Unterstützung für diesen Algorithmus beginnt.<br /> | 




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

 

 




