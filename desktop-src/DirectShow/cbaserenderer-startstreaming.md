---
description: Die startstreaming-Methode initiiert das Streaming, wenn der Filter in den Status wird ausgeführt wechselt.
ms.assetid: 198e9c1b-be69-4ba6-aa67-9f24ed080ab6
title: Cbaserderderer. startstreaming-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.StartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7bf1fcb1cbfb651221296054493688b2d9f33bd3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352135"
---
# <a name="cbaserendererstartstreaming-method"></a>Cbaserderderer. startstreaming-Methode

Die- `StartStreaming` Methode initiiert das Streaming, wenn der Filter in den Status wird ausgeführt wechselt.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT StartStreaming();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK oder einen anderen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn der Filter ein Beispiel enthält, wird das Beispiel für das Rendering geplant. Andernfalls sendet der Filter ein Ereignis vom Typ " [**EC \_ Complete**](ec-complete.md) " an den Filter Graph-Manager, wenn eine ausstehende streambenachrichtigung vorliegt.

Diese Methode ruft die [**cbaserdenderer:: onstartstreaming**](cbaserenderer-onstartstreaming.md) -Methode auf. Diese Methode führt in der Basisklasse keine Aktion aus, die abgeleitete Klasse kann Sie jedoch überschreiben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaserderderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




