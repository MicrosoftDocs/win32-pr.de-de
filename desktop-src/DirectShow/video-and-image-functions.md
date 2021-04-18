---
description: Video-und Bildfunktionen
ms.assetid: 02401edc-362b-4f6c-b10b-c46b30b3ebe7
title: Video-und Bildfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c55e439a17dd570b6e939d1cb84d836f9100eaf7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345194"
---
# <a name="video-and-image-functions"></a>Video-und Bildfunktionen

Diese Funktionen und Makros bearbeiten die Format Strukturen des DirectShow-Videos.



| Funktion                                                             | BESCHREIBUNG                                                                                                                                                       |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Bitmasken \_ stimmen zu**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-bit_masks_match)                         | Vergleicht die Farb Masken für zwei [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) -Strukturen.                                                                                       |
| [**Bitmasken**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-bitmasks)                                         | Ruft die Farb Masken aus einer [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) -Struktur ab.                                                                                         |
| [**Checkvideoinfotype**](checkvideoinfotype.md)                     | Überprüft einen Medientyp, der eine [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Format Struktur für Fehler enthält, die Pufferüberläufe oder ganzzahlige über Läufe verursachen können.   |
| [**CheckVideoInfo2Type**](checkvideoinfo2type.md)                   | Überprüft einen Medientyp, der eine [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) -Format Struktur für Fehler enthält, die Pufferüberläufe oder ganzzahlige über Läufe verursachen können. |
| [**Ellen**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-colors)                                             | Ruft die Paletteneinträge aus einer [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) -Struktur ab.                                                                                     |
| [**Containspalette**](containspalette.md)                           | Bestimmt, ob eine angegebene [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur eine Palette enthält.                                                           |
| [**ConvertVideoInfoToVideoInfo2**](convertvideoinfotovideoinfo2.md) | Konvertiert einen Medientyp, der [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) verwendet, in einen, der [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) verwendet.                          |
| [**Dibsize**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-dibsize)                                           | Berechnet die Anzahl der Bytes, die für eine geräteunabhängige Bitmap (DIB) erforderlich sind.                                                                                     |
| [**Getbitcount**](getbitcount.md)                                   | Gibt die Anzahl der Bits pro Pixel zurück, die von einem angegebenen Video Untertyp verwendet werden.                                                                                           |
| [**Getbitmapformatsize**](getbitmapformatsize.md)                   | Berechnet die für eine [**videinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) -Struktur benötigte Größe, die eine angegebene [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur enthalten kann.       |
| [**GetBitmapPalette**](getbitmappalette.md)                         | Gibt den ersten Paletteneintrag in einer [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur zurück.                                                                        |
| [**Getbitmapsize**](getbitmapsize.md)                               | Berechnet die Anzahl der Bytes, die für eine geräteunabhängige Bitmap (DIB) erforderlich sind.                                                                                     |
| [**Getbitmapsubtype**](getbitmapsubtype.md)                         | Gibt die **GUID** des Medien Untertyps für die angegebene Bitmap zurück.                                                                                                      |
| [**Getsubtypame**](getsubtypename.md)                             | Ruft den lesbaren Namen eines Video Untertyps ab.                                                                                                             |
| [**Gettruecolortype**](gettruecolortype.md)                         | Gibt die **GUID** des Medien Untertyps für eine unkomprimierte 16-Bit-RGB-Bitmap zurück.                                                                                          |
| [**Header**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-header)                                             | Gibt die Adresse des [**bitmapinfoheaders**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) in einem [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)zurück.                                      |
| [**MPEG1- \_ Sequenz \_ Informationen**](/previous-versions/windows/desktop/api/amvideo/nf-amvideo-mpeg1_sequence_info)                 | Gibt die Adresse des Sequenz Headers innerhalb einer [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) -Struktur zurück.                                                          |
| [**Palettisiert**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-palettised)                                     | Überprüft, ob eine Bitmap eine Farbtiefe von 8 Bits oder weniger aufweist.                                                                                                      |
| [**\_Paletteneinträge**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-palette_entries)                          | Ruft die maximale Anzahl von Farben in der Palette einer angegebenen Bitmap ab.                                                                                      |
| [**Masken zurücksetzen \_**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-reset_masks)                                  | Füllt die Farbmasken Felder in einer [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) -Struktur mit Nullen.                                                                            |
| [**Header zurücksetzen \_**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-reset_header)                                | Füllt einen [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) mit Nullen.                                                                                                   |
| [**Palette zurücksetzen \_**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-reset_palette)                              | Füllt die Paletteneinträge in einer [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) -Struktur mit Nullen.                                                                              |
| [**Größe der \_ EGA- \_ Palette**](/previous-versions/windows/desktop/legacy/dd377602(v=vs.85))                       | Berechnet die Größe, die für die Paletteneinträge in einer 4-Bit-RGB-Bitmap benötigt wird.                                                                                         |
| [**Größen \_ Masken**](/previous-versions/windows/desktop/legacy/dd377603(v=vs.85))                                    | Berechnet die Größe der Farb Masken in einer [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) -Struktur.                                                                             |
| [**Größe \_ MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-size_mpeg1videoinfo)                  | Berechnet die Größe einer [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) -Struktur, einschließlich des Sequenz Headers.                                                      |
| [**\_Palettengröße**](/previous-versions/windows/desktop/legacy/dd377605(v=vs.85))                                | berechnet die Größe der Paletteneinträge in einer [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) -Struktur.                                                                         |
| [**SIZE- \_ preheader**](/previous-versions/windows/desktop/legacy/dd377606(v=vs.85))                            | Berechnet den Byte Offset des **bmiheader** -Felds innerhalb einer [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur.                                              |
| [**\_Video Header Größe**](/previous-versions/windows/desktop/legacy/dd377607(v=vs.85))                        | Berechnet die Größe der [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur.                                                                                  |
| [**TrueColor**](/previous-versions/windows/desktop/legacy/dd407230(v=vs.85))                                   | Gibt die [**truecolorinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-truecolorinfo) -Struktur aus einer [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) -Struktur zurück.                                            |
| [**Validatebitmapinfoheader**](validatebitmapinfoheader.md)         | Überprüft eine [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur auf Fehler, die Pufferüberläufe oder ganzzahlige über Läufe verursachen können.                                   |



 

## <a name="remarks"></a>Bemerkungen

Die meisten Makros und Funktionen, die im Abschnitt beschrieben werden, sind für die Bearbeitung von **videoinfoheader** -und **videoinfo** -Strukturen für RGB-Bitmaps konzipiert. Verwenden Sie diese Makros mit Vorsicht: bei den meisten davon wird davon ausgegangen, dass die angegebene Struktur ordnungsgemäß initialisiert wurde. Viele davon gehen auch davon aus, dass die **BITMAPINFOHEADER** -Struktur die Standardgröße ist. Das heißt `biSize == sizeof(BITMAPINFOHEADER)` .

Die DirectShow-Basisklassen Bibliothek bietet auch die folgenden globalen Konstanten, die die Standard Farb Masken für True-Color-Bitmaps definieren.



| Globale Daten | BESCHREIBUNG                                                   |
|-------------|---------------------------------------------------------------|
| **bits555** | Array von Farb Masken für eine 16-Bit-RGB-Bitmap im 5-5-5-Format. |
| **bits565** | Array von Farb Masken für eine 16-Bit-RGB-Bitmap im 5-6-5-Format. |
| **bits888** | Array von Farb Masken für eine 24-Bit-RGB-Bitmap.                 |



 

Jede dieser Konstanten in einem Array von drei **DWORD** s, das die roten, grünen und blauen Masken in dieser Reihenfolge enthält.

 

 
