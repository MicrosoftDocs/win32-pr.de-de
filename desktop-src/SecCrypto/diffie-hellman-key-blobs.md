---
description: Blobvorgänge werden mit dem Diffie-Hellman-Anbieter verwendet, um Schlüssel aus dem Kryptografiedienstanbieter (CSP) zu exportieren und Schlüssel in zu importieren.
ms.assetid: 052f2108-d402-41a0-b4ac-e93ba6b06b49
title: Diffie-Hellman von schlüsselblobschlüsseln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9194a9c12542fc0acf36aa0064a2f3e304e25f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348603"
---
# <a name="diffie-hellman-key-blobs"></a>Diffie-Hellman von schlüsselblobschlüsseln

[*BLOB*](../secgloss/b-gly.md) werden mit dem [*Diffie-Hellman-*](../secgloss/d-gly.md) Anbieter verwendet, um Schlüssel aus dem [*Kryptografiedienstanbieter (kryptografischen Service Provider*](../secgloss/c-gly.md) , CSP) zu exportieren und Schlüssel in zu importieren.

-   [Blobschlüssel für öffentliche Schlüssel](#public-key-blobs)
-   [Blobschlüssel für private Schlüssel](#private-key-blobs)

## <a name="public-key-blobs"></a>Blobschlüssel für öffentliche Schlüssel

Geben Sie Diffie-Hellman [*BLOBs für öffentliche Schlüssel*](../secgloss/p-gly.md)den Wert **PublicKeyBlob** ein, mit dem der (G ^ X) mod P-Wert in einem Diffie-Hellman-Schlüsselaustausch ausgetauscht wird. Diese Schlüssel werden als Bytefolge im folgenden Format exportiert und importiert.

``` syntax
PUBLICKEYSTRUC  publickeystruc; 
DHPUBKEY dhpubkey;
BYTE y[dhpubkey.bitlen/8]; // Where y = (G^X) mod P
```

In der folgenden Tabelle werden die einzelnen Komponenten des [*Schlüssel-BLOBs*](../secgloss/k-gly.md)beschrieben.



| Feld          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dhpubkey       | Eine [**dhpubkey**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) -Struktur. Der **Magic** -Member sollte auf 0x31484400 festgelegt werden. Dieser Hexadezimalwert ist die [*ASCII*](../secgloss/a-gly.md) -Codierung von "DH1".                                                                                                                                                                                                                                                                                                                                                                 |
| publickeystruc | Eine [**publickeystruc**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) -Struktur.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Y              | Eine **Byte** Sequenz. Der Y-Wert (G ^ X) mod P befindet sich direkt hinter der [**dhpubkey**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) -Struktur und sollte immer die Länge (in Byte) des bitlen-Felds von **dhpubkey** (Bit-Länge von P) dividiert durch acht sein. Wenn die Länge der Daten, die sich aus der Berechnung von (G ^ X) mod P ergeben, mindestens ein Byte kürzer als P ist, das durch acht geteilt wird, müssen die Daten mit den erforderlichen Bytes (von NULL Wert) aufgefüllt werden, damit die Daten die gewünschte Länge haben ([*Little-Endian-*](../secgloss/l-gly.md) Format). |



 

## <a name="private-key-blobs"></a>Blobschlüssel für private Schlüssel

Geben Sie Diffie-Hellman [*privaten Schlüsselblobs*](../secgloss/p-gly.md) **privatekeyblob** ein, die zum Speichern der öffentlichen/privaten Informationen eines Diffie-Hellman Schlüssels verwendet werden. Diese Schlüssel werden als Bytefolge im folgenden Format exportiert und importiert.

``` syntax
PUBLICKEYSTRUC  publickeystruc; 
DHPUBKEY        dhpubkey;
BYTE            prime[dhpubkey.bitlen/8];
BYTE            generator[dhpubkey.bitlen/8];
BYTE            secret[dhpubkey.bitlen/8];
```

In der folgenden Tabelle werden die einzelnen Komponenten des Schlüssel-BLOBs beschrieben.



| Feld          | BESCHREIBUNG                                                                                                                                                                                                  |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dhpubkey       | Eine [**dhpubkey**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) -Struktur. Der **Magic** -Member muss auf 0x32484400 festgelegt werden. Dieser Hexadezimalwert ist die [*ASCII*](../secgloss/a-gly.md) -Codierung von "DH2". |
| Generator      | Eine **Byte** Sequenz. Der Generator, G.                                                                                                                                                                       |
| publickeystruc | Eine [**publickeystruc**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) -Struktur.                                                                                                                                                        |
| wichtigsten          | Eine **Byte** Sequenz. Der primmodulus (P). Diese Daten müssen immer das signifikanteste Bit aufweisen, das auf eins festgelegt ist.                                                                      |
| secret         | Eine **Byte** Sequenz. Der geheime Exponent, X.                                                                                                                                                                 |



 

> [!Note]  
> Der Generator und der geheime Schlüssel müssen immer dieselbe Länge haben (in Bytes). Wenn ein Byte oder kürzer als das andere ist, muss es mit der erforderlichen Anzahl von 0 (null) Byte aufgefüllt werden, damit die Werte identisch sind. Der Generator und der geheime Schlüssel sind im [*Little-Endian-*](../secgloss/l-gly.md) Format.

 

 

 
