---
description: Gibt einen Algorithmusbezeichner an.
ms.assetid: 557436b4-f7f1-4708-acc7-c6b47e6322ad
title: ALG_ID (Wincrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82f4b6c476a8ea6e61785a096abf33c357d9b024
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482396"
---
# <a name="alg_id"></a>ALG_ID

Der **ALG_ID** Datentyp gibt einen Algorithmusbezeichner an. Parameter dieses Datentyps werden an die meisten Funktionen in CryptoAPI übergeben.


```C++
typedef unsigned int ALG_ID;
```



In der folgenden Tabelle sind die derzeit definierten Algorithmusbezeichner aufgeführt. Autoren von benutzerdefinierten [*Kryptografiedienstanbietern (Cryptographic Service Providers,*](../secgloss/c-gly.md) CSPs) können neue Werte definieren. Außerdem sind die **ALG_ID,** die von benutzerdefinierten CSPs für die Schlüsselspezifikationen **AT_KEYEXCHANGE** und **AT_SIGNATURE** verwendet werden, anbieterabhängig. Aktuelle Zuordnungen folgen der Tabelle.




| Bezeichner | Wert | BESCHREIBUNG | 
|------------|-------|-------------|
| CALG_3DES | 0x00006603 | <a href="/windows/desktop/SecGloss/t-gly"><em>Triple</em></a> DES-Verschlüsselungsalgorithmus. | 
| CALG_3DES_112 | 0x00006609 | Triple <a href="/windows/desktop/SecGloss/t-gly"><em>DES-Verschlüsselung</em></a> mit zwei Schlüsseln mit einer effektiven Schlüssellänge von 112 Bits. | 
| CALG_AES | 0x00006611 | Advanced Encryption Standard (AES). Dieser Algorithmus wird vom <a href="microsoft-aes-cryptographic-provider.md">Microsoft AES-Kryptografieanbieter</a>unterstützt. | 
| CALG_AES_128 | 0x0000660e | 128-Bit-AES. Dieser Algorithmus wird vom <a href="microsoft-aes-cryptographic-provider.md">Microsoft AES-Kryptografieanbieter</a>unterstützt. | 
| CALG_AES_192 | 0x0000660f | 192-Bit-AES. Dieser Algorithmus wird vom <a href="microsoft-aes-cryptographic-provider.md">Microsoft AES-Kryptografieanbieter</a>unterstützt. | 
| CALG_AES_256 | 0x00006610 | 256-Bit-AES. Dieser Algorithmus wird vom <a href="microsoft-aes-cryptographic-provider.md">Microsoft AES-Kryptografieanbieter</a>unterstützt. | 
| CALG_AGREEDKEY_ANY | 0x0000aa03 | Temporärer Algorithmusbezeichner für Handles von Diffie-Hellman-bezogenen Schlüsseln. | 
| CALG_CYLINK_MEK | 0x0000660c | Ein Algorithmus zum Erstellen eines 40-Bit-DES-Schlüssels mit Paritätsbits und Schlüsselbits mit Null, sodass seine Schlüssellänge 64 Bit beträgt. Dieser Algorithmus wird vom <a href=""></a> <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>unterstützt. | 
| CALG_DES | 0x00006601 | DES-Verschlüsselungsalgorithmus. | 
| CALG_DESX | 0x00006604 | DESX-Verschlüsselungsalgorithmus. | 
| CALG_DH_EPHEM | 0x0000aa02 | Diffie-Hellman Algorithmus für den kurzlebigen Schlüsselaustausch. | 
| CALG_DH_SF | 0x0000aa01 | Diffie-Hellman Algorithmus zum Speichern und Weiterleiten des Schlüsselaustauschs. | 
| CALG_DSS_SIGN | 0x00002200 | Signaturalgorithmus für <a href="/windows/desktop/SecGloss/p-gly"><em>den öffentlichen DSA-Schlüssel.</em></a> | 
| CALG_ECDH | 0x0000aa05 | Elliptische Kurve Diffie-Hellman Schlüsselaustauschalgorithmus.<blockquote>[!Note]<br />Dieser Algorithmus wird nur über <a href="/windows/desktop/SecCNG/cng-portal">die Kryptografie-API unterstützt: Next Generation</a>.</blockquote><br /><strong>Windows Server 2003 und Windows XP:</strong> Dieser Algorithmus wird nicht unterstützt.<br /> | 
| CALG_ECDH_EPHEM | 0x0000ae06 | Kurzlebige elliptische Kurve Diffie-Hellman Schlüsselaustauschalgorithmus.<blockquote>[!Note]<br />Dieser Algorithmus wird nur über <a href="/windows/desktop/SecCNG/cng-portal">die Kryptografie-API unterstützt: Next Generation</a>.</blockquote><br /><strong>Windows Server 2003 und Windows XP:</strong> Dieser Algorithmus wird nicht unterstützt.<br /> | 
| CALG_ECDSA | 0x00002203 | Digitale Signaturalgorithmus für elliptische Kurve.<blockquote>[!Note]<br />Dieser Algorithmus wird nur über <a href="/windows/desktop/SecCNG/cng-portal">die Kryptografie-API unterstützt: Next Generation</a>.</blockquote><br /><strong>Windows Server 2003 und Windows XP:</strong> Dieser Algorithmus wird nicht unterstützt.<br /> | 
| CALG_ECMQV | 0x0000a001 | Schlüsselaustauschalgorithmus für Elliptic Curve Menezes, Qu und Vanstone (MQV). Dieser Algorithmus wird nicht unterstützt. | 
| CALG_HASH_REPLACE_OWF | 0x0000800b | Ein-Wege-Funktionshashingalgorithmus. | 
| CALG_HUGHES_MD5 | 0x0000a003 | Der MD5-Hashalgorithmus ist ein Hashalgorithmus. | 
| CALG_HMAC | 0x00008009 | HMAC-Hashalgorithmus mit Schlüssel. Dieser Algorithmus wird vom <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>unterstützt. | 
| CALG_KEA_KEYX | 0x0000aa04 | KEA-Schlüsselaustauschalgorithmus (FORTEZZA). Dieser Algorithmus wird nicht unterstützt. | 
| CALG_MAC | 0x00008005 | <a href="/windows/desktop/SecGloss/m-gly"><em>HASH-Algorithmus</em></a> mit MAC-Taste. Dieser Algorithmus wird vom <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>unterstützt. | 
| CALG_MD2 | 0x00008001 | MD2-Hashalgorithmus Dieser Algorithmus wird vom <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>unterstützt. | 
| CALG_MD4 | 0x00008002 | MD4-Hashalgorithmus | 
| CALG_MD5 | 0x00008003 | MD5-Hashalgorithmus Dieser Algorithmus wird vom <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider unterstützt.</a> | 
| CALG_NO_SIGN | 0x00002000 | Kein Signaturalgorithmus. | 
| CALG_OID_INFO_CNG_ONLY | 0xffffffff | Der Algorithmus wird nur in CNG implementiert. Das Makro IS_SPECIAL_OID_INFO_ALGID kann verwendet werden, um zu bestimmen, ob ein Kryptografiealgorithmus nur mithilfe der CNG-Funktionen unterstützt wird. | 
| CALG_OID_INFO_PARAMETERS | 0xfffffffe | Der Algorithmus wird in den codierten Parametern definiert. Der Algorithmus wird nur mit CNG unterstützt. Das Makro IS_SPECIAL_OID_INFO_ALGID kann verwendet werden, um zu bestimmen, ob ein Kryptografiealgorithmus nur mithilfe der CNG-Funktionen unterstützt wird. | 
| CALG_PCT1_MASTER | 0x00004c04 | Wird vom Schannel.dll verwendet. Diese <strong>ALG_ID</strong> sollte nicht von Anwendungen verwendet werden. | 
| CALG_RC2 | 0x00006602 | RC2-Blockverschlüsselungsalgorithmus. Dieser Algorithmus wird vom <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider unterstützt.</a> | 
| CALG_RC4 | 0x00006801 | RC4-Streamverschlüsselungsalgorithmus. Dieser Algorithmus wird vom <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider unterstützt.</a> | 
| CALG_RC5 | 0x0000660d | RC5-Blockverschlüsselungsalgorithmus. | 
| CALG_RSA_KEYX | 0x0000a400 | Rsa-Algorithmus für den Austausch öffentlicher Schlüssel. Dieser Algorithmus wird vom <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider unterstützt.</a> | 
| CALG_RSA_SIGN | 0x00002400 | Signaturalgorithmus für den öffentlichen RSA-Schlüssel. Dieser Algorithmus wird vom <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider unterstützt.</a> | 
| CALG_SCHANNEL_ENC_KEY | 0x00004c07 | Wird vom Schannel.dll verwendet. Diese <strong>ALG_ID</strong> sollte nicht von Anwendungen verwendet werden. | 
| CALG_SCHANNEL_MAC_KEY | 0x00004c03 | Wird vom Schannel.dll verwendet. Diese <strong>ALG_ID</strong> sollte nicht von Anwendungen verwendet werden. | 
| CALG_SCHANNEL_MASTER_HASH | 0x00004c02 | Wird vom Schannel.dll verwendet. Diese <strong>ALG_ID</strong> sollte nicht von Anwendungen verwendet werden. | 
| CALG_SEAL | 0x00006802 | SEAL-Verschlüsselungsalgorithmus. Dieser Algorithmus wird nicht unterstützt. | 
| CALG_SHA | 0x00008004 | SHA-Hashalgorithmus Dieser Algorithmus wird vom <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider unterstützt.</a> | 
| CALG_SHA1 | 0x00008004 | Identisch mit <strong>CALG_SHA</strong>. Dieser Algorithmus wird vom <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider unterstützt.</a> | 
| CALG_SHA_256 | 0x0000800c | 256-Bit-SHA-Hashalgorithmus. Dieser Algorithmus wird von Microsoft Enhanced RSA und AES Cryptographic Provider unterstützt. <strong>Windows XP mit SP3:</strong> Dieser Algorithmus wird von Microsoft Enhanced RSA und AES Cryptographic Provider (Prototype) unterstützt.<br /><strong>Windows XP mit SP2, Windows XP mit SP1 und Windows XP:</strong> Dieser Algorithmus wird nicht unterstützt.<br /> | 
| CALG_SHA_384 | 0x0000800d | 384-Bit-SHA-Hashalgorithmus. Dieser Algorithmus wird von Microsoft Enhanced RSA und AES Cryptographic Provider unterstützt. <strong>Windows XP mit SP3:</strong> Dieser Algorithmus wird von Microsoft Enhanced RSA und AES Cryptographic Provider (Prototype) unterstützt.<br /><strong>Windows XP mit SP2, Windows XP mit SP1 und Windows XP:</strong> Dieser Algorithmus wird nicht unterstützt.<br /> | 
| CALG_SHA_512 | 0x0000800e | SHA-Hashalgorithmus mit 512 Bit. Dieser Algorithmus wird von Microsoft Enhanced RSA und AES Cryptographic Provider unterstützt. <strong>Windows XP mit SP3:</strong> Dieser Algorithmus wird von Microsoft Enhanced RSA und AES Cryptographic Provider (Prototype) unterstützt.<br /><strong>Windows XP mit SP2, Windows XP mit SP1 und Windows XP:</strong> Dieser Algorithmus wird nicht unterstützt.<br /> | 
| CALG_SKIPJACK | 0x0000660a | Skipjack-Blockverschlüsselungsalgorithmus (FORTEZZA). Dieser Algorithmus wird nicht unterstützt. | 
| CALG_SSL2_MASTER | 0x00004c05 | Wird vom Schannel.dll verwendet. Diese <strong>ALG_ID</strong> sollte nicht von Anwendungen verwendet werden. | 
| CALG_SSL3_MASTER | 0x00004c01 | Wird vom Schannel.dll verwendet. Diese <strong>ALG_ID</strong> sollte nicht von Anwendungen verwendet werden. | 
| CALG_SSL3_SHAMD5 | 0x00008008 | Wird vom Schannel.dll verwendet. Diese <strong>ALG_ID</strong> sollte nicht von Anwendungen verwendet werden. | 
| CALG_TEK | 0x0000660b | TEK (FORTEZZA). Dieser Algorithmus wird nicht unterstützt. | 
| CALG_TLS1_MASTER | 0x00004c06 | Wird vom Schannel.dll verwendet. Diese <strong>ALG_ID</strong> sollte nicht von Anwendungen verwendet werden. | 
| CALG_TLS1PRF | 0x0000800a | Wird vom Schannel.dll verwendet. Diese <strong>ALG_ID</strong> sollte nicht von Anwendungen verwendet werden. | 




 

Für [den Microsoft Base Cryptographic Provider](microsoft-base-cryptographic-provider.md), den Microsoft Strong Cryptographic [Provider](microsoft-strong-cryptographic-provider.md)und den Microsoft Enhanced [Cryptographic Provider](microsoft-enhanced-cryptographic-provider.md)werden die **ALG_IDs** für die Schlüsselspezifikationen **AT_KEYEXCHANGE** und AT_SIGNATURE wie **folgt** verwendet:

-   **CALG_RSA_KEYX** wird für **AT_KEYEXCHANGE.**
-   **CALG_RSA_SIGN** wird für **AT_SIGNATURE.**

Für [den Microsoft Base DSS](microsoft-base-dss-and-diffie-hellman-cryptographic-provider.md)und Diffie-Hellman  Cryptographic Provider werden die ALG_IDs für die  schlüsselspezifikationen **AT_KEYEXCHANGE** und AT_SIGNATURE wie folgt verwendet:

-   **CALG_DH_SF** wird für **AT_KEYEXCHANGE.**
-   **CALG_DSS_SIGN** wird für **AT_SIGNATURE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Wincrypt.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Kryptografiefunktionen](cryptography-functions.md)
</dt> <dt>

[**CRYPT_ALGORITHM_IDENTIFIER**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_algorithm_identifier)
</dt> <dt>

[**CryptFindOIDInfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfindoidinfo)
</dt> </dl>

 

 
