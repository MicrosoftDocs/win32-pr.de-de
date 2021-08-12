---
description: Die m bUsingImageAllocator-Membervariable gibt an, ob die Zuweisung für die Pinverbindung \_ ein CImageAllocator-Objekt ist. Wenn der Wert TRUE ist, ist die Zuweisung ein CImageAllocator-Objekt (oder wird von dieser Klasse abgeleitet).
ms.assetid: 8eddcab6-77b9-4c8f-be74-33e91661430d
title: CDrawImage::m_bUsingImageAllocator-Member (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bUsingImageAllocator
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bf60184758598872577e0c6b293f8eb0b72c5bf7305f1516a4dd6b5a4a639b94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118657110"
---
# <a name="cdrawimagem_busingimageallocator-member"></a>CDrawImage::m \_ bUsingImageAllocator-Member

Die `m_bUsingImageAllocator` Membervariable gibt an, ob die Zuweisung für die Pinverbindung ein **CImageAllocator-Objekt** ist. Wenn der Wert **TRUE ist,** ist die Zuweisung ein **CImageAllocator-Objekt** (oder wird von dieser Klasse abgeleitet).

## <a name="syntax"></a>Syntax


```C++
BOOL m_bUsingImageAllocator;
```



## <a name="remarks"></a>Hinweise

Wenn der Wert **TRUE ist,** kann das **CDrawImage-Objekt** die GDI-Funktionen **BitBlt** und **StretchBlt** anstelle der langsameren **Funktionen SetDIBitsToDevice** und **StretchDIBits** verwenden, um das Bild zu rendern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CDrawImage-Klasse**](cdrawimage.md)
</dt> <dt>

[**CDrawImage::NotifyAllocator**](cdrawimage-notifyallocator.md)
</dt> <dt>

[**CDrawImage::UsingImageAllocator**](cdrawimage-usingimageallocator.md)
</dt> </dl>

 

 




