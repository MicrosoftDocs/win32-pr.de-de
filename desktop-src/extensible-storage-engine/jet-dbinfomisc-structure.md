---
description: 'Weitere Informationen finden Sie hier: JET_DBINFOMISC Struktur'
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
ms.openlocfilehash: 649e16e956e5dcd272e6201f779cdddd352a7bef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525052"
---
# <a name="jet_dbinfomisc-structure"></a>JET_DBINFOMISC-Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_dbinfomisc-structure"></a>JET_DBINFOMISC-Struktur

Die **JET_DBINFOMISC** -Struktur enthält verschiedene Informationen zu einer-Datenbank. Dies sind die Informationen, die im Daten Bank Header enthalten sind.

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

**ulversion**

Die native Version der Datenbank-Engine, die die Datenbank erstellt hat. Informationen zum Abrufen der systemeigenen Version für die aktuelle Datenbank-Engine finden Sie unter [jetgetversion](./jetgetversion-function.md) .

**ulupdate**

Verfolgt inkrementelle Datenbankformat Updates, die abwärts kompatibel sind.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>ulversion, ulupdate =</p></th>
<th><p>Bedeutung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>0x620, 0</p></td>
<td><p>Ursprüngliches Betriebssystem-Beta Format (4/22/97).</p></td>
</tr>
<tr class="even">
<td><p>0x620, 1</p></td>
<td><p>Fügen Sie im Katalog Spalten für die bedingte Indizierung und die alte (5/29/97) hinzu.</p></td>
</tr>
<tr class="odd">
<td><p>0x620, 2</p></td>
<td><p>Fügen Sie das flocalizedtext-Flag in IDB (6/5/97) hinzu.</p></td>
</tr>
<tr class="even">
<td><p>0x620, 3</p></td>
<td><p>Fügen Sie den Stamm Seiten der Speicherplatz Struktur SPLIT_BUFFER hinzu (10/30/97).</p></td>
</tr>
<tr class="odd">
<td><p>0x620, 2</p></td>
<td><p>Revision wiederherstellen, damit ESE97 vorwärts kompatibel bleibt (1/28/98).</p></td>
</tr>
<tr class="even">
<td><p>0x620, 3</p></td>
<td><p>Fügen Sie dem Katalog neue markierte Spalten hinzu ( &quot; callBackData &quot; und &quot; callbackdependen) &quot; .</p></td>
</tr>
<tr class="odd">
<td><p>0x620, 4</p></td>
<td><p>SLV-Unterstützung: signslv, fslvvorhanden in DB-Header (5/5/98).</p></td>
</tr>
<tr class="even">
<td><p>0x620, 5</p></td>
<td><p>Neue SLV-Raumstruktur (5/29/98).</p></td>
</tr>
<tr class="odd">
<td><p>0x620, 6</p></td>
<td><p>SLV-Speicherplatz Zuordnung (10/12/98).</p></td>
</tr>
<tr class="even">
<td><p>0x620, 7</p></td>
<td><p>4-Byte-idxsekunden (12/10/98).</p></td>
</tr>
<tr class="odd">
<td><p>0x620, 8</p></td>
<td><p>Neues Vorlagen Spalten Format (1/25/99).</p></td>
</tr>
<tr class="even">
<td><p>0x620, 9</p></td>
<td><p>Sortierte Vorlagen Spalten (6/24/99).</p></td>
</tr>
<tr class="odd">
<td><p>0x623, 0</p></td>
<td><p>Neuer Speicherplatz-Manager (5/15/99).</p></td>
</tr>
</tbody>
</table>


**signdb**

Signatur der Datenbank (einschließlich Erstellungszeit). Diese Struktur hat 28 bytes.

**dbstate**

Dies ist der Daten Bank Status.

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
<td><p>Für die Datenbank muss eine harte oder weiche Wiederherstellung ausgeführt werden, damit Sie verwendet werden kann. Es sollte nicht versucht werden, Datenbanken in diesem Zustand zu verschieben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_dbstateCleanShutdown<br />
3</p></td>
<td><p>Die Datenbank befindet sich in einem sauberen Zustand. Die Datenbank kann ohne Protokolldateien angefügt werden.</p></td>
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


**lgposkonsistent**

NULL, wenn sich die Datenbank in einem fehlerhaften Zustand befindet. Dies ist die Protokoll Position, die verwendet wurde, als die Datenbank zuletzt in den Zustand "fehlerfreies Herunterfahren" gebracht wurde.

**logtimekonsistent**

NULL, wenn sich die Datenbank in einem fehlerhaften Zustand befindet. Dies ist der Zeitpunkt, zu dem die Datenbank zuletzt in den Zustand "sauberes Herunterfahren" versetzt wurde.

**logtimeattach**

Der Zeitpunkt, zu dem die Datenbank zuletzt an [jetattachdatabase](./jetattachdatabase-function.md)angefügt wurde.

**lgposattach**

Die Protokoll Position, die beim letzten Anfügen der Datenbank mit [jetattachdatabase](./jetattachdatabase-function.md)verwendet wurde.

**logtimedetach**

Der Zeitpunkt, zu dem die Datenbank zuletzt mit [jetdetachdatabase](./jetdetachdatabase-function.md)getrennt wurde.

**lgposdetach**

Die Protokoll Position, die beim letzten Trennen der Datenbank mit [jetdetachdatabase](./jetdetachdatabase-function.md)verwendet wurde.

**signlog**

Unterstützt die ESE-Infrastruktur und kann nicht in Ihrem Code verwendet werden.

**bkinfofullprev**

Unterstützt die ESE-Infrastruktur und kann nicht in Ihrem Code verwendet werden.

**bkinfoincprev**

Unterstützt die ESE-Infrastruktur und kann nicht in Ihrem Code verwendet werden.

**bkinfofullcur**

Unterstützt die ESE-Infrastruktur und kann nicht in Ihrem Code verwendet werden.

**' f ' wingdeaktiviert**

Unterstützt die ESE-Infrastruktur und kann nicht in Ihrem Code verwendet werden.

**FUpgrade DB**

Unterstützt die ESE-Infrastruktur und kann nicht in Ihrem Code verwendet werden.

**dwMajorVersion**

Stellt die Windows NT-Versionsnummern beim Aktualisieren der Datenbankindizes dar. Wird zum Aktualisieren von Indizes verwendet.

**dwMinorVersion**

Stellt die Windows NT-Versionsnummern beim Aktualisieren der Datenbankindizes dar. Wird zum Aktualisieren von Indizes verwendet.

**dwBuildNumber**

Stellt die Windows NT-Versionsnummern beim Aktualisieren der Datenbankindizes dar. Wird zum Aktualisieren von Indizes verwendet.

**lspnumber**

Stellt die Windows NT-Versionsnummern beim Aktualisieren der Datenbankindizes dar. Wird zum Aktualisieren von Indizes verwendet.

**cbpagesize**

Größe der Datenbankseite. 0 bedeutet, dass die Seitengröße 4 KB beträgt.

Dieser Wert wird nur abgerufen, wenn JET_DbInfoMisc an [jetgetdatabaseingefo](./jetgetdatabaseinfo-function.md) oder [jetgetdatabasefilinput Info](./jetgetdatabasefileinfo-function.md)übermittelt wurde.

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

[JET_BKINFO](./jet-bkinfo-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_LGPOS](./jet-lgpos-structure.md)  
[JET_SIGNATURE](./jet-signature-structure.md)  
[Jetgetdatabaseingefo](./jetgetdatabaseinfo-function.md)  
[Jetgetdatabasefileingefo](./jetgetdatabasefileinfo-function.md)
