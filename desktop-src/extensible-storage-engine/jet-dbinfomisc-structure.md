---
description: 'Weitere Informationen zu: JET_DBINFOMISC-Struktur'
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
ms.openlocfilehash: 6c7684fe69cff252d75ea2cceb0872044e8a011b39e88375d6eb576cb1b5360e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118486333"
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

Verfolgt inkrementelle Datenbankformatupdates nach, die abwärtskompatibel sind.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>ulVersion, ulUpdate =</p></th>
<th><p>Bedeutung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>0x620,0</p></td>
<td><p>Betaformat des ursprünglichen Betriebssystems (22.4.97).</p></td>
</tr>
<tr class="even">
<td><p>0x620,1</p></td>
<td><p>Fügen Sie Im Katalog Spalten für die bedingte Indizierung und OLD (29.5.97) hinzu.</p></td>
</tr>
<tr class="odd">
<td><p>0x620,2</p></td>
<td><p>Fügen Sie das Flag fLocalizedText in IDB hinzu (5.6.97).</p></td>
</tr>
<tr class="even">
<td><p>0x620,3</p></td>
<td><p>Fügen Sie SPLIT_BUFFER zu den Stammseiten der Raumstruktur hinzu (30.10.97).</p></td>
</tr>
<tr class="odd">
<td><p>0x620,2</p></td>
<td><p>Kehren Sie die Revision zurück, damit ESE97 vorwärtskompatibel bleibt (28.1.98).</p></td>
</tr>
<tr class="even">
<td><p>0x620,3</p></td>
<td><p>Hinzufügen neuer markierter Spalten zum Katalog ( &quot; CallbackData &quot; und &quot; CallbackDependencies &quot; ).</p></td>
</tr>
<tr class="odd">
<td><p>0x620,4</p></td>
<td><p>SLV-Unterstützung: signSLV, fSLVExists im Db-Header (5.5.98).</p></td>
</tr>
<tr class="even">
<td><p>0x620,5</p></td>
<td><p>Neue SLV-Raumstruktur (29.5.98).</p></td>
</tr>
<tr class="odd">
<td><p>0x620,6</p></td>
<td><p>SLV-Raumkarte (12.10.98).</p></td>
</tr>
<tr class="even">
<td><p>0x620,7</p></td>
<td><p>4-Byte-IDXSEG (10.12.98).</p></td>
</tr>
<tr class="odd">
<td><p>0x620,8</p></td>
<td><p>Neues Vorlagenspaltenformat (25.1.99).</p></td>
</tr>
<tr class="even">
<td><p>0x620,9</p></td>
<td><p>Sortierte Vorlagenspalten (24.6.99).</p></td>
</tr>
<tr class="odd">
<td><p>0x623,0</p></td>
<td><p>Neuer Space Manager (15.5.99)</p></td>
</tr>
</tbody>
</table>


**signDb**

Signatur der Datenbank (einschließlich Erstellungszeit). Diese Struktur beträgt 28 Bytes.

**dbstate**

Dies ist der Datenbankstatus.

Die folgenden Optionen sind für diesen Member verfügbar.

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
<td><p>JET_dbstateJustCreated<br />
1</p></td>
<td><p>Die Datenbank wurde soeben erstellt.</p></td>
</tr>
<tr class="even">
<td><p>JET_dbstateDirtyShutdown<br />
2</p></td>
<td><p>Die Datenbank erfordert eine harte oder weiche Wiederherstellung, um verwendbar oder verschiebebar zu werden. Es sollte nicht versucht werden, Datenbanken in diesem Zustand zu verschieben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_dbstateCleanShutdown<br />
3</p></td>
<td><p>Die Datenbank befindet sich in einem fehlerfreien Zustand. Die Datenbank kann ohne Protokolldateien angefügt werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_dbstateBeingConverted<br />
4</p></td>
<td><p>Die Datenbank wird aktualisiert.</p></td>
</tr>
<tr class="odd">
<td><p>JET_dbstateForceDetach<br />
5</p></td>
<td><p>Intern.</p></td>
</tr>
</tbody>
</table>


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

[JET_BKINFO](./jet-bkinfo-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_LGPOS](./jet-lgpos-structure.md)  
[JET_SIGNATURE](./jet-signature-structure.md)  
[JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)  
[JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)
