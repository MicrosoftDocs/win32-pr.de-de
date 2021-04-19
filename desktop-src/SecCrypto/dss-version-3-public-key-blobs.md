---
description: DSS, Version 3, BLOBs mit öffentlichem Schlüssel vom Typ "PublicKeyBlob" werden zum Exportieren und Importieren von Informationen über einen öffentlichen DH-Schlüssel verwendet.
ms.assetid: 9aac1d61-8b61-4f0f-b037-afe4a60302de
title: DSS, Version 3, blobschlüssel für öffentliche Schlüssel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 593ac69025ff046a9a8d014286c2464788c07b02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356728"
---
# <a name="dss-version-3-public-key-blobs"></a>DSS, Version 3, blobschlüssel für öffentliche Schlüssel

DSS, Version 3, [*BLOBs mit öffentlichem Schlüssel*](../secgloss/p-gly.md) vom Typ "PublicKeyBlob" werden zum Exportieren und Importieren von Informationen über einen öffentlichen DH-Schlüssel verwendet. Sie haben das folgende Format:


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



Dieses [*BLOB*](../secgloss/b-gly.md) -Format wird exportiert, wenn das Crypt \_ BLOB \_ VER3-Flag mit [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)verwendet wird. Da sich die Version im BLOB befindet, ist es nicht erforderlich, ein Flag anzugeben, wenn dieses BLOB mit " [**cryptimportkey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey)" verwendet wird.

Außerdem wird dieses BLOB-Format mit der Funktion " [**cryptsetkeyparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) " verwendet, wenn der *dwparam* -Wert "KP \_ pub \_ params" zum Festlegen von Schlüsselparametern für einen DSS-Schlüssel verwendet wird. Dies geschieht, wenn das Crypt \_ pregen-Flag verwendet wurde, um den Schlüssel zu generieren. Bei Verwendung in dieser Situation wird der y-Wert ignoriert und sollte daher nicht in das BLOB eingeschlossen werden.

In der folgenden Tabelle werden die einzelnen Komponenten des Schlüssel-BLOBs beschrieben.



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
<td>Eine <a href="/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc"><strong>blobheader</strong></a> -Struktur. Der <strong>bType</strong> -Member muss den Wert PublicKeyBlob aufweisen.</td>
</tr>
<tr class="even">
<td>Dsspubkeyver3</td>
<td>Eine <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a> -Struktur. Der <strong>Magic</strong> -Member sollte &quot; &quot; für öffentliche Schlüssel auf DSS3 (0x33535344) festgelegt werden. Beachten Sie, dass der Hexadezimalwert nur eine <a href="/windows/desktop/SecGloss/a-gly"><em>ASCII</em></a> -Codierung von &quot; DSS3 ist.&quot;<br/></td>
</tr>
<tr class="odd">
<td>P</td>
<td>Der P-Wert befindet sich direkt hinter der <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a> Struktur und sollte immer die Länge (in Byte) des DSSPUBKEY_VER3 <strong>bitlenp</strong> -Felds (Bitlänge von P) dividiert durch acht (<a href="/windows/desktop/SecGloss/l-gly"><em>Little-Endian-</em></a> Format) sein.</td>
</tr>
<tr class="even">
<td>Q</td>
<td>Der Q-Wert befindet sich direkt hinter dem P-Wert und sollte immer die Länge des <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenq</strong> -Members in Bytes aufweisen, dividiert durch acht (<a href="/windows/desktop/SecGloss/l-gly"><em>Little-Endian-</em></a> Format).</td>
</tr>
<tr class="odd">
<td>G</td>
<td>Der G-Wert befindet sich direkt nach dem Q-Wert und sollte immer die Länge (in Byte) des <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenp</strong> -Members (Bitlänge von P) dividiert durch acht sein. Wenn die Länge der Daten mindestens ein Byte kürzer als P dividiert durch 8 ist, müssen die Daten mit den erforderlichen Bytes (von null) aufgefüllt werden, damit die Daten die gewünschte Länge haben (<a href="/windows/desktop/SecGloss/l-gly"><em>Little-Endian-</em></a> Format).</td>
</tr>
<tr class="even">
<td>J</td>
<td>Der J-Wert befindet sich direkt hinter dem G-Wert und sollte immer die Länge in Bytes des <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenj</strong> -Members dividiert durch acht (<a href="/windows/desktop/SecGloss/l-gly"><em>Little-Endian-</em></a> Format) sein. Wenn der bitlenq-Wert 0 ist, ist der Wert im BLOB nicht vorhanden.</td>
</tr>
<tr class="odd">
<td>J</td>
<td>Der Y-Wert (G ^ X) mod P befindet sich direkt hinter dem J-Wert und sollte immer die Länge (in Byte) des <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenp</strong> -Members (Bitlänge von P) dividiert durch acht sein. Wenn die Länge der Daten, die sich aus der Berechnung von (G ^ X) mod P ergeben, mindestens ein Byte kürzer als P ist, das durch 8 geteilt wird, müssen die Daten mit den erforderlichen Bytes (von null) aufgefüllt werden, damit die Daten die gewünschte Länge haben (<a href="/windows/desktop/SecGloss/l-gly"><em>Little-Endian-</em></a> Format).
<blockquote>
[!Note]<br />
Wenn diese Struktur mit " <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam"><strong>cryptsetkeyparam</strong></a> " mit dem <em>dwparam</em> -Wert KP_PUB_PARAMS verwendet wird, ist dieser Wert nicht im BLOB enthalten.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> BLOBs für öffentliche Schlüssel werden nicht verschlüsselt, enthalten aber öffentliche Schlüssel in Klartext.

 

 

 
