---
title: IBackgroundCopyJob GetState-Methode (Deliveryoptimization.h)
description: Ruft den Status des Auftrags ab.
ms.assetid: 975AF0FB-37AE-4CE8-9EC1-35A972E422D8
keywords:
- GetState-Methode
- GetState-Methode, IBackgroundCopyJob-Schnittstelle
- IBackgroundCopyJob-Schnittstelle, GetState-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetState
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 64a26d1cc301230a9bb8330b9a2b2daf3178b1538ec95f593cd5e3f4d3099d7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755300"
---
# <a name="ibackgroundcopyjobgetstate-method"></a>IBackgroundCopyJob::GetState-Methode

Ruft den Status des Auftrags ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetState(
  [out] BG_JOB_STATE *pJobState
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pJobState* \[ out\]
</dt> <dd>

Der Status des Auftrags. Der Status gibt beispielsweise an, ob der Auftrag einen Fehler auft, Daten übertragen oder angehalten hat. Eine Liste der Auftragszustände finden Sie in [**der**](bg-job-state-.md) BG_JOB_STATE Enumeration.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt die folgenden **HRESULT-Werte** sowie andere zurück.



| Rückgabecode                                                                              | Beschreibung                                                 |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>S_OK S_OK</dt> </dl> | Der Status des Auftrags wurde erfolgreich abgerufen.<br/> |



 

## <a name="remarks"></a>Hinweise

Wenn Sie wissen möchten, wann ein Auftrag einen Fehler aufwiesen oder alle Dateien im Auftrag übertragen hat, können Sie diese Methode verwenden, um den Status des Auftrags zu erhalten, oder Sie können sich registrieren, um Benachrichtigungen zu erhalten, wenn Ereignisse auftreten. Weitere Informationen zum Registrieren für den Empfang von Ereignisbenachrichtigungen finden Sie auf der [**IBackgroundCopyCallback-Schnittstelle.**](ibackgroundcopycallback.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10 Desktop-Apps, Version 1709 \[\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob ist als 37668D37-507E-4160-9316-26306D150B12 definiert.<br/>               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**BG_JOB_STATE**](bg-job-state-.md)
</dt> <dt>

[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)
</dt> </dl>

 

 





