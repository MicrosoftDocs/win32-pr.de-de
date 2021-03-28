---
title: Textur Block Komprimierung in Direct3D 11
description: Block Komprimierungs Unterstützung (BC) für Texturen wurde in Direct3D 11 erweitert, um die BC6H-und bzw bc7-Algorithmen einzubeziehen.
ms.assetid: E0735D4E-9C0F-45DC-854A-C27EB8367D86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f80a22c97c8a706a3825abfb4ac2b5133c1a9beb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101727"
---
# <a name="texture-block-compression-in-direct3d-11"></a>Textur Block Komprimierung in Direct3D 11

Block Komprimierungs Unterstützung (BC) für Texturen wurde in Direct3D 11 erweitert, um die BC6H-und bzw bc7-Algorithmen einzubeziehen. BC6H unterstützt Datenquellen Daten mit hoher dynamischer Bereichs Farbe, und bzw bc7 bietet eine bessere Qualitäts Komprimierung mit weniger Artefakten für Standard-RGB-Quelldaten.

Spezifischere Informationen zur Unterstützung von Block Komprimierungs Algorithmen vor Direct3D 11, einschließlich der Unterstützung für die BC1 bis BC5-Formate, finden Sie unter [Block Komprimierung (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression).

**Beachten Sie die folgenden Dateiformate:** Die Textur Komprimierungs Formate BC6H und bzw bc7 verwenden das DDS-Dateiformat zum Speichern der komprimierten Textur Daten. Weitere Informationen finden Sie im [Programmier Handbuch für DDS](/windows/desktop/direct3ddds/dx-graphics-dds-pguide) .

## <a name="block-compression-formats-supported-in-direct3d-11"></a>In Direct3D 11 unterstützte Block Komprimierungs Formate



| Quelldaten                                  | Mindestens erforderliche Daten Komprimierungs Auflösung                              | Empfohlenes Format | Unterstützte Mindestfunktionsebene |
|----------------------------------------------|---------------------------------------------------------------------------|--------------------|---------------------------------|
| Drei-Kanal-Farbe mit Alphakanal       | Drei Farbkanäle (5 Bits: 6 Bits: 5 Bits) mit 0 oder 1 Bit (s) von Alpha  | BC1                | Direct3D 9,1                    |
| Drei-Kanal-Farbe mit Alphakanal       | Drei Farbkanäle (5 Bits: 6 Bits: 5 Bits) mit 4 Bits Alpha         | BU2                | Direct3D 9,1                    |
| Drei-Kanal-Farbe mit Alphakanal       | Drei Farbkanäle (5 Bits: 6 Bits: 5 Bits) mit 8 Bits von Alpha          | BC3                | Direct3D 9,1                    |
| One-Channel-Farbe                            | Ein Farbkanal (8 Bits)                                                | BC4                | Direct3D 10                     |
| Farbe mit zwei Kanälen                            | Zwei Farbkanäle (8 Bits: 8 Bits)                                        | BC5                | Direct3D 10                     |
| Breite des dynamischen Bereichs mit drei Kanälen (HDR) | Drei Farbkanäle (16 Bits: 16 Bits: 16 Bits) im "halben" Gleit Komma\* | BC6H               | Direct3D 11                     |
| Drei-Kanal-Farbe, Alphakanal optional  | Drei Farbkanäle (4 bis 7 Bits pro Kanal) mit 0 bis 8 Bits von Alpha  | Bzw bc7                | Direct3D 11                     |



 

\*"Half" Floating Point ist ein 16-Bit-Wert, der aus einem optionalen Signier Bit, einem 5-Bit-Exponenten Exponenten und einer 10-oder 11-Bit-Mantisse besteht.

## <a name="bc1-bc2-and-b3-formats"></a>BC1-, BC2-und B3-Formate

Die BC1-, BC2-und BC3-Formate entsprechen den Direct3D 9 DXTn-Textur Komprimierungs Formaten und sind identisch mit den entsprechenden Formaten Direct3D 10 BC1, BC2 und BC3. Die Unterstützung für diese drei Formate ist für alle featureebenen erforderlich (D3D \_ Feature \_ Level \_ 9 \_ 1, D3D \_ Feature \_ Level \_ 9 \_ 2, D3D \_ Feature \_ Level \_ 9 \_ 3, D3D \_ Feature \_ Level \_ 10 \_ 0, D3D \_ Feature \_ Level \_ 10 \_ 1 und D3D \_ Feature \_ Level \_ 11 \_ 0).



| Block Komprimierungs Format | DXGI-Format                                                                           | Direct3D 9 entsprechendes Format                               | Bytes pro 4X4-Pixel Block |
|--------------------------|---------------------------------------------------------------------------------------|------------------------------------------------------------|---------------------------|
| BC1                      | DXGI- \_ Format \_ BC1 \_ unorm, DXGI- \_ Format \_ BC1 \_ unorm \_ sRGB, DXGI- \_ Format \_ BC1 \_ typlose | D3DFMT \_ DXT1, FourCC = "DXT1"                                | 8                         |
| BU2                      | DXGI- \_ Format \_ BC2 \_ unorm, DXGI- \_ Format \_ BC2 \_ unorm \_ sRGB, DXGI- \_ Format \_ BC2 \_ typlose | D3DFMT \_ DXT2 \* , FourCC = "DXT2", D3DFMT \_ DXT3, FourCC = "DXT3" | 16                        |
| BC3                      | DXGI- \_ Format \_ BC3 \_ unorm, DXGI- \_ Format \_ BC3 \_ unorm \_ sRGB, DXGI- \_ Format \_ BC3 \_ typlose | D3DFMT \_ DXT4 \* , FourCC = "DXT4", D3DFMT \_ DXT5, FourCC = "DXT5" | 16                        |



 

\*Diese Komprimierungs Schemas (DXT2 und DXT4) unterscheiden sich nicht zwischen den vorab multiplizierten Alpha Formaten Direct3D 9 und den Alpha Formaten Standard. Dieser Unterschied muss von den programmierbaren Shadern zur Rendering-Zeit behandelt werden.

## <a name="bc4-and-bc5-formats"></a>BC4-und BC5-Formate



| Block Komprimierungs Format | DXGI-Format                                                                     | Direct3D 9 entsprechendes Format | Bytes pro 4X4-Pixel Block |
|--------------------------|---------------------------------------------------------------------------------|------------------------------|---------------------------|
| BC4                      | DXGI- \_ Format \_ BC4 \_ unorm, DXGI- \_ Format \_ BC4 \_ snorm, DXGI- \_ Format \_ BC4 \_ typlose | FourCC = "ATI1"                | 8                         |
| BC5                      | DXGI- \_ Format \_ BC5 \_ unorm, DXGI- \_ Format \_ BC5 \_ snorm, DXGI- \_ Format \_ BC5 \_ typlose | FourCC = "ati2"                | 16                        |



 

## <a name="bc6h-format"></a>BC6H-Format

Ausführlichere Informationen zu diesem Format finden Sie in der Dokumentation zum [BC6H-Format](bc6h-format.md) .



| Block Komprimierungs Format | DXGI-Format                                                                      | Direct3D 9 entsprechendes Format | Bytes pro 4X4-Pixel Block |
|--------------------------|----------------------------------------------------------------------------------|------------------------------|---------------------------|
| BC6H                     | DXGI- \_ Format \_ BC6H \_ UF16, DXGI- \_ Format \_ BC6H \_ SF16, DXGI- \_ Format \_ BC6H \_ typlose | –                          | 16                        |



 

Das BC6H-Format kann für jeden 4 x 4-Pixel Block verschiedene Codierungs Modi auswählen. Es sind insgesamt 14 verschiedene Codierungs Modi verfügbar, von denen jedes in der resultierenden visuellen Qualität der angezeigten Textur etwas andere Kompromisse hat. Die Auswahl der Modi ermöglicht eine schnelle Decodierung durch die Hardware, bei der die Qualitätsstufe entsprechend dem Quell Inhalt ausgewählt oder angepasst wird, aber auch die Komplexität des Suchraums erheblich erhöht.

## <a name="bc7-format"></a>Bzw bc7-Format

Ausführlichere Informationen zu diesem Format finden Sie in der Dokumentation zum [bzw bc7-Format](bc7-format.md) .



| Block Komprimierungs Format | DXGI-Format                                                                           | Direct3D 9 entsprechendes Format | Bytes pro 4X4-Pixel Block |
|--------------------------|---------------------------------------------------------------------------------------|------------------------------|---------------------------|
| Bzw bc7                      | DXGI- \_ Format \_ bzw bc7 \_ unorm, DXGI- \_ Format \_ bzw bc7 \_ unorm \_ sRGB, DXGI- \_ Format \_ bzw bc7 \_ typlose | –                          | 16                        |



 

Das bzw bc7-Format kann für jeden 4 x 4-Pixel Block verschiedene Codierungs Modi auswählen. Es sind insgesamt 8 verschiedene Codierungs Modi verfügbar, von denen jede in der resultierenden visuellen Qualität der angezeigten Textur etwas abweicht. Die Auswahl der Modi ermöglicht eine schnelle Decodierung durch die Hardware, bei der die Qualitätsstufe entsprechend dem Quell Inhalt ausgewählt oder angepasst wird, aber auch die Komplexität des Suchraums erheblich erhöht.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                 | BESCHREIBUNG                                                                                                                          |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [BC6H-Format](bc6h-format.md)<br/>                             | Das BC6H-Format ist ein Textur Komprimierungs Format, das für die Unterstützung von HDR-Farbräumen (High Dynamic Range) in Quelldaten konzipiert ist.<br/> |
| [Bzw bc7-Format](bc7-format.md)<br/>                               | Das bzw bc7-Format ist ein Textur Komprimierungs Format, das für die hochwertige Komprimierung von RGB-und RGBA-Daten verwendet wird.<br/>                    |
| [Bzw bc7-formatmodusverweis](bc7-format-mode-reference.md)<br/> | Diese Dokumentation enthält eine Liste der 8 Block Modi und bitbelegungen für bzw bc7 Textur Komprimierungs-Format Blöcke.<br/>    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Block Komprimierung (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression)
</dt> <dt>

[Texturen](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

