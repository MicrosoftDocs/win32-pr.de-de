---
description: Umgebungslicht ist umgebendes Licht, das aus allen Richtungen lichtet. Informationen dazu, wie Direct3D Umgebungslicht verwendet, finden Sie unter Mathematik der Beleuchtung (Direct3D 9).
ms.assetid: c5aa493e-09b8-433c-a21c-e39af795b3c9
title: Umgebungslichtzustand (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc32a6ec654bd30627c853bc00c90e94b6008e769fb3aa708e963a9430e0dc85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952690"
---
# <a name="ambient-lighting-state-direct3d-9"></a>Umgebungslichtzustand (Direct3D 9)

Umgebungslicht ist umgebendes Licht, das aus allen Richtungen lichtet. Informationen dazu, wie Direct3D Umgebungslicht verwendet, finden Sie unter [Mathematik der Beleuchtung (Direct3D 9).](mathematics-of-lighting.md)

Eine C++-Anwendung legt die Farbe der Umgebungsbeleuchtung fest, indem sie die [**IDirect3DDevice9::SetRenderState-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) aufruft und den enumerationsierten Wert D3DRS \_ AMBIENT als ersten Parameter übergibt. Der zweite Parameter ist ein Farbwert. Der Standardwert ist 0 (null).


```
// This code example assumes that d3dDevice is a
// valid pointer to an IDirect3DDevice9 interface.

// Set the ambient light.

d3dDevice->SetRenderState(D3DRS_AMBIENT, 0x00202020);
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Renderzustände](render-states.md)
</dt> </dl>

 

 
