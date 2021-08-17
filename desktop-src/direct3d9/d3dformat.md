---
description: Definiert die verschiedenen Typen von Oberflächenformaten.
ms.assetid: a222e3bb-310c-4019-93ee-6a2da2a46ded
title: D3DFORMAT (D3D9Types.h)
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
ms.openlocfilehash: ec3f934d9d94bfcc1129414b652de770d205b6e190b9f901c6e4f35768f59217
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117732402"
---
# <a name="d3dformat"></a>D3DFORMAT

Definiert die verschiedenen Typen von Oberflächenformaten.

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

## <a name="remarks"></a>Hinweise

Es gibt mehrere Arten von Formaten:

-   [BackBuffer- oder Anzeigeformate](#backbuffer-or-display-formats)
-   [Pufferformate](#buffer-formats)
-   [DXTn Compressed Texture Formats](#dxtn-compressed-texture-formats)
-   [Gleitkommaformate](#floating-point-formats)
-   [FOURCC-Formate](#fourcc-formats)
-   [IEEE-Formate](#ieee-formats)
-   [Gemischte Formate](#mixed-formats)
-   [Signierte Formate](#signed-formats)
-   [Formate ohne Vorzeichen](#unsigned-formats)
-   [Andere](#other)

Alle Formate werden von links nach rechts aufgeführt, das wichtigste Bit bis das am wenigsten signifikante Bit. Beispielsweise wird **D3DFORMAT \_ ARGB** vom wichtigsten Bitkanal A (Alpha) zum am wenigsten signifikanten Bitkanal B (blau) geordnet. Beim Durchlaufen von Oberflächendaten werden die Daten im Arbeitsspeicher vom am wenigsten signifikanten Bit zum höchstwertigsten Bit gespeichert. Dies bedeutet, dass die Kanal reihenfolge im Arbeitsspeicher von dem am wenigsten signifikanten Bit (blau) bis zum höchstwertigsten Bit (Alpha) liegt.

Der Standardwert für Formate, die nicht definierte Kanäle enthalten (G16R16, A8 und so weiter), ist 1. Die einzige Ausnahme ist das A8-Format, das für die drei Farbkanäle mit 000 initialisiert wird.

Die Reihenfolge der Bits liegt vom wichtigsten Byte an erster Stelle. D3DFMT A8L8 gibt daher an, dass das hohe Byte dieses \_ 2-Byte-Formats alpha ist. **D3DFMT \_ D16 gibt** einen 16-Bit-Ganzzahlwert und eine anwendungssperrbare Oberfläche an.

Pixelformate wurden ausgewählt, um den Ausdruck von vom Hardwareanbieter definierten Erweiterungsformaten zu aktivieren und die bewährte FOURCC-Methode ein beispielweise zu verwenden. Der Satz von Formaten, die von der Direct3D-Runtime verstanden werden, wird durch D3DFORMAT definiert.

Beachten Sie, dass Formate von unabhängigen Hardwareanbietern (Independent Hardware Vendors, IHVs) bereitgestellt werden und viele FOURCC-Codes nicht aufgeführt sind. Die Formate in dieser Enumeration sind eindeutig, da sie von der Laufzeit sanktioniert werden, was bedeutet, dass der Referenzraster für alle diese Typen verwendet wird. Von der IHV bereitgestellte Formate werden von den einzelnen IHVs kartenbasierte Unterstützt.

### <a name="backbuffer-or-display-formats"></a>BackBuffer- oder Anzeigeformate

Diese Formate sind die einzigen gültigen Formate für einen Hintergrundpuffer oder eine Anzeige.



| Format      | Zurück-Puffer | Anzeige                   |
|-------------|-------------|---------------------------|
| A2R10G10B10 | x           | x (nur Vollbildmodus) |
| A8R8G8B8    | x           |                           |
| X8R8G8B8    | x           | x                         |
| A1R5G5B5    | x           |                           |
| X1R5G5B5    | x           | x                         |
| R5G6B5      | x           | x                         |



 

### <a name="buffer-formats"></a>Pufferformate

Tiefen-, Schablonen-, Scheitelpunkt- und Indexpuffer haben jeweils eindeutige Formate.



| Pufferflags               | Wert | Format                                                                                                                                        |
|----------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| **D3DFMT \_ D16 \_ LOCKABLE**  | 70    | 16-Bit-Z-Pufferbittiefe.                                                                                                                    |
| **D3DFMT \_ D32**            | 71    | 32-Bit-Z-Pufferbittiefe.                                                                                                                    |
| **D3DFMT \_ D15S1**          | 73    | 16-Bit-Z-Pufferbittiefe, wobei 15 Bits für den Tiefenkanal und 1 Bit für den Schablonenkanal reserviert sind.                     |
| **D3DFMT \_ D24S8**          | 75    | 32-Bit-Z-Pufferbittiefe mit 24 Bits für den Tiefenkanal und 8 Bits für den Schablonenkanal.                                             |
| **D3DFMT \_ D24X8**          | 77    | 32-Bit-Z-Pufferbittiefe mit 24 Bits für den Tiefenkanal.                                                                                |
| **D3DFMT \_ D24X4S4**        | 79    | 32-Bit-Z-Pufferbittiefe mit 24 Bits für den Tiefenkanal und 4 Bits für den Schablonenkanal.                                             |
| **D3DFMT \_ D32F \_ LOCKABLE** | 82    | Ein sperrbares Format, in dem der Tiefenwert als IEEE-Standard-Gleitkommazahl dargestellt wird.                                              |
| **D3DFMT \_ D24FS8**         | 83    | Ein nicht sperrbares Format, das 24 Bits Tiefe (in einem 24-Bit-Gleitkommaformat – 20e4) und 8 Bits Schablone enthält.                        |
| **D3DFMT \_ D32 \_ LOCKABLE**  | 84    | Ein sperrbarer 32-Bit-Tiefenpuffer. **Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:** Dieses Flag ist nur in Direct3D 9Ex verfügbar.<br/>  |
| **D3DFMT \_ S8 \_ LOCKABLE**   | 85    | Ein sperrbarer 8-Bit-Schablonenpuffer. **Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:** Dieses Flag ist nur in Direct3D 9Ex verfügbar.<br/> |
| **D3DFMT \_ D16**            | 80    | 16-Bit-Z-Pufferbittiefe.                                                                                                                    |
| **D3DFMT \_ VERTEXDATA**     | 100   | Beschreibt eine Scheitelpunktpufferoberfläche.                                                                                                            |
| **D3DFMT \_ INDEX16**        | 101   | 16-Bit-Indexpufferbittiefe.                                                                                                                |
| **D3DFMT \_ INDEX32**        | 102   | 32-Bit-Indexpufferbittiefe.                                                                                                                |



 

Alle Tiefen-Schablonenformate mit Ausnahme von D3DFMT D16 LOCKABLE geben keine bestimmte Bit reihenfolge pro Pixel an, und der Treiber darf mehr als die angegebene Anzahl von Bits pro Tiefenkanal (aber keinen Schablonenkanal) \_ \_ verbrauchen.

### <a name="dxtn-compressed-texture-formats"></a>DXTn Compressed Texture Formats

Diese Flags werden für komprimierte Texturen verwendet:



| DXTn Compressed Texture flags (DXTn-Flags für komprimierte Texturen) | Wert                          | Format                          |
|-------------------------------|--------------------------------|---------------------------------|
| **D3DFMT \_ DXT1**              | MAKEFOURCC('D', 'X', 'T', '1') | DXT1-Komprimierungstexturformat |
| **D3DFMT \_ DXT2**              | MAKEFOURCC('D', 'X', 'T', '2') | DXT2-Komprimierungstexturformat |
| **D3DFMT \_ DXT3**              | MAKEFOURCC('D', 'X', 'T', '3') | DXT3-Komprimierungstexturformat |
| **D3DFMT \_ DXT4**              | MAKEFOURCC('D', 'X', 'T', '4') | DXT4-Komprimierungstexturformat |
| **D3DFMT \_ DXT5**              | MAKEFOURCC('D', 'X', 'T', '5') | DXT5-Komprimierungstexturformat |



 

Die Runtime lässt nicht zu, dass eine Anwendung eine Oberfläche mit einem DXTn-Format erstellt, es sei denn, die Oberflächendimensionen sind Vielfache von 4. Dies gilt für reine Offscreenoberflächen, Renderziele, 2D-Texturen, Cubetexturen und Volumetexturen.

### <a name="floating-point-formats"></a>Floating-Point Formate

Diese Flags werden für Gleitkommaoberflächenformate verwendet. Diese Formate mit 16 Bits pro Kanal werden auch als s10e5-Formate bezeichnet.



| Gleitkommaflags      | Wert | Format                                                                                   |
|---------------------------|-------|------------------------------------------------------------------------------------------|
| **D3DFMT \_ R16F**          | 111   | 16-Bit-Gleitkommaformat mit 16 Bits für den roten Kanal.                                   |
| **D3DFMT \_ G16R16F**       | 112   | 32-Bit-Gleitkommaformat mit 16 Bits für den roten Kanal und 16 Bits für den grünen Kanal. |
| **D3DFMT \_ A16B16G16R16F** | 113   | 64-Bit-Gleitkommaformat mit 16 Bits für jeden Kanal (Alpha, Blau, Grün, Rot).        |



 

### <a name="fourcc-formats"></a>FOURCC-Formate

Daten im FOURCC-Format sind komprimierte Daten.

### <a name="makefourcc"></a>MAKEFOURCC

Es folgt ein Makro zum Generieren von Vierzeichencodes:

``` syntax
#define MAKEFOURCC(ch0, ch1, ch2, ch3)                              \
                ((DWORD)(BYTE)(ch0) | ((DWORD)(BYTE)(ch1) << 8) |   \
                ((DWORD)(BYTE)(ch2) << 16) | ((DWORD)(BYTE)(ch3) << 24 ))
```

Hier sind die definierten FOURCC-Formate:



| FOURCC-Flags              | Wert                          | Format                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **D3DFMT \_ MULTI2 \_ ARGB8** | MAKEFOURCC('M','E','T','1')    | MultiElement-Textur (nicht komprimiert)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **D3DFMT \_ G8R8 \_ G8B8**    | MAKEFOURCC('G', 'R', 'G', 'B') | Ein 16-Bit-gepacktes RGB-Format analog zu YUY2 (Y0U0, Y1V0, Y2U2 und so weiter). Es ist ein Pixelpaar erforderlich, um den Farbwert ordnungsgemäß darstellen zu können. Das erste Pixel im Paar enthält 8 Bits grün (in den hohen 8 Bits) und 8 Bits Rot (in den unteren 8 Bits). Das zweite Pixel enthält 8 Bits grün (in den hohen 8 Bits) und 8 Bits blau (in den niedrigen 8 Bits). Zusammen teilen sich die beiden Pixel die roten und blauen Komponenten, während jedes über eine eindeutige grüne Komponente (G0R0, G1B0, G2R2 und so weiter) verfügt. Der Texturs sampler normalisiert die Farben nicht, wenn er in einen Pixel-Shader nach oben sucht. sie verbleiben im Bereich von 0,0f bis 255,0f. Dies gilt für alle programmierbaren Pixel-Shadermodelle. Für den Pixel-Shader der festen Funktion sollte sich die Hardware im Bereich von 0,f bis 1,f normalisieren und im Wesentlichen als YUY2-Textur behandeln. Für Hardware, die dieses Format verfügbar macht, muss das PixelShader1xMaxValue-Member von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) auf einen Wert festgelegt sein, der diesen Bereich behandeln kann. |
| **D3DFMT \_ R8G8 \_ B8G8**    | MAKEFOURCC('R', 'G', 'B', 'G') | Ein 16-Bit-gepacktes RGB-Format analog zu UY INTERNET (U0Y0, V0Y1, U2Y2 und so weiter). Es ist ein Pixelpaar erforderlich, um den Farbwert ordnungsgemäß darstellen zu können. Das erste Pixel im Paar enthält 8 Bits grün (in den unteren 8 Bits) und 8 Bits rot (in den hohen 8 Bits). Das zweite Pixel enthält 8 Bits grün (in den niedrigen 8 Bits) und 8 Bits blau (in den hohen 8 Bits). Zusammen teilen sich die beiden Pixel die roten und blauen Komponenten, während jede über eine eindeutige grüne Komponente (R0G0, B0G1, R2G2 und so weiter) verfügt. Der Texturs sampler normalisiert die Farben nicht, wenn er in einen Pixel-Shader nach oben sucht. sie verbleiben im Bereich von 0,0f bis 255,0f. Dies gilt für alle programmierbaren Pixel-Shadermodelle. Für den Pixel-Shader der festen Funktion sollte sich die Hardware im Bereich von 0,f bis 1,f normalisieren und im Wesentlichen als YUY2-Textur behandeln. Für Hardware, die dieses Format verfügbar macht, muss das PixelShader1xMaxValue-Member von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) auf einen Wert festgelegt sein, der diesen Bereich behandeln kann.     |
| **D3DFMT \_ UYKVM**          | MAKEFOURCC('U', 'Y', 'V', 'Y') | UYFOL-Format (PC98-Konformität)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **D3DFMT \_ YUY2**          | MAKEFOURCC('Y', 'U', 'Y', '2') | YUY2-Format (PC98-Konformität)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



 

### <a name="ieee-formats"></a>IEEE-Formate

Diese Flags werden für Gleitkommaoberflächenformate verwendet. Diese Formate mit 32 Bits pro Kanal werden auch als s23e8-Formate bezeichnet.



| Gleitkommaflags      | Wert | Format                                                                                   |
|---------------------------|-------|------------------------------------------------------------------------------------------|
| **D3DFMT \_ R32F**          | 114   | 32-Bit-Gleitkommaformat mit 32 Bits für den roten Kanal.                                   |
| **D3DFMT \_ G32R32F**       | 115   | 64-Bit-Gleitkommaformat mit 32 Bits für den roten Kanal und 32 Bits für den grünen Kanal. |
| **D3DFMT \_ A32B32G32R32F** | 116   | 128-Bit-Gleitkommaformat mit 32 Bits für jeden Kanal (Alpha, Blau, Grün, Rot).       |



 

### <a name="mixed-formats"></a>Gemischte Formate

Daten in gemischten Formaten können eine Kombination aus daten ohne Vorzeichen und signierten Daten enthalten.



| Flags im gemischten Format      | Wert | Format                                                                                         |
|-------------------------|-------|------------------------------------------------------------------------------------------------|
| **D3DFMT \_ L6V5U5**      | 61    | 16-Bit-Bumpmapformat mit Leuchtdichte mit 6 Bits für Leuchtdichte und jeweils 5 Bits für v und Sie. |
| **D3DFMT \_ X8L8V8U8**    | 62    | 32-Bit-Bumpmapformat mit Leuchtdichte mit 8 Bits für jeden Kanal.                           |
| **D3DFMT \_ A2W10V10U10** | 67    | 32-Bit-Bumpmapformat mit 2 Bits für Alpha und jeweils 10 Bits für w, v und Sie.                |



 

### <a name="signed-formats"></a>Signierte Formate

Daten in einem signierten Format können sowohl positiv als auch negativ sein. Signierte Formate verwenden Kombinationen aus (U), (V), (W) und (Q) Daten.



| Signierte Formatflags      | Wert | Format                                                                                                    |
|--------------------------|-------|-----------------------------------------------------------------------------------------------------------|
| **D3DFMT \_ V8U8**         | 60    | 16-Bit-Bumpmapformat mit jeweils 8 Bits für Sie und V-Daten.                                                |
| **D3DFMT \_ Q8W8V8U8**     | 63    | 32-Bit-Bumpmapformat mit 8 Bits für jeden Kanal.                                                     |
| **D3DFMT \_ V16U16**       | 64    | 32-Bit-Bumpmapformat mit 16 Bits für jeden Kanal.                                                    |
| **D3DFMT \_ Q16W16V16U16** | 110   | 64-Bit-Bumpmapformat mit 16 Bits für jede Komponente.                                                  |
| **D3DFMT \_ CxV8U8**       | 117   | Normales 16-Bit-Komprimierungsformat. Der Texturs sampler berechnet den C-Kanal aus: C = sqrt(1 - U%). |



 

### <a name="unsigned-formats"></a>Formate ohne Vorzeichen

Daten in einem Format ohne Vorzeichen müssen positiv sein. Für Formate ohne Vorzeichen werden Kombinationen aus (R)ed-, (G)reen-, (B)lue-, (A)lpha-, (L)udominanz- und (P)arill-Daten verwendet. Palettendaten werden auch als farbindizierte Daten bezeichnet, da die Daten zum Indizieren einer Farbpalette verwendet werden.



| Formatflags ohne Vorzeichen             | Wert | Format                                                                                                                                                                    |
|-----------------------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **D3DFMT \_ R8G8B8**                | 20    | 24-Bit-RGB-Pixelformat mit 8 Bits pro Kanal.                                                                                                                          |
| **D3DFMT \_ A8R8G8B8**              | 21    | 32-Bit-ARGB-Pixelformat mit Alpha mit 8 Bits pro Kanal.                                                                                                            |
| **D3DFMT \_ X8R8G8B8**              | 22    | 32-Bit-RGB-Pixelformat, wobei 8 Bits für jede Farbe reserviert sind.                                                                                                        |
| **D3DFMT \_ R5G6B5**                | 23    | 16-Bit-RGB-Pixelformat mit 5 Bits für Rot, 6 Bits für Grün und 5 Bits für Blau.                                                                                       |
| **D3DFMT \_ X1R5G5B5**              | 24    | 16-Bit-Pixelformat, in dem 5 Bits für jede Farbe reserviert sind.                                                                                                             |
| **D3DFMT \_ A1R5G5B5**              | 25    | 16-Bit-Pixelformat, bei dem 5 Bits für jede Farbe und 1 Bit für Alpha reserviert sind.                                                                             |
| **D3DFMT \_ A4R4G4B4**              | 26    | 16-Bit-ARGB-Pixelformat mit 4 Bits für jeden Kanal.                                                                                                                    |
| **D3DFMT \_ R3G3B2**                | 27    | 8-Bit-RGB-Texturformat mit 3 Bits für Rot, 3 Bits für Grün und 2 Bits für Blau.                                                                                     |
| **D3DFMT \_ A8**                    | 28    | Nur 8-Bit-Alpha.                                                                                                                                                         |
| **D3DFMT \_ A8R3G3B2**              | 29    | 16-Bit-ARGB-Texturformat mit 8 Bits für Alpha, jeweils 3 Bits für Rot und Grün und 2 Bits für Blau.                                                                    |
| **D3DFMT \_ X4R4G4B4**              | 30    | 16-Bit-RGB-Pixelformat mit 4 Bits für jede Farbe.                                                                                                                      |
| **D3DFMT \_ A2B10G10R10**           | 31    | 32-Bit-Pixelformat mit 10 Bits für jede Farbe und 2 Bits für Alpha.                                                                                                    |
| **D3DFMT \_ A8B8G8R8**              | 32    | 32-Bit-ARGB-Pixelformat mit Alpha mit 8 Bits pro Kanal.                                                                                                            |
| **D3DFMT \_ X8B8G8R8**              | 33    | 32-Bit-RGB-Pixelformat, wobei 8 Bits für jede Farbe reserviert sind.                                                                                                        |
| **D3DFMT \_ G16R16**                | 34    | 32-Bit-Pixelformat mit jeweils 16 Bits für Grün und Rot.                                                                                                                 |
| **D3DFMT \_ A2R10G10B10**           | 35    | 32-Bit-Pixelformat mit jeweils 10 Bits für Rot, Grün und Blau und 2 Bits für Alpha.                                                                                    |
| **D3DFMT \_ A16B16G16R16**          | 36    | 64-Bit-Pixelformat mit 16 Bits für jede Komponente.                                                                                                                     |
| **D3DFMT \_ A8P8**                  | 40    | 8-Bit-Farbe indiziert mit 8 Bits Alpha.                                                                                                                                 |
| **D3DFMT \_ P8**                    | 41    | 8-Bit-Farbe indiziert.                                                                                                                                                      |
| **D3DFMT \_ L8**                    | 50    | Nur 8-Bit-Leuchtdichte.                                                                                                                                                     |
| **D3DFMT \_ L16**                   | 81    | Nur 16-Bit-Leuchtdichte.                                                                                                                                                    |
| **D3DFMT \_ A8L8**                  | 51    | 16-Bit mit jeweils 8 Bits für Alpha- und Leuchtdichte.                                                                                                                         |
| **D3DFMT \_ A4L4**                  | 52    | 8-Bit mit jeweils 4 Bits für Alpha- und Leuchtdichte.                                                                                                                          |
| **D3DFMT \_ A1**                    | 118   | 1-Bit-Monotone. **Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:** Dieses Flag ist nur in Direct3D 9Ex verfügbar.<br/>                                            |
| **D3DFMT \_ A2B10G10R10 \_ XR \_ BIAS** | 119   | 2.8-Biased Fixed Point. **Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:** Dieses Flag ist nur in Direct3D 9Ex verfügbar.<br/>                                      |
| **D3DFMT \_ BINARYBUFFER**          | 199   | Binärformat, das angibt, dass die Daten keinen inhärenten Typ haben. **Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:** Dieses Flag ist nur in Direct3D 9Ex verfügbar.<br/> |



 

### <a name="other"></a>Andere

Dieses Flag wird für nicht definierte Formate verwendet.



| Andere Flags         | Wert | Format                    |
|---------------------|-------|---------------------------|
| **D3DFMT \_ UNKNOWN** | 0     | Das Oberflächenformat ist unbekannt. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




