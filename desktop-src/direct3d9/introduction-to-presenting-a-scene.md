---
description: Bei den Präsentations-APIs handelt es sich um eine Reihe von Methoden, die den Zustand des Geräts steuern, die sich auf das auswirken, was dem Benutzer auf dem Monitor angezeigt wird. Zu diesen Methoden gehören das Festlegen von Anzeigemodi und Einmal-pro-Frame-Methoden, die zum Präsentieren von Bildern für den Benutzer verwendet werden.
ms.assetid: fb2ddc0d-50ac-48aa-8a5c-f232b0f8e7aa
title: Einführung in die Präsentation einer Szene (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9abf584bad1bfbbde2bbfa2e9281acf3ad2173403507e06bbdc2abc5f5edd1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846550"
---
# <a name="introduction-to-presenting-a-scene-direct3d-9"></a>Einführung in die Präsentation einer Szene (Direct3D 9)

Bei den Präsentations-APIs handelt es sich um eine Reihe von Methoden, die den Zustand des Geräts steuern, die sich auf das auswirken, was dem Benutzer auf dem Monitor angezeigt wird. Zu diesen Methoden gehören das Festlegen von Anzeigemodi und Einmal-pro-Frame-Methoden, die zum Präsentieren von Bildern für den Benutzer verwendet werden.

-   [**IDirect3DDevice9::P resent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)
-   [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)
-   [**IDirect3DDevice9::GetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp)
-   [**IDirect3DDevice9::SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp)
-   [**IDirect3DDevice9::GetRasterStatus**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrasterstatus)

Vertrautheit mit den folgenden Begriffen ist erforderlich, um die Präsentations-APIs zu verstehen.

-   Frontpuffer. Ein Rechteck des Arbeitsspeichers, das vom Grafikadapter übersetzt und auf dem Monitor oder einem anderen Ausgabegerät angezeigt wird.
-   Backpuffer. Eine Oberfläche, deren Inhalt in den Frontpuffer promotet werden kann.
-   Auslagerungskette. Eine Auflistung von Hintergrundpuffern, die dem Frontpuffer seriell präsentiert werden können. In der Regel zeigt eine Auslagerungskette im Vollbildmodus nachfolgende Bilder mit der flipping Device Driver Interface (DDI) an, und eine Swapkette mit Fenstern stellt Bilder mit der blitting DDI bereit.

Da Direct3D 9 über eine Swapkette als Eigenschaft des Geräts verfügt, gibt es immer mindestens eine Austauschkette pro Gerät. Die [**IDirect3DDevice9-Schnittstelle**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) verfügt über eine Reihe von Methoden, die die implizite Austauschkette bearbeiten und eine Kopie der eigenen Schnittstelle der Swapkette sind. Anwendungen können zusätzliche Austauschketten erstellen. Dies ist jedoch für die typische Einzelfenster- oder Vollbildanwendung nicht erforderlich.

Der Frontpuffer wird in Direct3D 9 nicht direkt verfügbar gemacht. Daher können Anwendungen den Frontpuffer nicht sperren oder rendern. Weitere Informationen finden Sie unter [Zugreifen auf den Farbfrontpuffer (Direct3D 9).](accessing-the-color-front-buffer.md)

> [!Note]  
> DirectX 7 stellt eine Reihe von Präsentations-APIs zur Verfügung, die zusammen aufgerufen wurden. Ein gutes Beispiel hierfür ist die Sequenz IDirectDraw7::SetCooperativeLevel, IDirectDraw7::SetDisplayMode und IDirectDraw7::CreateSurface. Darüber hinaus signalisierten die Methoden IDirectDrawSurface7::Flip und IDirectDrawSurface7::Blt den Transport gerenderter Frames an den Monitor. Direct3D 9 reduziert diese Gruppen von APIs in zwei Hauptmethoden: Reset und Present. Setzen Sie die Subsums SetCooperativeLevel, SetDisplayMode, CreateSurface und einige der parameter zurück, die gekippt werden müssen. Present subsumes flip and the presentation uses of blit.

 

Ein Aufruf von [**IDirect3D9::CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) stellt eine implizite Zurücksetzung des Geräts dar. Die Direct3D 9-API hat keine Vorstellung von einer primären Oberfläche. Sie können kein Objekt erstellen, das die primäre Oberfläche darstellt. Es wird als interne Eigenschaft des Geräts betrachtet.

Gamma-Rampen sind einer Austauschkette zugeordnet und werden mit den [**Methoden IDirect3DDevice9::GetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp) und [**IDirect3DDevice9::SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) bearbeitet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Präsentieren einer Szene](presenting-a-scene.md)
</dt> </dl>

 

 
