---
description: Mit der setsourcerect-Methode wird das aktuelle Quellvideo Rechteck (rein virtuell) festgelegt. Dabei handelt es sich um eine interne Member-Funktion, die aufgerufen wird, wenn das Quell Rechteck geändert wird.
ms.assetid: 13bb594b-b154-40a2-ad00-f1e86781074d
title: Cbasecontrolvideo. setsourcerect-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0e3be6cc3819e1452fd196d4906377204a6e90bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366883"
---
# <a name="cbasecontrolvideosetsourcerect-method"></a>Cbasecontrolvideo. setsourcerect-Methode

Die- `SetSourceRect` Methode legt das aktuelle Quellvideo Rechteck (rein virtuell) fest. Dabei handelt es sich um eine interne Member-Funktion, die aufgerufen wird, wenn das Quell Rechteck geändert wird.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT SetSourceRect(
   RECT *pSourceRect
) = 0;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*psourcerect* 
</dt> <dd>

Zeiger auf das Quell Rechteck.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Abgeleitete Klassen sollten diese Member-Funktion überschreiben, um zu ermitteln, wann das Quell Rechteck geändert wird. Sie wird von den folgenden Member-Funktionen aufgerufen.

-   [**Cbasecontrolvideo:: setsourceposition**](cbasecontrolvideo-setsourceposition.md)
-   [**Cbasecontrolvideo::p UT \_ sourceLeft**](cbasecontrolvideo-put-sourceleft.md)
-   [**Cbasecontrolvideo::p UT \_ sourceWidth**](cbasecontrolvideo-put-sourcewidth.md)
-   [**Cbasecontrolvideo::p UT \_ sourceTop**](cbasecontrolvideo-put-sourcetop.md)
-   [**Cbasecontrolvideo::p UT \_ sourceHeight**](cbasecontrolvideo-put-sourceheight.md)

Im folgenden Beispiel wird eine Implementierung dieser Funktion in einer abgeleiteten Klasse veranschaulicht.


```C++
HRESULT CVideoText::SetSourceRect(RECT *pSourceRect)
{
    m_pRenderer->m_DrawImage.SetSourceRect(pSourceRect);
    return NOERROR;
}
```



In diesem Beispiel ist cvideotext eine Klasse, die von [**cbasecontrolvideo**](cbasecontrolvideo.md)abgeleitet ist. m \_ prenderer enthält ein Objekt einer Klasse, die von [**cbasevideorenderer**](cbasevideorenderer.md)abgeleitet ist, und das \_ in der abgeleiteten Klasse definierte Datenmember m DrawImage enthält ein [**cdrawimage**](cdrawimage.md) -Objekt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolvideo-Klasse**](cbasecontrolvideo.md)
</dt> </dl>

 

 




