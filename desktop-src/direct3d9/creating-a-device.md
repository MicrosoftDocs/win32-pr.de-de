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
# <a name="creating-a-device-direct3d-9"></a><span data-ttu-id="fcf4e-103">Erstellen eines Geräts (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="fcf4e-103">Creating a Device (Direct3D 9)</span></span>

<span data-ttu-id="fcf4e-104">Um ein Direct3D-Gerät zu erstellen, erstellen Sie zuerst ein Direct3D-Objekt (siehe [**Direct3DCreate9**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9)).</span><span class="sxs-lookup"><span data-stu-id="fcf4e-104">To create a Direct3D device, first create a Direct3D object (see [**Direct3DCreate9**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9)).</span></span> <span data-ttu-id="fcf4e-105">Alle renderinggeräte, die von einem Direct3D-Objekt erstellt wurden, verwenden dieselben physischen Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="fcf4e-105">All rendering devices created by a Direct3D object share the same physical resources.</span></span> <span data-ttu-id="fcf4e-106">Wenn Sie mehrere renderinggeräte aus einem einzelnen Direct3D-Objekt erstellen, fallen extreme Leistungseinbußen an, da Sie dieselbe Hardware gemeinsam nutzen.</span><span class="sxs-lookup"><span data-stu-id="fcf4e-106">If you create multiple rendering devices from a single Direct3D object, extreme performance penalties will be incurred because they share the same hardware.</span></span>

<span data-ttu-id="fcf4e-107">Initialisieren Sie zunächst Werte für die [**D3DPRESENT \_ Parameters**](d3dpresent-parameters.md) -Struktur, die zum Erstellen des Direct3D-Geräts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fcf4e-107">First, initialize values for the [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md) structure that is used to create the Direct3D device.</span></span> <span data-ttu-id="fcf4e-108">Im folgenden Codebeispiel wird eine Anwendung angegeben, bei der der Hintergrund Puffer nur während eines vertikalen Synchronisierungs Vorgangs in den Vorder-Puffer kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="fcf4e-108">The following code example specifies a windowed application where the back buffer is copied to the front buffer during a vertical sync operation only.</span></span>


```
LPDIRECT3DDEVICE9 pDevice = NULL;

D3DPRESENT_PARAMETERS d3dpp; 

ZeroMemory( &d3dpp, sizeof(d3dpp) );
d3dpp.Windowed   = TRUE;
d3dpp.SwapEffect = D3DSWAPEFFECT_COPY;
```



<span data-ttu-id="fcf4e-109">Erstellen Sie als nächstes das Direct3D-Gerät.</span><span class="sxs-lookup"><span data-stu-id="fcf4e-109">Next, create the Direct3D device.</span></span> <span data-ttu-id="fcf4e-110">Der folgende [**IDirect3D9:: kreatedevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) -Befehl gibt den Standard Adapter, ein HAL-Gerät (Hardware Abstraktion Layer) und die Verarbeitung von Software Scheitel Punkten an.</span><span class="sxs-lookup"><span data-stu-id="fcf4e-110">The following [**IDirect3D9::CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) call specifies the default adapter, a hardware abstraction layer (HAL) device, and software vertex processing.</span></span>


```
if( FAILED( g_pD3D->CreateDevice( D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                                    D3DCREATE_SOFTWARE_VERTEXPROCESSING,
                                    &d3dpp, &d3dDevice ) ) )
    return E_FAIL;
```



<span data-ttu-id="fcf4e-111">Beachten Sie, dass ein Rückruf zum Erstellen, freigeben oder Zurücksetzen des Geräts nur im gleichen Thread wie die Fenster Prozedur des Fokus Fensters erfolgen sollte.</span><span class="sxs-lookup"><span data-stu-id="fcf4e-111">Note that a call to create, release, or reset the device should happen only on the same thread as the window procedure of the focus window.</span></span>

<span data-ttu-id="fcf4e-112">Nachdem Sie das Gerät erstellt haben, legen Sie seinen Status fest.</span><span class="sxs-lookup"><span data-stu-id="fcf4e-112">After creating the device, set its state.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fcf4e-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fcf4e-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fcf4e-114">Direct3D-Geräte</span><span class="sxs-lookup"><span data-stu-id="fcf4e-114">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 
