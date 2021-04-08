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
# <a name="creating-dxva-hd-video-surfaces"></a>Erstellen von DXVA-HD-Video Oberflächen

Die Anwendung muss mindestens eine Direct3D-Oberfläche erstellen, die für die Eingabe Rahmen verwendet werden soll. Diese müssen im Speicherpool zugeordnet werden, der vom **inputpool** -Member der [**\_ vpdevcaps-Struktur dxvahd**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) angegeben wird. Die folgenden Oberflächentypen können verwendet werden:

-   Eine Video Oberfläche, die durch Aufrufen von [**idxvahd \_ Device:: createvideosurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) und durch Angeben des Datentyps **dxvahd \_ Surface \_ Type \_ Video \_ Input** oder **dxvahd \_ Surface \_ Type \_ \_ \_ private** Surface Type erstellt wurde. Dieser Oberflächen Typ entspricht einer flachen Oberfläche.
-   Eine renderzieloberfläche des Decoders, die durch Aufrufen von [**idirectxvideoaccelerationservice:: CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) und angeben des **DXVA2 \_ videodecoderrendertarget** -Oberflächen Typs erstellt wird. Dieser Surface-Typ wird für die DXVA-Decodierung verwendet.
-   Eine Schaltfläche außerhalb des Bildschirms.

Der folgende Code zeigt, wie Sie eine Video Oberfläche mithilfe von [**createvideosurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface)zuordnen:


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

 

 



