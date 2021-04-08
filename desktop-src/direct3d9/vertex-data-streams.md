---
description: Die renderingschnittstellen für Direct3D bestehen aus Methoden zum Rendern von primitiven aus Scheitelpunkt Daten, die in einem oder mehreren Daten Puffern gespeichert sind.
ms.assetid: e89eae14-f480-470c-b301-f7ff316ad339
title: Vertex-Datenströme (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efd45fc3f645de49060cd201a6a6e9e238712338
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746104"
---
# <a name="vertex-data-streams-direct3d-9"></a><span data-ttu-id="c0224-103">Vertex-Datenströme (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c0224-103">Vertex Data Streams (Direct3D 9)</span></span>

<span data-ttu-id="c0224-104">Die renderingschnittstellen für Direct3D bestehen aus Methoden zum Rendern von primitiven aus Scheitelpunkt Daten, die in einem oder mehreren Daten Puffern gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="c0224-104">The rendering interfaces for Direct3D consist of methods that render primitives from vertex data stored in one or more data buffers.</span></span> <span data-ttu-id="c0224-105">Vertex-Daten bestehen aus Vertex-Elementen, die zum bilden von Scheitelpunkt Komponenten kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="c0224-105">Vertex data consists of vertex elements combined to form vertex components.</span></span> <span data-ttu-id="c0224-106">Vertex-Elemente, die kleinste Einheit eines Scheitel Punkts, stellen Entitäten dar, z. b. Position, normal oder Farbe.</span><span class="sxs-lookup"><span data-stu-id="c0224-106">Vertex elements, the smallest unit of a vertex, represent entities such as position, normal, or color.</span></span>

<span data-ttu-id="c0224-107">Bei Scheitelpunkt Komponenten handelt es sich um ein oder mehrere Vertex-Elemente, die in einem einzelnen Speicherpuffer zusammenhängend (verschachtelt pro Scheitelpunkt) gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="c0224-107">Vertex components are one or more vertex elements stored contiguously (interleaved per vertex) in a single memory buffer.</span></span> <span data-ttu-id="c0224-108">Ein kompletter Scheitelpunkt besteht aus einer oder mehreren Komponenten, wobei sich jede Komponente in einem separaten Speicherpuffer befindet.</span><span class="sxs-lookup"><span data-stu-id="c0224-108">A complete vertex consists of one or more components, where each component is in a separate memory buffer.</span></span> <span data-ttu-id="c0224-109">Zum Rendering eines primitiven werden mehrere Scheitelpunkt Komponenten gelesen und zusammengestellt, sodass für die Vertexverarbeitung umfassende Scheitel Punkte verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="c0224-109">To render a primitive, multiple vertex components are read and assembled so that complete vertices are available for vertex processing.</span></span> <span data-ttu-id="c0224-110">Das folgende Diagramm zeigt den Prozess des Renderings primitiver mithilfe von Scheitelpunkt Komponenten.</span><span class="sxs-lookup"><span data-stu-id="c0224-110">The following diagram shows the process of rendering primitives using vertex components.</span></span>

![Diagramm des Prozesses zum Rendering von primitiven mithilfe von Scheitelpunkt Komponenten](images/vertexdata.png)

<span data-ttu-id="c0224-112">Das Rendern von primitiven besteht aus zwei Schritten.</span><span class="sxs-lookup"><span data-stu-id="c0224-112">Rendering primitives consists of two steps.</span></span> <span data-ttu-id="c0224-113">Richten Sie zuerst einen oder mehrere Scheitelpunkt-komponentenstreams ein. Rufen Sie zweitens eine [**IDirect3DDevice9::D rawprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) -Methode auf, um diese Datenströme zu Rendering.</span><span class="sxs-lookup"><span data-stu-id="c0224-113">First, set up one or more vertex component streams; second, invoke a [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) method to render from those streams.</span></span> <span data-ttu-id="c0224-114">Die Identifizierung der Scheitelpunkt Elemente innerhalb dieser komponentenstreams wird vom Vertexshader angegeben.</span><span class="sxs-lookup"><span data-stu-id="c0224-114">Identification of vertex elements within these component streams is specified by the vertex shader.</span></span>

<span data-ttu-id="c0224-115">Die [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) -Methoden geben einen Offset in den Vertex-Datenströmen an, sodass eine beliebige zusammenhängende Teilmenge der primitiven innerhalb eines Satzes von Scheitelpunkt Daten mit jedem Zeichnen-Aufruf gerendert werden kann.</span><span class="sxs-lookup"><span data-stu-id="c0224-115">The [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) methods specify an offset in the vertex data streams so that an arbitrary contiguous subset of the primitives within one set of vertex data can be rendered with each draw invocation.</span></span> <span data-ttu-id="c0224-116">Dies ermöglicht es Ihnen, den Renderingzustand des Geräts zwischen Gruppen primitiver Elemente zu ändern, die aus denselben Scheitelpunkt Puffern gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="c0224-116">This enables you to change the device rendering state between groups of primitives that are rendered from the same vertex buffers.</span></span>

<span data-ttu-id="c0224-117">Indizierte und nicht indizierte Zeichnungs Methoden werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c0224-117">Both indexed and nonindexed drawing methods are supported.</span></span> <span data-ttu-id="c0224-118">Weitere Informationen finden Sie unter [Rendering from Scheitelpunkt and Index Buffers (Direct3D 9)](rendering-from-vertex-and-index-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="c0224-118">For more information, see [Rendering from Vertex and Index Buffers (Direct3D 9)](rendering-from-vertex-and-index-buffers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c0224-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c0224-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0224-120">Rendern von primitiven</span><span class="sxs-lookup"><span data-stu-id="c0224-120">Rendering Primitives</span></span>](rendering-primitives.md)
</dt> </dl>

 

 
