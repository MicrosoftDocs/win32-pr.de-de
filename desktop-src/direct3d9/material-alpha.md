---
description: Alpha kann auch in einem Material bereitgestellt werden. Legen Sie zum Aktivieren von Material Alpha den Rendering-Zustand des diffusen Materials so fest, dass die Common Language Runtime anstelle der vertexdiffusen Farbkomponenten die Komponenten der diffusen Farben verwendet.
ms.assetid: fd477d8f-d838-4a08-a8c6-38678798e0b0
title: Material Alpha (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f07ac2c28b497167f7bd742ecd8176b82b61e8f8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123338"
---
# <a name="material-alpha-direct3d-9"></a>Material Alpha (Direct3D 9)

Alpha kann auch in einem Material bereitgestellt werden. Legen Sie zum Aktivieren von Material Alpha den Rendering-Zustand des diffusen Materials so fest, dass die Common Language Runtime anstelle der vertexdiffusen Farbkomponenten die Komponenten der diffusen Farben verwendet.


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

[Alpha Blending](alpha-blending.md)
</dt> </dl>

 

 



