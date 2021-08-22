---
description: 'Direct3D 10 definiert eine Reihe von Schnittstellen für die beiden grundlegenden Ressourcentypen: Puffer und Texturen.'
ms.assetid: e53ca7ab-6ca5-4774-8a52-825b10c1a2ce
title: Ressourcenschnittstellen (Direct3D 10-Grafiken)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94eb7a0f2ce0b6792ccb98b95605f00504fbf239ee0cecf0846814d84566de9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119282820"
---
# <a name="resource-interfaces-direct3d-10-graphics"></a>Ressourcenschnittstellen (Direct3D 10-Grafiken)

Direct3D 10 definiert eine Reihe von Schnittstellen für die beiden grundlegenden Ressourcentypen: [Puffer](d3d10-graphics-programming-guide-resources-types.md) und Texturen.



| Schnittstellen                                           | Beschreibung                                          |
|------------------------------------------------------|------------------------------------------------------|
| [**ID3D10Buffer-Schnittstelle**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)       | Zugriff auf Pufferdaten.                                |
| [**ID3D10Resource-Schnittstelle**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)   | Basisklasse für eine Ressource.                           |
| [**ID3D10Texture1D-Schnittstelle**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture1d) | Greifen Auf Daten in einer 1D-Textur oder einem 1D-Texturarray zu. |
| [**ID3D10Texture2D-Schnittstelle**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d) | Zugreifen auf Daten in einer 2D-Textur oder einem 2D-Texturarray  |
| [**ID3D10Texture3D-Schnittstelle**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture3d) | Greifen Auf Daten in einer 3D-Textur oder einem 3D-Texturarray zu. |



 

Eine Anwendung verwendet eine Ansicht, um eine Ressource an eine [Pipelinephase zu binden.](d3d10-graphics-programming-guide-pipeline-stages.md) Die [Ansicht](d3d10-graphics-programming-guide-resources-access-views.md) definiert, wie während des Renderings auf die Ressource zugegriffen werden kann. Die API enthält diese Ansichtsschnittstellen.



| Schnittstellen                                                               | Beschreibung                                                                                                  |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**ID3D10DepthStencilView-Schnittstelle**](/windows/desktop/api/D3D10/nn-d3d10-id3d10depthstencilview)       | Greifen Auf Daten in einer [Tiefen-Schablonentextur](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md) zu. |
| [**ID3D10RenderTargetView-Schnittstelle**](/windows/desktop/api/D3D10/nn-d3d10-id3d10rendertargetview)       | Auf Daten in einem [Renderziel zu.](d3d10-graphics-programming-guide-resources-creating-textures.md)        |
| [**ID3D10ShaderResourceView-Schnittstelle**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)   | Zugriff auf Daten in einer Shaderressource in Direct3D 10.0.                                                         |
| [**ID3D10ShaderResourceView1-Schnittstelle**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10shaderresourceview1) | Zugriff auf Daten in einer Shaderressource in Direct3D 10.1.                                                         |
| [**ID3D10View-Schnittstelle**](/windows/desktop/api/D3D10/nn-d3d10-id3d10view)                               | Basisklasse für eine Ansicht.                                                                                       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourcenreferenz](d3d10-graphics-reference-resource.md)
</dt> </dl>

 

 
