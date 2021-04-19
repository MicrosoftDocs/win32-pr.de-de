---
description: Die stopstreaming-Methode stoppt das Streaming, wenn der Filter den Status "wird ausgeführt" verlässt.
ms.assetid: 465dde15-adec-46da-b8c8-56743e0cbd29
title: Cbaserderderer. stopstreaming-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.StopStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfd943de6a53383d7505fa9e884dcc152da6e5f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367180"
---
# <a name="cbaserendererstopstreaming-method"></a>Cbaserderderer. stopstreaming-Methode

Die- `StopStreaming` Methode stoppt das Streaming, wenn der Filter den Status "wird ausgeführt" verlässt.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT StopStreaming();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode ruft die [**cbaserdenderer:: onstopstreaming**](cbaserenderer-onstopstreaming.md) -Methode auf. Diese Methode führt in der Basisklasse keine Aktion aus, die abgeleitete Klasse kann Sie jedoch überschreiben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaserderderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




