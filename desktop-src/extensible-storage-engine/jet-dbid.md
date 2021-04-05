---
description: 'Weitere Informationen finden Sie hier: JET_DBID'
title: JET_DBID
TOCTitle: JET_DBID
ms:assetid: 516acb79-aa75-4609-81b6-3b2e4e0c95af
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269248(v=EXCHG.10)
ms:contentKeyID: 32765550
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
ms.openlocfilehash: fe3a8ccd813ececcb42388c7d577f78e9055d5b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751376"
---
# <a name="jet_dbid"></a>JET_DBID


_**Gilt für:** Windows | Windows Server_

## <a name="jet_dbid"></a>JET_DBID

Der **JET_DBID** -Datentyp enthält das Handle für die Datenbank. Ein Daten Bank Handle wird zum Verwalten des Schemas einer Datenbank verwendet. Sie kann auch verwendet werden, um die Tabellen in der Datenbank zu verwalten.

```cpp
    typedef unsigned long JET_DBID;
```

### <a name="data-types"></a>Datentypen

JET_DBID

Handle für die Datenbank.

Der Wert JET_dbidNil gibt an, dass das Handle ungültig ist.

### <a name="remarks"></a>Bemerkungen

Ein Daten Bank Handle wird durch einen Aufrufen von [jetkreatedatabase](./jetcreatedatabase-function.md) oder [jetopd](./jetopendatabase-function.md)erstellt.

Ein Daten Bank Handle kann von [jetclosedatabase](./jetclosedatabase-function.md) explizit geschlossen oder durch [jetendsession](./jetendsession-function.md) oder [jetterm](./jetterm-function.md)implizit geschlossen werden.

Ein Daten Bank Handle kann nur innerhalb der Sitzung verwendet werden, in der es erstellt wurde. Das vorhanden sein eines Daten Bank Handles entspricht dem logischen Öffnen einer Datenbank. Ein logisches Open unterscheidet sich vom physischen Öffnen einer Datenbank. Dies geschieht, wenn eine Datenbank mit dem System verbunden ist.

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

[Jetkreatedatabase](./jetcreatedatabase-function.md)  
[Jetopumdatabase](./jetopendatabase-function.md)  
[Jetclosedatabase](./jetclosedatabase-function.md)  
[Jetendsession](./jetendsession-function.md)
