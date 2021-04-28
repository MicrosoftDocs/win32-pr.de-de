---
description: 'D3DXComputeBoundingSphere-Funktion (D3DX9Mesh.h): Berechnet eine Begrenzungskugel für das Gitternetz.'
ms.assetid: efa1365b-fe3a-4165-a3cb-bc1cd2ba03c0
title: D3DXComputeBoundingSphere-Funktion (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeBoundingSphere
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dbfccb13dfe15b06de98ddba114cdc62c5f4ec05
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115818"
---
# <a name="d3dxcomputeboundingsphere-function-d3dx9meshh"></a>D3DXComputeBoundingSphere-Funktion (D3DX9Mesh.h)

Berechnet eine Begrenzungskugel für das Gitternetz.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXComputeBoundingSphere(
  _In_  const D3DXVECTOR3 *pFirstPosition,
  _In_        DWORD       NumVertices,
  _In_        DWORD       dwStride,
  _Out_       D3DXVECTOR3 *pCenter,
  _Out_       FLOAT       *pRadius
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pFirstPosition* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf die erste Position.

</dd> <dt>

*NumVertices* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Anzahl der Scheitelzeichen.

</dd> <dt>

*dwStride* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Anzahl von Bytes zwischen Positionsvektoren. Verwenden [**Sie GetNumBytesPerVertex,**](id3dxbasemesh--getnumbytespervertex.md) [**D3DXGetFVFVertexSize**](d3dxgetfvfvertexsize.md)oder [**D3DXGetDeclVertexSize,**](d3dxgetdeclvertexsize.md) um das Scheitelpunkt-Stride zu erhalten.

</dd> <dt>

*pCenter* \[ out\]
</dt> <dd>

Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

[**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die den Koordinatenmittelbereich der zurückgegebenen Begrenzungskugel definiert.

</dd> <dt>

*pRadius* \[ out\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Radius der zurückgegebenen Begrenzungskugel.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Sein: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mesh-Funktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
