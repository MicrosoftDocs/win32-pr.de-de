---
description: 'Weitere Informationen finden Sie unter: JET_OBJECTINFO Struktur'
title: JET_OBJECTINFO-Struktur
TOCTitle: JET_OBJECTINFO Structure
ms:assetid: 9d348ab3-d453-4316-9233-681f165e8ef1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269353(v=EXCHG.10)
ms:contentKeyID: 32765640
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
ms.openlocfilehash: af21d3f885a979ac81fef502a64281ea5445046983f652033566c689991a70ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119720310"
---
# <a name="jet_objectinfo-structure"></a>JET_OBJECTINFO-Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_objectinfo-structure"></a>JET_OBJECTINFO-Struktur

Die **JET_OBJECTINFO-Struktur** enthält Informationen zu einem -Objekt. Tabellen sind die einzigen Objekttypen, die derzeit unterstützt werden.

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_OBJTYP objtyp;
      JET_DATESERIAL dtCreate;
      JET_DATESERIAL dtUpdate;
      JET_GRBIT grbit;
      unsigned long flags;
      unsigned long cRecord;
      unsigned long cPage;
    } JET_OBJECTINFO;
```

### <a name="members"></a>Member

**cbStruct**

Die Größe der -Struktur in **Bytes JET_OBJECTINFO** Struktur.

**objtyp**

Enthält die [JET_OBJTYP](./jet-objtyp.md) der -Struktur. Derzeit werden nur Tabellen zurückgegeben (d. h. JET_objtypTable).

**dtCreate**

Veraltet. Darf nicht verwendet werden.

**dtUpdate**

Veraltet. Darf nicht verwendet werden.

**grbit**

Eine Gruppe von Bits, die die für diesen Aufruf verfügbaren Optionen enthalten, die null oder mehr der folgenden Elemente enthalten.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Wert</p></th>
<th><p>Bedeutung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitTableInfoBookmark</p></td>
<td><p>Die Tabelle kann Lesezeichen haben.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTableInfoRollback</p></td>
<td><p>Für die Tabelle kann ein Rollback verwendet werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTableInfoUpdatable</p></td>
<td><p>Die Tabelle kann aktualisiert werden.</p></td>
</tr>
</tbody>
</table>


**flags**

Ein Bitfeld, das null oder mehr der folgenden Flags enthält.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Wert</p></th>
<th><p>Bedeutung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitObjectSystem</p></td>
<td><p>Die Tabelle ist eine Systemtabelle und nur zur internen Verwendung.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitObjectTableDerived</p></td>
<td><p>Die Tabelle hat DDL von einer Vorlagentabelle geerbt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitObjectTableFixedDDL</p></td>
<td><p>Die DDL für die Tabelle kann nicht geändert werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitObjectTableNoFixedVarColumnsInDerivedTables</p></td>
<td><p>Wird in Verbindung mit JET_bitObjectTableTemplate verwendet, um feste oder variable Spalten in abgeleiteten Tabellen zu vermeiden (sodass der Vorlage in Zukunft feste oder variable Spalten hinzugefügt werden können).</p>
<p><strong>Windows XP:</strong> Dieser Wert wird in xp Windows eingeführt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitObjectTableTemplate</p></td>
<td><p>Die Tabelle ist eine Vorlagentabelle.</p></td>
</tr>
</tbody>
</table>


**cRecord**

Die Anzahl der Datensätze in der Tabelle.

Dieser Wert wird nur abgerufen, wenn **JET_OBJECTINFO** An [JetGetObjectInfo übergeben wurde.](./jetgetobjectinfo-function.md)

**cPage**

Die Anzahl der Seiten, die von der Tabelle verwendet werden.

Dieser Wert wird nur abgerufen, wenn **JET_OBJECTINFO** An [JetGetObjectInfo übergeben wurde.](./jetgetobjectinfo-function.md)

### <a name="remarks"></a>Hinweise

Eine **JET_OBJECTINFO-Struktur** wird durch einen Aufruf von [JetGetObjectInfo](./jetgetobjectinfo-function.md) oder [JetGetTableInfo aufgefüllt.](./jetgettableinfo-function.md) Wenn der API-Aufruf nicht erfolgreich ist, ist der Inhalt der Struktur nicht definiert.

Falls zutreffend, enthalten die Tabellenstatistiken die Anzahl der Datensätze und die Anzahl der Seiten im gruppierten Index (d. h. den Index, der die Datensatzdaten enthält). Auf die Indexstatistiken wird separat über den Namen zugegriffen, indem [JetGetIndexInfo](./jetgetindexinfo-function.md) oder [JetGetTableIndexInfo verwendet wird.](./jetgettableindexinfo-function.md)

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
<td><p>Wird in Esent.h deklariert.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_OBJTYP](./jet-objtyp.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetIndexInfo](./jetgetindexinfo-function.md)  
[JetGetObjectInfo](./jetgetobjectinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetGetTableInfo](./jetgettableinfo-function.md)
