---
description: Eine Oberfläche stellt einen linearen Bereich des Anzeigespeichers dar und befindet sich in der Regel im Anzeigespeicher der Anzeigekarte, obwohl Oberflächen im Systemspeicher vorhanden sein können. Oberflächen werden von der IDirect3DSurface9-Schnittstelle verwaltet.
ms.assetid: 17add726-3d95-46bc-8e15-3be0e570c49c
title: Direct3D-Oberflächen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 529320673eca39cf4b9afdb96377295d595191fd79cd81c316b258841d82ae6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988200"
---
# <a name="direct3d-surfaces-direct3d-9"></a>Direct3D-Oberflächen (Direct3D 9)

Eine Oberfläche stellt einen linearen Bereich des Anzeigespeichers dar und befindet sich in der Regel im Anzeigespeicher der Anzeigekarte, obwohl Oberflächen im Systemspeicher vorhanden sein können. Oberflächen werden von der [**IDirect3DSurface9-Schnittstelle**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) verwaltet.

-   Front Buffer( Frontpuffer). Ein Rechteck des Arbeitsspeichers, das vom Grafikadapter übersetzt und auf dem Monitor angezeigt wird. In Direct3D schreibt eine Anwendung nie direkt in den Frontpuffer.
-   Hintergrundpuffer. Ein Rechteck des Arbeitsspeichers, in das eine Anwendung direkt schreiben kann. Der Hintergrundpuffer wird nie direkt auf dem Monitor angezeigt.
-   Spiegelnde Oberflächen. Der Prozess des Verschiebens des Puffers zurück in den Frontpuffer.
-   Auslagerungskette. Eine Auflistung von einem oder mehr Hintergrundpuffern, die dem Frontpuffer seriell präsentiert werden können.

## <a name="getting-a-surface"></a>Abrufen einer Oberfläche

Erstellen Sie eine Oberfläche, indem Sie eine der folgenden Methoden aufrufen:

-   [**CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface)
-   [**CreateOffscreenPlainSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface)
-   [**CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget)

Oberflächenformate bestimmen, wie Daten für jedes Pixel im Oberflächenspeicher interpretiert werden. Direct3D verwendet den [D3DFORMAT-Member](d3dformat.md) der [**D3DSURFACE \_ DESC-Struktur,**](d3dsurface-desc.md) um das Oberflächenformat zu beschreiben. Sie können das Format einer vorhandenen Oberfläche abrufen, indem Sie die [**GetDesc-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdesc) aufrufen.

Sobald eine Oberfläche erstellt wurde, können Sie einen Zeiger darauf erhalten, indem Sie eine der folgenden Methoden aufrufen:

-   [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface)
-   [**GetBackBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getbackbuffer)
-   [**GetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdepthstencilsurface)
-   [**GetFrontBufferData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getfrontbufferdata)
-   [**GetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrendertarget)
-   [**GetBackBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getbackbuffer)
-   [**GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel)

Mit [**der IDirect3DSurface9-Schnittstelle**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) können Sie indirekt über die [**UpdateSurface-Methode**](/windows/desktop/api) auf den Arbeitsspeicher zugreifen. Mit dieser Methode können Sie einen rechteckigen Pixelbereich von einer **IDirect3DSurface9-Schnittstelle** in eine andere **IDirect3DSurface9-Schnittstelle** kopieren. Die Oberfläche verfügt auch über Methoden für den direkten Zugriff auf den Anzeigespeicher. Beispielsweise können Sie die [**LockRect-Methode**](/windows/desktop/api) verwenden, um einen rechteckigen Bereich des Anzeigespeichers zu sperren. Es ist wichtig, [**UnlockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-unlockrect) aufzurufen, nachdem Sie die Arbeit mit dem gesperrten rechteckigen Bereich auf der Oberfläche abgeschlossen haben.

## <a name="additional-surface-topics"></a>Weitere Surface-Themen

Erfahren Sie mehr über die Verwendung von Oberflächen mit einem der folgenden Themen:

-   [Oberflächenformate (Direct3D 9)](surface-formats.md)
-   [Was ist eine Austauschkette? (Direct3D 9)](what-is-a-swap-chain-.md)
-   [Breite im Vergleich zur Tonhöhe (Direct3D 9)](width-vs--pitch.md)
-   [Spiegelnde Oberflächen (Direct3D 9)](flipping-surfaces.md)
-   [Seitenumkehrung und Zurückpufferung (Direct3D 9)](page-flipping-and-back-buffering.md)
-   [Kopieren auf Oberflächen (Direct3D 9)](copying-to-surfaces.md)
-   [Kopieren von Oberflächen (Direct3D 9)](copying-surfaces.md)
-   [Direkter Zugriff auf Surface Memory (Direct3D 9)](accessing-surface-memory-directly.md)
-   [Private Surface Data (Direct3D 9)](private-surface-data.md)
-   [Gammasteuerelemente (Direct3D 9)](gamma-controls.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erste Schritte](getting-started.md)
</dt> </dl>

 

 
