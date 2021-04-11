---
description: 'Weitere Informationen finden Sie hier: JET_OBJECTINFO Struktur'
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
ms.openlocfilehash: cd1f8a876153b5b457cfb153cbf35fa2d388b0f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042659"
---
# <a name="jet_objectinfo-structure"></a>JET_OBJECTINFO-Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_objectinfo-structure"></a>JET_OBJECTINFO-Struktur

Die **JET_OBJECTINFO** -Struktur enthält Informationen zu einem-Objekt. Tabellen sind die einzigen Objekttypen, die derzeit unterstützt werden.

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

Die Größe der **JET_OBJECTINFO** Struktur in Bytes.

**objyp**

Enthält die [JET_OBJTYP](./jet-objtyp.md) der-Struktur. Zurzeit werden nur Tabellen zurückgegeben (d. h. JET_objtypTable).

**dtcreate**

Veraltet. Darf nicht verwendet werden.

**dtupdate**

Veraltet. Darf nicht verwendet werden.

**grbit**

Eine Gruppe von Bits, die die für diesen-Befehl verfügbaren Optionen enthalten, die NULL oder mehr der folgenden Elemente enthalten.

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
<td><p>Die Tabelle kann Lesezeichen enthalten.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTableInfoRollback</p></td>
<td><p>Für die Tabelle kann ein Rollback ausgeführt werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTableInfoUpdatable</p></td>
<td><p>Die Tabelle kann aktualisiert werden.</p></td>
</tr>
</tbody>
</table>


**flags**

Ein Bitfeld, das NULL oder mehr der folgenden Flags enthält.

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
<td><p>Die Tabelle ist eine System Tabelle und nur für die interne Verwendung vorgesehen.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitObjectTableDerived</p></td>
<td><p>Die Tabelle hat DDL aus einer Vorlagen Tabelle geerbt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitObjectTableFixedDDL</p></td>
<td><p>Die DDL für die Tabelle kann nicht geändert werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitObjectTableNoFixedVarColumnsInDerivedTables</p></td>
<td><p>Wird in Verbindung mit JET_bitObjectTableTemplate verwendet, um die festgelegten oder Variablen Spalten in abgeleiteten Tabellen nicht zuzulassen (sodass der Vorlage in Zukunft festgelegte oder Variablen Spalten hinzugefügt werden können).</p>
<p><strong>Windows XP:  </strong> Dieser Wert wird in Windows XP eingeführt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitObjectTableTemplate</p></td>
<td><p>Die Tabelle ist eine Vorlagen Tabelle.</p></td>
</tr>
</tbody>
</table>


**crecord**

Die Anzahl der Datensätze in der Tabelle.

Dieser Wert wird nur abgerufen, wenn **JET_OBJECTINFO** an [jetgetobjectinfo](./jetgetobjectinfo-function.md)übermittelt wurde.

**cpage**

Die Anzahl der Seiten, die von der Tabelle verwendet werden.

Dieser Wert wird nur abgerufen, wenn **JET_OBJECTINFO** an [jetgetobjectinfo](./jetgetobjectinfo-function.md)übermittelt wurde.

### <a name="remarks"></a>Bemerkungen

Eine **JET_OBJECTINFO** Struktur wird durch einen Aufrufen von [jetgetobjectinfo](./jetgetobjectinfo-function.md) oder [jetgettableinfo](./jetgettableinfo-function.md)aufgefüllt. Wenn der API-Befehl nicht erfolgreich ist, ist der Inhalt der Struktur nicht definiert.

Falls zutreffend, enthält die Tabellen Statistik die Anzahl der Datensätze und die Anzahl der Seiten im gruppierten Index (d. h. den Index, der die Daten des Datensatzes enthält). Der Zugriff auf die Index Statistiken erfolgt separat über den Namen, mithilfe von [jetgetindexinfo](./jetgetindexinfo-function.md) oder [jetgettableindexinfo](./jetgettableindexinfo-function.md).

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

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_OBJTYP](./jet-objtyp.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[Jetgetindexinfo](./jetgetindexinfo-function.md)  
[Jetgetobjectinfo](./jetgetobjectinfo-function.md)  
[Jetgettableindexinfo](./jetgettableindexinfo-function.md)  
[Jetgettableinfo](./jetgettableinfo-function.md)
