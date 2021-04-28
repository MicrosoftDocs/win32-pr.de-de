---
description: 'D3DXComputeBoundingBox-Funktion (D3DX9Mesh.h): Berechnet ein koordinatenachsenorientiertes Begrenzungsfeld.'
ms.assetid: 74e1b84e-1264-49eb-9172-7842af7e25e0
title: D3DXComputeBoundingBox-Funktion (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeBoundingBox
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 39fdf4123781b84d87ec1c9d790eb5ffae058892
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115828"
---
# <a name="d3dxcomputeboundingbox-function-d3dx9meshh"></a>D3DXComputeBoundingBox-Funktion (D3DX9Mesh.h)

Berechnet ein koordinatenachsenorientiertes Begrenzungsfeld.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXComputeBoundingBox(
  _In_  const D3DXVECTOR3 *pFirstPosition,
  _In_        DWORD       NumVertices,
  _In_        DWORD       dwStride,
  _Out_       D3DXVECTOR3 *pMin,
  _Out_       D3DXVECTOR3 *pMax
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

Anzahl der Scheitelpunkte.

</dd> <dt>

*dwStride* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Anzahl oder Anzahl der Bytes zwischen Scheitelpunkten.

</dd> <dt>

*pMin* \[ out\]
</dt> <dd>

Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die die zurückgegebene linke untere Ecke des umgebenden Felds beschreibt. Siehe Hinweise.

</dd> <dt>

*pMax* \[ out\]
</dt> <dd>

Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die die zurückgegebene rechte obere Ecke des umgebenden Felds beschreibt. Siehe Hinweise.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mesh-Funktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
