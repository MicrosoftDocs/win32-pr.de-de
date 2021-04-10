---
description: D3DDEVCAPS2-treiberfunktionsflags.
ms.assetid: 3f3b9f86-dee3-4506-bd2e-1dcc8ba617ed
title: D3DDEVCAPS2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e774076f5ad93abf5ab1ffc343f573497592728f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214132"
---
# <a name="d3ddevcaps2"></a><span data-ttu-id="a8761-103">D3DDEVCAPS2</span><span class="sxs-lookup"><span data-stu-id="a8761-103">D3DDEVCAPS2</span></span>

<span data-ttu-id="a8761-104">D3DDEVCAPS2-treiberfunktionsflags.</span><span class="sxs-lookup"><span data-stu-id="a8761-104">D3DDEVCAPS2 driver capability flags.</span></span>



|                                                 |                                                                                                                                                                                                                           |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8761-105">\#definieren</span><span class="sxs-lookup"><span data-stu-id="a8761-105">\#define</span></span>                                        | <span data-ttu-id="a8761-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a8761-106">Description</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="a8761-107">D3DDEVCAPS2 \_ adaptivetess-Patch</span><span class="sxs-lookup"><span data-stu-id="a8761-107">D3DDEVCAPS2\_ADAPTIVETESSRTPATCH</span></span>                | <span data-ttu-id="a8761-108">Das Gerät unterstützt das adaptive Mosaik von RT-Patches.</span><span class="sxs-lookup"><span data-stu-id="a8761-108">Device supports adaptive tessellation of RT-patches</span></span>                                                                                                                                                                       |
| <span data-ttu-id="a8761-109">D3DDEVCAPS2 \_ adaptivetess npatch</span><span class="sxs-lookup"><span data-stu-id="a8761-109">D3DDEVCAPS2\_ADAPTIVETESSNPATCH</span></span>                 | <span data-ttu-id="a8761-110">Das Gerät unterstützt das adaptive Mosaik von N-Patches.</span><span class="sxs-lookup"><span data-stu-id="a8761-110">Device supports adaptive tessellation of N-patches.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="a8761-111">D3DDEVCAPS2 \_ kann \_ \_ von \_ Texturen gestrebe werden.</span><span class="sxs-lookup"><span data-stu-id="a8761-111">D3DDEVCAPS2\_CAN\_STRETCHRECT\_FROM\_TEXTURES</span></span>   | <span data-ttu-id="a8761-112">Das Gerät unterstützt [**stretchrect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect) mithilfe einer Textur als Quelle.</span><span class="sxs-lookup"><span data-stu-id="a8761-112">Device supports [**StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect) using a texture as the source.</span></span>                                                                                                                       |
| <span data-ttu-id="a8761-113">D3DDEVCAPS2 \_ dmapnpatch</span><span class="sxs-lookup"><span data-stu-id="a8761-113">D3DDEVCAPS2\_DMAPNPATCH</span></span>                         | <span data-ttu-id="a8761-114">Das Gerät unterstützt Verschiebungs Zuordnungen für N-Patches.</span><span class="sxs-lookup"><span data-stu-id="a8761-114">Device supports displacement maps for N-patches.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="a8761-115">D3DDEVCAPS2 \_ presampleddmapnpatch</span><span class="sxs-lookup"><span data-stu-id="a8761-115">D3DDEVCAPS2\_PRESAMPLEDDMAPNPATCH</span></span>               | <span data-ttu-id="a8761-116">Das Gerät unterstützt die Verschiebungs Zuordnungen für N-Patches.</span><span class="sxs-lookup"><span data-stu-id="a8761-116">Device supports presampled displacement maps for N-patches.</span></span> <span data-ttu-id="a8761-117">Weitere Informationen zur Verschiebungs Zuordnung finden Sie unter [Verschiebungs Zuordnung (Direct3D 9)](displacement-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="a8761-117">For more information about displacement mapping, see [Displacement Mapping (Direct3D 9)](displacement-mapping.md).</span></span>                                           |
| <span data-ttu-id="a8761-118">D3DDEVCAPS2 \_ Streamoffset</span><span class="sxs-lookup"><span data-stu-id="a8761-118">D3DDEVCAPS2\_STREAMOFFSET</span></span>                       | <span data-ttu-id="a8761-119">Das Gerät unterstützt streamoffsets.</span><span class="sxs-lookup"><span data-stu-id="a8761-119">Device supports stream offsets.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="a8761-120">D3DDEVCAPS2 \_ vertexelementscansharestreamoffset</span><span class="sxs-lookup"><span data-stu-id="a8761-120">D3DDEVCAPS2\_VERTEXELEMENTSCANSHARESTREAMOFFSET</span></span> | <span data-ttu-id="a8761-121">Mehrere Scheitelpunkt Elemente können denselben Offset in einem Datenstrom gemeinsam verwenden, wenn D3DDEVCAPS2 \_ vertexelementscansharestreamoffset vom Gerät festgelegt wird und die Vertexdeklaration kein Element mit D3DDECLUSAGE \_ POSITIONT0 enthält.</span><span class="sxs-lookup"><span data-stu-id="a8761-121">Multiple vertex elements can share the same offset in a stream if D3DDEVCAPS2\_VERTEXELEMENTSCANSHARESTREAMOFFSET is set by the device and the vertex declaration does not have an element with D3DDECLUSAGE\_POSITIONT0.</span></span> |



 

## <a name="constant-information"></a><span data-ttu-id="a8761-122">Konstante Informationen</span><span class="sxs-lookup"><span data-stu-id="a8761-122">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="a8761-123">Header</span><span class="sxs-lookup"><span data-stu-id="a8761-123">Header</span></span>                   | <span data-ttu-id="a8761-124">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="a8761-124">d3d9caps.h</span></span> |
| <span data-ttu-id="a8761-125">Mindestens Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="a8761-125">Minimum operating system</span></span> | <span data-ttu-id="a8761-126">Windows 98</span><span class="sxs-lookup"><span data-stu-id="a8761-126">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a8761-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a8761-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8761-128">Direct3D-Konstanten</span><span class="sxs-lookup"><span data-stu-id="a8761-128">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
