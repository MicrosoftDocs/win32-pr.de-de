---
description: 'Direct3D 10 definiert eine Reihe von Schnittstellen für die beiden grundlegenden Arten von Ressourcen: Puffer und Texturen.'
ms.assetid: e53ca7ab-6ca5-4774-8a52-825b10c1a2ce
title: Ressourcen Schnittstellen (Direct3D 10-Grafiken)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f677130d99ede09cec86cf0d45bc0ec0bc5f9093
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126554"
---
# <a name="resource-interfaces-direct3d-10-graphics"></a>Ressourcen Schnittstellen (Direct3D 10-Grafiken)

Direct3D 10 definiert eine Reihe von Schnittstellen für die beiden grundlegenden Arten von Ressourcen: [Puffer](d3d10-graphics-programming-guide-resources-types.md) und Texturen.



| Schnittstellen                                           | BESCHREIBUNG                                          |
|------------------------------------------------------|------------------------------------------------------|
| [**ID3D10Buffer-Schnittstelle**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)       | Greift auf Puffer Daten zu.                                |
| [**ID3D10Resource-Schnittstelle**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)   | Basisklasse für eine Ressource.                           |
| [**ID3D10Texture1D-Schnittstelle**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture1d) | Greift auf Daten in einer 1D-Textur oder einem 1D-Textur Array zu. |
| [**ID3D10Texture2D-Schnittstelle**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d) | Greift auf Daten in einer 2D-Textur oder einem 2D-Textur Array zu.  |
| [**ID3D10Texture3D-Schnittstelle**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture3d) | Greift auf Daten in einer 3D-Textur oder einem 3D-Textur Array zu. |



 

Eine Anwendung verwendet eine Ansicht, um eine Ressource an eine [Pipeline Stufe](d3d10-graphics-programming-guide-pipeline-stages.md)zu binden. Die [Sicht](d3d10-graphics-programming-guide-resources-access-views.md) definiert, wie während des Renderings auf die Ressource zugegriffen werden kann. Die API enthält diese Ansichts Schnittstellen.



| Schnittstellen                                                               | BESCHREIBUNG                                                                                                  |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**ID3D10DepthStencilView-Schnittstelle**](/windows/desktop/api/D3D10/nn-d3d10-id3d10depthstencilview)       | Greift auf Daten in einer [tiefen Schablone](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md) zu. |
| [**ID3D10RenderTargetView-Schnittstelle**](/windows/desktop/api/D3D10/nn-d3d10-id3d10rendertargetview)       | Greift auf Daten in einem [Renderziel](d3d10-graphics-programming-guide-resources-creating-textures.md)zu.        |
| [**ID3D10ShaderResourceView-Schnittstelle**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)   | Greift auf Daten in einer Shader-Ressource in Direct3D 10,0 zu.                                                         |
| [**ID3D10ShaderResourceView1-Schnittstelle**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10shaderresourceview1) | Greift auf Daten in einer Shader-Ressource in Direct3D 10,1 zu.                                                         |
| [**ID3D10View-Schnittstelle**](/windows/desktop/api/D3D10/nn-d3d10-id3d10view)                               | Basisklasse für eine Ansicht.                                                                                       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourcen Verweis](d3d10-graphics-reference-resource.md)
</dt> </dl>

 

 
