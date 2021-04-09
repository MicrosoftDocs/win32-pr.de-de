---
description: 'Weitere Informationen finden Sie hier: JET_RECORDLIST Struktur'
title: JET_RECORDLIST Struktur
TOCTitle: JET_RECORDLIST Structure
ms:assetid: 6b4d97a0-4b42-4f7c-bb18-b6db3c92668a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269287(v=EXCHG.10)
ms:contentKeyID: 32765579
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
ms.openlocfilehash: 16aca3a13bbae7c61bfe03aca49acea775820d39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868372"
---
# <a name="jet_recordlist-structure"></a>JET_RECORDLIST Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_recordlist-structure"></a>JET_RECORDLIST Struktur

Die **JET_RECORDLIST** -Struktur findet Datensätze, die sich in der Schnittmenge der angegebenen Index Bereiche befinden, wenn Sie mit der [jetintersectindexes](./jetintersectindexes-function.md) -Funktion verwendet werden.

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      unsigned long cRecord;
      JET_COLUMNID columnidBookmark;
    } JET_RECORDLIST;
```

### <a name="members"></a>Member

**cbStruct**

Die Größe der **JET_RECORDLIST** Struktur in Bytes.

**TableID**

Der Tabellen Bezeichner einer temporären Tabelle, die die Lesezeichen für die Ergebnisse der Abfrage enthält. Die Tabelle wird automatisch geschlossen, wenn für die aktuelle Transaktion ein Rollback mit [jetrollback](./jetrollback-function.md)durchgeführt wird. Andernfalls muss Sie mit [jetclosetable](./jetclosetable-function.md)geschlossen werden.

**crecord**

Die Anzahl der Zeilen in der temporären Tabelle.

**columnidbookmark**

Der Spalten Bezeichner der Lesezeichen Spalte in der temporären Tabelle.

### <a name="remarks"></a>Bemerkungen

Die temporäre Tabelle, die von **TableID** identifiziert wird, verfügt über eine einzelne Spalte. Diese einzelne Spalte enthält Lesezeichen, und jeder Datensatz sollte in einen Puffer der Größe JET_cbBookmarkMost Bytes passen.

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

[JET_COLUMNID](./jet-columnid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLEID](./jet-tableid.md)  
[Jetclosetable](./jetclosetable-function.md)  
[Jetintersectindexes](./jetintersectindexes-function.md)  
[Jetrollback](./jetrollback-function.md)
