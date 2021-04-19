---
title: Ibackgroundcopyjob getnotifyinterface-Methode (deliveryoptimization. h)
description: Ruft den Schnittstellen Zeiger auf die Implementierung der ibackgroundcopycallback-Schnittstelle ab.
ms.assetid: 1AA50C03-AC84-4AA9-8EC3-3FBA865C70C0
keywords:
- Getnotifyinterface-Methode
- Getnotifyinterface-Methode, ibackgroundcopyjob-Schnittstelle
- Ibackgroundcopyjob-Schnittstelle, getnotifyinterface-Methode
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
ms.openlocfilehash: 6586a90de5783ceb24e5a7677f699a9cf6dfa60c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346340"
---
# <a name="ibackgroundcopyjobgetnotifyinterface-method"></a>Ibackgroundcopyjob:: getnotifyinterface-Methode

Ruft den Schnittstellen Zeiger auf die Implementierung der [**ibackgroundcopycallback**](ibackgroundcopycallback.md) -Schnittstelle ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetNotifyInterface(
  [out] IUnknown **ppNotifyInterface
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppnotifyinterface* \[ vorgenommen\]
</dt> <dd>

Ein Schnittstellen Zeiger auf Ihre Implementierung der [**ibackgroundcopycallback**](ibackgroundcopycallback.md) -Schnittstelle. Wenn Sie dies erledigt haben, Release *ppnotifyinterface*.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt sowohl die folgenden **HRESULT** -Werte als auch andere zurück.



| Rückgabecode                                                                              | Beschreibung                                                           |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | Der Benachrichtigungs Schnittstellen Zeiger wurde erfolgreich abgerufen.<br/> |



 

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

 

 





