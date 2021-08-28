---
description: Weitere Informationen zur JetGetInstanceInfo-Funktion
title: JetGetInstanceInfo-Funktion
TOCTitle: JetGetInstanceInfo Function
ms:assetid: ffccdac0-3631-4753-876a-90ddfdd0252f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294149(v=EXCHG.10)
ms:contentKeyID: 32765763
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetInstanceInfoW
- JetGetInstanceInfo
- JetGetInstanceInfoA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9dfc8bec0e6cee6e127dc99135d82db3ee3001ab
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478346"
---
# <a name="jetgetinstanceinfo-function"></a>JetGetInstanceInfo-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgetinstanceinfo-function"></a>JetGetInstanceInfo-Funktion

Die **JetGetInstanceInfo-Funktion** ruft Informationen zu den ausgeführten Instanzen ab.

**Windows XP: JetGetInstanceInfo** wird in Windows XP eingeführt.

```cpp
    JET_ERR JET_API JetGetInstanceInfo(
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo
    );
```

### <a name="parameters"></a>Parameter

*pcInstanceInfo*

Ein Zeiger auf einen Puffer, der die Anzahl der in *paInstanceInfo* gespeicherten Elemente empfängt.

*paInstanceInfo*

Ein Zeiger auf einen Puffer, der die Adresse des ersten Elements eines Arrays von Strukturen empfängt.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Einer der bereitgestellten Parameter enthielt einen unerwarteten Wert oder einen Wert, der in Kombination mit dem Wert eines anderen Parameters nicht sinnvoll war. Dieser Fehler wird von <strong>JetGetInstanceInfo</strong> zurückgegeben, wenn:</p><ul><li><p><em>pcInstanceInfo</em> oder <em>paInstanceInfo</em> sind NULL.</p></li></ul> | 
| <p>JET_errOutOfMemory</p> | <p>Es ist nicht genügend Arbeitsspeicher zum Verarbeiten der Anforderung vorhanden.</p> | 



#### <a name="remarks"></a>Hinweise

Die Datenbank-Engine ordnet ein Array von [JET_INSTANCE_INFO](./jet-instance-info-structure.md) Strukturen zu. Der Aufrufer ist dafür verantwortlich, diesen Arbeitsspeicher mit [JetFreeBuffer](./jetfreebuffer-function.md)freizugeben.

Wenn keine aktiven Instanzen vorhanden sind, gibt **JetGetInstanceInfo** JET_errSuccess zurück, und *pcInstanceInfo* erhält den Wert 0.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista oder Windows XP.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008 oder Windows Server 2003.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Wird als <strong>JetGetInstanceInfoW</strong> (Unicode) und <strong>JetGetInstanceInfoA</strong> (ANSI) implementiert.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_INSTANCE_INFO](./jet-instance-info-structure.md)  
[JetFreeBuffer](./jetfreebuffer-function.md)
