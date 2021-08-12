---
title: IBackgroundCopyJob SetNoProgressTimeout-Methode (Deliveryoptimization.h)
description: Legt die Zeitspanne fest, die Übermittlungsoptimierung (DO) versucht, die Datei nach auftreten einer vorübergehenden Fehlerbedingung zu übertragen. Wenn ein Fortschritt vorliegt, wird der Timer zurückgesetzt.
ms.assetid: DC86F74F-8429-4D78-B425-CAF19867B05E
keywords:
- SetNoProgressTimeout-Methode
- SetNoProgressTimeout-Methode, IBackgroundCopyJob-Schnittstelle
- IBackgroundCopyJob-Schnittstelle, SetNoProgressTimeout-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetNoProgressTimeout
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dcf6905388d54103aaac34ae934c89e2fd8ccc16ce32a384eb730376606351b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542927"
---
# <a name="ibackgroundcopyjobsetnoprogresstimeout-method"></a>IBackgroundCopyJob::SetNoProgressTimeout-Methode

Legt die Zeitspanne fest, die Übermittlungsoptimierung (DO) versucht, die Datei nach auftreten einer vorübergehenden Fehlerbedingung zu übertragen. Wenn ein Fortschritt vorliegt, wird der Timer zurückgesetzt.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetNoProgressTimeout(
  [in] ULONG RetryPeriod
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*RetryPeriod* \[ In\]
</dt> <dd>

Die Zeitspanne in Sekunden, in der do versucht, die Datei zu übertragen, nachdem kein Fortschritt erzielt wurde. Der Standardwiederholungszeitraum für einen Auftrag mit hoher Priorität beträgt 3600 Sekunden (1 Stunde) und für einen Auftrag mit niedriger Priorität 86.400 Sekunden (24 Stunden).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt die folgenden **HRESULT-Werte** sowie andere zurück.



| Rückgabecode                                                                                          | Beschreibung                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK</dt> </dl>             | Der Wiederholungszeitraum wurde erfolgreich festgelegt.<br/>                                                            |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | Der Status des Auftrags kann nicht BG_JOB_STATE_CANCELLED oder BG_JOB_STATE_ACKNOWLEDGED werden.<br/> |



 

## <a name="remarks"></a>Hinweise

Wenn do während des Wiederholungszeitraums keinen Fortschritt macht, wird der Status des Auftrags von BG_JOB_STATE_TRANSIENT_ERROR in BG_JOB_STATE_ERROR verschoben. Wenn Sie eine Fehlerbenachrichtigung anfordern, rufen Sie den [**JobError-Rückruf**](https://www.bing.com/search?q=**JobError**) auf.

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



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IBackgroundCopyJob::GetNoProgressTimeout**](ibackgroundcopyjob-getnoprogresstimeout.md)
</dt> </dl>

 

 





