---
description: Weitere Informationen finden Sie unter JetGetSessionParameter-Funktion.
title: JetGetSessionParameter-Funktion
TOCTitle: JetGetSessionParameter Function
ms:assetid: 36fbcc06-a72d-4bfb-976b-1b705487732a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835039(v=EXCHG.10)
ms:contentKeyID: 49894661
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetGetSessionParameter
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 183169f8356a664b450e74534558286607fed62c
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984773"
---
# <a name="jetgetsessionparameter-function"></a>JetGetSessionParameter-Funktion


_**Gilt für:** Windows | Windows Server_

Die **JetGetSessionParameter-Funktion** liest den Sitzungsparameter für die gegebene Sitzung.

Die **JetGetSessionParameter-Funktion** wurde im Windows 8 eingeführt.

``` c++
JET_ERR JET_API JetGetSessionParameter (
  __in_opt      JET_SESID sesid,
  __in          unsigned long sesparamid,
  __out_cap_post_count_(cbParamMax, *pcbParamActual)  void* pvParam,
  __in          unsigned long cbParamMax,
  __out_opt_    unsigned long pcbParamActual
);
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die für diesen Aufruf verwendet werden soll.

Wenn angegeben, wird die angegebene -Instanz ignoriert, und die der Sitzung zugeordnete -Instanz wird verwendet.

*sespartrenn*

Die ID des sitzungsparameters, der festgelegt werden soll.

*pvParam*

Daten in diesem Sitzungsparameter.

*cbParamMax*

Die maximale Größe des DataSets in diesem Sitzungsparameter.

*-ParamActual*

Die tatsächliche Größe des DataSets in diesem Sitzungsparameter.

### <a name="return-value"></a>Rückgabewert

Bei Erfolg wird der für den angeforderten Sitzungsparameter geeignete Ausgabepuffer auf den Wert dieses Sitzungsparameters festgelegt.

Bei einem Fehler ist der Status der Ausgabepuffer nicht definiert.

#### <a name="remarks"></a>Bemerkungen

Der Sitzungsparameter wird für die Lebensdauer der Sitzung oder bis zum Zurücksetzen des Werts verwendet.

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows 8.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2012.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Siehe auch

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Systemparameter](./extensible-storage-engine-system-parameters.md)
