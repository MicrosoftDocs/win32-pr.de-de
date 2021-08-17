---
description: BLOBs werden mit dem Diffie-Hellman/Schannel-Anbieter verwendet, um Schlüssel aus dem Kryptografiedienstanbieter (Cryptographic Service Provider, CSP) zu exportieren und in diesen zu importieren.
ms.assetid: ebb85b7c-204d-4b1c-86dc-5a03c8eda47b
title: Diffie-Hellman/Schannel Key BLOBs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03c653e26f53611e8b00a1dae4e49df7084e6dc655d67f11550a430860fab12d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767694"
---
# <a name="diffie-hellmanschannel-key-blobs"></a>Diffie-Hellman/Schannel Key BLOBs

[*BLOBs*](../secgloss/b-gly.md) werden mit dem [*Diffie-Hellman*](../secgloss/d-gly.md) / [*Schannel-Anbieter*](../secgloss/s-gly.md) verwendet, um Schlüssel aus dem [*Kryptografiedienstanbieter (Cryptographic Service Provider,*](../secgloss/c-gly.md) CSP) zu exportieren und in diesen zu importieren.

-   [BLOBs mit öffentlichem Schlüssel](#public-key-blobs)
-   [Private Schlüsselblobs](#private-key-blobs)

## <a name="public-key-blobs"></a>BLOBs mit öffentlichem Schlüssel

Diffie-Hellman [*BLOBs*](../secgloss/p-gly.md)mit öffentlichem Schlüssel , geben Sie **PUBLICKEYBLOB** ein, werden verwendet, um den Mod P-Wert (G^X) in einem Diffie-Hellman Schlüsselaustausch auszutauschen. Diese Schlüssel werden als Bytesequenz im folgenden Format exportiert und importiert.

``` syntax
PUBLICKEYSTRUC  publickeystruc;
DHPUBKEY        dhpubkey;
BYTE            y[dhpubkey.bitlen/8]; // Where y = (G^X) mod P
```

In der folgenden Tabelle werden die einzelnen Komponenten des [*Schlüssel-BLOB*](../secgloss/k-gly.md)beschrieben.



| Feld          | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dhpubkey       | Eine [**DHPUBKEY-Struktur.**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) Der **magic-Member** muss auf 0x31484400 festgelegt werden. Dieser Hexadezimalwert ist die [*ASCII-Codierung*](../secgloss/a-gly.md) von DH1.                                                                                                                                                                                                                                                                                                                                                      |
| publickeystruc | Eine [**PUBLICKEYSTRUC-Struktur.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| y              | Eine **BYTE-Sequenz.** Der y-Wert (G^X) mod P befindet sich direkt hinter der [**DHPUBKEY-Struktur.**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) Die Länge der Sequenz in Bytes ist der **Bitlenmember** von **DHPUBKEY** geteilt durch acht. Wenn die Länge der Daten, die sich aus der Berechnung von (G^X) mod P ergeben, ein oder mehrere Bytes kürzer als P dividiert durch acht ist, müssen die Daten mit den erforderlichen Bytes (null Wert) aufgefüllt werden, damit die Daten die gewünschte Länge [*(Little-Endian-Format)*](../secgloss/l-gly.md) erhalten. |



 

## <a name="private-key-blobs"></a>Private Schlüsselblobs

Private [*D-H-Schlüsselblobs*](../secgloss/p-gly.md)vom Typ **PRIVATEKEYBLOB** werden verwendet, um private Informationen eines D-H-Schlüssels zu exportieren und zu importieren. Diese Schlüssel werden als Bytesequenz im folgenden Format exportiert und importiert.

``` syntax
PUBLICKEYSTRUC  publickeystruc;
DHPUBKEY        dhpubkey;
BYTE            prime[dhpubkey.bitlen/8];
BYTE            generator[dhpubkey.bitlen/8];
BYTE            secret[dhpubkey.bitlen/8];
```

In der folgenden Tabelle werden die einzelnen Komponenten des Schlüsselblobs beschrieben.



| Feld          | Beschreibung                                                                                                                                                                                                |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dhpubkey       | Eine [**DHPUBKEY-Struktur.**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) Der **magic-Member** muss auf 0x32484400 festgelegt werden. Dieser Hexadezimalwert ist die [*ASCII-Codierung*](../secgloss/a-gly.md) von DH2. |
| Generator      | Eine **BYTE-Sequenz.** Der Generator G.                                                                                                                                                                      |
| publickeystruc | Eine [**PUBLICKEYSTRUC-Struktur.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)                                                                                                                                                      |
| Prime          | Eine **BYTE-Sequenz.** Der Primmodulus P. Für diese Daten muss immer das wichtigste Bit des wichtigsten Byte auf 1 festgelegt sein.                                                                    |
| secret         | Eine **BYTE-Sequenz.** Der geheime Exponent X.                                                                                                                                                                |



 

> [!Note]  
> Die Werte für Primzahl, Generator und Geheimnis müssen immer die gleiche Länge in Bytes aufweisen. Wenn ein Wert ein Byte oder kürzer als die anderen ist, muss er mit der erforderlichen Anzahl von 0 Bytes aufgefüllt werden, um sie gleich zu machen. Primzahl, Generator und Geheimnis liegen im [*Little-Endian-Format*](../secgloss/l-gly.md) vor.

 

 

 
