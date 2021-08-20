---
description: Bitmapheadertypen
ms.assetid: 6df4655a-f707-4893-b6e6-f7e4d7f67b4e
title: Bitmapheadertypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c88839947845cc45633cbc07b7c36aec727318c91910bfc277680b1946080531
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966410"
---
# <a name="bitmap-header-types"></a>Bitmapheadertypen

Die Bitmap verfügt über vier grundlegende Headertypen:

-   [**BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader)
-   [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85))
-   [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)
-   [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header)

Die vier Arten von Bitmapheadern unterscheiden sich durch den **Size-Member,** der das erste **DWORD** in jeder der -Strukturen ist.

Die [**BITMAPV5HEADER-Struktur**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) ist eine erweiterte [**BITMAPV4HEADER-Struktur,**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header) bei der es sich um eine erweiterte [**BITMAPINFOHEADER-Struktur**](/previous-versions//dd183376(v=vs.85)) handelt. **BitmapINFOHEADER** und [**BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader) haben jedoch nur den **Size-Member** gemeinsam mit anderen Bitmapheaderstrukturen.

Die [**Formate BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader) und [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header) wurden durch die Formate [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) bzw. [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) ersetzt. Die **Formate BITMAPCOREHEADER** und **BITMAPV4HEADER** werden aus Gründen der Vollständigkeit und Abwärtskompatibilität dargestellt.

Das Format für einen DIB ist wie folgt (weitere Informationen finden Sie unter [Bitmap Storage](bitmap-storage.md) ):

-   eine [**BITMAPFILEHEADER-Struktur**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader)
-   entweder ein [**BITMAPCOREHEADER,**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader)ein [**BITMAPINFOHEADER,**](/previous-versions//dd183376(v=vs.85))ein [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)oder eine [**BITMAPV5HEADER-Struktur.**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header)
-   eine optionale Farbtabelle, bei der es sich entweder um eine Gruppe von [**RGBQUAD-Strukturen**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) oder um eine Gruppe von [**RGBTRIPLE-Strukturen**](/windows/win32/api/wingdi/ns-wingdi-rgbtriple) handelt.
-   die Bitmapdaten
-   Optionale Profildaten

In einer Farbtabelle wird beschrieben, wie Pixelwerte RGB-Farbwerten entsprechen. RGB ist ein Modell zum Beschreiben von Farben, die durch Diessinführung von Licht erzeugt werden.

*Profildaten* beziehen sich entweder auf den Profildateinamen (verknüpftes Profil) oder auf die tatsächlichen Profilbits (eingebettetes Profil). Das Dateiformat platziert die Profildaten am Ende der Datei. Die Profildaten werden direkt nach der Farbtabelle platziert (sofern vorhanden). Wenn die Funktion jedoch einen gepackten DIB empfängt, werden die Profildaten wie im Dateiformat nach den Bitmapbits gespeichert.

Profildaten sind nur für [**BITMAPV5HEADER-Strukturen**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) vorhanden, bei denen **bV5CSType** PROFILE \_ LINKED oder PROFILE EMBEDDED \_ ist. Für Funktionen, die gepackte DIBs empfangen, werden die Profildaten nach den Bitmapdaten angezeigt.

Ein palettiertes Gerät ist ein beliebiges Gerät, das Paletten zum Zuweisen von Farben verwendet. Das klassische Beispiel für ein palettiertes Gerät ist eine Anzeige, die in 8-Bit-Farbtiefe (d. h. 256 Farben) ausgeführt wird. Die Anzeige in diesem Modus verwendet eine kleine Farbtabelle, um einer Bitmap Farben zu zuweisen. Die Farben in einer Bitmap werden der nächstgelegenen Farbe in der Palette zugewiesen, die das Gerät verwendet. Das palettierte Gerät erstellt keine optimale Palette zum Anzeigen der Bitmap. es verwendet einfach das, was sich in der aktuellen Palette befindet. Anwendungen sind dafür verantwortlich, eine Palette zu erstellen und im System auszuwählen. Im Allgemeinen enthalten Bitmaps mit 16, 24 und 32 Bits pro Pixel (bpp) keine Farbtabellen (auch als optimale Paletten für die Bitmap); Die Anwendung ist in diesem Fall für die Generierung einer optimalen Palette verantwortlich. 16-, 24- und 32-BPP-Bitmaps können jedoch so optimale Farbtabellen für die Anzeige auf palettierten Geräten enthalten. In diesem Fall muss die Anwendung nur eine Palette erstellen, die auf der Farbtabelle in der Bitmapdatei basiert.

Bitmaps mit 1, 4 oder 8 BPP müssen über eine Farbtabelle mit einer maximalen Größe verfügen, die auf dem BPP basiert. Die maximale Größe für 1, 4 und 8 BPP-Bitmaps beträgt 2 zur Leistung des BPP. Daher hat eine 1 BPP-Bitmap maximal zwei Farben, die 4 BPP-Bitmap hat maximal 16 Farben und die 8 BPP-Bitmap maximal 256 Farben.

Bitmaps mit 16, 24 oder 32 BPP erfordern keine Farbtabellen, müssen aber möglicherweise Farben für palettierte Geräte angeben. Wenn eine Farbtabelle für 16-, 24- oder 32-bpp-Bitmaps vorhanden ist, gibt das **element biClrUsed** die Größe der Farbtabelle an, und die Farbtabelle muss so viele Farben enthalten. Wenn **biClrUsed 0** (null) ist, gibt es keine Farbtabelle.

Die roten, grünen und blauen Bitfeldmasken für BI-BITFIELD-Bitmaps folgen unmittelbar auf die \_ [**BitmapINFOHEADER-,**](/previous-versions//dd183376(v=vs.85)) [**BITMAPV4HEADER-**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)und [**BITMAPV5HEADER-Strukturen.**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) Die **BitmapV4HEADER-** und **BITMAPV5HEADER-Strukturen** enthalten wie folgt zusätzliche Member für rote, grüne und blaue Masken.



| Member        | Bedeutung                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------|
| **RedMask**   | Farbmaske, die die rote Komponente jedes Pixels angibt, nur gültig, wenn das **Compression-Element** auf BI \_ BITFIELDS festgelegt ist.   |
| **GreenMask** | Farbmaske, die die grüne Komponente jedes Pixels angibt, nur gültig, wenn das **Compression-Element** auf BI \_ BITFIELDS festgelegt ist. |
| **BlueMask**  | Farbmaske, die die blaue Komponente jedes Pixels angibt, nur gültig, wenn das **Compression-Element** auf BI \_ BITFIELDS festgelegt ist.  |



 

Wenn **das biCompression-Element** von [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) auf BI BITFIELDS festgelegt ist und die Funktion ein Argument vom Typ \_ **LPBITMAPINFO** empfängt, folgen die Farbmasken unmittelbar auf den Header. Falls vorhanden, folgt die Farbtabelle den Farbmasken. [**BitmapCOREHEADER-Bitmaps**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader) unterstützen keine Farbmasken.

Standardmäßig werden Bitmapdaten im Format von unten nach oben angezeigt. Bottom-up bedeutet, dass die erste Scanzeile in den Bitmapdaten die letzte anzuzeigende Scanzeile ist. Das 0-te<sup></sup> Pixel der 0-th-Scanzeile der Bitmapdaten einer Bitmap mit 10 Pixeln und 10 Pixeln<sup></sup> ist beispielsweise das<sup>0-te</sup> Pixel der neunten Scanzeile des angezeigten oder gedruckten Bilds.<sup></sup> Bitmaps im RLE-Format (Run-Length encoded) und [**BITMAPCOREHEADER-Bitmaps**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader) dürfen keine Bitmaps von oben nach unten sein. Die Scanzeilen sind mit Ausnahme von RLE-komprimierten Bitmaps **DWORD-ausgerichtet.** Sie müssen für Scanlinienbreiten in Bytes aufschlossen werden, die nicht gleichmäßig durch vier teilbar sind, mit Ausnahme von RLE-komprimierten Bitmaps. Eine 10- mal 10-Pixel-24-BPP-Bitmap hat beispielsweise zwei Aufabstandsbytes am Ende jeder Scanzeile.

 

 
