---
description: Bitmap-Header Typen
ms.assetid: 6df4655a-f707-4893-b6e6-f7e4d7f67b4e
title: Bitmap-Header Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5910b0fb5be1166e807db1f3362186a206abc2b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863688"
---
# <a name="bitmap-header-types"></a>Bitmap-Header Typen

Die Bitmap verfügt über vier grundlegende Header Typen:

-   [**BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader)
-   [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85))
-   [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)
-   [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header)

Die vier Typen von bitmapheadern unterscheiden sich durch den **size** -Member, bei dem es sich um das erste **DWORD** in den einzelnen Strukturen handelt.

Die [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) -Struktur ist eine erweiterte [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header) -Struktur, bei der es sich um eine erweiterte [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) -Struktur handelt. Allerdings verfügen **BITMAPINFOHEADER** und [**BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader) nur über das **Größen** Element, das gemeinsam mit anderen Bitmap-Header Strukturen vorhanden ist.

Die Formate " [**BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader) " und " [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header) " wurden durch die Formate " [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) " bzw. " [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) " abgelöst. Die Formate " **BITMAPCOREHEADER** " und " **BITMAPV4HEADER** " werden aus Gründen der Vollständigkeit und Abwärtskompatibilität dargestellt.

Das Format für einen DIB lautet wie folgt (Weitere Informationen finden Sie unter [Bitmap-Speicher](bitmap-storage.md) ):

-   eine [**BITMAPFILEHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader) -Struktur
-   entweder ein [**BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader), eine [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85))-, eine [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)-oder [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) -Struktur.
-   eine optionale Farbtabelle, bei der es sich entweder um einen Satz von [**rgbquad**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) -Strukturen oder eine Reihe von [**rgbtriple**](/windows/win32/api/wingdi/ns-wingdi-rgbtriple) -Strukturen handelt.
-   die Bitmapdaten
-   optionale Profildaten

In einer Farbtabelle wird beschrieben, wie Pixelwerte RGB-Farbwerten entsprechen. RGB ist ein Modell zum Beschreiben von Farben, die durch Ausgeben von Licht erzeugt werden.

*Profildaten* beziehen sich entweder auf den Namen der Profil Datei (verknüpftes Profil) oder die tatsächlichen Profil Bits (eingebettetes Profil). Das Dateiformat speichert die Profildaten am Ende der Datei. Die Profildaten werden direkt hinter der Farbtabelle platziert (sofern vorhanden). Wenn die Funktion jedoch ein gepacktes DIB empfängt, werden die Profildaten nach den Bitmapbits angezeigt, wie im Dateiformat.

Profildaten sind nur für [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) -Strukturen vorhanden, bei denen **bV5CSType** ein Profil \_ verknüpft ist oder das Profil eingebettet ist \_ . Bei Funktionen, die gepackte Disb empfangen, werden die Profildaten nach den Bitmapdaten angezeigt.

Ein palettengerät ist ein beliebiges Gerät, das Paletten zum Zuweisen von Farben verwendet. Das klassische Beispiel eines Paletten-Geräts ist eine Anzeige, die in 8-Bit-Farbtiefe (256 Farben) ausgeführt wird. Die Anzeige in diesem Modus verwendet eine kleine Farbtabelle, um einer Bitmap Farben zuzuweisen. Die Farben in einer Bitmap werden der nächstgelegenen Farbe in der Palette zugewiesen, die vom Gerät verwendet wird. Das palettengerät erstellt keine optimale Palette zum Anzeigen der Bitmap. Es verwendet einfach alle in der aktuellen Palette vorhandenen. Anwendungen sind dafür verantwortlich, eine Palette zu erstellen und im System auszuwählen. Im Allgemeinen enthalten 16-, 24-und 32-Bit-pro-Pixel-Bitmaps (BPP) keine Farbtabellen (auch als optimale Paletten für die Bitmap); in diesem Fall ist die Anwendung dafür verantwortlich, eine optimale Palette zu erzeugen. Allerdings können 16-, 24-und 32-bpp-Bitmaps solche optimalen Farbtabellen für die Anzeige auf Paletten-Geräten enthalten. in diesem Fall muss die Anwendung nur eine Palette erstellen, die auf der in der Bitmapdatei vorhandenen Farbtabelle basiert.

