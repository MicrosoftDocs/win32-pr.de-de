---
description: Frame buffer alpha-blending is a bit different than vertex alpha, material alpha, and texture alpha.
ms.assetid: 3664215d-ad03-400e-beab-b0421cf6b693
title: Frame Buffer Alpha (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec091e8cc42d6b21142d3b9372f6d2931ba25d1dfe12aa7717e0b09acf0b0718
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118297495"
---
# <a name="frame-buffer-alpha-direct3d-9"></a>Frame Buffer Alpha (Direct3D 9)

Frame buffer alpha-blending is a bit different than vertex alpha, material alpha, and texture alpha. Vertex-, Material- und Textur-Alphasatz-Transparenzwerte, die nur für die aktuelle Primitive verwendet werden und allein keine Auswirkungen auf andere Primitive haben. Das Alphablending des Framepuffers steuert, wie das aktuelle Primitiv mit vorhandenen Pixeln im Framepuffer kombiniert wird, um eine endgültige Pixelfarbe zu erzielen.

Beim Alphablending werden zwei Farben kombiniert: eine Quellfarbe und eine Zielfarbe. Die Quellfarbe stammt aus dem transparenten Objekt, die Zielfarbe ist die Farbe, die sich bereits an der Pixelposition befindet. Die Zielfarbe ist das Ergebnis des Renderns eines anderen Objekts, das sich hinter dem transparenten -Objekt befindet, d. b. das Objekt, das über das transparente Objekt sichtbar ist. Beim Alphablending wird eine Formel verwendet, um das Verhältnis zwischen Quell- und Zielobjekten zu steuern.


```
Final Color = ObjectColor * SourceBlendFactor + PixelColor * DestinationBlendFactor 
```



ObjectColor ist der Beitrag des Primitiven, der an der aktuellen Pixelposition gerendert wird. PixelColor ist der Beitrag des Framepuffers an der aktuellen Pixelposition.

Die Alphamischungsfaktoren, die verwendet werden können, sind unten aufgeführt.



| Blendmodusfaktor         | Beschreibung                                                                                                                                                                              |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DBLEND \_ ZERO            | (0, 0, 0, 0)                                                                                                                                                                             |
| D3DBLEND \_ ONE             | (1, 1, 1, 1)                                                                                                                                                                             |
| D3DBLEND \_ SRCCOLOR        | (Rs, Gs, Bs, As)                                                                                                                                                                         |
| D3DBLEND \_ INVSRCCOLOR     | (1 Rs, 1 Gs, 1-Bs, 1-As)                                                                                                                                                                 |
| D3DBLEND \_ SRCALPHA        | (As, As, As, As)                                                                                                                                                                         |
| D3DBLEND \_ INVSRCALPHA     | (1-As, 1-As, 1-As, 1-As)                                                                                                                                                                 |
| D3DBLEND \_ DESTALPHA       | (Ad, Ad, Ad, Ad)                                                                                                                                                                         |
| D3DBLEND \_ INVDESTALPHA    | (1-Ad, 1-Ad, 1-Ad, 1-Ad)                                                                                                                                                                 |
| D3DBLEND \_ DESTCOLOR       | (Rd, Gd, Bd, Ad)                                                                                                                                                                         |
| D3DBLEND \_ INVDESTCOLOR    | (1-Rd, 1-Gd, 1-Bd, 1-Ad)                                                                                                                                                                 |
| D3DBLEND \_ SRCALPHASAT     | (f, f, f, 1); f = min(As, 1-Ad)                                                                                                                                                          |
| D3DBLEND \_ BOTHSRCALPHA    | Für DirectX 6 und höher veraltet. Sie können den gleichen Effekt erzielen, indem Sie die Quell- und Zielmischungsfaktoren in separaten Aufrufen auf \_ D3DBLEND SRCALPHA und D3DBLEND \_ INVSRCALPHA festlegen. |
| D3DBLEND \_ BOTHINVSRCALPHA | Für DirectX 6 veraltet. Sie können den gleichen Effekt erzielen, indem Sie die Quell- und Zielmischungsfaktoren in separaten Aufrufen auf \_ D3DBLEND INVSRCALPHA und D3DBLEND \_ SRCALPHA festlegen.           |
| D3DBLEND \_ BLENDFACTOR     | Verwenden Sie color.r, color.g, color.b und color.a aus der D3DRS \_ BLENDFACTOR-Einstellung.                                                                                                 |
| D3DBLEND \_ INVBLENDFACTOR  | Verwenden Sie 1-color.r, 1-color.g, 1-color.b und 1-color.a aus der D3DRS \_ BLENDFACTOR-Einstellung.                                                                                         |



 

Direct3D verwendet den D3DRS \_ ALPHABLENDENABLE-Renderzustand, um alpha-Transparenzblending zu ermöglichen. Die Art der Alphamischung hängt von den D3DRS \_ SRCBLEND- und D3DRS \_ DESTBLEND-Renderzuständen ab. Quell- und Zielblendzustände werden paarweise verwendet. Das folgende Codefragment legt den Quellmischungszustand auf D3DBLEND SRCCOLOR und den Zielmischungszustand auf \_ D3DBLEND \_ INVSRCCOLOR fest.


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



Dieser Code führt eine lineare Mischung zwischen der Quellfarbe (der Farbe des Primitives, der an der aktuellen Position gerendert wird) und der Zielfarbe (der Farbe an der aktuellen Position im Framepuffer) aus. Das resultierende Erscheinungsbild ähnelt dem Tönungsglas, da ein Teil der Farbe des Zielobjekts über das Quellobjekt übertragen zu werden scheint. der Rest scheint ungn- und ungnend zu sein.

Viele dieser Überblendfaktoren erfordern Alphawerte in der Textur, um ordnungsgemäß zu funktionieren. Wenn Sie also Scheitelpunkt oder Material alpha verwenden, ist die Anwendung darauf beschränkt, welche Modi zu interessanten Ergebnissen führen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Alphablending](alpha-blending.md)
</dt> </dl>

 

 



