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
ms.openlocfilehash: 7953c2359d651d1bb6c9d5a006c02d9b19de6662
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477916"
---
# <a name="jetgetsessionparameter-function"></a>JetGetSessionParameter-Funktion


_**Gilt für:** Windows | Windows Server_

Die **JetGetSessionParameter-Funktion** liest den Sitzungsparameter für die angegebene Sitzung.

Die **JetGetSessionParameter-Funktion** wurde im Windows 8 Betriebssystem eingeführt.

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

Wenn angegeben, wird die angegebene Instanz ignoriert, und die der Sitzung zugeordnete Instanz wird verwendet.

*sesparbor*

Die ID des festzulegende Sitzungsparameters.

*pvParam*

Daten in diesem Sitzungsparameter.

*cbParamMax*

Die maximale Größe des Datasets in diesem Sitzungsparameter.

*pwParamActual*

Die tatsächliche Größe des Datasets in diesem Sitzungsparameter.

### <a name="return-value"></a>Rückgabewert

Bei Erfolg wird der für den angeforderten Sitzungsparameter geeignete Ausgabepuffer auf den Wert dieses Sitzungsparameters festgelegt.

Bei einem Fehler ist der Status der Ausgabepuffer nicht definiert.

#### <a name="remarks"></a>Hinweise

Der Sitzungsparameter wird für die Lebensdauer der Sitzung oder bis zum Zurücksetzen des Werts verwendet.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows 8.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2012.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Systemparameter](./extensible-storage-engine-system-parameters.md)
