---
title: IBackgroundCopyJob5 GetProperty-Methode (deliveryoptimization. h)
description: Eine generische Methode zum erhalten von Auftrags Eigenschaften für die Übermittlungs Optimierung (Do).
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
ms.openlocfilehash: 8200bb63a131db6fcab30b77f35a89fc9c943675
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956557"
---
# <a name="ibackgroundcopyjob5getproperty-method"></a>IBackgroundCopyJob5:: GetProperty-Methode

Eine generische Methode zum erhalten von Auftrags Eigenschaften für die Übermittlungs Optimierung (Do).

## <a name="syntax"></a>Syntax


```C++
HRESULT GetProperty(
  [in]  BITS_JOB_PROPERTY_ID    PropertyId,
  [out] BITS_JOB_PROPERTY_VALUE *pPropertyValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PropertyId* \[ in\]
</dt> <dd>

Die ID der Eigenschaft, die abgerufen wird, als [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) Enumerationswert.

</dd> <dt>

*ppropertyvalue* \[ vorgenommen\]
</dt> <dd>

Der Eigenschafts Wert, der als BITS_JOB_PROPERTY_VALUE Union zurückgegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt die folgenden Rückgabewerte zurück.



| Rückgabecode                                                                          | Beschreibung        |
|--------------------------------------------------------------------------------------|--------------------|
| <dl> <dt>**S_OK**</dt> </dl> | Erfolg<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1709, \[ nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, Version 1709, \[ nur Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Deliveryoptimization. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob5 ist als E847030C-bbba-4657-AF6D-484aa42bf1fe definiert.<br/>              |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IBackgroundCopyJob5**](ibackgroundcopyjob5.md)
</dt> <dt>

[**IBackgroundCopyJob5:: SetProperty**](ibackgroundcopyjob5-setproperty.md)
</dt> </dl>

 

 





