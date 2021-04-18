---
description: Generiert ein vereinfachtes Mesh mit den bereitgestellten Gewichtungen, die so nah wie möglich für den angegebenen MinValue sind.
ms.assetid: 589356a9-f272-4851-92ae-54dbecc0b234
title: D3DXSimplifyMesh-Funktion (D3DX9Mesh. h)
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
ms.openlocfilehash: 0258047631a41e31d108ba45531988e4cb6a35ae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355006"
---
# <a name="d3dxsimplifymesh-function"></a>D3DXSimplifyMesh-Funktion

Generiert ein vereinfachtes Mesh mit den bereitgestellten Gewichtungen, die so nah wie möglich für den angegebenen MinValue sind.

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

*pmesh* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**

Zeiger auf eine [**ID3DXMesh**](id3dxmesh.md) -Schnittstelle, die das quellmesh darstellt.

</dd> <dt>

*padjacency* \[ in\]
</dt> <dd>

Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***

Zeiger auf ein Array von drei DWORDs pro Gesicht, das die drei Nachbarn für jedes Gesicht im Mesh angibt, das vereinfacht werden soll.

</dd> <dt>

*pvertexattributegewichtungen* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) \***

Zeiger auf eine [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) -Struktur, die die Gewichtung für jede Scheitelpunkt Komponente enthält. Wenn dieser Parameter auf **null** festgelegt ist, wird eine Standardstruktur verwendet. Siehe Hinweise.

</dd> <dt>

*pvertexgewichtungen* \[ in\]
</dt> <dd>

Typ: Konstante **[**float**](../winprog/windows-data-types.md) \***

Zeiger auf ein Array von Vertex-Gewichtungen. Wenn dieser Parameter auf **null** festgelegt ist, werden alle Scheitelpunkt Gewichtungen auf 1,0 festgelegt.

</dd> <dt>

*MinValue* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Anzahl der Scheitel Punkte oder Gesichter, abhängig von dem im *options* -Parameter festgelegten Flag, um das quellmesh zu vereinfachen.

</dd> <dt>

*Optionen* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Gibt Vereinfachungs Optionen für das Mesh an. Eines der Flags in [**D3DXMESHSIMP**](./d3dxmeshsimp.md) kann festgelegt werden.

</dd> <dt>

*ppmesh* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Adresse eines Zeigers auf eine [**ID3DXMesh**](id3dxmesh.md) -Schnittstelle, die das zurückgegebene Vereinfachungs Mesh darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.

## <a name="remarks"></a>Bemerkungen

Diese Funktion generiert ein Mesh, das über *MinValue* -Scheitel Punkte oder Gesichter verfügt.

Wenn das Mesh durch den Vereinfachungsprozess nicht auf *MinValue* reduziert werden kann, ist der-Vorgang weiterhin erfolgreich, da *MinValue* ein gewünschter Minimalwert und kein absolutes Minimalwert ist.

Wenn *pvertexattributegewichtungen* auf **null** festgelegt ist, werden die folgenden Werte der [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) -Standardstruktur zugewiesen.


```
D3DXATTRIBUTEWEIGHTS AttributeWeights;
    
AttributeWeights.Position  = 1.0;
AttributeWeights.Boundary =  1.0;
AttributeWeights.Normal   =  1.0;
AttributeWeights.Diffuse  =  0.0;
AttributeWeights.Specular =  0.0;
AttributeWeights.Tex[8]   =  {0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0};
```



Diese Standardstruktur sollte von den meisten Anwendungen verwendet werden, da Sie nur eine geometrische und normale Anpassung berücksichtigt. Nur in besonderen Fällen müssen die anderen Mitglieds Felder geändert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mesh-Funktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
