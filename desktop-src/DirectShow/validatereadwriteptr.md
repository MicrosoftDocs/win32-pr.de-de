---
description: Überprüft, ob der aufrufende Prozess über Lese-/Schreibzugriff auf einen Speicherblock verfügt. Andernfalls ruft das Makro das dbgbreak-Makro auf.
ms.assetid: 215f6db9-67b6-47e1-bee1-dc37082ae2b8
title: Validatereadschreiteptr-Makro (wxdebug. h)
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
ms.openlocfilehash: b551f3c72a2480ea1f160b2b384fe87dbede51f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372745"
---
# <a name="validatereadwriteptr-macro"></a>Validatereadschreiteptr-Makro

Überprüft, ob der aufrufende Prozess über Lese-/Schreibzugriff auf einen Speicherblock verfügt. Andernfalls ruft das Makro das [**dbgbreak**](dbgbreak.md) -Makro auf.

> [!Note]  
> Dieses Makro ist veraltet. Im Windows SDK für Windows Vista (und höher) führt dieses Makro nichts aus.

 

## <a name="syntax"></a>Syntax


```C++
void ValidateReadWritePtr(
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

 

 




