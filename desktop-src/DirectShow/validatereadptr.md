---
description: Überprüft, ob der aufrufenden Prozess über Lesezugriff auf einen Speicherblock verfügt. Andernfalls ruft das Makro das dbgbreak-Makro auf.
ms.assetid: 1a70e4e5-e144-4cfe-b6be-c0a70aac9ada
title: Validatereadptr-Makro (wxdebug. h)
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
ms.openlocfilehash: aa8093ecbd428cafbf1266179b1489cac0d69c4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369276"
---
# <a name="validatereadptr-macro"></a>Validatereadptr-Makro

Überprüft, ob der aufrufenden Prozess über Lesezugriff auf einen Speicherblock verfügt. Andernfalls ruft das Makro das [**dbgbreak**](dbgbreak.md) -Makro auf.

> [!Note]  
> Dieses Makro ist veraltet. Im Windows SDK für Windows Vista (und höher) führt dieses Makro nichts aus.

 

## <a name="syntax"></a>Syntax


```C++
void ValidateReadPtr(
   const void *p,
         UINT cb
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*cker* 
</dt> <dd>

Zeiger auf einen Speicherblock.

</dd> <dt>

*betrieben* 
</dt> <dd>

Größe des Speicherblocks in Bytes.

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

 

 




