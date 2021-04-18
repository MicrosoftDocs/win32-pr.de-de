---
description: 'Weitere Informationen finden Sie hier: JET_COLUMNLIST Struktur'
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
ms.openlocfilehash: 9bce36c818dd35408d95c770540ff4865bdf639b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354542"
---
# <a name="jet_columnlist-structure"></a>JET_COLUMNLIST-Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_columnlist-structure"></a>JET_COLUMNLIST-Struktur

Die **JET_COLUMNLIST** -Struktur enthält die Informationen, die erforderlich sind, um die temporäre Tabelle zu durchlaufen, die von den Funktionen [jetgetcolumninfo](./jetgetcolumninfo-function.md) und [jetgettablecolumninfo](./jetgettablecolumninfo-function.md) erstellt wird. Jede Zeile in der temporären Tabelle beschreibt eine Spalte in der Tabelle, die im API-Befehl angegeben ist. Diese Struktur wird nur mit [jetgetcolumninfo](./jetgetcolumninfo-function.md) und [jetgettablecolumninfo](./jetgettablecolumninfo-function.md)verwendet.

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

Die Größe der Struktur in Bytes. Der API-Aufruf aktualisiert dieses Feld, sodass der Aufrufer sicherstellen muss, dass dieser Wert sizeof (JET_COLUMNLIST) entspricht.

**TableID**

Der Tabellen Bezeichner der temporären Tabelle, die erstellt wurde. Es liegt in der Verantwortung des Aufrufers, die Tabelle zu schließen.

**crecord**

Die Anzahl der Datensätze in der temporären Tabelle, die durch den API-Befehl erstellt wurde.

**columnidpresentationorder**

Der Spalten Bezeichner der Präsentations Reihenfolge.

Die Präsentations Reihenfolge wird verwendet, um die Zeilen der temporären Tabelle zu sortieren. Die Präsentations Reihenfolge ist ein festes [JET_coltypLong](./jet-coltyp.md). Wenn die angegebene Informationsebene keine Compact-Ebene war, wird Sie auch als JET_bitColumnTTKey gekennzeichnet.

**columnidcolumnname**

Der Spalten Bezeichner des Spaltennamens.

Wenn die angegebene Informationsebene nicht kompakt ist, wird Sie auch als JET_bitColumnTTKey gekennzeichnet.

**columnidcolumnid**

Der Spalten Bezeichner des Spalten Bezeichners.

Der Spalten Bezeichner ist ein fester [JET_coltypLong](./jet-coltyp.md).

**columnidcolyp**

Der Spalten Bezeichner des Spalten Typs.

Der Spaltentyp ist ein fester [JET_coltypLong](./jet-coltyp.md).

**columnidcountry**

Der Spalten Bezeichner des Ländercodes.

Der Ländercode ist ein fester [JET_coltypShort](./jet-coltyp.md).

**columnidlangid**

Der Spalten Bezeichner des sprach Bezeichners.

Der sprach Bezeichner ist ein fester [JET_coltypShort](./jet-coltyp.md).

**columnidcp**

Der Spalten Bezeichner der Codepage.

Die Codepage ist ein festes [JET_coltypShort](./jet-coltyp.md).

**columnidcollate**

Der Spalten Bezeichner der Sortierungs Sequenz.

Die Sortierreihenfolge ist ein festes [JET_coltypShort](./jet-coltyp.md).

**columnidcbmax**

Der Spalten Bezeichner des **cbmax** -Felds.

**Cbmax** ist ein fester [JET_coltypLong](./jet-coltyp.md).

**columnidgrbit**

Der Spalten Bezeichner der *grbits* der Spalte. Das *grbit* -Feld ist ein festes [JET_coltypLong](./jet-coltyp.md). Weitere Informationen zu diesen Bits finden Sie unter [JET_COLUMNDEF](./jet-columndef-structure.md).

Für **columnidgrbit** sind folgende Werte möglich:

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

**columniddefault**

Der Spalten Bezeichner des Standardwerts der Spalte.

Der Standardwert ist eine [JET_coltypLongBinary](./jet-coltyp.md).

**columnidbasetablename**

Der Spalten Bezeichner des Namens der Tabelle, aus der die Tabelle abgeleitet wurde.

Der Tabellenname ist eine [JET_coltypText](./jet-coltyp.md).

**columnidbasecolumschlag Name**

Der Spalten Bezeichner des Namens der Spalte, von der die Spalte abgeleitet wurde.

Der Spaltenname ist eine [JET_coltypText](./jet-coltyp.md).

**columnidDefinitionName**

Der Spalten Bezeichner des Namens der Spaltendefinition.

Der Spalten Definitions Name ist eine [JET_coltypText](./jet-coltyp.md).

### <a name="remarks"></a>Bemerkungen

Standardmäßig wird die Reihenfolge der Zeilen in der temporären Tabelle nach dem Namen der Spalte sortiert. Sie kann auch nach Spalten Bezeichner sortiert werden. Weitere Informationen zum Sortieren nach Spalten Bezeichner finden Sie unter [jetgetcolumninfo](./jetgetcolumninfo-function.md) und [jetgettablecolumninfo](./jetgettablecolumninfo-function.md).

Beim Aufrufen von [jetgetcolumninfo](./jetgetcolumninfo-function.md) oder [jetgettablecolumninfo](./jetgettablecolumninfo-function.md) kann eine kompakte Form von Ergebnissen angegeben werden. Wenn Spalten von einer Vorlagen Tabelle geerbt wurden, werden Sie in den Compact-Ergebnissen nicht gespeichert.

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

[JET_COLUMNDEF](./jet-columndef-structure.md)

[JET_COLUMNID](./jet-columnid.md)

[JET_ERR](./jet-err.md)

[JET_GRBIT](./jet-grbit.md)

[JET_SESID](./jet-sesid.md)

[JET_TABLEID](./jet-tableid.md)

[Jetgetcolumninfo](./jetgetcolumninfo-function.md)

[Jetgettablecolumninfo](./jetgettablecolumninfo-function.md)
