---
description: 'Im folgenden Codebeispiel wird die Verwendung der IDirect3DDevice9:: getdepthstencilsurface-Methode zum Abrufen eines Zeigers auf die Tiefe Puffer Oberfläche des Geräts veranschaulicht.'
ms.assetid: cd5c158a-d2c4-4ced-aa6f-cd8c0e426a74
title: Abrufen eines tiefen Puffers (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae914b8506fd0c4169f0cfec0d78d7c3bd9b9d61
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125149"
---
# <a name="retrieving-a-depth-buffer-direct3d-9"></a>Abrufen eines tiefen Puffers (Direct3D 9)

Im folgenden Codebeispiel wird die Verwendung der [**IDirect3DDevice9:: getdepthstencilsurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdepthstencilsurface) -Methode zum Abrufen eines Zeigers auf die Tiefe Puffer Oberfläche des Geräts veranschaulicht.


```
LPDIRECT3DSURFACE9 pZBuffer;

m_d3dDevice->GetDepthStencilSurface( &pZBuffer );
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Tiefen Puffer](depth-buffers.md)
</dt> </dl>

 

 
