---
description: Die settargetrect-Methode legt das aktuelle Ziel Rechteck (rein virtuell) fest. Dabei handelt es sich um eine interne Member-Funktion, die aufgerufen wird, wenn das Ziel Rechteck geändert wird.
ms.assetid: 9e48989d-5995-4f9d-82b2-01229473c3e8
title: Cbasecontrolvideo. settargetrect-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3868e7d8df93940829fb96c7152a55048a5cae82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366882"
---
# <a name="cbasecontrolvideosettargetrect-method"></a>Cbasecontrolvideo. settargetrect-Methode

Die- `SetTargetRect` Methode legt das aktuelle Ziel Rechteck (rein virtuell) fest. Dabei handelt es sich um eine interne Member-Funktion, die aufgerufen wird, wenn das Ziel Rechteck geändert wird.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT SetTargetRect(
   RECT *pTargetRect
) = 0;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ptargetrect* 
</dt> <dd>

Zeiger auf das Ziel Rechteck.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Abgeleitete Klassen sollten diese überschreiben, um zu ermitteln, wann das Ziel Rechteck geändert wird. Sie wird von den folgenden Member-Funktionen aufgerufen.

-   [**Cbasecontrolvideo:: setdestinationposition**](cbasecontrolvideo-setdestinationposition.md)
-   [**Cbasecontrolvideo::p UT \_ destinationleft**](cbasecontrolvideo-put-destinationleft.md)
-   [**Cbasecontrolvideo::p UT \_ destinationwidth**](cbasecontrolvideo-put-destinationwidth.md)
-   [**Cbasecontrolvideo::p UT \_ destinationtop**](cbasecontrolvideo-put-destinationtop.md)
-   [**Cbasecontrolvideo::p UT \_ destinationheight**](cbasecontrolvideo-put-destinationheight.md)

Im folgenden Beispiel wird eine Implementierung dieser Funktion in einer abgeleiteten Klasse veranschaulicht.


```C++
HRESULT CVideoText::SetTargetRect(RECT *pTargetRect)
{
    m_pRenderer->m_DrawImage.SetTargetRect(pTargetRect);
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

 

 




