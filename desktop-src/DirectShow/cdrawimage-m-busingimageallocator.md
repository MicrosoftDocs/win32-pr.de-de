---
description: Die \_ Member-Variable m busingimagezuweisung gibt an, ob die Zuweisung für die PIN-Verbindung ein cimagezuordcator-Objekt ist. Wenn der Wert true ist, ist die Zuweisung ein cimagezuordcator-Objekt (oder wird von dieser Klasse abgeleitet).
ms.assetid: 8eddcab6-77b9-4c8f-be74-33e91661430d
title: 'Cdrawimage:: m_bUsingImageAllocator Member (winutil. h)'
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
ms.openlocfilehash: e08d1e8217f42c6855759cefeef40e56949156fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372633"
---
# <a name="cdrawimagem_busingimageallocator-member"></a>Cdrawimage:: m \_ busingimagezuordcator-Member

Die `m_bUsingImageAllocator` Member-Variable gibt an, ob die Zuweisung der Pin-Verbindung ein **cimagezuordcator** -Objekt ist. Wenn der Wert **true** ist, ist die Zuweisung ein **cimagezuordcator** -Objekt (oder wird von dieser Klasse abgeleitet).

## <a name="syntax"></a>Syntax


```C++
BOOL m_bUsingImageAllocator;
```



## <a name="remarks"></a>Bemerkungen

Wenn der Wert **true** ist, kann das **cdrawimage** -Objekt die GDI **-BitBLT** -Funktion und die **StretchBlt** -Funktion verwenden, um das Bild zu Rendering, anstatt die langsamsten Funktionen **SetDIBitsToDevice** und **StretchDIBits** zu verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cdrawimage-Klasse**](cdrawimage.md)
</dt> <dt>

[**Cdrawimage:: notifyzucator**](cdrawimage-notifyallocator.md)
</dt> <dt>

[**Cdrawimage:: usingimagezuordcator**](cdrawimage-usingimageallocator.md)
</dt> </dl>

 

 




