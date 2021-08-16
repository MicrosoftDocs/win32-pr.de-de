---
title: Effekte 11 Schnittstellen
description: Dieser Abschnitt enthält Referenzinformationen für die COM-Schnittstellen (Component Object Model) der Quelle Effects 11.
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

Dieser Abschnitt enthält Referenzinformationen für die COM-Schnittstellen (Component Object Model) der Quelle Effects 11.


## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ID3DX11Effect**](id3dx11effect.md)<br/>                                                       | Eine [**ID3DX11Effect-Schnittstelle**](id3dx11effect.md) verwaltet einen Satz von Zustandsobjekten, Ressourcen und Shadern für die Implementierung eines Renderingeffekts.<br/>                                                                                                                                                    |
| [**ID3DX11EffectBlendVariable**](id3dx11effectblendvariable.md)<br/>                             | Die Blend-Variable-Schnittstelle greifen auf den Blendzustand zu.<br/>                                                                                                                                                                                                                                                 |
| [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)<br/>             | Greifen Sie auf eine Klasseninstanz zu.<br/>                                                                                                                                                                                                                                                                         |
| [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)<br/>                           | Eine Konstantenpufferschnittstelle greifen auf konstante Puffer oder Texturpuffer zu.<br/>                                                                                                                                                                                                                          |
| [**ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md)<br/>               | Eine Tiefen-Schablonenvariablen-Schnittstelle greifen auf den Tiefen-Schablonenzustand zu.<br/>                                                                                                                                                                                                                                   |
| [**ID3DX11EffectDepthStencilViewVariable**](id3dx11effectdepthstencilviewvariable.md)<br/>       | Eine Tiefen-Schablonenansicht-Variable-Schnittstelle greifen auf eine Tiefen-Schablonenansicht zu.<br/>                                                                                                                                                                                                                             |
| [**ID3DX11EffectGroup**](id3dx11effectgroup.md)<br/>                                             | Die [**ID3DX11EffectGroup-Schnittstelle**](id3dx11effectgroup.md) greifen auf eine Effect-Gruppe zu.<br/> Die Lebensdauer eines [**ID3DX11EffectGroup-Objekts**](id3dx11effectgroup.md) entspricht der Lebensdauer des übergeordneten [**ID3DX11Effect-Objekts.**](id3dx11effect.md)<br/>                               |
| [**ID3DX11EffectInterfaceVariable**](id3dx11effectinterfacevariable.md)<br/>                     | Greifen Sie auf eine Schnittstellenvariable zu.<br/>                                                                                                                                                                                                                                                                    |
| [**ID3DX11EffectMatrixVariable**](id3dx11effectmatrixvariable.md)<br/>                           | Eine Matrixvariablenschnittstelle greifen auf eine Matrix zu.<br/>                                                                                                                                                                                                                                                     |
| [**ID3DX11EffectPass**](id3dx11effectpass.md)<br/>                                               | Eine [**ID3DX11EffectPass-Schnittstelle**](id3dx11effectpass.md) kapselt Zustandszuweisungen innerhalb einer Technik.<br/> Die Lebensdauer eines [**ID3DX11EffectPass-Objekts**](id3dx11effectpass.md) entspricht der Lebensdauer des übergeordneten [**ID3DX11Effect-Objekts.**](id3dx11effect.md)<br/>           |
| [**ID3DX11EffectRasterizerVariable**](id3dx11effectrasterizervariable.md)<br/>                   | Eine Rasterizer-Variable-Schnittstelle greifen auf den Rasterizerzustand zu.<br/>                                                                                                                                                                                                                                         |
| [**ID3DX11EffectRenderTargetViewVariable**](id3dx11effectrendertargetviewvariable.md)<br/>       | Eine Renderzielansichtsschnittstelle greifen auf ein Renderziel zu.<br/>                                                                                                                                                                                                                                           |
| [**ID3DX11EffectSamplerVariable**](id3dx11effectsamplervariable.md)<br/>                         | Eine Samplerschnittstelle greifen auf den Samplerzustand zu.<br/>                                                                                                                                                                                                                                                        |
| [**ID3DX11EffectScalarVariable**](id3dx11effectscalarvariable.md)<br/>                           | Eine Effect-Scalar-Variable-Schnittstelle greifen auf Skalarwerte zu.<br/>                                                                                                                                                                                                                                        |
| [**ID3DX11EffectShaderResourceVariable**](id3dx11effectshaderresourcevariable.md)<br/>           | Eine Shaderressourcenschnittstelle greifen auf eine Shaderressource zu.<br/>                                                                                                                                                                                                                                            |
| [**ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)<br/>                           | Eine Shadervariablenschnittstelle greifen auf eine Shadervariable zu.<br/>                                                                                                                                                                                                                                            |
| [**ID3DX11EffectStringVariable**](id3dx11effectstringvariable.md)<br/>                           | Eine Zeichenfolgenvariablenschnittstelle greifen auf eine Zeichenfolgenvariable zu.<br/>                                                                                                                                                                                                                                            |
| [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)<br/>                                     | Eine [**ID3DX11EffectTechnique-Schnittstelle**](id3dx11effecttechnique.md) ist eine Auflistung von Durchläufen.<br/> Die Lebensdauer eines [**ID3DX11EffectTechnique-Objekts**](id3dx11effecttechnique.md) entspricht der Lebensdauer des übergeordneten [**ID3DX11Effect-Objekts.**](id3dx11effect.md)<br/>               |
| [**ID3DX11EffectType**](id3dx11effecttype.md)<br/>                                               | Die [**ID3DX11EffectType-Schnittstelle**](id3dx11effecttype.md) greifen auf Effect-Variablen nach Typ zu.<br/> Die Lebensdauer eines [**ID3DX11EffectType-Objekts**](id3dx11effecttype.md) entspricht der Lebensdauer des übergeordneten [**ID3DX11Effect-Objekts.**](id3dx11effect.md)<br/>                          |
| [**ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md)<br/> | Greifen Sie auf eine ungeordnete Zugriffsansicht zu.<br/>                                                                                                                                                                                                                                                                 |
| [**ID3DX11EffectVariable**](id3dx11effectvariable.md)<br/>                                       | Die [**ID3DX11EffectVariable-Schnittstelle**](id3dx11effectvariable.md) ist die Basisklasse für alle Effektvariablen.<br/> Die Lebensdauer eines [**ID3DX11EffectVariable-Objekts**](id3dx11effectvariable.md) entspricht der Lebensdauer des übergeordneten [**ID3DX11Effect-Objekts.**](id3dx11effect.md)<br/> |
| [**ID3DX11EffectVectorVariable**](id3dx11effectvectorvariable.md)<br/>                           | Eine Vektorvariablenschnittstelle greifen auf einen Vektor mit vier Komponenten zu.<br/>                                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Referenz zu Effekten 11](d3d11-graphics-reference-effects11.md)
</dt> </dl>

 

 





