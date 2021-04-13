---
title: Effekte 11-Schnittstellen
description: Dieser Abschnitt enthält Referenzinformationen zu den COM-Schnittstellen (Component Object Model) der Effekte 11-Quelle.
ms.assetid: 1b997513-73f7-423a-8af3-1c9fa0d2f469
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 215e319720f2afc4cf74f6c49056de35fb59d004
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104976897"
---
# <a name="effects-11-interfaces"></a>Effekte 11-Schnittstellen

Dieser Abschnitt enthält Referenzinformationen zu den COM-Schnittstellen (Component Object Model) der Effekte 11-Quelle.


## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ID3DX11Effect**](id3dx11effect.md)<br/>                                                       | Eine [**ID3DX11Effect**](id3dx11effect.md) -Schnittstelle verwaltet einen Satz von Zustands Objekten, Ressourcen und Shadern zum Implementieren eines renderingeffekts.<br/>                                                                                                                                                    |
| [**ID3DX11EffectBlendVariable**](id3dx11effectblendvariable.md)<br/>                             | Die Blend-Variable-Schnittstelle greift auf Blend-Status zu.<br/>                                                                                                                                                                                                                                                 |
| [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)<br/>             | Greift auf eine Klasseninstanz zu.<br/>                                                                                                                                                                                                                                                                         |
| [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)<br/>                           | Eine Konstante Puffer Schnittstelle greift auf Konstante Puffer oder Textur Puffer zu.<br/>                                                                                                                                                                                                                          |
| [**ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md)<br/>               | Eine tiefen Schablone-Variablen-Schnittstelle greift auf den Status der tiefen Schablone zu.<br/>                                                                                                                                                                                                                                   |
| [**ID3DX11EffectDepthStencilViewVariable**](id3dx11effectdepthstencilviewvariable.md)<br/>       | Eine tiefen Schablone-View-Variable-Schnittstelle greift auf eine Ansicht der tiefen Schablone zu.<br/>                                                                                                                                                                                                                             |
| [**ID3DX11EffectGroup**](id3dx11effectgroup.md)<br/>                                             | Die [**ID3DX11EffectGroup**](id3dx11effectgroup.md) -Schnittstelle greift auf eine Effekt Gruppe zu.<br/> Die Lebensdauer eines [**ID3DX11EffectGroup**](id3dx11effectgroup.md) -Objekts entspricht der Lebensdauer seines übergeordneten [**ID3DX11Effect**](id3dx11effect.md) -Objekts.<br/>                               |
| [**ID3DX11EffectInterfaceVariable**](id3dx11effectinterfacevariable.md)<br/>                     | Greift auf eine Schnittstellen Variable zu.<br/>                                                                                                                                                                                                                                                                    |
| [**ID3DX11EffectMatrixVariable**](id3dx11effectmatrixvariable.md)<br/>                           | Eine Matrix Variable-Schnittstelle greift auf eine Matrix zu.<br/>                                                                                                                                                                                                                                                     |
| [**ID3DX11EffectPass**](id3dx11effectpass.md)<br/>                                               | Eine [**ID3DX11EffectPass**](id3dx11effectpass.md) -Schnittstelle kapselt Zustands Zuweisungen innerhalb eines Verfahrens.<br/> Die Lebensdauer eines [**ID3DX11EffectPass**](id3dx11effectpass.md) -Objekts entspricht der Lebensdauer seines übergeordneten [**ID3DX11Effect**](id3dx11effect.md) -Objekts.<br/>           |
| [**ID3DX11EffectRasterizerVariable**](id3dx11effectrasterizervariable.md)<br/>                   | Eine Raster-Variable-Schnittstelle greift auf den Status des Rasterizers zu.<br/>                                                                                                                                                                                                                                         |
| [**ID3DX11EffectRenderTargetViewVariable**](id3dx11effectrendertargetviewvariable.md)<br/>       | Eine Renderziel-View-Schnittstelle greift auf ein Renderziel zu.<br/>                                                                                                                                                                                                                                           |
| [**ID3DX11EffectSamplerVariable**](id3dx11effectsamplervariable.md)<br/>                         | Eine samplerschnittstelle greift auf den samplerstatus<br/>                                                                                                                                                                                                                                                        |
| [**ID3DX11EffectScalarVariable**](id3dx11effectscalarvariable.md)<br/>                           | Eine Effect-Skalarvariable-Schnittstelle greift auf skalare Werte zu.<br/>                                                                                                                                                                                                                                        |
| [**ID3DX11EffectShaderResourceVariable**](id3dx11effectshaderresourcevariable.md)<br/>           | Eine Shader-Resource-Schnittstelle greift auf eine Shaderressource zu.<br/>                                                                                                                                                                                                                                            |
| [**ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)<br/>                           | Eine Shader-Variable-Schnittstelle greift auf eine Shader-Variable zu.<br/>                                                                                                                                                                                                                                            |
| [**ID3DX11EffectStringVariable**](id3dx11effectstringvariable.md)<br/>                           | Eine Zeichen folgen Variable-Schnittstelle greift auf eine Zeichen folgen Variable zu.<br/>                                                                                                                                                                                                                                            |
| [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)<br/>                                     | Eine [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md) -Schnittstelle ist eine Auflistung von Durchläufen.<br/> Die Lebensdauer eines [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md) -Objekts entspricht der Lebensdauer seines übergeordneten [**ID3DX11Effect**](id3dx11effect.md) -Objekts.<br/>               |
| [**ID3DX11EffectType**](id3dx11effecttype.md)<br/>                                               | Die [**ID3DX11EffectType**](id3dx11effecttype.md) -Schnittstelle greift auf die Effekt Variablen nach Typ zu.<br/> Die Lebensdauer eines [**ID3DX11EffectType**](id3dx11effecttype.md) -Objekts entspricht der Lebensdauer seines übergeordneten [**ID3DX11Effect**](id3dx11effect.md) -Objekts.<br/>                          |
| [**ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md)<br/> | Greift auf eine ungeordnete Zugriffs Ansicht zu.<br/>                                                                                                                                                                                                                                                                 |
| [**ID3DX11EffectVariable**](id3dx11effectvariable.md)<br/>                                       | Die [**ID3DX11EffectVariable**](id3dx11effectvariable.md) -Schnittstelle ist die Basisklasse für alle Effekt Variablen.<br/> Die Lebensdauer eines [**ID3DX11EffectVariable**](id3dx11effectvariable.md) -Objekts entspricht der Lebensdauer seines übergeordneten [**ID3DX11Effect**](id3dx11effect.md) -Objekts.<br/> |
| [**ID3DX11EffectVectorVariable**](id3dx11effectvectorvariable.md)<br/>                           | Eine Vektor Variable-Schnittstelle greift auf einen vier-Komponenten-Vektor zu.<br/>                                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Auswirkung 11-Referenz](d3d11-graphics-reference-effects11.md)
</dt> </dl>

 

 





