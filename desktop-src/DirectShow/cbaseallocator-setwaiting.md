---
description: Die setwaiting-Methode erhöht die Anzahl der wartenden Threads.
ms.assetid: 4aec6177-fb32-44be-a58e-41a4f4aaf4f2
title: Cbasezucator. setwaiting-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.SetWaiting
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 92cba22e128a76f7884050d74a7819142c696dc9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372228"
---
# <a name="cbaseallocatorsetwaiting-method"></a>Cbasezucator. setwaiting-Methode

Die- `SetWaiting` Methode erhöht die Anzahl der wartenden Threads.

## <a name="syntax"></a>Syntax


```C++
void SetWaiting();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode erhöht die Member-Variable [**cbasezucator:: m \_ lwaiting**](cbaseallocator-m-lwaiting.md) . Wenn ein Thread in der [**cbasezucator:: GetBuffer**](cbaseallocator-getbuffer.md) -Methode blockiert ist, ruft die Zuweisung auf `SetWaiting` und wartet dann darauf, dass das [**cbasezucator:: m \_ hsem**](cbaseallocator-m-hsem.md) -Semaphor signalisiert wird. Die [**cbasezucator:: ReleaseBuffer**](cbaseallocator-releasebuffer.md) -Methode signalisiert dem Semaphor und legt *m \_ lwaiting* auf NULL fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasezucator-Klasse**](cbaseallocator.md)
</dt> </dl>

 

 




