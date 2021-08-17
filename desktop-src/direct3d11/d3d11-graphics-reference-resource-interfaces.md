---
title: Ressourcenschnittstellen (Direct3D 11-Grafiken)
description: Es gibt eine Reihe von Schnittstellen für die beiden grundlegenden Typen von Ressourcenpuffern und Texturen.
ms.assetid: 8e40573a-b186-41ec-b2ff-81279d77bd3a
keywords:
- Schnittstellen, Direct3D 11-Ressource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0896bd04a51a989e502676ee314e17d1bf94a110df8a5af9dfe82210dd1b6b71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119125344"
---
# <a name="resource-interfaces-direct3d-11-graphics"></a>Ressourcenschnittstellen (Direct3D 11-Grafiken)

Es gibt eine Reihe von Schnittstellen für die beiden grundlegenden Ressourcentypen: Puffer und Texturen. Es gibt auch Schnittstellen für Ansichten von Ressourcen.

Eine Anwendung verwendet eine Ansicht, um eine Ressource an eine Pipelinephase zu binden. Die Ansicht definiert, wie während des Renderings auf die Ressource zugegriffen werden kann. In diesem Abschnitt werden die Ansichtsschnittstellen beschrieben.


## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                       | Beschreibung                                                                                                                                                                                            |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)<br/>                             | Eine Pufferschnittstelle greifen auf eine Pufferressource zu, bei der es sich um unstrukturierten Speicher handelt. Puffer speichern in der Regel Scheitelpunkt- oder Indexdaten.<br/>                                                                  |
| [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)<br/>         | Eine Tiefen-Schablonenansicht-Schnittstelle greifen während des Tiefen-Schablonentests auf eine Texturressource zu.<br/>                                                                                                    |
| [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)<br/>         | Eine Renderzielansichtsschnittstelle identifiziert die Unterressourcen des Renderziels, auf die während des Renderings zugegriffen werden kann.<br/>                                                                             |
| [**ID3D11RenderTargetView1**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11rendertargetview1)<br/>       | Eine Renderzielansichtsschnittstelle stellt die Unterressourcen des Renderziels dar, auf die während des Renderings zugegriffen werden kann.<br/>                                                                             |
| [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)<br/>                         | Eine Ressourcenschnittstelle stellt allgemeine Aktionen für alle Ressourcen bereit.<br/>                                                                                                                              |
| [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)<br/>     | Eine Shader-Ressourcenansichtsschnittstelle gibt die Unterressourcen an, auf die ein Shader während des Renderings zugreifen kann. Beispiele für Shaderressourcen sind ein konstanter Puffer, ein Texturpuffer und eine Textur.<br/>  |
| [**ID3D11ShaderResourceView1**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11shaderresourceview1)<br/>   | Eine Shader-Ressourcenansicht-Schnittstelle stellt die Unterressourcen dar, auf die ein Shader während des Renderings zugreifen kann. Beispiele für Shaderressourcen sind ein konstanter Puffer, ein Texturpuffer und eine Textur.<br/> |
| [**ID3D11Texture1D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture1d)<br/>                       | Eine 1D-Texturschnittstelle greifen auf texel-Daten zu, bei denen es sich um strukturierten Speicher handelt.<br/>                                                                                                                     |
| [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)<br/>                       | Eine 2D-Texturschnittstelle verwaltet Texeldaten, bei denen es sich um strukturierten Speicher handelt.<br/>                                                                                                                      |
| [**ID3D11Texture2D1**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11texture2d1)<br/>                     | Eine 2D-Texturschnittstelle stellt Texeldaten dar, bei denen es sich um strukturierten Speicher handelt.<br/>                                                                                                                   |
| [**ID3D11Texture3D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture3d)<br/>                       | Eine 3D-Texturschnittstelle greifen auf texel-Daten zu, bei denen es sich um strukturierten Speicher handelt.<br/>                                                                                                                     |
| [**ID3D11Texture3D1**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11texture3d1)<br/>                     | Eine 3D-Texturschnittstelle stellt Texeldaten dar, bei denen es sich um strukturierten Speicher handelt.<br/>                                                                                                                   |
| [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)<br/>   | Eine Ansichtsschnittstelle gibt die Teile einer Ressource an, auf die die Pipeline während des Renderings zugreifen kann.<br/>                                                                                                |
| [**ID3D11UnorderedAccessView1**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11unorderedaccessview1)<br/> | Eine ungeordnete Access View-Schnittstelle stellt die Teile einer Ressource dar, auf die die Pipeline während des Renderings zugreifen kann.<br/>                                                                             |
| [**ID3D11View**](/windows/desktop/api/D3D11/nn-d3d11-id3d11view)<br/>                                 | Eine Ansichtsschnittstelle gibt die Teile einer Ressource an, auf die die Pipeline während des Renderings zugreifen kann.<br/>                                                                                                |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourcenreferenz](d3d11-graphics-reference-resource.md)
</dt> </dl>

 

 





