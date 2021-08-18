---
description: Wenn Sie IDirect3DDevice9::UpdateSurface verwenden, übergeben Sie ein Rechteck auf der Quelloberfläche, oder verwenden Sie NULL, um die gesamte Oberfläche anzugeben.
ms.assetid: 2219d037-8480-4c36-b04e-0c23406a2e7e
title: Kopieren auf Oberflächen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e28a8518f0792948af7aabda269fffe9679de2c6fc704ee93e2cf05381176b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989290"
---
# <a name="copying-to-surfaces-direct3d-9"></a>Kopieren auf Oberflächen (Direct3D 9)

Wenn [**Sie IDirect3DDevice9::UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface)verwenden, übergeben Sie ein Rechteck auf der Quelloberfläche, oder verwenden Sie **NULL,** um die gesamte Oberfläche anzugeben. Außerdem übergeben Sie einen Punkt auf der Zieloberfläche, an den die obere linke Position des Rechtecks auf dem Quellbild kopiert wird. Diese Methode unterstützt kein Clipping. Der Vorgang schlägt fehl, es sei denn, das Quellrechteck und das entsprechende Zielrechteck sind vollständig in der Quell- bzw. Zieloberfläche enthalten. Diese Methode unterstützt keine Alphamischung, Farbschlüssel oder Formatkonvertierung. Beachten Sie, dass die Ziel- und Quelloberflächen unterschiedlich sein müssen.

Weitere Einschränkungen bei der Verwendung von UpdateSurface finden Sie unter [**IDirect3DDevice9::UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface).

Die folgenden Methoden sind auch in C++/C zum Kopieren von Bildern auf eine Direct3D-Oberfläche verfügbar.

-   [**D3DXLoadSurfaceFromFile**](d3dxloadsurfacefromfile.md)
-   [**D3DXLoadSurfaceFromFileInMemory**](d3dxloadsurfacefromfileinmemory.md)
-   [**D3DXLoadSurfaceFromMemory**](d3dxloadsurfacefrommemory.md)
-   [**D3DXLoadSurfaceFromResource**](d3dxloadsurfacefromresource.md)
-   [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md)
-   [**IDirect3DDevice9::UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface)

## <a name="updatesurface-example"></a>UpdateSurface-Beispiel

Im folgenden Beispiel werden zwei Rechtecke von der Quelloberfläche in eine Zieloberfläche kopiert. Das erste Rechteck wird von (0, 0, 50, 50) auf der Quelloberfläche an die gleiche Position auf der Zieloberfläche kopiert, und das zweite Rechteck wird von (50, 50, 100, 100) auf der Quelloberfläche in (150, 150, 200, 200) auf der Zieloberfläche kopiert.


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

[**IDirect3DDevice9::StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect)
</dt> </dl>

 

 
