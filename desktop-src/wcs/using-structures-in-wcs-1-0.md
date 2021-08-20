---
title: Verwenden von Strukturen in WCS 1.0
description: Die meisten von WCS 1.0 verwendeten Strukturen sind sehr einfach und erfordern nur wenig Erklärung. Sie sind im ABSCHNITT WCS 1.0-Referenz mit dem Titel Strukturen dokumentiert.
ms.assetid: 8d3682e2-38fd-4a33-b386-ab0716bb6972
keywords:
- Windows Farbsystem (WCS), Strukturen
- WCS (Windows Color System), Strukturen
- Bildfarbverwaltung,Strukturen
- Farbverwaltung,Strukturen
- Farben, Strukturen
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2abd7eec0a32a169e422c3a3cbba52abd4b94bd54be41b3c8bd241d303e82cab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117670773"
---
# <a name="using-structures-in-wcs-10"></a>Verwenden von Strukturen in WCS 1.0

Die meisten von WCS 1.0 verwendeten Strukturen sind sehr einfach und erfordern nur wenig Erklärung. Sie sind im WCS 1.0-Referenzabschnitt mit dem Titel [Strukturen](structures.md)dokumentiert.

Ausnahmen sind die [**COLORMATCHSETUPW-Struktur,**](/windows/win32/api/icm/ns-icm-colormatchsetupw) die von der [**SetupColorMatchingW-Funktion**](/windows/win32/api/icm/nf-icm-setupcolormatchingw) verwendet wird, und die folgenden Windows in Wingdi.h definierten Strukturen:

