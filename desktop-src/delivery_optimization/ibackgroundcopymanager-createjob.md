---
title: IBackgroundCopyManager CreateJob-Methode (Deliveryoptimization.h)
description: Erstellt einen Auftrag.
ms.assetid: BDE5BE4D-9AE9-463D-B900-850D255EAB58
keywords:
- CreateJob-Methode
- CreateJob-Methode, IBackgroundCopyManager-Schnittstelle
- IBackgroundCopyManager-Schnittstelle, CreateJob-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyManager.CreateJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 165b0a74f71ee5267fb3bd300baec4e48c51662b33c83203ebae1ba462f10a0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953560"
---
# <a name="ibackgroundcopymanagercreatejob-method"></a>IBackgroundCopyManager::CreateJob-Methode

Erstellt einen Auftrag.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateJob(
  [in]  LPCWSTR            pDisplayName,
  [in]  BG_JOB_TYPE        Type,
  [out] GUID               *pJobID,
  [out] IBackgroundCopyJob **ppJob
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDisplayName* \[ In\]
</dt> <dd>

Auf NULL endende Zeichenfolge, die einen Anzeigenamen für den Auftrag enthält. In der Regel wird der Anzeigename verwendet, um den Auftrag auf einer Benutzeroberfläche zu identifizieren. Beachten Sie, dass mehr als ein Auftrag den gleichen Anzeigenamen aufweisen kann. Darf nicht **NULL** sein. Der Name ist auf 256 Zeichen beschränkt, ohne das NULL-Abschlusszeichen.

</dd> <dt>

*Typ* \[ In\]
</dt> <dd>

Typ des Übertragungsauftrags, z. B. BG_JOB_TYPE_DOWNLOAD. Eine Liste der Übertragungstypen [](bg-job-type.md) finden Sie in der BG_JOB_TYPE-Enumeration.

</dd> <dt>

*pJobID* \[ out\]
</dt> <dd>

Identifiziert Ihren Auftrag eindeutig in der Warteschlange. Verwenden Sie diesen Bezeichner, wenn Sie die [**IBackgroundCopyManager::GetJob-Methode**](ibackgroundcopymanager-getjob.md) aufrufen, um einen Auftrag aus der Warteschlange abzurufen.

</dd> <dt>

*ppJob* \[ out\]
</dt> <dd>

Ein [**IBackgroundCopyJob-Schnittstellenzeiger,**](ibackgroundcopyjob-.md) mit dem Sie die Eigenschaften des Auftrags ändern und die zu übertragenden Dateien angeben. Um den Auftrag in der Warteschlange zu aktivieren, rufen Sie die [**IBackgroundCopyJob::Resume-Methode**](ibackgroundcopyjob-resume.md) auf. Veröffentlichen Sie *ppJob,* wenn Sie fertig sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt die folgenden **HRESULT-Werte** sowie andere zurück.



| Rückgabecode                                                                              | Beschreibung                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>S_OK</dt> </dl> | Der neue Auftrag wurde erfolgreich generiert.<br/> |



 

## <a name="remarks"></a>Hinweise

Nur der Benutzer, der den Auftrag erstellt, oder ein Benutzer mit Administratorrechten kann [dem Auftrag Dateien hinzufügen](https://www.bing.com/search?q=add+files+to+the+job) und die Eigenschaften des Auftrags [ändern.](https://www.bing.com/search?q=change+the+job's+properties)

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IBackgroundCopyManager**](ibackgroundcopymanager.md)
</dt> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IBackgroundCopyJob::Resume**](ibackgroundcopyjob-resume.md)
</dt> </dl>
