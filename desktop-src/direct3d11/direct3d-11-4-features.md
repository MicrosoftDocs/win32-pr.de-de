---
title: Direct3D 11,4-Features
description: Die folgende Funktionalität wurde in Direct3D 11,4 hinzugefügt.
ms.assetid: 689A0460-5725-4C48-B960-41FE20499082
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5b0d2814aa1f9a7ac7b5f2c87ff9d918b36116f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948899"
---
# <a name="direct3d-114-features"></a><span data-ttu-id="f4c5b-103">Direct3D 11,4-Features</span><span class="sxs-lookup"><span data-stu-id="f4c5b-103">Direct3D 11.4 Features</span></span>

<span data-ttu-id="f4c5b-104">Die folgende Funktionalität wurde in Direct3D 11,4 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f4c5b-104">The following functionality has been added in Direct3D 11.4.</span></span>

<span data-ttu-id="f4c5b-105">Weitere Informationen finden Sie auch [unter wo ist das DirectX SDK?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="f4c5b-105">Also see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

## <a name="direct3d-device-removal"></a><span data-ttu-id="f4c5b-106">Direct3D Entfernen von Geräten</span><span class="sxs-lookup"><span data-stu-id="f4c5b-106">Direct3D device removal</span></span>

<span data-ttu-id="f4c5b-107">Die [**registerdeviceremovedevent**](/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-registerdeviceremovedevent)-Methode und die [**unregisterdeviceremoved**](/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-unregisterdeviceremoved) -Methode werden von der neuen Schnittstelle [**ID3D11Device4**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4)unterstützt, um den Empfang einer asynchronen Ereignis Benachrichtigung zu unterstützen, wenn ein Direct3D-Gerät entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="f4c5b-107">The [**RegisterDeviceRemovedEvent**](/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-registerdeviceremovedevent), and [**UnregisterDeviceRemoved**](/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-unregisterdeviceremoved) methods are supported by a new interface, [**ID3D11Device4**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4), to support receiving an asynchronous event notification when a Direct3D device has been removed.</span></span>

## <a name="multithreaded-protection"></a><span data-ttu-id="f4c5b-108">Multithread-Schutz</span><span class="sxs-lookup"><span data-stu-id="f4c5b-108">Multithreaded protection</span></span>

<span data-ttu-id="f4c5b-109">Um sicherzustellen, dass Grafikbefehle speziell in einer bestimmten Reihenfolge ausgeführt werden, verfügt die [**ID3D11Multithread**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11multithread) -Schnittstelle über Methoden zum Aktivieren und Deaktivieren des multithreadschutzes sowie Methoden zum eingeben und verlassen von kritischem Code, der diesen Schutz erfordert.</span><span class="sxs-lookup"><span data-stu-id="f4c5b-109">To ensure that graphics commands in particular are executed in a specific order, the [**ID3D11Multithread**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11multithread) interface has methods to turn multithread protection on and off, and methods to enter and leave critical code requiring this protection.</span></span>

## <a name="fences-for-multi-device-synchronization-and-interop-with-direct3d-12"></a><span data-ttu-id="f4c5b-110">Zäune für die Synchronisierung von mehreren Geräten und Interop mit Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="f4c5b-110">Fences for multi-device synchronization and interop with Direct3D 12</span></span>

<span data-ttu-id="f4c5b-111">[**ID3D11Fence**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11fence), [**ID3D11Device5**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5) und [**ID3D11DeviceContext4**](/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4) bieten die gleiche Fence-Funktionalität wie Direct3D 12 für Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="f4c5b-111">The [**ID3D11Fence**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11fence), [**ID3D11Device5**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5) and [**ID3D11DeviceContext4**](/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4) provide the same fence functionality as Direct3D 12 for Direct3D 11.</span></span> <span data-ttu-id="f4c5b-112">Mithilfe von Zäunen werden mehrere Direct3D11-Geräte und Interop zwischen Direct3D 11 und Direct3D 12 synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="f4c5b-112">Fences are used to synchronize multiple Direct3D11 devices, and for interop between Direct3D 11 and Direct3D 12.</span></span> <span data-ttu-id="f4c5b-113">Im Windows 10 Creators Update werden Zäune unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f4c5b-113">Fences are supported in the Windows 10 Creators Update.</span></span>

## <a name="extended-nv12-texture-support"></a><span data-ttu-id="f4c5b-114">Erweiterte NV12-Textur Unterstützung</span><span class="sxs-lookup"><span data-stu-id="f4c5b-114">Extended NV12 texture support</span></span>

<span data-ttu-id="f4c5b-115">NV12 Texturen mit Erfassungs-und videocodierfunktionen unterstützen jetzt die Freigabe.</span><span class="sxs-lookup"><span data-stu-id="f4c5b-115">NV12 textures with capture and video encode capabilities now support sharing.</span></span> <span data-ttu-id="f4c5b-116">Ältere D3D11-Textur-Flags für videoencode und Capture sind für NV12 veraltet, da Sie für neue Treiber ständig festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f4c5b-116">Older D3D11 texture flags for video encode and capture are deprecated for NV12, as it will be set all the time for new drivers.</span></span> <span data-ttu-id="f4c5b-117">Solche Texturen können nicht nur mit D3D11, sondern auch mit D3D12 freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f4c5b-117">Such textures can be shared not only with D3D11, but also with D3D12.</span></span> <span data-ttu-id="f4c5b-118">In D3D12 stellen keine neuen Flags diese Textur Funktionen dar.</span><span class="sxs-lookup"><span data-stu-id="f4c5b-118">In D3D12, no new flags represent these texture capabilities.</span></span>

<span data-ttu-id="f4c5b-119">Weitere Informationen finden Sie in der booleschen Einstellung in [**D3D11 \_ Feature \_ Data \_ D3D11 \_ OPTIONS4**](/windows/desktop/api/d3d11_4/ns-d3d11_4-d3d11_feature_data_d3d11_options4).</span><span class="sxs-lookup"><span data-stu-id="f4c5b-119">Refer to the boolean setting in [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS4**](/windows/desktop/api/d3d11_4/ns-d3d11_4-d3d11_feature_data_d3d11_options4).</span></span>

## <a name="shader-caching"></a><span data-ttu-id="f4c5b-120">Shader-Caching</span><span class="sxs-lookup"><span data-stu-id="f4c5b-120">Shader Caching</span></span>

<span data-ttu-id="f4c5b-121">Treiber unterstützen möglicherweise das vom Betriebssystem verwaltete Shader-Caching von Direct3D11-Anwendungen im Windows 10 Creators Update.</span><span class="sxs-lookup"><span data-stu-id="f4c5b-121">Drivers may support OS-managed shader caching of Direct3D11 applications in the Windows 10 Creators update.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f4c5b-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f4c5b-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4c5b-123">Neuerungen in Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="f4c5b-123">What's new in Direct3D 11</span></span>](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 