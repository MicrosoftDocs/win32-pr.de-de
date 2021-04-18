---
description: 'Im Unterschied zur Cryptography API (CryptoAPI) trennt Cryptography API: Next Generation (CNG) Kryptografieanbieter von Schlüsselspeicher Anbietern.'
ms.assetid: ce29bc97-049e-4c82-979f-4c805a318ba0
title: CNG-kryptografiealgorithmusanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bc64926236157e581ce6406d95681bd8d4add14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347718"
---
# <a name="cng-cryptographic-algorithm-providers"></a>CNG-kryptografiealgorithmusanbieter

Im Unterschied zur Cryptography API (CryptoAPI) trennt Cryptography API: Next Generation (CNG) Kryptografieanbieter von Schlüsselspeicher Anbietern. Grundlegende Vorgänge für kryptografische Algorithmen, z. b. Hashs und Signierung, werden als primitive Vorgänge oder einfach als primitive bezeichnet. CNG enthält einen Anbieter, der die folgenden Algorithmen implementiert.

-   [Symmetrische Algorithmen](#symmetric-algorithms)
-   [Asymmetrische Algorithmen](#asymmetric-algorithms)
-   [Hashalgorithmen](#hashing-algorithms)
-   [Schlüsselaustausch Algorithmen](#key-exchange-algorithms)
-   [Zugehörige Themen](#related-topics)

## <a name="symmetric-algorithms"></a>Symmetrische Algorithmen



| Name                                   | Unterstützte Modi                                                                                                                                                                                                 | Schlüsselgröße in Bits (Standard/min/max) |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| Advanced Encryption Standard (AES)     | ECB, CBC, CFB8, CFB128, GCM, ccm, GMAC, CMAC, AES Key Wrap, XTS<br/> **Windows 8:** Die Unterstützung für die CFB128-und CMAC-Modi beginnt.<br/> **Windows 10:** Die Unterstützung für den XTS-AES-Modus beginnt.<br/> | 128/192/256                        |
| Data Encryption Standard (des)         | ECB, CBC, CFB8, CFB64<br/> **Windows 8:** Die Unterstützung für den CFB64-Modus beginnt.<br/>                                                                                                                   | 56/56/56                           |
| Data Encryption Standard XoReD (DESX)   | ECB, CBC, CFB8, CFB64 <br/> **Windows 8:** Die Unterstützung für den CFB64-Modus beginnt.<br/>                                                                                                                  | 192/192/192                        |
| Triple Data Encryption Standard (3DES) | ECB, CBC, CFB8, CFB64 <br/> **Windows 8:** Die Unterstützung für den CFB64-Modus beginnt.<br/>                                                                                                                  | 112/168                            |
| RSA Data Security 2 (RC2)              | Die Modi ECB, CBC, CFB8 und CFB64 werden unterstützt.<br/> **Windows 8:** Die Unterstützung für den CFB64-Modus beginnt.<br/>                                                                                              | 16 bis 128 in 8-Bit-Inkrementen      |
| RSA Data Security 4 (RC4)              |                                                                                                                                                                                                                 | 8 bis 512, in 8-Bit-Inkrementen      |



 

## <a name="asymmetric-algorithms"></a>Asymmetrische Algorithmen



| Name                              | Notizen                                                                                                                                                                             | Schlüsselgröße in Bits (Standard/min/max)                                                                            |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Digital Signature-Algorithmus (DSA) | Die Implementierung entspricht dem Wert von "fps 186-3" für Schlüsselgrößen zwischen 1024 und 3072 Bits. <br/> Die Implementierung entspricht dem Wert von "fps 186-2" für Schlüsselgrößen von 512 bis 1024 Bits.<br/> | 512 bis 3072, in 64-Bit-Inkrementen<br/> **Windows 8:** Die Unterstützung für die 3072-Bit-Taste beginnt.<br/> |
| RSA                               | Schließt RSA-Algorithmen ein, die PKCS1, optimale OAEP (asymmetrisch Encryption Auffüllung)-Codierung oder-Auffüll-oder Auffüll-und Auffüll-und Auffüll Text Auffüll Zeichen verwenden.               | 512 bis 16384, in 64-Bit-Inkrementen                                                                            |



 

## <a name="hashing-algorithms"></a>Hashalgorithmen



| Name                               | Notizen               | Schlüsselgröße in Bits (Standard/min/max) |
|------------------------------------|---------------------|------------------------------------|
| Secure-Hash-Algorithmus 1 (SHA1)     | Umfasst HmacSha1   | 160/160/160                        |
| Secure Hash-Algorithmus 256 (SHA256) | Umfasst HmacSha256 | 256/256/256                        |
| Secure Hash-Algorithmus 384 (SHA384) | Umfasst HmacSha384 | 384/384/384                        |
| Secure Hash-Algorithmus 512 (SHA512) | Umfasst HmacSha512 | 512/512/512                        |
| Message Digest 2 (MD2)             | Umfasst HmacMd2    | 128/128/128                        |
| Message Digest 4 (MD4)             | Umfasst HmacMd4    | 128/128/128                        |
| Message Digest 5 (MD5)             | Umfasst HmacMd5    | 128/128/128                        |



 

## <a name="key-exchange-algorithms"></a>Schlüsselaustausch Algorithmen



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Algorithmusname</th>
<th>Notizen</th>
<th>Schlüsselgröße in Bits (Standard/min/max)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Diffie-Hellman Schlüsselaustausch Algorithmus</td>

<td>512 bis 4096, in 64-Bit-Inkrementen</td>
</tr>
<tr class="even">
<td>ECDH (Elliptic Curve Diffie-Hellman)</td>
<td>Schließt Kurven ein, die die öffentlichen Schlüssel 256, 384 und 521 Bit verwenden, wie in SP800-56a angegeben.</td>
<td>256/384/521</td>
</tr>
<tr class="odd">
<td>ECDSA (Elliptic Curve Digital Signature-Algorithmus)</td>
<td>Schließt Kurven ein, die die öffentlichen Schlüssel 256, 384 und 521 Bit verwenden, wie in "fps 186-3" angegeben.
<blockquote>
[!Note]<br />
Verwenden Sie <strong>certutil displayecccurve</strong>, um alle benannten elliptischen Kurven anzuzeigen.
</blockquote>
<br/></td>
<td>256/384/521</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**CNG-Algorithmusbezeichner**](/windows/desktop/SecCNG/cng-algorithm-identifiers)
</dt> <dt>

[Kryptografische CNG-Funktionen](/windows/desktop/SecCNG/cng-cryptographic-primitive-functions)
</dt> <dt>

[Grundlegendes zu Kryptografieanbietern](understanding-cryptographic-providers.md)
</dt> </dl>

 

