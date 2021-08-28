---
description: 'Weitere Informationen finden Sie unter: JET_ENUMCOLUMNVALUE Struktur'
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
ms.openlocfilehash: 3a4d9500980434c21f9dfa6584db666418605de8
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988613"
---
# <a name="jet_enumcolumnvalue-structure"></a>JET_ENUMCOLUMNVALUE Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_enumcolumnvalue-structure"></a>JET_ENUMCOLUMNVALUE Struktur

Die **JET_ENUMCOLUMNVALUE-Struktur** aufzählt die Spaltenwerte eines Datensatzes mithilfe der [JetEnumerateColumns-Funktion.](./jetenumeratecolumns-function.md) [JetEnumerateColumns gibt](./jetenumeratecolumns-function.md) ein Array von **JET_ENUMCOLUMNVALUE** zurück. Das Array wird im Arbeitsspeicher zurückgegeben, der mit dem [realloc-kompatiblen](/cpp/c-runtime-library/reference/realloc?view=vs-2019) Rückruf zugeordnet wurde, der für diese Funktion bereitgestellt wurde.

```cpp
    typedef struct {
      unsigned long itagSequence;
      JET_ERR err;
      unsigned long cbData;
      void* pvData;
    } JET_ENUMCOLUMNVALUE;
```

### <a name="members"></a>Member

**itagSequence**

Der Spaltenwert (durch einen 1-basierten Index), der aufzählt wurde.

**Err**

Der Spaltenstatuscode, der sich aus der Enumeration des Spaltenwerts ergibt.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_wrnColumnNull</p> | <p>Der angeforderte Spaltenwert ist NULL.</p> | 
| <p>JET_wrnColumnSkipped</p> | <p>Die <em>itagSequence,</em> die im -Element des <em>rgtagSequence-Arrays</em> in der <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN-Struktur</a> angegeben ist, die dieser JET_ENUMCOLUMNVALUE Struktur war 0 (null). <strong></strong></p> | 
| <p>JET_wrnColumnTruncated</p> | <p>Der angeforderte Spaltenwert wurde auf die angegebene Größe abgeschnitten, bevor er zurückgegeben wurde.</p><p>Diese Kürzung erfolgt nur für lange Textspalten und lange binäre Spalten, die große Datenmengen enthalten.</p> | 



**cbData**

Der Spaltenwert, der für die Spalte aufzählt wurde.

Der Ausgabepuffer wird im Arbeitsspeicher zurückgegeben, der mithilfe des [realloc-kompatiblen](/cpp/c-runtime-library/reference/realloc?view=vs-2019) Rückrufs zugeordnet wurde, der [für JetEnumerateColumns bereitgestellt wurde.](./jetenumeratecolumns-function.md)

**pvData**

Der Spaltenwert, der für die Spalte aufzählt wurde.

Der Ausgabepuffer wird im Arbeitsspeicher zurückgegeben, der mithilfe des [realloc-kompatiblen](/cpp/c-runtime-library/reference/realloc?view=vs-2019) Rückrufs zugeordnet wurde, der [für JetEnumerateColumns bereitgestellt wurde.](./jetenumeratecolumns-function.md)

### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JET_ENUMCOLUMN](./jet-enumcolumn-structure.md)  
[JET_ENUMCOLUMNVALUE]()  
[JET_ERR](./jet-err.md)  
[JetEnumerateColumns](./jetenumeratecolumns-function.md)  
[realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019)
