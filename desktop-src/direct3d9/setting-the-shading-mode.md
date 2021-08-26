---
description: Direct3D ermöglicht die gleichzeitige Auswahl eines Schattierungsmodus.
ms.assetid: 9531947d-4cd8-43c3-8825-4c48a0d69395
title: Festlegen des Schattierungsmodus (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 769908513d4388fafae73f5a6788aef37c3ac9456a00f2e3280c57e04c18b462
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068960"
---
# <a name="setting-the-shading-mode-direct3d-9"></a>Festlegen des Schattierungsmodus (Direct3D 9)

Direct3D ermöglicht die gleichzeitige Auswahl eines Schattierungsmodus. Standardmäßig ist Die Gouraud-Schattierung ausgewählt. In C++ können Sie den Schattierungsmodus ändern, indem Sie die [**IDirect3DDevice9::SetRenderState-Methode**](/windows/desktop/api) aufrufen. Legen Sie den *State-Parameter* auf D3DRS \_ SHADEMODE fest. Der *State-Parameter* muss auf einen Member der [**D3DSHADEMODE-Enumeration**](./d3dshademode.md) festgelegt werden. Die folgenden Beispielcodebeispiele veranschaulichen, wie der aktuelle Schattierungsmodus einer Direct3D-Anwendung auf den Schattierungsmodus "Flat" oder "Gouraud" festgelegt werden kann.


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

 

 
