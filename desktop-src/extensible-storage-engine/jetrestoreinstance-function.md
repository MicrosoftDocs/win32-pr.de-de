---
description: 'Weitere Informationen zu: jetrestorerstance-Funktion'
title: JetRestoreInstance-Funktion
TOCTitle: JetRestoreInstance Function
ms:assetid: 7ba2b6ee-96f5-44c5-9842-5e58580f60f1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269306(v=EXCHG.10)
ms:contentKeyID: 32765597
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRestoreInstanceW
- JetRestoreInstance
- JetRestoreInstanceA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bb7af096a63880a88496631999ddbc26a975cac4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218130"
---
# <a name="jetrestoreinstance-function"></a>JetRestoreInstance-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetrestoreinstance-function"></a>JetRestoreInstance-Funktion

Die **jetrestoreinstance** -Funktion stellt eine Streamingsicherung einer Instanz wieder her, die alle angefügten Datenbanken einschließt. Es ist für die Arbeit mit einer mit der [jetbackupinstance](./jetbackupinstance-function.md) -Funktion erstellten Sicherung konzipiert. Dies ist die einfachste und am meisten gekapselte Wiederherstellungs Funktion.

**Windows XP:**  **jetrestoreinstance** wird in Windows XP eingeführt.

```cpp
    JET_ERR JET_API JetRestoreInstance(
      __in          JET_INSTANCE instance,
      __in          JET_PCSTR sz,
      __in_opt      JET_PCSTR szDest,
      __in          JET_PFNSTATUS pfn
    );
```

### <a name="parameters"></a>Parameter

*lichen*

Gibt die-Instanz an, die für diesen Befehl verwendet werden soll.

Für Windows XP und spätere Versionen hängt die Verwendung dieses Parameters vom Betriebsmodus der Engine ab. Wenn die Engine im Legacy Modus betrieben wird (Windows 2000-Kompatibilitätsmodus), in dem nur eine Instanz unterstützt wird, kann dieser Parameter entweder NULL sein, oder er kann auf einen gültigen Ausgabepuffer festgelegt werden, der NULL oder JET_instanceNil enthält, der das globale Instanzhandle zurückgibt, das als Nebeneffekt der Initialisierung erstellt wird. Dieser Instanzhandle kann dann an jede andere API weitergegeben werden, die eine-Instanz annimmt. Wenn die Engine im Modus für mehrere Instanzen betrieben wird, muss dieser Parameter auf einen gültigen Eingabepuffer festgelegt werden, der das von [jetkreateinstance](./jetcreateinstance-function.md) zurückgegebene Instanzhandle enthält, das initialisiert wird.

*RT*

Der Ordner, in dem sich die Sicherung befindet. Die Sicherung muss mithilfe der [JetBackup](./jetbackup-function.md) -APIs generiert werden.

*szdest*

Der Name des Ordners, in den die Datenbankdateien aus dem Sicherungs Satz kopiert und wieder hergestellt werden. Wenn dies auf NULL festgelegt ist (Dies ist der Fall für den Legacy- [jetrestore](./jetrestore-function.md)), werden die Datenbankdateien kopiert und an Ihrem ursprünglichen Speicherort wieder hergestellt.

*PFN*

Der optionale Zeiger auf die Funktion, die als Benachrichtigungs Informationen zum Fortschritt des Wiederherstellungs Vorgangs aufgerufen wird.

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
<td><p>JET_errAlreadyInitialized</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da die Engine für diese Instanz bereits initialisiert ist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidLogSequence</p></td>
<td><p>Der Satz von Protokolldateien aus dem Sicherungs Satz und aus dem aktuellen Protokoll Pfad stimmt nicht mit dem Satz der Protokolldateien identisch.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Einer der angegebenen Parameter enthielt einen unerwarteten Wert oder enthielt einen Wert, der nicht sinnvoll war, wenn er mit dem Wert eines anderen Parameters kombiniert wurde. Dieser Fehler wird von <strong>jetrestoreinstance</strong> zurückgegeben, wenn sich die Engine im multiinstanzmodus befindet und pinstance auf eine ungültige Instanz von Windows XP und höheren Versionen verweist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidPath</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, weil einige der angegebenen Pfade ungültig sind (der Sicherungs Pfad, der Zielpfad, der Protokoll-oder Systempfad für die Instanz).</p></td>
</tr>
<tr class="even">
<td><p>JET_errPageSizeMismatch</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da die Engine für die Verwendung einer Datenbankseiten Größe (mit <a href="gg294044(v=exchg.10).md">jetsetsystemparameter</a> für <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) konfiguriert ist, die nicht mit der Datenbankseiten Größe identisch ist, die zum Erstellen der Transaktionsprotokoll Dateien oder der Datenbanken verwendet wird, die den Transaktionsprotokoll Dateien zugeordnet sind.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, weil die Parameter den einzelinstanzmodus (Windows 2000-Kompatibilitätsmodus) impliziert haben und sich die Engine bereits im Modus für mehrere Instanzen befindet.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg werden Datenbankdateien aus dem Sicherungs Satz an ihrem Speicherort wieder hergestellt, und die Wiederherstellung wird ausgeführt, sodass sich die Datenbanken in einem sauberen Transaktions Konsistenz Zustand befinden. Bei der Wiederherstellung werden die Protokolldateien aus dem Sicherungs Satz und die Protokolldateien aus dem Protokoll Pfad wiedergegeben, wenn solche Dateien vorhanden sind. Diese Wiederherstellung führt zu Änderungen an der Prüf Punkt Datei, den Transaktionsprotokoll Dateien und allen Datenbanken, auf die von diesen Transaktionsprotokoll Dateien verwiesen wird.

