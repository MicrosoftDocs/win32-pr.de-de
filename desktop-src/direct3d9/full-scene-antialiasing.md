---
description: Das Vollbild-Antialiasing bezieht sich auf das Verwischen der Kanten der einzelnen Polygon in der Szene, wenn es in einem einzigen Durchlauf gerragt wird. Es ist kein zweiter Durchlauf erforderlich.
ms.assetid: b57974ab-5654-412d-ae59-58f67a88c121
title: Full-Scene Antialiasing (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d73d559c4b4fec060efbff7468ee29e6c83b64c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520912"
---
# <a name="full-scene-antialiasing-direct3d-9"></a>Full-Scene Antialiasing (Direct3D 9)

Das Vollbild-Antialiasing bezieht sich auf das Verwischen der Kanten der einzelnen Polygon in der Szene, wenn es in einem einzigen Durchlauf gerragt wird. Es ist kein zweiter Durchlauf erforderlich. Das Vollbild-Antialiasing wirkt sich bei Unterstützung nur auf Dreiecke und Gruppen von Dreiecken aus. Zeilen können nicht mithilfe von Direct3D Services als Antialiasing verwendet werden. Das Vollbild-Antialiasing erfolgt in Direct3D mithilfe von multisamplinggrad auf den einzelnen Pixeln. Wenn die multisamplinggrad-Funktion aktiviert ist, werden alle Teil Beispiele eines Pixels in einem Durchlauf aktualisiert. Wenn Sie jedoch für andere Effekte verwendet werden, die mehrere Renderingdurchläufen einschließen, kann die Anwendung angeben, dass nur einige unter Beispiele von einem gegebenen Renderingdurchlauf betroffen sein sollen. Mit diesem letzteren Ansatz wird die Simulation von Bewegungsunschärfe, tiefen Fokus Effekten, reflektionstypen usw. ermöglicht.

In beiden Fällen werden die verschiedenen für jedes Pixel aufgezeichneten Beispiele kombiniert und auf dem Bildschirm ausgegeben. Dies ermöglicht die verbesserte Bildqualität von Antialiasing oder anderen Effekten.

Vor dem Erstellen eines Geräts mit der [**IDirect3D9:: kreatedevice**](/windows/desktop/api) -Methode müssen Sie bestimmen, ob das Vollbild-Antialiasing unterstützt wird. Rufen Sie dazu die [**IDirect3D9:: checkdevicemultisampletype**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) -Methode auf, wie im folgenden Codebeispiel gezeigt.


```
/*
* The code below assumes that pD3D is a valid pointer 
*   to a IDirect3D9 interface.
*/

if( SUCCEEDED(pD3D->CheckDeviceMultiSampleType( D3DADAPTER_DEFAULT, 
                    D3DDEVTYPE_HAL , D3DFMT_R8G8B8, FALSE, 
                    D3DMULTISAMPLE_2_SAMPLES, NULL ) ) )
// Full-scene antialiasing is supported. Enable it here.
```



Der erste Parameter, den [**IDirect3D9:: checkdevicemultisampletype**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) annimmt, ist eine Ordinalzahl, die den abzufragenden Anzeige Adapter angibt. In diesem Beispiel wird D3DADAPTER \_ default verwendet, um den primären Anzeige Adapter anzugeben. Der zweite Parameter ist ein Wert aus dem [**D3DDEVTYPE**](./d3ddevtype.md) -Enumerationstyp, der den Gerätetyp angibt. Der dritte Parameter gibt das Format der-Oberfläche an. Der vierte Parameter gibt Direct3D an, ob die multisamplinggrad-Funktion (**true**) oder das Vollbild-Antialiasing (**false**) vollständig im Fenster beschrieben wird. In diesem Beispiel wird **false** verwendet, um Direct3D zu sagen, dass es sich um das Antialiasing in der vollständigen Szene handelt. Der letzte Parameter gibt die multisamplinggrad-Methode an, die Sie testen möchten. Verwenden Sie einen Wert aus dem enumerierten Typ [**D3DMULTISAMPLE \_ Type**](./d3dmultisample-type.md) . In diesem Beispiel wird getestet, ob zwei Ebenen von multisamplinggrad unterstützt werden.

Wenn das Gerät die gewünschte multisamplinggrad-Ebene unterstützt, besteht der nächste Schritt darin, die Präsentations Parameter festzulegen, indem die entsprechenden Member der [**D3DPRESENT \_ Parameters**](d3dpresent-parameters.md) -Struktur ausgefüllt werden, um eine Multisampling-Renderingoberfläche zu erstellen. Danach können Sie das Gerät erstellen. Der folgende Beispielcode zeigt, wie Sie ein Gerät mit einer multisamplinggrad-Renderoberfläche einrichten.


```
/*
* The example below assumes that pD3D is a valid pointer 
* to a IDirect3D9 interface, d3dDevice is a pointer to a 
* IDirect3DDevice9 interface, and hWnd is a valid handle
* to a window.
*/

D3DPRESENT_PARAMETER d3dPP
ZeroMemory( &d3dPP, sizeof( d3dPP ) );
d3dPP.Windowed        = FALSE
d3dPP.SwapEffect      = D3DSWAPEFFECT_DISCARD;
d3dPP.MultiSampleType = D3DMULTISAMPLE_2_SAMPLES;
pD3D->CreateDevice(D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                    D3DCREATE_SOFTWARE_VERTEXPROCESSING,
                    &d3dpp, &d3dDevice)
```



Zum Verwenden von Multisampling muss das Member-Element von "D3DPRESENT" \_ auf "D3DSWAPEFFECT verwerfen" festgelegt werden \_ .

Der letzte Schritt besteht darin, das multisamplinggrad-Antialiasing zu aktivieren, indem die [**IDirect3DDevice9:: btrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) -Methode aufgerufen und der D3DRS \_ multisampleantialias auf **true** festgelegt wird. Nachdem Sie diesen Wert auf " **true**" festgelegt haben, wird für jedes Rendering, das Sie ausführen, eine multisamplinggrad-Funktion angewendet. Je nachdem, was Sie rendern, empfiehlt es sich, Multisampling zu aktivieren und zu deaktivieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Antialiasing](antialiasing.md)
</dt> </dl>

 

 
