---
description: 'Weitere Informationen zu: JET_INDEXLIST-Struktur'
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
ms.openlocfilehash: c57fda6eaea161839cdaa758c41f13749d4c5eda
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480046"
---
# <a name="jet_indexlist-structure"></a>JET_INDEXLIST-Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_indexlist-structure"></a>JET_INDEXLIST-Struktur

Die **JET_INDEXLIST-Struktur** enthält die erforderlichen Informationen, um eine temporäre Tabelle zu durchlaufen, die von den [JetGetIndexInfo-](./jetgetindexinfo-function.md) oder [JetGetTableIndexInfo-Funktionen](./jetgettableindexinfo-function.md) erstellt wird. Jede Zeile in der temporären Tabelle beschreibt eine Spalte eines Indexes.

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

Die Größe der -Struktur in Bytes. Der API-Aufruf aktualisiert dieses Feld, sodass der Aufrufer sicherstellen sollte, dass dieser Wert mit sizeof( JET_INDEXLIST ) übereinstimmt.

**tableid**

Der Tabellenbezeichner der temporären Tabelle, die erstellt wurde. Es liegt in der Verantwortung des Aufrufers, die Tabelle zu schließen.

**cRecord**

Die Anzahl der Datensätze in der temporären Tabelle, die erstellt wurde.

**columnidindexname**

Der Spaltenbezeichner des Indexnamens.

Diese Spalte ist ein [JET_coltypText](./jet-coltyp.md).

**columnidgrbitIndex**

Der Spaltenbezeichner der *grbits,* die für den Index verwendet werden. Eine Liste gültiger Bits finden Sie [unter JET_INDEXCREATE.](./jet-indexcreate-structure.md)

Diese Spalte ist eine [JET_coltypLong](./jet-coltyp.md).

**columnidcKey**

Der Spaltenbezeichner der Anzahl der Schlüssel im Index.

Diese Spalte ist eine [JET_coltypLong](./jet-coltyp.md).

**columnidcEntry**

Der Spaltenbezeichner der Anzahl der Einträge im Index.

Diese Spalte ist eine [JET_coltypLong](./jet-coltyp.md).

**columnidcPage**

Der Spaltenbezeichner der Vom Index verwendeten Seitenanzahl. Diese Spalte ist eine [JET_coltypLong](./jet-coltyp.md).

**columnidcColumn**

Der Spaltenbezeichner der Gesamtzahl der Spalten, die der Index umfasst.

Diese Spalte ist eine [JET_coltypLong](./jet-coltyp.md).

**columnidiColumn**

Der Spaltenbezeichner der Nummer der Spalten im Index. Weitere Informationen finden Sie im Abschnitt "Hinweise" dieses Themas.

Diese Spalte ist eine [JET_coltypLong](./jet-coltyp.md).


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>cIndexInfoCols<br />15</p> | <p>Gibt an, dass 15 Spalten zulässig sind.</p> | 
| <p>cColumnInfoCols<br />14</p> | <p>Gibt an, dass 14 Spalten zulässig sind.</p> | 
| <p>cObjectInfoCols<br />9</p> | <p>Gibt an, dass 9 Spalten zulässig sind.</p> | 



**columnidcolumnid**

Der Spaltenbezeichner der indizierten Spalte. Weitere Informationen finden Sie im Abschnitt "Hinweise" dieses Themas. Diese Spalte ist eine [JET_coltypLong](./jet-coltyp.md).

**columnidcoltyp**

Der Spaltenbezeichner des Coltyps der indizierten Spalte. Weitere Informationen finden Sie im Abschnitt "Hinweise" dieses Themas. Diese Spalte ist eine [JET_coltypLong](./jet-coltyp.md).

**columnidCountry**

Der Spaltenbezeichner des Ländercodes der indizierten Spalte. Der Ländercode ist veraltet.

Diese Spalte ist eine [JET_coltypShort](./jet-coltyp.md).

