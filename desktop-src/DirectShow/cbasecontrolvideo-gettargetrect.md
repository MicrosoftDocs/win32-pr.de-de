---
description: Die gettargetrect-Methode ruft das Ziel Rechteck ab. Dies ist eine interne Hilfsmember-Funktion.
ms.assetid: bf9d95c9-eee8-46b8-bdee-a7d16777ed83
title: Cbasecontrolvideo. gettargetrect-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d59a12e134edf37c8ab0a63f46f77923b112605d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364952"
---
# <a name="cbasecontrolvideogettargetrect-method"></a>Cbasecontrolvideo. gettargetrect-Methode

Die- `GetTargetRect` Methode ruft das Ziel Rechteck ab. Dies ist eine interne Hilfsmember-Funktion.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT GetTargetRect(
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

Diese Member-Funktion muss in der abgeleiteten Klasse überschrieben werden, um das Ziel Rechteck zurückzugeben, das der Videorenderer innehat. Sie wird von den folgenden [**cbasecontrolvideo**](cbasecontrolvideo.md) -Element Funktionen aufgerufen.

-   [**Cbasecontrolvideo:: getdestinationposition**](cbasecontrolvideo-getdestinationposition.md)
-   [**Cbasecontrolvideo::p UT \_ destinationleft**](cbasecontrolvideo-put-destinationleft.md)
-   [**Cbasecontrolvideo:: get \_ destinationleft**](cbasecontrolvideo-get-destinationleft.md)
-   [**Cbasecontrolvideo::p UT \_ destinationwidth**](cbasecontrolvideo-put-destinationwidth.md)
-   [**Cbasecontrolvideo:: get \_ destinationwidth**](cbasecontrolvideo-get-destinationwidth.md)
-   [**Cbasecontrolvideo::p UT \_ destinationtop**](cbasecontrolvideo-put-destinationtop.md)
-   [**Cbasecontrolvideo:: get \_ destinationtop**](cbasecontrolvideo-get-destinationtop.md)
-   [**Cbasecontrolvideo::p UT \_ destinationheight**](cbasecontrolvideo-put-destinationheight.md)
-   [**Cbasecontrolvideo:: get \_ destinationheight**](cbasecontrolvideo-get-destinationheight.md)

Im folgenden Beispiel wird eine Implementierung dieser Funktion in einer abgeleiteten Klasse veranschaulicht.


```C++
// Return the current destination rectangle.
HRESULT CVideoText::GetTargetRect(RECT *pTargetRect)
{
    ASSERT(pTargetRect);
    m_pRenderer->m_DrawImage.GetTargetRect(pTargetRect);
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

 

 




