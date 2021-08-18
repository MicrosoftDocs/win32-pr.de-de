---
description: Medientypattribute
ms.assetid: e84ba3f6-4857-4340-baca-5847650ea7b8
title: Medientypattribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b52e906baa7bbac14d33dbc263e3a1edfa43b65851d96d0573032784c0149425
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827460"
---
# <a name="media-type-attributes"></a>Medientypattribute

Die folgenden Attribute gelten für Medientypen. Einige dieser Attribute sind nur für die Konvertierung von Legacymedientypformaten in Media Foundation vorgesehen.

## <a name="general-format-attributes"></a>Allgemeine Formatattribute

Diese Attribute können auf alle Medientypen angewendet werden.



| attribute                                                                            | Beschreibung                                                                            |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**MF \_ MT \_ ALL \_ SAMPLES \_ INDEPENDENT**](mf-mt-all-samples-independent-attribute.md) | Gibt an, ob jedes Beispiel von den anderen Stichproben im Stream unabhängig ist.       |
| [**MF \_ MT \_ \_ AM-FORMATTYP \_**](mf-mt-am-format-type-attribute.md)                   | Formatieren der GUID.                                                                           |
| [**MF \_ MT \_ COMPRESSED**](mf-mt-compressed-attribute.md)                             | Gibt an, ob die Mediendaten komprimiert werden.                                         |
| [**BEISPIELE FÜR MF \_ MT \_ MIT FESTER \_ \_ GRÖßE**](mf-mt-fixed-size-samples-attribute.md)           | Gibt an, ob die Beispiele eine feste Größe haben.                                       |
| [**MF \_ \_ MT-HAUPTTYP \_**](mf-mt-major-type-attribute.md)                            | Haupttyp-GUID.                                                                       |
| [**MF \_ \_ MT-STICHPROBENGRÖßE \_**](mf-mt-sample-size-attribute.md)                          | Größe der einzelnen Stichproben in Bytes.                                                         |
| [**MF \_ \_ MT-UNTERTYP**](mf-mt-subtype-attribute.md)                                   | Untertyp-GUID.                                                                          |
| [**MF \_ \_ MT-BENUTZERDATEN \_**](mf-mt-user-data-attribute.md)                              | Enthält Benutzerdaten für einen Medientyp, der aus einer Legacyformatstruktur konvertiert wurde. |
| [**UMSCHLOSSENER MF \_ \_ \_ MT-TYP**](mf-mt-wrapped-type-attribute.md)                        | Enthält einen Medientyp, der von einem anderen Medientyp umschlossen wurde.                     |



 

## <a name="audio-format-attributes"></a>Audioformatattribute

Diese Attribute können auf Medientypen angewendet werden, deren Haupttyp MFMediaType \_ Audio entspricht.



