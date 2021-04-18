---
title: Windows Media-Format-SDK-Strukturen
description: Windows Media-Format-SDK-Strukturen
ms.assetid: 118ef278-ca4f-4c30-9633-a2d851f5c758
keywords:
- Windows Media-Format-SDK, Strukturen
- Advanced Systems Format (ASF), Strukturen
- ASF (Advanced Systems Format), Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f730ba3cbc5bd8bbec2a9f01c72df1fe46f0b64
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106338111"
---
# <a name="windows-media-format-sdk-structures"></a>Windows Media-Format-SDK-Strukturen

Das Windows Media-Format SDK implementiert die folgenden Strukturen.



| Struktur                                                                                | BESCHREIBUNG                                                                                                                                                               |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DRM- \_ Kopier- \_ OPL**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_copy_opl)                                                   | Enthält Informationen zur Ausgabe Schutz Ebene, die für die Kopier Aktion in einer DRM-Lizenz gelten.                                                                               |
| [**DRM- \_ Lizenz \_ Zustands \_ Daten**](drm-license-state-data.md)                              | Enthält [*Lizenz*](wmformat-glossary.md) Informationen zu einem angegebenen [*DRM*](wmformat-glossary.md) -Recht. |
| [**minimale DRM- \_ \_ Ausgabe \_ Schutz \_ Ebenen**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_minimum_output_protection_levels) | Enthält die minimalen Ausgabe Schutz Ebenen, die für eine DRM-Lizenz erforderlich sind, um Inhalte in verschiedenen Formaten wiederzugeben.                                                                      |
| [**DRM- \_ OPL- \_ Ausgabe- \_ IDs**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_opl_output_ids)                                      | Enthält ein Array von DRM-Technologie bezeichlern. Diese Struktur wird verwendet, um Gruppen von Technologien in anderen DRM-Strukturen zu definieren.                                            |
| [**DRM- \_ Wiedergabe- \_ OPL**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_play_opl)                                                   | Enthält Informationen zur Ausgabe Schutz Ebene, die für die Wiedergabe Aktion in einer DRM-Lizenz gelten.                                                                               |
| [**DRM- \_ Wiedergabelisten \_ Inhalts- \_ ID**](drm-playlist-content-id.md)                            | Enthält Informationen zu Inhalten, die als Teil einer Wiedergabeliste auf CD kopiert werden sollen.                                                                                 |
| [**DRM- \_ VAL16**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-drm_val16)                                                          | Speichert einen 128-Bit-Wert, der als Geräte Bezeichner verwendet wird.                                                                                                                       |
| [**DRM- \_ Video \_ Ausgabe \_ Schutz**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_output_protection)                    | Enthält den Bezeichner einer Videoschutz Technologie und die Konfigurationsdaten, die von dieser Technologie benötigt werden.                                                             |
| [**DRM- \_ Video- \_ Ausgabe Schutz- \_ \_ IDs**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_video_output_protection_ids)           | Enthält ein Array von **DRM- \_ Video- \_ ausgabeschutzstrukturen \_** .                                                                                                          |
| [**WAVEFORMATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85))                                                | Definiert das Format von Waveform-Audiodaten.                                                                                                                                |
| [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85))                                | Definiert das Format von Waveform-Audiodaten für Formate mit mehr als zwei Kanälen.                                                                                      |
| [**WM \_ - \_ adressaccessentry**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_address_accessentry)                               | Gibt einen Eintrag in einer IP-Adress Zugriffsliste an.                                                                                                                          |
| [**WM- \_ Client \_ Eigenschaften**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_client_properties)                                   | Zeichnet Informationen zum Client auf.                                                                                                                                     |
| [**WM- \_ Client \_ Eigenschaften ( \_ Ex)**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_client_properties_ex)                            | Zeichnet erweiterte Informationen über den Client auf.                                                                                                                            |
| [**WM \_ - \_ Lizenz \_ Daten erhalten**](wm-get-license-data.md)                                    | Enthält Informationen über eine DRM-Lizenz.                                                                                                                                 |
| [**Status der WM- \_ Individualisierung \_**](wm-individualize-status.md)                             | Zeichnet den Status des [*Individualisierungs*](wmformat-glossary.md) Vorgangs auf.                                                                |
| [**WM- \_ Lecks- \_ Bucket- \_ paar**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_leaky_bucket_pair)                                  | Beschreibt die Puffer Anforderungen für eine VBR-Datei (Variable-Bitrate).                                                                                                  |
| [**WM- \_ Lizenz \_ Zustands \_ Daten**](/previous-versions/windows/desktop/legacy/dd757942(v=vs.85))                                | Kapselt eine [**DRM- \_ Lizenz \_ Zustands \_ Daten**](drm-license-state-data.md) Struktur, in der DRM-Lizenz Zustandsdaten beschrieben werden.                                              |
| [**WM \_ - \_ Medientyp**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type)                                                 | Beschreibt ein Medien Beispiel.                                                                                                                                                 |
| [**WMMPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmmpeg2videoinfo)                                             | Beschreibt einen MPEG-2-Videostream.                                                                                                                                         |
| [**WM- \_ Bild**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture)                                                        | Enthält die Daten für das komplexe Metadatenattribut [**WM/Bild**](wmpicture.md) .                                                                                     |
| [**\_Port \_ Nummern \_ Bereich der WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_port_number_range)                                  | Beschreibt den Bereich von Portnummern, die von der **iwmreadernetworkconfig** -Schnittstelle verwendet werden.                                                                                     |
| [**WM \_ Reader \_ CLIENTINFO**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_clientinfo)                                   | Beschreibt den Client Leser (Player), der auf den Mediendaten Strom zugreift.                                                                                                          |
| [**WM \_ Reader- \_ Statistik**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics)                                   | Beschreibt die Leistung eines Lesevorgangs.                                                                                                                         |
| [**Wmscriptformat**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmscriptformat)                                                 | Definiert das Format eines Skript Datenstroms.                                                                                                                                    |
| [**Datensatz für WM- \_ \_ Datenstrom Priorität \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_priority_record)                        | Enthält eine streamnummer und gibt an, ob die Übermittlung dieses Streams obligatorisch ist.                                                                                      |
| [**Informationen zum WM- \_ \_ Streamtyp \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_type_info)                                    | Enthält die Daten für das komplexe Metadatenattribut [**WM/streamtypeinfo**](wm-streamtypeinfo.md) .                                                                      |
| [**\_synchronisierte WM- \_ Texte**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_synchronised_lyrics)                               | Enthält die Daten für das [**\_ synchierte**](wm-lyrics-synchronised.md) , komplexe Metadatenattribut der WM/Liedtexte.                                                           |
| [**WM- \_ Benutzer \_ Text**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_user_text)                                                   | Enthält die Daten für das Attribut der komplexen [**WM/Text-**](wm-text.md) Metadaten.                                                                                          |
| [**Web-URL für WM- \_ Benutzer \_ \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_user_web_url)                                            | Enthält die Daten für das komplexe Metadatenattribut [**WM/userweburl**](wm-userweburl.md) .                                                                              |
| [**WM \_ Writer- \_ Statistik**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics)                                   | Beschreibt die Leistung eines Schreibvorgangs.                                                                                                                         |
| [**WM \_ Writer \_ Statistics ( \_ Ex)**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics_ex)                            | Enthält erweiterte Writer-Statistiken.                                                                                                                                      |
| [**WMDRM- \_ Import \_ Inhalts \_ Schlüssel**](wmdrm-import-content-key.md)                          | Enthält den Inhalts Schlüssel, der beim Importieren geschützter Inhalte verwendet wird.                                                                                                                |
| [**WMDRM- \_ Import \_ Init- \_ Struktur**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct)                          | Enthält den verschlüsselten Sitzungsschlüssel und den Inhalts Schlüssel, die beim Importieren geschützter Inhalte verwendet werden.                                                                                      |
| [**WMDRM- \_ Schlüssel zum Importieren der \_ Sitzung \_**](wmdrm-import-session-key.md)                          | Enthält den Sitzungsschlüssel zum Importieren geschützter Inhalte.                                                                                                                    |
| [**WMT- \_ Puffer \_ Segment**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_buffer_segment)                                       | Enthält die Informationen, die erforderlich sind, um ein Segment in einem Paket anzugeben.                                                                                                      |
| [**WMT \_ colorspaceingefo- \_ Erweiterungs \_ Daten**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_colorspaceinfo_extension_data)        | Enthält die Daten für die WM- \_ sampleextensionguid \_ colorspaceinfo-Dateneinheiten Erweiterung.                                                                                    |
| [**WMT- \_ filesink- \_ Daten \_ Einheit**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_filesink_data_unit)                              | Enthält Informationen zu einem Paket.                                                                                                                                      |
| [**WMT- \_ Nutz Last \_ Fragment**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_payload_fragment)                                   | Enthält die Informationen, die erforderlich sind, um ein Nutz Last Fragment aus einem Paket zu extrahieren.                                                                                           |
| [**WMT- \_ Zeit Code \_ Erweiterungs \_ Daten**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data)                    | Enthält einen einzelnen SMPTE-Zeit Code und zugehörige Informationen.                                                                                                                |
| [**WMT \_ Videoimage- \_ Beispiel**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample)                                 | Enthält Informationen zu einem Video Bildbeispiel.                                                                                                                          |
| [**WMT- \_ Wasserzeichen \_ Eintrag**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_watermark_entry)                                     | Enthält Informationen über ein Wasserzeichen System.                                                                                                                         |
| [**WMT- \_ Webstream- \_ Format**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format)                                   | Enthält Informationen zu einem Webstream.                                                                                                                                  |
| [**WMT- \_ Webstream- \_ Beispiel \_ Header**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_sample_header)                    | Enthält Header Informationen für webstreambeispiele.                                                                                                                       |
| [**Wmvideoinfoheader**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader)                                           | Beschreibt die Bitmap-und Farbinformationen eines Video Bilds.                                                                                                             |
| [**WMVIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader2)                                         | Beschreibt die Bitmap-und Farbinformationen für ein Video Bild, einschließlich [*interspitze*](wmformat-glossary.md), Kopierschutz und Seitenverhältnis.       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierverzeichnis**](programming-reference.md)
</dt> </dl>

 

 
