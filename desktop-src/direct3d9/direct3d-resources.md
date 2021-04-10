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
# <a name="direct3d-resources-direct3d-9"></a><span data-ttu-id="a2f3f-103">Direct3D-Ressourcen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a2f3f-103">Direct3D Resources (Direct3D 9)</span></span>

<span data-ttu-id="a2f3f-104">Ressourcen sind die Texturen und Puffer, die zum Rendering einer Szene verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a2f3f-104">Resources are the textures and buffers that are used to render a scene.</span></span> <span data-ttu-id="a2f3f-105">Anwendungen müssen Ressourcen erstellen, laden, kopieren und verwenden.</span><span class="sxs-lookup"><span data-stu-id="a2f3f-105">Applications need to create, load, copy, and use resources.</span></span> <span data-ttu-id="a2f3f-106">Dieser Abschnitt enthält eine kurze Einführung in die Ressourcen sowie die Schritte und Methoden, die von Anwendungen beim Arbeiten mit Ressourcen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a2f3f-106">This section gives a brief introduction to resources and the steps and methods used by applications when working with resources.</span></span>

<span data-ttu-id="a2f3f-107">Alle Ressourcen, einschließlich der Geometry-Ressourcen [**IDirect3DIndexBuffer9**](/windows/desktop/api) und [**IDirect3DVertexBuffer9**](/windows/desktop/api), erben von der [**IDirect3DResource9**](/windows/desktop/api) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="a2f3f-107">All resources, including the geometry resources [**IDirect3DIndexBuffer9**](/windows/desktop/api) and [**IDirect3DVertexBuffer9**](/windows/desktop/api), inherit from the [**IDirect3DResource9**](/windows/desktop/api) interface.</span></span> <span data-ttu-id="a2f3f-108">Die Textur Ressourcen, [**IDirect3DCubeTexture9**](/windows/desktop/api), [**IDirect3DTexture9**](/windows/desktop/api)und [**IDirect3DVolumeTexture9**](/windows/desktop/api), Erben auch von der [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="a2f3f-108">The texture resources, [**IDirect3DCubeTexture9**](/windows/desktop/api), [**IDirect3DTexture9**](/windows/desktop/api), and [**IDirect3DVolumeTexture9**](/windows/desktop/api), also inherit from the [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) interface.</span></span>

-   [<span data-ttu-id="a2f3f-109">Ressourcen Eigenschaften (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a2f3f-109">Resource Properties (Direct3D 9)</span></span>](resource-properties.md)
-   [<span data-ttu-id="a2f3f-110">Bearbeiten von Ressourcen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a2f3f-110">Manipulating Resources (Direct3D 9)</span></span>](manipulating-resources.md)
-   [<span data-ttu-id="a2f3f-111">Sperren von Ressourcen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a2f3f-111">Locking Resources (Direct3D 9)</span></span>](locking-resources.md)
-   [<span data-ttu-id="a2f3f-112">Ressourcen Beziehungen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a2f3f-112">Resource Relationships (Direct3D 9)</span></span>](resource-relationships.md)
-   [<span data-ttu-id="a2f3f-113">Verwalten von Ressourcen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a2f3f-113">Managing Resources (Direct3D 9)</span></span>](managing-resources.md)
-   [<span data-ttu-id="a2f3f-114">Von der Anwendung verwaltete Ressourcen und Zuordnungs Strategien (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a2f3f-114">Application-Managed Resources and Allocation Strategies (Direct3D 9)</span></span>](application-managed-resources-and-allocation-strategies.md)

<!-- -->

-   [<span data-ttu-id="a2f3f-115">Index Puffer (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a2f3f-115">Index Buffers (Direct3D 9)</span></span>](index-buffers.md)
-   [<span data-ttu-id="a2f3f-116">Vertex-Puffer (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a2f3f-116">Vertex Buffers (Direct3D 9)</span></span>](vertex-buffers.md)

## <a name="related-topics"></a><span data-ttu-id="a2f3f-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a2f3f-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2f3f-118">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="a2f3f-118">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 
