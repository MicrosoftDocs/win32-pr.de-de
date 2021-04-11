---
description: 'Zum Rendern von Scheitelpunkt Daten aus einem Vertex-Puffer sind einige Schritte erforderlich. Zuerst müssen Sie die Streamquelle festlegen, indem Sie die IDirect3DDevice9:: SetStreamSource-Methode aufrufen, wie im folgenden Beispiel gezeigt.'
ms.assetid: a0435a3d-e1dd-4365-904d-8e5713e379ce
title: Rendering von einem Scheitelpunkt Puffer (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cebb68c5395a827a9aee4ea1f8465257c436bb7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123428"
---
# <a name="rendering-from-a-vertex-buffer-direct3d-9"></a><span data-ttu-id="57e23-104">Rendering von einem Scheitelpunkt Puffer (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="57e23-104">Rendering from a Vertex Buffer (Direct3D 9)</span></span>

<span data-ttu-id="57e23-105">Zum Rendern von Scheitelpunkt Daten aus einem Vertex-Puffer sind einige Schritte erforderlich.</span><span class="sxs-lookup"><span data-stu-id="57e23-105">Rendering vertex data from a vertex buffer requires a few steps.</span></span> <span data-ttu-id="57e23-106">Zuerst müssen Sie die Streamquelle festlegen, indem Sie die [**IDirect3DDevice9:: SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) -Methode aufrufen, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="57e23-106">First, you need to set the stream source by calling the [**IDirect3DDevice9::SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) method, as shown in the following example.</span></span>


```
d3dDevice->SetStreamSource( 0, g_pVB, 0, sizeof(CUSTOMVERTEX) );
```



<span data-ttu-id="57e23-107">Der erste Parameter von [**IDirect3DDevice9:: SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) teilt Direct3D die Quelle des Datenstroms des Geräts.</span><span class="sxs-lookup"><span data-stu-id="57e23-107">The first parameter of [**IDirect3DDevice9::SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) tells Direct3D the source of the device data stream.</span></span> <span data-ttu-id="57e23-108">Der zweite Parameter ist der Vertex-Puffer, der an den Datenstream gebunden werden soll.</span><span class="sxs-lookup"><span data-stu-id="57e23-108">The second parameter is the vertex buffer to bind to the data stream.</span></span> <span data-ttu-id="57e23-109">Der dritte Parameter ist der Offset vom Anfang des Streams bis zum Anfang der Scheitelpunkt Daten (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="57e23-109">The third parameter is the offset from the beginning of the stream to the beginning of the vertex data, in bytes.</span></span> <span data-ttu-id="57e23-110">Der vierte Parameter ist der Schritt der Komponente (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="57e23-110">The fourth parameter is the stride of the component, in bytes.</span></span> <span data-ttu-id="57e23-111">Im obigen Beispielcode wird die Größe eines CustomVertex für den Schritt der Komponente verwendet.</span><span class="sxs-lookup"><span data-stu-id="57e23-111">In the sample code above, the size of a CUSTOMVERTEX is used for the stride of the component.</span></span>

<span data-ttu-id="57e23-112">Der nächste Schritt besteht darin, den zu verwendenden Vertex-Shader zu informieren Direct3D indem Sie die [**IDirect3DDevice9:: setvertexshader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="57e23-112">The next step is to inform Direct3D which vertex shader to use by calling the [**IDirect3DDevice9::SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) method.</span></span> <span data-ttu-id="57e23-113">Der folgende Beispielcode legt einen f-Code für den Vertex-Shader fest.</span><span class="sxs-lookup"><span data-stu-id="57e23-113">The following sample code sets an FVF code for the vertex shader.</span></span> <span data-ttu-id="57e23-114">Dies informiert Direct3D über die Typen der Scheitel Punkte, mit denen es umzugehen ist.</span><span class="sxs-lookup"><span data-stu-id="57e23-114">This informs Direct3D of the types of vertices it is dealing with.</span></span>


```
d3dDevice->SetFVF( D3DFVF_CUSTOMVERTEX );
```



<span data-ttu-id="57e23-115">Nachdem Sie die Streamquelle und den Vertexshader festgelegt haben, verwenden alle Draw-Methoden den Vertex-Puffer.</span><span class="sxs-lookup"><span data-stu-id="57e23-115">After setting the stream source and vertex shader, any draw methods will use the vertex buffer.</span></span> <span data-ttu-id="57e23-116">Im folgenden Codebeispiel wird gezeigt, wie Vertices aus einem Vertex-Puffer mit der [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) -Methode gerwiert werden.</span><span class="sxs-lookup"><span data-stu-id="57e23-116">The code example below shows how to render vertices from a vertex buffer with the [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) method.</span></span>


```
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, 1 );
```



<span data-ttu-id="57e23-117">Der zweite Parameter, den [**IDirect3DDevice9::D rawprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) akzeptiert, ist der Index des ersten Vektors im Vertex-Puffer, der geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="57e23-117">The second parameter that [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) accepts is the index of the first vector in the vertex buffer to load.</span></span>

## <a name="related-topics"></a><span data-ttu-id="57e23-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="57e23-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57e23-119">Vertex-Puffer</span><span class="sxs-lookup"><span data-stu-id="57e23-119">Vertex Buffers</span></span>](vertex-buffers.md)
</dt> <dt>

[<span data-ttu-id="57e23-120">Rendering aus Scheitelpunkt-und Index Puffer (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="57e23-120">Rendering from Vertex and Index Buffers (Direct3D 9)</span></span>](rendering-from-vertex-and-index-buffers.md)
</dt> </dl>

 

 
