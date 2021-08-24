---
description: Die UsingImageAllocator-Methode gibt an, ob die aktuelle Zuweisung ein CImageAllocator-Objekt ist.
ms.assetid: 842bbcbc-2cc8-4e9d-b6c0-e07f7e472ca1
title: CDrawImage.UsingImageAllocator-Methode (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.UsingImageAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f10caec569733724a0c42b310facd36f74467472aee4339c83b68b382da09fa9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119539800"
---
# <a name="cdrawimageusingimageallocator-method"></a>CDrawImage.UsingImageAllocator-Methode

Die `UsingImageAllocator` -Methode gibt an, ob die aktuelle Zuweisung ein [**CImageAllocator-Objekt**](cimageallocator.md) ist.

## <a name="syntax"></a>Syntax


```C++
BOOL UsingImageAllocator();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn die aktuelle Zuweisung ein **CImageAllocator-Objekt** ist, andernfalls **FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CDrawImage-Klasse**](cdrawimage.md)
</dt> <dt>

[**CDrawImage::NotifyAllocator**](cdrawimage-notifyallocator.md)
</dt> </dl>

 

 




