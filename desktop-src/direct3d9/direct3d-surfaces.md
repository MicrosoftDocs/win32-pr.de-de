---
description: Eine Oberfläche stellt einen linearen Bereich des Anzeige Speichers dar und befindet sich normalerweise im Anzeige Speicher der Anzeigekarte, obwohl die Oberfläche im Systemspeicher vorhanden sein kann. Oberflächen werden von der IDirect3DSurface9-Schnittstelle verwaltet.
ms.assetid: 17add726-3d95-46bc-8e15-3be0e570c49c
title: Direct3D-Oberflächen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08729cc7252c39ddf71048991a796469f2e8b0b2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745400"
---
# <a name="direct3d-surfaces-direct3d-9"></a>Direct3D-Oberflächen (Direct3D 9)

Eine Oberfläche stellt einen linearen Bereich des Anzeige Speichers dar und befindet sich normalerweise im Anzeige Speicher der Anzeigekarte, obwohl die Oberfläche im Systemspeicher vorhanden sein kann. Oberflächen werden von der [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) -Schnittstelle verwaltet.

-   Vorder-Puffer. Ein Rechteck des Arbeitsspeichers, der vom Grafikadapter übersetzt und auf dem Monitor angezeigt wird. In Direct3D schreibt eine Anwendung niemals direkt in den Vorder-Puffer.
-   Hintergrund Puffer. Ein Rechteck des Arbeitsspeichers, in den eine Anwendung direkt schreiben kann. Der Hintergrund Puffer wird nie direkt auf dem Monitor angezeigt.
-   Flipping-Oberflächen. Der Prozess, bei dem der Hintergrund Puffer in den Vordergrund Puffer verschoben wird.
-   Austausch Kette. Eine Auflistung von einem oder mehreren Back Puffern, die seriell dem Vorder-Puffer angezeigt werden können.

## <a name="getting-a-surface"></a>Erhalten einer Oberfläche

Erstellen Sie eine Oberfläche, indem Sie eine der folgenden Methoden aufrufen:

-   [**"Kreatedepthstencilsurface"**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface)
-   [**"Kreateoffscreenplainsurface"**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface)
-   [**"Kreaterendertarget"**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget)

Oberflächen Formate legen fest, wie Daten für die einzelnen Pixel im Oberflächen Speicher interpretiert werden. Direct3D verwendet das [D3DFORMAT](d3dformat.md) -Member der [**D3DSURFACE \_ DESC**](d3dsurface-desc.md) -Struktur, um das Oberflächen Format zu beschreiben. Sie können das Format einer vorhandenen Oberfläche abrufen, indem Sie die [**getdesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdesc) -Methode aufrufen.

Nachdem eine Oberfläche erstellt wurde, können Sie einen Zeiger darauf abrufen, indem Sie eine der folgenden Methoden aufrufen:

-   [**Getcubemapsurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface)
-   [**GetBackBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getbackbuffer)
-   [**Getdepthstencilsurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdepthstencilsurface)
-   [**Getfrontbufferdata**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getfrontbufferdata)
-   [**GetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrendertarget)
-   [**GetBackBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getbackbuffer)
-   [**Getsurfakelevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel)

Die [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) -Schnittstelle ermöglicht Ihnen den indirekten Zugriff auf den Arbeitsspeicher über die [**updatesurface**](/windows/desktop/api) -Methode. Mit dieser Methode können Sie einen rechteckigen Bereich von Pixeln von einer **IDirect3DSurface9** -Schnittstelle in eine andere **IDirect3DSurface9** -Schnittstelle kopieren. Die Oberflächen Schnittstelle verfügt auch über Methoden, um direkt auf den Anzeige Speicher zuzugreifen. Beispielsweise können Sie die [**lockrect**](/windows/desktop/api) -Methode verwenden, um einen rechteckigen Bereich des Anzeige Speichers zu sperren. Es ist wichtig, [**unlockrect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-unlockrect) aufzurufen, nachdem Sie die Arbeit mit dem gesperrten rechteckigen Bereich auf der-Oberfläche abgeschlossen haben.

## <a name="additional-surface-topics"></a>Zusätzliche Oberflächen Themen

Weitere Informationen zur Verwendung von Oberflächen finden Sie in den folgenden Themen:

-   [Oberflächen Formate (Direct3D 9)](surface-formats.md)
-   [Was ist eine austauschkette? (Direct3D 9)](what-is-a-swap-chain-.md)
-   [Breite und Tonhöhe (Direct3D 9)](width-vs--pitch.md)
-   [Flipping-Oberflächen (Direct3D 9)](flipping-surfaces.md)
-   [Seiten kippen und zurück Pufferung (Direct3D 9)](page-flipping-and-back-buffering.md)
-   [Kopieren auf Oberflächen (Direct3D 9)](copying-to-surfaces.md)
-   [Kopieren von Oberflächen (Direct3D 9)](copying-surfaces.md)
-   [Direktes Zugreifen auf den Surface-Speicher (Direct3D 9)](accessing-surface-memory-directly.md)
-   [Private Oberflächendaten (Direct3D 9)](private-surface-data.md)
-   [Gamma Steuerelemente (Direct3D 9)](gamma-controls.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erste Schritte](getting-started.md)
</dt> </dl>

 

 
