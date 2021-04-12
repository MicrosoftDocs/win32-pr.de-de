---
description: Präsentations deskriptorattribute
ms.assetid: 2a092a6a-956b-4c1f-955f-529ec08665fe
title: Präsentations deskriptorattribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18bba97a0e0428bf2ceb91b04c79f69b557876a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527854"
---
# <a name="presentation-descriptor-attributes"></a>Präsentations deskriptorattribute

## <a name="common-presentation-descriptor-attributes"></a>Allgemeine Präsentations deskriptorattribute

Die folgenden Attribute können auf jeden Präsentations Deskriptor angewendet werden.



| Attribut                                                                          | BESCHREIBUNG                                                                                                                                     |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MF- \_ PD- \_ App- \_ Kontext**](mf-pd-app-context-attribute.md)                        | Enthält einen Zeiger auf den Präsentations Deskriptor aus dem geschützten Medien Pfad (PMP).                                                          |
| [**MF \_ \_ -PD- \_ audiocodierungsbitrate \_**](mf-pd-audio-encoding-bitrate-attribute.md) | Gibt die audiocodierungs-Bitrate für die Präsentation in Bits pro Sekunde an.                                                                 |
| [MF \_ PD \_ -Audioschnittstelle \_ isvariablebitrate](mf-pd-audio-isvariablebitrate.md)              | Gibt an, ob die Audiodatenströme in der Präsentation über eine Variable Bitrate verfügen.                                                               |
| [**MF- \_ PD- \_ Dauer**](mf-pd-duration-attribute.md)                               | Gibt die Dauer einer Präsentation in 100-Nanosecond-Einheiten an.                                                                              |
| [**\_Zeitpunkt der \_ letzten \_ Änderung \_ der MF-PD**](mf-pd-last-modified-time-attribute.md)         | Gibt an, wann eine Präsentation zuletzt geändert wurde.                                                                                                |
| [**MF \_ PD- \_ MIME- \_ Typ**](mf-pd-mime-type-attribute.md)                            | Gibt den MIME-Typ des Inhalts an.                                                                                                         |
| [MF \_ - \_ Zeit für Wiedergabe \_ Grenze \_](mf-pd-playback-boundary-time.md)               | Die Uhrzeit, zu der die Präsentation beginnen muss, relativ zum Anfang der Medienquelle.                                                       |
| [MF \_ - \_ ID-Wiedergabe \_ Element- \_ ID](mf-pd-playback-element-id.md)                     | Der Bezeichner des Wiedergabelisten Elements in der Präsentation.                                                                                     |
| [**MF- \_ PD \_ pmphost- \_ Kontext**](mf-pd-pmphost-context-attribute.md)                | Enthält einen Zeiger auf das Proxy Objekt für den Präsentations Deskriptor der Anwendung.                                                           |
| [von MF \_ PD \_ bevorzugte \_ Sprache](mf-pd-preferred-language.md)                        | Enthält die bevorzugte RFC 1766-Sprache der Medienquelle.                                                                                   |
| [**MF \_ PD \_ Sami \_ stylelist**](mf-pd-sami-stylelist-attribute.md)                  | Enthält den anzeigen amen der unterstützten Sami-Stile (synchronisiert Accessible Media Interchange). Dieses Attribut gilt nur für samadateien. |
| [**gesamte MF- \_ PD- \_ \_ Datei \_ Größe**](mf-pd-total-file-size-attribute.md)               | Gibt die Gesamtgröße der Quelldatei in Bytes an.                                                                                          |
| [**MF \_ PD- \_ Video \_ Codierungs \_ Bitrate**](mf-pd-video-encoding-bitrate-attribute.md) | Gibt die Video Codierungs Bitrate für die Präsentation in Bits pro Sekunde an.                                                                 |



 

## <a name="presentation-descriptor-attributes-for-asf"></a>Präsentations deskriptorattribute für ASF

Die folgenden Attribute gelten für Präsentations Deskriptoren für ASF-Dateien (Advanced Systems Format).



