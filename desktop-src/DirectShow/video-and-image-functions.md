---
description: Video- und Bildfunktionen
ms.assetid: 02401edc-362b-4f6c-b10b-c46b30b3ebe7
title: Video- und Bildfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ab4b57f804c1da1e4a6da0ca4625e3503ed9987077a80f1f98dde91cf2e27f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119432120"
---
# <a name="video-and-image-functions"></a>Video- und Bildfunktionen

Diese Funktionen und Makros bearbeiten die DirectShow-Videoformatstrukturen.



| Funktion                                                             | Beschreibung                                                                                                                                                       |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BIT \_ MASKS \_ MATCH**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-bit_masks_match)                         | Vergleicht die Farbmasken für zwei [**VIDEOINFO-Strukturen.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)                                                                                       |
| [**Bitmasken**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-bitmasks)                                         | Ruft die Farbmasken aus einer [**VIDEOINFO-Struktur**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) ab.                                                                                         |
| [**CheckVideoInfoType**](checkvideoinfotype.md)                     | Überprüft einen Medientyp, der eine [**VIDEOINFOHEADER-Formatstruktur**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) enthält, auf Fehler, die Pufferüberläufe oder Ganzzahlüberläufe verursachen können.   |
| [**CheckVideoInfo2Type**](checkvideoinfo2type.md)                   | Überprüft einen Medientyp, der eine [**VIDEOINFOHEADER2-Formatstruktur**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) enthält, auf Fehler, die Pufferüberläufe oder Ganzzahlüberläufe verursachen können. |
| [**Farben**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-colors)                                             | Ruft die Paletteneinträge aus einer [**VIDEOINFO-Struktur**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) ab.                                                                                     |
| [**ContainsPalette**](containspalette.md)                           | Bestimmt, ob eine angegebene [**VIDEOINFOHEADER-Struktur**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) eine Palette enthält.                                                           |
| [**ConvertVideoInfoToVideoInfo2**](convertvideoinfotovideoinfo2.md) | Konvertiert einen Medientyp, der [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) verwendet, in einen Medientyp, der [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) verwendet.                          |
| [**DIBSIZE**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-dibsize)                                           | Berechnet die Anzahl der Bytes, die von einer geräteunabhängigen Bitmap (DIB) benötigt werden.                                                                                     |
| [**GetBitCount**](getbitcount.md)                                   | Gibt die Anzahl der Bits pro Pixel zurück, die von einem angegebenen Videountertyp verwendet werden.                                                                                           |
| [**GetBitmapFormatSize**](getbitmapformatsize.md)                   | Berechnet die erforderliche Größe für eine [**VIDEOINFO-Struktur,**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) die eine angegebene [**BITMAPINFOHEADER-Struktur**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) enthalten kann.       |
| [**GetBitmapPalette**](getbitmappalette.md)                         | Gibt den ersten Paletteneintrag in einer [**VIDEOINFOHEADER-Struktur**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) zurück.                                                                        |
| [**GetBitmapSize**](getbitmapsize.md)                               | Berechnet die Anzahl der Bytes, die von einer geräteunabhängigen Bitmap (DIB) benötigt werden.                                                                                     |
| [**GetBitmapSubtype**](getbitmapsubtype.md)                         | Gibt die **Medienuntertyp-GUID** für die angegebene Bitmap zurück.                                                                                                      |
| [**GetSubtypeName**](getsubtypename.md)                             | Ruft den für Menschen lesbaren Namen eines Videountertyps ab.                                                                                                             |
| [**GetTrueColorType**](gettruecolortype.md)                         | Gibt die **Medienuntertyp-GUID** für eine nicht komprimierte 16-Bit-RGB-Bitmap zurück.                                                                                          |
| [**Header**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-header)                                             | Gibt die Adresse des [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) in einem [**VIDEOINFOHEADER zurück.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)                                      |
| [**MPEG1 \_ SEQUENCE \_ INFO**](/previous-versions/windows/desktop/api/amvideo/nf-amvideo-mpeg1_sequence_info)                 | Gibt die Adresse des Sequenzheaders innerhalb einer [**MPEG1VIDEOINFO-Struktur**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) zurück.                                                          |
| [**PALETTISIERT**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-palettised)                                     | Überprüft, ob eine Bitmap eine Farbtiefe von mindestens 8 Bit auf hat.                                                                                                      |
| [**\_PALETTENEINTRÄGE**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-palette_entries)                          | Ruft die maximale Anzahl von Farben in der Palette einer angegebenen Bitmap ab.                                                                                      |
| [**ZURÜCKSETZEN \_ VON MASKEN**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-reset_masks)                                  | Füllt die Farbmaskenfelder in einer [**VIDEOINFO-Struktur**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) mit Nullen auf.                                                                            |
| [**RESET \_ HEADER**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-reset_header)                                | Füllt einen [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) mit Nullen.                                                                                                   |
| [**PALETTE \_ ZURÜCKSETZEN**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-reset_palette)                              | Füllt die Paletteneinträge in einer [**VIDEOINFO-Struktur**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) mit Nullen auf.                                                                              |
| [**\_ \_ GRÖßEN-EGA-PALETTE**](/previous-versions/windows/desktop/legacy/dd377602(v=vs.85))                       | Berechnet die erforderliche Größe für die Paletteneinträge in einer 4-Bit-RGB-Bitmap.                                                                                         |
| [**\_GRÖßENMASKEN**](/previous-versions/windows/desktop/legacy/dd377603(v=vs.85))                                    | Berechnet die Größe der Farbmasken in einer [**VIDEOINFO-Struktur.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)                                                                             |
| [**SIZE \_ MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-size_mpeg1videoinfo)                  | Berechnet die Größe einer [**MPEG1VIDEOINFO-Struktur,**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) einschließlich des Sequenzheaders.                                                      |
| [**\_GRÖßENPALETTE**](/previous-versions/windows/desktop/legacy/dd377605(v=vs.85))                                | berechnet die Größe der Paletteneinträge in einer [**VIDEOINFO-Struktur.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)                                                                         |
| [**SIZE \_ PREHEADER**](/previous-versions/windows/desktop/legacy/dd377606(v=vs.85))                            | Berechnet den Byteoffset des **bmiHeader-Felds** innerhalb einer [**VIDEOINFOHEADER-Struktur.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)                                              |
| [**SIZE \_ VIDEOHEADER**](/previous-versions/windows/desktop/legacy/dd377607(v=vs.85))                        | Berechnet die Größe der [**VIDEOINFOHEADER-Struktur.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)                                                                                  |
| [**Truecolor**](/previous-versions/windows/desktop/legacy/dd407230(v=vs.85))                                   | Gibt die [**TRUECOLORINFO-Struktur**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-truecolorinfo) aus einer [**VIDEOINFO-Struktur**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) zurück.                                            |
| [**ValidateBitmapInfoHeader**](validatebitmapinfoheader.md)         | Überprüft eine [**BITMAPINFOHEADER-Struktur**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) auf Fehler, die Pufferüberläufe oder Ganzzahlüberläufe verursachen können.                                   |



 

