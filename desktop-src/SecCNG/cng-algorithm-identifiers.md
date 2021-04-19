---
description: Wird zum Identifizieren von Standard Verschlüsselungsalgorithmen in verschiedenen CNG-Funktionen und-Strukturen verwendet, wie z. b. der Crypt- \_ Schnittstelle \_ reg
ms.assetid: a05ae7e6-d882-4287-9990-23e4cd340b05
title: CNG-Algorithmusbezeichner (bcrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba244f2a815933322793fdd572ed7a4e69256a0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342631"
---
# <a name="cng-algorithm-identifiers"></a>CNG-Algorithmusbezeichner

Die folgenden Bezeichner werden verwendet, um Standard Verschlüsselungsalgorithmen in verschiedenen CNG-Funktionen und-Strukturen zu identifizieren, wie z. b. die Struktur der [**crypt- \_ Schnittstellen \_ reg**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_interface_reg) . Anbieter von Drittanbietern verfügen möglicherweise über zusätzliche Algorithmen, die Sie unterstützen.



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
<td style="text-align: left;">Der Algorithmus für die symmetrische Verschlüsselung mit Triple Data Encryption Standard.<br/> Standard: SP800-67, SP800-38A<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_3DES_112_ALGORITHM"></span><span id="bcrypt_3des_112_algorithm"></span><dl> <dt><strong>BCRYPT_3DES_112_ALGORITHM</strong></dt> <dt> &quot; 3DES_112 &quot; </dt> </dl></td>
<td style="text-align: left;">Der standardmäßige symmetrische Verschlüsselungsalgorithmus für die 112-Bit-Datenverschlüsselung.<br/> Standard: SP800-67, SP800-38A<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_AES_ALGORITHM"></span><span id="bcrypt_aes_algorithm"></span><dl> <dt><strong>BCRYPT_AES_ALGORITHM</strong></dt> <dt> &quot; AES &quot; </dt> </dl></td>
<td style="text-align: left;">Der symmetrische Verschlüsselungsalgorithmus für den erweiterten Verschlüsselungsstandard.<br/> Standard: FPS 197<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_AES_CMAC_ALGORITHM"></span><span id="bcrypt_aes_cmac_algorithm"></span><dl> <dt><strong>BCRYPT_AES_CMAC_ALGORITHM</strong></dt> <dt> &quot; AES-CMAC &quot; </dt> </dl></td>
<td style="text-align: left;">Der AES-Verschlüsselungsalgorithmus (Advanced Encryption Standard), der symmetrische Verschlüsselungsalgorithmus (Message Authentication Code, CMAC) ist.<br/> Standard: SP 800-38b<br/> <strong>Windows 8:</strong> Die Unterstützung für diesen Algorithmus beginnt.<br/> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_AES_GMAC_ALGORITHM"></span><span id="bcrypt_aes_gmac_algorithm"></span><dl> <dt><strong>BCRYPT_AES_GMAC_ALGORITHM</strong></dt> <dt> &quot; AES-GMAC &quot; </dt> </dl></td>
<td style="text-align: left;">Der symmetrische Verschlüsselungsalgorithmus für den Advanced Encryption Standard (AES).<br/> Standard: SP800-38d<br/> <strong>Windows Vista:</strong> Dieser Algorithmus wird ab Windows Vista mit SP1 unterstützt.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_CAPI_KDF_ALGORITHM"></span><span id="bcrypt_capi_kdf_algorithm"></span><dl> <dt><strong>BCRYPT_CAPI_KDF_ALGORITHM</strong></dt> <dt>L &quot; CAPI_KDF &quot; </dt> </dl></td>
<td style="text-align: left;">Algorithmus der Kryptografiefunktion der kryptografieapi (CAPI). Wird von den Funktionen " <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>bcryptkeyderivations</strong></a> " und " <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>ncryptkeyderivations</strong></a> " verwendet.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_DES_ALGORITHM"></span><span id="bcrypt_des_algorithm"></span><dl> <dt><strong>BCRYPT_DES_ALGORITHM</strong></dt> <dt> &quot; des &quot; </dt> </dl></td>
<td style="text-align: left;">Der symmetrische Verschlüsselungsalgorithmus für den Daten Verschlüsselungsstandard.<br/> Standard: FPS 46-3, FPS 81<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_DESX_ALGORITHM"></span><span id="bcrypt_desx_algorithm"></span><dl> <dt><strong>BCRYPT_DESX_ALGORITHM</strong></dt> <dt> &quot; DESX &quot; </dt> </dl></td>
<td style="text-align: left;">Der Algorithmus für die symmetrische Verschlüsselung der erweiterten Datenverschlüsselung Standard.<br/> Standard: keine<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_DH_ALGORITHM"></span><span id="bcrypt_dh_algorithm"></span><dl> <dt><strong>BCRYPT_DH_ALGORITHM</strong></dt> <dt> &quot; dh &quot; </dt> </dl></td>
<td style="text-align: left;">Der Diffie-Hellman Schlüsselaustausch Algorithmus.<br/> Standard: PKCS-#3<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_DSA_ALGORITHM"></span><span id="bcrypt_dsa_algorithm"></span><dl> <dt><strong>BCRYPT_DSA_ALGORITHM</strong></dt> <dt> &quot; DSA &quot; </dt> </dl></td>
<td style="text-align: left;">Der Algorithmus für die digitale Signatur.<br/> Standard: FPS 186-2<br/> <strong>Windows 8:</strong> Ab Windows 8 unterstützt dieser Algorithmus die Verwendung von "fps 186-3". Schlüssel, die kleiner oder gleich 1024 Bits sind, entsprechen dem Wert von "fps 186-2", und die Schlüssel sind größer als 1024 186-3 bis "".<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_ECDH_P256_ALGORITHM"></span><span id="bcrypt_ecdh_p256_algorithm"></span><dl> <dt><strong>BCRYPT_ECDH_P256_ALGORITHM</strong></dt> <dt> &quot; ECDH_P256 &quot; </dt> </dl></td>
<td style="text-align: left;">Die 256-Bit-primelliptische Kurve Diffie-Hellman Algorithmus für den Schlüsselaustausch.<br/> Standard: SP800-56a<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_ECDH_P384_ALGORITHM"></span><span id="bcrypt_ecdh_p384_algorithm"></span><dl> <dt><strong>BCRYPT_ECDH_P384_ALGORITHM</strong></dt> <dt> &quot; ECDH_P384 &quot; </dt> </dl></td>
<td style="text-align: left;">Die 384-Bit-primelliptische Kurve Diffie-Hellman Algorithmus für den Schlüsselaustausch.<br/> Standard: SP800-56a<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_ECDH_P521_ALGORITHM"></span><span id="bcrypt_ecdh_p521_algorithm"></span><dl> <dt><strong>BCRYPT_ECDH_P521_ALGORITHM</strong></dt> <dt> &quot; ECDH_P521 &quot; </dt> </dl></td>
<td style="text-align: left;">Die 521-Bit-primelliptische Kurve Diffie-Hellman Algorithmus für den Schlüsselaustausch.<br/> Standard: SP800-56a<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_ECDSA_P256_ALGORITHM"></span><span id="bcrypt_ecdsa_p256_algorithm"></span><dl> <dt><strong>BCRYPT_ECDSA_P256_ALGORITHM</strong></dt> <dt> &quot; ECDSA_P256 &quot; </dt> </dl></td>
<td style="text-align: left;">Der 256-Bit-primelliptische Kurve Digital Signature-Algorithmus (fps 186-2).<br/> Standard: FPS 186-2, x 9.62<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_ECDSA_P384_ALGORITHM"></span><span id="bcrypt_ecdsa_p384_algorithm"></span><dl> <dt><strong>BCRYPT_ECDSA_P384_ALGORITHM</strong></dt> <dt> &quot; ECDSA_P384 &quot; </dt> </dl></td>
<td style="text-align: left;">Der 384-Bit-primelliptische Kurve Digital Signature-Algorithmus (fps 186-2).<br/> Standard: FPS 186-2, x 9.62<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_ECDSA_P521_ALGORITHM"></span><span id="bcrypt_ecdsa_p521_algorithm"></span><dl> <dt><strong>BCRYPT_ECDSA_P521_ALGORITHM</strong></dt> <dt> &quot; ECDSA_P521 &quot; </dt> </dl></td>
<td style="text-align: left;">Der 521-Bit-primelliptische Kurve Digital Signature-Algorithmus (fps 186-2).<br/> Standard: FPS 186-2, x 9.62<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_MD2_ALGORITHM"></span><span id="bcrypt_md2_algorithm"></span><dl> <dt><strong>BCRYPT_MD2_ALGORITHM</strong></dt> <dt> &quot; MD2 &quot; </dt> </dl></td>
<td style="text-align: left;">Der MD2-Hash Algorithmus.<br/> Standard: RFC 1319<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_MD4_ALGORITHM"></span><span id="bcrypt_md4_algorithm"></span><dl> <dt><strong>BCRYPT_MD4_ALGORITHM</strong></dt> <dt> &quot; MD4 &quot; </dt> </dl></td>
<td style="text-align: left;">Der MD4-Hash Algorithmus.<br/> Standard: RFC 1320<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_MD5_ALGORITHM"></span><span id="bcrypt_md5_algorithm"></span><dl> <dt><strong>BCRYPT_MD5_ALGORITHM</strong></dt> <dt> &quot; MD5 &quot; </dt> </dl></td>
<td style="text-align: left;">Der MD5-Hash Algorithmus.<br/> Standard: RFC 1321<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_RC2_ALGORITHM"></span><span id="bcrypt_rc2_algorithm"></span><dl> <dt><strong>BCRYPT_RC2_ALGORITHM</strong></dt> <dt> &quot; RC2 &quot; </dt> </dl></td>
<td style="text-align: left;">Der RC2-Block für symmetrische Verschlüsselungsalgorithmen.<br/> Standard: RFC 2268<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_RC4_ALGORITHM"></span><span id="bcrypt_rc4_algorithm"></span><dl> <dt><strong>BCRYPT_RC4_ALGORITHM</strong></dt> <dt> &quot; RC4 &quot; </dt> </dl></td>
<td style="text-align: left;">Der symmetrische RC4-Verschlüsselungsalgorithmus.<br/> Standard: verschiedene<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_RNG_ALGORITHM"></span><span id="bcrypt_rng_algorithm"></span><dl> <dt><strong>BCRYPT_RNG_ALGORITHM</strong></dt> <dt> &quot; RNG &quot; </dt> </dl></td>
<td style="text-align: left;">Der Algorithmus für Zufallszahlengenerator.<br/> Standard: FPS 186-2, FPS 140-2, NIST SP 800-90<br/>
<blockquote>
[!Note]<br />
Ab Windows Vista mit SP1 und Windows Server 2008 basiert der Zufallszahlen-Generator auf dem AES-gegen Modus, der im NIST SP 800-90-Standard angegeben ist.
</blockquote>
<br/> <strong>Windows Vista:</strong> Der Zufallszahlen-Generator basiert auf dem Hash basierten Zufallszahlen-Generator, der im Standard-Standard für 186-2 die Standard-ID angegeben ist.<br/> <strong>Windows 8:</strong> Ab Windows 8 unterstützt der RNG-Algorithmus die Verwendung von "fps 186-3". Schlüssel, die kleiner oder gleich 1024 Bits sind, entsprechen dem Wert von "fps 186-2", und die Schlüssel sind größer als 1024 186-3 bis "".<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_RNG_DUAL_EC_ALGORITHM"></span><span id="bcrypt_rng_dual_ec_algorithm"></span><dl> <dt><strong>BCRYPT_RNG_DUAL_EC_ALGORITHM</strong></dt> <dt> &quot; dualecrng &quot; </dt> </dl></td>
<td style="text-align: left;">Der Dual Elliptic Curve Random-Number Generator-Algorithmus. <br/> Standard: SP800-90.<br/> <strong>Windows 8:</strong> Ab Windows 8 unterstützt der EC-RNG-Algorithmus die Verwendung von "fps 186-3". Schlüssel, die kleiner oder gleich 1024 Bits sind, entsprechen dem Wert von "fps 186-2", und die Schlüssel sind größer als 1024 186-3 bis "".<br/> <strong>Windows 10:</strong> Ab Windows 10 wurde der Dual Elliptic Curve Random Number Generator-Algorithmus entfernt. Die vorhandene Verwendung dieses Algorithmus funktioniert weiterhin. der Zufallszahlen-Generator basiert jedoch auf dem AES-Counter-Modus, der im NIST SP 800-90-Standard angegeben ist. Neuer Code sollte <strong>BCRYPT_RNG_ALGORITHM</strong>verwenden, und es wird empfohlen, dass vorhandener Code so geändert wird, dass er <strong>BCRYPT_RNG_ALGORITHM</strong>verwendet. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_RNG_FIPS186_DSA_ALGORITHM"></span><span id="bcrypt_rng_fips186_dsa_algorithm"></span><dl> <dt><strong>BCRYPT_RNG_FIPS186_DSA_ALGORITHM</strong></dt> <dt> &quot; FIPS186DSARNG &quot; </dt> </dl></td>
<td style="text-align: left;">Der für DSA geeignete Algorithmus für Zufallszahlen-Generator (Digital Signature-Algorithmus). <br/> Standard: FPS 186-2.<br/> <strong>Windows 8:</strong> Die Unterstützung für "fps 186-3" wird gestartet.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_RSA_ALGORITHM"></span><span id="bcrypt_rsa_algorithm"></span><dl> <dt><strong>BCRYPT_RSA_ALGORITHM</strong></dt> <dt> &quot; RSA &quot; </dt> </dl></td>
<td style="text-align: left;">Der RSA-Algorithmus für öffentliche Schlüssel. <br/> Standard: PKCS #1 v 1.5 und v 2.0.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_RSA_SIGN_ALGORITHM"></span><span id="bcrypt_rsa_sign_algorithm"></span><dl> <dt><strong>BCRYPT_RSA_SIGN_ALGORITHM</strong></dt> <dt> &quot; RSA_SIGN &quot; </dt> </dl></td>
<td style="text-align: left;">Der RSA-Signatur Algorithmus. Dieser Algorithmus wird derzeit nicht unterstützt. Sie können den <strong>BCRYPT_RSA_ALGORITHM</strong> -Algorithmus verwenden, um RSA-Signatur Vorgänge auszuführen. <br/> Standard: PKCS #1 v 1.5 und v 2.0.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_SHA1_ALGORITHM"></span><span id="bcrypt_sha1_algorithm"></span><dl> <dt><strong>BCRYPT_SHA1_ALGORITHM</strong></dt> <dt> &quot; SHA1 &quot; </dt> </dl></td>
<td style="text-align: left;">Der 160-Bit-sichere Hash Algorithmus. <br/> Standard: FPS 180-2, FPS 198.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_SHA256_ALGORITHM"></span><span id="bcrypt_sha256_algorithm"></span><dl> <dt><strong>BCRYPT_SHA256_ALGORITHM</strong></dt> <dt> &quot; SHA256 &quot; </dt> </dl></td>
<td style="text-align: left;">Der 256-Bit-sichere Hash Algorithmus.<br/> Standard: FPS 180-2, FPS 198.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_SHA384_ALGORITHM"></span><span id="bcrypt_sha384_algorithm"></span><dl> <dt><strong>BCRYPT_SHA384_ALGORITHM</strong></dt> <dt> &quot; SHA384 &quot; </dt> </dl></td>
<td style="text-align: left;">Der 384-Bit-sichere Hash Algorithmus. <br/> Standard: FPS 180-2, FPS 198.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_SHA512_ALGORITHM"></span><span id="bcrypt_sha512_algorithm"></span><dl> <dt><strong>BCRYPT_SHA512_ALGORITHM</strong></dt> <dt> &quot; SHA512 &quot; </dt> </dl></td>
<td style="text-align: left;">Der 512-Bit-sichere Hash Algorithmus. <br/> Standard: FPS 180-2, FPS 198.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_SP800108_CTR_HMAC_ALGORITHM"></span><span id="bcrypt_sp800108_ctr_hmac_algorithm"></span><dl> <dt><strong>BCRYPT_SP800108_CTR_HMAC_ALGORITHM</strong></dt> <dt>L &quot; SP800_108_CTR_HMAC &quot; </dt> </dl></td>
<td style="text-align: left;">Counter-Modus, Hash basierter Nachrichten Authentifizierungscode (HMAC) Key derivations Function-Algorithmus. Wird von den Funktionen " <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>bcryptkeyderivations</strong></a> " und " <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>ncryptkeyderivations</strong></a> " verwendet.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_SP80056A_CONCAT_ALGORITHM"></span><span id="bcrypt_sp80056a_concat_algorithm"></span><dl> <dt><strong>BCRYPT_SP80056A_CONCAT_ALGORITHM</strong></dt> <dt>L &quot; SP800_56A_CONCAT &quot; </dt> </dl></td>
<td style="text-align: left;">SP800-56a schlüsselabderivationsfunktions-Algorithmus. Wird von den Funktionen " <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>bcryptkeyderivations</strong></a> " und " <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>ncryptkeyderivations</strong></a> " verwendet.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="_BCRYPT_PBKDF2_ALGORITHM"></span><span id="_bcrypt_pbkdf2_algorithm"></span><dl> <dt> <strong>BCRYPT_PBKDF2_ALGORITHM</strong> </dt> <dt>L &quot; PBKDF2 &quot; </dt> </dl></td>
<td style="text-align: left;">PBKDF2-Algorithmus (Password-Based Key derivations Funktion 2). Wird von den Funktionen " <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>bcryptkeyderivations</strong></a> " und " <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>ncryptkeyderivations</strong></a> " verwendet.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_ECDSA_ALGORITHM"></span><span id="bcrypt_ecdsa_algorithm"></span><dl> <dt><strong>BCRYPT_ECDSA_ALGORITHM</strong></dt> <dt> &quot; ECDSA &quot; </dt> </dl></td>
<td style="text-align: left;">Generischer generischer Signatur Algorithmus der elliptischen Kurve <strong>(Weitere Informationen finden Sie</strong> in den Hinweisen). <br/> Standard: ANSI x 9.62.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_ECDH_ALGORITHM"></span><span id="bcrypt_ecdh_algorithm"></span><dl> <dt><strong>BCRYPT_ECDH_ALGORITHM</strong></dt> <dt> &quot; ECDH &quot; </dt> </dl></td>
<td style="text-align: left;">Generische primelliptische Kurve Diffie-Hellman Algorithmus für den Schlüsselaustausch <strong>(Weitere Informationen</strong> finden Sie in den Hinweisen). <br/> Standard: SP800-56a.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_XTS_AES_ALGORITHM"></span><span id="bcrypt_xts_aes_algorithm"></span><dl> <dt><strong>BCRYPT_XTS_AES_ALGORITHM</strong></dt> <dt> &quot; XTS-AES &quot; </dt> </dl></td>
<td style="text-align: left;">Der symmetrische Verschlüsselungsalgorithmus für den erweiterten Verschlüsselungsstandard im XTS-Modus. <br/> Standard: SP-800-38E, IEEE Std 1619-2007.<br/> <strong>Windows 10:</strong> Die Unterstützung für diesen Algorithmus beginnt.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Bemerkungen

Um **bcrypt \_ ECDSA \_ ALGORITM** oder **bcrypt \_ ECDH- \_ Algorithmus** zu verwenden, nennen Sie [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) mit einem **bcrypt \_ ECDSA- \_ Algorithmus** oder einem **bcrypt \_ ECDH- \_ Algorithmus** als *pszalgid*. Verwenden Sie dann [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) , um die Eigenschaft **bcrypt \_ ECC- \_ Kurven \_ Name** auf einen benannten Algorithmus festzulegen, der in CNG benannte Kurven aufgeführt ist.

Wenn Sie benutzerdefinierte elliptische Kurven Parameter Direktanbieter verwenden möchten, legen Sie mit [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) die Eigenschaft **bcrypt \_ ECC- \_ Parameter** fest. Laden Sie das [Windows 10 Cryptographic Provider Developer Kit (cpdk)](https://www.microsoft.com/download/details.aspx?id=30688) herunter, um weitere Informationen zu finden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Bcrypt. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider)
</dt> <dt>

[**Ncryptkreatepersistedkey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey)
</dt> </dl>

 

 




