---
description: Der Basisanbieter und der erweiterte Anbieter verwenden die gleichen Schlüssel-BLOBs.
ms.assetid: b4592036-0fa3-4b7e-beed-78cf1d2f39a9
title: Basisanbieter-Schlüssel-BLOBs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d95eaeaa1b6438045ebba55d2bb45785e4068154ff51818e937bc434dff7fb29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773042"
---
# <a name="base-provider-key-blobs"></a>Basisanbieter-Schlüssel-BLOBs

Der Basisanbieter und der erweiterte Anbieter verwenden die gleichen [*Schlüssel-BLOBs.*](../secgloss/k-gly.md)

-   [BLOBs mit öffentlichem Schlüssel](#public-key-blobs)
-   [Private Schlüsselblobs](#private-key-blobs)
-   [Einfache Schlüsselblobs](#simple-key-blobs)

## <a name="public-key-blobs"></a>BLOBs mit öffentlichem Schlüssel

[*Öffentliche Schlüssel-BLOBs*](../secgloss/p-gly.md)vom Typ **PUBLICKEYBLOB** werden verwendet, um [*öffentliche Schlüssel*](../secgloss/p-gly.md) außerhalb eines [*Kryptografiedienstanbieters (Cryptographic Service Provider,*](../secgloss/c-gly.md) CSP) zu speichern. Basisanbieter-BLOBs mit öffentlichem Schlüssel weisen das folgende Format auf.

``` syntax
PUBLICKEYSTRUC  publickeystruc;
RSAPUBKEY rsapubkey;
BYTE modulus[rsapubkey.bitlen/8];
```

In der folgenden Tabelle werden die einzelnen Komponenten des öffentlichen Schlüssels beschrieben. Alle Werte liegen im [*Little-Endian-Format*](../secgloss/l-gly.md) vor.



| Feld          | Beschreibung                                                                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| modulus        | Die Modulusdaten des öffentlichen Schlüssels befinden sich direkt nach der [**RSAPUBKEY-Struktur.**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) Die Größe dieser Daten variiert je nach Größe des öffentlichen Schlüssels. Die Anzahl der Bytes kann bestimmt werden, indem der Wert des **RSAPUBKEY-Bitlenfelds** durch acht dividiert wird. |
| publickeystruc | Eine [**PUBLICKEYSTRUC-Struktur.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)                                                                                                                                                                                                                                 |
| rsapubkey      | Eine [**RSAPUBKEY-Struktur.**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) Der **Magic-Member** muss auf 0x31415352 festgelegt werden. Dieser Hexadezimalwert ist die [*ASCII-Codierung*](../secgloss/a-gly.md) von RSA1.                                                                         |



 

> [!Note]  
> BLOBs mit öffentlichem Schlüssel werden nicht verschlüsselt. Sie enthalten öffentliche Schlüssel in [*Klartextform.*](../secgloss/p-gly.md)

 

## <a name="private-key-blobs"></a>Private Schlüsselblobs

[*Private Schlüssel-BLOBs*](../secgloss/p-gly.md)vom Typ **PRIVATEKEYBLOB** werden verwendet, um [*private Schlüssel*](../secgloss/p-gly.md) außerhalb eines CSP zu speichern. Basisanbieter-BLOBs mit privatem Schlüssel weisen das folgende Format auf.

``` syntax
PUBLICKEYSTRUC  publickeystruc;
RSAPUBKEY rsapubkey;
BYTE modulus[rsapubkey.bitlen/8];
BYTE prime1[rsapubkey.bitlen/16];
BYTE prime2[rsapubkey.bitlen/16];
BYTE exponent1[rsapubkey.bitlen/16];
BYTE exponent2[rsapubkey.bitlen/16];
BYTE coefficient[rsapubkey.bitlen/16];
BYTE privateExponent[rsapubkey.bitlen/8];
```

In der folgenden Tabelle wird die BLOB-Komponente des privaten Schlüssels beschrieben.

> [!Note]  
> Diese Felder entsprechen den Feldern, die in Abschnitt 7.2 von [*Public Key Cryptography Standards*](../secgloss/p-gly.md) (PKCS) \# 1 mit geringfügigen Unterschieden beschrieben werden.

 



| Feld           | Beschreibung                                                                                                                                                                                                   |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Koeffizient     | Koeffizient. Dieser weist den numerischen Wert (umkehrend von q) mod p auf.                                                                                                                                                |
| exponent1       | Exponent 1. Dieser weist den numerischen Wert d mod (p – 1) auf.                                                                                                                                                        |
| exponent2       | Exponent 2. Dieser weist den numerischen Wert d mod (q – 1) auf.                                                                                                                                                        |
| Modulus         | Der Modulus. Dieser hat den Wert *Prime1*×*Prime2* und wird häufig als n bezeichnet.                                                                                                                                   |
| prime1          | Primzahl 1, häufig als p bezeichnet.                                                                                                                                                                             |
| prime2          | Primzahl 2, häufig als q bezeichnet.                                                                                                                                                                             |
| privateExponent | Privater Exponent, häufig als d bezeichnet.                                                                                                                                                                           |
| publickeystruc  | Eine [**PUBLICKEYSTRUC-Struktur.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)                                                                                                                                                         |
| rsapubkey       | Eine [**RSAPUBKEY-Struktur.**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) Der **magic-Member** muss auf 0x32415352 festgelegt werden. Dieser Hexadezimalwert ist die [*ASCII-Codierung*](../secgloss/a-gly.md) von RSA2. |



 

> [!Note]  
> Private Schlüsselblobs werden nicht verschlüsselt. Sie enthalten private Schlüssel in Klartextform.

 

Beim Aufrufen von [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)kann der Entwickler auswählen, ob der Schlüssel verschlüsselt werden soll. **PRIVATEKEYBLOB** wird verschlüsselt, wenn der *hExpKey-Parameter* ein gültiges Handle für einen Sitzungsschlüssel enthält. Alles außer dem [**PUBLICKEYSTRUC-Teil**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) des BLOB wird verschlüsselt.

> [!Note]  
> Der Verschlüsselungsalgorithmus und die Verschlüsselungsschlüsselparameter werden nicht zusammen mit dem BLOB des privaten Schlüssels gespeichert. Die Anwendung muss diese Informationen verwalten und speichern. Wenn 0 (null) für *hExpKey* übergeben wird, wird der private Schlüssel ohne Verschlüsselung exportiert.

 

> [!Caution]  
> Es ist gefährlich, private Schlüssel ohne Verschlüsselung zu exportieren, da sie dann anfällig für abfangende und nicht autorisierte Entitäten sind.

 

## <a name="simple-key-blobs"></a>Einfache Schlüsselblobs

[*Einfache Schlüssel-BLOBs*](../secgloss/s-gly.md)vom Typ **SIMPLEBLOB** werden verwendet, um Sitzungsschlüssel außerhalb eines CSP zu speichern und zu transportieren. Basisanbieter-BLOBs mit einfachen Schlüsseln werden immer mit einem [*öffentlichen Schlüssel für den Schlüsselaustausch*](../secgloss/k-gly.md)verschlüsselt. Der **pbData-Member** von **SIMPLEBLOB** ist eine Bytefolge im folgenden Format.

``` syntax
PUBLICKEYSTRUC  publickeystruc;
ALG_ID algid;
BYTE encryptedkey[rsapubkey.bitlen/8];
```

In der folgenden Tabelle werden die einzelnen Komponenten des **pbData-Members** von **SIMPLEBLOB** beschrieben.



| Feld          | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| algid          | Eine [**\_ ALG-ID-Struktur,**](alg-id.md) die den Verschlüsselungsalgorithmus zum Verschlüsseln der Sitzungsschlüsseldaten angibt. Dieser weist in der Regel den Wert CALG \_ RSA \_ KEYX auf, der angibt, dass die Sitzungsschlüsseldaten mit einem öffentlichen Schlüsselaustauschschlüssel mit dem [*RSA-Algorithmus für öffentliche Schlüssel*](../secgloss/r-gly.md)verschlüsselt wurden.                                                                                                                           |
| Encryptedkey   | Eine **BYTE-Sequenz,** die die verschlüsselten Sitzungsschlüsseldaten in Form eines PKCS \# 1-Verschlüsselungsblocks vom Typ 2 darstellt. Informationen zu diesem Datenformat finden Sie unter Public Key Cryptography Standards (PKCS) \# 1, veröffentlicht von RSA Data Security, Inc. Diese Daten haben immer die gleiche Größe wie der Modulus des öffentlichen Schlüssels. Beispielsweise können öffentliche Schlüssel, die vom Microsoft RSA-Basisanbieter generiert werden, eine Länge von 512 Bits (64 Bytes) haben, sodass die verschlüsselten Sitzungsschlüsseldaten ebenfalls immer 512 Bits (64 Bytes) haben.<br/> |
| publickeystruc | Eine [**PUBLICKEYSTRUC-Struktur.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

 

 
