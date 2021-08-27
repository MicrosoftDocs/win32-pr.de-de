---
description: Weitere Informationen finden Sie unter JetInit3-Funktion.
title: JetInit3-Funktion
TOCTitle: JetInit3 Function
ms:assetid: 752589b6-1b8f-4b6f-a14a-00f4b1405db5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269296(v=EXCHG.10)
ms:contentKeyID: 32765588
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetInit3
- JetInit3A
- JetInit3W
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0a0c73343550768a9ccd061c702fae89d562d095
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477906"
---
# <a name="jetinit3-function"></a>JetInit3-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetinit3-function"></a>JetInit3-Funktion

Die **JetInit3-Funktion** versetzt die Datenbank-Engine in einen Zustand, in dem sie die Anwendungsnutzung von Datenbankdateien unterstützen kann. Die Engine muss bereits ordnungsgemäß für die Initialisierung konfiguriert sein, die Sie mithilfe der [JetSetSystemParameter-Funktion](./jetsetsystemparameter-function.md) erreichen. Beachten Sie, dass die Datenbankabsturzwiederherstellung automatisch im Rahmen des Initialisierungsprozesses erfolgt.

**Windows Vista:****JetInit3** wird in Windows Vista eingeführt.  

```cpp
    JET_ERR JET_API JetInit3(
      __in_out_opt  JET_INSTANCE* pinstance,
      __in_opt      JET_RSTINFO* prstInfo,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*Pinstance*

Die -Instanz, die Sie für einen bestimmten Aufruf verwenden. Die Verwendung dieses Parameters hängt vom Betriebsmodus der Engine ab. Wenn die Engine im Legacymodus (Windows 2000-Kompatibilitätsmodus) ausgeführt wird, in dem nur eine Instanz unterstützt wird, können Sie diesen Parameter entweder auf **NULL** oder auf einen gültigen Ausgabepuffer mit **NULL** oder JET_instanceNil festlegen, der das globale Instanzhand handle zurückgibt, das als Nebeneffekt der Initialisierung erstellt wurde. Dieses Instanzhand handle kann dann an jede andere API übergeben werden, die eine -Instanz verwendet. Wenn die Engine im Modus mit mehreren Instanzen ausgeführt wird, müssen Sie diesen Parameter auf einen gültigen Eingabepuffer festlegen, der das Instanzhandl enthält, das von der [initialisierten JetCreateInstance-Funktion](./jetcreateinstance-function.md) zurückgegeben wird.

*prstInfo*

Zusätzliche Wiederherstellungsparameter, die zum Neubestimmen von Datenbanken während der Wiederherstellung, zum Festlegen der Position, an der die Wiederherstellung anhalten wird, oder zum Bestimmen des aktuellen Wiederherstellungsstatus verwendet werden.

*grbit*

Eine Gruppe von Bits, die null oder mehr der in der folgenden Tabelle aufgeführten und definierten Optionen angibt.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitReplayReplicatedLogFiles</p> | <p>Dieser Wert ist für die zukünftige Verwendung reserviert.</p> | 
| <p>JET_bitCreateSFSVolumeIfNotExist</p> | <p>Dieser Wert ist für die zukünftige Verwendung reserviert.</p> | 
| <p>JET_bitReplayIgnoreMissingDB</p> | <p>Mit diesem Wert kann der Benutzer die Wiederherstellung für eine Gruppe von Protokolldateien ausführen, auch wenn die Datenbanken nicht mehr an den Protokolldateisatz angefügt wurden.</p> | 
| <p>JET_bitRecoveryWithoutUndo</p> | <p>Dieser Wert ermöglicht es dem Benutzer, die Wiederherstellung durchzuführen, jedoch nur bis zur Phase Rückgängig (und nicht einschließlich). Mit diesem Wert können zusätzliche Transaktionsprotokolle kopiert und angewendet werden.</p> | 
| <p>JET_bitTruncateLogsAfterRecovery</p> | <p>Dieser Wert bewirkt, dass Protokolldateien während einer erfolgreichen weichen Wiederherstellung abgeschnitten werden.</p> | 
| <p>JET_bitReplayMissingMapEntryDB</p> | <p>Dieser Wert bewirkt, dass ein fehlender Datenbankzuordnungseintrag standardmäßig auf denselben Speicherort festgelegt wird.</p> | 
| <p>JET_bitReplayIgnoreLostLogs</p> | <p>Dieser Wert bewirkt, dass Protokolle, die am Ende des Protokolldatenstroms verloren gehen, während einer Wiederherstellung ignoriert werden.</p><p><strong>Windows 7:JET_bitReplayIgnoreLostLogs</strong> wird in Windows 7 eingeführt.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR-Datentyp](./jet-err.md) mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern (Extensible Storage Engine) finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


#### <a name="remarks"></a>Hinweise

Eine Instanz muss mit einem Aufruf der **JetInit3-Funktion** initialisiert werden, bevor sie von einer anderen Funktion als der [JetSetSystemParameter-Funktion verwendet werden](./jetsetsystemparameter-function.md) kann.

Eine Instanz wird durch einen Aufruf der [JetTerm-Funktion](./jetterm-function.md) zerstört, auch wenn diese Instanz nie mithilfe der [JetInit-Funktion initialisiert](./jetinit-function.md) wurde. Eine -Instanz ist die Einheit der Wiederherstellbarkeit für die Datenbank-Engine. Sie steuert den Lebenszyklus aller Dateien, die zum Schutz der Integrität der Daten in einer Gruppe von Datenbankdateien verwendet werden. Zu diesen Dateien gehören die Prüfpunktdatei und die Transaktionsprotokolldateien. Beachten [Sie, dass JetTerm](./jetterm-function.md) nicht aufgerufen werden sollte, wenn die **JetInit3-Funktion** fehlschlägt. JetTerm [sollte](./jetterm-function.md) jedoch weiterhin für alle instanzen aufgerufen werden, die von **JetCreateInstance2** erstellt wurden, wenn **JetInit3** nie aufgerufen wurde oder **wenn JetInit3** erfolgreich ist.

Wenn die Wiederherstellung für eine Gruppe von Protokollen ausgeführt wird, für die nicht alle zugehörigen Datenbanken vorhanden sind (wodurch unter normalen Umständen der Fehler JET_errAttachedDatabaseMismatch zurückgegeben wird) und der Client möchte, dass die Wiederherstellung trotz der fehlenden Datenbanken fortgesetzt wird, wird der JET_bitReplayIgnoreMissingDB-Fehler verwendet, um die Wiederherstellung für die verfügbaren Datenbanken fortzufahren.

Da die Absturzwiederherstellung in der Regel nicht auf demselben Computer (und mit der gleichen Konfiguration) wie zum Zeitpunkt des Absturzes erfolgt, ändert eine Datenbank den Speicherort in der Regel nicht. In bestimmten Szenarien, z. B. beim Verschieben von Dateien auf einen anderen Computer oder beim Wiederherstellen der Momentaufnahmesicherung an verschiedenen Speicherorten, ist dies nicht mehr der Fall. Mit **der JetInit3-Funktion** können Sie eine [](./jet-rstinfo-structure.md) Zuordnung (mithilfe der JET_RSTINFO- und [JET_RSTMAP-Strukturen)](./jet-rstmap-structure.md) zwischen dem alten und dem neuen Speicherort der Datenbank angeben. Tatsächlich benötigen Sie nur den neuen Speicherort, solange die Datenbankdateien an diesem Speicherort vorhanden sind. Sobald Sie die Speicherorte der wiederhergestellten Datenbanken kennen, wird die Datenbanksignatur verwendet, um die Datenbank während des Wiederherstellungsprozesses zu identifizieren. Sie benötigen den ursprünglichen Datenbankspeicherort nur, wenn Sie eine Datenbank neu erstellen müssen. In diesem Fall ist die Signatur bekannt.

Wenn Sie eine Wiederherstellung nach einem Rückgängig-Vorgang beenden müssen, können Sie außerdem eine bestimmte Protokollposition angeben, an der die Wiederherstellung stoppt. Beachten Sie, dass dies die Möglichkeit umfasst, am Ende einer bestimmten Protokollgenerierung anzuhalten, wenn die angegebene Position Teil der Generierung, aber über das Ende des eigentlichen Protokolls liegt.

Weitere Informationen finden Sie im Abschnitt "Hinweise" des [JetInit-Themas.](./jetinit-function.md)

#### <a name="requirements"></a>Anforderungen


| | | <p>Client</p> | <p>Erfordert Windows Vista.</p> | | <p>Server</p> | <p>Erfordert Windows Server 2008.</p> | | <p>Header</p> | <p>Wird in Esent.h deklariert.</p> | | <p>Bibliothek</p> | <p>Verwendet ESENT.lib.</p> | | <p>DLL</p> | <p>Erfordert ESENT.dll.</p> | | <p>Unicode</p> | <p>Wird als <strong>JetInit3W</strong> (Unicode) und <strong>JetInit3A</strong> (ANSI) implementiert.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[Erweiterbare Storage-Engine-Dateien](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_RSTINFO](./jet-rstinfo-structure.md)  
[JET_RSTMAP](./jet-rstmap-structure.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetInit2](./jetinit2-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Ressourcenparameter](./resource-parameters.md)
