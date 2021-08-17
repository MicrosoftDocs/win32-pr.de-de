---
title: IBackgroundCopyManager GetJob-Methode (Deliveryoptimization.h)
description: Ruft einen angegebenen Auftrag aus der Übertragungswarteschlange ab. In der Regel wird die Auftrags-ID von Ihrer Anwendung beibehalten, sodass Sie den Auftrag später aus der Warteschlange abrufen können.
ms.assetid: ED551A6B-66C7-47E9-93DA-E231BD637522
keywords:
- GetJob-Methode
- GetJob-Methode, IBackgroundCopyManager-Schnittstelle
- IBackgroundCopyManager-Schnittstelle, GetJob-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyManager.GetJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d8d05b496eaa0d6f1520f22efeed8a39af5eb8e4c338457e18c65a7913489472
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542288"
---
# <a name="ibackgroundcopymanagergetjob-method"></a>IBackgroundCopyManager::GetJob-Methode

Ruft einen angegebenen Auftrag aus der Übertragungswarteschlange ab. In der Regel wird die Auftrags-ID von Ihrer Anwendung beibehalten, sodass Sie den Auftrag später aus der Warteschlange abrufen können.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetJob(
  [in]  REFGUID            JobID,
  [out] IBackgroundCopyJob **ppJob
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*JobID* \[ In\]
</dt> <dd>

Identifiziert den Auftrag, der aus der Übertragungswarteschlange abgerufen werden soll. Die [**CreateJob-Methode**](ibackgroundcopymanager-createjob.md) gibt den Auftragsbezeichner zurück.

</dd> <dt>

*ppJob* \[ out\]
</dt> <dd>

Ein [**IBackgroundCopyJob-Schnittstellenzeiger**](ibackgroundcopyjob-.md) auf den durch *JobID* angegebenen Auftrag. Wenn Sie fertig sind, geben Sie *ppJob frei.*

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt die folgenden **HRESULT-Werte** sowie andere zurück.



| Rückgabecode                                                                                      | Beschreibung                                                        |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>S_OK</dt> </dl>         | Der Auftrag wurde erfolgreich aus der Übertragungswarteschlange abgerufen.<br/> |
| <dl> <dt>**DO_E_NOT_FOUND**</dt> </dl> | Der Auftrag wurde nicht in der Warteschlange gefunden.<br/>                     |
| <dl> <dt>**E_ACCESSDENIED**</dt> </dl>   | Der Benutzer verfügt nicht über die Berechtigung zum Abrufen des Auftrags.<br/>      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, nur Desktop-Apps der Version 1709 \[\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, nur Desktop-Apps der Version 1709 \[\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyManager ist als 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C definiert.<br/>           |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IBackgroundCopyManager**](ibackgroundcopymanager.md)
</dt> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IBackgroundCopyJob::GetId**](ibackgroundcopyjob-getid.md)
</dt> <dt>

[**IBackgroundCopyManager::CreateJob**](ibackgroundcopymanager-createjob.md)
</dt> </dl>

 

 





