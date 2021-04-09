---
title: Ibackgroundcopyjob Cancel-Methode (deliveryoptimization. h)
description: Löscht den Auftrag aus der Übertragungs Warteschlange und entfernt zugehörige temporäre Dateien vom Client (Downloads) und Server (Uploads).
ms.assetid: DC502DC2-1335-476F-A1B8-FDB6BA595FF1
keywords:
- Cancel-Methode
- Cancel-Methode, ibackgroundcopyjob-Schnittstelle
- Ibackgroundcopyjob-Schnittstelle, Cancel-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Cancel
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f72cdcea82ef7db30de141af295bb74594a7a630
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858836"
---
# <a name="ibackgroundcopyjobcancel-method"></a>Ibackgroundcopyjob:: Cancel-Methode

Löscht den Auftrag aus der Übertragungs Warteschlange und entfernt zugehörige temporäre Dateien vom Client (Downloads) und Server (Uploads).

## <a name="syntax"></a>Syntax


```C++
HRESULT Cancel();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt sowohl die folgenden **HRESULT** -Werte als auch andere zurück.



| Rückgabecode                                                                                          | Beschreibung                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>             | Der Auftrag wurde erfolgreich abgebrochen.<br/>                                                                |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | Ein Auftrag, dessen Status BG_JOB_STATE_CANCELLED oder BG_JOB_STATE_ACKNOWLEDGED ist, kann nicht abgebrochen werden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Sie können einen Auftrag jederzeit abbrechen. der Auftrag kann jedoch nicht wieder hergestellt werden, nachdem er abgebrochen wurde.

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

[**Ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md)
</dt> <dt>

[**Ibackgroundcopyjob:: Resume**](ibackgroundcopyjob-resume.md)
</dt> <dt>

[**Ibackgroundcopyjob:: Suspend**](ibackgroundcopyjob-suspend.md)
</dt> </dl>

 

 





