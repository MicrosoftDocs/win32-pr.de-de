---
description: Medientyp Attribute
ms.assetid: e84ba3f6-4857-4340-baca-5847650ea7b8
title: Medientyp Attribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fd3bc77197a3a897cd5280338451c33f1ea2637
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351559"
---
# <a name="media-type-attributes"></a>Medientyp Attribute

Die folgenden Attribute gelten für Medientypen. Einige dieser Attribute sind nur für das Umstellen von Legacy-Medientyp Formaten in Media Foundation Medientypen vorgesehen.

## <a name="general-format-attributes"></a>Allgemeine Format Attribute

Diese Attribute können auf alle Medientypen angewendet werden.



| Attribut                                                                            | BESCHREIBUNG                                                                            |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**\_ \_ alle \_ Beispiele \_ unabhängig von MF**](mf-mt-all-samples-independent-attribute.md) | Gibt an, ob jede Stichprobe unabhängig von den anderen Beispielen im Stream ist.       |
| [**MF \_ MT \_ am \_ - \_ Formattyp**](mf-mt-am-format-type-attribute.md)                   | Format-GUID.                                                                           |
| [**MF- \_ MT \_ komprimiert**](mf-mt-compressed-attribute.md)                             | Gibt an, ob die Mediendaten komprimiert sind.                                         |
| [**\_Beispiele für \_ die \_ große Größe \_ von MF MT**](mf-mt-fixed-size-samples-attribute.md)           | Gibt an, ob die Stichproben eine festgelegte Größe aufweisen.                                       |
| [**Haupt-Typ des MF- \_ MT \_ \_**](mf-mt-major-type-attribute.md)                            | GUID des Haupt Typs.                                                                       |
| [**Größe des MF-MT-Beispiels \_ \_ \_**](mf-mt-sample-size-attribute.md)                          | Größe der einzelnen Stichproben (in Bytes).                                                         |
| [**MF- \_ MT- \_ Untertyp**](mf-mt-subtype-attribute.md)                                   | Untertyp-GUID.                                                                          |
| [**\_ \_ Benutzer \_ Daten für MF-MT**](mf-mt-user-data-attribute.md)                              | Enthält Benutzerdaten für einen Medientyp, der aus einer Legacy-Format Struktur konvertiert wurde. |
| [**umschließtes MF- \_ MT \_ \_**](mf-mt-wrapped-type-attribute.md)                        | Enthält einen Medientyp, der in einem anderen Medientyp umschließt wurde.                     |



 

## <a name="audio-format-attributes"></a>Audioformatattribute

Diese Attribute können auf Medientypen angewendet werden, deren Haupttyp mfmediatype \_ -Audiodaten entspricht.



