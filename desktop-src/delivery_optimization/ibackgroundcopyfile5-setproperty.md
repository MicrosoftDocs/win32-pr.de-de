---
title: IBackgroundCopyFile5 SetProperty-Methode (Deliveryoptimization.h)
description: Legt eine generische Eigenschaft einer Übermittlungsoptimierung(DO)-Dateiübertragung fest.
ms.assetid: 63B6806E-47D6-49B0-9867-628C110540D0
keywords:
- SetProperty-Methode
- SetProperty-Methode, IBackgroundCopyFile5-Schnittstelle
- IBackgroundCopyFile5-Schnittstelle, SetProperty-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyFile5.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 10da7fff9066ccefe7c356e3577ffffe7b0fc2e89d5fdb3f74611f5621d5b757
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755600"
---
# <a name="ibackgroundcopyfile5setproperty-method"></a>IBackgroundCopyFile5::SetProperty-Methode

Legt eine generische Eigenschaft einer Übermittlungsoptimierung(DO)-Dateiübertragung fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetProperty(
  [in]  BITS_FILE_PROPERTY_ID    PropertyId,
  [out] BITS_FILE_PROPERTY_VALUE *ProertyValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PropertyId* \[ In\]
</dt> <dd>

Gibt die eigenschaft an, die festgelegt werden soll.

</dd> <dt>

*ProertyValue* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Union, die den wert angibt, der festgelegt werden soll. Der für die Eigenschaften-ID geeignete Union-Member wird verwendet.

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IBackgroundCopyFile5**](ibackgroundcopyfile5.md)
</dt> <dt>

[**IBackgroundCopyFile5.GetProperty**](ibackgroundcopyfile5-getproperty.md)
</dt> </dl>

 

 





