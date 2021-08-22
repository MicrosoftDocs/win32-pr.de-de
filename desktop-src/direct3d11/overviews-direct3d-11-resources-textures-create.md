---
title: Erstellen einer Textur
description: In diesem Thema wird gezeigt, wie Sie eine Textur erstellen.
ms.assetid: dfe88635-b2c2-48f8-a21e-cce845b518fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6539caec121f301dd89906f7cd78134d3b7cd79083c0d185af63d488ef1648eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565550"
---
# <a name="how-to-create-a-texture"></a>How to: Create a Texture

Die einfachste Möglichkeit, eine Textur zu erstellen, besteht in der Beschreibung ihrer Eigenschaften und dem Aufrufen der Texturerstellungs-API. In diesem Thema wird gezeigt, wie Sie eine Textur erstellen.

**So erstellen Sie eine Textur**

1.  Füllen Sie eine [**D3D11 \_ TEXTURE2D \_ DESC-Struktur**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) mit einer Beschreibung der Texturparameter aus.
2.  Erstellen Sie die Textur, indem Sie [**ID3D11Device::CreateTexture2D mit**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) der Texturbeschreibung aufrufen.

In diesem Beispiel wird eine 256 x [](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)256-Textur mit dynamischer Verwendung erstellt, die als [**Shaderressource**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) mit [**CPU-Schreibzugriff verwendet werden kann.**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag)


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

[Verwenden von Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Texturen](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

 




