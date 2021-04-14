---
description: Durch Nebeleffekte kann eine 3D-Szene mehr realistisch sein.
ms.assetid: 26fe4f7c-7bb3-4a52-b539-5de2b11256e9
title: Nebelzustand (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d3103cbbd3dfb220e2ddd75078040702fd7557
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392331"
---
# <a name="fog-state-direct3d-9"></a><span data-ttu-id="a6c02-103">Nebelzustand (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a6c02-103">Fog State (Direct3D 9)</span></span>

<span data-ttu-id="a6c02-104">Durch Nebeleffekte kann eine 3D-Szene mehr realistisch sein.</span><span class="sxs-lookup"><span data-stu-id="a6c02-104">Fog effects can give a 3D scene greater realism.</span></span> <span data-ttu-id="a6c02-105">Sie können Nebeleffekte zum Simulieren von Nebel verwenden.</span><span class="sxs-lookup"><span data-stu-id="a6c02-105">You can use fog effects for more than simulating fog.</span></span> <span data-ttu-id="a6c02-106">Sie können auch die Klarheit einer Szene mit Distanz verringern.</span><span class="sxs-lookup"><span data-stu-id="a6c02-106">They can also decrease the clarity of a scene with distance.</span></span> <span data-ttu-id="a6c02-107">Dies spiegelt, was in der realen Welt passiert. Wenn Objekte vom Benutzer entfernter werden, sind die Details weniger unterschiedlich.</span><span class="sxs-lookup"><span data-stu-id="a6c02-107">This mirrors what happens in the real world; as objects become more distant from the user, their detail is less distinct.</span></span>

<span data-ttu-id="a6c02-108">Weitere Informationen zur Verwendung von Nebel in der Anwendung finden Sie unter [Nebel (Direct3D 9)](fog.md).</span><span class="sxs-lookup"><span data-stu-id="a6c02-108">For more information about using fog in your application, see [Fog (Direct3D 9)](fog.md).</span></span>

<span data-ttu-id="a6c02-109">Eine C++-Anwendung steuert den Nebel durch Renderingzustände des Geräts.</span><span class="sxs-lookup"><span data-stu-id="a6c02-109">A C++ application controls fog through device rendering states.</span></span> <span data-ttu-id="a6c02-110">Der [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) -Enumerationstyp enthält Zustände, mit denen gesteuert werden kann, ob Pixel (Tabelle) oder Scheitelpunkt Nebel verwendet wird, welche Farbe es ist, welche Farbe das System anwendet und welche Parameter der Formel verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a6c02-110">The [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) enumerated type includes states to control whether pixel (table) or vertex fog is used, what color it is, the fog formula the system applies, and the parameters of the formula.</span></span>

<span data-ttu-id="a6c02-111">Sie aktivieren den Nebel, indem Sie den D3DRS \_ fogenable-Rendering-Zustand auf " **true**" festlegen.</span><span class="sxs-lookup"><span data-stu-id="a6c02-111">You enable fog by setting the D3DRS\_FOGENABLE render state to **TRUE**.</span></span> <span data-ttu-id="a6c02-112">Die Schnebel Farbe kann auf einen beliebigen Farbwert festgelegt werden, indem der D3DRS \_ fogcolor-Rendering-Zustand verwendet wird. die Alpha Komponente der Nebelfarbe wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a6c02-112">The fog color can be set to any color value by using the D3DRS\_FOGCOLOR render state; the alpha component of the fog color is ignored.</span></span>

<span data-ttu-id="a6c02-113">Die \_ renderzustände D3DRS fogtablemode und D3DRS \_ fogvertexmode steuern die auf Nebel Berechnungen angewendete Nebel Formel und Steuern indirekt, welcher Typ von Nebel angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="a6c02-113">The D3DRS\_FOGTABLEMODE and D3DRS\_FOGVERTEXMODE render states control the fog formula applied for fog calculations, and they indirectly control which type of fog is applied.</span></span> <span data-ttu-id="a6c02-114">Beide Rendering-Zustände können auf einen Member des [**D3DFOGMODE**](./d3dfogmode.md) -enumerierten Typs festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a6c02-114">Both render states can be set to a member of the [**D3DFOGMODE**](./d3dfogmode.md) enumerated type.</span></span> <span data-ttu-id="a6c02-115">Wenn Sie den renderzustand auf D3DFOG \_ None festlegen, wird der Pixel-bzw. Scheitelpunkt Nebel deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="a6c02-115">Setting either render state to D3DFOG\_NONE disables pixel or vertex fog, respectively.</span></span> <span data-ttu-id="a6c02-116">Wenn beide renderzustände auf gültige Modi festgelegt sind, wendet das System nur Pixel Nebeleffekte an.</span><span class="sxs-lookup"><span data-stu-id="a6c02-116">If both render states are set to valid modes, the system applies only pixel fog effects.</span></span>

<span data-ttu-id="a6c02-117">Mit den \_ Renderingzuständen D3DRS fogstart und D3DRS \_ fogend werden die Nebel Formel Parameter für den D3DFOG \_ Linear-Modus gesteuert.</span><span class="sxs-lookup"><span data-stu-id="a6c02-117">The D3DRS\_FOGSTART and D3DRS\_FOGEND render states control fog formula parameters for the D3DFOG\_LINEAR mode.</span></span> <span data-ttu-id="a6c02-118">Der D3DRS \_ fogdensity-renderzustand steuert die Nebeldichte in den exponentialnebelmodi.</span><span class="sxs-lookup"><span data-stu-id="a6c02-118">The D3DRS\_FOGDENSITY render state controls fog density in the exponential fog modes.</span></span>

<span data-ttu-id="a6c02-119">Weitere Informationen finden Sie unter " [Fog Parameters" (Direct3D 9)](fog-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a6c02-119">For more information, see [Fog Parameters (Direct3D 9)](fog-parameters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a6c02-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a6c02-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6c02-121">Rendering-Zustände</span><span class="sxs-lookup"><span data-stu-id="a6c02-121">Render States</span></span>](render-states.md)
</dt> </dl>

 

 
