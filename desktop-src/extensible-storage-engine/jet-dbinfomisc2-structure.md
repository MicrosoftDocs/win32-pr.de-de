---
description: 'Weitere Informationen finden Sie unter: JET_DBINFOMISC2 Struktur'
title: JET_DBINFOMISC2-Struktur
TOCTitle: JET_DBINFOMISC2 Structure
ms:assetid: c62e87ca-c02c-4d6f-a1e6-f80d022c6aad
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294085(v=EXCHG.10)
ms:contentKeyID: 32765700
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
ms.openlocfilehash: 1f2b42433df5a2712061c1c88ce2d0ad8afbabc3
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480496"
---
# <a name="jet_dbinfomisc2-structure"></a>JET_DBINFOMISC2-Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_dbinfomisc2-structure"></a>JET_DBINFOMISC2-Struktur

Die **JET_DBINFOMISC2-Struktur** enthält verschiedene Informationen zu einer Datenbank. Dies sind die Informationen, die im Datenbankheader enthalten sind.

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
      unsigned long genMinRequired;
      unsigned long genMaxRequired;
      JET_LOGTIME logtimeGenMaxCreate;
      unsigned long ulRepairCount;
      JET_LOGTIME logtimeRepair;
      unsigned long ulRepairCountOld;
      unsigned long ulECCFixSuccess;
      JET_LOGTIME logtimeECCFixSuccess;
      unsigned long ulECCFixSuccessOld;
      unsigned long ulECCFixFail;
      JET_LOGTIME logtimeECCFixFail;
      unsigned long ulECCFixFailOld;
      unsigned long ulBadChecksum;
      JET_LOGTIME logtimeBadChecksum;
      unsigned long ulBadChecksumOld;
    } JET_DBINFOMISC2;
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
| <p>0x620,A</p> | <p>Zusammengeführte Codebasis (26.03.2003).</p> | 
| <p>0x620,B</p> | <p>Neues Prüfsummenformat (08.1.2004).</p> | 
| <p>0x620,C</p> | <p>Die maximale Schlüssellänge wurde auf 1000/2000 Bytes für 4/8 KB Seiten (15.1.2004) erhöht.</p> | 
| <p>0x620,D</p> | <p>Katalograumhinweise, space_header.v2 (15.7.2007).</p> | 
| <p>0x620,E</p> | <p>Fügen Sie dem Space Manager ein neues Knoten-/Extentformat hinzu, und verwenden Sie es für reservierte Speicherplatzpools (9.8.2007).</p> | 
| <p>0x620,F</p> | <p>Komprimierung für systeminterne Long-Werte (30.10.2007).</p> | 
| <p>0x620,10</p> | <p>Komprimierung für getrennte Long-Werte (05.12.2007).</p> | 
| <p>0x620,11</p> | <p>Neue LV-Blockgröße für große Seiten (29.12.2007).</p> | 



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

**genMinRequired**

Stellt die minimale Protokollgenerierung dar, die zum Wiederverlegen der Protokolle erforderlich ist. Dies wird in der Regel als Prüfpunktgenerierung verwendet.

**genMaxRequired**

Stellt die maximale Protokollgenerierung dar, die zum Wiederverlegen der Protokolle erforderlich ist.

**logtimeGenMaxCreate**

Stellt das Erstellungsdatum und die Erstellungszeit der genMax-Protokolldatei dar.

**ulRepairCount**

Gibt an, wie oft eine Reparatur für diese Datenbank aufgerufen wurde.

**logtimeRepair**

Stellt das Datum und die Uhrzeit der letzten Reparatur dar.

**ulRepairCountOld**

Die Anzahl der Ausführungen der Reparatur für diese Datenbank vor der letzten Defragmentierung.

**ulECCFixSuccess**

Gibt an, wie oft ein Ein-Bit-Fehler behoben wurde und zu einer guten Seite führte.

**logtimeECCFixSuccess**

Stellt das Datum und die Uhrzeit dar, zu der der letzte Ein-Bit-Fehler behoben wurde und zu einer guten Seite führte.

**ulECCFixSuccessOld**

Gibt an, wie oft ein Ein-Bit-Fehler behoben wurde und vor der letzten Reparatur zu einer guten Seite führte.

**ulECCFixFail**

Gibt an, wie oft ein Ein-Bit-Fehler behoben wurde und zu einer fehlerhaften Seite führte.

**logtimeECCFixFail**

Stellt das Datum und die Uhrzeit dar, zu der der letzte Ein-Bit-Fehler behoben wurde und zu einer fehlerhaften Seite führte.

**ulECCFixFailOld**

Gibt an, wie oft ein Ein-Bit-Fehler behoben wurde und vor der letzten Reparatur zu einer fehlerhaften Seite führte.

**ulBadChecksum**

Gibt an, wie oft ein nicht behebter ECC-/Prüfsummenfehler gefunden wurde.

**logtimeBadChecksum**

Stellt das Datum und die Uhrzeit des letzten nicht behebtbaren ECC-/Prüfsummenfehlers dar.

**ulBadChecksumOld**

Gibt an, wie oft vor der letzten Reparatur ein nicht behebtbarer ECC-/Prüfsummenfehler gefunden wurde.

### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JET_BKINFO](./jet-bkinfo-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_LGPOS](./jet-lgpos-structure.md)  
[JET_SIGNATURE](./jet-signature-structure.md)  
[JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)  
[JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)
