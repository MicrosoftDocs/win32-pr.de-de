---
description: Um ein Direct3D-Gerät zu erstellen, erstellen Sie zuerst ein Direct3D-Objekt (siehe Direct3DCreate9).
ms.assetid: 06810f31-fa6c-416e-bd7b-65cfb3e6d7f2
title: Erstellen eines Geräts (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a9c033ed25262f0a3bcdee9db73509ddf5cb53b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340108"
---
# <a name="creating-a-device-direct3d-9"></a>Erstellen eines Geräts (Direct3D 9)

Um ein Direct3D-Gerät zu erstellen, erstellen Sie zuerst ein Direct3D-Objekt (siehe [**Direct3DCreate9**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9)). Alle renderinggeräte, die von einem Direct3D-Objekt erstellt wurden, verwenden dieselben physischen Ressourcen. Wenn Sie mehrere renderinggeräte aus einem einzelnen Direct3D-Objekt erstellen, fallen extreme Leistungseinbußen an, da Sie dieselbe Hardware gemeinsam nutzen.

Initialisieren Sie zunächst Werte für die [**D3DPRESENT \_ Parameters**](d3dpresent-parameters.md) -Struktur, die zum Erstellen des Direct3D-Geräts verwendet wird. Im folgenden Codebeispiel wird eine Anwendung angegeben, bei der der Hintergrund Puffer nur während eines vertikalen Synchronisierungs Vorgangs in den Vorder-Puffer kopiert wird.


```
LPDIRECT3DDEVICE9 pDevice = NULL;

D3DPRESENT_PARAMETERS d3dpp; 

ZeroMemory( &d3dpp, sizeof(d3dpp) );
d3dpp.Windowed   = TRUE;
d3dpp.SwapEffect = D3DSWAPEFFECT_COPY;
```



Erstellen Sie als nächstes das Direct3D-Gerät. Der folgende [**IDirect3D9:: kreatedevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) -Befehl gibt den Standard Adapter, ein HAL-Gerät (Hardware Abstraktion Layer) und die Verarbeitung von Software Scheitel Punkten an.


```
if( FAILED( g_pD3D->CreateDevice( D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                                    D3DCREATE_SOFTWARE_VERTEXPROCESSING,
                                    &d3dpp, &d3dDevice ) ) )
    return E_FAIL;
```



Beachten Sie, dass ein Rückruf zum Erstellen, freigeben oder Zurücksetzen des Geräts nur im gleichen Thread wie die Fenster Prozedur des Fokus Fensters erfolgen sollte.

Nachdem Sie das Gerät erstellt haben, legen Sie seinen Status fest.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Geräte](direct3d-devices.md)
</dt> </dl>

 

 
