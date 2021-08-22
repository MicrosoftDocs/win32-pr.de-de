---
description: Reine virtuelle Methode, die von abgeleiteten Klassen überschrieben wird.
ms.assetid: 05c73f6b-27f4-4930-b4d5-1688b6bf1791
title: CBaseControlVideo.GetStaticImage-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetStaticImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 69496754c8a1f80be341c475f422229aba6108dbc0e73cd1db9506a301690ffa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660830"
---
# <a name="cbasecontrolvideogetstaticimage-method"></a>CBaseControlVideo.GetStaticImage-Methode

Reine virtuelle Methode, die von abgeleiteten Klassen überschrieben wird.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT GetStaticImage(
   long *pBufferSize,
   long *pDIBImage
) = 0;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pBufferSize* 
</dt> <dd>

Zeiger auf die Größe des Ausgabepuffers.

</dd> <dt>

*pDIBImage* 
</dt> <dd>

Zeiger auf den Ausgabepuffer.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Über die [**IBasicVideo-Schnittstelle**](/windows/desktop/api/Control/nn-control-ibasicvideo) kann eine Anwendung anfordern, dass sie eine Kopie des aktuellen Bilds in einem Speicherpuffer erhält (einige Renderer können E NOTIMPL an diese zurückgeben, wenn sie es nicht \_ unterstützen). Die abgeleitete Klasse bestimmt, wie das Bild abgerufen wird. Wenn die Anwendung **CBaseControlVideo::GetStaticImage** aufruft, ruft sie diese reine virtuelle Methode auf, die die abgeleitete Klasse überschreiben sollte, um sie zu implementieren. Dies wird auch von der [**CBaseControlVideo::GetCurrentImage-Memberfunktion**](cbasecontrolvideo-getcurrentimage.md) aufgerufen.

Die -Klasse stellt die Hilfsfunktion [**CBaseControlVideo::CopyImage**](cbasecontrolvideo-copyimage.md)zur Verfügung, der ein Beispiel mit einem Bild gegeben werden kann, und die Memberfunktion kopiert den relevanten Abschnitt davon (basierend auf dem aktuellen Quellrechteck) in den von der Anwendung bereitgestellten Ausgabepuffer.

Im folgenden Beispiel wird eine Implementierung dieser Memberfunktion in einer abgeleiteten Klasse veranschaulicht. In diesem Beispiel enthält m pRenderer ein Objekt einer Klasse, die von \_ [**CBaseVideoRenderer abgeleitet wurde.**](cbasevideorenderer.md)


```C++
// Return a copy of the current image in the video renderer
HRESULT CVideoText::GetStaticImage(long *pBufferSize,long *pDIBImage)
{
    // Get any sample the renderer may be holding.

    IMediaSample *pMediaSample = m_pRenderer->GetCurrentSample();
    if (pMediaSample == NULL) {
        return E_UNEXPECTED;
    }

    // Call the base class helper method to do the work.

    HRESULT hr = CopyImage(pMediaSample,       // Buffer containing image
                      &m_pRenderer->m_mtIn,    // Type representing bitmap
                      pBufferSize,             // Size of buffer for DIB
                     (BYTE*) pDIBImage);       // Data buffer for output

    pMediaSample->Release();
    return hr;
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseControlVideo-Klasse**](cbasecontrolvideo.md)
</dt> </dl>

 

 




