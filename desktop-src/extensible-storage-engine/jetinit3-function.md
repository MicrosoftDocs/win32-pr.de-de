---
description: 'Weitere Informationen finden Sie hier: JetInit3-Funktion'
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
ms.openlocfilehash: c96171920b7538e71e822eaf0879e476fb2fd31e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350419"
---
# <a name="jetinit3-function"></a>JetInit3-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetinit3-function"></a>JetInit3-Funktion

Die **JetInit3** -Funktion versetzt die Datenbank-Engine in einen Zustand, in dem Sie die Anwendungs Verwendung von Datenbankdateien unterstützen kann. Die Engine muss bereits ordnungsgemäß für die Initialisierung konfiguriert sein, die Sie mithilfe der [jetsetsystemparameter](./jetsetsystemparameter-function.md) -Funktion ausführen. Beachten Sie, dass die Wiederherstellung von Daten Bank abstürzen automatisch als Teil des Initialisierungs Prozesses erfolgt.

**Windows Vista:**  **JetInit3** wird in Windows Vista eingeführt.

```cpp
    JET_ERR JET_API JetInit3(
      __in_out_opt  JET_INSTANCE* pinstance,
      __in_opt      JET_RSTINFO* prstInfo,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*pinstance*

Die-Instanz, die Sie für einen bestimmten-Befehl verwenden. Die Verwendung dieses Parameters hängt vom Betriebsmodus der Engine ab. Wenn die Engine im Legacy Modus (Windows 2000-Kompatibilitätsmodus) betrieben wird, in dem nur eine Instanz unterstützt wird, können Sie diesen Parameter entweder auf **null** oder auf einen gültigen Ausgabepuffer festlegen, der entweder **null** oder JET_instanceNil enthält, der das globale Instanzhandle zurückgibt, das als Nebeneffekt der Initialisierung erstellt wurde. Dieser Instanzhandle kann dann an jede andere API weitergegeben werden, die eine-Instanz annimmt. Wenn die Engine im Modus für mehrere Instanzen ausgeführt wird, müssen Sie diesen Parameter auf einen gültigen Eingabepuffer festlegen, der das Instanzhandle enthält, das von der zu initialisierenden [jetkreateinstance](./jetcreateinstance-function.md) -Funktion zurückgegeben wird.

*prstinfo*

Zusätzliche Wiederherstellungs Parameter zum erneuten Zuordnen von Datenbanken während der Wiederherstellung, zum Festlegen der Position, an der die Wiederherstellung beendet wird, oder zum Ermitteln des aktuellen Wiederherstellungs Status.

*grbit*

Eine Gruppe von Bits, die NULL oder mehr Optionen angibt, die in der folgenden Tabelle aufgelistet und definiert sind.

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
<td><p>JET_bitReplayReplicatedLogFiles</p></td>
<td><p>Dieser Wert ist für die zukünftige Verwendung reserviert.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitCreateSFSVolumeIfNotExist</p></td>
<td><p>Dieser Wert ist für die zukünftige Verwendung reserviert.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitReplayIgnoreMissingDB</p></td>
<td><p>Mit diesem Wert kann der Benutzer die Wiederherstellung für einen Satz von Protokolldateien ausführen, auch wenn keine Datenbanken vorhanden sind, die zu einem bestimmten Zeitpunkt an den Protokolldatei Satz angefügt wurden.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRecoveryWithoutUndo</p></td>
<td><p>Mit diesem Wert kann der Benutzer die Wiederherstellung durchführen, aber nur bis zu (und nicht einschließlich) der Roll Back Phase. Mithilfe dieses Werts können zusätzliche Transaktionsprotokolle in kopiert und angewendet werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTruncateLogsAfterRecovery</p></td>
<td><p>Dieser Wert bewirkt, dass Protokolldateien während einer erfolgreichen Soft-Wiederherstellung abgeschnitten werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitReplayMissingMapEntryDB</p></td>
<td><p>Dieser Wert bewirkt, dass ein fehlender Daten Bank Zuordnungs Eintrag dem gleichen Speicherort entspricht.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitReplayIgnoreLostLogs</p></td>
<td><p>Dieser Wert bewirkt, dass Protokolle, die vom Ende des Protokolldaten Stroms verloren gehen, während einer Wiederherstellung ignoriert werden.</p>
<p><strong>Windows 7: JET_bitReplayIgnoreLostLogs</strong> wurde in Windows 7 eingeführt.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) -Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern (Extensible Storage Engine) finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Fehler Behandlungsparameter](./error-handling-parameters.md).


#### <a name="remarks"></a>Bemerkungen

Eine Instanz muss mit einem Aufrufen der **JetInit3** -Funktion initialisiert werden, bevor Sie von einem anderen als der [jetsetsystemparameter](./jetsetsystemparameter-function.md) -Funktion verwendet werden kann.

Eine Instanz wird durch einen-Rückruf der [jetterm](./jetterm-function.md) -Funktion zerstört, auch wenn diese Instanz nicht mithilfe der [jetinit](./jetinit-function.md) -Funktion initialisiert wurde. Eine Instanz ist die Wiederherstellbarkeits Einheit für die Datenbank-Engine. Er steuert den Lebenszyklus aller Dateien, mit denen die Integrität der Daten in einem Satz von Datenbankdateien geschützt wird. Diese Dateien enthalten die Prüf Punkt Datei und die Transaktionsprotokoll Dateien. Beachten Sie, dass [jetterm](./jetterm-function.md) nicht aufgerufen werden sollte, wenn die **JetInit3** -Funktion fehlschlägt. [Jetterm](./jetterm-function.md) sollte jedoch immer noch für alle Instanzen aufgerufen werden, die von **JetCreateInstance2** erstellt wurden, wenn **JetInit3** nie aufgerufen wurde oder **JetInit3** erfolgreich ist.

Wenn die Wiederherstellung für eine Gruppe von Protokollen ausgeführt wird, für die nicht alle zugehörigen Datenbanken vorhanden sind (was den Fehler JET_errAttachedDatabaseMismatch unter normalen Umständen zurückgibt), und der Client möchte, dass die Wiederherstellung trotz fehlender Datenbanken fortgesetzt wird, wird der JET_bitReplayIgnoreMissingDB Fehler verwendet, um die Wiederherstellung für die verfügbaren Datenbanken fortzusetzen.

Da die Absturz Wiederherstellung in der Regel nicht auf dem gleichen Computer (und mit derselben Konfiguration) wie zum Zeitpunkt des Absturzes stattfindet, ändert sich eine Datenbank in der Regel nicht. In bestimmten Szenarien, z. b. beim Verschieben von Dateien auf einen anderen Computer oder beim Wiederherstellen der Momentaufnahme Sicherung an verschiedenen Speicherorten, ist dies nicht mehr der Fall Mit der **JetInit3** -Funktion können Sie eine Zuordnung (mithilfe der [JET_RSTINFO](./jet-rstinfo-structure.md) -und [JET_RSTMAP](./jet-rstmap-structure.md) Strukturen) zwischen dem alten Daten Bank Speicherort und dem neuen Speicherort angeben. Tatsächlich benötigen Sie nur den neuen Speicherort, sofern die Datenbankdateien an diesem Speicherort vorhanden sind. Sobald Sie die Speicherorte der wiederhergestellten Datenbanken kennen, wird die Daten Bank Signatur verwendet, um die Datenbank durch den Wiederherstellungs Vorgang zu identifizieren. Sie benötigen den ursprünglichen Speicherort der Datenbank nur dann, wenn Sie eine Datenbank neu erstellen müssen. in diesem Fall ist die Signatur bekannt.

Wenn Sie eine Wiederherstellung nach einem Rückgängig-Vorgang beenden müssen, können Sie außerdem eine bestimmte Protokoll Position angeben, an der die Wiederherstellung beendet wird. Beachten Sie, dass die Möglichkeit besteht, am Ende einer bestimmten Protokoll Generierung anzuhalten, wenn die angegebene Position Teil der Generierung ist, aber hinter dem Ende des eigentlichen Protokolls liegt.

Weitere Informationen finden Sie im Abschnitt "Hinweise" des Themas [jetinit](./jetinit-function.md) .

#### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Client</p></td>
<td><p>Erfordert Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p>Server</p></td>
<td><p>Erfordert Windows Server 2008.</p></td>
</tr>
<tr class="odd">
<td><p>Header</p></td>
<td><p>In "ESENT. h" deklariert.</p></td>
</tr>
<tr class="even">
<td><p>Bibliothek</p></td>
<td><p>Verwendet ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p>DLL</p></td>
<td><p>Erfordert ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p>Unicode</p></td>
<td><p>Implementiert als <strong>JetInit3W</strong> (Unicode) und <strong>JetInit3A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[Extensible Storage Engine-Dateien](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_RSTINFO](./jet-rstinfo-structure.md)  
[JET_RSTMAP](./jet-rstmap-structure.md)  
[Jetkreateingestance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetInit2](./jetinit2-function.md)  
[Jetsetsystemparameter](./jetsetsystemparameter-function.md)  
[Ressourcenparameter](./resource-parameters.md)