Bei einem Fehler verbleibt die Instanz in einem nicht initialisierten Zustand. Der Status der Transaktionsprotokoll Dateien und sämtlicher Datenbanken, auf die von diesen Transaktionsprotokoll Dateien verwiesen wird, wurde bei dem Versuch, die Wiederherstellung zu initialisieren und die Datenbanken wiederherzustellen, wahrscheinlich geändert.

#### <a name="remarks"></a>Bemerkungen

Beim Wiederherstellungs Vorgang werden die Datenbanken, die während der Sicherung an die Instanz angefügt sind, rekonstruiert und die Änderungen in den Datenbankdateien wieder hergestellt. Das Ergebnis sind Datenbanken, die Transaktions konsistent sind. Wenn möglich, werden die Änderungen, die seit der Sicherung vorgenommen wurden, auch in der Datenbank gespeichert, bis die letzte Änderung in den Transaktions Protokollen gefunden wurde. Dies wäre möglich, wenn die seit der Sicherung generierten Transaktionsprotokolle weiterhin im Transaktionsprotokoll Verzeichnis vorhanden sind. Beachten Sie Folgendes: Wenn die zirkuläre Protokollierung für die Instanz aktiviert wurde, werden die generierten Transaktionsprotokolle so wieder verwendet, dass die Wiederherstellung die Änderungen speichern kann, die bis zum Sicherungs Zeitpunkt stattfinden. In jedem Fall ist es möglich, dass dieser Vorgang sehr viel Zeit in Anspruch nimmt, wenn die Anzahl der Transaktionsprotokoll Dateien, die für die Datenbanken wiedergegeben werden sollen, groß ist.

**Jetrestoreinstance** muss für eine Instanz aufgerufen werden, die bereits mit [jetkreateinstance](./jetcreateinstance-function.md)erstellt wurde.

Da bei der Wiederherstellung eine beträchtliche Anzahl von Datenbankseiten und Transaktions Protokollen verwendet wird, gibt es eine ganze Reihe von Fehlern, die von diesen Funktionen zurückgegeben werden können. Solche Fehler können aus temporären Ressourcen Zuordnungs Fehlern wie JET_errOutOfMemory zu Fehlern bestehen, die physische Beschädigungen wie JET_errReadVerifyFailure, JET_errLogFileCorrupt oder JET_errBadPageLink darstellen. Diese Fehler werden fast immer durch Hardwareprobleme verursacht und können daher nicht vermieden werden. Die Datei Misswirtschaft wird am häufigsten als JET_errMissingLogFile oder JET_errAttachedDatabaseMismatch oder JET_errDatabaseSharingViolation oder JET_errInvalidLogSequence Manifest. Diese Fehler können von der Anwendung verhindert werden. Die Anwendung muss darauf achten, das Repository dieser Dateien vor der Bearbeitung durch externe Kräfte wie z. b. den Benutzer oder andere Anwendungen zu schützen. Wenn die Anwendung eine Instanz vollständig zerstören möchte, müssen alle Dateien, die der Instanz zugeordnet sind, gelöscht werden. Hierzu gehören die Prüf Punkt Datei, die Transaktionsprotokoll Dateien und alle Datenbankdateien, die an die Instanz angefügt sind.

In den verschiedenen Schritten der Wiederherstellung werden Ereignisprotokoll Einträge generiert, einschließlich des Status der Wiedergabe des Transaktions Protokolls und des Endergebnis der Wiederherstellung.

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
<td><p>Implementiert als <strong>jetrestoreingestancew</strong> (Unicode) und <strong>jetrestoreingestancea</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetBackup](./jetbackup-function.md)  
[Jetbackupinstance](./jetbackupinstance-function.md)  
[Jetkreateingestance](./jetcreateinstance-function.md)  
[Jetsetsystemparameter](./jetsetsystemparameter-function.md)
