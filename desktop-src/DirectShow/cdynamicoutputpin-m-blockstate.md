---
description: Blockierungsstatus.
ms.assetid: 55afd314-efd3-47bf-80e3-e17c1332a4cf
title: CDynamicOutputPin::m_BlockState-Member (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_BlockState
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9f539f200e6424aeccf4e507c25f5debbcc295cfdd9469e05dd1c9db71d6d121
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119292180"
---
# <a name="cdynamicoutputpinm_blockstate-member"></a>CDynamicOutputPin::m \_ BlockState-Member

Blockierungsstatus.

## <a name="syntax"></a>Syntax


```C++
BLOCK_STATE m_BlockState;
```



## <a name="remarks"></a>Hinweise

Die folgenden Zustände sind definiert:

-   NICHT \_ BLOCKIERT
-   PENDING (AUSSTEHEND)
-   Blockiert

Halten Sie vor dem Zugriff auf diese Variable den kritischen [**Abschnitt CDynamicOutputPin::m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) bei.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CDynamicOutputPin-Klasse**](cdynamicoutputpin.md)
</dt> </dl>

 

 




