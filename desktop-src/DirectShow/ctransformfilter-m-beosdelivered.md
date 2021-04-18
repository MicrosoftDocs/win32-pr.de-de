---
description: Flag, das angibt, ob der Filter eine Benachrichtigung über das Ende des Datenstroms gesendet hat.
ms.assetid: 93f897de-04bb-4de4-a612-39b27c7d6f6c
title: 'Ctransformfilter:: m_bEOSDelivered Member (Transfrm. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bEOSDelivered
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f24b87f9808c53b5f64f66031a8ee2a4e9449089
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371679"
---
# <a name="ctransformfilterm_beosdelivered-member"></a>Ctransformfilter:: m-über \_ mittelte Member

Flag, das angibt, ob der Filter eine Benachrichtigung über das Ende des Datenstroms gesendet hat.

## <a name="syntax"></a>Syntax


```C++
BOOL m_bEOSDelivered;
```



## <a name="remarks"></a>Bemerkungen

Wenn der Filter angehalten wird, wenn keine Eingabe Verbindung vorhanden ist, sendet er eine downstreambenachrichtigung und legt dieses Flag auf **true** fest. Die Benachrichtigung über das Ende des Datenstroms stellt sicher, dass der Downstream-Filter nicht auf Stichproben wartet. Beachten Sie, dass die [**EndOf Stream**](ctransformfilter-endofstream.md) -Methode des Filters dieses Flag nicht festgelegt hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ctransformfilter-Klasse**](ctransformfilter.md)
</dt> </dl>

 

 




