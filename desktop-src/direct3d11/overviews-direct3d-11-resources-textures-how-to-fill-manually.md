---
title: Programmgesteuertes Initialisieren einer Textur
description: Dieses Thema enthält mehrere Beispiele, die zeigen, wie Texturen initialisiert werden, die mit verschiedenen Verwendungstypen erstellt werden.
ms.assetid: 65e8ae82-50aa-4303-853e-3457da18f44f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07b7d34e7e85fd647a6f45c93d61b3330825261f59d87b9c13a95547e742e365
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118530562"
---
# <a name="how-to-initialize-a-texture-programmatically"></a>How to: Initialize a Texture Programmatically

Sie können eine Textur während der Objekterstellung initialisieren oder das Objekt programmgesteuert füllen, nachdem es erstellt wurde. Dieses Thema enthält mehrere Beispiele, die zeigen, wie Texturen initialisiert werden, die mit verschiedenen Verwendungstypen erstellt werden. In diesem Beispiel wird davon ausgegangen, dass Sie bereits wissen, wie [Sie eine Textur erstellen.](overviews-direct3d-11-resources-textures-create.md)

-   [Standardverwendung](#default-usage)
-   [Dynamische Nutzung](#dynamic-usage)
-   [Stagingverwendung](#staging-usage)
-   [Zugehörige Themen](#related-topics)

## <a name="default-usage"></a>Standardverwendung

Der gängigste Verwendungstyp ist die Standardverwendung. Um eine Standardtextur zu füllen (eine textur, die mit **D3D11 \_ USAGE \_ DEFAULT** erstellt wurde), können Sie eine der beiden beiden:

-   Rufen [**Sie ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) auf, und initialisieren Sie *pInitialData,* um auf daten zu verweisen, die von einer Anwendung bereitgestellt werden.

    oder

-   Verwenden Sie nach dem Aufruf von [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) [**ID3D11DeviceContext::UpdateSubresource,**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) um die Standardtextur mit Daten aus einem von der Anwendung bereitgestellten Zeiger zu füllen.

## <a name="dynamic-usage"></a>Dynamische Nutzung

So füllen Sie eine dynamische Textur (eine, die mit **D3D11 \_ USAGE DYNAMIC erstellt \_ wurde):**

1.  Rufen Sie einen Zeiger auf den Texturspeicher ab, indem **Sie D3D11 \_ MAP WRITE \_ \_ DISCARD** beim Aufrufen von [**ID3D11DeviceContext::Map übergeben.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)
2.  Schreiben sie Daten in den Arbeitsspeicher.
3.  Rufen [**Sie ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) auf, wenn Sie mit dem Schreiben von Daten fertig sind.

## <a name="staging-usage"></a>Stagingverwendung

So füllen Sie eine Stagingtextur (eine, die mit **D3D11 \_ USAGE STAGING erstellt \_ wurde):**

1.  Rufen Sie einen Zeiger auf den Texturspeicher ab, indem **Sie D3D11 \_ MAP \_ WRITE** übergeben, wenn [**ID3D11DeviceContext::Map aufgerufen wird.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)
2.  Schreiben sie Daten in den Arbeitsspeicher.
3.  Rufen [**Sie ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) auf, wenn Sie mit dem Schreiben von Daten fertig sind.

Eine Stagingtextur kann dann als Quellparameter für [**ID3D11DeviceContext::CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) oder [**ID3D11DeviceContext::CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) verwendet werden, um eine Standardressource oder eine dynamische Ressource zu füllen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Texturen](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

 




