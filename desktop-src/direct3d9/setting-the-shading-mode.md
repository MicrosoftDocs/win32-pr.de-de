---
description: Direct3D ermöglicht die Auswahl eines Schattierungs Modus gleichzeitig.
ms.assetid: 9531947d-4cd8-43c3-8825-4c48a0d69395
title: Festlegen des Schattierungs Modus (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62f93d79e4507d9e9d08569e5cbd75bb8b42aa4f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482083"
---
# <a name="setting-the-shading-mode-direct3d-9"></a><span data-ttu-id="e5462-103">Festlegen des Schattierungs Modus (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e5462-103">Setting the Shading Mode (Direct3D 9)</span></span>

<span data-ttu-id="e5462-104">Direct3D ermöglicht die Auswahl eines Schattierungs Modus gleichzeitig.</span><span class="sxs-lookup"><span data-stu-id="e5462-104">Direct3D enables one shading mode to be selected at a time.</span></span> <span data-ttu-id="e5462-105">Standardmäßig ist die Option "Gouraud-Schattierung" ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="e5462-105">By default, Gouraud shading is selected.</span></span> <span data-ttu-id="e5462-106">In C++ können Sie den Schattierungs Modus ändern, indem Sie die Methode [**IDirect3DDevice9:: settrenderstate**](/windows/desktop/api) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e5462-106">In C++, you can change the shading mode by calling the [**IDirect3DDevice9::SetRenderState**](/windows/desktop/api) method.</span></span> <span data-ttu-id="e5462-107">Legen Sie den *State* -Parameter auf D3DRS \_ SHADEMODE fest.</span><span class="sxs-lookup"><span data-stu-id="e5462-107">Set the *State* parameter to D3DRS\_SHADEMODE.</span></span> <span data-ttu-id="e5462-108">Der *State* -Parameter muss auf einen Member der [**D3DSHADEMODE**](./d3dshademode.md) -Enumeration festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e5462-108">The *State* parameter must be set to a member of the [**D3DSHADEMODE**](./d3dshademode.md) enumeration.</span></span> <span data-ttu-id="e5462-109">Die folgenden Beispielcode Beispiele veranschaulichen, wie der aktuelle Schattierungs Modus einer Direct3D-Anwendung auf den flachen oder den Gouraud-Schattierungs Modus festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="e5462-109">The following sample code examples illustrate how the current shading mode of a Direct3D application can be set to flat or Gouraud shading mode.</span></span>


```
// Set to flat shading.
// This code example assumes that pDev is a valid pointer to 
// an IDirect3DDevice9 interface.
hr = pDev->SetRenderState(D3DRS_SHADEMODE, D3DSHADE_FLAT);
if(FAILED(hr))
{
    // Code to handle the error goes here.
}

// Set to Gouraud shading. This is the default for Direct3D.
hr = pDev->SetRenderState(D3DRS_SHADEMODE,
                            D3DSHADE_GOURAUD);
if(FAILED(hr))
{
    // Code to handle the error goes here.
}
```



## <a name="related-topics"></a><span data-ttu-id="e5462-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e5462-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5462-111">Schattierung</span><span class="sxs-lookup"><span data-stu-id="e5462-111">Shading</span></span>](shading.md)
</dt> </dl>

 

 
