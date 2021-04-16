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
# <a name="setting-the-shading-mode-direct3d-9"></a>Festlegen des Schattierungs Modus (Direct3D 9)

Direct3D ermöglicht die Auswahl eines Schattierungs Modus gleichzeitig. Standardmäßig ist die Option "Gouraud-Schattierung" ausgewählt. In C++ können Sie den Schattierungs Modus ändern, indem Sie die Methode [**IDirect3DDevice9:: settrenderstate**](/windows/desktop/api) aufrufen. Legen Sie den *State* -Parameter auf D3DRS \_ SHADEMODE fest. Der *State* -Parameter muss auf einen Member der [**D3DSHADEMODE**](./d3dshademode.md) -Enumeration festgelegt werden. Die folgenden Beispielcode Beispiele veranschaulichen, wie der aktuelle Schattierungs Modus einer Direct3D-Anwendung auf den flachen oder den Gouraud-Schattierungs Modus festgelegt werden kann.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schattierung](shading.md)
</dt> </dl>

 

 
