---
description: Ruft die Position im Vektor ab, an der die Änderung aufgetreten ist.
ms.assetid: 00756d77-aae0-45f0-8bd4-cf68af9bdc7c
title: IVectorChangedEventArgs::get_Index-Methode (IVectorChangedEventArgs.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVectorChangedEventArgs.get_Index
api_type:
- COM
api_location:
- IVectorChangedEventArgs.h
ms.openlocfilehash: 72df7f0d46e1e3073262c43064daf58b1fefbf43af913bb7f1b912ed22e67a7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118560646"
---
# <a name="ivectorchangedeventargsget_index-method"></a>IVectorChangedEventArgs::get \_ Index-Methode

Ruft die Position im Vektor ab, an der die Änderung aufgetreten ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Index(
  [out, retval] unsigned *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*value* \[ out, retval\]
</dt> <dd>

Typ: **unsigned \***

Die nullbasierte Position im Vektor, an der die Änderung aufgetreten ist, falls zutreffend.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                       |
| Header<br/>                   | <dl> <dt>IVectorChangedEventArgs.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVectorChangedEventArgs**](ivectorchangedeventargs.md)
</dt> </dl>

 

 




