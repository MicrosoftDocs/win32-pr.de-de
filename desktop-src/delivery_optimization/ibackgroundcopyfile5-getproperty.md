---
title: IBackgroundCopyFile5 GetProperty-Methode (deliveryoptimization. h)
description: Ruft eine generische Eigenschaft einer Dateiübertragung für die Übermittlungs Optimierung (Do) ab.
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
ms.openlocfilehash: 84c6a9f96fc332bda940573bde78d7dd05efeeb1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103507"
---
# <a name="ibackgroundcopyfile5getproperty-method"></a>IBackgroundCopyFile5:: GetProperty-Methode

Ruft eine generische Eigenschaft einer Dateiübertragung für die Übermittlungs Optimierung (Do) ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetProperty(
  [in]  BITS_FILE_PROPERTY_ID    PropertyId,
  [out] BITS_FILE_PROPERTY_VALUE *PropertyValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PropertyId* \[ in\]
</dt> <dd>

Gibt die Datei Eigenschaft an, deren Wert abgerufen werden soll.

</dd> <dt>

*PropertyValue* \[ vorgenommen\]
</dt> <dd>

Der Eigenschafts Wert, der als Zeiger auf einen BITS_FILE_PROPERTY_VALUE Union zurückgegeben wird. Verwenden Sie das Union-Feld, das für den Wert der Eigenschaft ID geeignet ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1709, \[ nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, Version 1709, \[ nur Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Deliveryoptimization. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile5 ist als "85c1657f-DAFC-40e8-8834-df18ea25717e" definiert.<br/>             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IBackgroundCopyFile5**](ibackgroundcopyfile5.md)
</dt> <dt>

[**IBackgroundCopyFile5. SetProperty**](ibackgroundcopyfile5-setproperty.md)
</dt> </dl>

 

 





