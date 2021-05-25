---
description: D3DDEVCAPS2-Treiberfunktionsflags.
ms.assetid: 3f3b9f86-dee3-4506-bd2e-1dcc8ba617ed
title: D3DDEVCAPS2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6296db9b338d5f9a8c8ede702a784baf1fdfd462
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343205"
---
# <a name="d3ddevcaps2"></a><span data-ttu-id="98a31-103">D3DDEVCAPS2</span><span class="sxs-lookup"><span data-stu-id="98a31-103">D3DDEVCAPS2</span></span>

<span data-ttu-id="98a31-104">D3DDEVCAPS2-Treiberfunktionsflags.</span><span class="sxs-lookup"><span data-stu-id="98a31-104">D3DDEVCAPS2 driver capability flags.</span></span>



| <span data-ttu-id="98a31-105">\#Definieren</span><span class="sxs-lookup"><span data-stu-id="98a31-105">\#define</span></span>                                        | <span data-ttu-id="98a31-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="98a31-106">Description</span></span>                                                                                                                                                                                                               |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98a31-107">D3DDEVCAPS2 \_ ADAPTIVETESSRTPATCH</span><span class="sxs-lookup"><span data-stu-id="98a31-107">D3DDEVCAPS2\_ADAPTIVETESSRTPATCH</span></span>                | <span data-ttu-id="98a31-108">Das Gerät unterstützt die adaptive Mosaikierung von RT-Patches.</span><span class="sxs-lookup"><span data-stu-id="98a31-108">Device supports adaptive tessellation of RT-patches</span></span>                                                                                                                                                                       |
| <span data-ttu-id="98a31-109">D3DDEVCAPS2 \_ ADAPTIVETESSNPATCH</span><span class="sxs-lookup"><span data-stu-id="98a31-109">D3DDEVCAPS2\_ADAPTIVETESSNPATCH</span></span>                 | <span data-ttu-id="98a31-110">Das Gerät unterstützt die adaptive Mosaikierung von N-Patches.</span><span class="sxs-lookup"><span data-stu-id="98a31-110">Device supports adaptive tessellation of N-patches.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="98a31-111">D3DDEVCAPS2 \_ KANN \_ \_ STRETCHRECT AUS \_ TEXTUREN ZIEHEN.</span><span class="sxs-lookup"><span data-stu-id="98a31-111">D3DDEVCAPS2\_CAN\_STRETCHRECT\_FROM\_TEXTURES</span></span>   | <span data-ttu-id="98a31-112">Das Gerät unterstützt [**StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect) mithilfe einer Textur als Quelle.</span><span class="sxs-lookup"><span data-stu-id="98a31-112">Device supports [**StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect) using a texture as the source.</span></span>                                                                                                                       |
| <span data-ttu-id="98a31-113">D3DDEVCAPS2 \_ DMAPNPATCH</span><span class="sxs-lookup"><span data-stu-id="98a31-113">D3DDEVCAPS2\_DMAPNPATCH</span></span>                         | <span data-ttu-id="98a31-114">Das Gerät unterstützt Verschiebungszuordnungen für N-Patches.</span><span class="sxs-lookup"><span data-stu-id="98a31-114">Device supports displacement maps for N-patches.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="98a31-115">D3DDEVCAPS2 \_ PRESAMPLEDDMAPNPATCH</span><span class="sxs-lookup"><span data-stu-id="98a31-115">D3DDEVCAPS2\_PRESAMPLEDDMAPNPATCH</span></span>               | <span data-ttu-id="98a31-116">Das Gerät unterstützt vorsampelte Verschiebungszuordnungen für N-Patches.</span><span class="sxs-lookup"><span data-stu-id="98a31-116">Device supports presampled displacement maps for N-patches.</span></span> <span data-ttu-id="98a31-117">Weitere Informationen zur Verschiebungszuordnung finden Sie unter [Verschiebungszuordnung (Direct3D 9).](displacement-mapping.md)</span><span class="sxs-lookup"><span data-stu-id="98a31-117">For more information about displacement mapping, see [Displacement Mapping (Direct3D 9)](displacement-mapping.md).</span></span>                                           |
| <span data-ttu-id="98a31-118">D3DDEVCAPS2 \_ STREAMOFFSET</span><span class="sxs-lookup"><span data-stu-id="98a31-118">D3DDEVCAPS2\_STREAMOFFSET</span></span>                       | <span data-ttu-id="98a31-119">Das Gerät unterstützt Streamoffsets.</span><span class="sxs-lookup"><span data-stu-id="98a31-119">Device supports stream offsets.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="98a31-120">D3DDEVCAPS2 \_ VERTEXELEMENTSCANSHARESTREAMOFFSET</span><span class="sxs-lookup"><span data-stu-id="98a31-120">D3DDEVCAPS2\_VERTEXELEMENTSCANSHARESTREAMOFFSET</span></span> | <span data-ttu-id="98a31-121">Mehrere Vertexelemente können denselben Offset in einem Stream gemeinsam nutzen, wenn D3DDEVCAPS2 \_ VERTEXELEMENTSCANSHARESTREAMOFFSET vom Gerät festgelegt wird und die Scheitelpunktdeklaration kein Element mit D3DDECLUSAGE \_ POSITIONT0 aufwies.</span><span class="sxs-lookup"><span data-stu-id="98a31-121">Multiple vertex elements can share the same offset in a stream if D3DDEVCAPS2\_VERTEXELEMENTSCANSHARESTREAMOFFSET is set by the device and the vertex declaration does not have an element with D3DDECLUSAGE\_POSITIONT0.</span></span> |



 

## <a name="constant-information"></a><span data-ttu-id="98a31-122">Konstante Informationen</span><span class="sxs-lookup"><span data-stu-id="98a31-122">Constant Information</span></span>



| <span data-ttu-id="98a31-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="98a31-123">Requirement</span></span>                         | <span data-ttu-id="98a31-124">Wert</span><span class="sxs-lookup"><span data-stu-id="98a31-124">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="98a31-125">Header</span><span class="sxs-lookup"><span data-stu-id="98a31-125">Header</span></span>                   | <span data-ttu-id="98a31-126">d3d9caps.h</span><span class="sxs-lookup"><span data-stu-id="98a31-126">d3d9caps.h</span></span> |
| <span data-ttu-id="98a31-127">Mindestbetriebssystem</span><span class="sxs-lookup"><span data-stu-id="98a31-127">Minimum operating system</span></span> | <span data-ttu-id="98a31-128">Windows 98</span><span class="sxs-lookup"><span data-stu-id="98a31-128">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="98a31-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="98a31-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98a31-130">Direct3D-Konstanten</span><span class="sxs-lookup"><span data-stu-id="98a31-130">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
