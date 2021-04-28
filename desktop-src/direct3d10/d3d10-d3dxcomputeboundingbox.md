---
description: 'D3DXComputeBoundingBox-Funktion (D3DX10math.h): Berechnet ein koordinatenachsenorientiertes Begrenzungsfeld.'
ms.assetid: 1b8f328c-2fe1-462e-b464-c8dd9dc03e67
title: D3DXComputeBoundingBox-Funktion (D3DX10math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2a12e7e302fb36ffb8856e6402f110e01bb2afb2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103528"
---
# <a name="d3dxcomputeboundingbox-function-d3dx10mathh"></a>D3DXComputeBoundingBox-Funktion (D3DX10math.h)

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

Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

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

Anzahl oder Anzahl von Bytes zwischen Scheitelzeichen.

</dd> <dt>

*pMin* \[ out\]
</dt> <dd>

Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3d10-d3dxvector3.md) die die zurückgegebene linke untere Ecke des Begrenzungsfelds beschreibt.

</dd> <dt>

*pMax* \[ out\]
</dt> <dd>

Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3d10-d3dxvector3.md) die die zurückgegebene rechte obere Ecke des Begrenzungsfelds beschreibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mesh-Funktionen](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
