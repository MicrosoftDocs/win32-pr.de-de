---
description: Die folgenden GUIDs definieren Nutzlasterweiterungen für ASF-Datenströme (Advanced Systems Format).
ms.assetid: db973b41-1e5c-4bc8-921d-5e9312eb21cb
title: GUIDs der ASF-Nutzlasterweiterung (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6478c024d3e79b0f8035f03b6e893e2e5d0308037242f9ac3013450b57f83242
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959570"
---
# <a name="asf-payload-extension-guids"></a>ASF-Nutzlasterweiterungs-GUIDs

Die folgenden GUIDs definieren Nutzlasterweiterungen für ASF-Datenströme (Advanced Systems Format).



| Konstante                                                                                                                                                                                                                                                                                      | Beschreibung                                                                                                                                                                      |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASFSampleExtension_SampleDuration"></span><span id="mfasfsampleextension_sampleduration"></span><span id="MFASFSAMPLEEXTENSION_SAMPLEDURATION"></span><dl> <dt>**MFASFSampleExtension \_ SampleDuration**</dt> </dl>         | Die Daten geben die Dauer des im Pufferobjekt enthaltenen Beispiels in Millisekunden an.<br/>                                                                       |
| <span id="MFASFSampleExtension_OutputCleanPoint"></span><span id="mfasfsampleextension_outputcleanpoint"></span><span id="MFASFSAMPLEEXTENSION_OUTPUTCLEANPOINT"></span><dl> <dt>**MFASFSampleExtension \_ OutputCleanPoint**</dt> </dl> | Die Daten geben an, ob es sich bei der Stichprobe um einen Keyframe handelt. Der Wert 0 (null) gibt an, dass es sich bei der Stichprobe nicht um einen Keyframe handelt. Ein Wert ungleich 0 (null) gibt an, dass es sich um einen Keyframe handelt.<br/> |
| <span id="MFASFSampleExtension_SMPTE"></span><span id="mfasfsampleextension_smpte"></span><span id="MFASFSAMPLEEXTENSION_SMPTE"></span><dl> <dt>**MFASFSampleExtension \_ SMPTE**</dt> </dl>                                             | Die Daten sind ein SMPTE-Zeitcode.<br/>                                                                                                                                        |
| <span id="MFASFSampleExtension_FileName"></span><span id="mfasfsampleextension_filename"></span><span id="MFASFSAMPLEEXTENSION_FILENAME"></span><dl> <dt>**MFASFSampleExtension \_ FileName**</dt> </dl>                                 | Die Daten in der Beispielerweiterung geben den Namen der Datei an, aus der der Inhalt des Beispiels entnommen wurde.<br/>                                                       |
| <span id="MFASFSampleExtension_ContentType"></span><span id="mfasfsampleextension_contenttype"></span><span id="MFASFSAMPLEEXTENSION_CONTENTTYPE"></span><dl> <dt>**MFASFSampleExtension \_ ContentType**</dt> </dl>                     | Die Daten geben den Inhaltstyp an, der im Beispiel enthalten ist.<br/>                                                                                                     |
| <span id="MFASFSampleExtension_PixelAspectRatio"></span><span id="mfasfsampleextension_pixelaspectratio"></span><span id="MFASFSAMPLEEXTENSION_PIXELASPECTRATIO"></span><dl> <dt>**MFASFSampleExtension \_ PixelAspectRatio**</dt> </dl> | Die Daten geben das Pixel-Seitenverhältnis des Inhalts im Beispiel an.<br/>                                                                                               |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Wmcontainer.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMFASFStreamConfig::AddPayloadExtension**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-addpayloadextension)
</dt> <dt>

[**IMFASFStreamConfig::GetPayloadExtension**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getpayloadextension)
</dt> <dt>

[Media Foundation Konstanten](media-foundation-constants.md)
</dt> </dl>

 

 




