---
description: Beschreibt das Format eines exportierten privaten DSS-Schlüssels der Version 3.
ms.assetid: 650532fd-919b-495a-9fb9-981790447d3d
title: DSS Version 3 Private Key BLOBs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6706f8cbfccb8c836efefb99a30086dc459619c8477b773a557f503ebbb2243
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767255"
---
# <a name="dss-version-3-private-key-blobs"></a>DSS Version 3 Private Key BLOBs

Wenn ein [*privater*](../secgloss/p-gly.md) [*DSS-Schlüssel*](../secgloss/d-gly.md) der Version 3 exportiert wird, weist er das folgende Format auf:


```C++
BLOBHEADER        blobheader; 
DSSPRIVKEY_VER3   dssprivkeyver3;
BYTE p[dssprivkeyver3.bitlenP/8]; 
                    // Where P is the prime modulus
BYTE q[dssprivkeyver3.bitlenQ/8]; 
                    // Where Q is a large factor of P-1
BYTE g[dssprivkeyver3.bitlenP/8]; 
                    // Where G is the generator parameter
BYTE j[dssprivkeyver3.bitlenJ/8]; 
                    // Where J is (P-1)/Q
BYTE y[dssprivkeyver3.bitlenP/8]; 
                    // Where Y is (G^X) mod P
BYTE x[dssprivkeyver3.bitlenX/8]; 
                    // Where X is the private exponent
```



Dieses [*BLOB-Format*](../secgloss/b-gly.md) wird exportiert, wenn das CRYPT \_ BLOB \_ VER3-Flag mit [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)verwendet wird. Da sich die Version im BLOB befindet, muss bei Verwendung dieses BLOB mit [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey)kein Flag angegeben werden.

In der folgenden Tabelle werden die einzelnen Komponenten des [*Schlüssel-BLOB*](../secgloss/k-gly.md)beschrieben.



| Feld          | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Blobheader     | Eine [**BLOBHEADER-Struktur.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) Der **bType-Member** muss über den Wert PUBLICKEYBLOB verfügen.                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Dssprivkeyver3 | Eine **DSSPRIVKEY \_ VER3-Struktur.** Der **Magic-Member** sollte für private Schlüssel auf "DSS4" (0x34535344) festgelegt werden. Beachten Sie, dass der Hexadezimalwert nur eine [*ASCII-Codierung*](../secgloss/a-gly.md) von "DSS4" ist.<br/>                                                                                                                                                                                                                                                                     |
| P              | Der P-Wert befindet sich direkt hinter der **DSSPRIVKEY \_ VER3-Struktur** und sollte immer die Länge des **DSSPRIVKEY \_ VER3-BitlenP-Felds** (Bitlänge von P) dividiert durch acht ([*Little-Endian-Format)*](../secgloss/l-gly.md) sein.                                                                                                                                                                                                                           |
| Q              | Der Q-Wert befindet sich direkt hinter dem P-Wert und sollte immer die Länge des **\_ BitlenQ-Felds DSSPRIVKEY VER3** dividiert durch acht [*(Little-Endian-Format)*](../secgloss/l-gly.md) in Bytes sein.                                                                                                                                                                                                                                                                     |
| G              | Der G-Wert befindet sich direkt hinter dem Q-Wert und sollte immer die Länge des **BitlenP-Felds DSSPRIVKEY \_ VER3 (Bitlänge** P) dividiert durch acht in Bytes sein. Wenn die Länge der Daten ein oder mehrere Bytes kürzer ist als P dividiert durch 8, müssen die Daten mit den erforderlichen Bytes (von 0 Wert) aufgefüllt werden, damit die Daten die gewünschte Länge haben [*(Little-Endian-Format).*](../secgloss/l-gly.md)                                                                 |
| J              | Der J-Wert befindet sich direkt hinter dem G-Wert und sollte immer die Länge des **\_ BitlenJ-Felds DSSPRIVKEY VER3** dividiert durch acht [*(Little-Endian-Format)*](../secgloss/l-gly.md) in Bytes sein. Wenn der bitlenJ-Wert 0 ist, fehlt der Wert im BLOB.                                                                                                                                                                                                   |
| J              | Der Y-Wert (G^X) mod P befindet sich direkt hinter dem J-Wert und sollte immer die Länge des **DSSPRIVKEY \_ VER3-BitlenP-Felds (Bitlänge** von P) geteilt durch acht in Bytes sein. Wenn die Länge der Daten, die sich aus der Berechnung von (G^X) mod P ergeben, mindestens ein Bytes kürzer als P dividiert durch 8 ist, müssen die Daten mit den erforderlichen Bytes (von 0 Wert) aufgefüllt werden, damit die Daten die gewünschte Länge [*(Little-Endian-Format)*](../secgloss/l-gly.md) erhalten. |
| X              | Der X-Wert ist eine zufällige große ganze Zahl, sodass der öffentliche Teil des DH-Schlüsselpaars, Y, gleich ist: Y = (G^X) mod P<br/>                                                                                                                                                                                                                                                                                                                                                                                               |



 

Beim Aufrufen von [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)kann der Entwickler auswählen, ob der Schlüssel verschlüsselt werden soll. Der Schlüssel wird verschlüsselt, wenn der *hExpKey-Parameter* ein gültiges Handle für einen Sitzungsschlüssel enthält. Alles außer dem [**BLOBHEADER-Teil**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) des BLOB wird verschlüsselt. Beachten Sie, dass der Verschlüsselungsalgorithmus und die Verschlüsselungsschlüsselparameter nicht zusammen mit dem BLOB des [*privaten Schlüssels*](../secgloss/p-gly.md)gespeichert werden. Die Anwendung muss diese Informationen verwalten und speichern. Wenn 0 (null) für *hExpKey* übergeben wird, wird der private Schlüssel ohne Verschlüsselung exportiert.

> [!IMPORTANT]
> Es ist gefährlich, private Schlüssel ohne Verschlüsselung zu exportieren, da sie dann anfällig für abfangende und nicht autorisierte Entitäten sind.

 

 

 
