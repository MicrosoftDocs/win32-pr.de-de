---
description: Die setsourcerect-Methode legt das Quell Rechteck fest.
ms.assetid: 982636fe-73ea-4f13-9f2b-7ae8df839ab1
title: Cdrawimage. setsourcerect-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 64fb8729b694d38eac2d6321f92904292d99bd38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370566"
---
# <a name="cdrawimagesetsourcerect-method"></a>Cdrawimage. setsourcerect-Methode

Die- `SetSourceRect` Methode legt das Quell Rechteck fest.

## <a name="syntax"></a>Syntax


```C++
void SetSourceRect(
   RECT *pSourceRect
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*psourcerect* 
</dt> <dd>

Zeiger auf eine **Rect** -Struktur, die das neue Quell Rechteck definiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Der besitzende Filter sollte diese Methode beim Ändern des Quell Rechtecks aufruft. beispielsweise als Reaktion auf einen [**ibasicvideo:: setsourceposition**](/windows/desktop/api/Control/nf-control-ibasicvideo-setsourceposition) -Befehl.

Überprüfen Sie das in *psourcerect* angegebene Rechteck, bevor Sie diese Methode aufrufen, um sicherzustellen, dass Sie nicht über die systemeigene Videogröße hinaus erweitert wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cdrawimage-Klasse**](cdrawimage.md)
</dt> </dl>

 

 




