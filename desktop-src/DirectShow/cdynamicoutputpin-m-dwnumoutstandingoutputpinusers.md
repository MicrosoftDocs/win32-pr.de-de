---
description: Anzahl der Streamingthreads, die diesen Pin verwenden.
ms.assetid: f8650a17-edab-4d69-91da-78107c3c60b9
title: CDynamicOutputPin::m_dwNumOutstandingOutputPinUsers-Member (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dwNumOutstandingOutputPinUsers
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 29fc593065af4252f58ce4bb08dd41fac82926dc11490377f6a8af614794b22a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688710"
---
# <a name="cdynamicoutputpinm_dwnumoutstandingoutputpinusers-member"></a>CDynamicOutputPin::m \_ dwNumOutstandingOutputPinUsers-Member

Anzahl der Streamingthreads, die diesen Pin verwenden.

## <a name="syntax"></a>Syntax


```C++
DWORD m_dwNumOutstandingOutputPinUsers;
```



## <a name="remarks"></a>Hinweise

Die [**CDynamicOutputPin::StartUsingOutputPin-Methode**](cdynamicoutputpin-startusingoutputpin.md) erhöht diese Variable, und die [**CDynamicOutputPin::StopUsingOutputPin-Methode**](cdynamicoutputpin-stopusingoutputpin.md) dekrementiert sie. Wenn der Wert größer als 0 (null) ist, verwendet ein Thread diesen Pin, um Daten zu streamen oder den Verbindungstyp zu ändern. Die Stecknadel kann nicht blockiert werden, während dies der Fall ist.

Bevor Sie auf diese Variable zugreifen, speichern Sie den kritischen Abschnitt [**CDynamicOutputPin::m \_ BlockStateLock.**](cdynamicoutputpin-m-blockstatelock.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CDynamicOutputPin-Klasse**](cdynamicoutputpin.md)
</dt> <dt>

[**CDynamicOutputPin::StreamingThreadUsingOutputPin**](cdynamicoutputpin-streamingthreadusingoutputpin.md)
</dt> </dl>

 

 




