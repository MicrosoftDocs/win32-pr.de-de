---
description: Diffie-Hellman Version 3 werden BLOBs mit öffentlichem Schlüssel (Typ PUBLICKEYBLOB) verwendet, um Informationen zu einem öffentlichen DH-Schlüssel zu exportieren und zu importieren.
ms.assetid: ba29a71a-7509-49c7-93d2-f0a699532706
title: 'Diffie-Hellman Version 3: BLOBs mit öffentlichem Schlüssel'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21515e370fba1c63ab3d852a88ad45b974683a3ca5ba3c3ad258733593fb6e5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767417"
---
# <a name="diffie-hellman-version-3-public-key-blobs"></a>Diffie-Hellman Version 3: BLOBs mit öffentlichem Schlüssel

Diffie-Hellman Version 3 [*werden BLOBs*](../secgloss/p-gly.md) mit öffentlichem Schlüssel (Typ PUBLICKEYBLOB) verwendet, um Informationen zu einem öffentlichen DH-Schlüssel zu exportieren und zu importieren. Sie haben das folgende Format:


```C++
BLOBHEADER blobheader; 
                 // As explained under "Data Structures"
DHPUBKEY_VER3 dhpubkeyver3;
BYTE p[dhpubkeyver3.bitlenP/8]; 
                 // Where P is the prime modulus
BYTE q[dhpubkeyver3.bitlenQ/8]; 
                 // Where Q is a large factor of P-1
BYTE g[dhpubkeyver3.bitlenP/8]; 
                 // Where G is the generator parameter
BYTE j[dhpubkeyver3.bitlenJ/8]; 
                 // Where J is (P-1)/Q
BYTE y[dhpubkeyver3.bitlenP/8]; 
                 // Where Y is (G^X) mod P
```



Dieses BLOB-Format wird exportiert, wenn das CRYPT \_ BLOB \_ VER3-Flag mit [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)verwendet wird. Da sich die Version im BLOB befindet, muss bei Verwendung dieses [*BLOB*](../secgloss/b-gly.md) mit [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey)kein Flag angegeben werden.

Darüber hinaus wird dieses BLOB-Format mit der [**CryptSetKeyParam-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) verwendet, wenn der *dwParam-Wert* KP \_ PUB \_ PARAMS verwendet wird, um Schlüsselparameter für einen DH-Schlüssel festzulegen. Dies geschieht, wenn das CRYPT \_ PREGEN-Flag zum Generieren des Schlüssels verwendet wurde. Bei Verwendung in dieser Situation wird der y-Wert ignoriert und sollte daher nicht in das BLOB aufgenommen werden.

In der folgenden Tabelle werden die einzelnen Komponenten des Schlüsselblobs beschrieben.



| Feld        | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| blobheader   | Eine [**BLOBHEADER-Struktur.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) Der **bType-Member** muss über den Wert PUBLICKEYBLOB verfügen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| dhpubkeyver3 | Eine [**DHPUBKEY \_ VER3-Struktur.**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) Der **Magic-Member** sollte auf 0x33484400 für öffentliche Schlüssel festgelegt werden. Beachten Sie, dass der Hexadezimalwert nur eine [*ASCII-Codierung*](../secgloss/a-gly.md) von "DH3" ist.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| P            | Der P-Wert befindet sich direkt hinter der [**DHPUBKEY \_ VER3-Struktur**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) und sollte immer die Länge des **DHPUBKEY VER3-BitlenP-Felds \_** **(Bitlänge** von P) dividiert durch acht [*(Little-Endian-Format)*](../secgloss/l-gly.md) in Bytes sein.                                                                                                                                                                                                                                                                                                                                                                                           |
| Q            | Der Q-Wert befindet sich direkt hinter dem P-Wert und sollte immer die Länge des [**DHPUBKEY VER3-BitlenQ-Felds \_**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) dividiert durch acht [*(Little-Endian-Format)*](../secgloss/l-gly.md) in Bytes sein.  Wenn der bitlenQ-Wert 0 ist, fehlt der Wert im BLOB.                                                                                                                                                                                                                                                                                                                                                                 |
| G            | Der G-Wert befindet sich direkt hinter dem Q-Wert und sollte immer die Länge des [**DHPUBKEY \_ VER3-BitlenP-Felds**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) **(Bitlänge** P) dividiert durch acht in Bytes sein. Wenn die Länge der Daten ein oder mehrere Bytes kürzer ist als P dividiert durch 8, müssen die Daten mit den erforderlichen Bytes (von 0 Wert) aufgefüllt werden, damit die Daten die gewünschte Länge haben [*(Little-Endian-Format).*](../secgloss/l-gly.md)                                                                                                                                                                                                                              |
| J            | Der J-Wert befindet sich direkt hinter dem G-Wert und sollte immer die Länge des [**DHPUBKEY VER3-BitlenJ-Felds \_**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) dividiert durch acht [*(Little-Endian-Format)*](../secgloss/l-gly.md) in Bytes sein.  Wenn der bitlenQ-Wert 0 ist, fehlt der Wert im BLOB.                                                                                                                                                                                                                                                                                                                                                                 |
| J            | Der Y-Wert (G^X) mod P befindet sich direkt hinter dem J-Wert und sollte immer die Länge des [**DHPUBKEY \_ VER3-BitlenP-Felds**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) **(Bitlänge** von P) dividiert durch acht sein. Wenn die Länge der Daten, die sich aus der Berechnung von (G^X) mod P ergeben, mindestens ein Bytes kürzer als P dividiert durch 8 ist, müssen die Daten mit den erforderlichen Bytes (von 0 Wert) aufgefüllt werden, damit die Daten die gewünschte Länge [*(Little-Endian-Format)*](../secgloss/l-gly.md) erhalten. Wenn diese Struktur mit [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) mit dem *dwParam-Wert* KP PUB PARAMS verwendet \_ \_ wird, ist dieser Wert nicht im BLOB enthalten. |



 

> [!Note]  
> BLOBs mit öffentlichem Schlüssel sind nicht verschlüsselt, enthalten jedoch öffentliche Schlüssel in Klartextform.

 

 

 
