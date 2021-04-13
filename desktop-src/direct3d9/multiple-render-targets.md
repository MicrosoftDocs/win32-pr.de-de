---
description: Mehrere Renderziele (MRT) bezieht sich auf die Fähigkeit zum renderingzeichen auf mehreren Oberflächen (siehe IDirect3D9Surface) mit einem einzelnen zeichnen-Befehl.
ms.assetid: ae48c5ce-b7f5-4189-8b04-880836be3fe0
title: Mehrere Renderziele (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb7aafeedb621e43abb288eb9bbceb17ddb0cc0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482046"
---
# <a name="multiple-render-targets-direct3d-9"></a>Mehrere Renderziele (Direct3D 9)

Mehrere Renderziele (MRT) bezieht sich auf die Fähigkeit zum renderingzeichen auf mehreren Oberflächen (siehe [**IDirect3D9Surface**](/windows/desktop/api)) mit einem einzelnen zeichnen-Befehl. Diese Oberflächen können unabhängig voneinander erstellt werden. Renderziele können mithilfe von [**IDirect3DDevice9:: SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget)festgelegt werden.

Mehrere Renderziele weisen die folgenden Einschränkungen auf:

-   Alle gemeinsamen renderzieloberflächen müssen die gleiche Bittiefe aufweisen, können jedoch unterschiedliche Formate aufweisen, es sei denn, das D3DPMISCCAPS \_ mrtindependentbittiefen-Cap ist festgelegt.
-   Alle Oberflächen eines multirenderziels sollten dieselbe Breite und Höhe aufweisen.
-   Einige Implementierungen können keine Post-Pixel-Shader-Vorgänge für mehrere Renderziele ausführen, wie z. b. "keine Dithering", "Alpha Test", "kein erstellen", "keine Vermischung" und Maskierung, außer dem z-Test und dem Schablone Geräte, die Post-Pixel-Shader-Vorgänge unterstützen können, legen das Cap-Bit auf D3DPMISCCAPS \_ mrtpostpixelshaderblending fest.

    Wenn das D3DPMISCCAPS \_ mrtpostpixelshaderblending-Cap festgelegt ist, müssen Sie zuerst das [**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) mit der Verwendungs \_ Abfrage \_ postpixelshader- \_ Mischungs Ergebnis für das jeweilige Oberflächen Format überprüfen. Wenn der Wert false ist, sind keine Mischungs Vorgänge nach Pixel-Shader für dieses bestimmte Oberflächen Format verfügbar. Wenn der Wert true ist, wird erwartet, dass das Gerät denselben Status auf alle gleichzeitigen Renderziele anwendet wie folgt:

    -   Alpha Blend: der Farbwert in OCI wird mit dem ITH-Renderziel gemischt.
    -   Alpha-Test: der Vergleich erfolgt mit oC0. Wenn der Vergleich fehlschlägt, wird der Pixel Test für alle Renderziele beendet.
    -   Nebel: Renderziel 0 wird gefoppt. Andere Renderziele sind nicht definiert. Implementierungen können alle mit dem gleichen Zustand ein Nebel durch die Auswahl treffen.
    -   Dithering: nicht definiert.

-   Es wird kein Antialiasing unterstützt.
-   Einige Implementierungen wenden nicht die Ausgabe Schreib Maske an (D3DRS \_ colorschreiteenable). Solche, die über unabhängige Farb Schreib Masken verfügen können. Dies wird mithilfe eines neuen Funktionsbits ausgedrückt. Die Anzahl der verfügbaren unabhängigen Farb Schreib Masken ist gleich der maximalen Anzahl von Elementen, für die das Gerät geeignet ist.

Neue Hardware Obergrenzen:


```
D3DCAPS9.NumSimultaneousRTs         
// The value is 1 for all hardware except those that  
//   can support this feature. It is never 0.
D3DPMISCCAPS_MRTINDEPENDENTBITDEPTHS - True if the hardware can support it
D3DPMISCCAPS_MRTPOSTPIXELSHADERBLENDING - True if the hardware can support it
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixel Pipeline](pixel-pipeline.md)
</dt> </dl>

 

 
