---
description: 'Die IDirect3DDevice9:: SetStreamSource-Methode bindet einen Scheitelpunkt Puffer an einen Gerätedaten Strom, wobei eine Zuordnung zwischen den Scheitelpunkt Daten und einem von mehreren datenstreamports erstellt wird, die die primitiven Verarbeitungsfunktionen übertragen.'
ms.assetid: ef317537-3095-435d-b0f2-83cb3b385da2
title: Festlegen der Streamquelle (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76d0c296b79d258be6eee2d683979081673d5d04
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521912"
---
# <a name="setting-the-stream-source-direct3d-9"></a><span data-ttu-id="7fc63-103">Festlegen der Streamquelle (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7fc63-103">Setting the Stream Source (Direct3D 9)</span></span>

<span data-ttu-id="7fc63-104">Die [**IDirect3DDevice9:: SetStreamSource**](/windows/desktop/api) -Methode bindet einen Scheitelpunkt Puffer an einen Gerätedaten Strom, wobei eine Zuordnung zwischen den Scheitelpunkt Daten und einem von mehreren datenstreamports erstellt wird, die die primitiven Verarbeitungsfunktionen übertragen.</span><span class="sxs-lookup"><span data-stu-id="7fc63-104">The [**IDirect3DDevice9::SetStreamSource**](/windows/desktop/api) method binds a vertex buffer to a device data stream, creating an association between the vertex data and one of several data stream ports that feed the primitive processing functions.</span></span> <span data-ttu-id="7fc63-105">Die tatsächlichen Verweise auf die Streamdaten treten erst auf, wenn eine Zeichnungs Methode, z. b. [**IDirect3DDevice9::D rawprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="7fc63-105">The actual references to the stream data do not occur until a drawing method, such as [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), is called.</span></span>

<span data-ttu-id="7fc63-106">Ein Datenstrom ist als einheitliches Array von Komponenten Daten definiert, wobei jede Komponente aus mindestens einem Element besteht, das eine einzelne Entität, z. b. Position, normal, Farbe usw., darstellt.</span><span class="sxs-lookup"><span data-stu-id="7fc63-106">A stream is defined as a uniform array of component data, where each component consists of one or more elements representing a single entity such as position, normal, color, and so on.</span></span> <span data-ttu-id="7fc63-107">Der Stride-Parameter gibt die Größe der Komponente in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="7fc63-107">The Stride parameter specifies the size of the component, in bytes.</span></span>

<span data-ttu-id="7fc63-108">Der folgende Code veranschaulicht das Festlegen der Streamquelle und das Zeichnen Ihres Inhalts.</span><span class="sxs-lookup"><span data-stu-id="7fc63-108">The following code demonstrates setting the stream source and drawing its contents.</span></span> <span data-ttu-id="7fc63-109">Die Variable "g \_ PVB" ist eine LPDIRECT3DVERTEXBUFFER9, die Scheitelpunkt Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="7fc63-109">The g\_pVB variable is a LPDIRECT3DVERTEXBUFFER9 that contains vertex data.</span></span>


```
if( SUCCEEDED( g_pd3dDevice->BeginScene() ) )
{
    // Setup the world, view, and projection matrices
    SetupMatrices();

    // Render the vertex buffer contents
    g_pd3dDevice->SetStreamSource( 0, g_pVB, 0, sizeof(CUSTOMVERTEX) );
    g_pd3dDevice->SetFVF( D3DFVF_CUSTOMVERTEX );
    g_pd3dDevice->DrawPrimitive( D3DPT_TRIANGLESTRIP, 0, 1 );

    // End the scene
    g_pd3dDevice->EndScene();
}
```



<span data-ttu-id="7fc63-110">Weitere Informationen zu diesem Code finden Sie im folgenden Tutorial: [Tutorial 3: Verwenden von Matrizen](https://msdn.microsoft.com/library/Ee418892(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="7fc63-110">For more information about this code see the following tutorial: [Tutorial 3: Using Matrices](https://msdn.microsoft.com/library/Ee418892(v=VS.85).aspx)</span></span>

## <a name="related-topics"></a><span data-ttu-id="7fc63-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7fc63-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7fc63-112">Rendern von primitiven</span><span class="sxs-lookup"><span data-stu-id="7fc63-112">Rendering Primitives</span></span>](rendering-primitives.md)
</dt> </dl>

 

 
