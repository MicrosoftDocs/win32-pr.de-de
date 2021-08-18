---
description: BLOBs werden mit dem RSA/Schannel-Anbieter verwendet, um Schlüssel aus dem Kryptografiedienstanbieter (Cryptographic Service Provider, CSP) zu exportieren und in diesen zu importieren.
ms.assetid: 97d5ee6d-4687-4cd2-b122-36f8ea3c93ca
title: RSA/Schannel-Schlüssel-BLOBs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3be8bfa8b87ee901317e220583ff7b08ea110e342a2d9dd9abb477053ffdf05c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900535"
---
# <a name="rsaschannel-key-blobs"></a>RSA/Schannel-Schlüssel-BLOBs

[*BLOBs*](../secgloss/b-gly.md) werden mit dem [*RSA*](../secgloss/r-gly.md) / [*Schannel-Anbieter*](../secgloss/s-gly.md) verwendet, um Schlüssel aus dem [*Kryptografiedienstanbieter (Cryptographic Service Provider,*](../secgloss/c-gly.md) CSP) zu exportieren und in diesen zu importieren.

-   [BLOBs mit öffentlichem Schlüssel](#public-key-blobs)
-   [Private Schlüsselblobs](#private-key-blobs)
-   [Einfache Schlüsselblobs](#simple-key-blobs)

## <a name="public-key-blobs"></a>BLOBs mit öffentlichem Schlüssel

[*BLOBs*](../secgloss/p-gly.md)mit öffentlichem Schlüssel , typ **PUBLICKEYBLOB,** werden verwendet, um [*öffentliche Schlüssel*](../secgloss/p-gly.md)zu speichern. Diese Schlüssel werden als Bytesequenz im folgenden Format exportiert und importiert.

``` syntax
PUBLICKEYSTRUC  publickeystruc ;
RSAPUBKEY       rsapubkey;
BYTE            modulus[rsapubkey.bitlen/8];
```

In der folgenden Tabelle werden die einzelnen Komponenten des öffentlichen Schlüssels beschrieben. Alle Werte liegen im [*Little-Endian-Format*](../secgloss/l-gly.md) vor.



| Feld          | BESCHREIBUNG                                                                                                                                                                                                                                                                                        |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| modulus        | Eine **BYTE-Sequenz.** Die Modulusdaten des öffentlichen Schlüssels befinden sich direkt nach der **RSAPUBKEY-Struktur.** Die Länge dieser Daten variiert je nach Länge des öffentlichen Schlüssels. Die Anzahl der Bytes kann bestimmt werden, indem der Wert des **Bitlenmembers** von **RSAPUBKEY** durch acht dividiert wird. |
| publickeystruc | Eine [**PUBLICKEYSTRUC-Struktur.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)                                                                                                                                                                                                                                              |
| rsapubkey      | Eine [**RSAPUBKEY-Struktur.**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) Der **Magic-Member** muss auf 0x31415352 festgelegt werden. Dieser Hexadezimalwert ist die [*ASCII-Codierung*](../secgloss/a-gly.md) von RSA1.                                                                                      |



 

> [!Note]  
> BLOBs mit öffentlichem Schlüssel werden nicht verschlüsselt. Sie enthalten öffentliche Schlüssel in [*Klartextform.*](../secgloss/p-gly.md)

 

## <a name="private-key-blobs"></a>Private Schlüsselblobs

[*Private Schlüssel-BLOBs*](../secgloss/p-gly.md)vom Typ **PRIVATEKEYBLOB** werden verwendet, um [*öffentliche/private Schlüsselpaare*](../secgloss/p-gly.md)zu speichern. Diese Schlüssel werden als Bytesequenz im folgenden Format exportiert und importiert.

``` syntax
PUBLICKEYSTRUC  publickeystruc ;
RSAPUBKEY       rsapubkey;
BYTE            modulus[rsapubkey.bitlen/8];
BYTE            prime1[rsapubkey.bitlen/16];
BYTE            prime2[rsapubkey.bitlen/16];
BYTE            exponent1[rsapubkey.bitlen/16];
BYTE            exponent2[rsapubkey.bitlen/16];
BYTE            coefficient[rsapubkey.bitlen/16];
BYTE            privateExponent[rsapubkey.bitlen/8];
```

Wenn das [*Schlüsselblob*](../secgloss/k-gly.md) verschlüsselt ist, wird alles außer dem [**PUBLICKEYSTRUC-Teil**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) des BLOB verschlüsselt.

> [!Note]  
> Der Verschlüsselungsalgorithmus und die Verschlüsselungsschlüsselparameter werden nicht zusammen mit dem BLOB des privaten Schlüssels gespeichert. Es liegt in der Verantwortung der Anwendung, diese Informationen zu verwalten.

 

In der folgenden Tabelle werden die einzelnen BLOB-Komponenten für private Schlüssel beschrieben.

> [!Note]  
> Diese Felder entsprechen den Feldern, die in Abschnitt 7.2 von [*Public Key Cryptography Standards*](../secgloss/p-gly.md) (PKCS) \# 1 mit geringfügigen Unterschieden beschrieben werden.

 



| Feld           | BESCHREIBUNG                                                                                                                                                                                                   |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| exponent1       | Eine **BYTE-Sequenz.** Der erste Exponent. Dieser weist den numerischen Wert d mod (p – 1) auf.                                                                                                                           |
| exponent2       | Eine **BYTE-Sequenz.** Der zweite Exponent. Dieser weist den numerischen Wert d mod (q – 1) auf.                                                                                                                          |
| Koeffizient     | Eine **BYTE-Sequenz.** Koeffizient. Dieser weist den numerischen Wert (umkehrend von q) mod p auf.                                                                                                                           |
| Modulus         | Eine **BYTE-Sequenz.** Der Modulus. Diese weist eine Zeichenfolge auf, die *Prime1* \* *Prime2* enthält. Sie wird häufig als n bezeichnet.                                                                                               |
| prime1          | Eine **BYTE-Sequenz.** Primzahl 1, häufig als p bezeichnet.                                                                                                                                                        |
| prime2          | Eine **BYTE-Sequenz.** Primzahl 2, häufig als q bezeichnet.                                                                                                                                                        |
| publickeystruc  | Eine [**PUBLICKEYSTRUC-Struktur.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)                                                                                                                                                         |
| privateExponent | Eine **BYTE-Sequenz.** Der private Exponent, häufig als d bezeichnet.                                                                                                                                                  |
| rsapubkey       | Eine [**RSAPUBKEY-Struktur.**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) Der **magic-Member** muss auf 0x32415352 festgelegt werden. Dieser Hexadezimalwert ist die [*ASCII-Codierung*](../secgloss/a-gly.md) von RSA2. |



 

> [!Note]  
> Private Schlüsselblobs werden nicht verschlüsselt. Sie enthalten private Schlüssel in Klartextform.

 

Beim Aufrufen von [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)kann der Entwickler auswählen, ob der Schlüssel verschlüsselt werden soll. **PRIVATEKEYBLOB** wird verschlüsselt, wenn der *hExpKey-Parameter* ein gültiges Handle für einen Sitzungsschlüssel enthält. Alles außer dem [**PUBLICKEYSTRUC-Teil**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) des BLOB wird verschlüsselt.

> [!Note]  
> Der Verschlüsselungsalgorithmus und die Verschlüsselungsschlüsselparameter werden nicht zusammen mit dem BLOB des privaten Schlüssels gespeichert. Die Anwendung muss diese Informationen verwalten und speichern. Wenn 0 (null) für *hExpKey* übergeben wird, wird der private Schlüssel ohne Verschlüsselung exportiert.

 

> [!Caution]  
> Es ist gefährlich, private Schlüssel ohne Verschlüsselung zu exportieren, da sie dann anfällig für abfangende und nicht autorisierte Entitäten sind.

 

## <a name="simple-key-blobs"></a>Einfache Schlüsselblobs

[*Einfache Schlüssel-BLOBs*](../secgloss/s-gly.md)vom Typ **SIMPLEBLOB** werden zum Speichern und Transport von Sitzungsschlüsseln verwendet. Diese werden immer mit einem öffentlichen Schlüssel für den [*Schlüsselaustausch*](../secgloss/k-gly.md)verschlüsselt. Diese Schlüssel werden als Bytesequenz im folgenden Format exportiert und importiert.

``` syntax
PUBLICKEYSTRUC  publickeystruc ;
ALG_ID          algid;
BYTE            encryptedkey[rsapubkey.bitlen/8];
```

In der folgenden Tabelle werden die einzelnen einfachen BLOB-Komponenten beschrieben.



| Feld          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                   |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| algid          | Eine [**\_ ALG-ID-Struktur.**](alg-id.md) Dies gibt in der Regel den CALG \_ RSA \_ KEYX-Algorithmus an, der angibt, dass die Sitzungsschlüsseldaten mit einem öffentlichen Schlüsselaustauschschlüssel verschlüsselt wurden, indem der [*RSA Public Key-Algorithmus*](../secgloss/r-gly.md)verwendet wird. |
| Encryptedkey   | Eine **BYTE-Sequenz.** Die verschlüsselten Sitzungsschlüsseldaten haben die Form eines PKCS \# 1-Verschlüsselungsblocks vom Typ 2. Informationen zu diesem Datenformat finden Sie unter Public Key Cryptography Standards (PKCS), veröffentlicht von RSA Data Security, Inc.                                                                                     |
| publickeystruc | Eine [**PUBLICKEYSTRUC-Struktur.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)                                                                                                                                                                                                                                                                         |



 

Diese Daten haben immer die gleiche Größe wie der Modulus des öffentlichen Schlüssels. Beispielsweise haben öffentliche Schlüssel, die vom Microsoft Base Cryptographic Provider generiert werden, immer eine Länge von 512 Bits (64 Bytes), sodass die verschlüsselten Sitzungsschlüsseldaten ebenfalls immer 64 Bytes betragen.

 

 