| Attribut                                                                                            | BESCHREIBUNG                                                                                 |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Anzeige der MF \_ \_ \_ -AAC- \_ \_ audioprofilebene \_](mf-mt-aac-audio-profile-level-indication.md)       | Gibt das Audioprofil und die Ebene eines AAC-Streams (Advanced audiocoding) an.             |
| [MF- \_ MT- \_ AAC- \_ Nutzlast \_](mf-mt-aac-payload-type.md)                                             | Gibt den Nutz Lasttyp für einen AAC-Datenstrom (Advanced audiocoding) an.                       |
| [**MF \_ \_ -MT-audiodurchschn. \_ \_ Byte \_ pro \_ Sekunde**](mf-mt-audio-avg-bytes-per-second-attribute.md)         | Die durchschnittliche Anzahl von Bytes pro Sekunde.                                                         |
| [**MF \_ \_ -MT- \_ audiobits \_ pro \_ Beispiel**](mf-mt-audio-bits-per-sample-attribute.md)                    | Anzahl von Bits pro audiostich Probe.                                                            |
| [**MF \_ \_ -MT- \_ Audioblock \_ Ausrichtung**](mf-mt-audio-block-alignment-attribute.md)                     | Block Ausrichtung (in Bytes).                                                                  |
| [**MF \_ \_ -MT \_ - \_ audiokanalmaske**](mf-mt-audio-channel-mask-attribute.md)                           | Gibt die Zuweisung von Audiokanälen zu Redner Positionen an.                            |
| [**MF \_ \_ -MT- \_ audiofloat- \_ Beispiele \_ pro \_ Sekunde**](mf-mt-audio-float-samples-per-second-attribute.md) | Anzahl von Audiobeispielen pro Sekunde (Gleit Komma Wert).                                  |
| [**Konfigurations \_ \_ -und \_ FoldDown- \_ Matrix für MF-MT**](mf-mt-audio-folddown-matrix-attribute.md)                     | Gibt an, wie ein Audiodecoder Multichannel-Audiodaten in Stereoausgabe umwandeln soll.        |
| [**MF \_ \_ -MT- \_ audionum- \_ Kanäle**](mf-mt-audio-num-channels-attribute.md)                           | Anzahl der Audiokanäle.                                                                   |
| [**MF \_ \_ -MT-Audiodaten \_ bevorzugen \_ WaveFormatEx**](mf-mt-audio-prefer-waveformatex-attribute.md)             | Gibt die bevorzugte Legacy Format Struktur an, die beim Umrechnen eines audiomedientyps verwendet werden soll. |
| [**MF \_ \_ -MT- \_ Audiobeispiele \_ pro \_ Block**](mf-mt-audio-samples-per-block-attribute.md)                | Anzahl von Audiobeispielen, die in einem komprimierten Block von Audiodaten enthalten sind.                    |
| [**MF \_ \_ -MT- \_ Audiobeispiele \_ pro \_ Sekunde**](mf-mt-audio-samples-per-second-attribute.md)              | Anzahl von Audiobeispielen pro Sekunde (ganzzahliger Wert).                                         |
| [**zulässige \_ \_ \_ \_ Bits \_ pro \_ Beispiel für MF-MT-Audiodaten**](mf-mt-audio-valid-bits-per-sample-attribute.md)       | Anzahl gültiger Bits von Audiodaten in jedem Audiobeispiel.                                    |
| [**MF \_ MT \_ -Audiodatei \_ wmadrc \_ avgref**](mf-mt-audio-wmadrc-avgref-attribute.md)                         | Verweis auf die durchschnittliche Volumeebene einer Windows Media Audio Datei.                               |
| [**MF \_ MT \_ -Audiodatei \_ wmadrc \_ avgtarget**](mf-mt-audio-wmadrc-avgtarget-attribute.md)                   | Die durchschnittliche zielvolumeebene einer Windows Media Audio Datei.                                  |
| [**MF \_ MT \_ -Audiodatei \_ wmademokratische \_ Peer-Ref**](mf-mt-audio-wmadrc-peakref-attribute.md)                       | Verweis Spitzen Volume-Ebene einer Windows Media Audio Datei.                                  |
| [**MF \_ MT \_ -Audiodatei \_ wmadrc- \_ Peer Ziel**](mf-mt-audio-wmadrc-peaktarget-attribute.md)                 | Die zielvolumeebene einer Windows Media Audio Datei.                                     |
| [MF- \_ MT- \_ ursprüngliches \_ Wave- \_ \_ Formattag](mf-mt-original-wave-format-tag.md)                            | Enthält das ursprüngliche Wave-Formattag für einen Audiodatenstrom.                                  |



 

## <a name="video-format-attributes"></a>Video Format Attribute

Diese Attribute können auf Medientypen angewendet werden, deren Haupttyp dem mfmediatype- \_ Video entspricht.



