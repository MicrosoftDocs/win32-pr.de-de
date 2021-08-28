---
description: 'Weitere Informationen zu: JetStopServiceInstance2-Funktion'
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
ms.openlocfilehash: 1b5446306bd4035c68f33db2966b1cfadd0b6d82
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987233"
---
# <a name="jetstopserviceinstance2-function"></a>JetStopServiceInstance2-Funktion


_**Gilt für:** Windows | Windows Server_

Die **JetStopServiceInstance2-Funktion** bereitet eine Instanz vor Suspend und eine Instanz nach Resume vor. Anhalten und Fortsetzen sind Ausführungszustände des Windows Store App-Lebenszyklusmodells.

Die **JetStopServiceInstance2-Funktion** wurde in Windows 8 eingeführt.

``` c++
JET_ERR JET_API JetStopServiceInstance2(
  _In_          JET_INSTANCE       instance
  _In_          const JET_GRBIT    grbit
);
```

### <a name="parameters"></a>Parameter

*Instanz*

Die Zielinstanz. Der **JET_INSTANCE** Datentyp ist ein Handle für die Instanz der Datenbank, die für einen Aufruf der JET-API verwendet werden soll. Dieses Handle wird abgerufen, wenn Sie eine Instanz der Datenbank erstellen, indem Sie die Funktionen [JetCreateInstance,](./jetcreateinstance-function.md) [JetCreateInstance2,](./jetcreateinstance2-function.md) [JetInit](./jetinit-function.md)oder [JetInit2](./jetinit2-function.md) aufrufen.

*grbit*

Eine Gruppe von Bits, die einen oder mehrere der in der folgenden Tabelle aufgeführten und definierten Werte angibt.


| <p>Wert</p> | <p>BESCHREIBUNG</p> | 
|--------------|--------------------|
| <p>JET_bitStopServiceAll</p> | <p>Beendet alle ESE-Dienste (Extensible Storage Engine) für die angegebene Instanz.</p> | 
| <p>JET_bitStopServiceBackgroundUserTasks</p> | <p>Beendet neu startbare clientspezifische Hintergrundwartungsaufgaben (z. B. B+ Tree Defrag).</p> | 
| <p>JET_bitStopServiceQuiesceCaches</p> | <p>Lädt alle geänderten Caches in den Ruhespeicher auf den Datenträger. Dieser Wert ist asynchron und kann abgebrochen werden.</p> | 
| <p>JET_bitStopServiceResume</p> | <p>Setzt zuvor ausgegebene StopService-Vorgänge fort. Das heißt, der Dienst wird neu gestartet. Dieser Wert kann mit dem <em>grbits-Parameter</em> kombiniert werden, um bestimmte Dienste fortzusetzen, oder mit JET_bitStopServiceAll zum Fortsetzen aller zuvor beendeten Dienste. Dieses Bit kann nur verwendet werden, um StopServiceBackgroundUserTasks und JET_bitStopServiceQuiesceCaches fortzusetzen. Wenn Sie zuvor mit JET_bitStopServiceAll aufgerufen haben, schlägt der Versuch fehl, JET_bitStopServiceResume zu verwenden. Wenn der zweite Schritt zum Fortsetzen nicht aufgerufen wird, wird die Leistung der Anwendung beeinträchtigt. In diesem Fall wird der Prüfpunkt bei 0 (null) gehalten.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 



#### <a name="remarks"></a>Bemerkungen

Mit dieser Funktion kann eine JET-Anwendung den Datenbankcache in einen bereinigten oder nahezu bereinigten Zustand verschieben (mit im Leerlauf befindlicher Betriebssystem-E/A), sodass die Wiederherstellung schnell erfolgen würde, wenn die Anwendung beendet würde. Dieser Ansatz wird dem Beenden von JET durch Aufrufen der [JetTerm-](./jetterm-function.md) oder [JetDetachDatabase-Funktionen](./jetdetachdatabase-function.md) vorgezogen, sodass die Anwendung im gängigeren Szenario einfach nicht mehr verwendet wird und die Anwendung später über den gesamten Cache verfügt und so schnell wie möglich einsatzbereit ist.

Wenn diese Funktion erfolgreich ausgeführt wird, bereitet sie den Datenbankcache auf eine bevorstehende Unterbrechung vor. Diese Funktion warteschlangen arbeiten mit einem Arbeitsthread im Hintergrund und kehren sofort zum Aufrufer zurück. Die Funktion sollte basierend auf DER SICHTBARKEITNotice aufgerufen werden, anstatt vom Ereignishandler für das Anhalten der Anwendung aufzurufen, um sicherzustellen, dass JET Zeit zum Leeren von geänderten Puffern hat, bevor DER PROZESS angehalten/beendet wird. Intern löst JET bei Konfigurationsänderungen eine sofortige Verteilung der Prüfpunktwartung aus (entweder prüfpunktaktualisierung oder dieses neue Incesce-Cachebit). Weitere Informationen zu VisibilityNotice-Ereignissen finden Sie unter [VisibilityChangedEventArgs-Klasse.](/uwp/api/windows.ui.core.visibilitychangedeventargs)

Diese Funktion muss zweimal aufgerufen werden. Sie wird aufgerufen, nachdem die Anwendung die Unterbrechungsbenachrichtigung vom Betriebssystem erhalten hat, aber bevor die Anwendung angehalten wurde. Anschließend wird er erneut aufgerufen, nachdem das Betriebssystem die Anwendung fortgesetzt hat. Beispiel:

Bei Aufruf von Suspend: JET_ERR JET_API JetStopServiceInstance2( instanz, JET_bitStopServiceQuiesceCaches);

Bei Fortsetzung: JET_ERR JET_API JetStopServiceInstance2(-Instanz, JET_bitStopServiceQuiesceCaches| JET_bitStopServiceResume );

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows 8.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2012.</p> | 
| <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Siehe auch

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
