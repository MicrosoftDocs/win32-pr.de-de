---
description: Definiert die verschiedenen Typen von Oberflächen Formaten.
ms.assetid: a222e3bb-310c-4019-93ee-6a2da2a46ded
title: D3DFORMAT (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DFORMAT
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 228884435322992b8c87d20a9f351161f945c43c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762108"
---
# <a name="d3dformat"></a>D3DFORMAT

Definiert die verschiedenen Typen von Oberflächen Formaten.

``` syntax
typedef enum _D3DFORMAT {
    D3DFMT_UNKNOWN              =  0,

    D3DFMT_R8G8B8               = 20,
    D3DFMT_A8R8G8B8             = 21,
    D3DFMT_X8R8G8B8             = 22,
    D3DFMT_R5G6B5               = 23,
    D3DFMT_X1R5G5B5             = 24,
    D3DFMT_A1R5G5B5             = 25,
    D3DFMT_A4R4G4B4             = 26,
    D3DFMT_R3G3B2               = 27,
    D3DFMT_A8                   = 28,
    D3DFMT_A8R3G3B2             = 29,
    D3DFMT_X4R4G4B4             = 30,
    D3DFMT_A2B10G10R10          = 31,
    D3DFMT_A8B8G8R8             = 32,
    D3DFMT_X8B8G8R8             = 33,
    D3DFMT_G16R16               = 34,
    D3DFMT_A2R10G10B10          = 35,
    D3DFMT_A16B16G16R16         = 36,

    D3DFMT_A8P8                 = 40,
    D3DFMT_P8                   = 41,

    D3DFMT_L8                   = 50,
    D3DFMT_A8L8                 = 51,
    D3DFMT_A4L4                 = 52,

    D3DFMT_V8U8                 = 60,
    D3DFMT_L6V5U5               = 61,
    D3DFMT_X8L8V8U8             = 62,
    D3DFMT_Q8W8V8U8             = 63,
    D3DFMT_V16U16               = 64,
    D3DFMT_A2W10V10U10          = 67,

    D3DFMT_UYVY                 = MAKEFOURCC('U', 'Y', 'V', 'Y'),
    D3DFMT_R8G8_B8G8            = MAKEFOURCC('R', 'G', 'B', 'G'),
    D3DFMT_YUY2                 = MAKEFOURCC('Y', 'U', 'Y', '2'),
    D3DFMT_G8R8_G8B8            = MAKEFOURCC('G', 'R', 'G', 'B'),
    D3DFMT_DXT1                 = MAKEFOURCC('D', 'X', 'T', '1'),
    D3DFMT_DXT2                 = MAKEFOURCC('D', 'X', 'T', '2'),
    D3DFMT_DXT3                 = MAKEFOURCC('D', 'X', 'T', '3'),
    D3DFMT_DXT4                 = MAKEFOURCC('D', 'X', 'T', '4'),
    D3DFMT_DXT5                 = MAKEFOURCC('D', 'X', 'T', '5'),

    D3DFMT_D16_LOCKABLE         = 70,
    D3DFMT_D32                  = 71,
    D3DFMT_D15S1                = 73,
    D3DFMT_D24S8                = 75,
    D3DFMT_D24X8                = 77,
    D3DFMT_D24X4S4              = 79,
    D3DFMT_D16                  = 80,

    D3DFMT_D32F_LOCKABLE        = 82,
    D3DFMT_D24FS8               = 83,

#if !defined(D3D_DISABLE_9EX)
    D3DFMT_D32_LOCKABLE         = 84,
    D3DFMT_S8_LOCKABLE          = 85,
#endif // !D3D_DISABLE_9EX

    D3DFMT_L16                  = 81,

    D3DFMT_VERTEXDATA           =100,
    D3DFMT_INDEX16              =101,
    D3DFMT_INDEX32              =102,

    D3DFMT_Q16W16V16U16         =110,

    D3DFMT_MULTI2_ARGB8         = MAKEFOURCC('M','E','T','1'),

    D3DFMT_R16F                 = 111,
    D3DFMT_G16R16F              = 112,
    D3DFMT_A16B16G16R16F        = 113,

    D3DFMT_R32F                 = 114,
    D3DFMT_G32R32F              = 115,
    D3DFMT_A32B32G32R32F        = 116,

    D3DFMT_CxV8U8               = 117,

#if !defined(D3D_DISABLE_9EX)
    D3DFMT_A1                   = 118,
    D3DFMT_A2B10G10R10_XR_BIAS  = 119,
    D3DFMT_BINARYBUFFER         = 199,
#endif // !D3D_DISABLE_9EX

    D3DFMT_FORCE_DWORD          =0x7fffffff
} D3DFORMAT;
```

## <a name="remarks"></a>Bemerkungen

Es gibt verschiedene Arten von Formaten:

-   [BackBuffer-oder Anzeige Formate](#backbuffer-or-display-formats)
-   [Puffer Formate](#buffer-formats)
-   [Komprimierte DXTn-Textur Formate](#dxtn-compressed-texture-formats)
-   [Gleit Komma Formate](#floating-point-formats)
-   [FourCC-Formate](#fourcc-formats)
-   [IEEE-Formate](#ieee-formats)
-   [Gemischte Formate](#mixed-formats)
-   [Signierte Formate](#signed-formats)
-   [Nicht signierte Formate](#unsigned-formats)
-   [Andere](#other)

Alle Formate werden von links nach rechts, das wichtigste Bit bis zum niedrigsten Bit aufgelistet. **D3DFORMAT \_ ARGB** wird z. B. von dem signifikantesten bidirektional a (Alpha) bis zum am wenigsten signifikanten bidirektional B (Blue) geordnet. Beim Durchlaufen von Surface-Daten werden die Daten im Arbeitsspeicher von dem minimal signifikanten Bit bis zum signifikantesten Bit gespeichert. Dies bedeutet, dass die Channelreihenfolge im Speicher von der niedrigsten (blauen) bis zum höchst wertigen Bit (Alpha) ist.

Der Standardwert für Formate mit nicht definierten Kanälen (G16R16, A8 usw.) ist 1. Die einzige Ausnahme ist das A8-Format, das für die drei Farbkanäle mit dem Wert "000" initialisiert wird.

Die Reihenfolge der Bits basiert zuerst auf dem signifikantesten Byte, daher \_ gibt D3DFMT A8L8 an, dass das hohe Byte dieses 2-Byte-Formats Alpha ist. **D3DFMT \_ D16** gibt einen 16-Bit-ganzzahligen Wert und eine Anwendungs Sperr Bare Oberfläche an.

Pixel Formate wurden ausgewählt, um den Ausdruck von Hardwarehersteller definierten Erweiterungs Formaten zu aktivieren und die bewährte FourCC-Methode einzubeziehen. Der Satz von Formaten, der von der Direct3D-Laufzeit verstanden wird, wird von D3DFORMAT definiert.

Beachten Sie, dass die Formate von unabhängigen Hardwareanbietern (IHVs) bereitgestellt werden und dass viele FOURCC-Codes nicht aufgeführt sind. Die Formate in dieser Enumeration sind insofern eindeutig, als Sie von der Laufzeit sanktioniert werden, was bedeutet, dass der verweisrasterizer alle diese Typen verarbeitet. Von IHV bereitgestellte Formate werden von den einzelnen IHVs auf Karten Basis unterstützt.

### <a name="backbuffer-or-display-formats"></a>BackBuffer-oder Anzeige Formate

Diese Formate sind die einzigen gültigen Formate für einen Hintergrund Puffer oder eine Anzeige.



| Format      | Hintergrund Puffer | Anzeige                   |
|-------------|-------------|---------------------------|
| A2R10G10B10 | x           | x (nur Vollbildmodus) |
| A8R8G8B8    | x           |                           |
| X8R8G8B8    | x           | x                         |
| A1R5G5B5    | x           |                           |
| X1R5G5B5    | x           | x                         |
| R5G6B5      | x           | x                         |



 

### <a name="buffer-formats"></a>Puffer Formate

Tiefe, Schablone, Scheitelpunkt und Index Puffer verfügen jeweils über eindeutige Formate.



| Pufferflags               | Wert | Format                                                                                                                                        |
|----------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| **D3DFMT \_ D16 \_ Lockable**  | 70    | 16-Bit-z-Puffer-Bittiefe.                                                                                                                    |
| **D3DFMT \_ d32**            | 71    | 32-Bit-z-Puffer-Bittiefe.                                                                                                                    |
| **D3DFMT \_ D15S1**          | 73    | 16-Bit-z-Puffer-bidirektiontiefe, bei der 15 Bits für den tiefen Kanal reserviert sind und ein Bit für den Schablonen Kanal reserviert ist.                     |
| **D3DFMT \_ D24S8**          | 75    | 32-Bit-z-Puffer Bit Tiefe mit 24 Bits für den tiefen Kanal und 8 Bits für den Schablonen Kanal.                                             |
| **D3DFMT \_ D24X8**          | 77    | 32-Bit-z-Puffer Bit Tiefe mit 24 Bits für den tiefen Kanal.                                                                                |
| **D3DFMT \_ D24X4S4**        | 79    | 32-Bit-z-Puffer Bit Tiefe mit 24 Bits für den tiefen Kanal und 4 Bits für den Schablonen Kanal.                                             |
| **D3DFMT \_ D32F \_ Lockable** | 82    | Ein Sperr bares Format, bei dem der tiefen Wert als Standard-IEEE-Gleit Komma Zahl dargestellt wird.                                              |
| **D3DFMT \_ D24FS8**         | 83    | Ein nicht sperrbares Format, das 24 Bits Tiefe (in einem 24-Bit-Gleit Komma Format-20E4) und 8 Bits der Schablone enthält.                        |
| **D3DFMT \_ d32 \_ Lockable**  | 84    | Ein Sperr Bare 32-Bit-Tiefen Puffer. **Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:** Dieses Flag ist nur in Direct3D 9Ex verfügbar.<br/>  |
| **D3DFMT \_ S8 \_ Sperr fähig**   | 85    | Ein Sperr bares 8-Bit-Schablonen Puffer. **Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:** Dieses Flag ist nur in Direct3D 9Ex verfügbar.<br/> |
| **D3DFMT \_ D16**            | 80    | 16-Bit-z-Puffer-Bittiefe.                                                                                                                    |
| **D3DFMT \_ vertexdata**     | 100   | Beschreibt eine Vertex-Puffer Oberfläche.                                                                                                            |
| **D3DFMT \_ INDEX16**        | 101   | 16-Bit-Index-Puffer Bit Tiefe.                                                                                                                |
| **D3DFMT \_ INDEX32**        | 102   | 32-Bit-Bittiefe des Index Puffers.                                                                                                                |



 

Alle tiefen Schablonen Formate mit Ausnahme von D3DFMT \_ D16 \_ Lockable zeigen keine bestimmte bitreihen Folge pro Pixel an, und der Treiber kann mehr als die festgestellte Anzahl von Bits-pro-Tiefe-Kanälen (aber nicht Schablone-Kanal) beanspruchen.

### <a name="dxtn-compressed-texture-formats"></a>Komprimierte DXTn-Textur Formate

Diese Flags werden für komprimierte Texturen verwendet:



| Komprimierte DXTn-Textur-Flags | Wert                          | Format                          |
|-------------------------------|--------------------------------|---------------------------------|
| **D3DFMT \_ DXT1**              | Makefourcc ("d", "X", "'t", "1") | DXT1 Komprimierungs Textur Format |
| **D3DFMT \_ DXT2**              | Makefourcc ("d", "X", "'t", "2") | DXT2 Komprimierungs Textur Format |
| **D3DFMT \_ DXT3**              | Makefourcc ("d", "X", "'t", "3") | DXT3 Komprimierungs Textur Format |
| **D3DFMT \_ DXT4**              | Makefourcc ("d", "X", "'t", "4") | DXT4 Komprimierungs Textur Format |
| **D3DFMT \_ DXT5**              | Makefourcc ("d", "X", "t", "5") | DXT5 Komprimierungs Textur Format |



 

Die Laufzeit ermöglicht es einer Anwendung nicht, eine Oberfläche mit einem DXTn-Format zu erstellen, es sei denn, die Oberflächen Dimensionen sind Vielfachen von 4. Dies gilt für Offscreen-Plain-Flächen, Renderziele, 2D-Texturen, Cube-Texturen und volumetexturen.

### <a name="floating-point-formats"></a>Floating-Point Formate

Diese Flags werden für Gleit Komma Oberflächen Formate verwendet. Diese 16-Bit-pro-Kanal-Formate werden auch als s10e5-Formate bezeichnet.



| Gleit Komma-Flags      | Wert | Format                                                                                   |
|---------------------------|-------|------------------------------------------------------------------------------------------|
| **D3DFMT \_ R16F**          | 111   | 16-Bit-Float-Format mit 16 Bits für den roten Kanal.                                   |
| **D3DFMT \_ G16R16F**       | 112   | 32-Bit-Float-Format mit 16 Bits für den roten Kanal und 16 Bits für den grünen Kanal. |
| **D3DFMT \_ A16B16G16R16F** | 113   | 64-Bit-Float-Format mit 16 Bits für jeden Kanal (Alpha, blau, grün, rot).        |



 

### <a name="fourcc-formats"></a>FourCC-Formate

Daten in einem FourCC-Format sind komprimierte Daten.

### <a name="makefourcc"></a>Makefourcc

Ein Makro zum Erzeugen von vier Zeichen Codes folgt:

``` syntax
#define MAKEFOURCC(ch0, ch1, ch2, ch3)                              \
                ((DWORD)(BYTE)(ch0) | ((DWORD)(BYTE)(ch1) << 8) |   \
                ((DWORD)(BYTE)(ch2) << 16) | ((DWORD)(BYTE)(ch3) << 24 ))
```

Dies sind die definierten FourCC-Formate:



| FourCC-Flags              | Wert                          | Format                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **D3DFMT \_ MULTI2 \_ ARGB8** | Makefourcc ('m ', ' E ', 't ', ' 1 ')    | Multielement-Textur (nicht komprimiert)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **D3DFMT \_ G8R8 \_ G8B8**    | makefourcc ("g", "R", "g", "B") | Ein 16-Bit-gepacktes RGB-Format analog zu im YUY2 (Y0U0, Y1V0, Y2U2 usw.). Es ist ein Pixel-paar erforderlich, um den Farbwert ordnungsgemäß darzustellen. Das erste Pixel im Paar enthält 8 Bits von Grün (in den hohen 8 Bits) und 8 Bits rot (in den unteren 8 Bits). Das zweite Pixel enthält 8 Bits von Grün (in den großen 8 Bits) und 8 Bits blau (in den unteren 8 Bits). Gemeinsam haben die beiden Pixel die roten und blauen Komponenten gemeinsam, während jede über eine eindeutige grüne Komponente verfügt (G0R0, G1B0, G2R2 usw.). Der Textur Sampler normalisiert die Farben bei der Suche in einem Pixelshader nicht. Sie verbleiben im Bereich von 0,0 f bis 255.0 f. Dies gilt für alle programmierbaren Pixel-Shader-Modelle. Für den Pixel-Shader der Fixed-Funktion sollte die Hardware in den Bereich 0. f bis 1. f normalisieren und im Wesentlichen als im YUY2-Textur behandelt werden. Für Hardware, die dieses Format verfügbar macht, muss der PixelShader1xMaxValue-Member von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) auf einen Wert festgelegt sein, der diesen Bereich verarbeiten darf. |
| **D3DFMT \_ R8G8 \_ B8G8**    | makefourcc ("R", "g", "B", "g") | Ein 16-Bit-gepacktes RGB-Format analog zu UYVY (U0Y0, V0Y1, U2Y2 usw.). Es ist ein Pixel-paar erforderlich, um den Farbwert ordnungsgemäß darzustellen. Das erste Pixel im Paar enthält 8 Bits von Grün (in den unteren 8 Bits) und 8 Bits rot (in den hohen 8 Bits). Das zweite Pixel enthält 8 Bits von Grün (in den unteren 8 Bits) und 8 Bits von blau (in den hohen 8 Bits). Gemeinsam haben die beiden Pixel die roten und blauen Komponenten gemeinsam, während jede über eine eindeutige grüne Komponente verfügt (R0G0, B0G1, R2G2 usw.). Der Textur Sampler normalisiert die Farben bei der Suche in einem Pixelshader nicht. Sie verbleiben im Bereich von 0,0 f bis 255.0 f. Dies gilt für alle programmierbaren Pixel-Shader-Modelle. Für den Pixel-Shader der Fixed-Funktion sollte die Hardware in den Bereich 0. f bis 1. f normalisieren und im Wesentlichen als im YUY2-Textur behandelt werden. Für Hardware, die dieses Format verfügbar macht, muss der PixelShader1xMaxValue-Member von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) auf einen Wert festgelegt werden, der diesen Bereich verarbeiten darf.     |
| **D3DFMT \_ UYVY**          | makefourcc ("U", "y", "V", "y") | UYVY-Format (PC98-Konformität)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **D3DFMT \_ im YUY2**          | Makefourcc ("y", "U", "y", "2") | Im YUY2-Format (PC98-Konformität)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



 

### <a name="ieee-formats"></a>IEEE-Formate

Diese Flags werden für Gleit Komma Oberflächen Formate verwendet. Diese 32-Bits-pro-Channel-Formate werden auch als s23e8-Formate bezeichnet.



| Gleit Komma-Flags      | Wert | Format                                                                                   |
|---------------------------|-------|------------------------------------------------------------------------------------------|
| **D3DFMT \_ R32F**          | 114   | 32-Bit-Float-Format unter Verwendung von 32 Bits für den roten Kanal.                                   |
| **D3DFMT \_ G32R32F**       | 115   | 64-Bit-Float-Format unter Verwendung von 32 Bits für den roten Kanal und 32 Bits für den grünen Kanal. |
| **D3DFMT \_ A32B32G32R32F** | 116   | 128-Bit-Float-Format unter Verwendung von 32 Bits für jeden Kanal (Alpha, blau, grün, rot).       |



 

### <a name="mixed-formats"></a>Gemischte Formate

Daten in gemischten Formaten können eine Kombination aus nicht signierten Daten und signierten Daten enthalten.



| Gemischte Formatflags      | Wert | Format                                                                                         |
|-------------------------|-------|------------------------------------------------------------------------------------------------|
| **D3DFMT \_ L6V5U5**      | 61    | 16-Bit-Bump-Map-Format mit Leuchtkraft, das 6 Bits für die Leuchtkraft verwendet, und 5 Bits für v und Sie. |
| **D3DFMT \_ X8L8V8U8**    | 62    | 32-Bit-Bump-Map-Format mit der Leuchtkraft, wobei für jeden Kanal 8 Bits verwendet werden.                           |
| **D3DFMT \_ A2W10V10U10** | 67    | 32-Bit-Bump-Map-Format, bei dem 2 Bits für Alpha und 10 Bits für w, v und Sie verwendet werden.                |



 

### <a name="signed-formats"></a>Signierte Formate

Daten in einem signierten Format können sowohl positiv als auch negativ sein. Signierte Formate verwenden Kombinationen von (U), (V), (W) und (Q)-Daten.



| Signierte Formatflags      | Wert | Format                                                                                                    |
|--------------------------|-------|-----------------------------------------------------------------------------------------------------------|
| **D3DFMT \_ V8U8**         | 60    | 16-Bit-Bump-Map-Format mit jeweils 8 Bits für Sie und v-Daten.                                                |
| **D3DFMT \_ Q8W8V8U8**     | 63    | 32-Bit-Bump-Map-Format, bei dem für jeden Kanal 8 Bits verwendet werden.                                                     |
| **D3DFMT \_ V16U16**       | 64    | 32-Bit-Bump-Map-Format mit 16 Bits für jeden Kanal.                                                    |
| **D3DFMT \_ Q16W16V16U16** | 110   | 64-Bit-Bump-Map-Format mit 16 Bits für jede Komponente.                                                  |
| **D3DFMT \_ CxV8U8**       | 117   | normales 16-Bit-Komprimierungs Format. Der Textur Sampler berechnet den c-Kanal von: c = sqrt (1-U ²-V ²). |



 

### <a name="unsigned-formats"></a>Nicht signierte Formate

Daten in einem unsignierten Format müssen positiv sein. Unsignierte Formate verwenden Kombinationen von (R) Ed-, (G) Reen, (B) Lue, (A) lpha, (L) uminance und (P) Alette Daten. Palettendaten werden auch als Farb indizierte Daten bezeichnet, da die Daten zum Indizieren einer Farbpalette verwendet werden.



| Nicht signierte Formatflags             | Wert | Format                                                                                                                                                                    |
|-----------------------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **D3DFMT \_ R8G8B8**                | 20    | 24-Bit-RGB-Pixel-Format mit 8 Bits pro Kanal.                                                                                                                          |
| **D3DFMT \_ A8R8G8B8**              | 21    | 32-Bit-ARGB-Pixel Format mit Alpha, bei dem 8 Bits pro Kanal verwendet werden.                                                                                                            |
| **D3DFMT \_ X8R8G8B8**              | 22    | 32-Bit-RGB-Pixel Format, bei dem 8 Bits für jede Farbe reserviert sind.                                                                                                        |
| **D3DFMT \_ R5G6B5**                | 23    | 16-Bit-RGB-Pixel-Format mit 5 Bits für Rot, 6 Bits für Grün und 5 Bits für blau.                                                                                       |
| **D3DFMT \_ X1R5G5B5**              | 24    | 16-Bit-Pixel Format, bei dem 5 Bits für jede Farbe reserviert sind.                                                                                                             |
| **D3DFMT \_ A1R5G5B5**              | 25    | 16-Bit-Pixel Format, bei dem 5 Bits für jede Farbe reserviert sind und ein Bit für Alpha reserviert ist.                                                                             |
| **D3DFMT \_ A4R4G4B4**              | 26    | 16-Bit-ARGB-Pixel Format mit 4 Bits für jeden Kanal.                                                                                                                    |
| **D3DFMT \_ R3G3B2**                | 27    | 8-Bit-RGB-Textur Format mit 3 Bits für Rot, 3 Bits für Grün und 2 Bits für blau.                                                                                     |
| **D3DFMT \_ a8**                    | 28    | nur 8-Bit-Alpha.                                                                                                                                                         |
| **D3DFMT \_ A8R3G3B2**              | 29    | ein 16-Bit-ARGB-Textur Format mit 8 Bits für Alpha, 3 Bits für Rot und grün und 2 Bits für blau.                                                                    |
| **D3DFMT \_ X4R4G4B4**              | 30    | 16-Bit-RGB-Pixel-Format mit 4 Bits für jede Farbe.                                                                                                                      |
| **D3DFMT \_ A2B10G10R10**           | 31    | 32-Bit-Pixel Format mit 10 Bits für jede Farbe und 2 Bits für Alpha.                                                                                                    |
| **D3DFMT \_ A8B8G8R8**              | 32    | 32-Bit-ARGB-Pixel Format mit Alpha, bei dem 8 Bits pro Kanal verwendet werden.                                                                                                            |
| **D3DFMT \_ X8B8G8R8**              | 33    | 32-Bit-RGB-Pixel Format, bei dem 8 Bits für jede Farbe reserviert sind.                                                                                                        |
| **D3DFMT \_ G16R16**                | 34    | 32-Bit-Pixel Format mit jeweils 16 Bits für Grün und rot.                                                                                                                 |
| **D3DFMT \_ A2R10G10B10**           | 35    | 32-Bit-Pixel Format mit jeweils 10 Bits für Rot, grün und blau und 2 Bits für Alpha.                                                                                    |
| **D3DFMT \_ A16B16G16R16**          | 36    | 64-Bit-Pixel Format mit 16 Bits für jede Komponente.                                                                                                                     |
| **D3DFMT \_ A8P8**                  | 40    | 8-Bit-Farbe mit 8 Bits Alpha indiziert.                                                                                                                                 |
| **D3DFMT \_ P8**                    | 41    | 8-Bit-Farbe indiziert.                                                                                                                                                      |
| **D3DFMT \_ L8**                    | 50    | nur 8-Bit-Leuchtkraft.                                                                                                                                                     |
| **D3DFMT \_ L16**                   | 81    | nur 16-Bit-Leuchtkraft.                                                                                                                                                    |
| **D3DFMT \_ A8L8**                  | 51    | 16 Bit mit jeweils 8 Bits für Alpha und Leuchtkraft.                                                                                                                         |
| **D3DFMT \_ A4L4**                  | 52    | 8-Bit mit jeweils 4 Bits für Alpha und Leuchtkraft.                                                                                                                          |
| **D3DFMT \_ a1**                    | 118   | 1-Bit-Monochrome. **Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:** Dieses Flag ist nur in Direct3D 9Ex verfügbar.<br/>                                            |
| **D3DFMT \_ A2B10G10R10 \_ XR- \_ Bias** | 119   | 2,8-seitiger fester Punkt. **Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:** Dieses Flag ist nur in Direct3D 9Ex verfügbar.<br/>                                      |
| **D3DFMT \_ binaryBuffer**          | 199   | Binärformat, das angibt, dass die Daten keinen inhärenten Typ aufweisen. **Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:** Dieses Flag ist nur in Direct3D 9Ex verfügbar.<br/> |



 

### <a name="other"></a>Sonstiges

Dieses Flag wird für nicht definierte Formate verwendet.



| Andere Flags         | Wert | Format                    |
|---------------------|-------|---------------------------|
| **D3DFMT \_ unbekannt** | 0     | Das Oberflächen Format ist unbekannt. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




