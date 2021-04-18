---
description: 'Weitere Informationen finden Sie hier: Meta Parameters'
title: Meta-Parameter
TOCTitle: Meta Parameters
ms:assetid: 947e9342-7916-4e62-85e5-2d18805000c0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269346(v=EXCHG.10)
ms:contentKeyID: 32765634
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
ms.openlocfilehash: 82b5fac0cc59e9a0511344e72b3f316af9013965
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345675"
---
# <a name="meta-parameters"></a>Meta-Parameter


_**Gilt für:** Windows | Windows Server_

## <a name="meta-parameters"></a>Meta-Parameter

Dieses Thema enthält Parameter, die verwendet werden, um andere Parameter zu steuern.

JET_paramConfiguration  
129  
Dieser Parameter macht mehrere Sätze von Standardwerten für den gesamten Satz von Systemparametern verfügbar. Wenn dieser Parameter auf eine bestimmte Konfiguration festgelegt ist, werden alle Systemparameter Werte auf ihre Standardwerte für diese Konfiguration zurückgesetzt. Wenn die Konfiguration für eine bestimmte Instanz festgelegt ist, werden die globalen Systemparameter nicht auf ihre Standardwerte zurückgesetzt.

Außerdem kann der Parameter selbst andere Auswirkungen auf das Verhalten der Datenbank-Engine haben.

Zurzeit werden zwei Konfigurationen unterstützt:

  - Kleine Konfiguration (0): die Datenbank-Engine ist für die Speichernutzung optimiert.

  - Legacy Konfiguration (1): die Datenbank-Engine verfügt über die herkömmlichen Standardeinstellungen.

Bei der kleinen Konfiguration werden die Standardwerte der folgenden Systemparameter auf die angegebenen Werte geändert:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>System Parameter</p></th>
<th><p>Neuer Standardwert</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_paramMaxSessions</p></td>
<td><p>30.000</p></td>
</tr>
<tr class="even">
<td><p>JET_paramMaxOpenTables</p></td>
<td><p>2147483647</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramMaxCursors</p></td>
<td><p>2147483647</p></td>
</tr>
<tr class="even">
<td><p>JET_paramMaxVerPages</p></td>
<td><p>2147483647</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramMaxTemporaryTables</p></td>
<td><p>2147483647</p></td>
</tr>
<tr class="even">
<td><p>JET_paramLogFileSize</p></td>
<td><p>64</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramLogBuffers</p></td>
<td><p>1</p></td>
</tr>
<tr class="even">
<td><p>JET_paramDbExtensionSize</p></td>
<td><p>16</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramPageTempDBMin</p></td>
<td><p>14</p></td>
</tr>
<tr class="even">
<td><p>JET_paramCacheSizeMax</p></td>
<td><p>16</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramCheckpointDepthMax</p></td>
<td><p>65536</p></td>
</tr>
<tr class="even">
<td><p>JET_paramLRUKHistoryMax</p></td>
<td><p>10</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramOutstandingIOMax</p></td>
<td><p>16</p></td>
</tr>
<tr class="even">
<td><p>JET_paramStartFlushThreshold</p></td>
<td><p>1</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramStopFlushThreshold</p></td>
<td><p>2</p></td>
</tr>
<tr class="even">
<td><p>JET_paramNoInformationEvent</p></td>
<td><p>1</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramCacheSizeMin</p></td>
<td><p>16</p></td>
</tr>
<tr class="even">
<td><p>JET_paramPreferredVerPages</p></td>
<td><p>2147483647</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramLogFileCreateAsynch</p></td>
<td><p>0</p></td>
</tr>
<tr class="even">
<td><p>JET_paramGlobalMinVerPages</p></td>
<td><p>1</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramPageHintCacheSize</p></td>
<td><p>32</p></td>
</tr>
<tr class="even">
<td><p>JET_paramDisablePerfmon</p></td>
<td><p>1</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramEnableFileCache</p></td>
<td><p>1</p></td>
</tr>
<tr class="even">
<td><p>JET_paramEnableViewCache</p></td>
<td><p>1</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramVerPageSize</p></td>
<td><p>1024</p></td>
</tr>
<tr class="even">
<td><p>JET_paramEnableAdvanced</p></td>
<td><p>0</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramCheckpointIOMax</p></td>
<td><p>8</p></td>
</tr>
</tbody>
</table>


