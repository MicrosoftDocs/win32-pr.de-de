---
description: Um zu ermitteln, ob Direct3D die vertextwiening unterstützt, überprüfen Sie das D3DVTXPCAPS \_ Tweening-Flag im VertexProcessingCaps-Member der D3DCAPS9-Struktur.
ms.assetid: b60c7f96-3752-4703-9059-486d9906c508
title: Verwenden von Vertex-Tweening (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12ca56cc521b5bff01a5d6af5c2d4ab6b02cd49e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860191"
---
# <a name="using-vertex-tweening-direct3d-9"></a>Verwenden von Vertex-Tweening (Direct3D 9)

Um zu ermitteln, ob Direct3D die vertextwiening unterstützt, überprüfen Sie das D3DVTXPCAPS \_ Tweening-Flag im VertexProcessingCaps-Member der [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) -Struktur. Im folgenden Codebeispiel wird die [**IDirect3DDevice9:: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) -Methode verwendet, um zu bestimmen, ob das twiening unterstützt wird.


```
// This example assumes that m_pD3DDevice is 
// a valid pointer to a IDirect3DDevice9 interface.
//
D3DCAPS9 d3dCaps;

m_pD3DDevice->GetDeviceCaps( &d3dCaps );
if( 0 != (d3dCaps.VertexProcessingCaps & D3DVTXPCAPS_TWEENING) )
    // Vertex tweening is supported.
```



Um Vector Tweening verwenden zu können, müssen Sie zuerst einen benutzerdefinierten vertextyp einrichten, der eine zweite normale oder eine zweite Position verwendet. Das folgende Codebeispiel zeigt eine Beispiel Deklaration, die einen zweiten Punkt und eine zweite Position enthält.


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



Der nächste Schritt besteht darin, die aktuelle Deklaration festzulegen. Das folgende Codebeispiel zeigt, wie Sie dies tun.


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



Weitere Informationen zum Erstellen eines benutzerdefinierten Scheitelpunkt Typs und eines Scheitelpunkt Puffers finden Sie unter [Erstellen eines Scheitelpunkt Puffers (Direct3D 9)](creating-a-vertex-buffer.md).

> [!Note]  
> Wenn die Vertex-Tweening aktiviert ist, muss in der aktuellen Deklaration eine zweite Position oder eine zweite normale Position vorhanden sein.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Tweening](vertex-tweening.md)
</dt> </dl>

 

 
