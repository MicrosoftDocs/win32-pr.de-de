---
description: 'Weitere Informationen zu: JET_OBJECTINFO-Struktur'
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
ms.openlocfilehash: d61c42897da6d55dc96f2e59847fcf727424d60e
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986123"
---
# <a name="jet_objectinfo-structure"></a>JET_OBJECTINFO-Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_objectinfo-structure"></a>JET_OBJECTINFO-Struktur

Die **JET_OBJECTINFO-Struktur** enthält Informationen zu einem Objekt. Tabellen sind die einzigen Objekttypen, die derzeit unterstützt werden.

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

Die Größe der **JET_OBJECTINFO** -Struktur in Bytes.

**objtyp**

Enthält die [JET_OBJTYP](./jet-objtyp.md) der -Struktur. Derzeit werden nur Tabellen zurückgegeben (d. JET_objtypTable).

**dtCreate**

Veraltet. Darf nicht verwendet werden.

**dtUpdate**

Veraltet. Darf nicht verwendet werden.

**grbit**

Eine Gruppe von Bits, die die für diesen Aufruf verfügbaren Optionen enthalten, die null oder mehr der folgenden Elemente enthalten.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitTableInfoBookmark</p> | <p>Die Tabelle kann Lesezeichen enthalten.</p> | 
| <p>JET_bitTableInfoRollback</p> | <p>Für die Tabelle kann ein Rollback ausgeführt werden.</p> | 
| <p>JET_bitTableInfoUpdatable</p> | <p>Die Tabelle kann aktualisiert werden.</p> | 



**flags**

Ein Bitfeld, das null oder mehr der folgenden Flags enthält.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitObjectSystem</p> | <p>Die Tabelle ist eine Systemtabelle und nur zur internen Verwendung vorgesehen.</p> | 
| <p>JET_bitObjectTableDerived</p> | <p>Die von einer Vorlagentabelle geerbte DDL.</p> | 
| <p>JET_bitObjectTableFixedDDL</p> | <p>Die DDL für die Tabelle kann nicht geändert werden.</p> | 
| <p>JET_bitObjectTableNoFixedVarColumnsInDerivedTables</p> | <p>Wird in Verbindung mit JET_bitObjectTableTemplate verwendet, um feste oder variable Spalten in abgeleiteten Tabellen nicht zu lassen (damit feste oder variable Spalten der Vorlage in Zukunft hinzugefügt werden können).</p><p><strong>Windows XP:</strong> Dieser Wert wird in Windows XP eingeführt.</p> | 
| <p>JET_bitObjectTableTemplate</p> | <p>Die Tabelle ist eine Vorlagentabelle.</p> | 



**cRecord**

Die Anzahl der Datensätze in der Tabelle.

Dieser Wert wird nur abgerufen, wenn **JET_OBJECTINFO** an [JetGetObjectInfo](./jetgetobjectinfo-function.md)übergeben wurde.

**cPage**

Die Anzahl der Seiten, die von der Tabelle verwendet werden.

Dieser Wert wird nur abgerufen, wenn **JET_OBJECTINFO** an [JetGetObjectInfo](./jetgetobjectinfo-function.md)übergeben wurde.

### <a name="remarks"></a>Bemerkungen

Eine **JET_OBJECTINFO-Struktur** wird durch einen Aufruf von [JetGetObjectInfo](./jetgetobjectinfo-function.md) oder [JetGetTableInfo](./jetgettableinfo-function.md)aufgefüllt. Wenn der API-Aufruf nicht erfolgreich ist, ist der Inhalt der -Struktur nicht definiert.

Falls zutreffend, enthalten die Tabellenstatistiken die Anzahl der Datensätze und die Anzahl der Seiten, die sich im gruppierten Index befinden (d. amp;n.b. der Index, der die Datensatzdaten enthält). Auf die Indexstatistiken wird mit [jetGetIndexInfo](./jetgetindexinfo-function.md) oder [JetGetTableIndexInfo](./jetgettableindexinfo-function.md)separat anhand des Namens zugegriffen.

### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 



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
