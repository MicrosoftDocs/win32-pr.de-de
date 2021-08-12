---
title: IBackgroundCopyJob5 SetProperty-Methode (Deliveryoptimization.h)
description: Eine generische Methode zum Festlegen Übermittlungsoptimierung (DO)-Auftragseigenschaften.
ms.assetid: 9A8CCE04-B3EB-43CC-A135-7054EC40ABEC
keywords:
- SetProperty-Methode
- SetProperty-Methode, IBackgroundCopyJob5-Schnittstelle
- IBackgroundCopyJob5-Schnittstelle, SetProperty-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyJob5.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f9b7dab17780572a59e12dde9905c3d8db23895e6564aac47cb6eb2d984bfaf3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542683"
---
# <a name="ibackgroundcopyjob5setproperty-method"></a>IBackgroundCopyJob5::SetProperty-Methode

Eine generische Methode zum Festlegen Übermittlungsoptimierung (DO)-Auftragseigenschaften.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetProperty(
  [in] BITS_JOB_PROPERTY_ID    PropertyId,
  [in] BITS_JOB_PROPERTY_VALUE PropertyValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PropertyId* \[ In\]
</dt> <dd>

Die ID der Eigenschaft, die als [](bits-job-property-id.md) Einsenumerwert BITS_JOB_PROPERTY_ID festgelegt wird.

</dd> <dt>

*PropertyValue* \[ In\]
</dt> <dd>

Der Wert der Eigenschaft, die festgelegt wird. Um einen Wert zu halten, dessen Typ für die -Eigenschaft geeignet ist, wird dieser Wert über die BITS_JOB_PROPERTY_VALUE-Union angegeben, die aus allen bekannten Eigenschaftentypen besteht. [](bits-job-property-value-.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt die folgenden Rückgabewerte zurück.



| Rückgabecode                                                                          | Beschreibung        |
|--------------------------------------------------------------------------------------|--------------------|
| <dl> <dt>**S_OK**</dt> </dl> | Erfolg<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10 Desktop-Apps, Version 1709 \[\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob5 ist als E847030C-BBBA-4657-AF6D-484AA42BF1FE definiert.<br/>              |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**IBackgroundCopyJob5**](ibackgroundcopyjob5.md)
</dt> <dt>

[**IBackgroundCopyJob5::GetProperty**](ibackgroundcopyjob5-getproperty.md)
</dt> </dl>

 

 





