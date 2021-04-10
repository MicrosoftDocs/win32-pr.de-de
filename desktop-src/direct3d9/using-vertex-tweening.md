---
description: Um zu ermitteln, ob Direct3D die vertextwiening unterstützt, überprüfen Sie das D3DVTXPCAPS \_ Tweening-Flag im VertexProcessingCaps-Member der D3DCAPS9-Struktur.
ms.assetid: b60c7f96-3752-4703-9059-486d9906c508
title: Verwenden von Vertex-Tweening (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12ca56cc521b5bff01a5d6af5c2d4ab6b02cd49e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860191"
---
# <a name="using-vertex-tweening-direct3d-9"></a><span data-ttu-id="92cf8-103">Verwenden von Vertex-Tweening (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="92cf8-103">Using Vertex Tweening (Direct3D 9)</span></span>

<span data-ttu-id="92cf8-104">Um zu ermitteln, ob Direct3D die vertextwiening unterstützt, überprüfen Sie das D3DVTXPCAPS \_ Tweening-Flag im VertexProcessingCaps-Member der [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="92cf8-104">To determine if Direct3D supports vertex tweening, check for the D3DVTXPCAPS\_TWEENING flag in the VertexProcessingCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure.</span></span> <span data-ttu-id="92cf8-105">Im folgenden Codebeispiel wird die [**IDirect3DDevice9:: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) -Methode verwendet, um zu bestimmen, ob das twiening unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="92cf8-105">The following code example uses the [**IDirect3DDevice9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) method to determine if tweening is supported.</span></span>


```
// This example assumes that m_pD3DDevice is 
// a valid pointer to a IDirect3DDevice9 interface.
//
D3DCAPS9 d3dCaps;

m_pD3DDevice->GetDeviceCaps( &d3dCaps );
if( 0 != (d3dCaps.VertexProcessingCaps & D3DVTXPCAPS_TWEENING) )
    // Vertex tweening is supported.
```



<span data-ttu-id="92cf8-106">Um Vector Tweening verwenden zu können, müssen Sie zuerst einen benutzerdefinierten vertextyp einrichten, der eine zweite normale oder eine zweite Position verwendet.</span><span class="sxs-lookup"><span data-stu-id="92cf8-106">To use vector tweening, you must first set up a custom vertex type that uses a second normal or a second position.</span></span> <span data-ttu-id="92cf8-107">Das folgende Codebeispiel zeigt eine Beispiel Deklaration, die einen zweiten Punkt und eine zweite Position enthält.</span><span class="sxs-lookup"><span data-stu-id="92cf8-107">The following code example shows a sample declaration that includes both a second point and a second position.</span></span>


```
struct TEX_VERTEX
{
    D3DVECTOR position;
    D3DVECTOR normal;
    D3DVECTOR position2;
    D3DVECTOR normal2;
};

//Create a vertex buffer with the type TEX_VERTEX.
```



<span data-ttu-id="92cf8-108">Der nächste Schritt besteht darin, die aktuelle Deklaration festzulegen.</span><span class="sxs-lookup"><span data-stu-id="92cf8-108">The next step is to set the current declaration.</span></span> <span data-ttu-id="92cf8-109">Das folgende Codebeispiel zeigt, wie Sie dies tun.</span><span class="sxs-lookup"><span data-stu-id="92cf8-109">The code example below shows how to do this.</span></span>


```
// Create the shader declaration.
D3DVERTEXELEMENT9 decl[] = 
{
    { 0, 0,  D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0 },
    { 0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL, 0 },
    { 0, 24, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 1 },
    { 0, 36, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL, 1 },
    D3DDECL_END()
};
```



<span data-ttu-id="92cf8-110">Weitere Informationen zum Erstellen eines benutzerdefinierten Scheitelpunkt Typs und eines Scheitelpunkt Puffers finden Sie unter [Erstellen eines Scheitelpunkt Puffers (Direct3D 9)](creating-a-vertex-buffer.md).</span><span class="sxs-lookup"><span data-stu-id="92cf8-110">For more information about creating a custom vertex type and a vertex buffer, see [Creating a Vertex Buffer (Direct3D 9)](creating-a-vertex-buffer.md).</span></span>

> [!Note]  
> <span data-ttu-id="92cf8-111">Wenn die Vertex-Tweening aktiviert ist, muss in der aktuellen Deklaration eine zweite Position oder eine zweite normale Position vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="92cf8-111">When vertex tweening is enabled, a second position or a second normal must be present in the current declaration.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="92cf8-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="92cf8-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92cf8-113">Vertex-Tweening</span><span class="sxs-lookup"><span data-stu-id="92cf8-113">Vertex Tweening</span></span>](vertex-tweening.md)
</dt> </dl>

 

 
