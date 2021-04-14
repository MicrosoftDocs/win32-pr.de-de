---
description: Ihre Anwendung bearbeitet Ressourcen, um eine Szene zu Rendering.
ms.assetid: 4f0eea7d-b1e4-4d53-a136-f40df7a0fbb1
title: Bearbeiten von Ressourcen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 886dfee3af024d103dab8666687f1b053a5fb46a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392329"
---
# <a name="manipulating-resources-direct3d-9"></a><span data-ttu-id="4670a-103">Bearbeiten von Ressourcen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="4670a-103">Manipulating Resources (Direct3D 9)</span></span>

<span data-ttu-id="4670a-104">Ihre Anwendung bearbeitet Ressourcen, um eine Szene zu Rendering.</span><span class="sxs-lookup"><span data-stu-id="4670a-104">Your application manipulates resources in order to render a scene.</span></span> <span data-ttu-id="4670a-105">Zuerst muss eine Anwendung eine Textur Ressource mit einer der folgenden Methoden erstellen:</span><span class="sxs-lookup"><span data-stu-id="4670a-105">First, an application needs to create a texture resource with one of the following methods:</span></span>

-   [<span data-ttu-id="4670a-106">**IDirect3DDevice9:: kreatecubetexture**</span><span class="sxs-lookup"><span data-stu-id="4670a-106">**IDirect3DDevice9::CreateCubeTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture)
-   [<span data-ttu-id="4670a-107">**IDirect3DDevice9:: kreatetexture**</span><span class="sxs-lookup"><span data-stu-id="4670a-107">**IDirect3DDevice9::CreateTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)
-   [<span data-ttu-id="4670a-108">**IDirect3DDevice9:: kreatevolumetexture**</span><span class="sxs-lookup"><span data-stu-id="4670a-108">**IDirect3DDevice9::CreateVolumeTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture)

<span data-ttu-id="4670a-109">Eine Textur Ressource kann stattdessen mit einer der D3DXCreatexxx Texturing-Funktionen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="4670a-109">A texture resource can instead be created with one of the D3DXCreatexxx texturing functions.</span></span>

<span data-ttu-id="4670a-110">Die Textur Objekte, die von den Textur Erstellungs Methoden zurückgegeben werden, sind Container für Oberflächen oder Volumes. Diese Container werden generisch als Puffer bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="4670a-110">The texture objects returned by the texture creation methods are containers for surfaces or volumes; these containers are generically known as buffers.</span></span> <span data-ttu-id="4670a-111">Die Puffer, die sich im Besitz der Ressource befinden, erben die Verwendungen, das Format und den Pool der Ressource, haben aber ihren eigenen Typ.</span><span class="sxs-lookup"><span data-stu-id="4670a-111">The buffers owned by the resource inherit the usages, format, and pool of the resource but have their own type.</span></span> <span data-ttu-id="4670a-112">Weitere Informationen finden Sie unter [Ressourcen Eigenschaften (Direct3D 9)](resource-properties.md).</span><span class="sxs-lookup"><span data-stu-id="4670a-112">For more information, see [Resource Properties (Direct3D 9)](resource-properties.md).</span></span>

<span data-ttu-id="4670a-113">Die Anwendung erhält Zugriff auf die enthaltenen Oberflächen zum Zweck des Ladens von Grafiken durch Aufrufen der folgenden Methoden.</span><span class="sxs-lookup"><span data-stu-id="4670a-113">The application gains access to the contained surfaces, for the purpose of loading artwork, by calling the following methods.</span></span> <span data-ttu-id="4670a-114">Weitere Informationen finden Sie unter [Sperren von Ressourcen (Direct3D 9)](locking-resources.md).</span><span class="sxs-lookup"><span data-stu-id="4670a-114">For details, see [Locking Resources (Direct3D 9)](locking-resources.md).</span></span>

