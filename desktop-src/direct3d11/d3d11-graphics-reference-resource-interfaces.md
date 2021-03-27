---
title: Ressourcen Schnittstellen (Direct3D 11-Grafiken)
description: Es gibt eine Reihe von Schnittstellen für die beiden grundlegenden Typen von Ressourcen Puffern und Texturen.
ms.assetid: 8e40573a-b186-41ec-b2ff-81279d77bd3a
keywords:
- Schnittstellen, Direct3D 11-Ressource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4d8f01e8d485fcdf575e8aea1a5beeb2184946b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739616"
---
# <a name="resource-interfaces-direct3d-11-graphics"></a>Ressourcen Schnittstellen (Direct3D 11-Grafiken)

Es gibt eine Reihe von Schnittstellen für die beiden grundlegenden Arten von Ressourcen: Puffer und Texturen. Es gibt auch Schnittstellen für Ansichten von Ressourcen.

Eine Anwendung verwendet eine Ansicht, um eine Ressource an eine Pipeline Stufe zu binden. Die Sicht definiert, wie während des Renderings auf die Ressource zugegriffen werden kann. In diesem Abschnitt werden die Ansichts Schnittstellen beschrieben.


## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                       | BESCHREIBUNG                                                                                                                                                                                            |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)<br/>                             | Eine Puffer Schnittstelle greift auf eine Puffer Ressource zu, bei der es sich um unstrukturierten Speicher handelt. Puffer speichern in der Regel Scheitelpunkt-oder Indexdaten.<br/>                                                                  |
| [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)<br/>         | Eine Schnittstelle für die tiefen Schablone greift beim Testen von tiefen Schablone auf eine Textur Ressource zu.<br/>                                                                                                    |
| [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)<br/>         | Eine Renderziel-View-Schnittstelle identifiziert die Renderziel-unter Ressourcen, auf die während des Renderings zugegriffen werden kann.<br/>                                                                             |
| [**ID3D11RenderTargetView1**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11rendertargetview1)<br/>       | Eine Renderziel-View-Schnittstelle stellt die Renderziel-unter Ressourcen dar, auf die während des Renderings zugegriffen werden kann.<br/>                                                                             |
| [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)<br/>                         | Eine Ressourcen Schnittstelle stellt häufige Aktionen für alle Ressourcen bereit.<br/>                                                                                                                              |
| [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)<br/>     | Eine Shader-Resource-View-Schnittstelle gibt die unter Ressourcen an, auf die ein Shader während des Renderings zugreifen kann. Beispiele für Shader-Ressourcen sind ein konstanter Puffer, ein Textur Puffer und eine Textur.<br/>  |
| [**ID3D11ShaderResourceView1**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11shaderresourceview1)<br/>   | Eine Shader-Resource-View-Schnittstelle stellt die unter Ressourcen dar, auf die ein Shader während des Renderings zugreifen kann. Beispiele für Shader-Ressourcen sind ein konstanter Puffer, ein Textur Puffer und eine Textur.<br/> |
| [**ID3D11Texture1D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture1d)<br/>                       | Eine 1D-Textur Schnittstelle greift auf texaus dem strukturierten Arbeitsspeicher zu.<br/>                                                                                                                     |
| [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)<br/>                       | Eine 2D-Textur Schnittstelle dient zum Verwalten von Textem Arbeitsspeicher.<br/>                                                                                                                      |
| [**ID3D11Texture2D1**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11texture2d1)<br/>                     | Eine 2D-Textur Schnittstelle stellt texturdaten dar, d. h. strukturierter Arbeitsspeicher.<br/>                                                                                                                   |
| [**ID3D11Texture3D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture3d)<br/>                       | Eine 3D-Textur Schnittstelle greift auf texaus dem strukturierten Arbeitsspeicher zu.<br/>                                                                                                                     |
| [**ID3D11Texture3D1**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11texture3d1)<br/>                     | Eine 3D-Textur Schnittstelle stellt texturdaten dar, d. h. strukturierter Arbeitsspeicher.<br/>                                                                                                                   |
| [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)<br/>   | Eine Ansichts Schnittstelle gibt die Teile einer Ressource an, auf die die Pipeline während des Renderings zugreifen kann.<br/>                                                                                                |
| [**ID3D11UnorderedAccessView1**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11unorderedaccessview1)<br/> | Eine ungeordnete Access-View-Schnittstelle stellt die Teile einer Ressource dar, auf die die Pipeline während des Renderings zugreifen kann.<br/>                                                                             |
| [**ID3D11View**](/windows/desktop/api/D3D11/nn-d3d11-id3d11view)<br/>                                 | Eine Ansichts Schnittstelle gibt die Teile einer Ressource an, auf die die Pipeline während des Renderings zugreifen kann.<br/>                                                                                                |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourcen Verweis](d3d11-graphics-reference-resource.md)
</dt> </dl>

 

 





