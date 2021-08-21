---
description: Codec-API-Enumerationen
ms.assetid: 5d6e48cb-d181-448e-a96e-e5ab500427d7
title: Codec-API-Enumerationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c28b82d73d6bd6fefed5f3c9296a666d1053cd71b074a782858b31e94dc3a3ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079330"
---
# <a name="codec-api-enumerations"></a>Codec-API-Enumerationen



| Enumeration                                                                              | Beschreibung                                                                                               |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**eAVAudioChannelConfig**](/windows/desktop/api/codecapi/ne-codecapi-eavaudiochannelconfig)                                   | Gibt die Sprecherkonfiguration für die Audiokanäle im Audiobitstream an.                       |
| [**eAVDDSurroundMode**](/windows/desktop/api/codecapi/ne-codecapi-eavddsurroundmode)                                           | Gibt an, ob die Audiodaten in Dolby Surround codiert sind.                                                 |
| [**eAVDecAACDownmixMode**](/windows/win32/api/codecapi/ne-codecapi-eavdecaacdownmixmode)                                     | Gibt an, ob ein AAC-Decoder standardmäßige MPEG-2/MPEG-4 Stereo-Downmixgleichungen verwendet.                    |
| [**eAVDecAudioDualMono**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmono)                                       | Gibt an, ob der Eingabeaudiostream Stereo oder Dual Mono ist.                                          |
| [**eAVDecAudioDualMonoReproMode**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmonorepromode)                     | Gibt an, wie der Decoder duale Mono-Audiodaten reproduziert.                                                     |
| [**eAVDecDDOperationalMode**](/windows/desktop/api/codecapi/ne-codecapi-eavdecddoperationalmode)                               | Gibt den Komprimierungssteuerungsmodus für einen Dolby AC-3-Audiostream an.                                     |
| [**eAVDecHEAACDynamicRangeControl**](/windows/desktop/api/codecapi/ne-codecapi-eavdecheaacdynamicrangecontrol)                 | Gibt an, ob ein AAC-Decoder ein Dynamisches Bereichssteuerelement ausführt.                                          |
| [**eAVDecVideoInputScanType**](/windows/win32/api/codecapi/ne-codecapi-eavdecvideoinputscantype)                             | Gibt an, wie der decodierte Videostream übersprungen wird.                                                     |
| [**eAVDecVideoSoftwareDeinterlaceMode**](/windows/desktop/api/codecapi/ne-codecapi-eavdecvideosoftwaredeinterlacemode)         | Gibt den Softwaredeinterlacemodus eines Videodecoders an.                                                    |
| [**eAVDecVideoSWPowerLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavdecvideoswpowerlevel)                               | Gibt die Energiesparstufe eines Videodecoders an.                                                      |
| [**eAVDSPLoudnessEqualization**](/windows/desktop/api/codecapi/ne-codecapi-eavdsploudnessequalization)                         | Gibt an, ob die Lautheitsgleichheit in einem Audiodecoder oder digitalen Signalprozessor (Digital Signal Processor, DSP) aktiviert ist. |
| [**eAVDSPSpeakerFill**](/windows/desktop/api/codecapi/ne-codecapi-eavdspspeakerfill)                                           | Gibt an, ob die Sprecherfüllung in einem Audiodecoder oder DSP aktiviert ist.                                     |
| [**eAVEncAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavencaudiodualmono)                                       | Gibt an, ob 2-Kanal-Audio als Stereo oder Dual Mono codiert wird.                                      |
| [**eAVEncAudioInputContent-Enumeration**](/windows/win32/api/codecapi/ne-codecapi-eavencaudioinputcontent)                   | Gibt an, ob der Audioinhalt Musik oder Stimme enthält.                                              |
| [**eAVEncCommonRateControlMode**](/windows/win32/api/codecapi/ne-codecapi-eavenccommonratecontrolmode)                       | Gibt den Ratensteuerungsmodus an.                                                                          |
| [**eAVEncCommonStreamEndHandling**](/windows/win32/api/codecapi/ne-codecapi-eavenccommonstreamendhandling)                   | Gibt an, ob der Encoder teilgruppen von Bildern (GOPs) am Ende des Streams verwirft.        |
| [**eAVEncDDAtoDConverterType**](/windows/win32/api/codecapi/ne-codecapi-eavencddatodconvertertype)                           | Gibt den Typ der Analog-digital-Konvertierung (A/D) für einen Dolby Digital-Audiostream an.                |
| [**eAVEncDDDynamicRangeCompressionControl**](/windows/win32/api/codecapi/ne-codecapi-eavencdddynamicrangecompressioncontrol) | Gibt das Dynamische Bereichssteuerungsprofil in einem Dolby Digital-Audiostream an.                              |
| [**eAVEncDDHeadphoneMode**](/windows/desktop/api/codecapi/ne-codecapi-eavencddheadphonemode)                                   | Gibt den Bereinigungsmodus für einen Dolby Digital-Audiostream an.                                                |
| [**eAVEncDDPreferredStereoDownMixMode**](/windows/desktop/api/codecapi/ne-codecapi-eavencddpreferredstereodownmixmode)         | Gibt den bevorzugten Stereo-Downmixmodus für einen Dolby Digital-Audiostream an.                             |
| [**eAVEncDDProductionRoomType**](/windows/win32/api/codecapi/ne-codecapi-eavencddproductionroomtype)                         | Gibt den Raumtyp für einen Dolby Digital-Audiostream an.                                                 |
| [**eAVEncDDService**](/windows/desktop/api/codecapi/ne-codecapi-eavencddservice)                                               | Gibt den Audiodienst an, der in einem Dolby Digital-Audiostream enthalten ist.                                    |
| [**eAVEncDDSurroundExMode**](/windows/desktop/api/codecapi/ne-codecapi-eavencddsurroundexmode)                                 | Gibt an, ob ein Dolby Digital-Audiostream in Dolby Digital Surround EX codiert ist.                   |
| [**eAVEncInputVideoSystem**](/windows/desktop/api/codecapi/ne-codecapi-eavencinputvideosystem)                                 | Gibt den nominalen Bereich für eine Videoquelle an.                                                           |
| [**eAVEncMPACodingMode**](/windows/desktop/api/codecapi/ne-codecapi-eavencmpacodingmode)                                       | Gibt den MPEG-Audiocodierungsmodus an.                                                                   |
| [**eAVEncMPAEmphasisType**](/windows/win32/api/codecapi/ne-codecapi-eavencmpaemphasistype)                                   | Gibt den Typ des Filters zum Deaktivieren der Hervorhebung an, der beim Decodieren verwendet werden soll.                               |
| [**eAVEncMPALayer**](/windows/win32/api/codecapi/ne-codecapi-eavencmpalayer)                                                 | Gibt die MPEG-Audioebene an.                                                                           |
| [**eAVEncMPVFrameFieldMode**](/windows/desktop/api/codecapi/ne-codecapi-eavencmpvframefieldmode)                               | Gibt an, ob der Encoder codierte Felder oder codierte Frames erzeugt.                                  |
| [**eAVEncMPVIntraVLCTable**](/windows/desktop/api/codecapi/ne-codecapi-eavencmpvintravlctable)                                 | Gibt an, welche VLC-Tabelle (Variable Length Coding) für die Codierung der Entropie verwendet werden soll.                             |
| [**eAVEncMPVLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavencmpvlevel)                                                 | Gibt das MPEG-2-Profil an.                                                                             |
| [**eAVEncMPVProfile**](/windows/win32/api/codecapi/ne-codecapi-eavencmpvprofile)                                             | Gibt das MPEG-2-Profil an.                                                                             |
| [**eAVEncMPVQScaleType**](/windows/desktop/api/codecapi/ne-codecapi-eavencmpvqscaletype)                                       | Gibt an, ob die Quantizerskala linear oder nicht linear ist.                                            |
| [**eAVEncMPVScanPattern**](/windows/win32/api/codecapi/ne-codecapi-eavencmpvscanpattern)                                     | Gibt das Makroblock-Scanmuster an.                                                                    |
| [**eAVEncMPVSceneDetection**](/windows/win32/api/codecapi/ne-codecapi-eavencmpvscenedetection)                               | Gibt an, wie sich der Encoder verhält, wenn er eine neue Szene erkennt.                                            |
| [**eAVEncMuxOutput**](/windows/win32/api/codecapi/ne-codecapi-eavencmuxoutput)                                               | Gibt den Typ des Ausgabestreams an, der von einem Multiplexer erzeugt wird.                                            |
| [**eAVEncVideoColoraResolution**](/windows/win32/api/codecapi/ne-codecapi-eavencvideochromaresolution)                       | Gibt die Auflösung von Lösern an.                                                                              |
| [**eAVEncVideoColoraSubsampling**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideochromasubsampling)                     | Gibt die Färbung an.                                                                                  |
| [**eAVEncVideoColorLighting**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideocolorlighting)                             | Gibt die beabsichtigten Beleuchtungsbedingungen zum Anzeigen einer Videoquelle an.                                    |
| [**eAVEncVideoColorNominalRange**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideocolornominalrange)                     | Gibt den nominalen Bereich für eine Videoquelle an.                                                           |
| [**eAVEncVideoColorPrimaries**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideocolorprimaries)                           | Gibt die Farbprimärdateien des Videos an.                                                               |
| [**eAVEncVideoColorTransferFunction**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideocolortransferfunction)             | Gibt die Konvertierungsfunktion von R'G'B' in RGB an.                                                     |
| [**eAVEncVideoColorTransferMatrix**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideocolortransfermatrix)                 | Gibt die Konvertierungsmatrix vom Farbraum Y'Cb'Cr' in den R'G'B'-Farbraum an.                  |
| [**eAVEncVideoLappenContent**](/windows/win32/api/codecapi/ne-codecapi-eavencvideofilmcontent)                                 | Gibt an, ob die ursprüngliche Quelle des Eingabevideos Film oder Video war.                               |
| [**eAVEncVideoOutputFrameRateConversion**](/windows/win32/api/codecapi/ne-codecapi-eavencvideooutputframerateconversion)     | Gibt an, ob der Encoder die Bildfrequenz konvertiert.                                                    |
| [**eAVEncVideoOutputScanType**](/windows/win32/api/codecapi/ne-codecapi-eavencvideooutputscantype)                           | Gibt an, wie der Encoder das Ausgabevideo übersprungen.                                                    |
| [**eAVEncVideoSourceScanType**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideosourcescantype)                           | Gibt an, ob die Eingabeframes für einen Encoder progressiv oder übersprungen sind.                          |
| [**eAVFastDecodeMode**](/windows/desktop/api/codecapi/ne-codecapi-eavfastdecodemode)                                           | Gibt die Geschwindigkeit der Videodecodierung an.                                                                       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Codec-API-Referenz](codec-api-reference.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 
