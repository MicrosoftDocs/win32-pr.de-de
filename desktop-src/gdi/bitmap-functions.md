---
description: Die folgenden Funktionen werden mit Bitmaps verwendet.
ms.assetid: ef3abc8a-5d95-41d0-8eb6-47719d472414
title: Bitmap-Funktionen (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05e61ef02f5065d746f0d82a7b3352c3445ebf61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994134"
---
# <a name="bitmap-functions-windows-gdi"></a>Bitmap-Funktionen (Windows GDI)

Die folgenden Funktionen werden mit Bitmaps verwendet.



| Funktion                                                 | BESCHREIBUNG                                                    |
|----------------------------------------------------------|----------------------------------------------------------------|
| [**AlphaBlend**](/windows/desktop/api/WinGdi/nf-wingdi-alphablend)                         | Zeigt eine Bitmap mit transparenten oder semitransparenten Pixeln an.  |
| [**BitBLT**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt)                                 | Führt eine Bitblock Übertragung aus.                                 |
| [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap)                     | Erstellt eine Bitmap.                                              |
| [**Createbitmapindirect Memberfunktion**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect)     | Erstellt eine Bitmap.                                              |
| [**"Kreatecompatiblebitmap"**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) | Erstellt eine Bitmap, die mit einem Gerät kompatibel ist.                     |
| [**"Kreatedibitmap"**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)                 | Erstellt eine Geräte abhängige Bitmap (DDB) aus einem DIB.            |
| [**"Kreatedibsection"**](/windows/desktop/api/Wingdi/nf-wingdi-createdibsection)             | Erstellt ein DIB, in das Anwendungen direkt schreiben können.         |
| [**Extflufill**](/windows/desktop/api/Wingdi/nf-wingdi-extfloodfill)                     | Füllt einen Bereich der Anzeige Oberfläche mit dem aktuellen Pinsel.   |
| [**Getbitmapdimensionex**](/windows/desktop/api/Wingdi/nf-wingdi-getbitmapdimensionex)     | Ruft die Dimensionen einer Bitmap ab.                               |
| [**Getdibcolortable**](/windows/desktop/api/Wingdi/nf-wingdi-getdibcolortable)             | Ruft RGB-Farbwerte aus einer DIB-Abschnitts Bitmap ab.          |
| [**GetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-getdibits)                           | Kopiert eine Bitmap in einen Puffer.                                 |
| [**GetPixel**](/windows/desktop/api/Wingdi/nf-wingdi-getpixel)                             | Ruft den RGB-Farbwert des Pixels an einer angegebenen Koordinate ab.   |
| [**Getstretchbltmode**](/windows/desktop/api/Wingdi/nf-wingdi-getstretchbltmode)           | Ruft den aktuellen streckungs Modus ab.                              |
| [**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill)                     | Füllt Rechteck-und Dreieck Strukturen aus.                       |
| [**LoadBitmap**](/windows/desktop/api/Winuser/nf-winuser-loadbitmapa)                         | Lädt eine Bitmap aus der ausführbaren Datei eines Moduls.                |
| [**MaskBlt**](/windows/desktop/api/Wingdi/nf-wingdi-maskblt)                               | Kombiniert die Farbdaten in den Quell-und Ziel Bitmaps. |
| [**Plgblt**](/windows/desktop/api/Wingdi/nf-wingdi-plgblt)                                 | Führt eine Bitblock Übertragung aus.                                 |
| [**Setbitmapdimensionex**](/windows/desktop/api/Wingdi/nf-wingdi-setbitmapdimensionex)     | Legt die bevorzugten Dimensionen auf eine Bitmap fest.                     |
| [**Setdibcolortable**](/windows/desktop/api/Wingdi/nf-wingdi-setdibcolortable)             | Legt RGB-Werte in einem DIB fest.                                      |
| [**SetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-setdibits)                           | Legt die Pixel in einer Bitmap mithilfe von Farbdaten aus einem DIB fest.       |
| [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice)           | Legt die Pixel in einem Rechteck mithilfe von Farbdaten aus einem DIB fest.    |
| [**SetPixel**](/windows/desktop/api/Wingdi/nf-wingdi-setpixel)                             | Legt die Farbe für ein Pixel fest.                                    |
| [**Setpixelv**](/windows/desktop/api/Wingdi/nf-wingdi-setpixelv)                           | Legt ein Pixel auf die beste Näherung einer Farbe fest.             |
| [**Setstretchbltmode**](/windows/desktop/api/Wingdi/nf-wingdi-setstretchbltmode)           | Legt den Modus für die Bitmap-Streckung fest.                               |
| [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt)                         | Kopiert eine Bitmap und dehnt sie aus bzw. komprimiert Sie.                |
| [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits)                   | Kopiert die Farbdaten in einem DIB.                                |
| [**TransparentBlt**](/windows/desktop/api/WinGdi/nf-wingdi-transparentblt)                 | Führt eine Bitblock Übertragung von Farbdaten aus.                   |



 

## <a name="obsolete-functions"></a>Veraltete Funktionen

Die folgenden Funktionen werden nur für die Kompatibilität mit 16-Bit-Versionen von Microsoft Windows bereitgestellt:

-   [**"Kreateverwerdablebitmap"**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap)
-   [**Auffüllen**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill)
-   [**Getbitmapbits**](/windows/desktop/api/Wingdi/nf-wingdi-getbitmapbits)
-   [**Setbitmapbits**](/windows/desktop/api/Wingdi/nf-wingdi-setbitmapbits)

 

 



