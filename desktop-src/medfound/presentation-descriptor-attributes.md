---
description: Präsentationsdeskriptorattribute
ms.assetid: 2a092a6a-956b-4c1f-955f-529ec08665fe
title: Präsentationsdeskriptorattribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beb9947a926fc6ea5e21f81219e6bd8d85a8d74bea9b9432ac497c539450b638
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118238966"
---
# <a name="presentation-descriptor-attributes"></a>Präsentationsdeskriptorattribute

## <a name="common-presentation-descriptor-attributes"></a>Allgemeine Darstellungsdeskriptorattribute

Die folgenden Attribute können für jeden Präsentationsdeskriptor gelten.



| attribute                                                                          | BESCHREIBUNG                                                                                                                                     |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MF \_ \_ PD-APP-KONTEXT \_**](mf-pd-app-context-attribute.md)                        | Enthält einen Zeiger auf den Präsentationsdeskriptor aus dem geschützten Medienpfad (PMP).                                                          |
| [**MF \_ PD \_ AUDIO \_ ENCODING \_ BITRATE**](mf-pd-audio-encoding-bitrate-attribute.md) | Gibt die Audiocodierungsbitrate für die Präsentation in Bits pro Sekunde an.                                                                 |
| [MF \_ PD \_ AUDIO \_ ISVARIABLEBITRATE](mf-pd-audio-isvariablebitrate.md)              | Gibt an, ob die Audiostreams in der Präsentation eine variable Bitrate haben.                                                               |
| [**MF \_ PD \_ DURATION**](mf-pd-duration-attribute.md)                               | Gibt die Dauer einer Präsentation in Einheiten von 100 Nanosekunden an.                                                                              |
| [**ZEITPUNKT DER \_ LETZTEN ÄNDERUNG DER MF-PD \_ \_ \_**](mf-pd-last-modified-time-attribute.md)         | Gibt an, wann eine Präsentation zuletzt geändert wurde.                                                                                                |
| [**MF \_ PD \_ \_ MIME-TYP**](mf-pd-mime-type-attribute.md)                            | Gibt den MIME-Typ des Inhalts an.                                                                                                         |
| [MF \_ \_ PD– \_ \_ WIEDERGABEBEGRENZUNGSZEIT](mf-pd-playback-boundary-time.md)               | Die Zeit, zu der die Präsentation relativ zum Anfang der Medienquelle beginnen muss.                                                       |
| [MF \_ PD \_ PLAYBACK \_ ELEMENT \_ ID](mf-pd-playback-element-id.md)                     | Der Bezeichner des Wiedergabelistenelements in der Präsentation.                                                                                     |
| [**MF \_ PD \_ PMPHOST-KONTEXT \_**](mf-pd-pmphost-context-attribute.md)                | Enthält einen Zeiger auf das Proxyobjekt für den Präsentationsdeskriptor der Anwendung.                                                           |
| [BEVORZUGTE SPRACHE \_ FÜR MF PD \_ \_](mf-pd-preferred-language.md)                        | Enthält die bevorzugte RFC 1766-Sprache der Medienquelle.                                                                                   |
| [**MF \_ PD \_ SAMI \_ STYLELIST**](mf-pd-sami-stylelist-attribute.md)                  | Enthält den Benutzerfreundlichen Namen der unterstützten SAMI-Formate (Synchronized Accessible Media Interchange). Dieses Attribut gilt nur für SAMI-Dateien. |
| [**MF \_ PD \_ \_ \_ GESAMTDATEIGRÖßE**](mf-pd-total-file-size-attribute.md)               | Gibt die Gesamtgröße der Quelldatei in Bytes an.                                                                                          |
| [**MF \_ PD \_ VIDEO \_ ENCODING \_ BITRATE**](mf-pd-video-encoding-bitrate-attribute.md) | Gibt die Videocodierungsbitrate für die Präsentation in Bits pro Sekunde an.                                                                 |



 

