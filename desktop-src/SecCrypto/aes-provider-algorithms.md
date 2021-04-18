---
description: In der folgenden Tabelle sind die Algorithmen aufgelistet, die vom Kryptografieanbieter von Microsoft Advanced Encryption Standard (AES) unterstützt werden.
ms.assetid: 34d0479f-9d1e-41cd-87b0-6bc18c7a062b
title: AES-Anbieter Algorithmen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e5e197100060d53304bb5233560dcccae083756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359075"
---
# <a name="aes-provider-algorithms"></a>AES-Anbieter Algorithmen

In der folgenden Tabelle sind die Algorithmen aufgelistet, die vom Kryptografieanbieter von Microsoft [*Advanced Encryption Standard*](../secgloss/a-gly.md) (AES) unterstützt werden.



| Algorithmuskennung       | BESCHREIBUNG                                                                                                                                                     | Kommentare                                                                                                                                                   |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Calg \_ 3DES         | Triple des.                                                                                                                                                     | Schlüssellänge: 168 Bits. Standardmodus: Chiffre Block Verkettung.<br/> Block Größe: 64 Bits.<br/> Es ist kein Salt zulässig.<br/>                          |
| Calg \_ 3DES \_ 112    | [*Triple des*](../secgloss/t-gly.md) -Verschlüsselung mit zwei Schlüsseln.                                                            | Schlüssellänge: 112 Bits. Standardmodus: Chiffre Block Verkettung.<br/> Block Größe: 64 Bits.<br/> Es ist kein Salt zulässig.<br/>                          |
| Calg \_ AES \_ 128     | AES-Block Verschlüsselungsalgorithmus.                                                                                                                                 | Schlüssellänge: 128 Bits.                                                                                                                                      |
| Calg \_ AES \_ 192     | AES-Block Verschlüsselungsalgorithmus.                                                                                                                                 | Schlüssellänge: 192 Bits.                                                                                                                                      |
| Calg \_ AES \_ 256     | AES-Block Verschlüsselungsalgorithmus.                                                                                                                                 | Schlüssellänge: 256 Bits.                                                                                                                                      |
| " \_ calg"          | DES-Verschlüsselung.                                                                                                                                                 | Schlüssellänge: 56 Bits. Standardmodus: Chiffre Block Verkettung.<br/> Block Größe: 64 Bits.<br/> Es ist kein Salt zulässig.<br/>                           |
| HMAC (calg) \_         | MAC-schlüsselgebundener Hashalgorithmus                                                                                                                                       | HMAC-Berechnung.                                                                                                                                          |
| calg- \_ Mac          | [*Nachrichtenauthentifizierungscode*](../secgloss/m-gly.md) (Mac)-Hash Algorithmus. | Blockieren Sie den Mac-Chiffre.                                                                                                                                          |
| Calg \_ MD2          | MD2-Hashalgorithmus                                                                                                                                          | Weitere Informationen finden Sie unter [*MD2-Algorithmus*](../secgloss/m-gly.md).                                       |
| Calg \_ MD5          | MD5-Hashalgorithmus                                                                                                                                          | Weitere Informationen finden Sie unter [*MD5-Algorithmus*](../secgloss/m-gly.md).                                       |
| Calg \_ RC2          | RC2-Block Verschlüsselungsalgorithmus.                                                                                                                                 | Schlüssellänge: 128 Bits. Standardmodus: Chiffre Block Verkettung.<br/> Block Größe: 64 Bits.<br/> Salt length: kann festgelegt werden.<br/>                  |
| Calg \_ RC4          | RC4-Stream-Verschlüsselungsalgorithmus.                                                                                                                                | Schlüssellänge: 128 Bits. Salt length: kann festgelegt werden.<br/>                                                                                                  |
| calg \_ RSA \_ Keyx    | RSA-Algorithmus für den öffentlichen Schlüsselaustausch.                                                                                                                              | Schlüssellänge: kann festgelegt werden, 384 Bits auf 16.384 Bits in 8-Bit-Inkrementen. Standard Schlüssellänge: 1.024 Bits.<br/>                                            |
| calg- \_ RSA- \_ Zeichen    | RSA-Algorithmus für die öffentliche Schlüssel Signatur.                                                                                                                             | Schlüssellänge: kann festgelegt werden, 384 Bits auf 16.384 Bits in 8-Bit-Inkrementen. Standard Schlüssellänge: 1.024 Bits.<br/> Die Signatur entspricht PKCS \# 6.<br/> |
| calg \_ SHA          | SHA-Hashalgorithmus                                                                                                                                          | Weitere Informationen finden Sie unter [*Secure Hash-Algorithmus*](../secgloss/s-gly.md).               |
| Calg \_ SHA1         | Identisch mit **calg \_ SHA**.                                                                                                                                          | Weitere Informationen finden Sie unter [*Secure Hash-Algorithmus*](../secgloss/s-gly.md).               |
| Calg \_ SHA \_ 256     | SHA-Hashalgorithmus                                                                                                                                          | Schlüssellänge: 256 Bits. **Windows XP:** Dieser Algorithmus wird nicht unterstützt.<br/>                                                                           |
| Calg \_ SHA \_ 384     | SHA-Hashalgorithmus                                                                                                                                          | Schlüssellänge: 384 Bits. **Windows XP:** Dieser Algorithmus wird nicht unterstützt.<br/>                                                                           |
| Calg \_ SHA \_ 512     | SHA-Hashalgorithmus                                                                                                                                          | Schlüssellänge: 512 Bits. **Windows XP:** Dieser Algorithmus wird nicht unterstützt.<br/>                                                                           |
| Calg \_ SSL3 \_ SHAMD5 | SSL3 Client Authentication-Algorithmus.                                                                                                                           | Weitere Informationen finden Sie unter [Creating a calg \_ SSL3 \_ SHAMD5 Hash](creating-a-calg-ssl3-shamd5-hash.md).                                                      |



 

 

 
