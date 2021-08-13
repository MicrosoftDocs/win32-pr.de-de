---
title: Programmierhandbuch für DDS
description: Direct3D implementiert das DDS-Dateiformat zum Speichern von unkomprimierten oder komprimierten Texturen (DXTn).
ms.assetid: 39f9847e-3b1c-4401-a253-74c183ffcc83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8fc1f8b9b84c2dc1f9236c79c320ae75848834ef2183db55b189f6b9d340d06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118796720"
---
# <a name="programming-guide-for-dds"></a>Programmierhandbuch für DDS

Direct3D implementiert das DDS-Dateiformat zum Speichern von unkomprimierten oder komprimierten Texturen (DXTn). Das Dateiformat implementiert mehrere leicht unterschiedliche Typen, die zum Speichern verschiedener Datentypen entwickelt wurden, und unterstützt Texturen auf einer Ebene, Texturen mit Mipmaps, Cubezuordnungen, Volumezuordnungen und Texturarrays (in Direct3D 10/11). In diesem Abschnitt wird das Layout einer DDS-Datei beschrieben.

Hilfe beim Erstellen einer Textur in Direct3D 11 finden Sie unter [Vorgehensweise: Erstellen einer Textur.](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-create) Hilfe zu Direct3D 9 finden Sie unter [Texturunterstützung in D3DX (Direct3D 9).](/windows/desktop/direct3d9/texture-support-in-d3dx)

