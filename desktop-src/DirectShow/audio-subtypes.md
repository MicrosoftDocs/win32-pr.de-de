---
description: In den folgenden Tabellen sind Medien Untertyp-GUIDs für Audiodaten aufgeführt. Sofern zutreffend, listet jede Tabelle das entsprechende Formattag auf, das in mmreg. h deklariert ist.
ms.assetid: 55012be5-2d61-4d38-aab7-0c42f161f555
title: Audiountertypen
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82b9ccbe83a20f23976e506124c674119eee3a96
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481574"
---
# <a name="audio-subtypes"></a>Audiountertypen

In den folgenden Tabellen sind Medien Untertyp-GUIDs für Audiodaten aufgeführt. Sofern zutreffend, listet jede Tabelle das entsprechende Formattag auf, das in mmreg. h deklariert ist.

## <a name="uncompressed-audio-types"></a>Nicht komprimierte Audiotypen



| GUID                          | BESCHREIBUNG                | Header  | Entsprechendes Formattag                  |
|-------------------------------|----------------------------|---------|----------------------------------------|
| **mediasubtype \_ IEEE \_ float** | IEEE-Gleit Komma-Audiodaten. | UUIDs. h | **Welle \_ \_IEEE \_ float** (0x0003) formatieren |
| **mediasubtype \_ PCM**         | PCM-Audiodatei.                 | UUIDs. h | **Welle \_ Formatieren von \_ PCM** (0x0001)         |



 

## <a name="mpeg-4-and-aac-audio-types"></a>MPEG-4-und AAC-Audiotypen



