---
title: Programmier Handbuch für DDS
description: Direct3D implementiert das DDS-Dateiformat zum Speichern von nicht komprimierten oder komprimierten (DXTn) Texturen.
ms.assetid: 39f9847e-3b1c-4401-a253-74c183ffcc83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4940db5ec40e6ec0b907aa4ee7ce725cd585e961
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104391230"
---
# <a name="programming-guide-for-dds"></a>Programmier Handbuch für DDS

Direct3D implementiert das DDS-Dateiformat zum Speichern von nicht komprimierten oder komprimierten (DXTn) Texturen. Das Dateiformat implementiert verschiedene leicht unterschiedliche Typen, die zum Speichern von unterschiedlichen Datentypen entworfen wurden, und unterstützt einfache Texturen, Texturen mit Mipmaps, Cubemaps, volumemaps und Textur Arrays (in Direct3D 10/11). In diesem Abschnitt wird das Layout einer DDS-Datei beschrieben.

Hilfe zum Erstellen einer Textur in Direct3D 11 finden Sie unter Gewusst [wie: Erstellen einer Textur](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-create). Hilfe zu Direct3D 9 finden Sie [unter Textur Unterstützung in D3DX (Direct3D 9)](/windows/desktop/direct3d9/texture-support-in-d3dx).

