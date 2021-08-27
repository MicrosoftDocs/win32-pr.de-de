---
description: 'Weitere Informationen finden Sie unter: JET_DBINFOMISC Struktur'
title: JET_DBINFOMISC-Struktur
TOCTitle: JET_DBINFOMISC Structure
ms:assetid: ff287087-35b8-495e-9922-418ec2439e19
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294147(v=EXCHG.10)
ms:contentKeyID: 32765761
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7d7861e558bbf6a1938d252a52e7bb781068a331
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476866"
---
# <a name="jet_dbinfomisc-structure"></a>JET_DBINFOMISC-Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_dbinfomisc-structure"></a>JET_DBINFOMISC-Struktur

Die **JET_DBINFOMISC-Struktur** enthält verschiedene Informationen zu einer Datenbank. Dies sind die Informationen, die im Datenbankheader enthalten sind.

```cpp
    typedef struct {
      unsigned long ulVersion;
      unsigned long ulUpdate;
      JET_SIGNATURE signDb;
      unsigned long dbstate;
      JET_LGPOS lgposConsistent;
      JET_LOGTIME logtimeConsistent;
      JET_LOGTIME logtimeAttach;
      JET_LGPOS lgposAttach;
      JET_LOGTIME logtimeDetach;
      JET_LGPOS lgposDetach;
      JET_SIGNATURE signLog;
      JET_BKINFO bkinfoFullPrev;
      JET_BKINFO bkinfoIncPrev;
      JET_BKINFO bkinfoFullCur;
      unsigned long fShadowingDisabled;
      unsigned long fUpgradeDb;
      unsigned long dwMajorVersion;
      unsigned long dwMinorVersion;
      unsigned long dwBuildNumber;
      long lSPNumber;
      unsigned long cbPageSize;
    } JET_DBINFOMISC;
```

### <a name="members"></a>Member

**ulVersion**

Die native Version der Datenbank-Engine, die die Datenbank erstellt hat. Informationen zum Abrufen der nativen Version für die aktuelle Datenbank-Engine finden Sie unter [JetGetVersion.](./jetgetversion-function.md)

**ulUpdate**

Verfolgt inkrementelle Aktualisierungen des Datenbankformats nach, die abwärtskompatibel sind.


| <p>ulVersion, ulUpdate =</p> | <p>Bedeutung</p> | 
|------------------------------|----------------|
| <p>0x620,0</p> | <p>Betaformat des ursprünglichen Betriebssystems (22.4.97).</p> | 
| <p>0x620,1</p> | <p>Fügen Sie Spalten im Katalog für die bedingte Indizierung und OLD (29.05.97) hinzu.</p> | 
| <p>0x620,2</p> | <p>Fügen Sie das Flag fLocalizedText in IDB (5.6.97) hinzu.</p> | 
| <p>0x620,3</p> | <p>Fügen SPLIT_BUFFER Stammseiten der Raumstruktur hinzu (30.10.97).</p> | 
| <p>0x620,2</p> | <p>Wenden Sie die Revision zurück, damit ESE97 vorwärtskompatibel bleibt (28.1.98).</p> | 
| <p>0x620,3</p> | <p>Fügen Sie dem Katalog neue markierte Spalten hinzu ("CallbackData" und "CallbackDependencies").</p> | 
| <p>0x620,4</p> | <p>SLV-Unterstützung: signSLV, fSLVExists in db header (5/5/98).</p> | 
| <p>0x620,5</p> | <p>Neue SLV-Platzstruktur (29.05.98)</p> | 
| <p>0x620,6</p> | <p>SLV-Raumkarte (12.10.98)</p> | 
| <p>0x620,7</p> | <p>4-Byte-IDXSEG (10.12.98).</p> | 
| <p>0x620,8</p> | <p>Neues Vorlagenspaltenformat (25.1.99).</p> | 
| <p>0x620,9</p> | <p>Sortierte Vorlagenspalten (24.06.99).</p> | 
| <p>0x623,0</p> | <p>Neuer Space Manager (15.5.99)</p> | 



**signDb**

Signatur der Datenbank (einschließlich Erstellungszeit). Diese Struktur ist 28 Bytes.

**dbstate**

Dies ist der Datenbankstatus.