| GUID                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | Header       | Entsprechendes Formattag                      |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|--------------------------------------------|
| **mediasubtype \_ MPEG \_ ADTs \_ AAC** | "Advanced audiocoding (AAC)"-Audiodatei im ADTs-Format (Audiodaten-Transport Datenstrom).<br/> Der Format Block ist eine [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur mit **wformattag** , die dem **Wave- \_ Format \_ MPEG \_ ADTs \_ AAC** entspricht.<br/> Die [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur gibt die Kern-AAC-LC-Samplingrate und die Anzahl von Kanälen an, bevor Sie vorhanden ist.<br/> Nach der [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur sind keine weiteren Daten erforderlich.<br/>                                                                                                                                                                 | wmcodecdsp. h | **Welle \_ Format \_ MPEG \_ ADTs \_ AAC** (0x1600) |
| **mediasubtype \_ MPEG \_ heaac**     | High-Efficiency Advanced audiocoding (HE-AAC)-Stream.<br/> Der Format Block ist eine [**heaacwaveformat**](/windows/win32/api/mmreg/ns-mmreg-heaacwaveformat) -Struktur.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | wmcodecdsp. h | **Welle \_ Format \_ MPEG \_ heaac** (0x1610)     |
| **mediasubtype \_ MPEG- \_ LoAs**      | MPEG-4-audiotransportstream mit einer Synchronisierungs Schicht (LoAs) und einer Multiplex Schicht (latm).<br/> Der Format Block ist eine [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur mit **wformattag** , die dem **Wave- \_ Format \_ MPEG \_ LoAs** entspricht.<br/> Die [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur gibt die Kern-AAC-LC-Samplingrate und die Anzahl der Kanäle an, bevor Sie die spektralen SBR-oder PS-Tools anwenden.<br/> Nach der [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur sind keine weiteren Daten erforderlich.<br/>                                                                                                                                                                                             | wmcodecdsp. h | **Welle \_ Formatieren von \_ MPEG- \_ LoAs** (0x1602)      |
| **Mediasubtype \_ RAW \_ AAC1**       | RAW-AAC.<br/> Der Format Block ist eine [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur mit **wformattag** , die dem **Wave \_ Format \_ RAW \_ AAC1** entspricht.<br/> Die [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur gibt die Samplingrate und die Anzahl der Kanäle im decodierten Audioformat an, nachdem SBR und PS-Tools, sofern vorhanden, angewendet wurden.<br/> Auf die [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur folgen zusätzliche Bytes, die die audiospecificconfig ()-Daten enthalten, wie durch ISO/IEC 14496-3 (MPEG-4-Audio) definiert. <br/> Die Länge der audiospecificconfig ()-Daten beträgt 2 Bytes für AAC-LC oder den-AAC mit impliziter Signalisierung von SBR/PS. Es sind mehr als 2 Bytes für den-AAC mit expliziten Signalisierung von SBR/PS verfügbar.<br/> | wmcodecdps. h | **Welle \_ Formatieren von \_ Rohdaten \_ AAC1** (0x00FF)       |



 

## <a name="dolby-audio-types"></a>Dolby-Audiotypen



| GUID                                | BESCHREIBUNG                                                                                                                                                                                                             | Header       | Entsprechendes Formattag                        |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|----------------------------------------------|
| **mediasubtype \_ Dolby \_ ddplus**     | Dolby Digital Plus-Audiodatei.                                                                                                                                                                                               | wmcodecdsp. h | –                                          |
| **Mediasubtype \_ Dolby \_ AC3**        | Dolby Digital-Audiodatei (AC-3).                                                                                                                                                                                             | ksuuids. h    | –                                          |
| **Mediasubtype \_ Dolby \_ AC3 \_ SPDIF** | Dolby AC-3 über S/PDIF.                                                                                                                                                                                                 | UUIDs. h      | **Welle \_ Format \_ Dolby \_ AC3 \_ SPDIF** (0x0092) |
| **mediasubtype \_ DVM**               | DVM AC-3-Codec. Wird beim Abspielen von AVI-Dateien mit Dolby Digital-Audiodatei verwendet.<br/> Der Format Block ist eine [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur mit dem Format-Tag, das dem **Wave- \_ Format \_ DVM** entspricht.<br/> | wmcodecdsp. h | **Welle \_ Format \_ DVM** (0x2000)               |
| **mediasubtype- \_ Rohdaten \_ Sport**        | AC-3 über S/PDIF; siehe Hinweise.                                                                                                                                                                                          | UUIDs. h      | **Welle \_ Formatieren von \_ \_ Sport** (0x0240)        |
| **Mediasubtype \_ SPDIF- \_ Tag \_ 241h**  | AC-3 über S/PDIF; siehe Hinweise.                                                                                                                                                                                          | UUIDs. h      | **Welle \_ Format \_ esst \_ AC3** (0x0241)         |



 

Verwenden Sie zum Angeben des aufgefüllten AC-3 den Untertyp **mediasubtype \_ Dolby \_ AC3 \_ SPDIF**, der dem Formattag 0x0092 (Wave \_ Format \_ Dolby \_ AC3 \_ SPDIF) entspricht. Die Werte 0x240 und 0x241 wurden auch verwendet, um die aufgefüllte AC-3 anzugeben, aber Microsoft fördert die Verwendung von 0x0092.

## <a name="miscellaneous-audio-types"></a>Verschiedene Audiotypen



| GUID                                | BESCHREIBUNG                                                                                                                                                                                                                                                                          | Header       | Entsprechendes Formattag           |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|---------------------------------|
| **Mediasubtype \_ DRM \_ -Audiodatei**        | Der Schutz von Audiodateien mit Digital Rights Management (DRM).                                                                                                                                                                                                                               | UUIDs. h      | **Welle \_ Formatieren von \_ DRM** (0x0009)  |
| **mediasubtype- \_ DTS**               | Digital Theater Systems (DTS)-Audiodatei.<br/> Der Format Block ist eine [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur, bei der das Format-Tag gleich dem **Wave- \_ Format ' \_ Unknown**' ist.<br/>                                                                                              | ksuuids. h    | –                             |
| **Mediasubtype \_ DTS2**              | Digital Theater Systems (DTS)-Audiodatei.<br/> Der Format Block ist eine [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur mit dem Format-Tag, das dem **Wave- \_ Format \_ DTS2** entspricht.<br/> Dieser Untertyp entspricht **mediasubtype \_ DTS** , verwendet jedoch ein anderes Formattag.<br/> | wmcodecdsp. h | **Welle \_ Format \_ DTS2** (0x2001) |
| **mediasubtype \_ DVD \_ LPCM \_ -Audiodatei**  | DVD-Audiodaten.                                                                                                                                                                                                                                                                      | ksuuids. h    | –                             |
| **Mediasubtype \_ MPEG1AudioPayload** | MPEG-1-audionutzlast.                                                                                                                                                                                                                                                                | UUIDs. h      | **Welle \_ Format \_ MPEG** (0x0050) |
| **Mediasubtype \_ MPEG1Packet**       | MPEG1-audiopaket.                                                                                                                                                                                                                                                                  | UUIDs. h      | –                             |
| **Mediasubtype \_ MPEG1Payload**      | MPEG1-audionutzlast.                                                                                                                                                                                                                                                                 | UUIDs. h      | –                             |
| **Mediasubtype \_ \_ -Audiodatei**      | MPEG-2-Audiodaten.                                                                                                                                                                                                                                                                   | ksuuids. h    | –                             |



 

## <a name="audio-format-tags"></a>Audioformattags

Das Feld " **wformattag** " in der Struktur " [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) " gibt den audioformattyp an. Bei Medien Beispielen handelt es sich im Allgemeinen um ganze Anzahl von Beispielen, die im Feld " **wbitspersample** " der Struktur " **WaveFormatEx** " angegeben sind. Dies gilt nicht unbedingt für MPEG-Audiobeispiele, die aus packetisiert-Streams stammen können und daher nicht notwendigerweise an Sample/Frame-Begrenzungen verpackt sind. Bei MPEG-Audiodaten ist der Zeitstempel in einem Medien Beispiel der Zeitstempel für den ersten Frame, dessen erstes Byte im Medien Beispiel enthalten ist.

Medien Untertypen werden für jedes **wformattag** wie folgt definiert:

-   Das data1-Unterfeld der Untertyp-GUID ist mit dem **wformattag** -Wert identisch.
-   Das Data 2-Feld ist 0 (null).
-   Das Data 3-Feld ist 0x0010.
-   Das Feld Data 4 ist 0x80, 0x00, 0x00, 0xAA, 0x00, 0x38, 0x9b, 0x71.

Daher ist für PCM-Audiodaten der Untertyp-GUID (in "UUIDs. h" als **mediasubtype \_ PCM** definiert):

`{00000001-0000-0010-8000-00AA00389B71}`

Mithilfe der Funktion " [**deateaudiomediatype**](createaudiomediatype.md) " kann eine " [**am \_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) "-Struktur aus einer **WaveFormatEx** -Struktur erstellt werden.

## <a name="obsolete-audio-types"></a>Veraltete Audiotypen

Die folgenden audiountertypen sind veraltet und sollten nicht verwendet werden:

-   **mediasubtype \_ MPEG \_ RAW \_ AAC**
-   **Mediasubtype \_ PCMAudioObsolete**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AM \_ - \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type)
</dt> <dt>

[Medientypen](media-types.md)
</dt> </dl>

 

