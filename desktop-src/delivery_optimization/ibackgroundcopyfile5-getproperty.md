---
title: IBackgroundCopyFile5 GetProperty-Methode (Deliveryoptimization.h)
description: Ruft eine generische Eigenschaft einer Übermittlungsoptimierung -Dateiübertragung (DO) ab.
ms.assetid: E2E96A0F-5670-4DE7-9DF8-A215AFAD0E8A
keywords:
- GetProperty-Methode
- GetProperty-Methode, IBackgroundCopyFile5-Schnittstelle
- IBackgroundCopyFile5-Schnittstelle, GetProperty-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyFile5.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0a664c752bd28b176189cdd77e955684236cfa23c6b384378610336335651fad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635950"
---
# <a name="ibackgroundcopyfile5getproperty-method"></a>IBackgroundCopyFile5::GetProperty-Methode

Ruft eine generische Eigenschaft einer Übermittlungsoptimierung -Dateiübertragung (DO) ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetProperty(
  [in]  BITS_FILE_PROPERTY_ID    PropertyId,
  [out] BITS_FILE_PROPERTY_VALUE *PropertyValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PropertyId* \[ In\]
</dt> <dd>

Gibt die Dateieigenschaft an, deren Wert abgerufen werden soll.

</dd> <dt>

*PropertyValue* \[ out\]
</dt> <dd>

Der Eigenschaftswert, der als Zeiger auf eine BITS_FILE_PROPERTY_VALUE zurückgegeben wird. Verwenden Sie das union-Feld, das für den übergebenen Eigenschafts-ID-Wert geeignet ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, gibt **sie** S_OK. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, version 1709 desktop apps only (Nur Desktop-Apps der Version 1709) \[\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile5 ist als 85C1657F-DAFC-40E8-8834-DF18EA25717E definiert.<br/>             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IBackgroundCopyFile5**](ibackgroundcopyfile5.md)
</dt> <dt>

[**IBackgroundCopyFile5.SetProperty**](ibackgroundcopyfile5-setproperty.md)
</dt> </dl>

 

 





