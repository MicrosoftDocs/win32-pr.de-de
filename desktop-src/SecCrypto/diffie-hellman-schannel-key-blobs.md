---
description: BLOB werden mit dem Diffie-Hellman/SChannel-Anbieter verwendet, um Schlüssel aus dem Kryptografiedienstanbieter (kryptografischen Service Provider, CSP) zu exportieren und Schlüssel in zu importieren.
ms.assetid: ebb85b7c-204d-4b1c-86dc-5a03c8eda47b
title: Diffie-Hellman/SChannel-Schlüsselblob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a76869c6c6239e17a5ae14921805a076c9381c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756535"
---
# <a name="diffie-hellmanschannel-key-blobs"></a>Diffie-Hellman/SChannel-Schlüsselblob

[*BLOB*](../secgloss/b-gly.md) werden mit dem [*Diffie-Hellman*](../secgloss/d-gly.md) / [*SChannel*](../secgloss/s-gly.md) -Anbieter verwendet, um Schlüssel aus dem [*Kryptografiedienstanbieter (kryptografischen Service Provider*](../secgloss/c-gly.md) , CSP) zu exportieren und Schlüssel in zu importieren.

-   [Blobschlüssel für öffentliche Schlüssel](#public-key-blobs)
-   [Blobschlüssel für private Schlüssel](#private-key-blobs)

## <a name="public-key-blobs"></a>Blobschlüssel für öffentliche Schlüssel

Geben Sie Diffie-Hellman [*BLOBs für öffentliche Schlüssel*](../secgloss/p-gly.md)den Wert **PublicKeyBlob** ein, mit dem der (G ^ X) mod P-Wert in einem Diffie-Hellman-Schlüsselaustausch ausgetauscht wird. Diese Schlüssel werden als Bytefolge im folgenden Format exportiert und importiert.

``` syntax
PUBLICKEYSTRUC  publickeystruc;
DHPUBKEY        dhpubkey;
BYTE            y[dhpubkey.bitlen/8]; // Where y = (G^X) mod P
```

In der folgenden Tabelle werden die einzelnen Komponenten des [*Schlüssel-BLOBs*](../secgloss/k-gly.md)beschrieben.



| Feld          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dhpubkey       | Eine [**dhpubkey**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) -Struktur. Der **Magic** -Member muss auf 0x31484400 festgelegt werden. Dieser Hexadezimalwert ist die [*ASCII*](../secgloss/a-gly.md) -Codierung von DH1.                                                                                                                                                                                                                                                                                                                                                      |
| publickeystruc | Eine [**publickeystruc**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) -Struktur.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Y              | Eine **Byte** Sequenz. Der y-Wert (G ^ X) mod P befindet sich direkt hinter der [**dhpubkey**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) -Struktur. Die Länge (in Byte) der Sequenz ist das **bitlen** -Element von **dhpubkey** , dividiert durch acht. Wenn die Länge der Daten, die sich aus der Berechnung von (G ^ X) mod P ergeben, mindestens ein Byte kürzer als P ist, das durch acht geteilt wird, müssen die Daten mit den erforderlichen Bytes (von NULL Wert) aufgefüllt werden, damit die Daten die gewünschte Länge haben ([*Little-Endian-*](../secgloss/l-gly.md) Format). |



 

## <a name="private-key-blobs"></a>Blobschlüssel für private Schlüssel

[*BLOBs für private Schlüssel*](../secgloss/p-gly.md)von d-h, Typ **privatekeyblob**, werden zum Exportieren und importieren privater Informationen eines D-H-Schlüssels verwendet. Diese Schlüssel werden als Bytefolge im folgenden Format exportiert und importiert.

``` syntax
PUBLICKEYSTRUC  publickeystruc;
DHPUBKEY        dhpubkey;
BYTE            prime[dhpubkey.bitlen/8];
BYTE            generator[dhpubkey.bitlen/8];
BYTE            secret[dhpubkey.bitlen/8];
```

In der folgenden Tabelle werden die einzelnen Komponenten des Schlüssel-BLOBs beschrieben.



| Feld          | BESCHREIBUNG                                                                                                                                                                                                |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dhpubkey       | Eine [**dhpubkey**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) -Struktur. Der **Magic** -Member muss auf 0x32484400 festgelegt werden. Dieser Hexadezimalwert ist die [*ASCII*](../secgloss/a-gly.md) -Codierung von DH2. |
| Generator      | Eine **Byte** Sequenz. Der Generator G.                                                                                                                                                                      |
| publickeystruc | Eine [**publickeystruc**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) -Struktur.                                                                                                                                                      |
| wichtigsten          | Eine **Byte** Sequenz. Der primmodulus (P). Diese Daten müssen immer das signifikanteste Bit aufweisen, das auf eins festgelegt ist.                                                                    |
| secret         | Eine **Byte** Sequenz. Der geheime Exponent X.                                                                                                                                                                |



 

> [!Note]  
> Der primwert, der Generator und der geheime Wert müssen immer dieselbe Länge haben (in Bytes). Wenn ein Wert ein Byte oder kürzer als der andere Wert ist, muss er mit der erforderlichen Anzahl von 0 Bytes aufgefüllt werden, damit diese identisch sind. Die Primzahl, der Generator und das Geheimnis liegen im [*Little-Endian-*](../secgloss/l-gly.md) Format vor.

 

 

 
