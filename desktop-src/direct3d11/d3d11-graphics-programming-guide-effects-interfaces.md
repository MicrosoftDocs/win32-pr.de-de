---
title: Effect-System Schnittstellen (Direct3D 11)
description: Das Effect-System definiert mehrere Schnittstellen zur Verwaltung des Wirkungs Zustands.
ms.assetid: 5cba6055-d153-4837-9a08-96efbde5f48f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af76a54be06e52e320743ca945abb31d1d50d213
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708544"
---
# <a name="effect-system-interfaces-direct3d-11"></a>Effect-System Schnittstellen (Direct3D 11)

Das Effect-System definiert mehrere Schnittstellen zur Verwaltung des Wirkungs Zustands. Es gibt zwei Arten von Schnittstellen: solche, die von der Laufzeit verwendet werden, um einen Effekt und reflektionsschnittstellen zum erhalten und Festlegen von Effekt Variablen zu erzeugen.

-   [Lauf Zeit Schnittstellen von Effekten](#effect-runtime-interfaces)
-   [Effekt reflektionseschnittstellen](#effect-reflection-interfaces)

## <a name="effect-runtime-interfaces"></a>Lauf Zeit Schnittstellen von Effekten

Verwenden Sie Lauf Zeit Schnittstellen zum Rendering eines Effekts.



| Lauf Zeit Schnittstellen                                       | BESCHREIBUNG                                                    |
|----------------------------------------------------------|----------------------------------------------------------------|
| [**ID3DX11Effect**](id3dx11effect.md)                   | Sammlung von einer oder mehreren Gruppen und Techniken zum Rendern. |
| [**ID3DX11EffectPass**](id3dx11effectpass.md)           | Eine Auflistung von Zustands Zuweisungen.                             |
| [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md) | Eine Auflistung von einem oder mehreren Durchläufen.                            |
| [**ID3DX11EffectGroup**](id3dx11effectgroup.md)         | Eine Auflistung von einer oder mehreren Techniken.                        |



 

## <a name="effect-reflection-interfaces"></a>Effekt reflektionseschnittstellen

Reflektion wird im Effektsystem implementiert, um das Lesen (und schreiben) des Wirkungs Zustands zu unterstützen. Es gibt mehrere Möglichkeiten, auf Wirkungs Variablen zuzugreifen.

### <a name="setting-groups-of-effect-state"></a>Festlegen von Gruppen von Effekt Zuständen

Verwenden Sie diese Schnittstellen, um eine Gruppe des Zustands zu erhalten und festzulegen.



| Reflektionseschnittstellen                                                          | BESCHREIBUNG                      |
|--------------------------------------------------------------------------------|----------------------------------|
| [**ID3DX11EffectBlendVariable**](id3dx11effectblendvariable.md)               | Get-und Set-Blend-Zustand.         |
| [**ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md) | Get und Set tiefen Schablone State. |
| [**ID3DX11EffectRasterizerVariable**](id3dx11effectrasterizervariable.md)     | Get-und Set-Status des Rasterizers.    |
| [**ID3DX11EffectSamplerVariable**](id3dx11effectsamplervariable.md)           | Holen Sie sich den samplerzustand.       |



 

### <a name="setting-effect-resources"></a>Festlegen von Effekt Ressourcen

Verwenden Sie diese Schnittstellen, um Ressourcen zu erhalten und festzulegen.



| Reflektionseschnittstellen                                                                        | BESCHREIBUNG                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)                           | Zugreifen auf Daten in einem Textur Puffer oder Konstantenpuffer. |
| [**ID3DX11EffectDepthStencilViewVariable**](id3dx11effectdepthstencilviewvariable.md)       | Zugreifen auf Daten in einer tiefen Schablone-Ressource.            |
| [**ID3DX11EffectRenderTargetViewVariable**](id3dx11effectrendertargetviewvariable.md)       | Zugreifen auf Daten in einem Renderziel.                     |
| [**ID3DX11EffectShaderResourceVariable**](id3dx11effectshaderresourcevariable.md)           | Zugreifen auf Daten in einer Shaderressource.                   |
| [**ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md) | Zugreifen auf Daten in einer ungeordneten Zugriffs Ansicht.            |



 

### <a name="setting-other-effect-variables"></a>Festlegen anderer Effekt Variablen

Verwenden Sie diese Schnittstellen, um den Status anhand des Variablen Typs zu erhalten und festzulegen.



| Reflektionseschnittstellen                                                            | BESCHREIBUNG               |
|----------------------------------------------------------------------------------|---------------------------|
| [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md) | Eine Klasseninstanz erhalten.     |
| [**ID3DX11EffectInterfaceVariable**](id3dx11effectinterfacevariable.md)         | Sie erhalten eine Schnittstelle und legen Sie fest. |
| [**ID3DX11EffectMatrixVariable**](id3dx11effectmatrixvariable.md)               | Gibt eine Matrix an und legt Sie fest.     |
| [**ID3DX11EffectScalarVariable**](id3dx11effectscalarvariable.md)               | Ein Skalarwert wird abgerufen und festgelegt.     |
| [**ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)               | Eine shadervariable erhalten.    |
| [**ID3DX11EffectStringVariable**](id3dx11effectstringvariable.md)               | Gibt eine Zeichenfolge zurück und legt Sie fest.     |
| [**ID3DX11EffectType**](id3dx11effecttype.md)                                   | Einen Variablentyp erhalten.      |
| [**ID3DX11EffectVectorVariable**](id3dx11effectvectorvariable.md)               | Get und Set a Vector.     |



 

Alle Reflektionsobjekte werden von [**ID3DX11EffectVariable**](id3dx11effectvariable.md)abgeleitet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effekte (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> <dt>

[Programmieranleitung für Direct3D 11](dx-graphics-overviews.md)
</dt> </dl>

 

 