-   [<span data-ttu-id="4670a-115">**IDirect3DCubeTexture9:: lockrect**</span><span class="sxs-lookup"><span data-stu-id="4670a-115">**IDirect3DCubeTexture9::LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
-   [<span data-ttu-id="4670a-116">**IDirect3DTexture9:: lockrect**</span><span class="sxs-lookup"><span data-stu-id="4670a-116">**IDirect3DTexture9::LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-lockrect)
-   [<span data-ttu-id="4670a-117">**IDirect3DVolumeTexture9:: Lockbox**</span><span class="sxs-lookup"><span data-stu-id="4670a-117">**IDirect3DVolumeTexture9::LockBox**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-lockbox)

<span data-ttu-id="4670a-118">Die Lock-Methoden verwenden Argumente, die die enthaltene Oberfläche anzeigen, z. b. die MipMap-Unterebene oder die cubeseite der Textur und geben Zeiger auf die Pixel zurück.</span><span class="sxs-lookup"><span data-stu-id="4670a-118">The lock methods take arguments denoting the contained surface - for example, the mipmap sub-level or cube face of the texture - and return pointers to the pixels.</span></span> <span data-ttu-id="4670a-119">Die typische Anwendung verwendet niemals direkt ein Surface-Objekt.</span><span class="sxs-lookup"><span data-stu-id="4670a-119">The typical application never uses a surface object directly.</span></span>

<span data-ttu-id="4670a-120">Erstellen Sie Geometrie orientierte Ressourcen durch Aufrufen von [**IDirect3DDevice9:: createindexbuffer**](/windows/desktop/api) oder [**IDirect3DDevice9:: createvertexbuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer).</span><span class="sxs-lookup"><span data-stu-id="4670a-120">Create geometry-oriented resources by calling [**IDirect3DDevice9::CreateIndexBuffer**](/windows/desktop/api) or [**IDirect3DDevice9::CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer).</span></span>

<span data-ttu-id="4670a-121">Sperren und füllen Sie die Puffer Ressourcen, indem Sie entweder [**IDirect3DIndexBuffer9:: Lock**](/windows/desktop/api) oder [**IDirect3DVertexBuffer9:: Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock)aufrufen, abhängig von der Ressource.</span><span class="sxs-lookup"><span data-stu-id="4670a-121">Lock and fill the buffer resources by calling either [**IDirect3DIndexBuffer9::Lock**](/windows/desktop/api) or [**IDirect3DVertexBuffer9::Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock), depending upon the resource.</span></span>

<span data-ttu-id="4670a-122">Bei verwalteten Textur Ressourcen wird der Prozess der Ressourcen Erstellung hier beendet.</span><span class="sxs-lookup"><span data-stu-id="4670a-122">For managed texture resources, the resource creation process ends here.</span></span> <span data-ttu-id="4670a-123">Bei nicht verwalteten Textur Ressourcen stuft eine Anwendung Systemspeicher Ressourcen auf Geräte zugängliche Ressourcen (für die Hardwarebeschleunigung) durch Aufrufen von [**IDirect3DDevice9:: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture)herauf.</span><span class="sxs-lookup"><span data-stu-id="4670a-123">For non-managed texture resources, an application promotes system memory resources to device-accessible resources (for hardware acceleration) by calling [**IDirect3DDevice9::UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture).</span></span>

<span data-ttu-id="4670a-124">Zum Darstellen von Bildern, die aus Ressourcen gerendert werden, benötigt die Anwendung auch Farb-und tiefen Schablonen Puffer.</span><span class="sxs-lookup"><span data-stu-id="4670a-124">To present images rendered from resources, the application also needs color and depth-stencil buffers.</span></span> <span data-ttu-id="4670a-125">Bei typischen Anwendungen gehört der Farb Puffer der Swapkette des Geräts an, bei der es sich um eine Sammlung von backpufferoberflächen handelt, die implizit mit dem Gerät erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="4670a-125">For typical applications, the color buffer is owned by the device's swap chain, which is a collection of back-buffer surfaces, and is implicitly created with the device.</span></span> <span data-ttu-id="4670a-126">Tiefen Schablone können mithilfe der [**IDirect3DDevice9:: foatedepthstencilsurface**](/windows/desktop/api) -Methode implizit erstellt oder explizit erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="4670a-126">Depth-stencil surfaces can be implicitly created, or explicitly created by using the [**IDirect3DDevice9::CreateDepthStencilSurface**](/windows/desktop/api) method.</span></span> <span data-ttu-id="4670a-127">Die Anwendung ordnet ein Gerät und seine tiefe und ihren Farb Puffer einem [**IDirect3DDevice9:: SetRenderTarget**](/windows/desktop/api) -oder [**IDirect3DDevice9:: setdepthstencilsurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface)-Befehl zu.</span><span class="sxs-lookup"><span data-stu-id="4670a-127">The application associates a device and its depth and color buffer with a call to [**IDirect3DDevice9::SetRenderTarget**](/windows/desktop/api) or [**IDirect3DDevice9::SetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface).</span></span>

<span data-ttu-id="4670a-128">Ausführliche Informationen zur Darstellung des endgültigen Bilds finden Sie unter [präsentieren einer Szene (Direct3D 9)](presenting-a-scene.md).</span><span class="sxs-lookup"><span data-stu-id="4670a-128">For details on presenting the final image, see [Presenting a Scene (Direct3D 9)](presenting-a-scene.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4670a-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4670a-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4670a-130">Direct3D-Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4670a-130">Direct3D Resources</span></span>](direct3d-resources.md)
</dt> </dl>

 

 
