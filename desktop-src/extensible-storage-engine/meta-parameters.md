---
description: Weitere Informationen finden Sie unter Metaparameter.
title: Metaparameter
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
ms.openlocfilehash: 2f821d3aea8055f6c1344ed9d5107417adbaf604
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985513"
---
# <a name="meta-parameters"></a>Metaparameter


_**Gilt für:** Windows | Windows Server_

## <a name="meta-parameters"></a>Metaparameter

Dieses Thema enthält Parameter, die zum Steuern anderer Parameter verwendet werden.

JET_paramConfiguration  
129  
Dieser Parameter macht mehrere Sätze von Standardwerten für den gesamten Satz von Systemparametern verfügbar. Wenn dieser Parameter auf eine bestimmte Konfiguration festgelegt ist, werden alle Systemparameterwerte auf ihre Standardwerte für diese Konfiguration zurückgesetzt. Wenn die Konfiguration für eine bestimmte Instanz festgelegt ist, werden globale Systemparameter nicht auf ihre Standardwerte zurückgesetzt.

Darüber hinaus kann der Parameter selbst andere Auswirkungen auf das Verhalten der Datenbank-Engine haben.

Derzeit werden zwei Konfigurationen unterstützt:

  - Kleine Konfiguration (0): Die Datenbank-Engine ist für die Speichernutzung optimiert.

  - Legacykonfiguration (1): Die Datenbank-Engine hat ihre herkömmlichen Standardwerte.

Small Configuration ändert die Standardwerte der folgenden Systemparameter in die angegebenen Werte:


| <p>Systemparameter</p> | <p>Neuer Standardwert</p> | 
|-------------------------|--------------------------|
| <p>JET_paramMaxSessions</p> | <p>30.000</p> | 
| <p>JET_paramMaxOpenTables</p> | <p>2147483647</p> | 
| <p>JET_paramMaxCursors</p> | <p>2147483647</p> | 
| <p>JET_paramMaxVerPages</p> | <p>2147483647</p> | 
| <p>JET_paramMaxTemporaryTables</p> | <p>2147483647</p> | 
| <p>JET_paramLogFileSize</p> | <p>64</p> | 
| <p>JET_paramLogBuffers</p> | <p>1</p> | 
| <p>JET_paramDbExtensionSize</p> | <p>16</p> | 
| <p>JET_paramPageTempDBMin</p> | <p>14</p> | 
| <p>JET_paramCacheSizeMax</p> | <p>16</p> | 
| <p>JET_paramCheckpointDepthMax</p> | <p>65536</p> | 
| <p>JET_paramLRUKHistoryMax</p> | <p>10</p> | 
| <p>JET_paramOutstandingIOMax</p> | <p>16</p> | 
| <p>JET_paramStartFlushThreshold</p> | <p>1</p> | 
| <p>JET_paramStopFlushThreshold</p> | <p>2</p> | 
| <p>JET_paramNoInformationEvent</p> | <p>1</p> | 
| <p>JET_paramCacheSizeMin</p> | <p>16</p> | 
| <p>JET_paramPreferredVerPages</p> | <p>2147483647</p> | 
| <p>JET_paramLogFileCreateAsynch</p> | <p>0</p> | 
| <p>JET_paramGlobalMinVerPages</p> | <p>1</p> | 
| <p>JET_paramPageHintCacheSize</p> | <p>32</p> | 
| <p>JET_paramDisablePerfmon</p> | <p>1</p> | 
| <p>JET_paramEnableFileCache</p> | <p>1</p> | 
| <p>JET_paramEnableViewCache</p> | <p>1</p> | 
| <p>JET_paramVerPageSize</p> | <p>1024</p> | 
| <p>JET_paramEnableAdvanced</p> | <p>0</p> | 
| <p>JET_paramCheckpointIOMax</p> | <p>8</p> | 



Small Configuration hat auch mehrere andere Auswirkungen auf die Datenbank-Engine, z. B.:

  - Alle von Systemparametern verwalteten Ressourcen werden nach Bedarf aus dem Heap zugeordnet.

  - Andere interne Ressourcen, die von der Datenbank-Engine verwendet werden, werden in der Größe herunterskaliert.

  - Verschiedene Wartungsaktivitäten werden zurückskaliert, um Hintergrundthreadaktivitäten zu vermeiden.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>1 (Legacy)</p> | 
| <p>Typ:</p> | <p>Integer</p> | 
| <p>Gültiger Bereich:</p> | <p>0 – 1</p> | 
| <p>Umfang:</p> | <p>Instanz</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>No</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>No</p> | 
| <p>Beeinträchtigt die Leistung:</p> | <p>Yes</p> | 
| <p>Betrifft Ressourcen:</p> | <p>Yes</p> | 
| <p>Verfügbarkeit:</p> | <p>Ab Windows Server 2008 und Windows Vista</p> | 



JET_paramEnableAdvanced  
130  
Dieser Parameter wird verwendet, um zu steuern, wann die Datenbank-Engine Änderungen an einer Teilmenge der Systemparameter akzeptiert oder zurückgibt. Dieser Parameter wird in Verbindung mit JET_paramConfiguration verwendet, um zu verhindern, dass einige Systemparameter von den Standardeinstellungen der ausgewählten Konfiguration entfernt werden.

Die folgenden Systemparameter werden vor dem Festlegen geschützt, wenn dieser Parameter auf False festgelegt ist:

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


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>Richtig</p> | 
| <p>Typ:</p> | <p>Boolean</p> | 
| <p>Gültiger Bereich:</p> | <p>False, True</p> | 
| <p>Umfang:</p> | <p>Instanz</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Yes</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>No</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>No</p> | 
| <p>Beeinträchtigt die Leistung:</p> | <p>No</p> | 
| <p>Betrifft Ressourcen:</p> | <p>No</p> | 
| <p>Verfügbarkeit:</p> | <p>Ab Windows Server 2008 und Windows Vista</p> | 



### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)
