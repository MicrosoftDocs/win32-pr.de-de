---
description: Transformations Zustände 256-511 sind zum Speichern von bis zu 256 Matrizen reserviert, die mithilfe von 8-Bit-Indizes indiziert werden können.
ms.assetid: 4c15cfc5-afdf-48d4-8fd1-b10cbe596a1c
title: Verwenden der indizierten vertexmischung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 120362e4a86081ff51aee9053d1526a9a08f014a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860086"
---
# <a name="using-indexed-vertex-blending-direct3d-9"></a>Verwenden der indizierten vertexmischung (Direct3D 9)

Transformations Zustände 256-511 sind zum Speichern von bis zu 256 Matrizen reserviert, die mithilfe von 8-Bit-Indizes indiziert werden können. Verwenden Sie das Makro [**D3DTS \_ worldmatrix**](d3dts-worldmatrix.md) , um die Indizes 0-255 den entsprechenden Transformations Zuständen zuzuordnen. Im folgenden Codebeispiel wird gezeigt, wie die [**IDirect3DDevice9:: setTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) -Methode verwendet wird, um die Matrix bei der Transformations Zustands Nummer 256 in eine Identitätsmatrix festzulegen.


```
D3DMATRIX matBlend1;
D3DXMatrixIdentity( &matBlend1 );
m_pD3DDevice->SetTransform( D3DTS_WORLDMATRIX(0), &matBlend );
```



Legen Sie zum Aktivieren oder Deaktivieren des indizierten Vertex-Mischungs Zustands den D3DRS \_ indexedvertexblendenable-Rendering-Zustand auf **true** fest. Wenn der renderzustand aktiviert ist, müssen Sie Matrix Indizes als gepackte DWords an jeden Scheitelpunkt übergeben. Wenn dieser renderzustand deaktiviert und die Scheitelpunkt Mischung aktiviert ist, entspricht er den Matrix Indizes 0, 1, 2 und 3 in jedem Scheitelpunkt. Im folgenden Codebeispiel wird die [**IDirect3DDevice9:: setrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) -Methode verwendet, um die indizierte Vertex-Mischung zu aktivieren.


```
m_pD3DDevice->SetRenderState( D3DRS_INDEXEDVERTEXBLENDENABLE, TRUE );
```



Legen Sie zum Aktivieren oder Deaktivieren der Scheitelpunkt Mischung den [**IDirect3DDevice9:: setrenderstate-renderzustand**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) auf einen anderen Wert als D3DRS \_ deaktiviert aus dem [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) -enumerierten Typ fest. Wenn dieser renderzustand nicht auf D3DRS deaktivieren festgelegt ist \_ , müssen Sie die erforderliche Anzahl von Gewichtungen für jeden Scheitelpunkt übergeben. Im folgenden Codebeispiel wird **IDirect3DDevice9:: setrenderstate** verwendet, um die Vertex-Mischung mit drei Gewichtungen für jeden Scheitelpunkt zu aktivieren.


```
m_pD3DDevice->SetRenderState( D3DRS_VERTEXBLEND, D3DVBF_3WEIGHTS );
```



## <a name="determining-indexed-vertex-blending-support"></a>Festlegen der Unterstützung für indizierte vertexblending

Überprüfen Sie den Member "maxvertexblendmatrixindex" der [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) -Struktur, um die maximale Größe für die indizierte Vertex-Mischungs Matrix zu ermitteln. Im folgenden Codebeispiel wird die [**IDirect3DDevice9:: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) -Methode verwendet, um diese Größe abzurufen.


```
D3DCAPS9 d3dCaps;
    
m_pD3DDevice->GetDeviceCaps( &d3dCaps );
IndexedMatrixMaxSize = d3dCaps.MaxVertexBlendMatrixIndex;
```



Wenn der in maxvertexblendmatrixindex festgelegte Wert 0 ist, unterstützt das Gerät keine indizierten Matrizen.

> [!Note]  
> Wenn die Verarbeitung von Software Scheitel Punkten verwendet wird, können 256 Matrizen für indizierte vertexmischungs Vorgänge mit oder ohne normale Vermischung verwendet werden.

 

## <a name="passing-matrix-indices-to-direct3d"></a>Übergeben von Matrix Indizes an Direct3D

World Matrix-Indizes können mithilfe von Legacy-Vertex-Shader-FVF-oder-Deklarationen an Direct3D übermittelt werden.

Das folgende Codebeispiel zeigt, wie ältere Scheitelpunkt-Shader verwendet werden.


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



Wenn ein veralteter Scheitelpunkt-Shader verwendet wird, werden Matrix Indizes mithilfe von D3DFVF xyzbn-Flags mit Scheitelpunkt Positionen übermittelt \_ . Matrix Indizes werden in einem DWORD als Bytes und müssen direkt hinter der letzten Scheitelpunkt Gewichtung vorhanden sein. Vertex-Gewichtungen werden auch mit D3DFVF \_ xyzbn übermittelt. Ein gepacktes DWORD enthält index3, index2, index1 und index0, wobei sich index0 im niedrigsten Byte des DWORD befindet. Die Anzahl der verwendeten World-Matrix-Indizes ist gleich der Zahl, die an die Anzahl von Matrizen, die für die Mischung verwendet werden, gemäß [**D3DRS \_ vertexblend**](./d3drenderstatetype.md), festgelegt wurde.

Wenn eine Deklaration verwendet wird, \_ definiert D3DVSDE blendindices das Eingabe Vertex-Register, von dem Matrix Indizes abzurufen sind. Matrix Indizes müssen als D3DVSDT \_ UBYTE4.

Das folgende Codebeispiel zeigt, wie Deklarationen verwendet werden. Beachten Sie, dass die Reihenfolge der Komponenten nicht mehr wichtig ist, es sei denn, Sie verwenden einen Vertex-Shader fester Funktion.

Hier ist die Vertex-Deklaration.


```
struct VERTEX
{
    float x,y,z;
    float weight;
    DWORD matrixIndices;
    float normal[3];
}
```



Hier ist die entsprechende Register-Deklaration.


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

[Indiziertes Vertex-Blending](indexed-vertex-blending.md)
</dt> </dl>

 

 
