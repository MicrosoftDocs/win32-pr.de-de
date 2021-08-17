---
description: Die folgenden Funktionen werden mit Bitmaps verwendet.
ms.assetid: ef3abc8a-5d95-41d0-8eb6-47719d472414
title: Bitmapfunktionen (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 454cc4d23cceaeddd8abe9aaf9a5a7cc522345bedfe12a10e8e114c5dde46d8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119400460"
---
# <a name="bitmap-functions-windows-gdi"></a>Bitmapfunktionen (Windows GDI)

Die folgenden Funktionen werden mit Bitmaps verwendet.



| Funktion                                                 | BESCHREIBUNG                                                    |
|----------------------------------------------------------|----------------------------------------------------------------|
| [**AlphaBlend**](/windows/desktop/api/WinGdi/nf-wingdi-alphablend)                         | Zeigt eine Bitmap mit transparenten oder halbtransparenten Pixeln an.  |
| [**Bitblt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt)                                 | Führt eine Bitblockübertragung durch.                                 |
| [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap)                     | Erstellt eine Bitmap.                                              |
| [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect)     | Erstellt eine Bitmap.                                              |
| [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) | Erstellt eine Bitmap, die mit einem Gerät kompatibel ist.                     |
| [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)                 | Erstellt eine geräteabhängige Bitmap (DDB) aus einem DIB.            |
| [**CreateDIBSection**](/windows/desktop/api/Wingdi/nf-wingdi-createdibsection)             | Erstellt ein DIB, in das Anwendungen direkt schreiben können.         |
| [**ExtFloodFill**](/windows/desktop/api/Wingdi/nf-wingdi-extfloodfill)                     | Füllt einen Bereich der Anzeigeoberfläche mit dem aktuellen Pinsel aus.   |
| [**GetBitmapDimensionEx**](/windows/desktop/api/Wingdi/nf-wingdi-getbitmapdimensionex)     | Ruft die Dimensionen einer Bitmap ab.                               |
| [**GetDIBColorTable**](/windows/desktop/api/Wingdi/nf-wingdi-getdibcolortable)             | Ruft RGB-Farbwerte aus einer DIB-Abschnittbitmap ab.          |
| [**GetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-getdibits)                           | Kopiert eine Bitmap in einen Puffer.                                 |
| [**GetPixel**](/windows/desktop/api/Wingdi/nf-wingdi-getpixel)                             | Ruft den RGB-Farbwert des Pixels an einer angegebenen Koordinate ab.   |
| [**GetStretchBltMode**](/windows/desktop/api/Wingdi/nf-wingdi-getstretchbltmode)           | Ruft den aktuellen Stretchingmodus ab.                              |
| [**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill)                     | Füllt Rechteck- und Dreiecksstrukturen aus.                       |
| [**LoadBitmap**](/windows/desktop/api/Winuser/nf-winuser-loadbitmapa)                         | Lädt eine Bitmap aus der ausführbaren Datei eines Moduls.                |
| [**MaskBlt**](/windows/desktop/api/Wingdi/nf-wingdi-maskblt)                               | Kombiniert die Farbdaten in den Quell- und Zielbitmaps. |
| [**PlgBlt**](/windows/desktop/api/Wingdi/nf-wingdi-plgblt)                                 | Führt eine Bitblockübertragung durch.                                 |
| [**SetBitmapDimensionEx**](/windows/desktop/api/Wingdi/nf-wingdi-setbitmapdimensionex)     | Legt die bevorzugten Dimensionen auf eine Bitmap fest.                     |
| [**SetDIBColorTable**](/windows/desktop/api/Wingdi/nf-wingdi-setdibcolortable)             | Legt RGB-Werte in einem DIB fest.                                      |
| [**SetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-setdibits)                           | Legt die Pixel in einer Bitmap mithilfe von Farbdaten aus einem DIB fest.       |
| [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice)           | Legt die Pixel in einem Rechteck mithilfe von Farbdaten aus einem DIB fest.    |
| [**SetPixel**](/windows/desktop/api/Wingdi/nf-wingdi-setpixel)                             | Legt die Farbe für ein Pixel fest.                                    |
| [**SetPixelV**](/windows/desktop/api/Wingdi/nf-wingdi-setpixelv)                           | Legt ein Pixel auf die beste Näherung einer Farbe fest.             |
| [**SetStretchBltMode**](/windows/desktop/api/Wingdi/nf-wingdi-setstretchbltmode)           | Legt den Bitmap-Stretchingmodus fest.                               |
| [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt)                         | Kopiert eine Bitmap und streckt oder komprimiert sie.                |
| [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits)                   | Kopiert die Farbdaten in ein DIB.                                |
| [**TransparentBlt**](/windows/desktop/api/WinGdi/nf-wingdi-transparentblt)                 | Führt eine Bitblockübertragung von Farbdaten durch.                   |



 

## <a name="obsolete-functions"></a>Veraltete Funktionen

Die folgenden Funktionen werden nur zur Kompatibilität mit 16-Bit-Versionen von Microsoft Windows bereitgestellt:

-   [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap)
-   [**FloodFill**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill)
-   [**GetBitmapBits**](/windows/desktop/api/Wingdi/nf-wingdi-getbitmapbits)
-   [**SetBitmapBits**](/windows/desktop/api/Wingdi/nf-wingdi-setbitmapbits)

 

 



