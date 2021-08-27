---
description: 'Weitere Informationen finden Sie unter: JET_RECORDLIST Struktur'
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
ms.openlocfilehash: e83145f74d5edf97658fdadc62f018a151ee8b55
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988227"
---
# <a name="jet_recordlist-structure"></a>JET_RECORDLIST Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_recordlist-structure"></a>JET_RECORDLIST Struktur

Die **JET_RECORDLIST-Struktur** sucht Datensätze, die sich in der Schnittmenge der angegebenen Indexbereiche befinden, wenn sie mit der [JetIntersectIndexes-Funktion verwendet](./jetintersectindexes-function.md) werden.

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

Die Größe  der JET_RECORDLIST-Struktur in Bytes.

**tableid**

Der Tabellenbezeichner einer temporären Tabelle, die die Lesezeichen für die Ergebnisse der Abfrage enthält. Die Tabelle wird automatisch geschlossen, wenn für die aktuelle Transaktion ein Rollback mit [JetRollback ausgeführt wird.](./jetrollback-function.md) Andernfalls muss sie mit [JetCloseTable geschlossen werden.](./jetclosetable-function.md)

**cRecord**

Die Anzahl der Zeilen in der temporären Tabelle.

**columnidBookmark**

Der Spaltenbezeichner der Lesezeichenspalte in der temporären Tabelle.

### <a name="remarks"></a>Bemerkungen

Die temporäre Tabelle, die durch **tableid identifiziert wird,** verfügt über eine einzelne Spalte. Diese einzelne Spalte enthält Lesezeichen, und jeder Datensatz sollte in einen Puffer mit einer Größe von JET_cbBookmarkMost passen.

### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JET_COLUMNID](./jet-columnid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetIntersectIndexes](./jetintersectindexes-function.md)  
[JetRollback](./jetrollback-function.md)
