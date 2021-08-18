---
title: IBackgroundCopyJob GetTimes-Methode (Deliveryoptimization.h)
description: Ruft auftragsbezogene Zeitstempel ab, z. B. den Zeitpunkt, zu dem der Auftrag erstellt oder zuletzt geändert wurde.
ms.assetid: 9002FB8D-08CB-4878-980F-15FE0DC952A6
keywords:
- GetTimes-Methode
- GetTimes-Methode, IBackgroundCopyJob-Schnittstelle
- IBackgroundCopyJob-Schnittstelle, GetTimes-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetTimes
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3179342630fe932dd55efc4e75e15cd06a879d6cdc93005981cc7e0ebca7e05c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755210"
---
# <a name="ibackgroundcopyjobgettimes-method"></a>IBackgroundCopyJob::GetTimes-Methode

Ruft auftragsbezogene Zeitstempel ab, z. B. den Zeitpunkt, zu dem der Auftrag erstellt oder zuletzt geändert wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetTimes(
  [out] BG_JOB_TIMES *pTimes
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pTimes* \[ out\]
</dt> <dd>

Enthält auftragsbezogene Zeitstempel. Informationen zu verfügbaren Zeitstempeln finden Sie in der [**BG_JOB_TIMES-Struktur.**](bg-job-times.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt die folgenden **HRESULT-Werte** sowie andere zurück.



| Rückgabecode                                                                              | Beschreibung                                         |
|------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>S_OK</dt> </dl> | Zeitstempel wurden erfolgreich abgerufen.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, nur Desktop-Apps der Version 1709 \[\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, nur Desktop-Apps der Version 1709 \[\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob ist als 37668D37-507E-4160-9316-26306D150B12 definiert.<br/>               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**BG_JOB_TIMES**](bg-job-times.md)
</dt> </dl>

 

 





