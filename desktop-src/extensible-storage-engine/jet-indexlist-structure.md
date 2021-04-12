---
description: 'Weitere Informationen finden Sie hier: JET_INDEXLIST Struktur'
title: JET_INDEXLIST-Struktur
TOCTitle: JET_INDEXLIST Structure
ms:assetid: 0c092b48-e583-49f3-8f5e-1428a84d9265
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269185(v=EXCHG.10)
ms:contentKeyID: 32765488
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
ms.openlocfilehash: a696d1c52a42cad2b3b67b047984b48d77637a1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346998"
---
# <a name="jet_indexlist-structure"></a>JET_INDEXLIST-Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_indexlist-structure"></a>JET_INDEXLIST-Struktur

Die **JET_INDEXLIST** -Struktur enthält die erforderlichen Informationen zum Durchlaufen einer temporären Tabelle, die von der [jetgetindexinfo](./jetgetindexinfo-function.md) -Funktion oder der [jetgettableindexinfo](./jetgettableindexinfo-function.md) -Funktion erstellt wird. Jede Zeile in der temporären Tabelle beschreibt eine Spalte eines Indexes.

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      gned long cRecord;
      JET_COLUMNID columnidindexname;
      JET_COLUMNID columnidgrbitIndex;
      JET_COLUMNID columnidcKey;
      JET_COLUMNID columnidcEntry;
      JET_COLUMNID columnidcPage;
      JET_COLUMNID columnidcColumn;
      JET_COLUMNID columnidiColumn;
      JET_COLUMNID columnidcolumnid;
      JET_COLUMNID columnidcoltyp;
      JET_COLUMNID columnidCountry;
      JET_COLUMNID columnidLangid;
      JET_COLUMNID columnidCp;
      JET_COLUMNID columnidCollate;
      JET_COLUMNID columnidgrbitColumn;
      JET_COLUMNID columnidcolumnname;
      JET_COLUMNID columnidLCMapFlags;
    } JET_INDEXLIST;