-   [DDS-Dateilayout](#dds-file-layout)
-   [DDS-Varianten](#dds-variants)
-   [Verwenden von Texturarrays in Direct3D 10/11](#using-texture-arrays-in-direct3d-1011)
-   [Allgemeine DDS-Dateiformate und zugeordneter Headerinhalt](#common-dds-file-resource-formats-and-associated-header-content)
-   [Zugehörige Themen](#related-topics)

## <a name="dds-file-layout"></a>DDS-Dateilayout

Eine DDS-Datei ist eine Binärdatei mit den folgenden Informationen:

-   DWORD ("Magic Number") mit dem vierstelligen Codewert "DDS" (0x20534444)

-   Beschreibung der Daten in der Datei

    Die Daten werden mit einer Headerbeschreibung mit [**DDS \_ HEADER**](dds-header.md)beschrieben. Das Pixelformat wird mit [**DDS \_ PIXELFORMAT**](dds-pixelformat.md)definiert. Beachten Sie, dass die **DDS \_ HEADER-** und **DDS \_ PIXELFORMAT-Strukturen** die veralteten Strukturen DDSURFACEDESC2, DDSCAPS2 und DDPIXELFORMAT DirectDraw 7 ersetzen. **DDS \_ HEADER** ist die binäre Entsprechung von DDSURFACEDESC2 und DDSCAPS2. **DDS \_ PIXELFORMAT** ist die binäre Entsprechung von DDPIXELFORMAT.

    ```
    DWORD               dwMagic;
    DDS_HEADER          header;
            
    ```

    

    Wenn DDS \_ PIXELFORMAT dwFlags auf DDPF \_ FOURCC und dwFourCC auf "DX10" festgelegt ist, ist eine zusätzliche [**DDS \_ HEADER \_ DXT10-Struktur**](dds-header-dxt10.md) vorhanden, um Texturarrays oder DXGI-Formate aufzunehmen, die nicht als RGB-Pixelformat wie Gleitkommaformate, sRGB-Formate usw. ausgedrückt werden können. Wenn die **DDS \_ HEADER \_ DXT10-Struktur** vorhanden ist, sieht die gesamte Datenbeschreibung wie folgt aus.

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

    

Für umfassende Hardwareunterstützung empfehlen wir Die Verwendung von [**DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM,**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [**DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM \_ SRGB,**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [**DXGI FORMAT \_ \_ R8G8B8A8 \_ SNORM,**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [**DXGI FORMAT \_ \_ B8G8R8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), [**DXGI FORMAT \_ \_ R16G16 \_ SNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), [**DXGI FORMAT \_ \_ R8G8 \_ SNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), [**DXGI FORMAT \_ \_ R8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), [**DXGI FORMAT \_ \_ BC1 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), [**DXGI FORMAT \_ \_ BC1 \_ UNORM \_ SRGB,**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [**DXGI FORMAT \_ \_ BC2 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), [**DXGI FORMAT \_ \_ BC2 \_ UNORM \_ SRGB,**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [**DXGI FORMAT \_ \_ BC3 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)oder [**DXGI FORMAT \_ \_ BC3 \_ UNORM \_ SRGB**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) FORMAT.

Weitere Informationen zu komprimierten Texturformaten finden Sie unter [Texturblockkomprimierung in Direct3D 11](/windows/desktop/direct3d11/texture-block-compression-in-direct3d-11) und [Blockkomprimierung (Direct3D 10).](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression)

Die D3DX-Bibliothek (z.B. D3DX11.lib) und andere ähnliche Bibliotheken stellen den Tonhöhenwert im **dwPitchOrLinearSize-Member** der [**DDS \_ HEADER-Struktur**](dds-header.md) unausgeglich oder inkonsistent bereit. Daher wird empfohlen, beim Lesen und Schreiben in DDS-Dateien die Tonhöhe auf eine der folgenden Arten für die angegebenen Formate zu berechnen:

-   Berechnen Sie für blockkomprimierte Formate die Tonhöhe wie:

    max( 1, ((width+3)/4) ) \* block-size

    Die Blockgröße beträgt 8 Bytes für DXT1-, BC1- und BC4-Formate und 16 Bytes für andere blockkomprimierte Formate.

-   Berechnen Sie für R8G8 \_ B8G8, G8R8 \_ G8B8, ältere UYVY-gepackte und ältere YUY2-gepackte Formate die Tonhöhe wie:

    ((width+1) >> 1) \* 4

-   Berechnen Sie für andere Formate die Tonhöhe wie:

    ( \* Breite Bits pro Pixel + 7 ) / 8

    Sie dividieren für die Byteausrichtung durch 8.

> [!Note]  
> Der von Ihnen berechnete Tonhöhenwert entspricht nicht immer der Von der Laufzeit bereitgestellten Tonhöhe, die in einigen Situationen DWORD-ausgerichtet und in anderen Situationen bytebündig ausgerichtet ist. Daher wird empfohlen, eine Scanzeile gleichzeitig zu kopieren, anstatt zu versuchen, das gesamte Bild in einer Kopie zu kopieren.

 

## <a name="dds-variants"></a>DDS-Varianten

Es gibt viele Tools, die DDS-Dateien erstellen und nutzen, aber sie können in den Details variieren, was sie im Header benötigen. Writer sollten die Header so vollständig wie möglich auffüllen, und Leser sollten die Minimalwerte auf maximale Kompatibilität überprüfen. Um eine DDS-Datei zu überprüfen, sollte ein Reader sicherstellen, dass die Datei mindestens 128 Bytes lang ist, um den magic-Wert und den Basic-Header aufzunehmen. Der Magic-Wert ist 0x20534444 ("DDS"), die \_ DDS-HEADERgröße ist 124 und das DDS \_ PIXELFORMAT in der Headergröße 32. Wenn DDS \_ PIXELFORMAT dwFlags auf DDPF \_ FOURCC und dwFourCC auf "DX10" festgelegt ist, muss die Gesamtdateigröße mindestens 148 Bytes betragen.

Es gibt einige gängige Varianten, bei denen das Pixelformat auf einen DDPF \_ FOURCC-Code festgelegt ist, wobei dwFourCC auf einen D3DFORMAT- oder DXGI \_ FORMAT-Enumerationswert festgelegt ist. Es gibt keine Möglichkeit, zu erkennen, ob ein Enumerationswert ein D3DFORMAT- oder \_ DXGI-FORMAT ist. Daher wird dringend empfohlen, stattdessen die Erweiterung "DX10" und den DDS \_ HEADER \_ DXT10-Header zum Speichern von dxgiFormat zu verwenden, wenn DDS \_ PIXELFORMAT das Format nicht ausdrücken kann.

Das Standardmäßige DDS \_ PIXELFORMAT sollte für maximale Kompatibilität bevorzugt werden, um RGB-unkomprimierte Daten und DXT1-5-Daten zu speichern, da nicht alle DDS-Tools die DX10-Erweiterung unterstützen.

## <a name="using-texture-arrays-in-direct3d-1011"></a>Verwenden von Texturarrays in Direct3D 10/11

Die neuen DDS-Strukturen ([**DDS \_ HEADER**](dds-header.md) und [**DDS \_ HEADER \_ DXT10**](dds-header-dxt10.md)) in Direct3D 10/11 erweitern das DDS-Dateiformat, um ein Array von Texturen zu unterstützen. Dies ist ein neuer Ressourcentyp in Direct3D 10/11. Hier ist ein Beispielcode angegeben, der zeigt, wie sie mithilfe der neuen Header auf die verschiedenen Mipmapebenen in einem Array von Texturen zugreifen.


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



## <a name="common-dds-file-resource-formats-and-associated-header-content"></a>Allgemeine DDS-Dateiformate und zugeordneter Headerinhalt



| Ressourcenformat                                                                            | dwFlags        | dwRGBBitCount | dwRBitMask | dwGBitMask | dwBBitMask | dwABitMask |
|--------------------------------------------------------------------------------------------|----------------|---------------|------------|------------|------------|------------|
| DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM<br/> D3DFMT \_ A8B8G8R8<br/>                       | DDS \_ RGBA      | 32            | 0xff       | 0xff00     | 0xff0000   | 0xff000000 |
| \_DXGI-FORMAT \_ R16G16 \_ UNORM<br/> D3DFMT \_ G16R16<br/>                           | DDS \_ RGBA      | 32            | 0xffff     | 0xffff0000 |            |            |
| \*\*<br/> DXGI \_ FORMAT \_ R10G10B10A2 \_ UNORM<br/> D3DFMT \_ A2B10G10R10<br/> | DDS \_ RGBA      | 32            | 0x3ff      | 0xffc00    | 0x3ff00000 |            |
| \_DXGI-FORMAT \_ R16G16 \_ UNORM<br/> D3DFMT \_ G16R16<br/>                           | DDS \_ RGB       | 32            | 0xffff     | 0xffff0000 |            |            |
| \_DXGI-FORMAT \_ B5G5R5A1 \_ UNORM<br/> D3DFMT \_ A1R5G5B5<br/>                       | DDS \_ RGBA      | 16            | 0x7c00     | 0x3e0      | 0x1f       | 0x8000     |
| \_DXGI-FORMAT \_ B5G6R5 \_ UNORM<br/> D3FMT \_ R5G6B5<br/>                            | DDS \_ RGB       | 16            | 0xf800     | 0x7e0      | 0x1f       |            |
| DXGI \_ A8 \_ UNORM<br/> D3DFMT \_ A8<br/>                                           | DDS \_ ALPHA     | 8             |            |            |            | 0xff       |
| D3DFMT \_ A8R8G8B8<br/>                                                                | DDS \_ RGBA      | 32            | 0xff0000   | 0xff00     | 0xff       | 0xff000000 |
| D3DFMT \_ X8R8G8B8<br/>                                                                | DDS \_ RGB       | 32            | 0xff0000   | 0xff00     | 0xff       |            |
| D3DFMT \_ X8B8G8R8<br/>                                                                | DDS \_ RGB       | 32            | 0xff       | 0xff00     | 0xff0000   |            |
| \*\*<br/> D3DFMT \_ A2R10G10B10<br/>                                             | DDS \_ RGBA      | 32            | 0x3ff00000 | 0xffc00    | 0x3ff      | 0xc0000000 |
| D3DFMT \_ R8G8B8<br/>                                                                  | DDS \_ RGB       | 24            | 0xff0000   | 0xff00     | 0xff       |            |
| D3DFMT \_ X1R5G5B5<br/>                                                                | DDS \_ RGB       | 16            | 0x7c00     | 0x3e0      | 0x1f       |            |
| D3DFMT \_ A4R4G4B4<br/>                                                                | DDS \_ RGBA      | 16            | 0xf00      | 0xf0       | 0xf        | 0xf000     |
| D3DFMT \_ X4R4G4B4<br/>                                                                | DDS \_ RGB       | 16            | 0xf00      | 0xf0       | 0xf        |            |
| D3DFMT \_ A8R3G3B2<br/>                                                                | DDS \_ RGBA      | 16            | 0xe0       | 0x1c       | 0x3        | 0xff00     |
| D3DFMT \_ A8L8<br/>                                                                    | \_DDS-LUDOMINANZ | 16            | 0xff       |            |            | 0xff00     |
| D3DFMT \_ L16<br/>                                                                     | \_DDS-LUDOMINANZ | 16            | 0xffff     |            |            |            |
| D3DFMT \_ L8<br/>                                                                      | \_DDS-LUDOMINANZ | 8             | 0xff       |            |            |            |
| D3DFMT \_ A4L4<br/>                                                                    | \_DDS-LUDOMINANZ | 8             | 0xf        |            |            | 0xf0       |



 



| Ressourcenformat                                                                             | dwFlags     | dwFourCC |
|---------------------------------------------------------------------------------------------|-------------|----------|
| DXGI \_ FORMAT \_ BC1 \_ UNORM<br/> D3DFMT \_ DXT1<br/>                                 | DDS \_ FOURCC | "DXT1"   |
| DXGI \_ FORMAT \_ BC2 \_ UNORM<br/> D3DFMT \_ DXT3<br/>                                 | DDS \_ FOURCC | "DXT3"   |
| DXGI \_ FORMAT \_ BC3 \_ UNORM<br/> D3DFMT \_ DXT5<br/>                                 | DDS \_ FOURCC | "DXT5"   |
| \*<br/> DXGI \_ FORMAT \_ BC4 \_ UNORM<br/>                                           | DDS \_ FOURCC | "BC4U"   |
| \*<br/> DXGI \_ FORMAT \_ BC4 \_ SNORM<br/>                                           | DDS \_ FOURCC | "BC4S"   |
| \*<br/> DXGI \_ FORMAT \_ BC5 \_ UNORM<br/>                                           | DDS \_ FOURCC | "ATI2"   |
| \*<br/> DXGI \_ FORMAT \_ BC5 \_ SNORM<br/>                                           | DDS \_ FOURCC | "BC5S"   |
| DXGI \_ FORMAT \_ R8G8 \_ B8G8 \_ UNORM<br/> D3DFMT \_ R8G8 \_ B8G8<br/>                    | DDS \_ FOURCC | "RGBG"   |
| DXGI \_ FORMAT \_ G8R8 \_ G8B8 \_ UNORM<br/> D3DFMT \_ G8R8 \_ G8B8<br/>                    | DDS \_ FOURCC | "GRGB"   |
| \*<br/> DXGI \_ FORMAT \_ R16G16B16A16 \_ UNORM<br/> D3DFMT \_ A16B16G16R16<br/>  | DDS \_ FOURCC | 36       |
| \*<br/> DXGI \_ FORMAT \_ R16G16B16A16 \_ SNORM<br/> D3DFMT \_ Q16W16V16U16<br/>  | DDS \_ FOURCC | 110      |
| \*<br/> DXGI \_ FORMAT \_ R16 \_ FLOAT<br/> D3DFMT \_ R16F<br/>                   | DDS \_ FOURCC | 111      |
| \*<br/> DXGI \_ FORMAT \_ R16G16 \_ FLOAT<br/> D3DFMT \_ G16R16F<br/>             | DDS \_ FOURCC | 112      |
| \*<br/> DXGI \_ FORMAT \_ R16G16B16A16 \_ FLOAT<br/> D3DFMT \_ A16B16G16R16F<br/> | DDS \_ FOURCC | 113      |
| \*<br/> DXGI \_ FORMAT \_ R32 \_ FLOAT<br/> D3DFMT \_ R32F<br/>                   | DDS \_ FOURCC | 114      |
| \*<br/> DXGI \_ FORMAT \_ R32G32 \_ FLOAT<br/> D3DFMT \_ G32R32F<br/>             | DDS \_ FOURCC | 115      |
| \*<br/> DXGI \_ FORMAT \_ R32G32B32A32 \_ FLOAT<br/> D3DFMT \_ A32B32G32R32F<br/> | DDS \_ FOURCC | 116      |
| D3DFMT \_ DXT2<br/>                                                                     | DDS \_ FOURCC | "DXT2"   |
| D3DFMT \_ DXT4<br/>                                                                     | DDS \_ FOURCC | "DXT4"   |
| D3DFMT \_ UYKVM<br/>                                                                     | DDS \_ FOURCC | "UYVIG"   |
| D3DFMT \_ YUY2<br/>                                                                     | DDS \_ FOURCC | "YUY2"   |
| D3DFMT \_ CxV8U8<br/>                                                                   | DDS \_ FOURCC | 117      |
| Beliebiges DXGI-Format                                                                             | DDS \_ FOURCC | "DX10"   |



 

\* = Ein stabiler DDS-Reader muss in der Lage sein, diese Legacyformatcodes zu verarbeiten. Ein solcher DDS-Reader sollte jedoch die Headererweiterung "DX10" verwenden, wenn er diese Formatcodes schreibt, um Mehrdeutigkeiten zu vermeiden.

\*\* = Aufgrund einiger langfristiger Probleme in gängigen Implementierungen von DDS-Readern und -Writern besteht die robusteste Möglichkeit zum Schreiben von Daten vom Typ 10:10:10:2 in der Verwendung der DX10-Headererweiterung mit dem [**DXGI \_ FORMAT-Code**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) "24" (d. h. dem DXGI \_ FORMAT \_ R10G10B10A2 \_ UNORM-Wert). D3DFMT \_ A2R10G10B10-Daten sollten in Daten des Typs 10:10:10:2 konvertiert werden, bevor sie als DXGI \_ FORMAT \_ R10G10B10A2-UNORM-Format-DDS-Datei geschrieben \_ werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Dds](dx-graphics-dds.md)
</dt> </dl>

 

