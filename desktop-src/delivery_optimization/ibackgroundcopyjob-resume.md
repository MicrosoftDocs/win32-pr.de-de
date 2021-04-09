---
title: Ibackgroundcopyjob Resume-Methode (deliveryoptimization. h)
description: Aktiviert einen neuen Auftrag oder startet einen Auftrag, der angehalten wurde, neu.
ms.assetid: B745BDA6-36B9-41FD-9737-61D14150A9E4
keywords:
- Resume-Methode
- Resume-Methode, ibackgroundcopyjob-Schnittstelle
- Ibackgroundcopyjob-Schnittstelle, Resume-Methode
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
ms.openlocfilehash: f87f5b5347785810d84331ce56f240cd1f016383
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103242"
---
# <a name="ibackgroundcopyjobresume-method"></a>Ibackgroundcopyjob:: Resume-Methode

Aktiviert einen neuen Auftrag oder startet einen Auftrag, der angehalten wurde, neu.

## <a name="syntax"></a>Syntax


```C++
HRESULT Resume();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt sowohl die folgenden **HRESULT** -Werte als auch andere zurück.



| Rückgabecode                                                                                          | Beschreibung                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>             | Der Auftrag wurde erfolgreich neu gestartet.<br/>                                                           |
| <dl> <dt>**DO_E_EMPTY**</dt> </dl>          | Es sind keine zu übertragenden Dateien vorhanden.<br/>                                                           |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | Der Status des Auftrags kann nicht BG_JOB_STATE_CANCELLED oder BG_JOB_STATE_ACKNOWLEDGED sein.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Auftrag erstellen, wird der Auftrag anfänglich angehalten. Durch Aufrufen von **Resume** wird der Auftrag in den Übertragungs Zustand versetzt. Beachten Sie, dass der Auftrag vor dem Aufrufen dieser Methode eine oder mehrere Dateien enthalten muss.

Wenn ein Auftrag im Status BG_JOB_STATE_TRANSIENT_ERROR oder BG_JOB_STATE_ERROR ist, wird die **Resume** -Methode aufgerufen, um den Auftrag neu zu starten, nachdem Sie den Fehler behoben haben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1709, \[ nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, Version 1709, \[ nur Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Deliveryoptimization. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob ist als 37668d37-507E-4160-9316-26306d150b12 definiert.<br/>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**Ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[**Ibackgroundcopyjob:: Suspend**](ibackgroundcopyjob-suspend.md)
</dt> </dl>

 

 





