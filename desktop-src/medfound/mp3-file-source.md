---
description: Die MP3-Dateiquelle analysiert MP3-Dateien.
ms.assetid: 37362642-1b8a-4fb3-950d-ed1afe3696e5
title: MP3-Dateiquelle
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c95e54319fb189fa3bcc366b554b4d6555b2f4a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479836"
---
# <a name="mp3-file-source"></a>MP3-Dateiquelle

Die MP3-Dateiquelle analysiert MP3-Dateien.

Die MP3-Dateiquelle gibt Puffer aus, die MPEG-1-Audioframes enthalten. Die Audiodaten werden nicht decodiert.

## <a name="file-extensions-and-mime-types"></a>Dateierweiterungen und MIME-Typen

Die MP3-Dateiquelle ist die Standardmedienquelle für die folgende Dateierweiterung:

-   .mp3

Es ist auch die Standardmedienquelle für die folgenden MIME-Typen.

-   audio/mpeg
-   audio/x-mp3
-   audio/x-mpeg

## <a name="media-types"></a>Medientypen

Der von der MP3-Dateiquelle angebotene Medientyp enthält die folgenden Attribute.



| Attribut                                                                                    | BESCHREIBUNG                                                                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MF \_ \_ MT-HAUPTTYP \_**](mf-mt-major-type-attribute.md)                                    | Entspricht **MFMediaType \_ Audio**.                                                                                                                   |
| [**MF \_ \_ MT-UNTERTYP**](mf-mt-subtype-attribute.md)                                           | Entspricht **MFAudioFormat \_ MP3 oder** **MFAudioFormat \_ MPEG**.                                                                                        |
| [**MF \_ MT \_ AUDIO \_ AVG \_ BYTES \_ PER \_ SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) | Durchschnittliche Anzahl von Bytes pro Sekunde.                                                                                                                |
| [**MF MT AUDIO BLOCK ALIGNMENT (MF \_ \_ MT-AUDIOBLOCKAUSRICHTUNG) \_ \_**](mf-mt-audio-block-alignment-attribute.md)             | Gleich 1.                                                                                                                                        |
| [**MF \_ MT AUDIO \_ \_ \_ NUM-KANÄLE**](mf-mt-audio-num-channels-attribute.md)                   | Anzahl der Audiokanäle.                                                                                                                          |
| [**MF \_ \_ MT-AUDIOBEISPIELE \_ \_ PRO \_ SEKUNDE**](mf-mt-audio-samples-per-second-attribute.md)      | Anzahl von Audiobeispielen pro Sekunde.                                                                                                                |
| [**MF \_ \_ MT-BENUTZERDATEN \_**](mf-mt-user-data-attribute.md)                                      | Enthält den Teil einer [**MPEGLAYER3WAVEFORMAT-Struktur,**](/windows/win32/api/mmreg/ns-mmreg-mpeglayer3waveformat) der nach dem **wfx-Member** der -Struktur angezeigt wird. |



 

## <a name="interfaces"></a>Schnittstellen

Die MP3-Dateiquelle macht die folgenden Schnittstellen über [**QueryInterface verfügbar:**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))

-   [**GEGETService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**VERERBUNGMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
-   [**VERERBUNGMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)

Darüber hinaus werden die folgenden Schnittstellen über [**DENTGETService verfügbar macht:**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)




| Dienst-GUID | Schnittstelle | 
|--------------|-----------|
| <strong>MF_METADATA_PROVIDER_SERVICE</strong> | <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider"><strong>ANBIETERMetadataProvider</strong></a> | 
| <strong>MF_PROPERTY_HANDLER_SERVICE</strong> | <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>Ipropertystore</strong></a><blockquote>[!Note]<br />Weitere Informationen finden <a href="shell-metadata-providers.md">Sie unter Shell metadata providers (Shellmetadatenanbieter).</a></blockquote><br /><br /> | 
| <strong>MF_RATE_CONTROL_SERVICE</strong> | <a href="/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol"><strong>DURCHSCHN.RateControl</strong></a> | 
| <strong>MF_RATE_CONTROL_SERVICE</strong> | <a href="/windows/desktop/api/mfidl/nn-mfidl-imfratesupport"><strong>VERRATRateSupport</strong></a> | 




 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                           |
| DLL<br/>                      | <dl> <dt>Mf.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Medienquellen und -senken](media-sources-and-sinks.md)
</dt> <dt>

[Medienquellen](media-sources.md)
</dt> <dt>

[Quellre resolver](source-resolver.md)
</dt> <dt>

[Unterstützte Medienformate in Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 
