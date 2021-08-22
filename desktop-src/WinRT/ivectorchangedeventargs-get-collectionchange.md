---
description: Ruft den Änderungstyp ab, der im Vektor aufgetreten ist.
ms.assetid: 213f4794-b972-44e3-a400-8a24b1583ddd
title: IVectorChangedEventArgs::get_CollectionChange-Methode (IVectorChangedEventArgs.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVectorChangedEventArgs.get_CollectionChange
api_type:
- COM
api_location:
- IVectorChangedEventArgs.h
ms.openlocfilehash: 2476f9563b4e2a0cabf9babbcfc265ee4f3549416c2fdfda0dbb0f204b7ca9bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119504810"
---
# <a name="ivectorchangedeventargsget_collectionchange-method"></a>IVectorChangedEventArgs::get \_ CollectionChange-Methode

Ruft den Änderungstyp ab, der im Vektor aufgetreten ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_CollectionChange(
  [out, retval] CollectionChange *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wert* \[ out, retval\]
</dt> <dd>

Typ: **CollectionChange \***

Ein Wert aus der [**CollectionChange-Enumeration,**](/uwp/api/Windows.Foundation.Collections.CollectionChange?view=winrt-19041) der die Änderung beschreibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                       |
| Header<br/>                   | <dl> <dt>IVectorChangedEventArgs.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVectorChangedEventArgs**](ivectorchangedeventargs.md)
</dt> </dl>

 

 
