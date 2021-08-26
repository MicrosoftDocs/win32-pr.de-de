---
description: Die IsDefaultSourceRect-Methode bestimmt, ob der Renderer das Standardquellenrechteck (rein virtuell) verwendet.
ms.assetid: 08c7a365-585c-47e6-9c26-6aa1fa3625e7
title: CBaseControlVideo.IsDefaultSourceRect-Methode (Ctlutil.h)
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
ms.openlocfilehash: d8cdce3f01bc3a0ed28ee9ce758ef6cb136676a9bd8b4b314547103045e5b284
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056870"
---
# <a name="cbasecontrolvideoisdefaultsourcerect-method"></a>CBaseControlVideo.IsDefaultSourceRect-Methode

Die `IsDefaultSourceRect` -Methode bestimmt, ob der Renderer das Standardquellenrechteck (rein virtuell) verwendet.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT IsDefaultSourceRect() = 0;
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn der Renderer die Standardquelle verwendet; andernfalls wird S \_ FALSE zurückgegeben.

## <a name="remarks"></a>Hinweise

Diese Memberfunktion muss in der abgeleiteten Klasse implementiert werden. Sie wird von der [**CBaseControlVideo::IsUsingDefaultSource-Memberfunktion**](cbasecontrolvideo-isusingdefaultsource.md) aufgerufen.

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



In diesem Beispiel ist CVideoText eine von [**CBaseControlVideo**](cbasecontrolvideo.md)abgeleitete Klasse, m pRenderer enthält ein Objekt einer Klasse, die von CBaseVideoRenderer abgeleitet wurde, und der m DrawImage-Daten member, der in der abgeleiteten Klasse definiert ist, enthält ein \_ [](cbasevideorenderer.md) \_ [**CDrawImage-Objekt.**](cdrawimage.md) Der m mtIn-Daten member, der auch in der abgeleiteten Klasse definiert ist, enthält ein \_ [**CMediaType-Objekt**](cmediatype.md) mit dem Medientyp des Eingabepins.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseControlVideo-Klasse**](cbasecontrolvideo.md)
</dt> </dl>

 

 




