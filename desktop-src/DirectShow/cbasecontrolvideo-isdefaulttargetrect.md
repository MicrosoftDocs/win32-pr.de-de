---
description: Die isdefaulttargetrect-Methode bestimmt, ob der Renderer das standardmäßige Ziel Rechteck (rein virtuell) verwendet.
ms.assetid: 60c09515-7a34-421c-b3e8-ce746a935583
title: Cbasecontrolvideo. isdefaulttargetrect-Methode (ctlutil. h)
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
ms.openlocfilehash: e267cc65345d18800beccbc80ac7952c89d781d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360447"
---
# <a name="cbasecontrolvideoisdefaulttargetrect-method"></a>Cbasecontrolvideo. isdefaulttargetrect-Methode

Die- `IsDefaultTargetRect` Methode bestimmt, ob der Renderer das standardmäßige Ziel Rechteck (rein virtuell) verwendet.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT IsDefaultTargetRect() = 0;
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt s \_ OK zurück, wenn der Renderer das Standardziel verwendet; andernfalls wird s \_ false zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion muss in der abgeleiteten Klasse implementiert werden. Sie wird von der [**cbasecontrolvideo:: isusingdefaultdestination**](cbasecontrolvideo-isusingdefaultdestination.md) -Member-Funktion aufgerufen.

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

 

 




