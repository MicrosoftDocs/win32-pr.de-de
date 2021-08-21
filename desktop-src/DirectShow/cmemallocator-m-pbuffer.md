---
description: Zeiger auf den Speicherblock, der die Puffer enthält.
ms.assetid: b9d08f5b-8616-4f68-869a-e8ebb77ccdc1
title: CMemAllocator::m_pBuffer-Member (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pBuffer
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4fa9c56c5a90c1fa3fde7dda4bca82cd3f473a591db9e2e24f0b1d141c6aa33e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118155982"
---
# <a name="cmemallocatorm_pbuffer-member"></a>CMemAllocator::m \_ pBuffer-Member

Zeiger auf den Speicherblock, der die Puffer enthält.

## <a name="syntax"></a>Syntax


```C++
LPBYTE m_pBuffer;
```



## <a name="remarks"></a>Hinweise

Beispielpuffer werden als Offsets von diesem Zeiger berechnet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CMemAllocator-Klasse**](cmemallocator.md)
</dt> </dl>

 

 




