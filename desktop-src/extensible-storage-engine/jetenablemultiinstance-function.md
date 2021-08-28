---
description: 'Weitere Informationen zu: JetEnableMultiInstance-Funktion'
title: JetEnableMultiInstance-Funktion
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
ms.openlocfilehash: 618552b01a4702790fca0d234ee40aff0de39f45
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481366"
---
# <a name="jetenablemultiinstance-function"></a>JetEnableMultiInstance-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetenablemultiinstance-function"></a>JetEnableMultiInstance-Funktion

Die **JetEnableMultiInstance-Funktion** konfiguriert die Datenbank-Engine für die Verwendung mit mehreren Instanzen im gleichen Prozess. Dem ersten Aufrufer steht ein optionales Array globaler Systemparameter zur Verfügung, das die Umstellung auf den Modus mit mehreren Instanzen ermöglicht.

**Windows XP: JetEnableMultiInstance** wird in Windows XP eingeführt.

```cpp
    JET_ERR JET_API JetEnableMultiInstance(
      __in_opt      JET_SETSYSPARAM* psetsysparam,
      __in_opt      unsigned long csetsysparam,
      __out_opt     unsigned long* pcsetsucceed
    );
```

### <a name="parameters"></a>Parameter

*psetsysparam*

Ein Array globaler Systemparameter, das nur dann festgelegt werden soll, wenn die Engine aufgrund dieses Aufrufs in den Modus mit mehreren Instanzen wechselt. Wenn *csetsysparam 0* (null) ist, wird *psetsysparam* ignoriert.

*csetsysparam*

Die Anzahl der Elemente für das Array von globalen Parametern, die nur dann festgelegt werden sollen, wenn die Engine aufgrund dieses Aufrufs in den Modus mit mehreren Instanzen wechselt. Wenn *csetsysparam 0* (null) ist, wird *psetsysparam* ignoriert.

*pcsetsucceed*

Ein Zeiger auf die Anzahl der globalen Systemparameter, die als Ergebnis dieses Aufrufs erfolgreich konfiguriert wurden.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errIndexTuplesInvalidLimits</p> | <p>Die angegebenen Tupelindexparameter waren nicht zulässig. Dieser Fehler kann von <strong>JetEnableMultiInstance</strong> nur zurückgegeben werden, wenn <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMin</a>, <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>oder <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesToIndexMax</a> auf einen ungültigen Wert festgelegt wird.</p><p><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</p> | 
| <p>JET_errInvalidPath</p> | <p>Der angegebene Dateisystempfad war ungültig. Dieser Fehler kann von <strong>JetEnableMultiInstance</strong> nur zurückgegeben werden, wenn Systemparameter festgelegt werden, die Dateisystempfade darstellen. Beispielsweise kann <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> diesen Fehler zurückgeben.</p> | 
| <p>JET_errRunningInOneInstanceMode</p> | <p>Fehler beim Vorgang, weil er ungültig ist, wenn die Datenbank-Engine im Einzelinstanzmodus (Windows 2000-Kompatibilitätsmodus) ausgeführt wird.</p> | 
| <p>JET_errSystemParamsAlreadySet</p> | <p>Fehler bei <strong>JetEnableMultiInstance,</strong> weil sich die Engine bereits im Modus mit mehreren Instanzen befindet.</p><p><strong>Hinweis  </strong> Dies geschieht auch, wenn keine Systemparameter angegeben werden.</p> | 



Wenn diese Funktion erfolgreich ausgeführt wird, wird die Datenbank-Engine für die Ausführung im Modus mit mehreren Instanzen konfiguriert. Die Engine wurde auch erfolgreich mit der optionalen Liste der globalen Systemparameter konfiguriert.

Wenn diese Funktion fehlschlägt, verbleibt die Datenbank-Engine im aktuellen Modus. Wenn *pcsetsucceed* ungleich 0 (null) ist, bleibt diese Anzahl von Systemparametern festgelegt.

#### <a name="remarks"></a>Hinweise

Diese Funktion sollte nur verwendet werden, wenn die Anwendung einen bestimmten Satz von Systemparametern atomisch konfigurieren muss, wenn die Datenbank-Engine für die Verwendung in einem Szenario mit mehreren Benutzern im gleichen Prozess eingerichtet wird. Wenn eine andere Synchronisierungsmethode verfügbar ist, ist es besser, [JetCreateInstance](./jetcreateinstance-function.md) und [JetSetSystemParameter](./jetsetsystemparameter-function.md) separat aufzurufen.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista oder Windows XP.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008 oder Windows Server 2003.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementiert als <strong>JetEnableMultiInstanceW</strong> (Unicode) und <strong>JetEnableMultiInstanceA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_SETSYSPARAM](./jet-setsysparam-structure.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