-   [BITMAPV5HEADER](#windows-bitmap-header-structures)
-   [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea)
-   [**CIEXYZ**](/windows/desktop/api/Wingdi/ns-wingdi-tagciexyz)
-   [**CIEXYZTRIPLE**](/windows/desktop/api/Wingdi/ns-wingdi-tagicexyztriple)

Die folgenden Themen werden ausführlicher erläutert:

-   [Windows Bitmapheaderstrukturen](#windows-bitmap-header-structures)
-   [Unterschiede zwischen V4- und V5-Headern](#differences-between-v4-and-v5-headers)
-   [Bitmap.exe: ein Command-Line-Hilfsprogramm zum Konvertieren von Bitmapheadern](#bitmapexe-a-command-line-utility-for-converting-bitmap-headers)

## <a name="windows-bitmap-header-structures"></a>Windows Bitmapheaderstrukturen

WCS 1.0 ermöglicht das Verknüpfen oder Einbetten von COLOR-Farbprofilen in geräteunabhängige Bitmaps (DIBs). Dadurch können DIB-Farben genauer gekennzeichnet werden, als dies mit WCS in Windows 95 möglich war. [BITMAPV5HEADER](/windows/win32/api/wingdi/ns-wingdi-bitmapv5header) , die neue Bitmapheaderstruktur, wird in Wingdi.h in der Veröffentlichung von Windows 98 definiert. Zu Entwicklungszwecken ist sie auch in der Datei Icm.h mit dieser Programmierreferenz enthalten. Die **BITMAPV5HEADER-Struktur** sieht wie folgt aus:


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



Der Member **bV5CSType** kann die Werte PROFILE \_ EMBEDDED oder PROFILE LINKED \_ aufweisen, um anzugeben, ob ein Profil eingebettet oder mit dem DIB verknüpft ist. Der Member **bV5ProfileData** ist der Offset in Bytes vom Anfang der **BITMAPV5HEADER-Struktur** bis zum Anfang der Profildaten. Wenn das Profil eingebettet ist, sind Profildaten das tatsächliche Profil, und wenn es verknüpft ist, sind die Profildaten der auf NULL endende Dateiname des Profils. Dies kann keine Unicode-Zeichenfolge sein. Er muss ausschließlich aus Zeichen aus dem Windows Zeichensatz bestehen (Codepage 1252).

Wenn ein DIB in den Arbeitsspeicher geladen wird, sollten die Profildaten (sofern vorhanden) der Farbtabelle folgen, und **bV5ProfileData** sollte den Offset der Profildaten vom Anfang der **BITMAPV5HEADER-Struktur** angeben. Der Wert dieses Members ist jetzt anders, da die Bitmapbits nicht der Farbtabelle im Arbeitsspeicher folgen. Anwendungen sollten das **bV5ProfileData-Element** ändern, nachdem das DIB in den Arbeitsspeicher geladen wurde.

Bei gepackten DIBs sollten die Profildaten den Bitmapbits ähnlich dem Dateiformat entsprechen. Der **bV5ProfileData-Member** sollte weiterhin den Offset der Profildaten vom Anfang der **BITMAPV5HEADER-Struktur** angeben.

Anwendungen sollten nur dann auf die Profildaten zugreifen, wenn **bV5Size**  ==  **sizeof** ( **BITMAPV5HEADER** ) **ANDbV5CSType** PROFILE \_ EMBEDDED oder PROFILE LINKED \_ ist.

Wenn ein Profil verknüpft ist, kann der Pfad des Profils ein beliebiger vollqualifizierte Name (einschließlich eines Netzwerkpfads) sein, der mit der Win32 **CreateFile-Funktion** geöffnet werden kann.

## <a name="differences-between-v4-and-v5-headers"></a>Unterschiede zwischen V4- und V5-Headern

Bei der Arbeit mit der neuen Bitmapstruktur ist es hilfreich, Unterschiede in der Einrichtung von **BITMAPV4HEADER-** und **BITMAPV5HEADER-Strukturen** zu erkennen:



| V4-Header     | Bedeutung                                                                                                                              |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------|
| **bV4CSType** | \_LCS-KALIBRIERTES \_ RGB. Dieser Wert impliziert, dass Endpunkte und Gammas in den entsprechenden Feldern angegeben werden. Falsche Werte verursachen Probleme. |
| **bV4CSType** | LCS \_ sRGB. Dieser Wert impliziert, dass sich die Bitmap im sRGB-Farbraum befindet (Gammas und Endpunkte werden ignoriert).                                 |
| **bV4CSType** | LCS \_ \_ WINDOWS-FARBRAUM. \_ Dieser Wert impliziert, dass sich die Bitmap in Windows Standardfarbraum befindet.                                    |



 



| V5-Header     | Bedeutung                                                                                                                                                      |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **bV5CSType** | \_LCS-KALIBRIERTES \_ RGB. Dieser Wert impliziert, dass Endpunkte und Gammas in den entsprechenden Feldern angegeben werden. Falsche Werte verursachen Probleme.                         |
| **bV5CSType** | LCS \_ sRGB. Dieser Wert impliziert, dass sich die Bitmap im sRGB-Farbraum befindet (Gammas und Endpunkte werden ignoriert).                                                         |
| **bV5CSType** | PROFIL \_ EINGEBETTET. Dieser Wert impliziert, dass **bV5ProfileData** auf einen Speicherpuffer verweist, der das zu verwendende Profil enthält (Gammas und Endpunkte werden ignoriert). |
| **bV5CSType** | \_PROFIL VERKNÜPFT. Dieser Wert impliziert, dass **bV5ProfileData** auf den Dateinamen des zu verwendenden Profils verweist (Gammas und Endpunkte werden ignoriert).                |
| **bV5CSType** | LCS \_ \_ WINDOWS-FARBRAUM. \_ Dieser Wert impliziert, dass sich die Bitmap in Windows Standardfarbraum befindet.                                                            |



 

Um ältere Bitmaps in und aus der neuen **BITMAPV5HEADER-Struktur** zu konvertieren, ist in der WCS 1.0-Programmierreferenz eine Befehlszeilenkonvertierungs-Hilfsprogrammdatei mit dem Namen Bitmap.exe enthalten.

## <a name="bitmapexe-a-command-line-utility-for-converting-bitmap-headers"></a>BitMap.exe: ein Command-Line-Hilfsprogramm zum Konvertieren von Bitmapheadern

Bitmap.exe ist ein Befehlszeilenprogramm, das sich im \\ Ordner Bin unter dem von Ihnen angegebenen Installationsordner befindet. Sie ändert die Header von Windows Bitmaps, sodass Sie vorhandene Bitmaps von **BITMAPINFOHEADER-** und **BITMAPV4HEADER-Headerstrukturen** in die neuere **BITMAPV5HEADER-Struktur** und wieder zurück konvertieren können. Die Befehlszeilensyntax lautet wie folgt:


```C++
BITMAP [/d] [/1|4|5] [/s] [/f] 
filename
```



Die Befehlszeilenschalter haben die folgenden Auswirkungen.



| Switch | Bedeutung                                                                  |
|--------|--------------------------------------------------------------------------|
| /d     | Standardwerte werden automatisch in die konvertierten Header eingegeben.       |
| /1     | Konvertieren der angegebenen Bitmaps in **BITMAPINFOHEADER**                    |
| /4     | Konvertieren der angegebenen Bitmaps in **BITMAPV4HEADER**                      |
| /5     | Konvertieren der angegebenen Bitmaps in **BITMAPV5HEADER**                      |
| /f     | Erzwingt die Konvertierung, auch wenn die Bitmap bereits über den richtigen Header verfügt.       |
| /s     | Konvertiert Bitmaps im angegebenen Ordner und in alle darunter befindlichen Unterverzeichnisse. |



 

 

 