| Attribut                                                                              | BESCHREIBUNG                                                                                                                             |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**durchschnittliche \_ \_ \_ \_ Fehler \_ Rate des MF-MT-Durchschnittl.**](mf-mt-avg-bit-error-rate-attribute.md)            | Datenfehler Rate.                                                                                                                        |
| [**MF-mittlere mittlere \_ \_ \_ Bitrate**](mf-mt-avg-bitrate-attribute.md)                            | Ungefähre Datenrate des Videostreams.                                                                                              |
| [**\_ \_ benutzerdefinierte benutzerdefinierte \_ Videos \_ zu MF MT**](mf-mt-custom-video-primaries-attribute.md)     | Benutzerdefinierte Farb Replikate.                                                                                                                 |
| [**MF- \_ MT- \_ Standard \_ Schritt**](mf-mt-default-stride-attribute.md)                      | Standard Oberflächen Schritt.                                                                                                                 |
| [**MF- \_ MT- \_ DRM- \_ Flags**](mf-mt-drm-flags-attribute.md)                                | Gibt an, ob für das Video der Kopierschutz erzwungen werden muss.                                                                         |
| [**MF- \_ MT- \_ Frame \_ Rate**](mf-mt-frame-rate-attribute.md)                              | Die Framerate.                                                                                                                             |
| [maximal zulässige Anzahl von MF- \_ MT- \_ Frame \_ Raten \_ \_](mf-mt-frame-rate-range-max.md)                      | Die von einem Video Erfassungsgerät unterstützte maximale Framerate.                                                                             |
| [Bereich für die Anzahl von MF \_ MT- \_ Frame \_ Raten \_ \_](mf-mt-frame-rate-range-min.md)                      | Die von einem Video Erfassungsgerät unterstützte minimale Framerate.                                                                             |
| [**MF- \_ MT- \_ Frame \_ Größe**](mf-mt-frame-size-attribute.md)                              | Breite und Höhe des Video Frames.                                                                                                    |
| [**\_geometrische Monte-MT- \_ \_ Öffnung**](mf-mt-geometric-aperture-attribute.md)              | Geometrische Öffnung.                                                                                                                     |
| [**MF- \_ MT- \_ Interlace- \_ Modus**](mf-mt-interlace-mode-attribute.md)                      | Beschreibt, wie die Frames mit Zeilen Sprung verknüpft werden.                                                                                                |
| [**\_Maximale Anzahl \_ von \_ Keyframes für MF-MT \_**](mf-mt-max-keyframe-spacing-attribute.md)         | Maximale Anzahl von Frames von einem Keyframe zum nächsten.                                                                                |
| [**minimale Anzahl von MF- \_ MT- \_ \_ anzeigen \_**](mf-mt-minimum-display-aperture-attribute.md) | Minimale Anzeige Öffnung.                                                                                                               |
| [**MF- \_ MT- \_ MPEG- \_ Sequenz \_ Header**](mf-mt-mpeg-sequence-header-attribute.md)         | MPEG-1-oder MPEG-2-Sequenz Header.                                                                                                       |
| [**Code der MF- \_ \_ MPEG- \_ \_ Startzeit \_**](mf-mt-mpeg-start-time-code-attribute.md)        | GOP-Startzeit (Group of Pictures).                                                                                                |
| [**MF- \_ MT- \_ MPEG2- \_ Flags**](mf-mt-mpeg2-flags-attribute.md)                            | Verschiedene Flags für MPEG-2-Video.                                                                                                   |
| [**MF- \_ MT- \_ \_ Ebene**](mf-mt-mpeg2-level-attribute.md)                            | MPEG-2-oder H. 264-Ebene.                                                                                                                  |
| [**MF- \_ MT- \_ MPEG2- \_ Profil**](mf-mt-mpeg2-profile-attribute.md)                        | MPEG-2-oder H. 264-Profil.                                                                                                                |
| [MF \_ MT \_ ursprüngliches \_ 4CC](mf-mt-original-4cc.md)                                        | Enthält den ursprünglichen Codec FourCC für einen Videostream.                                                                                  |
| [**MF- \_ MT- \_ \_ \_ steuerungflags**](mf-mt-pad-control-flags-attribute.md)               | Seitenverhältnis des Ausgabe Rechtecks.                                                                                                   |
| [**MF- \_ MT- \_ Palette**](mf-mt-palette-attribute.md)                                     | Paletteneinträge.                                                                                                                        |
| [**MF- \_ MT- \_ Schwenken- \_ Überprüfung \_**](mf-mt-pan-scan-aperture-attribute.md)               | Definiert den 4 × 3-Bereich von Video, der im Pan/Scan-Modus angezeigt werden soll.                                                              |
| [**MF- \_ MT- \_ Schwenken- \_ Scan \_ aktiviert**](mf-mt-pan-scan-enabled-attribute.md)                 | Gibt an, ob der Pan/Scan-Modus aktiviert ist.                                                                                             |
| [**Verhältnis der MF- \_ MT- \_ Pixel \_ Seite \_**](mf-mt-pixel-aspect-ratio-attribute.md)             | Pixel Seitenverhältnis.                                                                                                                     |
| [**MF- \_ MT- \_ Quell \_ Inhalts \_ Hinweis**](mf-mt-source-content-hint-attribute.md)           | Gewünschtes Seitenverhältnis.                                                                                                                  |
| [**MF- \_ MT- \_ Übertragungs \_ Funktion**](mf-mt-transfer-function-attribute.md)                | Konvertierungs Funktion von RGB in r' g ' B '.                                                                                                 |
| [MF \_ \_ -MT \_ -Video 3D](mf-mt-video-3d.md)                                                | Gibt an, ob ein Videostream 3D-Inhalt enthält.                                                                                   |
| [**MF- \_ MT- \_ Video- \_ Chroma- \_ siting**](mf-mt-video-chroma-siting-attribute.md)           | Beschreibt, wie Chroma für das Video "y' cb' CR '" als Stichprobe genommen wurde.                                                                                    |
| [**MF- \_ MT- \_ Video \_ Beleuchtung**](mf-mt-video-lighting-attribute.md)                      | Optimale Beleuchtungsbedingungen für die Anzeige.                                                                                                |
| [**\_ \_ \_ nominaler Bereich von MF MT-Video \_**](mf-mt-video-nominal-range-attribute.md)           | Der nominale Bereich der Farbinformationen                                                                                                  |
| [**MF- \_ MT- \_ Video- \_ primär**](mf-mt-video-primaries-attribute.md)                    | Farb Replikate.                                                                                                                        |
| [MF- \_ MT- \_ Video \_ Drehung](mf-mt-video-rotation.md)                                    | Gibt die Drehung eines Video Frames in der Richtung gegen den Uhrzeigersinn an.                                                             |
| [**MF \_ MT \_ YUV \_ Matrix**](mf-mt-yuv-matrix-attribute.md)                              | Die Konvertierungs Matrix aus dem Farbraum ' ' der ' ' ' ' ' CR ' '                                                              |
| [MF \_ xvp \_ Caller \_ weist die \_ Ausgabe zu](mf-xvp-caller-allocates-output.md)               | Gibt an, ob der Aufrufer die Texturen zuweist, die von der [**Video Prozessor-MFT**](video-processor-mft.md)für die Ausgabe verwendet werden. |
| [MF \_ xvp \_ deaktiviert \_ FRC](mf-xvp-disable-frc.md)                                        | Deaktiviert die Frameraten Konvertierung in der [**MFT des Video Prozessors**](video-processor-mft.md).                                               |



 

