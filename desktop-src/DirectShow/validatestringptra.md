---
description: Überprüft, ob der aufrufende Prozess über Lesezugriff auf eine ANSI-Zeichenfolge verfügt. Andernfalls ruft das Makro das dbgbreak-Makro auf.
ms.assetid: 44be67f8-9896-4360-82de-083a5f28a3d0
title: Validatestringptra-Makro (wxdebug. h)
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
ms.openlocfilehash: 94ce34393ec494f34cce621afc168a4d6bbe4325
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364479"
---
# <a name="validatestringptra-macro"></a>Validatestringptra-Makro

Überprüft, ob der aufrufende Prozess über Lesezugriff auf eine ANSI-Zeichenfolge verfügt. Andernfalls ruft das Makro das [**dbgbreak**](dbgbreak.md) -Makro auf.

> [!Note]  
> Dieses Makro ist veraltet. Im Windows SDK für Windows Vista (und höher) führt dieses Makro nichts aus.

 

## <a name="syntax"></a>Syntax


```C++
void ValidateStringPtrA(
   LPCSTR p
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*cker* 
</dt> <dd>

Zeiger auf eine mit NULL endende ANSI-Zeichenfolge.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Makro gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Dieses Makro wird ignoriert, es sei denn, Debug, \_ Debug oder vfwrobust wird definiert, wenn die DirectShow-Basisklassen-Header Datei eingeschlossen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wxdebug. h (Include Streams. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Zeiger Validierungs Makros](pointer-validation-macros.md)
</dt> </dl>

 

 




