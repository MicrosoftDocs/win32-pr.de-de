---
description: 'Dieser Abschnitt enthält Informationen zu den folgenden Effekten: Systemschnittstellen:'
ms.assetid: ebe0afc7-6261-4c96-a54e-9b491e240c03
title: Effekt Schnittstellen (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1946e7b9e3711bf2d79c0876efca1c533e0ff4ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748016"
---
# <a name="effect-interfaces-direct3d-10"></a>Effekt Schnittstellen (Direct3D 10)

Dieser Abschnitt enthält Informationen zu den folgenden Effekten: Systemschnittstellen:



| Schnittstellen                                                                                     | BESCHREIBUNG                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**ID3D10EffectBlendVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectblendvariable)                       | Greift auf Blend-Status zu.                                            |
| [**ID3D10EffectConstantBuffer-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectconstantbuffer)                     | Greift auf einen Textur Puffer oder einen konstanten Puffer zu.                  |
| [**ID3D10EffectDepthStencilVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilvariable)         | Greift auf den Status der tiefen Schablone zu.                                    |
| [**ID3D10EffectDepthStencilViewVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilviewvariable) | Greift auf eine Ansicht der tiefen Schablone zu.                                   |
| [**ID3D10Effect-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)                                                 | Kapselt den Pipeline Status in mindestens einem Renderingverfahren. |
| [**ID3D10Include-Schnittstelle**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))                                               | Vom Benutzer implementierte Methoden zum Lesen von Includedateien.              |
| [**ID3D10EffectMatrixVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectmatrixvariable)                     | Greift auf eine Matrix zu.                                               |
| [**ID3D10EffectPass-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpass)                                         | Kapselt den Effekt Zustand in einem Durchlauf.                             |
| [**ID3D10EffectPool-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)                                         | Identifiziert Variablen mit gemeinsam genutzten Effekten.                              |
| [**ID3D10EffectRasterizerVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrasterizervariable)             | Greift auf den Status des Rasterizers zu.                                       |
| [**ID3D10EffectRenderTargetViewVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrendertargetviewvariable) | Greift auf ein Renderziel zu.                                        |
| [**ID3D10EffectSamplerVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectsamplervariable)                   | Greift auf den Sampler-Zustand zu                                          |
| [**ID3D10EffectScalarVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectscalarvariable)                     | Greift auf eine skalare Variable zu.                                      |
| [**ID3D10EffectShaderResourceVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshaderresourcevariable)     | Greift auf eine Shaderressource zu.                                      |
| [**ID3D10EffectShaderVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshadervariable)                     | Greift auf eine Shader-Variable zu.                                      |
| [**ID3D10EffectStringVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectstringvariable)                     | Greift auf eine Zeichenfolge zu.                                               |
| [**ID3D10EffectTechnique-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttechnique)                               | Kapselt einen oder mehrere Durchgänge.                                 |
| [**ID3D10EffectType-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttype)                                         | Implementiert Methoden für den Zugriff auf Wirkungs Variablen.               |
| [**ID3D10EffectVectorVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvectorvariable)                     | Greift auf einen Vektor zu.                                               |



 

Es gibt zwei Arten von Schnittstellen im Effect-Framework: renderingschnittstellen zum Rendern von Effekten und reflektionsschnittstellen zum erhalten und Festlegen von Effekt Variablen mit der API. Alle Reflexions Schnittstellen werden von der [**ID3D10EffectVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable)abgeleitet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effekt Referenz](d3d10-graphics-reference-effect.md)
</dt> </dl>

 

 
