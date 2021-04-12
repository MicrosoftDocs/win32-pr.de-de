---
description: Eigenschaften der Codec-API
ms.assetid: 5d527af7-07cf-42e2-99bb-d56c856cc1bc
title: Eigenschaften der Codec-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06269591c8ddf087b83146ed72a62f4565b8340a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481187"
---
# <a name="codec-api-properties"></a>Eigenschaften der Codec-API

-   [Allgemeine Audioeigenschaften](#common-audio-properties)
-   [Allgemeine Decoder-Eigenschaften](#common-decoder-properties)
-   [Allgemeine Codierungs Eigenschaften](#common-encoder-properties)
-   [Video Decoder-Eigenschaften](#video-decoder-properties)
-   [Audiodecoder-Eigenschaften](#audio-decoder-properties)
-   [Video Encoder-Eigenschaften](#video-encoder-properties)
-   [Audioencodereigenschaften](#audio-encoder-properties)
-   [MPEG-Video Encoder-Eigenschaften](#mpeg-video-encoder-properties)
-   [MPEG-audiocodierungs Eigenschaften](#mpeg-audio-encoder-properties)
-   [Dolby Digital-Audiodecoder-Eigenschaften](#dolby-digital-audio-decoder-properties)
-   [Dolby Digital-audioencodereigenschaften](#dolby-digital-audio-encoder-properties)
-   [Eigenschaften der digitalen Signal Verarbeitung (DSP)](#digital-signal-processing-dsp-properties)

### <a name="common-audio-properties"></a>Allgemeine Audioeigenschaften

Diese Eigenschaften gelten für audiocodierern und Audiodecoder.



| Eigenschaft                                                      | BESCHREIBUNG                                                                    |
|---------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**Avaudiochannelconfig**](avaudiochannelconfig-property.md) | Ruft die sprecherkonfigurationskonfiguration für die Audiokanäle im audiobit-Stream ab. |
| [**Avaudiochannelcount**](avaudiochannelcount-property.md)   | Ruft die Anzahl der Kanäle im audiobit-Stream ab.                           |
| [**Avaudiosamplerate**](avaudiosamplerate-property.md)       | Ruft die Stichprobenrate des audiobit-Streams in Stichproben pro Sekunde ab.          |
| [**Avddsurroundmode**](avddsurroundmode-property.md)         | Gibt an, ob das Audioformat in Dolby Surround codiert ist.                      |



 

### <a name="common-decoder-properties"></a>Allgemeine Decoder-Eigenschaften

Diese Eigenschaften gelten sowohl für Audiodecoders als auch für Video Decoder.



| Eigenschaft                                                            | BESCHREIBUNG                                                                             |
|---------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**Avdeccommoninputformat**](avdeccommoninputformat-property.md)   | Gibt das aktuelle Eingabeformat für den Decoder an.                                     |
| [**Avdeccommonmeanbitrate**](avdeccommonmeanbitrate.md)            | Ruft die aktuelle Mean-Bitrate des Decoders ab.                                          |
| [**Avdeccommonoutputformat**](avdeccommonoutputformat-property.md) | Gibt das Ausgabeformat für den Decoder an.                                            |
| [**Avdecmmcssclass**](avdecmmcss-property.md)                      | Gibt die MMCSS-Klasse (Multimedia Class Scheduler Service) für den Decodierungs Thread an. |



 

### <a name="common-encoder-properties"></a>Allgemeine Codierungs Eigenschaften

Diese Eigenschaften gelten sowohl für Audioencoder als auch für Video Encoder.



| Eigenschaft                                                                          | BESCHREIBUNG                                                                                                     |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**Avenccodectype**](avenccodectype-property.md)                                 | Gibt das Codierungsschema an.                                                                                  |
| [**Avenccommonbufferinlevel**](avenccommonbufferinlevel-property.md)             | Gibt die Anfangs Ebene des Codierungs Puffers an.                                                             |
| [**Avenccommonbufferoutlevel**](avenccommonbufferoutlevel-property.md)           | Gibt die endgültige Ebene des Codierungs Puffers am Ende des Codierungs Vorgangs an.                            |
| [**Avenccommonbuffersize**](avenccommonbuffersize-property.md)                   | Gibt die Größe des Puffers an, der während der Codierung verwendet wird.                                                          |
| [**Avenccommonformateinschränkung**](avenccommonformatconstraint-property.md)       | Gibt das Zielformat für einen Encoder an.                                                                     |
| [**Avenccommonlowlatency**](avenccommonlowlatency-property.md)                   | Gibt an, ob der Ausgabestream so strukturiert werden soll, dass der codierte Stream eine geringe Decodierungs Latenz aufweist. |
| [**Avenccommonmaxbitrate**](avenccommonmaxbitrate-property.md)                   | Gibt die maximale Bitrate an.                                                                                 |
| [**Avenccommonmeanbitrate**](avenccommonmeanbitrate-property.md)                 | Gibt die durchschnittliche Bitrate an.                                                                                 |
| [**Avenccommonmeanbitrateingeterval**](avenccommonmeanbitrateinterval-property.md) | Gibt das Zeitintervall an, für das die durchschnittliche Bitrate gilt.                                            |
| [**Avenccommonminbitrate**](avenccommonminbitrate-property.md)                   | Gibt die minimale Bitrate an.                                                                                 |
| [**Avenccommonmultipassmode**](avenccommonmultipassmode-property.md)             | Gibt die Anzahl von Codierungs Durchläufen an, die der Encoder unterstützt.                                              |
| [**Avenccommonpassend**](avenccommonpassend-property.md)                         | Beendet den aktuellen Codierungs Durchlauf oder fragt ab, ob der aktuelle Codierungs Durchlauf der letzte ist.                  |
| [**Avenccommonpassstart**](avenccommonpassstart-property.md)                     | Startet den ersten Codierungs Durchlauf.                                                                                 |
| [**Avenccommonquality**](avenccommonquality-property.md)                         | Gibt die Qualitätsstufe für die Codierung an.                                                                       |
| [**Avenccommonqualityvsspeed**](avenccommonqualityvsspeed-property.md)           | Gibt den Kompromiss zwischen Codierungsqualität und Geschwindigkeit an.                                                      |
| [**Avenccommonratecontrolmode**](avenccommonratecontrolmode-property.md)         | Gibt den Raten Steuerungs Modus an.                                                                                |
| [**Avenccommonrealtime**](avenccommonrealtime-property.md)                       | Gibt an, ob die Anwendung die Echt Zeit Codierungs Leistung erfordert.                                      |
| [**Avenccommonstreamendbehandlung**](avenccommonstreamendhandling-property.md)     | Gibt an, ob der Encoder am Ende des Streams partielle Gruppen von Bildern (GOPs) verwirft.              |
| [**Avencmuxoutputstreamtype**](avencmuxoutputstreamtype.md)                      | Gibt den Typ des Ausgabestreams an, der von einem Multiplexer erzeugt wird.                                                  |
| [**Avencstatucommoncompletedpass**](avencstatcommoncompletedpasses-property.md) | Gibt die Anzahl der abgeschlossenen Codierungs Durchläufen an.                                                              |



 

### <a name="video-decoder-properties"></a>Video Decoder-Eigenschaften



| Eigenschaft                                                                                | BESCHREIBUNG                                                                     |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**Avdecvideoacceleration \_ H264**](avdecvideoacceleration-h264-property.md)            | Aktiviert oder deaktiviert die Hardwarebeschleunigung für die H. 264-Video Decodierung.             |
| [**Avdecvideoacceleration- \_ MPEG2**](avdecvideoacceleration-mpeg2-property.md)          | Aktiviert oder deaktiviert die Hardwarebeschleunigung für MPEG-2-Video Decodierung.            |
| [**Avdecvideoacceleration \_ VC1**](avdecvideoacceleration-vc1-property.md)              | Aktiviert oder deaktiviert die Hardwarebeschleunigung für das Decodieren von VC-1-Videos.              |
| [**Avdecvideodroppicwithmissingref**](avdecvideodroppicwithmissingref-property.md)     | Gibt an, ob der Decoder innerhalb von Frames mit fehlenden Verweis Rahmen löscht. |
| [**Avdecvideofastdecodemode**](avdecvideofastdecodemode.md)                            | Ruft die videodecodierungs Geschwindigkeit ab oder legt Sie fest                                          |
| [**Avdecvideoimagesize**](avdecvideoimagesize.md)                                      | Ruft die Größe des decodierten Bilds in Pixel ab.                                  |
| [**Avdecvideoinputscantype**](avdecvideoinputscantype-property.md)                     | Gibt an, wie der decodierte Videostream mit Zeilen Sprung verknüpft ist.                           |
| [**Avdecvideopixelaspectratio**](avdecvideopixelaspectratio-property.md)               | Gibt das Pixel Seitenverhältnis des decodierten Videostreams an.                   |
| [**Avdecvideosoftwaredeingeterlacemode**](avdecvideosoftwaredeinterlacemode-property.md) | Gibt den Software Deinterlacing-Modus des Decoders an.                              |
| [**Avdecvideoswpowerlevel**](avdecvideoswpowerlevel-property.md)                       | Gibt die Energiespar Stufe an.                                               |
| [**Avdecvideothumbnailgenerationmode**](avdecvideothumbnailgenerationmode-property.md) | Aktiviert oder deaktiviert den Miniatur Ansichts Generierungs Modus.                                  |



 

### <a name="audio-decoder-properties"></a>Audiodecoder-Eigenschaften



| Eigenschaft                                                                        | BESCHREIBUNG                                                                                                            |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**Avdecaacdownmixmode**](avdecaacdownmixmode-property.md)                     | Gibt an, ob ein AAC-Decoder standardmäßige MPEG-2/MPEG-4-Stereo Abmischungs Gleichungen verwendet oder eine nicht standardmäßige downmischungs-verwendet. |
| [**Avdecaudiodualmono**](avdecaudiodualmono-property.md)                       | Gibt an, ob die zwei-Kanal-Audiodaten als Stereo oder Dual Mono codiert werden.                                                   |
| [**Avdecaudiodualmonorepromode**](avdecaudiodualmonorepromode-property.md)     | Gibt an, wie der Decoder Dual Mono-Audiodaten wiederherstellt.                                                                  |
| [**Avabcheaacdynamicrangecontrol**](avdecheaacdynamicrangecontrol-property.md) | Aktiviert oder deaktiviert das dynamische Bereichs Steuerelement in einem AAC-Decoder.                                                           |



 

### <a name="video-encoder-properties"></a>Video Encoder-Eigenschaften



| Eigenschaft                                                                                        | BESCHREIBUNG                                                                                                           |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**Avencinputvideosystem**](avencinputvideosystem-property.md)                                 | Gibt das Videosystem des Quell Inhalts an.                                                                     |
| [**Avencstatus videocodedframes**](avencstatvideocodedframes-property.md)                         | Gibt die Anzahl der codierten Video Frames zurück.                                                                 |
| [**Avencstatus videooutputframerate**](avencstatvideooutputframerate-property.md)                 | Gibt die durchschnittliche Framerate des Video Inhalts zurück.                                                                  |
| [**Avencstatus videototalframes**](avencstatvideototalframes-property.md)                         | Gibt die Anzahl der Video Frames zurück, die der Encoder empfangen hat.                                                         |
| [**"Avencvideocbrmutiontradeoff"**](avencvideocbrmotiontradeoff-property.md)                     | Gibt den Kompromiss zwischen Bewegung und noch Bildern an.                                                               |
| [**Avencvideocodedvideoaccessunitsize**](avencvideocodedvideoaccessunitsize-property.md)       | Gibt die Größe der Video Zugriffs Einheiten an.                                                                         |
| [**Avencvideodefaultupperfielddominant**](avencvideodefaultupperfielddominant-property.md)     | Gibt an, welches Feld zuerst angezeigt wird.                                                                             |
| [**Avencvideodisplaydimension**](avencvideodisplaydimension-property.md)                       | Gibt die Größe des Videodaten Stroms an, wenn er decodiert wird.                                                            |
| [**Avencvideoencodedimension**](avencvideoencodedimension-property.md)                         | Gibt die Breite und Höhe des codierten Videos an, wenn das Video zugeschnitten ist.                                         |
| [**Avencvideoencodeoffctorigin**](avencvideoencodeoffsetorigin-property.md)                   | Gibt die linke und die obere Ecke des clippingrechtecks an, wenn das Video zugeschnitten ist.                                |
| [**Avencvideofieldswap**](avencvideofieldswap-property.md)                                     | Kehrt die Reihenfolge der Zeilen Sprung Felder im Quellvideo um.                                                      |
| [**Avencvideoforcesourcescantype**](avencvideoforcesourcescantype-property.md)                 | Gibt an, ob die Eingabe Frames progressiv oder Zeilen Sprung sind.                                                     |
| [**Avencvideoheaderdropframe**](avencvideoheaderdropframe-property.md)                         | Gibt den Wert des Drop Frame-Flags im GOP-Header an.                                                             |
| [**Avencvideoheaderframes**](avencvideoheaderframes-property.md)                               | Gibt die Start Rahmennummer im GOP-Header an.                                                                |
| [**Avencvideoheaderhours**](avencvideoheaderhours-property.md)                                 | Gibt die anfangsstunden Nummer im GOP-Header an.                                                                 |
| [**Avencvideoheaderminutes**](avencvideoheaderminutes-property.md)                             | Gibt die anfangsminute Nummer im GOP-Header an.                                                               |
| [**Avencvideoheaderseconds**](avencvideoheaderseconds-property.md)                             | Gibt die Anfangs zweite Zahl im GOP-Header an.                                                               |
| [**Avencvideoinputchromaresolution**](avencvideoinputchromaresolution-property.md)             | Gibt die Chroma-Auflösung des Eingangs Videos an.                                                                   |
| [**Avencvideoinputchromasubsampling**](avencvideoinputchromasubsampling-property.md)           | Gibt die Chroma-Positionierung für das Eingabe Video an.                                                                      |
| [**Avencvideoinputcolorbeleuchtung**](avencvideoinputcolorlighting-property.md)                   | Gibt die vorgesehenen Beleuchtungsbedingungen zum Anzeigen des Eingabe Videos an.                                               |
| [**Avencvideoinputcolornominalrange**](avencvideoinputcolornominalrange-property.md)           | Gibt den nominalen Bereich für das Eingabe Video an.                                                                      |
| [**Avencvideoinputcolorprimaries**](avencvideoinputcolorprimaries-property.md)                 | Gibt die Farb Primärwerte für das Eingabe Video an.                                                                    |
| [**Avencvideoinputcolortransferfunction**](avencvideoinputcolortransferfunction-property.md)   | Gibt die Konvertierungs Funktion von RGB zu r' B ' für ein Eingabe Video an.                                                  |
| [**Avencvideoinputcolortransfermatrix**](avencvideoinputcolortransfermatrix-property.md)       | Gibt für das Eingabe Video die Konvertierungs Matrix aus dem Farbraum ' ' der ' CR ' CR '-Eigenschaft in den ' g ' B '-Farbraum an.         |
| [**Avencvideoinverabtelecineenable**](avencvideoinversetelecineenable-property.md)             | Gibt an, ob der Encoder Inverse Telecine ausführt.                                                              |
| [**Avencvideoinverabtelecinethreshold**](avencvideoinversetelecinethreshold-property.md)       | Legt den Schwellenwert fest, bei dem der Encoder ein Video Feld als redundant ansieht.                                            |
| [**Avencvideomaxkeyframedistance**](avencvideomaxkeyframedistance-property.md)                 | Gibt die maximale Anzahl von Frames zwischen Keyframes an.                                                            |
| [**Avencvideonooffieldstococode**](avencvideonooffieldstoencode-property.md)                   | Gibt die Anzahl der zu codierende Felder an.                                                                             |
| [**Avencvideonooffieldstoskip**](avencvideonooffieldstoskip-property.md)                       | Gibt die Anzahl der Felder an, die während der Codierung übersprungen werden.                                                               |
| [**Avencvideooutputchromaresolution**](avencvideooutputchromaresolution-property.md)           | Gibt die Chroma-Auflösung des codierten Videos an.                                                                 |
| [**Avencvideooutputchromasubsampling**](avencvideooutputchromasubsampling-property.md)         | Gibt die Chroma-Positionierung für das codierte Video an.                                                                    |
| [**Avencvideooutputcolorbeleuchtung**](avencvideooutputcolorlighting-property.md)                 | Gibt die vorgesehenen Beleuchtungsbedingungen zum Anzeigen des codierten Videos an.                                             |
| [**Avencvideooutputcolornominalrange**](avencvideooutputcolornominalrange-property.md)         | Gibt den nominalen Bereich für das codierte Video an.                                                                    |
| [**Avencvideooutputcolorprimaries**](avencvideooutputcolorprimaries-property.md)               | Gibt die Farb Primärwerte für das codierte Video an.                                                                  |
| [**Avencvideooutputcolortransferfunction**](avencvideooutputcolortransferfunction-property.md) | Gibt die Konvertierungs Funktion von RGB in r' B ' für codiertes Video an.                                               |
| [**Avencvideooutputcolortransfermatrix**](avencvideooutputcolortransfermatrix-property.md)     | Gibt die Konvertierungs Matrix für das codierte Video aus dem Farbraum ' ' der ' '-Eigenschaft ' CR ' in den ' g '-Zeichenbereich ' B ' an.       |
| [**Avencvideooutputframerate**](avencvideooutputframerate-property.md)                         | Gibt die Framerate für den Ausgabestream des Encoders in Frames pro Sekunde an.                                        |
| [**Avencvideooutputframerateconversion**](avencvideooutputframerateconversion-property.md)     | Gibt an, ob der Encoder die Framerate konvertiert, wenn die Ausgabe Frame Rate nicht mit der Eingangs Frame Rate identisch ist. |
| [**Avencvideooutputscantype**](avencvideooutputscantype-property.md)                           | Gibt an, wie der Encoder das Ausgabevideo interziert.                                                                |
| [**Avencvideopixelaspectratio**](avencvideopixelaspectratio-property.md)                       | Gibt das Pixel Seitenverhältnis an.                                                                                     |
| [**Avencvideosourcefilmcontent**](avencvideosourcefilmcontent-property.md)                     | Gibt an, ob die ursprüngliche Quelle des Eingabe Videos "Film" oder "Video" war.                                           |
| [**Avencvideosourceisbw**](avencvideosourceisbw-property.md)                                   | Gibt an, ob das Video Monochrom (schwarz und weiß) oder Farbe enthält.                                        |



 

### <a name="audio-encoder-properties"></a>Audioencodereigenschaften



| Eigenschaft                                                                        | BESCHREIBUNG                                                                         |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**Avencaudiodualmono**](avencaudiodualmono-property.md)                       | Gibt an, ob die zwei-Kanal-Audiodaten als Stereo oder Dual Mono codiert werden.                |
| [**Avencaudioinputcontent**](avencaudioinputcontent-property.md)               | Gibt an, ob der Audioinhalt Musik oder Sprache enthält.                        |
| [**Avencaudiointervaldecodecode**](avencaudiointervaltoencode-property.md)       | Gibt die Anzahl der zu codierende Audiobeispiele an.                                    |
| [**Avencaudiointervaldeskip**](avencaudiointervaltoskip-property.md)           | Gibt die Anzahl der Audiobeispiele an, die der Encoder überspringen soll.                      |
| [**Avencaudiomapdestchannel N**](avencaudiomapdestchanneln-property.md)        | Gibt an, welcher Audiokanal Channel *N* im codierten Audiostream zugeordnet ist. |
| [**Avencaudiomeanbitrate**](avencaudiomeanbitrate.md)                          | Gibt die durchschnittliche Bitrate des codierten Audiostreams an.                         |
| [**Avencstatuaudioaveragebps**](avencstataudioaveragebps-property.md)           | Gibt die durchschnittlichen Bits pro Sekunde der codierten Audiodaten zurück.                           |
| [**AVEncStatAudioAveragePCMValue**](avencstataudioaveragepcmvalue-property.md) | Gibt die durchschnittliche Volumeebene des Audioinhalts zurück.                              |
| [**AVEncStatAudioPeakPCMValue**](avencstataudiopeakpcmvalue-property.md)       | Gibt die höchste Volumeebene zurück, die im Audioinhalt vorhanden war.             |



 

### <a name="mpeg-video-encoder-properties"></a>MPEG-Video Encoder-Eigenschaften



| Eigenschaft                                                                                    | BESCHREIBUNG                                                                          |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**Avencmpvaddseqendcode**](avencmpvaddseqendcode-property.md)                             | Gibt an, ob der Encoder am Ende des Streams einen Sequenz-End-Code hinzufügt.     |
| [**Avencmpvdefaultbpicturecount**](avencmpvdefaultbpicturecount-property.md)               | Gibt die Standard Anzahl von aufeinander folgenden B-Frames zwischen I-und P-Frames an.         |
| [**Avencmpvframefieldmode**](avencmpvframefieldmode-property.md)                           | Gibt an, ob der Encoder codierte Felder oder codierte Frames erzeugt.             |
| [**Avencmpvgenerateheaderpicdispext**](avencmpvgenerateheaderpicdispext-property.md)       | Gibt an, ob der Encoder Bild Anzeige Erweiterungs Header generiert.           |
| [**Avencmpvgenerateheaderpicext**](avencmpvgenerateheaderpicext-property.md)               | Gibt an, ob der Encoder Bild Erweiterungs Header generiert.                   |
| [**Avencmpvgenerateheadercqdispext**](avencmpvgenerateheaderseqdispext-property.md)       | Gibt an, ob der Encoder Sequenz Anzeige-Erweiterungs Header generiert.          |
| [**Avencmpvgenerateheaderationqext**](avencmpvgenerateheaderseqext-property.md)               | Gibt an, ob der Encoder Sequenz Erweiterungs Header generiert.                  |
| [**Avencmpvgenerateheadersqscaleext**](avencmpvgenerateheaderseqscaleext-property.md)     | Gibt an, ob der Encoder Sequenz skalierbare Erweiterungs Header generiert.         |
| [**Avencmpvgopopen**](avencmpvgopopen-property.md)                                         | Gibt an, ob der Encoder offene GOPs oder geschlossene GOPs erzeugt.                     |
| [**Avencmpvgopsinabl**](avencmpvgopsinseq-property.md)                                     | Gibt die Anzahl der GOPs Zwischensequenz Headern an.                               |
| [**Avencmpvgopsize**](avencmpvgopsize-property.md)                                         | Gibt die maximale Anzahl von Bildern von einem GOP-Header zum nächsten GOP-Header an. |
| [**Avencmpvintradcprecision**](avencmpvintradcprecision-property.md)                       | Gibt die Genauigkeit der DC-Koeffizienten an.                                      |
| [**Avencmpvintravlctable**](avencmpvintravlctable-property.md)                             | Gibt an, welche VLC-Tabelle (Variable Length Coding) für die Entropie Codierung verwendet werden soll.        |
| [**Avencmpvlevel**](avencmpvlevel-property.md)                                             | Gibt die MPEG-2-Ebene an.                                                          |
| [**Avencmpvprofile**](avencmpvprofile-property.md)                                         | Gibt das MPEG-2-Profil an.                                                        |
| [**Avencmpvqscaletype**](avencmpvqscaletype-property.md)                                   | Gibt an, ob die quantisierungsskala linear oder nicht linear ist.                       |
| [**Avencmpvquantmatrixchromaintra**](avencmpvquantmatrixchromaintra-property.md)           | Gibt die Chroma-quantisierungsmatrix für Intra-Makroblocks an.                      |
| [**Avencmpvquantmatrixchromanonintra**](avencmpvquantmatrixchromanonintra-property.md)     | Gibt die Chroma-quantisierungsmatrix für nicht-Inner-Makroblocks an.                  |
| [**Avencmpvquantmatrixintra**](avencmpvquantmatrixintra-property.md)                       | Gibt die Luma-quantisierungsmatrix für Inner Makroblocks an.                        |
| [**Avencmpvquantmatrixnonintra**](avencmpvquantmatrixnonintra-property.md)                 | Gibt die Luma-quantisierungsmatrix für nicht-Inner-Makroblocks an.                    |
| [**Avencmpvscanpattern**](avencmpvscanpattern-property.md)                                 | Gibt das Makroblock-Scan Muster an.                                               |
| [**Avencmpvsceneerkennungs**](avencmpvscenedetection-property.md)                           | Gibt an, wie sich der Encoder verhält, wenn er eine neue Szene erkennt.                       |
| [**Avencmpvuseconcealmentmotionvectors**](avencmpvuseconcealmentmotionvectors-property.md) | Gibt an, ob der Encoder Verschleierung-Bewegungsvektoren verwendet.                       |



 

### <a name="mpeg-audio-encoder-properties"></a>MPEG-audiocodierungs Eigenschaften



| Eigenschaft                                                                                  | BESCHREIBUNG                                                                   |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**Avencmpacodingmode**](avencmpacodingmode-property.md)                                 | Gibt den MPEG-1-audiocodierungs Modus an.                                     |
| [**Avencmpacopyright**](avencmpacopyright-property.md)                                   | Gibt die Standardeinstellung für das Copyright-Bit an.                          |
| [**Avencmpbetonung sType**](avencmpaemphasistype-property.md)                             | Gibt den Typ des deduplizierungsfilters an, der beim Decodieren verwendet werden soll.   |
| [**Avencmpenableredundancyprotection**](avencmpaenableredundancyprotection-property.md) | Gibt an, ob dem Frame Header eine zyklische Redundanz Überprüfung (CRC) hinzugefügt werden soll. |
| [**Avencmpalayer**](avencmpalayer-property.md)                                           | Gibt die MPEG-Audioschicht an.                                               |
| [**Avencmporiginalbitstream**](avencmpaoriginalbitstream-property.md)                   | Gibt die Standardeinstellung für das ursprüngliche Bit an.                           |
| [**Avencmpaprivateuserbit**](avencmpaprivateuserbit-property.md)                         | Legt den Wert des privaten Benutzer Bits fest.                                       |



 

### <a name="dolby-digital-audio-decoder-properties"></a>Dolby Digital-Audiodecoder-Eigenschaften



| Eigenschaft                                                                      | BESCHREIBUNG                                                                    |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**Avdecdddynamicrangescalehigh**](avdecdddynamicrangescalehigh-property.md) | Gibt den Ausschneide Bereich auf hoher Ebene an, wenn der Decoder das dynamische Bereichs Steuerelement ausführt.  |
| [**Avdecdddynamicrangescalelow**](avdecdddynamicrangescalelow-property.md)   | Gibt die Verstärkung auf niedriger Ebene an, wenn der Decoder das dynamische Bereichs Steuerelement ausführt. |
| [**Avdecddoperationalmode**](avdecddoperationalmode-property.md)             | Gibt den Komprimierungs Steuerungs Modus an.                                        |



 

### <a name="dolby-digital-audio-encoder-properties"></a>Dolby Digital-audioencodereigenschaften



| Eigenschaft                                                                                        | BESCHREIBUNG                                                                               |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**Avencddatodconvertertype**](avencddatodconvertertype-property.md)                           | Gibt den Typ der analog-zu-Digital-Konvertierung (A/D) an.                                 |
| [**Avencddcentredownmixlevel**](avencddcentredownmixlevel-property.md)                         | Gibt die mitteldownmischungs Ebene an.                                                       |
| [**Avencddchannelbwlowpassfilter**](avencddchannelbwlowpassfilter-property.md)                 | Gibt an, ob ein Low-Pass-Filter auf die Haupt Eingabe Kanäle angewendet wird.                |
| [**Avencddcopyright**](avencddcopyright-property.md)                                           | Gibt das Copyright-Flag an.                                                             |
| [**Avencdddchighpassfilter**](avencdddchighpassfilter-property.md)                             | Gibt an, ob ein DC-blockierender High-Pass-Filter angewendet wird.                              |
| [**Avencdddialognormalisierung**](avencdddialognormalization-property.md)                       | Gibt die Dialogfeld normalisierungs Ebene an.                                                 |
| [**Avencdddigitaldeakzente**](avencdddigitaldeemphasis-property.md)                           | Gibt an, ob digitale Deduplizierung.                                                    |
| [**Avencdddynamicrangecompressioncontrol**](avencdddynamicrangecompressioncontrol-property.md) | Gibt das Profil für das dynamische Bereichs Steuerelement an.                                              |
| [**Avencddheadphonemode**](avencddheadphonemode-property.md)                                   | Gibt den Telefonmodus an.                                                             |
| [**Avencddlfelowpassfilter**](avencddlfelowpassfilter-property.md)                             | Gibt an, ob ein Low-Pass-Filter auf den LFE-Kanal (Low Frequency Effect) angewendet wird. |
| [**Avencddlorocentermixlvl \_ x10**](avencddlorocentermixlvl-x10-property.md)                    | Gibt die Schicht Schicht an, die auf den Mittelpunkt für das LO/RO-Downmix angewendet wird.     |
| [**Avencddlorosurroundmixlvl \_ x10**](avencddlorosurroundmixlvl-x10-property.md)                | Gibt die Schicht Schicht an, die auf die umschließenden Kanäle für das LO/RO-Downmix angewendet wird.  |
| [**Avencddltrtcentermixlvl \_ x10**](avencddltrtcentermixlvl-x10-property.md)                    | Gibt die Schicht Schicht an, die auf den Mittelkanal für die LT/RT-downmischung angewendet wird.     |
| [**Avencddltrtsurroundmixlvl \_ x10**](avencddltrtsurroundmixlvl-x10-property.md)                | Gibt die auf den umschließenden Kanälen für die LT/RT-downmischung angewendete Schicht Schicht an.  |
| [**Avencddoriginalbitstream**](avencddoriginalbitstream-property.md)                           | Gibt das ursprüngliche Bitstrom-Flag an.                                                    |
| [**Avencddpreferredstereodownmixmode**](avencddpreferredstereodownmixmode-property.md)         | Gibt den bevorzugten Stereo Downmix-Modus an.                                              |
| [**Avencddproductioninfovorhanden**](avencddproductioninfoexists-property.md)                     | Gibt das Flag für die audioproduktionsinformationen an.                                          |
| [**Avencddproductionmixlevel**](avencddproductionmixlevel-property.md)                         | Gibt die Mischungs Ebene an.                                                               |
| [**Avencddproductionroomtype**](avencddproductionroomtype-property.md)                         | Gibt den Raumtyp an.                                                                  |
| [**Avencddrf prebetonung sFilter**](avencddrfpreemphasisfilter-property.md)                       | Gibt die Schutz Einstellung für RF-overmodulation an.                                       |
| [**Avencddservice**](avencddservice-property.md)                                               | Gibt den Audiodienst an.                                                              |
| [**AVEncDDSurround3dBAttenuation**](avencddsurround3dbattenuation-property.md)                 | Gibt an, ob die umschließenden Kanäle vor der Codierung gedämpft werden.                   |
| [**AVEncDDSurround90DegreeePhaseShift**](avencddsurround90degreeephaseshift-property.md)       | Gibt an, ob ein 90-Grad-Phasenwechsel auf die umschließenden Kanäle angewendet wird.            |
| [**Avencddsurrounddownmixlevel**](avencddsurrounddownmixlevel-property.md)                     | Gibt die umschließende Mischungs Ebene an.                                                    |
| [**Avencddsurroundexmode**](avencddsurroundexmode-property.md)                                 | Gibt an, ob der Audiostream in der umschließenden Ex codiert ist                             |



 

### <a name="digital-signal-processing-dsp-properties"></a>Eigenschaften der digitalen Signal Verarbeitung (DSP)



| Eigenschaft                                                                | BESCHREIBUNG                               |
|-------------------------------------------------------------------------|-------------------------------------------|
| [**Avdsploudnesabqualization**](avdsploudnessequalization-property.md) | Aktiviert oder deaktiviert die Lautstärke Ausgleich. |
| [**Avdspspeakerfill**](avdspspeakerfill-property.md)                   | Aktiviert oder deaktiviert die Lautsprecher Füllung.          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[API-Referenz für Codec](codec-api-reference.md)
</dt> </dl>

 

 



