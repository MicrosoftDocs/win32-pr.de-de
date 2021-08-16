---
description: Führt replizierte Scheitelungen zusammen, die über gleiche Attribute verfügen. Diese Methode verwendet angegebene epsilon-Werte für Gleichheitsvergleiche.
ms.assetid: bddf6e0c-55a1-40d2-8681-e7f0f9002bfa
title: D3DXWeldVertices-Funktion (D3DX9Mesh.h)
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
ms.openlocfilehash: 3ce6a9a05573467e0725785a6272e5542c4f871080fe221ac12078b17165eb5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118803273"
---
# <a name="d3dxweldvertices-function"></a>D3DXWeldVertices-Funktion

Führt replizierte Scheitelungen zusammen, die über gleiche Attribute verfügen. Diese Methode verwendet angegebene epsilon-Werte für Gleichheitsvergleiche.

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

*pMesh* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**

Zeiger auf ein [**ID3DXMesh-Objekt,**](id3dxmesh.md) das Gittermodell, aus dem Scheitelpunkts gezähnt werden.

</dd> <dt>

*Flags* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Kombination aus mindestens einem Flag von [**D3DXWELDEPSILONSFLAGS**](./d3dxweldepsilonsflags.md).

</dd> <dt>

*pEpsilons* \[ In\]
</dt> <dd>

Typ: **const [**D3DXWeldEpsilons**](d3dxweldepsilons.md) \***

Zeiger auf eine [**D3DXWeldEpsilons-Struktur,**](d3dxweldepsilons.md) in der die epsilon-Werte angegeben werden, die für diese Methode verwendet werden sollen. Verwenden **Sie NULL,** um alle Strukturmitglieder auf den Standardwert 1.0e-6f zu initialisieren.

</dd> <dt>

*pAdjacencyIn* \[ In\]
</dt> <dd>

Typ: **const [**DWORD**](../winprog/windows-data-types.md) \***

Zeiger auf ein Array von drei DWORDs pro Gesicht, die die drei Nachbarn für jedes Gesicht im Quellgitter angeben. Wenn der Rand keine angrenzenden Gesichter hat, wird der Wert 0xffffffff. Wenn dieser Parameter auf NULL festgelegt **ist,** [**wird ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md) aufgerufen, um logische Adjacency-Informationen zu erstellen.

</dd> <dt>

*pAdjacencyOut* \[ in, out\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Zeiger auf ein Array von drei DWORDs pro Gesicht, die die drei Nachbarn für jedes Gesicht im optimierten Gitter angeben. Wenn der Rand keine angrenzenden Gesichter hat, wird der Wert 0xffffffff.

</dd> <dt>

*pFaceRemap* \[ out\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Ein Array von DWORDs pro Gesicht, das das ursprüngliche Gitternetzgesicht identifiziert, das jedem Gesicht im Gitternetz entspricht.

</dd> <dt>

*ppVertexRemap* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Adresse eines Zeigers auf eine [**ID3DXBuffer-Schnittstelle,**](id3dxbuffer.md) die ein DWORD für jeden Scheitelpunkt enthält, das angibt, wie die neuen Scheitelpunkte den alten Scheitelpunkte zuordnen. Diese Neuzuordnung ist nützlich, wenn Sie externe Daten basierend auf der neuen Scheitelpunktzuordnung ändern müssen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Diese Funktion verwendet bereitgestellte Adjacency-Informationen, um die replizierten Punkte zu bestimmen. Scheitelungen werden basierend auf einem Epsilon-Vergleich zusammengeführt. Scheitelpunkt mit gleicher Position müssen bereits berechnet und durch punkt repräsentative Daten dargestellt worden sein.

Diese Funktion kombiniert logisch strukturierte Scheitelelemente, die ähnliche Komponenten aufweisen, z. B. Normal- oder Texturkoordinaten innerhalb von pEpsilons.

Der folgende Beispielcode ruft diese Funktion mit aktivierter -Funktion auf. Scheitelpunkte werden mithilfe von Epsilonwerten für normale Vektor- und Scheitelpunktposition verglichen. Ein Zeiger wird auf ein Array zur Neuzuordnung der Gesichtserkennung *(pFaceRemap) zurückgegeben.*


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
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mesh-Funktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
