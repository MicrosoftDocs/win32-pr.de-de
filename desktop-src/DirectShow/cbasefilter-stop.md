---
description: 'Die Methode "beenden" beendet den Filter. Diese Methode implementiert die imediafilter:: stopmethode.'
ms.assetid: 68d77f9a-95a2-4a71-bbe1-28be76fbc538
title: Cbasefilter. stoppt-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b4c4893edcf02fa18da3dc207a49f87c91b2a9ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371119"
---
# <a name="cbasefilterstop-method"></a>Cbasefilter. stoppt-Methode

Die- `Stop` Methode beendet den Filter. Diese Methode implementiert die [**imediafilter:: stopmethode**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) .

## <a name="syntax"></a>Syntax


```C++
HRESULT Stop();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt \_ bei Erfolg S OK oder einen **HRESULT** -Wert zurück, der die Ursache des Fehlers angibt.

## <a name="remarks"></a>Bemerkungen

Diese Methode ruft die [**cbasepin:: inaktive**](cbasepin-inactive.md) -Methode für jeden verbundenen Pins des Filters auf. Außerdem wird der Zustand des Filters auf "beendet" festgelegt \_ .

Wenn der Filter angehalten wird, sollte er Beispiele von Upstream ablehnen, die Bereitstellung von Beispielen nach unten beenden, Arbeitsthreads Herunterfahren und alle Ressourcen freigeben, die für das Streaming verwendet wurden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasefilter-Klasse**](cbasefilter.md)
</dt> </dl>

 

 




