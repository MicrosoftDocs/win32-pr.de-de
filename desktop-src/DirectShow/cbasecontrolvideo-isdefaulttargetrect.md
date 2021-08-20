---
description: Die IsDefaultTargetRect-Methode bestimmt, ob der Renderer das Standardzielrechteck (rein virtuell) verwendet.
ms.assetid: 60c09515-7a34-421c-b3e8-ce746a935583
title: CBaseControlVideo.IsDefaultTargetRect-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.IsDefaultTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c11d5b99610ff88a9e5f4088aa47efdcd8f3d9d676f0b17fad4d8e316324e807
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955239"
---
# <a name="cbasecontrolvideoisdefaulttargetrect-method"></a>CBaseControlVideo.IsDefaultTargetRect-Methode

Die `IsDefaultTargetRect` -Methode bestimmt, ob der Renderer das Standardzielrechteck (rein virtuell) verwendet.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT IsDefaultTargetRect() = 0;
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn der Renderer das Standardziel verwendet, andernfalls S \_ FALSE.

## <a name="remarks"></a>Hinweise

Diese Memberfunktion muss in der abgeleiteten Klasse implementiert werden. Sie wird von der [**CBaseControlVideo::IsUsingDefaultDestination-Memberfunktion**](cbasecontrolvideo-isusingdefaultdestination.md) aufgerufen.

Im folgenden Beispiel wird eine Implementierung dieser Funktion in einer abgeleiteten Klasse veranschaulicht.


```C++
// Return S_OK if using the default target; otherwise, S_FALSE.
HRESULT CVideoText::IsDefaultTargetRect()
{
    RECT TargetRect;

    VIDEOINFO *pVideoInfo = (VIDEOINFO *) m_pRenderer->m_mtIn.Format();
    BITMAPINFOHEADER *pHeader = HEADER(pVideoInfo);
    m_pRenderer->m_DrawImage.GetTargetRect(&TargetRect);

    // Check the destination that matches the initial client area.

    if (TargetRect.left != 0 || TargetRect.top != 0 ||
            TargetRect.right != m_Size.cx ||
                TargetRect.bottom != m_Size.cy) {
                    return S_FALSE;
    }
    return S_OK;
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

 

 