Die kleine Konfiguration hat auch eine Reihe weiterer Auswirkungen auf die Datenbank-Engine, einschließlich:

  - Alle durch Systemparameter verwalteten Ressourcen werden nach Bedarf aus dem Heap zugeordnet.

  - Andere interne Ressourcen, die von der Datenbank-Engine verwendet werden, werden zentral herunterskaliert.

  - Verschiedene Wartungsaktivitäten werden wieder herunterskaliert, um Hintergrund Thread Aktivitäten zu vermeiden.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>1 (Legacy)</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>0 – 1</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Instanz</p></td>
</tr>
<tr class="odd">
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Hat Auswirkungen auf das physische Layout:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Beeinträchtigt die Zuverlässigkeit:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Beeinträchtigt die Leistung:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Betrifft Ressourcen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Ab Windows Server 2008 und Windows Vista</p></td>
</tr>
</tbody>
</table>


JET_paramEnableAdvanced  
130  
Dieser Parameter wird verwendet, um zu steuern, wann die Datenbank-Engine Änderungen an einer Teilmenge der Systemparameter akzeptiert oder ablehnt. Dieser Parameter wird zusammen mit JET_paramConfiguration verwendet, um zu verhindern, dass einige Systemparameter aus den Standardeinstellungen der ausgewählten Konfiguration entfernt werden.

Die folgenden Systemparameter werden vor der Festlegung geschützt, wenn dieser Parameter auf "false" festgelegt ist:

  - JET_paramMaxSessionsfon

  - JET_paramMaxOpenTables

  - JET_paramPreferredMaxOpenTables

  - JET_paramMaxCursors

  - JET_paramMaxVerPages

  - JET_paramMaxTemporaryTables

  - JET_paramLogBuffers

  - JET_paramWaitLogFlush

  - JET_paramLogCheckpointPeriod

  - JET_paramLogWaitingUserMax

  - JET_paramDbExtensionSize

  - JET_paramPageTempDBMin

  - JET_paramPageFragment

  - JET_paramBatchIOBufferMax

  - JET_paramCacheSizeMax

  - JET_paramLRUKCorrInterval

  - JET_paramLRUKHistoryMax

  - JET_paramLRUKPolicy

  - JET_paramLRUKTimeout

  - JET_paramLRUKTrxCorrInterval

  - JET_paramOutstandingIOMax

  - JET_paramStartFlushThreshold

  - JET_paramStopFlushThreshold

  - JET_paramCacheSize

  - JET_paramCacheSizeMin

  - JET_paramPreferredVerPages

  - JET_paramBackupChunkSize

  - JET_paramBackupOutstandingReads

  - JET_paramLogFileCreateAsynch

  - JET_paramRecordUpgradeDirtyLevel

  - JET_paramGlobalMinVerPages

  - JET_paramPageHintCacheSize

  - JET_paramVersionStoreTaskQueueMax

  - JET_paramDBAPageAvailMin

  - JET_paramMaxRandomIOSize

  - JET_paramCachedClosedTables

  - JET_paramEnableFileCache

  - JET_paramEnableViewCache

  - JET_paramVerPageSize

  - JET_paramCheckpointIOMax

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>Richtig</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>False, True</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Instanz</p></td>
</tr>
<tr class="odd">
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Hat Auswirkungen auf das physische Layout:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Beeinträchtigt die Zuverlässigkeit:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Beeinträchtigt die Leistung:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Betrifft Ressourcen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Ab Windows Server 2008 und Windows Vista</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>In "ESENT. h" deklariert.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[Jetkreateingestance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)
