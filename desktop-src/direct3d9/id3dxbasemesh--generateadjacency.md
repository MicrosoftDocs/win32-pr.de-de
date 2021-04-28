---
description: 'ID3DXBaseMesh::GenerateAdjaency-Methode: Generieren Sie eine Liste von Gitternetzkanten sowie eine Liste von Gesichtern, die die einzelnen Kanten gemeinsam nutzen.'
ms.assetid: 9d52290f-1c9e-43a7-b239-35cd54e36466
title: ID3DXBaseMesh::GenerateAdencyency-Methode (D3DX9Mesh.h)
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
ms.openlocfilehash: 783ed7ad61337e606793b9b467e4b17fddd7ecd2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115458"
---
# <a name="id3dxbasemeshgenerateadjacency-method"></a>ID3DXBaseMesh::GenerateAdjaency-Methode

Generieren Sie eine Liste von Gitternetzrändern sowie eine Liste von Gesichtern, die die einzelnen Kanten gemeinsam nutzen.

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

Gibt an, dass Scheitelpunkte, die sich in der Position um weniger als epsilon unterscheiden, als zufällig behandelt werden sollen.

</dd> <dt>

*pAdjazenz* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Zeiger auf ein Array von drei DWORDs pro Gesicht, das mit den Indizes benachbarter Gesichter gefüllt werden soll. Die Anzahl der Bytes in diesem Array muss mindestens \* [**3 ID3DXBaseMesh::GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof(DWORD) betragen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Bemerkungen

Nachdem eine Anwendung Adjazenzinformationen für ein Gitternetz generiert hat, können die Gitternetzdaten optimiert werden, um eine bessere Zeichnungsleistung zu erzielen.

Die Reihenfolge der Einträge im Adjazenzpuffer wird durch die Reihenfolge der Scheitelpunktindizes im Indexpuffer bestimmt. Das angrenzende Dreieck 0 entspricht immer dem Rand zwischen den Indizes der Ecken 0 und 1. Das angrenzende Dreieck 1 entspricht immer dem Rand zwischen den Indizes der Ecken 1 und 2, während das angrenzende Dreieck 2 dem Rand zwischen den Indizes der Ecken 2 und 0 entspricht.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> <dt>

[**ID3DXMesh::Optimize**](id3dxmesh--optimize.md)
</dt> <dt>

[**ID3DXMesh::OptimizeInplace**](id3dxmesh--optimizeinplace.md)
</dt> </dl>

 

 
