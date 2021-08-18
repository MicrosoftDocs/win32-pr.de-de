---
title: IBackgroundCopyJob GetNotifyInterface-Methode (Deliveryoptimization.h)
description: Ruft den Schnittstellenzeiger auf Ihre Implementierung der IBackgroundCopyCallback-Schnittstelle ab.
ms.assetid: 1AA50C03-AC84-4AA9-8EC3-3FBA865C70C0
keywords:
- GetNotifyInterface-Methode
- GetNotifyInterface-Methode, IBackgroundCopyJob-Schnittstelle
- IBackgroundCopyJob-Schnittstelle, GetNotifyInterface-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetNotifyInterface
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ef8eab6c101cadde2b715c48fe3dae2443e72e93f623b397036e2467bcbf0b5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755380"
---
# <a name="ibackgroundcopyjobgetnotifyinterface-method"></a>IBackgroundCopyJob::GetNotifyInterface-Methode

Ruft den Schnittstellenzeiger auf Ihre Implementierung der [**IBackgroundCopyCallback-Schnittstelle**](ibackgroundcopycallback.md) ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetNotifyInterface(
  [out] IUnknown **ppNotifyInterface
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppNotifyInterface* \[ out\]
</dt> <dd>

Schnittstellenzeiger auf Ihre Implementierung der [**IBackgroundCopyCallback-Schnittstelle.**](ibackgroundcopycallback.md) Wenn Sie fertig sind, geben *Sie ppNotifyInterface frei.*

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt die folgenden **HRESULT-Werte** sowie andere zurück.



| Rückgabecode                                                                              | Beschreibung                                                           |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>S_OK S_OK</dt> </dl> | Der Benachrichtigungsschnittstellenzeiger wurde erfolgreich abgerufen.<br/> |



 

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

[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)
</dt> <dt>

[**IBackgroundCopyJob::GetNotifyFlags**](ibackgroundcopyjob-getnotifyflags.md)
</dt> <dt>

[**IBackgroundCopyJob::SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md)
</dt> </dl>

 

 





