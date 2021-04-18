---
description: 'Weitere Informationen finden Sie hier: JET_DBINFOUPGRADE Struktur'
title: JET_DBINFOUPGRADE-Struktur
TOCTitle: JET_DBINFOUPGRADE Structure
ms:assetid: dd8a881a-33b5-4314-8cfb-b1d75ad37b21
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294114(v=EXCHG.10)
ms:contentKeyID: 32765728
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
ms.openlocfilehash: 9652b0050805ad116a7087cb2ec4cd146255b6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345054"
---
# <a name="jet_dbinfoupgrade-structure"></a>JET_DBINFOUPGRADE-Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_dbinfoupgrade-structure"></a>JET_DBINFOUPGRADE-Struktur

Die **JET_DBINFOUPGRADE** Struktur enthält Informationen zum Upgradestatus der Datenbank. Dieser Wert wird nur abgerufen, wenn **JET_DBINFOUPGRADE** an [jetgetdatabaseingefo](./jetgetdatabaseinfo-function.md) oder [jetgetdatabasefilinput Info](./jetgetdatabasefileinfo-function.md)übermittelt wurde. Diese Struktur ist für aktuelle Betriebssystemversionen der Datenbank-Engine nicht erforderlich.

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cbFilesizeLow;
      unsigned long cbFilesizeHigh;
      unsigned long cbFreeSpaceRequiredLow;
      unsigned long  cbFreeSpaceRequiredHigh;
      unsigned long csecToUpgrade;
      union {
        unsigned long ulFlags;
        struct {
          unsigned long fUpgradable  :1;
          unsigned long fAlreadyUpgraded  :1;
        };
      };
    } JET_DBINFOUPGRADE;
```

### <a name="members"></a>Member

**cbStruct**

Legen Sie auf die Größe der **JET_DBINFOUPGRADE** Struktur in Bytes fest.

**cbfilesizelow**

Das niedrige **DWORD** , das die aktuelle Dateigröße für die Datenbank widerspiegelt.

**cbfilesizehigh**

Das hohe **DWORD** , das die aktuelle Dateigröße für die Datenbank widerspiegelt.

**cbfreespacerequiredlow**

Das niedrige **DWORD** des geschätzten freien Speicherplatzes, der für ein direktes Upgrade benötigt wird.

**cbfreespacerequiredhigh**

Das hohe **DWORD** des geschätzten freien Speicherplatzes, der für ein direktes Upgrade benötigt wird.

**csectoupgrade**

Die geschätzte Zeit, die für das Upgrade benötigt wird (in Sekunden).

**ulFlags**

Ein Bitfeld, das aus null oder mehr der folgenden Flags besteht: **fupgradable**, **falsoryupgrade**.

**fupgradable**

Die Datenbank kann aktualisiert werden.

**falsch aktualisiert**

Die Datenbank wird auf das aktuelle Datenbankformat aktualisiert.

### <a name="remarks"></a>Bemerkungen

Eine **JET_DBINFOUPGRADE** Struktur wird durch einen Aufrufen von [jetgetdatabaseinfo](./jetgetdatabaseinfo-function.md) oder [jetgetdatabasefileinfo](./jetgetdatabasefileinfo-function.md)aufgefüllt. Wenn die Funktion nicht erfolgreich ausgeführt werden kann, ist der Inhalt der-Struktur nicht definiert.

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

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[Jetgetindexinfo](./jetgetindexinfo-function.md)  
[Jetgetobjectinfo](./jetgetobjectinfo-function.md)  
[Jetgettableindexinfo](./jetgettableindexinfo-function.md)  
[Jetgettableinfo](./jetgettableinfo-function.md)
