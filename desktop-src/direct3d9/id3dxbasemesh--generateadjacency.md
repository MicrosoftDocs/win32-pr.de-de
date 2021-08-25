---
description: 'ID3DXBaseMesh::GenerateAdjacency-Methode: Generiert eine Liste von Gitternetzrändern sowie eine Liste von Gesichtern, die die einzelnen Ränder gemeinsam verwenden.'
ms.assetid: 9d52290f-1c9e-43a7-b239-35cd54e36466
title: ID3DXBaseMesh::GenerateAdjacency-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GenerateAdjacency
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d51070b5b67b50859338943a60e44cbb224e572ab9e5704e56940328a65479f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848530"
---
# <a name="id3dxbasemeshgenerateadjacency-method"></a>ID3DXBaseMesh::GenerateAdjacency-Methode

Generieren Sie eine Liste von Gitternetzrändern sowie eine Liste von Gesichtern, die die einzelnen Ränder gemeinsam haben.

## <a name="syntax"></a>Syntax


```C++
HRESULT GenerateAdjacency(
  [in] FLOAT Epsilon,
  [in] DWORD *pAdjacency
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Epsilon* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Gibt an, dass Scheitelungen, die sich an der Position von kleiner als epsilon unterscheiden, als zufällig behandelt werden sollen.

</dd> <dt>

*pAdjacency* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Zeiger auf ein Array von drei DWORDs pro Gesicht, die mit den Indizes benachbarter Gesichter gefüllt werden sollen. Die Anzahl der Bytes in diesem Array muss mindestens \* [**3 ID3DXBaseMesh::GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof(DWORD) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Nachdem eine Anwendung Adjazienzinformationen für ein Gitternetz generiert hat, können die Gitternetzdaten für eine bessere Zeichnungsleistung optimiert werden.

Die Reihenfolge der Einträge im Adjacency-Puffer wird durch die Reihenfolge der Scheitelpunktindizes im Indexpuffer bestimmt. Das benachbarte Dreieck 0 entspricht immer dem Rand zwischen den Indizes der Ecken 0 und 1. Das angrenzende Dreieck 1 entspricht immer dem Rand zwischen den Indizes der Ecken 1 und 2, während das angrenzende Dreieck 2 dem Rand zwischen den Indizes der Ecken 2 und 0 entspricht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> <dt>

[**ID3DXMesh::Optimize**](id3dxmesh--optimize.md)
</dt> <dt>

[**ID3DXMesh::OptimizeInplace**](id3dxmesh--optimizeinplace.md)
</dt> </dl>

 

 
