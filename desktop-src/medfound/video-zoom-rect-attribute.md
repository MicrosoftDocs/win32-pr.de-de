---
description: Gibt das Quellrechteck für den Videomixer des erweiterten Videorenderers (EVR) an. Das Quellrechteck ist der Teil des Videoframes, der vom Mixer auf die Zieloberfläche eingeteilt wird.
ms.assetid: 4364ff87-816e-4b64-b5e9-c53dd6c9bb33
title: VIDEO_ZOOM_RECT -Attribut (Evr.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2e6ce19c808545d400f53b9c0091cdbcc20c8efbc13372ae5386e419d244143
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118737145"
---
# <a name="video_zoom_rect-attribute"></a>VIDEO \_ ZOOM \_ RECT-Attribut

Gibt das Quellrechteck für den Videomixer des [erweiterten Videorenderers](enhanced-video-renderer.md) (EVR) an. Das Quellrechteck ist der Teil des Videoframes, der vom Mixer auf die Zieloberfläche eingeteilt wird.

## <a name="data-type"></a>Datentyp

Bytearray

## <a name="remarks"></a>Hinweise

Der Wert dieses Attributs ist eine [**MFVideoNormalizedRect-Struktur.**](/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect)

Das Quellrechteck wird relativ zu einem normalisierten Koordinatensystem definiert, in dem der gesamte Videoframe ein Rechteck mit den Koordinaten {0, 0, 1, 1} einnimmt. Das Quellrechteck muss in den Videoframe passen. Die Koordinaten des Quellrechtecks haben einen Bereich von (0...1).

Die EVR-Standard-Moderatorin legt dieses Attribut auf dem Mixer fest. Gehen Sie wie folgt vor, um das Attribut zu festlegen:

1.  Rufen [**Sie IMTRANSFORM::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) im Mixer auf, um den Attributspeicher des Mixers zu erhalten.
2.  Rufen [**Sie DIE ATTRIBUTE::SetBlob auf,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob) um das **VIDEO ZOOM \_ \_ RECT-Attribut** für den Mixer zu setzen. Der Wert ist eine [**MFVideoNormalizedRect-Struktur.**](/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect)

In einem benutzerdefinierten EVR-Presenter können Sie dieses Attribut verwenden, um die [**METHODE DURCHZEIGERVideoDisplayControl::SetVideoPosition zu**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) implementieren. Weitere Informationen finden Sie unter [Quell- und Zielrechtecke.](how-to-write-an-evr-presenter.md)

Die GUID-Konstante für dieses Attribut wird aus strmiids.lib exportiert.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das Quellrechteck für den Mixer definiert.


```C++
HRESULT SetMixerSourceRect(IMFTransform *pMixer, const MFVideoNormalizedRect& nrcSource)
{
    if (pMixer == NULL)
    {
        return E_POINTER;
    }

    IMFAttributes *pAttributes = NULL;

    HRESULT hr = pMixer->GetAttributes(&pAttributes);
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetBlob(VIDEO_ZOOM_RECT, (const UINT8*)&nrcSource, sizeof(nrcSource));
        pAttributes->Release();
    }
    return hr;
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Evr.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Erweiterte Videorendererattribute](enhanced-video-renderer-attributes.md)
</dt> <dt>

[Schreiben eines EVR-Presenters](how-to-write-an-evr-presenter.md)
</dt> <dt>

[**ATTRIBUTEs::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**ATTRIBUTEs::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> </dl>

 

 