| attribute                                                                                            | Beschreibung                                                                                 |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [MF \_ MT \_ AAC \_ AUDIO \_ PROFILE \_ LEVEL \_ INDICATION](mf-mt-aac-audio-profile-level-indication.md)       | Gibt das Audioprofil und die Ebene eines AAC-Streams (Advanced Audio Coding) an.             |
| [MF \_ MT \_ \_ AAC-NUTZLASTTYP \_](mf-mt-aac-payload-type.md)                                             | Gibt den Nutzlasttyp für einen AAC-Stream (Advanced Audio Coding) an.                       |
| [**MF \_ MT \_ AUDIO \_ AVG \_ BYTES \_ PER \_ SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md)         | Durchschnittliche Anzahl von Bytes pro Sekunde.                                                         |
| [**MF \_ \_ MT-AUDIOBITS \_ \_ PRO \_ BEISPIEL**](mf-mt-audio-bits-per-sample-attribute.md)                    | Anzahl der Bits pro Audiobeispiel.                                                            |
| [**MF MT AUDIO BLOCK ALIGNMENT (MF \_ \_ MT-AUDIOBLOCKAUSRICHTUNG) \_ \_**](mf-mt-audio-block-alignment-attribute.md)                     | Blockausrichtung in Bytes.                                                                  |
| [**MF \_ MT \_ AUDIO \_ CHANNEL \_ MASK**](mf-mt-audio-channel-mask-attribute.md)                           | Gibt die Zuweisung von Audiokanälen zu Sprecherpositionen an.                            |
| [**MF \_ MT \_ AUDIO \_ FLOAT \_ SAMPLES \_ PER \_ SECOND**](mf-mt-audio-float-samples-per-second-attribute.md) | Anzahl von Audiobeispielen pro Sekunde (Gleitkommawert).                                  |
| [**MF \_ MT \_ AUDIO \_ FOLDDOWN \_ MATRIX**](mf-mt-audio-folddown-matrix-attribute.md)                     | Gibt an, wie ein Audiodecoder Multichannel-Audio in Stereoausgabe transformieren soll.        |
| [**MF \_ MT AUDIO \_ \_ \_ NUM-KANÄLE**](mf-mt-audio-num-channels-attribute.md)                           | Anzahl der Audiokanäle.                                                                   |
| [**MF \_ MT \_ AUDIO \_ PREFER \_ WAVEFORMATEX**](mf-mt-audio-prefer-waveformatex-attribute.md)             | Gibt die bevorzugte Legacyformatstruktur an, die beim Konvertieren eines Audiomedientyps verwendet werden soll. |
| [**MF \_ \_ MT-AUDIOBEISPIELE \_ \_ PRO \_ BLOCK**](mf-mt-audio-samples-per-block-attribute.md)                | Anzahl der Audiobeispiele, die in einem komprimierten Block von Audiodaten enthalten sind.                    |
| [**MF \_ \_ MT-AUDIOBEISPIELE \_ \_ PRO \_ SEKUNDE**](mf-mt-audio-samples-per-second-attribute.md)              | Anzahl der Audiobeispiele pro Sekunde (ganzzahliger Wert).                                         |
| [**GÜLTIGE MF \_ \_ MT-AUDIOBITS \_ \_ PRO \_ \_ BEISPIEL**](mf-mt-audio-valid-bits-per-sample-attribute.md)       | Anzahl der gültigen Bits von Audiodaten in jedem Audiobeispiel.                                    |
| [**MF \_ MT \_ AUDIO \_ WMADRC \_ AVGREF**](mf-mt-audio-wmadrc-avgref-attribute.md)                         | Referenz zur durchschnittlichen Volumeebene einer Windows Medienaudiodatei.                               |
| [**MF \_ MT \_ AUDIO \_ WMADRC \_ AVGTARGET**](mf-mt-audio-wmadrc-avgtarget-attribute.md)                   | Ziel der durchschnittlichen Volumeebene einer Windows Medienaudiodatei.                                  |
| [**MF \_ MT \_ AUDIO \_ WMADRC \_ PEAKREF**](mf-mt-audio-wmadrc-peakref-attribute.md)                       | Verweisen sie auf die Spitzenvolumenebene einer Windows Medienaudiodatei.                                  |
| [**MF \_ MT \_ AUDIO \_ WMADRC \_ PEAKTARGET**](mf-mt-audio-wmadrc-peaktarget-attribute.md)                 | Das Ziel der Spitzenvolumenebene einer Windows Medienaudiodatei.                                     |
| [MF \_ MT \_ ORIGINAL \_ WAVE \_ FORMAT \_ TAG](mf-mt-original-wave-format-tag.md)                            | Enthält das ursprüngliche WAVE-Formattag für einen Audiostream.                                  |



 

## <a name="video-format-attributes"></a>Videoformatattribute

Diese Attribute können auf Medientypen angewendet werden, deren Haupttyp MFMediaType \_ Video entspricht.



