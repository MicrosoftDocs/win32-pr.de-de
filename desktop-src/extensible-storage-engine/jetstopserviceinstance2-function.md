---
description: Weitere Informationen finden Sie unter JetStopServiceInstance2-Funktion.
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
ms.openlocfilehash: 3a28439932d9c0eb76675ed4e88d5595c64b5ace
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470766"
---
# <a name="jetstopserviceinstance2-function"></a>JetStopServiceInstance2-Funktion


_**Gilt für:** Windows | Windows Server_

Die **JetStopServiceInstance2-Funktion** bereitet eine Instanz vor Suspend vor und bereitet eine Instanz nach resume vor. "Suspend" und "Resume" sind Ausführungszustände des Windows Store App-Lebenszyklusmodells.

Die **JetStopServiceInstance2-Funktion** wurde in Windows 8.

``` c++
JET_ERR JET_API JetStopServiceInstance2(
  _In_          JET_INSTANCE       instance
  _In_          const JET_GRBIT    grbit
);
```

### <a name="parameters"></a>Parameter

*Instanz*

Die Zielinstanz. Der **JET_INSTANCE** ist ein Handle für die Instanz der Datenbank, die für einen Aufruf der JET-API verwendet werden soll. Dieses Handle wird beim Erstellen einer Instanz der Datenbank durch Aufrufen der [JetCreateInstance-,](./jetcreateinstance-function.md) [JetCreateInstance2-,](./jetcreateinstance2-function.md) [JetInit-](./jetinit-function.md)oder [JetInit2-Funktionen](./jetinit2-function.md) erhalten.

*grbit*

Eine Gruppe von Bits, die mindestens einen der in der folgenden Tabelle aufgeführten und definierten Werte angibt.


| <p>Wert</p> | <p>BESCHREIBUNG</p> | 
|--------------|--------------------|
| <p>JET_bitStopServiceAll</p> | <p>Beendet alle ESE-Dienste (Extensible Storage Engine) für die angegebene Instanz.</p> | 
| <p>JET_bitStopServiceBackgroundUserTasks</p> | <p>Beendet neu startbare clientspezifische Hintergrundwartungsaufgaben (z. B. B+-Strukturdefragmentierung).</p> | 
| <p>JET_bitStopServiceQuiesceCaches</p> | <p>Macht alle dirty Caches auf den Datenträger in Ruhe. Dieser Wert ist asynchron und kann abgebrochen werden.</p> | 
| <p>JET_bitStopServiceResume</p> | <p>Setzt zuvor ausgegebene StopService-Vorgänge fort. Das heißt, der Dienst wird neu gestartet. Dieser Wert kann mit dem <em>grbits-Parameter kombiniert</em> werden, um bestimmte Dienste wieder aufzunehmen, oder mit JET_bitStopServiceAll alle zuvor beendeten Dienste fortsetzen. Dieses Bit kann nur verwendet werden, um StopServiceBackgroundUserTasks und -JET_bitStopServiceQuiesceCaches. Wenn Sie zuvor mit JET_bitStopServiceAll aufgerufen haben, ist ein Versuch, JET_bitStopServiceResume zu verwenden, fehlgeschlagen. Wenn der zweite Fortsetzungsschritt nicht aufgerufen wird, hat die Anwendung eine beeinträchtigte Leistung. In diesem Fall wird der Prüfpunkt bei 0 (null) beibehalten.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR-Datentyp](./jet-err.md) mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 



#### <a name="remarks"></a>Hinweise

Diese Funktion ermöglicht es einer JET-Anwendung, den Datenbankcache in einen sauberen oder nahezu bereinigten Zustand zu verschieben (mit leerer E/A des Betriebssystems), damit die Wiederherstellung schnell ausgeführt werden kann, wenn die Anwendung beendet wird. Dieser Ansatz wird vor dem Beenden von JET bevorzugt, indem die [JetTerm-](./jetterm-function.md) oder [JetDetachDatabase-Funktionen](./jetdetachdatabase-function.md) aufruft werden, sodass die Anwendung im häufigeren Szenario einfach nicht mehr verwendet wird und die Anwendung später über den gesamten Cache verfügt und so schnell wie möglich einsatzbereit ist.

Wenn diese Funktion erfolgreich ist, bereitet sie den Datenbankcache auf eine bevorstehende Unterbrechung vor. Diese Funktion arbeitet in einem Hintergrundarbeitsthread und kehrt sofort zum Aufrufer zurück. Die Funktion sollte auf Grundlage von DER VISIBILITyNotice aufgerufen werden, im Gegensatz zum Aufrufen vom Unterbrechungsereignishandler der Anwendung, um sicherzustellen, dass JET Zeit hat, dirty Puffer zu leeren, bevor DER PROZESS angehalten/beendet wird. Intern löst JET eine sofortige Versendung der Prüfpunktwartung nach einer Konfigurationsänderung aus (entweder prüfpunktaktualisierung oder dieses neue Inkullcachebit). Weitere Informationen zu VisibilityNotice-Ereignissen finden Sie unter [VisibilityChangedEventArgs-Klasse.](/uwp/api/windows.ui.core.visibilitychangedeventargs)

Diese Funktion muss zweimal aufgerufen werden. Sie wird aufgerufen, nachdem die Anwendung den Unterbrechungshinweis vom Betriebssystem erhalten hat, aber bevor die Anwendung angehalten wurde. Anschließend wird sie erneut aufgerufen, nachdem das Betriebssystem die Anwendung fortgesetzt hat. Beispiel:

Bei Einem -Aussetzen: JET_ERR JET_API JetStopServiceInstance2(-Instanz, JET_bitStopServiceQuiesceCaches);

Bei Fortgesetzt: JET_ERR JET_API JetStopServiceInstance2(-Instanz, JET_bitStopServiceQuiesceCaches| JET_bitStopServiceResume );

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows 8.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2012.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetDetachDatabase](./jetdetachdatabase-function.md)  
[JetEndSession](./jetendsession-function.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetTerm](./jetterm-function.md)  
[JetTerm2](./jetterm2-function.md)
