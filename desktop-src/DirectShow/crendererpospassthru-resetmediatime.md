---
description: Die resetmediatime-Methode setzt die zwischengespeicherten Zeitstempel auf NULL zurück.
ms.assetid: 80dd2ae3-0a83-4017-8860-a089bef9a919
title: Crendererpospassthru. resetmediatime-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.ResetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 667b060258864290b64c5ffd780488ccb5d442ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354131"
---
# <a name="crendererpospassthruresetmediatime-method"></a>Crendererpospassthru. resetmediatime-Methode

Die- `ResetMediaTime` Methode setzt die zwischengespeicherten Zeitstempel auf NULL zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT ResetMediaTime();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Der Filter sollte diese Methode immer dann aufrufen, wenn die Zeitstempel, die von der [**crendererpospassthru:: registermediatime**](crendererpospassthru-registermediatime.md) -Methode zwischengespeichert werden, ungültig werden. Insbesondere sollte diese Methode als Antwort auf die [**IPin:: endflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) -Methode und die [**imediafilter::**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) End-Methode aufgerufen werden.

Nachdem diese Methode aufgerufen wurde, gibt die [**crendererpospassthru:: getmediatime**](crendererpospassthru-getmediatime.md) -Methode für die Start-und Endzeit 0 (null) zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




