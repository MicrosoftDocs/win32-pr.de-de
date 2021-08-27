---
description: 'Weitere Informationen zu: JET_DBINFOUPGRADE-Struktur'
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
ms.openlocfilehash: 57c9265f45412bd31e087a52ab2b923c9c55c430
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467657"
---
# <a name="jet_dbinfoupgrade-structure"></a>JET_DBINFOUPGRADE-Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_dbinfoupgrade-structure"></a>JET_DBINFOUPGRADE-Struktur

Die **JET_DBINFOUPGRADE-Struktur** enthält Informationen zum Upgradestatus der Datenbank. Dieser Wert wird nur abgerufen, wenn **JET_DBINFOUPGRADE** an [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) oder [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)übergeben wurde. Diese Struktur ist für aktuelle Betriebssystemversionen der Datenbank-Engine nicht erforderlich.

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

Wird auf die Größe der **JET_DBINFOUPGRADE-Struktur** in Bytes festgelegt.

**cbFilesizeLow**

Das niedrige **DWORD,** das die aktuelle Dateigröße für die Datenbank widerspiegelt.

**cbFilesizeHigh**

Der hohe **DWORD-Ausdruck,** der die aktuelle Dateigröße für die Datenbank wiedergibt.

**cbFreeSpaceRequiredLow**

Das niedrige **DWORD** des geschätzten freien Speicherplatzes, der für ein upgrade in-place erforderlich ist.

**cbFreeSpaceRequiredHigh**

Das hohe **DWORD** des geschätzten freien Speicherplatzes, der für ein upgrade in-place erforderlich ist.

**csecToUpgrade**

Die geschätzte Zeit, die für das Upgrade benötigt wird(in Sekunden).

**ulFlags**

Ein Bitfeld, das aus 0 (null) oder mehr der folgenden Flags besteht: **fUpgradable**, **fAlreadyUpgraded**.

**fUpgradable**

Die Datenbank kann aktualisiert werden.

**fAlreadyUpgraded**

Die Datenbank wird auf das aktuelle Datenbankformat aktualisiert.

### <a name="remarks"></a>Hinweise

Eine **JET_DBINFOUPGRADE** Struktur wird durch einen Aufruf von [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) oder [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)aufgefüllt. Wenn die Funktion nicht erfolgreich ist, ist der Inhalt der -Struktur nicht definiert.

### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetIndexInfo](./jetgetindexinfo-function.md)  
[JetGetObjectInfo](./jetgetobjectinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetGetTableInfo](./jetgettableinfo-function.md)
