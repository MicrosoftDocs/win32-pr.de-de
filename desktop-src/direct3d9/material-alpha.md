---
description: Alpha kann auch in einem Material angegeben werden. Um material alpha zu aktivieren, legen Sie den Renderzustand des diffusen Materials so fest, dass die Laufzeit die materialen diffusen Farbkomponenten anstelle der diffusen Vertexfarbkomponenten verwendet.
ms.assetid: fd477d8f-d838-4a08-a8c6-38678798e0b0
title: Material Alpha (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a70ed4a3f5bcaf38f4ace079af5b2e1804af0e24340e5004898c9ed26707d40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118798977"
---
# <a name="material-alpha-direct3d-9"></a>Material Alpha (Direct3D 9)

Alpha kann auch in einem Material angegeben werden. Um material alpha zu aktivieren, legen Sie den Renderzustand des diffusen Materials so fest, dass die Laufzeit die materialen diffusen Farbkomponenten anstelle der diffusen Vertexfarbkomponenten verwendet.


```
m_pd3dDevice->SetRenderState( D3DRS_DIFFUSEMATERIALSOURCE, D3DMCS_MATERIAL );
```



Initialisieren Sie das Material mit einem Alphawert, und legen Sie das Material vor dem Zeichnen fest.


```
D3DMATERIAL9 mtrl;
mtrl.Diffuse = mtrl.Ambient = mtrl.Specular = mtrl.Emissive = 
    D3DCOLORVALUE(255,0,0,0.5f)

m_pd3dDevice->SetMaterial(&mtrl);     
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Alphablending](alpha-blending.md)
</dt> </dl>

 

 



