---
title: Programm gesteuertes Initialisieren einer Textur
description: Dieses Thema enthält mehrere Beispiele, die zeigen, wie Texturen initialisiert werden, die mit verschiedenen Arten von Verwendungen erstellt werden.
ms.assetid: 65e8ae82-50aa-4303-853e-3457da18f44f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5584885b885f6026ee32a3e4c52a24aad78c3c08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856424"
---
# <a name="how-to-initialize-a-texture-programmatically"></a><span data-ttu-id="724e3-103">Gewusst wie: Programm gesteuertes Initialisieren einer Textur</span><span class="sxs-lookup"><span data-stu-id="724e3-103">How to: Initialize a Texture Programmatically</span></span>

<span data-ttu-id="724e3-104">Sie können während der Objekt Erstellung eine Textur initialisieren, oder Sie können das Objekt Programm gesteuert auffüllen, nachdem es erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="724e3-104">You can initialize a texture during object creation, or you can fill the object programmatically after it is created.</span></span> <span data-ttu-id="724e3-105">Dieses Thema enthält mehrere Beispiele, die zeigen, wie Texturen initialisiert werden, die mit verschiedenen Arten von Verwendungen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="724e3-105">This topic has several examples showing how to initialize textures that are created with different types of usages.</span></span> <span data-ttu-id="724e3-106">In diesem Beispiel wird davon ausgegangen, dass Sie bereits wissen, wie [eine Textur erstellt](overviews-direct3d-11-resources-textures-create.md)wird.</span><span class="sxs-lookup"><span data-stu-id="724e3-106">This example assumes you already know how to [Create a Texture](overviews-direct3d-11-resources-textures-create.md).</span></span>

-   [<span data-ttu-id="724e3-107">Standardverwendung</span><span class="sxs-lookup"><span data-stu-id="724e3-107">Default Usage</span></span>](#default-usage)
-   [<span data-ttu-id="724e3-108">Dynamische Verwendung</span><span class="sxs-lookup"><span data-stu-id="724e3-108">Dynamic Usage</span></span>](#dynamic-usage)
-   [<span data-ttu-id="724e3-109">Staging-Verwendung</span><span class="sxs-lookup"><span data-stu-id="724e3-109">Staging Usage</span></span>](#staging-usage)
-   [<span data-ttu-id="724e3-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="724e3-110">Related topics</span></span>](#related-topics)

## <a name="default-usage"></a><span data-ttu-id="724e3-111">Standardverwendung</span><span class="sxs-lookup"><span data-stu-id="724e3-111">Default Usage</span></span>

<span data-ttu-id="724e3-112">Die häufigste Art der Verwendung ist die Standardverwendung.</span><span class="sxs-lookup"><span data-stu-id="724e3-112">The most common type of usage is default usage.</span></span> <span data-ttu-id="724e3-113">Zum Auffüllen einer Standard Textur (mit **D3D11 \_ Usage \_ default**) können Sie Folgendes tun:</span><span class="sxs-lookup"><span data-stu-id="724e3-113">To fill a default texture (one created with **D3D11\_USAGE\_DEFAULT**) you can either:</span></span>

-   <span data-ttu-id="724e3-114">Wenden Sie [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) an, und initialisieren Sie *pinitialdata* , um auf die von einer Anwendung bereitgestellten Daten zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="724e3-114">Call [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) and initialize *pInitialData* to point to data provided from an application.</span></span>

    <span data-ttu-id="724e3-115">oder</span><span class="sxs-lookup"><span data-stu-id="724e3-115">or</span></span>

-   <span data-ttu-id="724e3-116">Verwenden Sie nach dem Aufrufen von [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) [**Verknüpfung id3d11devicecontext aus:: updatesubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) , um die Standard Textur mit Daten aus einem von der Anwendung bereitgestellten Zeiger zu füllen.</span><span class="sxs-lookup"><span data-stu-id="724e3-116">After calling [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d), use [**ID3D11DeviceContext::UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) to fill the default texture with data from a pointer provided by the application.</span></span>

## <a name="dynamic-usage"></a><span data-ttu-id="724e3-117">Dynamische Verwendung</span><span class="sxs-lookup"><span data-stu-id="724e3-117">Dynamic Usage</span></span>

<span data-ttu-id="724e3-118">So füllen Sie eine dynamische Textur (eine mit **\_ \_ dynamischer D3D11-Auslastung** erstellt):</span><span class="sxs-lookup"><span data-stu-id="724e3-118">To fill a dynamic texture (one created with **D3D11\_USAGE\_DYNAMIC**):</span></span>

1.  <span data-ttu-id="724e3-119">Rufen Sie einen Zeiger auf den Texturspeicher ab, indem Sie **D3D11 \_ map \_ Write \_ verwerfen** übergeben, wenn Sie [**Verknüpfung id3d11devicecontext aus:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="724e3-119">Get a pointer to the texture memory by passing in **D3D11\_MAP\_WRITE\_DISCARD** when calling [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).</span></span>
2.  <span data-ttu-id="724e3-120">Schreiben von Daten in den Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="724e3-120">Write data to the memory.</span></span>
3.  <span data-ttu-id="724e3-121">Wenn Sie mit dem Schreiben von Daten fertig sind, wird [**Verknüpfung id3d11devicecontext aus:: unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="724e3-121">Call [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) when you are finished writing data.</span></span>

## <a name="staging-usage"></a><span data-ttu-id="724e3-122">Staging-Verwendung</span><span class="sxs-lookup"><span data-stu-id="724e3-122">Staging Usage</span></span>

<span data-ttu-id="724e3-123">So füllen Sie eine stagingtextur (eine mit **D3D11 \_ Usage \_ Staging** erstellt):</span><span class="sxs-lookup"><span data-stu-id="724e3-123">To fill a staging texture (one created with **D3D11\_USAGE\_STAGING**):</span></span>

1.  <span data-ttu-id="724e3-124">Rufen Sie einen Zeiger auf den Texturspeicher ab, indem Sie beim Aufrufen von [**Verknüpfung id3d11devicecontext aus:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)den **D3D11 \_ map- \_ Schreibvorgang** übergeben.</span><span class="sxs-lookup"><span data-stu-id="724e3-124">Get a pointer to the texture memory by passing in **D3D11\_MAP\_WRITE** when calling [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).</span></span>
2.  <span data-ttu-id="724e3-125">Schreiben von Daten in den Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="724e3-125">Write data to the memory.</span></span>
3.  <span data-ttu-id="724e3-126">Wenn Sie mit dem Schreiben von Daten fertig sind, wird [**Verknüpfung id3d11devicecontext aus:: unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="724e3-126">Call [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) when you are finished writing data.</span></span>

<span data-ttu-id="724e3-127">Eine stagingtextur kann dann als Quellparameter für [**Verknüpfung id3d11devicecontext aus:: copyresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) oder [**Verknüpfung id3d11devicecontext aus:: copysubresourceregion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) verwendet werden, um eine Standard-oder dynamische Ressource auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="724e3-127">A staging texture can then be used as the source parameter to [**ID3D11DeviceContext::CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) or [**ID3D11DeviceContext::CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) to fill a default or dynamic resource.</span></span>

## <a name="related-topics"></a><span data-ttu-id="724e3-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="724e3-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="724e3-129">Verwendung von Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="724e3-129">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> <dt>

[<span data-ttu-id="724e3-130">Texturen</span><span class="sxs-lookup"><span data-stu-id="724e3-130">Textures</span></span>](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

 




