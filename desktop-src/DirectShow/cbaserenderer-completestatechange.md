---
description: Die completestatechange-Methode bestimmt, ob ein Übergang zum angehaltenen Zustand abgeschlossen ist.
ms.assetid: 505a0b31-deaa-46be-91e6-f9bc8e47dd3a
title: Cbaserderderer. completestatechange-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CompleteStateChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d2465aeed3347f6ebc592dbe01bc3580a30983e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370174"
---
# <a name="cbaserenderercompletestatechange-method"></a>Cbaserderderer. completestatechange-Methode

Die- `CompleteStateChange` Methode bestimmt, ob ein Übergang zum angehaltenen Zustand beendet ist.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT CompleteStateChange(
   FILTER_STATE OldState
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*OldState* 
</dt> <dd>

Zustand vor dem Übergang.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn der Übergang beendet ist. Andernfalls gibt S \_ false zurück.

## <a name="remarks"></a>Bemerkungen

Die [**cbaserererermethode::P ause**](cbaserenderer-pause.md) -Methode ruft diese Methode auf, um den Status Übergangsstatus zu aktualisieren. Im Allgemeinen wird die Umstellung auf angehalten erst beendet, wenn der Filter ein Beispiel empfängt. In einigen Situationen wird der Übergang jedoch sofort abgeschlossen, z. b. wenn der Filter nicht verbunden ist, oder wenn das Ende des Streams erreicht wurde. Diese Methode überprüft die verschiedenen Kriterien und ruft dann die [**cbaserenderer:: Ready**](cbaserenderer-ready.md) -Methode oder die [**cbaserenderer:: notready**](cbaserenderer-notready.md) -Methode auf, um den Übergangsstatus zu aktualisieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaserderderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




