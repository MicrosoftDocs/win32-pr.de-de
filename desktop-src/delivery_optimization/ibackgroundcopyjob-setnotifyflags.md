---
title: IBackgroundCopyJob SetNotifyFlags-Methode (Deliveryoptimization.h)
description: Gibt den Typ der Ereignisbenachrichtigung an, die Sie empfangen möchten, z. B. ereignisse, die vom Auftrag übertragen werden sollen.
ms.assetid: 19E626A5-6B6E-44E0-BD6F-43F132F32890
keywords:
- SetNotifyFlags-Methode
- SetNotifyFlags-Methode, IBackgroundCopyJob-Schnittstelle
- IBackgroundCopyJob-Schnittstelle, SetNotifyFlags-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetNotifyFlags
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cdb1750391027163a7ac8fb9ba8cc20085a06d187de0d7f05850641a5a774b18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542917"
---
# <a name="ibackgroundcopyjobsetnotifyflags-method"></a>IBackgroundCopyJob::SetNotifyFlags-Methode

Gibt den Typ der Ereignisbenachrichtigung an, die Sie empfangen möchten, z. B. ereignisse, die vom Auftrag übertragen werden sollen.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetNotifyFlags(
  [in] ULONG NotifyFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NotifyFlags* \[ In\]
</dt> <dd>

Legen Sie mindestens eines der folgenden Flags fest, um die Ereignisse zu identifizieren, die Sie empfangen möchten.



| Wert                                                                                                                                                                                                                                                                                    | Bedeutung                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BG_NOTIFY_JOB_TRANSFERRED"></span><span id="bg_notify_job_transferred"></span><dl> <dt>**BG_NOTIFY_JOB_TRANSFERRED**</dt> <dt>0x0001</dt> </dl>                          | Alle Dateien im Auftrag wurden übertragen.<br/>                                                                                                                                                          |
| <span id="BG_NOTIFY_JOB_ERROR"></span><span id="bg_notify_job_error"></span><dl> <dt>**BG_NOTIFY_JOB_ERROR**</dt> <dt>0x0002</dt> </dl>                                            | Es ist ein Fehler aufgetreten.<br/>                                                                                                                                                                                      |
| <span id="BG_NOTIFY_DISABLE"></span><span id="bg_notify_disable"></span><dl> <dt>**BG_NOTIFY_DISABLE**</dt> <dt>0x0004</dt> </dl>                                                   | Wird nicht unterstützt.<br/>                                                                                                                                                                                              |
| <span id="BG_NOTIFY_JOB_MODIFICATION"></span><span id="bg_notify_job_modification"></span><dl> <dt>**BG_NOTIFY_JOB_MODIFICATION**</dt> <dt>0x0008</dt> </dl>                       | Der Auftrag wurde geändert. Beispielsweise wurde ein Eigenschaftswert geändert, der Status des Auftrags geändert, oder der Fortschritt wird beim Übertragen der Dateien ausgeführt. Dieses Flag wird ignoriert, wenn eine Befehlszeilenbenachrichtigung angegeben wird.<br/> |
| <span id="BG_NOTIFY_FILE_TRANSFERRED"></span><span id="bg_notify_file_transferred"></span><dl> <dt>**BG_NOTIFY_FILE_TRANSFERRED**</dt> <dt>0x0010</dt> </dl>                       | Eine Datei im Auftrag wurde übertragen. Dieses Flag wird ignoriert, wenn eine Befehlszeilenbenachrichtigung angegeben wird.<br/>                                                                                                     |
| <span id="BG_NOTIFY_FILE_RANGES_TRANSFERRED"></span><span id="bg_notify_file_ranges_transferred"></span><dl> <dt>**BG_NOTIFY_FILE_RANGES_TRANSFERRED**</dt> <dt>0x0020</dt> </dl> | Wird nicht unterstützt.<br/>                                                                                                                                                                                              |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt die folgenden **HRESULT-Werte** sowie andere zurück.



| Rückgabecode                                                                                          | Beschreibung                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK</dt> </dl>             | Der Typ der Ereignisbenachrichtigung wurde erfolgreich festgelegt.<br/>                                          |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | Der Status des Auftrags kann nicht BG_JOB_STATE_CANCELLED oder BG_JOB_STATE_ACKNOWLEDGED werden.<br/> |



 

## <a name="remarks"></a>Hinweise

Verwenden Sie die **SetNotifyFlags-Methode** in Verbindung mit [**IBackgroundCopyJob::SetNotifyInterface.**](ibackgroundcopyjob-setnotifyinterface.md)

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

[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)
</dt> <dt>

[**IBackgroundCopyJob::GetNotifyFlags**](ibackgroundcopyjob-getnotifyflags.md)
</dt> <dt>

[**IBackgroundCopyJob::SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md)
</dt> </dl>

 

 





