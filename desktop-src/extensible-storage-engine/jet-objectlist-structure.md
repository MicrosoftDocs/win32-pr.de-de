---
description: 'Weitere Informationen finden Sie hier: JET_OBJECTLIST Struktur'
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
ms.openlocfilehash: a7a66bb3b7f7dfbbfd1087d1fe0ce32c4144a8bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347518"
---
# <a name="jet_objectlist-structure"></a>JET_OBJECTLIST-Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_objectlist-structure"></a>JET_OBJECTLIST-Struktur

Die **JET_OBJECTLIST** -Struktur durchläuft eine temporäre Tabelle, die mit [jetgetobjectinfo](./jetgetobjectinfo-function.md)erstellt wurde. Jede Zeile in der temporären Tabelle beschreibt ein Objekt in der Datenbank.

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

Die Größe der-Struktur in Bytes. Der API-Aufruf aktualisiert dieses Feld, sodass der Aufrufer sicherstellen muss, dass dieser Wert sizeof (JET_INDEXLIST) entspricht.

**TableID**

Der Tabellen Bezeichner der temporären Tabelle, die erstellt wurde. Der Aufrufer muss Code enthalten, der die Tabelle schließt.

**crecord**

Die Anzahl der Datensätze in der temporären Tabelle, die erstellt wurde.

**columnidcontainername**

Der Spalten Bezeichner des Namens des Container Typs.

Die einzigen derzeit unterstützten Container sind Tabellen. Diese Spalte ist eine [JET_coltypText](./jet-coltyp.md).

**columnidobjectname**

Der Spalten Bezeichner des Namens des Objekts.

Diese Spalte ist eine [JET_coltypText](./jet-coltyp.md).

**columnidobjyp**

Der Spalten Bezeichner des Typs des Objekts. Die einzigen derzeit unterstützten Container sind Tabellen, sodass dieses Feld JET_objtypTable wird.

Diese Spalte ist eine [JET_coltypLong](./jet-coltyp.md).

**columniddtcreate**

Veraltet. Darf nicht verwendet werden.

**columniddtupdate**

Veraltet. Darf nicht verwendet werden.

**columnidgrbit**

Der Spalten Bezeichner der **grbits** , die auf das-Objekt anwendbar sind. Eine Liste der anwendbaren **grbits** finden Sie unter [JET_TABLECREATE](./jet-tablecreate-structure.md).

Diese Spalte ist eine [JET_coltypLong](./jet-coltyp.md).

**columnidflags**

Der Spalten Bezeichner der Flags, die auf das-Objekt anwendbar sind. Eine Liste der anwendbaren Flags finden Sie unter [JET_OBJECTINFO](./jet-objectinfo-structure.md).

Diese Spalte ist eine [JET_coltypLong](./jet-coltyp.md).

**columnidcrecord**

Der Spalten Bezeichner der Anzahl von Datensätzen, die in der Tabelle vorhanden sind, die in **columnidobjectname** benannt ist.

Diese Spalte ist eine [JET_coltypLong](./jet-coltyp.md).

**columnidcpage**

Der Spalten Bezeichner der Anzahl der Seiten, die vom-Objekt verwendet werden.

Diese Spalte ist eine [JET_coltypLong](./jet-coltyp.md).

### <a name="remarks"></a>Bemerkungen

Jede Zeile in der temporären Tabelle entspricht einem Objekt in der Datenbank.

Wenn die temporäre Tabelle mit dem *infolevel* -Parameter in der [jetgetobjectinfo](./jetgetobjectinfo-function.md) -Funktion auf JET_ObjInfoListNoStats festgelegt wird, enthalten die von **columnidcrecord** und **columnidcpage** identifizierten Spalten keine aussagekräftigen Informationen.

Derzeit werden nur Informationen zu Tabellen in der temporären Tabelle angezeigt.

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

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JET_TABLECREATE](./jet-tablecreate-structure.md)  
[Jetgetobjectinfo](./jetgetobjectinfo-function.md)
