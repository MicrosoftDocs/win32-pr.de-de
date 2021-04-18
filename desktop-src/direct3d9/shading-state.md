---
description: Direct3D unterstützt sowohl Flat-als auch Gouraud-Schattierung. Der Standardwert ist Gouraud-Schattierung. Um den aktuellen Schattierungs Modus zu steuern, gibt Ihre C++-Anwendung einen Member des D3DSHADEMODE-Enumerationstyps für den D3DRS \_ shdemode-renderzustand an.
ms.assetid: 0019b1b7-65f2-4009-8d0f-5a99cf32a410
title: Schattierungs Zustand (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ebac826704fee0e1903c1aa2a2348bff4a089c2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344169"
---
# <a name="shading-state-direct3d-9"></a>Schattierungs Zustand (Direct3D 9)

Direct3D unterstützt sowohl Flat-als auch Gouraud-Schattierung. Der Standardwert ist Gouraud-Schattierung. Um den aktuellen Schattierungs Modus zu steuern, gibt Ihre C++-Anwendung einen Member des [**D3DSHADEMODE**](./d3dshademode.md) -Enumerationstyps für den D3DRS \_ shdemode-renderzustand an.

Im folgenden C++-Codebeispiel wird veranschaulicht, wie der Schattierungs Zustand auf den flachen Schattierungs Modus festgelegt wird.


```
// This code example assumes that d3dDevice is a
// valid pointer to a IDirect3DDevice9 interface.
// Set the shading state.
d3dDevice->SetRenderState(D3DRS_SHADEMODE, D3DSHADE_FLAT);
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rendering-Zustände](render-states.md)
</dt> </dl>

 

 
