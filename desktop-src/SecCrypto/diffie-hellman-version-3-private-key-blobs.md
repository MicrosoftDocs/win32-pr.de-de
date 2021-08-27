---
description: Beschreibt das Format eines exportierten Diffie-Hellman Version 3 des blob-Schlüssels.
ms.assetid: c759e6e1-f7af-4cd6-a67e-ff0da1e91eb1
title: 'Diffie-Hellman Version 3: BLOBs für private Schlüssel'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1adeb61f7f64d7362e832ea395a125f9f25de9a5ac2ce82325645fd19745bb4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100830"
---
# <a name="diffie-hellman-version-3-private-key-blobs"></a>Diffie-Hellman Version 3: BLOBs für private Schlüssel

Wenn ein blob Diffie-Hellman Version [*3*](../secgloss/p-gly.md) des privaten Schlüssels exportiert wird, hat es das folgende Format:


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



Dieses [*BLOB-Format*](../secgloss/b-gly.md) wird exportiert, wenn das CRYPT \_ BLOB \_ VER3-Flag mit [**CryptExportKey verwendet wird.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) Da sich die Version im BLOB befindet, ist es nicht notwendig, ein Flag anzugeben, wenn dieses BLOB mit [**CryptImportKey verwendet wird.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey)

In der folgenden Tabelle werden die einzelnen Komponenten des [*Schlüsselblobs beschrieben.*](../secgloss/k-gly.md)



| Feld         | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| blobheader    | Eine [**BLOBHEADER-Struktur.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| dhprivkeyver3 | Eine [**DHPRIVKEY \_ VER3-Struktur.**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) Der **Magic-Member** sollte auf 0x34484400 für private Schlüssel festgelegt werden. Beachten Sie, dass der Hexadezimalwert nur eine [*ASCII-Codierung*](../secgloss/a-gly.md) von "DH4" ist.                                                                                                                                                                                                                                                                                            |
| P             | Der P-Wert befindet sich direkt hinter der [**DHPRIVKEY \_ VER3-Struktur**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) und sollte immer die Länge in Bytes des **DHPRIVKEY VER3-BitlenP-Felds \_** (Bitlänge von P) sein, geteilt durch acht [*(Little-Endian-Format).*](../secgloss/l-gly.md)                                                                                                                                                                                                                             |
| Q             | Der Q-Wert befindet sich direkt hinter dem P-Wert und sollte immer die Länge in Bytes des [**DHPRIVKEY VER3-BitlenQ-Felds \_**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) dividiert durch acht [*(Little-Endian-Format)*](../secgloss/l-gly.md) sein.  Wenn der bitlenQ-Wert 0 ist, ist der Wert im BLOB nicht vorhanden.                                                                                                                                                                                                  |
| G             | Der G-Wert befindet sich direkt hinter dem Q-Wert und sollte immer die Länge in Bytes des [**DHPRIVKEY \_ VER3-BitlenP-Felds**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) (Bitlänge von P) dividiert durch acht sein.  Wenn die Länge der Daten mindestens ein Byte kürzer als P geteilt durch 8 ist, müssen die Daten mit den erforderlichen Bytes (null) aufschlossen werden, damit die Daten die gewünschte Länge haben [*(Little-Endian-Format).*](../secgloss/l-gly.md)                                                                 |
| J             | Der J-Wert befindet sich direkt hinter dem G-Wert und sollte immer die Länge in Bytes des [**DHPRIVKEY VER3-BitlenJ-Felds \_**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) sein, dividiert durch acht ([*Little-Endian-Format).*](../secgloss/l-gly.md)  Wenn der bitlenJ-Wert 0 ist, ist der Wert im BLOB nicht vorhanden.                                                                                                                                                                                                  |
| J             | Der Y-Wert (G^X) mod P befindet sich direkt hinter dem J-Wert und sollte immer die Länge in Bytes des [**DHPRIVKEY \_ VER3-BitlenP-Felds**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) (Bitlänge von P) dividiert durch acht sein.  Wenn die Länge der Daten, die sich aus der Berechnung von (G^X) mod P ergeben, mindestens ein Byte kürzer als P geteilt durch 8 ist, müssen die Daten mit den erforderlichen Bytes (null) aufschlossen werden, damit die Daten die gewünschte Länge haben [*(Little-Endian-Format).*](../secgloss/l-gly.md) |
| X             | Der X-Wert ist eine zufällige große ganze Zahl, bei der der öffentliche Teil des DH-Schlüsselpaars Y gleich ist: Y = (G^X) mod P<br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

Beim Aufrufen [**von CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)kann der Entwickler auswählen, ob der Schlüssel verschlüsselt werden soll. Der Schlüssel wird verschlüsselt, wenn *der hExpKey-Parameter* ein gültiges Handle für einen Sitzungsschlüssel enthält. Alles bis auf [**den BLOBHEADER-Teil**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) des BLOB wird verschlüsselt. Beachten Sie, dass der Verschlüsselungsalgorithmus und die Verschlüsselungsschlüsselparameter nicht zusammen mit dem [*BLOB des privaten Schlüssels gespeichert werden.*](../secgloss/p-gly.md) Die Anwendung muss diese Informationen verwalten und speichern. Wenn 0 (null) für *hExpKey übergeben* wird, wird der private Schlüssel ohne Verschlüsselung exportiert.

> [!Note]  
> Es ist gefährlich, private Schlüssel ohne Verschlüsselung zu exportieren, da sie dann anfällig für Abfangen und Verwenden durch nicht autorisierte Entitäten sind.

 

 

 
