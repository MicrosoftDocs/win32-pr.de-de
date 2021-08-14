---
description: Die Transformationszustände 256-511 sind für die Speicherung von bis zu 256 Matrizen reserviert, die mithilfe von 8-Bit-Indizes indiziert werden können.
ms.assetid: 4c15cfc5-afdf-48d4-8fd1-b10cbe596a1c
title: Verwenden von indizierter Vertexmischung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a2d14e66fd934e2eaa8b403d694d203edddb229aab0795fa4a396b8baf367ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118519475"
---
# <a name="using-indexed-vertex-blending-direct3d-9"></a>Verwenden von indizierter Vertexmischung (Direct3D 9)

Die Transformationszustände 256-511 sind für die Speicherung von bis zu 256 Matrizen reserviert, die mithilfe von 8-Bit-Indizes indiziert werden können. Verwenden Sie das [**Makro D3DTS \_ WORLDMATRIX,**](d3dts-worldmatrix.md) um die Indizes 0-255 den entsprechenden Transformationszuständen zu zuordnen. Das folgende Codebeispiel zeigt, wie sie die [**IDirect3DDevice9::SetTransform-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) verwendet, um die Matrix bei der Transformationszustandsnummer 256 auf eine Identitätsmatrix zu setzen.


```
D3DMATRIX matBlend1;
D3DXMatrixIdentity( &matBlend1 );
m_pD3DDevice->SetTransform( D3DTS_WORLDMATRIX(0), &matBlend );
```



Um indiziertes Vertexblending zu aktivieren oder zu deaktivieren, legen Sie den D3DRS \_ INDEXEDVERTEXBLENDENABLE-Renderzustand auf **TRUE fest.** Wenn der Renderzustand aktiviert ist, müssen Sie Matrixindizes als gepackte DWORDs mit jedem Scheitelpunkt übergeben. Wenn dieser Renderzustand deaktiviert und vertex blending aktiviert ist, entspricht dies den Matrixindizes 0, 1, 2 und 3 in jedem Scheitelpunkt. Im folgenden Codebeispiel wird die [**IDirect3DDevice9::SetRenderState-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) verwendet, um indiziertes Vertexblending zu aktivieren.


```
m_pD3DDevice->SetRenderState( D3DRS_INDEXEDVERTEXBLENDENABLE, TRUE );
```



Um vertex blending zu aktivieren oder zu deaktivieren, legen Sie den [**Renderzustand IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) auf einen anderen Wert als D3DRS DISABLE aus dem \_ aufzählten [**D3DVERTEXBLENDFLAGS-Typ**](./d3dvertexblendflags.md) fest. Wenn dieser Renderzustand nicht auf D3DRS DISABLE festgelegt ist, müssen Sie die erforderliche Anzahl von Gewichtungen für \_ jeden Scheitelpunkt übergeben. Im folgenden Codebeispiel wird **IDirect3DDevice9::SetRenderState** verwendet, um vertex blending mit drei Gewichtungen für jeden Scheitelpunkt zu aktivieren.


```
m_pD3DDevice->SetRenderState( D3DRS_VERTEXBLEND, D3DVBF_3WEIGHTS );
```



## <a name="determining-indexed-vertex-blending-support"></a>Bestimmen der Unterstützung für indiziertes Scheitelpunktblending

Um die maximale Größe für die indizierte Vertexmischungsmatrix zu bestimmen, überprüfen Sie das MaxVertexBlendMatrixIndex-Member der [**D3DCAPS9-Struktur.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) Im folgenden Codebeispiel wird die [**IDirect3DDevice9::GetDeviceCaps-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) verwendet, um diese Größe abzurufen.


```
D3DCAPS9 d3dCaps;
    
m_pD3DDevice->GetDeviceCaps( &d3dCaps );
IndexedMatrixMaxSize = d3dCaps.MaxVertexBlendMatrixIndex;
```



Wenn der in MaxVertexBlendMatrixIndex festgelegte Wert 0 ist, unterstützt das Gerät keine indizierten Matrizen.

> [!Note]  
> Wenn die Softwarevertexverarbeitung verwendet wird, können 256 Matrizen für indiziertes Vertexblending mit oder ohne normales Mischen verwendet werden.

 

## <a name="passing-matrix-indices-to-direct3d"></a>Übergeben von Matrixindizes an Direct3D

Weltmatrixindizes können mithilfe von Legacy-Vertex-Shadern (FVF) oder Deklarationen an Direct3D übergeben werden.

Das folgende Codebeispiel zeigt, wie Ältere Vertex-Shader verwendet werden.


```
struct VERTEX
{
    float x,y,z;
    float weight;
    DWORD matrixIndices;
    float normal[3];
};
    
#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZB2 | D3DFVF_LASTBETA_UBYTE4 |
                             D3DFVF_NORMAL);
```



Wenn ein Legacy-Vertex-Shader verwendet wird, werden Matrixindizes zusammen mit Scheitelpunktpositionen mithilfe von D3DFVF \_ XYZBn-Flags übergeben. Matrixindizes werden als Bytes innerhalb eines DWORD übergeben und müssen unmittelbar nach der letzten Scheitelpunktgewichtung vorhanden sein. Scheitelpunktgewichtungen werden auch mit D3DFVF \_ XYZBn übergeben. Ein gepacktes DWORD enthält index3, index2, index1 und index0, wobei index0 sich im niedrigsten Byte des DWORD befindet. Die Anzahl der verwendeten Weltmatrixindizes entspricht der Zahl, die an die Anzahl der Matrizen übergeben wird, die für das Mischen verwendet werden, wie von [**D3DRS \_ VERTEXBLEND definiert.**](./d3drenderstatetype.md)

Wenn eine Deklaration verwendet wird, definiert D3DVSDE \_ BLENDINDICES das Eingabevertexregister zum Erhalten von Matrixindizes. Matrixindizes müssen als D3DVSDT \_ UBYTE4 übergeben werden.

Das folgende Codebeispiel zeigt, wie Deklarationen verwendet werden. Beachten Sie, dass die Reihenfolge der Komponenten nur dann von Bedeutung ist, wenn ein Vertex-Shader mit fester Funktion verwendet wird.

Hier ist die Scheitelpunktdeklaration.


```
struct VERTEX
{
    float x,y,z;
    float weight;
    DWORD matrixIndices;
    float normal[3];
}
```



Hier ist die entsprechende Registerdeklaration.


```
// Create the shader declaration.
D3DVERTEXELEMENT9 decl[] = 
{
    { 0, 0,  D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0 },
    { 0, 12, D3DDECLTYPE_FLOAT1, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BLENDWEIGHT, 0 },
    { 0, 16, D3DDECLTYPE_UBYTE4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BLENDINDICES, 0 },
    { 0, 20, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL, 0 },
    D3DDECL_END()
};
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Indiziertes Vertexblending](indexed-vertex-blending.md)
</dt> </dl>

 

 
