---
description: Codec-API-Eigenschaften
ms.assetid: 5d527af7-07cf-42e2-99bb-d56c856cc1bc
title: Codec-API-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91346b6595944b8e95da5e9e43023052119e49a8b88809fce08b6fca780beba1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792910"
---
# <a name="codec-api-properties"></a>Codec-API-Eigenschaften

-   [Allgemeine Audioeigenschaften](#common-audio-properties)
-   [Allgemeine Decodereigenschaften](#common-decoder-properties)
-   [Allgemeine Encodereigenschaften](#common-encoder-properties)
-   [Eigenschaften des Videodecoders](#video-decoder-properties)
-   [Eigenschaften des Audiodecoders](#audio-decoder-properties)
-   [Video Encoder-Eigenschaften](#video-encoder-properties)
-   [Eigenschaften des Audioencoders](#audio-encoder-properties)
-   [MPEG Video Encoder-Eigenschaften](#mpeg-video-encoder-properties)
-   [MPEG Audio Encoder Properties](#mpeg-audio-encoder-properties)
-   [Dolby Digital Audio Decoder Properties](#dolby-digital-audio-decoder-properties)
-   [Dolby Digital Audio Encoder Properties](#dolby-digital-audio-encoder-properties)
-   [DSP-Eigenschaften (Digital Signal Processing)](#digital-signal-processing-dsp-properties)

### <a name="common-audio-properties"></a>Allgemeine Audioeigenschaften

Diese Eigenschaften gelten sowohl für Audioencoder als auch für Audiodecoder.



| Eigenschaft                                                      | Beschreibung                                                                    |
|---------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**AVAudioChannelConfig**](avaudiochannelconfig-property.md) | Ruft die Sprecherkonfiguration für die Audiokanäle im Audiobitstream ab. |
| [**AVAudioChannelCount**](avaudiochannelcount-property.md)   | Ruft die Anzahl der Kanäle im Audiobitstream ab.                           |
| [**AVAudioSampleRate**](avaudiosamplerate-property.md)       | Ruft die Abtastrate des Audiobitstreams in Stichproben pro Sekunde ab.          |
| [**AVDDSurroundMode**](avddsurroundmode-property.md)         | Gibt an, ob die Audiodaten in Dolby Surround codiert sind.                      |



 

### <a name="common-decoder-properties"></a>Allgemeine Decodereigenschaften

Diese Eigenschaften gelten sowohl für Audiodecoder als auch für Videodecoder.



| Eigenschaft                                                            | Beschreibung                                                                             |
|---------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**AVDecCommonInputFormat**](avdeccommoninputformat-property.md)   | Gibt das aktuelle Eingabeformat für den Decoder an.                                     |
| [**AVDecCommonMeanBitRate**](avdeccommonmeanbitrate.md)            | Ruft die aktuelle mittlere Bitrate des Decoders ab.                                          |
| [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) | Gibt das Ausgabeformat für den Decoder an.                                            |
| [**AVDecMmcssClass**](avdecmmcss-property.md)                      | Gibt die MMCSS-Klasse (Multimedia Class Scheduler Service) für den Decodierungsthread an. |



 

### <a name="common-encoder-properties"></a>Allgemeine Encodereigenschaften

Diese Eigenschaften gelten sowohl für Audioencoder als auch für Videoencoder.



| Eigenschaft                                                                          | Beschreibung                                                                                                     |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**AVEncCodecType**](avenccodectype-property.md)                                 | Gibt das Codierungsschema an.                                                                                  |
| [**AVEncCommonBufferInLevel**](avenccommonbufferinlevel-property.md)             | Gibt die Anfangsebene des Codierungspuffers an.                                                             |
| [**AVEncCommonBufferOutLevel**](avenccommonbufferoutlevel-property.md)           | Gibt die endgültige Ebene des Codierungspuffers am Ende des Codierungsprozesses an.                            |
| [**AVEncCommonBufferSize**](avenccommonbuffersize-property.md)                   | Gibt die Größe des Puffers an, der während der Codierung verwendet wird.                                                          |
| [**AVEncCommonFormatConstraint**](avenccommonformatconstraint-property.md)       | Gibt das Zielformat für einen Encoder an.                                                                     |
| [**AVEncCommonLowLatency**](avenccommonlowlatency-property.md)                   | Gibt an, ob der Ausgabestream so strukturiert werden soll, dass der codierte Stream eine niedrige Decodierungslatenz aufweist. |
| [**AVEncCommonMaxBitRate**](avenccommonmaxbitrate-property.md)                   | Gibt die maximale Bitrate an.                                                                                 |
| [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md)                 | Gibt die durchschnittliche Bitrate an.                                                                                 |
| [**AVEncCommonMeanBitRateInterval**](avenccommonmeanbitrateinterval-property.md) | Gibt das Zeitintervall an, für das die durchschnittliche Bitrate gilt.                                            |
| [**AVEncCommonMinBitRate**](avenccommonminbitrate-property.md)                   | Gibt die minimale Bitrate an.                                                                                 |
| [**AVEncCommonMultipassMode**](avenccommonmultipassmode-property.md)             | Gibt die Anzahl von Codierungsdurchläufen an, die der Encoder unterstützt.                                              |
| [**AVEncCommonPassEnd**](avenccommonpassend-property.md)                         | Beendet den aktuellen Codierungsdurchlauf oder fragt ab, ob der aktuelle Codierungsdurchlauf der letzte ist.                  |
| [**AVEncCommonPassStart**](avenccommonpassstart-property.md)                     | Startet den ersten Codierungsdurchlauf.                                                                                 |
| [**AVEncCommonQuality**](avenccommonquality-property.md)                         | Gibt die Qualitätsstufe für die Codierung an.                                                                       |
| [**AVEncCommonQualityVsSpeed**](avenccommonqualityvsspeed-property.md)           | Gibt den Kompromiss zwischen Codierungsqualität und Geschwindigkeit an.                                                      |
| [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md)         | Gibt den Ratensteuerungsmodus an.                                                                                |
| [**AVEncCommonRealTime**](avenccommonrealtime-property.md)                       | Gibt an, ob die Anwendung eine Echtzeitcodierungsleistung erfordert.                                      |
| [**AVEncCommonStreamEndHandling**](avenccommonstreamendhandling-property.md)     | Gibt an, ob der Encoder teilgruppen von Bildern (GOPs) am Ende des Streams verwirft.              |
| [**AVEncMuxOutputStreamType**](avencmuxoutputstreamtype.md)                      | Gibt den Typ des Ausgabestreams an, der von einem Multiplexer erzeugt wird.                                                  |
| [**AVEncStatCommonCompletedPasses**](avencstatcommoncompletedpasses-property.md) | Gibt die Anzahl abgeschlossener Codierungsdurchläufe an.                                                              |



 

### <a name="video-decoder-properties"></a>Eigenschaften des Videodecoders



| Eigenschaft                                                                                | Beschreibung                                                                     |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**AVDecVideoAcceleration \_ H264**](avdecvideoacceleration-h264-property.md)            | Aktiviert oder deaktiviert die Hardwarebeschleunigung für die H.264-Videodecodierung.             |
| [**AVDecVideoAcceleration \_ MPEG2**](avdecvideoacceleration-mpeg2-property.md)          | Aktiviert oder deaktiviert die Hardwarebeschleunigung für die MPEG-2-Videodecodierung.            |
| [**AVDecVideoAcceleration \_ VC1**](avdecvideoacceleration-vc1-property.md)              | Aktiviert oder deaktiviert die Hardwarebeschleunigung für die VC-1-Videodecodierung.              |
| [**AVDecVideoDropPicWithMissingRef**](avdecvideodroppicwithmissingref-property.md)     | Gibt an, ob der Decoder intraframes mit fehlenden Verweisframes löscht. |
| [**AVDecVideoFastDecodeMode**](avdecvideofastdecodemode.md)                            | Ruft die Geschwindigkeit der Videodecodierung ab oder legt sie fest.                                          |
| [**AVDecVideoImageSize**](avdecvideoimagesize.md)                                      | Ruft die Größe des decodierten Bilds in Pixel ab.                                  |
| [**AVDecVideoInputScanType**](avdecvideoinputscantype-property.md)                     | Gibt an, wie der decodierte Videostream übersprungen wird.                           |
| [**AVDecVideoPixelAspectRatio**](avdecvideopixelaspectratio-property.md)               | Gibt das Pixel-Seitenverhältnis des decodierten Videostreams an.                   |
| [**AVDecVideoSoftwareDeinterlaceMode**](avdecvideosoftwaredeinterlacemode-property.md) | Gibt den Softwaredeinterlacemodus des Decoders an.                              |
| [**AVDecVideoSWPowerLevel**](avdecvideoswpowerlevel-property.md)                       | Gibt die Energiesparstufe an.                                               |
| [**AVDecVideoThumbnailGenerationMode**](avdecvideothumbnailgenerationmode-property.md) | Aktiviert oder deaktiviert den Miniaturansichtsgenerierungsmodus.                                  |



 

### <a name="audio-decoder-properties"></a>Eigenschaften des Audiodecoders



| Eigenschaft                                                                        | Beschreibung                                                                                                            |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**AVDecAACDownmixMode**](avdecaacdownmixmode-property.md)                     | Gibt an, ob ein AAC-Decoder standardmäßige MPEG-2/MPEG-4-Stereo-Downmix-Gleichungen oder einen nicht standardmäßigen Downmix verwendet. |
| [**AVDecAudioDualMono**](avdecaudiodualmono-property.md)                       | Gibt an, ob 2-Kanal-Audio als Stereo oder Dual Mono codiert wird.                                                   |
| [**AVDecAudioDualMonoReproMode**](avdecaudiodualmonorepromode-property.md)     | Gibt an, wie der Decoder duale Mono-Audiodaten reproduziert.                                                                  |
| [**AVDecHEAACDynamicRangeControl**](avdecheaacdynamicrangecontrol-property.md) | Aktiviert oder deaktiviert die dynamische Bereichssteuerung in einem AAC-Decoder.                                                           |



 

### <a name="video-encoder-properties"></a>VideoEncoder-Eigenschaften



| Eigenschaft                                                                                        | Beschreibung                                                                                                           |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**AVEncInputVideoSystem**](avencinputvideosystem-property.md)                                 | Gibt das Videosystem des Quellinhalts an.                                                                     |
| [**AVEncStatVideoCodedFrames**](avencstatvideocodedframes-property.md)                         | Gibt die Anzahl der codierten Videoframes zurück.                                                                 |
| [**AVEncStatVideoOutputFrameRate**](avencstatvideooutputframerate-property.md)                 | Gibt die durchschnittliche Bildfrequenz des Videoinhalts zurück.                                                                  |
| [**AVEncStatVideoTotalFrames**](avencstatvideototalframes-property.md)                         | Gibt die Anzahl der Videoframes zurück, die der Encoder empfangen hat.                                                         |
| [**AVEncVideoCBRMotionMotionMotionoff**](avencvideocbrmotiontradeoff-property.md)                     | Gibt den Kompromiss zwischen Bewegungs- und Stillbild an.                                                               |
| [**AVEncVideoCodedVideoAccessUnitSize**](avencvideocodedvideoaccessunitsize-property.md)       | Gibt die Größe der Videozugriffseinheiten an.                                                                         |
| [**AVEncVideoDefaultUpperFieldDominant**](avencvideodefaultupperfielddominant-property.md)     | Gibt an, welches Feld zuerst angezeigt wird.                                                                             |
| [**AVEncVideoDisplayDimension**](avencvideodisplaydimension-property.md)                       | Gibt die Größe des Videostreams an, wenn er decodiert wird.                                                            |
| [**AVEncVideoEncodeDimension**](avencvideoencodedimension-property.md)                         | Gibt die Breite und Höhe des codierten Videos an, wenn das Video zugeschnitten wird.                                         |
| [**AVEncVideoEncodeOffsetOrigin**](avencvideoencodeoffsetorigin-property.md)                   | Gibt die linke und obere Ecke des Clippingrechtecks an, wenn das Video zugeschnitten wird.                                |
| [**AVEncVideoFieldSwap**](avencvideofieldswap-property.md)                                     | Kehrt die Reihenfolge der Verschachtelungsfelder im Quellvideo um.                                                      |
| [**AVEncVideoForceSourceScanType**](avencvideoforcesourcescantype-property.md)                 | Gibt an, ob die Eingabeframes progressiv oder interlaced sind.                                                     |
| [**AVEncVideoHeaderDropFrame**](avencvideoheaderdropframe-property.md)                         | Gibt den Wert des Dropframeflags im GOP-Header an.                                                             |
| [**AVEncVideoHeaderFrames**](avencvideoheaderframes-property.md)                               | Gibt die Startrahmennummer im GOP-Header an.                                                                |
| [**AVEncVideoHeaderHours**](avencvideoheaderhours-property.md)                                 | Gibt die Startstundennummer im GOP-Header an.                                                                 |
| [**AVEncVideoHeaderMinutes**](avencvideoheaderminutes-property.md)                             | Gibt die Nummer der Anfangsminute im GOP-Header an.                                                               |
| [**AVEncVideoHeaderSeconds**](avencvideoheaderseconds-property.md)                             | Gibt die starte zweite Zahl im GOP-Header an.                                                               |
| [**AVEncVideoInputChromaResolution**](avencvideoinputchromaresolution-property.md)             | Gibt die Auflösung des Eingangsvideos an.                                                                   |
| [**AVEncVideoInputChromaSubsampling**](avencvideoinputchromasubsampling-property.md)           | Gibt die Ziernung für das Eingabevideo an.                                                                      |
| [**AVEncVideoInputColorLighting**](avencvideoinputcolorlighting-property.md)                   | Gibt die beabsichtigten Beleuchtungsbedingungen für die Anzeige des Eingabevideos an.                                               |
| [**AVEncVideoInputColorNominalRange**](avencvideoinputcolornominalrange-property.md)           | Gibt den nominalen Bereich für das Eingabevideo an.                                                                      |
| [**AVEncVideoInputColorPrimaries**](avencvideoinputcolorprimaries-property.md)                 | Gibt die Farbprimitäten für das Eingabevideo an.                                                                    |
| [**AVEncVideoInputColorTransferFunction**](avencvideoinputcolortransferfunction-property.md)   | Gibt die Konvertierungsfunktion von RGB in R'G'B' für Eingabevideos an                                                  |
| [**AVEncVideoInputColorTransferMatrix**](avencvideoinputcolortransfermatrix-property.md)       | Gibt die Konvertierungsmatrix vom Farbraum Y'Cb'Cr' in den Farbraum R'G'B' für das Eingabevideo an.         |
| [**AVEncVideoInverseTelecineEnable**](avencvideoinversetelecineenable-property.md)             | Gibt an, ob der Encoder inverse Telecine ausführt.                                                              |
| [**AVEncVideoInverseTelecineThreshold**](avencvideoinversetelecinethreshold-property.md)       | Legt den Schwellenwert fest, bei dem der Encoder ein Videofeld redundant betrachtet.                                            |
| [**AVEncVideoMaxKeyframeDistance**](avencvideomaxkeyframedistance-property.md)                 | Gibt die maximale Anzahl von Frames zwischen Keyframes an.                                                            |
| [**AVEncVideoNoOfFieldsToEncode**](avencvideonooffieldstoencode-property.md)                   | Gibt die Anzahl der zu codierenden Felder an.                                                                             |
| [**AVEncVideoNoOfFieldsToSkip**](avencvideonooffieldstoskip-property.md)                       | Gibt die Anzahl der Felder an, die während der Codierung übersprungen werden.                                                               |
| [**AVEncVideoOutputChromaResolution**](avencvideooutputchromaresolution-property.md)           | Gibt die Auflösung des codierten Videos an.                                                                 |
| [**AVEncVideoOutputChromaSubsampling**](avencvideooutputchromasubsampling-property.md)         | Gibt die Ziernung für das codierte Video an.                                                                    |
| [**AVEncVideoOutputColorLighting**](avencvideooutputcolorlighting-property.md)                 | Gibt die beabsichtigten Beleuchtungsbedingungen zum Anzeigen des codierten Videos an.                                             |
| [**AVEncVideoOutputColorNominalRange**](avencvideooutputcolornominalrange-property.md)         | Gibt den nominalen Bereich für das codierte Video an.                                                                    |
| [**AVEncVideoOutputColorPrimaries**](avencvideooutputcolorprimaries-property.md)               | Gibt die Farbprimitäten für das codierte Video an.                                                                  |
| [**AVEncVideoOutputColorTransferFunction**](avencvideooutputcolortransferfunction-property.md) | Gibt die Konvertierungsfunktion von RGB in R'G'B' für codiertes Video an.                                               |
| [**AVEncVideoOutputColorTransferMatrix**](avencvideooutputcolortransfermatrix-property.md)     | Gibt die Konvertierungsmatrix vom Farbraum Y'Cb'Cr' in den Farbraum R'G'B' für das codierte Video an.       |
| [**AVEncVideoOutputFrameRate**](avencvideooutputframerate-property.md)                         | Gibt die Bildfrequenz im Ausgabestream des Encoders in Frames pro Sekunde an.                                        |
| [**AVEncVideoOutputFrameRateConversion**](avencvideooutputframerateconversion-property.md)     | Gibt an, ob der Encoder die Bildfrequenz konvertiert, wenn die Ausgabebildrate nicht mit der Eingabebildrate übereinstimmen soll. |
| [**AVEncVideoOutputScanType**](avencvideooutputscantype-property.md)                           | Gibt an, wie der Encoder das Ausgabevideo übergibt.                                                                |
| [**AVEncVideoPixelAspectRatio**](avencvideopixelaspectratio-property.md)                       | Gibt das Pixelseitenverhältnis an.                                                                                     |
| [**AVEncVideoSourceInhalt**](avencvideosourcefilmcontent-property.md)                     | Gibt an, ob die ursprüngliche Quelle des Eingabevideos Film oder Video war.                                           |
| [**AVEncVideoSourceIsBW**](avencvideosourceisbw-property.md)                                   | Gibt an, ob das Video monocolore (schwarz und weiß) ist oder Farbe enthält.                                        |



 

### <a name="audio-encoder-properties"></a>Eigenschaften des Audioencoders



| Eigenschaft                                                                        | Beschreibung                                                                         |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**AVEncAudioDualMono**](avencaudiodualmono-property.md)                       | Gibt an, ob 2-Kanal-Audio als Stereo oder Dual Mono codiert wird.                |
| [**AVEncAudioInputContent**](avencaudioinputcontent-property.md)               | Gibt an, ob der Audioinhalt Musik oder Stimme enthält.                        |
| [**AVEncAudioIntervalToEncode**](avencaudiointervaltoencode-property.md)       | Gibt die Anzahl der zu codierenden Audiobeispiele an.                                    |
| [**AVEncAudioIntervalToSkip**](avencaudiointervaltoskip-property.md)           | Gibt die Anzahl der Audiobeispiele an, die der Encoder überspringen soll.                      |
| [**AVEncAudioMapDestChannel N**](avencaudiomapdestchanneln-property.md)        | Gibt an, welcher Audiokanal dem Kanal *N* im codierten Audiostream zugeordnet wird. |
| [**AVEncAudioMeanBitRate**](avencaudiomeanbitrate.md)                          | Gibt die durchschnittliche Bitrate des codierten Audiostreams an.                         |
| [**AVEncStatAudioAverageBPS**](avencstataudioaveragebps-property.md)           | Gibt die durchschnittlichen Bits pro Sekunde des codierten Audios zurück.                           |
| [**AVEncStatAudioAveragePCMValue**](avencstataudioaveragepcmvalue-property.md) | Gibt die durchschnittliche Lautstärkestufe des Audioinhalts zurück.                              |
| [**AVEncStatAudioPeakPCMValue**](avencstataudiopeakpcmvalue-property.md)       | Gibt die höchste Volumeebene zurück, die im Audioinhalt vorhanden war.             |



 

### <a name="mpeg-video-encoder-properties"></a>MPEG Video Encoder-Eigenschaften



| Eigenschaft                                                                                    | Beschreibung                                                                          |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**AVEncMPVAddSeqEndCode**](avencmpvaddseqendcode-property.md)                             | Gibt an, ob der Encoder einen Sequenzendcode am Ende des Streams hinzufügt.     |
| [**AVEncMPVDefaultBPictureCount**](avencmpvdefaultbpicturecount-property.md)               | Gibt die Standardanzahl aufeinanderfolgender B-Frames zwischen I- und P-Frames an.         |
| [**AVEncMPVFrameFieldMode**](avencmpvframefieldmode-property.md)                           | Gibt an, ob der Encoder codierte Felder oder codierte Frames erzeugt.             |
| [**AVEncMPVGenerateHeaderPicDispExt**](avencmpvgenerateheaderpicdispext-property.md)       | Gibt an, ob der Encoder Bildanzeigeerweiterungsheader generiert.           |
| [**AVEncMPVGenerateHeaderPicExt**](avencmpvgenerateheaderpicext-property.md)               | Gibt an, ob der Encoder Bilderweiterungsheader generiert.                   |
| [**AVEncMPVGenerateHeaderSeqDispExt**](avencmpvgenerateheaderseqdispext-property.md)       | Gibt an, ob der Encoder Erweiterungsheader für die Sequenzanzeige generiert.          |
| [**AVEncMPVGenerateHeaderSeqExt**](avencmpvgenerateheaderseqext-property.md)               | Gibt an, ob der Encoder Sequenzerweiterungsheader generiert.                  |
| [**AVEncMPVGenerateHeaderSeqScaleExt**](avencmpvgenerateheaderseqscaleext-property.md)     | Gibt an, ob der Encoder sequenzskalierbare Erweiterungsheader generiert.         |
| [**AVEncMPVGOPOpOpen**](avencmpvgopopen-property.md)                                         | Gibt an, ob der Encoder offene ODER geschlossene GOPs erzeugt.                     |
| [**AVEncMPVGOPSInSeq**](avencmpvgopsinseq-property.md)                                     | Gibt die Anzahl der GOPs zwischen Sequenzheadern an.                               |
| [**AVEncMPVGOPSize**](avencmpvgopsize-property.md)                                         | Gibt die maximale Anzahl von Bildern von einem GOP-Header zum nächsten GOP-Header an. |
| [**AVEncMPVIntraDCPrecision**](avencmpvintradcprecision-property.md)                       | Gibt die Genauigkeit der DC-Koeffizienten an.                                      |
| [**AVEncMPVIntraVLCTable**](avencmpvintravlctable-property.md)                             | Gibt an, welche VLC-Tabelle (Variable Length Coding) für die Codierung der Entropie verwendet werden soll.        |
| [**AVEncMPVLevel**](avencmpvlevel-property.md)                                             | Gibt die MPEG-2-Ebene an.                                                          |
| [**AVEncMPVProfile**](avencmpvprofile-property.md)                                         | Gibt das MPEG-2-Profil an.                                                        |
| [**AVEncMPVQScaleType**](avencmpvqscaletype-property.md)                                   | Gibt an, ob die Quantizerskala linear oder nicht linear ist.                       |
| [**AVEncMPVQuantMatrixColoraIntra**](avencmpvquantmatrixchromaintra-property.md)           | Gibt die Matrix der Generatorquantisierung für makroblockinterne Blöcke an.                      |
| [**AVEncMPVQuantMatrixColoraNonIntra**](avencmpvquantmatrixchromanonintra-property.md)     | Gibt die Quantifizierungsmatrix für nicht-interne Makroblocks an.                  |
| [**AVEncMPVQuantMatrixIntra**](avencmpvquantmatrixintra-property.md)                       | Gibt die Luma-Quantisierungsmatrix für makroblockinterne Blöcke an.                        |
| [**AVEncMPVQuantMatrixNonIntra**](avencmpvquantmatrixnonintra-property.md)                 | Gibt die Luma-Quantisierungsmatrix für nicht-interne Makroblocks an.                    |
| [**AVEncMPVScanPattern**](avencmpvscanpattern-property.md)                                 | Gibt das Makroblock-Scanmuster an.                                               |
| [**AVEncMPVSceneDetection**](avencmpvscenedetection-property.md)                           | Gibt an, wie sich der Encoder verhält, wenn er eine neue Szene erkennt.                       |
| [**AVEncMPVUseConcealmentMotionVectors**](avencmpvuseconcealmentmotionvectors-property.md) | Gibt an, ob der Encoder Verschleierungsbewegungsvektoren verwendet.                       |



 

### <a name="mpeg-audio-encoder-properties"></a>MPEG Audio Encoder Properties



| Eigenschaft                                                                                  | Beschreibung                                                                   |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**AVEncMPACodingMode**](avencmpacodingmode-property.md)                                 | Gibt den MPEG-1-Audiocodierungsmodus an.                                     |
| [**AVEncMPACopyright**](avencmpacopyright-property.md)                                   | Gibt die Standardeinstellung für das Copyrightbit an.                          |
| [**AVEncMPAEmphasisType**](avencmpaemphasistype-property.md)                             | Gibt den Typ des Filters zum Deaktivieren der Hervorhebung an, der beim Decodieren verwendet werden soll.   |
| [**AVEncMPAEnableRedundancyProtection**](avencmpaenableredundancyprotection-property.md) | Gibt an, ob dem Frameheader eine zyklische Redundanzprüfung (CRC) hinzugefügt werden soll. |
| [**AVEncMPALayer**](avencmpalayer-property.md)                                           | Gibt die MPEG-Audioebene an.                                               |
| [**AVEncMPAOriginalBitstream**](avencmpaoriginalbitstream-property.md)                   | Gibt die Standardeinstellung für das ursprüngliche Bit an.                           |
| [**AVEncMPAPrivateUserBit**](avencmpaprivateuserbit-property.md)                         | Legt den Wert des Bits des privaten Benutzers fest.                                       |



 

### <a name="dolby-digital-audio-decoder-properties"></a>Dolby Digital Audio Decoder Properties



| Eigenschaft                                                                      | Beschreibung                                                                    |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**AVDecDDDynamicRangeScaleHigh**](avdecdddynamicrangescalehigh-property.md) | Gibt den übergeordneten Cut an, wenn der Decoder ein Dynamisches Bereichssteuerelement ausführt.  |
| [**AVDecDDDynamicRangeScaleLow**](avdecdddynamicrangescalelow-property.md)   | Gibt die Verstärkung auf niedriger Ebene an, wenn der Decoder die Steuerung des dynamischen Bereichs ausführt. |
| [**AVDecDDOperationalMode**](avdecddoperationalmode-property.md)             | Gibt den Komprimierungssteuerungsmodus an.                                        |



 

### <a name="dolby-digital-audio-encoder-properties"></a>Dolby Digital Audio Encoder–Eigenschaften



| Eigenschaft                                                                                        | Beschreibung                                                                               |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**AVEncDDAtoDConverterType**](avencddatodconvertertype-property.md)                           | Gibt den Typ der Analog-Digital-Konvertierung (A/D) an.                                 |
| [**AVEncDDCentreDownMixLevel**](avencddcentredownmixlevel-property.md)                         | Gibt die zentrierte Downmixebene an.                                                       |
| [**AVEncDDChannelBWLowPassFilter**](avencddchannelbwlowpassfilter-property.md)                 | Gibt an, ob ein Low-Pass-Filter auf die Haupteingabekanäle angewendet wird.                |
| [**AVEncDDCopyright**](avencddcopyright-property.md)                                           | Gibt das Copyrightflag an.                                                             |
| [**AVEncDDDCHighPassFilter**](avencdddchighpassfilter-property.md)                             | Gibt an, ob ein DC-blockierende Filter mit hohem Durchgang angewendet wird.                              |
| [**AVEncDDDialogNormalization**](avencdddialognormalization-property.md)                       | Gibt die Dialognormalisierungsebene an.                                                 |
| [**AVEncDDDigitalDeemphasis**](avencdddigitaldeemphasis-property.md)                           | Gibt an, ob die digitale De-Hervorhebung vorgibt.                                                    |
| [**AVEncDDDynamicRangeCompressionControl**](avencdddynamicrangecompressioncontrol-property.md) | Gibt das Dynamische Bereichssteuerungsprofil an.                                              |
| [**AVEncDDHeadphoneMode**](avencddheadphonemode-property.md)                                   | Gibt den Ziermodus an.                                                             |
| [**AVEncDDLFELowPassFilter**](avencddlfelowpassfilter-property.md)                             | Gibt an, ob ein Low-Pass-Filter auf den LFE-Kanal (Low Frequency Effect) angewendet wird. |
| [**AVEncDDLoRoCenterMixLvl \_ x10**](avencddlorocentermixlvl-x10-property.md)                    | Gibt die Pegelverschiebung an, die für das Lo/Ro-Downmixing auf den Mittelkanal angewendet wird.     |
| [**AVEncDDLoRoSurroundMixLvl \_ x10**](avencddlorosurroundmixlvl-x10-property.md)                | Gibt die Pegelverschiebung an, die auf die Umschließkanäle für Lo/Ro-Downmixing angewendet wird.  |
| [**AVEncDDLtRtCenterMixLvl \_ x10**](avencddltrtcentermixlvl-x10-property.md)                    | Gibt die Pegelverschiebung an, die für lt/rt-Downmixing auf den Mittelkanal angewendet wird.     |
| [**AVEncDDLtRtSurroundMixLvl \_ x10**](avencddltrtsurroundmixlvl-x10-property.md)                | Gibt die Pegelverschiebung an, die auf die Umschließkanäle für lt/rt-Downmixing angewendet wird.  |
| [**AVEncDDOriginalBitstream**](avencddoriginalbitstream-property.md)                           | Gibt das ursprüngliche Bitstreamflag an.                                                    |
| [**AVEncDDPreferredStereoDownMixMode**](avencddpreferredstereodownmixmode-property.md)         | Gibt den bevorzugten Stereo-Downmixmodus an.                                              |
| [**AVEncDDProductionInfoExists**](avencddproductioninfoexists-property.md)                     | Gibt das Flag für Audioproduktionsinformationen an.                                          |
| [**AVEncDDProductionMixLevel**](avencddproductionmixlevel-property.md)                         | Gibt den Mischungsgrad an.                                                               |
| [**AVEncDDProductionRoomType**](avencddproductionroomtype-property.md)                         | Gibt den Raumtyp an.                                                                  |
| [**AVEncDDRFPreEmphasisFilter**](avencddrfpreemphasisfilter-property.md)                       | Gibt die Einstellung für den RF-Overmodulation-Schutz an.                                       |
| [**AVEncDDService**](avencddservice-property.md)                                               | Gibt den Audiodienst an.                                                              |
| [**AVEncDDSurround3dBAttenuation**](avencddsurround3dbattenuation-property.md)                 | Gibt an, ob die Umschließkanäle vor der Codierung abgedämpft werden.                   |
| [**AVEncDDSurround90DegreeePhaseShift**](avencddsurround90degreeephaseshift-property.md)       | Gibt an, ob eine Phasenverschiebung um 90 Grad auf die Umschließkanäle angewendet wird.            |
| [**AVEncDDSurroundDownMixLevel**](avencddsurrounddownmixlevel-property.md)                     | Gibt die Umschließen der Mischungsebene "Umschließen" an.                                                    |
| [**AVEncDDSurroundExMode**](avencddsurroundexmode-property.md)                                 | Gibt an, ob der Audiostream in Surround EX codiert ist.                             |



 

### <a name="digital-signal-processing-dsp-properties"></a>DSP-Eigenschaften (Digital Signal Processing)



| Eigenschaft                                                                | Beschreibung                               |
|-------------------------------------------------------------------------|-------------------------------------------|
| [**AVDSPCafdnessEqualization**](avdsploudnessequalization-property.md) | Aktiviert oder deaktiviert die Lautheitsgleichheit. |
| [**AVDSPSpeakerFill**](avdspspeakerfill-property.md)                   | Aktiviert oder deaktiviert die Sprecherfüllung.          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Codec-API-Referenz](codec-api-reference.md)
</dt> </dl>

 

 



