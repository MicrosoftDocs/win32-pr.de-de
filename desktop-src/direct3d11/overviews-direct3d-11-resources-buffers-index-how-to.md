---
title: Erstellen eines Indexpuffers
description: In diesem Thema wird gezeigt, wie ein Indexpuffer als Vorbereitung für das Rendering initialisiert wird.
ms.assetid: 4b33d32a-27fd-4652-87ac-3b7268881f89
keywords:
- Indexpuffer, erstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d474114e5908a42a112dddd550e24c13e5e1d3bf2cec523d47dfe1d617ac0bf5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119500"
---
# <a name="how-to-create-an-index-buffer"></a>Vorgehensweise: Erstellen eines Indexpuffers

[Indexpuffer](overviews-direct3d-11-resources-buffers-intro.md) enthalten Indexdaten. In diesem Thema wird gezeigt, wie ein [Indexpuffer](overviews-direct3d-11-resources-buffers-intro.md) als Vorbereitung für das Rendering initialisiert wird.

**So initialisieren Sie einen Indexpuffer**

1.  Erstellen Sie einen Puffer, der Ihre Indexinformationen enthält.
2.  Erstellen Sie eine Pufferbeschreibung, indem Sie eine [**D3D11 \_ BUFFER \_ DESC-Struktur**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) ausfüllen. Übergeben Sie das BIND INDEX BUFFER-Flag D3D11 \_ \_ an den \_ **BindFlags-Member,** und übergeben Sie die Größe des Puffers in Bytes an den **ByteWidth-Member.**
3.  Erstellen Sie eine Beschreibung der Unterressourcendaten, indem Sie eine [**D3D11 \_ SUBRESOURCE \_ DATA-Struktur**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) ausfüllen. Der **pSysMem-Member** sollte direkt auf die Indexdaten verweisen, die in Schritt 1 erstellt wurden.
4.  Rufen Sie [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) auf, während Sie die [**D3D11 \_ BUFFER \_ DESC-Struktur,**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) die [**D3D11 \_ SUBRESOURCE \_ DATA-Struktur**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) und die Adresse eines Zeigers auf die zu initialisierende [**ID3D11Buffer-Schnittstelle**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) übergeben.

Im folgenden Codebeispiel wird veranschaulicht, wie ein Indexpuffer erstellt wird. In diesem Beispiel wird davon ausgegangen, dass


```
g_pd3dDevice
```



ist ein gültiges [**ID3D11Device-Objekt,**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) und das


```
g_pd3dContext
```



ist ein gültiges [**ID3D11DeviceContext-Objekt.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)


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

[Verwenden von Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




