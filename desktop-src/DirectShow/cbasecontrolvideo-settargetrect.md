---
description: Die SetTargetRect-Methode legt das aktuelle Zielrechteck (rein virtuell) fest. Dies ist eine interne Memberfunktion, die aufgerufen wird, wenn sich das Zielrechteck ändert.
ms.assetid: 9e48989d-5995-4f9d-82b2-01229473c3e8
title: CBaseControlVideo.SetTargetRect-Methode (Ctlutil.h)
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
ms.openlocfilehash: 3af420d9280d21ccf11bfdc6a23b63b33f10c1bf5a360f1770647dcb51655cf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017408"
---
# <a name="cbasecontrolvideosettargetrect-method"></a>CBaseControlVideo.SetTargetRect-Methode

Die `SetTargetRect` -Methode legt das aktuelle Zielrechteck (rein virtuell) fest. Dies ist eine interne Memberfunktion, die aufgerufen wird, wenn sich das Zielrechteck ändert.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT SetTargetRect(
   RECT *pTargetRect
) = 0;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pTargetRect* 
</dt> <dd>

Zeiger auf das Zielrechteck.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Abgeleitete Klassen sollten dies überschreiben, um zu wissen, wann sich das Zielrechteck ändert. Sie wird von den folgenden Memberfunktionen aufgerufen.

-   [**CBaseControlVideo::SetDestinationPosition**](cbasecontrolvideo-setdestinationposition.md)
-   [**CBaseControlVideo::put \_ DestinationLeft**](cbasecontrolvideo-put-destinationleft.md)
-   [**CBaseControlVideo::put \_ DestinationWidth**](cbasecontrolvideo-put-destinationwidth.md)
-   [**CBaseControlVideo::put \_ DestinationTop**](cbasecontrolvideo-put-destinationtop.md)
-   [**CBaseControlVideo::put \_ DestinationHeight**](cbasecontrolvideo-put-destinationheight.md)

Im folgenden Beispiel wird eine Implementierung dieser Funktion in einer abgeleiteten Klasse veranschaulicht.


```C++
HRESULT CVideoText::SetTargetRect(RECT *pTargetRect)
{
    m_pRenderer->m_DrawImage.SetTargetRect(pTargetRect);
    return NOERROR;
}
```



In diesem Beispiel ist CVideoText eine von [**CBaseControlVideo**](cbasecontrolvideo.md)abgeleitete Klasse, m \_ pRenderer enthält ein Objekt einer klasse, die von [**CBaseVideoRenderer**](cbasevideorenderer.md)abgeleitet wurde, und der \_ m DrawImage-Datenmember, der in der abgeleiteten Klasse definiert ist, enthält ein [**CDrawImage-Objekt.**](cdrawimage.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseControlVideo-Klasse**](cbasecontrolvideo.md)
</dt> </dl>

 

 




