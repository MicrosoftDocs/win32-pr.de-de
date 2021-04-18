---
title: Verwenden von Strukturen in WCS 1.0
description: Die meisten der von WCS 1,0 verwendeten Strukturen sind sehr unkompliziert und erfordern wenig Erläuterungen. Sie sind im Abschnitt "WCS 1,0 Reference" mit dem Titel "Strukturen" dokumentiert.
ms.assetid: 8d3682e2-38fd-4a33-b386-ab0716bb6972
keywords:
- Windows Color System (WCS), Strukturen
- WCS (Windows Color System), Strukturen
- Bild Farbverwaltung, Strukturen
- Farbverwaltung, Strukturen
- Farben, Strukturen
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13d6e434ccfa6d96aa815f0c1997dc7f34178a32
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106354922"
---
# <a name="using-structures-in-wcs-10"></a>Verwenden von Strukturen in WCS 1.0

Die meisten der von WCS 1,0 verwendeten Strukturen sind sehr unkompliziert und erfordern wenig Erläuterungen. Sie sind im Abschnitt "WCS 1,0 Reference" mit dem Titel " [Strukturen](structures.md)" dokumentiert.

Ausnahmen sind die [**colormatchsetupw**](/windows/win32/api/icm/ns-icm-colormatchsetupw) -Struktur, die von der [**setupcolormatchingw**](/windows/win32/api/icm/nf-icm-setupcolormatchingw) -Funktion verwendet wird, und die folgenden Windows-Strukturen, die in WinGDI. h definiert sind:

