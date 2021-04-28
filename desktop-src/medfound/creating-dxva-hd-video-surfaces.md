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
# <a name="creating-dxva-hd-video-surfaces"></a>Erstellen von DXVA-HD-Videooberflächen

Die Anwendung muss eine oder mehrere Direct3D-Oberflächen erstellen, die für die Eingabeframes verwendet werden sollen. Diese müssen in dem Vom **InputPool-Member** der [**DXVAHD \_ VPDEVCAPS-Struktur**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) angegebenen Speicherpool zugeordnet werden. Die folgenden Oberflächentypen können verwendet werden:

-   Eine Videooberfläche, die durch Aufrufen von [**IDXVAHD \_ Device::CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) und Angeben des **DXVAHD \_ SURFACE TYPE VIDEO \_ \_ \_ INPUT-** oder **DXVAHD \_ SURFACE TYPE VIDEO INPUT \_ \_ \_ PRIVATE-Oberflächentyps \_** erstellt wurde. Dieser Oberflächentyp entspricht einer einfachen Oberfläche im Off-Screen-Bereich.
-   Eine Renderzieloberfläche des Decoders, die durch Aufrufen von [**IDirectXVideoAccelerationService::CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) und Angeben des **DXVA2 \_ VideoDecoderRenderTarget-Oberflächentyps** erstellt wird. Dieser Oberflächentyp wird für die DXVA-Decodierung verwendet.
-   Eine einfache Oberfläche im Off-Screen-Bildschirm.

Der folgende Code zeigt, wie Sie mit [**CreateVideoSurface eine Videooberfläche zuordnen:**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface)


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DXVA-HD](dxva-hd.md)
</dt> </dl>

 

 



