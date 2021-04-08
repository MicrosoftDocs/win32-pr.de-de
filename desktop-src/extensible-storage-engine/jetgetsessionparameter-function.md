---
description: 'Weitere Informationen zu: jetgeungessionparameter-Funktion'
title: Jetgeungessionparameter-Funktion
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
ms.openlocfilehash: f0ac02142d48009d668d903b39163b425d738b55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861932"
---
# <a name="jetgetsessionparameter-function"></a>Jetgeungessionparameter-Funktion


_**Gilt für:** Windows | Windows Server_

Die **jetgeungessionparameter** -Funktion liest den Sitzungs Parameter für die angegebene Sitzung.

Die **jetgezessionparameter** -Funktion wurde im Windows 8-Betriebssystem eingeführt.

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

*-sid*

Die Sitzung, die für diesen-Befehl verwendet werden soll.

Wenn angegeben, wird die angegebene-Instanz ignoriert, und die-Instanz, die der Sitzung zugeordnet ist, wird verwendet.

*sesparamid*

Die ID des festzulegenden Sitzungs Parameters.

*pvParam*

Daten in diesem Sitzungs Parameter.

*cbparammax*

Die maximale Größe des Datasets in diesem Sitzungs Parameter.

*pcbparamactual*

Die tatsächliche Größe des Datasets in diesem Sitzungs Parameter.

### <a name="return-value"></a>Rückgabewert

Bei Erfolg wird der für den angeforderten Sitzungs Parameter geeignete Ausgabepuffer auf den Wert dieses Sitzungs Parameters festgelegt.

Bei einem Fehler wird der Status der Ausgabepuffer nicht definiert.

#### <a name="remarks"></a>Bemerkungen

Der Session-Parameter wird für die Lebensdauer der Sitzung oder bis zum Zurücksetzen des Werts verwendet.

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

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[Jetkreateingestance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[Jetsetsystemparameter](./jetsetsystemparameter-function.md)  
[Jetstopservice](./jetstopservice-function.md)  
[System Parameter](./extensible-storage-engine-system-parameters.md)
