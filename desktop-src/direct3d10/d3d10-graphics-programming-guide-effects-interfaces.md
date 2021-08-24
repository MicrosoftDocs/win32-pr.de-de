---
description: 'Das Effektsystem definiert mehrere Schnittstellen zum Verwalten des Effektzustands. Es gibt zwei Arten von Schnittstellen: diejenigen, die von der Laufzeit zum Rendern von Effekt- und Reflektionsschnittstellen zum Abrufen und Festlegen von Effektvariablen verwendet werden.'
ms.assetid: 068d49d2-0e14-4080-9fee-20d984f22545
title: Effektsystemschnittstellen (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d5d640b31d0d1db9ac9b58ed166b45acff762b30edc0e71f1d7138b5818b3e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128392"
---
# <a name="effect-system-interfaces-direct3d-10"></a>Effektsystemschnittstellen (Direct3D 10)

Das Effektsystem definiert mehrere Schnittstellen zum Verwalten des Effektzustands. Es gibt zwei Arten von Schnittstellen: diejenigen, die von der Laufzeit zum Rendern von Effekt- und Reflektionsschnittstellen zum Abrufen und Festlegen von Effektvariablen verwendet werden.

-   [Effektlaufzeitschnittstellen](#effect-runtime-interfaces)
-   [Effektreflektionsschnittstellen](#effect-reflection-interfaces)

## <a name="effect-runtime-interfaces"></a>Effektlaufzeitschnittstellen

Verwenden Sie Laufzeitschnittstellen, um einen Effekt zu rendern.



| Laufzeitschnittstellen                                               | Beschreibung                                                          |
|------------------------------------------------------------------|----------------------------------------------------------------------|
| [**ID3D10Effect-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)                   | Auflistung von einem oder mehreren Techniken zum Rendern.                  |
| [**ID3D10Include-Schnittstelle**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))                 | Eine Schnittstelle zum Hinzufügen benutzerdefinierter Verhaltensweisen beim Lesen von Includedateien. |
| [**ID3D10EffectPass-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpass)           | Eine Auflistung von Zustandszuweisungen.                                   |
| [**ID3D10EffectPool-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)           | Erstellen Sie einen Speicherort für Variablen, die von den Effekten gemeinsam genutzt werden sollen. |
| [**ID3D10EffectTechnique-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttechnique) | Eine Auflistung von einem oder mehreren Durchläufen.                                  |



 

## <a name="effect-reflection-interfaces"></a>Effektreflektionsschnittstellen

Reflektion wird im Effektsystem implementiert, um das Lesen (und Schreiben) des Effektzustands zu unterstützen. Es gibt mehrere Möglichkeiten, auf Effektvariablen zuzugreifen.

### <a name="setting-groups-of-effect-state"></a>Festlegen von Effect-Statusgruppen

Verwenden Sie diese Schnittstellen, um eine Statusgruppe abzurufen und festzulegen.



| Reflektionsschnittstellen                                                                  | Beschreibung                      |
|----------------------------------------------------------------------------------------|----------------------------------|
| [**ID3D10EffectBlendVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectblendvariable)               | Abrufen und Festlegen des Blendzustands.         |
| [**ID3D10EffectDepthStencilVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilvariable) | Abrufen und Festlegen des Tiefenschablonenzustands. |
| [**ID3D10EffectRasterizerVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrasterizervariable)     | Abrufen und Festlegen des Rasterizerzustands.    |
| [**ID3D10EffectSamplerVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectsamplervariable)           | Abrufen und Festlegen des Samplerzustands.       |



 

### <a name="setting-effect-resources"></a>Festlegen von Effect-Ressourcen

Verwenden Sie diese Schnittstellen, um Ressourcen abzurufen und festzulegen.



| Reflektionsschnittstellen                                                                          | Beschreibung                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [**ID3D10EffectConstantBuffer-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectconstantbuffer)                     | Zugreifen auf Daten in einem Texturpuffer oder konstanten Puffer. |
| [**ID3D10EffectDepthStencilViewVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilviewvariable) | Zugreifen auf Daten in einer Tiefenschablonenressource.            |
| [**ID3D10EffectRenderTargetViewVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrendertargetviewvariable) | Zugreifen auf Daten in einem Renderziel.                     |
| [**ID3D10EffectShaderResourceVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshaderresourcevariable)     | Zugreifen auf Daten in einer Shaderressource.                   |



 

### <a name="setting-other-effect-variables"></a>Festlegen anderer Effektvariablen

Verwenden Sie diese Schnittstellen, um den Zustand anhand des Variablentyps abzurufen und festzulegen.



| Reflektionsschnittstellen                                                      | Beschreibung                    |
|----------------------------------------------------------------------------|--------------------------------|
| [**ID3D10EffectMatrixVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectmatrixvariable) | Abrufen und Festlegen einer Matrix.          |
| [**ID3D10EffectScalarVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectscalarvariable) | Abrufen und Festlegen eines Skalars.          |
| [**ID3D10EffectShaderVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshadervariable) | Abrufen und Festlegen einer Shadervariablen. |
| [**ID3D10EffectStringVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectstringvariable) | Abrufen und Festlegen einer Zeichenfolge.          |
| [**ID3D10EffectType-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttype)                     | Abrufen eines Variablentyps.           |
| [**ID3D10EffectVectorVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvectorvariable) | Abrufen und Festlegen eines Vektors.          |



 

Alle Reflektionsschnittstellen werden von [**der ID3D10EffectVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable)abgeleitet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effekte](d3d10-graphics-programming-guide-effects.md)
</dt> <dt>

[Programmierhandbuch für Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
