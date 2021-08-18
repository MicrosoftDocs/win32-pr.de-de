---
description: Überprüft, ob der aufrufende Prozess Lesezugriff auf eine Breitzeichenzeichenfolge hat. Falls nicht, ruft das Makro das DbgBreak-Makro auf.
ms.assetid: 526e8027-31e5-428d-856d-9fc6698693c3
title: ValidateStringPtrW-Makro (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateStringPtrW
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 71567070618796ad564b7f7fb5e8d854f580d482e91d9f4fd7381a582e32495c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755670"
---
# <a name="validatestringptrw-macro"></a>ValidateStringPtrW-Makro

Überprüft, ob der aufrufende Prozess Lesezugriff auf eine Breitzeichenzeichenfolge hat. Falls nicht, ruft das Makro das [**DbgBreak-Makro**](dbgbreak.md) auf.

> [!Note]  
> Dieses Makro ist veraltet. Im Windows SDK für Windows Vista (und höher) führt dieses Makro keine Aktion aus.

 

## <a name="syntax"></a>Syntax


```C++
void ValidateStringPtrW(
   LPCWSTR p
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*P* 
</dt> <dd>

Zeiger auf eine NULL-endende Breitzeichenzeichenfolge.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Makro gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Dieses Makro wird ignoriert, es sei denn, \_ DEBUG, DEBUG oder VFWROBUST wird definiert, wenn die DirectShow-Basisklassenheaderdatei enthalten ist. Dieses Makro kann erhebliche Leistungskosten haben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wxdebug.h (include Streams.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Zeigervalidierungsmakros](pointer-validation-macros.md)
</dt> </dl>

 

 




