---
description: Der Microsoft Enhanced Cryptographic Provider unterstützt die folgenden Algorithmen.
ms.assetid: d58bcd99-c54b-4fda-9fe1-e10a66707d81
title: Erweiterte Anbieteralgorithmen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a8be464a57a482fa74fef07de097508508d7e965a5c20817ccbd884bb169e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117766101"
---
# <a name="enhanced-provider-algorithms"></a>Erweiterte Anbieteralgorithmen

Der [Microsoft Enhanced Cryptographic Provider](microsoft-enhanced-cryptographic-provider.md) unterstützt die folgenden Algorithmen.



| Algorithmus-ID       | BESCHREIBUNG                                                                                                                                                     | Kommentare                                                                                                                                                   |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CALG \_ 3DES         | Triple DES.                                                                                                                                                     | Schlüssellänge: 168 Bits. Standardmodus: Verschlüsselungsblockverkettung.<br/> Blockgröße: 64 Bits.<br/> Es ist kein Salt zulässig.<br/>                           |
| CALG \_ 3DES \_ 112    | Dreifache [*DES-Verschlüsselung mit zwei*](../secgloss/t-gly.md) Schlüsseln.                                                            | Schlüssellänge: 112 Bits. Standardmodus: Verschlüsselungsblockverkettung.<br/> Blockgröße: 64 Bits.<br/> Es ist kein Salt zulässig.<br/>                           |
| CALG \_ DES          | DES-Verschlüsselung.                                                                                                                                                 | Schlüssellänge: 56 Bits. Standardmodus: Verschlüsselungsblockverkettung.<br/> Blockgröße: 64 Bits.<br/> Es ist kein Salt zulässig.<br/>                            |
| CALG \_ HMAC         | MAC-schlüsselgebundener Hashalgorithmus                                                                                                                                       | HMAC-Berechnung.                                                                                                                                          |
| CALG \_ MAC          | [*Nachrichtenauthentifizierungscode*](../secgloss/m-gly.md) (MAC) mit Schlüsselhashalgorithmus. | Mac-Verschlüsselung blockieren.                                                                                                                                          |
| CALG \_ MD2          | MD2-Hashalgorithmus                                                                                                                                          | Weitere Informationen finden Sie unter [*MD2-Algorithmus.*](../secgloss/m-gly.md)                                       |
| CALG \_ MD5          | MD5-Hashalgorithmus                                                                                                                                          | Weitere Informationen finden Sie unter [*MD5-Algorithmus.*](../secgloss/m-gly.md)                                       |
| CALG \_ RC2          | RC2-Blockverschlüsselungsalgorithmus.                                                                                                                                 | Schlüssellänge: 128 Bits. Standardmodus: Verschlüsselungsblockverkettung.<br/> Blockgröße: 64 Bits.<br/> Salt-Länge: Kann festgelegt werden.<br/>                   |
| CALG \_ RC4          | RC4-Streamverschlüsselungsalgorithmus.                                                                                                                                | Schlüssellänge: 128 Bits. Salt-Länge: Kann festgelegt werden.<br/>                                                                                                   |
| CALG \_ RSA \_ KEYX    | Rsa-Algorithmus für den Austausch öffentlicher Schlüssel.                                                                                                                              | Schlüssellänge: Kann festgelegt werden, 384 Bits bis 16.384 Bits in 8-Bit-Schritten. Standardschlüssellänge: 1.024 Bits.<br/>                                            |
| CALG \_ RSA \_ SIGN    | Signaturalgorithmus für den öffentlichen RSA-Schlüssel.                                                                                                                             | Schlüssellänge: Kann festgelegt werden, 384 Bits bis 16.384 Bits in 8-Bit-Schritten. Standardschlüssellänge: 1.024 Bits.<br/> Die Signatur entspricht PKCS \# 6.<br/> |
| CALG \_ SHA          | SHA-Hashalgorithmus                                                                                                                                          | Weitere Informationen finden Sie unter [*Secure Hash Algorithm*](../secgloss/s-gly.md).               |
| CALG \_ SHA1         | Identisch mit CALG \_ SHA.                                                                                                                                              | Weitere Informationen finden Sie unter [*Secure Hash Algorithm*](../secgloss/s-gly.md).               |
| CALG \_ SSL3 \_ SHAMD5 | SSL3-Clientauthentifizierungsalgorithmus.                                                                                                                           | Weitere Informationen finden Sie unter [Creating a CALG \_ SSL3 \_ SHAMD5 Hash](creating-a-calg-ssl3-shamd5-hash.md).                                                      |



 

 

 
