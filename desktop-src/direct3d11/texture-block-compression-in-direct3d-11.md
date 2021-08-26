---
title: Texturblockkomprimierung in Direct3D 11
description: Die Unterstützung der Blockkomprimierung für Texturen wurde in Direct3D 11 um die BC6H- und BC7-Algorithmen erweitert.
ms.assetid: E0735D4E-9C0F-45DC-854A-C27EB8367D86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b52c2c764c0f9dca4021dcb14187db67e697cd7155701294a9c6214b4543d00b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027800"
---
# <a name="texture-block-compression-in-direct3d-11"></a>Texturblockkomprimierung in Direct3D 11

Die Unterstützung der Blockkomprimierung für Texturen wurde in Direct3D 11 um die BC6H- und BC7-Algorithmen erweitert. BC6H unterstützt Farbquelldaten mit hohem dynamischen Bereich, und BC7 bietet eine bessere als die durchschnittliche Qualitätskomprimierung mit weniger Artefakten für RGB-Standardquelldaten.

Ausführlichere Informationen zur Unterstützung von Blockkomprimierungsalgorithmen vor Direct3D 11, einschließlich Unterstützung für bc1 bis BC5-Formate, finden Sie unter [Blockkomprimierung (Direct3D 10).](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression)

**Hinweis zu Dateiformaten:** Die Texturkomprimierungsformate BC6H und BC7 verwenden das DDS-Dateiformat zum Speichern der komprimierten Texturdaten. Weitere Informationen finden Sie im [Programmierhandbuch für DDS.](/windows/desktop/direct3ddds/dx-graphics-dds-pguide)

## <a name="block-compression-formats-supported-in-direct3d-11"></a>In Direct3D 11 unterstützte Blockkomprimierungsformate



| Quelldaten                                  | Mindestens erforderliche Datenkomprimierungsauflösung                              | Empfohlenes Format | Unterstützte Mindestfunktionsebene |
|----------------------------------------------|---------------------------------------------------------------------------|--------------------|---------------------------------|
| Farbe mit drei Kanälen mit Alphakanal       | Drei Farbkanäle (5 Bits:6 Bits:5 Bits), mit 0 oder 1 Bit alpha  | BC1                | Direct3D 9.1                    |
| Farbe mit drei Kanälen mit Alphakanal       | Drei Farbkanäle (5 Bits:6 Bits:5 Bits), mit 4 Bit Alpha         | BU2                | Direct3D 9.1                    |
| Farbe mit drei Kanälen mit Alphakanal       | Drei Farbkanäle (5 Bits:6 Bits:5 Bits) mit 8 Bit Alpha          | BC3                | Direct3D 9.1                    |
| Einkanalfarbe                            | Ein Farbkanal (8 Bits)                                                | BC4                | Direct3D 10                     |
| Farbe mit zwei Kanälen                            | Zwei Farbkanäle (8 Bits:8 Bits)                                        | BC5                | Direct3D 10                     |
| HDR-Farbe (High Dynamic Range) mit drei Kanälen | Drei Farbkanäle (16 Bits:16 Bits:16 Bits) in "halber" Gleitkomma\* | BC6H               | Direct3D 11                     |
| Farbe mit drei Kanälen, Alphakanal optional  | Drei Farbkanäle (4 bis 7 Bits pro Kanal) mit 0 bis 8 Bit Alpha  | BC7                | Direct3D 11                     |



 

\*"Halb"-Gleitkomma ist ein 16-Bit-Wert, der aus einem optionalen Vorzeichenbit, einem 5-Bit-Exponenten und einer 10- oder 11-Bit-Mantisse besteht.

## <a name="bc1-bc2-and-b3-formats"></a>BC1-, BC2- und B3-Formate

Die Formate BC1, BC2 und BC3 entsprechen den Direct3D 9 DXTn-Texturkomprimierungsformaten und entsprechen den entsprechenden Direct3D 10 BC1-, BC2- und BC3-Formaten. Unterstützung für diese drei Formate ist für alle Featureebenen erforderlich (D3D \_ FEATURE \_ LEVEL \_ 9 \_ 1, D3D \_ FEATURE LEVEL \_ \_ 9 \_ 2, D3D \_ FEATURE LEVEL \_ \_ 9 \_ 3, D3D \_ FEATURE LEVEL \_ \_ 10 \_ 0, D3D \_ FEATURE LEVEL \_ \_ 10 \_ 1 und D3D \_ FEATURE LEVEL \_ \_ 11 \_ 0).



| Blockkomprimierungsformat | DXGI-Format                                                                           | Direct3D 9-äquivalentes Format                               | Bytes pro Block mit 4 x 4 Pixeln |
|--------------------------|---------------------------------------------------------------------------------------|------------------------------------------------------------|---------------------------|
| BC1                      | DXGI \_ FORMAT \_ BC1 \_ UNORM, DXGI \_ FORMAT \_ BC1 \_ UNORM \_ SRGB, DXGI \_ FORMAT \_ BC1 \_ TYPELESS | D3DFMT \_ DXT1, FourCC="DXT1"                                | 8                         |
| BU2                      | DXGI \_ FORMAT \_ BC2 \_ UNORM, DXGI \_ FORMAT \_ BC2 \_ UNORM \_ SRGB, DXGI \_ FORMAT \_ BC2 \_ TYPELESS | D3DFMT \_ DXT2 \* , FourCC="DXT2", D3DFMT \_ DXT3, FourCC="DXT3" | 16                        |
| BC3                      | DXGI \_ FORMAT \_ BC3 \_ UNORM, DXGI \_ FORMAT \_ BC3 \_ UNORM \_ SRGB, DXGI \_ FORMAT \_ BC3 \_ TYPELESS | D3DFMT \_ DXT4 \* , FourCC="DXT4", D3DFMT \_ DXT5, FourCC="DXT5" | 16                        |



 

