---
description: Überprüft, ob der aufrufende Prozess Schreibzugriff auf einen Speicherblock hat. Wenn nicht, ruft das Makro das DbgBreak-Makro auf.
ms.assetid: efbb5ca6-0289-487d-b55a-f85b38d0515a
title: ValidateWritePtr-Makro (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateWritePtr
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: f20739093692977b2560de465b916cac12aeb67e2dbf9a6b9488ef8cd61f544f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072124"
---
# <a name="validatewriteptr-macro"></a>ValidateWritePtr-Makro

Überprüft, ob der aufrufende Prozess Schreibzugriff auf einen Speicherblock hat. Wenn nicht, ruft das Makro das [**DbgBreak-Makro**](dbgbreak.md) auf.

> [!Note]  
> Dieses Makro ist veraltet. Im Windows SDK für Windows Vista (und höher) führt dieses Makro nichts aus.

 

## <a name="syntax"></a>Syntax


```C++
void ValidateWritePtr(
   const void *p,
         UINT cb
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*P* 
</dt> <dd>

Zeiger auf einen Speicherblock.

</dd> <dt>

*Cb* 
</dt> <dd>

Größe des Speicherblocks in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Makro gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Dieses Makro wird ignoriert, es sei \_ denn, DEBUG, DEBUG oder VFWROBUST wird definiert, wenn die DirectShow-Basisklassenheaderdatei enthalten ist. Dieses Makro kann erhebliche Leistungskosten haben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wxdebug.h (include Streams.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Zeigervalidierungsmakros](pointer-validation-macros.md)
</dt> </dl>

 

 




