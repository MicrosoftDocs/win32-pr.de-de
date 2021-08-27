---
description: 'Weitere Informationen zu: JET_COLUMNLIST-Struktur'
title: JET_COLUMNLIST-Struktur
TOCTitle: JET_COLUMNLIST Structure
ms:assetid: 3899676f-c96e-4f15-9089-4faea6808bc2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269228(v=EXCHG.10)
ms:contentKeyID: 32765530
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
ms.openlocfilehash: c61f3492a9f92700fc51b7e51e13f8c3c3febc69
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985263"
---
# <a name="jet_columnlist-structure"></a>JET_COLUMNLIST-Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_columnlist-structure"></a>JET_COLUMNLIST-Struktur

Die **JET_COLUMNLIST-Struktur** enthält die Informationen, die zum Durchlaufen der temporären Tabelle erforderlich sind, die von den [JetGetColumnInfo-](./jetgetcolumninfo-function.md) und [JetGetTableColumnInfo-Funktionen](./jetgettablecolumninfo-function.md) erstellt wird. Jede Zeile in der temporären Tabelle beschreibt eine Spalte in der Im API-Aufruf angegebenen Tabelle. Diese Struktur wird nur mit [JetGetColumnInfo](./jetgetcolumninfo-function.md) und [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)verwendet.

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      unsigned long cRecord;
      JET_COLUMNID columnidPresentationOrder;
      JET_COLUMNID columnidcolumnname;
      JET_COLUMNID columnidcolumnid;
      JET_COLUMNID columnidcoltyp;
      JET_COLUMNID columnidCountry;
      JET_COLUMNID columnidLangid;
      JET_COLUMNID columnidCp;
      JET_COLUMNID columnidCollate;
      JET_COLUMNID columnidcbMax;
      JET_COLUMNID columnidgrbit;
      JET_COLUMNID columnidDefault;
      JET_COLUMNID columnidBaseTableName;
      JET_COLUMNID columnidBaseColumnName;
      JET_COLUMNID columnidDefinitionName;
    } JET_COLUMNLIST;
```

### <a name="members"></a>Member

**cbStruct**

Die Größe der -Struktur in Bytes. Der API-Aufruf aktualisiert dieses Feld, sodass der Aufrufer sicherstellen sollte, dass dieser Wert mit sizeof( JET_COLUMNLIST ) übereinstimmt.

**tableid**

Der Tabellenbezeichner der temporären Tabelle, die erstellt wurde. Es liegt in der Verantwortung des Aufrufers, die Tabelle zu schließen.

**cRecord**

Die Anzahl der Datensätze in der temporären Tabelle, die durch den API-Aufruf erstellt wurde.

**columnidPresentationOrder**

Der Spaltenbezeichner der Präsentationsreihenfolge.

Die Präsentationsreihenfolge wird verwendet, um die Zeilen der temporären Tabelle zu sortieren. Die Präsentationsreihenfolge ist eine feste [JET_coltypLong](./jet-coltyp.md). Wenn es sich bei der angegebenen Informationsebene nicht um eine kompakte Ebene handelt, wird sie auch als JET_bitColumnTTKey markiert.

**columnidcolumnname**

Der Spaltenbezeichner des Spaltennamens.

Wenn die angegebene Informationsebene nicht kompakt war, wird sie auch als JET_bitColumnTTKey markiert.

**columnidcolumnid**

Der Spaltenbezeichner des Spaltenbezeichners.

Der Spaltenbezeichner ist ein fester [JET_coltypLong](./jet-coltyp.md).

**columnidcoltyp**

Der Spaltenbezeichner des Spaltentyps.

Der Spaltentyp ist ein fester [JET_coltypLong](./jet-coltyp.md).

**columnidCountry**

Der Spaltenbezeichner des Ländercodes.

Der Ländercode ist ein fester [JET_coltypShort](./jet-coltyp.md).

**columnidLangid**

Der Spaltenbezeichner des Sprachbezeichners.

Der Sprachbezeichner ist ein fester [JET_coltypShort](./jet-coltyp.md).

**columnidCp**

Der Spaltenbezeichner der Codepage.

Die Codepage ist eine feste [JET_coltypShort](./jet-coltyp.md).

**columnidCollate**

Der Spaltenbezeichner der Sortierungssequenz.

Die Sortierungssequenz ist eine feste [JET_coltypShort](./jet-coltyp.md).

**columnidcbMax**

Der Spaltenbezeichner des **cbMax-Felds.**

**CbMax** ist ein fester [JET_coltypLong](./jet-coltyp.md).

**columnidgrbit**

Der Spaltenbezeichner der *Grbits* der Spalte. Das *Grbitfeld* ist ein fester [JET_coltypLong](./jet-coltyp.md). Weitere Informationen zu diesen Bits finden Sie unter [JET_COLUMNDEF](./jet-columndef-structure.md).

Folgende Werte sind für **columnidgrbit** möglich:

JET_bitColumnTagged

JET_bitColumnFixed

JET_bitColumnUpdatable

JET_bitColumnNotNULL

JET_bitColumnAutoincrement

JET_bitColumnVersion

JET_bitColumnMultiValued

JET_bitColumnEscrowUpdate

JET_bitColumnFinalize

JET_bitColumnDeleteOnZero

JET_bitColumnUserDefinedDefault

**columnidDefault**

Der Spaltenbezeichner des Standardwerts der Spalte.

Der Standardwert ist ein [JET_coltypLongBinary](./jet-coltyp.md).

**columnidBaseTableName**

Der Spaltenbezeichner des Namens der Tabelle, von der die Tabelle abgeleitet wurde.

Der Tabellenname ist ein [JET_coltypText](./jet-coltyp.md).

**columnidBaseColumnName**

Der Spaltenbezeichner des Namens der Spalte, von der die Spalte abgeleitet wurde.

Der Spaltenname ist ein [JET_coltypText](./jet-coltyp.md).

**columnidDefinitionName**

Der Spaltenbezeichner des Namens der Spaltendefinition.

Der Spaltendefinitionsname ist ein [JET_coltypText](./jet-coltyp.md).

### <a name="remarks"></a>Bemerkungen

Standardmäßig wird die Reihenfolge der Zeilen in der temporären Tabelle nach dem Namen der Spalte sortiert. Sie kann auch nach Spaltenbezeichner sortiert werden. Weitere Informationen zum Sortieren nach Spaltenbezeichner finden Sie unter [JetGetColumnInfo](./jetgetcolumninfo-function.md) und [JetGetTableColumnInfo.](./jetgettablecolumninfo-function.md)

Der Aufruf von [JetGetColumnInfo](./jetgetcolumninfo-function.md) oder [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) kann eine kompakte Form von Ergebnissen angeben. Wenn Spalten von einer Vorlagentabelle geerbt wurden, werden sie in den kompakten Ergebnissen nicht gespeichert.

### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JET_COLTYP](./jet-coltyp.md)

[JET_COLUMNDEF](./jet-columndef-structure.md)

[JET_COLUMNID](./jet-columnid.md)

[JET_ERR](./jet-err.md)

[JET_GRBIT](./jet-grbit.md)

[JET_SESID](./jet-sesid.md)

[JET_TABLEID](./jet-tableid.md)

[JetGetColumnInfo](./jetgetcolumninfo-function.md)

[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)
