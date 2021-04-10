---
description: Ruft den Typ der Änderung ab, die im Vektor aufgetreten ist.
ms.assetid: 213f4794-b972-44e3-a400-8a24b1583ddd
title: 'Ivectorchangedeventargs:: get_CollectionChange-Methode (ivectorchangedeventargs. h)'
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
ms.openlocfilehash: a843574bcaf93ec524173ba76800cc15012c89fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214604"
---
# <a name="ivectorchangedeventargsget_collectionchange-method"></a>Ivectorchangedeventargs:: get \_ CollectionChange-Methode

Ruft den Typ der Änderung ab, die im Vektor aufgetreten ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_CollectionChange(
  [out, retval] CollectionChange *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Wert* \[ Out, retval\]
</dt> <dd>

Typ: **CollectionChange \** _

Ein Wert aus der [_ *CollectionChange* *](/uwp/api/Windows.Foundation.Collections.CollectionChange?view=winrt-19041) -Enumeration, der die Änderung beschreibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                       |
| Header<br/>                   | <dl> <dt>IVector changedebug-args. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVector changedebug-args**](ivectorchangedeventargs.md)
</dt> </dl>

 

 
