---
description: 'Weitere Informationen zu: JET_ENUMCOLUMN-Struktur'
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

Die **JET_ENUMCOLUMN-Struktur** listet die Spaltenwerte eines Datensatzes auf, wenn die [JetEnumerateColumns-Funktion](./jetenumeratecolumns-function.md) verwendet wird. [JetEnumerateColumns](./jetenumeratecolumns-function.md) gibt ein Array von **JET_ENUMCOLUMN** Strukturen zurück. Das Array wird im Arbeitsspeicher zurückgegeben, der mithilfe des [reloc-kompatiblen](/cpp/c-runtime-library/reference/realloc?view=vs-2019) Rückrufs zugeordnet wird, der für diese API bereitgestellt wurde.

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

Die Aufzählungsspalten-ID.

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
<td><p>JET_bitEnumeratePresenceOnly angegeben wurde und mindestens ein Spaltenwert ungleich NULL für diese Spalte zurückgegeben worden wäre.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnSingleValue</p></td>
<td><p>JET_bitEnumerateCompressOutput angegeben wurde und genau ein Nicht-NULL-Spaltenwert für diese Spalte zurückgegeben wurde. Daher wurde die komprimierte Form von <strong>JET_ENUMCOLUMN</strong> zurückgegeben. Weitere Informationen finden Sie <strong>unter JET_ENUMCOLUMN.</strong></p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnSkipped</p></td>
<td><p>Die Spalten-ID in der <a href="gg269251(v=exchg.10).md">JET_ENUMCOLUMNID</a> Struktur, die dieser <strong>JET_ENUMCOLUMN</strong> Struktur entspricht, war 0 (null).</p></td>
</tr>
</tbody>
</table>


**cEnumColumnValue**

Das Array von Spaltenwerten, das für die Spalte aufzählt wurde. Der Ausgabepuffer wird im Arbeitsspeicher zurückgegeben, der mit dem [relokalkompatiblen](/cpp/c-runtime-library/reference/realloc?view=vs-2019) Rückruf zugeordnet wurde, der an [JetEnumerateColumns](./jetenumeratecolumns-function.md)bereitgestellt wurde.

Dieser Ausgabepuffer wird verwendet, wenn der Spaltenstatuscode nicht gleich JET_wrnColumnSingleValue ist. Weitere Informationen finden Sie unter [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Dies wird zurückgegeben, wenn "err \! = JET_wrnColumnSingleValue".

**rgEnumColumnValue**

Das Array von Spaltenwerten, das für die Spalte aufzählt wurde. Der Ausgabepuffer wird im Arbeitsspeicher zurückgegeben, der mit dem [relokalkompatiblen](/cpp/c-runtime-library/reference/realloc?view=vs-2019) Rückruf zugeordnet wurde, der an [JetEnumerateColumns](./jetenumeratecolumns-function.md)bereitgestellt wurde.

Dieser Ausgabepuffer wird verwendet, wenn der Spaltenstatuscode nicht gleich JET_wrnColumnSingleValue ist. Weitere Informationen finden Sie unter [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Dies wird zurückgegeben, wenn "err \! = JET_wrnColumnSingleValue".

**cbData**

Der Spaltenwert, der für die Spalte aufzählt wurde.

Der Ausgabepuffer wird im Arbeitsspeicher zurückgegeben, der mit dem [relokalkompatiblen](/cpp/c-runtime-library/reference/realloc?view=vs-2019) Rückruf zugeordnet wurde, der an [JetEnumerateColumns](./jetenumeratecolumns-function.md)bereitgestellt wurde.

Dieser Ausgabepuffer wird nur verwendet, wenn der Spaltenstatuscode JET_wrnColumnSingleValue ist. Weitere Informationen finden Sie unter [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Dies wird zurückgegeben, wenn "err == JET_wrnColumnSingleValue".

**pvData**

Der Spaltenwert, der für die Spalte aufzählt wurde.

Der Ausgabepuffer wird im Arbeitsspeicher zurückgegeben, der mit dem [relokalkompatiblen](/cpp/c-runtime-library/reference/realloc?view=vs-2019) Rückruf zugeordnet wurde, der an [JetEnumerateColumns](./jetenumeratecolumns-function.md)bereitgestellt wurde.

Dieser Ausgabepuffer wird nur verwendet, wenn der Spaltenstatuscode JET_wrnColumnSingleValue ist. Weitere Informationen finden Sie unter [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Dies wird zurückgegeben, wenn "err == JET_wrnColumnSingleValue".

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
<td><p>Deklariert in Esent.h.</p></td>
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