-   [DDS-Datei Layout](#dds-file-layout)
-   [DDS-Varianten](#dds-variants)
-   [Verwenden von Textur Arrays in Direct3D 10/11](#using-texture-arrays-in-direct3d-1011)
-   [Allgemeine DDS-Datei Ressourcen Formate und zugehörige Header Inhalte](#common-dds-file-resource-formats-and-associated-header-content)
-   [Zugehörige Themen](#related-topics)

## <a name="dds-file-layout"></a>DDS-Datei Layout

Eine DDS-Datei ist eine Binärdatei mit den folgenden Informationen:

-   DWORD ("Magic Number") mit dem vierstelligen Codewert "DDS" (0x20534444)

-   Beschreibung der Daten in der Datei

    Die Daten werden mit einer Header Beschreibung mithilfe des [**DDS- \_ Headers**](dds-header.md)beschrieben. das Pixel Format wird mit [**DDS \_ Pixel Format**](dds-pixelformat.md)definiert. Beachten Sie, dass der **DDS- \_ Header** und die **DDS- \_ Pixel Format** -Strukturen die veralteten DDSURFACEDESC2-, DDSCAPS2-und ddpixelformat DirectDraw 7-Strukturen ersetzen. **DDS \_ Header** ist die binäre Entsprechung von DDSURFACEDESC2 und DDSCAPS2. **DDS \_ Pixel Format** ist das binäre Äquivalent von ddpixelformat.

    ```
    DWORD               dwMagic;
    DDS_HEADER          header;
            
    ```

    

    Wenn DDS \_ Pixel Format dwFlags auf ddpf FourCC festgelegt ist \_ und dwfourcc auf "DX10" festgelegt ist, wird eine zusätzliche [**DDS- \_ Header \_ DXT10**](dds-header-dxt10.md) Struktur vorhanden sein, um Textur Arrays oder DXGI-Formate zu unterstützen, die nicht als RGB-Pixel formatiert werden können, wie z. b. Gleit Komma Formate, sRGB-Formate usw. Wenn die **DDS- \_ Header \_ DXT10** -Struktur vorhanden ist, sieht die gesamte Daten Beschreibung wie folgt aus.

    ```
    DWORD               dwMagic;
    DDS_HEADER          header;
    DDS_HEADER_DXT10    header10;
    ```

    

-   Ein Zeiger auf ein Bytearray, in dem die Hauptoberflächendaten enthalten sind.
    ```
    BYTE bdata[]
    ```

    

-   Ein Zeiger auf ein Bytearray, in dem die verbleibenden Oberflächen enthalten sind, z. B. Mipmap-Ebenen, Seiten einer Würfelmap, Tiefen in einer Volumentextur. Weitere Informationen zum Layout der DDS-Datei finden Sie unter den folgenden Links: [texture](dds-file-layout-for-textures.md)[Cubemap](dds-file-layout-for-cubic-environment-maps.md) oder [Volumentextur](dds-file-layout-for-volume-textures.md).

    ```
    BYTE bdata2[]
    ```

    

Für eine umfangreiche Hardwareunterstützung empfehlen wir die Verwendung des [**DXGI- \_ Formats \_ R8G8B8A8 \_ unorm**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), [**DXGI \_ Format \_ R8G8B8A8 \_ unorm \_ sRGB**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), [**DXGI \_ Format \_ R8G8B8A8 \_ snorm**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), [**DXGI \_ Format \_ B8G8R8A8 \_ unorm**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), [**DXGI \_ Format \_ R16G16 \_ snorm**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), [**DXGI \_ Format \_ R8G8 \_ snorm**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), [**DXGI- \_ Format \_ R8 \_ unorm**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), [**DXGI- \_ Format \_ BC1 \_ unorm**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), [**DXGI- \_ Format \_ BC1 \_ unorm \_ sRGB**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), [**DXGI- \_ Format \_ BC2 \_ unorm**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), [**DXGI- \_ Format \_ BC2 \_ unorm \_ sRGB**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), [**DXGI- \_ Format \_ BC3 \_ unorm**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)oder [**DXGI- \_ Format \_ BC3 \_ unorm \_ sRGB**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) -Format.

Weitere Informationen zu komprimierten Textur Formaten finden Sie unter [Textur Block Komprimierung in Direct3D 11](/windows/desktop/direct3d11/texture-block-compression-in-direct3d-11) und [Block Komprimierung (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression).

Die D3DX-Bibliothek (z. b. Bibliothek d3dx11. lib) und andere ähnliche Bibliotheken sind unzuverlässig oder inkonsistent, stellen den Wert für die Tonhöhe im **dwpitchorlinearsize** -Member der [**DDS- \_ Header**](dds-header.md) Struktur bereit. Daher wird beim Lesen und Schreiben von DDS-Dateien empfohlen, dass Sie die-Tonhöhe auf eine der folgenden Weisen für die folgenden Formate berechnen:

-   Berechnen Sie für Block komprimierte Formate die Tonhöhe wie folgt:

    Max (1, ((Breite + 3)/4)) \* Blockgröße

    Die Blockgröße beträgt 8 Bytes für DXT1-, BC1-und BC4-Formate und 16 Bytes für andere Block komprimierte Formate.

-   Berechnen Sie für R8G8 \_ B8G8, G8R8 \_ G8B8, Legacy-und Legacy-im YUY2-packingformate die folgenden Optionen:

    ((Breite + 1)  >> 1) \* 0:

-   Für andere Formate berechnen Sie die Tonhöhe wie folgt:

    (Breite \* Bits pro Pixel + 7)/8

    Sie teilen durch 8 die Byte Ausrichtung.

> [!Note]  
> Der von Ihnen berechene Wert ist nicht immer mit der von der Runtime bereitgestellten Tonhöhe identisch. Dies ist in einigen Situationen DWORD-ausgerichtet und in anderen Situationen in Byte ausgerichtet. Daher empfiehlt es sich, eine Scan Zeile zu einem Zeitpunkt zu kopieren, anstatt zu versuchen, das gesamte Bild in einer Kopie zu kopieren.

 

## <a name="dds-variants"></a>DDS-Varianten

Es gibt viele Tools, mit denen DDS-Dateien erstellt und genutzt werden können. Sie können jedoch in den Details der erforderlichen Elemente in der Kopfzeile variieren. Writer sollten die Header so umfassend wie möglich auffüllen, und die Leser sollten die minimalen Werte auf maximale Kompatibilität überprüfen. Um eine DDS-Datei zu validieren, sollte ein Reader sicherstellen, dass die Datei mindestens 128 Byte lang ist, um den Magic-Wert und den Basic-Header zu berücksichtigen, der Magic-Wert 0x20534444 ("DDS"), die DDS- \_ Header Größe 124 und das DDS- \_ Pixel Format in der Header Größe 32 ist. Wenn DDS \_ Pixel Format dwFlags auf ddpf \_ FourCC und dwfourcc auf "DX10" festgelegt ist, muss die Gesamt Dateigröße mindestens 148 Byte betragen.

Es gibt einige häufig verwendete Varianten, bei denen das Pixel Format auf einen ddpf-FourCC-Code festgelegt ist, \_ bei dem dwfourcc auf einen D3DFORMAT-oder DXGI- \_ formatenumerationswert festgelegt ist. Es gibt keine Möglichkeit, zu ermitteln, ob es sich bei einem Enumerationswert um ein D3DFORMAT-oder DXGI \_ -Format handelt. Daher wird dringend empfohlen, stattdessen die "DX10"-Erweiterung und den DDS- \_ Header \_ DXT10-Header zum Speichern von dxgiformat zu verwenden, wenn das grundlegende DDS- \_ Pixel Format das Format nicht ausdrücken kann.

Das DDS \_ -Standard Pixel Format sollte für maximale Kompatibilität für das Speichern von nicht komprimierten RGB-Daten und DXT1-5-Daten bevorzugt werden, da nicht alle DDS-Tools die DX10-Erweiterung unterstützen.

## <a name="using-texture-arrays-in-direct3d-1011"></a>Verwenden von Textur Arrays in Direct3D 10/11

Die neuen DDS-Strukturen ([**DDS- \_ Header**](dds-header.md) und [**DDS- \_ Header \_ DXT10**](dds-header-dxt10.md)) in Direct3D 10/11 erweitern das DDS-Dateiformat, um ein Array von Texturen zu unterstützen, bei dem es sich um einen neuen Ressourcentyp in Direct3D 10/11 handelt. Im folgenden finden Sie einen Beispielcode, der zeigt, wie Sie mithilfe der neuen Header auf die verschiedenen MipMap-Ebenen in einem Array von Texturen zugreifen können.


```
DWORD               dwMagic;
DDS_HEADER          header;
DDS_HEADER_DXT10    header10;
   
for (int iArrayElement = 0; iArrayElement < header10.arraySize; iArrayElement++)
{
   for (int iMipLevel = 0; iMipLevel < header.dwMipMapCount; iMipLevel++)
   {
     ...
   }
}       
```



## <a name="common-dds-file-resource-formats-and-associated-header-content"></a>Allgemeine DDS-Datei Ressourcen Formate und zugehörige Header Inhalte



| Ressourcen Format                                                                            | dwFlags        | dwrgbbitcount | dwrbitmaske | dwgbitmaske | dwbbitmask | dwabitmask |
|--------------------------------------------------------------------------------------------|----------------|---------------|------------|------------|------------|------------|
| DXGI- \_ Format \_ R8G8B8A8 \_ unorm<br/> D3DFMT \_ A8B8G8R8<br/>                       | DDS- \_ RGBA      | 32            | 0xFF       | 0xFF00     | 0xFF0000   | 0xFF000000 |
| DXGI- \_ Format \_ R16G16 \_ unorm<br/> D3DFMT \_ G16R16<br/>                           | DDS- \_ RGBA      | 32            | 0xFFFF     | 0xFFFF0000 |            |            |
| \*\*<br/> DXGI- \_ Format \_ R10G10B10A2 \_ unorm<br/> D3DFMT \_ A2B10G10R10<br/> | DDS- \_ RGBA      | 32            | 0x3ff      | 0xffc00    | 0x3ff00000 |            |
| DXGI- \_ Format \_ R16G16 \_ unorm<br/> D3DFMT \_ G16R16<br/>                           | DDS \_ RGB       | 32            | 0xFFFF     | 0xFFFF0000 |            |            |
| DXGI- \_ Format \_ B5G5R5A1 \_ unorm<br/> D3DFMT \_ A1R5G5B5<br/>                       | DDS- \_ RGBA      | 16            | 0x7c00     | 0x3e0      | 0x1F       | 0x8000     |
| DXGI- \_ Format \_ B5G6R5 \_ unorm<br/> D3FMT \_ R5G6B5<br/>                            | DDS \_ RGB       | 16            | 0xF 800     | 0x7e0      | 0x1F       |            |
| DXGI \_ a8 \_ unorm<br/> D3DFMT \_ a8<br/>                                           | DDS- \_ Alpha     | 8             |            |            |            | 0xFF       |
| D3DFMT \_ A8R8G8B8<br/>                                                                | DDS- \_ RGBA      | 32            | 0xFF0000   | 0xFF00     | 0xFF       | 0xFF000000 |
| D3DFMT \_ X8R8G8B8<br/>                                                                | DDS \_ RGB       | 32            | 0xFF0000   | 0xFF00     | 0xFF       |            |
| D3DFMT \_ X8B8G8R8<br/>                                                                | DDS \_ RGB       | 32            | 0xFF       | 0xFF00     | 0xFF0000   |            |
| \*\*<br/> D3DFMT \_ A2R10G10B10<br/>                                             | DDS- \_ RGBA      | 32            | 0x3ff00000 | 0xffc00    | 0x3ff      | 0xC0000000 |
| D3DFMT \_ R8G8B8<br/>                                                                  | DDS \_ RGB       | 24            | 0xFF0000   | 0xFF00     | 0xFF       |            |
| D3DFMT \_ X1R5G5B5<br/>                                                                | DDS \_ RGB       | 16            | 0x7c00     | 0x3e0      | 0x1F       |            |
| D3DFMT \_ A4R4G4B4<br/>                                                                | DDS- \_ RGBA      | 16            | 0xF 00      | 0xf0       | 0xF        | 0xF     |
| D3DFMT \_ X4R4G4B4<br/>                                                                | DDS \_ RGB       | 16            | 0xF 00      | 0xf0       | 0xF        |            |
| D3DFMT \_ A8R3G3B2<br/>                                                                | DDS- \_ RGBA      | 16            | 0xe0       | 0x1C       | 0x3        | 0xFF00     |
| D3DFMT \_ A8L8<br/>                                                                    | DDS- \_ Beleuchtung | 16            | 0xFF       |            |            | 0xFF00     |
| D3DFMT \_ L16<br/>                                                                     | DDS- \_ Beleuchtung | 16            | 0xFFFF     |            |            |            |
| D3DFMT \_ L8<br/>                                                                      | DDS- \_ Beleuchtung | 8             | 0xFF       |            |            |            |
| D3DFMT \_ A4L4<br/>                                                                    | DDS- \_ Beleuchtung | 8             | 0xF        |            |            | 0xf0       |



 



| Ressourcen Format                                                                             | dwFlags     | dwfourcc |
|---------------------------------------------------------------------------------------------|-------------|----------|
| DXGI- \_ Format \_ BC1 \_ unorm<br/> D3DFMT \_ DXT1<br/>                                 | DDS \_ FourCC | DXT1   |
| DXGI- \_ Format \_ BC2 \_ unorm<br/> D3DFMT \_ DXT3<br/>                                 | DDS \_ FourCC | "DXT3"   |
| DXGI- \_ Format \_ BC3 \_ unorm<br/> D3DFMT \_ DXT5<br/>                                 | DDS \_ FourCC | DXT5   |
| \*<br/> DXGI- \_ Format \_ BC4 \_ unorm<br/>                                           | DDS \_ FourCC | "BC4U"   |
| \*<br/> DXGI- \_ Format \_ BC4 \_ snorm<br/>                                           | DDS \_ FourCC | "BC4S"   |
| \*<br/> DXGI- \_ Format \_ BC5 \_ unorm<br/>                                           | DDS \_ FourCC | "ATI2"   |
| \*<br/> DXGI- \_ Format \_ BC5 \_ snorm<br/>                                           | DDS \_ FourCC | "BC5S"   |
| DXGI- \_ Format \_ R8G8 \_ B8G8 \_ unorm<br/> D3DFMT \_ R8G8 \_ B8G8<br/>                    | DDS \_ FourCC | "RgBG"   |
| DXGI- \_ Format \_ G8R8 \_ G8B8 \_ unorm<br/> D3DFMT \_ G8R8 \_ G8B8<br/>                    | DDS \_ FourCC | "Grgb"   |
| \*<br/> DXGI- \_ Format \_ R16G16B16A16 \_ unorm<br/> D3DFMT \_ A16B16G16R16<br/>  | DDS \_ FourCC | 36       |
| \*<br/> DXGI- \_ Format \_ R16G16B16A16 \_ snorm<br/> D3DFMT \_ Q16W16V16U16<br/>  | DDS \_ FourCC | 110      |
| \*<br/> DXGI- \_ Format \_ R16 \_ float<br/> D3DFMT \_ R16F<br/>                   | DDS \_ FourCC | 111      |
| \*<br/> DXGI- \_ Format \_ R16G16 \_ float<br/> D3DFMT \_ G16R16F<br/>             | DDS \_ FourCC | 112      |
| \*<br/> DXGI- \_ Format \_ R16G16B16A16 \_ float<br/> D3DFMT \_ A16B16G16R16F<br/> | DDS \_ FourCC | 113      |
| \*<br/> DXGI- \_ Format \_ R32 \_ float<br/> D3DFMT \_ R32F<br/>                   | DDS \_ FourCC | 114      |
| \*<br/> DXGI- \_ Format \_ R32G32 \_ float<br/> D3DFMT \_ G32R32F<br/>             | DDS \_ FourCC | 115      |
| \*<br/> DXGI- \_ Format \_ R32G32B32A32 \_ float<br/> D3DFMT \_ A32B32G32R32F<br/> | DDS \_ FourCC | 116      |
| D3DFMT \_ DXT2<br/>                                                                     | DDS \_ FourCC | "DXT2"   |
| D3DFMT \_ DXT4<br/>                                                                     | DDS \_ FourCC | "DXT4"   |
| D3DFMT \_ UYVY<br/>                                                                     | DDS \_ FourCC | UYVY   |
| D3DFMT \_ im YUY2<br/>                                                                     | DDS \_ FourCC | Im YUY2   |
| D3DFMT \_ CxV8U8<br/>                                                                   | DDS \_ FourCC | 117      |
| Beliebiges DXGI-Format                                                                             | DDS \_ FourCC | DX10   |



 

\* = Ein robuster DDS-Reader muss in der Lage sein, diese Legacy-Formatcodes zu verarbeiten. Ein solcher DDS-Reader sollte jedoch bevorzugen, die Header Erweiterung "DX10" zu verwenden, wenn diese Formatcodes geschrieben werden, um Mehrdeutigkeiten zu vermeiden.

\*\* = Aufgrund von sehr langen Problemen bei häufigen Implementierungen von DDS-Readern und-Writern ist die zuverlässigste Methode zum Schreiben von 10:10:10:2-Typdaten die Verwendung der "DX10"-Header Erweiterung mit dem [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Code "24" (d. h. das DXGI- \_ Format \_ R10G10B10A2 \_ unorm-Wert). D3DFMT \_ A2R10G10B10-Daten sollten vor dem Schreiben in die DDS-Datei im DXGI- \_ Format \_ R10G10B10A2 unorm-Format in 10:10:10:2-Daten konvertiert werden \_ .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DDS](dx-graphics-dds.md)
</dt> </dl>

 

