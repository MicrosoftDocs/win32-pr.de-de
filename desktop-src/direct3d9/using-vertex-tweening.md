---
description: Um zu ermitteln, ob Direct3D die Vertex-Tweening unterstützt, suchen Sie \_ im VertexProcessingCaps-Member der D3DCAPS9-Struktur nach dem D3DVTXPCAPS-TWEENING-Flag.
ms.assetid: b60c7f96-3752-4703-9059-486d9906c508
title: Verwenden von Vertex-Tweening (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14c4d2da3f32698cc24e052a152b674ecb023f79e90541af23374c0903d54d55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118797088"
---
# <a name="using-vertex-tweening-direct3d-9"></a>Verwenden von Vertex-Tweening (Direct3D 9)

Um zu ermitteln, ob Direct3D die Vertex-Tweening unterstützt, suchen Sie \_ im VertexProcessingCaps-Member der [**D3DCAPS9-Struktur nach dem D3DVTXPCAPS-TWEENING-Flag.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) Im folgenden Codebeispiel wird die [**IDirect3DDevice9::GetDeviceCaps-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) verwendet, um zu bestimmen, ob Tweening unterstützt wird.


```
// This example assumes that m_pD3DDevice is 
// a valid pointer to a IDirect3DDevice9 interface.
//
D3DCAPS9 d3dCaps;

m_pD3DDevice->GetDeviceCaps( &d3dCaps );
if( 0 != (d3dCaps.VertexProcessingCaps & D3DVTXPCAPS_TWEENING) )
    // Vertex tweening is supported.
```



Um Vektor-Tweening zu verwenden, müssen Sie zunächst einen benutzerdefinierten Scheitelpunkttyp einrichten, der eine zweite normale oder eine zweite Position verwendet. Das folgende Codebeispiel zeigt eine Beispieldeklaration, die sowohl einen zweiten Punkt als auch eine zweite Position enthält.


```
struct TEX_VERTEX
{
    D3DVECTOR position;
    D3DVECTOR normal;
    D3DVECTOR position2;
    D3DVECTOR normal2;
};

//Create a vertex buffer with the type TEX_VERTEX.
```



Im nächsten Schritt wird die aktuelle Deklaration festgelegt. Das folgende Codebeispiel zeigt, wie dies funktioniert.


```
// Create the shader declaration.
D3DVERTEXELEMENT9 decl[] = 
{
    { 0, 0,  D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0 },
    { 0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL, 0 },
    { 0, 24, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 1 },
    { 0, 36, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL, 1 },
    D3DDECL_END()
};
```



Weitere Informationen zum Erstellen eines benutzerdefinierten Scheitelpunkttyps und eines Scheitelpunktpuffers finden Sie unter [Erstellen eines Scheitelpunktpuffers (Direct3D 9).](creating-a-vertex-buffer.md)

> [!Note]  
> Wenn vertex tweening aktiviert ist, muss eine zweite Position oder eine zweite Normalität in der aktuellen Deklaration vorhanden sein.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Tweening](vertex-tweening.md)
</dt> </dl>

 

 