\*Diese Komprimierungsschemas (DXT2 und DXT4) machen keinen Unterschied zwischen den vormultiplizierten Direct3D 9-Alphaformaten und den Standard-Alphaformaten. Diese Unterscheidung muss von den programmierbaren Shadern zur Renderzeit behandelt werden.

## <a name="bc4-and-bc5-formats"></a>BC4- und BC5-Formate



| Blockkomprimierungsformat | DXGI-Format                                                                     | Direct3D 9-äquivalentes Format | Bytes pro Block mit 4 x 4 Pixeln |
|--------------------------|---------------------------------------------------------------------------------|------------------------------|---------------------------|
| BC4                      | DXGI \_ FORMAT \_ BC4 \_ UNORM, DXGI \_ FORMAT \_ BC4 \_ SNORM, DXGI \_ FORMAT \_ BC4 \_ TYPELESS | FourCC="ATI1"                | 8                         |
| BC5                      | DXGI \_ FORMAT \_ BC5 \_ UNORM, DXGI \_ FORMAT \_ BC5 \_ SNORM, DXGI \_ FORMAT \_ BC5 \_ TYPELESS | FourCC="ATI2"                | 16                        |



 

## <a name="bc6h-format"></a>BC6H-Format

Ausführlichere Informationen zu diesem Format finden Sie in der Dokumentation zum [BC6H-Format.](bc6h-format.md)



| Blockkomprimierungsformat | DXGI-Format                                                                      | Direct3D 9-äquivalentes Format | Bytes pro Block mit 4 x 4 Pixeln |
|--------------------------|----------------------------------------------------------------------------------|------------------------------|---------------------------|
| BC6H                     | \_DXGI-FORMAT \_ BC6H \_ UF16, \_ DXGI-FORMAT \_ BC6H \_ SF16, \_ DXGI-FORMAT \_ BC6H \_ TYPLOS | Nicht zutreffend                          | 16                        |



 

Das BC6H-Format kann für jeden Block mit 4 x 4 Pixeln verschiedene Codierungsmodi auswählen. Insgesamt stehen 14 verschiedene Codierungsmodi zur Verfügung, die jeweils geringfügig unterschiedliche Vor- und Nachsichten in der resultierenden visuellen Qualität der angezeigten Textur aufweisen. Die Auswahl der Modi ermöglicht eine schnelle Decodierung durch die Hardware mit der Qualitätsstufe, die entsprechend dem Quellinhalt ausgewählt oder angepasst wurde, erhöht aber auch die Komplexität des Suchbereichs erheblich.

## <a name="bc7-format"></a>BC7-Format

Ausführlichere Informationen zu diesem Format finden Sie in der Dokumentation zum [BC7-Format.](bc7-format.md)



| Blockkomprimierungsformat | DXGI-Format                                                                           | Direct3D 9-äquivalentes Format | Bytes pro Block mit 4 x 4 Pixeln |
|--------------------------|---------------------------------------------------------------------------------------|------------------------------|---------------------------|
| BC7                      | DXGI \_ FORMAT \_ BC7 \_ UNORM, DXGI \_ FORMAT \_ BC7 \_ UNORM \_ SRGB, DXGI \_ FORMAT \_ BC7 \_ TYPELESS | Nicht zutreffend                          | 16                        |



 

Das BC7-Format kann für jeden Block mit 4 x 4 Pixeln verschiedene Codierungsmodi auswählen. Insgesamt sind 8 verschiedene Codierungsmodi verfügbar, die jeweils geringfügig unterschiedliche Vor- und Abkungen in der resultierenden visuellen Qualität der angezeigten Textur aufweisen. Die Wahl der Modi ermöglicht eine schnelle Decodierung durch die Hardware mit der Qualitätsstufe, die entsprechend dem Quellinhalt ausgewählt oder angepasst wurde, erhöht aber auch die Komplexität des Suchbereichs deutlich.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                 | BESCHREIBUNG                                                                                                                          |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [BC6H-Format](bc6h-format.md)<br/>                             | Das BC6H-Format ist ein Texturkomprimierungsformat, das zur Unterstützung von HDR-Farbräumen (High Dynamic Range) in Quelldaten entwickelt wurde.<br/> |
| [BC7-Format](bc7-format.md)<br/>                               | Das BC7-Format ist ein Texturkomprimierungsformat, das für die hochwertige Komprimierung von RGB- und RGBA-Daten verwendet wird.<br/>                    |
| [REFERENZ ZUM BC7-Formatmodus](bc7-format-mode-reference.md)<br/> | Diese Dokumentation enthält eine Liste der 8 Blockmodi und Bitzuordnungen für BC7-Texturkomprimierungsformatblöcke.<br/>    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Blockkomprimierung (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression)
</dt> <dt>

[Texturen](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

