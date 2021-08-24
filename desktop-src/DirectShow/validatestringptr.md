---
description: Überprüft, ob der aufrufende Prozess Lesezugriff auf eine Zeichenfolge hat. Falls nicht, ruft das Makro das DbgBreak-Makro auf.
ms.assetid: 749a8c22-7a4a-49c2-a214-fc64dc5a0202
title: ValidateStringPtr-Makro (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateReadPtr
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: e6b04b83f3bd3b938f7cc6cc488a931e34bcca6207770b44cbd3c77c01dc9624
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755690"
---
# <a name="validatestringptr-macro"></a>ValidateStringPtr-Makro

Überprüft, ob der aufrufende Prozess Lesezugriff auf eine Zeichenfolge hat. Falls nicht, ruft das Makro das [**DbgBreak-Makro**](dbgbreak.md) auf.

> [!Note]  
> Dieses Makro ist veraltet. Im Windows SDK für Windows Vista (und höher) führt dieses Makro keine Aktion aus.

 

## <a name="syntax"></a>Syntax


```C++
void ValidateReadPtr(
   LPCTSTR p
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*p* 
</dt> <dd>

Zeiger auf eine auf NULL endende **TCHAR-Zeichenfolge.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Makro gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Dieses Makro wird ignoriert, es sei denn, \_ DEBUG, DEBUG oder VFWROBUST wird definiert, wenn die DirectShow-Basisklassenheaderdatei enthalten ist. Dieses Makro kann erhebliche Leistungskosten haben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wxdebug.h (include Streams.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Zeigervalidierungsmakros](pointer-validation-macros.md)
</dt> </dl>

 

 




