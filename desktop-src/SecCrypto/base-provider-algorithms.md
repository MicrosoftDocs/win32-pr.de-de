---
description: Der Microsoft Base Cryptographic Provider unterstützt die folgenden Algorithmen.
ms.assetid: 767d5192-6e8f-488a-b954-29d56488ccbb
title: Basisanbieteralgorithmen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6b6f3af49529ad46e70dd154c06febf433f5fb483861f7c0b2530af7ebbef2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879750"
---
# <a name="base-provider-algorithms"></a>Basisanbieteralgorithmen

Der Microsoft Base Cryptographic Provider unterstützt die folgenden Algorithmen.



| Algorithmus-ID                  | BESCHREIBUNG                                                                                                                                                               | Kommentare                                                                                                                                                                |
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CALG \_ MD2<br/>          | MD2-Hashalgorithmus<br/>                                                                                                                                          | Weitere Informationen finden Sie unter [*MD2-Algorithmus.*](../secgloss/m-gly.md)<br/>                                         |
| CALG \_ MD5<br/>          | MD5-Hashalgorithmus<br/>                                                                                                                                          | Weitere Informationen finden Sie unter [*MD5-Algorithmus.*](../secgloss/m-gly.md)<br/>                                         |
| CALG \_ SHA<br/>          | SHA-Hashalgorithmus<br/>                                                                                                                                          | Weitere Informationen finden Sie unter [*Sicherer Hashalgorithmus.*](../secgloss/s-gly.md)<br/>                 |
| CALG \_ SHA1<br/>         | Identisch mit CALG \_ SHA<br/>                                                                                                                                              | Weitere Informationen finden Sie unter [*Sicherer Hashalgorithmus.*](../secgloss/s-gly.md)<br/>                 |
| CALG \_ MAC<br/>          | keyed-hash-Algorithmus (MAC) [*für Nachrichtenauthentifizierungscode*](../secgloss/m-gly.md)<br/> | Mac-Verschlüsselung blockieren.<br/>                                                                                                                                            |
| CALG \_ HMAC<br/>         | MAC-Schlüsselhashalgorithmus<br/>                                                                                                                                       | HMAC-Berechnung.<br/>                                                                                                                                            |
| CALG \_ SSL3 \_ SHAMD5<br/> | SLL3-Clientauthentifizierungsalgorithmus<br/>                                                                                                                           | Weitere Informationen finden Sie unter [Creating a CALG \_ SSL3 \_ SHAMD5 Hash](creating-a-calg-ssl3-shamd5-hash.md).<br/>                                                        |
| CALG \_ RSA \_ SIGN<br/>    | RSA-Algorithmus für die Signatur mit öffentlichem Schlüssel<br/>                                                                                                                             | Schlüssellänge: Kann von 384 Bits auf 16.384 Bits in 8-Bit-Schritten festgelegt werden.<br/> Standardschlüssellänge: 512 Bits.<br/> Die Signatur entspricht PKCS \# 6.<br/> |
| CALG \_ RSA \_ KEYX<br/>    | RSA-Algorithmus für den Austausch öffentlicher Schlüssel<br/>                                                                                                                              | Schlüssellänge: Kann von 384 Bits auf 1024 Bits in 8-Bit-Schritten festgelegt werden.<br/> Standardschlüssellänge: 512 Bits.<br/>                                              |
| CALG \_ RC2<br/>          | RC2-Blockverschlüsselungsalgorithmus<br/>                                                                                                                                 | Schlüssellänge: 40 Bits.<br/> Standardmodus: Verschlüsselungsblockverkettung.<br/> Blockgröße: 64 Bits.<br/> Salt-Länge: 88 Bits.<br/>                        |
| CALG \_ RC4<br/>          | RC4-Datenstromverschlüsselungsalgorithmus<br/>                                                                                                                                | Schlüssellänge: 40 Bits.<br/> Salt-Länge: 88 Bits.<br/>                                                                                                        |
| CALG \_ DES<br/>          | DES-Verschlüsselung<br/>                                                                                                                                                 | Weitere Informationen finden Sie unter [*Data Encryption Standard*](../secgloss/d-gly.md) (DES).<br/>  |



 

 

 