## <a name="remarks"></a>Hinweise

Die meisten der im Abschnitt beschriebenen Makros und Funktionen sind für die Bearbeitung von **VIDEOINFOHEADER-** und **VIDEOINFO-Strukturen** für RGB-Bitmaps konzipiert. Verwenden Sie diese Makros mit Vorsicht: Die meisten von ihnen gehen davon aus, dass die angegebene Struktur ordnungsgemäß initialisiert wurde. Viele davon gehen auch davon aus, dass die **BITMAPINFOHEADER-Struktur** die Standardgröße ist. das heißt, `biSize == sizeof(BITMAPINFOHEADER)` .

Die DirectShow-Basisklassenbibliothek stellt auch die folgenden globalen Konstanten bereit, die die Standardfarbmasken für True-Color-Bitmaps definieren.



| Globale Daten | Beschreibung                                                   |
|-------------|---------------------------------------------------------------|
| **bits555** | Array von Farbmasken für eine 16-Bit-RGB-Bitmap im 5-5-5-Format. |
| **bits565** | Array von Farbmasken für eine 16-Bit-RGB-Bitmap im 5-6-5-Format. |
| **bits888** | Array von Farbmasken für eine 24-Bit-RGB-Bitmap.                 |



 

Jede dieser Konstanten in einem Array von drei **DWORD-S,** das die roten, grünen und blauen Masken in dieser Reihenfolge enthält.

 

 