| Attribut                                                                                                             | BESCHREIBUNG                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**MF \_ PD, \_ ASF \_ codeclist**](mf-pd-asf-codeclist-attribute.md)                                                       | Enthält Informationen zu den Codecs, die zum Codieren des Inhalts in einer ASF-Datei verwendet werden.                     |
| [**\_Benutzer- \_ ID-Schlüssel-ID für MF PD ASF \_ \_**](mf-pd-asf-contentencryption-keyid-attribute.md)                          | Gibt den Schlüssel Bezeichner für eine verschlüsselte ASF-Datei an.                                              |
| [**Lizenz-URL für MF \_ PD \_ ASF \_ contentencryption \_ \_**](mf-pd-asf-contentencryption-license-url-attribute.md)             | Gibt die Lizenz Erwerbs-URL für eine verschlüsselte ASF-Datei an.                                     |
| [**Daten für die MF \_ PD- \_ ASF- \_ Inhalts Verschlüsselung \_ \_**](mf-pd-asf-contentencryption-secret-data-attribute.md)             | Enthält geheime Daten für eine verschlüsselte ASF-Datei.                                                      |
| [**MF \_ PD \_ ASF \_ contentencryption- \_ Typ**](mf-pd-asf-contentencryption-type-attribute.md)                            | Gibt den Typ des Schutzmechanismus an, der in einer ASF-Datei verwendet wird.                                      |
| [**MF \_ PD \_ ASF \_ contentverschlüsselungex- \_ Verschlüsselungs \_ Daten**](mf-pd-asf-contentencryptionex-encryption-data-attribute.md) | Enthält Verschlüsselungs Daten für eine ASF-Datei.                                                            |
| [**Länge der MF- \_ \_ \_ Daten \_ Länge von MF**](mf-pd-asf-data-length-attribute.md)                                                  | Gibt die Größe des Daten Abschnitts einer ASF-Datei in Bytes an.                                    |
| [**\_ \_ \_ \_ Start \_ Offset für MF PD-ASF-Daten**](mf-pd-asf-data-start-offset-attribute.md)                                     | Gibt den Offset in Bytes vom Beginn einer ASF-Datei bis zum Anfang des ersten Datenpakets an. |
| [**Zeitpunkt der Erstellung der MF \_ PD- \_ \_ Dateieigenschaften \_ \_**](mf-pd-asf-fileproperties-creation-time-attribute.md)               | Gibt das Datum und die Uhrzeit der anfänglichen Erstellung einer ASF-Datei an.                                  |
| [**Datei-ID für MF \_ PD \_ ASF \_ File Properties \_ \_**](mf-pd-asf-fileproperties-file-id-attribute.md)                           | Gibt den Datei Bezeichner einer ASF-Datei an.                                                        |
| [**MF-und MF- \_ \_ dateproperties- \_ \_ Flags**](mf-pd-asf-fileproperties-flags-attribute.md)                                | Enthält verschiedene Flags aus einem ASF-Header.                                                     |
| [**MF \_ PD \_ ASF \_ File Properties \_ Max. \_ Bitrate**](mf-pd-asf-fileproperties-max-bitrate-attribute.md)                   | Gibt die maximale sofortige Bitrate in Bits pro Sekunde für eine ASF-Datei an.                   |
| [**\_maximal zulässige \_ \_ \_ \_ Paket \_ Größe für MF PD ASF File Properties**](mf-pd-asf-fileproperties-max-packet-size-attribute.md)          | Gibt die maximale Paketgröße in Byte für eine ASF-Datei an.                                         |
| [**MF \_ PD \_ ASF \_ File Properties \_ Min. \_ Paket \_ Größe**](mf-pd-asf-fileproperties-min-packet-size-attribute.md)          | Gibt die minimale Paketgröße in Byte für eine ASF-Datei an.                                        |
| [**MF-,-Paket- \_ \_ \_ Dateieigenschaften \_ Pakete**](mf-pd-asf-fileproperties-packets-attribute.md)                            | Gibt die Anzahl der Pakete im Daten Abschnitt einer ASF-Datei an.                                  |
| [**\_Dauer der \_ \_ \_ Wiedergabe \_ Dauer von MF PD ASF File Properties**](mf-pd-asf-fileproperties-play-duration-attribute.md)               | Gibt die Zeit an, die für die Wiedergabe einer ASF-Datei in 100-Nanosecond-Einheiten erforderlich ist.                              |
| [**MF \_ PD \_ ASF \_ FileProperties- \_ Vorabversion**](mf-pd-asf-fileproperties-preroll-attribute.md)                            | Gibt die Zeitspanne an, die zum Puffern von Daten vor dem Start der Wiedergabe einer ASF-Datei in Millisekunden angegeben wird.    |
| [**\_Dauer der \_ \_ \_ Sende \_ Dauer von MF PD ASF File Properties**](mf-pd-asf-fileproperties-send-duration-attribute.md)               | Gibt die Zeit an, die zum Senden einer ASF-Datei in 100-Nanosecond-Einheiten benötigt wird.                              |
| [**MF \_ PD \_ \_ -ASF \_ -Info enthält \_ Audiodaten**](mf-pd-asf-info-has-audio-attribute.md)                                           | Gibt an, ob eine ASF-Datei mindestens einen Audiostream enthält.                                    |
| [**MF \_ PD \_ \_ -ASF \_ -Info enthält \_ nicht \_ \_ Audiovideo**](mf-pd-asf-info-has-non-audio-video-attribute.md)                     | Gibt an, ob eine ASF-Datei beliebige nicht Audiodatenströme enthält.                             |
| [**MF \_ PD- \_ ASF- \_ Info \_ enthält \_ Video**](mf-pd-asf-info-has-video-attribute.md)                                           | Gibt an, ob eine ASF-Datei mindestens einen Videostream enthält.                                    |
| [**MF \_ PD, \_ ASF \_ langlist**](mf-pd-asf-langlist-attribute.md)                                                         | Gibt die Liste der Sprachen an, die in einer ASF-Datei verwendet werden.                                                 |
| [MF \_ PD \_ ASF \_ langlist \_ legacyorder](mf-pd-asf-langlist-legacyorder.md)                                              | Enthält eine Liste der in der aktuellen Präsentation verwendeten RFC 1766-Sprachen.                              |
| [**MF-,- \_ \_ ASF- \_ Marker**](mf-pd-asf-marker-attribute.md)                                                             | Gibt die Marker in einer ASF-Datei an.                                                                |
| [**MF-,- \_ \_ ASF- \_ Metadaten \_ sind \_ VBR**](mf-pd-asf-metadata-is-vbr-attribute.md)                                         | Gibt an, ob eine ASF-Datei die Codierung der Variablen Bitrate (VBR) verwendet.                                 |
| [**MF \_ PD- \_ ASF-Metadaten, Lecks, \_ Bucket- \_ \_ \_ Paare**](mf-pd-asf-metadata-leaky-bucket-pairs-attribute.md)                | Beschreibt die Puffer Anforderungen für eine VBR-ASF-Datei.                                             |
| [**MF \_ PD \_ ASF \_ Metadata \_ V8 \_ bufferaverage**](mf-pd-asf-metadata-v8-bufferaverage-attribute.md)                     | Gibt die durchschnittliche Puffergröße an, die für eine VBR-ASF-Datei benötigt wird.                                         |
| [**MF \_ PD \_ ASF \_ Metadata \_ V8 \_ vbrpeak**](mf-pd-asf-metadata-v8-vbrpeak-attribute.md)                                 | Gibt die höchste momentane Bitrate in einer VBR-ASF-Datei an.                                          |
| [**MF-,- \_ \_ ASF- \_ Skript**](mf-pd-asf-script-attribute.md)                                                             | Gibt die Skript Befehle in einer ASF-Datei an.                                                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation Attribute](media-foundation-attributes.md)
</dt> <dt>

[Präsentations Deskriptoren](presentation-descriptors.md)
</dt> <dt>

[**IMF presentationdescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> </dl>

 

 



