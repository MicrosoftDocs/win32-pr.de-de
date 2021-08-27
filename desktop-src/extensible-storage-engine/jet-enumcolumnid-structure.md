---
description: 'Weitere Informationen finden Sie unter: JET_ENUMCOLUMNID Struktur'
title: JET_ENUMCOLUMNID Struktur
TOCTitle: JET_ENUMCOLUMNID Structure
ms:assetid: 5480ebf1-4fc9-49b5-bbb3-12542b86c8f1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269251(v=EXCHG.10)
ms:contentKeyID: 32765553
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
ms.openlocfilehash: be9b25f989998450808ea78d99a5b96c2d4c4dc2
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984183"
---
# <a name="jet_enumcolumnid-structure"></a>JET_ENUMCOLUMNID Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_enumcolumnid-structure"></a>JET_ENUMCOLUMNID Struktur

Die **JET_ENUMCOLUMNID-Struktur** aufzählt einen bestimmten Satz von Spalten und optional einen bestimmten Satz von mehreren Werten für diese Spalten, wenn die [JetEnumerateColumns-Funktion](./jetenumeratecolumns-function.md) verwendet wird. [JetEnumerateColumns gibt](./jetenumeratecolumns-function.md) ein Array von **JET_ENUMCOLUMNID** zurück.

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      unsigned long ctagSequence;
      unsigned long* rgtagSequence;
    } JET_ENUMCOLUMNID;
```

### <a name="members"></a>Member

**Columnid**

Die aufzählte Spalten-ID.

Wenn die Spalten-ID 0 (null) ist, wird die Enumeration dieser Spalte übersprungen, und ein entsprechender Slot im Ausgabearray von [JET_ENUMCOLUMN-Strukturen](./jet-enumcolumn-structure.md) wird mit dem Spaltenzustand JET_wrnColumnSkipped.

**ctagSequence**

Identifiziert optional ein Array von Spaltenwerten (durch einen 1-basierten Index), die für die angegebene Spalten-ID aufzählt werden.

Wenn **ctagSequence** 0 (null) ist, wird **rgtagSequence** ignoriert, und alle Spaltenwerte für die angegebene Spalten-ID werden aufzählt.

Wenn ein Element von **rgtagSequence** 0 (null) ist, wird die Enumeration dieses Spaltenwerts (durch einen 1-basierten Index) übersprungen. Ein entsprechender Slot im Ausgabearray der JET_ENUMCOLUMNID **wird** mit dem Spaltenstatuswert JET_wrnColumnSkipped.

**rgtagSequence**

Ein Array von einsbasierten Indizes im Array von Spaltenwerten für eine bestimmte Spalte. Ein einzelnes Element ist eine **itagSequence,** die [in](./jet-retrievecolumn-structure.md)der JET_RETRIEVECOLUMN. Eine **itagSequence von** 0 (null) bedeutet "skip". Eine **itagSequence** von 1 bedeutet, dass der erste Spaltenwert der Spalte, 2 die zweite Spalte und so weiter zurückgeben.

### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JET_COLUMNID](./jet-columnid.md)  
[JET_ENUMCOLUMN](./jet-enumcolumn-structure.md)  
[JET_ENUMCOLUMNID]()  
[JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)  
[JetEnumerateColumns](./jetenumeratecolumns-function.md)
