---
description: Die getsourcerect-Methode ruft das Quell Rechteck ab. Dies ist eine interne Methode.
ms.assetid: 51028b79-6aab-4abc-8ee8-2965bda9d191
title: Cbasecontrolvideo. getsourcerect-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e57a5beda7b147e952ecbb26c96df5f7e372e6d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372337"
---
# <a name="cbasecontrolvideogetsourcerect-method"></a>Cbasecontrolvideo. getsourcerect-Methode

Die- `GetSourceRect` Methode ruft das Quell Rechteck ab. Dies ist eine interne Methode.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT GetSourceRect(
   RECT *pSourceRect
) = 0;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*psourcerect* 
</dt> <dd>

Zeiger auf das abgerufene Quell Rechteck.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion muss in der abgeleiteten Klasse überschrieben werden, um das vom Videorenderer gehaltene Quell Rechteck zurückzugeben. Sie wird von den folgenden [**cbasecontrolvideo**](cbasecontrolvideo.md) -Element Funktionen aufgerufen.

-   [**Cbasecontrolvideo:: getsourceposition**](cbasecontrolvideo-getsourceposition.md)
-   [**Cbasecontrolvideo::p UT \_ sourceLeft**](cbasecontrolvideo-put-sourceleft.md)
-   [**Cbasecontrolvideo:: get \_ sourceLeft**](cbasecontrolvideo-get-sourceleft.md)
-   [**Cbasecontrolvideo::p UT \_ sourceWidth**](cbasecontrolvideo-put-sourcewidth.md)
-   [**Cbasecontrolvideo:: get \_ sourceWidth**](cbasecontrolvideo-get-sourcewidth.md)
-   [**Cbasecontrolvideo::p UT \_ sourceTop**](cbasecontrolvideo-put-sourcetop.md)
-   [**Cbasecontrolvideo:: get \_ sourceTop**](cbasecontrolvideo-get-sourcetop.md)
-   [**Cbasecontrolvideo::p UT \_ sourceHeight**](cbasecontrolvideo-put-sourceheight.md)
-   [**Cbasecontrolvideo:: get \_ sourceHeight**](cbasecontrolvideo-get-sourceheight.md)

Im folgenden Beispiel wird eine Implementierung dieser Funktion in einer abgeleiteten Klasse veranschaulicht.


```C++
// Return the current source rectangle
HRESULT CVideoText::GetSourceRect(RECT *pSourceRect)
{
    ASSERT(pSourceRect);
    m_pRenderer->m_DrawImage.GetSourceRect(pSourceRect);
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

 

 




