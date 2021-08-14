---
description: 'Weitere Informationen finden Sie unter: JET_ENUMCOLUMN Struktur'
title: JET_ENUMCOLUMN-Struktur
TOCTitle: JET_ENUMCOLUMN Structure
ms:assetid: f8f512fd-5fcf-47ed-a5db-2fb3bd76c2d7
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294138(v=EXCHG.10)
ms:contentKeyID: 32765752
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
ms.openlocfilehash: 6ac89a45e37631b554fc7b2dc28266c95cfae3fba54debb427abfd8db621ea3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118766088"
---
# <a name="jet_enumcolumn-structure"></a>JET_ENUMCOLUMN-Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_enumcolumn-structure"></a>JET_ENUMCOLUMN-Struktur

Die **JET_ENUMCOLUMN-Struktur** aufzählt die Spaltenwerte eines Datensatzes, wenn die [JetEnumerateColumns-Funktion](./jetenumeratecolumns-function.md) verwendet wird. [JetEnumerateColumns gibt](./jetenumeratecolumns-function.md) ein Array von **JET_ENUMCOLUMN** zurück. Das Array wird im Arbeitsspeicher zurückgegeben, der mit dem [realloc-kompatiblen](/cpp/c-runtime-library/reference/realloc?view=vs-2019) Rückruf zugeordnet wird, der für diese API bereitgestellt wurde.

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      JET_ERR err;
      union {
        struct {
          unsigned long cEnumColumnValue;
          JET_ENUMCOLUMNVALUE rgEnumColumnValue;
        };
        struct {
          unsigned long cbData;
          void* pvData;
        };
      };
    } JET_ENUMCOLUMN;
```

### <a name="members"></a>Member

**Columnid**

Die Spalten-ID, die aufzählt wurde.

**Err**

Der Spaltenstatuscode, der sich aus der Enumeration der Spalte ergibt.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Fehlercodes</p></th>
<th><p>Bedeutung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errBadColumnId</p></td>
<td><p>Die Spalten-ID liegt außerhalb der rechtlichen Grenzen einer Spalten-ID.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnNotFound</p></td>
<td><p>Die durch die Spalten-ID beschriebene Spalte ist in der Tabelle nicht vorhanden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnNull</p></td>
<td><p>Alle Werte für diese Spalte sind NULL.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnPresent</p></td>
<td><p>JET_bitEnumeratePresenceOnly wurde angegeben, und für diese Spalte wurde mindestens ein Nicht-NULL-Spaltenwert zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnSingleValue</p></td>
<td><p>JET_bitEnumerateCompressOutput wurde angegeben, und für diese Spalte wurde genau ein Nicht-NULL-Spaltenwert zurückgegeben. Daher wurde die komprimierte Form der <strong>JET_ENUMCOLUMN</strong> zurückgegeben. Weitere <strong>JET_ENUMCOLUMN</strong> finden Sie unter .</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnSkipped</p></td>
<td><p>Die Spalten-ID in <a href="gg269251(v=exchg.10).md">der JET_ENUMCOLUMNID</a> struktur, die dieser Struktur <strong>entspricht JET_ENUMCOLUMN</strong> 0 (null) war.</p></td>
</tr>
</tbody>
</table>


**cEnumColumnValue**

Das Array von Spaltenwerten, das für die Spalte aufzählt wurde. Der Ausgabepuffer wird im Arbeitsspeicher zurückgegeben, der mithilfe des [realloc-kompatiblen](/cpp/c-runtime-library/reference/realloc?view=vs-2019) Rückrufs zugeordnet wurde, der [für JetEnumerateColumns bereitgestellt wurde.](./jetenumeratecolumns-function.md)

Dieser Ausgabepuffer wird verwendet, wenn der Spaltenstatuscode nicht gleich JET_wrnColumnSingleValue. Weitere Informationen finden Sie unter [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Dies wird zurückgegeben, wenn "err \! = JET_wrnColumnSingleValue" ist.

**rgEnumColumnValue**

Das Array von Spaltenwerten, das für die Spalte aufzählt wurde. Der Ausgabepuffer wird im Arbeitsspeicher zurückgegeben, der mithilfe des [realloc-kompatiblen](/cpp/c-runtime-library/reference/realloc?view=vs-2019) Rückrufs zugeordnet wurde, der [für JetEnumerateColumns bereitgestellt wurde.](./jetenumeratecolumns-function.md)

Dieser Ausgabepuffer wird verwendet, wenn der Spaltenstatuscode nicht gleich JET_wrnColumnSingleValue. Weitere Informationen finden Sie unter [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Dies wird zurückgegeben, wenn "err \! = JET_wrnColumnSingleValue" ist.

**cbData**

Der Spaltenwert, der für die Spalte aufzählt wurde.

Der Ausgabepuffer wird im Arbeitsspeicher zurückgegeben, der mithilfe des [realloc-kompatiblen](/cpp/c-runtime-library/reference/realloc?view=vs-2019) Rückrufs zugeordnet wurde, der [für JetEnumerateColumns bereitgestellt wurde.](./jetenumeratecolumns-function.md)

Dieser Ausgabepuffer wird nur verwendet, wenn der Spaltenstatuscode JET_wrnColumnSingleValue. Weitere Informationen finden Sie unter [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Dies wird zurückgegeben, wenn "err == JET_wrnColumnSingleValue" ist.

**pvData**

Der Spaltenwert, der für die Spalte aufzählt wurde.

Der Ausgabepuffer wird im Arbeitsspeicher zurückgegeben, der mithilfe des [realloc-kompatiblen](/cpp/c-runtime-library/reference/realloc?view=vs-2019) Rückrufs zugeordnet wurde, der [für JetEnumerateColumns bereitgestellt wurde.](./jetenumeratecolumns-function.md)

Dieser Ausgabepuffer wird nur verwendet, wenn der Spaltenstatuscode JET_wrnColumnSingleValue. Weitere Informationen finden Sie unter [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Dies wird zurückgegeben, wenn "err == JET_wrnColumnSingleValue" ist.

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
<td><p>In Esent.h deklariert.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_ENUMCOLUMNID](./jet-enumcolumnid-structure.md)  
[JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-structure.md)  
[JetEnumerateColumns](./jetenumeratecolumns-function.md)  
[realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019)
