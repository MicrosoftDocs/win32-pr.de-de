---
description: Beschreibt das Format eines exportierten privaten Schlüssels der DSS, Version 3.
ms.assetid: 650532fd-919b-495a-9fb9-981790447d3d
title: DSS, Version 3, blobblobdaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a6434e411ba3268901176a5c9739ceecfa79689
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215997"
---
# <a name="dss-version-3-private-key-blobs"></a>DSS, Version 3, blobblobdaten

Wenn ein privater [*DSS*](../secgloss/d-gly.md) - [*Schlüssel*](../secgloss/p-gly.md) der Version 3 exportiert wird, befindet er sich in einem Format wie folgt:


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



Dieses [*BLOB*](../secgloss/b-gly.md) -Format wird exportiert, wenn das Crypt \_ BLOB \_ VER3-Flag mit [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)verwendet wird. Da sich die Version im BLOB befindet, ist es nicht erforderlich, ein Flag anzugeben, wenn dieses BLOB mit " [**cryptimportkey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey)" verwendet wird.

In der folgenden Tabelle werden die einzelnen Komponenten des [*Schlüssel-BLOBs*](../secgloss/k-gly.md)beschrieben.



| Feld          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Blobheader     | Eine [**blobheader**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) -Struktur. Der **bType** -Member muss den Wert PublicKeyBlob aufweisen.                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Dssprivkeyver3 | Eine **dssprivkey \_ VER3** -Struktur. Der **Magic** -Member sollte für private Schlüssel auf "DSS4" (0x34535344) festgelegt werden. Beachten Sie, dass der Hexadezimalwert nur eine [*ASCII*](../secgloss/a-gly.md) -Codierung von "DSS4" ist.<br/>                                                                                                                                                                                                                                                                     |
| P              | Der P-Wert befindet sich direkt nach der **dssprivkey \_ VER3** -Struktur und sollte immer die Länge (in Byte) des Felds **dssprivkey \_ VER3 bitlenp (Bitlänge** von P) dividiert durch acht ([*Little-Endian-*](../secgloss/l-gly.md) Format) sein.                                                                                                                                                                                                                           |
| Q              | Der Q-Wert befindet sich direkt hinter dem P-Wert und sollte immer die Länge (in Byte) des **dssprivkey \_ VER3 bitlenq** -Felds dividiert durch acht ([*Little-Endian-*](../secgloss/l-gly.md) Format) sein.                                                                                                                                                                                                                                                                     |
| G              | Der G-Wert befindet sich direkt hinter dem Q-Wert und sollte immer die Länge (in Byte) des Felds **dssprivkey \_ VER3 bitlenp (Bitlänge** von P) dividiert durch acht sein. Wenn die Länge der Daten mindestens ein Byte kürzer als P dividiert durch 8 ist, müssen die Daten mit den erforderlichen Bytes (von null) aufgefüllt werden, damit die Daten die gewünschte Länge haben ([*Little-Endian-*](../secgloss/l-gly.md) Format).                                                                 |
| J              | Der J-Wert befindet sich direkt hinter dem G-Wert und sollte immer die Länge (in Byte) des **dssprivkey \_ VER3 bitlenj** -Felds dividiert durch acht ([*Little-Endian-*](../secgloss/l-gly.md) Format) sein. Wenn der bitlenj-Wert 0 (null) ist, ist der Wert im BLOB nicht vorhanden.                                                                                                                                                                                                   |
| J              | Der Y-Wert (G ^ X) mod P befindet sich direkt hinter dem J-Wert und sollte immer die Länge (in Byte) des **dssprivkey \_ VER3 bitlenp** -Felds (Bitlänge von P) dividiert durch acht sein. Wenn die Länge der Daten, die sich aus der Berechnung von (G ^ X) mod P ergeben, mindestens ein Byte kürzer als P ist, das durch 8 geteilt wird, müssen die Daten mit den erforderlichen Bytes (von null) aufgefüllt werden, damit die Daten die gewünschte Länge haben ([*Little-Endian-*](../secgloss/l-gly.md) Format). |
| X              | Der X-Wert ist eine zufällige große Ganzzahl, sodass der öffentliche Teil des DH-Schlüssel Paars Y, gleich: y = (G ^ X) mod P ist.<br/>                                                                                                                                                                                                                                                                                                                                                                                               |



 

Wenn Sie [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)aufrufen, kann der Entwickler auswählen, ob der Schlüssel verschlüsselt werden soll. Der Schlüssel wird verschlüsselt, wenn der *hexpkey* -Parameter ein gültiges Handle für einen Sitzungsschlüssel enthält. Alles außer dem [**blobheader**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) -Teil des BLOBs wird verschlüsselt. Beachten Sie, dass der Verschlüsselungsalgorithmus und die Verschlüsselungsschlüssel Parameter nicht zusammen mit dem [*BLOB für den privaten Schlüssel*](../secgloss/p-gly.md)gespeichert werden. Diese Informationen müssen von der Anwendung verwaltet und gespeichert werden. Wenn 0 (null) für *hexpkey* übermittelt wird, wird der private Schlüssel ohne Verschlüsselung exportiert.

> [!IMPORTANT]
> Es ist gefährlich, private Schlüssel ohne Verschlüsselung zu exportieren, da Sie dann anfällig für das Abfangen und die Verwendung durch nicht autorisierte Entitäten sind.

 

 

 
