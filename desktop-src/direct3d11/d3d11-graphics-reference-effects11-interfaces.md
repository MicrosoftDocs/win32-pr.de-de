---
title: Effekte 11 Schnittstellen
description: Dieser Abschnitt enthält Referenzinformationen für die COM-Schnittstellen (Component Object Model) der Effects 11-Quelle.
ms.assetid: 1b997513-73f7-423a-8af3-1c9fa0d2f469
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b20713f5a40b2d8b85edb92166b7e64af18fefee62e5267adcffa25356c6f7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118537702"
---
# <a name="effects-11-interfaces"></a>Effekte 11 Schnittstellen

Dieser Abschnitt enthält Referenzinformationen für die COM-Schnittstellen (Component Object Model) der Effects 11-Quelle.


## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                   | Beschreibung                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ID3DX11Effect**](id3dx11effect.md)<br/>                                                       | Eine [**ID3DX11Effect-Schnittstelle**](id3dx11effect.md) verwaltet eine Reihe von Zustandsobjekten, Ressourcen und Shadern für die Implementierung eines Renderingeffekts.<br/>                                                                                                                                                    |
| [**ID3DX11EffectBlendVariable**](id3dx11effectblendvariable.md)<br/>                             | Die Blend-Variable-Schnittstelle greift auf den Blendzustand zu.<br/>                                                                                                                                                                                                                                                 |
| [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)<br/>             | Greift auf eine Klasseninstanz zu.<br/>                                                                                                                                                                                                                                                                         |
| [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)<br/>                           | Eine Konstante-Puffer-Schnittstelle greift auf Konstantenpuffer oder Texturpuffer zu.<br/>                                                                                                                                                                                                                          |
| [**ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md)<br/>               | Eine Tiefenschablonenvariablenschnittstelle greift auf den Tiefenschablonenzustand zu.<br/>                                                                                                                                                                                                                                   |
| [**ID3DX11EffectDepthStencilViewVariable**](id3dx11effectdepthstencilviewvariable.md)<br/>       | Eine Tiefenschablonenansicht-Variable-Schnittstelle greift auf eine Tiefenschablonenansicht zu.<br/>                                                                                                                                                                                                                             |
| [**ID3DX11EffectGroup**](id3dx11effectgroup.md)<br/>                                             | Die [**ID3DX11EffectGroup-Schnittstelle**](id3dx11effectgroup.md) greift auf eine Effect-Gruppe zu.<br/> Die Lebensdauer eines [**ID3DX11EffectGroup-Objekts**](id3dx11effectgroup.md) entspricht der Lebensdauer des übergeordneten [**ID3DX11Effect-Objekts.**](id3dx11effect.md)<br/>                               |
| [**ID3DX11EffectInterfaceVariable**](id3dx11effectinterfacevariable.md)<br/>                     | Greift auf eine Schnittstellenvariable zu.<br/>                                                                                                                                                                                                                                                                    |
| [**ID3DX11EffectMatrixVariable**](id3dx11effectmatrixvariable.md)<br/>                           | Eine Matrixvariablenschnittstelle greift auf eine Matrix zu.<br/>                                                                                                                                                                                                                                                     |
| [**ID3DX11EffectPass**](id3dx11effectpass.md)<br/>                                               | Eine [**ID3DX11EffectPass-Schnittstelle**](id3dx11effectpass.md) kapselt Zustandszuweisungen innerhalb einer Technik.<br/> Die Lebensdauer eines [**ID3DX11EffectPass-Objekts**](id3dx11effectpass.md) entspricht der Lebensdauer des übergeordneten [**ID3DX11Effect-Objekts.**](id3dx11effect.md)<br/>           |
| [**ID3DX11EffectRasterizerVariable**](id3dx11effectrasterizervariable.md)<br/>                   | Eine Rasterizer-Variable-Schnittstelle greift auf den Rasterizerzustand zu.<br/>                                                                                                                                                                                                                                         |
| [**ID3DX11EffectRenderTargetViewVariable**](id3dx11effectrendertargetviewvariable.md)<br/>       | Eine Schnittstelle für render-target-view greift auf ein Renderziel zu.<br/>                                                                                                                                                                                                                                           |
| [**ID3DX11EffectSamplerVariable**](id3dx11effectsamplervariable.md)<br/>                         | Eine Samplerschnittstelle greift auf den Samplerzustand zu.<br/>                                                                                                                                                                                                                                                        |
| [**ID3DX11EffectScalarVariable**](id3dx11effectscalarvariable.md)<br/>                           | Eine Effect-Scalar-Variable-Schnittstelle greift auf Skalarwerte zu.<br/>                                                                                                                                                                                                                                        |
| [**ID3DX11EffectShaderResourceVariable**](id3dx11effectshaderresourcevariable.md)<br/>           | Eine Shader-Ressourcenschnittstelle greift auf eine Shaderressource zu.<br/>                                                                                                                                                                                                                                            |
| [**ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)<br/>                           | Eine Shadervariablenschnittstelle greift auf eine Shadervariable zu.<br/>                                                                                                                                                                                                                                            |
| [**ID3DX11EffectStringVariable**](id3dx11effectstringvariable.md)<br/>                           | Eine Zeichenfolgenvariablenschnittstelle greift auf eine Zeichenfolgenvariable zu.<br/>                                                                                                                                                                                                                                            |
| [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)<br/>                                     | Eine [**ID3DX11EffectTechnique-Schnittstelle**](id3dx11effecttechnique.md) ist eine Sammlung von Durchläufen.<br/> Die Lebensdauer eines [**ID3DX11EffectTechnique-Objekts**](id3dx11effecttechnique.md) entspricht der Lebensdauer des übergeordneten [**ID3DX11Effect-Objekts.**](id3dx11effect.md)<br/>               |
| [**ID3DX11EffectType**](id3dx11effecttype.md)<br/>                                               | Die [**ID3DX11EffectType-Schnittstelle**](id3dx11effecttype.md) greift auf Effektvariablen nach Typ zu.<br/> Die Lebensdauer eines [**ID3DX11EffectType-Objekts**](id3dx11effecttype.md) entspricht der Lebensdauer des übergeordneten [**ID3DX11Effect-Objekts.**](id3dx11effect.md)<br/>                          |
| [**ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md)<br/> | Greift auf eine ungeordnete Zugriffsansicht zu.<br/>                                                                                                                                                                                                                                                                 |
| [**ID3DX11EffectVariable**](id3dx11effectvariable.md)<br/>                                       | Die [**ID3DX11EffectVariable-Schnittstelle**](id3dx11effectvariable.md) ist die Basisklasse für alle Effektvariablen.<br/> Die Lebensdauer eines [**ID3DX11EffectVariable-Objekts**](id3dx11effectvariable.md) entspricht der Lebensdauer des übergeordneten [**ID3DX11Effect-Objekts.**](id3dx11effect.md)<br/> |
| [**ID3DX11EffectVectorVariable**](id3dx11effectvectorvariable.md)<br/>                           | Eine Vektorvariablenschnittstelle greift auf einen Vektor mit vier Komponenten zu.<br/>                                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Referenz zu Effekten 11](d3d11-graphics-reference-effects11.md)
</dt> </dl>

 

 





