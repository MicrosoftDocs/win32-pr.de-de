---
description: Testet, ob ein Zeiger an einer angegebenen Grenze ausgerichtet ist. Andernfalls ruft dieses Makro das ASSERT-Makro auf. Wird in Einzelhandels Builds ignoriert.
ms.assetid: 4d9ec3a9-7107-45a3-a7aa-28d6e38fa92a
title: Dbgassertaligned-Makro (wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgAssertAligned
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 22b357f7f28e9df04ce36636e3972dbadc3036a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361485"
---
# <a name="dbgassertaligned-macro"></a>Dbgassertaligned-Makro

Testet, ob ein Zeiger an einer angegebenen Grenze ausgerichtet ist. Andernfalls ruft dieses Makro das [**Assert**](assert.md) -Makro auf. Wird in Einzelhandels Builds ignoriert.

## <a name="syntax"></a>Syntax


```C++
void DbgAssertAligned(
    ptr,
    alignment
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ptr* 
</dt> <dd>

Die Zeiger Variable.

</dd> <dt>

*Richt* 
</dt> <dd>

Erforderliche Ausrichtung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Makro gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wxdebug. h (Include Streams. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Assert-und breakpointmakros](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




