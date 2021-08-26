---
description: 'Im Gegensatz zur Kryptografie-API (CryptoAPI) trennt cryptography API: Next Generation (CNG) Kryptografieanbieter von Schlüsselspeicheranbietern.'
ms.assetid: ce29bc97-049e-4c82-979f-4c805a318ba0
title: CNG-Kryptografiealgorithmusanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fd98a7eb6fd159c54977cdf8b72ebffd747da48
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467077"
---
# <a name="cng-cryptographic-algorithm-providers"></a>CNG-Kryptografiealgorithmusanbieter

Im Gegensatz zur Kryptografie-API (CryptoAPI) trennt cryptography API: Next Generation (CNG) Kryptografieanbieter von Schlüsselspeicheranbietern. Grundlegende Kryptografiealgorithmusvorgänge wie Hashing und Signierung werden als primitive Vorgänge oder einfach primitive Vorgänge bezeichnet. CNG enthält einen Anbieter, der die folgenden Algorithmen implementiert.

-   [Symmetrische Algorithmen](#symmetric-algorithms)
-   [Asymmetrische Algorithmen](#asymmetric-algorithms)
-   [Hashalgorithmen](#hashing-algorithms)
-   [Wichtige Exchange Algorithmen](#key-exchange-algorithms)
-   [Zugehörige Themen](#related-topics)

## <a name="symmetric-algorithms"></a>Symmetrische Algorithmen



| Name                                   | Unterstützte Modi                                                                                                                                                                                                 | Schlüsselgröße in Bits (Standard/Min./Max.) |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| Advanced Encryption Standard (AES)     | TASTEN, CBC, CFB8, CFB128, GCM, CCM, GMAC, CMAC, AES Key Wrap, XTS<br/> **Windows 8:** Die Unterstützung für die Modi CFB128 und CMAC beginnt.<br/> **Windows 10:** Die Unterstützung für den XTS-AES-Modus beginnt.<br/> | 128/192/256                        |
| Data Encryption Standard (DES)         | VEREERBUNG, CBC, CFB8, CFB64<br/> **Windows 8:** Die Unterstützung für den CFB64-Modus beginnt.<br/>                                                                                                                   | 56/56/56                           |
| Data Encryption Standard XORed(DESX)   | VEREERBUNG, CBC, CFB8, CFB64 <br/> **Windows 8:** Die Unterstützung für den CFB64-Modus beginnt.<br/>                                                                                                                  | 192/192/192                        |
| Triple Data Encryption Standard (3DES) | VEREERBUNG, CBC, CFB8, CFB64 <br/> **Windows 8:** Die Unterstützung für den CFB64-Modus beginnt.<br/>                                                                                                                  | 112/168                            |
| RSA Data Security 2 (RC2)              | DIE MODI 1, CBC, CFB8 und CFB64 werden unterstützt.<br/> **Windows 8:** Die Unterstützung für den CFB64-Modus beginnt.<br/>                                                                                              | 16 bis 128 in 8-Bit-Schritten      |
| RSA Data Security 4 (RC4)              |                                                                                                                                                                                                                 | 8 bis 512 in 8-Bit-Schritten      |



 

## <a name="asymmetric-algorithms"></a>Asymmetrische Algorithmen



| Name                              | Notizen                                                                                                                                                                             | Schlüsselgröße in Bits (Standard/Min./Max.)                                                                            |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Digital Signature Algorithm (DSA) | Die Implementierung entspricht FIPS 186-3 für Schlüsselgrößen zwischen 1024 und 3072 Bit. <br/> Die Implementierung entspricht FIPS 186-2 für Schlüsselgrößen von 512 bis 1024 Bit.<br/> | 512 bis 3072 in 64-Bit-Schritten<br/> **Windows 8:** Die Unterstützung für einen 3072-Bit-Schlüssel beginnt.<br/> |
| RSA                               | Enthält RSA-Algorithmen, die PKCS1, OAEP-Codierung (Optimal Asymmetric Encryption Padding) oder Probabilistic Signature Scheme (PSS)-Klartextauf padding verwenden.               | 512 bis 16384 in 64-Bit-Schritten                                                                            |



 

## <a name="hashing-algorithms"></a>Hashalgorithmen



| Name                               | Notizen               | Schlüsselgröße in Bits (Standard/Min./Max.) |
|------------------------------------|---------------------|------------------------------------|
| Secure-Hash-Algorithmus 1 (SHA1)     | Enthält HmacSha1   | 160/160/160                        |
| Sicherer Hashalgorithmus 256 (SHA256) | Enthält HmacSha256 | 256/256/256                        |
| Sicherer Hashalgorithmus 384 (SHA384) | Enthält HmacSha384 | 384/384/384                        |
| Sicherer Hashalgorithmus 512 (SHA512) | Enthält HmacSha512 | 512/512/512                        |
| Message Digest 2 (MD2)             | Enthält HmacMd2    | 128/128/128                        |
| Message Digest 4 (MD4)             | Enthält HmacMd4    | 128/128/128                        |
| Message Digest 5 (MD5)             | Enthält HmacMd5    | 128/128/128                        |



 

## <a name="key-exchange-algorithms"></a>Wichtige Exchange Algorithmen




| Algorithmusname | Hinweise | Schlüsselgröße in Bits (Standard/Min./Max.) | 
|----------------|-------|------------------------------------|
| Diffie-Hellman Key Exchange Algorithm | 512 bis 4096 in 64-Bit-Schritten | 
| Elliptic Curve Diffie-Hellman (ECDH) | Schließt Kurven ein, die öffentliche Schlüssel mit 256, 384 und 521 Bit verwenden, wie in SP800-56A angegeben. | 256/384/521 | 
| Elliptic Curve Digital Signature Algorithm (ECDSA) | Schließt Kurven ein, die öffentliche Schlüssel mit 256, 384 und 521 Bit verwenden, wie in FIPS 186-3 angegeben.<blockquote>[!Note]<br />Um alle benannten elliptischen Kurven anzuzeigen, verwenden Sie <strong>certutil displayEccCurve</strong>.</blockquote><br /> | 256/384/521 | 




 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**CNG-Algorithmusbezeichner**](/windows/desktop/SecCNG/cng-algorithm-identifiers)
</dt> <dt>

[Kryptografische primitive CNG-Funktionen](/windows/desktop/SecCNG/cng-cryptographic-primitive-functions)
</dt> <dt>

[Grundlegendes zu Kryptografieanbietern](understanding-cryptographic-providers.md)
</dt> </dl>

 

