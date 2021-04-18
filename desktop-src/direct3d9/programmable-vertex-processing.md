---
description: Wenn Sie einen programmierten Vertex-Shader verwenden, werden die Elemente, die im Ziel Vertex-Puffer aktualisiert werden, vom Shader-Funktionsprogramm gesteuert.
ms.assetid: c75564ef-528b-4af5-9ed7-a32b9120bf6a
title: Programmierbare Vertex-Verarbeitung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5108792350aebbca4f58924fde81d191b062591b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344794"
---
# <a name="programmable-vertex-processing-direct3d-9"></a><span data-ttu-id="5da7f-103">Programmierbare Vertex-Verarbeitung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="5da7f-103">Programmable Vertex Processing (Direct3D 9)</span></span>

<span data-ttu-id="5da7f-104">Wenn Sie einen programmierten Vertex-Shader verwenden, werden die Elemente, die im Ziel Vertex-Puffer aktualisiert werden, vom Shader-Funktionsprogramm gesteuert.</span><span class="sxs-lookup"><span data-stu-id="5da7f-104">When using a programmed vertex shader, the elements updated in the destination vertex buffer are controlled by the shader function program.</span></span> <span data-ttu-id="5da7f-105">Wenn die Anwendung in eines der Ziel-Vertex-Register schreibt, wird das entsprechende Element in jedem Scheitelpunkt des Ziel Vertex-Puffers aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="5da7f-105">When the application writes to one of the destination vertex registers, the corresponding element within each vertex of the destination vertex buffer is updated.</span></span> <span data-ttu-id="5da7f-106">Elemente im Ziel Vertex-Puffer, auf die nicht von der Anwendung geschrieben wird, werden nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="5da7f-106">Elements in the destination vertex buffer that are not written to by the application are not modified.</span></span> <span data-ttu-id="5da7f-107">[**IDirect3DDevice9::P rocess Vertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) schlägt fehl, wenn die Anwendung in Elemente schreibt, die nicht im Ziel Vertex-Puffer vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="5da7f-107">[**IDirect3DDevice9::ProcessVertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) will fail if the application writes to elements that are not present in the destination vertex buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5da7f-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5da7f-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5da7f-109">Vertex-Puffer</span><span class="sxs-lookup"><span data-stu-id="5da7f-109">Vertex Buffers</span></span>](vertex-buffers.md)
</dt> </dl>

 

 
