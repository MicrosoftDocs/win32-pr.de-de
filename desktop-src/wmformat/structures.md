---
title: Windows Medienformat-SDK-Strukturen
description: Windows Medienformat-SDK-Strukturen
ms.assetid: 118ef278-ca4f-4c30-9633-a2d851f5c758
keywords:
- Windows Medienformat-SDK, Strukturen
- Advanced Systems Format (ASF), Strukturen
- ASF (Advanced Systems Format), structures
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 319be2d061132f59c1c75ebb295c8ceb8ae87ffbcce48e8259a1faedcf18d666
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006610"
---
# <a name="windows-media-format-sdk-structures"></a>Windows Medienformat-SDK-Strukturen

Das Windows Media Format SDK implementiert die folgenden Strukturen.



| Struktur                                                                                | Beschreibung                                                                                                                                                               |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DRM \_ COPY \_ OPL**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_copy_opl)                                                   | Enthält Informationen zur Schutzebene der Ausgabe, die für die Kopieraktion in einer DRM-Lizenz gelten.                                                                               |
| [**\_ \_ DRM-LIZENZSTATUSDATEN \_**](drm-license-state-data.md)                              | Enthält [*Lizenzinformationen*](wmformat-glossary.md) zu einem angegebenen [*DRM-Recht.*](wmformat-glossary.md) |
| [**MINIMALE \_ \_ DRM-AUSGABESCHUTZEBENEN \_ \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_minimum_output_protection_levels) | Enthält mindeste Ausgabeschutzebenen, die für eine DRM-Lizenz erforderlich sind, um Inhalte in verschiedenen Formaten wieder zu spielen.                                                                      |
| [**DRM \_ \_ \_ OPL-AUSGABE-IDs**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_opl_output_ids)                                      | Enthält ein Array von DRM-Technologiebezeichnern. Diese Struktur wird verwendet, um Gruppen von Technologien in anderen DRM-Strukturen zu definieren.                                            |
| [**DRM \_ PLAY \_ OPL**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_play_opl)                                                   | Enthält Informationen zur Schutzebene der Ausgabe, die für die Wiedergabeaktion in einer DRM-Lizenz gelten.                                                                               |
| [**\_INHALTS-ID DER DRM-WIEDERGABELISTE \_ \_**](drm-playlist-content-id.md)                            | Enthält Informationen zu Inhalten, die im Rahmen eines Wiedergabelisten-Burnings auf CD kopiert werden sollen.                                                                                 |
| [**DRM \_ VAL16**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-drm_val16)                                                          | Speichert einen 128-Bit-Wert, der als Gerätebezeichner verwendet wird.                                                                                                                       |
| [**\_ \_ DRM-VIDEOAUSGABESCHUTZ \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_output_protection)                    | Enthält den Bezeichner einer Videoschutztechnologie und die für diese Technologie erforderlichen Konfigurationsdaten.                                                             |
| [**\_ \_ \_ DRM-VIDEOAUSGABESCHUTZ-IDS \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_video_output_protection_ids)           | Enthält ein Array von **DRM \_ VIDEO OUTPUT \_ \_ PROTECTION-Strukturen.**                                                                                                          |
| [**WAVEFORMATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85))                                                | Definiert das Format von Waveform-Audiodaten.                                                                                                                                |
| [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85))                                | Definiert das Format von Waveform-Audiodaten für Formate mit mehr als zwei Kanälen.                                                                                      |
| [**WM \_ ADDRESS \_ ACCESSENTRY**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_address_accessentry)                               | Gibt einen Eintrag in einer IP-Adresszugriffsliste an.                                                                                                                          |
| [**\_ \_ WM-CLIENTEIGENSCHAFTEN**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_client_properties)                                   | Zeichnet Informationen zum Client auf.                                                                                                                                     |
| [**WM \_ CLIENT \_ PROPERTIES \_ EX**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_client_properties_ex)                            | Zeichnet erweiterte Informationen zum Client auf.                                                                                                                            |
| [**WM \_ GET \_ LICENSE \_ DATA**](wm-get-license-data.md)                                    | Enthält Informationen zu einer DRM-Lizenz.                                                                                                                                 |
| [**WM \_ INDIVIDUALIZE \_ STATUS**](wm-individualize-status.md)                             | Zeichnet den Status des [*Individualisierungsprozesses*](wmformat-glossary.md) auf.                                                                |
| [**WM \_ LEAKY \_ BUCKET \_ PAIR**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_leaky_bucket_pair)                                  | Beschreibt die Pufferanforderungen für eine VBR-Datei (Variable Bit Rate).                                                                                                  |
| [**\_ \_ WM-LIZENZSTATUSDATEN \_**](/previous-versions/windows/desktop/legacy/dd757942(v=vs.85))                                | Kapselt eine [**DRM \_ LICENSE STATE \_ \_ DATA-Struktur,**](drm-license-state-data.md) die DRM-Lizenzstatusdaten beschreibt.                                              |
| [**\_ \_ WM-MEDIENTYP**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type)                                                 | Beschreibt ein Medienbeispiel.                                                                                                                                                 |
| [**WMMPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmmpeg2videoinfo)                                             | Beschreibt einen MPEG-2-Videostream.                                                                                                                                         |
| [**\_WM-BILD**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture)                                                        | Enthält die Daten für das [**komplexe WM/Picture-Metadatenattribut.**](wmpicture.md)                                                                                     |
| [**\_ \_ WM-PORTNUMMERBEREICH \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_port_number_range)                                  | Beschreibt den Portnummernbereich, der von der **IWMReaderNetworkConfig-Schnittstelle verwendet** wird.                                                                                     |
| [**WM \_ READER \_ CLIENTINFO**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_clientinfo)                                   | Beschreibt den Clientreader (Player), der auf den Medienstream zutritt.                                                                                                          |
| [**WM \_ READER \_ STATISTICS**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics)                                   | Beschreibt die Leistung eines Lesevorgang.                                                                                                                         |
| [**WMSCRIPTFORMAT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmscriptformat)                                                 | Definiert das Format eines Skriptstreams.                                                                                                                                    |
| [**WM \_ STREAM \_ PRIORITY \_ RECORD**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_priority_record)                        | Enthält eine Streamnummer und gibt an, ob die Übermittlung dieses Streams obligatorisch ist.                                                                                      |
| [**WM \_ STREAM \_ TYPE \_ INFO**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_type_info)                                    | Enthält die Daten für das [**komplexe Metadatenattribut WM/StreamTypeInfo.**](wm-streamtypeinfo.md)                                                                      |
| [**WM \_ \_ SYNCHRONISED-SYNCHRONISIERUNGS-SYNCHRONISIERUNGEN**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_synchronised_lyrics)                               | Enthält die Daten für das [**komplexe Metadatenattribut WM/Synchronisierungssynchronisierung. \_**](wm-lyrics-synchronised.md)                                                           |
| [**\_ \_ WM-BENUTZERTEXT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_user_text)                                                   | Enthält die Daten für das [**komplexe WM/Text-Metadatenattribut.**](wm-text.md)                                                                                          |
| [**\_ \_ WM-BENUTZER-WEB-URL \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_user_web_url)                                            | Enthält die Daten für das [**komplexe Metadatenattribut WM/UserWebURL.**](wm-userweburl.md)                                                                              |
| [**WM \_ WRITER \_ STATISTICS**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics)                                   | Beschreibt die Leistung eines Schreibvorgang.                                                                                                                         |
| [**WM \_ WRITER \_ STATISTICS \_ EX**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics_ex)                            | Enthält erweiterte Writerstatistiken.                                                                                                                                      |
| [**WMDRM \_ IMPORT \_ CONTENT \_ KEY**](wmdrm-import-content-key.md)                          | Enthält den Inhaltsschlüssel, der beim Importieren geschützter Inhalte verwendet wird.                                                                                                                |
| [**WMDRM \_ IMPORT \_ \_ INIT-STRUKTUR**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct)                          | Enthält den verschlüsselten Sitzungsschlüssel und Inhaltsschlüssel, der beim Importieren geschützter Inhalte verwendet wird.                                                                                      |
| [**WMDRM \_ IMPORT \_ SESSION \_ KEY**](wmdrm-import-session-key.md)                          | Enthält den Sitzungsschlüssel zum Importieren geschützter Inhalte.                                                                                                                    |
| [**WMT \_ BUFFER \_ SEGMENT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_buffer_segment)                                       | Enthält die Informationen, die zum Angeben eines Segments in einem Paket erforderlich sind.                                                                                                      |
| [**WMT \_ \_ COLORSPACEINFO-ERWEITERUNGSDATEN \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_colorspaceinfo_extension_data)        | Enthält die Daten für die Dateneinheitserweiterung WM \_ SampleExtensionGUID \_ ColorSpaceInfo.                                                                                    |
| [**WMT \_ FILESINK \_ DATA \_ UNIT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_filesink_data_unit)                              | Enthält Informationen zu einem Paket.                                                                                                                                      |
| [**\_WMT-NUTZLASTFRAGMENT \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_payload_fragment)                                   | Enthält die Informationen, die zum Extrahieren eines Nutzlastfragments aus einem Paket erforderlich sind.                                                                                           |
| [**WMT \_ TIMECODE \_ EXTENSION \_ DATA**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data)                    | Enthält einen einzelnen SMPTE-Zeitcode und zugehörige Informationen.                                                                                                                |
| [**WMT \_ VIDEOIMAGE \_ SAMPLE**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample)                                 | Enthält Informationen zu einem Videobildbeispiel.                                                                                                                          |
| [**\_ \_ WMT-WASSERZEICHENEINTRAG**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_watermark_entry)                                     | Enthält Informationen zu einem Wasserzeichensystem.                                                                                                                         |
| [**WMT \_ WEBSTREAM \_ FORMAT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format)                                   | Enthält Informationen zu einem Webstream.                                                                                                                                  |
| [**\_ \_ WMT-WEBSTREAM-BEISPIELHEADER \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_sample_header)                    | Enthält Headerinformationen für Webstreambeispiele.                                                                                                                       |
| [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader)                                           | Beschreibt die Bitmap- und Farbinformationen für ein Videobild.                                                                                                             |
| [**WMVIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader2)                                         | Beschreibt die Bitmap- und Farbinformationen für ein Videobild, einschließlich [*Interlace,*](wmformat-glossary.md)Kopierschutz und Seitenverhältnis.       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierverzeichnis**](programming-reference.md)
</dt> </dl>

 

 
