---
title: IBackgroundCopyJob5 GetProperty-Methode (Deliveryoptimization.h)
description: Eine generische Methode zum Abrufen Übermittlungsoptimierung (DO)-Auftragseigenschaften.
ms.assetid: 22BA2FAB-3F24-4801-8FB7-CB6F9E8DFBB3
keywords:
- GetProperty-Methode
- GetProperty-Methode, IBackgroundCopyJob5-Schnittstelle
- IBackgroundCopyJob5-Schnittstelle, GetProperty-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyJob5.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2141afba2d2f58a08c62d609b9029c07ae07923e35f43e985f61a13a02aa68d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542799"
---
# <a name="ibackgroundcopyjob5getproperty-method"></a>IBackgroundCopyJob5::GetProperty-Methode

Eine generische Methode zum Abrufen Übermittlungsoptimierung (DO)-Auftragseigenschaften.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetProperty(
  [in]  BITS_JOB_PROPERTY_ID    PropertyId,
  [out] BITS_JOB_PROPERTY_VALUE *pPropertyValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PropertyId* \[ In\]
</dt> <dd>

Die ID der Eigenschaft, die als [](bits-job-property-id.md) Einsenumerwert BITS_JOB_PROPERTY_ID wird.

</dd> <dt>

*pPropertyValue* \[ out\]
</dt> <dd>

Der eigenschaftswert, der als BITS_JOB_PROPERTY_VALUE zurückgegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt die folgenden Rückgabewerte zurück.



| Rückgabecode                                                                          | Beschreibung        |
|--------------------------------------------------------------------------------------|--------------------|
| <dl> <dt>**S_OK**</dt> </dl> | Erfolg<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, version 1709 desktop apps only (Nur Desktop-Apps der Version 1709) \[\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob5 ist als E847030C-BBBA-4657-AF6D-484AA42BF1FE definiert.<br/>              |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IBackgroundCopyJob5**](ibackgroundcopyjob5.md)
</dt> <dt>

[**IBackgroundCopyJob5::SetProperty**](ibackgroundcopyjob5-setproperty.md)
</dt> </dl>

 

 





