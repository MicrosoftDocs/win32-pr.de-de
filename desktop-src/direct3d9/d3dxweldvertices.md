---
description: Führt eine kombinieren von replizierten Vertices mit identischen Attributen aus. Diese Methode verwendet angegebene Epsilon-Werte für Gleichheits Vergleiche.
ms.assetid: bddf6e0c-55a1-40d2-8681-e7f0f9002bfa
title: D3DXWeldVertices-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXWeldVertices
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 76e0a6f259bc8ba547a02b2e95cccf718d54e904
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762084"
---
# <a name="d3dxweldvertices-function"></a>D3DXWeldVertices-Funktion

Führt eine kombinieren von replizierten Vertices mit identischen Attributen aus. Diese Methode verwendet angegebene Epsilon-Werte für Gleichheits Vergleiche.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXWeldVertices(
  _In_          LPD3DXMESH       pMesh,
  _In_          DWORD            Flags,
  _In_    const D3DXWeldEpsilons *pEpsilons,
  _In_    const DWORD            *pAdjacencyIn,
  _Inout_       DWORD            *pAdjacencyOut,
  _Out_         DWORD            *pFaceRemap,
  _Out_         LPD3DXBUFFER     *ppVertexRemap
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pmesh* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**

Zeiger auf ein [**ID3DXMesh**](id3dxmesh.md) -Objekt, das Mesh, von dem Vertices geschweißt werden.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Eine Kombination aus einem oder mehreren Flags aus [**D3DXWELDEPSILONSFLAGS**](./d3dxweldepsilonsflags.md).

</dd> <dt>

*pepsilons* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXWeldEpsilons**](d3dxweldepsilons.md) \***

Zeiger auf eine [**D3DXWeldEpsilons**](d3dxweldepsilons.md) -Struktur, die die Epsilon-Werte angibt, die für diese Methode verwendet werden sollen. Verwenden Sie **null** , um alle Strukturmember mit einem Standardwert von 1.0 e-6f zu initialisieren.

</dd> <dt>

*padjackocyin* \[ in\]
</dt> <dd>

Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***

Zeiger auf ein Array von drei DWORDs pro Gesicht, das die drei Nachbarn für jedes Gesicht im quellmesh angibt. Wenn der Rand keine angrenzenden Gesichter hat, ist der Wert 0xFFFFFFFF. Wenn dieser Parameter auf **null** festgelegt ist, wird [**ID3DXBaseMesh:: generateseency**](id3dxbasemesh--generateadjacency.md) aufgerufen, um logische Informations Informationen zu erstellen.

</dd> <dt>

*padjacumcyout* \[ in, out\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Zeiger auf ein Array von drei DWORDs pro Gesicht, das die drei Nachbarn für jedes Gesicht im optimierten Mesh angibt. Wenn der Rand keine angrenzenden Gesichter hat, ist der Wert 0xFFFFFFFF.

</dd> <dt>

*pfakeremap* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Ein Array von DWords, eines pro Gesicht, das die ursprüngliche Gitterfläche angibt, die jedem Gesicht im geschweißten Mesh entspricht.

</dd> <dt>

*ppvertexremap* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Adresse eines Zeigers auf eine [**ID3DXBuffer**](id3dxbuffer.md) -Schnittstelle, die ein DWORD für jeden Scheitelpunkt enthält, der angibt, wie die neuen Scheitel Punkten den alten Scheitel Punkten zugeordnet werden. Diese Neuzuordnung ist nützlich, wenn Sie externe Daten basierend auf der neuen Scheitelpunkt Zuordnung ändern müssen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ oudefmemory.

## <a name="remarks"></a>Bemerkungen

Diese Funktion verwendet die angegebenen Informationen zum Ermitteln der Punkte, die repliziert werden. Vertices werden auf Grundlage eines Epsilon-Vergleichs zusammengeführt. Vertices mit gleicher Position müssen bereits berechnet und durch Punkt repräsentative Daten dargestellt werden.

Diese Funktion kombiniert logisch versießte Scheitel Punkte, die ähnliche Komponenten aufweisen, wie z. b. normale oder Texturkoordinaten innerhalb von pepsilons.

Im folgenden Beispielcode wird diese Funktion mit aktiviertem Schweißen aufgerufen. Vertices werden mithilfe von Epsilon-Werten für den normalen Vektor und die Scheitelpunkt Position verglichen. Ein Zeiger wird an ein Flächen *kartogramm (pfakeremap*) zurückgegeben.


```
TCHAR            strMediaPath[512];       // X-file path 
LPD3DXBUFFER     pAdjacencyBuffer = NULL; // adjacency data buffer
LPD3DXBUFFER     pD3DXMtrlBuffer  = NULL; // material buffer
LPD3DXMESH       pMesh            = NULL; // mesh object
DWORD            m_dwNumMaterials;        // number of materials
D3DXWELDEPSILONS Epsilons;                // structure with epsilon values
DWORD            *pFaceRemap[65536];      // face remapping array
DWORD            i;                       // internal variable
    
    // Load the mesh from the specified file
    hr = D3DXLoadMeshFromX ( strMediaPath,
                         D3DXMESH_MANAGED,
                         m_pd3dDevice,
                         &pAdjacencyBuffer,
                         &pD3DXMtrlBuffer,
                         NULL,
                         &m_dwNumMaterials,
                         &pMesh ) )
                             
    if( FAILED( hr ) ) 
      goto End;              // Go to error handling
    
    // Set epsilon values
    Epsilons.Normal = 0.001;
    Epsilons.Position = 0.1;
    
    // Weld the vertices
    for( i=0; i < 65536; i++ )
    { 
        pFaceRemap[i] = 0; 
    }
    
    hr = D3DXWeldVertices ( pMesh,
                            D3DXWELDEPSILONS_WELDPARTIALMATCHES,
                            &Epsilons,
                            (DWORD*)pAdjacencyBuffer->GetBufferPointer(),
                            (DWORD*)pAdjacencyBuffer->GetBufferPointer(),
                            (DWORD*)pFaceRemap,
                            NULL )
                            
    if( FAILED( hr ) ) 
      goto End;              // Go to error handling
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mesh-Funktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
