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
# <a name="how-to-create-a-texture"></a><span data-ttu-id="2b101-103">Vorgehensweise: Erstellen einer Textur</span><span class="sxs-lookup"><span data-stu-id="2b101-103">How to: Create a Texture</span></span>

<span data-ttu-id="2b101-104">Die einfachste Möglichkeit zum Erstellen einer Textur besteht darin, die Eigenschaften zu beschreiben und die Textur Erstellungs-API aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="2b101-104">The simplest way to create a texture is to describe its properties and call the texture creation API.</span></span> <span data-ttu-id="2b101-105">In diesem Thema wird gezeigt, wie eine Textur erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="2b101-105">This topic shows how to create a texture.</span></span>

<span data-ttu-id="2b101-106">**So erstellen Sie eine Textur**</span><span class="sxs-lookup"><span data-stu-id="2b101-106">**To create a texture**</span></span>

1.  <span data-ttu-id="2b101-107">Füllen Sie eine [**D3D11 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) -Struktur mit einer Beschreibung der Textur Parameter aus.</span><span class="sxs-lookup"><span data-stu-id="2b101-107">Fill in a [**D3D11\_TEXTURE2D\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) structure with a description of the texture parameters.</span></span>
2.  <span data-ttu-id="2b101-108">Erstellen Sie die Textur durch Aufrufen von [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) mit der Textur Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="2b101-108">Create the texture by calling [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) with the texture description.</span></span>

<span data-ttu-id="2b101-109">Dieses Beispiel erstellt eine 256 x 256-Textur mit [**dynamischer Verwendung**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), die als [**Shaderressource**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) mit CPU- [**Schreibzugriff**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag)verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="2b101-109">This example creates a 256 x 256 texture, with [**dynamic usage**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), for use as a [**shader resource**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) with [**cpu write access**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="2b101-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2b101-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b101-111">Verwendung von Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="2b101-111">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> <dt>

[<span data-ttu-id="2b101-112">Texturen</span><span class="sxs-lookup"><span data-stu-id="2b101-112">Textures</span></span>](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

 




