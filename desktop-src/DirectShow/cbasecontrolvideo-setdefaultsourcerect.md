---
description: Die SetDefaultSourceRect-Methode legt das Standardquellvideorechteck (rein virtuell) fest. Dies in einer internen Memberfunktion, die aufgerufen wird, wenn das Quellrechteck zurückgesetzt wird.
ms.assetid: d0dae0a9-8763-485e-b9d3-80076a3f2f35
title: CBaseControlVideo.SetDefaultSourceRect-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetDefaultSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ae7f2e88e170b0c21187b2615029fcb4ed2bed4717af09b60eb4309aee2bea0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119432610"
---
# <a name="cbasecontrolvideosetdefaultsourcerect-method"></a>CBaseControlVideo.SetDefaultSourceRect-Methode

Die `SetDefaultSourceRect` -Methode legt das Standardquellvideorechteck (rein virtuell) fest. Dies in einer internen Memberfunktion, die aufgerufen wird, wenn das Quellrechteck zurückgesetzt wird.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT SetDefaultSourceRect() = 0;
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Abgeleitete Klassen sollten dies überschreiben, um das Quellrechteck zurückzusetzen. Sie wird von [**CBaseControlVideo::SetDefaultSourcePosition**](cbasecontrolvideo-setdefaultsourceposition.md)aufgerufen.

Im folgenden Beispiel wird eine Implementierung dieser Funktion in einer abgeleiteten Klasse veranschaulicht.


```C++
// This is called when you reset the default source rectangle.
HRESULT CVideoText::SetDefaultSourceRect()
{
    VIDEOINFO *pVideoInfo = (VIDEOINFO *) m_pRenderer->m_mtIn.Format();
    BITMAPINFOHEADER *pHeader = HEADER(pVideoInfo);
    RECT SourceRect = {0,0,pHeader->biWidth,pHeader->biHeight};
    m_pRenderer->m_DrawImage.SetSourceRect(&SourceRect);
    return NOERROR;
}
```



In diesem Beispiel ist CVideoText eine von [**CBaseControlVideo**](cbasecontrolvideo.md)abgeleitete Klasse, m \_ pRenderer enthält ein Objekt einer klasse, die von [**CBaseVideoRenderer**](cbasevideorenderer.md)abgeleitet wurde, und der \_ m DrawImage-Datenmember, der in der abgeleiteten Klasse definiert ist, enthält ein [**CDrawImage-Objekt.**](cdrawimage.md) Der m \_ mtIn-Datenmember, der auch in der abgeleiteten Klasse definiert ist, enthält ein [**CMediaType-Objekt**](cmediatype.md) mit dem Medientyp des Eingabepins.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseControlVideo-Klasse**](cbasecontrolvideo.md)
</dt> </dl>

 

 




