---
description: Überprüft, ob der aufrufende Prozess Lesezugriff auf einen Speicherblock hat. Falls nicht, ruft das Makro das DbgBreak-Makro auf.
ms.assetid: 1a70e4e5-e144-4cfe-b6be-c0a70aac9ada
title: ValidateReadPtr-Makro (Wxdebug.h)
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
ms.openlocfilehash: caf429437d284a27e4cda830b51e4512375310f2d466a597e58c394a2fea551f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501630"
---
# <a name="validatereadptr-macro"></a>ValidateReadPtr-Makro

Überprüft, ob der aufrufende Prozess Lesezugriff auf einen Speicherblock hat. Falls nicht, ruft das Makro das [**DbgBreak-Makro**](dbgbreak.md) auf.

> [!Note]  
> Dieses Makro ist veraltet. Im Windows SDK für Windows Vista (und höher) führt dieses Makro keine Aktion aus.

 

## <a name="syntax"></a>Syntax


```C++
void ValidateReadPtr(
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

Dieses Makro wird ignoriert, es sei denn, \_ DEBUG, DEBUG oder VFWROBUST wird definiert, wenn die DirectShow-Basisklassenheaderdatei enthalten ist. Dieses Makro kann erhebliche Leistungskosten haben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wxdebug.h (include Streams.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Zeigervalidierungsmakros](pointer-validation-macros.md)
</dt> </dl>

 

 




