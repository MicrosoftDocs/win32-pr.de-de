---
title: Ibackgroundcopyjob SetPriority-Methode (deliveryoptimization. h)
description: Gibt die Prioritätsstufe des Auftrags an. Die Prioritätsstufe bestimmt, wann der Auftrag in Bezug auf andere Aufträge in der Übertragungs Warteschlange verarbeitet wird.
ms.assetid: DC943093-CA1D-4840-B7AC-29710764D4E5
keywords:
- SetPriority-Methode
- SetPriority-Methode, ibackgroundcopyjob-Schnittstelle
- Ibackgroundcopyjob-Schnittstelle, SetPriority-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetPriority
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6fb6407c5d693a2c6e75f8aaf8f7a0544d08cdec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741713"
---
# <a name="ibackgroundcopyjobsetpriority-method"></a>Ibackgroundcopyjob:: SetPriority-Methode

Gibt die Prioritätsstufe des Auftrags an. Die Prioritätsstufe bestimmt, wann der Auftrag in Bezug auf andere Aufträge in der Übertragungs Warteschlange verarbeitet wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetPriority(
  [in] BG_JOB_PRIORITY Priority
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Priorität* \[ in\]
</dt> <dd>

Gibt die Prioritätsstufe Ihres Auftrags in Relation zu anderen Aufträgen in der Übertragungs Warteschlange an. Der Standardwert ist BG_JOB_PRIORITY_NORMAL. Eine Liste der Prioritätsstufen finden Sie in der [**BG_JOB_PRIORITY**](bg-job-priority-.md) -Enumeration.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt sowohl die folgenden **HRESULT** -Werte als auch andere zurück.



| Rückgabecode                                                                              | Beschreibung                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | Die Auftrags Priorität wurde erfolgreich festgelegt.<br/> |



 

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

[**BG_JOB_PRIORITY**](bg-job-priority-.md)
</dt> <dt>

[**Ibackgroundcopyjob:: GetPriority**](ibackgroundcopyjob-getpriority.md)
</dt> </dl>

 

 





