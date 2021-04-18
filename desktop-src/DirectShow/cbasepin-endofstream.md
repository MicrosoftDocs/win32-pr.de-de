---
description: 'Die EndOf-Methode benachrichtigt die PIN, dass keine weiteren Daten erwartet werden. Diese Methode implementiert die IPin:: EndOf Stream-Methode. Diese Methode nur für Eingabe Pins aufzurufen.'
ms.assetid: 52a71c30-bd68-4152-8901-71ef2e65913a
title: Cbasepin. EndOf Stream-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2324bae8ec1266dce2471049f8ba2f06b0c9e6e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364459"
---
# <a name="cbasepinendofstream-method"></a>Cbasepin. EndOf Stream-Methode

Die- `EndOfStream` Methode benachrichtigt die PIN, dass keine weiteren Daten erwartet werden. Diese Methode implementiert die [**IPin:: EndOf Stream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) -Methode. Diese Methode nur für Eingabe Pins aufzurufen.

## <a name="syntax"></a>Syntax


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Der Filter sollte Streamende Benachrichtigungen an die Eingabe Pins verbundener Filter übergeben. Wenn der Filter ein Renderer ist, sollte er eine [**EC \_ Complete**](ec-complete.md) Event-Benachrichtigung an den Filter Graph-Manager senden. Weitere Informationen finden Sie unter [Datenfluss im Filter Diagramm](data-flow-in-the-filter-graph.md).

In der Basisklasse führt diese Methode keine Aktion aus. Abgeleitete Klassen sollten diese Methode überschreiben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




