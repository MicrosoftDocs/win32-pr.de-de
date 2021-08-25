---
description: Erstellen von DXVA-HD-Videooberflächen
ms.assetid: a4508a1e-d68b-4c55-bce4-c8b462134fa1
title: Erstellen von DXVA-HD-Videooberflächen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d40058a02c179a8f9f0690eea9cce777bdd0563d5d27b36ddcb3d34f8fff8a07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829050"
---
# <a name="creating-dxva-hd-video-surfaces"></a>Erstellen von DXVA-HD-Videooberflächen

Die Anwendung muss eine oder mehrere Direct3D-Oberflächen erstellen, die für die Eingabeframes verwendet werden sollen. Diese müssen in dem Vom **InputPool-Member** der [**DXVAHD \_ VPDEVCAPS-Struktur**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) angegebenen Speicherpool zugeordnet werden. Die folgenden Oberflächentypen können verwendet werden:

-   Eine Videooberfläche, die durch Aufrufen von [**IDXVAHD \_ Device::CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) und Angeben des **DXVAHD \_ SURFACE TYPE VIDEO \_ \_ \_ INPUT-** oder **DXVAHD \_ SURFACE TYPE VIDEO INPUT \_ \_ \_ \_ PRIVATE** Surface-Typs erstellt wurde. Dieser Oberflächentyp entspricht einer einfachen Oberfläche im Off-Screen-Bereich.
-   Eine Renderzieloberfläche des Decoders, die durch Aufrufen von [**IDirectXVideoAccelerationService::CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) und Angeben des **DXVA2 \_ VideoDecoderRenderTarget-Oberflächentyps** erstellt wurde. Dieser Oberflächentyp wird für die DXVA-Decodierung verwendet.
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

 

 



