---
description: Polygone, die in Ihrem 3D-Raum Coplanar sind, können so gestaltet werden, als wären Sie nicht durch Hinzufügen eines z-Bias zu jedem.
ms.assetid: 0ab4f63b-49de-4bd0-a10f-6f90b9706c58
title: Tiefen Abweichung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ce605ea1df161e5ebfed95c214c3dd180ab7ee6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481563"
---
# <a name="depth-bias-direct3d-9"></a><span data-ttu-id="f87bc-103">Tiefen Abweichung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f87bc-103">Depth Bias (Direct3D 9)</span></span>

<span data-ttu-id="f87bc-104">Polygone, die in Ihrem 3D-Raum Coplanar sind, können so gestaltet werden, als wären Sie nicht durch Hinzufügen eines z-Bias zu jedem.</span><span class="sxs-lookup"><span data-stu-id="f87bc-104">Polygons that are coplanar in your 3D space can be made to appear as if they are not coplanar by adding a z-bias to each one.</span></span> <span data-ttu-id="f87bc-105">Dies ist eine Technik, die häufig verwendet wird, um sicherzustellen, dass Schatten in einer Szene ordnungsgemäß angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f87bc-105">This is a technique commonly used to ensure that shadows in a scene are displayed properly.</span></span> <span data-ttu-id="f87bc-106">Beispielsweise hat ein Schatten auf einer Wand wahrscheinlich denselben tiefen Wert wie die Wand.</span><span class="sxs-lookup"><span data-stu-id="f87bc-106">For instance, a shadow on a wall will likely have the same depth value as the wall does.</span></span> <span data-ttu-id="f87bc-107">Wenn Sie die Wand zuerst und dann den Schatten darstellen, ist der Schatten möglicherweise nicht sichtbar, oder es sind keine tiefen Artefakte sichtbar.</span><span class="sxs-lookup"><span data-stu-id="f87bc-107">If you render the wall first and then the shadow, the shadow might not be visible, or depth artifacts might be visible.</span></span> <span data-ttu-id="f87bc-108">Sie können die Reihenfolge, in der Sie die Coplanar-Objekte renden, umkehren, um den Effekt umzukehren, aber tiefe Artefakte sind immer noch wahrscheinlich.</span><span class="sxs-lookup"><span data-stu-id="f87bc-108">You can reverse the order in which you render the coplanar objects in hopes of reversing the effect, but depth artifacts are still likely.</span></span>

<span data-ttu-id="f87bc-109">Eine Anwendung kann sicherstellen, dass Coplanar-Polygone ordnungsgemäß gerendert werden, indem Sie den z-Werten, die das System beim Rendern der Mengen von Coplanar-Polygonen verwendet, einen Bias hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f87bc-109">An application can help ensure that coplanar polygons are rendered properly by adding a bias to the z-values that the system uses when rendering the sets of coplanar polygons.</span></span> <span data-ttu-id="f87bc-110">Zum Hinzufügen eines z-Bias zu einem Satz von Polygonen Aufrufen der [**IDirect3DDevice9:: btrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) -Methode direkt vor dem Rendern, Festlegen des *State* -Parameters auf D3DRS \_ depthbias und des *value* -Parameters auf einen passenden float-Wert (z. b. kann ein geeigneter Wert von-1,0 bis 1,0 sein). um diesen Wert an "\* **Trend User State**" zu übergeben, müssen Sie auch den Wert in ein **DWORD** umwandeln</span><span class="sxs-lookup"><span data-stu-id="f87bc-110">To add a z-bias to a set of polygons, call the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method just before rendering them, setting the *State* parameter to D3DRS\_DEPTHBIAS, and the *Value* parameter to a suitable float value (for example, a suitable value might be from -1.0 to 1.0); to pass this value to **SetRenderState**, you must also cast the value to a **DWORD**.</span></span> <span data-ttu-id="f87bc-111">Ein höherer z-Bias-Wert erhöht die Wahrscheinlichkeit, dass die von Ihnen dargestellten Polygone sichtbar sind, wenn Sie mit anderen Coplanar-Polygonen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f87bc-111">A higher z-bias value increases the likelihood that the polygons you render will be visible when displayed with other coplanar polygons.</span></span>


```
Offset = m * D3DRS_SLOPESCALEDEPTHBIAS + D3DRS_DEPTHBIAS
```



<span data-ttu-id="f87bc-112">wobei m der maximale tiefen Rand des gerenderten Dreiecks ist.</span><span class="sxs-lookup"><span data-stu-id="f87bc-112">where m is the maximum depth slope of the triangle being rendered.</span></span>


```
m = max(abs(delta z / delta x), abs(delta z / delta y)) 
```



<span data-ttu-id="f87bc-113">Die Einheiten für die \_ Rendering-Zustände D3DRS depthbias und D3DRS \_ slopescaledepthbias sind davon abhängig, ob z-Pufferung oder w-Pufferung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="f87bc-113">The units for the D3DRS\_DEPTHBIAS and D3DRS\_SLOPESCALEDEPTHBIAS render states depend on whether z-buffering or w-buffering is enabled.</span></span> <span data-ttu-id="f87bc-114">Die Anwendung muss geeignete Werte bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="f87bc-114">The application must provide suitable values.</span></span>

<span data-ttu-id="f87bc-115">Der Bias wird nicht auf Zeilen-und Punkt primitive angewendet.</span><span class="sxs-lookup"><span data-stu-id="f87bc-115">The bias is not applied to any line and point primitive.</span></span> <span data-ttu-id="f87bc-116">Dieser Bias muss jedoch auf Dreiecke angewendet werden, die im Draht Modell-Modus gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="f87bc-116">However, this bias needs to be applied to triangles drawn in wireframe mode.</span></span>


```
// RenderStates
D3DRS_SLOPESCALEDEPTHBIAS, // Defaults to zero
D3DRS_DEPTHBIAS,           // Defaults to zero
```




```
// Caps
D3DPRASTERCAPS_DEPTHBIAS           
D3DPRASTERCAPS_SLOPESCALEDEPTHBIAS 
```



## <a name="related-topics"></a><span data-ttu-id="f87bc-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f87bc-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f87bc-118">Pixel Pipeline</span><span class="sxs-lookup"><span data-stu-id="f87bc-118">Pixel Pipeline</span></span>](pixel-pipeline.md)
</dt> </dl>

 

 
