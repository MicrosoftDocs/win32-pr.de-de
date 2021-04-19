---
description: Ein Zustands Block kann zum Erfassen aller Gerätezustände verwendet werden (siehe Status Blöcke speichern und Wiederherstellen (Direct3D 9)).
ms.assetid: e14077e4-1453-4aa3-b2de-4d3a829a819a
title: Speichern aller Gerätezustände mit einem stateblock (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bfdb4f9b3a9c1e33c2e8e7f50765f1656bd59e1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106345598"
---
# <a name="saving-all-device-states-with-a-stateblock-direct3d-9"></a><span data-ttu-id="e4b6a-103">Speichern aller Gerätezustände mit einem stateblock (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e4b6a-103">Saving All Device States with a StateBlock (Direct3D 9)</span></span>

<span data-ttu-id="e4b6a-104">Ein Zustands Block kann zum Erfassen aller Gerätezustände verwendet werden (siehe [Status Blöcke speichern und Wiederherstellen (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span><span class="sxs-lookup"><span data-stu-id="e4b6a-104">A state block can be used to capture all device states (see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span></span> <span data-ttu-id="e4b6a-105">Die folgenden Zustands Elemente sind im Gerätestatus enthalten:</span><span class="sxs-lookup"><span data-stu-id="e4b6a-105">The following state elements are included in the device state:</span></span>

-   <span data-ttu-id="e4b6a-106">Scheitelpunkt Status (siehe [Speichern von Scheitelpunkt Zuständen mit einem stateblock (Direct3D 9)](saving-vertex-states-with-a-stateblock.md)).</span><span class="sxs-lookup"><span data-stu-id="e4b6a-106">Vertex state (see [Saving Vertex States With a StateBlock (Direct3D 9)](saving-vertex-states-with-a-stateblock.md)).</span></span>
-   <span data-ttu-id="e4b6a-107">Pixel Zustand (siehe [Speichern des Pixel Zustands mit einem stateblock (Direct3D 9)](saving-pixel-states-with-a-stateblock.md)).</span><span class="sxs-lookup"><span data-stu-id="e4b6a-107">Pixel state (see [Saving Pixel State With a StateBlock (Direct3D 9)](saving-pixel-states-with-a-stateblock.md)).</span></span>
-   <span data-ttu-id="e4b6a-108">Jede Textur, die einem Sampler zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="e4b6a-108">Each texture assigned to a sampler.</span></span>
-   <span data-ttu-id="e4b6a-109">Jede Scheitelpunkt Textur.</span><span class="sxs-lookup"><span data-stu-id="e4b6a-109">Each vertex texture.</span></span>
-   <span data-ttu-id="e4b6a-110">Jede Verschiebungs Karten Textur.</span><span class="sxs-lookup"><span data-stu-id="e4b6a-110">Each displacement map texture.</span></span>
-   <span data-ttu-id="e4b6a-111">Die aktuelle Texturpalette.</span><span class="sxs-lookup"><span data-stu-id="e4b6a-111">The current texture palette.</span></span>
-   <span data-ttu-id="e4b6a-112">Für jeden vertexstream: ein Zeiger auf den Vertex-Puffer, jedes Argument aus [**IDirect3DDevice9:: SetStreamSource**](/windows/desktop/api)und der unter Teiler (sofern vorhanden) von [**IDirect3DDevice9:: setstreamsourcefreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq).</span><span class="sxs-lookup"><span data-stu-id="e4b6a-112">For each vertex stream: a pointer to the vertex buffer, each argument from [**IDirect3DDevice9::SetStreamSource**](/windows/desktop/api), and the divider (if any) from [**IDirect3DDevice9::SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq).</span></span>
-   <span data-ttu-id="e4b6a-113">Ein Zeiger auf den Index Puffer.</span><span class="sxs-lookup"><span data-stu-id="e4b6a-113">A pointer to the index buffer.</span></span>
-   <span data-ttu-id="e4b6a-114">Der Viewport.</span><span class="sxs-lookup"><span data-stu-id="e4b6a-114">The viewport.</span></span>
-   <span data-ttu-id="e4b6a-115">Das Scheren Rechteck.</span><span class="sxs-lookup"><span data-stu-id="e4b6a-115">The scissors rectangle.</span></span>
-   <span data-ttu-id="e4b6a-116">Die Matrizen "World", "View" und "Projection".</span><span class="sxs-lookup"><span data-stu-id="e4b6a-116">The world, view, and projection matrices.</span></span>
-   <span data-ttu-id="e4b6a-117">Die Textur Transformationen.</span><span class="sxs-lookup"><span data-stu-id="e4b6a-117">The texture transforms.</span></span>
-   <span data-ttu-id="e4b6a-118">Die Clippingebenen (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="e4b6a-118">The clipping planes (if any).</span></span>
-   <span data-ttu-id="e4b6a-119">Das aktuelle Material.</span><span class="sxs-lookup"><span data-stu-id="e4b6a-119">The current material.</span></span>

<span data-ttu-id="e4b6a-120">Um alle Gerätezustände mit einem Zustands Block zu erfassen, geben Sie D3DSBT all an, \_ Wenn Sie [**IDirect3DDevice9:: createstateblock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e4b6a-120">To capture all device states with a state block, specify D3DSBT\_ALL when calling [**IDirect3DDevice9::CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4b6a-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e4b6a-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4b6a-122">Status Blöcke speichern und Wiederherstellen</span><span class="sxs-lookup"><span data-stu-id="e4b6a-122">State Blocks Save and Restore State</span></span>](state-blocks-save-and-restore-state.md)
</dt> </dl>

 

 
