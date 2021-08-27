---
description: 'Weitere Informationen zu: JET_OBJECTLIST-Struktur'
title: JET_OBJECTLIST-Struktur
TOCTitle: JET_OBJECTLIST Structure
ms:assetid: 95f12f2a-13da-48d4-a254-fc0cb718b17d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269348(v=EXCHG.10)
ms:contentKeyID: 32765635
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a2f035a15c0f0f2861c7c6698878e0782feb35ce
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476536"
---
# <a name="jet_objectlist-structure"></a>JET_OBJECTLIST-Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_objectlist-structure"></a>JET_OBJECTLIST-Struktur

Die **JET_OBJECTLIST-Struktur** durchläuft eine temporäre Tabelle, die mit [JetGetObjectInfo](./jetgetobjectinfo-function.md)erstellt wurde. Jede Zeile in der temporären Tabelle beschreibt ein Objekt in der Datenbank.

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      unsigned long cRecord;
      JET_COLUMNID columnidcontainername;
      JET_COLUMNID columnidobjectname;
      JET_COLUMNID columnidobjtyp;
      JET_COLUMNID columniddtCreate;
      JET_COLUMNID columniddtUpdate;
      JET_COLUMNID columnidgrbit;
      JET_COLUMNID columnidflags;
      JET_COLUMNID columnidcRecord;
      JET_COLUMNID columnidcPage;
    } JET_OBJECTLIST;
```

### <a name="members"></a>Member

**cbStruct**

Die Größe der -Struktur in Bytes. Der API-Aufruf aktualisiert dieses Feld, sodass der Aufrufer sicherstellen sollte, dass dieser Wert mit sizeof( JET_INDEXLIST ) übereinstimmt.

**tableid**

Der Tabellenbezeichner der temporären Tabelle, die erstellt wurde. Der Aufrufer muss Code enthalten, der die Tabelle schließt.

**cRecord**

Die Anzahl der Datensätze in der temporären Tabelle, die erstellt wurde.

**columnidcontainername**

Der Spaltenbezeichner des Namens des Typs des Containers.

Die einzigen Container, die derzeit unterstützt werden, sind Tabellen. Diese Spalte ist ein [JET_coltypText](./jet-coltyp.md).

**columnidobjectname**

Der Spaltenbezeichner des Namens des Objekts.

Diese Spalte ist ein [JET_coltypText](./jet-coltyp.md).

**columnidobjtyp**

Der Spaltenbezeichner des Objekttyps. Die einzigen Container, die derzeit unterstützt werden, sind Tabellen, sodass dieses Feld JET_objtypTable wird.

Diese Spalte ist eine [JET_coltypLong](./jet-coltyp.md).

**columniddtCreate**

Veraltet. Darf nicht verwendet werden.

**columniddtUpdate**

Veraltet. Darf nicht verwendet werden.

**columnidgrbit**

Der Spaltenbezeichner der **Grbits,** die auf das -Objekt anwendbar sind. Eine Liste der anwendbaren **Grbits** finden Sie unter [JET_TABLECREATE](./jet-tablecreate-structure.md).

Diese Spalte ist eine [JET_coltypLong](./jet-coltyp.md).

**columnidflags**

Der Spaltenbezeichner der Flags, die auf das -Objekt anwendbar sind. Eine Liste der anwendbaren Flags finden Sie unter [JET_OBJECTINFO](./jet-objectinfo-structure.md).

Diese Spalte ist eine [JET_coltypLong](./jet-coltyp.md).

**columnidcRecord**

Der Spaltenbezeichner der Anzahl von Datensätzen, die in der Tabelle mit dem Namen **columnidobjectname** vorhanden sind.

Diese Spalte ist eine [JET_coltypLong](./jet-coltyp.md).

**columnidcPage**

Der Spaltenbezeichner der Vom -Objekt verwendeten Seitenanzahl.

Diese Spalte ist eine [JET_coltypLong](./jet-coltyp.md).

### <a name="remarks"></a>Hinweise

Jede Zeile in der temporären Tabelle entspricht einem Objekt in der Datenbank.

Wenn die temporäre Tabelle mit dem *InfoLevel-Parameter* in der [JetGetObjectInfo-Funktion](./jetgetobjectinfo-function.md) erstellt wird, die auf JET_ObjInfoListNoStats festgelegt ist, enthalten die durch **columnidcRecord** und **columnidcPage** identifizierten Spalten keine aussagekräftigen Informationen.

Derzeit befinden sich nur Informationen zu Tabellen in der temporären Tabelle.

### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JET_TABLECREATE](./jet-tablecreate-structure.md)  
[JetGetObjectInfo](./jetgetobjectinfo-function.md)
