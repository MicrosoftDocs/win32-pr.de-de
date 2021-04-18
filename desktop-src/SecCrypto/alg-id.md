---
description: Gibt einen Algorithmusbezeichner an.
ms.assetid: 557436b4-f7f1-4708-acc7-c6b47e6322ad
title: ALG_ID (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ab1eb6dc262faae76d38f2b96c9e6191a313390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366237"
---
# <a name="alg_id"></a>ALG_ID

Der **ALG_ID** -Datentyp gibt einen Algorithmusbezeichner an. Parameter dieses Datentyps werden an die meisten Funktionen in CryptoAPI übermittelt.


```C++
typedef unsigned int ALG_ID;
```



In der folgenden Tabelle werden die zurzeit definierten Algorithmusbezeichner aufgelistet. Autoren von benutzerdefinierten [*Kryptografiedienstanbietern*](../secgloss/c-gly.md) (CSPs) können neue Werte definieren. Außerdem sind die **ALG_ID** , die von benutzerdefinierten CSPs für die Schlüssel Spezifikationen **AT_KEYEXCHANGE** und **AT_SIGNATURE** verwendet werden, vom Anbieter abhängig. Aktuelle Zuordnungen Folgen der Tabelle.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Bezeichner</th>
<th>Wert</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>CALG_3DES</td>
<td>0x00006603</td>
<td><a href="/windows/desktop/SecGloss/t-gly"><em>Triple des</em></a> -Verschlüsselungsalgorithmus.</td>
</tr>
<tr class="even">
<td>CALG_3DES_112</td>
<td>0x00006609</td>
<td>Die zwei-Schlüssel- <a href="/windows/desktop/SecGloss/t-gly"><em>Triple-des</em></a> -Verschlüsselung mit einer effektiven Schlüssellänge von 112 Bits.</td>
</tr>
<tr class="odd">
<td>CALG_AES</td>
<td>0x00006611</td>
<td>Advanced Encryption Standard (AES). Dieser Algorithmus wird vom <a href="microsoft-aes-cryptographic-provider.md">Microsoft AES-Kryptografieanbieter</a>unterstützt.</td>
</tr>
<tr class="even">
<td>CALG_AES_128</td>
<td>0x0000660e</td>
<td>128-Bit-AES. Dieser Algorithmus wird vom <a href="microsoft-aes-cryptographic-provider.md">Microsoft AES-Kryptografieanbieter</a>unterstützt.</td>
</tr>
<tr class="odd">
<td>CALG_AES_192</td>
<td>0x0000660f</td>
<td>192-Bit-AES. Dieser Algorithmus wird vom <a href="microsoft-aes-cryptographic-provider.md">Microsoft AES-Kryptografieanbieter</a>unterstützt.</td>
</tr>
<tr class="even">
<td>CALG_AES_256</td>
<td>0x00006610</td>
<td>256-Bit-AES. Dieser Algorithmus wird vom <a href="microsoft-aes-cryptographic-provider.md">Microsoft AES-Kryptografieanbieter</a>unterstützt.</td>
</tr>
<tr class="odd">
<td>CALG_AGREEDKEY_ANY</td>
<td>0x0000aa03</td>
<td>Temporärer Algorithmusbezeichner für Handles von Diffie-Hellman – vereinbarten Schlüsseln.</td>
</tr>
<tr class="even">
<td>CALG_CYLINK_MEK</td>
<td>0x0000660c</td>
<td>Ein Algorithmus zum Erstellen eines 40-Bit-des-Schlüssels, der Paritätsbits und NULL-Bit-Schlüssel Bits enthält, um die Schlüssellänge 64 Bits zu erzielen. Dieser Algorithmus wird vom Microsoft- <a href=""></a> <a href="microsoft-base-cryptographic-provider.md">Basis-Kryptografieanbieter</a>unterstützt.</td>
</tr>
<tr class="odd">
<td>CALG_DES</td>
<td>0x00006601</td>
<td>DES-Verschlüsselungsalgorithmus.</td>
</tr>
<tr class="even">
<td>CALG_DESX</td>
<td>0x00006604</td>
<td>DESX-Verschlüsselungsalgorithmus.</td>
</tr>
<tr class="odd">
<td>CALG_DH_EPHEM</td>
<td>0x0000aa02</td>
<td>Diffie-Hellman kurzlebigen Algorithmus für den Schlüsselaustausch.</td>
</tr>
<tr class="even">
<td>CALG_DH_SF</td>
<td>0x0000aa01</td>
<td>Diffie-Hellman den Algorithmus zum Speichern und Weiterleiten eines Schlüssel Austauschs.</td>
</tr>
<tr class="odd">
<td>CALG_DSS_SIGN</td>
<td>0x00002200</td>
<td>DSA-Algorithmus für die <a href="/windows/desktop/SecGloss/p-gly"><em>öffentliche Schlüssel</em></a> Signatur.</td>
</tr>
<tr class="even">
<td>CALG_ECDH</td>
<td>0x0000aa05</td>
<td>Elliptische Kurve Diffie-Hellman Algorithmus für den Schlüsselaustausch.
<blockquote>
[!Note]<br />
Dieser Algorithmus wird nur über die <a href="/windows/desktop/SecCNG/cng-portal">kryptografieapi: Next Generation</a>unterstützt.
</blockquote>
<br/> <strong>Windows Server 2003 und Windows XP:</strong> Dieser Algorithmus wird nicht unterstützt.<br/></td>
</tr>
<tr class="odd">
<td>CALG_ECDH_EPHEM</td>
<td>0x0000ae06</td>
<td>Kurzlebige elliptische Kurve Diffie-Hellman Algorithmus für den Schlüsselaustausch.
<blockquote>
[!Note]<br />
Dieser Algorithmus wird nur über die <a href="/windows/desktop/SecCNG/cng-portal">kryptografieapi: Next Generation</a>unterstützt.
</blockquote>
<br/> <strong>Windows Server 2003 und Windows XP:</strong> Dieser Algorithmus wird nicht unterstützt.<br/></td>
</tr>
<tr class="even">
<td>CALG_ECDSA</td>
<td>0x00002203</td>
<td>Digitaler Signatur Algorithmus für elliptische Kurve.
<blockquote>
[!Note]<br />
Dieser Algorithmus wird nur über die <a href="/windows/desktop/SecCNG/cng-portal">kryptografieapi: Next Generation</a>unterstützt.
</blockquote>
<br/> <strong>Windows Server 2003 und Windows XP:</strong> Dieser Algorithmus wird nicht unterstützt.<br/></td>
</tr>
<tr class="odd">
<td>CALG_ECMQV</td>
<td>0x0000a001</td>
<td>Schlüsselaustausch Algorithmus für die elliptische Kurve "Menezes", "Qu" und "Vanstone" (mqv). Dieser Algorithmus wird nicht unterstützt.</td>
</tr>
<tr class="even">
<td>CALG_HASH_REPLACE_OWF</td>
<td>0x0000800b</td>
<td>Ein unidirektionaler Funktions Hash Algorithmus.</td>
</tr>
<tr class="odd">
<td>CALG_HUGHES_MD5</td>
<td>0x0000a003</td>
<td>Hughes MD5-Hash Algorithmus.</td>
</tr>
<tr class="even">
<td>CALG_HMAC</td>
<td>0x00008009</td>
<td>HMAC-verschlüsselter Hash Algorithmus. Dieser Algorithmus wird vom Microsoft- <a href="microsoft-base-cryptographic-provider.md">Basis-Kryptografieanbieter</a>unterstützt.</td>
</tr>
<tr class="odd">
<td>CALG_KEA_KEYX</td>
<td>0x0000aa04</td>
<td>KEA-Schlüsselaustausch Algorithmus (Fortezza). Dieser Algorithmus wird nicht unterstützt.</td>
</tr>
<tr class="even">
<td>CALG_MAC</td>
<td>0x00008005</td>
<td><a href="/windows/desktop/SecGloss/m-gly"><em>Mac</em></a> -verschlüsselter Hash Algorithmus. Dieser Algorithmus wird vom Microsoft- <a href="microsoft-base-cryptographic-provider.md">Basis-Kryptografieanbieter</a>unterstützt.</td>
</tr>
<tr class="odd">
<td>CALG_MD2</td>
<td>0x00008001</td>
<td>MD2-Hashalgorithmus Dieser Algorithmus wird vom Microsoft- <a href="microsoft-base-cryptographic-provider.md">Basis-Kryptografieanbieter</a>unterstützt.</td>
</tr>
<tr class="even">
<td>CALG_MD4</td>
<td>0x00008002</td>
<td>MD4-Hashalgorithmus</td>
</tr>
<tr class="odd">
<td>CALG_MD5</td>
<td>0x00008003</td>
<td>MD5-Hashalgorithmus Dieser Algorithmus wird vom Microsoft- <a href="microsoft-base-cryptographic-provider.md">Basis-Kryptografieanbieter</a>unterstützt.</td>
</tr>
<tr class="even">
<td>CALG_NO_SIGN</td>
<td>0x00002000</td>
<td>Kein Signatur Algorithmus.</td>
</tr>
<tr class="odd">
<td>CALG_OID_INFO_CNG_ONLY</td>
<td>0xFFFFFFFF</td>
<td>Der Algorithmus ist nur in CNG implementiert. Das-Makro, IS_SPECIAL_OID_INFO_ALGID, kann verwendet werden, um zu bestimmen, ob ein Kryptografiealgorithmus nur mithilfe der CNG-Funktionen unterstützt wird.</td>
</tr>
<tr class="even">
<td>CALG_OID_INFO_PARAMETERS</td>
<td>0xfffffffe</td>
<td>Der Algorithmus wird in den codierten Parametern definiert. Der Algorithmus wird nur durch die Verwendung von CNG unterstützt. Das-Makro, IS_SPECIAL_OID_INFO_ALGID, kann verwendet werden, um zu bestimmen, ob ein Kryptografiealgorithmus nur mithilfe der CNG-Funktionen unterstützt wird.</td>
</tr>
<tr class="odd">
<td>CALG_PCT1_MASTER</td>
<td>0x00004c04</td>
<td>Wird vom Schannel.dll-Betriebssystem verwendet. Diese <strong>ALG_ID</strong> sollte von Anwendungen nicht verwendet werden.</td>
</tr>
<tr class="even">
<td>CALG_RC2</td>
<td>0x00006602</td>
<td>RC2-Block Verschlüsselungsalgorithmus. Dieser Algorithmus wird vom Microsoft- <a href="microsoft-base-cryptographic-provider.md">Basis-Kryptografieanbieter</a>unterstützt.</td>
</tr>
<tr class="odd">
<td>CALG_RC4</td>
<td>0x00006801</td>
<td>RC4-Stream-Verschlüsselungsalgorithmus. Dieser Algorithmus wird vom Microsoft- <a href="microsoft-base-cryptographic-provider.md">Basis-Kryptografieanbieter</a>unterstützt.</td>
</tr>
<tr class="even">
<td>CALG_RC5</td>
<td>0x0000660d</td>
<td>RC5 Block Verschlüsselungsalgorithmus.</td>
</tr>
<tr class="odd">
<td>CALG_RSA_KEYX</td>
<td>0x0000a400</td>
<td>RSA-Algorithmus für den öffentlichen Schlüsselaustausch. Dieser Algorithmus wird vom Microsoft- <a href="microsoft-base-cryptographic-provider.md">Basis-Kryptografieanbieter</a>unterstützt.</td>
</tr>
<tr class="even">
<td>CALG_RSA_SIGN</td>
<td>0x00002400</td>
<td>RSA-Algorithmus für die öffentliche Schlüssel Signatur. Dieser Algorithmus wird vom Microsoft- <a href="microsoft-base-cryptographic-provider.md">Basis-Kryptografieanbieter</a>unterstützt.</td>
</tr>
<tr class="odd">
<td>CALG_SCHANNEL_ENC_KEY</td>
<td>0x00004c07</td>
<td>Wird vom Schannel.dll-Betriebssystem verwendet. Diese <strong>ALG_ID</strong> sollte von Anwendungen nicht verwendet werden.</td>
</tr>
<tr class="even">
<td>CALG_SCHANNEL_MAC_KEY</td>
<td>0x00004c03</td>
<td>Wird vom Schannel.dll-Betriebssystem verwendet. Diese <strong>ALG_ID</strong> sollte von Anwendungen nicht verwendet werden.</td>
</tr>
<tr class="odd">
<td>CALG_SCHANNEL_MASTER_HASH</td>
<td>0x00004c02</td>
<td>Wird vom Schannel.dll-Betriebssystem verwendet. Diese <strong>ALG_ID</strong> sollte von Anwendungen nicht verwendet werden.</td>
</tr>
<tr class="even">
<td>CALG_SEAL</td>
<td>0x00006802</td>
<td>Versiegelt den Verschlüsselungsalgorithmus. Dieser Algorithmus wird nicht unterstützt.</td>
</tr>
<tr class="odd">
<td>CALG_SHA</td>
<td>0x00008004</td>
<td>SHA-Hashalgorithmus Dieser Algorithmus wird vom Microsoft- <a href="microsoft-base-cryptographic-provider.md">Basis-Kryptografieanbieter</a>unterstützt.</td>
</tr>
<tr class="even">
<td>CALG_SHA1</td>
<td>0x00008004</td>
<td>Identisch mit <strong>CALG_SHA</strong>. Dieser Algorithmus wird vom Microsoft- <a href="microsoft-base-cryptographic-provider.md">Basis-Kryptografieanbieter</a>unterstützt.</td>
</tr>
<tr class="odd">
<td>CALG_SHA_256</td>
<td>0x0000800c</td>
<td>256-Bit-SHA-Hash Algorithmus. Dieser Algorithmus wird von Microsoft Enhanced RSA und AES Cryptographic Provider unterstützt. <strong>Windows XP mit SP3:</strong> Dieser Algorithmus wird von Microsoft Enhanced RSA und AES Cryptographic Provider (Prototype) unterstützt.<br/> <strong>Windows XP mit SP2, Windows XP mit SP1 und Windows XP:</strong> Dieser Algorithmus wird nicht unterstützt.<br/></td>
</tr>
<tr class="even">
<td>CALG_SHA_384</td>
<td>0x0000800d</td>
<td>384-Bit-SHA-Hash Algorithmus. Dieser Algorithmus wird von Microsoft Enhanced RSA und AES Cryptographic Provider unterstützt. <strong>Windows XP mit SP3:</strong> Dieser Algorithmus wird von Microsoft Enhanced RSA und AES Cryptographic Provider (Prototype) unterstützt.<br/> <strong>Windows XP mit SP2, Windows XP mit SP1 und Windows XP:</strong> Dieser Algorithmus wird nicht unterstützt.<br/></td>
</tr>
<tr class="odd">
<td>CALG_SHA_512</td>
<td>0x0000800e</td>
<td>512-Bit-SHA-Hash Algorithmus. Dieser Algorithmus wird von Microsoft Enhanced RSA und AES Cryptographic Provider unterstützt. <strong>Windows XP mit SP3:</strong> Dieser Algorithmus wird von Microsoft Enhanced RSA und AES Cryptographic Provider (Prototype) unterstützt.<br/> <strong>Windows XP mit SP2, Windows XP mit SP1 und Windows XP:</strong> Dieser Algorithmus wird nicht unterstützt.<br/></td>
</tr>
<tr class="even">
<td>CALG_SKIPJACK</td>
<td>0x0000660a</td>
<td>Skipjack-Block Verschlüsselungsalgorithmus (Fortezza). Dieser Algorithmus wird nicht unterstützt.</td>
</tr>
<tr class="odd">
<td>CALG_SSL2_MASTER</td>
<td>0x00004c05</td>
<td>Wird vom Schannel.dll-Betriebssystem verwendet. Diese <strong>ALG_ID</strong> sollte von Anwendungen nicht verwendet werden.</td>
</tr>
<tr class="even">
<td>CALG_SSL3_MASTER</td>
<td>0x00004c01</td>
<td>Wird vom Schannel.dll-Betriebssystem verwendet. Diese <strong>ALG_ID</strong> sollte von Anwendungen nicht verwendet werden.</td>
</tr>
<tr class="odd">
<td>CALG_SSL3_SHAMD5</td>
<td>0x00008008</td>
<td>Wird vom Schannel.dll-Betriebssystem verwendet. Diese <strong>ALG_ID</strong> sollte von Anwendungen nicht verwendet werden.</td>
</tr>
<tr class="even">
<td>CALG_TEK</td>
<td>0x0000660b</td>
<td>Tek (Fortezza). Dieser Algorithmus wird nicht unterstützt.</td>
</tr>
<tr class="odd">
<td>CALG_TLS1_MASTER</td>
<td>0x00004c06</td>
<td>Wird vom Schannel.dll-Betriebssystem verwendet. Diese <strong>ALG_ID</strong> sollte von Anwendungen nicht verwendet werden.</td>
</tr>
<tr class="even">
<td>CALG_TLS1PRF</td>
<td>0x0000800a</td>
<td>Wird vom Schannel.dll-Betriebssystem verwendet. Diese <strong>ALG_ID</strong> sollte von Anwendungen nicht verwendet werden.</td>
</tr>
</tbody>
</table>



 

Für den [Kryptografieanbieter](microsoft-base-cryptographic-provider.md)Microsoft, den [starken Kryptografieanbieter](microsoft-strong-cryptographic-provider.md)von Microsoft und den [erweiterten Kryptografieanbieter von Microsoft](microsoft-enhanced-cryptographic-provider.md), werden die **ALG_IDs** für die Schlüssel Spezifikationen **AT_KEYEXCHANGE** und **AT_SIGNATURE** wie folgt verwendet:

-   **CALG_RSA_KEYX** wird für **AT_KEYEXCHANGE** verwendet.
-   **CALG_RSA_SIGN** wird für **AT_SIGNATURE** verwendet.

Für den [Microsoft Base DSS und den Diffie-Hellman Kryptografieanbieter](microsoft-base-dss-and-diffie-hellman-cryptographic-provider.md)lauten die **ALG_IDs** , die für die Schlüssel Spezifikationen **AT_KEYEXCHANGE** und **AT_SIGNATURE** verwendet werden, wie folgt:

-   **CALG_DH_SF** wird für **AT_KEYEXCHANGE** verwendet.
-   **CALG_DSS_SIGN** wird für **AT_SIGNATURE** verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>WinCrypt. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Kryptografiefunktionen](cryptography-functions.md)
</dt> <dt>

[**CRYPT_ALGORITHM_IDENTIFIER**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_algorithm_identifier)
</dt> <dt>

[**Cryptfindoidinfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfindoidinfo)
</dt> </dl>

 

 
