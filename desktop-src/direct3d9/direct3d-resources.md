---
description: Ressourcen sind die Texturen und Puffer, die zum Rendering einer Szene verwendet werden.
ms.assetid: 815a330c-9fd2-45ff-b7df-192fc197074f
title: Direct3D-Ressourcen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7745318db3d880711ee962edb086996764455ec8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124496"
---
# <a name="direct3d-resources-direct3d-9"></a>Direct3D-Ressourcen (Direct3D 9)

Ressourcen sind die Texturen und Puffer, die zum Rendering einer Szene verwendet werden. Anwendungen müssen Ressourcen erstellen, laden, kopieren und verwenden. Dieser Abschnitt enthält eine kurze Einführung in die Ressourcen sowie die Schritte und Methoden, die von Anwendungen beim Arbeiten mit Ressourcen verwendet werden.

Alle Ressourcen, einschließlich der Geometry-Ressourcen [**IDirect3DIndexBuffer9**](/windows/desktop/api) und [**IDirect3DVertexBuffer9**](/windows/desktop/api), erben von der [**IDirect3DResource9**](/windows/desktop/api) -Schnittstelle. Die Textur Ressourcen, [**IDirect3DCubeTexture9**](/windows/desktop/api), [**IDirect3DTexture9**](/windows/desktop/api)und [**IDirect3DVolumeTexture9**](/windows/desktop/api), Erben auch von der [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) -Schnittstelle.

-   [Ressourcen Eigenschaften (Direct3D 9)](resource-properties.md)
-   [Bearbeiten von Ressourcen (Direct3D 9)](manipulating-resources.md)
-   [Sperren von Ressourcen (Direct3D 9)](locking-resources.md)
-   [Ressourcen Beziehungen (Direct3D 9)](resource-relationships.md)
-   [Verwalten von Ressourcen (Direct3D 9)](managing-resources.md)
-   [Von der Anwendung verwaltete Ressourcen und Zuordnungs Strategien (Direct3D 9)](application-managed-resources-and-allocation-strategies.md)

<!-- -->

-   [Index Puffer (Direct3D 9)](index-buffers.md)
-   [Vertex-Puffer (Direct3D 9)](vertex-buffers.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erste Schritte](getting-started.md)
</dt> </dl>

 

 
