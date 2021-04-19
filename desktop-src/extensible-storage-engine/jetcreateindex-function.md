---
description: 'Weitere Informationen zu: jetkreateinzudex-Funktion'
title: JetCreateIndex-Funktion
TOCTitle: JetCreateIndex Function
ms:assetid: d164e74a-7719-4587-9059-8fb18b365133
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294099(v=EXCHG.10)
ms:contentKeyID: 32765714
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateIndexA
- JetCreateIndex
- JetCreateIndexW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c0208a5f0adac4ff5128b506123f3b68589cd0d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106367984"
---
# <a name="jetcreateindex-function"></a>JetCreateIndex-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetcreateindex-function"></a>JetCreateIndex-Funktion

Mithilfe der **jetkreateindex** -Funktion können Sie einen Index von Daten in einer ESE-Datenbank (Extensible Storage Engine) erstellen, die Sie verwenden können, um bestimmte Daten schnell zu suchen.

```cpp
    JET_ERR JET_API JetCreateIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szIndexName,
      __in          JET_GRBIT grbit,
      __in          const tchar* szKey,
      __in          unsigned long cbKey,
      __in          unsigned long lDensity
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Der Daten Bank Sitzungs Kontext, der für einen bestimmten API-Befehl verwendet werden soll.

*TableID*

Die Tabelle, für die ein Index erstellt wird.

*szindexname*

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des zu erstellenden Indexes angibt.

Der Indexname muss den folgenden Richtlinien entsprechen:

  - Es muss weniger Zeichen als JET_cbNameMost enthalten, ohne das abschließende Null Zeichen.

  - Er darf nur Zeichen aus den folgenden Kategorien enthalten: 0 bis 9, a bis z, a bis z und alle Interpunktions Zeichen mit Ausnahme von " \! ". (Ausrufezeichen), "," (Komma), " \[ " (öffnende eckige Klammer) und " \] " (schließende Klammer) – d. h. die ASCII-Zeichen 0x20, 0x22 bis 0x2D, 0x2F bis 0x5A, 0x5c und 0x5d bis 0x7F.

  - Er darf nicht mit einem Leerzeichen beginnen.

  - Sie muss mindestens ein Zeichen enthalten, das kein Leerzeichen ist.

*grbit*

Eine Gruppe von Bits, die die Optionen enthält, die für einen bestimmten-aufrufbedarf verwendet werden sollen. Dieser Parameter kann NULL oder mehr der Optionen enthalten, die in der [JET_INDEXCREATE](./jet-indexcreate-structure.md) Struktur gefunden werden.

*szkey*

Ein Zeiger auf eine Double-NULL-terminierte Zeichenfolge von NULL-getrennten Token.

Weitere Informationen zu diesem Parameter finden Sie in der [JET_INDEXCREATE](./jet-indexcreate-structure.md) -Struktur.

*cbKey*

Die Länge des *szkey* -Parameters in Bytes, einschließlich der beiden abschließenden NULL Zeichen.

*ldensity*

Die prozentuale Dichte des ersten Index B +-Baums.

Weitere Informationen zu diesem Parameter finden Sie in der [JET_INDEXCREATE](./jet-indexcreate-structure.md) -Struktur.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) -Datentyp mit einem der in der folgenden Tabelle aufgelisteten Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Rückgabecode</p></th>
<th><p>Bedeutung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>Der Vorgang wurde erfolgreich abgeschlossen.</p></td>
</tr>
</tbody>
</table>


Eine Liste mit zusätzlichen Fehlern, die von der **jetkreateinzudex** -Funktion zurückgegeben werden können, finden Sie unter [JetCreateIndex2](./jetcreateindex2-function.md).

#### <a name="remarks"></a>Bemerkungen

Das Aufrufen der **jetcreateindex** -Funktion ist identisch mit dem Aufruf der [JetCreateIndex2](./jetcreateindex2-function.md) -Funktion mit einer [JET_INDEXCREATE](./jet-indexcreate-structure.md) -Struktur, die die gleichen Einstellungen wie die Parameter von **jetcreateindex** und einen *cindexcreate* -Parameter gleich 1 enthält. Für die Felder der [JET_INDEXCREATE](./jet-indexcreate-structure.md) Struktur, die keine entsprechenden Parameter in **jetkreatandex** aufweisen, wird der Wert 0 angenommen.

Beachten Sie, dass **jetkreatandex** durch [JetCreateIndex2](./jetcreateindex2-function.md)abgelöst wurde.

#### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Client</p></td>
<td><p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p>Server</p></td>
<td><p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p>Header</p></td>
<td><p>Wird in "ESENT. h" deklariert.</p></td>
</tr>
<tr class="even">
<td><p>Bibliothek</p></td>
<td><p>Verwendet ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p>DLL</p></td>
<td><p>Erfordert ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p>Unicode</p></td>
<td><p>Ist als <strong>jetkreateingedexw</strong> (Unicode) und <strong>jetkreateingedexa</strong> (ANSI) implementiert.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JetCreateIndex2](./jetcreateindex2-function.md)  
[Jetkreatetablecolumnindex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)
