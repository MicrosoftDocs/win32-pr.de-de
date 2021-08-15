---
description: In der folgenden Tabelle sind die Algorithmen aufgeführt, die vom AES-Kryptografieanbieter (Microsoft Advanced Encryption Standard) unterstützt werden.
ms.assetid: 34d0479f-9d1e-41cd-87b0-6bc18c7a062b
title: AES-Anbieteralgorithmen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a06381c3f7fcf3d410a9a9a90c70633cab17c1ffd2e3e967ba6f3e7c3787fbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773775"
---
# <a name="aes-provider-algorithms"></a>AES-Anbieteralgorithmen

In der folgenden Tabelle sind die Algorithmen aufgeführt, die vom AES-Kryptografieanbieter (Microsoft [*Advanced Encryption Standard)*](../secgloss/a-gly.md) unterstützt werden.



| Algorithmus-ID       | BESCHREIBUNG                                                                                                                                                     | Kommentare                                                                                                                                                   |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CALG \_ 3DES         | Triple DES.                                                                                                                                                     | Schlüssellänge: 168 Bits. Standardmodus: Verschlüsselungsblockverkettung.<br/> Blockgröße: 64 Bits.<br/> Kein Salt zulässig.<br/>                          |
| CALG \_ 3DES \_ 112    | Triple [*DES-Verschlüsselung*](../secgloss/t-gly.md) mit zwei Schlüsseln.                                                            | Schlüssellänge: 112 Bits. Standardmodus: Verschlüsselungsblockverkettung.<br/> Blockgröße: 64 Bits.<br/> Kein Salt zulässig.<br/>                          |
| CALG \_ AES \_ 128     | AES-Blockverschlüsselungsalgorithmus.                                                                                                                                 | Schlüssellänge: 128 Bits.                                                                                                                                      |
| CALG \_ AES \_ 192     | AES-Blockverschlüsselungsalgorithmus.                                                                                                                                 | Schlüssellänge: 192 Bits.                                                                                                                                      |
| CALG \_ AES \_ 256     | AES-Blockverschlüsselungsalgorithmus.                                                                                                                                 | Schlüssellänge: 256 Bits.                                                                                                                                      |
| CALG \_ DES          | DES-Verschlüsselung.                                                                                                                                                 | Schlüssellänge: 56 Bits. Standardmodus: Verschlüsselungsblockverkettung.<br/> Blockgröße: 64 Bits.<br/> Kein Salt zulässig.<br/>                           |
| CALG \_ HMAC         | MAC-schlüsselgebundener Hashalgorithmus                                                                                                                                       | HMAC-Berechnung.                                                                                                                                          |
| CALG \_ MAC          | [](../secgloss/m-gly.md) Nachrichtenauthentifizierungscode(MAC)-Hashalgorithmus. | Mac-Verschlüsselung blockieren.                                                                                                                                          |
| CALG \_ MD2          | MD2-Hashalgorithmus                                                                                                                                          | Weitere Informationen finden Sie unter [*MD2-Algorithmus.*](../secgloss/m-gly.md)                                       |
| CALG \_ MD5          | MD5-Hashalgorithmus                                                                                                                                          | Weitere Informationen finden Sie unter [*MD5-Algorithmus.*](../secgloss/m-gly.md)                                       |
| CALG \_ RC2          | RC2-Blockverschlüsselungsalgorithmus.                                                                                                                                 | Schlüssellänge: 128 Bits. Standardmodus: Verschlüsselungsblockverkettung.<br/> Blockgröße: 64 Bits.<br/> Salt-Länge: Kann festgelegt werden.<br/>                  |
| CALG \_ RC4          | RC4-Streamverschlüsselungsalgorithmus.                                                                                                                                | Schlüssellänge: 128 Bits. Salt-Länge: Kann festgelegt werden.<br/>                                                                                                  |
| CALG \_ RSA \_ KEYX    | RSA-Algorithmus für den Austausch öffentlicher Schlüssel.                                                                                                                              | Schlüssellänge: Kann in 8-Bit-Schritten auf 16.384 Bits festgelegt werden. Standardschlüssellänge: 1.024 Bits.<br/>                                            |
| CALG \_ RSA \_ SIGN    | Signaturalgorithmus für öffentlichen RSA-Schlüssel.                                                                                                                             | Schlüssellänge: Kann in 8-Bit-Schritten auf 16.384 Bits festgelegt werden. Standardschlüssellänge: 1.024 Bits.<br/> Die Signatur entspricht PKCS \# 6.<br/> |
| CALG \_ SHA          | SHA-Hashalgorithmus                                                                                                                                          | Weitere Informationen finden Sie unter [*Sicherer Hashalgorithmus.*](../secgloss/s-gly.md)               |
| CALG \_ SHA1         | Identisch mit **CALG \_ SHA**.                                                                                                                                          | Weitere Informationen finden Sie unter [*Sicherer Hashalgorithmus.*](../secgloss/s-gly.md)               |
| CALG \_ SHA \_ 256     | SHA-Hashalgorithmus                                                                                                                                          | Schlüssellänge: 256 Bits. **Windows XP:** Dieser Algorithmus wird nicht unterstützt.<br/>                                                                           |
| CALG \_ SHA \_ 384     | SHA-Hashalgorithmus                                                                                                                                          | Schlüssellänge: 384 Bits. **Windows XP:** Dieser Algorithmus wird nicht unterstützt.<br/>                                                                           |
| CALG \_ SHA \_ 512     | SHA-Hashalgorithmus                                                                                                                                          | Schlüssellänge: 512 Bits. **Windows XP:** Dieser Algorithmus wird nicht unterstützt.<br/>                                                                           |
| CALG \_ SSL3 \_ SHAMD5 | SSL3-Clientauthentifizierungsalgorithmus.                                                                                                                           | Weitere Informationen finden Sie unter [Creating a CALG \_ SSL3 \_ SHAMD5 Hash](creating-a-calg-ssl3-shamd5-hash.md).                                                      |



 

 

 
