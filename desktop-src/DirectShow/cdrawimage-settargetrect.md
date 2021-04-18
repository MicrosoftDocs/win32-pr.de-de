---
description: Die settargetrect-Methode legt das Ziel Rechteck fest.
ms.assetid: 033f8bae-e63d-4be0-8dd0-715cc1229392
title: Cdrawimage. settargetrect-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4513b6aeda16d19476769290a6139f91b2fd1f19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364916"
---
# <a name="cdrawimagesettargetrect-method"></a>Cdrawimage. settargetrect-Methode

Die- `SetTargetRect` Methode legt das Ziel Rechteck fest.

## <a name="syntax"></a>Syntax


```C++
void SetTargetRect(
   RECT *pTargetRect
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ptargetrect* 
</dt> <dd>

Ein Zeiger auf eine **Rect** -Struktur, die das neue Ziel Rechteck definiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Der besitzende Filter sollte diese Methode beim Ändern des Quell Rechtecks aufruft. beispielsweise als Reaktion auf einen [**ibasicvideo:: setdestinationposition**](/windows/desktop/api/Control/nf-control-ibasicvideo-setdestinationposition) -Aufruf.

Überprüfen Sie vor dem Aufrufen dieser Methode das in *ptargetrect* angegebene Rechteck relativ zum Videofenster.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cdrawimage-Klasse**](cdrawimage.md)
</dt> </dl>

 

 




