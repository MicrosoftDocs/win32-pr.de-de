---
description: 'Weitere Informationen zu: JetInit2-Funktion'
title: JetInit2-Funktion
TOCTitle: JetInit2 Function
ms:assetid: b5541429-6ce6-457b-88cf-673d267f6209
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294065(v=EXCHG.10)
ms:contentKeyID: 32765680
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetInit2
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7874c475dc18beb5d7f6849b9f628ea06cbc32a3
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470455"
---
# <a name="jetinit2-function"></a>JetInit2-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetinit2-function"></a>JetInit2-Funktion

Die **JetInit2-Funktion** versetzt die Datenbank-Engine in einen Zustand, in dem sie die Anwendungsverwendung von Datenbankdateien unterstützen kann. Die Engine muss bereits ordnungsgemäß für die Initialisierung mit [JetSetSystemParameter](./jetsetsystemparameter-function.md)konfiguriert sein. Die Datenbankabsturzwiederherstellung wird automatisch als Teil des Initialisierungsprozesses ausgeführt.

**Windows XP:****JetInit2** wird in Windows XP eingeführt.  

Diese Funktion ist veraltet. Verwenden Sie stattdessen [JetInit3.](./jetinit3-function.md)

```cpp
JET_ERR JET_API JetInit2(
  __in_out_opt  JET_INSTANCE* pinstance,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a>Parameter

*Pinstance*

Die -Instanz, die für diesen Aufruf verwendet werden soll.

Für Windows 2000 wird dieser Parameter ignoriert und sollte immer NULL sein.

Für Windows XP und höhere Versionen hängt die Verwendung dieses Parameters vom Betriebsmodus der Engine ab. Wenn die Engine im Legacymodus (Windows 2000-Kompatibilitätsmodus) ausgeführt wird, in dem nur eine Instanz unterstützt wird, kann dieser Parameter entweder NULL sein oder auf einen gültigen Ausgabepuffer mit NULL oder JET_instanceNil festgelegt werden, der das globale Instanzhandle zurückgibt, das als Nebeneffekt der Initialisierung erstellt wurde. Dieses Instanzhandle kann dann an jede andere API übergeben werden, die eine -Instanz annimmt. Wenn die Engine im Modus mit mehreren Instanzen ausgeführt wird, muss dieser Parameter auf einen gültigen Eingabepuffer festgelegt werden, der das Instanzhandle enthält, das von der initialisierten [JetCreateInstance](./jetcreateinstance-function.md) zurückgegeben wird.

*grbit*

Eine Gruppe von Bits, die null oder mehr der folgenden Optionen angibt.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitReplayReplicatedLogFiles</p> | <p>Für die zukünftige Verwendung reserviert.</p> | 
| <p>JET_bitCreateSFSVolumeIfNotExist</p> | <p>Für die zukünftige Verwendung reserviert.</p> | 
| <p>JET_bitReplayIgnoreMissingDB</p> | <p>Mit dieser Option kann der Benutzer die Wiederherstellung für einen Satz von Protokolldateien ausführen, ohne dass alle Datenbanken vorhanden sind, die an einem Punkt des Protokollsatzes angefügt wurden.</p> | 
| <p>JET_bitRecoveryWithoutUndo</p> | <p>Führen Sie die Wiederherstellung durch, aber halten Sie in der Rückgängig-Phase an. Dadurch können zusätzliche Transaktionsprotokolle kopiert und angewendet werden.</p> | 
| <p>JET_bitTruncateLogsAfterRecovery</p> | <p>Kürzen Sie protokolldateien bei erfolgreicher soft recovery ab.</p> | 
| <p>JET_bitReplayMissingMapEntryDB</p> | <p>Fehlender Datenbankzuordnungseintrag wird standardmäßig an demselben Speicherort verwendet.</p> | 
| <p>JET_bitReplayIgnoreLostLogs</p> | <p>Ignorieren Sie Protokolle, die am Ende des Protokolldatenstroms verloren gegangen sind.</p><p><strong>Windows 7:JET_bitReplayIgnoreLostLogs</strong> wird in Windows 7 eingeführt.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


#### <a name="remarks"></a>Hinweise

Eine -Instanz muss mit einem Aufruf von **JetInit2** initialisiert werden, bevor sie von anderen Instanzen als [JetSetSystemParameter](./jetsetsystemparameter-function.md)verwendet werden kann.

Eine -Instanz wird durch einen Aufruf der [JetTerm-Funktion](./jetterm-function.md) zerstört, auch wenn diese Instanz nie mit [JetInit](./jetinit-function.md)initialisiert wurde. Eine -Instanz ist die Einheit der Wiederherstellbarkeit für die Datenbank-Engine. Sie steuert den Lebenszyklus aller Dateien, die zum Schutz der Integrität der Daten in einem Satz von Datenbankdateien verwendet werden. Zu diesen Dateien gehören die Prüfpunktdatei und die Transaktionsprotokolldateien.

Wenn die Wiederherstellung für eine Reihe von Protokollen ausgeführt wird, für die nicht alle Datenbanken vorhanden sind (wodurch der Fehler unter normalen Umständen JET_errAttachedDatabaseMismatch zurückgegeben wird) und der Client die Wiederherstellung trotz fehlender Datenbanken fortsetzen möchte, wird die JET_ bitReplayIgnoreMissingDB verwendet, um die Wiederherstellung für die verfügbaren Datenbanken fortzusetzen.

Weitere Informationen finden Sie im Abschnitt "Hinweise" in [JetInit.](./jetinit-function.md)

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista oder Windows XP.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008 oder Windows Server 2003.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[Erweiterbare Storage-Engine-Dateien](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetInit3](./jetinit3-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Ressourcenparameter](./resource-parameters.md)