Für diesen Member sind die folgenden Optionen verfügbar.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_dbstateJustCreated<br />1</p> | <p>Die Datenbank wurde gerade erstellt.</p> | 
| <p>JET_dbstateDirtyShutdown<br />2</p> | <p>Für die Datenbank muss eine harte oder weiche Wiederherstellung ausgeführt werden, um nutzbar oder umsetzbar zu werden. Es sollte nicht versucht werden, Datenbanken in diesem Zustand zu verschieben.</p> | 
| <p>JET_dbstateCleanShutdown<br />3</p> | <p>Die Datenbank befindet sich in einem bereinigten Zustand. Die Datenbank kann ohne Protokolldateien angefügt werden.</p> | 
| <p>JET_dbstateBeingConverted<br />4</p> | <p>Die Datenbank wird aktualisiert.</p> | 
| <p>JET_dbstateForceDetach<br />5</p> | <p>Intern.</p> | 



**lgposConsistent**

NULL, wenn sich die Datenbank in einem dirty-Zustand befindet. Dies ist die Protokollposition, die beim letzten Herunterfahren der Datenbank verwendet wurde.

**logtimeConsistent**

NULL, wenn sich die Datenbank in einem dirty-Zustand befindet. Dies ist der Zeitpunkt, zu dem die Datenbank zuletzt in einen zustandsbereinigungsbereinigungsbereinigten Herunterfahrenzustand gebracht wurde.

**logtimeAttach**

Der Zeitpunkt, zu dem die Datenbank zuletzt mit [JetAttachDatabase angefügt wurde.](./jetattachdatabase-function.md)

**lgposAttach**

Die Protokollposition, die beim letzten Anfügen der Datenbank mit [JetAttachDatabase verwendet wurde.](./jetattachdatabase-function.md)

**logtimeDetach**

Der Zeitpunkt, zu dem die Datenbank zuletzt mit [JetDetachDatabase getrennt wurde.](./jetdetachdatabase-function.md)

**lgposDetach**

Die Protokollposition, die beim letzten Trennen der Datenbank mit [JetDetachDatabase verwendet wurde.](./jetdetachdatabase-function.md)

**signLog**

Unterstützt die ESE-Infrastruktur und kann nicht in Ihrem Code verwendet werden.

**bkinfoFullPrev**

Unterstützt die ESE-Infrastruktur und kann nicht in Ihrem Code verwendet werden.

**bkinfoIncPrev**

Unterstützt die ESE-Infrastruktur und kann nicht in Ihrem Code verwendet werden.

**bkinfoFullCur**

Unterstützt die ESE-Infrastruktur und kann nicht in Ihrem Code verwendet werden.

**fShadowingDisabled**

Unterstützt die ESE-Infrastruktur und kann nicht in Ihrem Code verwendet werden.

**fUpgradeDb**

Unterstützt die ESE-Infrastruktur und kann nicht in Ihrem Code verwendet werden.

**dwMajorVersion**

Stellt die Windows NT-Versionsnummern dar, wenn die Datenbankindizes aktualisiert wurden. Wird zum Aktualisieren von Indizes verwendet.

**dwMinorVersion**

Stellt die Windows NT-Versionsnummern dar, wenn die Datenbankindizes aktualisiert wurden. Wird zum Aktualisieren von Indizes verwendet.

**dwBuildNumber**

Stellt die Windows NT-Versionsnummern dar, wenn die Datenbankindizes aktualisiert wurden. Wird zum Aktualisieren von Indizes verwendet.

**lSPNumber**

Stellt die Windows NT-Versionsnummern dar, wenn die Datenbankindizes aktualisiert wurden. Wird zum Aktualisieren von Indizes verwendet.

**cbPageSize**

Größe der Datenbankseite. 0 bedeutet, dass die Seitengröße 4 KB beträgt.

Dieser Wert wird nur abgerufen, wenn JET_DbInfoMisc [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) oder [JetGetDatabaseFileInfo übergeben wurde.](./jetgetdatabasefileinfo-function.md)

### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JET_BKINFO](./jet-bkinfo-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_LGPOS](./jet-lgpos-structure.md)  
[JET_SIGNATURE](./jet-signature-structure.md)  
[JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)  
[JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)
