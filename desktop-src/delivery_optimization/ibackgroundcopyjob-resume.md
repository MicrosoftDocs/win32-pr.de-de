---
title: IBackgroundCopyJob Resume-Methode (Deliveryoptimization.h)
description: Aktiviert einen neuen Auftrag oder startet einen Auftrag neu, der angehalten wurde.
ms.assetid: B745BDA6-36B9-41FD-9737-61D14150A9E4
keywords:
- Resume-Methode
- Resume-Methode, IBackgroundCopyJob-Schnittstelle
- IBackgroundCopyJob-Schnittstelle, Resume-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Resume
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fa4bd9a98626b7f26fc4ac9968d27d54604b5db56539eb383bb8aff696b2a561
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543006"
---
# <a name="ibackgroundcopyjobresume-method"></a>IBackgroundCopyJob::Resume-Methode

Aktiviert einen neuen Auftrag oder startet einen Auftrag neu, der angehalten wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT Resume();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt die folgenden **HRESULT-Werte** sowie andere zurück.



| Rückgabecode                                                                                          | Beschreibung                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK</dt> </dl>             | Der Auftrag wurde erfolgreich neu gestartet.<br/>                                                           |
| <dl> <dt>**DO_E_EMPTY**</dt> </dl>          | Es sind keine zu übertragenden Dateien vorhanden.<br/>                                                           |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | Der Status des Auftrags kann nicht BG_JOB_STATE_CANCELLED oder BG_JOB_STATE_ACKNOWLEDGED werden.<br/> |



 

## <a name="remarks"></a>Hinweise

Wenn Sie einen Auftrag erstellen, wird der Auftrag zunächst angehalten. Durch Aufrufen von **Resume** wird der Auftrag in den Zustand Übertragen versetzt. Beachten Sie, dass der Auftrag eine oder mehrere Dateien enthalten muss, bevor diese Methode aufgerufen wird.

Wenn sich ein Auftrag im BG_JOB_STATE_TRANSIENT_ERROR- oder BG_JOB_STATE_ERROR-Zustand befindet, rufen Sie die **Resume-Methode** auf, um den Auftrag neu zu starten, nachdem Sie den Fehler behoben haben.

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

[**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[**IBackgroundCopyJob::Suspend**](ibackgroundcopyjob-suspend.md)
</dt> </dl>

 

 





