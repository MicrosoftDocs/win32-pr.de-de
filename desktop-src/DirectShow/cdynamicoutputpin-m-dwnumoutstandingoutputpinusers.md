---
description: Anzahl der streamingthreads, die diese PIN verwenden.
ms.assetid: f8650a17-edab-4d69-91da-78107c3c60b9
title: 'Cdynamicoutputpin:: m_dwNumOutstandingOutputPinUsers Member (amfilter. h)'
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
ms.openlocfilehash: 2ba214a2c1c6d3d056147db54c936cb61b73dcfc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352155"
---
# <a name="cdynamicoutputpinm_dwnumoutstandingoutputpinusers-member"></a>Cdynamicoutputpin:: m \_ dwnumoutstandingoutputpinusers-Member

Anzahl der streamingthreads, die diese PIN verwenden.

## <a name="syntax"></a>Syntax


```C++
DWORD m_dwNumOutstandingOutputPinUsers;
```



## <a name="remarks"></a>Bemerkungen

Die [**cdynamicoutputpin:: startusingoutputpin**](cdynamicoutputpin-startusingoutputpin.md) -Methode erhöht diese Variable, und die [**cdynamicoutputpin:: stopusingoutputpin**](cdynamicoutputpin-stopusingoutputpin.md) -Methode dekretet diese Variable. Wenn der Wert größer als 0 (null) ist, verwendet ein Thread diese PIN, um Daten zu streamen oder den Verbindungstyp zu ändern. Die PIN kann nicht blockiert werden, wenn dies der Fall ist.

Bevor Sie auf diese Variable zugreifen, halten Sie den kritischen Abschnitt [**cdynamicoutputpin:: m \_ blockstatus eLOCK**](cdynamicoutputpin-m-blockstatelock.md) .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cdynamicoutputpin-Klasse**](cdynamicoutputpin.md)
</dt> <dt>

[**Cdynamicoutputpin:: streamingthreadusingoutputpin**](cdynamicoutputpin-streamingthreadusingoutputpin.md)
</dt> </dl>

 

 




