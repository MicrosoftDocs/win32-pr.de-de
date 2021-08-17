---
description: Überprüft, ob der aufrufende Prozess Lesezugriff auf eine ANSI-Zeichenfolge hat. Falls nicht, ruft das Makro das DbgBreak-Makro auf.
ms.assetid: 44be67f8-9896-4360-82de-083a5f28a3d0
title: ValidateStringPtrA-Makro (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateStringPtrA
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 26a0e000f5b2b8de645924300eb650a05a66a4b57c16c5eda3f124e7bc0903a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119432100"
---
# <a name="validatestringptra-macro"></a>ValidateStringPtrA-Makro

Überprüft, ob der aufrufende Prozess Lesezugriff auf eine ANSI-Zeichenfolge hat. Falls nicht, ruft das Makro das [**DbgBreak-Makro**](dbgbreak.md) auf.

> [!Note]  
> Dieses Makro ist veraltet. Im Windows SDK für Windows Vista (und höher) führt dieses Makro keine Aktion aus.

 

## <a name="syntax"></a>Syntax


```C++
void ValidateStringPtrA(
   LPCSTR p
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*p* 
</dt> <dd>

Zeiger auf eine NULL-terminierte ANSI-Zeichenfolge.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Makro gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Dieses Makro wird ignoriert, es sei denn, \_ DEBUG, DEBUG oder VFWROBUST wird definiert, wenn die DirectShow-Basisklassenheaderdatei enthalten ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wxdebug.h (include Streams.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Zeigervalidierungsmakros](pointer-validation-macros.md)
</dt> </dl>

 

 




