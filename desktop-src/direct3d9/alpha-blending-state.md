---
description: Der Alpha-Wert einer Farbe steuert seine Transparenz. Durch das Aktivieren von Alpha Blending können Farben, Materialien und Texturen auf einer Oberfläche mit Transparenz auf eine andere Oberfläche gemischt werden.
ms.assetid: e8e925d5-262d-45c0-be9f-21c9a103d7b7
title: Alpha Mischungs Zustand (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 884ecad07fb9aefba08a0abbab92969937ec6361
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393122"
---
# <a name="alpha-blending-state-direct3d-9"></a><span data-ttu-id="1ddc9-104">Alpha Mischungs Zustand (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1ddc9-104">Alpha Blending State (Direct3D 9)</span></span>

<span data-ttu-id="1ddc9-105">Der Alpha-Wert einer Farbe steuert seine Transparenz.</span><span class="sxs-lookup"><span data-stu-id="1ddc9-105">The alpha value of a color controls its transparency.</span></span> <span data-ttu-id="1ddc9-106">Durch das Aktivieren von Alpha Blending können Farben, Materialien und Texturen auf einer Oberfläche mit Transparenz auf eine andere Oberfläche gemischt werden.</span><span class="sxs-lookup"><span data-stu-id="1ddc9-106">Enabling alpha blending allows colors, materials, and textures on a surface to be blended with transparency onto another surface.</span></span>

<span data-ttu-id="1ddc9-107">Weitere Informationen finden Sie unter [Alpha Textur blending (Direct3D 9)](alpha-texture-blending.md) und [Textur blending (Direct3D 9)](texture-blending.md).</span><span class="sxs-lookup"><span data-stu-id="1ddc9-107">For more information, see [Alpha Texture Blending (Direct3D 9)](alpha-texture-blending.md) and [Texture Blending (Direct3D 9)](texture-blending.md).</span></span>

<span data-ttu-id="1ddc9-108">In C++ geschriebene Anwendungen verwenden den [**D3DRS \_ AlphaBlendEnable**](./d3drenderstatetype.md) -Rendering-Status, um Alpha-Transparenz-Blending zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="1ddc9-108">Applications written in C++ use the [**D3DRS\_ALPHABLENDENABLE**](./d3drenderstatetype.md) render state to enable alpha transparency blending.</span></span> <span data-ttu-id="1ddc9-109">Die Direct3D-API ermöglicht viele Arten von Alpha Blending.</span><span class="sxs-lookup"><span data-stu-id="1ddc9-109">The Direct3D API allows many types of alpha blending.</span></span> <span data-ttu-id="1ddc9-110">Es ist jedoch wichtig zu beachten, dass die 3D-Hardware des Benutzers möglicherweise nicht alle Mischungs Zustände unterstützt, die von Direct3D zugelassen werden.</span><span class="sxs-lookup"><span data-stu-id="1ddc9-110">However, it is important to note the user's 3D hardware might not support all the blending states allowed by Direct3D.</span></span>

<span data-ttu-id="1ddc9-111">Der Typ der durchgeführten Alpha Mischung hängt von den [**D3DRS \_ srcblend**](./d3drenderstatetype.md) -und **D3DRS \_ destblend** -Rendering-Zuständen ab.</span><span class="sxs-lookup"><span data-stu-id="1ddc9-111">The type of alpha blending that is done depends on the [**D3DRS\_SRCBLEND**](./d3drenderstatetype.md) And **D3DRS\_DESTBLEND** render states.</span></span> <span data-ttu-id="1ddc9-112">Quell-und Ziel-Blend-Zustände werden paarweise verwendet.</span><span class="sxs-lookup"><span data-stu-id="1ddc9-112">Source and destination blend states are used in pairs.</span></span> <span data-ttu-id="1ddc9-113">Im folgenden Codebeispiel wird veranschaulicht, wie der Source Blend-Status auf D3DBLEND \_ srccolor und der Ziel-Blend-Zustand auf D3DBLEND \_ invsrccolor festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1ddc9-113">The following code example demonstrates how the source blend state is set to D3DBLEND\_SRCCOLOR and the destination blend state is set to D3DBLEND\_INVSRCCOLOR.</span></span>


```
// This code example assumes that d3dDevice is a
// valid pointer to an IDirect3DDevice9 interface.

// Set the source blend state.
d3dDevice->SetRenderState(D3DRS_SRCBLEND, D3DBLEND_SRCCOLOR);

// Set the destination blend state.

d3dDevice->SetRenderState(D3DRS_DESTBLEND, D3DBLEND_INVSRCCOLOR);
```



<span data-ttu-id="1ddc9-114">Das Ändern der Quell-und Ziel-Blend-Zustände kann die Darstellung von selbst leuchtendes-Objekten in einer nebligen oder Dusty-Atmosphäre aufweisen.</span><span class="sxs-lookup"><span data-stu-id="1ddc9-114">Altering the source and destination blend states can give the appearance of emissive objects in a foggy or dusty atmosphere.</span></span> <span data-ttu-id="1ddc9-115">Wenn Ihre Anwendung z. b. in einer fernen-Umgebung Flammen modelliert, Felder, Plasma Balken oder ähnlich strahlende Objekte erzwingt, legen Sie den Quell-und den Ziel-Blend-Status auf D3DBLEND \_ One fest.</span><span class="sxs-lookup"><span data-stu-id="1ddc9-115">For instance, if your application models flames, force fields, plasma beams, or similarly radiant objects in a foggy environment, set the source and destination blend states to D3DBLEND\_ONE.</span></span>

<span data-ttu-id="1ddc9-116">Eine andere Anwendung der Alpha Mischung ist die Steuerung der Beleuchtung in einer 3D-Szene, die auch als leichte Zuordnung bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="1ddc9-116">Another application of alpha blending is to control the lighting in a 3D scene, also called light mapping.</span></span> <span data-ttu-id="1ddc9-117">Wenn Sie den Source Blend-Status auf D3DBLEND \_ Zero und den Ziel-Blend-Zustand auf D3DBLEND \_ srcalpha festlegen, wird eine Szene entsprechend den Quell-Alpha Informationen dunkel.</span><span class="sxs-lookup"><span data-stu-id="1ddc9-117">Setting the source blend state to D3DBLEND\_ZERO and the destination blend state to D3DBLEND\_SRCALPHA darkens a scene according to the source alpha information.</span></span> <span data-ttu-id="1ddc9-118">Der Quell primitive wird als eine Licht Zuordnung verwendet, die den Inhalt des Frame Puffers skaliert, um ihn bei Bedarf zu darfiltern.</span><span class="sxs-lookup"><span data-stu-id="1ddc9-118">The source primitive is used as a light map that scales the contents of the frame buffer to darken it when appropriate.</span></span> <span data-ttu-id="1ddc9-119">Dies erzeugt eine monochrome helle Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="1ddc9-119">This produces monochrome light mapping.</span></span>

<span data-ttu-id="1ddc9-120">Sie können die Farb Füll Zuordnung erreichen, indem Sie den Quell-Alpha-Mischungs Zustand auf D3DBLEND \_ Zero und den Ziel-Blend-Zustand auf D3DBLEND \_ srccolor festlegen.</span><span class="sxs-lookup"><span data-stu-id="1ddc9-120">You can achieve color light mapping by setting the source alpha blending state to D3DBLEND\_ZERO and the destination blend state to D3DBLEND\_SRCCOLOR.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ddc9-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1ddc9-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ddc9-122">Rendering-Zustände</span><span class="sxs-lookup"><span data-stu-id="1ddc9-122">Render States</span></span>](render-states.md)
</dt> </dl>

 

 
