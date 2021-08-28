---
description: Direct3D unterstützt sowohl flache als auch Gouraud-Schattierung. Der Standardwert ist Gouraud shading. Um den aktuellen Schattierungsmodus zu steuern, gibt Ihre C++-Anwendung einen Member des D3DSHADEMODE-Enumerationstyps für den D3DRS \_ SHADEMODE-Renderzustand an.
ms.assetid: 0019b1b7-65f2-4009-8d0f-5a99cf32a410
title: Schattierungsstatus (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f28514fefbf39e75bd84a0ae56324fd859f0fd85fa4a25449e349ce592ab3b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119727600"
---
# <a name="shading-state-direct3d-9"></a>Schattierungsstatus (Direct3D 9)

Direct3D unterstützt sowohl flache als auch Gouraud-Schattierung. Der Standardwert ist Gouraud shading. Um den aktuellen Schattierungsmodus zu steuern, gibt Ihre C++-Anwendung einen Member des [**D3DSHADEMODE-Enumerationstyps**](./d3dshademode.md) für den D3DRS \_ SHADEMODE-Renderzustand an.

Im folgenden C++-Codebeispiel wird das Festlegen des Schattierungszustands auf den Flachschattierungsmodus veranschaulicht.


```
// This code example assumes that d3dDevice is a
// valid pointer to a IDirect3DDevice9 interface.
// Set the shading state.
d3dDevice->SetRenderState(D3DRS_SHADEMODE, D3DSHADE_FLAT);
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Renderzustände](render-states.md)
</dt> </dl>

 

 
