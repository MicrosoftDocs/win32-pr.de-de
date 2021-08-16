---
description: BLOBs werden mit dem Diffie-Hellman verwendet, um Schlüssel aus dem Kryptografiedienstanbieter (Cryptographic Service Provider, CSP) zu exportieren und in diese zu importieren.
ms.assetid: 052f2108-d402-41a0-b4ac-e93ba6b06b49
title: Diffie-Hellman Key BLOBs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8e993daf5b9ec0509ae6fa01df4edc06bafec733bb80f7b014921026fbc35ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767714"
---
# <a name="diffie-hellman-key-blobs"></a>Diffie-Hellman Key BLOBs

[*BLOBs werden*](../secgloss/b-gly.md) mit dem [*Diffie-Hellman-Anbieter*](../secgloss/d-gly.md) verwendet, um Schlüssel aus dem Kryptografiedienstanbieter (Cryptographic [*Service Provider,*](../secgloss/c-gly.md) CSP) zu exportieren und in diese zu importieren.

-   [BLOBs mit öffentlichem Schlüssel](#public-key-blobs)
-   [BLOBs für private Schlüssel](#private-key-blobs)

## <a name="public-key-blobs"></a>BLOBs mit öffentlichem Schlüssel

Diffie-Hellman öffentlichen [*Schlüsselblobs*](../secgloss/p-gly.md)vom Typ **PUBLICKEYBLOB** werden verwendet, um den (G^X) mod P-Wert in einem Diffie-Hellman austauschen. Diese Schlüssel werden als Bytesequenz im folgenden Format exportiert und importiert.

``` syntax
PUBLICKEYSTRUC  publickeystruc; 
DHPUBKEY dhpubkey;
BYTE y[dhpubkey.bitlen/8]; // Where y = (G^X) mod P
```

In der folgenden Tabelle werden die einzelnen Komponenten des [*Schlüsselblobs beschrieben.*](../secgloss/k-gly.md)



| Feld          | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dhpubkey       | Eine [**DHPUBKEY-Struktur.**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) Der **Magic-Member** sollte auf 0x31484400. Dieser Hexadezimalwert ist die [*ASCII-Codierung*](../secgloss/a-gly.md) von "DH1".                                                                                                                                                                                                                                                                                                                                                                 |
| publickeystruc | Eine [**PUBLICKEYSTRUC-Struktur.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| y              | Eine **BYTE-Sequenz.** Der Y-Wert (G^X) mod P befindet sich direkt hinter der [**DHPUBKEY-Struktur**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) und sollte immer die Länge des **DHPUBKEY-Bitlenfelds** (Bitlänge P) in Byte sein, geteilt durch acht. Wenn die Länge der Daten, die sich aus der Berechnung von (G^X) mod P ergeben, mindestens ein Byte kürzer als P geteilt durch acht ist, müssen die Daten mit den erforderlichen Bytes (null) aufschlossen werden, damit die Daten die gewünschte Länge haben [*(Little-Endian-Format).*](../secgloss/l-gly.md) |



 

## <a name="private-key-blobs"></a>BLOBs für private Schlüssel

Diffie-Hellman [*BLOBs*](../secgloss/p-gly.md)mit privatem Schlüssel vom Typ **PRIVATEKEYBLOB** werden verwendet, um die öffentlichen/privaten Informationen eines Diffie-Hellman zu speichern. Diese Schlüssel werden als Bytesequenz im folgenden Format exportiert und importiert.

``` syntax
PUBLICKEYSTRUC  publickeystruc; 
DHPUBKEY        dhpubkey;
BYTE            prime[dhpubkey.bitlen/8];
BYTE            generator[dhpubkey.bitlen/8];
BYTE            secret[dhpubkey.bitlen/8];
```

In der folgenden Tabelle werden die einzelnen Komponenten des Schlüsselblobs beschrieben.



| Feld          | Beschreibung                                                                                                                                                                                                  |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dhpubkey       | Eine [**DHPUBKEY-Struktur.**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) Der **Magic-Member** muss auf 0x32484400. Dieser Hexadezimalwert ist die [*ASCII-Codierung*](../secgloss/a-gly.md) von "DH2". |
| Generator      | Eine **BYTE-Sequenz.** Der Generator, G.                                                                                                                                                                       |
| publickeystruc | Eine [**PUBLICKEYSTRUC-Struktur.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)                                                                                                                                                        |
| Prime          | Eine **BYTE-Sequenz.** Der Primmodulus P. Für diese Daten muss immer das wichtigste Bit des wichtigsten Byte auf 1 festgelegt sein.                                                                      |
| secret         | Eine **BYTE-Sequenz.** Der Geheimnis exponent, X.                                                                                                                                                                 |



 

> [!Note]  
> Der Generator und das Geheimnis müssen immer die gleiche Länge in Bytes haben. Wenn eines der Byte oder kürzer als das andere ist, muss es mit der erforderlichen Anzahl von Nullwertbytes aufschlossen werden, um sie gleich zu machen. Sowohl der Generator als auch das Geheimnis haben das [*Little-Endian-Format.*](../secgloss/l-gly.md)

 

 

 
