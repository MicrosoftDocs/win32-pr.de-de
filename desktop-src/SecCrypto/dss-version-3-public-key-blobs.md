---
description: DSS Version 3 Public Key BLOBs vom Typ PUBLICKEYBLOB werden verwendet, um Informationen zu einem öffentlichen DH-Schlüssel zu exportieren und zu importieren.
ms.assetid: 9aac1d61-8b61-4f0f-b037-afe4a60302de
title: BLOBs für öffentliche Schlüssel der DSS-Version 3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5cc4894000f284dfd5d1b1dd9e9a7353e4eee0b09a42edc63de76e8eaa93184
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875260"
---
# <a name="dss-version-3-public-key-blobs"></a>BLOBs für öffentliche Schlüssel der DSS-Version 3

DSS Version 3 [*Public Key BLOBs*](../secgloss/p-gly.md) vom Typ PUBLICKEYBLOB werden verwendet, um Informationen zu einem öffentlichen DH-Schlüssel zu exportieren und zu importieren. Sie haben das folgende Format:


```C++
BLOBHEADER blobheader; 
        // As explained under "Data Structures"
DSSPUBKEY_VER3 dsspubkeyver3;
BYTE p[dsspubkeyver3.bitlenP/8]; 
       // Where P is the prime modulus
BYTE q[dsspubkeyver3.bitlenQ/8]; 
       // Where Q is a large factor of P-1
BYTE g[dsspubkeyver3.bitlenP/8]; 
       // Where G is the generator parameter
BYTE j[dsspubkeyver3.bitlenJ/8]; 
       // Where J is (P-1)/Q
BYTE y[dsspubkeyver3.bitlenP/8]; 
       // Where Y is (G^X) mod P
```



Dieses [*BLOB-Format*](../secgloss/b-gly.md) wird exportiert, wenn das CRYPT \_ BLOB \_ VER3-Flag mit [**CryptExportKey verwendet wird.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) Da sich die Version im BLOB befindet, ist es nicht notwendig, ein Flag anzugeben, wenn dieses BLOB mit [**CryptImportKey verwendet wird.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey)

Darüber hinaus wird dieses BLOB-Format mit der [**CryptSetKeyParam-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) verwendet, wenn der *dwParam-Wert* KP PUB PARAMS zum Festlegen von Schlüsselparametern für einen \_ \_ DSS-Schlüssel verwendet wird. Dies erfolgt, wenn das Flag CRYPT \_ PREGEN zum Generieren des Schlüssels verwendet wurde. Bei Verwendung in diesem Fall wird der y-Wert ignoriert und sollte daher nicht in das BLOB aufgenommen werden.

In der folgenden Tabelle werden die einzelnen Komponenten des Schlüsselblobs beschrieben.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Feld</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Blobheader</td>
<td>Eine <a href="/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc"><strong>BLOBHEADER-Struktur.</strong></a> Der <strong>bType-Member</strong> muss den Wert PUBLICKEYBLOB haben.</td>
</tr>
<tr class="even">
<td>Dsspubkeyver3</td>
<td>Eine <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a> Struktur. Der <strong>Magic-Member</strong> sollte für öffentliche Schlüssel auf &quot; DSS3 &quot; (0x33535344) festgelegt werden. Beachten Sie, dass der Hexadezimalwert nur eine <a href="/windows/desktop/SecGloss/a-gly"><em>ASCII-Codierung</em></a> von &quot; DSS3 ist.&quot;<br/></td>
</tr>
<tr class="odd">
<td>P</td>
<td>Der P-Wert befindet sich direkt hinter der <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3-Struktur</strong></a> und sollte immer die Länge des DSSPUBKEY_VER3 <strong>bitlenP-Felds</strong> (Bitlänge von P) sein, geteilt durch acht<a href="/windows/desktop/SecGloss/l-gly"><em>(Little-Endian-Format).</em></a></td>
</tr>
<tr class="even">
<td>Q</td>
<td>Der Q-Wert befindet sich direkt hinter dem P-Wert und sollte immer die Länge in Bytes des <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenQ-Members</strong> dividiert durch acht<a href="/windows/desktop/SecGloss/l-gly"><em>(Little-Endian-Format)</em></a> sein.</td>
</tr>
<tr class="odd">
<td>G</td>
<td>Der G-Wert befindet sich direkt hinter dem Q-Wert und <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong></strong></a>sollte immer die Länge des<strong>DSSPUBKEY_VER3-BitlenP-Members</strong> (Bitlänge von P) in Byte dividiert durch acht sein. Wenn die Länge der Daten mindestens ein Byte kürzer als P geteilt durch 8 ist, müssen die Daten mit den erforderlichen Bytes (null) aufschlossen werden, damit die Daten die gewünschte Länge haben<a href="/windows/desktop/SecGloss/l-gly"><em>(Little-Endian-Format).</em></a></td>
</tr>
<tr class="even">
<td>J</td>
<td>Der J-Wert befindet sich direkt hinter dem G-Wert und sollte immer die Länge in Bytes des DSSPUBKEY_VER3<strong>bitlenJ-Members</strong> dividiert durch acht<a href="/windows/desktop/SecGloss/l-gly"><em>(Little-Endian-Format)</em></a> sein. <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong></strong></a> Wenn der bitlenQ-Wert 0 ist, ist der Wert im BLOB nicht vorhanden.</td>
</tr>
<tr class="odd">
<td>J</td>
<td>Der <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>Y-Wert</strong></a>(G^X) mod P befindet sich direkt hinter dem J-Wert und sollte immer die Länge des<strong>DSSPUBKEY_VER3-BitlenP-Members</strong> (Bitlänge von P) dividiert durch acht sein. Wenn die Länge der Daten, die sich aus der Berechnung von (G^X) mod P ergeben, mindestens ein Byte kürzer als P geteilt durch 8 ist, müssen die Daten mit den erforderlichen Bytes (null) aufschlossen werden, damit die Daten die gewünschte Länge haben<a href="/windows/desktop/SecGloss/l-gly"><em>(Little-Endian-Format).</em></a>
<blockquote>
[!Note]<br />
Wenn diese Struktur mit <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam"><strong>CryptSetKeyParam</strong></a> mit dem <em>dwParam-Wert</em> KP_PUB_PARAMS wird, ist dieser Wert nicht im BLOB enthalten.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> BLOBs mit öffentlichen Schlüsseln werden nicht verschlüsselt, enthalten aber öffentliche Schlüssel in Klartextform.

 

 

 
