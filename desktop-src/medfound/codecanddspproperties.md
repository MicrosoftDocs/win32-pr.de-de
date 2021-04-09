---
description: Codec-und DSP-IPropertyBag-Konstanten.
ms.assetid: 078b0eea-16dd-4427-b984-9e52a43de559
title: Codec-und DSP-IPropertyBag-Konstanten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88dcf85e22f55082bb9e2c49041490f4c7aceb2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127996"
---
# <a name="codec-and-dsp-ipropertybag-constants"></a>Codec-und DSP-IPropertyBag-Konstanten

Es gibt zwei Methoden, um Eigenschaften für die Codec-und DSP-Objekte Programm gesteuert festzulegen, indem Sie entweder die **IPropertyBag** -Schnittstelle oder die **IPropertyStore** -Schnittstelle verwenden. Die gängigsten Eigenschaften sind über beide Schnittstellen verfügbar. Die Verwendung der **IPropertyStore** -Schnittstelle wird gegenüber **IPropertyBag** bevorzugt.



| IPropertyBag-Zeichen folgen Konstante          | IPropertyStore-Eigenschafts Schlüssel                                                                         |
|---------------------------------------|-----------------------------------------------------------------------------------------------------|
| g \_ wszavgframerate                    | [mfpkey \_ asfoverheadperframe](mfpkey-asfoverheadperframeproperty.md)                               |
| g \_ wszwmacavgbytespersecond           | [mfpkey \_ wmaaufc \_ avgbytespersec](mfpkey-wmaenc-avgbytespersecproperty.md)                          |
| g \_ wszwmacdrcsetting                  | [mfpkey \_ wmadec \_ drcmode](mfpkey-wmadec-drcmodeproperty.md)                                        |
| g \_ wszwmachiresoutput                 | [mfpkey \_ wmadec \_ hiresoutput](mfpkey-wmadec-hiresoutputproperty.md)                                |
| g \_ wszwmacmusicredner classmode        | [Mfpkey \_ wmavoice \_ ENC \_ musicvoiceclassmode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) |
| g \_ wszwmacoriginalwaveformat          | [mfpkey \_ wmaenc \_ origwaveformat](mfpkey-wmaenc-origwaveformatproperty.md)                          |
| g \_ wszwmacspeakerconfig               | [mfpkey \_ wmadec \_ spkrcfg](mfpkey-wmadec-spkrcfgproperty.md)                                        |
| g \_ wszwmacvoicebuffer                 | [Mfpkey \_ wmavoice \_ ENC \_ bufferwindow](mfpkey-wmavoice-enc-bufferwindowproperty.md)                 |
| g \_ wszwmacvoicebuffer                 | [mfpkey \_ wmavoice- \_ UMC \_ EDL](mfpkey-wmavoice-enc-edlproperty.md)                                   |
| g \_ wszwmadrcaveragereferenzierung          | [mfpkey \_ wmadrc \_ avgref](mfpkey-wmadrc-avgrefproperty.md)                                          |
| g \_ wszwmadrcaveragetarget             | [mfpkey \_ wmademokratische \_ avgtarget](mfpkey-wmadrc-avgtargetproperty.md)                                    |
| g \_ wszwmadrcpeer Reference             | [mfpkey \_ wmadrc- \_ Peer-Ref](mfpkey-wmadrc-peakrefproperty.md)                                        |
| g \_ wszwmadrcpeer Target                | [mfpkey \_ wmadrc- \_ Peer Ziel](mfpkey-wmadrc-peaktargetproperty.md)                                  |
| g \_ wszwmcpaudiovbrquality             | [mfpkey \_ vbrquality](mfpkey-vbrqualityproperty.md)                                                 |
| g \_ wszwmcpaudiovbrsupported           | [mfpkey \_ vbrenabled](mfpkey-vbrenabledproperty.md)                                                 |
| g \_ wszwmcpmaxpass                   | [mfpkey- \_ passesempfohlen](mfpkey-passesrecommendedproperty.md)                                   |
| g \_ wszwmvcavgbitrate                  | [mfpkey \_ Ravg](mfpkey-ravgproperty.md)                                                             |
| g \_ wszwmvcbavg                        | [mfpkey \_ bavg](mfpkey-bavgproperty.md)                                                             |
| g \_ wszwmvcbdelta taqp                    | [mfpkey \_ bdelta taqp](mfpkey-bdeltaqpproperty.md)                                                     |
| g \_ wszwmvcbmax                        | [mfpkey ( \_ bmax)](mfpkey-bmaxproperty.md)                                                             |
| g \_ wszwmvcbufferfullnessinfirstbyte   | [mfpkey \_ bufferfullnessinfirstbyte](mfpkey-bufferfullnessinfirstbyteproperty.md)                   |
| g \_ wszwmvccodedframes                 | [mfpkey- \_ codedframes](mfpkey-codedframesproperty.md)                                               |
| g \_ wszwmvccomplexityex                | [\_complexityex für mfpkey](mfpkey-complexityexproperty.md)                                             |
| g \_ wszwmvccomplexitymode              | [mfpkey- \_ Komplexität](mfpkey-complexityproperty.md)                                                 |
| g \_ wszwmvccompressionoptimizationtype | [mfpkey \_ compressionoptimizationtype](mfpkey-compressionoptimizationtypeproperty.md)               |
| g \_ wszwmvccrisp                       | [mfpkey \_ Crisp](mfpkey-crispproperty.md)                                                           |
| g \_ wszwmvcdecodercomplexityprofile    | [mfpkey \_ decodercomplexityprofile](mfpkey-decodercomplexityprofileproperty.md)                     |
| g \_ wszwmvcdecodercomplexityangefordert  | [mfpkey \_ decodercomplexityangefordert](mfpkey-decodercomplexityrequestedproperty.md)                 |
| g \_ wszwmvcdecoderdeinterlacing        | [mfpkey- \_ Decoder \_ Deinterlacing](mfpkey-decoder-deinterlacingproperty.md)                          |
| g \_ wszwmvcdenoise-Option               | [mfpkey \_ Denoise-Option](mfpkey-denoiseoptionproperty.md)                                           |
| g \_ wszwmvcendofpass                   | [mfpkey \_ endofpass](mfpkey-endofpassproperty.md)                                                   |
| g \_ wszwmvcforceframeheight            | [mfpkey \_ forceframeheight](mfpkey-forceframeheightproperty.md)                                     |
| g \_ wszwmvcforceframewidth             | [mfpkey \_ forceframewidth](mfpkey-forceframewidthproperty.md)                                       |
| g \_ wszwmvcforcemediansetting          | [mfpkey \_ forcemediansetting](mfpkey-forcemediansettingproperty.md)                                 |
| g \_ wszwmvcfourcc                      | [mfpkey \_ FourCC](mfpkey-fourccproperty.md)                                                         |
| g \_ wszwmvcinterlacedcodingenabled     | [mfpkey \_ interlacedcodingenabled](mfpkey-interlacedcodingenabledproperty.md)                       |
| g \_ wszwmvclookahead                   | [mfpkey- \_ Lookahead](mfpkey-lookaheadproperty.md)                                                   |
| g \_ wszwmvcloopfilter                  | [mfpkey- \_ loopfilter](mfpkey-loopfilterproperty.md)                                                 |
| g \_ wszwmvcmacroblockmodecostmethod    | [mfpkey \_ makroblockmodecostmethod](mfpkey-macroblockmodecostmethodproperty.md)                     |
| g \_ wszwmvcmaxbitrate                  | [mfpkey- \_ Rmax](mfpkey-rmaxproperty.md)                                                             |
| g \_ wszwmvcmutionmatchmethod           | [mfpkey- \_ Methode "mutionmatchmethod"](mfpkey-motionmatchmethodproperty.md)                                   |
| g \_ wszwmvcmutionsearchlevel           | [mfpkey- \_ mutesearchlevel](mfpkey-motionsearchlevelproperty.md)                                   |
| g \_ wszwmvcmutionsearchrange           | [mfpkey-" \_ mutionsearchrange"](mfpkey-motionsearchrangeproperty.md)                                   |
| g \_ wszwmvcnoiseedgeremuval            | [mfpkey \_ noiseedgeremuval](mfpkey-noiseedgeremovalproperty.md)                                     |
| g \_ wszwmvcnumthreads                  | [mfpkey- \_ numThreads](mfpkey-numthreadsproperty.md)                                                 |
| g \_ wszwmvcpassesempfohlen           | [mfpkey- \_ passesempfohlen](mfpkey-passesrecommendedproperty.md)                                   |
| g \_ wszwmvcpassesused                  | [mfpkey- \_ passesused](mfpkey-passesusedproperty.md)                                                 |
| g \_ wszwmvcperperaloptlevel          | [mfpkey- \_ peraloptlevel](mfpkey-perceptualoptlevelproperty.md)                                 |
| g \_ wszwmvcproducedummyframes          | [mfpkey \_ producedummyframes](mfpkey-producedummyframesproperty.md)                                 |
| g \_ wszwmvcrangeredux                  | [mfpkey \_ rangeredux](mfpkey-rangereduxproperty.md)                                                 |
| g \_ wszwmvctotalframes                 | [mfpkey- \_ totalFrames](mfpkey-totalframesproperty.md)                                               |
| g \_ wszwmvcvbrenabled                  | [mfpkey \_ vbrenabled](mfpkey-vbrenabledproperty.md)                                                 |
| g \_ wszwmvcvbrquality                  | [mfpkey \_ vbrquality](mfpkey-vbrqualityproperty.md)                                                 |
| g \_ wszwmvcvideosc.                | [mfpkey- \_ videoup](mfpkey-videoscalingproperty.md)                                             |
| g \_ wszwmvcvtype                       | [mfpkey- \_ VType](mfpkey-vtypeproperty.md)                                                           |
| g \_ wszwmvczerobyteframes              | [mfpkey- \_ zerobyteframes](mfpkey-zerobyteframesproperty.md)                                         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Media-Codecs](windows-media-codecs.md)
</dt> </dl>

 

 



