---
title: IBackgroundCopyJob5 SetProperty-Methode (deliveryoptimization. h)
description: Eine generische Methode zum Festlegen von Auftrags Eigenschaften für die Übermittlungs Optimierung.
ms.assetid: 9A8CCE04-B3EB-43CC-A135-7054EC40ABEC
keywords:
- SetProperty-Methode
- SetProperty-Methode, IBackgroundCopyJob5-Schnittstelle
- IBackgroundCopyJob5 Interface, SetProperty-Methode
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
ms.openlocfilehash: a3dbd1e7c66592ea959c9b1ff4f4864340c504d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742857"
---
# <a name="ibackgroundcopyjob5setproperty-method"></a>IBackgroundCopyJob5:: SetProperty-Methode

Eine generische Methode zum Festlegen von Auftrags Eigenschaften für die Übermittlungs Optimierung.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetProperty(
  [in] BITS_JOB_PROPERTY_ID    PropertyId,
  [in] BITS_JOB_PROPERTY_VALUE PropertyValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PropertyId* \[ in\]
</dt> <dd>

Die ID der Eigenschaft, die festgelegt wird, als [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) Enumerationswert festgelegt wird.

</dd> <dt>

*PropertyValue* \[ in\]
</dt> <dd>

Der Wert der Eigenschaft, die festgelegt wird. Um einen Wert aufzunehmen, dessen Typ der-Eigenschaft entspricht, wird dieser Wert über die [**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md) Union angegeben, die aus allen bekannten Eigenschafts Typen besteht.

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

[**IBackgroundCopyJob5:: GetProperty**](ibackgroundcopyjob5-getproperty.md)
</dt> </dl>

 

 





