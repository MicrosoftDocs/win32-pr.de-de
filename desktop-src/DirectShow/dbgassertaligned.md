---
description: Testet, ob ein Zeiger an einer angegebenen Grenze ausgerichtet ist. Falls nicht, ruft dieses Makro das ASSERT-Makro auf. Wird in Einzelhandelsbuilds ignoriert.
ms.assetid: 4d9ec3a9-7107-45a3-a7aa-28d6e38fa92a
title: DbgAssertAligned-Makro (Wxdebug.h)
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
ms.openlocfilehash: 36b835ccd7fd82e226eb76dfb45ca4cfcd034a713da0d3639e91fba8aa7e4fca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953349"
---
# <a name="dbgassertaligned-macro"></a>DbgAssertAligned-Makro

Testet, ob ein Zeiger an einer angegebenen Grenze ausgerichtet ist. Falls nicht, ruft dieses Makro das [**ASSERT-Makro**](assert.md) auf. Wird in Einzelhandelsbuilds ignoriert.

## <a name="syntax"></a>Syntax


```C++
void DbgAssertAligned(
    ptr,
    alignment
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Ptr* 
</dt> <dd>

Zeigervariable.

</dd> <dt>

*Ausrichtung* 
</dt> <dd>

Erforderliche Ausrichtung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Makro gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wxdebug.h (include Streams.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Assert- und Breakpoint-Makros](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




