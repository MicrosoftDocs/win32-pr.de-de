---
description: 'Wenn IDirect3DDevice9:: updatesurface verwendet wird, übergeben Sie ein Rechteck auf der Quell Oberfläche, oder verwenden Sie NULL, um die gesamte Oberfläche anzugeben.'
ms.assetid: 2219d037-8480-4c36-b04e-0c23406a2e7e
title: Kopieren auf Oberflächen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 163907aada5b2396a2a103d94af49d7ddd01d5ef
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483838"
---
# <a name="copying-to-surfaces-direct3d-9"></a>Kopieren auf Oberflächen (Direct3D 9)

Wenn [**IDirect3DDevice9:: updatesurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface)verwendet wird, übergeben Sie ein Rechteck auf der Quell Oberfläche, oder verwenden Sie **null** , um die gesamte Oberfläche anzugeben. Außerdem übergeben Sie einen Punkt auf der Ziel Oberfläche, auf den die obere linke Position des Rechtecks im Quellbild kopiert wird. Diese Methode unterstützt kein Clipping. Der Vorgang schlägt fehl, es sei denn, das Quell Rechteck und das zugehörige Ziel Rechteck sind vollständig in den Quell-und Ziel Oberflächen enthalten. Diese Methode unterstützt keine Alpha Blending, Farbtasten oder Formatkonvertierung. Beachten Sie, dass sich die Ziel-und Quell Oberflächen unterscheiden müssen.

Weitere Einschränkungen bei der Verwendung von updatesurface finden Sie unter [**IDirect3DDevice9:: updatesurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface).

Die folgenden Methoden sind auch in C++/C zum Kopieren von Bildern auf eine Direct3D-Oberfläche verfügbar.

-   [**D3DXLoadSurfaceFromFile**](d3dxloadsurfacefromfile.md)
-   [**D3DXLoadSurfaceFromFileInMemory**](d3dxloadsurfacefromfileinmemory.md)
-   [**D3DXLoadSurfaceFromMemory**](d3dxloadsurfacefrommemory.md)
-   [**D3DXLoadSurfaceFromResource**](d3dxloadsurfacefromresource.md)
-   [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md)
-   [**IDirect3DDevice9:: updatesurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface)

## <a name="updatesurface-example"></a>Updatesurface-Beispiel

Im folgenden Beispiel werden zwei Rechtecke von der Quell Oberfläche auf eine Ziel Oberfläche kopiert. Das erste Rechteck wird von (0, 0, 50, 50) auf der Quell Oberfläche an denselben Speicherort auf der Ziel Oberfläche kopiert, und das zweite Rechteck wird von (50, 50, 100, 100) auf der Quell Oberfläche in (150, 150, 200, 200) auf der Ziel Oberfläche kopiert.


```
//The following assumptions are made:
// -d3dDevice is a valid Direct3DDevice9 object.
// -pSource and pDest are valid IDirect3DSurface9 pointers.

RECT  rcSource[] = {  0,  0,  50,  50,
                     50, 50, 100, 100 };
POINT ptDest[]   = {  0,  0, 150, 150 };

d3dDevice->UpdateSurface( pSource, rcSource, 2, pDest, ptDest);
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Oberflächen](direct3d-surfaces.md)
</dt> <dt>

[**IDirect3DDevice9:: stretchrect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect)
</dt> </dl>

 

 