| attribute                                                                              | Beschreibung                                                                                                                             |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**MF \_ MT \_ AVG \_ BIT \_ ERROR \_ RATE**](mf-mt-avg-bit-error-rate-attribute.md)            | Datenfehlerrate.                                                                                                                        |
| [**MF \_ MT \_ AVG \_ BITRATE**](mf-mt-avg-bitrate-attribute.md)                            | Ungefähre Datenrate des Videostreams.                                                                                              |
| [**MF \_ MT CUSTOM VIDEO – \_ \_ \_ PRIMÄRER CODE**](mf-mt-custom-video-primaries-attribute.md)     | Benutzerdefinierte Farbprimprimries.                                                                                                                 |
| [**MF \_ MT \_ DEFAULT \_ STRIDE**](mf-mt-default-stride-attribute.md)                      | Standardoberflächenschritt.                                                                                                                 |
| [**MF \_ MT \_ \_ DRM-FLAGS**](mf-mt-drm-flags-attribute.md)                                | Gibt an, ob das Video den Kopierschutz erzwingen muss.                                                                         |
| [**MF \_ MT \_ FRAME \_ RATE**](mf-mt-frame-rate-attribute.md)                              | Bildrate.                                                                                                                             |
| [MF \_ MT \_ FRAME \_ RATE \_ RANGE \_ MAX](mf-mt-frame-rate-range-max.md)                      | Die maximale Bildfrequenz, die von einem Videoaufnahmegerät unterstützt wird.                                                                             |
| [MF \_ MT \_ FRAME \_ RATE \_ RANGE \_ MIN](mf-mt-frame-rate-range-min.md)                      | Die minimale Bildfrequenz, die von einem Videoaufnahmegerät unterstützt wird.                                                                             |
| [**MF \_ MT \_ FRAME \_ SIZE**](mf-mt-frame-size-attribute.md)                              | Breite und Höhe des Videoframes.                                                                                                    |
| [**MF \_ MT \_ GEOMETRIC \_ APERTURE**](mf-mt-geometric-aperture-attribute.md)              | Geometrische Öffnung.                                                                                                                     |
| [**MF \_ MT \_ INTERLACE-MODUS \_**](mf-mt-interlace-mode-attribute.md)                      | Beschreibt, wie die Frames verschachtelt werden.                                                                                                |
| [**MF \_ MT \_ MAX \_ KEYFRAME \_ SPACING**](mf-mt-max-keyframe-spacing-attribute.md)         | Maximale Anzahl von Frames von einem Keyframe zum nächsten.                                                                                |
| [**MF \_ MT \_ MINIMUM \_ DISPLAY \_ APERTURE**](mf-mt-minimum-display-aperture-attribute.md) | Minimale Anzeigeblende.                                                                                                               |
| [**MF \_ MT \_ MPEG \_ SEQUENCE \_ HEADER**](mf-mt-mpeg-sequence-header-attribute.md)         | MPEG-1- oder MPEG-2-Sequenzheader.                                                                                                       |
| [**MF \_ MT \_ MPEG \_ START \_ TIME \_ CODE**](mf-mt-mpeg-start-time-code-attribute.md)        | GoP-Startzeitcode (Group-of-Pictures).                                                                                                |
| [**MF \_ MT \_ \_ MPEG2-FLAGS**](mf-mt-mpeg2-flags-attribute.md)                            | Verschiedene Flags für MPEG-2-Videos.                                                                                                   |
| [**MF \_ MT \_ MPEG2 \_ LEVEL**](mf-mt-mpeg2-level-attribute.md)                            | MPEG-2- oder H.264-Ebene.                                                                                                                  |
| [**MF \_ MT \_ \_ MPEG2-PROFIL**](mf-mt-mpeg2-profile-attribute.md)                        | MPEG-2- oder H.264-Profil.                                                                                                                |
| [MF \_ MT \_ ORIGINAL \_ 4CC](mf-mt-original-4cc.md)                                        | Enthält den ursprünglichen Codec FOURCC für einen Videostream.                                                                                  |
| [**MF \_ MT \_ \_ PAD-STEUERUNGSFLAGS \_**](mf-mt-pad-control-flags-attribute.md)               | Seitenverhältnis des Ausgaberechtecks.                                                                                                   |
| [**MF \_ MT \_ PALETTE**](mf-mt-palette-attribute.md)                                     | Paletteneinträge.                                                                                                                        |
| [**MF \_ MT \_ PAN \_ SCAN \_ APERTURE**](mf-mt-pan-scan-aperture-attribute.md)               | Definiert den 4×3-Videobereich, der im Schwenk-/Scanmodus angezeigt werden soll.                                                              |
| [**MF \_ MT \_ PAN \_ SCAN \_ ENABLED**](mf-mt-pan-scan-enabled-attribute.md)                 | Gibt an, ob der Schwenk-/Scanmodus aktiviert ist.                                                                                             |
| [**MF \_ MT PIXEL \_ \_ \_ SEITENVERHÄLTNIS**](mf-mt-pixel-aspect-ratio-attribute.md)             | Pixel-Seitenverhältnis.                                                                                                                     |
| [**MF \_ \_ \_ MT-QUELLINHALTSHINWEIS \_**](mf-mt-source-content-hint-attribute.md)           | Beabsichtigtes Seitenverhältnis.                                                                                                                  |
| [**MF \_ MT \_ \_ TRANSFER-FUNKTION**](mf-mt-transfer-function-attribute.md)                | Konvertierungsfunktion von RGB in R'G'B'.                                                                                                 |
| [MF \_ MT \_ VIDEO \_ 3D](mf-mt-video-3d.md)                                                | Gibt an, ob ein Videostream 3D-Inhalt enthält.                                                                                   |
| [**MF \_ MT \_ VIDEO \_ \_ 2017 – SITING**](mf-mt-video-chroma-siting-attribute.md)           | Beschreibt, wie für das Video "Y'Cb'Cr" Stichproben von Y'Cb'Cr' entnommen wurden.                                                                                    |
| [**MF \_ MT \_ VIDEO \_ LIGHTING**](mf-mt-video-lighting-attribute.md)                      | Optimale Beleuchtungsbedingungen für die Anzeige.                                                                                                |
| [**NOMINALER MF \_ \_ \_ \_ MT-VIDEOBEREICH**](mf-mt-video-nominal-range-attribute.md)           | Nominaler Bereich der Farbinformationen                                                                                                  |
| [**MF \_ \_ MT-VIDEO \_ – PRIMÄRER**](mf-mt-video-primaries-attribute.md)                    | Farbprimprimries.                                                                                                                        |
| [MF \_ \_ MT-VIDEOROTATION \_](mf-mt-video-rotation.md)                                    | Gibt die Drehung eines Videoframes in richtung gegen den Uhrzeigersinn an.                                                             |
| [**MF \_ MT \_ YUV \_ MATRIX**](mf-mt-yuv-matrix-attribute.md)                              | Konvertierungsmatrix aus dem Farbraum Y'Cb'Cr' in den Farbraum R'G'B'.                                                              |
| [\_MF-XVP-AUFRUFER \_ \_ ORDNET AUSGABE \_ ZU](mf-xvp-caller-allocates-output.md)               | Gibt an, ob der Aufrufer die Texturen zuteilen soll, die vom [**Videoprozessor-MFT für**](video-processor-mft.md)die Ausgabe verwendet werden. |
| [MF \_ XVP \_ – \_ FRC DEAKTIVIEREN](mf-xvp-disable-frc.md)                                        | Deaktiviert die Bildfrequenzkonvertierung in [**der Videoprozessor-MFT**](video-processor-mft.md).                                               |



 

