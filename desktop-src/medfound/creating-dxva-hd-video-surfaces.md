---
description: .
ms.assetid: a4508a1e-d68b-4c55-bce4-c8b462134fa1
title: Erstellen von DXVA-HD-Video Oberflächen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 459504a312ec0d59cf3642f528f433ffce8ba094
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861819"
---
# <a name="creating-dxva-hd-video-surfaces"></a><span data-ttu-id="7141d-103">Erstellen von DXVA-HD-Video Oberflächen</span><span class="sxs-lookup"><span data-stu-id="7141d-103">Creating DXVA-HD Video Surfaces</span></span>

<span data-ttu-id="7141d-104">Die Anwendung muss mindestens eine Direct3D-Oberfläche erstellen, die für die Eingabe Rahmen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7141d-104">The application must create one or more Direct3D surfaces to use for the input frames.</span></span> <span data-ttu-id="7141d-105">Diese müssen im Speicherpool zugeordnet werden, der vom **inputpool** -Member der [**\_ vpdevcaps-Struktur dxvahd**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7141d-105">These must be allocated in the memory pool specified by the **InputPool** member of the [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure.</span></span> <span data-ttu-id="7141d-106">Die folgenden Oberflächentypen können verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="7141d-106">The following surface types can be used:</span></span>

-   <span data-ttu-id="7141d-107">Eine Video Oberfläche, die durch Aufrufen von [**idxvahd \_ Device:: createvideosurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) und durch Angeben des Datentyps **dxvahd \_ Surface \_ Type \_ Video \_ Input** oder **dxvahd \_ Surface \_ Type \_ \_ \_ private** Surface Type erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="7141d-107">A video surface created by calling [**IDXVAHD\_Device::CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) and specifying the **DXVAHD\_SURFACE\_TYPE\_VIDEO\_INPUT** or **DXVAHD\_SURFACE\_TYPE\_VIDEO\_INPUT\_PRIVATE** surface type.</span></span> <span data-ttu-id="7141d-108">Dieser Oberflächen Typ entspricht einer flachen Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="7141d-108">This surface type is equivalent to an off-screen plain surface.</span></span>
-   <span data-ttu-id="7141d-109">Eine renderzieloberfläche des Decoders, die durch Aufrufen von [**idirectxvideoaccelerationservice:: CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) und angeben des **DXVA2 \_ videodecoderrendertarget** -Oberflächen Typs erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="7141d-109">A decoder render-target surface, created by calling [**IDirectXVideoAccelerationService::CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) and specifying the **DXVA2\_VideoDecoderRenderTarget** surface type.</span></span> <span data-ttu-id="7141d-110">Dieser Surface-Typ wird für die DXVA-Decodierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="7141d-110">This surface type is used for DXVA decoding.</span></span>
-   <span data-ttu-id="7141d-111">Eine Schaltfläche außerhalb des Bildschirms.</span><span class="sxs-lookup"><span data-stu-id="7141d-111">An off-screen plain surface.</span></span>

<span data-ttu-id="7141d-112">Der folgende Code zeigt, wie Sie eine Video Oberfläche mithilfe von [**createvideosurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface)zuordnen:</span><span class="sxs-lookup"><span data-stu-id="7141d-112">The following code shows how to allocate a video surface, using [**CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface):</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="7141d-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7141d-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7141d-114">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="7141d-114">DXVA-HD</span></span>](dxva-hd.md)
</dt> </dl>

 

 



