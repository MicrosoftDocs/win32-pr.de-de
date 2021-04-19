---
description: Einige ältere 3D-Zugriffstasten bieten keine Unterstützung für Textur Mischungen mithilfe des Alphawerts des Zielpixels.
ms.assetid: 77d3b9fd-3232-4955-9df2-d4763d3eed6f
title: Monochrome helle Karten (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9ca63c2e7bb3ed51f1c6c5184536aa51e0a11e3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346183"
---
# <a name="monochrome-light-maps-direct3d-9"></a>Monochrome helle Karten (Direct3D 9)

Einige ältere 3D-Zugriffstasten bieten keine Unterstützung für Textur Mischungen mithilfe des Alphawerts des Zielpixels. Weitere Informationen finden Sie unter [Alpha Textur blending (Direct3D 9)](alpha-texture-blending.md) . Diese Adapter unterstützen in der Regel auch keine mehrfach Textur Mischung. Wenn die Anwendung auf einem Adapter wie diesem ausgeführt wird, kann Sie Multipass-Textur Mischungs Vorgänge verwenden, um eine monochrome einfache Zuordnung auszuführen.

Zum Durchführen einer Monochrom-Licht Zuordnung speichert eine Anwendung die Beleuchtungs Informationen in den Alpha Daten ihrer hellen Karten Texturen. Die Anwendung verwendet die Textur Filterungs Funktionen von Direct3D, um eine Zuordnung von jedem Pixel im primitiven Bild zu einem entsprechenden Texel in der lichtkarte auszuführen. Der quellmischungs Faktor wird auf den Alpha Wert des entsprechenden Texttyps festgelegt.

Im folgenden Beispiel wird veranschaulicht, wie eine Anwendung eine Textur als monochrome Light map verwenden kann:


```
// This example assumes that d3dDevice is a valid pointer to an
// IDirect3DDevice9 interface and that lptexLightMap is a valid
// pointer to a texture that contains monochrome light map data.

// Set the light map texture as the current texture.
d3dDevice->SetTexture(0, lptexLightMap);

// Set the color operation.
d3dDevice->SetTextureStageState(0, D3DTSS_COLOROP, D3DTOP_SELECTARG1);

// Set argument 1 to the color operation.
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG1,
                                D3DTA_TEXTURE | D3DTA_ALPHAREPLICATE);
```



Da Anzeige Adapter, die keine Ziel-Alpha-Blending unterstützen, in der Regel nicht mehrere Textur Mischungen unterstützen, wird in diesem Beispiel die helle Karte als erste Textur festgelegt, die auf allen 3D-Zugriffs Karten verfügbar ist. Im Beispielcode wird der Farb Vorgang für die Mischungs Phase der Textur festgelegt, um die Textur Daten mit der vorhandenen Farbe des Primitivs zu vermischen. Anschließend werden die erste Textur und die vorhandene Farbe des primitiven als Eingabedaten ausgewählt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einfache Zuordnung mit Texturen](light-mapping-with-textures.md)
</dt> </dl>

 

 



