---
description: 'Weitere Informationen: Ungültige handle-Konstanten'
title: Ungültige handle-Konstanten
TOCTitle: Invalid Handle Constants
ms:assetid: 594d7804-725f-4f72-b5f0-56f099c1c17b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269256(v=EXCHG.10)
ms:contentKeyID: 32765558
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
ms.openlocfilehash: f5614b36acfca8b5be4c13849d459d25f984336a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050408"
---
# <a name="invalid-handle-constants"></a>Ungültige handle-Konstanten


_**Gilt für:** Windows | Windows Server_

## <a name="invalid-handle-constants"></a>Ungültige handle-Konstanten

Die folgenden Konstanten weisen auf ungültige Handles für verschiedene Aspekte von ESE hin.

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
<td><p>JET_instanceNil<br />
(~ (JET_INSTANCE) 0)</p></td>
<td><p>Ein ungültiges Handle für eine Daten Bank Instanz.<br />
<strong>Windows XP:</strong> Eingeführt in Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_sesidNil<br />
(~ (JET_SESID) 0)</p></td>
<td><p>Ein ungültiges Handle für eine Sitzungs-ID.</p></td>
</tr>
<tr class="odd">
<td><p>JET_tableidNil<br />
(~ (JET_TABLEID) 0)</p></td>
<td><p>Ein ungültiges Handle für eine Tabellen-ID.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitNil<br />
((JET_GRBIT) 0)</p></td>
<td><p>Ein ungültiges Handle für eine Gruppe von Bits.</p></td>
</tr>
<tr class="odd">
<td><p>JET_LSNil<br />
(~ (JET_LS) 0)</p></td>
<td><p>Ein ungültiges Handle für den lokalen Speicher.</p></td>
</tr>
<tr class="even">
<td><p>JET_dbidNil<br />
((JET_DBID) 0xFFFFFFFF)</p></td>
<td><p>Ein ungültiges Handle für die Datenbank-ID.</p></td>
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

