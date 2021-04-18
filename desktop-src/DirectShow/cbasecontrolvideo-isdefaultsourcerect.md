---
description: Die isdefaultsourcerect-Methode bestimmt, ob der Renderer das standardmäßige Quell Rechteck (rein virtuell) verwendet.
ms.assetid: 08c7a365-585c-47e6-9c26-6aa1fa3625e7
title: Cbasecontrolvideo. isdefaultsourcerect-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.IsDefaultSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 390ae779eaa7d640d23b40a7e6f6579e158bf6ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372445"
---
# <a name="cbasecontrolvideoisdefaultsourcerect-method"></a>Cbasecontrolvideo. isdefaultsourcerect-Methode

Die- `IsDefaultSourceRect` Methode bestimmt, ob der Renderer das standardmäßige Quell Rechteck (rein virtuell) verwendet.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT IsDefaultSourceRect() = 0;
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt s \_ OK zurück, wenn der Renderer die Standard Quelle verwendet; andernfalls wird s \_ false zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion muss in der abgeleiteten Klasse implementiert werden. Sie wird von der [**cbasecontrolvideo:: isusingdefaultsource**](cbasecontrolvideo-isusingdefaultsource.md) -Member-Funktion aufgerufen.

Im folgenden Beispiel wird eine Implementierung dieser Funktion in einer abgeleiteten Klasse veranschaulicht.


```C++
// Return S_OK if using the default source; otherwise, S_FALSE.
HRESULT CVideoText::IsDefaultSourceRect()
{
    RECT SourceRect;

    VIDEOINFO *pVideoInfo = (VIDEOINFO *) m_pRenderer->m_mtIn.Format();
    BITMAPINFOHEADER *pHeader = HEADER(pVideoInfo);
    m_pRenderer->m_DrawImage.GetSourceRect(&SourceRect);

    // Check the coordinates that match the video dimensions.

    if (SourceRect.left != 0 || SourceRect.top != 0 ||
            SourceRect.right != pHeader->biWidth ||
                SourceRect.bottom != pHeader->biHeight) {
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

 

 




