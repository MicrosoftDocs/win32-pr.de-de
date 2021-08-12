---
description: 'Dieser Abschnitt enthält Informationen zu den folgenden Effektsystemschnittstellen:'
ms.assetid: ebe0afc7-6261-4c96-a54e-9b491e240c03
title: Effektschnittstellen (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d07e6ecf45f4ef052c7d576849a55d00ef0f877dde7c41fa5dc80b7592761325
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118303973"
---
# <a name="effect-interfaces-direct3d-10"></a>Effektschnittstellen (Direct3D 10)

Dieser Abschnitt enthält Informationen zu den folgenden Effektsystemschnittstellen:



| Schnittstellen                                                                                     | Beschreibung                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**ID3D10EffectBlendVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectblendvariable)                       | Zugriff auf den Überblendzustand.                                            |
| [**ID3D10EffectConstantBuffer-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectconstantbuffer)                     | Greifen Sie auf einen Texturpuffer oder einen Konstantenpuffer zu.                  |
| [**ID3D10EffectDepthStencilVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilvariable)         | Zugriff auf den Tiefen-Schablonenzustand.                                    |
| [**ID3D10EffectDepthStencilViewVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilviewvariable) | Greifen Sie auf eine Tiefen-Schablonenansicht zu.                                   |
| [**ID3D10Effect-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)                                                 | Kapselt den Pipelinezustand in mindestens einer Renderingtechnik. |
| [**ID3D10Include-Schnittstelle**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))                                               | Vom Benutzer implementierte Methoden zum Lesen von Includedateien.              |
| [**ID3D10EffectMatrixVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectmatrixvariable)                     | Greifen Sie auf eine Matrix zu.                                               |
| [**ID3D10EffectPass-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpass)                                         | Kapselt den Effektzustand in einem Durchgang.                             |
| [**ID3D10EffectPool-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)                                         | Identifiziert Freigegebene Effektvariablen.                              |
| [**ID3D10EffectRasterizerVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrasterizervariable)             | Zugriff auf den Rasterizerzustand.                                       |
| [**ID3D10EffectRenderTargetViewVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrendertargetviewvariable) | Greifen Sie auf ein Renderziel zu.                                        |
| [**ID3D10EffectSamplerVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectsamplervariable)                   | Zugriff auf den Samplerzustand.                                          |
| [**ID3D10EffectScalarVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectscalarvariable)                     | Greifen Sie auf eine Skalarvariable zu.                                      |
| [**ID3D10EffectShaderResourceVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshaderresourcevariable)     | Greifen Sie auf eine Shaderressource zu.                                      |
| [**ID3D10EffectShaderVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshadervariable)                     | Greifen Sie auf eine Shadervariable zu.                                      |
| [**ID3D10EffectStringVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectstringvariable)                     | Greifen Sie auf eine Zeichenfolge zu.                                               |
| [**ID3D10EffectTechnique-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttechnique)                               | Kapselt einen oder mehrere Durchläufe.                                 |
| [**ID3D10EffectType-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttype)                                         | Implementiert Methoden für den Zugriff auf Effektvariablen.               |
| [**ID3D10EffectVectorVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvectorvariable)                     | Greifen Sie auf einen Vektor zu.                                               |



 

Es gibt zwei Arten von Schnittstellen im Effektframework: Renderingschnittstellen zum Rendern eines Effekts und Reflektionsschnittstellen zum Abrufen und Festlegen von Effektvariablen mit der API. Alle Reflektionsschnittstellen werden von [**ID3D10EffectVariable Interface (ID3D10EffectVariable-Schnittstelle) ableiten.**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Referenz zu Effekten](d3d10-graphics-reference-effect.md)
</dt> </dl>

 

 
