---
title: Ibackgroundcopyjob GetState-Methode (deliveryoptimization. h)
description: Ruft den Status des Auftrags ab.
ms.assetid: 975AF0FB-37AE-4CE8-9EC1-35A972E422D8
keywords:
- GetState-Methode
- GetState-Methode, ibackgroundcopyjob-Schnittstelle
- Ibackgroundcopyjob-Schnittstelle, GetState-Methode
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
ms.openlocfilehash: 5b195377a44cab8f336bae8090bacc5ca5624d7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741720"
---
# <a name="ibackgroundcopyjobgetstate-method"></a>Ibackgroundcopyjob:: GetState-Methode

Ruft den Status des Auftrags ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetState(
  [out] BG_JOB_STATE *pJobState
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pjobstate* \[ vorgenommen\]
</dt> <dd>

Der Status des Auftrags. Der Status gibt beispielsweise an, ob der Auftrag fehlerhaft ist, Daten überträgt oder angehalten wird. Eine Liste der Auftrags Zustände finden Sie in der [**BG_JOB_STATE**](bg-job-state-.md) -Enumeration.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt sowohl die folgenden **HRESULT** -Werte als auch andere zurück.



| Rückgabecode                                                                              | Beschreibung                                                 |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | Der Status des Auftrags wurde erfolgreich abgerufen.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Wenn Sie wissen möchten, ob ein Auftrag fehlerhaft ist oder alle Dateien im Auftrag übertragen haben, können Sie diese Methode verwenden, um den Status des Auftrags abzurufen, oder Sie können sich registrieren, um eine Benachrichtigung zu erhalten, wenn Ereignisse auftreten. Ausführliche Informationen zum Registrieren von für den Empfang von Ereignis Benachrichtigungen finden Sie unter [**ibackgroundcopycallback**](ibackgroundcopycallback.md) -Schnittstelle.

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

[**BG_JOB_STATE**](bg-job-state-.md)
</dt> <dt>

[**Ibackgroundcopycallback**](ibackgroundcopycallback.md)
</dt> </dl>

 

 





