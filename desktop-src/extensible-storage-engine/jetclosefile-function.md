---
description: 'Weitere Informationen zu: jetclosefile-Funktion'
title: Jetclosefile-Funktion
TOCTitle: JetCloseFile Function
ms:assetid: e8930915-8102-44b0-ae42-abedbd3e0512
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294127(v=EXCHG.10)
ms:contentKeyID: 32765741
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCloseFile
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 29fc2c76bf8528956d3e3331b3c2f23bf52f929f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393381"
---
# <a name="jetclosefile-function"></a>Jetclosefile-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetclosefile-function"></a>Jetclosefile-Funktion

Die **jetclosefile** -Funktion schließt eine Datei, die mit [jetopenfile](./jetopenfile-function.md) geöffnet wurde, nachdem die Daten aus dieser Datei mit [jetreadfile](./jetreadfile-function.md)extrahiert wurden.

```cpp
    JET_ERR JET_API JetCloseFile(
      __in          JET_HANDLE hfFile
    );
```

### <a name="parameters"></a>Parameter

*hffile*

Das Handle der zu lesenden Datei.

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
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</p>
<p>Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Einer der angegebenen Parameter enthielt einen unerwarteten Wert oder enthielt einen Wert, der nicht sinnvoll war, wenn er mit dem Wert eines anderen Parameters kombiniert wurde. Dies kann bei <strong>jetclosefile</strong> vorkommen, wenn Folgendes geschieht:</p>
<ul>
<li><p>Das angegebene Instanzhandle ist ungültig (Windows XP und spätere Releases),</p></li>
<li><p>Das angegebene Datei Handle ist ungültig.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errNoBackup</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da keine externe Sicherung durchgeführt wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, weil versucht wurde, die Engine im Legacy Modus (Windows 2000-Kompatibilitätsmodus) zu verwenden, in dem nur eine Instanz unterstützt wird, wenn tatsächlich mehrere Instanzen bereits vorhanden sind.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg wird das Datei Handle geschlossen. Wenn eine Datenbankdatei geschlossen wurde, wird die zugehörige datenbankpatchdatei (falls vorhanden) zerstört.

Bei einem Fehler erfolgt keine Änderung.

#### <a name="remarks"></a>Bemerkungen

Die Datenbank-Engine unterstützt zurzeit nur eine geöffnete Datei durch [jetopenfile](./jetopenfile-function.md) . Wenn ein Datei Handle mit [jetopenfile](./jetopenfile-function.md) geöffnet wird, muss es mithilfe von **jetclosefile** geschlossen werden, bevor eine andere Datei geöffnet werden kann.

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

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_HANDLE](./jet-handle.md)  
[Jetopumfile](./jetopenfile-function.md)  
[Jetreadfile](./jetreadfile-function.md)  
[Jetstopservice](./jetstopservice-function.md)
