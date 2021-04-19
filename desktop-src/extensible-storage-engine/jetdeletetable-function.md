---
description: 'Weitere Informationen finden Sie unter: jetdeletetable-Funktion'
title: Jetdeletetable-Funktion
TOCTitle: JetDeleteTable Function
ms:assetid: e8a4131f-a69b-41f3-94c6-a1607fc23c1f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294128(v=EXCHG.10)
ms:contentKeyID: 32765742
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteTable
- JetDeleteTableA
- JetDeleteTableW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c432f8e09ad706b6632e4e5ca49a89a263a84dbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369892"
---
# <a name="jetdeletetable-function"></a>Jetdeletetable-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetdeletetable-function"></a>Jetdeletetable-Funktion

Die **jetdeletetable** -Funktion löscht eine Tabelle in einer ESE-Datenbank.

```cpp
    JET_ERR JET_API JetDeleteTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Der für den API-Befehl zu verwendende Daten Bank Sitzungs Kontext.

*DBID*

Der für den API-Befehl zu verwendende Daten Bank Bezeichner.

*sztablename*

Der Name der zu löschenden Tabelle.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Rückgabecode</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>Der Vorgang wurde erfolgreich abgeschlossen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTableInUse</p></td>
<td><p>Es wurde versucht, eine Tabelle zu löschen, während eine andere Sitzung über eine offene Tabellen-ID (<a href="gg269182(v=exchg.10).md">JET_TABLEID</a>) mit <a href="gg294118(v=exchg.10).md">jetopentable</a> oder <a href="gg269193(v=exchg.10).md">jetdupcursor</a>verfügt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCannotDeletetemporary Tabelle</p></td>
<td><p>Es wurde versucht, eine temporäre Tabelle zu löschen. Eine temporäre Tabelle wird automatisch gelöscht, wenn Sie mit <a href="gg294087(v=exchg.10).md">jetclosetable</a>geschlossen wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotDeleteTemplateTable</p></td>
<td><p>Es wurde versucht, eine Vorlagen Tabelle zu löschen, d. h. eine Tabelle, aus der DDL vererbt werden kann.</p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a>Anforderungen

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
<tr class="even">
<td><p><strong>Bibliothek</strong></p></td>
<td><p>Verwenden Sie ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Erfordert ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementiert als <strong>jetdeletetablew</strong> (Unicode) und <strong>jetdeletetablea</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_DBID](./jet-dbid.md)  
[JET_SESID](./jet-sesid.md)  
[Jetclosetable](./jetclosetable-function.md)
