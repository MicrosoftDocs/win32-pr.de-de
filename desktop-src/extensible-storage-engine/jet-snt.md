---
description: 'Weitere Informationen finden Sie unter: JET_SNT'
title: JET_SNT
TOCTitle: JET_SNT
ms:assetid: 74ac5142-8102-4dd3-8f2a-786a7a2ac78f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269294(v=EXCHG.10)
ms:contentKeyID: 32765586
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ad04730c52bce38e462c2521dc7c34872bfcb69c3337ac6af18d09d865b9cfd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118252514"
---
# <a name="jet_snt"></a>JET_SNT


_**Gilt für:** Windows | Windows Server_

## <a name="jet_snt"></a>JET_SNT

Die [JET_SNT]() Gruppe von Konstanten beschreibt die Punkte des Fortschritts eines Vorgangs, zu dem Informationen in einem Aufruf der rückruffunktion JET_PFNSTATUS [werden.](./jet-pfnstatus-callback-function.md)

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Konstante/Wert</p></th>
<th><p>BESCHREIBUNG</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_sntBegin<br />
5</p></td>
<td><p>Der Anfang eines Vorgangs</p></td>
</tr>
<tr class="even">
<td><p>JET_sntRequirements<br />
7</p></td>
<td><p>Wird nicht unterstützt.</p>
<p><strong>Windows 2000 Server:</strong>  Der Vorgang wird gestartet. In diesem Fall sollte der letzte Parameter der Rückruffunktion ein <a href="gg269328(v=exchg.10).md"></a> gültiger Zeiger auf eine JET_SNPROG-Struktur sein, die die Gesamtzahl der auszuführenden Einheiten angibt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_sntProgress<br />
0</p></td>
<td><p>Die Anzahl der abgeschlossenen Einheiten und die Anzahl der noch zu erledigenden Einheiten. Diese Informationen werden in den Membern einer JET_SNPROG <a href="gg269328(v=exchg.10).md">zurückgegeben.</a></p></td>
</tr>
<tr class="even">
<td><p>JET_sntComplete<br />
6</p></td>
<td><p>Der Abschluss eines Vorgangs.</p></td>
</tr>
<tr class="odd">
<td><p>JET_sntFail<br />
3</p></td>
<td><p>Der Fehler eines Vorgangs.</p></td>
</tr>
<tr class="even">
<td><p>JET_sntRecoveryStep<br />
8</p></td>
<td><p>Die Wiederherstellungssteuerung eines Vorgangs.</p>
<div class="alert">

> [!NOTE]
> <P>Dieser Wert gilt nicht für Versionen des Windows Betriebssystems, beginnend mit Windows 8.</P>


</div></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>In Esent.h deklariert.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JET_SNP](./jet-snp.md)  
[JET_SNPROG](./jet-snprog-structure.md)
