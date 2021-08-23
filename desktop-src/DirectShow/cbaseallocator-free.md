---
description: Die Free-Methode gibt den pufferspeicher frei. Diese Methode wird aufgerufen, wenn der besitzende Filter die Zuweisung decommitiert, nachdem das letzte Medienbeispiel freigegeben wurde.
ms.assetid: dd1e6c4d-762a-4caf-902b-015c6c9fdb4d
title: CBaseAllocator.Free-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Free
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e77555094625bfc6a31a0527fc3223a124b012e72c28ea76e5774de289d63391
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794210"
---
# <a name="cbaseallocatorfree-method"></a>CBaseAllocator.Free-Methode

Die `Free` -Methode gibt den pufferspeicher frei. Diese Methode wird aufgerufen, wenn der besitzende Filter die Zuweisung decommitiert, nachdem das letzte Medienbeispiel freigegeben wurde.

## <a name="syntax"></a>Syntax


```C++
virtual void Free() = 0;
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Nachdem die [**Decommit-Methode**](cbaseallocator-decommit.md) aufgerufen wurde, ruft die Zuweisung diese Methode auf, wenn sie das letzte Medienbeispiel frei gibt. Die abgeleitete Klasse muss diese Methode implementieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseAllocator-Klasse**](cbaseallocator.md)
</dt> </dl>

 

 




