---
title: Programm gesteuertes Initialisieren einer Textur
description: Dieses Thema enthält mehrere Beispiele, die zeigen, wie Texturen initialisiert werden, die mit verschiedenen Arten von Verwendungen erstellt werden.
ms.assetid: 65e8ae82-50aa-4303-853e-3457da18f44f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5584885b885f6026ee32a3e4c52a24aad78c3c08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856424"
---
# <a name="how-to-initialize-a-texture-programmatically"></a>Gewusst wie: Programm gesteuertes Initialisieren einer Textur

Sie können während der Objekt Erstellung eine Textur initialisieren, oder Sie können das Objekt Programm gesteuert auffüllen, nachdem es erstellt wurde. Dieses Thema enthält mehrere Beispiele, die zeigen, wie Texturen initialisiert werden, die mit verschiedenen Arten von Verwendungen erstellt werden. In diesem Beispiel wird davon ausgegangen, dass Sie bereits wissen, wie [eine Textur erstellt](overviews-direct3d-11-resources-textures-create.md)wird.

-   [Standardverwendung](#default-usage)
-   [Dynamische Verwendung](#dynamic-usage)
-   [Staging-Verwendung](#staging-usage)
-   [Zugehörige Themen](#related-topics)

## <a name="default-usage"></a>Standardverwendung

Die häufigste Art der Verwendung ist die Standardverwendung. Zum Auffüllen einer Standard Textur (mit **D3D11 \_ Usage \_ default**) können Sie Folgendes tun:

-   Wenden Sie [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) an, und initialisieren Sie *pinitialdata* , um auf die von einer Anwendung bereitgestellten Daten zu verweisen.

    oder

-   Verwenden Sie nach dem Aufrufen von [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) [**Verknüpfung id3d11devicecontext aus:: updatesubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) , um die Standard Textur mit Daten aus einem von der Anwendung bereitgestellten Zeiger zu füllen.

## <a name="dynamic-usage"></a>Dynamische Verwendung

So füllen Sie eine dynamische Textur (eine mit **\_ \_ dynamischer D3D11-Auslastung** erstellt):

1.  Rufen Sie einen Zeiger auf den Texturspeicher ab, indem Sie **D3D11 \_ map \_ Write \_ verwerfen** übergeben, wenn Sie [**Verknüpfung id3d11devicecontext aus:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)aufrufen.
2.  Schreiben von Daten in den Arbeitsspeicher.
3.  Wenn Sie mit dem Schreiben von Daten fertig sind, wird [**Verknüpfung id3d11devicecontext aus:: unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) aufgerufen.

## <a name="staging-usage"></a>Staging-Verwendung

So füllen Sie eine stagingtextur (eine mit **D3D11 \_ Usage \_ Staging** erstellt):

1.  Rufen Sie einen Zeiger auf den Texturspeicher ab, indem Sie beim Aufrufen von [**Verknüpfung id3d11devicecontext aus:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)den **D3D11 \_ map- \_ Schreibvorgang** übergeben.
2.  Schreiben von Daten in den Arbeitsspeicher.
3.  Wenn Sie mit dem Schreiben von Daten fertig sind, wird [**Verknüpfung id3d11devicecontext aus:: unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) aufgerufen.

Eine stagingtextur kann dann als Quellparameter für [**Verknüpfung id3d11devicecontext aus:: copyresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) oder [**Verknüpfung id3d11devicecontext aus:: copysubresourceregion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) verwendet werden, um eine Standard-oder dynamische Ressource auszufüllen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwendung von Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Texturen](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

 




