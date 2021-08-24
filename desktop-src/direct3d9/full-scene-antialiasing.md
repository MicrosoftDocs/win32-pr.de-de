---
description: Antialiasing für vollständige Szenen bezieht sich auf das Verwischen der Ränder jedes Polygons in der Szene, während es in einem einzigen Durchlauf gerastert wird. Es ist kein zweiter Durchlauf erforderlich.
ms.assetid: b57974ab-5654-412d-ae59-58f67a88c121
title: Full-Scene Antialiasing (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3fdeab18997db57ed1391af97f40f1500e7c326411019ddcb42453e4a68cc7e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893990"
---
# <a name="full-scene-antialiasing-direct3d-9"></a>Full-Scene Antialiasing (Direct3D 9)

Antialiasing für vollständige Szenen bezieht sich auf das Verwischen der Ränder jedes Polygons in der Szene, während es in einem einzigen Durchlauf gerastert wird. Es ist kein zweiter Durchlauf erforderlich. Das Antialiasing der vollständigen Szene wirkt sich, sofern unterstützt, nur auf Dreiecke und Gruppen von Dreiecken aus. Zeilen können nicht mithilfe von Direct3D-Diensten antialiasiert werden. Das Antialiasing der vollständigen Szene erfolgt in Direct3D mithilfe von Multisampling auf jedem Pixel. Wenn Multisampling aktiviert ist, werden alle Untersamples eines Pixels in einem Durchlauf aktualisiert. Wenn sie jedoch für andere Effekte mit mehreren Renderingdurchläufen verwendet wird, kann die Anwendung angeben, dass nur einige Untersamples von einem bestimmten Renderingdurchlauf betroffen sein sollen. Dieser zweite Ansatz ermöglicht die Simulation von Bewegungsunschärfe, Tiefenfokuseffekten, Reflektionsunschärfe usw.

In beiden Fällen werden die verschiedenen aufgezeichneten Stichproben für jedes Pixel kombiniert und auf dem Bildschirm ausgegeben. Dies ermöglicht die verbesserte Bildqualität von Antialiasing oder anderen Effekten.

Vor dem Erstellen eines Geräts mit der [**IDirect3D9::CreateDevice-Methode**](/windows/desktop/api) müssen Sie ermitteln, ob Antialiasing für vollständige Szenen unterstützt wird. Rufen Sie hierzu die [**IDirect3D9::CheckDeviceMultiSampleType-Methode**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) auf, wie im folgenden Codebeispiel gezeigt.


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



Der erste Parameter, den [**IDirect3D9::CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) akzeptiert, ist eine Ordnungszahl, die den abzufragenden Anzeigeadapter bezeichnet. In diesem Beispiel wird D3DADAPTER \_ DEFAULT verwendet, um den primären Anzeigeadapter anzugeben. Der zweite Parameter ist ein Wert aus dem [**D3DDEVTYPE-Enumerationstyp,**](./d3ddevtype.md) der den Gerätetyp angibt. Der dritte Parameter gibt das Format der Oberfläche an. Der vierte Parameter teilt Direct3D mit, ob bei Vollfenster-Multisampling **(TRUE)** oder bei Antialiasing für vollständige Szenen (**FALSE)** abgefragt werden soll. In diesem Beispiel wird **FALSE** verwendet, um Direct3D mitzuteilen, dass es sich um Antialiasing für vollständige Szenen handelt. Der letzte Parameter gibt die Multisampling-Technik an, die Sie testen möchten. Verwenden Sie einen Wert aus dem [**D3DMULTISAMPLE \_ TYPE-Enumerationstyp.**](./d3dmultisample-type.md) In diesem Beispiel wird getestet, ob zwei Multisamplingebenen unterstützt werden.

Wenn das Gerät die Multisamplingebene unterstützt, die Sie verwenden möchten, besteht der nächste Schritt darin, die Präsentationsparameter festzulegen, indem die entsprechenden Member der [**D3DPRESENT \_ PARAMETERS-Struktur**](d3dpresent-parameters.md) ausgefüllt werden, um eine Multisample-Renderingoberfläche zu erstellen. Danach können Sie das Gerät erstellen. Der folgende Beispielcode zeigt, wie Sie ein Gerät mit einer Multisampling-Renderoberfläche einrichten.


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



Um Multisampling zu verwenden, muss der SwapEffect-Member von D3DPRESENT \_ PARAMETER auf D3DSWAPEFFECT DISCARD festgelegt \_ werden.

Der letzte Schritt besteht darin, Multisampling-Antialiasing zu aktivieren, indem die [**IDirect3DDevice9::SetRenderState-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) aufgerufen und D3DRS \_ MULTISAMPLEANTIALIAS auf **TRUE** festgelegt wird. Nachdem Sie diesen Wert auf **TRUE** festgelegt haben, wird auf jedes Rendering, das Sie durchführen, Multisampling angewendet. Je nachdem, was Sie rendern, sollten Sie Multisampling aktivieren und deaktivieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Antialiasing](antialiasing.md)
</dt> </dl>

 

 
