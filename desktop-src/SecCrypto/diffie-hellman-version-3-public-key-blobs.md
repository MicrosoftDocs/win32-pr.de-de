---
description: Diffie-Hellman, Version 3, werden öffentliche Schlüssel-BLOBs (Type PublicKeyBlob) zum Exportieren und Importieren von Informationen über einen öffentlichen DH-Schlüssel verwendet.
ms.assetid: ba29a71a-7509-49c7-93d2-f0a699532706
title: Blobschlüssel für öffentliche Schlüssel Diffie-Hellman Version 3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df7228e4b4a786dc0eb25d1ba199b5c20923dd8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347355"
---
# <a name="diffie-hellman-version-3-public-key-blobs"></a>Blobschlüssel für öffentliche Schlüssel Diffie-Hellman Version 3

Diffie-Hellman, Version 3, werden [*öffentliche Schlüssel-BLOBs*](../secgloss/p-gly.md) (Type PublicKeyBlob) zum Exportieren und Importieren von Informationen über einen öffentlichen DH-Schlüssel verwendet. Sie haben das folgende Format:


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



Dieses BLOB-Format wird exportiert, wenn das Crypt \_ BLOB \_ VER3-Flag mit [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)verwendet wird. Da sich die Version im BLOB befindet, ist es nicht erforderlich, ein Flag anzugeben, wenn dieses [*BLOB*](../secgloss/b-gly.md) mit " [**cryptimportkey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey)" verwendet wird.

Außerdem wird dieses BLOB-Format mit der Funktion " [**cryptsetkeyparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) " verwendet, wenn der *dwparam* -Wert "KP \_ pub \_ params" zum Festlegen von Schlüsselparametern für einen DH-Schlüssel verwendet wird. Dies geschieht, wenn das Crypt \_ pregen-Flag verwendet wurde, um den Schlüssel zu generieren. Bei Verwendung in dieser Situation wird der y-Wert ignoriert und sollte daher nicht in das BLOB eingeschlossen werden.

In der folgenden Tabelle werden die einzelnen Komponenten des Schlüssel-BLOBs beschrieben.



| Feld        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| blobheader   | Eine [**blobheader**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) -Struktur. Der **bType** -Member muss den Wert PublicKeyBlob aufweisen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| dhpubkeyver3 | Eine [**dhpubkey \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) -Struktur. Der **Magic** -Member sollte für öffentliche Schlüssel auf 0x33484400 festgelegt werden. Beachten Sie, dass der Hexadezimalwert nur eine [*ASCII*](../secgloss/a-gly.md) -Codierung von "DH3" ist.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| P            | Der P-Wert befindet sich direkt hinter der [**dhpubkey \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) -Struktur und sollte immer die Länge (in Byte) des Felds **dhpubkey \_ VER3** **bitlenp (Bitlänge** von P) dividiert durch acht ([*Little-Endian-*](../secgloss/l-gly.md) Format) sein.                                                                                                                                                                                                                                                                                                                                                                                           |
| Q            | Der Q-Wert befindet sich direkt hinter dem P-Wert und sollte immer die Länge in Bytes des Felds [**dhpubkey \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) **bitlenq** dividiert durch acht ([*Little-Endian-*](../secgloss/l-gly.md) Format) sein. Wenn der bitlenq-Wert 0 ist, ist der Wert im BLOB nicht vorhanden.                                                                                                                                                                                                                                                                                                                                                                 |
| G            | Der G-Wert befindet sich direkt hinter dem Q-Wert und sollte immer die Länge (in Byte) des Felds " [**dhpubkey \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) **bitlenp" (Bitlänge** von P) dividiert durch acht sein. Wenn die Länge der Daten mindestens ein Byte kürzer als P dividiert durch 8 ist, müssen die Daten mit den erforderlichen Bytes (von null) aufgefüllt werden, damit die Daten die gewünschte Länge haben ([*Little-Endian-*](../secgloss/l-gly.md) Format).                                                                                                                                                                                                                              |
| J            | Der J-Wert befindet sich direkt hinter dem Wert G und sollte immer die Länge in Bytes des Felds [**dhpubkey \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) **bitlenj** dividiert durch acht ([*Little-Endian-*](../secgloss/l-gly.md) Format) sein. Wenn der bitlenq-Wert 0 ist, ist der Wert im BLOB nicht vorhanden.                                                                                                                                                                                                                                                                                                                                                                 |
| J            | Der Y-Wert (G ^ X) mod P befindet sich direkt hinter dem J-Wert und sollte immer die Länge in Bytes des Felds [**dhpubkey \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) **bitlenp (Bitlänge** von P) dividiert durch acht sein. Wenn die Länge der Daten, die sich aus der Berechnung von (G ^ X) mod P ergeben, mindestens ein Byte kürzer als P ist, das durch 8 geteilt wird, müssen die Daten mit den erforderlichen Bytes (von null) aufgefüllt werden, damit die Daten die gewünschte Länge haben ([*Little-Endian-*](../secgloss/l-gly.md) Format). Wenn diese Struktur mit [**cryptsetkeyparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) mit dem *dwparam* -Wert KP \_ pub \_ params verwendet wird, ist dieser Wert nicht im BLOB enthalten. |



 

> [!Note]  
> BLOBs für öffentliche Schlüssel werden nicht verschlüsselt, enthalten aber öffentliche Schlüssel in Klartext.

 

 

 
