---
description: 'Weitere Informationen finden Sie hier: JET_SNT'
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
ms.openlocfilehash: 5d1d4fa75c8a41528e9868bc94fa638042d01cff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214389"
---
# <a name="jet_snt"></a>JET_SNT


_**Gilt für:** Windows | Windows Server_

## <a name="jet_snt"></a>JET_SNT

Die [JET_SNT]() Gruppe von Konstanten beschreibt die Punkte des Status eines Vorgangs, über die Informationen angefordert werden, die in einem Rückruf der [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) Rückruffunktion angefordert werden.

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
<td><p>Der Anfang eines Vorgangs.</p></td>
</tr>
<tr class="even">
<td><p>JET_sntRequirements<br />
7</p></td>
<td><p>Wird nicht unterstützt.</p>
<p><strong>Windows 2000-Server:</strong>  Der Vorgang wird gestartet. In diesem Fall sollte der letzte Parameter der Rückruffunktion ein gültiger Zeiger auf eine <a href="gg269328(v=exchg.10).md">JET_SNPROG</a> Struktur sein, die die Gesamtzahl der auszuführenden Einheiten angibt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_sntProgress<br />
0</p></td>
<td><p>Die Anzahl der abgeschlossenen Einheiten und die Anzahl der Einheiten, die noch ausgeführt werden müssen. Diese Informationen werden in den Elementen einer <a href="gg269328(v=exchg.10).md">JET_SNPROG</a> Struktur zurückgegeben.</p></td>
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
<td><p>Die Wiederherstellungs Steuerung eines Vorgangs.</p>
<div class="alert">

> [!NOTE]
> <P>Dieser Wert gilt nicht für Versionen des Windows-Betriebssystems, beginnend mit Windows 8.</P>


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
<td><p>In "ESENT. h" deklariert.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JET_SNP](./jet-snp.md)  
[JET_SNPROG](./jet-snprog-structure.md)
