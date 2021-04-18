---
description: Überprüft, ob der aufrufenden Prozess Lesezugriff auf eine breit Zeichen-Zeichenfolge hat. Andernfalls ruft das Makro das dbgbreak-Makro auf.
ms.assetid: 526e8027-31e5-428d-856d-9fc6698693c3
title: Validatestringptrw-Makro (wxdebug. h)
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
ms.openlocfilehash: 1ece2caa0f2263c038121cd1ffd031cbe42d336a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371348"
---
# <a name="validatestringptrw-macro"></a>Validatestringptrw-Makro

Überprüft, ob der aufrufenden Prozess Lesezugriff auf eine breit Zeichen-Zeichenfolge hat. Andernfalls ruft das Makro das [**dbgbreak**](dbgbreak.md) -Makro auf.

> [!Note]  
> Dieses Makro ist veraltet. Im Windows SDK für Windows Vista (und höher) führt dieses Makro nichts aus.

 

## <a name="syntax"></a>Syntax


```C++
void ValidateStringPtrW(
   LPCWSTR p
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*cker* 
</dt> <dd>

Zeiger auf eine NULL-terminierte breit Zeichen-Zeichenfolge.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Makro gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Dieses Makro wird ignoriert, es sei denn, Debug, \_ Debug oder vfwrobust wird definiert, wenn die DirectShow-Basisklassen-Header Datei eingeschlossen wird. Dieses Makro kann einen erheblichen Leistungs Aufwand verursachen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wxdebug. h (Include Streams. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Zeiger Validierungs Makros](pointer-validation-macros.md)
</dt> </dl>

 

 