**columnidLangid**

Der Spaltenbezeichner des Sprachbezeichners (LCID), unter dem der Index erstellt wurde. Weitere Informationen finden Sie unter [JET_INDEXCREATE](./jet-indexcreate-structure.md).

Diese Spalte ist eine [JET_coltypShort](./jet-coltyp.md).

**columnidCp**

Der Spaltenbezeichner der Codepage, unter der der Index erstellt wurde. Weitere Informationen finden Sie unter [JET_COLUMNCREATE](./jet-columncreate-structure.md).

Diese Spalte ist eine [JET_coltypShort](./jet-coltyp.md).

**columnidCollate**

Der Spaltenbezeichner der Sortierungssequenz, unter der der Index erstellt wurde. Die Sortierungssequenz ist veraltet.

Diese Spalte ist eine [JET_coltypShort](./jet-coltyp.md).

**columnidgrbitColumn**

Der Spaltenbezeichner der *Grbits,* die für die Reihenfolge der Spalte im Index gelten.

Die Daten für diese Spalte können als JET_bitKeyAscending oder JET_bitKeyDescending sortiert werden. Diese Spalte ist eine [JET_coltypLong](./jet-coltyp.md). Ein Index, der als "-column1 \\ 0+column2 0" definiert ist, verfügt beispielsweise \\ über JET_bitKeyDescending für "column1" und JET_bitKeyAscending für "column2".

Die folgenden Optionen sind für dieses Element gültig.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitKeyAscending</p> | <p>Ein Indexsegment in aufsteigender Reihenfolge.</p> | 
| <p>JET_bitKeyDescending</p> | <p>Ein Indexsegment in absteigender Reihenfolge.</p> | 



**columnidcolumnname**

Der Spaltenbezeichner des Spaltennamens.

Diese Spalte ist ein [JET_coltypText](./jet-coltyp.md).

**columnidLCMapFlags**

Der Spaltenbezeichner der Flags, die zum Erstellen des Indexes verwendet werden. Weitere Informationen finden Sie im Abschnitt **dwMapFlags** [JET_UNICODEINDEX](./jet-unicodeindex-structure.md).

Diese Spalte ist eine [JET_coltypLong](./jet-coltyp.md).

### <a name="remarks"></a>Hinweise

Jede Zeile in der temporären Tabelle entspricht einer Spalte in einem bestimmten Index.

Der Index "+A \\ 0+B \\ 0+C \\ 0+D \\ 0+E \\ 0" ist beispielsweise mehr als fünf Spalten und belegt fünf Zeilen in der temporären Tabelle. Jede dieser fünf Zeilen hat den Wert 5 in der Spalte, der durch die columnid-Spalte identifiziert wird. Jede Zeile hat jedoch einen anderen Wert für die columnid-Spalte im Bereich von 0 bis 4.

Die Anzahl der Schlüssel in einem bestimmten Index entspricht der Anzahl eindeutiger Werte, für die ein Aufrufer eine genaue Übereinstimmung suchen und abrufen kann. Die Anzahl der Einträge ist die Anzahl der Zeilen, mit denen ein Index übereinstimmt. Wenn ein Index über eine Eindeutigkeitseinschränkung verfügt, entspricht die Anzahl der Schlüssel der Anzahl der Einträge. Wenn eine Tabelle beispielsweise die folgenden Informationen enthält und ein Index für die Spalte mit dem Namen "key" erstellt wird, gibt es drei Schlüssel (100, 200 und 500), aber es gibt vier Einträge ("this", "is", "an" und "example").


| <p>Schlüssel</p> | <p>Eingabe</p> | 
|------------|--------------|
| <p>100</p> | <p>"this"</p> | 
| <p>100</p> | <p>"is"</p> | 
| <p>200</p> | <p>"an"</p> | 
| <p>500</p> | <p>"Beispiel"</p> | 



### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 



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
[JetGetIndexInfo](./jetgetindexinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)
