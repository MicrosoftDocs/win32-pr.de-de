---
title: IBackgroundCopyJob SetPriority-Methode (Deliveryoptimization.h)
description: Gibt die Prioritätsstufe Ihres Auftrags an. Die Prioritätsebene bestimmt, wann Ihr Auftrag relativ zu anderen Aufträgen in der Übertragungswarteschlange verarbeitet wird.
ms.assetid: DC943093-CA1D-4840-B7AC-29710764D4E5
keywords:
- SetPriority-Methode
- SetPriority-Methode, IBackgroundCopyJob-Schnittstelle
- IBackgroundCopyJob-Schnittstelle, SetPriority-Methode
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
ms.openlocfilehash: 4ed1852d6990b94a000ac6affcec6020d266aaac5fae4611c3985a6f5c203aca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542871"
---
# <a name="ibackgroundcopyjobsetpriority-method"></a>IBackgroundCopyJob::SetPriority-Methode

Gibt die Prioritätsstufe Ihres Auftrags an. Die Prioritätsebene bestimmt, wann Ihr Auftrag relativ zu anderen Aufträgen in der Übertragungswarteschlange verarbeitet wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetPriority(
  [in] BG_JOB_PRIORITY Priority
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Priorität* \[ In\]
</dt> <dd>

Gibt die Prioritätsstufe Ihres Auftrags relativ zu anderen Aufträgen in der Übertragungswarteschlange an. Der Standardwert ist BG_JOB_PRIORITY_NORMAL. Eine Liste der Prioritätsebenen [](bg-job-priority-.md) finden Sie in der BG_JOB_PRIORITY-Enumeration.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt die folgenden **HRESULT-Werte** sowie andere zurück.



| Rückgabecode                                                                              | Beschreibung                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>S_OK</dt> </dl> | Die Auftragspriorität wurde erfolgreich festgelegt.<br/> |



 

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

[**BG_JOB_PRIORITY**](bg-job-priority-.md)
</dt> <dt>

[**IBackgroundCopyJob::GetPriority**](ibackgroundcopyjob-getpriority.md)
</dt> </dl>

 

 





