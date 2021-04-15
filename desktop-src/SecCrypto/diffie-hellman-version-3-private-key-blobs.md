---
description: Beschreibt das Format eines exportierten Diffie-Hellman privaten Schlüsselblobs der Version 3.
ms.assetid: c759e6e1-f7af-4cd6-a67e-ff0da1e91eb1
title: Diffie-Hellman, Version 3, blobblobschlüssel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb35a6db0cfd75d34ba30d26be816a64c1b04205
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484595"
---
# <a name="diffie-hellman-version-3-private-key-blobs"></a>Diffie-Hellman, Version 3, blobblobschlüssel

Wenn ein BLOB für das [*private Schlüssel*](../secgloss/p-gly.md) Diffie-Hellman Version 3 exportiert wird, weist es das folgende Format auf:


```C++
BLOBHEADER        blobheader;
DHPRIVKEY_VER3   dhprivkeyver3;
BYTE p[dhprivkeyver3.bitlenP/8]; 
            // Where P is the prime modulus
BYTE q[dhprivkeyver3.bitlenQ/8]; 
            // Where Q is a large factor of P-1
BYTE g[dhprivkeyver3.bitlenP/8]; 
            // Where G is the generator parameter
BYTE j[dhprivkeyver3.bitlenJ/8]; 
            // Where J is (P-1)/Q
BYTE y[dhprivkeyver3.bitlenP/8]; 
            // Where Y is (G^X) mod P
BYTE x[dhprivkeyver3.bitlenX/8]; 
            // Where X is the private exponent
```



Dieses [*BLOB*](../secgloss/b-gly.md) -Format wird exportiert, wenn das Crypt \_ BLOB \_ VER3-Flag mit [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)verwendet wird. Da sich die Version im BLOB befindet, ist es nicht erforderlich, ein Flag anzugeben, wenn dieses BLOB mit " [**cryptimportkey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey)" verwendet wird.

In der folgenden Tabelle werden die einzelnen Komponenten des [*Schlüssel-BLOBs*](../secgloss/k-gly.md)beschrieben.



| Feld         | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| blobheader    | Eine [**blobheader**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) -Struktur.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| dhprivkeyver3 | Eine [**dhprivkey \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) -Struktur. Der **Magic** -Member sollte für private Schlüssel auf 0x34484400 festgelegt werden. Beachten Sie, dass der Hexadezimalwert nur eine [*ASCII*](../secgloss/a-gly.md) -Codierung von "DH4" ist.                                                                                                                                                                                                                                                                                            |
| P             | Der P-Wert befindet sich direkt hinter der [**dhprivkey \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) -Struktur und sollte immer die Länge in Bytes des Felds **dhprivkey \_ VER3** **bitlenp (Bitlänge** von P) dividiert durch acht ([*Little-Endian-*](../secgloss/l-gly.md) Format) sein.                                                                                                                                                                                                                            |
| Q             | Der Q-Wert befindet sich direkt hinter dem P-Wert und sollte immer die Länge in Bytes des Felds [**dhprivkey \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) **bitlenq** dividiert durch acht ([*Little-Endian-*](../secgloss/l-gly.md) Format) sein. Wenn der bitlenq-Wert 0 ist, ist der Wert im BLOB nicht vorhanden.                                                                                                                                                                                                  |
| G             | Der G-Wert befindet sich direkt hinter dem Q-Wert und sollte immer die Länge in Bytes des Felds [**dhprivkey \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) **bitlenp (Bitlänge** von P) dividiert durch acht sein. Wenn die Länge der Daten mindestens ein Byte kürzer als P dividiert durch 8 ist, müssen die Daten mit den erforderlichen Bytes (von null) aufgefüllt werden, damit die Daten die gewünschte Länge haben ([*Little-Endian-*](../secgloss/l-gly.md) Format).                                                                 |
| J             | Der J-Wert befindet sich direkt hinter dem G-Wert und sollte immer die Länge in Bytes des Felds [**dhprivkey \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) **bitlenj** dividiert durch acht ([*Little-Endian-*](../secgloss/l-gly.md) Format) sein. Wenn der bitlenj-Wert 0 ist, ist der Wert im BLOB nicht vorhanden.                                                                                                                                                                                                  |
| J             | Der Y-Wert (G ^ X) mod P befindet sich direkt hinter dem J-Wert und sollte immer die Länge in Bytes des Felds [**dhprivkey \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) **bitlenp (Bitlänge** von P) dividiert durch acht aufweisen. Wenn die Länge der Daten, die sich aus der Berechnung von (G ^ X) mod P ergeben, mindestens ein Byte kürzer als P ist, das durch 8 geteilt wird, müssen die Daten mit den erforderlichen Bytes (von null) aufgefüllt werden, damit die Daten die gewünschte Länge haben ([*Little-Endian-*](../secgloss/l-gly.md) Format). |
| X             | Der X-Wert ist eine zufällige große Ganzzahl, sodass der öffentliche Teil des DH-Schlüssel Paars Y, gleich: y = (G ^ X) mod P ist.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

Wenn Sie [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)aufrufen, kann der Entwickler auswählen, ob der Schlüssel verschlüsselt werden soll. Der Schlüssel wird verschlüsselt, wenn der *hexpkey* -Parameter ein gültiges Handle für einen Sitzungsschlüssel enthält. Alles außer dem [**blobheader**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) -Teil des BLOBs wird verschlüsselt. Beachten Sie, dass der Verschlüsselungsalgorithmus und die Verschlüsselungsschlüssel Parameter nicht zusammen mit dem [*BLOB für den privaten Schlüssel*](../secgloss/p-gly.md)gespeichert werden. Diese Informationen müssen von der Anwendung verwaltet und gespeichert werden. Wenn 0 (null) für *hexpkey* übermittelt wird, wird der private Schlüssel ohne Verschlüsselung exportiert.

> [!Note]  
> Es ist gefährlich, private Schlüssel ohne Verschlüsselung zu exportieren, da Sie dann anfällig für das Abfangen und die Verwendung durch nicht autorisierte Entitäten sind.

 

 

 
