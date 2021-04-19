---
description: 'Weitere Informationen zu: jetenablemultiinstance-Funktion'
title: Jetenablemultiinstance-Funktion
TOCTitle: JetEnableMultiInstance Function
ms:assetid: d88a7b2a-c0d1-47de-9239-3631150d92da
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294107(v=EXCHG.10)
ms:contentKeyID: 32765722
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEnableMultiInstanceW
- JetEnableMultiInstanceA
- JetEnableMultiInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 61fb058b14d9a8abeb282d4227b110ba50304a7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373377"
---
# <a name="jetenablemultiinstance-function"></a>Jetenablemultiinstance-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetenablemultiinstance-function"></a>Jetenablemultiinstance-Funktion

Die **jetenablemultiinstance** -Funktion konfiguriert die Datenbank-Engine für die Verwendung mit mehreren Instanzen im gleichen Prozess. Ein optionales Array globaler Systemparameter ist für den ersten Aufrufer verfügbar, der die Änderung des Modus für mehrere Instanzen ermöglicht.

**Windows XP: jetenablemultiinstance** wird in Windows XP eingeführt.

```cpp
    JET_ERR JET_API JetEnableMultiInstance(
      __in_opt      JET_SETSYSPARAM* psetsysparam,
      __in_opt      unsigned long csetsysparam,
      __out_opt     unsigned long* pcsetsucceed
    );
```

### <a name="parameters"></a>Parameter

*psetsysparam*

Ein Array von globalen Systemparametern, das nur dann festgelegt werden soll, wenn die Engine als Ergebnis dieses Aufrufes in den multiinstanzmodus wechselt. Wenn *csetsysparam* gleich 0 (null) ist, wird *psetsysparam* ignoriert.

*csetsysparam*

Die Anzahl der Elemente für das Array von globalen Parametern, die nur dann festgelegt werden sollen, wenn die Engine als Ergebnis dieses Aufrufes den Modus für mehrere Instanzen eingibt. Wenn *csetsysparam* gleich 0 (null) ist, wird *psetsysparam* ignoriert.

*pcseterfolg*

Ein Zeiger auf die Anzahl der globalen Systemparameter, die als Ergebnis dieses Aufrufes erfolgreich konfiguriert wurden.

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
<td><p>JET_errIndexTuplesInvalidLimits</p></td>
<td><p>Die angegebenen tupelindexparameter waren nicht zulässig. Dieser Fehler kann von <strong>jetenablemultiinstance</strong> nur zurückgegeben werden, wenn <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMin</a>, <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>oder <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesToIndexMax</a> auf einen ungültigen Wert festgelegt wird.</p>
<p><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidPath</p></td>
<td><p>Der angegebene Dateisystempfad war ungültig. Dieser Fehler kann von <strong>jetenablemultiinstance</strong> nur beim Festlegen von Systemparametern zurückgegeben werden, die Dateisystem Pfade darstellen. Beispielsweise kann <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> diesen Fehler zurückgeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInOneInstanceMode</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da er unzulässig ist, wenn die Datenbank-Engine im einzelinstanzmodus (Windows 2000-Kompatibilitätsmodus) ausgeführt wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSystemParamsAlreadySet</p></td>
<td><p>Fehler bei <strong>jetenablemultiinstance</strong> , weil sich die Engine bereits im Modus für mehrere Instanzen befindet.</p>
<p><strong>Hinweis  </strong> Dies geschieht auch, wenn keine Systemparameter angegeben werden.</p></td>
</tr>
</tbody>
</table>


Wenn diese Funktion erfolgreich ausgeführt wird, wird die Datenbank-Engine so konfiguriert, dass Sie im Modus mit mehreren Instanzen ausgeführt wird. Die Engine wurde auch erfolgreich mit der optionalen Liste der globalen Systemparameter konfiguriert.

Wenn diese Funktion fehlschlägt, verbleibt die Datenbank-Engine im aktuellen Modus. Wenn *pcseterfolg* ungleich 0 (null) ist, bleibt diese Anzahl von Systemparametern festgelegt.

#### <a name="remarks"></a>Bemerkungen

Diese Funktion sollte nur verwendet werden, wenn die Anwendung einen bestimmten Satz von Systemparametern atomarisch konfigurieren muss, wenn die Datenbank-Engine für die Verwendung in einem Szenario mit mehreren Benutzern in demselben Prozess eingerichtet wird. Wenn eine andere Synchronisierungsmethode verfügbar ist, ist es vorzuziehen, [jetkreateinstance](./jetcreateinstance-function.md) und [jetsetsystemparameter](./jetsetsystemparameter-function.md) separat aufzurufen.

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
<td><p>Implementiert als <strong>jetenablemultiinstancew</strong> (Unicode) und <strong>jetenablemultiinstancea</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_SETSYSPARAM](./jet-setsysparam-structure.md)  
[Jetkreateingestance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[Jetsetsystemparameter](./jetsetsystemparameter-function.md)
