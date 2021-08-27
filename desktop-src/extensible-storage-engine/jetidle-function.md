---
description: Weitere Informationen finden Sie unter JetIdle-Funktion.
title: JetIdle-Funktion
TOCTitle: JetIdle Function
ms:assetid: 77e036eb-b894-4ff7-b14f-1564bf21873f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269301(v=EXCHG.10)
ms:contentKeyID: 32765593
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetIdle
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: babe3077c01b6b2a9c1f2f55b48921582d6343bd
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984543"
---
# <a name="jetidle-function"></a>JetIdle-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetidle-function"></a>JetIdle-Funktion

Die **JetIdle-Funktion** ist nicht mehr verwendet und sollte nur zu Testzwecken verwendet werden. **JetIdle kann** verwendet werden, um Bereinigungsaufgaben im Leerlauf auszuführen oder den Status des Versionsspeichers in ESE zu überprüfen.

```cpp
    JET_ERR JET_API JetIdle(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die für diesen Aufruf verwendet wird.

*grbit*

Eine Gruppe von Bits, die die für diesen Aufruf zu verwendenden Optionen enthalten, die null oder mehr der folgenden Bits enthalten:


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitIdleCompact</p> | <p>Löst eine Bereinigung des Versionsspeichers aus.</p> | 
| <p>JET_bitIdleFlushBuffers</p> | <p>Für die zukünftige Verwendung reserviert. Wenn dieses Flag angegeben wird, gibt die API JET_errInvalidgrbit.</p> | 
| <p>JET_bitIdleStatus</p> | <p>Gibt JET_wrnIdleFull zurück, wenn der Versionsspeicher mehr als die Hälfte voll ist.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Ein <em>grbit-Parameter,</em> der für die API bereitgestellt wurde, war ungültig.</p> | 



Wenn diese Funktion erfolgreich ist, wird der entsprechende Vorgang oder ein Fehlercode ausgelöst, der angibt, wie voll der Versionsspeicher abhängig vom bereitgestellten *Grbit* ist.

Wenn diese Funktion fehlschlägt, wurde der angeforderte Vorgang nicht erfolgreich abgeschlossen.

#### <a name="remarks"></a>Bemerkungen

Der Versionsspeicher verwaltet den Momentaufnahmeisolationsmechanismus von ESE. Wenn der Versionsspeicher mehr als halb voll ist, schließt das Programm möglicherweise Langlauftransaktionen. Wenn der Versionsspeicher durch eine Transaktion mit langer Laufzeit erschöpft wird, lässt ESE keine Schreibvorgänge mehr für die Datenbank zu.

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)
