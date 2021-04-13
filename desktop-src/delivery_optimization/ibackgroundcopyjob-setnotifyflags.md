---
title: Ibackgroundcopyjob setnotifyflags-Methode (deliveryoptimization. h)
description: Gibt den Typ der Ereignis Benachrichtigung an, die Sie empfangen möchten, z. b. Ereignisse, die übertragen werden.
ms.assetid: 19E626A5-6B6E-44E0-BD6F-43F132F32890
keywords:
- Setnotifyflags-Methode
- Setnotifyflags-Methode, ibackgroundcopyjob-Schnittstelle
- Ibackgroundcopyjob-Schnittstelle, setnotifyflags-Methode
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
ms.openlocfilehash: ea754eeafca8f0efdcad5545cfc3a462c8b508cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517849"
---
# <a name="ibackgroundcopyjobsetnotifyflags-method"></a>Ibackgroundcopyjob:: setnotifyflags-Methode

Gibt den Typ der Ereignis Benachrichtigung an, die Sie empfangen möchten, z. b. Ereignisse, die übertragen werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetNotifyFlags(
  [in] ULONG NotifyFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Notifyflags* \[ in\]
</dt> <dd>

Legen Sie mindestens eines der folgenden Flags fest, um die Ereignisse zu identifizieren, die Sie empfangen möchten.



| Wert                                                                                                                                                                                                                                                                                    | Bedeutung                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BG_NOTIFY_JOB_TRANSFERRED"></span><span id="bg_notify_job_transferred"></span><dl> <dt>**BG_NOTIFY_JOB_TRANSFERRED**</dt> <dt>0x0001</dt> </dl>                          | Alle Dateien im Auftrag wurden übertragen.<br/>                                                                                                                                                          |
| <span id="BG_NOTIFY_JOB_ERROR"></span><span id="bg_notify_job_error"></span><dl> <dt>**BG_NOTIFY_JOB_ERROR**</dt> <dt>0x0002</dt> </dl>                                            | Es ist ein Fehler aufgetreten.<br/>                                                                                                                                                                                      |
| <span id="BG_NOTIFY_DISABLE"></span><span id="bg_notify_disable"></span><dl> <dt>**BG_NOTIFY_DISABLE**</dt> <dt>0x0004</dt> </dl>                                                   | Wird nicht unterstützt.<br/>                                                                                                                                                                                              |
| <span id="BG_NOTIFY_JOB_MODIFICATION"></span><span id="bg_notify_job_modification"></span><dl> <dt>**BG_NOTIFY_JOB_MODIFICATION**</dt> <dt>0x0008</dt> </dl>                       | Der Auftrag wurde geändert. Beispielsweise wird ein Eigenschafts Wert geändert, der Status des Auftrags geändert, oder der Fortschritt wird durch das übertragen der Dateien durchgeführt. Dieses Flag wird ignoriert, wenn eine Befehlszeilen Benachrichtigung angegeben wird.<br/> |
| <span id="BG_NOTIFY_FILE_TRANSFERRED"></span><span id="bg_notify_file_transferred"></span><dl> <dt>**BG_NOTIFY_FILE_TRANSFERRED**</dt> <dt>0x0010</dt> </dl>                       | Eine Datei im Auftrag wurde übertragen. Dieses Flag wird ignoriert, wenn eine Befehlszeilen Benachrichtigung angegeben wird.<br/>                                                                                                     |
| <span id="BG_NOTIFY_FILE_RANGES_TRANSFERRED"></span><span id="bg_notify_file_ranges_transferred"></span><dl> <dt>**BG_NOTIFY_FILE_RANGES_TRANSFERRED**</dt> <dt>0x0020</dt> </dl> | Wird nicht unterstützt.<br/>                                                                                                                                                                                              |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt sowohl die folgenden **HRESULT** -Werte als auch andere zurück.



| Rückgabecode                                                                                          | Beschreibung                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>             | Der Typ der Ereignis Benachrichtigung wurde erfolgreich festgelegt.<br/>                                          |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | Der Status des Auftrags kann nicht BG_JOB_STATE_CANCELLED oder BG_JOB_STATE_ACKNOWLEDGED sein.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **setnotifyflags** -Methode in Verbindung mit der [**ibackgroundcopyjob:: setnotifyinterface**](ibackgroundcopyjob-setnotifyinterface.md)-Methode.

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

[**Ibackgroundcopycallback**](ibackgroundcopycallback.md)
</dt> <dt>

[**Ibackgroundcopyjob:: getnotifyflags**](ibackgroundcopyjob-getnotifyflags.md)
</dt> <dt>

[**Ibackgroundcopyjob:: setnotifyinterface**](ibackgroundcopyjob-setnotifyinterface.md)
</dt> </dl>

 

 





