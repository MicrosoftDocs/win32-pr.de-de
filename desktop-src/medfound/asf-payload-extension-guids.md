---
description: Die folgenden GUIDs definieren Nutz Last Erweiterungen für ASF-Streams (Advanced Systems Format).
ms.assetid: db973b41-1e5c-4bc8-921d-5e9312eb21cb
title: Namen der ASF-Nutz Last Erweiterung (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb7dbd27212c8f4812360ba22f89a717659307f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524664"
---
# <a name="asf-payload-extension-guids"></a>Namen der ASF-Nutz Last Erweiterung

Die folgenden GUIDs definieren Nutz Last Erweiterungen für ASF-Streams (Advanced Systems Format).



| Konstante                                                                                                                                                                                                                                                                                      | BESCHREIBUNG                                                                                                                                                                      |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASFSampleExtension_SampleDuration"></span><span id="mfasfsampleextension_sampleduration"></span><span id="MFASFSAMPLEEXTENSION_SAMPLEDURATION"></span><dl> <dt>**Mfasf Sample Extension \_ sampleduration**</dt> </dl>         | Die Daten zeigen die Dauer (in Millisekunden) des im Buffer-Objekt enthaltenen Beispiels an.<br/>                                                                       |
| <span id="MFASFSampleExtension_OutputCleanPoint"></span><span id="mfasfsampleextension_outputcleanpoint"></span><span id="MFASFSAMPLEEXTENSION_OUTPUTCLEANPOINT"></span><dl> <dt>**Mfasf Sample Extension \_ outputcleanpoint**</dt> </dl> | Die Daten zeigen an, ob das Beispiel ein Keyframe ist. Der Wert 0 (null) gibt an, dass das Beispiel kein Keyframe ist. Ein Wert ungleich NULL gibt an, dass es sich um einen Keyframe handelt.<br/> |
| <span id="MFASFSampleExtension_SMPTE"></span><span id="mfasfsampleextension_smpte"></span><span id="MFASFSAMPLEEXTENSION_SMPTE"></span><dl> <dt>**Mfasssampleextension ( \_ SMPTE)**</dt> </dl>                                             | Bei den Daten handelt es sich um einen SMPTE-Zeit Code.<br/>                                                                                                                                        |
| <span id="MFASFSampleExtension_FileName"></span><span id="mfasfsampleextension_filename"></span><span id="MFASFSAMPLEEXTENSION_FILENAME"></span><dl> <dt>**Mfasf Sample Extension- \_ Dateiname**</dt> </dl>                                 | Die Daten in der Beispiel Erweiterung geben den Namen der Datei an, aus der der Inhalt in der Stichprobe entnommen wurde.<br/>                                                       |
| <span id="MFASFSampleExtension_ContentType"></span><span id="mfasfsampleextension_contenttype"></span><span id="MFASFSAMPLEEXTENSION_CONTENTTYPE"></span><dl> <dt>**Mfasf Sample Extension- \_ ContentType**</dt> </dl>                     | Die Daten identifizieren den Inhaltstyp, den das Beispiel enthält.<br/>                                                                                                     |
| <span id="MFASFSampleExtension_PixelAspectRatio"></span><span id="mfasfsampleextension_pixelaspectratio"></span><span id="MFASFSAMPLEEXTENSION_PIXELASPECTRATIO"></span><dl> <dt>**Mfasf Sample Extension \_ pixelaspectratio**</dt> </dl> | Die Daten zeigen das Pixel Seitenverhältnis des Inhalts in der Stichprobe an.<br/>                                                                                               |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imfasf streamconfig:: addpayloadextension**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-addpayloadextension)
</dt> <dt>

[**Imfasf streamconfig:: getpayloadextension**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getpayloadextension)
</dt> <dt>

[Media Foundation Konstanten](media-foundation-constants.md)
</dt> </dl>

 

 




