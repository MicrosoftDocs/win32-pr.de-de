---
description: 'Weitere Informationen zu: JET_DBINFOMISC4-Struktur'
title: JET_DBINFOMISC4-Struktur
TOCTitle: JET_DBINFOMISC4 Structure
ms:assetid: 63f446bc-98b7-4a60-9575-d6b4757fb0fa
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269269(v=EXCHG.10)
ms:contentKeyID: 32765571
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
ms.openlocfilehash: 579b53a128406fd55466888248727f448950a762
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985213"
---
# <a name="jet_dbinfomisc4-structure"></a>JET_DBINFOMISC4-Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_dbinfomisc4-structure"></a>JET_DBINFOMISC4-Struktur

Die **JET_DBINFOMISC4-Struktur** enthält verschiedene Informationen zu einer Datenbank. Dies sind die Informationen, die im Datenbankheader enthalten sind.

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
      unsigned long genCommitted;
      JET_BKINFO bkinfoCopyPrev;
      JET_BKINFO bkinfoDiffPrev;
    } JET_DBINFOMISC4;
```

### <a name="members"></a>Member

**ulVersion**

Die native Version der Datenbank-Engine, die die Datenbank erstellt hat. Informationen zum Abrufen der nativen Version für die aktuelle Datenbank-Engine finden Sie unter [JetGetVersion.](./jetgetversion-function.md)

**ulUpdate**

Verfolgt inkrementelle Datenbankformatupdates nach, die abwärtskompatibel sind.


| <p>ulVersion, ulUpdate =</p> | <p>Bedeutung</p> | 
|------------------------------|----------------|
| <p>0x620,0</p> | <p>Betaformat des ursprünglichen Betriebssystems (22.4.97).</p> | 
| <p>0x620,1</p> | <p>Fügen Sie Im Katalog Spalten für die bedingte Indizierung und OLD (29.5.97) hinzu.</p> | 
| <p>0x620,2</p> | <p>Fügen Sie das Flag fLocalizedText in IDB hinzu (5.6.97).</p> | 
| <p>0x620,3</p> | <p>Fügen Sie SPLIT_BUFFER den Stammseiten der Raumstruktur hinzu (30.10.97).</p> | 
| <p>0x620,2</p> | <p>Kehren Sie die Revision zurück, damit ESE97 vorwärtskompatibel bleibt (28.1.98).</p> | 
| <p>0x620,3</p> | <p>Hinzufügen neuer markierter Spalten zum Katalog ("CallbackData" und "CallbackDependencies").</p> | 
| <p>0x620,4</p> | <p>SLV-Unterstützung: signSLV, fSLVExists im Db-Header (5.5.98).</p> | 
| <p>0x620,5</p> | <p>Neue SLV-Raumstruktur (29.5.98).</p> | 
| <p>0x620,6</p> | <p>SLV-Raumkarte (12.10.98).</p> | 
| <p>0x620,7</p> | <p>4-Byte-IDXSEG (10.12.98).</p> | 
| <p>0x620,8</p> | <p>Neues Vorlagenspaltenformat (25.1.99).</p> | 
| <p>0x620,9</p> | <p>Sortierte Vorlagenspalten (24.6.99).</p> | 
| <p>0x620,A</p> | <p>Zusammengeführte Codebasis (26.3.2003)</p> | 
| <p>0x620,B</p> | <p>Neues Prüfsummenformat (08.1.2004).</p> | 
| <p>0x620,C</p> | <p>Maximale Schlüssellänge auf 1000/2000 Byte für 4/8 KB-Seiten (15.01.2004) erhöht.</p> | 
| <p>0x620,D</p> | <p>Katalograumhinweise, space_header.v2 (15.7.2007).</p> | 
| <p>0x620, E</p> | <p>Fügen Sie dem Speicherplatz-Manager ein neues Knoten-/Erweiterungsformat hinzu, und verwenden Sie es für reservierte Speicherplatzpools (9.08.2007).</p> | 
| <p>0x620,F</p> | <p>Komprimierung für systeminterne Long-Werte (30.10.2007)</p> | 
| <p>0x620,10</p> | <p>Komprimierung für getrennte lange Werte (05.12.2007).</p> | 
| <p>0x620,11</p> | <p>Neue LV-Blockgröße für große Seiten (29.12.2007).</p> | 



**signDb**

Signatur der Datenbank (einschließlich Erstellungszeit). Diese Struktur beträgt 28 Bytes.

**dbstate**

Dies ist der Datenbankstatus.

Die folgenden Optionen sind für diesen Member verfügbar.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_dbstateJustCreated<br />1</p> | <p>Die Datenbank wurde soeben erstellt.</p> | 
| <p>JET_dbstateDirtyShutdown<br />2</p> | <p>Die Datenbank erfordert eine harte oder weiche Wiederherstellung, um verwendbar oder verschiebebar zu werden. Es sollte nicht versucht werden, Datenbanken in diesem Zustand zu verschieben.</p> | 
| <p>JET_dbstateCleanShutdown<br />3</p> | <p>Die Datenbank befindet sich in einem fehlerfreien Zustand. Die Datenbank kann ohne Protokolldateien angefügt werden.</p> | 
| <p>JET_dbstateBeingConverted<br />4</p> | <p>Die Datenbank wird aktualisiert.</p> | 
| <p>JET_dbstateForceDetach<br />5</p> | <p>Intern.</p> | 



**lgposConsistent**

NULL, wenn sich die Datenbank in einem geänderten Zustand befindet. Dies ist die Protokollposition, die verwendet wurde, als die Datenbank zuletzt in einen fehlerfreien Herunterfahrzustand gebracht wurde.

**logtimeConsistent**

NULL, wenn sich die Datenbank in einem geänderten Zustand befindet. Dies ist der Zeitpunkt, zu dem die Datenbank zuletzt in einen fehlerfreien Herunterfahrzustand gebracht wurde.

**logtimeAttach**

Der Zeitpunkt, zu dem die Datenbank zuletzt mit [JetAttachDatabase](./jetattachdatabase-function.md)angefügt wurde.

**lgposAttach**

Die Protokollposition, die beim letzten Anfügen der Datenbank mit [JetAttachDatabase](./jetattachdatabase-function.md)verwendet wurde.

**logtimeDetach**

Der Zeitpunkt, zu dem die Datenbank zuletzt mit [JetDetachDatabase](./jetdetachdatabase-function.md)getrennt wurde.

**lgposDetach**

Die Protokollposition, die beim letzten Trennen der Datenbank mit [JetDetachDatabase](./jetdetachdatabase-function.md)verwendet wurde.

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

Stellt die Windows NT-Versionsnummern dar, als die Datenbankindizes aktualisiert wurden. Wird zum Aktualisieren von Indizes verwendet.

**dwMinorVersion**

Stellt die Windows NT-Versionsnummern dar, als die Datenbankindizes aktualisiert wurden. Wird zum Aktualisieren von Indizes verwendet.

**dwBuildNumber**

Stellt die Windows NT-Versionsnummern dar, als die Datenbankindizes aktualisiert wurden. Wird zum Aktualisieren von Indizes verwendet.

**lSPNumber**

Stellt die Windows NT-Versionsnummern dar, als die Datenbankindizes aktualisiert wurden. Wird zum Aktualisieren von Indizes verwendet.

**cbPageSize**

Größe der Datenbankseite. 0 bedeutet, dass die Seitengröße 4 KB beträgt.

Dieser Wert wird nur abgerufen, wenn JET_DbInfoMisc an [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) oder [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)übergeben wurde.

**genMinRequired**

Stellt die minimale Protokollgenerierung dar, die für die Wiedergabe der Protokolle erforderlich ist. Dies wird in der Regel als Prüfpunktgenerierung verwendet.

**genMaxRequired**

Stellt die maximale Protokollgenerierung dar, die für die Wiedergabe der Protokolle erforderlich ist.

**logtimeGenMaxCreate**

Stellt das Erstellungsdatum und die Uhrzeit der genMax-Protokolldatei dar.

**ulRepairCount**

Gibt an, wie oft eine Reparatur für diese Datenbank aufgerufen wurde.

**logtimeRepair**

Stellt das Datum und die Uhrzeit der letzten Reparatur dar.

**ulRepairCountOld**

Gibt an, wie oft die Reparatur für diese Datenbank vor der letzten Defragmentierung ausgeführt wurde.

**ulECCFixSuccess**

Gibt an, wie oft ein Ein-Bit-Fehler behoben wurde und zu einer guten Seite geführt hat.

**logtimeECCFixSuccess**

Stellt das Datum und die Uhrzeit dar, zu der der letzte Ein-Bit-Fehler behoben wurde und zu einer guten Seite geführt hat.

**ulECCFixSuccessOld**

Stellt dar, wie oft ein Ein-Bit-Fehler behoben wurde und vor der letzten Reparatur zu einer guten Seite geführt hat.

**ulECCFixFail**

Gibt an, wie oft ein Ein-Bit-Fehler behoben wurde und zu einer fehlerhaften Seite geführt hat.

**logtimeECCFixFail**

Stellt das Datum und die Uhrzeit dar, zu der der letzte Ein-Bit-Fehler behoben wurde und zu einer fehlerhaften Seite geführt hat.

**ulECCFixFailOld**

Gibt an, wie oft ein Ein-Bit-Fehler behoben wurde und vor der letzten Reparatur zu einer fehlerhaften Seite geführt hat.

**ulBadChecksum**

Gibt an, wie oft ein nicht behebbarer ECC-/Prüfsummenfehler gefunden wurde.

**logtimeBadChecksum**

Stellt das Datum und die Uhrzeit dar, zu der der letzte nicht behebbare ECC-/Prüfsummenfehler gefunden wurde.

**ulBadChecksumOld**

Gibt an, wie oft vor der letzten Reparatur ein nicht behebbarer ECC-/Prüfsummenfehler gefunden wurde.

**genCommitted**

Die maximale Anzahl von Protokollgenerationen, für die ein Commit für die Datenbank ausgeführt wurde. In der Regel die aktuelle Protokollgenerierung.

**bkinfoCopyPrev**

Die letzte erfolgreiche Kopiesicherung.

**bkinfoDiffPrev**

Die letzte erfolgreiche differenzielle Sicherung. Dieser Wert wird zurückgesetzt, wenn bkinfoFullPrev festgelegt ist.

### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JET_BKINFO](./jet-bkinfo-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_LGPOS](./jet-lgpos-structure.md)  
[JET_SIGNATURE](./jet-signature-structure.md)  
[JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)  
[JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)
