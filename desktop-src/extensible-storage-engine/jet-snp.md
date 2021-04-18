---
description: 'Weitere Informationen finden Sie hier: JET_SNP'
title: JET_SNP
TOCTitle: JET_SNP
ms:assetid: 7f3d1cc5-7b27-454d-8dd1-584ab4b60ab0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269311(v=EXCHG.10)
ms:contentKeyID: 32765601
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
ms.openlocfilehash: 35ffb2d17c01c3d157fc7ed66a320529f844ff9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343639"
---
# <a name="jet_snp"></a>JET_SNP


_**Gilt für:** Windows | Windows Server_

## <a name="jet_snp"></a>JET_SNP

Die **JET_SNP** Gruppe von Konstanten beschreibt den Typ des Vorgangs, für den Statusinformationen abgerufen werden sollen. Diese Konstanten werden als der *SNP* -Parameter der [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) Rückruffunktion verwendet.

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
<td><p>JET_snpRepair<br />
2</p></td>
<td><p>Der Rückruf ist für einen Reparaturvorgang vorgesehen.</p></td>
</tr>
<tr class="even">
<td><p>JET_snpCompact<br />
4</p></td>
<td><p>Der Rückruf dient der Daten Bank Defragmentierung.</p></td>
</tr>
<tr class="odd">
<td><p>JET_snpRestore<br />
8</p></td>
<td><p>Der Rückruf ist für einen Wiederherstellungs Vorgang vorgesehen.</p></td>
</tr>
<tr class="even">
<td><p>JET_snpBackup<br />
9</p></td>
<td><p>Der Rückruf ist für einen Sicherungs Vorgang vorgesehen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_snpUpgrade<br />
10</p></td>
<td><p>Wird nicht unterstützt.</p>
<p><strong>Windows 2000:</strong>  Der Rückruf ist für den Upgradevorgang des Daten Bank Formats vorgesehen.</p></td>
</tr>
<tr class="even">
<td><p>JET_snpScrub<br />
11</p></td>
<td><p>Der Rückruf ist für einen Daten Bank Nullen (das heißt, Scrubbing).</p>
<p><strong>Windows Server 2003-und Windows 2000-Server:</strong>  Nicht unterstützt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_snpUpgradeRecordFormat<br />
12</p></td>
<td><p>Der Rückruf dient zum Aktualisieren des Daten Satz Formats aller Datenbankseiten.</p>
<p><strong>Windows Server 2003-und Windows 2000-Server:</strong>  Nicht unterstützt.</p></td>
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
[JET_SNPROG](./jet-snprog-structure.md)  
[JET_SNT](./jet-snt.md)
