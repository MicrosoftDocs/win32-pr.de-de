---
description: 'Weitere Informationen zu: jetclosefilinput Stance-Funktion'
title: Jetclosefilinput Stance-Funktion
TOCTitle: JetCloseFileInstance Function
ms:assetid: 64a38655-b128-453b-9593-46032bd6c470
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269270(v=EXCHG.10)
ms:contentKeyID: 32765572
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCloseFileInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d575e90d828159f310a27068ce8d88b29970f4e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524968"
---
# <a name="jetclosefileinstance-function"></a>Jetclosefilinput Stance-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetclosefileinstance-function"></a>Jetclosefilinput Stance-Funktion

Die **jetclosefileinstance** -Funktion schließt eine Datei, die mit [jetopenfileinstance](./jetopenfileinstance-function.md) geöffnet wurde, nachdem die Daten aus dieser Datei mit [jetreadfileinstance](./jetreadfileinstance-function.md)extrahiert wurden.

**Windows XP: jetclosefileinstance** wird in Windows XP eingeführt.

```cpp
    JET_ERR JET_API JetCloseFileInstance(
      __in          JET_INSTANCE instance,
      __in          JET_HANDLE hfFile
    );
```

### <a name="parameters"></a>Parameter

*lichen*

Die-Instanz, die für diesen Befehl verwendet werden soll.

Für Windows 2000 ist die API-Variante, die diesen Parameter akzeptiert, nicht verfügbar, da nur eine Instanz unterstützt wird. In diesem Fall wird die Verwendung dieser globalen Instanz impliziert.

Für Windows XP und spätere Versionen kann die API-Variante, die diesen Parameter nicht akzeptiert, nur aufgerufen werden, wenn sich die Engine im Legacy Modus (Windows 2000-Kompatibilitätsmodus) befindet, in dem nur eine Instanz unterstützt wird. Andernfalls schlägt der Vorgang mit JET_errRunningInMultiInstanceMode fehl.

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
<td><p>Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg294108(v=exchg.10).md">jetstopserviceinstance</a>beendet wurden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</p>
<p>Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Einer der Parameter, die bereitgestellt wurden, enthielt einen unerwarteten Wert, oder die Kombination mehrerer Parameterwerte hat ein unerwartetes Ergebnis zurückgegeben. Dies kann bei <strong>jetclosefilinput Stance</strong> vorkommen, wenn:</p>
<ul>
<li><p>Das angegebene Instanzhandle ist ungültig (Windows XP und spätere Releases).</p></li>
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

Die Datenbank-Engine unterstützt zurzeit nur eine geöffnete Datei durch [jetopenfileinstance](./jetopenfileinstance-function.md) . Wenn ein Datei Handle mit [jetopenfileinstance](./jetopenfileinstance-function.md) geöffnet wird, muss es mithilfe von **jetclosefileinstance** geschlossen werden, bevor eine andere Datei geöffnet werden kann.

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

[JET_ERR](./jet-err.md)  
[JET_HANDLE](./jet-handle.md)  
[JET_INSTANCE](./jet-instance.md)  
[Jetopeinfileinstance](./jetopenfileinstance-function.md)  
[Jetreadfilinput Stance](./jetreadfileinstance-function.md)  
[Jetstopserviczustance](./jetstopserviceinstance-function.md)
