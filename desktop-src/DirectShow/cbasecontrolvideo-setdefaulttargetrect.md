---
description: Mit der setdefaulttargetrect-Methode wird das standardmäßige Ziel Video Rechteck (rein virtuell) festgelegt. Dies ist eine interne Member-Funktion, die beim Zurücksetzen des Quell Rechtecks aufgerufen wird.
ms.assetid: bb7e32b2-f02c-465f-a8cb-6172d9724790
title: Cbasecontrolvideo. setdefaulttargetrect-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetDefaultTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54b31268935cb296543b3992bf67b7a2193c1a92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372079"
---
# <a name="cbasecontrolvideosetdefaulttargetrect-method"></a>Cbasecontrolvideo. setdefaulttargetrect-Methode

Mit der- `SetDefaultTargetRect` Methode wird das standardmäßige Ziel Video Rechteck (rein virtuell) festgelegt. Dies ist eine interne Member-Funktion, die beim Zurücksetzen des Quell Rechtecks aufgerufen wird.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT SetDefaultTargetRect() = 0;
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Abgeleitete Klassen sollten diese überschreiben, um das Ziel Video Rechteck zurückzusetzen. Sie wird von der [**cbasecontrolvideo:: setdefaultdestinationposition**](cbasecontrolvideo-setdefaultdestinationposition.md) -Member-Funktion aufgerufen.

Im folgenden Beispiel wird eine Implementierung dieser Funktion in einer abgeleiteten Klasse veranschaulicht.


```C++
// This is called when you reset the default target rectangle.
HRESULT CVideoText::SetDefaultTargetRect()
{
    VIDEOINFO *pVideoInfo = (VIDEOINFO *) m_pRenderer->m_mtIn.Format();
    BITMAPINFOHEADER *pHeader = HEADER(pVideoInfo);
    RECT TargetRect = {0,0,m_Size.cx,m_Size.cy};
    m_pRenderer->m_DrawImage.SetTargetRect(&TargetRect);
    return NOERROR;
}
```



In diesem Beispiel ist cvideotext eine Klasse, die von [**cbasecontrolvideo**](cbasecontrolvideo.md)abgeleitet ist. m \_ prenderer enthält ein Objekt einer Klasse, die von [**cbasevideorenderer**](cbasevideorenderer.md)abgeleitet ist, und das \_ in der abgeleiteten Klasse definierte Datenmember m DrawImage enthält ein [**cdrawimage**](cdrawimage.md) -Objekt. Der m \_ MTiN-Datenmember, der auch in der abgeleiteten Klasse definiert ist, enthält ein [**cmediatype**](cmediatype.md) -Objekt mit dem Medientyp der Eingabe-PIN.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolvideo-Klasse**](cbasecontrolvideo.md)
</dt> </dl>

 

 




