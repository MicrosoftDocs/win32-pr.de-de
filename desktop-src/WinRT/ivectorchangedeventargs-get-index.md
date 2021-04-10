---
description: Ruft die Position im Vektor ab, an der die Änderung aufgetreten ist.
ms.assetid: 00756d77-aae0-45f0-8bd4-cf68af9bdc7c
title: 'Ivectorchangedeventargs:: get_Index-Methode (ivectorchangedeventargs. h)'
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
ms.openlocfilehash: 5c131567ec7fc2861ce11db9e5d7ec581f6f663a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041736"
---
# <a name="ivectorchangedeventargsget_index-method"></a>Ivectorchangedeventargs:: get \_ Index-Methode

Ruft die Position im Vektor ab, an der die Änderung aufgetreten ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Index(
  [out, retval] unsigned *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Wert* \[ Out, retval\]
</dt> <dd>

Typ: **Ganzzahl ohne Vorzeichen \** _

Die null basierte Position im Vektor, an der die Änderung aufgetreten ist (falls zutreffend).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Type: _ *HRESULT**

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

 

 




