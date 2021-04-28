---
description: Erstellen von DXVA-HD-Videooberflächen
ms.assetid: a4508a1e-d68b-4c55-bce4-c8b462134fa1
title: Erstellen von DXVA-HD-Videooberflächen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e20dea8f34a275aab59b2d57f68ca76d46b1c1f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102548"
---
# <a name="creating-dxva-hd-video-surfaces"></a><span data-ttu-id="302b1-103">Erstellen von DXVA-HD-Videooberflächen</span><span class="sxs-lookup"><span data-stu-id="302b1-103">Creating DXVA-HD Video Surfaces</span></span>

<span data-ttu-id="302b1-104">Die Anwendung muss eine oder mehrere Direct3D-Oberflächen erstellen, die für die Eingabeframes verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="302b1-104">The application must create one or more Direct3D surfaces to use for the input frames.</span></span> <span data-ttu-id="302b1-105">Diese müssen in dem Vom **InputPool-Member** der [**DXVAHD \_ VPDEVCAPS-Struktur**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) angegebenen Speicherpool zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="302b1-105">These must be allocated in the memory pool specified by the **InputPool** member of the [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure.</span></span> <span data-ttu-id="302b1-106">Die folgenden Oberflächentypen können verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="302b1-106">The following surface types can be used:</span></span>

-   <span data-ttu-id="302b1-107">Eine Videooberfläche, die durch Aufrufen von [**IDXVAHD \_ Device::CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) und Angeben des **DXVAHD \_ SURFACE TYPE VIDEO \_ \_ \_ INPUT-** oder **DXVAHD \_ SURFACE TYPE VIDEO INPUT \_ \_ \_ PRIVATE-Oberflächentyps \_** erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="302b1-107">A video surface created by calling [**IDXVAHD\_Device::CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) and specifying the **DXVAHD\_SURFACE\_TYPE\_VIDEO\_INPUT** or **DXVAHD\_SURFACE\_TYPE\_VIDEO\_INPUT\_PRIVATE** surface type.</span></span> <span data-ttu-id="302b1-108">Dieser Oberflächentyp entspricht einer einfachen Oberfläche im Off-Screen-Bereich.</span><span class="sxs-lookup"><span data-stu-id="302b1-108">This surface type is equivalent to an off-screen plain surface.</span></span>
-   <span data-ttu-id="302b1-109">Eine Renderzieloberfläche des Decoders, die durch Aufrufen von [**IDirectXVideoAccelerationService::CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) und Angeben des **DXVA2 \_ VideoDecoderRenderTarget-Oberflächentyps** erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="302b1-109">A decoder render-target surface, created by calling [**IDirectXVideoAccelerationService::CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) and specifying the **DXVA2\_VideoDecoderRenderTarget** surface type.</span></span> <span data-ttu-id="302b1-110">Dieser Oberflächentyp wird für die DXVA-Decodierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="302b1-110">This surface type is used for DXVA decoding.</span></span>
-   <span data-ttu-id="302b1-111">Eine einfache Oberfläche im Off-Screen-Bildschirm.</span><span class="sxs-lookup"><span data-stu-id="302b1-111">An off-screen plain surface.</span></span>

<span data-ttu-id="302b1-112">Der folgende Code zeigt, wie Sie mit [**CreateVideoSurface eine Videooberfläche zuordnen:**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface)</span><span class="sxs-lookup"><span data-stu-id="302b1-112">The following code shows how to allocate a video surface, using [**CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface):</span></span>


```C++
    // Create the video surface for the primary video stream.
    hr = pDXVAHD->CreateVideoSurface(
        VIDEO_WIDTH,
        VIDEO_HEIGHT,
        VIDEO_FORMAT,
        caps.InputPool,
        0,  // Usage
        DXVAHD_SURFACE_TYPE_VIDEO_INPUT,
        1,      // Number of surfaces to create
        &pSurf, // Array of surface pointers
        NULL
        );
```



## <a name="related-topics"></a><span data-ttu-id="302b1-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="302b1-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="302b1-114">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="302b1-114">DXVA-HD</span></span>](dxva-hd.md)
</dt> </dl>

 

 



