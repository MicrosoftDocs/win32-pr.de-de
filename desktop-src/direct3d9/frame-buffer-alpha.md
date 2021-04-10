---
description: Die Alpha Mischung des Frame Puffers unterscheidet sich von Scheitelpunkt Alpha, Material Alpha und Textur Alpha.
ms.assetid: 3664215d-ad03-400e-beab-b0421cf6b693
title: Frame-Puffer Alpha (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb310e2c66f43282e65425fd0d6c6a24961accaa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123859"
---
# <a name="frame-buffer-alpha-direct3d-9"></a>Frame-Puffer Alpha (Direct3D 9)

Die Alpha Mischung des Frame Puffers unterscheidet sich von Scheitelpunkt Alpha, Material Alpha und Textur Alpha. Vertex, Material und Textur-Alpha legen Transparenzwerte fest, die nur für den aktuellen primitiven verwendet werden und selbst keine Auswirkung auf andere primitive haben. Mit dem Frame Puffer Alpha-Blending wird gesteuert, wie das aktuelle primitive mit vorhandenen Pixeln im Frame Puffer kombiniert wird, um eine endgültige Pixelfarbe zu erzielen.

Beim Durchführen einer Alpha Mischung werden zwei Farben kombiniert: eine Quellfarbe und eine Zielfarbe. Die Quellfarbe wird vom transparenten Objekt abgeleitet, die Zielfarbe ist die Farbe, die sich bereits am Pixel Speicherort befindet. Die Zielfarbe ist das Ergebnis des Renderings eines anderen Objekts hinter dem transparenten Objekt, d. h. dem Objekt, das durch das transparente Objekt sichtbar ist. Alpha Blending verwendet eine Formel, um das Verhältnis zwischen den Quell-und Ziel Objekten zu steuern.


```
Final Color = ObjectColor * SourceBlendFactor + PixelColor * DestinationBlendFactor 
```



Objectcolor ist der Beitrag des primitiven, der an der aktuellen Pixelposition gerendert wird. Pixel Color ist der Beitrag des Frame Puffers an der aktuellen Pixelposition.

Eine Reihe von Alpha Blend-Faktoren, die verwendet werden können, sind unten aufgeführt.



| Blend-modusfaktor         | BESCHREIBUNG                                                                                                                                                                              |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DBLEND \_ 0            | (0, 0, 0, 0)                                                                                                                                                                             |
| D3DBLEND \_             | (1, 1, 1, 1)                                                                                                                                                                             |
| D3DBLEND \_ srccolor        | (RS, GS, SB, as)                                                                                                                                                                         |
| D3DBLEND- \_ invsrccolor     | (1-RS, 1-GS, 1-SB, 1-AS)                                                                                                                                                                 |
| D3DBLEND \_ srcalpha        | (AS, as, as, as)                                                                                                                                                                         |
| D3DBLEND- \_ invsrcalpha     | (1-AS, 1-AS, 1-AS, 1-AS)                                                                                                                                                                 |
| D3DBLEND \_ -Debug       | (AD, AD, AD, AD)                                                                                                                                                                         |
| D3DBLEND- \_ invwastalpha    | (1-AD, 1-AD, 1-AD, 1-AD)                                                                                                                                                                 |
| D3DBLEND \_ destcolor       | (RD, GD, BD, AD)                                                                                                                                                                         |
| D3DBLEND \_ invdestcolor    | (1-RD, 1-GD, 1-BD, 1-AD)                                                                                                                                                                 |
| D3DBLEND \_ srcalphasat     | (f, f, f, 1); f = min (AS, 1-AD)                                                                                                                                                          |
| D3DBLEND \_ bothsrcalpha    | Veraltet für DirectX 6 und höher. Sie können denselben Effekt erzielen, indem Sie die Quell-und Ziel-Blend-Faktoren auf D3DBLEND \_ srcalpha und D3DBLEND \_ invsrcalpha in separaten Aufrufen festlegen. |
| D3DBLEND \_ bothinvsrcalpha | Veraltet für DirectX 6. Sie können denselben Effekt erzielen, indem Sie die Quell-und Ziel-Blend-Faktoren \_ in separaten Aufrufen auf D3DBLEND invsrcalpha und D3DBLEND \_ srcalpha festlegen.           |
| D3DBLEND \_ blendfactor     | Verwenden Sie "Color. r", "Color. g", "Color. b" und "Color. a" aus der D3DRS \_ blendfactor-Einstellung.                                                                                                 |
| D3DBLEND- \_ invblendfactor  | Verwenden Sie 1-Color. r, 1-Color. g, 1-Color. b und 1-Color. a aus der D3DRS \_ blendfactor-Einstellung.                                                                                         |



 

Direct3D verwendet den D3DRS \_ AlphaBlendEnable-Rendering-Status, um Alpha-Transparenz-Blending zu aktivieren. Der Typ der durchgeführten Alpha Mischung hängt von den D3DRS \_ srcblend-und D3DRS \_ destblend-Rendering-Zuständen ab. Quell-und Ziel-Blend-Zustände werden paarweise verwendet. Mit dem folgenden Code Fragment wird der Source Blend-Status auf D3DBLEND \_ srccolor und den Ziel-Blend-Zustand auf D3DBLEND \_ invsrccolor festgelegt.


```
// This code fragment assumes that lpD3DDevice is a 
//   valid pointer to a device.

// Enable alpha blending.
lpD3DDevice->SetRenderState(D3DRS_ALPHABLENDENABLE, 
                            TRUE);

// Set the source blend state.
lpD3DDevice->SetRenderState(D3DRS_SRCBLEND, 
                            D3DBLEND_SRCCOLOR);

// Set the destination blend state.
lpD3DDevice->SetRenderState(D3DRS_DESTBLEND, 
                            D3DBLEND_INVSRCCOLOR);
```



Dieser Code führt eine lineare Mischung zwischen der Quellfarbe (die Farbe des primitiven, das an der aktuellen Position gerendert wird) und der Zielfarbe (die Farbe an der aktuellen Position im Frame Puffer) aus. Die resultierende Darstellung ähnelt einem duktglas, wenn ein Teil der Farbe des Zielobjekts über das Quell Objekt übertragen wird. der Rest der Datei wird anscheinend aufgenommen.

Viele dieser Blend-Faktoren erfordern, dass Alpha Werte in der Textur ordnungsgemäß funktionieren. Daher ist die Anwendung bei Verwendung von Scheitelpunkt oder Material Alpha beschränkt, auf welche Modi interessante Ergebnisse erzeugt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Alpha Blending](alpha-blending.md)
</dt> </dl>

 

 



