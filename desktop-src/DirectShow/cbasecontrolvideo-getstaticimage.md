---
description: Reine virtuelle Methode, die abgeleitete Klassen überschreiben.
ms.assetid: 05c73f6b-27f4-4930-b4d5-1688b6bf1791
title: Cbasecontrolvideo. getstaticimage-Methode (ctlutil. h)
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
ms.openlocfilehash: 13b0515e20202373954050b6fa18f10a20a76a6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365475"
---
# <a name="cbasecontrolvideogetstaticimage-method"></a>Cbasecontrolvideo. getstaticimage-Methode

Reine virtuelle Methode, die abgeleitete Klassen überschreiben.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT GetStaticImage(
   long *pBufferSize,
   long *pDIBImage
) = 0;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbuffersize* 
</dt> <dd>

Ein Zeiger auf die Größe des Ausgabepuffers.

</dd> <dt>

*pdibimage* 
</dt> <dd>

Zeiger auf den Ausgabepuffer.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Mithilfe der [**ibasicvideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) -Schnittstelle kann eine Anwendung anfordern, dass Sie eine Kopie des aktuellen Bilds in einem Arbeitsspeicher Puffer erhält (einige Renderer können E \_ notimpl zurückgeben, wenn Sie Sie nicht unterstützen). Die abgeleitete Klasse bestimmt, wie das Bild abgerufen wird. Wenn die Anwendung **cbasecontrolvideo:: getstaticimage** aufruft, ruft Sie diese rein virtuelle Methode auf, die von der abgeleiteten Klasse überschrieben werden soll, um Sie zu implementieren. Dies wird auch durch die Member-Funktion [**cbasecontrolvideo:: Get-timage**](cbasecontrolvideo-getcurrentimage.md) aufgerufen.

Die-Klasse stellt eine Hilfsmember-Funktion, [**cbasecontrolvideo:: CopyImage**](cbasecontrolvideo-copyimage.md), bereit, die ein Beispiel erhalten kann, das ein Bild enthält, und die Member-Funktion kopiert den relevanten Abschnitt des Elements (auf Grundlage des aktuellen Quell Rechtecks) in den von der Anwendung bereitgestellten Ausgabepuffer.

Im folgenden Beispiel wird eine Implementierung dieser Member-Funktion in einer abgeleiteten Klasse veranschaulicht. In diesem Beispiel \_ enthält der m-prenderer ein Objekt einer Klasse, die von [**cbasevideorenderer**](cbasevideorenderer.md)abgeleitet ist.


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
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolvideo-Klasse**](cbasecontrolvideo.md)
</dt> </dl>

 

 




