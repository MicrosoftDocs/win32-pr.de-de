---
description: Die IDirect3DDevice9-Schnittstelle unterstützt die Scheitelpunkt Verarbeitung in Software und Hardware.
ms.assetid: c1ac0382-1701-40e4-967a-d400ada96533
title: Verarbeiten von Scheitelpunkt Daten (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15d350dee4c8de361d02d0d0844968298534ee47
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860403"
---
# <a name="processing-vertex-data-direct3d-9"></a><span data-ttu-id="e33c8-103">Verarbeiten von Scheitelpunkt Daten (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e33c8-103">Processing Vertex Data (Direct3D 9)</span></span>

<span data-ttu-id="e33c8-104">Die [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle unterstützt die Scheitelpunkt Verarbeitung in Software und Hardware.</span><span class="sxs-lookup"><span data-stu-id="e33c8-104">The [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface supports vertex processing in both software and hardware.</span></span> <span data-ttu-id="e33c8-105">Im Allgemeinen sind die Gerätefunktionen für die Verarbeitung von Software-und Hardware Scheitel Punkten nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="e33c8-105">In general, the device capabilities for software and hardware vertex processing are not identical.</span></span> <span data-ttu-id="e33c8-106">Die Hardware Funktionen sind abhängig vom Anzeige Adapter und Treiber variabel, während die Softwarefunktionen korrigiert werden.</span><span class="sxs-lookup"><span data-stu-id="e33c8-106">Hardware capabilities are variable, depending on the display adapter and driver, while software capabilities are fixed.</span></span>

<span data-ttu-id="e33c8-107">Die folgenden Flags steuern das Scheitelpunkt Verarbeitungs Verhalten für die Hardware Abstraktionsschicht (HAL) und Referenzgeräte.</span><span class="sxs-lookup"><span data-stu-id="e33c8-107">The following flags control vertex processing behavior for the hardware abstraction layer (HAL) and reference devices.</span></span>

-   <span data-ttu-id="e33c8-108">D3DCREATE \_ Software \_ vertexprocessing</span><span class="sxs-lookup"><span data-stu-id="e33c8-108">D3DCREATE\_SOFTWARE\_VERTEXPROCESSING</span></span>
-   <span data-ttu-id="e33c8-109">D3DCREATE \_ Hardware \_ vertexprocessing</span><span class="sxs-lookup"><span data-stu-id="e33c8-109">D3DCREATE\_HARDWARE\_VERTEXPROCESSING</span></span>
-   <span data-ttu-id="e33c8-110">D3DCREATE \_ gemischte \_ vertexprocessing</span><span class="sxs-lookup"><span data-stu-id="e33c8-110">D3DCREATE\_MIXED\_VERTEXPROCESSING</span></span>

<span data-ttu-id="e33c8-111">Geben Sie beim Aufrufen von [**IDirect3D9:: createdevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)eines der vertexprozessorverhaltenflags an.</span><span class="sxs-lookup"><span data-stu-id="e33c8-111">Specify one of the vertex processing behavior flags when calling [**IDirect3D9::CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice).</span></span> <span data-ttu-id="e33c8-112">Mit dem Flag für den gemischten Modus kann das Gerät sowohl die Software-als auch die Hardware Vertex-Verarbeitung durchführen.</span><span class="sxs-lookup"><span data-stu-id="e33c8-112">The mixed-mode flag enables the device to perform both software and hardware vertex processing.</span></span> <span data-ttu-id="e33c8-113">Für ein Gerät kann jeweils nur ein vertexverarbeitungsflag festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e33c8-113">Only one vertex processing flag may be set for a device at any one time.</span></span> <span data-ttu-id="e33c8-114">Beachten Sie, dass das D3DCREATE \_ Hardware \_ vertexprocessing-Flag festgelegt werden muss, wenn ein reines Gerät (D3DCREATE \_ puredevice) erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="e33c8-114">Note that the D3DCREATE\_HARDWARE\_VERTEXPROCESSING flag is required to be set when creating a pure device (D3DCREATE\_PUREDEVICE).</span></span>

<span data-ttu-id="e33c8-115">Um duale Scheitelpunkt Verarbeitungsfunktionen auf einem einzelnen Gerät zu vermeiden, können nur die Hardware-Scheitelpunkt Verarbeitungsfunktionen zur Laufzeit abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="e33c8-115">To avoid dual vertex processing capabilities on a single device, only the hardware vertex processing capabilities can be queried at run time.</span></span> <span data-ttu-id="e33c8-116">Die Verarbeitungsfunktionen der Software-Scheitel Punkte sind korrigiert und können zur Laufzeit nicht abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="e33c8-116">Software vertex processing capabilities are fixed and cannot be queried at run time.</span></span>

<span data-ttu-id="e33c8-117">Der VertexProcessingCaps-Member der [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) -Struktur bestimmt die Hardware-Scheitelpunkt Verarbeitungsfunktionen des Geräts.</span><span class="sxs-lookup"><span data-stu-id="e33c8-117">The VertexProcessingCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure determines the hardware vertex processing capabilities of the device.</span></span>

<span data-ttu-id="e33c8-118">Bei der Verarbeitung von Software Scheitel Punkten werden die folgenden Funktionen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e33c8-118">For software vertex processing the following capabilities are supported.</span></span>

-   <span data-ttu-id="e33c8-119">der D3DVTXPCAPS \_ DirectionalLights-Member von [D3DVTXPCAPS](d3dvtxpcaps.md)</span><span class="sxs-lookup"><span data-stu-id="e33c8-119">the D3DVTXPCAPS\_DIRECTIONALLIGHTS member of [D3DVTXPCAPS](d3dvtxpcaps.md)</span></span>
-   <span data-ttu-id="e33c8-120">der D3DVTXPCAPS \_ localviewer-Member von [D3DVTXPCAPS](d3dvtxpcaps.md)</span><span class="sxs-lookup"><span data-stu-id="e33c8-120">the D3DVTXPCAPS\_LOCALVIEWER member of [D3DVTXPCAPS](d3dvtxpcaps.md)</span></span>
-   <span data-ttu-id="e33c8-121">der D3DVTXPCAPS \_ MATERIALSOURCE7-Member von [D3DVTXPCAPS](d3dvtxpcaps.md)</span><span class="sxs-lookup"><span data-stu-id="e33c8-121">the D3DVTXPCAPS\_MATERIALSOURCE7 member of [D3DVTXPCAPS](d3dvtxpcaps.md)</span></span>
-   <span data-ttu-id="e33c8-122">der D3DVTXPCAPS \_ positionallights-Member von [D3DVTXPCAPS](d3dvtxpcaps.md)</span><span class="sxs-lookup"><span data-stu-id="e33c8-122">the D3DVTXPCAPS\_POSITIONALLIGHTS member of [D3DVTXPCAPS](d3dvtxpcaps.md)</span></span>
-   <span data-ttu-id="e33c8-123">der D3DVTXPCAPS \_ TEXGEN-Member von [D3DVTXPCAPS](d3dvtxpcaps.md)</span><span class="sxs-lookup"><span data-stu-id="e33c8-123">the D3DVTXPCAPS\_TEXGEN member of [D3DVTXPCAPS](d3dvtxpcaps.md)</span></span>
-   <span data-ttu-id="e33c8-124">der D3DVTXPCAPS \_ Tweening-Member von [D3DVTXPCAPS](d3dvtxpcaps.md)</span><span class="sxs-lookup"><span data-stu-id="e33c8-124">the D3DVTXPCAPS\_TWEENING member of [D3DVTXPCAPS](d3dvtxpcaps.md)</span></span>

<span data-ttu-id="e33c8-125">Außerdem werden in der folgenden Tabelle die Werte aufgelistet, die für Member der [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) -Struktur für ein Gerät im Software Scheitelpunkt-Verarbeitungsmodus festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="e33c8-125">In addition, the following table lists the values that are set for members of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure for a device in software vertex processing mode.</span></span>



| <span data-ttu-id="e33c8-126">Member</span><span class="sxs-lookup"><span data-stu-id="e33c8-126">Member</span></span>                 | <span data-ttu-id="e33c8-127">Verarbeitungsfunktionen für Software Scheitel Punkte</span><span class="sxs-lookup"><span data-stu-id="e33c8-127">Software vertex processing capabilities</span></span> |
|------------------------|-----------------------------------------|
| <span data-ttu-id="e33c8-128">MaxActiveLights</span><span class="sxs-lookup"><span data-stu-id="e33c8-128">MaxActiveLights</span></span>        | <span data-ttu-id="e33c8-129">Unbegrenzt</span><span class="sxs-lookup"><span data-stu-id="e33c8-129">Unlimited</span></span>                               |
| <span data-ttu-id="e33c8-130">Maxuserclipplane</span><span class="sxs-lookup"><span data-stu-id="e33c8-130">MaxUserClipPlanes</span></span>      | <span data-ttu-id="e33c8-131">6</span><span class="sxs-lookup"><span data-stu-id="e33c8-131">6</span></span>                                       |
| <span data-ttu-id="e33c8-132">Maxvertexblendmatrices</span><span class="sxs-lookup"><span data-stu-id="e33c8-132">MaxVertexBlendMatrices</span></span> | <span data-ttu-id="e33c8-133">4</span><span class="sxs-lookup"><span data-stu-id="e33c8-133">4</span></span>                                       |
| <span data-ttu-id="e33c8-134">Maxstreams</span><span class="sxs-lookup"><span data-stu-id="e33c8-134">MaxStreams</span></span>             | <span data-ttu-id="e33c8-135">16</span><span class="sxs-lookup"><span data-stu-id="e33c8-135">16</span></span>                                      |
| <span data-ttu-id="e33c8-136">MaxVertexIndex</span><span class="sxs-lookup"><span data-stu-id="e33c8-136">MaxVertexIndex</span></span>         | <span data-ttu-id="e33c8-137">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="e33c8-137">0xFFFFFFFF</span></span>                              |



 

<span data-ttu-id="e33c8-138">Im Allgemeinen sollte jede Anwendung, bei der die Vertexverarbeitung gebunden ist, ein HAL-Gerät verwenden.</span><span class="sxs-lookup"><span data-stu-id="e33c8-138">In general, any application that is vertex processing bound should use a HAL device.</span></span> <span data-ttu-id="e33c8-139">Die Verarbeitung von Software Scheitel Punkten bietet eine garantierte Reihe von vertexverarbeitungs Funktionen, einschließlich einer unbegrenzten Anzahl von Lichtern und vollständiger Unterstützung für programmierbare Vertex-Shader.</span><span class="sxs-lookup"><span data-stu-id="e33c8-139">Software vertex processing provides a guaranteed set of vertex processing capabilities, including an unbounded number of lights and full support for programmable vertex shaders.</span></span> <span data-ttu-id="e33c8-140">Sie können jederzeit zwischen der Verarbeitung von Software-und Hardware Scheitel Punkten wechseln, wenn Sie das HAL-Gerät verwenden (Hierbei handelt es sich um den einzigen Gerätetyp, der die Verarbeitung von Hardware-und Software Scheitel Punkten unterstützt).</span><span class="sxs-lookup"><span data-stu-id="e33c8-140">You can toggle between software and hardware vertex processing at any time when using the HAL device (which is the only device type that supports both hardware and software vertex processing).</span></span> <span data-ttu-id="e33c8-141">Die einzige Voraussetzung ist, dass Vertex-Puffer, die für die Verarbeitung von Software Vertex verwendet werden, im Systemspeicher zugeordnet werden müssen</span><span class="sxs-lookup"><span data-stu-id="e33c8-141">The only requirement is that vertex buffers used for software vertex processing must be allocated in system memory.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e33c8-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e33c8-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e33c8-143">Direct3D-Geräte</span><span class="sxs-lookup"><span data-stu-id="e33c8-143">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 
