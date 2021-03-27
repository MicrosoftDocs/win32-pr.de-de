---
title: Erstellen eines Index Puffers
description: In diesem Thema wird gezeigt, wie ein Index Puffer zur Vorbereitung des Renderings initialisiert wird.
ms.assetid: 4b33d32a-27fd-4652-87ac-3b7268881f89
keywords:
- Index Puffer, erstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c4c99639748876a5f5fd84e546aaf299885c76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207077"
---
# <a name="how-to-create-an-index-buffer"></a>Vorgehensweise: Erstellen eines Index Puffers

[Index Puffer](overviews-direct3d-11-resources-buffers-intro.md) enthalten Indexdaten. In diesem Thema wird gezeigt, wie ein [Index Puffer](overviews-direct3d-11-resources-buffers-intro.md) zur Vorbereitung des Renderings initialisiert wird.

**So initialisieren Sie einen Index Puffer**

1.  Erstellen Sie einen Puffer, der die Indexinformationen enthält.
2.  Erstellen Sie eine Puffer Beschreibung, indem Sie eine [**D3D11- \_ Puffer- \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) Debug-Struktur ausfüllen. Übergeben Sie das D3D11 \_ Bind \_ Index \_ buffer-Flag an den **bindflags** -Member, und übergeben Sie die Größe des Puffers in Bytes an den **bytewidth** -Member.
3.  Erstellen Sie eine Beschreibung der untergeordneten Quelldaten, indem Sie eine [**D3D11 \_ subresource- \_ Daten**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) Struktur ausfüllen. Der **psysmem** -Member sollte direkt auf die in Schritt 1 erstellten Indexdaten verweisen.
4.  Aufrufen von [**ID3D11Device:: up Buffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) beim Übergeben der [**D3D11- \_ Puffer- \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) Debug-Struktur, der [**D3D11 \_ subresource- \_ Daten**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) Struktur und der Adresse eines Zeigers auf die [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) -Schnittstelle, die initialisiert werden soll.

Im folgenden Codebeispiel wird veranschaulicht, wie ein Index Puffer erstellt wird. In diesem Beispiel wird angenommen, dass


```
g_pd3dDevice
```



ist ein gültiges [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) -Objekt, das


```
g_pd3dContext
```



ist ein gültiges [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) -Objekt.


```
ID3D11Buffer *g_pIndexBuffer = NULL;

// Create indices.
unsigned int indices[] = { 0, 1, 2 };

// Fill in a buffer description.
D3D11_BUFFER_DESC bufferDesc;
bufferDesc.Usage           = D3D11_USAGE_DEFAULT;
bufferDesc.ByteWidth       = sizeof( unsigned int ) * 3;
bufferDesc.BindFlags       = D3D11_BIND_INDEX_BUFFER;
bufferDesc.CPUAccessFlags  = 0;
bufferDesc.MiscFlags       = 0;

// Define the resource data.
D3D11_SUBRESOURCE_DATA InitData;
InitData.pSysMem = indices;
InitData.SysMemPitch = 0;
InitData.SysMemSlicePitch = 0;

// Create the buffer with the device.
hr = g_pd3dDevice->CreateBuffer( &bufferDesc, &InitData, &g_pIndexBuffer );
if( FAILED( hr ) )
    return hr;

// Set the buffer.
g_pd3dContext->IASetIndexBuffer( g_pIndexBuffer, DXGI_FORMAT_R32_UINT, 0 );
    
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Puffer](overviews-direct3d-11-resources-buffers.md)
</dt> <dt>

[Verwendung von Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




