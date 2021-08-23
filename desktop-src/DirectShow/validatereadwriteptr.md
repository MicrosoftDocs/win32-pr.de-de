---
description: Überprüft, ob der aufrufende Prozess Über Lese-/Schreibzugriff auf einen Speicherblock verfügt. Falls nicht, ruft das Makro das DbgBreak-Makro auf.
ms.assetid: 215f6db9-67b6-47e1-bee1-dc37082ae2b8
title: ValidateReadWritePtr-Makro (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateReadWritePtr
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: ec4d1c0440d0747024efadaa441ca062da512283f5a01f29be12b19c0f7c0567
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755660"
---
# <a name="validatereadwriteptr-macro"></a>ValidateReadWritePtr-Makro

Überprüft, ob der aufrufende Prozess Über Lese-/Schreibzugriff auf einen Speicherblock verfügt. Falls nicht, ruft das Makro das [**DbgBreak-Makro**](dbgbreak.md) auf.

> [!Note]  
> Dieses Makro ist veraltet. Im Windows SDK für Windows Vista (und höher) führt dieses Makro keine Aktion aus.

 

## <a name="syntax"></a>Syntax


```C++
void ValidateReadWritePtr(
   const void *p,
         UINT cb
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*p* 
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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Zeigervalidierungsmakros](pointer-validation-macros.md)
</dt> </dl>

 

 




