---
description: 'Weitere Informationen finden Sie hier: JetInit2-Funktion'
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
ms.openlocfilehash: 00cc3402567a7c1342e78d3c84a1d6cfca8ab4d8
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "103961788"
---
# <a name="jetinit2-function"></a>JetInit2-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetinit2-function"></a>JetInit2-Funktion

Die **JetInit2** -Funktion versetzt die Datenbank-Engine in einen Zustand, in dem Sie die Anwendungs Verwendung von Datenbankdateien unterstützen kann. Die Engine muss für die Initialisierung mit [jetsetsystemparameter](./jetsetsystemparameter-function.md)bereits ordnungsgemäß konfiguriert sein. Die Daten Bank Absturz Wiederherstellung wird automatisch als Teil des Initialisierungs Prozesses ausgeführt.

**Windows XP:**  **JetInit2** wird in Windows XP eingeführt.

Diese Funktion ist veraltet. Verwenden Sie stattdessen [JetInit3](./jetinit3-function.md) .

```cpp
JET_ERR JET_API JetInit2(
  __in_out_opt  JET_INSTANCE* pinstance,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a>Parameter

*pinstance*

Die-Instanz, die für diesen Befehl verwendet werden soll.

Für Windows 2000 wird dieser Parameter ignoriert und sollte immer NULL sein.

Für Windows XP und spätere Versionen hängt die Verwendung dieses Parameters vom Betriebsmodus der Engine ab. Wenn die Engine im Legacy Modus (Windows 2000-Kompatibilitätsmodus) ausgeführt wird, in dem nur eine Instanz unterstützt wird, kann dieser Parameter entweder NULL sein, oder er kann auf einen gültigen Ausgabepuffer festgelegt werden, der NULL oder JET_instanceNil enthält, der das globale Instanzhandle zurückgibt, das als Nebeneffekt der Initialisierung erstellt wurde. Dieser Instanzhandle kann dann an jede andere API weitergegeben werden, die eine-Instanz annimmt. Wenn die Engine im Modus für mehrere Instanzen ausgeführt wird, muss dieser Parameter auf einen gültigen Eingabepuffer festgelegt werden, der das von der zu initialisierende [jetkreateinstance](./jetcreateinstance-function.md) zurückgegebene Instanzhandle enthält.

*grbit*

Eine Gruppe von Bits, die NULL oder mehr der folgenden Optionen angibt.

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
<td><p>Für die zukünftige Verwendung reserviert.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitCreateSFSVolumeIfNotExist</p></td>
<td><p>Für die zukünftige Verwendung reserviert.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitReplayIgnoreMissingDB</p></td>
<td><p>Mit dieser Option kann der Benutzer die Wiederherstellung für einen Satz von Protokolldateien ausführen, ohne dass alle Datenbanken vorhanden sind, die an einem Punkt des Protokoll Satzes angefügt wurden.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRecoveryWithoutUndo</p></td>
<td><p>Führen Sie die Wiederherstellung aus, aber stoppen Sie die Roll Back Phase. Dadurch können zusätzliche Transaktionsprotokolle in kopiert und angewendet werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTruncateLogsAfterRecovery</p></td>
<td><p>Bei erfolgreicher Soft-Wiederherstellung kürzen Sie die Protokolldateien.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitReplayMissingMapEntryDB</p></td>
<td><p>Fehlender Daten Bank Zuordnungs Eintrag ist standardmäßig derselbe Speicherort.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitReplayIgnoreLostLogs</p></td>
<td><p>Ignorieren Sie die Protokolle, die am Ende des Protokolldaten Stroms verloren gegangen sind.</p>
<p><strong>Windows 7: JET_bitReplayIgnoreLostLogs</strong> wurde in Windows 7 eingeführt.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).


#### <a name="remarks"></a>Bemerkungen

Eine Instanz muss mit einem **JetInit2** -Aufrufvorgang initialisiert werden, bevor Sie von einem anderen als [jetsetsystemparameter](./jetsetsystemparameter-function.md)verwendet werden kann.

Eine Instanz wird durch einen-Rückruf der [jetterm](./jetterm-function.md) -Funktion zerstört, auch wenn diese Instanz nicht mit [jetinit](./jetinit-function.md)initialisiert wurde. Eine Instanz ist die Wiederherstellbarkeits Einheit für die Datenbank-Engine. Er steuert den Lebenszyklus aller Dateien, mit denen die Integrität der Daten in einem Satz von Datenbankdateien geschützt wird. Diese Dateien enthalten die Prüf Punkt Datei und die Transaktionsprotokoll Dateien.

Wenn die Wiederherstellung für eine Gruppe von Protokollen ausgeführt wird, für die nicht alle Datenbanken vorhanden sind (was den Fehler JET_errAttachedDatabaseMismatch unter normalen Umständen zurückgibt), und der Client wünscht, dass die Wiederherstellung trotz fehlender Datenbanken fortgesetzt wird, wird die JET_ bitreplayignoremissingdb verwendet, um die Wiederherstellung für die verfügbaren Datenbanken fortzusetzen.

Weitere Informationen finden Sie im Abschnitt "Hinweise" in [jetinit](./jetinit-function.md) .

#### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows Vista oder Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008 oder Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>In "ESENT. h" deklariert.</p></td>
</tr>
<tr class="even">
<td><p><strong>Bibliothek</strong></p></td>
<td><p>Verwenden Sie ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Erfordert ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[Extensible Storage Engine-Dateien](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[Jetkreateingestance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetInit3](./jetinit3-function.md)  
[Jetsetsystemparameter](./jetsetsystemparameter-function.md)  
[Ressourcenparameter](./resource-parameters.md)