## <a name="presentation-descriptor-attributes-for-asf"></a>Präsentationsdeskriptorattribute für ASF

Die folgenden Attribute gelten für Präsentationsdeskriptoren für ASF-Dateien (Advanced Systems Format).



| attribute                                                                                                             | BESCHREIBUNG                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**MF \_ PD \_ ASF \_ CODECLIST**](mf-pd-asf-codeclist-attribute.md)                                                       | Enthält Informationen zu den Codecs, die zum Codieren des Inhalts in einer ASF-Datei verwendet werden.                     |
| [**MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ KEYID**](mf-pd-asf-contentencryption-keyid-attribute.md)                          | Gibt den Schlüsselbezeichner für eine verschlüsselte ASF-Datei an.                                              |
| [**MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ LICENSE \_ URL**](mf-pd-asf-contentencryption-license-url-attribute.md)             | Gibt die Lizenzerwerbs-URL für eine verschlüsselte ASF-Datei an.                                     |
| [**MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ SECRET \_ DATA**](mf-pd-asf-contentencryption-secret-data-attribute.md)             | Enthält geheime Daten für eine verschlüsselte ASF-Datei.                                                      |
| [**MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ TYPE**](mf-pd-asf-contentencryption-type-attribute.md)                            | Gibt den Typ des Schutzmechanismus an, der in einer ASF-Datei verwendet wird.                                      |
| [**MF \_ PD \_ ASF \_ CONTENTENCRYPTIONEX \_ ENCRYPTION \_ DATA**](mf-pd-asf-contentencryptionex-encryption-data-attribute.md) | Enthält Verschlüsselungsdaten für eine ASF-Datei.                                                            |
| [**MF \_ PD \_ \_ ASF-DATENLÄNGE \_**](mf-pd-asf-data-length-attribute.md)                                                  | Gibt die Größe des Datenabschnitts einer ASF-Datei in Bytes an.                                    |
| [**MF \_ PD \_ ASF \_ DATA \_ START \_ OFFSET**](mf-pd-asf-data-start-offset-attribute.md)                                     | Gibt den Offset vom Anfang einer ASF-Datei bis zum Anfang des ersten Datenpakets in Bytes an. |
| [**ERSTELLUNGSZEIT DER MF \_ \_ PD-ASF-DATEIEIGENSCHAFTEN \_ \_ \_**](mf-pd-asf-fileproperties-creation-time-attribute.md)               | Gibt das Datum und die Uhrzeit der ersten Erstellung einer ASF-Datei an.                                  |
| [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ FILE \_ ID**](mf-pd-asf-fileproperties-file-id-attribute.md)                           | Gibt den Dateibezeichner einer ASF-Datei an.                                                        |
| [**MF \_ \_ PD-ASF-DATEIEIGENSCHAFTENFLAGS \_ \_**](mf-pd-asf-fileproperties-flags-attribute.md)                                | Enthält verschiedene Flags aus einem ASF-Header.                                                     |
| [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ MAX \_ BITRATE**](mf-pd-asf-fileproperties-max-bitrate-attribute.md)                   | Gibt die maximale sofortige Bitrate in Bits pro Sekunde für eine ASF-Datei an.                   |
| [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ MAX \_ PACKET \_ SIZE**](mf-pd-asf-fileproperties-max-packet-size-attribute.md)          | Gibt die maximale Paketgröße in Byte für eine ASF-Datei an.                                         |
| [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ MIN \_ PACKET \_ SIZE**](mf-pd-asf-fileproperties-min-packet-size-attribute.md)          | Gibt die minimale Paketgröße in Byte für eine ASF-Datei an.                                        |
| [**MF \_ \_ PD-ASF-DATEIEIGENSCHAFTENPAKETE \_ \_**](mf-pd-asf-fileproperties-packets-attribute.md)                            | Gibt die Anzahl der Pakete im Datenabschnitt einer ASF-Datei an.                                  |
| [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ PLAY \_ DURATION**](mf-pd-asf-fileproperties-play-duration-attribute.md)               | Gibt die zeit für die Wiedergabe einer ASF-Datei in Einheiten von 100 Nanosekunden an.                              |
| [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ PREROLL**](mf-pd-asf-fileproperties-preroll-attribute.md)                            | Gibt die Zeit in Millisekunden an, für die Daten gepuffert werden müssen, bevor mit der Wiedergabe einer ASF-Datei gestartet wird.    |
| [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ SEND \_ DURATION**](mf-pd-asf-fileproperties-send-duration-attribute.md)               | Gibt die Zeit an, die zum Senden einer ASF-Datei in Einheiten von 100 Nanosekunden benötigt wird.                              |
| [**MF \_ PD \_ ASF \_ INFO \_ HAS \_ AUDIO**](mf-pd-asf-info-has-audio-attribute.md)                                           | Gibt an, ob eine ASF-Datei mindestens einen Audiostream enthält.                                    |
| [**MF \_ PD \_ ASF \_ INFO \_ HAS \_ NON \_ AUDIO \_ VIDEO**](mf-pd-asf-info-has-non-audio-video-attribute.md)                     | Gibt an, ob eine ASF-Datei Nicht-Audiostreams enthält.                             |
| [**MF \_ PD \_ ASF \_ INFO \_ HAS \_ VIDEO**](mf-pd-asf-info-has-video-attribute.md)                                           | Gibt an, ob eine ASF-Datei mindestens einen Videostream enthält.                                    |
| [**MF \_ PD \_ ASF \_ LANGLIST**](mf-pd-asf-langlist-attribute.md)                                                         | Gibt die Liste der Sprachen an, die in einer ASF-Datei verwendet werden.                                                 |
| [MF \_ PD \_ ASF \_ LANGLIST \_ LEGACYORDER](mf-pd-asf-langlist-legacyorder.md)                                              | Enthält eine Liste der RFC 1766-Sprachen, die in der aktuellen Präsentation verwendet werden.                              |
| [**MF \_ PD \_ ASF \_ MARKER**](mf-pd-asf-marker-attribute.md)                                                             | Gibt die Marker in einer ASF-Datei an.                                                                |
| [**MF \_ \_ PD-ASF-METADATEN \_ \_ SIND \_ VBR**](mf-pd-asf-metadata-is-vbr-attribute.md)                                         | Gibt an, ob eine ASF-Datei die VBR-Codierung (Variable Bit Rate) verwendet.                                 |
| [**MF \_ PD \_ ASF \_ METADATA \_ LEAKY \_ BUCKET \_ PAIRS**](mf-pd-asf-metadata-leaky-bucket-pairs-attribute.md)                | Beschreibt die Pufferanforderungen für eine VBR-ASF-Datei.                                             |
| [**MF \_ PD \_ ASF \_ METADATA \_ V8 \_ BUFFERAVERAGE**](mf-pd-asf-metadata-v8-bufferaverage-attribute.md)                     | Gibt die durchschnittliche Puffergröße an, die für eine VBR-ASF-Datei erforderlich ist.                                         |
| [**MF \_ PD \_ ASF \_ METADATA \_ V8 \_ VBRPEAK**](mf-pd-asf-metadata-v8-vbrpeak-attribute.md)                                 | Gibt die höchste momentäre Bitrate in einer VBR-ASF-Datei an.                                          |
| [**MF \_ \_ PD-ASF-SKRIPT \_**](mf-pd-asf-script-attribute.md)                                                             | Gibt die Skriptbefehle in einer ASF-Datei an.                                                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation Attribute](media-foundation-attributes.md)
</dt> <dt>

[Präsentationsdeskriptoren](presentation-descriptors.md)
</dt> <dt>

[**PRESENTPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> </dl>

 

 



