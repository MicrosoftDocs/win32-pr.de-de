---
description: 'Weitere Informationen finden Sie hier: JetStopServiceInstance2-Funktion'
title: JetStopServiceInstance2-Funktion
TOCTitle: JetStopServiceInstance2 Function
ms:assetid: ac021e13-ec83-42eb-9aef-a906d7a7ed39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835046(v=EXCHG.10)
ms:contentKeyID: 49894668
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetStopServiceInstance2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5029e2cf45ec91d0282f32491895a24b32e6259e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752280"
---
# <a name="jetstopserviceinstance2-function"></a>JetStopServiceInstance2-Funktion


_**Gilt für:** Windows | Windows Server_

Die **JetStopServiceInstance2** -Funktion bereitet eine Instanz vor dem aussetzen vor und bereitet eine Instanz nach der Wiederaufnahme vor. Suspend und Resume sind Ausführungs Zustände des Lebenszyklus Modells der Windows Store-App.

Die **JetStopServiceInstance2** -Funktion wurde in Windows 8 eingeführt.

``` c++
JET_ERR JET_API JetStopServiceInstance2(
  _In_          JET_INSTANCE       instance
  _In_          const JET_GRBIT    grbit
);
```

### <a name="parameters"></a>Parameter

*lichen*

Die Ziel Instanz. Der **JET_INSTANCE** -Datentyp ist ein Handle für die Instanz der-Datenbank, die für einen aufzurufenden Jet-API-Befehl verwendet werden soll. Dieses Handle wird abgerufen, wenn Sie eine Instanz der Datenbank erstellen, indem Sie die [jetcreateinstance](./jetcreateinstance-function.md)-, [JetCreateInstance2](./jetcreateinstance2-function.md)-, [jetinit](./jetinit-function.md)-oder [JetInit2](./jetinit2-function.md) -Funktion aufrufen.

*grbit*

Eine Gruppe von Bits, die einen oder mehrere der Werte angibt, die in der folgenden Tabelle aufgelistet und definiert sind.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Wert</p></th>
<th><p>BESCHREIBUNG</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitStopServiceAll</p></td>
<td><p>Beendet alle ESE-Dienste (Extensible Storage Engine) für die angegebene-Instanz.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitStopServiceBackgroundUserTasks</p></td>
<td><p>Beendet neu startbare, vom Client angegebene Hintergrund Wartungs Tasks (z. B. B +-Struktur Defragmentierung).</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitStopServiceQuiesceCaches</p></td>
<td><p>Versetzt alle Dirty Caches auf den Datenträger. Dieser Wert ist asynchron und kann abgebrochen werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitStopServiceResume</p></td>
<td><p>Setzt zuvor ausgestellte Stopp Dienst Vorgänge fort. Das heißt, dass der Dienst neu gestartet wird. Dieser Wert kann mit dem <em>grbits</em> -Parameter kombiniert werden, um bestimmte Dienste fortzusetzen, oder mit JET_bitStopServiceAll, um alle zuvor beendeten Dienste wieder aufzunehmen. Dieses Bit kann nur zum Fortsetzen von stopservicebackgroundusertasks und JET_bitStopServiceQuiesceCaches verwendet werden. Wenn Sie zuvor mit JET_bitStopServiceAll aufgerufen haben, tritt beim Versuch, JET_bitStopServiceResume zu verwenden, ein Fehler auf. Wenn der zweite Fortschritt nicht aufgerufen wird, wird die Leistung der Anwendung beeinträchtigt. In dieser Situation wird der Prüfpunkt auf 0 (null) beibehalten.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) -Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).

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
</tbody>
</table>


#### <a name="remarks"></a>Bemerkungen

Diese Funktion ermöglicht es einer Jet-Anwendung, den Daten Bank Cache in den Zustand "bereinigt" oder "fast Clean" (mit dem Betriebssystem-e/a-Leerlauf) zu verschieben, sodass die Wiederherstellung schnell ausgeführt werden kann, wenn die Anwendung beendet werden soll. Diese Vorgehensweise wird für das Beenden von Jet bevorzugt, indem die [jetterm](./jetterm-function.md) -Funktion oder die [jetdetachdatabase](./jetdetachdatabase-function.md) -Funktion aufgerufen wird, sodass die Anwendung im gängigeren Szenario nicht angehalten wird und die Anwendung später den gesamten Cache hat und so schnell wie möglich ausgeführt werden kann.

Wenn diese Funktion erfolgreich ausgeführt wird, bereitet Sie den Daten Bank Cache auf eine bevorstehende Unterbrechung vor. Diese Funktion fügt arbeiten an einen Hintergrund Arbeitsthread an und kehrt sofort an den Aufrufer zurück. Die-Funktion sollte basierend auf dem PLM visibilitynotice aufgerufen werden, anstatt vom Handler für die Unterbrechung der Anwendung aufgerufen zu werden, um sicherzustellen, dass Jet Zeit zum leeren von Änderungs Puffern hat, bevor der Prozess von PLM angehalten oder beendet wird. Intern löst Jet eine sofortige Verteilung der Prüf Punkt Wartung bei der Konfigurationsänderung aus (entweder Checkpoint Update oder this New versetzen Caches Bit). Weitere Informationen zu visibilitynotice-Ereignissen finden Sie unter [visibilitychangedeventargs-Klasse](/uwp/api/windows.ui.core.visibilitychangedeventargs).

Diese Funktion muss zweimal aufgerufen werden. Sie wird aufgerufen, nachdem die Anwendung den Suspensions Hinweis vom Betriebssystem empfangen hat, aber bevor die Anwendung angehalten wurde. Anschließend wird Sie erneut aufgerufen, nachdem das Betriebssystem die Anwendung wieder aufnimmt. Beispiel:

Beim Aufrufen zum aussetzen: JET_ERR JET_API JetStopServiceInstance2 (Instanz, JET_bitStopServiceQuiesceCaches);

Beim fortsetzen: JET_ERR JET_API JetStopServiceInstance2 (Instanz, JET_bitStopServiceQuiesceCaches | JET_bitStopServiceResume);

#### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows 8.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2012.</p></td>
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


#### <a name="see-also"></a>Siehe auch

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[Jetclosedatabase](./jetclosedatabase-function.md)  
[Jetclosetable](./jetclosetable-function.md)  
[Jetdetachdatabase](./jetdetachdatabase-function.md)  
[Jetendsession](./jetendsession-function.md)  
[Jetresessioncontext](./jetresetsessioncontext-function.md)  
[Jetrollback](./jetrollback-function.md)  
[Jetterm](./jetterm-function.md)  
[JetTerm2](./jetterm2-function.md)