-   [BITMAPV5HEADER](#windows-bitmap-header-structures)
-   [**Logcolorspace**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea)
-   [**CIEXYZ**](/windows/desktop/api/Wingdi/ns-wingdi-tagciexyz)
-   [**Ciexyztriple**](/windows/desktop/api/Wingdi/ns-wingdi-tagicexyztriple)

Die folgenden Themen werden in größerem Umfang behandelt:

-   [Windows-Bitmap-Header Strukturen](#windows-bitmap-header-structures)
-   [Unterschiede zwischen v4-und V5-Headern](#differences-between-v4-and-v5-headers)
-   [Bitmap.exe: ein Command-Line Hilfsprogramm zum Umrechnen von bitmapheadern.](#bitmapexe-a-command-line-utility-for-converting-bitmap-headers)

## <a name="windows-bitmap-header-structures"></a>Windows-Bitmap-Header Strukturen

Mit WCS 1,0 können Sie die Verknüpfung von "ICC"-Farbprofilen in geräteunabhängigen Bitmaps (Disb) ermöglichen. Dadurch können DIB-Farben präziser als die Verwendung von WCS in Windows 95 gekennzeichnet werden. [BITMAPV5HEADER](/windows/win32/api/wingdi/ns-wingdi-bitmapv5header) , die neue Bitmap-Header Struktur, wird in WinGDI. h in der-Version von Windows 98 definiert. Zu Entwicklungszwecken ist es auch in der Datei "ICM. h" mit der Referenz dieses Programmierers enthalten. Die **BITMAPV5HEADER** -Struktur sieht wie folgt aus:


```C++
typedef struct {
    DWORD        bV5Size;
    LONG         bV5Width;
    LONG         bV5Height;
    WORD         bV5Planes;
    WORD         bV5BitCount;
    DWORD        bV5Compression;
    DWORD        bV5SizeImage;
    LONG         bV5XPelsPerMeter;
    LONG         bV5YPelsPerMeter;
    DWORD        bV5ClrUsed;
    DWORD        bV5ClrImportant;
    DWORD        bV5RedMask;
    DWORD        bV5GreenMask;
    DWORD        bV5BlueMask;
    DWORD        bV5AlphaMask;
    DWORD        bV5CSType;
    CIEXYZTRIPLE bV5Endpoints;
    DWORD        bV5GammaRed;
    DWORD        bV5GammaGreen;
    DWORD        bV5GammaBlue;
    DWORD        bV5Intent;         // Rendering intent for bitmap 
    DWORD        bV5ProfileData;    // Offset to profile data 
    DWORD        bV5ProfileSize;    // Size of embedded profile data 
    DWORD        bV5Reserved;       // Should be zero 
} BITMAPV5HEADER, FAR *LPBITMAPV5HEADER, *PBITMAPV5HEADER;
```



Der Member **bV5CSType** kann die Werte profile \_ Embedded oder Profile \_ Linked aufweisen, um anzugeben, ob ein Profil eingebettet oder mit dem DIB verknüpft ist. Der Member **bV5ProfileData** ist der Offset in Bytes vom Anfang der **BITMAPV5HEADER** -Struktur bis zum Anfang der Profildaten. Wenn das Profil eingebettet ist, handelt es sich bei den Profildaten um das tatsächliche Profil, und wenn es verknüpft ist, ist die Profildaten der mit NULL endenden Dateiname des Profils. Dies darf keine Unicode-Zeichenfolge sein. Sie muss ausschließlich aus Zeichen aus dem Windows-Zeichensatz (Codepage 1252) bestehen.

Wenn ein DIB in den Arbeitsspeicher geladen wird, sollten die Profildaten (falls vorhanden) der Farbtabelle folgen, und **bV5ProfileData** sollte den Offset der Profildaten vom Anfang der **BITMAPV5HEADER** -Struktur erhalten. Der Wert dieses Members ist nun anders, da die Bitmapbits nicht der Farbtabelle im Arbeitsspeicher folgen. Anwendungen sollten den **bV5ProfileData** -Member ändern, nachdem der DIB in den Arbeitsspeicher geladen wurde.

Für gepackte Disb sollten die Profildaten den Bitmapbits folgen, die dem Dateiformat ähneln. Der **bV5ProfileData** -Member sollte weiterhin den Offset der Profildaten vom Anfang der **BITMAPV5HEADER** -Struktur abgeben.

Anwendungen sollten nur auf die Profildaten zugreifen, wenn **bV5Size**  ==  **sizeof** ( **BITMAPV5HEADER** ) **ANDbV5CSType** profile \_ Embedded oder Profile \_ verknüpft ist.

Wenn ein Profil verknüpft ist, kann der Pfad des Profils ein beliebiger voll qualifizierter Name (einschließlich eines Netzwerk Pfads) sein, der mithilfe der Win32-Funktion " **deatefile** " geöffnet werden kann.

## <a name="differences-between-v4-and-v5-headers"></a>Unterschiede zwischen v4-und V5-Headern

Beim Arbeiten mit der neuen Bitmap-Struktur ist es sinnvoll, Unterschiede in der Einrichtung von **BITMAPV4HEADER** -und **BITMAPV5HEADER** -Strukturen zu erkennen:



| V4-Header     | Bedeutung                                                                                                                              |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------|
| **bV4CSType** | LCS- \_ kalibrierte \_ RGB. Dieser Wert impliziert, dass Endpunkte und Gammas in den entsprechenden Feldern angegeben werden. Falsche Werte verursachen Probleme. |
| **bV4CSType** | LCS \_ sRGB. Dieser Wert impliziert, dass die Bitmap den sRGB-Farbraum aufweist (Gammas und Endpunkte werden ignoriert).                                 |
| **bV4CSType** | LCS \_ Windows- \_ Farbraum \_ . Dieser Wert impliziert, dass die Bitmap in Windows-Standard Farbraum ist.                                    |



 



| V5-Header     | Bedeutung                                                                                                                                                      |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **bV5CSType** | LCS- \_ kalibrierte \_ RGB. Dieser Wert impliziert, dass Endpunkte und Gammas in den entsprechenden Feldern angegeben werden. Falsche Werte verursachen Probleme.                         |
| **bV5CSType** | LCS \_ sRGB. Dieser Wert impliziert, dass die Bitmap den sRGB-Farbraum aufweist (Gammas und Endpunkte werden ignoriert).                                                         |
| **bV5CSType** | Profil \_ eingebettet. Dieser Wert impliziert, dass **bV5ProfileData** auf einen Arbeitsspeicher Puffer verweist, der das zu verwendende Profil enthält (Gammas und Endpunkte werden ignoriert). |
| **bV5CSType** | Profil \_ verknüpft. Dieser Wert impliziert, dass **bV5ProfileData** auf den Dateinamen des zu verwendenden Profils zeigt (Gammas und Endpunkte werden ignoriert).                |
| **bV5CSType** | LCS \_ Windows- \_ Farbraum \_ . Dieser Wert impliziert, dass die Bitmap in Windows-Standard Farbraum ist.                                                            |



 

Um ältere Bitmaps in und aus der neuen **BITMAPV5HEADER** -Struktur zu konvertieren, ist eine Befehlszeilen-Konvertierungsprogramm Datei mit dem Namen Bitmap.exe in der WCS 1,0-Programmier Referenz enthalten.

## <a name="bitmapexe-a-command-line-utility-for-converting-bitmap-headers"></a>BitMap.exe: ein Command-Line Hilfsprogramm zum Umrechnen von bitmapheadern.

Bitmap.exe ist ein Befehlszeilenprogramm, das sich im \\ Ordner "bin" unter dem von Ihnen angegebenen Installationsordner befindet. Er ändert die Header von Windows-Bitmaps, sodass Sie vorhandene Bitmaps aus **BITMAPINFOHEADER** -und **BITMAPV4HEADER** -Header Strukturen in die neuere **BITMAPV5HEADER** -Struktur und wieder zurück konvertieren können. Die Befehlszeilen Syntax lautet wie folgt:


```C++
BITMAP [/d] [/1|4|5] [/s] [/f] 
filename
```



Die Befehls Zeilenschalter haben folgende Auswirkungen:



| Schalter | Bedeutung                                                                  |
|--------|--------------------------------------------------------------------------|
| /d     | Standardwerte werden automatisch in den konvertierten Headern eingegeben.       |
| /1     | Die angegebenen Bitmaps werden in **BITMAPINFOHEADER** konvertiert.                    |
| /4     | Die angegebenen Bitmaps werden in **BITMAPV4HEADER** konvertiert.                      |
| /5     | Die angegebenen Bitmaps werden in **BITMAPV5HEADER** konvertiert.                      |
| /f     | Erzwingt die Konvertierung, auch wenn die Bitmap bereits über den rechten Header verfügt.       |
| /s     | Konvertiert Bitmaps im angegebenen Ordner und in allen Unterverzeichnissen darunter. |



 

 

 