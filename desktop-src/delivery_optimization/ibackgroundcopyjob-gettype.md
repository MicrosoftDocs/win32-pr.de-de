---
title: Ibackgroundcopyjob GetType-Methode (deliveryoptimization. h)
description: Ruft den Übertragungstyp ab, wie z. b. das herunterladen oder Hochladen von Dateien.
ms.assetid: F543A601-9385-4A73-A4E2-DE61433E84D3
keywords:
- GetType-Methode
- GetType-Methode, ibackgroundcopyjob-Schnittstelle
- Ibackgroundcopyjob-Schnittstelle, GetType-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetType
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5b0a09a3c7387b5b911bf6731921e7ed4e9b9163
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040253"
---
# <a name="ibackgroundcopyjobgettype-method"></a>Ibackgroundcopyjob:: GetType-Methode

Ruft den Übertragungstyp ab, wie z. b. das herunterladen oder Hochladen von Dateien.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetType(
  [out] BG_JOB_TYPE *pJobType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pjobtype* \[ vorgenommen\]
</dt> <dd>

Der Übertragungstyp, der ausgeführt wird. Eine Liste der Übertragungs Typen finden Sie in der [**BG_JOB_TYPE**](bg-job-type.md) -Enumeration.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt sowohl die folgenden **HRESULT** -Werte als auch andere zurück.



| Rückgabecode                                                                              | Beschreibung                                          |
|------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | Der Übertragungstyp wurde erfolgreich abgerufen.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Geben Sie den Übertragungstyp beim Erstellen des Auftrags an.

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

[**BG_JOB_TYPE**](bg-job-type.md)
</dt> <dt>

[**Ibackgroundcopymanager:: kreatejob**](ibackgroundcopymanager-createjob.md)
</dt> </dl>

 

 





