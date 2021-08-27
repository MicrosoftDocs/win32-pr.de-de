---
description: Die SetDefaultTargetRect-Methode legt das Standardmäßige Zielvideorechteck (rein virtuell) fest. Dies ist eine interne Memberfunktion, die aufgerufen wird, wenn das Quellrechteck zurückgesetzt wird.
ms.assetid: bb7e32b2-f02c-465f-a8cb-6172d9724790
title: CBaseControlVideo.SetDefaultTargetRect-Methode (Ctlutil.h)
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
ms.openlocfilehash: 1ab9cf310ffc35df07ecd9e332325bb5f20f3cb4884ee17e672294b89c5abc9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087480"
---
# <a name="cbasecontrolvideosetdefaulttargetrect-method"></a>CBaseControlVideo.SetDefaultTargetRect-Methode

Die `SetDefaultTargetRect` -Methode legt das Standardmäßige Zielvideorechteck (rein virtuell) fest. Dies ist eine interne Memberfunktion, die aufgerufen wird, wenn das Quellrechteck zurückgesetzt wird.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT SetDefaultTargetRect() = 0;
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Abgeleitete Klassen sollten dies überschreiben, um das Zielvideorechteck zurückzusetzen. Sie wird von der [**CBaseControlVideo::SetDefaultDestinationPosition-Memberfunktion**](cbasecontrolvideo-setdefaultdestinationposition.md) aufgerufen.

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



In diesem Beispiel ist CVideoText eine von [**CBaseControlVideo**](cbasecontrolvideo.md)abgeleitete Klasse, m \_ pRenderer enthält ein Objekt einer klasse, die von [**CBaseVideoRenderer**](cbasevideorenderer.md)abgeleitet wurde, und der \_ m DrawImage-Datenmember, der in der abgeleiteten Klasse definiert ist, enthält ein [**CDrawImage-Objekt.**](cdrawimage.md) Der m \_ mtIn-Datenmember, der auch in der abgeleiteten Klasse definiert ist, enthält ein [**CMediaType-Objekt**](cmediatype.md) mit dem Medientyp des Eingabepins.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseControlVideo-Klasse**](cbasecontrolvideo.md)
</dt> </dl>

 

 