Bitmaps, die 1, 4 oder 8 bpp sind, müssen eine Farbtabelle mit einer maximalen Größe aufweisen, die auf dem bpp basiert. Die maximale Größe für 1, 4 und 8 bpp-Bitmaps liegt zwischen 2 und der Leistungsfähigkeit des bpp. Folglich hat eine 1 bpp-Bitmap maximal zwei Farben, die 4 bpp-Bitmap höchstens 16 Farben und die 8 bpp-Bitmap maximal 256 Farben.

Bitmaps, die 16-, 24-oder 32-bpp sind, erfordern keine Farbtabellen, können aber möglicherweise Farben für Paletten-Geräte angeben. Wenn eine Farbtabelle für eine 16-, 24-oder 32-bpp-Bitmap vorhanden ist, gibt der **biclrused** -Member die Größe der Farbtabelle an, und die Farbtabelle muss die Zahl der Farben enthalten. Wenn **biclrused** gleich 0 (null) ist, gibt es keine Farbtabelle.

Die roten, grünen und blauen Bitfeld Masken für BI \_ Bitfeld-Bitmaps folgen direkt den [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85))-, [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)-und [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) -Strukturen. Die **BITMAPV4HEADER** -und **BITMAPV5HEADER** -Strukturen enthalten zusätzliche Member für rote, grüne und blaue Masken wie folgt.



| Member        | Bedeutung                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------|
| **Redmask**   | Farbmaske, die die rote Komponente jedes Pixels angibt. diese ist nur gültig, wenn das **Komprimierungs** Element auf BI Bitfields festgelegt ist \_ .   |
| **Greenmask** | Farbmaske, die die grüne Komponente der einzelnen Pixel angibt. diese ist nur gültig, wenn das **Komprimierungs** Element auf BI Bitfields festgelegt ist \_ . |
| **Bluemask**  | Farbmaske, die die blaue Komponente der einzelnen Pixel angibt. diese ist nur gültig, wenn das **Komprimierungs** Element auf BI Bitfields festgelegt ist \_ .  |



 

Wenn das **bicompression** -Element von [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) auf BI Bitfields festgelegt ist \_ und die Funktion ein Argument vom Typ **lpbitmapinfo** empfängt, folgen die Farb Masken sofort dem Header. Die Farbtabelle folgt, falls vorhanden, den Farb Masken. [**BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader) -Bitmaps unterstützen keine Farb Masken.

Standardmäßig werden Bitmapdaten im zugehörigen Format im Format angezeigt. "Bottom-up" bedeutet, dass die erste Scan Zeile in den Bitmapdaten die letzte Überprüfungs Zeile ist, die angezeigt werden soll. Beispielsweise ist das 0<sup>.</sup> Pixel der 0<sup>.</sup> Scanzeile der Bitmapdaten einer 10-Pixel-Bitmap mit 10 Pixel<sup>das 0-</sup> fache Pixel der 9<sup>.</sup> Überprüfungs Zeile des angezeigten oder gedruckten Bilds. Bitmaps und [**BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader) -Bitmaps können nicht von oben nach unten ausgeführt werden. Die Überprüfungs Linien sind mit Ausnahme von RLE-komprimierten Bitmaps **DWORD** -bündig ausgerichtet. Sie müssen für die Überprüfung von Zeilen breiten in Byte aufgefüllt werden, die nicht gleichmäßig durch vier, außer für die-komprimierten Bitmaps, angezeigt werden. Beispielsweise weist eine 10-fache 24-bpp-Bitmap zwei Auffüll Bytes am Ende jeder Scan Zeile auf.

 

 
