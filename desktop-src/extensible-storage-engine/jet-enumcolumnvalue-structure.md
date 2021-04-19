---
description: 'Weitere Informationen finden Sie hier: JET_ENUMCOLUMNVALUE Struktur'
title: JET_ENUMCOLUMNVALUE Struktur
TOCTitle: JET_ENUMCOLUMNVALUE Structure
ms:assetid: a9882d7b-0c53-4a5d-bc98-0979e6e68c88
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294052(v=EXCHG.10)
ms:contentKeyID: 32765652
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
ms.openlocfilehash: bc95c6b8403a64432451ea29dbb66868fad25264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363664"
---
# <a name="jet_enumcolumnvalue-structure"></a>JET_ENUMCOLUMNVALUE Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_enumcolumnvalue-structure"></a>JET_ENUMCOLUMNVALUE Struktur

Die **JET_ENUMCOLUMNVALUE** -Struktur listet die Spaltenwerte eines Datensatzes mithilfe der [jetenumeratecolumns](./jetenumeratecolumns-function.md) -Funktion auf. [Jetenreeratecolenns](./jetenumeratecolumns-function.md) gibt ein Array von **JET_ENUMCOLUMNVALUE** Strukturen zurück. Das Array wird im Arbeitsspeicher zurückgegeben, der mit dem [rezubelegungskompatiblen](/cpp/c-runtime-library/reference/realloc?view=vs-2019) Rückruf zugewiesen wurde, der für diese Funktion bereitgestellt wurde.

```cpp
    typedef struct {
      unsigned long itagSequence;
      JET_ERR err;
      unsigned long cbData;
      void* pvData;
    } JET_ENUMCOLUMNVALUE;
```

### <a name="members"></a>Member

**itagsequence**

Der aufgelistete Spaltenwert (durch einen einsbasierten Index).

**irre**

Der Spalten Statuscode, der sich aus der Enumeration des Spaltenwerts ergibt.

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
<td><p>JET_wrnColumnNull</p></td>
<td><p>Der angeforderte Spaltenwert ist NULL.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnSkipped</p></td>
<td><p>Die <em>itagsequence</em> , die im-Element des <em>rgtagsequence</em> -Arrays in der <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> Struktur angegeben ist, die dieser <strong>JET_ENUMCOLUMNVALUE</strong> Struktur entspricht, war 0 (null).</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnTruncated</p></td>
<td><p>Der angeforderte Spaltenwert wurde auf die angegebene Größe abgeschnitten, bevor er zurückgegeben wird.</p>
<p>Diese Kürzung erfolgt nur für lange Text-und lange binäre Spalten, die große Datenmengen enthalten.</p></td>
</tr>
</tbody>
</table>


**cbData**

Der Spaltenwert, der für die Spalte aufgelistet wurde.

Der Ausgabepuffer wird im Arbeitsspeicher zurückgegeben, der mit dem [rezubelegungskompatiblen](/cpp/c-runtime-library/reference/realloc?view=vs-2019) Rückruf zugewiesen wurde, der für [jetenumeratecolumns](./jetenumeratecolumns-function.md)bereitgestellt wurde.

**pvData**

Der Spaltenwert, der für die Spalte aufgelistet wurde.

Der Ausgabepuffer wird im Arbeitsspeicher zurückgegeben, der mit dem [rezubelegungskompatiblen](/cpp/c-runtime-library/reference/realloc?view=vs-2019) Rückruf zugewiesen wurde, der für [jetenumeratecolumns](./jetenumeratecolumns-function.md)bereitgestellt wurde.

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

[JET_ENUMCOLUMN](./jet-enumcolumn-structure.md)  
[JET_ENUMCOLUMNVALUE]()  
[JET_ERR](./jet-err.md)  
[Jetenreeratecolumschlag](./jetenumeratecolumns-function.md)  
[realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019)
