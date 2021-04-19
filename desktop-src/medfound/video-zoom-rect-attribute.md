---
description: Gibt das Quell Rechteck für den Videomixer des erweiterten Videorenderer (EVR) an. Das Quell Rechteck ist der Teil des Video Rahmens, der vom Mixer an die Ziel Oberfläche blitet.
ms.assetid: 4364ff87-816e-4b64-b5e9-c53dd6c9bb33
title: VIDEO_ZOOM_RECT-Attribut (EVR. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dda4efca5beab844baf3b3f53074d6b3012e8621
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356573"
---
# <a name="video_zoom_rect-attribute"></a>Video \_ Zoom- \_ Rect-Attribut

Gibt das Quell Rechteck für den Videomixer des [erweiterten Videorenderer](enhanced-video-renderer.md) (EVR) an. Das Quell Rechteck ist der Teil des Video Rahmens, der vom Mixer an die Ziel Oberfläche blitet.

## <a name="data-type"></a>Datentyp

Bytearray

## <a name="remarks"></a>Bemerkungen

Der Wert dieses Attributs ist eine [**MF videonormalizedrect**](/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect) -Struktur.

Das Quell Rechteck wird relativ zu einem normalisierten Koordinatensystem definiert, in dem der gesamte Videorahmen ein Rechteck mit den Koordinaten {0, 0, 1, 1} einnimmt. Das Quell Rechteck muss in den Videoframe passen. die Koordinaten des Quell Rechtecks haben einen Bereich von (0... 1).

Der Standard-EVR Presenter legt dieses Attribut auf dem Mixer fest. Gehen Sie folgendermaßen vor, um das-Attribut festzulegen:

1.  Aufrufen von [**imftransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) auf dem Mixer, um den Attribut Speicher des Mischers abzurufen.
2.  Aufrufen von [**imfattributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob) , um das **Video Zoom- \_ \_ Rect** -Attribut auf dem Mixer festzulegen. Der Wert ist eine [**MF videonormalizedrect**](/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect) -Struktur.

In einem benutzerdefinierten EVR Presenter können Sie dieses Attribut verwenden, um die [**imfvideodisplaycontrol:: setvideoposition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) -Methode zu implementieren. Weitere Informationen finden Sie unter [Quell-und Ziel Rechtecke](how-to-write-an-evr-presenter.md).

Die GUID-Konstante für dieses Attribut wird aus "straumiids. lib" exportiert.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das Quell Rechteck auf dem Mixer festgelegt.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                   |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>EVR. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Erweiterte Videorenderer-Attribute](enhanced-video-renderer-attributes.md)
</dt> <dt>

[Schreiben von EVR Presenter](how-to-write-an-evr-presenter.md)
</dt> <dt>

[**Imfattributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**Imfattributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> </dl>

 

 




