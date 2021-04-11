---
description: 'Direct3D 10 definiert eine Reihe von Schnittstellen für die beiden grundlegenden Arten von Ressourcen: Puffer und Texturen.'
ms.assetid: e53ca7ab-6ca5-4774-8a52-825b10c1a2ce
title: Ressourcen Schnittstellen (Direct3D 10-Grafiken)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f677130d99ede09cec86cf0d45bc0ec0bc5f9093
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126554"
---
# <a name="resource-interfaces-direct3d-10-graphics"></a><span data-ttu-id="a5526-103">Ressourcen Schnittstellen (Direct3D 10-Grafiken)</span><span class="sxs-lookup"><span data-stu-id="a5526-103">Resource Interfaces (Direct3D 10 Graphics)</span></span>

<span data-ttu-id="a5526-104">Direct3D 10 definiert eine Reihe von Schnittstellen für die beiden grundlegenden Arten von Ressourcen: [Puffer](d3d10-graphics-programming-guide-resources-types.md) und Texturen.</span><span class="sxs-lookup"><span data-stu-id="a5526-104">Direct3D 10 defines a number of interfaces for the two basic types of resources: [buffers](d3d10-graphics-programming-guide-resources-types.md) and textures.</span></span>



| <span data-ttu-id="a5526-105">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="a5526-105">Interfaces</span></span>                                           | <span data-ttu-id="a5526-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a5526-106">Description</span></span>                                          |
|------------------------------------------------------|------------------------------------------------------|
| [<span data-ttu-id="a5526-107">**ID3D10Buffer-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a5526-107">**ID3D10Buffer Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)       | <span data-ttu-id="a5526-108">Greift auf Puffer Daten zu.</span><span class="sxs-lookup"><span data-stu-id="a5526-108">Accesses buffer data.</span></span>                                |
| [<span data-ttu-id="a5526-109">**ID3D10Resource-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a5526-109">**ID3D10Resource Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)   | <span data-ttu-id="a5526-110">Basisklasse für eine Ressource.</span><span class="sxs-lookup"><span data-stu-id="a5526-110">Base class for a resource.</span></span>                           |
| [<span data-ttu-id="a5526-111">**ID3D10Texture1D-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a5526-111">**ID3D10Texture1D Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture1d) | <span data-ttu-id="a5526-112">Greift auf Daten in einer 1D-Textur oder einem 1D-Textur Array zu.</span><span class="sxs-lookup"><span data-stu-id="a5526-112">Accesses data in a 1D texture or a 1D texture array.</span></span> |
| [<span data-ttu-id="a5526-113">**ID3D10Texture2D-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a5526-113">**ID3D10Texture2D Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d) | <span data-ttu-id="a5526-114">Greift auf Daten in einer 2D-Textur oder einem 2D-Textur Array zu.</span><span class="sxs-lookup"><span data-stu-id="a5526-114">Accesses data in a 2D texture or a 2D texture array</span></span>  |
| [<span data-ttu-id="a5526-115">**ID3D10Texture3D-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a5526-115">**ID3D10Texture3D Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture3d) | <span data-ttu-id="a5526-116">Greift auf Daten in einer 3D-Textur oder einem 3D-Textur Array zu.</span><span class="sxs-lookup"><span data-stu-id="a5526-116">Accesses data in a 3D texture or a 3D texture array.</span></span> |



 

<span data-ttu-id="a5526-117">Eine Anwendung verwendet eine Ansicht, um eine Ressource an eine [Pipeline Stufe](d3d10-graphics-programming-guide-pipeline-stages.md)zu binden.</span><span class="sxs-lookup"><span data-stu-id="a5526-117">An application uses a view to bind a resource to a [pipeline stage](d3d10-graphics-programming-guide-pipeline-stages.md).</span></span> <span data-ttu-id="a5526-118">Die [Sicht](d3d10-graphics-programming-guide-resources-access-views.md) definiert, wie während des Renderings auf die Ressource zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="a5526-118">The [view](d3d10-graphics-programming-guide-resources-access-views.md) defines how the resource can be accessed during rendering.</span></span> <span data-ttu-id="a5526-119">Die API enthält diese Ansichts Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="a5526-119">The API contains these view interfaces.</span></span>



| <span data-ttu-id="a5526-120">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="a5526-120">Interfaces</span></span>                                                               | <span data-ttu-id="a5526-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a5526-121">Description</span></span>                                                                                                  |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a5526-122">**ID3D10DepthStencilView-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a5526-122">**ID3D10DepthStencilView Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10depthstencilview)       | <span data-ttu-id="a5526-123">Greift auf Daten in einer [tiefen Schablone](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md) zu.</span><span class="sxs-lookup"><span data-stu-id="a5526-123">Accesses data in a [depth-stencil](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md) texture.</span></span> |
| [<span data-ttu-id="a5526-124">**ID3D10RenderTargetView-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a5526-124">**ID3D10RenderTargetView Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10rendertargetview)       | <span data-ttu-id="a5526-125">Greift auf Daten in einem [Renderziel](d3d10-graphics-programming-guide-resources-creating-textures.md)zu.</span><span class="sxs-lookup"><span data-stu-id="a5526-125">Accesses data in a [render target](d3d10-graphics-programming-guide-resources-creating-textures.md).</span></span>        |
| [<span data-ttu-id="a5526-126">**ID3D10ShaderResourceView-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a5526-126">**ID3D10ShaderResourceView Interface**</span></span>](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)   | <span data-ttu-id="a5526-127">Greift auf Daten in einer Shader-Ressource in Direct3D 10,0 zu.</span><span class="sxs-lookup"><span data-stu-id="a5526-127">Accesses data in a shader-resource in Direct3D 10.0.</span></span>                                                         |
| [<span data-ttu-id="a5526-128">**ID3D10ShaderResourceView1-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a5526-128">**ID3D10ShaderResourceView1 Interface**</span></span>](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10shaderresourceview1) | <span data-ttu-id="a5526-129">Greift auf Daten in einer Shader-Ressource in Direct3D 10,1 zu.</span><span class="sxs-lookup"><span data-stu-id="a5526-129">Accesses data in a shader-resource in Direct3D 10.1.</span></span>                                                         |
| [<span data-ttu-id="a5526-130">**ID3D10View-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a5526-130">**ID3D10View Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10view)                               | <span data-ttu-id="a5526-131">Basisklasse für eine Ansicht.</span><span class="sxs-lookup"><span data-stu-id="a5526-131">Base class for a view.</span></span>                                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="a5526-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a5526-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5526-133">Ressourcen Verweis</span><span class="sxs-lookup"><span data-stu-id="a5526-133">Resource Reference</span></span>](d3d10-graphics-reference-resource.md)
</dt> </dl>

 

 