## <a name="other-format-attributes"></a>Andere Formatattribute

Die folgenden Attribute gelten für überlappte DV-Videos.



| attribute                                                                      | Beschreibung                                                           |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [**MF \_ MT \_ DV \_ AAUX \_ STRG PACK \_ \_ 0**](mf-mt-dv-aaux-ctrl-pack-0-attribute.md) | AAUX-Quellcodeverwaltungspaket (Audio Auxiliary) für den ersten Audioblock. |
| [**MF \_ MT \_ DV \_ AAUX \_ STRG PACK \_ \_ 1**](mf-mt-dv-aaux-ctrl-pack-1-attribute.md) | AAUX-Quellcodeverwaltungspaket für den zweiten Audioblock.                  |
| [**MF \_ MT \_ DV \_ AAUX \_ SRC PACK \_ \_ 0**](mf-mt-dv-aaux-src-pack-0-attribute.md)   | AAUX-Quellpaket für den ersten Audioblock.                           |
| [**MF \_ MT \_ DV \_ AAUX \_ SRC PACK \_ \_ 1**](mf-mt-dv-aaux-src-pack-1-attribute.md)   | AAUX-Quellpaket für den zweiten Audioblock.                          |
| [**MF \_ MT \_ DV \_ VAUX \_ CTRL \_ PACK**](mf-mt-dv-vaux-ctrl-pack-attribute.md)      | Quellcodeverwaltungspaket für Videohilfsgeräte (Video Auxiliary, AUX).                           |
| [**MF \_ MT \_ DV \_ ́SRC \_ \_ PACK**](mf-mt-dv-vaux-src-pack-attribute.md)        | DANN-Quellpaket.                                                     |



 

Die folgenden Attribute gelten für ASF-Dateien (Advanced Streaming Format).



| attribute                                                      | Beschreibung                                                      |
|----------------------------------------------------------------|------------------------------------------------------------------|
| [MF \_ MT \_ ARBITRARY \_ FORMAT](mf-mt-arbitrary-format.md)        | Zusätzliche Formatdaten für einen binären Stream in einer ASF-Datei.       |
| [MF \_ MT \_ ARBITRARY \_ HEADER](mf-mt-arbitrary-header.md)        | Typspezifische Daten für einen binären Stream in einer ASF-Datei.           |
| [MF \_ MT– \_ \_ \_ BILDVERLUSTTOLERANT](mf-mt-image-loss-tolerant.md) | Gibt an, ob ein ASF-Bildstream ein heruntersetzbarer JPEG-Typ ist. |



 

Die folgenden Attribute gelten für MPEG-4-Dateien.



| attribute                                                                     | Beschreibung                                                   |
|-------------------------------------------------------------------------------|---------------------------------------------------------------|
| [MF \_ MT \_ MPEG4 – AKTUELLER \_ \_ \_ BEISPIELEINTRAG](mf-mt-mpeg4-current-sample-entry.md) | Der Index des aktuellen Eintrags im Beispielbeschreibungsfeld. |
| [BESCHREIBUNG DES MF \_ MT \_ \_ MPEG4-BEISPIELS \_](mf-mt-mpeg4-sample-description.md)      | Das Beispielbeschreibungsfeld.                                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**VERERBungstyp**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Media Foundation Attribute](media-foundation-attributes.md)
</dt> <dt>

[Medientypen](media-types.md)
</dt> <dt>

[Audiomedientypen](audio-media-types.md)
</dt> <dt>

[Videomedientypen](video-media-types.md)
</dt> </dl>

 

 



