---
description: Die tiefen Pufferung ist eine Methode zum Entfernen ausgeblendeter Linien und Oberflächen. Standardmäßig verwendet Direct3D keine tiefen Pufferung.
ms.assetid: 03795e4e-1daa-48e3-8724-8dd4b5187edc
title: Status der tiefen Pufferung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e632d3dfe6eebd54970c59ef6a666cfcb0950fcb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481555"
---
# <a name="depth-buffering-state-direct3d-9"></a><span data-ttu-id="fc611-104">Status der tiefen Pufferung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="fc611-104">Depth Buffering State (Direct3D 9)</span></span>

<span data-ttu-id="fc611-105">Die tiefen Pufferung ist eine Methode zum Entfernen ausgeblendeter Linien und Oberflächen.</span><span class="sxs-lookup"><span data-stu-id="fc611-105">Depth buffering is a method of removing hidden lines and surfaces.</span></span> <span data-ttu-id="fc611-106">Standardmäßig verwendet Direct3D keine tiefen Pufferung.</span><span class="sxs-lookup"><span data-stu-id="fc611-106">By default, Direct3D does not use depth buffering.</span></span>

<span data-ttu-id="fc611-107">Eine konzeptionelle Übersicht über tiefen Puffer finden Sie unter [tiefen Puffer (Direct3D 9)](depth-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="fc611-107">For a conceptual overview of depth buffers, see [Depth Buffers (Direct3D 9)](depth-buffers.md).</span></span>

<span data-ttu-id="fc611-108">C++-Anwendungen aktualisieren den tiefen Puffer Zustand mit dem D3DRS \_ zenable-renderzustand, wobei ein Member der [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) -Enumeration verwendet wird, um den neuen Zustandswert anzugeben.</span><span class="sxs-lookup"><span data-stu-id="fc611-108">C++ applications update the depth-buffering state with the D3DRS\_ZENABLE render state, using a member of the [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) enumeration to specify the new state value.</span></span>

<span data-ttu-id="fc611-109">Wenn Ihre Anwendung verhindern soll, dass Direct3D in den tiefen Puffer schreibt, kann Sie den D3DRS \_ zwriteenable-Enumerationswert verwenden, wobei D3DZB \_ false als zweiter Parameter für den Aufrufen von [**IDirect3DDevice9:: setrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fc611-109">If your application needs to prevent Direct3D from writing to the depth buffer, it can use the D3DRS\_ZWRITEENABLE enumerated value, specifying D3DZB\_FALSE as the second parameter for the call to [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).</span></span>

<span data-ttu-id="fc611-110">Im folgenden Codebeispiel wird gezeigt, wie der tiefen Puffer Zustand festgelegt wird, um z-Pufferung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="fc611-110">The following code example shows how the depth-buffer state is set to enable z-buffering.</span></span>


```
// This code example assumes that d3dDevice is a 
// valid pointer to an IDirect3DDevice9 interface.
// Enable z-buffering.
d3dDevice->SetRenderState(D3DRS_ZENABLE, D3DZB_TRUE);
```



<span data-ttu-id="fc611-111">Die Anwendung kann auch den D3DRS \_ zfunc-renderzustand verwenden, um die Vergleichsfunktion zu steuern, die Direct3D beim Durchführen von tiefen Pufferungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="fc611-111">Your application can also use the D3DRS\_ZFUNC render state to control the comparison function that Direct3D uses when performing depth buffering.</span></span>

<span data-ttu-id="fc611-112">Z-Biasing ist eine Methode, eine Oberfläche vor einer anderen anzuzeigen, auch wenn deren tiefen Werte identisch sind.</span><span class="sxs-lookup"><span data-stu-id="fc611-112">Z-biasing is a method of displaying one surface in front of another, even if their depth values are the same.</span></span> <span data-ttu-id="fc611-113">Diese Technik kann für eine Vielzahl von Effekten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fc611-113">You can use this technique for a variety of effects.</span></span> <span data-ttu-id="fc611-114">Ein gängiges Beispiel ist das Rendern von Schatten auf Wänden.</span><span class="sxs-lookup"><span data-stu-id="fc611-114">A common example is rendering shadows on walls.</span></span> <span data-ttu-id="fc611-115">Der Schatten und die Wand haben denselben tiefen Wert.</span><span class="sxs-lookup"><span data-stu-id="fc611-115">Both the shadow and the wall have the same depth value.</span></span> <span data-ttu-id="fc611-116">Sie möchten jedoch, dass Ihre Anwendung den Schatten auf der Wand anzeigt.</span><span class="sxs-lookup"><span data-stu-id="fc611-116">However, you want your application to show the shadow on the wall.</span></span> <span data-ttu-id="fc611-117">Durch die Angabe eines z-Bias zum Schatten macht Direct3D diese korrekt anzeigen (siehe D3DRS \_ depthbias).</span><span class="sxs-lookup"><span data-stu-id="fc611-117">Giving a z-bias to the shadow makes Direct3D display them properly (see D3DRS\_DEPTHBIAS).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc611-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fc611-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc611-119">Rendering-Zustände</span><span class="sxs-lookup"><span data-stu-id="fc611-119">Render States</span></span>](render-states.md)
</dt> </dl>

 

 
