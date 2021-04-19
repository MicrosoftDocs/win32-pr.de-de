---
description: Die onstartstreaming-Methode wird aufgerufen, wenn der Filter das Streaming startet.
ms.assetid: 02a5b334-f6c4-4cba-8882-c6b36d97feb3
title: Cbaserderderer. onstartstreaming-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnStartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 66433795b0674e1d2d5b7a7de5b1dcd1b50eb424
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366685"
---
# <a name="cbaserendereronstartstreaming-method"></a>Cbaserderderer. onstartstreaming-Methode

Die- `OnStartStreaming` Methode wird aufgerufen, wenn der Filter das Streaming startet.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT OnStartStreaming();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Die [**cbaserdenderer:: startstreaming**](cbaserenderer-startstreaming.md) -Methode ruft diese Methode auf. Es wird keine Aktion in der Basisklasse durchführt, aber die abgeleitete Klasse kann Sie überschreiben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaserderderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