## <a name="other-format-attributes"></a>Andere Format Attribute

Die folgenden Attribute gelten für das überlappende DV-Video.



| Attribut                                                                      | BESCHREIBUNG                                                           |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [**MF \_ MT \_ DV \_ Aaux \_ STRG \_ Pack \_ 0**](mf-mt-dv-aaux-ctrl-pack-0-attribute.md) | Das Quell Code Verwaltungspaket für die audioerweiterung (Aaux) für den ersten Audioblock. |
| [**MF \_ MT \_ DV \_ Aaux \_ STRG \_ Pack \_ 1**](mf-mt-dv-aaux-ctrl-pack-1-attribute.md) | Aaux-Quell Code Verwaltungspaket für den zweiten Audioblock.                  |
| [**MF \_ MT \_ DV \_ Aaux \_ src \_ Pack \_ 0**](mf-mt-dv-aaux-src-pack-0-attribute.md)   | Aaux Source Pack für den ersten Audioblock.                           |
| [**MF \_ MT \_ DV \_ Aaux \_ src \_ Pack \_ 1**](mf-mt-dv-aaux-src-pack-1-attribute.md)   | Aaux Source Pack für den zweiten Audioblock.                          |
| [**MF \_ MT \_ DV \_ Vaux \_ STRG- \_ Paket**](mf-mt-dv-vaux-ctrl-pack-attribute.md)      | Codehilfssteuerungspaket (Vaux).                           |
| [**MF \_ MT \_ DV \_ Vaux \_ src- \_ Paket**](mf-mt-dv-vaux-src-pack-attribute.md)        | Vaux-Quellpaket.                                                     |



 

Die folgenden Attribute gelten für ASF-Dateien (Advanced Streaming Format).



| Attribut                                                      | BESCHREIBUNG                                                      |
|----------------------------------------------------------------|------------------------------------------------------------------|
| [\_ \_ beliebiges \_ Format der MF-MT](mf-mt-arbitrary-format.md)        | Zusätzliche Formatierungsdaten für einen binären Stream in einer ASF-Datei.       |
| [\_ \_ beliebiger Header von MF MT \_](mf-mt-arbitrary-header.md)        | Typspezifische Daten für einen binären Stream in einer ASF-Datei.           |
| [MF- \_ MT- \_ Abbild \_ Verlust \_ TOLERANT](mf-mt-image-loss-tolerant.md) | Gibt an, ob ein ASF-Bildstream ein abbaubarer JPEG-Typ ist. |



 

Die folgenden Attribute gelten für MPEG-4-Dateien.



| Attribut                                                                     | BESCHREIBUNG                                                   |
|-------------------------------------------------------------------------------|---------------------------------------------------------------|
| [\_Beispiel Eintrag für MF MT \_ MPEG4 \_ aktuell \_ \_](mf-mt-mpeg4-current-sample-entry.md) | Der Index des aktuellen Eintrags im Feld für die Beispiel Beschreibung. |
| [\_ \_ \_ Beispiel Beschreibung für MF MT MPEG4 \_](mf-mt-mpeg4-sample-description.md)      | Das Feld für die Beispiel Beschreibung.                                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IMF MediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Media Foundation Attribute](media-foundation-attributes.md)
</dt> <dt>

[Medientypen](media-types.md)
</dt> <dt>

[Audiomedientypen](audio-media-types.md)
</dt> <dt>

[Video Medientypen](video-media-types.md)
</dt> </dl>

 

 



