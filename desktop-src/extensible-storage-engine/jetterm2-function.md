---
description: 'Weitere Informationen finden Sie hier: JetTerm2-Funktion'
title: JetTerm2-Funktion
TOCTitle: JetTerm2 Function
ms:assetid: 36464e24-1cc0-4cda-9d7a-f64555c622bf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269223(v=EXCHG.10)
ms:contentKeyID: 32765525
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTerm2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dc8b0c768e981b88e8759c30d349caa8e5575a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129717"
---
# <a name="jetterm2-function"></a>JetTerm2-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetterm2-function"></a>JetTerm2-Funktion

Die **JetTerm2** -Funktion initiiert das Herunterfahren einer Instanz, die von [jetinit](./jetinit-function.md)initialisiert wurde.

**JetTerm2** kann auch eine nicht initialisierte Instanz zerstören, die von [jetkreateinstance](./jetcreateinstance-function.md)erstellt wurde.

```cpp
    JET_ERR JET_API JetTerm2(
      __in          JET_INSTANCE instance,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*lichen*

Die-Instanz, die für diesen Befehl verwendet werden soll.

**Windows 2000:**  Dieser Parameter wird ignoriert und sollte immer **null** sein.

**Versionen von Windows XP und höher:**  Dieser Parameter ist überladen. Wenn die Engine im Legacy Modus (Windows 2000-Kompatibilitätsmodus) betrieben wird, in dem nur eine Instanz unterstützt wird, kann dieser Parameter **null** sein oder die tatsächliche Instanz enthalten, die von [jetinit](./jetinit-function.md)zurückgegeben wird. Wenn die Engine im Modus für mehrere Instanzen ausgeführt wird, muss dieser Parameter ein Zeiger auf eine Instanz sein, die mithilfe von [jetkreateinstance](./jetcreateinstance-function.md)erstellt wurde.

*grbit*

Eine Gruppe von Bits, die die für diesen-Befehl zu verwendenden Optionen enthalten, die 0 (null) oder mehrere der folgenden Werte enthalten.

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
<td><p>JET_bitTermComplete</p></td>
<td><p>Fordert an, dass die Instanz ordnungsgemäß heruntergefahren wird. Alle optionalen Bereinigungs arbeiten, die normalerweise zur Laufzeit im Hintergrund durchgeführt werden, werden sofort abgeschlossen.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTermAbrupt</p></td>
<td><p>Fordert an, dass die Instanz so schnell wie möglich heruntergefahren wird. Alle optionalen arbeiten, die normalerweise zur Laufzeit im Hintergrund durchgeführt werden, werden abgebrochen.</p>
<p><strong>Hinweis</strong>  Diese Option kann zum Verlust vorübergehender oder dauerhafter Speicherplatz in der Datenbank führen. Dieser verlorene Speicherplatz kann immer durch eine Offline Defragmentierung der Datenbank wieder hergestellt werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTermStopBackup</p></td>
<td><p>Fordert an, dass die Instanz heruntergefahren wird, auch wenn zurzeit eine Sicherung ausgeführt wird. Normalerweise bewirkt eine ausstehende Sicherung, dass <a href="gg269298(v=exchg.10).md">jetterm</a> mit JET_errBackupInProgress fehlschlägt. Wenn dieser Parameter nicht vorhanden ist, wird davon ausgegangen, dass sein Wert JET_bitTermAbrupt wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTermDirty</p></td>
<td><p>Fordert an, dass die Instanz mit allen angefügten Datenbanken heruntergefahren wird, die in einem fehlerhaften Zustand bleiben.</p>
<p>Windows 7: JET_bitTermDirty wurde in Windows 7 eingeführt.</p></td>
</tr>
</tbody>
</table>


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
<td><p>JET_errBackupInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die Instanz zurzeit ein Sicherungs Vorgang ausgeführt wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Einer der Parameter, die bereitgestellt wurden, enthielt einen unerwarteten Wert, oder die Kombination aus mehreren Parametern hat ein unerwartetes Ergebnis zurückgegeben. Dieser Fehler wird von <a href="gg269298(v=exchg.10).md">jetterm</a> zurückgegeben, wenn sich die Engine im Modus für mehrere Instanzen befindet und <em>pinstance</em> auf eine ungültige Instanz verweist.</p>
<p><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die Instanz noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die Instanz heruntergefahren wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die Instanz ein Wiederherstellungs Vorgang ausgeführt wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyActiveUsers</p></td>
<td><p>Die Instanz kann nicht heruntergefahren werden, da derzeit Sitzungen mit aktiven Transaktionen für die angegebene Instanz vorhanden sind. Dieser Fehler tritt nur auf, wenn die JET_bitTermComplete verwendet wird.</p></td>
</tr>
</tbody>
</table>


Wenn diese Funktion erfolgreich ausgeführt wird, wird die angegebene Instanz heruntergefahren. Der Instanzhandle wird auch geschlossen und für jede API, die einen Instanzhandle annimmt, nicht verfügbar gemacht. Alle anderen Objekte, die der-Instanz zugeordnet sind, z. b. Sitzungen, werden ebenfalls geschlossen. Der Status der Prüf Punkt Datei, der Transaktionsprotokoll Dateien und der Datenbankdateien, die an die Instanz angefügt sind, werden während des Beendigungs Vorgangs geändert.

Wenn diese Funktion aufgrund eines Verwendungs Fehlers fehlschlägt, verbleibt die Instanz in einem initialisierten Zustand, und es werden keine Änderungen vorgenommen. Andernfalls wird die Instanz nach wie vor für den Erfolgsfall heruntergefahren. Der Unterschied besteht darin, dass die Instanz bei der nächsten Initialisierung die Wiederherstellung von Abstürzen durchlaufen muss. Die Engine versucht, so viele Daten wie möglich zu leeren, um die erforderliche Wiederherstellungs Menge zu minimieren. Konzeptionell ist ein solcher Ausfall von [jetterm](./jetterm-function.md) nicht anders als bei einem Prozess Absturz.

#### <a name="remarks"></a>Bemerkungen

Siehe [jetterm](./jetterm-function.md).

#### <a name="requirements"></a>Anforderungen

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
[Jetkreateingestance](./jetcreateinstance-function.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JetInit](./jetinit-function.md)  
[JET_INSTANCE](./jet-instance.md)  
[Jetterm](./jetterm-function.md)
