---
description: Generiert ein vereinfachtes Gitternetz mithilfe der bereitgestellten Gewichtungen, die dem angegebenen MinValue möglichst nahe kommen.
ms.assetid: 589356a9-f272-4851-92ae-54dbecc0b234
title: D3DXSimplifyMesh-Funktion (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSimplifyMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3cc0bfe18afef7b91dbdf887500b485a446b154cb5775cbf950a7e712a332a9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749780"
---
# <a name="d3dxsimplifymesh-function"></a>D3DXSimplifyMesh-Funktion

Generiert ein vereinfachtes Gitternetz mithilfe der bereitgestellten Gewichtungen, die dem angegebenen MinValue möglichst nahe kommen.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXSimplifyMesh(
  _In_        LPD3DXMESH           pMesh,
  _In_  const DWORD                *pAdjacency,
  _In_  const D3DXATTRIBUTEWEIGHTS *pVertexAttributeWeights,
  _In_  const FLOAT                *pVertexWeights,
  _In_        DWORD                MinValue,
  _In_        DWORD                Options,
  _Out_       LPD3DXMESH           *ppMesh
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pMesh* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**

Zeiger auf eine [**ID3DXMesh-Schnittstelle,**](id3dxmesh.md) die das Quellgitternetz darstellt.

</dd> <dt>

*pAdjacency* \[ In\]
</dt> <dd>

Typ: **const [**DWORD**](../winprog/windows-data-types.md) \***

Zeiger auf ein Array von drei DWORDs pro Gesicht, die die drei Nachbarn für jedes Gesicht im Gitternetz angeben, die vereinfacht werden sollen.

</dd> <dt>

*pVertexAttributeWeights* \[ In\]
</dt> <dd>

Typ: **const [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) \***

Zeiger auf eine [**D3DXATTRIBUTEWEIGHTS-Struktur,**](d3dxattributeweights.md) die die Gewichtung für jede Scheitelpunktkomponente enthält. Wenn dieser Parameter auf **NULL festgelegt ist,** wird eine Standardstruktur verwendet. Siehe Hinweise.

</dd> <dt>

*pVertexWeights* \[ In\]
</dt> <dd>

Typ: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Zeiger auf ein Array von Scheitelpunktgewichtungen. Wenn dieser Parameter auf **NULL festgelegt ist,** werden alle Scheitelpunktgewichtungen auf 1,0 festgelegt.

</dd> <dt>

*MinValue* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Anzahl von Scheitelzeichen oder Gesichtern, je nach flag, das im *Options-Parameter* festgelegt ist, um das Quellgitternetz zu vereinfachen.

</dd> <dt>

*Optionen* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Gibt Vereinfachungsoptionen für das Gitternetz an. Eines der Flags in [**D3DXMESHSIMP**](./d3dxmeshsimp.md) kann festgelegt werden.

</dd> <dt>

*ppMesh* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Adresse eines Zeigers auf eine [**ID3DXMesh-Schnittstelle,**](id3dxmesh.md) die das zurückgegebene Vereinfachungsgitter darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Diese Funktion generiert ein  Gitternetz mit MinValue-Scheitelwerten oder Gesichtern.

Wenn der Vereinfachungsprozess das Gitternetz nicht auf *MinValue* reduzieren kann, ist der Aufruf trotzdem erfolgreich, da *MinValue* ein gewünschtes Minimum und kein absolutes Minimum ist.

Wenn *pVertexAttributeWeights auf* **NULL** festgelegt ist, werden der [**D3DXATTRIBUTEWEIGHTS-Standardstruktur die folgenden Werte zugewiesen.**](d3dxattributeweights.md)


```
D3DXATTRIBUTEWEIGHTS AttributeWeights;
    
AttributeWeights.Position  = 1.0;
AttributeWeights.Boundary =  1.0;
AttributeWeights.Normal   =  1.0;
AttributeWeights.Diffuse  =  0.0;
AttributeWeights.Specular =  0.0;
AttributeWeights.Tex[8]   =  {0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0};
```



Diese Standardstruktur sollte von den meisten Anwendungen verwendet werden, da nur geometrische und normale Anpassungen berücksichtigt werden. Nur in Sonderfällen müssen die anderen Memberfelder geändert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mesh-Funktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
