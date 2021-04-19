---
description: Weitere Informationen finden Sie in der jetgettruneureloginfoinstance-Funktion.
title: Jetgettruneureloginfoinstance-Funktion
TOCTitle: JetGetTruncateLogInfoInstance Function
ms:assetid: 1ecb2f2f-2cad-4c55-9296-5e5893b57695
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269199(v=EXCHG.10)
ms:contentKeyID: 32765502
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTruncateLogInfoInstanceA
- JetGetTruncateLogInfoInstanceW
- JetGetTruncateLogInfoInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3d51243ff6ca4b2bbaec77233bbe00437f55e0f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363742"
---
# <a name="jetgettruncateloginfoinstance-function"></a>Jetgettruneureloginfoinstance-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgettruncateloginfoinstance-function"></a>Jetgettruneureloginfoinstance-Funktion

Die **jetgettrunkateloginfoinstance** -Funktion wird während einer Sicherung verwendet, die von [jetbeginexternalbackup](./jetbeginexternalbackup-function.md) initiiert wird, um eine Instanz nach den Namen der Transaktionsprotokoll Dateien abzufragen, die nach erfolgreichem Abschluss der Sicherung sicher gelöscht werden können.

**Windows XP:**  **jetgettrun-eloginfoinstance** wird in Windows XP eingeführt.

```cpp
    JET_ERR JET_API JetGetTruncateLogInfoInstance(
      __in          JET_INSTANCE instance,
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a>Parameter

*lichen*

Die-Instanz, die für diesen Befehl verwendet werden soll.

*Szz*

Der Ausgabepuffer, der die Liste der mit NULL endenden Zeichen folgen empfängt, die den Satz von Transaktionsprotokoll Dateien beschreiben, die nach dem erfolgreichen Abschluss der Sicherung sicher gelöscht werden können.

Die Liste der Zeichen folgen, die in diesem Puffer zurückgegeben werden, hat das gleiche Format wie eine von der Registrierung verwendete Multizeichenfolge. Jede mit NULL endenden Zeichenfolge wird nacheinander zurückgegeben, gefolgt von einem abschließenden NULL-Terminator.

*cbmax*

Die maximale Größe des Ausgabepuffers in Bytes.

*pcbactual*

Ein Zeiger auf den Ausgabepuffer, der die tatsächliche Menge an Zeichen folgen Daten empfängt.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Rückgabecode</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>Der Vorgang wurde erfolgreich abgeschlossen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Einer der angegebenen Parameter enthielt einen unerwarteten Wert, oder die Kombination mehrerer Parameterwerte führte zu einem unerwarteten Ergebnis.</p>
<p><strong>Windows XP und höher:</strong>  Dies kann bei <strong>jetgettruneureloginfoinstance</strong> vorkommen, wenn das angegebene Instanzhandle ungültig ist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die-Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die-Instanz, die der Sitzung zugeordnet ist, einen schwerwiegenden Fehler festgestellt hat, der erfordert, dass der Zugriff auf alle Daten gesperrt wird, um die Integrität dieser Daten zu schützen</p>
<p><strong>Windows XP:</strong>  Dieser Rückgabewert wurde in Windows XP eingeführt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBackupAbortByServer</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da die aktuelle externe Sicherung durch einen <a href="gg294067(v=exchg.10).md">jetstopbackup</a>-Befehl abgebrochen wurde.</p>
<p><strong>Windows XP:</strong>  Dieser Rückgabewert wurde in Windows XP eingeführt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidBackupSequence</p></td>
<td><p>Der Sicherungs Vorgang ist fehlgeschlagen, da er außerhalb der Reihenfolge aufgerufen wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoBackup</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da keine externe Sicherung durchgeführt wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die-Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Jetgettruneureloginfoinstance</strong></p></td>
<td><p>Es gibt ausstehende Datei Handles, die mit <a href="gg269249(v=exchg.10).md">jetopenfile</a> für die-Instanz erstellt wurden.</p></td>
</tr>
</tbody>
</table>


Wenn diese Funktion erfolgreich ausgeführt wird, werden die angeforderten Informationen zu dem Satz von Transaktionsprotokoll Dateien, die nach dem erfolgreichen Abschluss der Sicherung sicher gelöscht werden können, in die Ausgabepuffer eingefügt, in denen Sie bereitgestellt werden. Der Sicherungs Zustands Automat wird so erweitert, dass die Sicherung von Datenbankdateien nicht mehr zulässig ist. Nur datenbankpatchdateien und Transaktionsprotokoll Dateien können über diesen Punkt hinaus zur Sicherung geöffnet werden.

Wenn diese Funktion fehlschlägt, ist der Status der Ausgabepuffer nicht definiert. Der Fehler führt dazu, dass der gesamte Sicherungsprozess für die Instanz abgebrochen wird.

#### <a name="remarks"></a>Bemerkungen

Diese API gibt keinen Fehler oder eine Warnung zurück, wenn der Ausgabepuffer zu klein ist, um die vollständige Liste der Dateien zu akzeptieren, die Bestandteil des Sicherungsdatei Satzes sein sollten. Die Anwendung sollte immer einen Puffer bereitstellen, um die tatsächliche Größe dieser Liste zu erhalten, und anhand dieser Informationen ermitteln, ob die Liste abgeschnitten wurde.

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementiert als <strong>jetgettruneureloginfoinstancew</strong> (Unicode) und <strong>jetgettrun-eloginfoinstancea</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[Jetbeginexternalbackup](./jetbeginexternalbackup-function.md)  
[Jetclosedatabase](./jetclosedatabase-function.md)  
[Jetclosetable](./jetclosetable-function.md)  
[Jetendsession](./jetendsession-function.md)  
[Jetopumfile](./jetopenfile-function.md)  
[Jetresessioncontext](./jetresetsessioncontext-function.md)  
[Jetrollback](./jetrollback-function.md)  
[Jetstopbackup](./jetstopbackup-function.md)  
[Jetstopservice](./jetstopservice-function.md)  
[Jetterm](./jetterm-function.md)  
[JetTerm2](./jetterm2-function.md)
