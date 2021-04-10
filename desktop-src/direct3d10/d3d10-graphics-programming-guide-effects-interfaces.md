---
description: 'Das Effect-System definiert mehrere Schnittstellen zur Verwaltung des Wirkungs Zustands. Es gibt zwei Arten von Schnittstellen: solche, die von der Laufzeit verwendet werden, um einen Effekt und reflektionsschnittstellen zum erhalten und Festlegen von Effekt Variablen zu erzeugen.'
ms.assetid: 068d49d2-0e14-4080-9fee-20d984f22545
title: Effect-System Schnittstellen (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b40b21d98bedaec65550343260e7c52e2df1c302
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126325"
---
# <a name="effect-system-interfaces-direct3d-10"></a>Effect-System Schnittstellen (Direct3D 10)

Das Effect-System definiert mehrere Schnittstellen zur Verwaltung des Wirkungs Zustands. Es gibt zwei Arten von Schnittstellen: solche, die von der Laufzeit verwendet werden, um einen Effekt und reflektionsschnittstellen zum erhalten und Festlegen von Effekt Variablen zu erzeugen.

-   [Lauf Zeit Schnittstellen von Effekten](#effect-runtime-interfaces)
-   [Effekt reflektionseschnittstellen](#effect-reflection-interfaces)

## <a name="effect-runtime-interfaces"></a>Lauf Zeit Schnittstellen von Effekten

Verwenden Sie Lauf Zeit Schnittstellen zum Rendering eines Effekts.



| Lauf Zeit Schnittstellen                                               | BESCHREIBUNG                                                          |
|------------------------------------------------------------------|----------------------------------------------------------------------|
| [**ID3D10Effect-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)                   | Sammlung von einer oder mehreren Techniken zum Rendern.                  |
| [**ID3D10Include-Schnittstelle**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))                 | Eine Schnittstelle zum Hinzufügen benutzerdefinierter Verhalten beim Lesen von Includedateien. |
| [**ID3D10EffectPass-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpass)           | Eine Auflistung von Zustands Zuweisungen.                                   |
| [**ID3D10EffectPool-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)           | Erstellen Sie einen Speicherort für Variablen, die zwischen Effekten gemeinsam verwendet werden sollen. |
| [**ID3D10EffectTechnique-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttechnique) | Eine Auflistung von einem oder mehreren Durchläufen.                                  |



 

## <a name="effect-reflection-interfaces"></a>Effekt reflektionseschnittstellen

Reflektion wird im Effektsystem implementiert, um das Lesen (und schreiben) des Wirkungs Zustands zu unterstützen. Es gibt mehrere Möglichkeiten, auf Wirkungs Variablen zuzugreifen.

### <a name="setting-groups-of-effect-state"></a>Festlegen von Gruppen von Effekt Zuständen

Verwenden Sie diese Schnittstellen, um eine Gruppe des Zustands zu erhalten und festzulegen.



| Reflektionseschnittstellen                                                                  | BESCHREIBUNG                      |
|----------------------------------------------------------------------------------------|----------------------------------|
| [**ID3D10EffectBlendVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectblendvariable)               | Get-und Set-Blend-Zustand.         |
| [**ID3D10EffectDepthStencilVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilvariable) | Get und Set tiefen Schablone State. |
| [**ID3D10EffectRasterizerVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrasterizervariable)     | Get-und Set-Status des Rasterizers.    |
| [**ID3D10EffectSamplerVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectsamplervariable)           | Holen Sie sich den samplerzustand.       |



 

### <a name="setting-effect-resources"></a>Festlegen von Effekt Ressourcen

Verwenden Sie diese Schnittstellen, um Ressourcen zu erhalten und festzulegen.



| Reflektionseschnittstellen                                                                          | BESCHREIBUNG                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [**ID3D10EffectConstantBuffer-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectconstantbuffer)                     | Zugreifen auf Daten in einem Textur Puffer oder Konstantenpuffer. |
| [**ID3D10EffectDepthStencilViewVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilviewvariable) | Zugreifen auf Daten in einer tiefen Schablone-Ressource.            |
| [**ID3D10EffectRenderTargetViewVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrendertargetviewvariable) | Zugreifen auf Daten in einem Renderziel.                     |
| [**ID3D10EffectShaderResourceVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshaderresourcevariable)     | Zugreifen auf Daten in einer Shaderressource.                   |



 

### <a name="setting-other-effect-variables"></a>Festlegen anderer Effekt Variablen

Verwenden Sie diese Schnittstellen, um den Status anhand des Variablen Typs zu erhalten und festzulegen.



| Reflektionseschnittstellen                                                      | BESCHREIBUNG                    |
|----------------------------------------------------------------------------|--------------------------------|
| [**ID3D10EffectMatrixVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectmatrixvariable) | Gibt eine Matrix an und legt Sie fest.          |
| [**ID3D10EffectScalarVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectscalarvariable) | Ein Skalarwert wird abgerufen und festgelegt.          |
| [**ID3D10EffectShaderVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshadervariable) | Get und Set a Shader Variable. |
| [**ID3D10EffectStringVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectstringvariable) | Gibt eine Zeichenfolge zurück und legt Sie fest.          |
| [**ID3D10EffectType-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttype)                     | Einen Variablentyp erhalten.           |
| [**ID3D10EffectVectorVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvectorvariable) | Get und Set a Vector.          |



 

Alle Reflexions Schnittstellen werden von der [**ID3D10EffectVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable)abgeleitet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effekte](d3d10-graphics-programming-guide-effects.md)
</dt> <dt>

[Programmier Handbuch für Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