```

### <a name="members"></a>Member

**cbStruct**

Die Größe der Struktur in Bytes. Der API-Aufruf aktualisiert dieses Feld, sodass der Aufrufer sicherstellen muss, dass dieser Wert sizeof (JET_INDEXLIST) entspricht.

**TableID**

Der Tabellen Bezeichner der temporären Tabelle, die erstellt wurde. Es liegt in der Verantwortung des Aufrufers, die Tabelle zu schließen.

**crecord**

Die Anzahl der Datensätze in der temporären Tabelle, die erstellt wurde.

**columnidindexname**

Der Spalten Bezeichner des Index namens.

Diese Spalte ist eine [JET_coltypText](./jet-coltyp.md).

**columnidgrbitindex**

Der Spalten Bezeichner der *grbits* , die für den Index verwendet werden. Eine Liste der gültigen Bits finden Sie unter [JET_INDEXCREATE](./jet-indexcreate-structure.md) .

Diese Spalte ist eine [JET_coltypLong](./jet-coltyp.md).

**columnidckey**

Der Spalten Bezeichner der Anzahl der Schlüssel im Index.

Diese Spalte ist eine [JET_coltypLong](./jet-coltyp.md).

**columnidcentry**

Der Spalten Bezeichner der Anzahl der Einträge im Index.

Diese Spalte ist eine [JET_coltypLong](./jet-coltyp.md).

**columnidcpage**

Der Spalten Bezeichner der Anzahl der Seiten, die vom Index verwendet werden. Diese Spalte ist eine [JET_coltypLong](./jet-coltyp.md).

**columnidccolumn**

Der Spalten Bezeichner der Gesamtzahl der Spalten, die der Index umfasst.

Diese Spalte ist eine [JET_coltypLong](./jet-coltyp.md).

**columnidicolumn**

Der Spalten Bezeichner der Anzahl der Spalten im Index. Weitere Informationen finden Sie im Abschnitt "Hinweise" in diesem Thema.

Diese Spalte ist eine [JET_coltypLong](./jet-coltyp.md).

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
<td><p>cindexinfocols<br />
15</p></td>
<td><p>Gibt an, dass 15 Spalten zulässig sind.</p></td>
</tr>
<tr class="even">
<td><p>ccolumninfocols<br />
14</p></td>
<td><p>Gibt an, dass 14 Spalten zulässig sind.</p></td>
</tr>
<tr class="odd">
<td><p>cobjectinfocols<br />
9</p></td>
<td><p>Gibt an, dass 9 Spalten zulässig sind.</p></td>
</tr>
</tbody>
</table>


**columnidcolumnid**

Der Spalten Bezeichner der indizierten Spalte. Weitere Informationen finden Sie im Abschnitt "Hinweise" in diesem Thema. Diese Spalte ist eine [JET_coltypLong](./jet-coltyp.md).

**columnidcolyp**

Der Spalten Bezeichner des coltyps der Spalte, der indiziert wird. Weitere Informationen finden Sie im Abschnitt "Hinweise" in diesem Thema. Diese Spalte ist eine [JET_coltypLong](./jet-coltyp.md).

**columnidcountry**

Der Spalten Bezeichner des Ländercodes der indizierten Spalte. Der Ländercode ist veraltet.

Diese Spalte ist eine [JET_coltypShort](./jet-coltyp.md).

**columnidlangid**

Der Spalten Bezeichner des sprach Bezeichners (LCID), unter dem der Index erstellt wurde. Weitere Informationen finden Sie unter [JET_INDEXCREATE](./jet-indexcreate-structure.md).

Diese Spalte ist eine [JET_coltypShort](./jet-coltyp.md).

**columnidcp**

Der Spalten Bezeichner der Codepage, unter der der Index erstellt wurde. Weitere Informationen finden Sie unter [JET_COLUMNCREATE](./jet-columncreate-structure.md).

Diese Spalte ist eine [JET_coltypShort](./jet-coltyp.md).

**columnidcollate**

Der Spalten Bezeichner der Sortierungs Sequenz, unter der der Index erstellt wurde. Die Sortierungs Sequenz ist veraltet.

Diese Spalte ist eine [JET_coltypShort](./jet-coltyp.md).

**columnidgrbitcolumn**

Der Spalten Bezeichner der *grbits* , die auf die Reihenfolge der Spalte im Index angewendet werden.

Die Daten für diese Spalte können als JET_bitKeyAscending oder JET_bitKeyDescending angeordnet werden. Diese Spalte ist eine [JET_coltypLong](./jet-coltyp.md). Ein Index, der als "-Column1 \\ 0 + Column2 \\ 0" definiert ist, hat z. b. JET_bitKeyDescending für "Column1" und JET_bitKeyAscending für "Column2".

Die folgenden Optionen sind für diesen Member gültig.

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
<td><p>JET_bitKeyAscending</p></td>
<td><p>Ein Index Segment in aufsteigender Reihenfolge.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitKeyDescending</p></td>
<td><p>Ein Index Segment in absteigender Reihenfolge.</p></td>
</tr>
</tbody>
</table>


**columnidcolumnname**

Der Spalten Bezeichner des Spaltennamens.

Diese Spalte ist eine [JET_coltypText](./jet-coltyp.md).

**columnidlcmapflags**

Der Spalten Bezeichner der Flags, die verwendet werden, um den Index zu erstellen. Weitere Informationen finden Sie im Abschnitt **dwmapflags** der [JET_UNICODEINDEX](./jet-unicodeindex-structure.md).

Diese Spalte ist eine [JET_coltypLong](./jet-coltyp.md).

### <a name="remarks"></a>Bemerkungen

Jede Zeile in der temporären Tabelle entspricht einer Spalte in einem bestimmten Index.

Der Index "+ A \\ 0 + B \\ 0 + C \\ 0 + D \\ 0 + E 0" ist z. b. \\ größer als fünf Spalten, und es werden fünf Zeilen in der temporären Tabelle belegt. Jede dieser fünf Zeilen hat den Wert 5 in der Spalte, die von der Spalte "ColumnID" identifiziert wird. Jede Zeile weist jedoch einen anderen Wert für die Spalten Spalte auf (von 0 bis 4).

Die Anzahl der Schlüssel in einem bestimmten Index entspricht der Anzahl der eindeutigen Werte, die ein Aufrufer suchen und eine genaue Übereinstimmung erhalten kann. Die Anzahl der Einträge ist die Anzahl der Zeilen, denen ein Index entspricht. Wenn ein Index eine Eindeutigkeits Einschränkung aufweist, entspricht die Anzahl der Schlüssel der Anzahl der Einträge. Wenn eine Tabelle z. b. die folgenden Informationen enthält und ein Index für die Spalte mit dem Namen "Key" erstellt wird, gibt es drei Schlüssel (100, 200 und 500), aber es gibt vier Einträge ("This", "is", "an" und "example").

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Schlüssel</p></th>
<th><p>Eingabe</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>100</p></td>
<td><p>&quot;this&quot;</p></td>
</tr>
<tr class="even">
<td><p>100</p></td>
<td><p>&quot;is&quot;</p></td>
</tr>
<tr class="odd">
<td><p>200</p></td>
<td><p>&quot;halbe&quot;</p></td>
</tr>
<tr class="even">
<td><p>500</p></td>
<td><p>&quot;example&quot;</p></td>
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


### <a name="see-also"></a>Weitere Informationen

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNCREATE](./jet-columncreate-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_UNICODEINDEX](./jet-unicodeindex-structure.md)  
[Jetgetindexinfo](./jetgetindexinfo-function.md)  
[Jetgettableindexinfo](./jetgettableindexinfo-function.md)
