---
description: Bei den Präsentations-APIs handelt es sich um einen Satz von Methoden, mit denen der Zustand des Geräts gesteuert wird, das sich auf den Benutzer des Monitors auswirkt. Zu diesen Methoden gehören das Festlegen von Anzeigemodi und einmal pro Frame-Methoden, die zum Darstellen von Bildern für den Benutzer verwendet werden.
ms.assetid: fb2ddc0d-50ac-48aa-8a5c-f232b0f8e7aa
title: Einführung in das präsentieren einer Szene (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d909f2d7fcc04cd58c27c7598ca8f826b27f48a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341839"
---
# <a name="introduction-to-presenting-a-scene-direct3d-9"></a>Einführung in das präsentieren einer Szene (Direct3D 9)

Bei den Präsentations-APIs handelt es sich um einen Satz von Methoden, mit denen der Zustand des Geräts gesteuert wird, das sich auf den Benutzer des Monitors auswirkt. Zu diesen Methoden gehören das Festlegen von Anzeigemodi und einmal pro Frame-Methoden, die zum Darstellen von Bildern für den Benutzer verwendet werden.

-   [**IDirect3DDevice9::P erneut gesendet.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)
-   [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)
-   [**IDirect3DDevice9:: getgammaramp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp)
-   [**IDirect3DDevice9:: setgammaramp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp)
-   [**IDirect3DDevice9:: getrasterstatus**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrasterstatus)

Kenntnisse der folgenden Begriffe sind erforderlich, um die Präsentations-APIs zu verstehen.

-   Vorder-Puffer. Ein Rechteck des Arbeitsspeichers, der vom Grafikadapter übersetzt und auf dem Monitor oder einem anderen Ausgabegerät angezeigt wird.
-   Hintergrund Puffer. Eine Oberfläche, deren Inhalt zum Vordergrund Puffer herauf gestuft werden kann.
-   Austausch Kette. Eine Auflistung von backpuffern, die seriell dem Vorder-Puffer angezeigt werden können. In der Regel stellt eine voll Bildaustausch Kette nachfolgende Bilder mit der flippinggeräte Treiberschnittstelle (DDI) dar, und eine Austausch Kette mit einem Fenster stellt Bilder mit dem blierungs-DDI dar.

Da Direct3D 9 eine SwapChain als Eigenschaft des Geräts hat, gibt es immer mindestens eine Auslagerungs Kette pro Gerät. Die [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle verfügt über eine Reihe von Methoden, die die implizite Austausch Kette bearbeiten und eine Kopie der eigenen Schnittstelle der SwapChain sind. Anwendungen können zusätzliche Austausch Ketten erstellen; Dies ist jedoch für die typische Einzelfenster-oder Vollbildanwendung nicht erforderlich.

Der Front-Puffer wird in Direct3D 9 nicht direkt verfügbar gemacht. Daher können Anwendungen nicht in den vorderen Puffer gesperrt oder gerenbt werden. Weitere Informationen finden Sie unter [zugreifen auf den Farben-Front-Puffer (Direct3D 9)](accessing-the-color-front-buffer.md).

> [!Note]  
> DirectX 7 hat eine Reihe von Präsentations-APIs bereitgestellt, die gleich aufgerufen wurden. Ein gutes Beispiel hierfür sind die Sequenz "IDirectDraw7:: setCooperativeLevel", "IDirectDraw7:: setdisplaymode" und "IDirectDraw7:: samatesurface". Darüber hinaus signalisieren die IDirectDrawSurface7:: Flip-Methode und die IDirectDrawSurface7:: BLT-Methode den Transport von gerenderten Frames zum Monitor. Direct3D 9 reduziert diese Gruppen von APIs in zwei Hauptmethoden, die zurückgesetzt und vorhanden sind. Setzen Sie die subsumen setkooperativelevel, setdisplaymode, up Sample und einige der Parameter zum Kippen zurück. Gegenwärtige subsumes kippen und die Präsentation von Blit.

 

Ein Aufrufen von [**IDirect3D9:: kreatedevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) stellt eine implizite zurück setzung des Geräts dar. Die API Direct3D 9 hat keine Vorstellung von einer primären Oberfläche. Sie können kein-Objekt erstellen, das die primäre Oberfläche darstellt. Es gilt als interne Eigenschaft des Geräts.

Gamma Rampen werden einer Swapkette zugeordnet und mit den Methoden [**IDirect3DDevice9:: getgammaramp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp) und [**IDirect3DDevice9:: setgammaramp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) manipuliert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Präsentieren einer Szene](presenting-a-scene.md)
</dt> </dl>

 

 
