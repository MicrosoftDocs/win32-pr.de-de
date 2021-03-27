---
title: Erstellen einer Textur
description: In diesem Thema wird gezeigt, wie eine Textur erstellt wird.
ms.assetid: dfe88635-b2c2-48f8-a21e-cce845b518fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3d3c4715bb4c790ea772dcbba4834051946747e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712059"
---
# <a name="how-to-create-a-texture"></a>Vorgehensweise: Erstellen einer Textur

Die einfachste Möglichkeit zum Erstellen einer Textur besteht darin, die Eigenschaften zu beschreiben und die Textur Erstellungs-API aufzurufen. In diesem Thema wird gezeigt, wie eine Textur erstellt wird.

**So erstellen Sie eine Textur**

1.  Füllen Sie eine [**D3D11 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) -Struktur mit einer Beschreibung der Textur Parameter aus.
2.  Erstellen Sie die Textur durch Aufrufen von [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) mit der Textur Beschreibung.

Dieses Beispiel erstellt eine 256 x 256-Textur mit [**dynamischer Verwendung**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), die als [**Shaderressource**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) mit CPU- [**Schreibzugriff**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag)verwendet werden kann.


```
D3D11_TEXTURE2D_DESC desc;
desc.Width = 256;
desc.Height = 256;
desc.MipLevels = desc.ArraySize = 1;
desc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
desc.SampleDesc.Count = 1;
desc.Usage = D3D11_USAGE_DYNAMIC;
desc.BindFlags = D3D11_BIND_SHADER_RESOURCE;
desc.CPUAccessFlags = D3D11_CPU_ACCESS_WRITE;
desc.MiscFlags = 0;

ID3D11Device *pd3dDevice; // Don't forget to initialize this
ID3D11Texture2D *pTexture = NULL;
pd3dDevice->CreateTexture2D( &desc, NULL, &pTexture );
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwendung von Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Texturen](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

 




